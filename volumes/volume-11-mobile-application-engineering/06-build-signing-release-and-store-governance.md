# 6. Build, Signing, Release, and Store Governance

Rules `MOB-121`–`MOB-145`.

## Requirements

- `MOB-121` Production mobile builds MUST be produced through a controlled and repeatable build process.
- `MOB-122` Build outputs MUST be traceable to source revision, build configuration, dependency state, and release approval.
- `MOB-123` Signing certificates, keystores, provisioning profiles, API keys, and store credentials MUST be protected as privileged secrets.
- `MOB-124` Signing credentials MUST NOT be committed to source repositories.
- `MOB-125` Access to production signing and store-publishing credentials MUST follow least privilege.
- `MOB-126` Signing credential rotation, expiry, recovery, and ownership MUST be documented.
- `MOB-127` Development/test builds MUST be clearly distinguishable from production builds.
- `MOB-128` Debug features, test endpoints, mock authentication, verbose logging, and developer menus MUST NOT be unintentionally enabled in production releases.
- `MOB-129` Release builds MUST use approved production endpoint configuration.
- `MOB-130` Dependency resolution SHOULD be reproducible and unexpected dependency upgrades MUST be reviewable.
- `MOB-131` Mobile CI SHOULD run lint/static checks, tests, security/dependency checks, and build validation before release.
- `MOB-132` Production releases MUST pass applicable security and quality gates before publishing.
- `MOB-133` Version names and build numbers MUST follow a documented versioning convention.
- `MOB-134` Backend compatibility MUST account for users remaining on older mobile versions after a new release.
- `MOB-135` Breaking mobile API changes MUST use controlled versioning or compatibility migration strategies.
- `MOB-136` Minimum supported application and OS versions MUST be managed intentionally, with forced-upgrade behavior reserved for justified cases.
- `MOB-137` Emergency releases MUST remain traceable and subject to post-release review.
- `MOB-138` Store metadata, privacy disclosures, permission declarations, screenshots, and release notes MUST accurately represent application behavior.
- `MOB-139` TestFlight, Play testing tracks, enterprise distribution, or equivalent pre-production channels SHOULD be used before broad production rollout where practical.
- `MOB-140` Staged/phased rollout SHOULD be considered for releases with material risk.
- `MOB-141` Release monitoring MUST detect abnormal crashes, authentication failures, API errors, or other severe regressions after rollout.
- `MOB-142` Mobile rollback planning MUST recognize that already-installed binaries cannot always be instantly recalled; backend feature flags and compatibility controls SHOULD support mitigation.
- `MOB-143` Compromised signing credentials or malicious releases MUST have an incident response procedure.
- `MOB-144` Ownership of Apple/Google developer accounts, certificates, app identifiers, and store applications MUST belong to the organization rather than an individual where organizational use applies.
- `MOB-145` Production release evidence MUST include approval, source/build traceability, quality/security results, signing/publishing identity, and post-release validation.

## Review Evidence

CI configuration, signing ownership, secret-management records, release checklist, version policy, store configuration, testing-track evidence, approval record, and post-release validation.
