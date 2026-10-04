# Architecture decision records

Create one short ADR for a durable technical decision with meaningful alternatives, such as selecting or upgrading an engine, choosing the simulation clock, changing scene organization, adopting a rendering pipeline, defining save compatibility, selecting a networking model, or changing content and build tooling.

Name files `NNNN-short-title.md`, assign numbers sequentially, and start from `.adr-template.md`.

## Rules

- Record the game, platform, production, performance, and team constraints that made the decision necessary.
- State the decision precisely enough that gameplay, engineering, content, and release work can follow it.
- Capture rejected alternatives and the evidence or tradeoff that ruled them out.
- Describe consequences for runtime behavior, content production, save or network compatibility, target platforms, tooling, testing, and operations.
- Use `Proposed`, `Accepted`, `Superseded`, or `Deprecated` status.
- Never rewrite the history of an accepted ADR. Create a new ADR and link both records when a decision changes.
