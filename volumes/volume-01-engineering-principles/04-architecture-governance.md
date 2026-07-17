# Architecture Governance

## Purpose

Architecture governance ensures that material technical decisions are intentional, reviewable, secure, supportable, and aligned with enterprise constraints without creating unnecessary bureaucracy.

## Governance Scope

Architecture review **MUST** occur for changes that materially affect:

- Trust boundaries, identity, permissions, or sensitive data
- Public or partner-facing interfaces
- Database ownership, schema compatibility, or data movement
- Integration contracts and messaging semantics
- Availability, disaster recovery, or deployment topology
- Introduction of a new language, framework, platform, database, or managed service
- Significant recurring cost or vendor lock-in
- Cross-team shared components
- Removal or replacement of mandatory controls

Routine implementation choices within an approved architecture do not require a separate architecture decision.

## Required Architecture Evidence

Material designs **MUST** document, at minimum:

1. Problem and measurable requirements
2. Context, assumptions, and constraints
3. System context and major components
4. Data classifications and data flows
5. Trust boundaries and authorization enforcement points
6. Dependencies and failure modes
7. Availability, recovery, and capacity expectations
8. Deployment and operational ownership
9. Considered alternatives and trade-offs
10. Migration, compatibility, and rollback strategy

## Governance Roles

- **Decision owner:** accountable for the business and technical outcome.
- **Author:** prepares the design and evidence.
- **Reviewers:** assess security, data, operations, architecture, and delivery concerns.
- **Approver:** accepts the decision within the organization's authority model.
- **Implementers:** ensure the approved decision is reflected in code and configuration.

One person may perform multiple roles in small teams, but high-risk decisions **SHOULD** receive independent review.

## Governance Rules

### ENG-016 — Architecture Before Irreversible Commitment

Material architecture decisions **MUST** be reviewed before contracts, schemas, interfaces, or production dependencies make the decision expensive to reverse.

### ENG-017 — Explicit Ownership

Every production system and shared component **MUST** have an accountable owner and a documented support path.

### ENG-018 — Technology Introduction Control

New technologies **MUST** be evaluated for security support, maintainability, licensing, operational skills, lifecycle, interoperability, deployment constraints, and exit strategy.

### ENG-019 — Contract Compatibility

Changes to shared APIs, events, schemas, or integrations **MUST** include compatibility and consumer-impact analysis.

### ENG-020 — Architecture Conformance

Implementation **MUST** remain consistent with approved architecture. Material divergence requires updating the design record before release.

## Review Outcomes

An architecture review results in one of:

- Approved
- Approved with tracked conditions
- Revision required
- Rejected with rationale
- Exception required

Conditions **MUST** have an owner and completion criterion. Approval does not transfer implementation accountability from the delivery team.

## Lightweight Governance

Governance should be proportional to risk. A concise ADR may be sufficient for a reversible internal decision, while a sensitive enterprise integration may require diagrams, threat modeling, data review, recovery analysis, and formal approval.
