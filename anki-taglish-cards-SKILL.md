---
name: anki-taglish-cards
description: >
  Generate Anki flashcards in Taglish (Tagalog-English) for programming or technical topics.
  Use this whenever the user asks to create Anki cards, flashcards, or study cards in Taglish,
  especially for coding concepts (e.g. "PHP loop", "JavaScript array", "SQL joins"). Also trigger
  when the user asks for "all possible questions" about a topic for Anki, or references the
  Foundational/Application card rule format. Produces two distinct card types - Foundational
  (cloze deletion, single-word answer) and Application (Front+Hint+Back or Front+Back,
  short-sentence/one-line answer).
---

# Anki Taglish Card Generator

Generates Anki-ready flashcards in Taglish for a given technical/programming topic, strictly following a two-tier card format.

## Card Rules

There are exactly two card types. Never mix their formats. **Always use the most recent rule the user gave in the conversation** — the two variants below are both valid; check which one currently applies before generating cards.

### 1. Foundational — Cloze
- Format: a single Taglish sentence explaining/defining a keyword or concept, with the relevant term(s) hidden using cloze syntax: `{{c1::keyword}}`.
- Sentence must give enough context that the hidden term is inferable from the rest of the sentence.
- Answer length: **no fixed restriction** — it can be one word, a short phrase, or a symbol, whatever fits naturally as the cloze deletion. (Note: an earlier rule variant restricted this to exactly one word — don't assume that constraint unless the user states it again.)
- Cover: keywords, syntax pieces, reserved words, symbols, and short defining phrases central to the topic.

### 2. Application / Scenario
- Default format: **Front + Back only** (no Hint field), unless the user explicitly asks for a Hint.
- Front: a scenario or "how do you..." question in Taglish, framed as a small real problem to solve (not a definition).
- Back / Answer: **isang linya lang / short sentence** — a single line of code, or one short sentence of explanation. Never multi-step or multi-line answers.

## Workflow

1. **Confirm the format variant** the user wants for Application cards if ambiguous: Front+Hint+Back, or Front+Back only. Default to whatever the user's most recent rule statement says.
2. **List sub-concepts** of the requested topic before writing cards (e.g. for "PHP loop": for, while, do-while, foreach, break, continue, nested loops, infinite loop). This ensures full coverage when the user asks for "all possible questions."
3. **Write Foundational cards first** — one per keyword/concept, cloze format, single-word answer.
4. **Write Application cards second** — one scenario per major construct, covering both "how to write it" and "what happens if..." style questions for variety.
5. **Keep everything in Taglish** — mix Tagalog connector/explanation words (ginagamit, kapag, paano, hangga't, ang, ay, gagawa) with English technical terms (loop, condition, variable, array) left untranslated, since translating code terms would be unnatural.
6. **Do not pad answers.** If the user's rule says "isang word lang" or "isang linya," a longer answer is a rule violation — trim it down.
7. Offer at the end to export as CSV for direct Anki import (see below), but don't create the file unless asked.

## Output Format (in-chat)

Present cards grouped under two headers: `FOUNDATIONAL (Cloze)` and `APPLICATION`. Number each card. Show cloze cards as the full sentence with `{{c1::...}}` inline, followed by the bolded single-word answer beneath (Anki hides it automatically at review time — the visible "answer" line here is just for the user's preview).

## CSV Export (if requested)

If the user wants a file for Anki import, use Basic (and reversed card) note types are not needed — use two separate CSVs or a single CSV with a "Type" column. **No header row** — the file starts directly with the first card row:

```
Cloze,"Sa PHP, ang {{c1::for}} loop ay ginagamit kapag alam mo na kung ilang beses uulitin ang code.",,for
Application,"Paano gagawa ng loop na mag-print ng numbers 1 to 5?","Gamitin ang for loop na may starting value, condition, at increment.","for ($i = 1; $i <= 5; $i++) { echo $i; }"
```

Save as `.csv` to `/mnt/user-data/outputs/`, then use `present_files`. Note for the user that in Anki's import dialog they must tick **"File has no headers"** and map the fields manually (since the "Type" column can't be mapped natively, splitting into two separate CSVs — one per note type: Cloze, Basic — is recommended).
