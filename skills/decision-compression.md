---
id: decision_compression
name: Decision Compression
type: skill
version: 1.0
status: active
purpose: Identify which decisions in a given workflow should not exist, and compress them into defaults, recommendations, or pre-resolved paths.
origin:
  - Decision Compression Systems framework
  - Cognitive load research on choice paralysis
  - Operating playbooks of high-velocity teams
inputs:
  - decision_inventory
  - workflow_trace
  - role_description
outputs:
  - eliminable_decision_list
  - default_candidates
  - recommendation_candidates
  - misrouted_decision_list
triggers:
  - the same decision recurs with the same answer 80% of the time
  - decisions block waiting on a person who can't add new information
  - meetings exist primarily to make a decision someone could have defaulted
  - AI produces options rather than resolving them
  - dashboards display information no one acts on
operational_logic:
  - List all decisions made in the target workflow over one week
  - For each decision, tag its frequency, owner, average resolution time, and stability of correct answer
  - Sort by frequency × stability — high-frequency, stable-answer decisions are the strongest candidates for defaults
  - For each candidate, draft the default value and the condition under which the default should be overridden
  - For the rest, identify which can be compressed into a recommendation (system suggests; human confirms) versus eliminated entirely
failure_modes:
  - Compressing rare, high-stakes decisions that genuinely need deliberation
  - Treating a recommendation system as compression when it still requires confirmation for every step
  - Defaulting decisions the operator is paid specifically to make
  - Replacing decision-making with option-generation
confidence_model:
  low: One workflow trace; defaults proposed but not validated against historical decisions
  medium: Multiple traces; defaults validated against at least one cycle of historical decisions
  high: Defaults running in production with measured outcome parity to the manual baseline
related_skills:
  - ghost_note_detection
  - iterative_error_compression
used_by_frameworks:
  - decision_compression_systems
  - complexity_compression_theory
used_by_agents:
  - golden_opportunity_strategist
  - moat_detection_agent
---

# Decision Compression

## Purpose
The atomic skill of looking at a workflow, finding the decisions that should not exist, and proposing the smallest change that makes them go away — by default, by recommendation, or by elimination.

## Core Principle
A decision is only valuable when its outcome varies with the deciding person's judgment. Every other decision is friction.

## Inputs
- An inventory of decisions made in the target workflow
- Frequency, owner, average resolution time per decision
- The stability of the "correct" answer over time

## Outputs
- The list of decisions that can be eliminated outright
- The list of decisions that can be defaulted
- The list of decisions that should become recommendations (system proposes; human confirms)
- The list of decisions that are misrouted — being made above or below their proper level

## Detection Logic
Apply this skill when:
- The operator describes feeling decision-saturated
- AI tools have *increased* the number of choices rather than resolved them
- The same disagreement keeps recurring in different meetings
- Founder-level approval is in the path of decisions a manager could own

## Operational Questions
1. What is the *frequency* of this decision per week?
2. What is the *stability* of the correct answer — how often does it differ from last time?
3. Who is making it — and is that the right level?
4. What is the *cost of being wrong* once vs. the *cost of deciding* every time?
5. What would the default be, and what condition should override it?

## AI Agent Usage
An agent invoking this skill should:
1. Accept a structured decision log
2. Return a table of decisions classified into `eliminate | default | recommend | keep`
3. For each `default` and `recommend` entry, return the proposed default value and override condition
4. Conform output to a future `decision-compression.schema.json` (planned)

## Failure Modes
- Compressing rare, high-stakes decisions that genuinely need deliberation
- Treating a recommendation system as compression when it still requires confirmation for every step
- Defaulting decisions the operator is *paid* specifically to make
- Replacing decision-making with option-generation — the cardinal AI-era error

## Related Skills
- `ghost_note_detection` — to surface decisions that should exist but aren't being made
- `iterative_error_compression` — to validate that compressed defaults match the manual baseline over time

## Compression Summary
**A decision worth keeping is one whose outcome depends on the person making it. Compress all the others.**
