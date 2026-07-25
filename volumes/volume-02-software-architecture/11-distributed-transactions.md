# Distributed Transactions and Consistency

## Purpose

Distributed systems cannot rely on a single local transaction across independently owned components. Business workflows must define consistency, failure handling, compensation, and reconciliation explicitly.

## Rules

### ARC-115 — Avoid cross-service ACID transactions
Independent services must not depend on a shared distributed transaction coordinator unless formally approved for a constrained platform case.

### ARC-116 — Consistency requirements must be classified
Each workflow must state which invariants require immediate consistency and which may use eventual consistency.

### ARC-117 — Local transactions must protect owned state
A service must atomically persist its own state changes and any durable record needed to publish resulting integration messages.

### ARC-118 — Transactional outbox is the default publication pattern
When a database change must emit an event or command, use an outbox or equivalent atomic publication mechanism.

### ARC-119 — Consumers must be idempotent
Message handlers must tolerate duplicate delivery through stable identifiers, deduplication, or naturally idempotent state transitions.

### ARC-120 — Sagas must define compensation
Multi-step business transactions must document participants, state transitions, timeouts, retries, compensation, and irreversible steps.

### ARC-121 — Compensation is a business operation
Compensating actions must be defined and approved by domain owners; they are not assumed to be technical rollback.

### ARC-122 — Ordering assumptions must be bounded
Systems must not depend on global message ordering. Required ordering must be scoped to a documented key or stream.

### ARC-123 — Delivery semantics must be declared
Publishers and consumers must state whether processing is at-most-once, at-least-once, or effectively-once and explain the controls used.

### ARC-124 — Poison messages must be isolated
Repeatedly failing messages must move to a controlled dead-letter or quarantine path with alerting, inspection, replay, and audit procedures.

### ARC-125 — Reconciliation is mandatory
Critical eventually consistent workflows require periodic detection and repair of missing, duplicated, or contradictory state.

### ARC-126 — Operators must see workflow state
Long-running or distributed transactions must expose status, failure reason, next action, and safe intervention capabilities.

## Required Workflow Evidence

- business invariants
- consistency model
- message identifiers
- retry and timeout policy
- compensation steps
- dead-letter handling
- reconciliation method
- observability and operator actions
