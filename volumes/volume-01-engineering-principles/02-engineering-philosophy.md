# Engineering Philosophy

## Purpose

This chapter defines how engineering decisions are made when priorities compete. It applies to product teams, platform teams, vendors, contractors, reviewers, architects, operators, and AI coding agents.

## Decision Order

When two valid options conflict, decisions **MUST** be evaluated in this order:

1. Safety, security, privacy, and legal obligations
2. Correctness and data integrity
3. Availability, recoverability, and operational resilience
4. Maintainability, testability, and clarity
5. Interoperability and controlled change
6. Performance and scalability
7. Delivery speed and implementation convenience

A lower-priority goal **MUST NOT** override a higher-priority obligation without an approved exception.

## Core Principles

### ENG-009 — Evidence-Based Decisions

Material architecture and engineering decisions **MUST** be supported by measurable requirements, documented constraints, test results, incident history, capacity data, or an explicit risk assessment.

### ENG-010 — Prefer Simplicity

Teams **SHOULD** choose the simplest design that satisfies known functional, security, reliability, and scalability requirements. Simplicity does not permit omission of mandatory controls.

### ENG-011 — Design for Change

Systems **MUST** isolate volatile business rules, external integrations, infrastructure dependencies, and vendor-specific behavior behind stable interfaces.

### ENG-012 — Automate Repeated Controls

Repeatable checks such as formatting, testing, dependency scanning, secret detection, schema validation, and release verification **SHOULD** be automated and executed consistently.

### ENG-013 — Fail Safely

Failures **MUST** preserve confidentiality, integrity, and authorization boundaries. Error handling must not expose secrets, bypass controls, silently corrupt data, or report success before durable completion.

### ENG-014 — Operability Is a Feature

Every production service **MUST** provide sufficient health signals, logs, metrics, tracing where appropriate, runbooks, ownership information, and recovery procedures.

### ENG-015 — Reversible Change

High-risk changes **SHOULD** support rollback, feature disablement, backward compatibility, or another tested recovery path.

## Decision Questions

Before approving a design, reviewers should be able to answer:

- What business outcome does this design support?
- What data and trust boundaries are involved?
- What happens when dependencies are slow, unavailable, or compromised?
- How is authorization enforced and audited?
- How is the change tested, deployed, monitored, and reversed?
- What assumptions may become invalid as usage grows?
- Which parts create vendor, platform, or technology lock-in?

## Prohibited Decision Patterns

- Selecting technology solely because it is fashionable
- Optimizing only for initial implementation speed
- Treating security review as a final deployment step
- Introducing distributed components without a demonstrated need
- Accepting undocumented manual production procedures
- Using AI-generated claims as evidence without independent verification
