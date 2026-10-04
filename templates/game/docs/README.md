# Documentation map

| Need | Read or update |
| --- | --- |
| Game vision, pillars, player experience, core loop, progression, and scope | `GDD.md` |
| Engine, architecture, runtime constraints, platform targets, and performance budgets | `TRD.md` |
| Save, replay, configuration, content, event, and network schemas | `data-contracts.md` |
| Rules, state transitions, tuning boundaries, and ownership for gameplay systems | `gameplay/README.md` |
| Asset creation, import, naming, licensing, and runtime budgets | `content/README.md` |
| Automated quality gates, playtests, compatibility coverage, and performance evidence | `testing/README.md` |
| Stable component and runtime architecture below the TRD | `architecture/` |
| Build, packaging, release, rollback, and platform procedures | `operations/` |
| Durable technical decisions and their rationale | `adr/` |
| Tracked implementation plans, dependencies, progress, and completion status | `plans/README.md` |

## Source-of-truth rules

- Keep player-facing intent and observable game rules in the GDD or the owning gameplay-system document.
- Keep technical boundaries and measurable budgets in the TRD. Architecture documents may add detail but must not contradict it.
- Keep serialized and cross-boundary formats authoritative in `data-contracts.md`; code, fixtures, importers, and migrations must agree with it.
- Keep content procedures in `content/`, verification procedures in `testing/`, and executable build or release procedures in `operations/`.
- Use ADRs for decisions that must remain understandable after the implementation changes.
- Treat plans as durable records of scope, order, dependencies, status, and verification. Plans link to higher-level sources of truth instead of redefining them.

When documents disagree, stop and resolve the conflict in the highest-level source of truth before changing implementation.
