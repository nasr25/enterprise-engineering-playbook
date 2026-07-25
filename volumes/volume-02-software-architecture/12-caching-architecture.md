# Caching Architecture

## Purpose

Caching is an optimization that introduces duplicated state, staleness, eviction behavior, and new failure modes. It must never be treated as invisible infrastructure.

## Rules

### ARC-127 — Caching must solve a measured problem
A cache must be justified by latency, throughput, cost, availability, or load evidence and have a defined success metric.

### ARC-128 — The source of truth must remain explicit
Every cached value must have a documented authoritative source and reconstruction method.

### ARC-129 — Cache keys must be deterministic and scoped
Keys must include all dimensions that affect the value, including tenant, authorization scope, locale, version, and relevant request parameters.

### ARC-130 — Sensitive data requires explicit cache approval
Secrets, credentials, personal data, and authorization decisions must not be cached without encryption, access, retention, and invalidation controls.

### ARC-131 — Time-to-live must reflect business tolerance
Expiration must be based on acceptable staleness, update frequency, recovery behavior, and load impact rather than arbitrary defaults.

### ARC-132 — Invalidation must be designed before implementation
The architecture must define write-through, write-behind, cache-aside, event invalidation, versioned keys, or deliberate expiration behavior.

### ARC-133 — Cache failure must degrade safely
Applications must define behavior when the cache is slow, empty, inconsistent, or unavailable and must avoid uncontrolled fallback load.

### ARC-134 — Stampedes must be prevented
High-demand keys require techniques such as request coalescing, locking, jittered expiry, stale-while-revalidate, or controlled prewarming.

### ARC-135 — Negative caching must be bounded
Caching absence or failures requires short expiration and must not hide newly created or recovered data.

### ARC-136 — Authorization caches must fail closed
Cached permissions must be scoped to identity and policy version, have bounded lifetime, and never grant access after uncertainty.

### ARC-137 — Cache consistency must be observable
Metrics must expose hit ratio, misses, evictions, latency, errors, memory pressure, stale reads where measurable, and fallback behavior.

### ARC-138 — Cache content must be disposable
Loss of a cache must not cause permanent data loss. Rebuild and warm-up procedures must be documented for critical caches.

### ARC-139 — Multi-level caches require coherence rules
Browser, CDN, gateway, application, and database caches must define ownership, propagation, invalidation, and maximum staleness.

### ARC-140 — Cache changes require load validation
Changes to key design, TTL, capacity, topology, or invalidation must be tested against realistic concurrency and failure conditions.

## Required Cache Record

- use case and measured objective
- source of truth
- key structure
- data classification
- TTL and invalidation
- failure and fallback behavior
- capacity assumptions
- observability
- recovery and warm-up
