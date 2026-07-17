# Compliance Evidence and Traceability

## Purpose

Engineering controls must produce reliable evidence that requirements were understood, implemented, tested, approved, and operated as intended.

## Rules

### ENG-060 — Requirement Traceability

Material business, security, privacy, regulatory, and operational requirements **MUST** be traceable to implementation artifacts and verification evidence.

### ENG-061 — Evidence by Design

Controls **MUST** define the evidence they produce, its owner, retention period, integrity requirements, and review method before production use.

### ENG-062 — Reproducible Verification

Compliance claims **MUST** be supported by reproducible evidence such as automated test results, scan reports, approvals, configuration snapshots, audit records, or recovery exercises.

### ENG-063 — Evidence Integrity

Compliance evidence **MUST** be protected from unauthorized alteration and must retain source, timestamp, scope, environment, and execution identity where applicable.

### ENG-064 — Control Ownership

Every mandatory engineering control **MUST** have an accountable control owner and a defined escalation path for failure or noncompliance.

### ENG-065 — No Checklist-Only Compliance

A completed checklist **MUST NOT** be treated as sufficient evidence when the control requires technical verification, operational testing, or independent review.

### ENG-066 — Retention Alignment

Evidence retention **MUST** align with legal, regulatory, contractual, security, incident-response, and organizational record-management obligations.

## Minimum Traceability Chain

A traceability chain should connect:

1. Requirement or control
2. Design decision or threat scenario
3. Implementation artifact
4. Test or verification method
5. Result and reviewer
6. Exception or remediation item, if any
7. Release or operational evidence

## Evidence Examples

- Pull request approvals and signed commits
- CI/CD results and deployment records
- SAST, DAST, SCA, secret, and infrastructure scan results
- Access reviews and authorization tests
- Database migration and rollback evidence
- Backup restoration and disaster-recovery exercise results
- Change records, ADRs, risk acceptances, and exception approvals

## Prohibited Practices

- Backdating evidence
- Reusing evidence from a materially different release or environment
- Claiming compliance based on undocumented verbal confirmation
- Deleting failed results to present only successful outcomes