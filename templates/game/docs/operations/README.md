# Build and release operations

This directory contains executable procedures for producing, validating, distributing, and recovering builds of {{PROJECT_NAME}}.

Create separate runbooks for local setup, development builds, release builds, content delivery, each target platform, signing, store submission, staged rollout, rollback, and crash response as needed.

## Rules

- Pin the engine, SDK, compiler, content tool, plugin, and platform-service versions needed for reproducible builds.
- Identify the working directory, environment, credentials boundary, configuration source, expected outputs, and artifact locations for every command.
- Never include real secrets, signing keys, player data, or private store credentials. Refer to the approved secret-management mechanism.
- Define version numbering for executable code, content, data contracts, and network compatibility.
- Include clean-build requirements, content validation, tests, target-device smoke checks, symbol generation, signing, packaging, and artifact checksums.
- Record rollout, health signals, compatibility constraints, store or platform review requirements, and a safe rollback or disable path.
- Mark destructive, irreversible, or player-data-affecting steps clearly and require a backup or confirmation.

## Runbook template

Every runbook should contain:

1. purpose, target platform, build type, and scope;
2. prerequisites, access, pinned tools, and clean-state requirements;
3. configuration, versioning, content, and safety checks;
4. ordered build, package, sign, upload, or release procedure;
5. automated verification and target-device smoke path;
6. expected artifacts, symbols, logs, and provenance;
7. rollout monitoring, rollback, or recovery;
8. troubleshooting and escalation.
