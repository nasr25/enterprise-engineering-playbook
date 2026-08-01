# Platform and Software Supply Chain Security

## Mandatory Rules

- **DO-109** — Software and infrastructure dependencies must come from approved, authenticated, and integrity-verified sources.
- **DO-110** — Dependency versions must be pinned or constrained through reviewed lock files and update policies.
- **DO-111** — Every release must produce or reference an SBOM appropriate to the artifact and deployment model.
- **DO-112** — Build provenance must identify source, builder, workflow, dependencies, and artifact digest.
- **DO-113** — Release artifacts and container images must be signed where platform capability and risk justify it.
- **DO-114** — Deployment systems must verify artifact integrity and provenance before promotion.
- **DO-115** — SAST, dependency, secret, IaC, and container scans must run at defined pipeline stages.
- **DO-116** — DAST or equivalent runtime security testing must be applied to exposed applications according to risk.
- **DO-117** — Critical and high-risk findings must block release unless formally accepted with expiry and remediation ownership.
- **DO-118** — Scan suppressions must be specific, justified, approved, time-bound, and periodically reviewed.
- **DO-119** — Build and deployment identities must be separated and restricted to required repositories, artifacts, and environments.
- **DO-120** — Third-party pipeline actions, plugins, images, and scripts must be pinned, reviewed, and monitored for compromise.
- **DO-121** — Untrusted pull-request code must not receive production secrets or privileged runner access.
- **DO-122** — Self-hosted runners must be isolated by trust level and cleaned between workloads where reuse creates risk.
- **DO-123** — Security policies must be automated as code where reliable enforcement is possible.
- **DO-124** — Base images, toolchains, and platform components must follow vulnerability and patch-management SLAs.
- **DO-125** — Compromised credentials, dependencies, artifacts, or build systems must trigger revocation, impact analysis, and rebuild from trusted sources.
- **DO-126** — Supply-chain incidents must support identification of affected builds, releases, environments, and consumers.

## Evidence

- SBOM and provenance records
- Scan results and exceptions
- Artifact signatures
- Runner trust design
- Dependency and patch inventory