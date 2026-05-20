---
id: attribution_analysis
name: Attribution Analysis
type: skill
version: 1.0
status: active
purpose: Identify what actually caused an observed outcome by separating cause from correlation, weighting candidate causes by evidence, and naming the gaps where attribution cannot yet be made cleanly.
origin:
  - M.A.P. Attribution Framework (Audio Jones)
  - Holdout testing and incrementality literature
  - Multi-touch attribution practice from performance marketing
inputs:
  - outcome_definition
  - candidate_causes_inventory
  - timeline_of_touchpoints
  - historical_outcome_data
outputs:
  - causal_map
  - weighted_attribution
  - over_credited_factors
  - under_credited_factors
  - attribution_gaps
  - holdout_or_validation_candidates
triggers:
  - the team is using last-click attribution in a multi-touch journey
  - attribution debates are being adjudicated by seniority rather than evidence
  - the same channel is being credited for every outcome
  - a campaign "worked" but no one can explain why
  - the team is about to scale spend against a channel without a causal model
operational_logic:
  - Name the outcome precisely — revenue, retention, qualified lead, trust signal, etc.
  - Inventory candidate causes — channels, touchpoints, messages, systems, decisions
  - For each candidate, gather evidence of contribution (timing, sequence, holdout data if available)
  - Weight candidates by evidence strength; explicitly mark inferences vs. validated causal claims
  - Identify what is being over-credited and what is being under-credited
  - Name the attribution gaps — what would need to be true for a causal claim to hold
  - Propose holdout, ablation, or incrementality tests for the highest-stakes claims
failure_modes:
  - Treating correlation as causation when timing happens to line up
  - Anchoring on the first hypothesis and confirming rather than competing it
  - Over-relying on the last touchpoint just because it's the easiest to measure
  - Producing an attribution map without naming the uncertainty
  - Using attribution to assign blame rather than to update the model
confidence_model:
  low: Single outcome cycle; attribution based on timing + inference only
  medium: Multiple cycles; at least one causal claim tested against a holdout or natural experiment
  high: Continuous attribution with validated causal claims across multiple cycles; predictions hold up
related_skills:
  - causal_inference_analysis
  - signal_hierarchy_analysis
  - ghost_note_detection
used_by_frameworks:
  - map_attribution_framework
  - signal_audit_framework
  - founder_prediction_error_model
  - niche_framework
used_by_agents:
  - ais_diagnostic_agent
  - golden_opportunity_strategist
---

# Attribution Analysis

## Purpose
The atomic skill of taking an outcome and producing a defensible causal explanation — with named uncertainties, explicit over-credits and under-credits, and a list of validation moves that would tighten the model next cycle.

## Core Principle
Attribution is not measurement. Attribution answers *why* an outcome happened, not *what* happened. Confusing the two is the most common failure mode in operator decision-making.

## Inputs
- A precisely-named outcome (revenue, retention, conversion, trust signal, etc.)
- An inventory of candidate causes (channels, touchpoints, messages, systems, decisions)
- The timeline of touchpoints and decisions leading to the outcome
- Historical outcome data — at least enough cycles to spot patterns

## Outputs
- A causal map (touchpoint → outcome weight)
- A weighted attribution claim with explicit confidence levels
- A list of over-credited factors
- A list of under-credited factors
- A list of attribution gaps (what we'd need to know to make a stronger claim)
- A list of candidate holdout / ablation / incrementality tests

## Detection Logic
Apply this skill when:
- The team is making spend or scaling decisions based on last-click or last-touch attribution
- Attribution debates are being settled by argument rather than evidence
- A campaign "worked" but no one can name the causal mechanism
- A channel is being credited for every outcome (red flag)
- The next decision depends on knowing *why* the previous outcome occurred

## Operational Questions
1. What is the outcome, named precisely?
2. What are *all* the plausible causes — including the boring ones?
3. For each candidate cause, what evidence supports its contribution? What evidence would falsify it?
4. Which cause is being over-credited? Which is being under-credited?
5. What test (holdout, ablation, incrementality) would let us update the attribution with confidence?

## AI Agent Usage
An agent invoking this skill should:
1. Accept an outcome definition + candidate causes + timeline + historical data
2. Return a weighted attribution map with confidence levels
3. Explicitly mark which weights are inferences vs. validated causal claims
4. Output a ranked list of validation moves

## Failure Modes
- Treating correlation as causation when timing happens to line up
- Anchoring on the first hypothesis and confirming rather than competing it
- Over-relying on the last touchpoint just because it's the easiest to measure
- Producing an attribution map without naming the uncertainty
- Using attribution to assign blame rather than to update the model

## Related Skills
- `causal_inference_analysis` — for stress-testing a specific causal claim
- `signal_hierarchy_analysis` — for picking the right outcome to attribute against
- `ghost_note_detection` — for surfacing the candidate causes nobody mentioned

## Compression Summary
**Attribution names *why*. If you can't name what would falsify your attribution, you have a correlation, not a cause.**
