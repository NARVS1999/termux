# Backend Developer Roadmap: Junior → Mid-Level

> General knowledge for backend developers, with Laravel-specific context.

## Core PHP & Language Mastery

- [x] **Phase 1** — PHP 8.x features: enums, readonly properties, attributes, named arguments, match expressions
- [x] **Phase 2** — Object-oriented design: SOLID, composition over inheritance, dependency injection
- [x] **Phase 3** — Design patterns: Repository, Factory, Strategy, Observer, Adapter, Facade
- [x] **Phase 4** — Type systems, exception handling, PHPStan/PHPCS static analysis
- [x] **Phase 5** — Composer: autoloading (PSR-4), package development, version constraints

## Laravel Deep-Dive

- [x] **Phase 6** — Service container bindings, service providers, facades internals
- [x] **Phase 7** — Middleware, pipeline, request lifecycle from entry to response
- [x] **Phase 8** — Eloquent: relationships, eager loading & preventing N+1, model events, casts, scopes
- [x] **Phase 9** — Query Builder, DB transactions, locking, query optimization (EXPLAIN)
- [x] **Phase 10** — Queues & Jobs, scheduling, event/listener vs observer patterns
- [x] **Phase 11** — Notifications, Mailables, filesystem drivers, storage & S3
- [x] **Phase 12** — Broadcasting (Pusher/Reverb), WebSockets, Livewire basics

## Databases & Data Modeling

- [x] **Phase 13** — Database design/normalization vs denormalization tradeoffs
- [x] **Phase 14** — Indexing strategy, composite indexes, covering indexes
- [x] **Phase 15** — MySQL/PostgreSQL advanced: window functions, CTEs, JSON columns
- [x] **Phase 16** — Migrations, seeders, factories, data integrity constraints

## Caching & Performance

- [x] **Phase 17** — Redis/Memcached: cache drivers, cache tags, locks, rate limiting
- [x] **Phase 18** — Caching strategies: cache-aside, write-through, cache invalidation
- [x] **Phase 19** — HTTP caching, asset optimization, OPcache, page caching
- [x] **Phase 20** — Profiling: Laravel Debugbar, Xdebug, Query Monitor, Blackfire/Telescope

## API Design & Integration

- [x] **Phase 21** — RESTful conventions, versioning, pagination, filtering (SPA/API resources)
- [x] **Phase 22** — Authentication/Authorization: Sanctum, Passport, JWT, OAuth2 flows
- [x] **Phase 23** — API rate limiting, idempotency, webhooks, idempotent retries
- [x] **Phase 24** — Third-party integrations, payment gateways, webhook signature validation

## Security (non-negotiable for mid-level)

- [x] **Phase 25** — OWASP Top 10: XSS, SQLi, CSRF, SSRF, IDOR, mass assignment
- [x] **Phase 26** — AuthN vs AuthZ, roles & permissions (Spatie, policies, gates)
- [x] **Phase 27** — Secrets management, encryption at rest and in transit
- [x] **Phase 28** — Logging & auditing, input validation & sanitization

## Testing

- **Phase 29** — Unit vs feature vs integration testing
- **Phase 30** — PHPUnit/Pest, TestCase, RefreshDatabase, factories
- **Phase 31** — Mocking, fake queues/mail/events, HTTP tests
- **Phase 32** — Test-driven development, coverage reports, CI integration

## Architecture & Engineering Practices

- **Phase 33** — Layered architecture, service layer, clean architecture concepts
- **Phase 34** — Refactoring techniques, code review, technical debt management
- **Phase 35** — Modular/multi-tenant application design
- **Phase 36** — Design for failure: retries, circuit breakers, graceful degradation
- **Phase 37** — Observability: structured logging, monitoring, alerting, error tracking (Sentry)

## DevOps & Deployment

- **Phase 38** — Git branching strategies, semantic versioning, CI/CD pipelines
- **Phase 39** — Docker & containers, docker-compose, multi-stage builds
- **Phase 40** — Server administration basics: Nginx, PHP-FPM, Supervisor
- **Phase 41** — Deployment strategies: zero-downtime, blue-green, env config management
- **Phase 42** — Basic cloud concepts: load balancers, auto-scaling, CDNs

## Communication & Soft Skills (what actually gets you promoted)

- **Phase 43** — Estimation and scoping, breaking work into tasks
- **Phase 44** — Writing ADRs (architecture decision records) and technical docs
- **Phase 45** — Defending technical decisions, running code reviews
- **Phase 46** — Reading/understanding unfamiliar codebases quickly
- **Phase 47** — Incident response and post-mortems

## Recommended Learning Path (priority order)

1. **Phase 2** — SOLID + design patterns
2. **Phase 8** — Eloquent optimization & N+1
3. **Phase 10** — Queues & caching
4. **Phase 29** — Testing
5. **Phase 25** — Security (OWASP)
6. **Phase 39** — Docker + CI/CD
7. **Phase 17** — Distributed concepts (Redis, queues, idempotency)

> Focus on depth over breadth — employers hire mid-levels for production-quality, testable, maintainable code plus ownership of features end-to-end.
