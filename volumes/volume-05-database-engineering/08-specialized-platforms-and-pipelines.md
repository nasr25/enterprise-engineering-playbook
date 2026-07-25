# Specialized Data Platforms and Pipelines

- **DB-146** — Use document, key-value, graph, time-series, search, and analytical stores only when their access model and operational tradeoffs fit the workload.
- **DB-147** — NoSQL designs must define consistency, partitioning, key access patterns, item limits, indexing, and conflict behavior before implementation.
- **DB-148** — Caches must define source of truth, key ownership, TTL, invalidation, stampede protection, serialization, and failure behavior.
- **DB-149** — Search indexes are derived stores and must support replay, reindexing, alias-based cutover, and reconciliation with the source of truth.
- **DB-150** — Time-series retention, aggregation, cardinality, timestamp precision, and late-arriving data behavior must be explicit.
- **DB-151** — Analytical databases and warehouses must separate source-system semantics from reporting models through governed transformations.
- **DB-152** — ETL and ELT pipelines must be idempotent, observable, restartable, versioned, and capable of quarantine and replay.
- **DB-153** — Data quality controls must measure completeness, validity, uniqueness, consistency, timeliness, lineage, and reconciliation.
- **DB-154** — Metadata must identify business meaning, owner, classification, lineage, refresh cadence, quality status, and consumers.
- **DB-155** — Data contracts must define schema, semantics, compatibility, ownership, service levels, and change notification.