# Architecture Principles

## Objective

Establish a consistent decision framework for selecting structures, technologies, deployment models, and integration patterns.

## Mandatory Rules

### ARC-001 — Requirements Drive Architecture

Architecture **MUST** be derived from documented functional requirements, quality attributes, constraints, data sensitivity, operational needs, and expected change.

### ARC-002 — Explicit Quality Attributes

Security, availability, recoverability, performance, scalability, maintainability, interoperability, accessibility, and observability requirements **MUST** be measurable where material.

### ARC-003 — Simplest Adequate Architecture

Teams **MUST** select the simplest architecture that satisfies validated requirements and foreseeable change. Complexity requires documented justification.

### ARC-004 — Technology Neutral Evaluation

Technology selection **MUST** consider fitness, lifecycle, supportability, security posture, operational capability, portability, cost, and vendor dependency rather than popularity alone.

### ARC-005 — Secure and Private by Design

Trust boundaries, identities, permissions, secrets, sensitive data flows, abuse cases, and security controls **MUST** be addressed during architecture design.

### ARC-006 — Operability by Design

Systems **MUST** be designed for deployment, monitoring, troubleshooting, rollback, backup, restoration, capacity management, and incident response.

### ARC-007 — Evolutionary Change

Architecture **MUST** enable controlled incremental change and avoid unnecessary irreversible decisions.

### ARC-008 — Explicit Trade-offs

Material architectural decisions **MUST** document benefits, costs, risks, alternatives, assumptions, and consequences through an ADR or equivalent approved record.

### ARC-009 — No Architecture by Accident

Framework defaults, generated code, AI recommendations, vendor templates, or inherited implementations **MUST NOT** become architectural policy without evaluation.

### ARC-010 — Validate Critical Assumptions

High-risk assumptions **MUST** be validated using prototypes, benchmarks, threat models, failure tests, or other appropriate evidence before commitment.

## Decision Priorities

When requirements conflict, decisions should prioritize:

1. Safety, security, privacy, and legal obligations
2. Data integrity and correctness
3. Availability and recoverability
4. Maintainability and operational control
5. Performance and scalability
6. Delivery speed and convenience

A lower priority may override a higher priority only through an explicit, approved risk decision.