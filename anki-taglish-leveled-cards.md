---
name: anki-taglish-leveled-cards
description: >
  Generate Anki flashcards in Taglish (Tagalog-English) for programming or technical topics,
  with card count scaled to the concept's difficulty level (basic, intermediate, advanced).
  Use this whenever the user asks to create Anki cards, flashcards, or study cards in Taglish
  for coding concepts (e.g. "PHP loop", "JavaScript array", "SQL joins", "React Native useEffect"),
  especially if they mention wanting cards scaled by difficulty/level, or reference the
  Foundational/Application leveled-count rule. Also trigger when the user asks for "all possible
  questions" about a topic for Anki. Produces two distinct card types - Foundational (cloze
  deletion) and Application (Front+Back, short-sentence/one-line answer) - with the number of
  each determined by whether the concept is basic, intermediate, or advanced.
---

# Anki Taglish Leveled Card Generator

Generates Anki-ready flashcards in Taglish for a given technical/programming topic, with the
number of cards per concept scaled to its difficulty level. This is a variant of the
`anki-taglish-cards` skill with a fixed card-count rule replacing the "cover everything"
open-ended approach.

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

Before writing any cards, **classify the concept/topic** as `basic`, `intermediate`, or
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
- If a topic contains multiple concepts at different levels (e.g. "PHP loops" → `for` is basic,
  `foreach` is intermediate, `nested loops with break/continue` is advanced), classify and count
  **each sub-concept separately**, then sum the totals. State the per-concept classification to
  the user before generating cards so they can correct it if needed.

## Workflow

1. **List sub-concepts** of the requested topic (e.g. for "PHP loop": for, while, do-while,
   foreach, break, continue, nested loops, infinite loop).
2. **Classify each sub-concept** as basic / intermediate / advanced per the criteria above, and
   show this classification to the user as a short list before generating cards.
3. **Generate cards per sub-concept** following the exact counts in the table (3/0, 3/2, or 3/5).
4. **Write Foundational cards first** for each sub-concept, cloze format.
5. **Write Application cards second** for each sub-concept (intermediate/advanced only),
   scenario-style, varying between "how to write it" and "what happens if..." questions.
6. **Keep everything in Taglish** — mix Tagalog connector/explanation words (ginagamit, kapag,
   paano, hangga't, ang, ay, gagawa) with English technical terms (loop, condition, variable,
   array) left untranslated.
7. **Do not pad answers.** Application answers stay to isang linya / one short sentence — trim
   if longer.
8. Offer at the end to export as CSV for direct Anki import (see below), but don't create the
   file unless asked.

## Output Format (in-chat)

First show the **classification list** (sub-concept → level → card count). Then present cards
grouped under two headers per sub-concept: `FOUNDATIONAL (Cloze)` and `APPLICATION`. Number each
card. Show cloze cards as the full sentence with `{{c1::...}}` inline, followed by the bolded
answer beneath (Anki hides it automatically at review time — this is just for the user's preview).

## CSV Export (if requested)

Use two note types — Cloze and Basic — since "Type" columns can't be mapped natively in Anki's
import. Either produce two separate CSVs or one CSV with a "Type" column and tell the user to
split it. **No header row** — the file starts directly with the first card row:

```
Cloze,"Sa PHP, ang {{c1::for}} loop ay ginagamit kapag alam mo na kung ilang beses uulitin ang code.",,for
Application,"Paano gagawa ng loop na mag-print ng numbers 1 to 5?","Gamitin ang for loop na may starting value, condition, at increment.","for ($i = 1; $i <= 5; $i++) { echo $i; }"
```

Save as `.csv` to `/mnt/user-data/outputs/`, then use `present_files`. Note for the user that in
Anki's import dialog they must tick **"File has no headers"** and map the fields manually.

### CSV Quoting Rules (RFC 4180 — GitHub/Anki safe)

- **Never backslash-escape quotes** (`\"` is invalid CSV).
- Quotes inside a quoted field must be **doubled** (`""`).
- Backslashes are literal in CSV — do NOT escape them (e.g. PHP namespaces stay `App\Models`).
- Every row must parse to exactly 4 fields with a standard CSV reader; verify with
  `python3 -c "import csv; [print(len(r)) for r in csv.reader(open('file.csv'))]"` before
  committing.
