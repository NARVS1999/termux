---
name: create-concept-name
description: >
  Generate a complete concept hierarchy markdown file for any topic, with each concept
  labeled by difficulty level (basic, intermediate, advanced). Use when the user asks to
  create a concept name list, concept hierarchy, concept map, or learning concepts for a
  technology or skill. Trigger on: "create concept name for X", "concept hierarchy for X",
  "concept map for X", "concepts for learning X", "list the concepts of X". The output
  serves as a complete learning roadmap and feeds directly into the
  anki-taglish-leveled-cards skill, where the difficulty label determines card counts.
---

# Create Concept Name Skill

Generates a complete concept hierarchy markdown file for any given topic, following a fixed
10-level structure. Each concept is then analyzed and labeled `basic`, `intermediate`, or
`advanced` so the output can be consumed directly by the `anki-taglish-leveled-cards` skill
(where the label decides Foundational/Application card counts).

## Concept Levels

Use exactly these 10 concept levels, in this order:

1. Foundational Concepts
2. Core Concepts
3. Implementation Concepts
4. Integration Concepts
5. Architectural Concepts
6. Design Concepts
7. Advanced Concepts
8. Production Concepts
9. Optimization Concepts
10. Expert/Strategic Concepts

## Concept Rules

- List the concepts belonging to each level.
- Use concept names only — do not explain the concepts.
- Do not skip important concepts.
- Do not duplicate concepts across levels.
- Order concepts within each level by prerequisite/dependency order.
- A concept must appear only after the concepts it depends on.
- Make the hierarchy comprehensive enough to serve as a complete learning roadmap.

## Description Rules

- Every concept gets a **concise description** after the difficulty label.
- Description is a **short Taglish one-liner** (~5–10 words) — English technical terms stay
  untranslated, mixed with short Tagalog connectors (ang, ay, ng, kapag, para sa, gaya ng).
- Keep it a definition/clue only — no full sentences of explanation, no examples, no extra
  lines. Concept name, label, and description all fit on one line.
- The description must not reveal concepts that depend on it later.

## Difficulty Labeling

After generating each level, classify every concept as `basic`, `intermediate`, or
`advanced` using the criteria from `anki-taglish-leveled-cards.md`:

- **basic** — a single fact or piece of syntax with little to no branching; nothing to apply
  or decide, just recall (e.g. "what is a variable", "array length property").
- **intermediate** — a mechanism with a couple of moving parts or a common gotcha, and at
  least one clear "how do you use this" scenario (e.g. "foreach loop", "useEffect dependency
  array").
- **advanced** — decision-making, edge cases, or "when to use X vs Y" judgment, usually
  combining multiple sub-concepts (e.g. "Context vs prop drilling", "query optimization").

Rules:
- Label each concept **individually by analysis**, not by its position in the 10 levels.
  A concept in an Expert-level section can still be `basic`; a Foundational-level section
  can contain an `advanced` concept.
- The 10-level position is only a hint (early levels lean basic, later levels lean advanced).

## Output Format

```markdown
# {Topic} Concept Hierarchy

## Foundational Concepts

1. Concept — basic — short Taglish description
2. Concept — intermediate — short Taglish description
3. Concept — advanced — short Taglish description

## Core Concepts

1. Concept — basic — short Taglish description
2. Concept — basic — short Taglish description
3. Concept — intermediate — short Taglish description

...
## Expert/Strategic Concepts

1. Concept — advanced — short Taglish description
2. Concept — advanced — short Taglish description
3. Concept — intermediate — short Taglish description
```

- Group headers use `## {Level Name}` in the fixed 10-level order (not numbered headers).
- Number concepts within each level starting at `1.`
- Each line: `{number}. {Concept} — {label} — {short Taglish description}`
- Concept names and labels only, plus the one-line description — never a multi-line
  explanation.

## Workflow

1. **Parse user input** — Extract the topic and any customizations (e.g. "skip level 8", "focus on X", "label only, no hierarchy", "no descriptions").
2. **Brainstorm concepts per level** — Fill all 10 levels with concept names following the Concept Rules.
3. **Label each concept** — Analyze and tag `basic` / `intermediate` / `advanced` per the Difficulty Labeling criteria.
4. **Describe each concept** — Append a concise Taglish one-liner per the Description Rules.
5. **Verify rules** — No duplicates across levels, prerequisite order respected, descriptions stay short and single-line.
6. **Generate the file** — Save as `{topic-slug}/{topic-slug}-concepts.md` (create the folder if missing).
7. **Confirm with user** — Show the file path and total concept count.

## File Naming

Save the hierarchy as: `{topic-slug}/{topic-slug}-concepts.md`

- `react` → `react/react-concepts.md`
- `vue js` → `vue/vue-concepts.md`
- `docker` → `docker/docker-concepts.md`
- `laravel` → `laravel/laravel-concepts.md`

## Customization Options

User may specify:
- **Difficulty labels**: "no labels" or "label only the advanced ones"
- **Levels**: "skip level 8" or "only first 5 levels"
- **Focus**: "focus on Laravel" or "include modern features"
- **Count**: "at least 5 concepts per level" or "keep it short"

## Example Trigger Phrases

- "create concept name for Vue.js"
- "concept hierarchy for Docker"
- "concept map for Python"
- "list the concepts of GraphQL"
- "concepts for learning Kubernetes"
