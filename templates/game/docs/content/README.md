# Content pipeline

This directory documents how art, animation, audio, narrative, level, localization, and gameplay-data assets move from source files into runtime-ready content.

## Content inventory

| Content type | Source location | Runtime location | Owner | Tool and version |
| --- | --- | --- | --- | --- |
| <type> | <path or system> | <path> | <owner> | <tool> |

## Required rules

- Define naming, directory ownership, units, scale, axes, pivots, color space, sample rates, and export settings for every relevant content type.
- Separate editable source assets from imported or generated runtime artifacts. State which files are authoritative and which may be regenerated.
- Preserve engine metadata, stable identifiers, references, and import relationships. Move or rename assets only through a safe tool or a verified repository procedure.
- Record asset provenance, license, attribution, modification rights, and redistribution restrictions. Do not add content whose project use is unclear.
- Pin tools and importer versions when their output affects reproducibility. Review import-setting changes as runtime changes.
- Define validation and preview steps before content is accepted. Detect missing references, invalid naming, unsupported formats, and budget violations automatically where practical.

## Budgets

Define budgets per target platform and representative scene, not as context-free global numbers.

| Content type | Runtime budget | Storage budget | Streaming or concurrency limit | Measurement |
| --- | --- | --- | --- | --- |
| Texture | <memory> | <package size> | <limit> | <tool and scene> |
| Mesh or geometry | <runtime cost> | <package size> | <limit> | <tool and scene> |
| Animation | <runtime cost> | <package size> | <limit> | <tool and scene> |
| Audio | <memory or voices> | <package size> | <limit> | <tool and scene> |

## Platform overrides

Document compression, quality tiers, fallback assets, downloadable content, localization packaging, and platform-specific import or memory constraints.

## Change checklist

- [ ] Source and runtime ownership are clear.
- [ ] License and attribution are recorded.
- [ ] Naming, format, and import settings conform.
- [ ] References and metadata remain valid.
- [ ] Target-platform budgets are measured.
- [ ] The asset is verified in a representative playable scenario.
