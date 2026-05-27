# Leviathan Lore

This repository is the master reference library for the Leviathan fictional universe. It is organized as a codex line rather than a wiki. Each codex volume should stand on its own as a usable reference text for game developers, fiction writers, and dedicated readers.

## Core Doctrine

- Golden rule: that math holds. Outside explicit FTL exceptions, claims about scale, travel, production, logistics, violence, and survival should obey internally consistent constraints.
- Every lore volume uses a dual voice: diegetic presentation first, Author Notes second.
- History is layered into four strata: Eldritch Layer, Hyborean Era, Ancient History, and Modern Times. These are narrative layers primarily, with implied ordering historically.

## Repository Layout

- `codex/` contains sellable, stand-alone lore volumes and appendices.
- `meta/` contains editorial doctrine and repository process.
- `templates/` contains the house manuscript format for new codex volumes.

## Working Method

- Add lore as codex volumes, appendices, or clearly bounded sections, not as scattered wiki pages.
- Prefer subject-focused documents that can be read on their own and cross-reference related volumes.
- Use AI primarily to organize material, maintain structure, and indicate where user-provided content should be placed.
- Use the four historical layers as organizing checkpoints in breakdowns and Author Notes so each lore element states which layer it primarily serves.
- Refactor structure roughly every 50 lore commits so categories, file boundaries, and cross-references stay coherent.
- When lore changes affect related documents, update those cross-references, companion volumes, appendices, and process notes in the same pass when practical.
- Do not defer obvious cascading documentation updates merely because a scheduled refactor pass has not yet happened.
- Preserve a consistent internal structure so documents can later be compiled, sold, or handed to downstream developers.

## AI Usage Policy

- AI may be used for organizational work, documentation support, and other non-editorial support tasks.
- AI may serve as a ghostwriter for editorial content when the user explicitly requests that help.
- AI-generated content should be documented in `AI_USAGE.LOG` when it adds canon-facing or editorial substance beyond pure organization, formatting, calculation, or maintenance.
- Non-editorial support tasks such as measurements, calculations, organizational help, or suggested random names are not editorial contributions by themselves.
- If a requested contribution may be editorial in nature, warn the user and ask permission before generating it.

## Current Core Volumes

- `CX-000` defines the setting doctrine that measurable claims must survive contact with arithmetic.
- `CX-001` defines the four historical layers of the setting.
- `CX-002` defines how the setting distinguishes hard record, reconstruction, legend, and contaminated evidence.
- `CX-003` establishes the broad nature of the galaxy, from Terran origin uncertainty to the present imperial order.
- `CX-004` defines the Imperial Throne, the Galactic Constitution, and the doctrine of managed fracture.
- `CX-005` defines the Wardens, the thirty-one clans, and the tripartite fleet order.
- `CX-006` defines campaigns of rediscovery, territorial integration, and the role of the Imperial Survey Corps.
- `CX-007` defines the automated industrial order, ATECs, and megacorporate manufacturing power.
- `CX-008` defines the Great War of the Capitals, the Monastery, and the lost military inheritance of the mythic age.
- `CX-009` defines the Silence, erasure sites, ghost signals, sealed vaults, and the Blank Centuries.
- `CX-010` defines science, survey, anomaly response, and recovery operations in the modern empire.
- `CX-011` defines coalition charters, Prizetts, and temporary Warden alliances under House service.
- `CX-012` defines campaign closure, Imperial settlement, pressed claims, and continuity between campaigns.
- `CX-013` begins the FTL rewrite by defining Conventional Space, Hyperspace, Jump Space, and the starter-gate campaign doctrine.
- `CX-014` defines Power Generation via Compact Dimensional Acceleration Packs (CDAP).
- `CX-015` defines Defensive and Offensive Systems, including shields, armor, weapon vectors, and the Valid Firing Solution (VFS).
- `CX-016` defines Thermal Management and Heat Rejection, establishing Thermal Batteries as a vessel's primary "Hit Points."
- `CX-999` defines the USO Unified Starship Building Codes, establishing structural standards, SCU metrics, and the layered hull construction doctrine.

## System Codices

- `Master Skill Codex` defines the suites, ranks, and progression for pilot and crew skills.
- `The Leviathan Parts Catalog` provides the authoritative registry of standardized ship hulls and class-based components.
- `The Leviathan Module Codex` defines ship module standards, slot types, and facility grouping requirements.

## Appendices

- `AX-001` records the major houses and their broad institutional identities.
- `AX-002` records the lesser houses and their liege relationships.
- `AX-003` records the territory-to-region-to-survey-sector-to-system hierarchy, fixes the survey sector as the default frontier fiefdom unit, and fixes T0 as the canonical Throne territory map.
- `AX-004` records the current CHJ calibration hull set, fixes SDF-1 Macross as the reference ship, and defines the volume-normalized mass baseline used for cross-franchise FTL comparison.
- `AX-005` provides the detailed component list, dimensions, and power requirements for FTL engines across all scale classes.
- `AX-006` (In-Progress) establishes the CDAP Power System Calibration and unit-level efficiency curves.

## Legacy Integration

- Compatible legacy lore is being migrated into codex volumes as it is reconciled with current canon.
- The dedicated FTL rewrite is now in progress through `CX-013`; legacy FTL files remain reference-only until their contents are explicitly reincorporated into current codex volumes.
- See `meta/LEGACY-INTEGRATION-STATUS.md` for the current integration and deferral record.