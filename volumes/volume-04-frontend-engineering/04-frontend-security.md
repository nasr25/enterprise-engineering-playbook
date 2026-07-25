# Frontend Security

## Purpose

Reduce browser-side attack surface while recognizing that the frontend is an untrusted execution environment.

## Mandatory Rules

- **FE-046** — The frontend must never be the sole enforcement point for authorization, entitlement, pricing, approval, or data access.
- **FE-047** — Untrusted content must be rendered through context-appropriate escaping or sanitization.
- **FE-048** — Raw HTML rendering is prohibited unless the content source, sanitizer, and allowed elements are explicitly controlled.
- **FE-049** — Authentication tokens must use the safest storage and transport model supported by the architecture; persistent browser storage requires explicit risk acceptance.
- **FE-050** — Secrets, private keys, service credentials, and privileged API keys must never be shipped to frontend bundles.
- **FE-051** — Content Security Policy must be defined for public and sensitive applications and should avoid unsafe inline execution.
- **FE-052** — Third-party scripts must be minimized, approved, version-controlled where possible, and reviewed for data collection and supply-chain risk.
- **FE-053** — External links opened in new browsing contexts must prevent opener abuse.
- **FE-054** — Redirect and return URLs must be validated against approved destinations.
- **FE-055** — CSRF protections must match the selected authentication model and must not be disabled for convenience.
- **FE-056** — Sensitive data must not appear in URLs, analytics payloads, client logs, browser storage, or error reports without approval.
- **FE-057** — Source maps in production must follow an explicit access and exposure decision.
- **FE-058** — Dependency integrity, vulnerability scanning, lockfiles, and controlled upgrades are mandatory.
- **FE-059** — Security headers and browser policies must be verified in the deployed environment, not only local development.
- **FE-060** — Logout must clear relevant client state, cached sensitive data, and cross-tab session artifacts.

## Security Review Evidence

- Threat model
- CSP and security-header verification
- Token lifecycle design
- Third-party script inventory
- Dependency scan results