# Architecture documentation

Use this directory for stable runtime or toolchain architecture that is too detailed for `../TRD.md`. Typical subjects include simulation, world streaming, rendering, audio, input, UI, persistence, multiplayer, editor tooling, and build pipelines.

Each architecture document should cover:

- scope and relationship to the GDD and TRD;
- component responsibilities, lifetimes, and code or content ownership;
- allowed dependency direction and forbidden coupling;
- initialization, update order, communication, pause, teardown, and failure behavior;
- data ownership, serialization boundaries, and relevant contracts;
- performance budgets, measurement scenarios, and degradation behavior;
- extension points and conditions that require architectural review;
- links to relevant gameplay systems, data contracts, plans, and ADRs.

Do not duplicate player-facing rules, exact schemas, implementation tasks, playtest procedures, or release runbooks. Link to their authoritative documents.
