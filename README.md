# Founder Intelligence System

> The canonical intelligence layer for founder cognition, organizational memory, signal detection, and strategic reasoning.

Founder Intelligence System (FIS) is a markdown-first, schema-first, ontology-first semantic substrate. It is the canonical source of truth for the doctrine, frameworks, skills, and agent routing logic that sit beneath future Audio Jones / AJ Digital systems.

The operating principle:

> **Complexity exists in the architecture. Not in the reading experience.**

---

## What This Is

A versioned, schema-validated, layered intelligence substrate that captures:

- **Skills** — atomic, reusable reasoning capabilities (`skills/`)
- **Frameworks** — composed strategic lenses applied to specific situations (`frameworks/`)
- **Doctrine** — the worldview, epistemology, and strategic philosophy (`doctrine/`)
- **Ontology** — the concept-relation graph (`ontology/`)
- **Schemas** — machine-readable JSON definitions for every layer (`schemas/`)
- **Agents** — workflow routers that compose skills and frameworks (`agents/`)
- **Templates, Scoring, Prompts, Transcripts, Extractions, Research, Examples** — the operational substrate

## What This Is Not

- Not an app, SaaS, or service
- Not a vector store, LangChain wrapper, or orchestration framework
- Not a Firebase/Docker/cloud project
- Not a frontend application
- Not a generic AI repo

This is the **semantic layer that operates above tooling**. Tools are interchangeable; the substrate is canonical.

## Why It Exists

In the AI era, the moat is not the model. It is the structured judgment, the encoded taste, the institutional memory, and the routing logic that compose raw capability into intelligence. FIS captures that layer as canonical, versioned, machine-readable knowledge — so future agents, products, and operators can compose against it.

---

## Repository Structure

```
founder-intelligence-system/
├── skills/         # Atomic reusable reasoning capabilities
├── frameworks/     # Multi-part operating models that compose skills
├── doctrine/       # Worldview, epistemology, strategic philosophy
├── ontology/       # Concept-relation graph and taxonomy
├── schemas/        # JSON schemas for every layer
├── agents/         # Workflow routers (agent definitions)
├── prompts/        # Reusable prompt templates
├── transcripts/    # Raw source transcripts
├── extractions/    # Structured outputs derived from transcripts
├── research/       # Supporting research notes and evidence
├── examples/       # Worked examples
├── templates/      # Reusable document templates (skill, framework, doctrine, brief)
├── scoring/        # Composite scoring rubrics
└── meta/           # System map, routing, governance, source archive
```

## The Layers, And How They Compose

```
Doctrine          (the worldview)
   ↓ informs
Frameworks        (composable strategic lenses)
   ↓ compose
Skills            (atomic reasoning capabilities)
   ↓ validated by
Schemas + Ontology
   ↓ orchestrated by
Agents + Prompts
   ↓ applied to
Transcripts → Extractions → Briefs
```

Each layer is independently useful and independently versioned. Each layer composes against the layer below it. Read `meta/system-map.md` for the full topology.

### Layer definitions

| Layer | What it is | What it is not | Examples |
|---|---|---|---|
| **Doctrine** | The worldview that frames *why* the other layers exist | Operational instructions | Signal Doctrine, Founder Intelligence System |
| **Frameworks** | Composed strategic lenses for specific situations | Atomic capabilities | Curse of Capability, Decision Compression Systems |
| **Skills** | Atomic, content-agnostic reasoning capabilities | Workflow routers | Ghost Note Detection, Iterative Error Compression |
| **Ontology** | The concept graph and relationships | A flat tag list | concept → relation → target triples |
| **Schemas** | Machine-readable definitions for each layer | Documentation | `skill.schema.json`, `framework.schema.json` |
| **Agents** | Workflow routers that compose skills and frameworks | Reasoning capabilities of their own | Golden Opportunity Strategist, Moat Detection Agent |
| **Prompts** | Reusable prompt templates | Agent definitions | per-use-case prompt skeletons |
| **Transcripts** | Raw source material | Frameworks | interview, podcast, call transcripts |
| **Extractions** | Structured outputs derived from transcripts | Raw text | claim inventories, signal maps |
| **Research** | Supporting evidence and source analysis | Doctrine | market scans, citations |
| **Templates** | Reusable document structures | Filled-in instances | skill template, opportunity brief template |
| **Scoring** | Composite rubrics that aggregate framework scores | Single framework scores | golden opportunity score, moat strength score |
| **Meta** | System maps, routing, governance | Layer content itself | this README, system-map, source archive |

---

## How AI Agents Should Use This Repo

1. **Start with `meta/system-map.md`** — that file is the entry point for any agent that needs to orient.
2. **Read the relevant doctrine** before invoking any framework. The doctrine explains *why* the framework composes as it does.
3. **For source material in:** invoke `agents/transcript-synthesis-agent.md`. It produces a signal extraction conforming to `schemas/routing.schema.json`.
4. **For framework routing:** invoke `agents/golden-opportunity-strategist.md`. It selects frameworks based on detected signals.
5. **For moat analysis:** invoke `agents/moat-detection-agent.md`. It composes `skills/moat-detection.md` against the six moat classes.
6. **For output:** conform to the templates in `templates/` and the schemas in `schemas/`.

Agents should treat YAML frontmatter as authoritative for routing. The markdown body is for human readers.

---

## Adding To The Library

### New skill (atomic capability)
1. Copy `templates/skill-template.md` → `skills/[name].md`
2. Fill required sections; conform to `schemas/skill.schema.json`
3. Update any framework that composes it (`skills_used` field)
4. Update `meta/system-map.md` if it introduces a new relationship

### New framework
1. Copy `templates/framework-template.md` → `frameworks/[name].md`
2. Fill required sections; conform to `schemas/framework.schema.json`
3. List composed skills under `skills_used`
4. Add routing logic to the relevant agent
5. Add scoring dimensions if applicable

### New doctrine
1. Copy `templates/doctrine-template.md` → `doctrine/[name].md`
2. Doctrine must be falsifiable — explicitly list what would invalidate it
3. List the frameworks and skills it informs

### Extracting frameworks from transcripts
1. Place the raw transcript in `transcripts/`
2. Invoke `agents/transcript-synthesis-agent.md`
3. Place the structured extraction in `extractions/`
4. Promote stable patterns into `frameworks/` or `skills/`

---

## Operating Philosophy

Every file in this repo is:

- **Atomic** at its layer
- **Composable** across layers
- **Schema-validated** where machine-readable
- **Falsifiable** — it declares what would invalidate it
- **Calibrated** — it declares its confidence model
- **Routable** — frontmatter so agents can decide when to use it

We avoid:

- Buzzwords without diagnostic content
- Fake integrations and aspirational tooling claims
- Coupling to specific vendors, models, or frameworks
- Premature abstractions
- Documentation that cannot be acted on

---

## Roadmap

- **v0.1 (current)** — canonical structure, seed library, schemas, doctrine layer
- **v0.2** — ontology graph populated, agent routing rules formalized, prompt library
- **v0.3** — worked examples across founder, market, product, and operational diagnostics
- **v0.4** — semantic retrieval indices, agent composition patterns
- **v1.0** — production-grade intelligence substrate

## Versioning

Each file declares `version` in its YAML frontmatter. Bump on substantive change. Schemas use JSON Schema draft-07.

## Contributing

See `CONTRIBUTING.md`.

## License

See `LICENSE`.
