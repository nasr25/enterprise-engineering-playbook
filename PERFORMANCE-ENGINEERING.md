# Performance Engineering — 31-Point Control Catalog

This cross-volume catalog consolidates existing standards and makes commonly requested performance techniques explicit. It is an **adoption and verification guide**, not a claim that every technique is mandatory in every application.

## Governance

- **PERF-001** — Every applicable control below MUST be evaluated for critical user journeys and documented as **Implemented**, **Planned**, **Not Applicable** (with rationale), or **Exception** (with owner and review date).
- **PERF-002** — Performance changes MUST be driven by a measurable baseline, target, and after-change evidence; optimize end-to-end latency, reliability, accessibility, security and cost rather than isolated scores.
- **PERF-003** — Conditional technologies (CDN, Redis, SSR/SSG, AI streaming, optimistic UI, virtualization, OpenTelemetry) MUST NOT be adopted without workload justification, operational ownership and risk review.
- **PERF-004** — Caching, batching, concurrency, rendering and compression MUST preserve authorization, tenant isolation, privacy, correctness and graceful failure.
- **PERF-005** — Critical user journeys MUST have risk-appropriate performance budgets, regression checks, and production or representative field monitoring.

## Control Catalog

| # | Control | Implementation and decision standard | Existing cross-reference | Minimum verification evidence |
|---|---|---|---|---|
| 1 | **Skeleton Loading** | Use accessible skeletons or meaningful progress indicators for perceptible waits; match final layout, avoid layout shifts, and do not mask errors. | FE-076, FE-090 | Visual regression, CLS and loading-state tests |
| 2 | **WebP / AVIF** | Serve modern image formats when supported with compatible fallback, responsive sizing and measured quality/byte savings; never blindly convert icons or already efficient images. | FE-080 | Image audit and network waterfall |
| 3 | **Duplicate API Calls** | Deduplicate equivalent in-flight requests; prevent lifecycle/refetch loops, cache-key collisions and accidental repeated mutations. Never deduplicate requests across distinct authorization scopes. | FE-084, BE-121 | Network trace and duplicate-request regression tests |
| 4 | **Debounce** | Debounce high-frequency search/filter/autocomplete input when appropriate; cancel stale work, preserve accessibility, and do not delay critical actions or security validation. | FE-076, FE-083 | Interaction trace, stale-response and keyboard tests |
| 5 | **Pagination** | Bound list/API results, use stable ordering, and prefer cursor/keyset pagination for large changing datasets; enforce limits server-side. | DB-041, DB-042, FE-085, BE-121 | Large-data query plan and API contract tests |
| 6 | **CDN** | Evaluate CDN for public static assets and geographic reach; set cache keys, invalidation, origin protection, privacy and residency rules. Do not cache private personalized responses publicly. | ARC-139, FE-086 | Cache-header audit, edge/origin latency comparison |
| 7 | **Background Job Queue** | Move justified long-running work to durable queues; define retries, idempotency, dead-letter handling, backpressure, progress and operational ownership. | BE-099–BE-116 | Queue metrics and failure/replay tests |
| 8 | **N+1 Queries** | Detect and eliminate N+1 ORM/database access with batching, eager loading, joins or aggregation without overfetching. | DB-043, BE-142 | Query count traces at representative scale |
| 9 | **Brotli / Gzip** | Enable negotiated Brotli and/or gzip for compressible text payloads at the appropriate proxy/server; verify content encoding, Vary, CPU cost and compatibility. Avoid compressing secrets mixed with attacker-controlled text when side-channel risk exists. | DO-088, FE-077 | HTTP header/transfer-size tests |
| 10 | **Redis Caching** | Use Redis or an approved equivalent only where justified; define keys, tenant/user scope, TTL, invalidation, stampede controls, capacity, failover and metrics. | ARC-127–ARC-140 | Hit-rate/latency measurements and outage tests |
| 11 | **Unused Dependencies** | Remove unused, duplicate, unsupported and unnecessary runtime/build dependencies after impact checks; scan transitive packages and preserve lockfile integrity. | FE-078, BE-134 | Dependency inventory, bundle/SCA report |
| 12 | **API Timeouts** | Set bounded inbound, outbound, database, queue and lock timeouts with cancellation, retry budgets and failure behavior; prevent cascading overload. | BE-119, BE-120 | Timeout/fault-injection tests |
| 13 | **AI Streaming** | Where AI responses are lengthy and progressive delivery improves UX, evaluate token/event streaming (SSE, chunked HTTP or approved transport); handle cancellation, moderation, authorization, backpressure, partial failure and sensitive output. | AI-061–AI-085, BE-119 | Time-to-first-token, cancellation and partial-stream tests |
| 14 | **Optimistic UI** | Use optimistic updates only for reversible low-risk actions; reconcile server authority, roll back on failure, handle conflicts and duplicate submission; avoid for irreversible/high-risk transactions. | FE-076, FE-084 | Conflict/offline/error UI tests |
| 15 | **Lazy Loading** | Lazy-load below-the-fold media, routes and heavy components while eagerly prioritizing critical above-the-fold content; avoid interaction delays and accessibility regressions. | FE-079, FE-080 | LCP, interaction and bundle tests |
| 16 | **Parallel Requests** | Run independent requests concurrently within downstream concurrency/rate limits; retain ordering/dependencies where necessary, cancellation and partial-failure handling; avoid uncontrolled fan-out. | BE-120, BE-123 | Waterfall comparison and load tests |
| 17 | **Database Indexes** | Design indexes from real predicates, joins, sorting and cardinality; validate execution plans, maintenance cost and write amplification. | DB-031–DB-038 | Execution plans and before/after latency |
| 18 | **OpenTelemetry** | Prefer interoperable tracing/metrics/log correlation such as OpenTelemetry where observability needs justify it; propagate trace context securely, sample appropriately and protect sensitive attributes. | SRE-041–SRE-065 | Cross-service trace and telemetry quality review |
| 19 | **Server / Database Proximity** | Assess application-to-database network latency, region/site placement, availability zones, residency and HA/DR trade-offs; do not sacrifice isolation or resilience solely for proximity. | ARC deployment topology, BE-117 | RTT/latency and architecture review |
| 20 | **SSR / Static Generation** | Choose SSR, SSG, hybrid or client rendering based on SEO, personalization, freshness, latency, infrastructure and caching; prevent private-data leaks in generated output. | FE-076–FE-090 | TTFB/LCP/SEO and cache-isolation tests |
| 21 | **Third-Party Scripts** | Inventory and justify third-party scripts, minimize blocking, defer noncritical loads, review privacy/security and failure impact; use CSP/SRI where applicable. | FE-082, FE-078 | Script waterfall, privacy and CSP audit |
| 22 | **Code Splitting** | Split bundles by routes and user journeys; preload only critical chunks, avoid fragmentation and ensure reliable cache-version compatibility. | FE-079, FE-088 | Chunk report and navigation performance |
| 23 | **Virtualization** | Virtualize very large lists/tables where measured DOM cost warrants it; preserve keyboard navigation, screen-reader semantics and stable row heights/scroll behavior. | FE-085 | Large-list interaction/accessibility tests |
| 24 | **Required Columns Only** | Select only fields needed by each operation; avoid SELECT *, sensitive overfetching and unnecessarily wide API payloads. | DB-040 | Query review and payload size audit |
| 25 | **Connection Pooling** | Bound database/HTTP connection pools by service instances and database capacity; tune queueing, idle lifetimes, saturation and failure recovery. | BE-120 | Pool saturation and DB connection metrics |
| 26 | **Unnecessary Re-renders** | Profile reactive state, component ownership and memoization; remove repeated renders/computations without speculative premature optimization. | FE-084 | Profiler comparison and UI regression |
| 27 | **Browser Caching** | Set explicit Cache-Control, ETag/Last-Modified where appropriate, immutable fingerprinted asset caching, safe HTML/service-worker invalidation and no-store for sensitive responses. | FE-086–FE-089, ARC-139 | Cache header and upgrade-path tests |
| 28 | **Load Balancing** | Use health-aware load balancing and capacity distribution for HA/scale; test session affinity assumptions, draining, failover, timeouts and backend consistency. | DO-087, ARC deployment topology | Failover/load test and health-check evidence |
| 29 | **Font Optimization** | Limit font families/weights, subset language glyphs carefully, preload only critical assets, choose font-display behavior and avoid CLS while preserving Arabic shaping. | FE-081 | Font transfer sizes, CLS and bilingual rendering |
| 30 | **Real User Monitoring** | Collect privacy-approved field performance data for key journeys (e.g. Web Vitals and errors) with representative sampling, retention, ownership and no secrets/PII. | FE-076, FE-090, SRE-041 | RUM dashboard and privacy review |
| 31 | **Performance Testing** | Set budgets and run representative load, stress, spike, soak and resilience tests with production-like datasets; compare baselines and enforce risk-based release gates. | BE-122, FE-090, TST non-functional | Signed performance report and regressions |

## Required Assessment Record

For each applicable item record: control number, owner, applicability/status, target metric, baseline, implementation link or configuration, verification result, date, and exception/next action if needed. Link to the Project Master Engineering Checklist and Production Readiness Review.

## Priority and Trade-offs

Start with measured bottlenecks (query plans/N+1, unnecessary requests, oversized payloads, critical rendering, timeouts and capacity) before adding infrastructure. Validate compression and caching at the deployed ingress. On isolated/on-premise environments, approved internal caches, reverse proxies and observability backends are valid alternatives to public SaaS/CDNs. Do not expose telemetry or protected data to unapproved external services.
