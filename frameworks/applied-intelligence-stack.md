---
id: applied_intelligence_stack
name: Applied Intelligence Stack
type: strategic_framework
version: 1.0
status: active
internal_only: true
use_when:
  - architecting an end-to-end intelligence system for a founder-led business
  - auditing where an existing AI / data / ops stack breaks down
  - sequencing investments across signal, data, attribution, intelligence, execution, and feedback
  - distinguishing AI augmentation from AI automation in a real system
avoid_when:
  - the business does not yet have any of the six layers; start with Signal Audit instead
  - the analysis is purely about a single layer (e.g., dashboards) — use a narrower framework
related_frameworks:
  - signal_audit_framework
  - map_attribution_framework
  - decision_compression_systems
  - founder_prediction_error_model
  - organizational_memory_infrastructure
skills_used:
  - signal_hierarchy_analysis
  - attribution_analysis
  - founder_bottleneck_detection
  - decision_compression
  - iterative_error_compression
related_doctrine:
  - founder_intelligence_system
  - signal_doctrine
  - organizational_memory
inputs_required:
  - current_stack_inventory
  - founder_role_description
  - outcome_definition
outputs:
  - layer_health_map
  - stack_gap_inventory
  - sequencing_recommendation
diagnostic_questions:
  - At each layer, is the right input present, clean, and actionable?
  - Where does the stack break between layers (signal → data, data → attribution, etc.)?
  - Which layer is the bottleneck — and is investment going there or elsewhere?
  - Where is AI being layered on top of unclear signal?
triggers:
  - "we added AI but it didn't move the business"
  - dashboards exist at every layer but the founder still has to integrate them by hand
  - the founder is the feedback loop
  - automation has been deployed on top of an unclear or unattributed process
scoring_dimensions:
  - name: layer_coverage
    description: How many of the six layers exist in a recognizable form
    scale: 1-10
  - name: layer_quality
    description: Within the layers that exist, how clean and decision-relevant the outputs are
    scale: 1-10
  - name: inter_layer_continuity
    description: How well the layers actually feed each other (vs. existing as isolated silos)
    scale: 1-10
failure_modes:
  - Building the intelligence and execution layers on top of an unclear signal layer
  - Treating dashboards as the intelligence layer
  - Automating execution before attribution is validated
  - Skipping the feedback layer — the business never learns from its own results
  - Confusing automation with intelligence
confidence_model:
  low: Single-pass audit of the stack; gaps named but not validated
  medium: Multi-cycle audit; layer health tracked over time
  high: Continuous instrumentation of the stack; each layer's health measurable independently
---

# Applied Intelligence Stack

> **Internal-only framework.** This is the operational architecture that backs Founder Intelligence System doctrine. It is not the public-facing umbrella concept (that role is held by Founder Intelligence System itself). Use this framework to *audit and design* the underlying stack, not to brand it.

## Purpose
Define the six-layer stack that integrates human judgment, business data, AI tools, attribution logic, and adaptive feedback loops into one operating system. Use it as a diagnostic for where a founder-led business's intelligence layer breaks down.

## Problem It Solves
Most founder-led businesses have *components* of an intelligence system — dashboards, automations, an AI tool, a CRM, a content pipeline. They do not have an integrated stack. The components do not talk. The signal layer is unclear, so the data layer captures the wrong things, so the attribution layer cannot run, so the intelligence layer produces fluent nonsense, so execution amplifies dysfunction, so the feedback layer never closes.

Applied Intelligence Stack names the six layers explicitly and forces an audit at each one.

## The Six Layers

| Layer | Function | Signal-doctrine question |
|---|---|---|
| **Signal Layer** | Identify what matters | What changes the next decision? |
| **Data Layer** | Capture clean inputs | Is what we capture actually what matters? |
| **Attribution Layer** | Separate cause from correlation | What actually caused the outcome? |
| **Intelligence Layer** | Use AI/judgment to process, summarize, recommend | Can the output be acted on without re-deriving context? |
| **Execution Layer** | Turn insight into action | Does action flow from the intelligence layer, or around it? |
| **Feedback Layer** | Measure results and improve the system | Does each cycle make the next one cheaper, sharper, faster? |

Each layer's quality is gated by the layer below it. Adding AI to a business with an unclear signal layer does not produce intelligence — it produces faster, fluent dysfunction.

## Related Skills
- **Signal Hierarchy Analysis** — for the signal layer
- **Attribution Analysis** — for the attribution layer
- **Founder Bottleneck Detection** — for spotting where the founder is filling in for a missing layer
- **Decision Compression** — for closing the gap between intelligence and execution
- **Iterative Error Compression** — for the feedback layer

## Operating Logic
1. Inventory the current state of each layer in the target business
2. Score each layer on coverage and quality (1–10)
3. Identify inter-layer breaks — places where the output of one layer cannot be consumed by the next
4. Locate the lowest-scoring layer; that is the current bottleneck
5. Refuse to invest in layers above the bottleneck until the bottleneck moves
6. Output a sequencing recommendation: which layer to invest in next, with what specific deliverable

## Inputs
- Inventory of current tools, dashboards, processes, agents
- Description of the founder's current role across the six layers
- Definition of the outcome the system is supposed to drive

## Outputs
- A layer health map (six-row scorecard)
- A stack gap inventory (what is missing, what is broken between layers)
- A sequencing recommendation (what to fix first, second, third)

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Only one or two layers exist; the founder is the integration glue |
| 3 | Most layers present but inter-layer continuity is poor |
| 5 | Layers exist and partially connect; the feedback layer is weakest |
| 7 | Full six-layer stack with continuous flow; some layer quality issues |
| 10 | All six layers operate independently, integrate cleanly, and improve cycle over cycle |

## Common Bottlenecks (Diagnostic Patterns)

| Symptom | Layer that's broken |
|---|---|
| Leadership cannot name what causes outcomes | Signal Layer |
| Dashboards exist but data is dirty or partial | Data Layer |
| Decisions adjudicated by who argues hardest | Attribution Layer |
| AI tools produce options nobody acts on | Intelligence Layer |
| Insight exists but action doesn't follow | Execution Layer |
| Same lessons learned every quarter | Feedback Layer |

## Failure Modes
- Building intelligence and execution on top of an unclear signal layer
- Treating dashboards as the intelligence layer (they are part of the data layer)
- Automating execution before attribution is validated — automation then amplifies the wrong cause
- Skipping the feedback layer entirely — the business never learns from its own results
- Conflating automation with intelligence — automation is a property of the execution layer, not a replacement for the intelligence layer

## Strategic Value
This framework gives the team a single diagnostic vocabulary for "where in the stack is this breaking?" without immediately reaching for a tool, a hire, or an automation. It enforces sequencing: signal before data, data before attribution, attribution before intelligence, intelligence before execution, execution before feedback.

## Example Applications
- AI readiness audits (audit each layer before adding AI)
- Founder decision dashboards (design the signal + data + attribution layers explicitly)
- Marketing attribution systems (apply M.A.P. inside the attribution layer)
- Internal operating systems for founder-led businesses
- Diagnosing why a previous AI initiative "didn't work"

## Compression Summary
**Six layers, gated bottom-up: signal, data, attribution, intelligence, execution, feedback. Adding capability above the bottleneck adds noise.**
