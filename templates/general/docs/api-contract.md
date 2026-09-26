# API Contract

**Version:** 1
**Status:** Draft
**Owners:** <provider owner>, <consumer owners>

This document is the integration source of truth for public APIs, events, commands, files, and cross-system schemas. Keep prose workflows in `integration/` and implemented endpoint reference in `api/`.

## 1. Contract conventions

Document conventions that apply everywhere:

- base URLs, protocol versions, and content types;
- field naming, identifiers, timestamps, units, and numeric precision;
- authentication and authorization model;
- idempotency, ordering, pagination, retries, and timeout behavior;
- compatibility policy and deprecation window;
- standard success envelope, error envelope, and correlation identifiers.

Do not assume that a convention is understood. If clients must implement it consistently, define it here.

## 2. Public interfaces

Create one section per external interface. For HTTP endpoints, include method, path, authentication, request, success response, reachable errors, side effects, and idempotency behavior. For events or commands, include producer, consumers, delivery guarantees, ordering, schema, and retry behavior.

### <Interface name>

**Type:** `<HTTP | WebSocket | event | command | file>`
**Owner:** `<component or team>`
**Consumers:** `<components or teams>`

#### Request or input

```json
{
  "field": "<verified example>"
}
```

| Field | Type | Required | Nullable | Constraints | Description |
| --- | --- | --- | --- | --- | --- |
| `field` | `string` | Yes | No | <constraints> | <meaning> |

#### Response or output

```json
{
  "field": "<verified example>"
}
```

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| `field` | `string` | No | <meaning> |

#### Errors

| Status or outcome | Code | Condition | Retryable |
| --- | --- | --- | --- |
| <status> | `<code>` | <verified condition> | <yes or no> |

#### Behavioral guarantees

- Describe side effects, idempotency, concurrency, ordering, lifecycle transitions, and consumer obligations.

## 3. Internal cross-component interfaces

Document schemas that cross independently owned or independently deployed component boundaries even when they are not public. Keep in-process details out unless they function as a versioned contract.

## 4. Compatibility and change process

- Additive optional fields may be introduced only when all consumers tolerate them.
- Breaking changes require a new contract version or a coordinated migration with explicit rollout and rollback steps.
- Update this contract before or in the same change as implementation.
- Update each affected API-group and integration guide without duplicating the authoritative schema.
- Add contract tests at provider and consumer boundaries.

## 5. Integration checklist

- [ ] Provider implementation matches every documented field and outcome.
- [ ] Consumer responsibilities, retry rules, and timeouts are explicit.
- [ ] Authentication and authorization behavior is verified.
- [ ] Idempotency, ordering, and concurrency behavior is verified.
- [ ] Reachable errors are documented and covered by tests.
- [ ] Backward compatibility and rollout sequencing are resolved.
- [ ] API-group and integration documents link to this contract and do not contradict it.
