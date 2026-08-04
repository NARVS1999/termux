---
name: merge-anki-cards
description: >
  Merge all per-phase cloze and basic CSV files in a folder into two combined files:
  {prefix}-all-cloze.csv and {prefix}-all-basic.csv, ready for a single Anki import.
  Use when the user says "create all cloze and basic", "merge all cards", "make combined csv
  for X", "combine all phase cards", or "all cards from {folder}". Works on any folder holding
  {prefix}-phase*-cloze.csv / {prefix}-phase*-basic.csv files (e.g. prep/, react/, backend/).
---

# Merge Anki Cards Skill

Merges per-phase Anki CSVs in an existing folder into two combined files so the user can import all cards of a topic in one go.

## Input

Any folder containing per-phase card files:

- `{prefix}-phase{N}-cloze.csv` (one or more, e.g. `prep-phase1-cloze.csv`, `prep-phase2-cloze.csv`, `prep-phase40-42-cloze.csv`)
- `{prefix}-phase{N}-basic.csv` (same phases)

`{prefix}` is the shared name before `-phase` in the filenames (e.g. `prep`, `react`, `backend`).

## Output

Two files written into the **same folder**:

- `{prefix}-all-cloze.csv`
- `{prefix}-all-basic.csv`

Both follow repo conventions: **no header row** — the file starts directly with the first card row, `Cloze` / `Application` type column, empty hint column.

## Workflow

### Step 1: Detect Prefix & Collect Files

1. List `*.csv` files in the target folder (default: folder of the referenced topic, e.g. `prep/`)
2. Match files against `*-phase*-cloze.csv` and `*-phase*-basic.csv`
3. Derive `{prefix}` from the first match (everything before `-phase`)
4. If no phase files found: report error and list folders that contain them

### Step 2: Concatenate in Numeric Phase Order

```bash
ls {folder}/*-cloze.csv | sort -V | xargs cat > {folder}/{prefix}-all-cloze.csv
ls {folder}/*-basic.csv | sort -V | xargs cat > {folder}/{prefix}-all-basic.csv
```

- **`sort -V` (version sort) is required** — plain alphabetical sort would put `phase10` before `phase2`
- **Raw concatenation only** — never re-parse/re-serialize: quoted fields may span multiple lines, and rewriting would corrupt them or add a header
- Do not reorder or edit card rows; phase files are already in the right order internally
- Combined phases (e.g. `phase11-12`, `phase40-42`) sort naturally into place by their leading number

### Step 3: Verify

Run a Python check on both merged files:

1. Every row has exactly 4 fields (valid CSV parse)
2. No duplicate rows (compare across the merged set, `sort | uniq -d` must be empty)
3. ASCII-only content (no Chinese/Cyrillic/foreign script chars — a past repo fix removed these)
4. No backslash-escaped quotes (`\"`) — quotes inside fields must be `""`-doubled (RFC 4180); backslashes are literal, never escaped (PHP namespaces `App\Models`, composer key `App\\`)

Expected counts: number of cloze cards = sum of rows across all `*-cloze.csv` phase files; same logic for basic.

### Step 4: Commit & Push

```bash
git add {folder}/{prefix}-all-cloze.csv {folder}/{prefix}-all-basic.csv
git commit -m "add {prefix} all cloze and basic cards"
git push origin main
```

Single commit containing both files (repo git workflow: direct commits to `main`, push to origin).

### Step 5: Report

Report:
- Total cloze cards and basic cards in the merged files
- File paths
- Commit hash pushed

## Edge Cases

| Case | Handling |
|------|----------|
| No phase files in folder | Report error, list available `*-SKILL.md`-style folders or other folders with phase CSVs |
| Only cloze or only basic files present | Merge the group that exists, report the other as missing |
| Duplicate rows found | Remove duplicates before writing (report what was removed) |
| Non-ASCII characters found | Report them, do not commit until fixed (matches repo ASCII-only rule) |
| Empty merged file | Report error, do not commit |

## Anki Import Note

Tell the user to import `{prefix}-all-cloze.csv` and `{prefix}-all-basic.csv` **separately** (one note type per import) and tick "File has no headers" in the import dialog — same as per-phase files.
