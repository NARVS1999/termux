---
name: anki-taglish-leveled-cards
description: >
  Generate Anki flashcards in Taglish (Tagalog-English) for programming or technical topics,
  with card count scaled to the concept's difficulty level (basic, intermediate, advanced),
  saved as per-level per-label CSV files for direct Anki import. Use this whenever the user
  asks to create Anki cards, flashcards, or study cards in Taglish for coding concepts
  (e.g. "PHP loop", "JavaScript array", "SQL joins", "React Native useEffect"),
  especially if they mention wanting cards scaled by difficulty/level, reference the
  Foundational/Application leveled-count rule, or want cards generated from a
  `{topic}-concepts.md` file. Also trigger when the user asks for "all possible questions"
  about a topic for Anki. Produces two distinct card types - Foundational (cloze
  deletion) and Application (Front+Back, short-sentence/one-line answer) - with the number
  of each determined by whether the concept is basic, intermediate, or advanced. Output is
  one CSV per topic level + difficulty label, saved next to the concepts file.
---

# Anki Taglish Leveled Card Generator

Generates Anki-ready flashcards in Taglish for a given technical/programming topic, with the
number of cards per concept scaled to its difficulty level. This is a variant of the
`anki-taglish-cards` skill with a fixed card-count rule replacing the "cover everything"
open-ended approach. Unlike that skill, output is always CSV files (one per level + label),
never chat-only.

## Card Rules

There are exactly two card types. Never mix their formats.

### 1. Foundational — Cloze
- Format: a single Taglish sentence explaining/defining a keyword or concept, with the relevant
  term(s) hidden using cloze syntax: `{{c1::keyword}}`.
- Sentence must give enough context that the hidden term is inferable from the rest of the sentence.
- Answer length: no fixed restriction — one word, short phrase, or symbol, whatever fits naturally
  as the cloze deletion.
- Cover: keywords, syntax pieces, reserved words, symbols, and short defining phrases central to
  the topic.

### 2. Application / Scenario — Basic
- Format: **Front + Back only** (no Hint field), unless the user explicitly asks for a Hint.
- Front: a scenario or "how do you..." question in Taglish, framed as a small real problem to
  solve (not a definition).
- Back / Answer: **isang linya lang / short sentence** — a single line of code, or one short
  sentence of explanation. Never multi-step or multi-line answers.

## Added Rule: Card Count by Difficulty Level

Before writing any cards, **classify the concept** as `basic`, `intermediate`, or
`advanced`. Use this as the guide:

- **Basic** — a single fact or piece of syntax with little to no branching (e.g. "what is a
  variable", "PHP echo statement", "array length property"). Nothing to apply or decide, just
  recall.
- **Intermediate** — has a mechanism with a couple of moving parts or a common gotcha, and at
  least one clear "how do you use this" scenario (e.g. "PHP foreach loop", "useEffect dependency
  array", "SQL JOIN").
- **Advanced** — involves decision-making, edge cases, or "when to use X vs Y" judgment, usually
  combining multiple sub-concepts (e.g. "React Context vs prop drilling", "SQL query
  optimization", "async race conditions").

Once classified, generate **exactly** this many cards for that concept — no more, no less:

| Level        | Foundational (Cloze) | Application (Basic) | Total |
|--------------|:---------------------:|:---------------------:|:-----:|
| Basic        | 3                     | 0                      | 3     |
| Intermediate | 3                     | 2                      | 5     |
| Advanced     | 3                     | 5                      | 8     |

Notes:
- Foundational count is **always 3**, regardless of level — pick the 3 most essential facts/
  keywords for that concept.
- Only Application card count scales with level. Basic concepts get zero Application cards
  since there's nothing to apply.
- Classify and count **each concept separately**, never the whole topic at once.

## Input Source

Prefer the topic's concepts file when it exists: `{topic}/{topic}-concepts.md`
(produced by the `create-concept-name` skill). Each line is one concept:

```
## Foundational Concepts
1. Client-Server Model — basic — ang naghahati ng app sa client side at server side
```

- The `## {Level Name}` header gives the topic level; the concept name, `— label —`, and
  Taglish description come from the line.
- Use the label **as written in the file** — do not re-classify.
- The description can seed one cloze card (reword into a full sentence with
  `{{c1::keyword}}`), then write 2 more distinct cloze facts for the same concept.
- If no concepts file exists, fall back to listing sub-concepts manually and classifying
  each one per the criteria above.

## CSV File Output

For each topic level (slugified `##` header) and each difficulty label present in that level,
write one CSV per card type, saved **in the same folder as the concepts md file**:

```
{topic}-{level}-{label}-cloze.csv    — always created (3 cloze cards per concept)
{topic}-{level}-{label}-basic.csv    — only for intermediate (2) and advanced (5) labels
```

- `{level}` = slugified level name: `Foundational Concepts` → `foundational`,
  `Expert/Strategic Concepts` → `expert-strategic`, `Core Concepts` → `core`, etc.
- `{label}` = `basic`, `intermediate`, or `advanced`.
- Basic-labeled concepts get **no** basic CSV (0 application cards). So a level containing
  all three labels produces **5 CSVs**: 3 cloze (`-basic-cloze`, `-intermediate-cloze`,
  `-advanced-cloze`) + 2 basic (`-intermediate-basic`, `-advanced-basic`).
- Example files for `react/react-concepts.md`:
  - `react-foundational-basic-cloze.csv`
  - `react-foundational-intermediate-basic.csv`
  - `react-expert-strategic-advanced-cloze.csv`
- **No header row** — the file starts directly with the first card row. Every row has
  exactly 4 fields, hint column always empty, matching the repo convention:

```
{Concept Name},"Ang {{c1::keyword}} ay {Taglish explanation}.",,keyword
{Concept Name},"Paano {verb} {object}?",,"{one-line answer}"
```

### CSV Quoting Rules (RFC 4180 — GitHub/Anki safe)

- **Never backslash-escape quotes** (`\"` is invalid CSV).
- Quotes inside a quoted field must be **doubled** (`""`).
- Backslashes are literal in CSV — do NOT escape them (e.g. PHP namespaces stay `App\Models`).
- **ASCII only** — no Chinese/Cyrillic/foreign script characters in cards.
- Verify every row parses to exactly 4 fields with a standard CSV reader:
  `python3 -c "import csv; [print(len(r)) for r in csv.reader(open('file.csv'))]"` before
  finishing.

## Workflow

1. **Locate the concepts file** — check `{topic}/{topic}-concepts.md`. If missing, list
   sub-concepts manually and classify each as basic / intermediate / advanced.
2. **Group concepts** — by topic level (each `##` header), then by label within the level.
3. **Write Foundational (cloze) cards** — 3 per concept, cloze format, one line per row.
4. **Write Application (basic) cards** — 2 per intermediate concept, 5 per advanced concept,
   scenario-style, varying between "how to write it" and "what happens if..." questions.
5. **Write the CSV files** — one per level + label per the naming rules, in the concepts
   file's folder.
6. **Keep everything in Taglish** — mix Tagalog connector/explanation words (ginagamit,
   kapag, paano, hangga't, ang, ay, gagawa) with English technical terms (loop, condition,
   variable, array) left untranslated.
7. **Do not pad answers.** Application answers stay to isang linya / one short sentence —
   trim if longer.
8. **Verify** — each CSV parses to 4 fields (python3 check) and is ASCII-only.
9. **Confirm with user** — list the created files with their card counts.

## Anki Import Note

Tell the user to import each CSV separately and tick **"File has no headers"** in Anki's
import dialog. The first column holds the concept/topic name the card belongs to (e.g.
`HTTP Methods`), not the note type. Cloze CSVs map to the Cloze note type, basic CSVs to
the Basic note type — never merge them, since Anki maps one note type per import.
