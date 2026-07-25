# Scalability and Capacity Architecture

## Purpose

Design systems to meet forecast demand without uncontrolled cost, instability, or emergency redesign.

## Mandatory Rules

- **ARC-175** — Critical systems must document expected load, growth assumptions, peak patterns, concurrency, payload sizes, and retention drivers.
- **ARC-176** — Capacity decisions must be based on measured bottlenecks or justified forecasts rather than arbitrary resource increases.
- **ARC-177** — Services intended for horizontal scaling must avoid uncoordinated local state or must externalize and protect that state.
- **ARC-178** — Scaling behavior must account for downstream capacity so that adding application replicas does not overload databases, queues, identity providers, or external services.
- **ARC-179** — Resource limits, quotas, and backpressure must be defined for workloads that can consume unbounded CPU, memory, storage, connections, or queue depth.
- **ARC-180** — Autoscaling signals must represent useful workload pressure and must include safe minimums, maximums, cooldowns, and failure behavior.
- **ARC-181** — Large datasets must use bounded queries, pagination or streaming, appropriate indexing, and controlled batch sizes.
- **ARC-182** — Capacity testing must include peak load, sustained load, burst behavior, degradation thresholds, and recovery after saturation.
- **ARC-183** — Performance targets must be expressed through measurable service objectives and tested at realistic scale.
- **ARC-184** — Cost-sensitive scaling decisions must identify the expected cost driver and a method for detecting inefficient growth.

## Required Evidence

- Capacity model
- Load-test results
- Bottleneck analysis
- Scaling policy
- Downstream dependency limits
