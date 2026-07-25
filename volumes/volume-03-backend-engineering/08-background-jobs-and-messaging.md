# Background Jobs and Messaging

## Purpose

Define reliable asynchronous processing with explicit delivery, retry, ordering, ownership, and recovery behavior.

## Mandatory Rules

- **BE-099** — Work must be moved to asynchronous processing only when latency, resilience, throughput, scheduling, or decoupling requirements justify it.
- **BE-100** — Every job or message must have a stable type, schema version, producer, consumer, ownership, and retention policy.
- **BE-101** — Consumers must be idempotent or must use a documented deduplication mechanism.
- **BE-102** — Retry policy must distinguish transient from permanent failure and must use bounded attempts, delay, and jitter.
- **BE-103** — Poison messages and exhausted jobs must move to a controlled failure state such as a dead-letter queue with alerting and investigation ownership.
- **BE-104** — Message acknowledgement must occur only after the required durable processing outcome is achieved.
- **BE-105** — Message handlers must validate schema, authorization context, tenant context, and business preconditions before mutation.
- **BE-106** — Ordering assumptions must be explicit and limited to the smallest required partition or key.
- **BE-107** — Handlers must tolerate duplicate, delayed, reordered, and replayed delivery where the transport permits it.
- **BE-108** — Scheduled jobs must prevent unsafe overlap through locking, partitioning, idempotency, or equivalent controls.
- **BE-109** — Long-running jobs must expose progress, heartbeat, timeout, cancellation, and resumability where business impact requires them.
- **BE-110** — Queue depth, processing latency, age of oldest item, retry rate, failure rate, and dead-letter volume must be observable.
- **BE-111** — Producers must apply backpressure or admission control when downstream processing cannot keep pace.
- **BE-112** — Transactional state changes and event publication must use an outbox or equivalent atomic publication pattern when loss would violate business correctness.
- **BE-113** — Replay operations must be authorized, scoped, rate-controlled, audited, and protected from duplicate side effects.
- **BE-114** — Message contracts must evolve compatibly and consumers must tolerate supported producer versions.
- **BE-115** — Personally identifiable or sensitive data in messages must be minimized, classified, encrypted where required, and governed by retention policy.
- **BE-116** — Operational tools for inspecting queues or jobs must enforce least privilege and must not allow uncontrolled payload modification.

## Required Evidence

- Job and message catalog
- Retry and dead-letter policy
- Idempotency design
- Replay runbook
- Queue dashboard and alerts