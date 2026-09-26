# Integration guides

Use `../api-contract.md` as the source of truth for schemas, status codes, error codes, events, and compatibility guarantees. Integration guides explain end-to-end workflows without repeating the contract.

## Boundaries

| Boundary | Guide | Owners |
| --- | --- | --- |
| `<consumer>` to `<provider>` | `<guide>.md` | <owners> |

Create one guide per independently owned integration boundary.

## Required content

Each guide should document:

- the purpose and prerequisites of the integration;
- the ordered request, event, callback, or file flow;
- responsibilities on both sides of the boundary;
- authentication, configuration, timeout, retry, idempotency, and cancellation behavior;
- error recovery, degraded behavior, and reconciliation;
- rollout, compatibility, and observability requirements;
- links to the authoritative contract and relevant operations guide.

Update a workflow guide when its sequence, consumer responsibility, retry behavior, or operational requirement changes. Update `../api-contract.md` when an interface or schema changes.
