# Data Architecture

## Purpose

Data architecture defines ownership, integrity, lifecycle, access, movement, and evidence requirements for information used by enterprise systems.

## Rules

### ARC-089 — Every data domain must have an owner
Each authoritative dataset must have an accountable business owner and a technical custodian.

### ARC-090 — Systems of record must be declared
For every critical entity, the authoritative source and permitted replicas must be documented.

### ARC-091 — Data ownership follows business capability
A component must own the schema and mutation rules for the data representing its capability.

### ARC-092 — Cross-boundary access must use contracts
Consumers must access another domain's data through supported APIs, events, governed extracts, or approved read models.

### ARC-093 — Schema evolution must be backward compatible
Database and message schema changes must support staged deployment, rollback, and mixed-version operation.

### ARC-094 — Data classification must drive controls
Classification must determine encryption, access, logging, masking, retention, residency, and disposal requirements.

### ARC-095 — Data minimization is mandatory
Systems must collect, replicate, expose, and retain only the data required for defined purposes.

### ARC-096 — Retention and deletion must be designed
Each dataset must have retention, archival, legal-hold, deletion, and verification rules.

### ARC-097 — Derived data must be traceable
Reports, aggregates, features, and analytical datasets must record source, transformation, freshness, and quality expectations.

### ARC-098 — Replication must declare consistency
Replicas and read models must specify acceptable staleness, reconciliation behavior, and recovery method.

### ARC-099 — Data quality must be measurable
Critical data must have defined completeness, validity, uniqueness, consistency, timeliness, and accuracy checks.

### ARC-100 — Sensitive production data must not leak into lower environments
Use synthetic, anonymized, tokenized, or formally approved masked data for development and testing.

### ARC-101 — Bulk data movement must be governed
Imports, exports, migrations, and backfills require validation, restartability, reconciliation, audit evidence, and rollback planning.

### ARC-102 — Database technology must follow workload needs
Technology selection must be justified by consistency, query, scale, latency, lifecycle, skills, and operational requirements.

## Required Data View

Architecture evidence should identify:

- systems of record
- domain ownership
- stores and schemas
- data flows
- classifications
- retention rules
- replication and consistency
- reporting and analytical consumers
- recovery objectives
