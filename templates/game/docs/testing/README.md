# Testing and playtesting

Use automated tests for deterministic rules and stable boundaries. Use repeatable playtests for player experience, presentation, device behavior, and scenarios that cannot be automated reliably. Important changes often require both.

## Quality matrix

| Area | Automated coverage | Playtest or manual coverage | Required platform or configuration |
| --- | --- | --- | --- |
| Core loop | <suite> | <case> | <configuration> |
| Save and load | <suite and fixtures> | <case> | <configuration> |
| Input and pause | <suite> | <case> | <devices> |
| Performance | <benchmark> | <scenario> | <target hardware> |

## Automated checks

Document unit, simulation, integration, content-validation, migration, replay, network, performance, and build checks. Each check must state what it proves, its command or tool, fixtures, environment, and failure artifacts.

Prefer deterministic setup, explicit random seeds, controlled clocks, and assertions on observable outcomes. A flaky test is a defect; isolate and track it rather than silently retrying indefinitely.

## Playtest cases

Create a playtest record from `.playtest-template.md` when verification needs player interaction or target hardware. Give reusable cases stable identifiers and keep one-off session notes separate from authoritative expected behavior.

Every defect report should include:

- build identifier, commit or revision, configuration, platform, hardware, and input device;
- clean or migrated save state and relevant content version;
- exact setup and shortest reproduction steps;
- observed and expected result, frequency, severity, and recovery;
- screenshots, video, logs, profiler capture, crash identifier, or save fixture when available.

## Compatibility coverage

Maintain a project-specific matrix for supported platforms, hardware tiers, display modes, input devices, languages, save versions, network conditions, and account states. Define which combinations block a milestone or release.

## Performance evidence

Performance comparisons must use the same target hardware, build type, scene or replay, quality settings, warm-up, capture duration, and profiler. Record distributions or representative captures rather than a single favorable frame.

## Release smoke path

At minimum, verify install or launch, first-run flow, input, settings, the core loop, pause and resume, save and reload, scene or level transition, failure and retry, platform suspend and resume when relevant, and clean exit.
