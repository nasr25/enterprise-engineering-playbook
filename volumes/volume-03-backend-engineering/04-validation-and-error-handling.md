# Validation and Error Handling

## Mandatory Rules

- **BE-039** — Inputs from clients, files, queues, integrations, configuration, and databases must be treated as untrusted at the receiving boundary.
- **BE-040** — Validation must cover syntax, type, length, range, format, allowed values, relationships, business invariants, and authorization-sensitive fields.
- **BE-041** — Unknown or protected fields must be rejected or safely ignored according to a documented contract; mass assignment must be prevented.
- **BE-042** — Validation behavior must be deterministic and must not reveal secrets, internal topology, stack traces, or sensitive existence information.
- **BE-043** — Error responses must use a consistent machine-readable model containing a stable code, safe message, correlation identifier, and field details where applicable.
- **BE-044** — Internal exceptions must be translated at the service boundary and must not leak framework, database, filesystem, or dependency details.
- **BE-045** — Expected business failures must be represented explicitly rather than through generic exceptions.
- **BE-046** — Unexpected failures must be logged once at the responsible boundary with sufficient context for diagnosis and without duplicate noisy logging.
- **BE-047** — Retriable errors must be distinguishable from permanent failures and must include safe retry guidance where useful.
- **BE-048** — Error codes exposed to consumers must remain stable across implementation refactoring.
- **BE-049** — Validation and error handling must preserve transaction integrity and avoid partial side effects unless partial processing is part of the contract.
- **BE-050** — Tests must cover boundary values, malformed payloads, unknown fields, injection attempts, invariant violations, dependency failures, and safe error disclosure.

## Recommended Error Shape

```json
{
  "code": "ORDER_STATE_CONFLICT",
  "message": "The order cannot be changed in its current state.",
  "correlationId": "...",
  "details": []
}
```

The exact schema may vary, but consistency and safe disclosure are mandatory.
