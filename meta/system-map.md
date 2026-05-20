# System Map

The Founder Intelligence System (FIS) is layered. This document is the entry point for any agent or operator orienting against the substrate.

## Layer Composition

```
        ┌─────────────────────────────────┐
        │           DOCTRINE              │   the worldview
        │  signal · fis · complexity ·    │
        │  simplicity · org-memory        │
        └────────────┬────────────────────┘
                     │ informs
        ┌────────────▼────────────────────┐
        │          FRAMEWORKS             │   composed strategic lenses
        │  complexity-compression-theory  │
        │  curse-of-capability            │
        │  decision-compression-systems   │
        │  organizational-memory-infra    │
        │  simplicity-arbitrage           │
        │  success-simulation-mapping     │
        │  time-recovery-economics        │
        │  signal-audit-framework         │
        │  founder-prediction-error-model │
        └────────────┬────────────────────┘
                     │ composes
        ┌────────────▼────────────────────┐
        │            SKILLS               │   atomic reasoning capabilities
        │  ghost-note-detection           │
        │  iterative-error-compression    │
        │  adaptive-tension-tolerance     │
        │  core-communication-protocol    │
        │  time-horizon-arbitrage         │
        │  decision-compression           │
        │  moat-detection                 │
        └────────────┬────────────────────┘
                     │ validated by
        ┌────────────▼────────────────────┐
        │      SCHEMAS + ONTOLOGY         │   machine-readable substrate
        │  skill · framework · doctrine · │
        │  agent · routing · scoring ·    │
        │  opportunity · ontology         │
        └────────────┬────────────────────┘
                     │ orchestrated by
        ┌────────────▼────────────────────┐
        │       AGENTS + PROMPTS          │   workflow routers
        │  transcript-synthesis-agent     │
        │  golden-opportunity-strategist  │
        │  moat-detection-agent           │
        └────────────┬────────────────────┘
                     │ applied to
        ┌────────────▼────────────────────┐
        │  TRANSCRIPTS → EXTRACTIONS →    │   the operational pipeline
        │  RESEARCH → SCORING → BRIEFS    │
        └─────────────────────────────────┘
```

## Layer Responsibilities

### Doctrine (`doctrine/`)
**What:** The worldview underneath the system. Doctrine answers *why* the frameworks compose the way they do.

**Tone:** Philosophical, falsifiable, opinionated.

**Examples:** Signal Doctrine, Founder Intelligence System doctrine, Complexity Compression, Simplicity Arbitrage, Organizational Memory.

**Authoring rule:** Every doctrine entry must declare its foundational assumptions and its falsifiers. Doctrine that cannot be wrong is not doctrine — it is decoration.

### Frameworks (`frameworks/`)
**What:** Composed strategic lenses for diagnosing specific situations. Each framework produces a scored finding (1–10) and a list of recommended moves.

**Tone:** Operational, diagnostic, scorable.

**Examples:** Complexity Compression Theory, Curse of Capability, Decision Compression Systems, Signal Audit Framework, Founder Prediction Error Model.

**Authoring rule:** Every framework must declare `use_when`, `avoid_when`, `skills_used`, scoring dimensions, and failure modes.

### Skills (`skills/`)
**What:** Atomic, content-agnostic reasoning capabilities. Skills are the smallest reusable units of cognition. Frameworks compose them; agents invoke them.

**Tone:** Procedural, content-agnostic, calibrated.

**Examples:** Ghost Note Detection, Iterative Error Compression, Decision Compression, Moat Detection.

**Authoring rule:** Skills declare `triggers`, `operational_logic`, `failure_modes`, and a `confidence_model`.

### Schemas (`schemas/`)
**What:** Machine-readable JSON definitions for every layer above. Agents validate against these. Tooling can index against them.

**Tone:** Lightweight, extensible, human-readable JSON Schema (draft-07).

### Ontology (`ontology/`)
**What:** The concept-relation graph. Captures the semantic relationships between concepts that span layers — including aliases, supersession, composition, and scoring relationships.

**Tone:** Structural, machine-readable, minimal narrative.

### Agents (`agents/`)
**What:** Workflow routers. Agents do not contain reasoning capabilities of their own — they orchestrate skills and frameworks against source material to produce structured output.

**Examples:** Transcript Synthesis Agent, Golden Opportunity Strategist, Moat Detection Agent.

**Authoring rule:** Every agent must declare its `process`, the `skills` and `frameworks` it composes, and the schemas its output conforms to.

### Prompts (`prompts/`)
**What:** Reusable prompt templates that wrap agent invocations for specific surfaces (chat, batch, copilot).

### Transcripts (`transcripts/`)
**What:** Raw source material — interviews, podcasts, founder calls, sales calls, strategy sessions. The substrate the agents operate on.

**Authoring rule:** Raw text only. No interpretation. No summary. No extraction. That work belongs in `extractions/`.

### Extractions (`extractions/`)
**What:** Structured outputs derived from transcripts via the synthesis agent. The bridge between raw source material and framework application.

### Research (`research/`)
**What:** Supporting evidence and source analysis — market scans, citations, comparative studies that inform doctrine or framework authorship.

### Examples (`examples/`)
**What:** Worked examples showing the system in action — fully filled-in briefs, multi-framework analyses, real moat detections.

### Templates (`templates/`)
**What:** Reusable document structures for the layers above. Copy a template, fill it, validate against the schema.

### Scoring (`scoring/`)
**What:** Composite scoring rubrics that aggregate individual framework scores into business-level scores (golden opportunity, moat strength, timing asymmetry).

### Meta (`meta/`)
**What:** This map, routing logic, governance, source archive — the system's metadata about itself.

---

## End-to-End Flow (Source → Brief)

1. **Drop a transcript** into `transcripts/[name]-[date].md`
2. **Invoke** `agents/transcript-synthesis-agent.md` to extract claims, themes, and signals → `extractions/[name].md`
3. **Invoke** `agents/golden-opportunity-strategist.md` against the extraction. It:
   - Routes signals to frameworks (per `schemas/routing.schema.json`)
   - Applies each framework, producing a finding + 1–10 score
4. **Compose** moat analysis via `agents/moat-detection-agent.md` (uses `skills/moat-detection.md`)
5. **Aggregate** scores via `scoring/golden-opportunity-score.md`, `scoring/moat-strength-score.md`, `scoring/timing-asymmetry-score.md`
6. **Produce** the brief by filling `templates/opportunity-brief-template.md`
7. **File** the brief in `examples/` if it is to be retained as a worked reference

---

## Agent Routing Logic

The default router lives inside `agents/golden-opportunity-strategist.md`. Its routing table is reproduced here for reference:

| Detected signal pattern | Framework to invoke |
|---|---|
| Tool overload, fragmented workflows, AI adds output not clarity | `complexity_compression_theory` |
| Founder is the bottleneck, sprawling offers | `curse_of_capability` |
| Feature-heavy category, confused buyer language | `simplicity_arbitrage` |
| Buyer/operator drowning in decisions | `decision_compression_systems` |
| Stress-testing scalability | `success_simulation_mapping` |
| Judgment lives only in people | `organizational_memory_infrastructure` |
| Pricing outcome-based offers | `time_recovery_economics` |
| Diligence: noticing layer suspect | `signal_audit_framework` |
| Calibrating founder judgment | `founder_prediction_error_model` |

When more than one framework's triggers fire, the router applies all and produces a stacked finding. Cross-framework combination rules are documented in `agents/golden-opportunity-strategist.md`.

---

## How Transcripts Become Reusable Intelligence

The promotion path looks like this:

```
Transcript (raw)
   → Extraction (structured)
   → Routing decision (signals → frameworks)
   → Framework application (finding + score)
   → Composite scoring
   → Brief
   ↓
   (if pattern recurs across multiple briefs)
   → Candidate framework or skill in /frameworks or /skills
   ↓
   (if pattern is foundational to the worldview)
   → Candidate doctrine in /doctrine
```

The promotion is not automatic. Promotion requires:
- The pattern appears in ≥ 3 independent extractions
- The pattern produces consistent diagnostic value across those extractions
- An author writes the new file conforming to the relevant schema

---

## Versioning Discipline

- Every file declares `version` in YAML frontmatter
- Bump on substantive change — not on typo fixes
- Schemas may add optional fields without bumping the major version
- Breaking schema changes require a migration note in `meta/`

---

## Future Routing (Roadmap)

- **v0.2** — formal routing rules expressed as a routing graph in `meta/routing.md` and `schemas/routing.schema.json`
- **v0.3** — agent composition patterns: which agents call which agents, with explicit hand-off contracts
- **v0.4** — embedding/index layer for semantic retrieval (substrate, not orchestration)
