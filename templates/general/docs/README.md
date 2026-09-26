# Documentation map

| Need | Read or update |
| --- | --- |
| Product scope, outcomes, users, and exclusions | `PRD.md` |
| System architecture, data model, and technical constraints | `TRD.md` |
| Public APIs, events, commands, files, and cross-system schemas | `api-contract.md` |
| Implemented API-group reference | `api/README.md` |
| Cross-system workflows and consumer responsibilities | `integration/README.md` |
| Durable technical decisions and their rationale | `adr/` |
| Local or cross-component architecture detail | `architecture/` |
| Configuration, deployment, maintenance, and incident procedures | `operations/` |
| Tracked implementation plans, dependencies, progress, and completion status | `plans/README.md` |

## Source-of-truth rules

- Do not duplicate the PRD or TRD in lower-level documents. Link to them and add only the detail owned by the lower-level document.
- Keep `api-contract.md` authoritative for external schemas and behavior. API-group and integration guides must agree with it.
- Keep API-group documents focused on behavior verified from the implementation.
- Use ADRs for decisions that must remain understandable after the implementation changes.
- Use operations documents for procedures, not architecture rationale.
- Treat files under `plans/` as durable project records for implementation scope, order, dependencies, status, and verification. They must link to higher-level sources of truth rather than redefining product, contract, or architecture decisions.

When two documents disagree, stop and resolve the conflict in the highest-level source of truth before changing implementation.
