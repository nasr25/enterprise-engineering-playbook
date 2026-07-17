# Contributing

## Change Process

All substantive changes must be submitted through a pull request.

1. Create a focused branch.
2. Identify affected volumes and rule IDs.
3. Add or update content using the rule template.
4. Check for conflicts, duplication, and broken links.
5. Update the changelog when the change affects published guidance.
6. Request review from the appropriate owner.

## Normative Language

Use these terms consistently:

- **MUST / SHALL / REQUIRED**: mandatory requirement.
- **MUST NOT / SHALL NOT / PROHIBITED**: mandatory prohibition.
- **SHOULD / RECOMMENDED**: expected unless a justified exception exists.
- **SHOULD NOT / DISCOURAGED**: normally avoided unless justified.
- **MAY / OPTIONAL**: permitted but not required.

## Rule Identifiers

Each enforceable rule must have a stable identifier using its domain prefix, for example:

- `ENG-001` Engineering principles
- `ARCH-001` Architecture
- `BE-001` Backend
- `FE-001` Frontend
- `MOB-001` Mobile
- `DB-001` Database
- `API-001` APIs
- `IAM-001` Identity and access management
- `SEC-001` Cybersecurity
- `PERF-001` Performance
- `DEVSECOPS-001` DevSecOps
- `TEST-001` Testing
- `AI-001` AI-assisted engineering
- `OPS-001` Operations
- `GOV-001` Governance

Rule IDs must not be reused after deletion. Deprecated rules should remain documented with their replacement when applicable.

## Exceptions

Any exception to a mandatory rule must document:

- Rule ID
- Business and technical justification
- Risk assessment
- Compensating controls
- Approver
- Expiration or review date
