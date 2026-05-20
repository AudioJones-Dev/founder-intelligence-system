# Concept Graph

A directed graph of every concept currently in the Founder Intelligence System, with explicit relationships.

Format: each row is a `(source) --[relation]--> (target)` edge. Relations follow `schemas/ontology.schema.json`.

## Doctrine → Frameworks / Skills

| Source | Relation | Target |
|---|---|---|
| `signal_doctrine` | `informs` | `signal_audit_framework` |
| `signal_doctrine` | `informs` | `map_attribution_framework` |
| `signal_doctrine` | `informs` | `complexity_compression_theory` |
| `signal_doctrine` | `informs` | `simplicity_arbitrage` |
| `signal_doctrine` | `informs` | `decision_compression_systems` |
| `signal_doctrine` | `informs` | `organizational_memory_infrastructure` |
| `signal_doctrine` | `informs` | `founder_prediction_error_model` |
| `signal_doctrine` | `informs` | `niche_framework` |
| `signal_doctrine` | `informs` | `applied_intelligence_stack` |
| `signal_doctrine` | `informs` | `ghost_note_detection` |
| `signal_doctrine` | `informs` | `iterative_error_compression` |
| `signal_doctrine` | `informs` | `signal_hierarchy_analysis` |
| `signal_doctrine` | `informs` | `attribution_analysis` |
| `signal_doctrine` | `informs` | `causal_inference_analysis` |
| `founder_intelligence_system` | `informs` | `curse_of_capability` |
| `founder_intelligence_system` | `informs` | `organizational_memory_infrastructure` |
| `founder_intelligence_system` | `informs` | `decision_compression_systems` |
| `founder_intelligence_system` | `informs` | `success_simulation_mapping` |
| `founder_intelligence_system` | `informs` | `founder_prediction_error_model` |
| `founder_intelligence_system` | `informs` | `signal_audit_framework` |
| `founder_intelligence_system` | `informs` | `map_attribution_framework` |
| `founder_intelligence_system` | `informs` | `applied_intelligence_stack` |
| `founder_intelligence_system` | `informs` | `founder_bottleneck_detection` |
| `founder_intelligence_system` | `informs` | `attribution_analysis` |
| `founder_intelligence_system` | `informs` | `signal_hierarchy_analysis` |
| `complexity_compression` | `informs` | `complexity_compression_theory` |
| `complexity_compression` | `informs` | `decision_compression_systems` |
| `complexity_compression` | `informs` | `simplicity_arbitrage` |
| `simplicity_arbitrage_doctrine` | `informs` | `simplicity_arbitrage` |
| `simplicity_arbitrage_doctrine` | `informs` | `decision_compression_systems` |
| `organizational_memory` | `informs` | `organizational_memory_infrastructure` |
| `organizational_memory` | `informs` | `curse_of_capability` |
| `organizational_memory` | `informs` | `decision_compression_systems` |

## Doctrine ↔ Doctrine

| Source | Relation | Target |
|---|---|---|
| `signal_doctrine` | `derives_from` | `founder_intelligence_system` |
| `complexity_compression` | `derives_from` | `signal_doctrine` |
| `organizational_memory` | `derives_from` | `founder_intelligence_system` |
| `simplicity_arbitrage_doctrine` | `derives_from` | `complexity_compression` |

## Frameworks ↔ Frameworks (operationalization + routing)

| Source | Relation | Target |
|---|---|---|
| `map_attribution_framework` | `operationalizes` | `signal_doctrine` |
| `signal_audit_framework` | `operationalizes` | `signal_doctrine` |
| `founder_prediction_error_model` | `operationalizes` | `founder_intelligence_system` |
| `applied_intelligence_stack` | `operationalizes` | `founder_intelligence_system` |
| `complexity_compression_theory` | `operationalizes` | `complexity_compression` |
| `decision_compression_systems` | `operationalizes` | `complexity_compression` |
| `simplicity_arbitrage` | `operationalizes` | `simplicity_arbitrage_doctrine` |
| `organizational_memory_infrastructure` | `operationalizes` | `organizational_memory` |
| `niche_framework` | `operationalizes` | `signal_doctrine` |
| `signal_audit_framework` | `routes_to` | `map_attribution_framework` |
| `signal_audit_framework` | `routes_to` | `founder_prediction_error_model` |
| `applied_intelligence_stack` | `routes_to` | `signal_audit_framework` |
| `applied_intelligence_stack` | `routes_to` | `map_attribution_framework` |
| `applied_intelligence_stack` | `routes_to` | `founder_prediction_error_model` |
| `map_attribution_framework` | `depends_on` | `signal_audit_framework` |
| `founder_prediction_error_model` | `depends_on` | `signal_audit_framework` |
| `founder_prediction_error_model` | `depends_on` | `map_attribution_framework` |
| `niche_framework` | `depends_on` | `signal_audit_framework` |

## Frameworks → Skills (composition)

| Framework | Relation | Skill |
|---|---|---|
| `signal_audit_framework` | `composed_by` | `ghost_note_detection` |
| `signal_audit_framework` | `composed_by` | `iterative_error_compression` |
| `signal_audit_framework` | `composed_by` | `core_communication_protocol` |
| `signal_audit_framework` | `composed_by` | `signal_hierarchy_analysis` |
| `signal_audit_framework` | `composed_by` | `founder_bottleneck_detection` |
| `map_attribution_framework` | `composed_by` | `attribution_analysis` |
| `map_attribution_framework` | `composed_by` | `causal_inference_analysis` |
| `map_attribution_framework` | `composed_by` | `signal_hierarchy_analysis` |
| `map_attribution_framework` | `composed_by` | `ghost_note_detection` |
| `map_attribution_framework` | `composed_by` | `decision_compression` |
| `applied_intelligence_stack` | `composed_by` | `signal_hierarchy_analysis` |
| `applied_intelligence_stack` | `composed_by` | `attribution_analysis` |
| `applied_intelligence_stack` | `composed_by` | `founder_bottleneck_detection` |
| `applied_intelligence_stack` | `composed_by` | `decision_compression` |
| `applied_intelligence_stack` | `composed_by` | `iterative_error_compression` |
| `founder_prediction_error_model` | `composed_by` | `iterative_error_compression` |
| `founder_prediction_error_model` | `composed_by` | `ghost_note_detection` |
| `founder_prediction_error_model` | `composed_by` | `time_horizon_arbitrage` |
| `founder_prediction_error_model` | `composed_by` | `attribution_analysis` |
| `founder_prediction_error_model` | `composed_by` | `founder_bottleneck_detection` |
| `niche_framework` | `composed_by` | `ghost_note_detection` |
| `niche_framework` | `composed_by` | `signal_hierarchy_analysis` |
| `niche_framework` | `composed_by` | `attribution_analysis` |
| `organizational_memory_infrastructure` | `composed_by` | `ghost_note_detection` |
| `organizational_memory_infrastructure` | `composed_by` | `iterative_error_compression` |
| `curse_of_capability` | `composed_by` | `ghost_note_detection` |
| `curse_of_capability` | `composed_by` | `adaptive_tension_tolerance` |
| `curse_of_capability` | `composed_by` | `core_communication_protocol` |
| `curse_of_capability` | `composed_by` | `founder_bottleneck_detection` |
| `simplicity_arbitrage` | `composed_by` | `ghost_note_detection` |
| `decision_compression_systems` | `composed_by` | `adaptive_tension_tolerance` |
| `decision_compression_systems` | `composed_by` | `iterative_error_compression` |
| `decision_compression_systems` | `composed_by` | `decision_compression` |
| `success_simulation_mapping` | `composed_by` | `time_horizon_arbitrage` |
| `time_recovery_economics` | `composed_by` | `time_horizon_arbitrage` |

## Skills → Skills (typed)

| Source | Relation | Target |
|---|---|---|
| `attribution_analysis` | `depends_on` | `signal_hierarchy_analysis` |
| `causal_inference_analysis` | `depends_on` | `attribution_analysis` |
| `signal_hierarchy_analysis` | `detects` | `ghost_note_detection` |
| `attribution_analysis` | `attributes` | `map_attribution_framework` |
| `founder_bottleneck_detection` | `detects` | `curse_of_capability` |
| `iterative_error_compression` | `evaluates_with` | `founder_prediction_error_model` |

## Agents → Skills + Frameworks (orchestration)

| Agent | Relation | Target |
|---|---|---|
| `transcript_synthesis_agent` | `composes` | `ghost_note_detection` |
| `transcript_synthesis_agent` | `routes_to` | `golden_opportunity_strategist` |
| `golden_opportunity_strategist` | `composes` | `ghost_note_detection` |
| `golden_opportunity_strategist` | `composes` | `iterative_error_compression` |
| `golden_opportunity_strategist` | `composes` | `signal_hierarchy_analysis` |
| `golden_opportunity_strategist` | `composes` | `attribution_analysis` |
| `golden_opportunity_strategist` | `composes` | `complexity_compression_theory` |
| `golden_opportunity_strategist` | `composes` | `curse_of_capability` |
| `golden_opportunity_strategist` | `composes` | `simplicity_arbitrage` |
| `golden_opportunity_strategist` | `composes` | `decision_compression_systems` |
| `golden_opportunity_strategist` | `composes` | `success_simulation_mapping` |
| `golden_opportunity_strategist` | `composes` | `organizational_memory_infrastructure` |
| `golden_opportunity_strategist` | `composes` | `time_recovery_economics` |
| `moat_detection_agent` | `composes` | `moat_detection` |
| `moat_detection_agent` | `composes` | `ghost_note_detection` |
| `moat_detection_agent` | `composes` | `iterative_error_compression` |
| `moat_detection_agent` | `composes` | `founder_bottleneck_detection` |
| `moat_detection_agent` | `composes` | `organizational_memory_infrastructure` |
| `moat_detection_agent` | `composes` | `decision_compression_systems` |
| `moat_detection_agent` | `composes` | `simplicity_arbitrage` |
| `founder_intelligence_diagnostic_agent` | `composes` | `signal_hierarchy_analysis` |
| `founder_intelligence_diagnostic_agent` | `composes` | `attribution_analysis` |
| `founder_intelligence_diagnostic_agent` | `composes` | `causal_inference_analysis` |
| `founder_intelligence_diagnostic_agent` | `composes` | `founder_bottleneck_detection` |
| `founder_intelligence_diagnostic_agent` | `composes` | `decision_compression` |
| `founder_intelligence_diagnostic_agent` | `composes` | `ghost_note_detection` |
| `founder_intelligence_diagnostic_agent` | `composes` | `iterative_error_compression` |
| `founder_intelligence_diagnostic_agent` | `composes` | `signal_audit_framework` |
| `founder_intelligence_diagnostic_agent` | `composes` | `map_attribution_framework` |
| `founder_intelligence_diagnostic_agent` | `composes` | `applied_intelligence_stack` |
| `founder_intelligence_diagnostic_agent` | `composes` | `founder_prediction_error_model` |
| `founder_intelligence_diagnostic_agent` | `composes` | `curse_of_capability` |
| `founder_intelligence_diagnostic_agent` | `composes` | `organizational_memory_infrastructure` |
| `founder_intelligence_diagnostic_agent` | `composes` | `decision_compression_systems` |
| `founder_intelligence_diagnostic_agent` | `routes_to` | `golden_opportunity_strategist` |
| `founder_intelligence_diagnostic_agent` | `routes_to` | `moat_detection_agent` |

## Scoring

| Source | Relation | Target |
|---|---|---|
| `golden_opportunity_score` | `evaluates_with` | `golden_opportunity_strategist` |
| `moat_strength_score` | `evaluates_with` | `moat_detection_agent` |
| `moat_strength_score` | `evaluates_with` | `moat_detection` |
| `timing_asymmetry_score` | `evaluates_with` | `golden_opportunity_strategist` |

## Templates → Frameworks / Agents (production)

| Source | Relation | Target |
|---|---|---|
| `framework_extraction_template` | `produces` | `transcript_synthesis_agent` |
| `market_thesis_template` | `produces` | `golden_opportunity_strategist` |
| `opportunity_brief_template` | `produces` | `golden_opportunity_strategist` |
| `opportunity_brief_template` | `produces` | `founder_intelligence_diagnostic_agent` |

## Aliases

| Source | Relation | Target |
|---|---|---|
| `ghost_note_detection` | `alias_of` | `absence_detection` |
