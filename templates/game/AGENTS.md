# Repository guide

## Working agreement

- Start with `docs/README.md` to find the source of truth for the area being changed.
- Read `docs/GDD.md` for player-facing intent, `docs/TRD.md` for technical boundaries and budgets, and `docs/data-contracts.md` before changing saved data, configuration, content schemas, gameplay events, replays, or network messages.
- Before implementing a feature, gameplay-system change, content-pipeline change, migration, coordinated refactor, or other multi-step change, create a tracked plan from `docs/plans/.plan-template.md`. Add it to `docs/plans/README.md` and keep its status, dependencies, findings, verification results, and completion date current.
- Keep implementation inside the system that owns the behavior. Create or update its document under `docs/gameplay/` when rules, state transitions, tuning boundaries, or player-visible behavior change.
- Preserve the game pillars, core loop, player promises, and explicit non-goals in the GDD. Resolve a design conflict there instead of silently changing the implementation contract.
- Treat frame time, memory, package size, loading time, and supported hardware as budgets. Measure changes on the target configuration defined in the TRD; do not claim a performance improvement without comparable evidence.
- Avoid unbounded work, blocking I/O, repeated asset loading, and avoidable allocation in per-frame or fixed-step paths. Keep simulation rules explicit about time source, update order, pausing, and determinism.
- Version persisted and externally exchanged data. A save, replay, configuration, content, or network schema change requires compatibility analysis, migration or rejection behavior, fixtures, and rollback considerations.
- Do not hand-edit binary assets or engine-generated files that require an editor or import tool. Preserve asset identifiers, metadata, references, and import relationships. Do not regenerate unrelated scenes, prefabs, maps, or serialized resources.
- New or changed assets must follow `docs/content/README.md`, including naming, ownership, source, license, import settings, platform overrides, and relevant size or runtime budgets.
- For multiplayer behavior, document authority, validation, trust boundaries, ordering, latency behavior, prediction or reconciliation, disconnects, retries, and abuse cases before implementation.
- A gameplay bug needs a regression test at the lowest useful boundary when automation is practical. Otherwise, add a repeatable playtest case with setup, actions, expected result, build, platform, and captured evidence.
- Before handoff, run the documented format, static-analysis, automated-test, and build checks. Complete the relevant smoke path or playtest and report every check that could not be run.
- Never commit credentials, private player data, licensed source assets that cannot be redistributed, local caches, generated builds, or crash dumps. Preserve existing user work and keep changes focused and reviewable.
- Use English for source code, comments, documentation, file names, configuration, and commit messages.
