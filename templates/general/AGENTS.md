# Repository guide

## Working agreement

- Start with `docs/README.md` to find the source-of-truth document and the correct place to create or update documentation.
- Read `docs/PRD.md` for product scope, `docs/TRD.md` for architecture and technical constraints, and `docs/api-contract.md` for public interfaces. The API contract is the integration source of truth.
- Before implementing a new feature, a product or technical update, a migration, a coordinated refactor, or any other change that needs multiple ordered steps, create a tracked plan under `docs/plans/` from `docs/plans/.plan-template.md`. Add it to `docs/plans/README.md` and set its initial status before editing implementation code.
- Keep the plan and its index entry current as work progresses. Record scope or decision changes, dependencies, blockers, verification results, and the completion date. Do not mark a plan complete until its definition of done and required checks are satisfied.
- Keep each change inside the component or domain that owns the behavior. Put shared code only in the shared area identified by `docs/TRD.md`, and keep external-system adapters at explicit integration boundaries.
- For a feature, create or update its API-group documentation by following `docs/api/README.md`; update the API contract when an external interface changes; add an ADR for a durable technical decision; update the relevant integration or operations guide when a workflow, configuration, service, or runbook changes.
- For a bug, add or update a regression test. Update API-group documentation when client-visible behavior changes. Update product or technical documents only when expected behavior, a contract, an architectural decision, or an operational procedure changes.
- Data-model changes require a forward migration. Breaking contract changes require a new version or an explicitly coordinated migration for every consumer.
- Before handoff, run the formatter, linter, type checker, tests, and build commands documented in `README.md`. Report any check that could not be run.
- Never commit credentials, private data, or generated artifacts. Preserve existing user work and keep changes focused and reviewable.
- Use English for source code, comments, documentation, file names, configuration, and commit messages.
