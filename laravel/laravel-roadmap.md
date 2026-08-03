# Laravel Developer Roadmap: Fundamentals → Intermediate

> General knowledge for backend developers, with Laravel-specific context.

## PHP Refresher (Prerequisites)

- [x] **Phase 1** — PHP basics: syntax, types, arrays, control flow, functions
- [x] **Phase 2** — OOP in PHP: classes, inheritance, interfaces, traits
- [x] **Phase 3** — Composer: install, autoload, packages, lockfile
- [x] **Phase 4** — Namespaces & PSR-4: autoloading, imports
- [x] **Phase 5** — Development setup: PHP, extensions, local servers

## Laravel Fundamentals

- [x] **Phase 6** — Installation: composer create-project, requirements
- [x] **Phase 7** — Project structure: app, routes, config, resources, database
- [x] **Phase 8** — Config & env: .env files, config caching, secrets
- [x] **Phase 9** — Routing basics: web routes, methods, parameters
- [x] **Phase 10** — Controllers: actions, dependencies, responses
- [x] **Phase 11** — Service container: bindings, resolution, facades

## Routing & Controllers

- [ ] **Phase 12** — Routes: named routes, parameters, fallbacks
- [ ] **Phase 13** — Route groups & middleware: auth, throttling, scopes
- [ ] **Phase 14** — Resource controllers: RESTful mapping, partials
- [ ] **Phase 15** — Route model binding: implicit, explicit, scoping
- [ ] **Phase 16** — API routes: prefixes, versioning, responses

## Eloquent ORM

- [ ] **Phase 17** — Models & migrations: schema, columns, rollbacks
- [ ] **Phase 18** — Relationships: one-to-many, many-to-many, polymorphic
- [ ] **Phase 19** — Scopes & accessors: query scopes, mutators, casts
- [ ] **Phase 20** — Eager loading: with, lazy loading, preventing N+1
- [ ] **Phase 21** — Queries & pagination: builder, aggregates, pagination
- [ ] **Phase 22** — Collections: methods, transforms, chunks

## Blade Templating

- [ ] **Phase 23** — Templates & layouts: inheritance, sections, includes
- [ ] **Phase 24** — Components & slots: class-based, anonymous, attributes
- [ ] **Phase 25** — Directives: conditionals, loops, auth checks
- [ ] **Phase 26** — Forms & CSRF: token handling, old input, errors

## Auth & Security

- [ ] **Phase 27** — Authentication: scaffolding, guards, login flows
- [ ] **Phase 28** — Authorization: gates, policies, abilities
- [ ] **Phase 29** — Security best practices: XSS, CSRF, injection, headers
- [ ] **Phase 30** — Validation: rules, custom rules, form requests
- [ ] **Phase 31** — Rate limiting: throttling, quotas, limits

## APIs

- [ ] **Phase 32** — API resources: transformations, collections
- [ ] **Phase 33** — Sanctum: token auth, SPA auth, scopes
- [ ] **Phase 34** — API testing: HTTP tests, assertions, pagination
- [ ] **Phase 35** — Versioning & documentation: v1/v2, docs, changes

## Testing

- [ ] **Phase 36** — PHPUnit setup: config, environment, databases
- [ ] **Phase 37** — Feature tests: HTTP, auth, database transactions
- [ ] **Phase 38** — Factories & seeders: model factories, test data
- [ ] **Phase 39** — Mocking & fakes: queues, mail, events
- [ ] **Phase 40** — Test organization: suites, helpers, coverage

## Queues, Jobs & Events

- [ ] **Phase 41** — Queues & jobs: drivers, dispatch, retries, failed jobs
- [ ] **Phase 42** — Events & listeners: dispatching, subscribers
- [ ] **Phase 43** — Scheduling: tasks, cron, command scheduling
- [ ] **Phase 44** — Mail & notifications: mailables, channels, queues

## Performance & Deployment

- [ ] **Phase 45** — Caching: cache drivers, queries, views, invalidation
- [ ] **Phase 46** — Optimization: eager loading, indexes, opcache
- [ ] **Phase 47** — Deployment: platforms, CI/CD, monitoring, maintenance

## Recommended Learning Path (priority order)

1. **Phase 1–5** — PHP refresher
2. **Phase 6–11** — Laravel fundamentals
3. **Phase 12–16** — Routing & controllers
4. **Phase 17–22** — Eloquent ORM
5. **Phase 27–31** — Auth & security
6. **Phase 36–40** — Testing
7. **Phase 45–47** — Performance & deployment

> Focus on building real projects — employers hire mid-level Laravel devs for clean, performant, well-tested code plus ownership of features end-to-end.
