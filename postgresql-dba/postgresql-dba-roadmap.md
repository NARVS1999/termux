# PostgreSQL DBA Roadmap: Fundamentals → Intermediate

> General knowledge for data engineers, with PostgreSQL-specific context.

## PostgreSQL Fundamentals

- [ ] **Phase 1** — Installation: packages, initdb, service management, directories
- [ ] **Phase 2** — psql basics: connecting, meta-commands, output formats, scripting
- [ ] **Phase 3** — Configuration: postgresql.conf, pg_hba.conf, shared_buffers, work_mem
- [ ] **Phase 4** — Data types: numerics, text, JSON/JSONB, arrays, ranges, UUIDs
- [ ] **Phase 5** — Client tools & ecosystem: pgAdmin, DBeaver, libpq, drivers

## SQL Mastery

- [ ] **Phase 6** — DDL & DML: CREATE/ALTER, INSERT/UPDATE/DELETE, TRUNCATE, RETURNING
- [ ] **Phase 7** — Joins & subqueries: inner/outer joins, lateral, correlated subqueries
- [ ] **Phase 8** — Aggregations: GROUP BY, HAVING, window functions, FILTER clauses
- [ ] **Phase 9** — CTEs & recursion: WITH, recursive CTEs, temporary tables
- [ ] **Phase 10** — Functions & triggers: PL/pgSQL, trigger functions, event triggers
- [ ] **Phase 11** — Views & materialized views: creation, refresh, incremental refresh

## Database Design

- [ ] **Phase 12** — Normalization: normal forms, denormalization tradeoffs
- [ ] **Phase 13** — Constraints: PK/FK, unique, check, exclusion, deferrable
- [ ] **Phase 14** — Schema migrations: versioning, rollback, zero-downtime changes
- [ ] **Phase 15** — Model tuning: data types choice, generated columns, partitioning plans

## Indexing & Query Tuning

- [ ] **Phase 16** — Index types: B-tree, GIN, GiST, BRIN, hash, when each applies
- [ ] **Phase 17** — Index design: composite keys, partial indexes, covering indexes
- [ ] **Phase 18** — EXPLAIN ANALYZE: plan nodes, costs, buffers, interpreting output
- [ ] **Phase 19** — Query planner: statistics, cost model, planner hints, settings
- [ ] **Phase 20** — Vacuum & bloat: dead tuples, autovacuum, bloat management
- [ ] **Phase 21** — Common bottlenecks: seq scans, missing indexes, bad joins, N+1

## Backup & Recovery

- [ ] **Phase 22** — Logical backups: pg_dump, pg_restore, format options
- [ ] **Phase 23** — Physical backups: pg_basebackup, backup tools, consistency
- [ ] **Phase 24** — WAL archiving & PITR: archive_command, recovery targets
- [ ] **Phase 25** — Restore strategies: full restores, partial restores, validation
- [ ] **Phase 26** — Disaster recovery: RPO/RTO, backup testing, retention policies

## Replication & High Availability

- [ ] **Phase 27** — Streaming replication: primary/standby, synchronous vs async
- [ ] **Phase 28** — Failover & HA: Patroni, repmgr, promotion, switchover
- [ ] **Phase 29** — Connection pooling: PgBouncer, pool modes, transaction pooling
- [ ] **Phase 30** — Logical replication: publication/subscription, use cases
- [ ] **Phase 31** — Multi-node setups: clusters, extensions for scale-out

## Security & Access Control

- [ ] **Phase 32** — Roles & privileges: GRANT/REVOKE, role inheritance, ownership
- [ ] **Phase 33** — Row-level security: policies, per-user visibility
- [ ] **Phase 34** — Transport security: SSL/TLS, certificates, host-based auth
- [ ] **Phase 35** — Audit logging: log settings, extension-based auditing, pgaudit

## Performance & Monitoring

- [ ] **Phase 36** — Monitoring tools: pg_stat_activity, pg_stat_statements, views
- [ ] **Phase 37** — Slow query tracking: log_min_duration, sampling, profiling
- [ ] **Phase 38** — Locks & deadlocks: lock types, deadlock detection, contention
- [ ] **Phase 39** — Resource tuning: memory, disk I/O, WAL settings, checkpoint tuning
- [ ] **Phase 40** — Capacity planning: growth trends, table sizes, bloat trends

## Maintenance & Operations

- [ ] **Phase 41** — Vacuum management: autovacuum tuning, manual vacuum, freeze
- [ ] **Phase 42** — Upgrades: major vs minor, pg_upgrade, rollback plans
- [ ] **Phase 43** — Partitioning: declarative partitioning, partition pruning, maintenance
- [ ] **Phase 44** — Data archiving: retention policies, old data strategies

## Ecosystem & Cloud

- [ ] **Phase 45** — Extensions: pg_trgm, PostGIS, pgvector, citext
- [ ] **Phase 46** — Time-series: TimescaleDB, hypertables, compression
- [ ] **Phase 47** — Cloud PostgreSQL: RDS/Aurora, managed services, pros and cons

## Recommended Learning Path (priority order)

1. **Phase 1–5** — PostgreSQL fundamentals
2. **Phase 6–11** — SQL mastery
3. **Phase 16–18** — Indexing & EXPLAIN
4. **Phase 22–26** — Backup & recovery
5. **Phase 27–31** — Replication & HA
6. **Phase 36–40** — Monitoring & tuning
7. **Phase 41–44** — Maintenance & operations

> Focus on building real projects — employers hire mid-level DBAs for clean, performant, reliable databases plus ownership of data infrastructure end-to-end.
