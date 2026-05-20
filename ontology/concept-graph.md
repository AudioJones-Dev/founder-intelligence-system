# Concept Graph

A directed graph of every concept currently in the Founder Intelligence System, with explicit relationships.

Format: each row is a `(source) --[relation]--> (target)` edge. Relations follow `schemas/ontology.schema.json`.

## Doctrine

| Source | Relation | Target |
|---|---|---|
| `signal_doctrine` | `informs` | `complexity_compression_theory` |
| `signal_doctrine` | `informs` | `simplicity_arbitrage` |
| `signal_doctrine` | `informs` | `decision_compression_systems` |
| `signal_doctrine` | `informs` | `organizational_memory_infrastructure` |
| `signal_doctrine` | `informs` | `signal_audit_framework` |
| `signal_doctrine` | `informs` | `ghost_note_detection` |
| `signal_doctrine` | `informs` | `iterative_error_compression` |
| `signal_doctrine` | `related_to` | `founder_intelligence_system` |
| `founder_intelligence_system` | `informs` | `curse_of_capability` |
| `founder_intelligence_system` | `informs` | `organizational_memory_infrastructure` |
| `founder_intelligence_system` | `informs` | `decision_compression_systems` |
| `founder_intelligence_system` | `informs` | `success_simulation_mapping` |
| `founder_intelligence_system` | `informs` | `founder_prediction_error_model` |
| `founder_intelligence_system` | `related_to` | `signal_doctrine` |
| `founder_intelligence_system` | `related_to` | `organizational_memory` |
| `complexity_compression` | `informs` | `complexity_compression_theory` |
| `complexity_compression` | `informs` | `decision_compression_systems` |
| `complexity_compression` | `informs` | `simplicity_arbitrage` |
| `complexity_compression` | `related_to` | `signal_doctrine` |
| `simplicity_arbitrage_doctrine` | `informs` | `simplicity_arbitrage` |
| `simplicity_arbitrage_doctrine` | `informs` | `decision_compression_systems` |
| `simplicity_arbitrage_doctrine` | `related_to` | `complexity_compression` |
| `organizational_memory` | `informs` | `organizational_memory_infrastructure` |
| `organizational_memory` | `informs` | `curse_of_capability` |
| `organizational_memory` | `informs` | `decision_compression_systems` |
| `organizational_memory` | `related_to` | `founder_intelligence_system` |

## Frameworks

| Source | Relation | Target |
|---|---|---|
| `complexity_compression_theory` | `related_to` | `curse_of_capability` |
| `complexity_compression_theory` | `related_to` | `simplicity_arbitrage` |
| `complexity_compression_theory` | `related_to` | `decision_compression_systems` |
| `curse_of_capability` | `related_to` | `complexity_compression_theory` |
| `curse_of_capability` | `related_to` | `decision_compression_systems` |
| `curse_of_capability` | `related_to` | `organizational_memory_infrastructure` |
| `decision_compression_systems` | `related_to` | `complexity_compression_theory` |
| `decision_compression_systems` | `related_to` | `simplicity_arbitrage` |
| `decision_compression_systems` | `related_to` | `organizational_memory_infrastructure` |
| `organizational_memory_infrastructure` | `related_to` | `curse_of_capability` |
| `organizational_memory_infrastructure` | `related_to` | `decision_compression_systems` |
| `organizational_memory_infrastructure` | `related_to` | `success_simulation_mapping` |
| `simplicity_arbitrage` | `related_to` | `complexity_compression_theory` |
| `simplicity_arbitrage` | `related_to` | `decision_compression_systems` |
| `success_simulation_mapping` | `related_to` | `curse_of_capability` |
| `success_simulation_mapping` | `related_to` | `complexity_compression_theory` |
| `success_simulation_mapping` | `related_to` | `organizational_memory_infrastructure` |
| `time_recovery_economics` | `related_to` | `decision_compression_systems` |
| `time_recovery_economics` | `related_to` | `simplicity_arbitrage` |
| `time_recovery_economics` | `related_to` | `complexity_compression_theory` |
| `signal_audit_framework` | `related_to` | `complexity_compression_theory` |
| `signal_audit_framework` | `related_to` | `organizational_memory_infrastructure` |
| `signal_audit_framework` | `related_to` | `decision_compression_systems` |
| `founder_prediction_error_model` | `related_to` | `curse_of_capability` |
| `founder_prediction_error_model` | `related_to` | `organizational_memory_infrastructure` |
| `founder_prediction_error_model` | `related_to` | `success_simulation_mapping` |

## Frameworks → Skills (composition)

| Framework | Relation | Skill |
|---|---|---|
| `signal_audit_framework` | `composed_by` | `ghost_note_detection` |
| `signal_audit_framework` | `composed_by` | `iterative_error_compression` |
| `signal_audit_framework` | `composed_by` | `core_communication_protocol` |
| `founder_prediction_error_model` | `composed_by` | `iterative_error_compression` |
| `founder_prediction_error_model` | `composed_by` | `ghost_note_detection` |
| `founder_prediction_error_model` | `composed_by` | `time_horizon_arbitrage` |
| `organizational_memory_infrastructure` | `composed_by` | `ghost_note_detection` |
| `organizational_memory_infrastructure` | `composed_by` | `iterative_error_compression` |
| `curse_of_capability` | `composed_by` | `ghost_note_detection` |
| `curse_of_capability` | `composed_by` | `adaptive_tension_tolerance` |
| `curse_of_capability` | `composed_by` | `core_communication_protocol` |
| `simplicity_arbitrage` | `composed_by` | `ghost_note_detection` |
| `decision_compression_systems` | `composed_by` | `adaptive_tension_tolerance` |
| `decision_compression_systems` | `composed_by` | `iterative_error_compression` |
| `decision_compression_systems` | `composed_by` | `decision_compression` |
| `success_simulation_mapping` | `composed_by` | `time_horizon_arbitrage` |
| `time_recovery_economics` | `composed_by` | `time_horizon_arbitrage` |

## Agents → Skills + Frameworks (orchestration)

| Agent | Relation | Target |
|---|---|---|
| `transcript_synthesis_agent` | `composes` | `ghost_note_detection` |
| `transcript_synthesis_agent` | `applies_to` | `golden_opportunity_strategist` |
| `golden_opportunity_strategist` | `composes` | `ghost_note_detection` |
| `golden_opportunity_strategist` | `composes` | `iterative_error_compression` |
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
| `moat_detection_agent` | `composes` | `organizational_memory_infrastructure` |
| `moat_detection_agent` | `composes` | `decision_compression_systems` |
| `moat_detection_agent` | `composes` | `simplicity_arbitrage` |

## Scoring

| Source | Relation | Target |
|---|---|---|
| `golden_opportunity_score` | `scores` | `golden_opportunity_strategist` |
| `moat_strength_score` | `scores` | `moat_detection_agent` |
| `moat_strength_score` | `scores` | `moat_detection` |
| `timing_asymmetry_score` | `scores` | `golden_opportunity_strategist` |

## Aliases

| Source | Relation | Target |
|---|---|---|
| `ghost_note_detection` | `alias_of` | `absence_detection` |
