# 8. Mobile Engineering Review Checklist

Rules `MOB-171`–`MOB-180`.

Use this checklist before production release and for material mobile changes.

- `MOB-171` Architecture: application boundaries, state ownership, lifecycle behavior, environment separation, and platform integrations are documented and reviewed.
- `MOB-172` Identity and authorization: authentication/session flows are secure and all protected business actions are authorized server-side.
- `MOB-173` Local security: tokens and sensitive data use approved protected storage; no secrets are embedded in code, assets, binaries, logs, or analytics.
- `MOB-174` External inputs: deep links, push actions, intents, QR/barcodes, files, WebViews, and external callbacks are validated and threat-modeled.
- `MOB-175` Offline and data: caching, local schema, synchronization, retry, duplicate prevention, conflicts, account switching, and data cleanup are defined and tested.
- `MOB-176` Device integrations: permissions are minimal, denial/revocation is safe, native/plugin surfaces are reviewed, and third-party SDKs are approved.
- `MOB-177` Quality: critical journeys, failure states, lifecycle transitions, offline cases, supported devices/OS versions, accessibility, localization, and performance have sufficient evidence.
- `MOB-178` Release governance: production build is traceable, reproducible, correctly configured, signed with controlled credentials, and published through approved accounts/channels.
- `MOB-179` Operations: crash/error monitoring, backend compatibility, phased rollout/mitigation where appropriate, incident response, and post-release validation are ready.
- `MOB-180` Flutter-specific review when applicable: architecture/state conventions, secure storage, plugins/platform channels, lifecycle disposal, static analysis, tests, iOS/Android behavior, and release builds meet `MOB-146`–`MOB-170`.

## Minimum Production Evidence

A production mobile application should normally provide:

- applicable architecture/ADRs;
- mobile threat model;
- authentication and authorization design;
- local-data and synchronization design where applicable;
- permission and third-party SDK inventory;
- automated test evidence and supported-platform matrix;
- security/dependency scan evidence;
- build/signing/release traceability;
- store or enterprise-distribution approval evidence;
- monitoring and post-release validation evidence;
- documented exceptions for any unmet applicable rules.

Completion of this checklist does not itself prove conformance. The underlying project evidence must support each applicable control.
