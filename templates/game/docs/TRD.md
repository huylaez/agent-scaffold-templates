# Technical Requirements Document — {{PROJECT_NAME}}

**Version:** 0.1 (draft)  
**Companion to:** `GDD.md`, `data-contracts.md`

## 1. Runtime architecture

Describe the runtime boundary and the flow from input through simulation, presentation, persistence, and platform services.

```text
input -> simulation -> presentation
             |             |
             v             v
        persistence    audio / rendering
             |
             v
       platform services
```

State the rules for dependency direction, ownership, lifetime, update order, and communication between systems.

## 2. Engine, tools, and versions

| Area | Selection | Version | Constraint or reason |
| --- | --- | --- | --- |
| Engine | <engine> | <version> | <constraint> |
| Language and runtime | <selection> | <version> | <constraint> |
| Content tools | <tools> | <versions> | <constraint> |
| Build toolchain | <toolchain> | <version> | <constraint> |

Pin versions required for reproducible imports and builds. Document the approved upgrade process.

## 3. Target platforms and configurations

For each supported platform, define minimum and target hardware, operating-system range, input devices, display modes, storage, network assumptions, and platform SDK requirements.

## 4. Project structure and ownership

For each module, plugin, package, scene group, or domain, document:

- responsibility and source location;
- owned runtime state and content;
- allowed dependencies and forbidden coupling;
- initialization, update, pause, teardown, and failure behavior;
- technical and content owner.

Shared code must contain only cross-cutting technical concerns. Platform and third-party integrations belong behind explicit adapters.

## 5. Simulation model

Define time sources, fixed and variable update responsibilities, ordering, determinism requirements, random-number ownership, pause behavior, replay requirements, backgrounding, and slow-frame behavior.

## 6. World, scene, and object lifecycle

Document scene or world partitioning, object ownership, spawning and despawning, pooling, streaming, loading transitions, persistence across transitions, and cleanup invariants.

## 7. Data and compatibility

Summarize runtime state, authored content, settings, save games, replays, and network state. Put exact formats, versioning, migration, validation, and rejection behavior in `data-contracts.md`.

## 8. Performance budgets

Record the measurement scene, target hardware, build configuration, tooling, and warm-up procedure for every budget.

| Area | Target | Hard limit | Measurement |
| --- | --- | --- | --- |
| Frame time | <CPU and GPU target> | <limit> | <profiler and scenario> |
| Memory | <target> | <limit> | <tool and lifecycle point> |
| Loading | <target> | <limit> | <transition and storage> |
| Package size | <target> | <limit> | <platform artifact> |
| Network | <bandwidth or latency> | <limit> | <scenario> |

## 9. Rendering, audio, physics, and input

Document selected pipelines, quality tiers, collision layers, audio buses, input abstraction, device switching, and platform fallbacks. Link to architecture documents for subsystem detail.

## 10. Online, multiplayer, and trust boundaries

When applicable, define authority, session lifecycle, matchmaking, validation, replication, ordering, prediction, reconciliation, latency tolerance, disconnect recovery, anti-cheat assumptions, authentication, and abuse controls. Write `Not applicable` otherwise.

## 11. Build and release architecture

Define environments, build variants, feature flags, signing boundaries, content packaging, version numbering, reproducibility, crash reporting, telemetry, rollout, and rollback. Put executable procedures in `operations/`.

## 12. Testing and quality gates

List required unit, simulation, integration, save-migration, content-validation, playtest, performance, soak, compatibility, and platform checks. Keep exact commands in the root `README.md` and procedures in `testing/`.

The definition of done for a behavior change is:

- player-facing intent and system rules agree with the implementation;
- required data migrations and compatibility behavior are complete;
- regression coverage or a repeatable playtest exists;
- affected target builds succeed;
- relevant performance budgets remain satisfied;
- required quality gates and smoke paths pass.

## 13. Security, privacy, and compliance

Document untrusted inputs, secrets, platform credentials, player data, telemetry consent, retention, child-safety or rating constraints, dependency risks, mod boundaries, and distribution requirements.

## 14. Decisions still needed

| Decision | Owner | Evidence needed | Needed by | Status |
| --- | --- | --- | --- | --- |
| <decision> | <owner> | <benchmark or prototype> | <milestone> | Open |
