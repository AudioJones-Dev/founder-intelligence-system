---
id: success_simulation_mapping
name: Success Simulation Mapping
type: strategic_framework
version: 1.0
status: active
use_when:
  - evaluating scalability
  - testing whether growth breaks the model
  - identifying future bottlenecks
  - pre-mortem on a strategy
  - assessing acquisition targets
avoid_when:
  - business is in pure discovery (no model to simulate)
related_frameworks:
  - curse_of_capability
  - complexity_compression_theory
  - organizational_memory_infrastructure
inputs_required:
  - current_business_model
  - growth_target
  - delivery_constraints
outputs:
  - breakage_points
  - capacity_constraints
  - structural_redesign_needs
---

# Success Simulation Mapping

## Core Definition
Project the business forward at its desired scale and locate the points where the current model breaks. Success is the stress test, not the goal.

## Core Question
If this business succeeded at 10x, what would break first?

## Diagnostic Signals
- the founder cannot describe what 10x looks like operationally
- hiring plan exists, but org design does not
- the same model is assumed to work at any scale
- "we'll figure it out when we get there" appears in planning
- delivery quality already wavers under current load
- the model only works because volume is currently low

## Diagnostic Questions
- At 10x customers, who delivers the work?
- At 10x revenue, what does the org chart look like?
- At 10x volume, which process breaks first?
- At 10x scale, what does the founder do?
- At 10x, which competitor enters the market?

## Opportunity Pattern
Most businesses are optimized for the size they are, not the size they want to be. Mapping the simulated future reveals which structures must be redesigned *before* growth, not after.

## Use This Framework To Evaluate
- early-stage SaaS planning to scale
- agencies considering productization
- service businesses considering acquisition
- founder transitions
- pricing-model decisions

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Model is structurally ready for 10x |
| 3 | Minor reinforcement needed |
| 5 | Visible breakage at 3–5x |
| 7 | Model breaks well before 10x |
| 10 | Current model cannot support meaningful scale |

## Scoring Dimensions
- **Delivery scalability** — can delivery scale without linear headcount
- **Decision scalability** — can decisions scale without founder bottleneck
- **Knowledge scalability** — does institutional knowledge survive hiring
- **Economic scalability** — do unit economics improve, hold, or break with scale

## Strategic Output
If score is 7+, the structural redesign must precede the growth investment. Otherwise growth amplifies the existing breakage.

## Common Failure Modes
- Simulating revenue without simulating delivery
- Assuming the founder simply "delegates more"
- Treating org design as a hiring problem instead of a system problem
