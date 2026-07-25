# Volume 05 — Database Engineering

## Purpose

Define enterprise standards for designing, operating, securing, evolving, and reviewing data stores used by transactional, analytical, integration, search, and reporting workloads.

## Scope

These standards apply to relational databases, document databases, key-value stores, search engines, time-series platforms, caches, analytical stores, and data pipelines. They are technology-neutral and may be implemented with MySQL, PostgreSQL, SQL Server, Oracle, MongoDB, Redis, Elasticsearch, and equivalent platforms.

## Chapters

1. [Architecture and Data Modeling](01-architecture-and-data-modeling.md)
2. [Schema, SQL, and Query Design](02-schema-sql-and-query-design.md)
3. [Transactions, Concurrency, and Integrity](03-transactions-concurrency-and-integrity.md)
4. [Scale, Availability, Backup, and Recovery](04-scale-availability-backup-and-recovery.md)
5. [Schema Evolution and Data Lifecycle](05-schema-evolution-and-data-lifecycle.md)
6. [Security, Privacy, and Multi-Tenancy](06-security-privacy-and-multi-tenancy.md)
7. [Operations, Performance, and Capacity](07-operations-performance-and-capacity.md)
8. [Specialized Data Platforms and Pipelines](08-specialized-platforms-and-pipelines.md)
9. [Database Engineering Review Checklist](09-database-engineering-review-checklist.md)

## Rule Namespace

Rules in this volume use the `DB` prefix and cover `DB-001` through `DB-160`.

## Core Position

Data integrity, recoverability, security, and predictable performance are architectural properties. They must be designed, tested, monitored, and governed rather than delegated to default database behavior.