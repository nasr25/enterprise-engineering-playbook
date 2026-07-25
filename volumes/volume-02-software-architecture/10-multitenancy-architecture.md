# Multi-Tenancy Architecture

## Purpose

Multi-tenancy decisions affect security, isolation, cost, deployment, customization, observability, and recovery. The selected model must match the risk profile of the tenants and data.

## Rules

### ARC-103 — Tenant identity must be explicit
Tenant context must be established through trusted authentication and propagated through every request, job, event, cache key, and audit record.

### ARC-104 — Tenant isolation must be enforced server-side
Client-provided identifiers alone must never authorize access to tenant data.

### ARC-105 — The isolation model must be documented
The architecture must state whether tenancy uses shared tables, shared databases with separate schemas, separate databases, or separate deployments.

### ARC-106 — Isolation strength must follow risk
Highly regulated, sensitive, or high-impact tenants may require stronger data, encryption, network, or deployment isolation.

### ARC-107 — Every query must be tenant-safe
Shared-store access must use centralized tenant filters, database policies, scoped repositories, or equivalent controls with automated tests.

### ARC-108 — Cache and storage keys must include tenant context
Caches, object stores, search indexes, queues, and temporary files must prevent cross-tenant collisions and disclosure.

### ARC-109 — Background processing must preserve tenant context
Scheduled tasks, retries, batch jobs, and event handlers must execute under an explicit tenant identity.

### ARC-110 — Tenant-aware observability must protect confidentiality
Logs, metrics, traces, and alerts should support tenant diagnosis while preventing unauthorized visibility into other tenants.

### ARC-111 — Noisy-neighbor risk must be controlled
Quotas, rate limits, workload partitioning, concurrency controls, and capacity monitoring must prevent one tenant from degrading others.

### ARC-112 — Tenant customization must not fork the product
Configuration, feature flags, policy data, and extension points should be preferred over tenant-specific code branches.

### ARC-113 — Tenant lifecycle must be automated
Provisioning, configuration, suspension, export, archival, deletion, and cryptographic erasure must be controlled and auditable.

### ARC-114 — Recovery must respect tenant boundaries
Backup, restore, point-in-time recovery, and legal discovery must define whether recovery is platform-wide or tenant-specific.

## Required Evidence

- tenancy and isolation model
- threat analysis for cross-tenant access
- tenant-context propagation design
- automated isolation tests
- quota and capacity strategy
- onboarding and offboarding runbooks
- backup and recovery limitations
