# Routing

The routing layer translates detected signals into framework and agent invocations. This file is the canonical reference for how signals route through the Founder Intelligence System.

The schema this routes against: `schemas/routing.schema.json`.

## Signal → Framework Map

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

## Combination Rules

Framework combinations that produce stronger diagnoses than either alone:

- `curse_of_capability` + `organizational_memory_infrastructure` → **founder-led service business diagnostic**
- `complexity_compression_theory` + `simplicity_arbitrage` → **category disruption thesis**
- `decision_compression_systems` + `time_recovery_economics` → **premium AI product pricing thesis**
- `success_simulation_mapping` + `curse_of_capability` → **pre-scale structural redesign**
- `signal_audit_framework` + `founder_prediction_error_model` → **founder cognition audit**
- `organizational_memory_infrastructure` + `founder_prediction_error_model` → **knowledge moat assessment**

## Skip Rules

When a framework's `avoid_when` condition fires, the router records the skip with rationale rather than running the framework. Skip decisions are first-class outputs.

## Agent Hand-off Contracts

```
transcript-synthesis-agent
   ↓ produces extraction conforming to routing.schema.json
golden-opportunity-strategist
   ↓ produces frameworks-applied output
moat-detection-agent
   ↓ produces moat-strength output
[composite scoring]
   ↓ produces brief conforming to opportunity.schema.json
```

## Versioning

This routing map is v1.0. New frameworks must be added here when they are added to `frameworks/`. Removal requires a deprecation entry, not deletion.
