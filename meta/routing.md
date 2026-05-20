# Routing

The routing layer translates detected signals into framework, skill, and agent invocations. This file is the canonical reference for how source material moves through the Founder Intelligence System.

The schema this routes against: `schemas/routing.schema.json`.

## Use-Case Routing Table

| Use case | Trigger condition | Primary framework | Supporting skills | Scoring rubric | Output template | Recommended agent |
|---|---|---|---|---|---|---|
| **Attribution analysis** | Operator cannot explain *why* an outcome occurred; last-click or last-touch attribution being trusted | `map_attribution_framework` | `attribution_analysis`, `causal_inference_analysis`, `signal_hierarchy_analysis` | (custom per engagement) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Founder overload / bottleneck** | Work pauses when founder is offline; decisions route back to founder; founder describes feeling "everywhere and nowhere" | `curse_of_capability` | `founder_bottleneck_detection`, `decision_compression`, `ghost_note_detection` | `moat_strength_score` (knowledge externalization class) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Signal audit / clarity diagnosis** | Dashboards exist without decisions attached; "more data" is being prescribed; team cannot list contrary signals | `signal_audit_framework` | `signal_hierarchy_analysis`, `ghost_note_detection`, `iterative_error_compression` | (custom: listening surface score) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Prediction mismatch / misattribution** | Same decisions go wrong repeatedly; founder reaching for tools/hires/content as fix; "I knew it" appears retroactively | `founder_prediction_error_model` | `iterative_error_compression`, `attribution_analysis`, `founder_bottleneck_detection`, `time_horizon_arbitrage` | (custom per engagement) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **AI readiness diagnostic** | "We added AI but it didn't move the business"; AI being deployed on top of unclear signal | `applied_intelligence_stack` | `signal_hierarchy_analysis`, `attribution_analysis`, `founder_bottleneck_detection` | `golden_opportunity_score` (component: strategic fit) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Operational bottleneck / complexity drag** | Tool overload, fragmented workflows, AI adds output not clarity | `complexity_compression_theory` | `decision_compression`, `ghost_note_detection` | (custom per engagement) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Market opportunity evaluation** | Identifying defensible niches; positioning a productized offer; choosing among candidate markets | `niche_framework` (draft) | `ghost_note_detection`, `signal_hierarchy_analysis`, `attribution_analysis` | `golden_opportunity_score`, `timing_asymmetry_score` | `market-thesis-template`, `opportunity-brief-template` | `golden_opportunity_strategist` |
| **Moat analysis** | Evaluating defensibility of a current advantage; diligence on whether a business has durable structure | `organizational_memory_infrastructure`, `simplicity_arbitrage` | `moat_detection`, `founder_bottleneck_detection`, `iterative_error_compression` | `moat_strength_score` | `opportunity-brief-template` | `moat_detection_agent` |
| **Decision-load diagnosis** | Buyer or operator drowning in decisions; AI producing options not resolutions | `decision_compression_systems` | `decision_compression`, `adaptive_tension_tolerance` | (custom per engagement) | `opportunity-brief-template` | `ais_diagnostic_agent` |
| **Pricing outcome-based offers** | Distinguishing time-saving from time-recovering; willingness-to-pay analysis | `time_recovery_economics` | `time_horizon_arbitrage`, `decision_compression` | (custom per engagement) | `market-thesis-template` | `golden_opportunity_strategist` |
| **Stress-testing scalability** | "What breaks at 10x?"; pre-mortem on a strategy | `success_simulation_mapping` | `time_horizon_arbitrage`, `founder_bottleneck_detection` | (custom per engagement) | `opportunity-brief-template` | `golden_opportunity_strategist` |
| **Transcript / content extraction** | Raw source material needs to become structured signals + candidate frameworks | (none; pre-routing) | `ghost_note_detection`, `signal_hierarchy_analysis` | n/a | `framework-extraction-template` | `transcript_synthesis_agent` |
| **Opportunity diligence (full)** | End-to-end evaluation of a business opportunity from signals to recommendation | All canonical frameworks selected by signals | All canonical skills selected by frameworks | `golden_opportunity_score`, `moat_strength_score`, `timing_asymmetry_score` | `opportunity-brief-template` | `golden_opportunity_strategist` |
| **Founder cognition calibration** | Founder wants explicit calibration of their judgment quality | `founder_prediction_error_model` | `iterative_error_compression`, `time_horizon_arbitrage`, `attribution_analysis` | (custom per engagement) | `opportunity-brief-template` | `ais_diagnostic_agent` |

## Signal → Framework Map (operational reference)

| Detected signal | Primary framework | Secondary framework |
|---|---|---|
| Tool overload, fragmented workflows | `complexity_compression_theory` | `decision_compression_systems` |
| Founder is bottleneck | `curse_of_capability` | `organizational_memory_infrastructure` |
| Sprawling offers tied to founder skills | `curse_of_capability` | `complexity_compression_theory` |
| Feature-heavy competitors, confused buyer language | `simplicity_arbitrage` | `complexity_compression_theory` |
| Repeated decisions with the same answer | `decision_compression_systems` | `complexity_compression_theory` |
| Dashboards exist without decisions attached | `signal_audit_framework` | `decision_compression_systems` |
| Judgment lives only in the founder | `organizational_memory_infrastructure` | `curse_of_capability` |
| Same lessons recur across projects | `organizational_memory_infrastructure` | `founder_prediction_error_model` |
| Pricing outcome-based offers | `time_recovery_economics` | `simplicity_arbitrage` |
| Stress-testing scalability | `success_simulation_mapping` | `curse_of_capability` |
| Narrative too clean to be true | `signal_audit_framework` | `founder_prediction_error_model` |
| Founder claims pattern recognition without artifacts | `founder_prediction_error_model` | `signal_audit_framework` |
| Last-click attribution being trusted | `map_attribution_framework` | `signal_audit_framework` |
| "More data" prescribed for a clarity problem | `signal_audit_framework` | `map_attribution_framework` |
| "AI didn't move the business" | `applied_intelligence_stack` | `signal_audit_framework` |
| Choosing among candidate niches | `niche_framework` | `simplicity_arbitrage` |

## Combination Rules

Framework combinations that produce stronger diagnoses than either alone:

- `curse_of_capability` + `organizational_memory_infrastructure` → **founder-led service business diagnostic**
- `complexity_compression_theory` + `simplicity_arbitrage` → **category disruption thesis**
- `decision_compression_systems` + `time_recovery_economics` → **premium AI product pricing thesis**
- `success_simulation_mapping` + `curse_of_capability` → **pre-scale structural redesign**
- `signal_audit_framework` + `founder_prediction_error_model` → **founder cognition audit**
- `organizational_memory_infrastructure` + `founder_prediction_error_model` → **knowledge moat assessment**
- `signal_audit_framework` + `map_attribution_framework` → **decision-quality diagnostic** (signal layer → attribution layer)
- `applied_intelligence_stack` + `map_attribution_framework` → **AI readiness assessment** (where in the stack is AI being layered on top of unclear attribution)
- `applied_intelligence_stack` + `founder_prediction_error_model` → **end-to-end founder operating-system diagnostic**
- `niche_framework` + `simplicity_arbitrage` → **offer design thesis**
- `map_attribution_framework` + `founder_prediction_error_model` → **calibration baseline before next quarter's planning**

## Skip Rules

When a framework's `avoid_when` condition fires, the router records the skip with rationale rather than running the framework. Skip decisions are first-class outputs.

## Maturity Notes

The following framework is currently `status: draft` and should be flagged as evolving in any output that uses it:

- `niche_framework` — v0.2 draft; expect iteration on the five letters and the scoring rubric

Outputs that depend on a draft framework must include a maturity disclaimer pointing the operator to the framework file.

## Agent Hand-off Contracts

```
transcript-synthesis-agent
   ↓ produces extraction conforming to routing.schema.json
ais-diagnostic-agent
   ↓ produces Diagnose → Design → Deploy brief
   ↓ may hand off to:
golden-opportunity-strategist
   ↓ produces frameworks-applied output
moat-detection-agent
   ↓ produces moat-strength output
[composite scoring]
   ↓ produces brief conforming to opportunity.schema.json
```

## Versioning

This routing map is v1.1 (extended with M.A.P., Applied Intelligence Stack, N.I.C.H.E., AIS Diagnostic Agent, and the four new skills). New frameworks and agents must be added here when they are added to their layer folders. Removal requires a deprecation entry, not deletion.
