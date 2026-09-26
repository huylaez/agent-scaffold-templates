# Architecture decision records

Create one short ADR for a durable decision with meaningful alternatives, such as changing a data store, job system, authentication boundary, external provider, deployment topology, or cross-component interface.

Name files `NNNN-short-title.md`, assign numbers sequentially, and start from `.adr-template.md`.

## Rules

- Record context and constraints that made the decision necessary.
- State the decision precisely enough that future work can follow it.
- Capture rejected alternatives and why they lost.
- Describe positive and negative consequences, migration, and rollback implications.
- Use `Proposed`, `Accepted`, `Superseded`, or `Deprecated` status.
- Never rewrite the history of an accepted ADR. Create a new ADR and link both records when a decision changes.
