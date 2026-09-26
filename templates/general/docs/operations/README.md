# Operations documentation

This directory contains executable procedures for running {{PROJECT_NAME}}. Create separate documents for local development, each deployed environment, routine maintenance, data recovery, and incident response as needed.

## Rules

- Write commands that can be copied safely and identify the directory and environment in which they run.
- List prerequisites, required access, configuration sources, and expected outputs.
- Never include real secrets. Refer to the approved secret-management mechanism.
- Include pre-deployment checks, migrations, deployment order, health verification, observability, and rollback.
- Mark destructive or irreversible steps clearly and add a confirmation or backup step.
- Keep architecture rationale in `../TRD.md` or an ADR; keep exact interface behavior in `../api-contract.md`.
- Update the relevant procedure in the same change as new configuration, services, dependencies, migrations, alerts, or recovery steps.

## Runbook template

Every runbook should contain:

1. purpose and scope;
2. prerequisites and access;
3. configuration and safety checks;
4. ordered procedure;
5. verification and expected signals;
6. rollback or recovery;
7. troubleshooting and escalation.
