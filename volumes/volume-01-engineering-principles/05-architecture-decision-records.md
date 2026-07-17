# Architecture Decision Records

## Purpose

Architecture Decision Records (ADRs) preserve the context, alternatives, trade-offs, and consequences of significant technical decisions.

## When an ADR Is Required

An ADR **MUST** be created when a decision:

- Introduces or replaces a major technology or platform
- Establishes a cross-project pattern or shared contract
- Changes trust boundaries, identity, authorization, or encryption
- Selects a database, messaging model, integration protocol, or deployment topology
- Accepts a significant security, availability, cost, or vendor risk
- Creates a difficult-to-reverse constraint
- Overrides or interprets a playbook rule

## ADR Lifecycle

Allowed statuses:

- Proposed
- Accepted
- Superseded
- Deprecated
- Rejected

Accepted ADRs are immutable historical records. Corrections that change the decision **MUST** be recorded in a new ADR that supersedes the previous one.

## Naming Convention

```text
adr/NNNN-short-decision-title.md
```

Example:

```text
adr/0007-use-openid-connect-for-workforce-sso.md
```

Numbers are sequential and are never reused.

## Required Structure

```markdown
# ADR-NNNN: Decision Title

- Status:
- Date:
- Owners:
- Related rules:

## Context

## Decision Drivers

## Considered Options

## Decision

## Security and Privacy Impact

## Operational Impact

## Consequences

## Migration and Rollback

## Validation

## Follow-up Actions
```

## ADR Quality Rules

### ENG-021 — Record Context, Not Only Outcome

An ADR **MUST** explain why the decision was needed, which constraints existed, and which alternatives were considered.

### ENG-022 — State Consequences Honestly

An ADR **MUST** document known positive and negative consequences, including operational burden, cost, lock-in, migration complexity, and residual risk.

### ENG-023 — Link Implementation

Relevant pull requests, diagrams, threat models, tickets, runbooks, and contracts **SHOULD** link to the governing ADR.

### ENG-024 — Validate Assumptions

Important assumptions in an ADR **MUST** be testable or assigned for later validation. Invalidated assumptions require review of the decision.

## Decision Quality Checklist

- Is the problem clearly defined?
- Are measurable drivers listed?
- Were credible alternatives considered?
- Are security and privacy effects explicit?
- Are failure and recovery implications understood?
- Is the decision compatible with enterprise constraints?
- Is there a migration or rollback path?
- Are owners and follow-up actions named?
