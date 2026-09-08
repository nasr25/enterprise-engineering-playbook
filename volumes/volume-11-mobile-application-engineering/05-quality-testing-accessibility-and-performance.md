# 5. Quality, Testing, Accessibility, and Performance

Rules `MOB-096`–`MOB-120`.

## Requirements

- `MOB-096` Mobile applications MUST have automated tests appropriate to business risk and change frequency.
- `MOB-097` Business/domain logic SHOULD be covered by fast unit tests independent of UI frameworks where practical.
- `MOB-098` API/data layers MUST be tested for success, failure, timeout, malformed data, expired sessions, and retry behavior.
- `MOB-099` Critical user journeys SHOULD have integration or end-to-end coverage on representative devices/emulators.
- `MOB-100` Tests MUST cover foreground/background transitions, process recreation, network loss, and session expiry for critical flows.
- `MOB-101` Offline/sync features MUST test duplicate retries, conflict scenarios, partial synchronization, and interrupted operations.
- `MOB-102` Authentication and authorization failure cases MUST be tested, not only successful login flows.
- `MOB-103` Deep links, push actions, intents, and externally supplied routes MUST have negative/security tests.
- `MOB-104` Device permission denial and revocation MUST be tested.
- `MOB-105` Supported OS versions and device classes MUST be explicitly defined and tested proportionately to usage/risk.
- `MOB-106` Release candidates SHOULD be tested on real devices in addition to simulators/emulators for material features.
- `MOB-107` Accessibility MUST be considered for labels, focus order, contrast, dynamic text scaling, touch targets, and screen readers.
- `MOB-108` Localization and right-to-left layouts MUST be tested when supported, including truncation and mirrored navigation behavior.
- `MOB-109` Loading, empty, error, offline, and degraded states MUST have explicit acceptance criteria.
- `MOB-110` Cold start, warm start, frame rendering, memory use, network latency, battery impact, and package size SHOULD be measured for performance-sensitive applications.
- `MOB-111` Main/UI thread blocking MUST be minimized; expensive parsing, I/O, cryptography, and computation SHOULD be moved off the UI thread when appropriate.
- `MOB-112` Large images, lists, and media MUST use memory-conscious loading, pagination, caching, and disposal strategies.
- `MOB-113` Network calls SHOULD be consolidated, cancellable where useful, and protected from unnecessary duplication.
- `MOB-114` Crash-free sessions/users and startup failures SHOULD be monitored for production applications.
- `MOB-115` Application crashes MUST be triaged with severity, affected versions, reproducibility, and business impact.
- `MOB-116` Performance regressions on critical flows SHOULD be prevented through measurable budgets or release thresholds.
- `MOB-117` Test data MUST avoid exposing real sensitive production data unless explicitly approved and protected.
- `MOB-118` Automated mobile tests MUST be deterministic enough to provide release confidence; flaky tests MUST be tracked and remediated.
- `MOB-119` Security testing MUST include the backend/API because mobile client testing alone cannot establish end-to-end security.
- `MOB-120` Release readiness MUST include evidence for functional quality, security, accessibility where applicable, performance, and supported-platform compatibility.

## Review Evidence

Test strategy, automated results, device/OS matrix, accessibility checks, performance measurements, crash metrics, and known-risk acceptance.
