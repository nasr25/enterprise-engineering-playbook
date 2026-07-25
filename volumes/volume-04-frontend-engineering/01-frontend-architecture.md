# Frontend Architecture

## Purpose

Structure frontend code around clear ownership, predictable dependencies, and independently testable behavior.

## Mandatory Rules

- **FE-001** — Frontend applications must define explicit boundaries between presentation, application behavior, domain logic, data access, and platform integration.
- **FE-002** — Business rules shared with or authoritative in the backend must not be reimplemented as independent client truth.
- **FE-003** — Feature-oriented modules are preferred over directories grouped only by technical file type.
- **FE-004** — Shared components must have documented purpose, supported variants, accessibility behavior, and ownership.
- **FE-005** — Feature modules must not import private internals from unrelated features.
- **FE-006** — Dependency direction must be explicit and cyclic dependencies are prohibited.
- **FE-007** — Framework-specific code should be isolated from domain and application logic where practical.
- **FE-008** — Routes must define ownership, authorization expectations, loading behavior, error behavior, and deep-link support.
- **FE-009** — Large applications must use lazy loading or equivalent code splitting aligned with user journeys.
- **FE-010** — Global mutable state must be minimized and justified.
- **FE-011** — Environment-specific behavior must be configuration-driven and must not require source edits.
- **FE-012** — Generated code, vendored code, and application-owned code must be clearly separated.
- **FE-013** — Design-system primitives must not embed feature-specific business behavior.
- **FE-014** — Architectural exceptions must record rationale, owner, risk, and planned resolution.
- **FE-015** — Major frontend architecture changes must include migration and rollback strategy.

## Required Evidence

- Module and dependency map
- Route inventory
- Shared-component ownership
- State ownership model
- Build and deployment boundaries