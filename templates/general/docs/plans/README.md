# Implementation plans

This directory contains tracked implementation plans for {{PROJECT_NAME}}. Plans are part of the project documentation and must be committed with the work they describe.

Create a plan before implementation when work introduces a new feature, a product or technical update, a migration, a coordinated refactor, a cross-component change, or any other change that requires multiple ordered steps or explicit verification. A trivial single-file correction may proceed without a plan when its scope and verification are self-evident.

## Plan index

Name plans `NN-short-title.md`, assign numbers sequentially, and add every plan to this table before implementation begins.

| Plan | Outcome | Status | Depends on | Last updated |
| --- | --- | --- | --- | --- |
| [`NN-short-title.md`](NN-short-title.md) | <intended outcome> | Draft | None | YYYY-MM-DD |

Use these statuses: `Draft`, `Ready`, `In progress`, `Blocked`, `Deferred`, `Cancelled`, or `Complete`.

- `Draft`: scope or decisions are still being developed.
- `Ready`: prerequisites, boundaries, and definition of done are resolved.
- `In progress`: implementation or verification is active.
- `Blocked`: progress requires a recorded dependency, decision, or external action.
- `Deferred`: valid work intentionally postponed with a reason.
- `Cancelled`: the outcome is no longer required; retain the plan and record why.
- `Complete`: every definition-of-done item and required check has passed.

Update the table whenever a plan's status or dependency changes. Do not start a dependent plan until its prerequisites are complete unless the plan explicitly documents a safe exception.

## Execution rules

- Start from `.plan-template.md`.
- Read every listed prerequisite before editing.
- Resolve product and technical decisions in their source-of-truth documents before implementation.
- Update external contracts before or in the same change as code.
- Create forward migrations instead of editing applied migrations.
- Follow the plan's implementation order and preserve its stated boundaries.
- Update the plan when verified findings, scope, decisions, dependencies, or risks change. Keep a concise progress log for material transitions.
- If repository code contradicts a frozen plan decision, stop and resolve the contract or plan explicitly. Do not silently invent different behavior.
- Run every required quality gate and inspect the final diff before handoff.
- Record verification results and completion date before setting the plan and index entry to `Complete`.

Keep product, technical, API, architecture, integration, and operations documentation in the locations defined by `../README.md`. A plan is authoritative for how a specific change is scoped, sequenced, tracked, and verified, but it must not override those higher-level sources of truth.
