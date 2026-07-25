# Deployment Topology

## Purpose

Define how software components are placed across networks, compute environments, trust zones, and failure domains.

## Mandatory Rules

- **ARC-141** — Every production system must have a documented deployment topology showing clients, ingress, application components, data stores, integrations, trust zones, and administrative paths.
- **ARC-142** — Internet-facing components must be separated from internal services by explicit network and security controls.
- **ARC-143** — Application and data tiers must not be collapsed into one host in production unless a documented exception is approved.
- **ARC-144** — Administrative interfaces must use dedicated protected paths and must not be exposed through public ingress by default.
- **ARC-145** — Stateful components must identify persistence, replication, backup, and recovery behavior.
- **ARC-146** — Production topology must identify single points of failure and the accepted mitigation for each.
- **ARC-147** — High-availability workloads must distribute replicas across independent failure domains where the platform supports it.
- **ARC-148** — Environment boundaries between development, test, staging, and production must be enforced through separate credentials, configuration, and access controls.
- **ARC-149** — Production secrets and data must not be copied into non-production environments without approved masking and protection.
- **ARC-150** — Deployment topology changes that alter trust boundaries, exposure, persistence, or availability must receive architecture and security review.

## Required Evidence

- Current deployment diagram
- Network and trust-zone mapping
- Port and protocol inventory
- Failure-domain analysis
- Environment separation statement
