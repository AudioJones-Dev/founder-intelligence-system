---
id: decision_compression_systems
name: Decision Compression Systems
type: strategic_framework
version: 1.0
status: active
use_when:
  - buyers need fewer decisions
  - founders are cognitively overloaded
  - AI creates more output than clarity
  - evaluating workflow products
  - designing internal operating systems
avoid_when:
  - decision quality requires deliberation (high-stakes, low-frequency)
  - user is paid specifically to make these decisions
related_frameworks:
  - complexity_compression_theory
  - simplicity_arbitrage
  - organizational_memory_infrastructure
skills_used:
  - decision_compression
  - signal_hierarchy_analysis
  - iterative_error_compression
inputs_required:
  - decision_inventory
  - decision_frequency
  - decision_owner
outputs:
  - decision_load_score
  - automation_candidates
  - default_setting_opportunities
---

# Decision Compression Systems

## Core Definition
A decision compression system removes, defaults, or pre-resolves decisions so that the operator (or buyer) faces fewer choices to reach the same or better outcome.

## Core Question
Which decisions in this workflow should not exist?

## Diagnostic Signals
- repeated decisions with the same answer
- decisions made by the wrong person (founder deciding what a manager should)
- decisions blocked waiting for context
- AI generating options instead of resolving them
- meetings that exist only to make a decision someone could have defaulted
- dashboards with no decision attached

## Diagnostic Questions
- How many decisions per week does the founder personally make?
- Which of those decisions have the same answer 80% of the time?
- Where does AI produce options instead of recommendations?
- What decisions could be eliminated with a better default?
- What decisions exist only because the system has no memory?

## Opportunity Pattern
The next generation of tools wins by *compressing* decisions, not by producing more output. Defaults, recommendations, and pre-resolved paths beat dashboards and option-generators.

## Use This Framework To Evaluate
- AI agents and copilots
- internal ops systems
- founder workflows
- onboarding flows
- pricing and packaging

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Decisions are already well-compressed |
| 3 | Some redundant decisions |
| 5 | Meaningful decision drag |
| 7 | Operator is decision-saturated |
| 10 | The system manufactures decisions faster than humans can resolve them |

## Scoring Dimensions
- **Decision volume** — number of decisions per role per week
- **Repeatability** — % of decisions with a stable correct answer
- **Locus mismatch** — % of decisions made above their proper level
- **AI-induced load** — decisions newly created by AI output

## Strategic Output
If score is 7+, build (or buy) a system that resolves, defaults, or absorbs the high-frequency decisions before they hit a human.

## Common Failure Modes
- Building recommendation engines that still require human confirmation for every step
- Compressing the wrong decisions (rare, high-stakes ones)
- Replacing decision-making with option-generation
