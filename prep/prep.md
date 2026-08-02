# 2-Month Backend/Laravel Interview Prep — Weekly Roadmap

> Follows your original roadmap numbering, Phase 1 onward (redoing Phase 1 since you want a full refresh). 5 study days/week × 8 weeks.
> Daily target: 2 Cloze (fundamentals) + 2 Application (scenario) cards = 4 new cards/day
> Reviews (SRS) run every day regardless of new-card day — don't skip reviews even on rest days.

---

## Week 1
- **Phase 1** — PHP 8.x features redo: enums, readonly, attributes, named arguments, match (refresh existing cards + add any gaps)
- **Phase 2** — SOLID principles
- **Phase 3** — Design patterns (Repository, Factory, Strategy, Observer, Adapter, Facade)
- **Phases 4+5** — Type systems/exception handling/static analysis + Composer (combined, lighter)
- **Review day** — mixed drill, Phases 1–5

## Week 2
- **Phase 6** — Service container, service providers, facades internals
- **Phase 7** — Middleware, pipeline, request lifecycle
- **Phase 8** — Eloquent deep-dive: relationships, eager loading, N+1, model events, casts, scopes
- **Phase 9** — Query Builder, transactions, locking, EXPLAIN
- **Review day** — mixed drill, Phases 6–9

## Week 3
- **Phase 10** — Queues & Jobs, scheduling, event/listener vs observer
- **Phases 11+12** — Notifications/Mailables/storage + Broadcasting/Livewire (combined, lighter)
- **Phase 13** — DB design: normalization vs denormalization
- **Phases 14+15** — Indexing strategy + advanced SQL (window functions, CTEs, JSON)
- **Review day** — mixed drill, Phases 10–15

## Week 4
- **Phase 16** — Migrations, seeders, factories, data integrity
- **Phase 17** — Redis/Memcached: drivers, cache tags, locks, rate limiting
- **Phase 18** — Caching strategies: cache-aside, write-through, invalidation
- **Phases 19+20** — HTTP caching/OPcache + profiling tools (combined, lighter)
- **Review day** — mixed drill, Phases 16–20

## Week 5
- **Phase 21** — RESTful conventions, versioning, pagination, filtering
- **Phase 22** — Auth: Sanctum, Passport, JWT, OAuth2
- **Phases 23+24** — Rate limiting/idempotency/webhooks + 3rd-party integrations (combined)
- **Phase 25** — OWASP Top 10 (XSS, SQLi, CSRF, SSRF, IDOR, mass assignment)
- **Review day** — mixed drill, Phases 21–25

## Week 6
- **Phase 26** — AuthN vs AuthZ, roles/permissions (Spatie, policies, gates)
- **Phases 27+28** — Secrets/encryption + logging/auditing/validation (combined)
- **Phase 29** — Unit vs feature vs integration testing
- **Phase 30** — PHPUnit/Pest, TestCase, RefreshDatabase, factories
- **Review day** — mixed drill, Phases 26–30

## Week 7
- **Phase 31** — Mocking, fake queues/mail/events, HTTP tests
- **Phase 32** — TDD, coverage reports, CI integration
- **Phase 33** — Layered architecture, service layer, clean architecture
- **Phases 34+35** — Refactoring/code review/tech debt + modular/multi-tenant design (combined)
- **Review day** — mixed drill, Phases 31–35

## Week 8 — Consolidation & Mock Interviews
- **Phase 36** — Design for failure: retries, circuit breakers, graceful degradation
- **Phase 37** — Observability: logging, monitoring, alerting, Sentry
- **Phases 38+39** — Git/CI-CD + Docker/docker-compose (combined)
- **Phases 40–42** — Server admin (Nginx/PHP-FPM/Supervisor) + deployment strategies + cloud basics (combined)
- **Mock interview day** — pick 8–10 random Application cards across all phases, explain out loud, time yourself

---

## Not covered by cards (Phases 43–47)
Estimation/scoping, ADRs, defending decisions, reading unfamiliar codebases, incident response — these are **practice skills, not recall facts**. Anki won't help much here; better spent doing a mock system-design/behavioral interview in Week 8 or on the job.

## Ground rules
1. Don't create new cards on a day you're behind on reviews — clear the queue first.
2. Every fundamental (cloze) gets a paired application card same day, same phase — keeps recall tied to usage.
3. Combined phases (e.g. 11+12, 19+20) get 2 cloze + 2 application total for the pair, not 4+4 — they're lower interview-priority, don't over-invest.
4. Week 8 has no new content on the last day — pure mock interview under time pressure.
