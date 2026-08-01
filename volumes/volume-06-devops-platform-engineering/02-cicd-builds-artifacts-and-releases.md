# CI/CD, Builds, Artifacts, and Releases

## Mandatory Rules

- **DO-019** — CI/CD pipelines must be defined as version-controlled code.
- **DO-020** — Pipeline changes must be reviewed and tested before affecting protected environments.
- **DO-021** — Builds must be reproducible from a known commit, dependency set, toolchain, and configuration.
- **DO-022** — Build agents must be isolated, patched, and prevented from retaining unnecessary secrets or artifacts.
- **DO-023** — Pipelines must fail closed when required tests, scans, approvals, or validations fail.
- **DO-024** — Build output must be immutable after publication.
- **DO-025** — The same approved artifact must be promoted across environments; rebuilding per environment is prohibited.
- **DO-026** — Artifacts must include version, source commit, build identity, timestamp, and provenance metadata.
- **DO-027** — Artifact repositories must enforce authentication, authorization, retention, integrity, and malware controls.
- **DO-028** — Release versions must follow a documented, consistent scheme.
- **DO-029** — Release notes must identify user impact, technical changes, migrations, known issues, and rollback guidance.
- **DO-030** — Pipeline stages must separate build, verification, approval, deployment, and post-deployment validation.
- **DO-031** — Production deployment permissions must be separated from ordinary development permissions.
- **DO-032** — Manual production actions must be minimized, logged, and covered by approved procedures.
- **DO-033** — Pipeline concurrency must prevent conflicting deployments to the same target.
- **DO-034** — Promotion decisions must be traceable to test evidence and approvals.
- **DO-035** — Release pipelines must support safe cancellation and clearly report partial completion.
- **DO-036** — Failed or abandoned artifacts must not be promoted to protected environments.

## Evidence

- Pipeline definitions
- Artifact provenance
- Release records
- Promotion approvals
- Pipeline access matrix