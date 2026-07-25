# Schema, SQL, and Query Design

## Schema Standards

- **DB-021** — Use consistent, documented naming conventions for schemas, tables, columns, constraints, indexes, views, procedures, and migration files.
- **DB-022** — Names must describe business meaning and must not depend on unexplained abbreviations.
- **DB-023** — Every table or collection must have a defined key and ownership boundary.
- **DB-024** — Primary keys must be stable, non-null, and never reused.
- **DB-025** — Enforce required uniqueness with database constraints rather than application checks alone.
- **DB-026** — Enforce referential integrity in the datastore unless a documented distributed-data constraint prevents it.
- **DB-027** — Define explicit nullability; do not use null as an undocumented multi-purpose state.
- **DB-028** — Defaults must represent valid domain behavior and must not conceal missing required input.
- **DB-029** — Check constraints must enforce stable domain invariants where supported.
- **DB-030** — Cascading updates and deletes require explicit review because they can amplify mistakes and lock contention.

## Indexing

- **DB-031** — Create indexes from verified query access paths, not speculative convenience.
- **DB-032** — Every production query must have an understood execution plan at expected data volume.
- **DB-033** — Composite index order must reflect filtering, equality, range, joining, grouping, and ordering behavior.
- **DB-034** — Remove unused and redundant indexes after workload validation.
- **DB-035** — Include index maintenance and write amplification in capacity decisions.
- **DB-036** — Unique indexes may enforce business uniqueness but must handle normalization and case rules consistently.
- **DB-037** — Partial, filtered, functional, covering, spatial, or full-text indexes require a documented workload justification.
- **DB-038** — Index foreign keys and high-volume join columns when the execution plan demonstrates need.

## SQL and Query Rules

- **DB-039** — Parameterize all dynamic queries; never concatenate untrusted values into SQL.
- **DB-040** — Select only required columns; avoid unrestricted `SELECT *` in production application code.
- **DB-041** — Every list query must have bounded pagination or an explicit result limit.
- **DB-042** — Prefer keyset pagination for large or frequently changing datasets.
- **DB-043** — Avoid N+1 query behavior through batching, joins, prefetching, or explicit aggregate queries.
- **DB-044** — Avoid functions and implicit conversions on indexed predicates when they prevent index use.
- **DB-045** — Queries must have deterministic ordering when result order affects behavior or pagination.
- **DB-046** — Large data modifications must be batched and resumable.
- **DB-047** — Query timeouts must be defined by workload class.
- **DB-048** — Stored procedures, functions, triggers, and views must follow version control, review, testing, observability, and deployment standards.
- **DB-049** — Triggers must not contain hidden cross-domain workflows or unbounded external side effects.
- **DB-050** — Materialized views and derived tables must define refresh timing, staleness, ownership, and failure handling.