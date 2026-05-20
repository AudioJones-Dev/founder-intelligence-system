# Source Archive

Original source material used to bootstrap the Founder Intelligence System.

## Contents

- `strategic-intelligence-system.zip` — the original archive provided at repo bootstrap. Contains the predecessor "Strategic Intelligence System" library with terminology `primitives → frameworks → skills`, which was normalized into the canonical FIS terminology `skills → frameworks → agents` during the bootstrap commit.
- `STRATEGIC-INTELLIGENCE-SYSTEM.md` — the README of the original archive, preserved for traceability.

## Why This Is Preserved

The original archive is kept as evidence of provenance — it lets future readers verify what was inherited, what was renamed, and what was added during the bootstrap normalization.

## What Was Renamed

| Source name | Canonical name | Reason |
|---|---|---|
| `primitives/` | `skills/` | The canonical FIS structure calls atomic capabilities "skills" |
| `skills/` (workflow routers) | `agents/` | The canonical FIS structure calls workflow routers "agents" |
| `outputs/` | `templates/` | The canonical FIS structure calls reusable document structures "templates" |
| `absence-detection` | `ghost-note-detection` | The musical "ghost notes" framing was the more evocative canonical name; the original ID is preserved as an alias |
| `moat-detection-skill` (id) | `moat_detection_agent` (id) | Workflow router → agent |
| `transcript-synthesis-skill` (id) | `transcript_synthesis_agent` (id) | Workflow router → agent |
| `router.schema.json` | `routing.schema.json` | Canonical naming |
| `primitive.schema.json` | `skill.schema.json` | Primitives → skills |

## What Was Added

- `doctrine/` layer (5 new files)
- `ontology/` layer (2 new files)
- New canonical examples per the bootstrap spec: `skills/decision-compression.md`, `skills/moat-detection.md`, `frameworks/signal-audit-framework.md`, `frameworks/founder-prediction-error-model.md`
- Schemas: `ontology.schema.json`, `agent.schema.json`, `doctrine.schema.json`
- Templates: `skill-template.md`, `framework-template.md`, `doctrine-template.md`
- Meta: `system-map.md`, `routing.md`
- Root files: `README.md`, `CONTRIBUTING.md`, `LICENSE`, `.gitignore`
