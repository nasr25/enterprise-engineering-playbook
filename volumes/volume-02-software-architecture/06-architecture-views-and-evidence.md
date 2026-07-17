# Architecture Views and Evidence

## Objective

Define the minimum architecture evidence required to communicate, review, operate, and evolve a system.

## Mandatory Rules

### ARC-055 — Audience-Appropriate Views

Architecture documentation **MUST** provide views appropriate to business owners, engineers, security reviewers, data owners, operations teams, and support teams.

### ARC-056 — Current-State Accuracy

Architecture diagrams and inventories **MUST** reflect the deployed or approved target state and include an owner and last-reviewed date.

### ARC-057 — System Context View

Every material system **MUST** maintain a context view showing users, external systems, ownership, business purpose, and trust boundaries.

### ARC-058 — Deployment View

Systems **MUST** document deployable units, environments, network zones, ingress and egress paths, data stores, shared services, and high-availability arrangements.

### ARC-059 — Data Flow View

Sensitive or regulated workflows **MUST** document data sources, destinations, classifications, transformations, persistence, encryption boundaries, and retention.

### ARC-060 — Runtime Interaction View

Critical workflows **MUST** document runtime interactions, including sequence, authorization points, timeouts, retries, asynchronous behavior, and failure outcomes.

### ARC-061 — Threat and Trust View

Systems **MUST** document trust boundaries, identities, privileged paths, exposed interfaces, major threats, and key mitigating controls.

### ARC-062 — Ownership View

Components, services, data domains, integrations, and operational controls **MUST** have identifiable business and technical owners.

### ARC-063 — Traceability

Material architecture elements **MUST** be traceable to requirements, ADRs, risks, controls, tests, and operational evidence.

### ARC-064 — Architecture Drift Detection

Teams **MUST** periodically compare approved architecture with deployed reality and record material drift as remediation work, technical debt, or an approved new decision.

## Minimum Architecture Pack

A production system should maintain:

- System context diagram
- Container or deployable-unit diagram
- Component or module view where complexity warrants it
- Deployment and network view
- Data-flow and classification view
- Critical sequence diagrams
- Integration inventory
- Dependency inventory
- ADR index
- Threat model
- Availability and recovery design
- Ownership and support matrix
- Open risks, exceptions, and technical debt

## Diagram Standards

Diagrams should:

- Use consistent notation and legends
- Identify system and trust boundaries
- Avoid ambiguous arrows
- Name protocols and interaction styles
- Distinguish current and target states
- Be stored in a version-controlled, reproducible format where practical
- Link to supporting records rather than duplicating volatile detail