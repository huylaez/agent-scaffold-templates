# Game Design Document — {{PROJECT_NAME}}

**Version:** 0.1 (draft)  
**Owner:** <name or team>  
**Status:** Draft

## 1. High concept

Describe the game in one sentence: player role, primary action, distinctive constraint, and desired fantasy.

## 2. Audience and platforms

| Audience | Need or motivation | Play context | Target platform |
| --- | --- | --- | --- |
| <audience> | <motivation> | <session context> | <platform> |

Document input methods, expected session length, age or content rating goals, languages, and accessibility assumptions.

## 3. Design pillars

Define three to five testable principles that guide tradeoffs. For each pillar, include what supports it and what would violate it.

## 4. Player fantasy and experience goals

Describe what the player should understand, feel, and master from first contact through long-term play. Separate intended challenge from accidental friction.

## 5. Core loop

```text
<observe> -> <decide> -> <act> -> <receive feedback> -> <progress or recover>
```

Define the actions, resources, feedback, failure recovery, and reasons to repeat the loop.

## 6. Game structure and progression

Document sessions, levels or runs, progression layers, unlocks, difficulty curve, checkpoints, completion conditions, fail states, and replay incentives.

## 7. Gameplay capabilities

### G1 — <Capability>

- **Player intent:** <what the player is trying to accomplish>
- **Rules:** <observable rules and constraints>
- **Feedback:** <visual, audio, haptic, and UI response>
- **Failure and recovery:** <what can go wrong and how play resumes>
- **Acceptance:** <repeatable player-visible outcome>

Add one section per capability and keep identifiers stable so system documents and plans can reference them.

## 8. Controls and camera

Define actions rather than physical buttons first. Then document default mappings, remapping, device changes, input buffering, dead zones, camera behavior, pause semantics, and accessibility alternatives.

## 9. Economy and balance

Document sources, sinks, currencies, rewards, costs, tuning ownership, anti-exploit constraints, difficulty variables, and the evidence used to evaluate balance. Write `Not applicable` when the game has no economy.

## 10. Content and presentation

Describe required content types, visual and audio direction, narrative delivery, UI principles, content density, and reuse strategy. Link to the content pipeline instead of duplicating import rules.

## 11. Accessibility and player safety

Define requirements for readable presentation, input alternatives, motion and flashing controls, audio alternatives, difficulty assistance, privacy, moderation, and age-appropriate behavior as applicable.

## 12. Success metrics

| Metric | Target | Measurement method | Guardrail |
| --- | --- | --- | --- |
| <metric> | <target> | <playtest or telemetry method> | <unwanted outcome to avoid> |

Do not collect telemetry until consent, privacy, retention, and access requirements are documented.

## 13. Scope and milestones

Define prototype, vertical slice, alpha, beta, and release outcomes as applicable. Each milestone needs entry criteria and a playable completion condition; task tracking belongs in `plans/`.

## 14. Non-goals

- State explicitly what the current version will not support.

## 15. Open design questions

| Question | Owner | Evidence needed | Needed by | Status |
| --- | --- | --- | --- | --- |
| <question> | <owner> | <prototype or playtest> | <milestone> | Open |
