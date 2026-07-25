# Architecture and Data Modeling

## Principles

- **DB-001** — Select a data platform from workload, consistency, latency, scale, operational, compliance, and recovery requirements rather than team familiarity alone.
- **DB-002** — Every authoritative dataset must have one declared system of record.
- **DB-003** — Separate transactional, analytical, search, cache, and archival responsibilities when their workload characteristics conflict.
- **DB-004** — Document ownership, consumers, criticality, classification, retention, RPO, and RTO for each datastore.
- **DB-005** — Avoid shared databases across independently deployable services unless ownership and change coordination are explicitly governed.
- **DB-006** — Services must not read or modify another service's private schema directly.
- **DB-007** — Data duplication across bounded contexts must use explicit synchronization contracts and reconciliation controls.
- **DB-008** — Model business concepts and invariants before choosing tables, documents, indexes, or vendor-specific features.
- **DB-009** — Use stable, immutable identifiers for long-lived entities.
- **DB-010** — Do not expose storage-specific identifiers as external contracts without an intentional compatibility decision.
- **DB-011** — Define cardinality, optionality, ownership, lifecycle, and deletion behavior for every relationship.
- **DB-012** — Normalize transactional models to prevent update anomalies; denormalize only for measured read, reporting, or availability needs.
- **DB-013** — Every denormalized attribute must have a declared source of truth and synchronization strategy.
- **DB-014** — Model effective dates and history explicitly when business state is time-dependent.
- **DB-015** — Store timestamps in UTC and preserve source timezone or offset when legally or operationally relevant.
- **DB-016** — Use precise domain types for money, quantities, dates, identifiers, status, and structured values.
- **DB-017** — Never represent monetary values with binary floating-point types.
- **DB-018** — Use controlled vocabularies or reference data for governed classifications and statuses.
- **DB-019** — Document expected growth, access paths, write patterns, hotspots, and data distribution before production approval.
- **DB-020** — Maintain current logical and physical data models for critical systems.