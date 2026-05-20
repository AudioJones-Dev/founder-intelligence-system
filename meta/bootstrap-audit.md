# Bootstrap Audit

This document records the audit and decisions made during the v0.1 bootstrap of the Founder Intelligence System repository.

## Source

`strategic-intelligence-system.zip` — a predecessor library titled "Strategic Intelligence System" containing 27 files across `primitives/`, `frameworks/`, `skills/`, `schemas/`, `scoring/`, `outputs/`.

The original archive is preserved verbatim at `meta/source-archive/strategic-intelligence-system.zip` along with its original README at `meta/source-archive/STRATEGIC-INTELLIGENCE-SYSTEM.md`.

## Terminology Normalization

The source library used `primitives → frameworks → skills` to describe its layering, where:
- "Primitives" were atomic, content-agnostic capabilities
- "Frameworks" were composed strategic lenses
- "Skills" were workflow routers (i.e., agents in Claude Code / FIS canonical vocabulary)

The canonical FIS structure mandates `skills → frameworks → doctrine` plus a distinct `agents/` layer for workflow routers. The bootstrap therefore renamed:

| Source | Canonical | Reason |
|---|---|---|
| `primitives/` | `skills/` | Atomic capabilities = skills in canonical |
| `skills/` | `agents/` | Workflow routers = agents in canonical |
| `outputs/` | `templates/` | Reusable document structures = templates |
| `router.schema.json` | `routing.schema.json` | Canonical naming |
| `primitive.schema.json` | `skill.schema.json` | Type rename |
| `id: *_skill` (workflow) | `id: *_agent` | ID alignment with new type |
| `type: primitive` | `type: skill` | Frontmatter alignment |
| `type: skill` (workflow) | `type: agent` | Frontmatter alignment |
| `used_by_skills:` | `used_by_agents:` | Field alignment |
| `primitives_used:` | `skills_used:` (canonical), `primitives_used` kept as deprecated alias in schema | Backward-compatible |
| `absence-detection.md` (file) | `ghost-note-detection.md` | The "ghost notes" framing is more evocative and was already documented in the file's origin; original id preserved as alias |

## Files Ingested From Source

All 27 source files were ingested and placed:

### Primitives → Skills
- `primitives/absence-detection.md` → `skills/ghost-note-detection.md` (renamed, ghost-note framing promoted)
- `primitives/adaptive-tension-tolerance.md` → `skills/adaptive-tension-tolerance.md`
- `primitives/core-communication-protocol.md` → `skills/core-communication-protocol.md`
- `primitives/iterative-error-compression.md` → `skills/iterative-error-compression.md`
- `primitives/time-horizon-arbitrage.md` → `skills/time-horizon-arbitrage.md`

### Frameworks → Frameworks (preserved)
- `frameworks/complexity-compression-theory.md`
- `frameworks/curse-of-capability.md`
- `frameworks/decision-compression-systems.md`
- `frameworks/organizational-memory-infrastructure.md`
- `frameworks/simplicity-arbitrage.md`
- `frameworks/success-simulation-mapping.md`
- `frameworks/time-recovery-economics.md`

### Workflow Routers → Agents
- `skills/golden-opportunity-strategist.md` → `agents/golden-opportunity-strategist.md`
- `skills/moat-detection-skill.md` → `agents/moat-detection-agent.md`
- `skills/transcript-synthesis-skill.md` → `agents/transcript-synthesis-agent.md`

### Output Templates → Templates
- `outputs/framework-extraction-template.md` → `templates/framework-extraction-template.md`
- `outputs/market-thesis-template.md` → `templates/market-thesis-template.md`
- `outputs/opportunity-brief-template.md` → `templates/opportunity-brief-template.md`

### Scoring → Scoring (preserved)
- `scoring/golden-opportunity-score.md`
- `scoring/moat-strength-score.md`
- `scoring/timing-asymmetry-score.md`

### Schemas → Schemas (with renames)
- `schemas/primitive.schema.json` → `schemas/skill.schema.json` (with type, title, aliases field updates)
- `schemas/framework.schema.json` (extended to v1.2 with `skills_used`, `related_doctrine`)
- `schemas/router.schema.json` → `schemas/routing.schema.json` (with title update)
- `schemas/scoring.schema.json` (unchanged)
- `schemas/opportunity.schema.json` (unchanged)

### README + Archive
- `README.md` (source) → `meta/source-archive/STRATEGIC-INTELLIGENCE-SYSTEM.md`
- `strategic-intelligence-system.zip` → `meta/source-archive/strategic-intelligence-system.zip`

## Files Authored During Bootstrap (Not From Source)

### Doctrine (5 new)
- `doctrine/signal-doctrine.md`
- `doctrine/founder-intelligence-system.md`
- `doctrine/complexity-compression.md`
- `doctrine/simplicity-arbitrage.md`
- `doctrine/organizational-memory.md`

### Skills (2 new)
- `skills/decision-compression.md`
- `skills/moat-detection.md`

### Frameworks (2 new)
- `frameworks/signal-audit-framework.md`
- `frameworks/founder-prediction-error-model.md`

### Schemas (3 new)
- `schemas/ontology.schema.json`
- `schemas/agent.schema.json`
- `schemas/doctrine.schema.json`

### Templates (3 new)
- `templates/skill-template.md`
- `templates/framework-template.md`
- `templates/doctrine-template.md`

### Ontology (2 new)
- `ontology/README.md`
- `ontology/concept-graph.md`
- `ontology/taxonomy.md`

### Meta (3 new)
- `meta/system-map.md`
- `meta/routing.md`
- `meta/bootstrap-audit.md` (this file)
- `meta/source-archive/README.md`

### Root (5 new or rewritten)
- `README.md` (rewritten from stub)
- `LICENSE` (MIT)
- `CONTRIBUTING.md`
- `.gitignore`

### Placeholder READMEs (4 new)
- `prompts/README.md`
- `transcripts/README.md`
- `extractions/README.md`
- `research/README.md`
- `examples/README.md`

## Files Intentionally Left Untouched

- `meta/source-archive/STRATEGIC-INTELLIGENCE-SYSTEM.md` — preserved verbatim from source for provenance. It contains the original terminology (primitives/frameworks/skills) and refers to old filenames; these stale references are intentional, since the file documents what was inherited.
- `meta/source-archive/strategic-intelligence-system.zip` — original archive, preserved unmodified.

## Unresolved Ambiguities

None blocking. Notes for future:

1. **Doctrine vs framework overlap.** Some concepts (complexity compression, simplicity arbitrage, organizational memory) now exist at both doctrine and framework levels. This is intentional — the framework is the operational diagnostic, the doctrine is the worldview. Future revisions may sharpen the boundary further.
2. **Backward-compatible YAML aliases.** The schema currently accepts both `primitives_used` (deprecated) and `skills_used` (canonical) on frameworks. Future cleanup can remove `primitives_used` once all existing framework files are updated.
3. **Source framework YAML.** The seven source frameworks do not currently fill the `skills_used` field. Future passes should backfill it to make agent routing fully resolvable from frontmatter alone.

## Quality Pass Results

- All 8 JSON schemas validate as parseable JSON
- No stale `type: primitive` entries in `skills/`
- No stale `used_by_skills` fields in `skills/`
- No empty markdown files
- All file references updated except inside the preserved source archive

## Recommended Next PR Title

`add: founder intelligence ontology + agent routing graph`

A reasonable v0.2 contribution would populate the agent routing graph in `meta/routing.md` with full hand-off contracts, backfill `skills_used` on the seven source frameworks, and add the first concrete prompt templates in `prompts/`.

## Bootstrap Commit Message

```
chore: bootstrap founder intelligence system repository
```
