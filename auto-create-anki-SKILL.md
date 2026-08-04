---
name: auto-create-anki
description: >
  Automatically generate Anki cards from a roadmap file, section by section, fully automatic.
  Use when the user says "auto-create-anki for X-roadmap.md", "generate all cards for X roadmap",
  "auto anki for X", or "create cards from X roadmap".
  Reads the roadmap, generates Taglish cloze + basic CSVs per phase following anki-taglish-cards rules,
  commits & pushes, marks phases complete, and repeats until all sections are done.
  Skips phases already marked [x]. Processes entire roadmap without pausing.
---

# Auto-Create Anki Cards from Roadmap

Automates the full Anki card generation workflow: read roadmap → generate cards → commit → mark done → repeat.

## Prerequisites

This skill **references** `anki-taglish-cards-SKILL.md` for card generation rules. Always follow those rules for cloze and basic card formats.

## Input

User provides:
- A roadmap file: `auto-create-anki for {topic}-roadmap.md`
- Or just the topic: `auto-create-anki react` (look for `{topic}/{topic}-roadmap.md` in the `{topic}/` folder)

## Topic Extraction

From the input, extract the `{topic}`:
- `auto-create-anki for vue-roadmap.md` → topic = `vue`
- `auto-create-anki react` → topic = `react`
- `auto-create-anki for docker-roadmap.md` → topic = `docker`

This `{topic}` is used for:
- CSV file naming: `{topic}/{topic}-phase{N}-cloze.csv`, `{topic}/{topic}-phase{N}-basic.csv`
- Git commit messages: `{topic} phase {start} - {end} cards`

## Workflow (Fully Automatic — No Pauses)

### Step 1: Read & Parse Roadmap
1. Read `{topic}/{topic}-roadmap.md`
2. Parse all `## Section` headers and their phases
3. For each phase line, check:
   - `[x]` → already done, **skip**
   - `[ ]` → needs cards, **process**
4. If all phases in a section are `[x]`, skip the entire section (no commits)

### Step 2: Per Section Loop
Process each section sequentially. For each section with unchecked phases:

#### 2a. Generate CSV Files
For each unchecked `[ ]` phase in the section:

**Cloze CSV** (`{topic}-phase{N}-cloze.csv`):
```
Cloze,"Ang {{c1::keyword}} ay {Taglish explanation}.",,keyword
Cloze,"Ang {{c1::keyword2}} ay {Taglish explanation}.",,keyword2
...
```
- **No header row** — file starts directly with the first card
- **8–11 cards** per phase
- Cover all keywords/concepts from the phase description
- Use `{{c1::keyword}}` cloze syntax
- Sentences start with `Ang` or `Sa`
- Hint column is always empty
- Back column repeats the keyword

**Basic CSV** (`{topic}-phase{N}-basic.csv`):
```
Application,"Paano {verb} {object}?",,"{one-line answer}"
Application,"Paano {verb} {object}?",,"{one-line answer}"
...
```
- **No header row** — file starts directly with the first card
- **5 cards** per phase
- Questions start with `Paano`
- Answers are single line of code or brief Taglish explanation
- Hint column is always empty

**CSV quoting (both types, strict — a past repo fix rewrote 48 files for this):**
- Never backslash-escape quotes (`\"` is invalid RFC 4180; GitHub preview breaks with "Any value after quoted field isn't allowed")
- Quotes inside a quoted field are **doubled** (`""`): `<Link href=""/about"">About</Link>`
- Backslashes are literal — never escaped (PHP namespace `App\Models`, composer key `App\\` with exactly two literal backslashes)

#### 2b. Git Commit & Push (CSVs)
```bash
git add {topic}/{topic}-phase{start}-cloze.csv {topic}/{topic}-phase{start}-basic.csv ... {topic}/{topic}-phase{end}-cloze.csv {topic}/{topic}-phase{end}-basic.csv
git commit -m "{topic} phase {start} - {end} cards"
git push origin main
```

#### 2c. Update Roadmap
- Change `[ ]` to `[x]` for each phase processed in this section
- Edit the roadmap file

#### 2d. Git Commit & Push (Roadmap)
```bash
git add {topic}/{topic}-roadmap.md
git commit -m "mark done {topic} phase {start} - {end}"
git push origin main
```

#### 2e. Next Section
- Move to the next section immediately
- No user confirmation needed
- Repeat until all sections are processed

### Step 3: Create Combined All-Cards Files

After all sections are processed, merge every per-phase CSV into two combined files (default behavior, do not skip):

```bash
ls {topic}/{topic}-phase*-cloze.csv | sort -V | xargs cat > {topic}/{topic}-all-cloze.csv
ls {topic}/{topic}-phase*-basic.csv | sort -V | xargs cat > {topic}/{topic}-all-basic.csv
```

- `sort -V` (version sort) — alphabetical would put `phase10` before `phase2`
- **Raw concatenation only** — quoted fields may span multiple lines; never re-parse/re-serialize
- No header row — matches per-phase files
- Verify both merged files: every row exactly 4 fields, no duplicate rows, ASCII-only, no backslash-escaped quotes (`\"` — must be `""` doubling, see quoting rules above)
- Report errors if any file fails verification; fix before committing

#### Git Commit & Push (Merged CSVs) — separate commit, after the last phase batch
```bash
git add {topic}/{topic}-all-cloze.csv {topic}/{topic}-all-basic.csv
git commit -m "add {topic} all cloze and basic cards"
git push origin main
```

> This step matches the process in `merge-anki-cards-SKILL.md` — run that skill standalone when the user asks to merge an already-completed folder.

### Step 4: Summary Report
After all sections are done, report:
- Total CSV files created (per-phase + 2 merged)
- Total cards generated (cloze + basic, including merged totals)
- Total git commits pushed
- Confirmation that all phases are now `[x]`
- Paths of the two merged files

## Card Generation Rules (from anki-taglish-cards-SKILL.md)

### Cloze Cards
- Format: `Ang {{c1::keyword}} ay {explanation in Taglish}.`
- One keyword per card
- Explanation must provide enough context to infer the keyword
- English technical terms left untranslated
- 8–11 cards per phase

### Basic (Application) Cards
- Format: `Paano {verb} {object}?`
- Answer: one line of code OR one short sentence in Taglish
- Never multi-line or multi-step answers
- 5 cards per phase

### Taglish Convention
- Tagalog connectors: `ang`, `ay`, `ginagamit`, `kapag`, `para sa`, `hindi`, `sa loob ng`, `mula sa`
- English technical terms: kept untranslated (e.g., `destructuring`, `React Router`, `SQL Injection`)
- Never translate code terms — it would be unnatural

## Phase Description Mapping

When generating cards for a phase like:
```
- [ ] **Phase 1** — ES6+ features: destructuring, spread/rest, template literals, arrow functions, optional chaining
```

Each subtopic after the colon becomes a card topic:
- `destructuring` → 1 cloze card + 1 basic card
- `spread/rest` → 1 cloze card + 1 basic card
- `template literals` → 1 cloze card + 1 basic card
- etc.

This ensures full coverage of the phase content.

## Skip Logic

```
For each section:
  unchecked_phases = [phase for phase in section.phases if phase.checkbox == '[ ]']
  if unchecked_phases is empty:
    SKIP section (no commits)
  else:
    process unchecked_phases
```

## File Naming Summary

| File | Format |
|------|--------|
| CSV (cloze) | `{topic}/{topic}-phase{N}-cloze.csv` |
| CSV (basic) | `{topic}/{topic}-phase{N}-basic.csv` |
| CSV (all cloze, merged) | `{topic}/{topic}-all-cloze.csv` |
| CSV (all basic, merged) | `{topic}/{topic}-all-basic.csv` |
| Roadmap | `{topic}/{topic}-roadmap.md` |

## Git Commit Messages

| Action | Message |
|--------|---------|
| CSV files | `{topic} phase {start} - {end} cards` |
| Roadmap update | `mark done {topic} phase {start} - {end}` |
| Merged CSV files | `add {topic} all cloze and basic cards` |

## Example Execution

User says: `auto-create-anki for react-roadmap.md`

1. Topic = `react`
2. Read `react/react-roadmap.md`
3. Section 1 (Phases 1-5): all `[ ]`
   - Generate 10 CSVs (5 cloze + 5 basic)
   - Commit: `react phase 1 - 5 cards`
   - Update roadmap: phases 1-5 → `[x]`
   - Commit: `mark done react phase 1 - 5`
4. Section 2 (Phases 6-12): all `[ ]`
   - Generate 14 CSVs (7 cloze + 7 basic)
   - Commit: `react phase 6 - 12 cards`
   - Update roadmap: phases 6-12 → `[x]`
   - Commit: `mark done react phase 6 - 12`
5. ... repeat until all 11 sections done
6. Merge all phase CSVs → `react/react-all-cloze.csv` + `react/react-all-basic.csv`
   - Commit: `add react all cloze and basic cards`
7. Report: "Created 94 per-phase CSV files + 2 merged files, ~500+ cards, 23 commits pushed"

## Error Handling

- If roadmap file not found: report error, list available `{topic}/*-roadmap.md` files
- If no unchecked phases: report "All phases already complete"
- If git push fails: report the error, suggest manual push
- If CSV generation fails for a phase: skip that phase, continue with next, report at end

## Output Format

After completion, present:
```
✅ Auto-create anki complete for {topic}

📊 Stats:
- {N} per-phase CSV files created
- {N} cloze cards generated
- {N} basic cards generated
- {N} total cards
- {N} commits pushed to origin/main

📁 Files: {topic}/{topic}-phase{1}-{total}-cloze.csv, {topic}/{topic}-phase{1}-{total}-basic.csv
📁 Merged: {topic}/{topic}-all-cloze.csv ({N} cards), {topic}/{topic}-all-basic.csv ({N} cards)
📝 Roadmap: All {total} phases marked [x]
```
