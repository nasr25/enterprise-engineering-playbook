# System Boundaries and Decomposition

## Objective

Define systems and components around clear responsibilities, ownership, data authority, security boundaries, and change patterns.

## Mandatory Rules

### ARC-011 — Explicit System Context

Every material system **MUST** document its users, external systems, trust boundaries, primary responsibilities, data classifications, and business ownership.

### ARC-012 — Cohesive Responsibilities

A component or service **MUST** group behavior and data that change for related business reasons. Unrelated capabilities must not be combined solely for implementation convenience.

### ARC-013 — Controlled Coupling

Components **MUST** interact through explicit contracts and **MUST NOT** depend on another component's private implementation details.

### ARC-014 — Data Ownership

Each authoritative data set **MUST** have a clearly identified owning system or bounded context responsible for its integrity, lifecycle, and access policy.

### ARC-015 — No Shared-Database Integration by Default

Independent systems or services **MUST NOT** integrate by directly reading or modifying each other's private database tables unless an approved exception documents ownership, compatibility, security, and migration controls.

### ARC-016 — Boundary-Based Authorization

Authorization **MUST** be enforced at every boundary where an operation or data resource can be accessed. Client-side checks are not authorization controls.

### ARC-017 — Modular Monolith Before Distributed Complexity

Teams **SHOULD** prefer a well-structured modular monolith when independent deployment, scaling, isolation, or ownership does not justify distributed services.

### ARC-018 — Service Extraction Criteria

A service boundary **MUST** be justified by measurable needs such as independent lifecycle, distinct ownership, scaling profile, security isolation, regulatory separation, or reliability requirements.

### ARC-019 — No Circular Dependencies

Logical modules, deployable components, and services **MUST NOT** form circular dependencies. Cycles must be removed through boundary redesign, contract extraction, or orchestration.

### ARC-020 — Public and Private Contracts

Every component **MUST** distinguish supported public contracts from internal implementation details. Consumers may depend only on documented public contracts.

## Decomposition Evidence

Architecture documentation should include:

- System context
- Container or deployable-unit view
- Component responsibilities
- Data ownership map
- Trust boundaries
- Integration contracts
- Dependency direction
- Ownership and support model