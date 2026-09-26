# Technical Requirements Document — {{PROJECT_NAME}}

**Version:** 0.1 (draft)
**Companion to:** `PRD.md`, `api-contract.md`

## 1. System architecture

Describe the system boundary and include a compact diagram of users, components, data stores, and external systems. State the most important boundary rules explicitly.

```text
<client> -> <application> -> <data store>
                   |
                   +-> <external system>
```

## 2. Platform and technology decisions

List the selected runtimes, frameworks, persistence systems, deployment targets, and version constraints. Explain constraints that future changes must preserve.

## 3. Components and ownership

For each component or domain, document:

- responsibility and code location;
- inputs, outputs, and owned data;
- allowed dependencies and forbidden coupling;
- failure behavior and operational owner.

Shared code must contain only cross-cutting technical concerns. External providers belong behind explicit adapters.

## 4. Data model and lifecycle

Document entities, ownership, invariants, indexes, retention, deletion, backup, and recovery. Schema changes require forward migrations; never rewrite a migration that may already have been applied.

## 5. Interfaces and workflows

Summarize the important request, event, job, and file flows. Put exact external schemas and status or error behavior in `api-contract.md`, then link to them here.

## 6. Non-functional requirements

| Area | Requirement | Verification |
| --- | --- | --- |
| Performance | <target and percentile> | <load test or metric> |
| Reliability | <availability or recovery target> | <test or alert> |
| Security | <control> | <review or automated check> |
| Privacy | <retention or access constraint> | <audit or test> |
| Cost | <budget or scaling guardrail> | <report or alert> |

## 7. Security and trust boundaries

Describe authentication, authorization, sensitive data, input validation, secrets, abuse cases, dependency risks, and which components are trusted with each class of data.

## 8. Operations and observability

Define environments, configuration ownership, structured logs, metrics, traces, alerts, deployment, rollback, migrations, backups, and incident recovery. Put executable procedures in `operations/`.

## 9. Testing and quality gates

List required unit, integration, contract, end-to-end, migration, security, and performance checks. Keep the exact handoff commands in the root `README.md`.

The definition of done for a behavior change is:

- implementation and migration are complete;
- regression coverage exists at the appropriate boundary;
- source-of-truth contracts and affected guides agree with the code;
- required quality gates pass;
- the behavior is verified in the environment required by the PRD.

## 10. Decisions still needed

| Decision | Owner | Needed by | Status |
| --- | --- | --- | --- |
| <decision> | <owner> | <date or milestone> | Open |
