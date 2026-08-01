# Node.js Developer Roadmap: Fundamentals → Intermediate

> General knowledge for backend developers, with Node.js-specific context.

## Node.js Fundamentals (Prerequisites)

- [ ] **Phase 1** — Runtime basics: installing Node, running scripts, REPL
- [ ] **Phase 2** — npm: init, install, scripts, dev vs prod deps, lockfiles
- [ ] **Phase 3** — Package.json: fields, semver, versions, publishing
- [ ] **Phase 4** — Modules: CommonJS, ES modules, require vs import
- [ ] **Phase 5** — Globals & process: process.env, argv, exit codes, globalThis

## Event Loop & Async

- [ ] **Phase 6** — Event loop: phases, microtasks, timers, blocking code
- [ ] **Phase 7** — Async patterns: callbacks, promises, async/await
- [ ] **Phase 8** — Streams: readable, writable, transform, piping
- [ ] **Phase 9** — Buffers: allocation, encoding, parsing
- [ ] **Phase 10** — Concurrency: worker threads, child processes, cluster

## Core Modules

- [ ] **Phase 11** — fs: reading, writing, watching, streams
- [ ] **Phase 12** — path & url: joining, parsing, resolving
- [ ] **Phase 13** — http & https: servers, requests, routing basics
- [ ] **Phase 14** — os & util: system info, helpers, promisify
- [ ] **Phase 15** — events: EventEmitter, custom events, error events

## Express & Web Frameworks

- [ ] **Phase 16** — Express basics: app setup, routes, handlers
- [ ] **Phase 17** — Middleware: built-in, custom, error middleware, order
- [ ] **Phase 18** — Routing: params, query strings, routers, nesting
- [ ] **Phase 19** — Error handling: async errors, status codes, error objects
- [ ] **Phase 20** — Validation: zod/joi, request schemas, sanitization
- [ ] **Phase 21** — Views & rendering: templates, static files, sessions

## Databases

- [ ] **Phase 22** — SQL with Node: pg driver, prepared statements, pools
- [ ] **Phase 23** — Prisma: schema, client, queries, relations, migrations
- [ ] **Phase 24** — MongoDB & Mongoose: models, schemas, queries
- [ ] **Phase 25** — Redis: caching, sessions, queues basics
- [ ] **Phase 26** — Migrations & seeds: versioning, data setup

## Authentication & Security

- [ ] **Phase 27** — Auth basics: sessions vs tokens, cookie handling
- [ ] **Phase 28** — JWT: signing, verifying, expiry, refresh tokens
- [ ] **Phase 29** — Password security: bcrypt, hashing, timing attacks
- [ ] **Phase 30** — Authorization: roles, permissions, middleware guards
- [ ] **Phase 31** — Security best practices: helmet, input validation, OWASP, rate limiting

## REST APIs

- [ ] **Phase 32** — API design: resources, methods, status codes
- [ ] **Phase 33** — Pagination & filtering: queries, cursors, sorting
- [ ] **Phase 34** — File uploads: multer, storage, validation, serving
- [ ] **Phase 35** — WebSockets: Socket.io, rooms, realtime events
- [ ] **Phase 36** — Background jobs: BullMQ, queues, workers, scheduling

## Testing & Debugging

- [ ] **Phase 37** — Unit testing: Jest/Vitest, assertions, coverage
- [ ] **Phase 38** — Integration testing: supertest, test databases, fixtures
- [ ] **Phase 39** — Mocking: spies, stubs, module mocks
- [ ] **Phase 40** — Debugging: inspector, logs, stack traces, profiling
- [ ] **Phase 41** — Code quality: linting, formatting, type checks

## Deployment & Performance

- [ ] **Phase 42** — Process management: PM2, clustering, restarts
- [ ] **Phase 43** — Docker: images, multi-stage builds, compose
- [ ] **Phase 44** — Deployment: platforms, env configs, health checks
- [ ] **Phase 45** — Monitoring: logs, metrics, uptime, error tracking
- [ ] **Phase 46** — Performance: profiling, memory leaks, load testing
- [ ] **Phase 47** — Caching strategies: HTTP cache, Redis cache, invalidation

## Recommended Learning Path (priority order)

1. **Phase 1–5** — Node fundamentals
2. **Phase 6–10** — Event loop & async
3. **Phase 16–21** — Express
4. **Phase 22–26** — Databases
5. **Phase 27–31** — Auth & security
6. **Phase 37–41** — Testing
7. **Phase 42–47** — Deployment & performance

> Focus on building real projects — employers hire mid-level Node.js devs for clean, performant, well-tested code plus ownership of features end-to-end.
