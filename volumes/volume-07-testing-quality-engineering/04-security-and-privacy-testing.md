# Security and Privacy Testing

## Mandatory Rules

- **TST-071** — Security testing must be derived from the threat model, data classification, attack surface, and applicable control baseline.
- **TST-072** — Static analysis must run on supported languages and must block unresolved critical findings unless formally accepted.
- **TST-073** — Software composition analysis must identify vulnerable, malicious, unsupported, and license-incompatible dependencies.
- **TST-074** — Dynamic testing must cover deployed attack surfaces in a representative environment.
- **TST-075** — Secret scanning must cover source, history, configuration, artifacts, images, logs, and generated files.
- **TST-076** — Authentication tests must cover enumeration, brute force, lockout, MFA, recovery, session expiry, and credential lifecycle.
- **TST-077** — Authorization tests must verify deny-by-default behavior, permission boundaries, object ownership, tenant isolation, and privilege escalation resistance.
- **TST-078** — Injection testing must cover SQL, command, template, LDAP, expression, path, and other interpreters used by the system.
- **TST-079** — Web testing must cover XSS, CSRF, clickjacking, unsafe redirects, CORS, CSP, cookies, and transport enforcement.
- **TST-080** — API security testing must cover broken object authorization, excessive data exposure, mass assignment, resource exhaustion, and unsafe business flows.
- **TST-081** — File handling tests must cover content validation, malware, path traversal, archive expansion, metadata leakage, and unauthorized retrieval.
- **TST-082** — Cryptographic tests must verify approved protocols, certificate validation, key usage, rotation, and failure behavior.
- **TST-083** — Sensitive data tests must verify encryption, masking, minimization, logging exclusions, export controls, and deletion behavior.
- **TST-084** — Privacy tests must verify notice, consent, purpose limitation, access, correction, export, retention, and erasure where applicable.
- **TST-085** — Audit testing must verify actor, action, target, outcome, timestamp, integrity, access control, and retention.
- **TST-086** — Multi-tenant tests must attempt cross-tenant reads, writes, searches, exports, caches, files, jobs, and administrative actions.
- **TST-087** — Business logic abuse tests must cover replay, duplicate redemption, sequence bypass, limit evasion, and race conditions.
- **TST-088** — Fuzz testing must be used for high-risk parsers, protocols, file formats, and complex input boundaries where practical.
- **TST-089** — Security headers and TLS configuration must be validated in the deployed environment.
- **TST-090** — Infrastructure and container tests must verify exposed ports, privilege, identity, secrets, images, network policy, and hardened configuration.
- **TST-091** — Penetration testing scope and cadence must reflect exposure, criticality, regulatory obligations, and material architectural change.
- **TST-092** — Security test evidence must distinguish confirmed vulnerabilities, false positives, mitigated risk, and accepted risk.
- **TST-093** — Remediation verification must reproduce the original issue and test likely bypass variants.
- **TST-094** — Production security testing must use approved safeguards and must not place users, data, or availability at uncontrolled risk.
- **TST-095** — Security testing tools and payloads must be authorized, controlled, and retained according to policy.