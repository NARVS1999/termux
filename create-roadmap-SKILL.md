---
name: create-roadmap
description: >
  Generate a developer roadmap markdown file for any topic. Use when the user asks to
  create a roadmap, learning path, or curriculum for a technology or skill.
  Trigger on: "create roadmap for X", "roadmap for X", "learning path for X",
  "generate curriculum for X", "make roadmap for X".
---

# Create Roadmap Skill

Generates a structured developer roadmap markdown file for any given topic, following a consistent format optimized for Anki card generation and progressive learning.

## Output Format

The roadmap must follow this exact structure:

### Title
```
# {Topic} Developer Roadmap: {Level Range}
```
- Default level range: `Fundamentals → Intermediate`
- User may specify custom range (e.g., "Junior → Mid-Level", "Beginner → Advanced")

### Context Note
```
> General knowledge for {domain}, with {topic}-specific context.
```
- Auto-detect domain from topic:
  - React, Vue, Angular, Svelte → `frontend developers`
  - Laravel, Django, Rails, Express → `backend developers`
  - Docker, Kubernetes, CI/CD → `DevOps engineers`
  - SQL, PostgreSQL, MongoDB → `data engineers`
  - Flutter, React Native, Swift → `mobile developers`
  - Generic/unclear → `software developers`

### Sections & Phases
- **7–11 sections** total
- **3–7 phases** per section
- **~40–47 total phases** (aim for 47 to match existing roadmaps)
- All phases start **unchecked** `[ ]`

Format:
```markdown
## {Section Name}

- [ ] **Phase N** — {Topic}: {subtopic1}, {subtopic2}, {subtopic3}
- [ ] **Phase N+1** — {Topic}: {subtopic1}, {subtopic2}, {subtopic3}
```

### Phase Description Rules
- Start with a high-level concept or tool name after the em dash
- Follow with colon, then comma-separated keywords/subtopics
- Keep it concise — no full sentences, just keywords
- Each phase should be a learnable chunk (1–3 hours of study)
- Avoid overlap between phases — each should cover distinct concepts

### Section Organization Pattern
Sections should follow this logical progression:
1. **Prerequisites** — Foundational knowledge needed before the main topic
2. **Core Concepts** — The fundamental building blocks
3. **Intermediate Topics** — Deeper dives into key areas
4. **Advanced Features** — Complex patterns and advanced usage
5. **Ecosystem & Tools** — Libraries, frameworks, and tooling
6. **Testing & Quality** — Testing strategies and code quality
7. **Performance & Optimization** — Speed, efficiency, and scaling
8. **Architecture & Patterns** — Design patterns and architectural decisions
9. **DevOps & Deployment** — CI/CD, deployment, infrastructure
10. **Soft Skills & Practices** — Communication, estimation, code review (if applicable)

Not all sections are required — pick the 7–11 that make sense for the topic.

### Recommended Learning Path
```markdown
## Recommended Learning Path (priority order)

1. **Phase N** — {short description}
2. **Phase N** — {short description}
...
7. **Phase N** — {short description}
```
- List exactly **7 phases** in priority order
- Pick the most foundational and high-impact phases
- Start with basics, progress to practical advanced topics

### Closing Note
```markdown
> Focus on building real projects — employers hire mid-level {role}s for clean, performant, well-tested code plus ownership of features end-to-end.
```
- `{role}` = topic-specific role (e.g., "React devs", "backend devs", "full-stack engineers")

## Workflow

1. **Parse user input** — Extract the topic and any customizations (level range, phase count, checked/unchecked)
2. **Determine domain** — Map topic to appropriate developer domain
3. **Brainstorm sections** — Create 7–11 logical groupings
4. **Distribute phases** — Assign 3–7 phases per section, totaling ~47
5. **Write phase descriptions** — Short, keyword-rich, non-overlapping
6. **Select learning path** — Pick 7 priority phases
7. **Generate the file** — Save as `{topic-slug}-roadmap.md`
8. **Confirm with user** — Show the file path and phase count

## Customization Options

User may specify:
- **Level range**: "Junior → Mid-Level", "Beginner → Advanced", etc.
- **Phase count**: "make it 30 phases" or "keep it short"
- **Checked/unchecked**: "all checked" or "start unchecked" (default: unchecked)
- **Specific sections**: "include a DevOps section" or "skip testing"
- **Context**: "focus on Laravel" or "use Python examples"

## File Naming

Save the roadmap as: `{topic-slug}-roadmap.md`
- `react` → `react-roadmap.md`
- `vue js` → `vue-roadmap.md`
- `docker` → `docker-roadmap.md`
- `laravel` → `laravel-roadmap.md`

## Example Trigger Phrases

- "create roadmap for Vue.js"
- "roadmap for Docker beginners"
- "generate a learning path for Python"
- "make a backend developer roadmap"
- "curriculum for learning GraphQL"
