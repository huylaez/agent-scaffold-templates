# Architecture documentation

Use this directory for component or cross-component architecture that is too detailed for `../TRD.md` but remains important for safe implementation.

Create a document only when it owns a stable architectural boundary. Typical examples include `backend.md`, `frontend.md`, `data-platform.md`, or a cross-domain data-flow document.

Each architecture document should cover:

- scope and relationship to the system described in `../TRD.md`;
- component responsibilities and code ownership;
- allowed dependency direction and forbidden coupling;
- important request, event, job, and persistence flows;
- failure modes, containment, retries, and recovery;
- extension points and conditions that require architectural review;
- links to relevant contracts and ADRs.

Do not duplicate product requirements, exact API schemas, implementation tasks, or runbook steps. Link to `../PRD.md`, `../api-contract.md`, `../plans/`, or `../operations/` respectively.
