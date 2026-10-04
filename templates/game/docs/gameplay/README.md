# Gameplay system documentation

This directory contains the authoritative detailed rules for implemented gameplay systems. Create one document per independently understandable system from `.system-template.md` and list it below.

## System index

| System | Document | GDD capabilities | Owner |
| --- | --- | --- | --- |
| `<system>` | [`<system>.md`](<system>.md) | <G1> | <owner> |

## Rules

- Describe player-visible behavior and system invariants, not engine-editor instructions.
- Link every system to the relevant GDD capability and technical owner.
- Make state transitions, timing, priorities, resource ownership, failure, and recovery explicit.
- Identify tuning parameters and allowed ranges without scattering unexplained constants through code or assets.
- Define interactions with other systems and resolve ambiguous ownership before implementation.
- Update the system document with changes to rules, states, inputs, feedback, balance boundaries, or edge cases.
- Keep exact serialized schemas in `../data-contracts.md`, architecture detail in `../architecture/`, and task progress in `../plans/`.
