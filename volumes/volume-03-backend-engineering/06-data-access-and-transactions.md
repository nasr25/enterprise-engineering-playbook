# Data Access and Transactions

## Purpose

Protect data integrity, performance, isolation, and evolvability in backend persistence code.

## Mandatory Rules

- **BE-066** — Persistence concerns must be isolated from transport and presentation logic through explicit application or domain boundaries.
- **BE-067** — Data access must use parameterized commands or approved query builders; dynamic string construction with untrusted input is prohibited.
- **BE-068** — Queries must select only required fields and must avoid unbounded result sets.
- **BE-069** — Pagination must use stable ordering and a documented consistency model; cursor pagination is preferred for large changing datasets.
- **BE-070** — Repository abstractions must reflect meaningful aggregate or use-case boundaries and must not merely hide every database capability.
- **BE-071** — Transaction scope must be as small as practical while preserving the required business invariant.
- **BE-072** — Network calls, user interaction, and long-running computation must not occur inside database transactions unless explicitly justified.
- **BE-073** — Isolation level must be selected according to identified anomalies and contention, not left to accidental defaults for critical workflows.
- **BE-074** — Concurrency conflicts must be detected and handled using optimistic or pessimistic controls appropriate to the use case.
- **BE-075** — Multi-record writes that implement one invariant must commit atomically when they share a transactional boundary.
- **BE-076** — Cross-boundary consistency must use an approved pattern such as outbox, saga, compensation, or reconciliation rather than hidden distributed transactions.
- **BE-077** — Database errors must be translated into stable domain or API outcomes without exposing schema or engine details.
- **BE-078** — Read replicas and caches must not be used for flows requiring read-your-write consistency unless the consistency gap is explicitly handled.
- **BE-079** — Migration code must be version-controlled, repeatable, observable, and compatible with the deployment and rollback strategy.
- **BE-080** — Destructive schema changes must use staged migration, verified data movement, and explicit recovery procedures.
- **BE-081** — Index changes must be justified by measured query patterns and evaluated for write, storage, and maintenance cost.
- **BE-082** — Bulk operations must be bounded, resumable where needed, and designed to avoid long locks or resource starvation.

## Review Evidence

- Query plans for critical paths
- Transaction-boundary diagram
- Concurrency test cases
- Migration and rollback plan
- Data-access performance measurements