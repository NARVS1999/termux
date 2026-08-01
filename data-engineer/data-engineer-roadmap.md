# Data Engineer Roadmap: Fundamentals → Intermediate

> General knowledge for data engineers, with data-engineering-specific context.

## Prerequisites

- [ ] **Phase 1** — Linux & CLI: shell navigation, file ops, pipes, process management
- [ ] **Phase 2** — Python basics: variables, types, control flow, functions, error handling
- [ ] **Phase 3** — SQL basics: SELECT, WHERE, GROUP BY, ORDER BY, LIMIT
- [ ] **Phase 4** — Git & version control: commits, branches, pull requests, repos

## Python for Data Engineering

- [ ] **Phase 5** — Data structures: lists, dicts, sets, tuples, comprehensions, generators
- [ ] **Phase 6** — File handling: CSV/JSON/Parquet I/O, encoding, streaming reads
- [ ] **Phase 7** — pandas basics: DataFrames, filtering, joins, groupby, memory usage
- [ ] **Phase 8** — Packaging & envs: venv, pip, pyproject, dependency pinning
- [ ] **Phase 9** — API & web data: requests, pagination, auth, parsing responses

## SQL & Databases

- [ ] **Phase 10** — Advanced SQL: joins, subqueries, CTEs, window functions
- [ ] **Phase 11** — Data modeling: normalization, star schema, facts, dimensions, keys
- [ ] **Phase 12** — OLTP vs OLAP: transactional vs analytical workloads, columnar stores
- [ ] **Phase 13** — NoSQL basics: document, key-value, wide-column stores, use cases
- [ ] **Phase 14** — Indexing & performance: indexes, EXPLAIN plans, partition pruning
- [ ] **Phase 15** — Transactions: ACID, isolation levels, batch idempotency

## Data Warehousing

- [ ] **Phase 16** — Warehouse concepts: Snowflake, BigQuery, Redshift, storage vs compute
- [ ] **Phase 17** — Schema design: star schema, snowflake schema, slowly changing dimensions
- [ ] **Phase 18** — dbt: models, materializations, tests, docs, lineage
- [ ] **Phase 19** — Partitioning & clustering: partition keys, clustering, micro-partitions
- [ ] **Phase 20** — Lakehouse: Delta Lake, Iceberg, Hudi, medallion architecture

## ETL/ELT Pipelines

- [ ] **Phase 21** — ETL vs ELT: when to transform before vs after loading
- [ ] **Phase 22** — Batch pipelines: scheduling, dependencies, retries, backfills
- [ ] **Phase 23** — Ingestion: CDC, APIs, file drops, database extracts, connectors
- [ ] **Phase 24** — Orchestration: Airflow DAGs, operators, sensors, task dependencies
- [ ] **Phase 25** — Incremental loads: watermarks, idempotency, deduplication, upserts
- [ ] **Phase 26** — Data quality checks: validation, expectations, anomaly alerts

## Streaming & Realtime

- [ ] **Phase 27** — Kafka basics: topics, partitions, offsets, brokers
- [ ] **Phase 28** — Producers & consumers: serialization, keying, consumer groups
- [ ] **Phase 29** — Stream processing: Flink/Spark Streaming, windows, exactly-once
- [ ] **Phase 30** — CDC pipelines: Debezium, log-based capture, schema evolution

## Big Data Tools

- [ ] **Phase 31** — Spark basics: DataFrames, RDDs, lazy evaluation, actions
- [ ] **Phase 32** — Spark SQL & optimization: partitioning, caching, shuffle tuning
- [ ] **Phase 33** — Hadoop ecosystem: HDFS, YARN, Hive basics
- [ ] **Phase 34** — Cloud data platforms: BigQuery, Snowflake, Databricks workflows

## Cloud & Infrastructure

- [ ] **Phase 35** — Cloud storage: S3/GCS/blob, lifecycle policies, versioning
- [ ] **Phase 36** — Containerized pipelines: Docker images, resource limits, ephemeral jobs
- [ ] **Phase 37** — IaC basics: Terraform resources, environments, drift management
- [ ] **Phase 38** — Pipeline monitoring: logs, metrics, alerts, SLAs, cost tracking

## Data Governance & Quality

- [ ] **Phase 39** — Data lineage: cataloging, impact analysis, field-level lineage
- [ ] **Phase 40** — Data cataloging: metadata, discovery, ownership, glossary
- [ ] **Phase 41** — Quality frameworks: Great Expectations, Soda, data contracts
- [ ] **Phase 42** — Privacy & compliance: PII handling, GDPR/CCPA, retention, masking

## Career & Collaboration

- [ ] **Phase 43** — Documentation: pipeline docs, runbooks, schema docs
- [ ] **Phase 44** — Cross-team collaboration: analysts, scientists, engineers
- [ ] **Phase 45** — Visualization basics: dashboards, trends, communicating data
- [ ] **Phase 46** — Project management: scoping, estimation, stakeholder updates
- [ ] **Phase 47** — Interview prep: data modeling questions, case studies, system design

## Recommended Learning Path (priority order)

1. **Phase 1–4** — Prerequisites
2. **Phase 5–9** — Python for data engineering
3. **Phase 10–15** — SQL & databases
4. **Phase 16–20** — Data warehousing
5. **Phase 21–26** — ETL/ELT pipelines
6. **Phase 27–30** — Streaming basics
7. **Phase 39–42** — Data governance

> Focus on building real projects — employers hire mid-level data engineers for clean, reliable, well-tested pipelines plus ownership of data end-to-end.
