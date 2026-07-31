# System Architecture Roadmap: Fundamentals → Intermediate

> General knowledge for software architects, with system design-specific context.

## Networking Fundamentals

- [x] **Phase 1** — OSI model, TCP/IP, HTTP/HTTPS protocols, ports, DNS resolution
- [x] **Phase 2** — REST, GraphQL, gRPC, WebSockets: API protocol tradeoffs
- [x] **Phase 3** — Load balancing algorithms: round-robin, least connections, consistent hashing
- [x] **Phase 4** — DNS: records types, resolution process, TTL, CDN routing
- [x] **Phase 5** — TLS/SSL: certificates, handshake, encryption at rest vs in transit

## Architecture Patterns

- [x] **Phase 6** — Monolithic architecture: benefits, drawbacks, when to use
- [x] **Phase 7** — Microservices: decomposition, service boundaries, communication patterns
- [x] **Phase 8** — Serverless: functions-as-a-service, event-driven, cold starts
- [x] **Phase 9** — Event-driven architecture: event sourcing, CQRS, message queues
- [x] **Phase 10** — Service mesh: sidecar proxies, mTLS, traffic management
- [x] **Phase 11** — Domain-driven design: bounded contexts, aggregates, domain events

## System Design Principles

- [x] **Phase 12** — CAP theorem: consistency, availability, partition tolerance tradeoffs
- [x] **Phase 13** — Horizontal vs vertical scaling: when to scale out vs scale up
- [x] **Phase 14** — High availability: redundancy, failover, health checks
- [x] **Phase 15** — Fault tolerance: graceful degradation, bulkheads, circuit breakers
- [x] **Phase 16** — Idempotency: safe retries, deduplication, exactly-once semantics

## Data Architecture

- [x] **Phase 17** — SQL vs NoSQL: relational, document, key-value, graph, time-series
- [x] **Phase 18** — Database replication: master-slave, master-master, leader election
- [x] **Phase 19** — Sharding strategies: hash-based, range-based, geo-based
- [x] **Phase 20** — Caching: Redis, Memcached, cache-aside, write-through, write-behind
- [x] **Phase 21** — Message queues: RabbitMQ, Kafka, SQS, publish-subscribe vs point-to-point
- [x] **Phase 22** — Data consistency: eventual consistency, strong consistency, Saga pattern

## Infrastructure & Networking

- [x] **Phase 23** — Containers: Docker, container orchestration, images vs containers
- [x] **Phase 24** — Kubernetes: pods, services, deployments, ingress, ConfigMaps
- [x] **Phase 25** — Load balancers: L4 vs L7, health checks, sticky sessions
- [x] **Phase 26** — CDNs: edge caching, origin servers, cache invalidation
- [x] **Phase 27** — Reverse proxies: Nginx, HAProxy, API gateways

## Security Architecture

- [x] **Phase 28** — Authentication: OAuth2, JWT, session tokens, API keys
- [x] **Phase 29** — Authorization: RBAC, ABAC, policy engines, least privilege
- [x] **Phase 30** — Network security: VPC, firewalls, WAF, DDoS protection
- [x] **Phase 31** — Secrets management: vault, key rotation, encryption at rest

## DevOps & Deployment

- [x] **Phase 32** — CI/CD pipelines: build, test, deploy stages, rollback strategies
- [x] **Phase 33** — Blue-green deployment: zero-downtime, traffic switching
- [x] **Phase 34** — Canary releases: incremental rollout, monitoring, rollback
- [x] **Phase 35** — Infrastructure as code: Terraform, CloudFormation, Ansible
- [x] **Phase 36** — GitOps: declarative infrastructure, ArgoCD, Flux

## Monitoring & Observability

- [ ] **Phase 37** — Metrics: Prometheus, Grafana, SLIs, SLOs, SLAs
- [ ] **Phase 38** — Logging: structured logging, ELK stack, log aggregation
- [ ] **Phase 39** — Distributed tracing: Jaeger, Zipkin, OpenTelemetry
- [ ] **Phase 40** — Alerting: alert fatigue, escalation policies, incident response

## Performance & Scaling

- [ ] **Phase 41** — Caching strategies: Redis patterns, cache invalidation, TTL
- [ ] **Phase 42** — Database optimization: query tuning, connection pooling, read replicas
- [ ] **Phase 43** — Rate limiting: token bucket, sliding window, API throttling
- [ ] **Phase 44** — Asynchronous processing: background jobs, event queues, batch processing

## Real-World System Design

- [ ] **Phase 45** — URL shortener: hashing, redirection, analytics, scaling
- [ ] **Phase 46** — Chat system: WebSockets, presence, message ordering, storage
- [ ] **Phase 47** — E-commerce platform: inventory, payments, search, recommendations

## Recommended Learning Path (priority order)

1. **Phase 1** — Networking fundamentals (TCP/IP, HTTP)
2. **Phase 6–7** — Monolith vs Microservices
3. **Phase 12** — CAP theorem
4. **Phase 17–18** — SQL vs NoSQL, replication
5. **Phase 20** — Caching strategies
6. **Phase 28** — Authentication & JWT
7. **Phase 37** — Monitoring & observability

> Focus on building real projects — employers hire mid-level architects for clean, scalable, well-documented system designs plus ownership of technical decisions end-to-end.
