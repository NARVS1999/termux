# System Design Roadmap: Fundamentals → Intermediate

> General knowledge for software developers, with system-design-specific context.

## Fundamentals (Prerequisites)

- [ ] **Phase 1** — System design basics: components, clients, servers, data flows
- [ ] **Phase 2** — Requirements: functional vs non-functional, constraints
- [ ] **Phase 3** — Tradeoffs: latency vs throughput, consistency vs availability
- [ ] **Phase 4** — Back-of-envelope estimation: QPS, storage, bandwidth

## Scalability

- [ ] **Phase 5** — Scaling models: vertical vs horizontal, scale-out patterns
- [ ] **Phase 6** — Load balancing: algorithms, layers, health checks, sticky sessions
- [ ] **Phase 7** — Stateless design: session handling, horizontal growth
- [ ] **Phase 8** — Auto-scaling: metrics, policies, cost control
- [ ] **Phase 9** — CDNs: edge caching, invalidation, dynamic content

## Caching

- [ ] **Phase 10** — Caching strategies: cache-aside, write-through, write-back
- [ ] **Phase 11** — Redis: data structures, persistence, eviction policies
- [ ] **Phase 12** — Cache invalidation: TTLs, versioning, event-driven invalidation
- [ ] **Phase 13** — Consistency: stale reads, cold starts, stampede prevention

## Databases

- [ ] **Phase 14** — SQL vs NoSQL: workloads, schemas, tradeoffs
- [ ] **Phase 15** — Replication: leader-follower, multi-leader, failover
- [ ] **Phase 16** — Sharding: keys, rebalancing, hot spots
- [ ] **Phase 17** — Indexing at scale: covering indexes, partial indexes
- [ ] **Phase 18** — Transactions & isolation: ACID, distributed concerns
- [ ] **Phase 19** — Analytics stores: columnar stores, data warehouses, OLAP

## Distributed Systems

- [ ] **Phase 20** — CAP theorem: consistency, availability, partition tolerance
- [ ] **Phase 21** — Consistency models: strong, eventual, causal, quorum reads
- [ ] **Phase 22** — Distributed transactions: sagas, outbox, two-phase commit
- [ ] **Phase 23** — Consensus: Raft, Paxos, leader election
- [ ] **Phase 24** — Failure handling: timeouts, retries, exponential backoff, circuit breakers
- [ ] **Phase 25** — Distributed tracing: spans, trace IDs, sampling

## Messaging & Queues

- [ ] **Phase 26** — Message queues: Kafka, RabbitMQ, SQS, use cases
- [ ] **Phase 27** — Pub/sub: topics, subscriptions, fan-out
- [ ] **Phase 28** — Stream processing: consumers, offsets, exactly-once
- [ ] **Phase 29** — Backpressure: flow control, buffering, rejection
- [ ] **Phase 30** — Event-driven design: events, schemas, evolution

## API Design at Scale

- [ ] **Phase 31** — API gateways: routing, auth, aggregation
- [ ] **Phase 32** — Rate limiting: token bucket, sliding window, distributed limits
- [ ] **Phase 33** — Idempotency: keys, retries, safe retry semantics
- [ ] **Phase 34** — Versioning: strategies, deprecation, migrations

## Microservices & Architecture

- [ ] **Phase 35** — Microservices vs monolith: boundaries, tradeoffs, strangler pattern
- [ ] **Phase 36** — Service discovery: registries, DNS, health checks
- [ ] **Phase 37** — Resilience: circuit breakers, bulkheads, fallbacks
- [ ] **Phase 38** — Observability: logs, metrics, traces, dashboards, SLOs
- [ ] **Phase 39** — Deployment strategies: blue-green, canary, rolling, feature flags

## Case Studies

- [ ] **Phase 40** — Social feed: timelines, caching, fan-out
- [ ] **Phase 41** — URL shortener: encoding, redirects, analytics
- [ ] **Phase 42** — Chat system: websockets, presence, storage
- [ ] **Phase 43** — Payment system: idempotency, ledger, reconciliation

## Interview Practice

- [ ] **Phase 44** — Interview formats: rounds, formats, expectations
- [ ] **Phase 45** — Whiteboarding: frameworks, structure, communication
- [ ] **Phase 46** — Estimation drills: QPS, storage, cost calculations
- [ ] **Phase 47** — Mock interviews: feedback, iteration, speed

## Recommended Learning Path (priority order)

1. **Phase 1–4** — Fundamentals
2. **Phase 5–9** — Scalability
3. **Phase 10–13** — Caching
4. **Phase 14–19** — Databases
5. **Phase 20–25** — Distributed systems
6. **Phase 26–30** — Messaging
7. **Phase 40–43** — Case studies

> Focus on building real projects — employers hire mid-level engineers for clean, scalable, well-designed systems plus ownership of features end-to-end.
