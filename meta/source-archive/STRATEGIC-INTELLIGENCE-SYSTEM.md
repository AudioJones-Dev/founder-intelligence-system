# Strategic Intelligence System

A modular framework library for AI-era opportunity analysis. This is a **strategic cognition layer**, not a note library.

## Architecture

```
/strategic-intelligence-system/
  /primitives/      # Atomic cognitive capabilities (one .md per primitive)
  /frameworks/      # Composed strategic lenses (one .md per framework)
  /schemas/         # JSON schemas for validation
  /skills/          # AI instruction files (workflow routers)
  /scoring/         # Composite scoring rubrics
  /outputs/         # Templates for repeatable reasoning
```

### Three Layers Of Cognition

| Layer | What it is | Examples |
|---|---|---|
| **Primitives** | Atomic, content-agnostic capabilities | absence detection, iterative error compression |
| **Frameworks** | Composed strategic lenses applied to specific situations | curse of capability, simplicity arbitrage |
| **Skills** | Workflow routers that drive the analysis | transcript synthesis, moat detection |

Primitives are *used by* frameworks and skills. Frameworks are *applied by* skills. Skills produce outputs that conform to the templates in `/outputs/`.

## How To Use

1. **Source material in** → run `skills/transcript-synthesis-skill.md` to extract claims and signals.
2. **Signals out** → run `skills/golden-opportunity-strategist.md` to route to the right frameworks.
3. **Frameworks applied** → each framework produces a finding + score, calling on primitives as needed.
4. **Score the opportunity** → composite via `scoring/golden-opportunity-score.md`.
5. **Test the moat** → run `skills/moat-detection-skill.md`.
6. **Produce the brief** → fill `outputs/opportunity-brief-template.md`.

## Primitives

| ID | Purpose |
|---|---|
| `absence_detection` | Find the signal in what is missing |
| `iterative_error_compression` | Improve by reducing error, not by repeating success |
| `adaptive_tension_tolerance` | Stay composed inside difficult conversations and decisions |
| `core_communication_protocol` | Curiosity → Objectivity → Reassurance → Empathy |
| `time_horizon_arbitrage` | Match the decision to its natural time horizon |

## Frameworks

| ID | Use When |
|---|---|
| `complexity_compression_theory` | Tool overload, fragmented workflows, AI adds output not clarity |
| `curse_of_capability` | Founder is the bottleneck, sprawling offers |
| `simplicity_arbitrage` | Feature-heavy category, confused buyer language |
| `decision_compression_systems` | Buyer/operator drowning in decisions |
| `success_simulation_mapping` | Stress-testing scalability |
| `organizational_memory_infrastructure` | Judgment lives only in people |
| `time_recovery_economics` | Pricing outcome-based offers |

## Adding A New Primitive

1. Create `/primitives/[name].md` with YAML frontmatter conforming to `/schemas/primitive.schema.json`.
2. Update any frameworks that compose it (`primitives_used` field).
3. Update any skills that invoke it directly.

## Adding A New Framework

1. Create `/frameworks/[name].md` with YAML frontmatter conforming to `/schemas/framework.schema.json` (v1.1).
2. List the primitives it composes in `primitives_used`.
3. Add routing logic to `/skills/golden-opportunity-strategist.md`.
4. If it introduces new scoring dimensions, update or add a rubric in `/scoring/`.
5. If it changes the output, update the relevant template in `/outputs/`.

## Design Principles

- **Atomic at the primitive layer** — primitives do one thing, are content-agnostic
- **Composed at the framework layer** — frameworks combine primitives for specific strategic situations
- **Routable** — YAML frontmatter so AI can decide when to use what
- **Scorable** — every framework produces a 1–10 score
- **Falsifiable** — every output names what would invalidate it
- **Calibrated** — every primitive and framework declares its confidence model

## Versioning

Each file declares `version` in its frontmatter. Bump on substantive change. The framework schema is at v1.1 (added `triggers`, `failure_modes`, `confidence_model`, `primitives_used`); existing framework files are still compatible because all new fields are optional. Backfill them framework-by-framework as you revise.
