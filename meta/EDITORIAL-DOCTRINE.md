# Editorial Doctrine

This repository exists to produce codex volumes, not loose encyclopedia pages. The unit of authorship is the document, not the isolated fact.

## Required Shape For Lore Volumes

Every lore volume should contain the following sections in this order unless there is a strong reason to deviate:

1. Title and metadata.
2. Abstract.
3. Diegetic Record.
4. Analytical Breakdown.
5. Material Implications.
6. Cross-References.
7. Author Notes.

## Editorial Rules

- The diegetic portion explains the lore as an in-universe text, briefing, record, chronicle, or analysis.
- The Author Notes explain why the lore element exists, what it is for, what assumptions it depends on, and where the hard constraints are.
- The four historical layers should be used as checkpoints in Author Notes and, when useful, in Analytical Breakdown sections.
- Each lore element should identify its primary layer function and note secondary layer interactions only when they materially affect interpretation.
- Author Notes should explicitly call out any numerical assumptions, scale assumptions, or sanctioned hand-waves.
- FTL may be hand-waved when needed, but the knock-on effects around it should still be constrained and consistent.
- Contradictions should be managed by evidentiary status first, not by allowing every source equal weight.

## AI-Assisted Workflow

- AI should default to organization, structure, cross-references, and placement guidance rather than unsolicited canon generation.
- AI may ghostwrite editorial or canon-facing prose when the user explicitly asks for that support.
- Log AI-generated material in `AI_USAGE.LOG` when it introduces substantive canon-facing content beyond the user's direct request.
- Borderline cases require a warning and explicit user permission before generation.

## Factoring Rules

- Prefer one volume per major topic, doctrine, institution, region, era, or event cluster.
- Split a document when it stops reading like a coherent supplemental chapter and starts behaving like a dump of unrelated facts.
- Use appendices for tables, chronologies, ship classes, dynasties, and terminology that support a larger volume.
- Keep cross-references explicit so later compilations can create omnibus books without rewriting the base material.
- When a new lore element changes the meaning, scope, or assumptions of existing material, update the affected documentation in the same work pass when practical.
- Treat cascading documentation edits as normal maintenance work, not something reserved only for scheduled refactor passes.

## Maintenance Rules

- Keep related doctrine, templates, cross-references, and supporting appendices aligned as lore evolves.
- Make small cascading documentation edits immediately when the dependency is clear.
- Use refactor passes for larger restructures, not as an excuse to leave known documentation drift in place.

## Refactor Cadence

- Review the codex structure roughly every 50 lore commits.
- Merge redundant documents, split overgrown ones, and normalize naming at each refactor pass.
- Update the README and template when the house format changes.