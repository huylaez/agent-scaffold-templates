# AGENTS.md

## Purpose

This repository contains **{{PROJECT_NAME}}**. Agents should optimize for correctness, clarity, and small reviewable changes.

## Working agreement

- Read `README.md` and the relevant files in `docs/` before making changes.
- Keep implementation and documentation synchronized.
- Prefer the smallest change that fully solves the requested problem.
- Preserve existing user work and avoid unrelated refactors.
- Never commit credentials, tokens, private keys, or local environment files.
- Ask before taking destructive or externally visible actions.

## Delivery standard

- Add or update tests for behavior changes.
- Run the relevant formatter, linter, type checker, and test suite.
- Report what changed, what was verified, and any remaining risk.
- Use English for source code, comments, documentation, and commit messages.

## Project documents

- `docs/PRD.md`: product goals, users, scope, and acceptance criteria.
- `docs/TRD.md`: technical requirements and operational constraints.
- `docs/ARCHITECTURE.md`: system boundaries, components, and important decisions.
- `docs/TASKS.md`: executable work items and current progress.

Update these documents when a decision changes their truth, not as an afterthought.
