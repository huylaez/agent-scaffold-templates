# API group documentation

This directory contains the implemented API reference, organized by the grouping used by the implementation, such as an OpenAPI tag, RPC service, command family, or event topic.

## Rules

- Keep exactly one `<group>.md` document for every implemented API group.
- Create group documents from `.api-template.md`.
- List every group document in the index below.
- Create or update the document in the same change as a request or response schema, authentication rule, status or error response, side effect, pagination, ordering, or other client-visible behavior.
- Verify every detail from implementation. Keep documents aligned with `../api-contract.md`; resolve disagreements instead of documenting conflicting behavior.
- Remove obsolete details and never duplicate an interface across group documents.

## API groups

| Implementation group | Document |
| --- | --- |
| `<group>` | [`<group>.md`](<group>.md) |

Add a row when adding a group. Remove a row only after the group no longer exists.
