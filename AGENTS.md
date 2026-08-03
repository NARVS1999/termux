# AGENTS.md

Content repo of Taglish (Tagalog-English) Anki flashcards for developer topics. No code, no build, no tests. All work is file generation + git.

## Structure

One folder per topic (`react/`, `backend/`, `mysql/`, `design-patterns/`, `system-architecture/`), each containing:

- `{topic}-roadmap.md` — 47 phases in `## Section` groups, each phase `- [ ] **Phase N** — Topic: subtopic1, subtopic2`. Completed phases are `[x]`.
- `{topic}-phase{N}-cloze.csv` — exactly 8–11 cloze cards
- `{topic}-phase{N}-basic.csv` — exactly 5 basic cards
- `*-SKILL.md` — process rules. Load before doing related work:
  - `create-roadmap-SKILL.md` — roadmap format (7–11 sections, ~47 phases)
  - `anki-taglish-cards-SKILL.md` — card format rules (authoritative for card content)
  - `auto-create-anki-SKILL.md` — the full workflow: parse roadmap → generate CSVs → commit → mark `[x]` → repeat

Current state: all 5 topics complete (react, backend, mysql, design-patterns, system-architecture — 470 CSVs, all phases `[x]`). New work = create a new topic folder + roadmap, then run auto-create-anki on it.

## Card format (verified against existing CSVs)

No header row — CSVs start directly with the first card row. Hint column is always empty:

- Cloze: `Cloze,"Ang {{c1::keyword}} ay {Taglish explanation}.",,keyword` — sentences start with `Ang`/`Sa`; Back repeats the cloze keyword.
- Basic: `Application,"Paano {verb} {object}?",,"{one-line answer}"` — one line of code or one short Taglish sentence, never multi-step.
- Taglish convention: English technical terms stay untranslated (e.g., `destructuring`, `optional chaining`).
- **ASCII only** — no Chinese/Cyrillic/foreign script characters in cards (a past commit fixed 11 files that had them).

## Git workflow (matches git history)

Direct commits to `main`, push to `origin` (`git@github.com:NARVS1999/termux.git`). Two commits per batch, in order:

1. `git add {topic}/{topic}-phase{N}-cloze.csv {topic}/{topic}-phase{N}-basic.csv ...` → commit `{topic} phase {start} - {end} cards`
2. after marking phases `[x]` in the roadmap → commit `mark done {topic} phase {start} - {end}`

## Anki import gotcha

Anki maps one note type per import; a `Type` column can't be mapped. Keep cloze and basic as separate files (already the repo convention); tell the user to import each CSV separately and tick "File has no headers" in the import dialog.

## Process rules

- Skip sections whose phases are all `[x]` (no commits, no regeneration).
- Phase subtopics after the colon map 1:1 to cards: each subtopic gets 1 cloze + 1 basic card, top up to the 8–11/5 counts.
- When a rule is ambiguous, the most recent variant the user stated wins (see note in `anki-taglish-cards-SKILL.md`).
