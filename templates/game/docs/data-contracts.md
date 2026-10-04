# Game Data Contracts

**Version:** 1  
**Status:** Draft  
**Owners:** <system and content owners>

This document is the source of truth for data that persists across sessions, crosses system or process boundaries, or is authored outside the consuming runtime code.

## 1. Conventions

Define identifiers, version fields, units, coordinate systems, time representation, numeric precision, enum evolution, optional and nullable fields, default behavior, validation, unknown-field handling, checksums, compression, and maximum sizes.

Never rely on an engine serializer's current output as an implicit long-term contract.

## 2. Contract inventory

| Contract | Producer | Consumer | Storage or transport | Version | Compatibility policy |
| --- | --- | --- | --- | --- | --- |
| <save profile> | <system> | <system> | <location> | <version> | <policy> |

Include save games, player settings, replays, authored content, downloadable content, gameplay events, analytics events, mod data, and network messages when applicable.

## 3. Contract definition

Create one section per contract.

### <Contract name>

**Owner:** <system or team>  
**Current version:** <version>  
**Compatibility window:** <supported versions>  
**Size or frequency budget:** <budget>

```json
{
  "version": 1,
  "field": "<verified example>"
}
```

| Field | Type | Required | Constraints | Default | Meaning |
| --- | --- | --- | --- | --- | --- |
| `version` | integer | Yes | Positive | None | Schema version |
| `field` | string | Yes | <constraints> | None | <meaning> |

Document invariants, ownership, lifecycle, ordering, validation, failure behavior, and security or trust assumptions.

## 4. Save and settings behavior

Define save triggers, slots, atomic-write strategy, backup, corruption recovery, cloud conflicts, partial progress, reset, deletion, downgrade behavior, and privacy requirements.

## 5. Migration and compatibility

- Never edit or reinterpret a released version without an explicit compatibility decision.
- Use forward migrations and retain fixtures for every supported input version.
- Define unsupported, corrupt, future, missing, and partially migrated data behavior.
- Test migration idempotency and interruption recovery when migration writes data.
- Coordinate breaking network, replay, mod, or downloadable-content changes across every producer and consumer.

## 6. Contract verification checklist

- [ ] Every producer and consumer uses the documented version and units.
- [ ] Required, optional, defaulted, and unknown fields behave as documented.
- [ ] Bounds and malformed input are tested.
- [ ] Supported historical fixtures load and produce the expected state.
- [ ] Corrupt and unsupported inputs fail safely with player-appropriate recovery.
- [ ] Size, frequency, privacy, and trust constraints are verified.
