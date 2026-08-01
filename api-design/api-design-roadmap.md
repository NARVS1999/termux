# API Design Roadmap: Fundamentals → Intermediate

> General knowledge for backend developers, with API-design-specific context.

## HTTP & Networking Fundamentals (Prerequisites)

- [ ] **Phase 1** — HTTP methods: GET, POST, PUT, PATCH, DELETE semantics
- [ ] **Phase 2** — Status codes: 2xx, 3xx, 4xx, 5xx, choosing correctly
- [ ] **Phase 3** — Headers: content types, auth, cache headers, custom headers
- [ ] **Phase 4** — URL design: paths, query strings, hierarchy, slashes
- [ ] **Phase 5** — Caching: ETags, Cache-Control, conditional requests

## REST Design Principles

- [ ] **Phase 6** — Resource modeling: nouns, collections, relationships
- [ ] **Phase 7** — Naming conventions: pluralization, casing, consistency
- [ ] **Phase 8** — CRUD mapping: actions to methods, sub-resources
- [ ] **Phase 9** — Filtering & pagination: params, cursor vs offset, sorting
- [ ] **Phase 10** — Idempotency: safe methods, idempotency keys, retries
- [ ] **Phase 11** — HATEOAS & links: hypermedia, discoverability

## API Security

- [ ] **Phase 12** — Authentication: API keys, tokens, sessions
- [ ] **Phase 13** — Authorization: scopes, permissions, RBAC, ABAC
- [ ] **Phase 14** — OAuth2 & OIDC: grant types, flows, token handling
- [ ] **Phase 15** — Rate limiting: quotas, throttling, headers, retry-after
- [ ] **Phase 16** — Input validation: schemas, sanitization, error responses
- [ ] **Phase 17** — CORS & CSRF: cross-origin policies, token defenses

## API Documentation

- [ ] **Phase 18** — OpenAPI/Swagger: specs, examples, generation
- [ ] **Phase 19** — Documentation quality: clarity, examples, errors
- [ ] **Phase 20** — Changelogs & updates: release notes, notices
- [ ] **Phase 21** — API portals: onboarding, keys, playground, support

## Versioning & Evolution

- [ ] **Phase 22** — Versioning strategies: URI, header, content negotiation
- [ ] **Phase 23** — Backward compatibility: additive changes, tolerance
- [ ] **Phase 24** — Deprecation: policies, sunset headers, migration
- [ ] **Phase 25** — Contract testing: consumer-driven contracts, breaking changes

## GraphQL

- [ ] **Phase 26** — Schema design: types, fields, relationships, nullability
- [ ] **Phase 27** — Queries & mutations: arguments, aliases, fragments
- [ ] **Phase 28** — Resolvers: data fetching, batching, loaders
- [ ] **Phase 29** — Subscriptions: realtime, events, scaling
- [ ] **Phase 30** — Performance: N+1 queries, depth limits, cost analysis

## gRPC & RPC

- [ ] **Phase 31** — Protobufs: message definitions, field numbers, types
- [ ] **Phase 32** — Services: unary, server/client streaming, bidirectional
- [ ] **Phase 33** — Error handling: status codes, error details
- [ ] **Phase 34** — gRPC ecosystem: gateways, interop, codegen

## API Testing & Quality

- [ ] **Phase 35** — Unit tests: handlers, services, validation logic
- [ ] **Phase 36** — Integration tests: end-to-end flows, test databases
- [ ] **Phase 37** — Contract tests: provider verification, consumer tests
- [ ] **Phase 38** — Performance testing: load, latency, throughput targets
- [ ] **Phase 39** — Mocking & simulation: test doubles, sandboxes, fake data

## API Platforms & Operations

- [ ] **Phase 40** — API gateways: routing, auth, throttling, transforms
- [ ] **Phase 41** — Rate limiting at scale: distributed limits, tiers
- [ ] **Phase 42** — Observability: logs, metrics, tracing, alerting
- [ ] **Phase 43** — API analytics: usage, errors, adoption insights
- [ ] **Phase 44** — Developer experience: SDKs, code samples, onboarding

## Advanced API Patterns

- [ ] **Phase 45** — Webhooks: subscriptions, delivery, retries, signatures
- [ ] **Phase 46** — Event-driven APIs: events, topics, async consumers
- [ ] **Phase 47** — Async patterns: request/reply, callbacks, message queues

## Recommended Learning Path (priority order)

1. **Phase 1–5** — HTTP fundamentals
2. **Phase 6–11** — REST design principles
3. **Phase 12–17** — API security
4. **Phase 18–21** — Documentation
5. **Phase 22–25** — Versioning & evolution
6. **Phase 35–39** — Testing & quality
7. **Phase 40–44** — Platforms & operations

> Focus on building real projects — employers hire mid-level backend devs for clean, secure, well-documented APIs plus ownership of features end-to-end.
