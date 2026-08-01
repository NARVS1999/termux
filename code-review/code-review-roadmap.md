# Code Review Roadmap: Fundamentals → Intermediate

> General knowledge for software developers, with code-review-specific context.

## Review Fundamentals (Prerequisites)

- [ ] **Phase 1** — Why code review: quality, knowledge sharing, ownership
- [ ] **Phase 2** — Review goals: correctness, design, maintainability, security
- [ ] **Phase 3** — Roles & responsibilities: author, reviewer, approver
- [ ] **Phase 4** — Review types: pull requests, pair review, design review
- [ ] **Phase 5** — Review culture: norms, expectations, psychological safety

## The Review Process

- [ ] **Phase 6** — Review workflow: assign, review, comment, approve
- [ ] **Phase 7** — PR anatomy: title, description, scope, tests
- [ ] **Phase 8** — Review timing: turnaround, batching, interruptions
- [ ] **Phase 9** — Process automation: templates, bots, checklists
- [ ] **Phase 10** — Merge criteria: approvals, CI, requirements

## Reading Code Effectively

- [ ] **Phase 11** — Reading strategies: structure, dependencies, entry points
- [ ] **Phase 12** — Understanding context: requirements, issue links, history
- [ ] **Phase 13** — Diff analysis: hunks, moved code, noise filtering
- [ ] **Phase 14** — Testing changes: reproducing, running tests, edge cases
- [ ] **Phase 15** — Verification: building, staging, manual checks

## Finding Issues

- [ ] **Phase 16** — Correctness bugs: logic errors, off-by-one, null handling
- [ ] **Phase 17** — Security issues: injection, auth flaws, secrets, OWASP
- [ ] **Phase 18** — Performance concerns: N+1 queries, re-renders, resource leaks
- [ ] **Phase 19** — Edge cases: empty states, boundaries, concurrency
- [ ] **Phase 20** — Maintainability: naming, duplication, complexity
- [ ] **Phase 21** — Test coverage: missing tests, weak assertions, flakiness

## Feedback & Communication

- [ ] **Phase 22** — Constructive feedback: specific, actionable, objective
- [ ] **Phase 23** — Tone & empathy: respect, questions over commands
- [ ] **Phase 24** — Asking questions: clarifying intent, exploring options
- [ ] **Phase 25** — Suggesting vs directing: guiding decisions, blocking issues
- [ ] **Phase 26** — Handling disagreements: evidence, escalation, compromise

## Writing Reviewable Code

- [ ] **Phase 27** — PR size: small changes, focused scope
- [ ] **Phase 28** — Descriptive PRs: context, rationale, testing notes
- [ ] **Phase 29** — Self-review: checking before requesting
- [ ] **Phase 30** — Commit hygiene: logical commits, clear messages

## Reviewing Specific Areas

- [ ] **Phase 31** — Frontend reviews: UX, accessibility, state, styling
- [ ] **Phase 32** — Backend reviews: APIs, data flow, error handling
- [ ] **Phase 33** — API reviews: contracts, versioning, security
- [ ] **Phase 34** — Infrastructure reviews: configs, IaC, deployment safety
- [ ] **Phase 35** — Design & architecture reviews: patterns, boundaries, tradeoffs

## Automated Review

- [ ] **Phase 36** — Linting & static analysis: rules, configs, severity
- [ ] **Phase 37** — CI checks: tests, builds, coverage gates
- [ ] **Phase 38** — AI-assisted review: suggestions, limitations, judgment
- [ ] **Phase 39** — Automated security scanning: SAST, dependency checks
- [ ] **Phase 40** — Automation balance: when humans are essential

## Metrics & Improvement

- [ ] **Phase 41** — Review metrics: time-to-review, comments, cycle time
- [ ] **Phase 42** — Bottlenecks: queues, ownership, knowledge gaps
- [ ] **Phase 43** — Documentation: review guides, standards, glossaries
- [ ] **Phase 44** — Skill building: practice, learning paths, retrospectives

## Leadership & Culture

- [ ] **Phase 45** — Mentoring reviewers: guidance, feedback, growth
- [ ] **Phase 46** — Setting standards: conventions, review checklists
- [ ] **Phase 47** — Organizational culture: incentives, recognition, habits

## Recommended Learning Path (priority order)

1. **Phase 1–5** — Review fundamentals
2. **Phase 6–10** — The review process
3. **Phase 11–15** — Reading code effectively
4. **Phase 16–21** — Finding issues
5. **Phase 22–26** — Feedback & communication
6. **Phase 27–30** — Writing reviewable code
7. **Phase 36–40** — Automated review

> Focus on building real projects — employers hire mid-level engineers for clean, reviewed, well-tested code plus ownership of quality end-to-end.
