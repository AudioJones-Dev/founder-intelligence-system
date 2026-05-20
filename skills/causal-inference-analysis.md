---
id: causal_inference_analysis
name: Causal Inference Analysis
type: skill
version: 1.0
status: active
purpose: Stress-test a specific claimed causal relationship — given a claim that X caused Y, surface confounders, alternative explanations, falsifiers, and the smallest validation move that could move the claim from "plausible" to "supported".
origin:
  - Standard causal inference methodology (confounders, counterfactuals, falsifiability)
  - M.A.P. Attribution Framework (the deeper layer beneath Attribution Analysis)
  - Decision-theory practice in pre-mortems
inputs:
  - causal_claim
  - supporting_evidence
  - context_in_which_outcome_occurred
outputs:
  - confounder_inventory
  - alternative_explanations
  - falsifiers
  - validation_proposal
  - revised_confidence_level
triggers:
  - a single causal claim is about to drive a meaningful investment, hire, or strategic pivot
  - the team treats "we ran the campaign and revenue went up" as proof
  - a finding is being escalated to "we know" without a falsification pass
  - the strongest attribution claim from an Attribution Analysis pass is being acted on
  - the founder is making a prediction whose accuracy will be judged later
operational_logic:
  - Restate the causal claim precisely (X caused Y under conditions Z)
  - Inventory plausible confounders — third variables that could explain both X and Y
  - Inventory plausible alternative explanations — other things that could have caused Y
  - Inventory plausible reverse-causation paths — could Y have caused X
  - For each, name what would have to be true for that explanation to dominate
  - Propose the smallest validation move (holdout, natural experiment, counterfactual analysis) that would update the claim
  - Output a revised confidence level for the original claim
failure_modes:
  - Anchoring on the original claim and pattern-matching evidence to it
  - Treating "I can't think of a confounder" as evidence there isn't one
  - Designing a validation move that the original claim cannot fail
  - Confusing statistical significance with causal validity
  - Producing a list of confounders without actually updating the claim's confidence
confidence_model:
  low: Initial pass against a single claim; no validation moves run
  medium: At least one structured falsification move applied; confidence revised based on result
  high: Claim has survived multiple validation cycles against fresh data
related_skills:
  - attribution_analysis
  - ghost_note_detection
  - iterative_error_compression
used_by_frameworks:
  - map_attribution_framework
  - founder_prediction_error_model
  - success_simulation_mapping
used_by_agents:
  - ais_diagnostic_agent
  - golden_opportunity_strategist
---

# Causal Inference Analysis

## Purpose
The atomic skill of taking a *single* causal claim — "X caused Y" — and stress-testing it before the team builds policy around it. Where Attribution Analysis produces the causal map across many factors, Causal Inference Analysis is the falsification pass on the strongest individual claim.

## Core Principle
A causal claim that cannot be falsified is not a claim. It is a narrative. Narratives are valuable for storytelling and destructive for resource allocation.

## Inputs
- A specific causal claim (X caused Y under conditions Z)
- The supporting evidence the team is currently relying on
- Context about the conditions in which the outcome occurred

## Outputs
- A confounder inventory (third variables that could explain both X and Y)
- A list of alternative explanations (other things that could have caused Y)
- A list of reverse-causation paths (could Y have caused X)
- A set of explicit falsifiers (what would have to be true to invalidate the claim)
- A proposed validation move
- A revised confidence level for the original claim

## Detection Logic
Apply this skill when:
- A single causal claim is about to drive an investment, hire, or pivot
- "We ran the campaign and revenue went up" is being treated as proof
- The strongest claim from an Attribution Analysis pass is being acted on
- A founder is making a prediction whose accuracy will be judged later
- The cost of being wrong about this specific cause is large

## Operational Questions
1. Restate the claim with the conditions made explicit
2. What third variables could plausibly explain both X and Y?
3. What other causes could have produced Y in this context?
4. Could Y have caused X (reverse causation)?
5. What would have to be observed to falsify the claim?
6. What is the smallest validation move that could move the confidence level meaningfully?

## AI Agent Usage
An agent invoking this skill should:
1. Accept a single causal claim + supporting evidence + context
2. Return the confounder, alternative-explanation, and reverse-causation inventories
3. Output the proposed falsifiers and validation move
4. Return a revised confidence level with rationale

## Failure Modes
- Anchoring on the original claim and pattern-matching evidence to it
- Treating "I can't think of a confounder" as evidence there isn't one
- Designing a validation move the claim cannot fail
- Confusing statistical significance with causal validity
- Producing a list of confounders without actually updating the claim's confidence

## Related Skills
- `attribution_analysis` — produces the map; this skill stress-tests the highest-stakes edge
- `ghost_note_detection` — for surfacing the confounders nobody named
- `iterative_error_compression` — for the multi-cycle calibration loop

## Compression Summary
**A causal claim that cannot be falsified is not a claim. It is a narrative.**
