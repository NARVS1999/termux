# Backend Developer Roadmap: Junior → Mid-Level

> General knowledge for backend developers, with Laravel-specific context.

## Core PHP & Language Mastery

- **Phase 1** — PHP 8.x features: enums, readonly properties, attributes, named arguments, match expressions
- **Phase 2** — Object-oriented design: SOLID, composition over inheritance, dependency injection
- **Phase 3** — Design patterns: Repository, Factory, Strategy, Observer, Adapter, Facade
- **Phase 4** — Type systems, exception handling, PHPStan/PHPCS static analysis
- **Phase 5** — Composer: autoloading (PSR-4), package development, version constraints

## Laravel Deep-Dive

- **Phase 6** — Service container bindings, service providers, facades internals
- **Phase 7** — Middleware, pipeline, request lifecycle from entry to response
- **Phase 8** — Eloquent: relationships, eager loading & preventing N+1, model events, casts, scopes
- **Phase 9** — Query Builder, DB transactions, locking, query optimization (EXPLAIN)
- **Phase 10** — Queues & Jobs, scheduling, event/listener vs observer patterns
- **Phase 11** — Notifications, Mailables, filesystem drivers, storage & S3
- **Phase 12** — Broadcasting (Pusher/Reverb), WebSockets, Livewire basics

## Databases & Data Modeling

- **Phase 13** — Database design/normalization vs denormalization tradeoffs
- **Phase 14** — Indexing strategy, composite indexes, covering indexes
- **Phase 15** — MySQL/PostgreSQL advanced: window functions, CTEs, JSON columns
- **Phase 16** — Migrations, seeders, factories, data integrity constraints

## Caching & Performance

- **Phase 17** — Redis/Memcached: cache drivers, cache tags, locks, rate limiting
- **Phase 18** — Caching strategies: cache-aside, write-through, cache invalidation
- **Phase 19** — HTTP caching, asset optimization, OPcache, page caching
- **Phase 20** — Profiling: Laravel Debugbar, Xdebug, Query Monitor, Blackfire/Telescope

## API Design & Integration

- **Phase 21** — RESTful conventions, versioning, pagination, filtering (SPA/API resources)
- **Phase 22** — Authentication/Authorization: Sanctum, Passport, JWT, OAuth2 flows
- **Phase 23** — API rate limiting, idempotency, webhooks, idempotent retries
- **Phase 24** — Third-party integrations, payment gateways, webhook signature validation

## Security (non-negotiable for mid-level)

- **Phase 25** — OWASP Top 10: XSS, SQLi, CSRF, SSRF, IDOR, mass assignment
- **Phase 26** — AuthN vs AuthZ, roles & permissions (Spatie, policies, gates)
- **Phase 27** — Secrets management, encryption at rest and in transit
- **Phase 28** — Logging & auditing, input validation & sanitization

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
