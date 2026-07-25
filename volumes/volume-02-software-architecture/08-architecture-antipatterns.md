# Architecture Anti-Patterns

## Purpose

This chapter identifies structures that create hidden coupling, fragile delivery, unclear ownership, or excessive operational cost.

## Rules

### ARC-077 — Distributed monoliths are prohibited
Separately deployed components must not require coordinated release, shared database mutation, or synchronous availability to behave correctly.

### ARC-078 — Shared databases require exceptional approval
Independent services must not write to the same schema or tables. Temporary exceptions require ownership, access boundaries, and a removal plan.

### ARC-079 — Cyclic dependencies must be removed
Cycles between modules, services, packages, or deployment units must be detected and treated as structural defects.

### ARC-080 — The database must not become the integration bus
Polling shared tables, triggers across domains, and undocumented stored-procedure coupling are prohibited as primary integration mechanisms.

### ARC-081 — Generic service layers must not absorb domain logic
Business rules must remain close to the domain model or capability that owns them.

### ARC-082 — God services and god modules must be decomposed
Components that own unrelated capabilities, excessive dependencies, or broad data access must be split by business responsibility.

### ARC-083 — Chatty remote interfaces must be redesigned
Remote APIs must not expose fine-grained interactions that require many calls to complete one business operation.

### ARC-084 — Synchronous chains must be bounded
Critical request paths must not depend on long, serial chains of remote calls without explicit latency and failure budgets.

### ARC-085 — Framework leakage must be contained
Business logic must not depend directly on transport, persistence, UI, or vendor-specific framework details.

### ARC-086 — Premature distribution is prohibited
A system must not be decomposed into distributed services solely for perceived modernity, team preference, or hypothetical scale.

### ARC-087 — Permanent transitional architecture is prohibited
Temporary bridges, duplicate writes, compatibility layers, and migration paths must have owners and removal dates.

### ARC-088 — Architecture by convention alone is insufficient
Critical boundaries must be validated with automated dependency tests, contract tests, policy checks, or deployment controls.

## Detection Signals

- every change touches many repositories
- releases require synchronized deployment
- one database outage disables all capabilities
- ownership cannot be mapped to components
- integration behavior is undocumented
- incident isolation is difficult
- local development requires the entire estate
