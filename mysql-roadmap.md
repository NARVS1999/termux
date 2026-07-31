# MySQL Database Design Roadmap: Fundamentals → Intermediate

> General knowledge for data engineers, with MySQL-specific context.

## Relational Database Fundamentals

- [x] **Phase 1** — Relational model: tables, rows, columns, schemas, data integrity
- [x] **Phase 2** — SQL fundamentals: SELECT, INSERT, UPDATE, DELETE, basic syntax
- [x] **Phase 3** — Data types: INT, VARCHAR, TEXT, DATE, TIMESTAMP, BLOB, ENUM, SET
- [x] **Phase 4** — Operators & expressions: comparison, logical, arithmetic, BETWEEN, IN, LIKE

## Table Design & Constraints

- [x] **Phase 5** — CREATE TABLE: column definitions, NOT NULL, DEFAULT, AUTO_INCREMENT
- [x] **Phase 6** — Primary keys: single-column, composite, surrogate vs natural keys
- [x] **Phase 7** — Foreign keys: REFERENCES, ON DELETE CASCADE/SET NULL, ON UPDATE
- [x] **Phase 8** — UNIQUE, CHECK constraints, indexes basics, data validation at DB level

## Normalization & Design Principles

- [x] **Phase 9** — Normalization: 1NF, 2NF, 3NF, Boyce-Codd normal form
- [x] **Phase 10** — Denormalization: tradeoffs, read-heavy vs write-heavy, materialized views
- [x] **Phase 11** — ER diagrams: entities, attributes, relationships, cardinality (1:1, 1:N, M:N)
- [x] **Phase 12** — Schema design patterns: audit tables, soft deletes, polymorphic associations

## Relationships & Joins

- [ ] **Phase 13** — One-to-one relationships: implementation, foreign key placement
- [ ] **Phase 14** — One-to-many relationships: junction tables, cascade rules
- [ ] **Phase 15** — Many-to-many relationships: junction tables, composite keys
- [ ] **Phase 16** — JOIN types: INNER, LEFT, RIGHT, FULL, CROSS, self-join

## Advanced SQL Queries

- [ ] **Phase 17** — Aggregate functions: COUNT, SUM, AVG, MIN, MAX, GROUP BY, HAVING
- [ ] **Phase 18** — Subqueries: correlated, non-correlated, EXISTS, IN, ANY, ALL
- [ ] **Phase 19** — Window functions: ROW_NUMBER, RANK, DENSE_RANK, OVER, PARTITION BY
- [ ] **Phase 20** — Common Table Expressions: WITH, recursive CTEs, hierarchical queries
- [ ] **Phase 21** — UNION, INTERSECT, EXCEPT, set operations, UNION ALL vs UNION

## Indexes & Query Optimization

- [ ] **Phase 22** — Index fundamentals: B-tree, hash, why indexes speed up reads
- [ ] **Phase 23** — Creating indexes: single-column, composite, covering indexes
- [ ] **Phase 24** — EXPLAIN/ANALYZE: reading query plans, identifying bottlenecks
- [ ] **Phase 25** — Index best practices: cardinality, selectivity, index maintenance
- [ ] **Phase 26** — Query optimization: slow query log, profiling, query rewriting

## Transactions & Data Integrity

- [ ] **Phase 27** — ACID properties: atomicity, consistency, isolation, durability
- [ ] **Phase 28** — Transaction control: BEGIN, COMMIT, ROLLBACK, SAVEPOINT
- [ ] **Phase 29** — Isolation levels: READ UNCOMMITTED, READ COMMITTED, REPEATABLE READ, SERIALIZABLE
- [ ] **Phase 30** — Locking: row locks, table locks, deadlock prevention, SELECT FOR UPDATE
- [ ] **Phase 31** — Concurrency control: MVCC, optimistic vs pessimistic locking

## Stored Procedures, Functions & Triggers

- [ ] **Phase 32** — Stored procedures: CREATE PROCEDURE, parameters, IN/OUT/INOUT
- [ ] **Phase 33** — Stored functions: CREATE FUNCTION, return values, deterministic vs non-deterministic
- [ ] **Phase 34** — Triggers: BEFORE/AFTER INSERT/UPDATE/DELETE, NEW/OLD records
- [ ] **Phase 35** — Events & scheduling: CREATE EVENT, event scheduler, cron-like tasks

## MySQL Administration

- [ ] **Phase 36** — User management: CREATE USER, GRANT, REVOKE, roles & privileges
- [ ] **Phase 37** — Backup & recovery: mysqldump, mysqlpump, xtrabackup, point-in-time recovery
- [ ] **Phase 38** — Replication: master-slave, GTID, binlog, read replicas
- [ ] **Phase 39** — Partitioning: RANGE, LIST, HASH, KEY, partition pruning

## Performance Tuning & Scaling

- [ ] **Phase 40** — MySQL config tuning: innodb_buffer_pool_size, query_cache, thread_cache
- [ ] **Phase 41** — InnoDB deep-dive: buffer pool, redo log, undo log, doublewrite buffer
- [ ] **Phase 42** — Connection pooling: thread per connection, pool sizes, connection limits
- [ ] **Phase 43** — Scaling strategies: read replicas, sharding, connection multiplexing

## Real-World Design Patterns

- [ ] **Phase 44** — E-commerce schema: products, orders, inventory, pricing, transactions
- [ ] **Phase 45** — User management: users, roles, permissions, sessions, audit logs
- [ ] **Phase 46** — Time-series data: partitioning by date, archiving, compression
- [ ] **Phase 47** — Migration strategies: schema changes online, zero-downtime migrations

## Recommended Learning Path (priority order)

1. **Phase 1** — Relational model fundamentals
2. **Phase 5–8** — Table design & constraints
3. **Phase 9** — Normalization (3NF)
4. **Phase 16** — JOINs
5. **Phase 22–24** — Indexes & EXPLAIN
6. **Phase 27–28** — ACID & transactions
7. **Phase 44** — Real-world schema design

> Focus on building real projects — employers hire mid-level data engineers for clean, normalized, performant database designs plus ownership of data architecture end-to-end.
