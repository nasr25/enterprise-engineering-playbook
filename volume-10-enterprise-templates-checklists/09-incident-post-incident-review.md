# Incident & Post-Incident Review — Template

## Incident Summary
- Incident ID:
- Service:
- Severity:
- Start time:
- Detection time:
- Mitigation time:
- Recovery time:
- Incident commander:
- Customer / business impact:

## Timeline
| Time | Event / Observation / Action | Actor | Evidence |
|---|---|---|---|

## Detection
- How was the incident detected?
- Did monitoring detect it before users?
- Which signals were useful or missing?

## Response
- What stopped or reduced impact?
- Which runbooks were used?
- What slowed diagnosis or mitigation?
- Were communications timely and accurate?

## Root Cause and Contributing Factors
Describe technical and organizational contributors using evidence. Avoid attributing the incident to a person when system conditions enabled the failure.

## Control Analysis
- Why did prevention controls not stop it?
- Why did detection controls not detect it earlier?
- Why did recovery controls not restore faster?

## Corrective Actions
| Action | Type: Prevent/Detect/Recover | Priority | Owner | Due Date | Verification |
|---|---|---|---|---|---|

## Reliability Follow-Up
- SLO / error-budget impact:
- Capacity implications:
- Architecture changes:
- Test additions:
- Runbook changes:
- Monitoring changes:

## Lessons
Record reusable engineering lessons and update the playbook or project standards when appropriate.
