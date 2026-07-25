# Performance and Backend Security

## Purpose

Require measurable backend efficiency and defense-in-depth against common server-side threats and abuse.

## Mandatory Rules

- **BE-117** — Critical backend operations must have measurable latency, throughput, concurrency, and resource-use objectives.
- **BE-118** — Performance optimization must begin with profiling and evidence rather than assumption.
- **BE-119** — Timeouts must be configured for inbound requests, database operations, outbound calls, locks, and background processing.
- **BE-120** — Connection pools, worker pools, queues, and thread limits must be bounded and sized against downstream capacity.
- **BE-121** — Expensive operations must use pagination, streaming, batching, caching, precomputation, or asynchronous execution as appropriate.
- **BE-122** — Load tests must cover normal, peak, burst, sustained, and recovery behavior using realistic data and dependency conditions.
- **BE-123** — Services must degrade predictably under saturation and must reject excess work before exhausting critical resources.
- **BE-124** — Backend endpoints must enforce authorization, validation, rate limits, and payload limits at the authoritative boundary.
- **BE-125** — All database, command, template, and directory operations must prevent injection through parameterization, allowlisting, or safe APIs.
- **BE-126** — Server-side request forgery risks must be controlled through destination allowlists, network policy, URL validation, and restricted credentials.
- **BE-127** — File upload processing must validate type, size, name, content, storage location, and malware risk before downstream use.
- **BE-128** — Deserialization must use trusted formats and explicit type constraints; unsafe polymorphic deserialization is prohibited.
- **BE-129** — Outbound responses must not expose stack traces, internal identifiers, connection strings, filesystem paths, or sensitive dependency details.
- **BE-130** — State-changing browser-accessible endpoints must protect against cross-site request forgery where ambient credentials are used.
- **BE-131** — Cross-origin access must use explicit trusted origins, methods, headers, and credential settings; wildcard credentials are prohibited.
- **BE-132** — Security headers and cookie attributes must be set consistently at the application or trusted ingress layer.
- **BE-133** — Sensitive operations must use replay protection, idempotency, step-up authentication, or transaction confirmation according to risk.
- **BE-134** — Dependencies must be pinned or constrained, scanned, updated, and removed when unsupported.
- **BE-135** — Administrative, diagnostic, health, metrics, and documentation endpoints must have an explicit exposure and authorization policy.
- **BE-136** — Security events must be logged and monitored without recording secret material.

## Required Evidence

- Performance test report
- Resource-limit configuration
- Threat model and abuse cases
- Security test results
- Dependency and endpoint inventory