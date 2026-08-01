# Containers, Kubernetes, and Network Entry

## Mandatory Rules

- **DO-073** — Container images must use minimal, supported, trusted base images.
- **DO-074** — Images must be built from version-controlled definitions and pinned dependencies.
- **DO-075** — Containers must run as non-root unless a documented technical requirement is approved.
- **DO-076** — Unnecessary capabilities, packages, shells, ports, and writable paths must be removed.
- **DO-077** — Container filesystems should be read-only where application behavior permits.
- **DO-078** — Images must not contain secrets, private keys, production data, or development tooling not required at runtime.
- **DO-079** — Resource requests, limits, health checks, shutdown behavior, and log output must be defined.
- **DO-080** — Images must be scanned before promotion and rescanned when new vulnerability intelligence appears.
- **DO-081** — Kubernetes workloads must use namespaces, service accounts, and policies aligned to trust and ownership boundaries.
- **DO-082** — Workloads must not use privileged mode, host networking, host paths, or broad cluster permissions without approved exception.
- **DO-083** — Kubernetes RBAC must use least privilege and avoid shared administrative identities.
- **DO-084** — Network policies or equivalent controls must restrict east-west traffic according to required flows.
- **DO-085** — Admission policies must enforce mandatory security, provenance, and configuration controls.
- **DO-086** — Persistent workloads must document storage class, backup, recovery, scaling, and failure behavior.
- **DO-087** — Ingress, reverse proxies, load balancers, and API gateways must terminate or pass through encryption according to documented trust boundaries.
- **DO-088** — Public entry points must enforce approved TLS, request limits, timeouts, security headers, and abuse controls.
- **DO-089** — Administrative endpoints must use separate protected access paths and must not be publicly exposed by default.
- **DO-090** — Service mesh adoption must be justified by operational need and must not obscure ownership, authorization, or failure diagnosis.

## Evidence

- Image definitions and scan results
- Runtime security contexts
- RBAC and network policies
- Ingress configuration
- Persistent workload recovery design