# Infrastructure as Code and Platform Engineering

## Mandatory Rules

- **DO-055** — Production infrastructure must be defined through version-controlled automation wherever the platform supports it.
- **DO-056** — Infrastructure definitions must be modular, reviewable, testable, and reusable without hiding critical security behavior.
- **DO-057** — Infrastructure changes must use plan, review, approval, apply, and verification stages.
- **DO-058** — Plans must be reviewed for destructive, replacement, privilege, network, persistence, and cost impact.
- **DO-059** — State files must be encrypted, access-controlled, backed up, and protected from concurrent corruption.
- **DO-060** — Secrets must not be embedded in infrastructure code or state where avoidable.
- **DO-061** — Manual infrastructure changes must be exceptional, logged, reconciled into code, and reviewed for drift.
- **DO-062** — Modules and providers must be pinned to reviewed versions and upgraded through controlled change.
- **DO-063** — Infrastructure code must enforce naming, tagging, ownership, environment, data classification, and lifecycle metadata.
- **DO-064** — Destructive operations must require explicit safeguards and independent approval for protected environments.
- **DO-065** — Platform services must publish supported capabilities, service levels, limits, ownership, and onboarding guidance.
- **DO-066** — Internal platforms must provide secure paved roads without preventing justified exceptions.
- **DO-067** — Platform APIs and templates must use secure defaults and least-privilege identities.
- **DO-068** — Platform changes must preserve backward compatibility or provide documented migration paths.
- **DO-069** — Golden images and base templates must be hardened, patched, scanned, versioned, and regularly rebuilt.
- **DO-070** — Infrastructure tests must cover syntax, policy, security, deployment feasibility, and critical runtime behavior.
- **DO-071** — Resource ownership and decommissioning criteria must be defined at creation time.
- **DO-072** — Infrastructure automation must support recovery from interrupted or partially applied changes.

## Evidence

- IaC repositories and plans
- State protection configuration
- Drift reports
- Platform service catalog
- Golden-image lifecycle records