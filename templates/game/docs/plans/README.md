# Implementation plans

This directory contains tracked implementation plans for {{PROJECT_NAME}}. Plans are durable project records and must be committed with the work they describe.

Create a plan before implementation when work introduces a gameplay capability, changes player-facing rules, adds a content pipeline, changes persisted or networked data, affects multiple systems, targets a new platform, changes performance architecture, requires a migration, or otherwise needs ordered implementation and verification. A trivial correction may proceed without a plan when its scope and verification are self-evident.

## Plan index

Name plans `NN-short-title.md`, assign numbers sequentially, and add every plan to this table before implementation begins.

| Plan | Playable or technical outcome | Status | Depends on | Last updated |
| --- | --- | --- | --- | --- |
| [`NN-short-title.md`](NN-short-title.md) | <intended outcome> | Draft | None | YYYY-MM-DD |

Use these statuses: `Draft`, `Ready`, `In progress`, `Blocked`, `Deferred`, `Cancelled`, or `Complete`.

- `Draft`: scope, design, evidence, or decisions are still being developed.
- `Ready`: prerequisites, ownership, budgets, contracts, and definition of done are resolved.
- `In progress`: implementation, content production, or verification is active.
- `Blocked`: progress requires a recorded dependency, decision, asset, platform capability, or external action.
- `Deferred`: valid work intentionally postponed with a reason.
- `Cancelled`: the outcome is no longer required; retain the plan and record why.
- `Complete`: every definition-of-done item, target build, and required verification has passed.

## Execution rules

- Start from `.plan-template.md` and read every listed prerequisite before editing.
- Resolve game-design, technical, data-contract, and content-pipeline decisions in their source-of-truth documents before implementation.
- Record the owning gameplay system, target platforms, compatibility boundary, performance budgets, and representative verification scenarios.
- Use forward migrations for released persisted data and retain historical fixtures.
- Keep code, content, editor tooling, tests, builds, and playtests ordered so intermediate states are safe and reviewable.
- Update the plan when verified findings, scope, design, dependencies, risks, or target-platform results change.
- Run every required quality gate, inspect the final diff, build affected targets, and complete the specified smoke or playtest path.
- Record commands, build identifiers, configurations, devices, results, evidence, and completion date before setting the plan to `Complete`.

A plan defines how one change is delivered, but it must not override the GDD, TRD, data contracts, gameplay-system rules, content pipeline, or an accepted ADR.
