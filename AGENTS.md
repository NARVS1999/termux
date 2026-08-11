# AGENTS.md

Content repo of Taglish (Tagalog-English) Anki flashcards for developer topics. No code, no build, no tests. All work is file generation + git.

## Structure

One folder per topic (`react/`, `backend/`, `mysql/`, `design-patterns/`, `system-architecture/`), each containing:

- `{topic}-roadmap.md` — 47 phases in `## Section` groups, each phase `- [ ] **Phase N** — Topic: subtopic1, subtopic2`. Completed phases are `[x]`.
- `{topic}-phase{N}-cloze.csv` — exactly 8–11 cloze cards
- `{topic}-phase{N}-basic.csv` — exactly 5 basic cards
- `*-SKILL.md` — process rules. Load before doing related work:
  - `create-roadmap-SKILL.md` — roadmap format (7–11 sections, ~47 phases)
  - `create-concept-name-SKILL.md` — 10-level concept hierarchy with per-concept difficulty labels (basic/intermediate/advanced) and short Taglish one-line descriptions, saved as `{topic}/{topic}-concepts.md`
  - `anki-taglish-cards-SKILL.md` — card format rules (authoritative for card content)
  - `anki-taglish-leveled-cards.md` — leveled variant: reads `{topic}-concepts.md`, scales card counts by difficulty label (3/0, 3/2, 3/5), writes one CSV per level+label (`{topic}-{level}-{label}-cloze.csv` / `-basic.csv`) next to the concepts file
  - `auto-create-anki-SKILL.md` — the full workflow: parse roadmap → generate CSVs → commit → mark `[x]` → repeat (also merges all phase CSVs into `{topic}-all-cloze.csv` + `{topic}-all-basic.csv` at the end)
  - `merge-anki-cards-SKILL.md` — merge existing per-phase CSVs in any folder into 2 combined files (`{prefix}-all-cloze.csv`, `{prefix}-all-basic.csv`)

Current state: all 5 topics complete (react, backend, mysql, design-patterns, system-architecture — 470 CSVs, all phases `[x]`). New work = create a new topic folder + roadmap, then run auto-create-anki on it.

## Card format (verified against existing CSVs)

No header row — CSVs start directly with the first card row. Hint column is always empty:

- Cloze: `{Concept Name},"Ang {{c1::keyword}} ay {Taglish explanation}.",,keyword` — sentences start with `Ang`/`Sa`; Back repeats the cloze keyword.
- Basic: `{Concept Name},"Paano {verb} {object}?",,"{one-line answer}"` — one line of code or one short Taglish sentence, never multi-step.
- First column holds the concept/topic name the card belongs to (e.g. `HTTP Methods`), not the note type. Existing per-phase CSVs keep `Cloze`/`Application`; new cards use the new format.
- Taglish convention: English technical terms stay untranslated (e.g., `destructuring`, `optional chaining`).
- **ASCII only** — no Chinese/Cyrillic/foreign script characters in cards (a past commit fixed 11 files that had them).
- **CSV quoting (RFC 4180)** — never `\"` backslash escapes (GitHub preview breaks); double inner quotes `""`; backslashes are literal, never escaped (e.g. PHP namespace `App\Models`). A past commit fixed 48 files with `\"`.

## Git workflow (matches git history)

Direct commits to `main`, push to `origin` (`git@github.com:NARVS1999/termux.git`). Two commits per batch, in order:

1. `git add {topic}/{topic}-phase{N}-cloze.csv {topic}/{topic}-phase{N}-basic.csv ...` → commit `{topic} phase {start} - {end} cards`
2. after marking phases `[x]` in the roadmap → commit `mark done {topic} phase {start} - {end}`

## Anki import gotcha

Anki maps one note type per import. The first column is the concept name, not the note type — keep cloze and basic as separate files (already the repo convention); tell the user to import each CSV separately and tick "File has no headers" in the import dialog.

## Process rules

- Skip sections whose phases are all `[x]` (no commits, no regeneration).
- Phase subtopics after the colon map 1:1 to cards: each subtopic gets 1 cloze + 1 basic card, top up to the 8–11/5 counts.
- When a rule is ambiguous, the most recent variant the user stated wins (see note in `anki-taglish-cards-SKILL.md`).
