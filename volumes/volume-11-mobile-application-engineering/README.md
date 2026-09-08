# Volume 11 — Mobile Application Engineering

Enterprise standards for designing, building, securing, testing, releasing, and operating mobile applications across iOS and Android.

This volume is technology-neutral. Flutter is covered explicitly as a reference implementation, while the engineering rules also apply to native iOS/Android, React Native, Kotlin Multiplatform, and comparable mobile stacks.

## Scope

Applies to mobile clients, mobile APIs, offline-capable applications, push-enabled applications, biometric authentication, device integrations, deep links, secure local storage, mobile CI/CD, App Store / Play Store delivery, and enterprise-distributed apps.

## Core Position

A mobile application is an untrusted client running on a user-controlled device. Security-sensitive authorization and data-integrity decisions MUST be enforced by trusted backend systems. Device protections reduce risk but do not replace server-side controls.

## Rule Namespace

Mobile rules use the prefix `MOB`.

## Chapters

1. Mobile Architecture and Application Structure — `MOB-001`–`MOB-025`
2. Mobile Security and Identity — `MOB-026`–`MOB-055`
3. Data, Offline Operation, and Synchronization — `MOB-056`–`MOB-075`
4. Device Capabilities, Integrations, and Notifications — `MOB-076`–`MOB-095`
5. Quality, Testing, Accessibility, and Performance — `MOB-096`–`MOB-120`
6. Build, Signing, Release, and Store Governance — `MOB-121`–`MOB-145`
7. Flutter Engineering Guidance — `MOB-146`–`MOB-170`
8. Mobile Engineering Review Checklist — `MOB-171`–`MOB-180`

## Cross-Volume Dependencies

Mobile projects must also apply relevant controls from:
- Volume 01 — Engineering Principles & Governance
- Volume 02 — Software Architecture
- Volume 03 — Backend Engineering
- Volume 05 — Database Engineering when local or backend persistence applies
- Volume 06 — DevOps & Platform Engineering
- Volume 07 — Testing & Quality Engineering
- Volume 09 — Operations & SRE
- Volume 10 — Enterprise Templates & Checklists
- Volume 08 — AI Engineering when AI/ML features are present

## Non-Negotiable Positions

- Mobile clients MUST NOT be trusted to make final authorization decisions.
- Secrets, private keys, signing credentials, and long-lived privileged tokens MUST NOT be embedded in application binaries or source code.
- Sensitive local data MUST use approved secure storage and platform protections.
- Offline workflows MUST define conflict handling, replay protection, synchronization ownership, and integrity rules.
- Deep links, push payloads, intents, universal links, and external app inputs MUST be treated as untrusted input.
- Production releases MUST be reproducible, signed through controlled credentials, traceable to source, and subject to review gates.
- Flutter applications MUST follow the same architecture, security, testing, and operational controls as any other production application.
