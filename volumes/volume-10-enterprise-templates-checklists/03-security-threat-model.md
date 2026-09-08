# Security Threat Model — Template

## System Context
- System / feature:
- Owner:
- Critical assets:
- Sensitive data:
- Trust boundaries:
- External actors and systems:

## Architecture Evidence
Attach or link data-flow and deployment diagrams showing clients, APIs, databases, queues, storage, identity systems, external integrations, administrative paths, and trust boundaries.

## Entry Points
| Entry Point | Actor | Authentication | Authorization | Data Classification |
|---|---|---|---|---|

## Threat Review
Evaluate at minimum:
- Spoofing / identity abuse
- Authorization bypass / privilege escalation
- Injection and unsafe deserialization
- Data disclosure and exfiltration
- Tampering and integrity loss
- Repudiation / insufficient auditability
- Denial of service / resource exhaustion
- SSRF and unsafe outbound connectivity
- File upload / parser risks
- Secrets and key compromise
- Supply-chain compromise
- Cross-tenant leakage
- Administrative interface abuse
- Business-logic abuse

## Threat Register
| ID | Threat | Asset | Likelihood | Impact | Existing Control | Required Treatment | Owner | Status |
|---|---|---|---|---|---|---|---|---|

## Security Verification
- [ ] Authentication tests
- [ ] Authorization / object-level authorization tests
- [ ] Input validation tests
- [ ] SAST / dependency / secret scanning
- [ ] DAST or equivalent runtime testing where applicable
- [ ] Security headers / TLS validation
- [ ] Rate and abuse controls
- [ ] Audit logging validation
- [ ] Backup / recovery security
- [ ] Penetration testing when risk requires it

## Residual Risk Acceptance
Document remaining risks, accountable approver, compensating controls, and expiry/review date.
