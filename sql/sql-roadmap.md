# SQL Developer Roadmap: Fundamentals → Intermediate

> General knowledge for data engineers, with SQL-specific context.

## SQL Fundamentals

- [x] **Phase 1** — SELECT basics: columns, expressions, literals, LIMIT
- [x] **Phase 2** — WHERE & filtering: operators, IN, BETWEEN, LIKE, NULL handling
- [x] **Phase 3** — ORDER BY & pagination: sorting, multiple keys, OFFSET/FETCH
- [x] **Phase 4** — DISTINCT & aliases: deduplication, column aliases, table aliases
- [x] **Phase 5** — Data types: numeric, string, date/time, booleans, casting

## Joins & Subqueries

- [x] **Phase 6** — INNER JOIN: matching rows, join conditions, multiple joins
- [x] **Phase 7** — Outer joins: LEFT, RIGHT, FULL, unmatched rows, nulls
- [x] **Phase 8** — Self joins & cross joins: hierarchies, comparisons, Cartesian products
- [x] **Phase 9** — Subqueries: scalar, row, table subqueries
- [x] **Phase 10** — Correlated subqueries: per-row evaluation, EXISTS
- [x] **Phase 11** — Set operations: UNION, INTERSECT, EXCEPT, precedence

## Aggregation & Window Functions

- [x] **Phase 12** — GROUP BY: grouping, grouping sets, ROLLUP, CUBE
- [x] **Phase 13** — HAVING: filtering groups, comparisons with aggregates
- [x] **Phase 14** — Aggregate functions: COUNT, SUM, AVG, MIN, MAX, DISTINCT aggregates
- [x] **Phase 15** — Window functions: PARTITION BY, ORDER BY, frames
- [x] **Phase 16** — Ranking functions: ROW_NUMBER, RANK, DENSE_RANK, NTILE

## Data Manipulation

- [x] **Phase 17** — INSERT: single, multi-row, SELECT INTO, RETURNING
- [x] **Phase 18** — UPDATE & DELETE: filters, joins, cascades, RETURNING
- [x] **Phase 19** — Transactions: BEGIN, COMMIT, ROLLBACK, savepoints
- [x] **Phase 20** — DDL: CREATE/DROP/ALTER tables, constraints, indexes
- [x] **Phase 21** — UPSERT: ON CONFLICT, MERGE, idempotent writes

## Query Optimization

- [x] **Phase 22** — Indexes: purpose, types, tradeoffs, column order
- [x] **Phase 23** — EXPLAIN plans: reading plans, costs, scan types
- [x] **Phase 24** — Query rewriting: join order, subquery unnesting, simplification
- [x] **Phase 25** — Normalization: normal forms, avoiding redundancy, tradeoffs
- [x] **Phase 26** — Denormalization: when to duplicate, materialization
- [x] **Phase 27** — Performance pitfalls: full scans, N+1, missing indexes, functions on columns

## Advanced SQL

- [x] **Phase 28** — CTEs: WITH clauses, readability, recursion
- [x] **Phase 29** — Recursive queries: hierarchies, graphs, traversal
- [x] **Phase 30** — Stored procedures: functions, PL/SQL basics, permissions
- [x] **Phase 31** — Triggers: event-driven logic, auditing, constraints
- [x] **Phase 32** — Views: simple, complex, materialized, permissions

## Database Design

- [x] **Phase 33** — Data modeling: entities, attributes, relationships
- [x] **Phase 34** — ERD: diagrams, cardinality, crow's foot notation
- [x] **Phase 35** — Keys & constraints: primary, foreign, unique, check, defaults
- [x] **Phase 36** — Normalization forms: 1NF-3NF, BCNF, practical balance
- [x] **Phase 37** — Schema migrations: versioning, rollback, data backfills

## Concurrency & Transactions

- [x] **Phase 38** — ACID: atomicity, consistency, isolation, durability
- [x] **Phase 39** — Isolation levels: read committed, repeatable read, serializable
- [x] **Phase 40** — Locks & deadlocks: shared/exclusive, blocking, detection
- [x] **Phase 41** — MVCC: snapshot isolation, versions, vacuum/cleanup
- [x] **Phase 42** — Concurrency patterns: optimistic locking, retries

## SQL in Practice

- [x] **Phase 43** — Database selection: PostgreSQL, MySQL, SQLite, workloads
- [x] **Phase 44** — Dialect differences: syntax, functions, vendor features
- [x] **Phase 45** — Security: privileges, injection prevention, encryption
- [x] **Phase 46** — Backup & restore: dumps, point-in-time, recovery testing
- [x] **Phase 47** — SQL in applications: ORMs, parameterization, connection pooling

## Recommended Learning Path (priority order)

1. **Phase 1–5** — SQL fundamentals
2. **Phase 6–11** — Joins & subqueries
3. **Phase 12–16** — Aggregation & windows
4. **Phase 22–27** — Query optimization
5. **Phase 33–37** — Database design
6. **Phase 28–32** — Advanced SQL
7. **Phase 38–42** — Concurrency & transactions

> Focus on building real projects — employers hire mid-level data engineers for clean, efficient, well-indexed queries plus ownership of data end-to-end.
