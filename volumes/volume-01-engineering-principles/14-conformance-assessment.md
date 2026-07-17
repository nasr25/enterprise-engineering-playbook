# Conformance Assessment

## Purpose

Conformance assessment provides a consistent method to determine whether a system, change, or release satisfies the applicable playbook requirements.

## Assessment Levels

### Level 0 — Not Assessed

No reliable evidence exists, or the assessment scope is undefined.

### Level 1 — Partially Conformant

Some applicable requirements are met, but material gaps, missing evidence, or unmanaged exceptions remain.

### Level 2 — Conformant

All applicable mandatory requirements are met or covered by approved, time-bound exceptions with compensating controls.

### Level 3 — Verified and Continuously Controlled

Level 2 is achieved, and key controls are continuously or regularly verified through automated evidence, monitoring, testing, and governance review.

## Rules

### ENG-074 — Defined Assessment Scope

Every conformance assessment **MUST** define the system, release, environment, components, applicable volumes, exclusions, and assessment date.

### ENG-075 — Evidence-Based Result

A conformance rating **MUST** be based on current, attributable evidence and **MUST NOT** rely solely on self-declaration.

### ENG-076 — Applicability Decisions

Requirements marked not applicable **MUST** include a documented rationale and reviewer.

### ENG-077 — Gap Ownership

Every identified gap **MUST** have a severity, accountable owner, target treatment date, and remediation or exception reference.

### ENG-078 — Release Blocking

Unresolved critical nonconformance **MUST** block production release unless an authorized risk owner approves a documented exception with compensating controls.

### ENG-079 — Reassessment Triggers

Reassessment **MUST** occur after material changes to architecture, security boundaries, data classification, authentication, authorization, deployment topology, critical dependencies, or regulatory scope.

## Minimum Assessment Record

- Assessment identifier and date
- Assessor and accountable system owner
- Scope and applicable playbook version
- Requirement-by-requirement result
- Evidence references
- Findings and severity
- Approved exceptions
- Remediation actions and due dates
- Final conformance level and approval

## Result Values

Each applicable rule should be recorded as:

- Conformant
- Partially conformant
- Nonconformant
- Not applicable
- Not assessed

## Independence

High-risk systems and major releases should include review by someone independent of the primary implementer.