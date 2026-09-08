# 3. Data, Offline Operation, and Synchronization

Rules `MOB-056`–`MOB-075`.

## Requirements

- `MOB-056` Local persistence MUST be classified by sensitivity, lifetime, and authoritative source.
- `MOB-057` Sensitive data MUST NOT be persisted locally without a documented need.
- `MOB-058` Credentials and tokens MUST use secure storage rather than general preferences or unprotected databases.
- `MOB-059` Local databases MUST define schema evolution and migration behavior across application upgrades.
- `MOB-060` Cache data MUST have explicit invalidation or expiry behavior.
- `MOB-061` Offline-capable features MUST define which operations are allowed while disconnected.
- `MOB-062` The authoritative system of record MUST be explicit for synchronized data.
- `MOB-063` Synchronization MUST be idempotent or otherwise protected against duplicate application.
- `MOB-064` Retries MUST use bounded backoff and MUST NOT create duplicate business transactions.
- `MOB-065` Mutation queues MUST persist sufficient metadata to distinguish pending, succeeded, failed, superseded, and conflicted operations.
- `MOB-066` Conflict resolution MUST be defined intentionally; silent last-write-wins MUST NOT be assumed for critical data.
- `MOB-067` Business-critical conflicts SHOULD be surfaced for deterministic resolution when automatic reconciliation is unsafe.
- `MOB-068` Offline authorization state MUST expire and MUST NOT grant indefinite access after server-side permissions change.
- `MOB-069` Sensitive cached data SHOULD be cleared or revalidated when users switch accounts.
- `MOB-070` Device clock MUST NOT be trusted as the sole authority for security-sensitive timestamps or expiry decisions.
- `MOB-071` Large datasets SHOULD use pagination, incremental sync, delta tokens, or equivalent mechanisms rather than full reloads.
- `MOB-072` Sync protocols SHOULD detect stale versions using version fields, ETags, revision numbers, or equivalent concurrency mechanisms.
- `MOB-073` Background synchronization MUST respect battery, data, OS scheduling, and user-experience constraints.
- `MOB-074` Local data corruption or failed migrations MUST have a documented recovery strategy that preserves server-authoritative data where possible.
- `MOB-075` Offline and synchronization behavior MUST be covered by automated tests for retries, duplicate delivery, conflicts, network transitions, and interrupted application lifecycle.

## Review Evidence

Data classification, local schema, cache policy, sync state model, conflict strategy, retry/idempotency behavior, migration tests, and offline test evidence.
