# Exception Management

## Purpose

Exceptions provide a controlled, transparent mechanism for temporary or justified deviation from mandatory playbook requirements. An exception is not a permanent alternative standard.

## Exception Requirements

A request to deviate from a **MUST** or **MUST NOT** rule **MUST** include:

- Unique exception identifier
- Affected rule identifiers
- System, component, environment, and scope
- Business and technical justification
- Risk statement and affected assets
- Data classification and exposure, where relevant
- Alternatives considered
- Compensating controls
- Named risk owner
- Approver and approval date
- Start date and expiry or review date
- Remediation or exit plan
- Evidence required for closure

## Prohibited Exceptions

Exceptions **MUST NOT** be used to:

- Conceal schedule or budget pressure
- Avoid documenting known vulnerabilities
- Grant indefinite privileged access without review
- Bypass legal, regulatory, or contractual requirements
- Accept a risk on behalf of an unauthorized owner
- normalize a repeated deviation that should become a formally reviewed standard

## Exception Lifecycle

```text
Draft → Risk Review → Approved / Rejected → Active → Remediated / Expired / Revoked
```

Expired exceptions are non-compliant unless renewed before expiry through a new review.

## Governance Rules

### ENG-025 — Time-Bound Exceptions

Exceptions **MUST** have an expiry or mandatory review date. Open-ended exceptions are prohibited.

### ENG-026 — Compensating Controls

Approved exceptions **MUST** implement practical compensating controls that reduce likelihood, impact, exposure, or duration.

### ENG-027 — Risk Ownership

The person approving an exception **MUST** have authority to accept the stated business risk. Engineering teams cannot unilaterally accept enterprise risk.

### ENG-028 — Exception Traceability

Active exceptions **MUST** be linked to affected repositories, deployments, services, findings, and remediation work.

### ENG-029 — Recurring Exception Review

Repeated or widespread exceptions to the same rule **MUST** trigger review of the rule, technology baseline, funding, or delivery process.

## Minimum Exception Template

```markdown
# EXC-NNNN: Short Title

- Status:
- Requested by:
- Risk owner:
- Approver:
- Rules affected:
- Scope:
- Start date:
- Review/expiry date:

## Justification

## Risk

## Alternatives Considered

## Compensating Controls

## Remediation and Exit Plan

## Closure Evidence
```

## Closure Checklist

- The original deviation has been removed or formally replaced.
- Tests and scans confirm compliance.
- Temporary credentials, access, rules, and configurations are removed.
- Documentation and architecture records are updated.
- The risk owner confirms closure.
