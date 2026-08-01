# Test Automation and CI Quality Gates

## Mandatory Rules

- **TST-096** — Automation must target repeatable, high-value, high-risk checks rather than maximizing automated test count.
- **TST-097** — Automated tests must be readable, maintainable, version-controlled, reviewed, and owned with production code.
- **TST-098** — Test architecture must separate reusable fixtures, data builders, clients, assertions, and environment configuration.
- **TST-099** — Tests must avoid arbitrary sleeps and must synchronize on observable conditions with bounded timeouts.
- **TST-100** — Automated tests must be deterministic and must control time, randomness, network, and external dependencies where needed.
- **TST-101** — Parallel tests must isolate data, accounts, files, ports, and other mutable resources.
- **TST-102** — Flaky tests must be quarantined only temporarily, assigned an owner, and corrected within an agreed timeframe.
- **TST-103** — Automatic retries must not conceal deterministic failures or inflate reported pass rates.
- **TST-104** — Pipeline stages must run the fastest and most diagnostic checks before slower suites.
- **TST-105** — Pull-request gates must include applicable build, unit, static, dependency, secret, and focused integration checks.
- **TST-106** — Main-branch and release gates must include broader integration, contract, security, regression, and deployment verification.
- **TST-107** — Critical gate failures must block promotion unless an authorized, recorded, time-bound exception exists.
- **TST-108** — Test reports must include failures, duration, environment, commit, artifacts, and links to diagnostic evidence.
- **TST-109** — Failed tests must preserve relevant logs, screenshots, traces, requests, responses, and environment metadata without exposing secrets.
- **TST-110** — Coverage thresholds must be risk-based and must not encourage low-value assertions or exclusion abuse.
- **TST-111** — Critical business and security rules must have explicit tests regardless of aggregate code coverage.
- **TST-112** — Mutation testing should be applied to critical logic where ordinary coverage does not demonstrate assertion strength.
- **TST-113** — Contract suites must run when provider or consumer contracts change.
- **TST-114** — Database migration tests must run from supported prior versions and verify forward compatibility and rollback strategy.
- **TST-115** — Deployment pipelines must execute post-deployment smoke and health validation before completing promotion.
- **TST-116** — Test selection optimization must preserve mandatory risk coverage and must be periodically validated.
- **TST-117** — Shared test tooling must be versioned, supported, secured, and compatible with project runtimes.
- **TST-118** — Generated test code must meet the same review, security, determinism, and maintenance standards as handwritten tests.
- **TST-119** — CI secrets and test credentials must be least-privileged, isolated, rotated, and excluded from output.
- **TST-120** — Quality-gate configuration changes must be reviewed and auditable.