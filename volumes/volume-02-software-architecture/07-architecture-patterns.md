# Architecture Patterns

## Purpose

Architecture patterns are reusable structures, not default answers. Teams must select them based on business capabilities, quality attributes, operational constraints, and delivery maturity.

## Rules

### ARC-065 — Pattern selection must be explicit
Every major structural pattern must be named, justified, and linked to the quality attributes it supports.

### ARC-066 — Prefer the simplest viable structure
A modular monolith should be preferred when it satisfies scale, deployment, ownership, and reliability needs.

### ARC-067 — Layered architecture must preserve direction
Presentation, application, domain, and infrastructure dependencies must flow inward toward stable business abstractions.

### ARC-068 — Clean or hexagonal boundaries must be enforceable
Ports and adapters must be represented in code, tests, and dependency rules rather than diagrams alone.

### ARC-069 — Domain boundaries must reflect business language
Bounded contexts must be derived from distinct models, policies, ownership, and change cadence.

### ARC-070 — Microservices require independent ownership
A service must have an accountable team, independent lifecycle, observable behavior, and an owned data boundary.

### ARC-071 — Event-driven architecture requires event ownership
Each event must have a producer, schema owner, compatibility policy, retention policy, and documented consumer expectations.

### ARC-072 — CQRS must solve a measured problem
CQRS may be used when read and write models have materially different consistency, scale, or complexity requirements.

### ARC-073 — Event sourcing requires reconstruction guarantees
Event-sourced systems must define replay, versioning, correction, snapshotting, retention, and privacy handling.

### ARC-074 — Workflow orchestration must expose state
Long-running workflows must make current state, transitions, retries, compensation, and operator intervention visible.

### ARC-075 — Choreography must limit hidden coupling
Event choreography must be bounded; business-critical flows with many participants should use explicit coordination or workflow visibility.

### ARC-076 — Pattern combinations must be reviewed
Combining microservices, CQRS, event sourcing, and asynchronous messaging requires an architecture review because complexity compounds.

## Selection Record

A pattern decision should include:

- problem and context
- quality attributes
- alternatives considered
- operational impact
- data ownership impact
- migration and rollback strategy
- expected failure modes
- decision expiry or review date
