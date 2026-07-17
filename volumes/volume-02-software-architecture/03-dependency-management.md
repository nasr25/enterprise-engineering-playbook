# Dependency Management

## Objective

Control technical and organizational dependencies so that systems remain secure, replaceable, testable, and capable of independent evolution.

## Mandatory Rules

### ARC-021 — Dependency Direction

Dependencies **MUST** point toward stable abstractions and business capabilities rather than infrastructure details.

### ARC-022 — Explicit Dependency Inventory

Applications **MUST** maintain an inventory of runtime, build-time, platform, service, data, and vendor dependencies, including ownership and lifecycle status.

### ARC-023 — Supported Versions

Dependencies **MUST** use supported versions with known maintenance and security status. End-of-life dependencies require an approved remediation plan or exception.

### ARC-024 — Minimal Dependency Surface

Teams **MUST NOT** introduce a library, platform, service, or framework when the benefit does not exceed its security, operational, licensing, upgrade, and lock-in costs.

### ARC-025 — Dependency Isolation

External SDKs, vendor APIs, infrastructure clients, and volatile frameworks **SHOULD** be isolated behind adapters or anti-corruption layers where replacement or change is plausible.

### ARC-026 — Deterministic Resolution

Builds **MUST** resolve dependencies deterministically using lock files, immutable versions, verified artifacts, or equivalent controls.

### ARC-027 — Provenance and Integrity

Third-party artifacts **MUST** originate from approved repositories and **MUST** be verified using available integrity, signature, checksum, or provenance controls.

### ARC-028 — Automated Dependency Analysis

Projects **MUST** automate vulnerability, license, outdated-version, and transitive-dependency analysis appropriate to their ecosystem.

### ARC-029 — Upgrade Ownership

Every material dependency **MUST** have an accountable owner and an upgrade strategy. Upgrade work must not be deferred indefinitely as unowned technical debt.

### ARC-030 — Failure Containment

Failure, latency, quota exhaustion, or incompatibility in a dependency **MUST NOT** cause uncontrolled cascading failure across the system.

## Dependency Review Questions

Architecture and code reviews should verify:

- Why is the dependency needed?
- Is it actively supported?
- What data and privileges does it access?
- How is it upgraded or replaced?
- What happens when it is unavailable?
- Does it introduce licensing or data-residency constraints?
- Is its use isolated and observable?