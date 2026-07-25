# Volume 04 — Frontend Engineering

## Purpose

Define production-grade standards for web frontends and client applications that are secure, accessible, maintainable, observable, performant, and resilient to backend and network failure.

## Scope

These standards apply to browser applications, progressive web applications, server-rendered web frontends, administrative portals, embedded web interfaces, and shared frontend component libraries.

## Chapters

1. [Frontend Architecture](01-frontend-architecture.md)
2. [State and Data Flow](02-state-and-data-flow.md)
3. [API Integration and Resilience](03-api-integration-and-resilience.md)
4. [Frontend Security](04-frontend-security.md)
5. [Accessibility and Internationalization](05-accessibility-and-internationalization.md)
6. [Performance and Delivery](06-performance-and-delivery.md)
7. [Testing and Quality](07-testing-and-quality.md)
8. [Observability and Operations](08-observability-and-operations.md)
9. [Frontend Review Checklist](09-frontend-review-checklist.md)

## Rule Namespace

Rules in this volume use the `FE` prefix. The completed rule set covers `FE-001` through `FE-120`.

## Core Position

The frontend is an untrusted client and a critical part of the user experience. It must not be the sole enforcement point for authorization or data integrity, but it remains responsible for secure rendering, accessible interaction, reliable state behavior, and measurable user-facing performance.