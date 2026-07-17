# Volume 01 — Engineering Principles

## Purpose

This volume defines the mandatory engineering principles and governance controls that apply to every current and future software project, regardless of technology, deployment model, team, vendor, or use of AI-assisted development.

## Scope

This volume applies to:

- New systems and major enhancements
- Existing systems undergoing maintenance
- Internal and public-facing applications
- Web, mobile, backend, API, integration, and data workloads
- On-premises, cloud, and hybrid deployments
- Human-written and AI-generated code

## Foundational Priorities

Engineering decisions should prioritize:

1. Security and privacy
2. Correctness and data integrity
3. Reliability and recoverability
4. Maintainability and testability
5. Observability and operability
6. Scalability and performance
7. Developer experience and delivery speed

Delivery speed must not be achieved by bypassing mandatory security, authorization, validation, testing, or audit controls.

## Chapters

1. [Vision and Objectives](01-vision-and-objectives.md)
2. [Engineering Philosophy](02-engineering-philosophy.md)
3. [Rule Classification and Identifiers](03-rule-classification.md)
4. [Architecture Governance](04-architecture-governance.md)
5. [Architecture Decision Records](05-architecture-decision-records.md)
6. [Exception Management](06-exception-management.md)
7. [AI-Assisted Engineering Contract](07-ai-engineering-contract.md)
8. [Enterprise Definition of Done](08-definition-of-done.md)

## Foundational Rule Set

### ENG-001 — Security by Design

Security requirements **MUST** be considered during analysis and design, not added only after implementation.

### ENG-002 — Least Privilege

Users, services, applications, databases, automation accounts, and infrastructure components **MUST** receive only the permissions required for their approved functions.

### ENG-003 — Deny by Default

Access control decisions **MUST** deny access when authorization information is absent, invalid, ambiguous, expired, or unavailable.

### ENG-004 — Separation of Concerns

Presentation, application logic, domain logic, persistence, and infrastructure concerns **MUST** remain appropriately separated.

### ENG-005 — No Hardcoded Security Decisions

Applications **MUST NOT** hardcode role names, user identifiers, secrets, tokens, credentials, environment URLs, or security exceptions in business logic.

Authorization decisions must rely on centrally managed permissions, policies, attributes, or equivalent authorization controls.

### ENG-006 — Impact Analysis

Changes affecting architecture, interfaces, schemas, security controls, permissions, integrations, or compatibility **MUST** include documented impact analysis before implementation.

### ENG-007 — Controlled Exceptions

Exceptions to mandatory rules **MUST** be documented, risk-assessed, approved, time-bound where appropriate, and protected by compensating controls.

### ENG-008 — AI-Generated Code Is Not Exempt

AI-generated or AI-modified code **MUST** undergo the same review, testing, security, documentation, and approval requirements as human-written code.

## Next Development Areas

The next increment will expand this volume with documentation standards, technical debt governance, configuration principles, compliance evidence, review cadence, and reusable governance templates.
