---
id: map_attribution_framework
name: M.A.P. Attribution Framework
type: strategic_framework
version: 1.0
status: active
use_when:
  - the business measures activity but cannot explain causality
  - dashboards multiply but decision quality stagnates
  - marketing spend is being optimized against last-click or last-touch only
  - the founder cannot answer "why did this work?" with confidence
  - planning the next quarter without a causal model of the previous one
  - building a forward-looking growth plan that must survive contact with reality
avoid_when:
  - the business is pre-revenue with no measurable outcomes yet
  - the time horizon of the decision is shorter than the measurement cycle
  - the cost of causal attribution exceeds the value of the decision it would inform
related_frameworks:
  - signal_audit_framework
  - founder_prediction_error_model
  - decision_compression_systems
  - applied_intelligence_stack
skills_used:
  - attribution_analysis
  - causal_inference_analysis
  - signal_hierarchy_analysis
  - ghost_note_detection
  - decision_compression
related_doctrine:
  - signal_doctrine
  - founder_intelligence_system
inputs_required:
  - business_outcome_definition
  - candidate_metrics_inventory
  - channel_and_touchpoint_inventory
  - historical_outcome_data
outputs:
  - signal_dashboard
  - causal_map
  - growth_decision_model
diagnostic_questions:
  - What are we tracking, and why?
  - Does this metric connect to revenue, trust, or action?
  - What caused this lead, this conversion, this retention event?
  - What touchpoint created belief?
  - What are we over-crediting?
  - Where should we invest next, given what we now know?
  - What signal predicts conversion?
  - What bottleneck limits growth?
triggers:
  - leadership uses words like "ROAS", "last click", or "impressions" as proxies for impact
  - the same metric appears on every dashboard but no one cites it in a decision
  - performance attribution gets adjudicated by who argued hardest
  - AI tools have been added to "improve marketing" without a baseline causal model
scoring_dimensions:
  - name: measurement_clarity
    description: Are we tracking the right things, and only the right things?
    scale: 1-10
  - name: attribution_strength
    description: How confidently can we move from correlation to causation?
    scale: 1-10
  - name: prediction_quality
    description: Can the team use attribution to make forward bets that hold up?
    scale: 1-10
failure_modes:
  - Treating clicks/views/sessions as attribution rather than as activity
  - Over-relying on last-click in multi-touch journeys
  - Adding more dashboards instead of a smaller, signal-dense one
  - Confusing high-confidence correlation with causation
  - Letting attribution debates be won by seniority rather than evidence
  - Using attribution to assign blame rather than to update the model
confidence_model:
  low: Measurement layer in place; attribution is inference from correlations only
  medium: Attribution layer in place across a representative sample of outcomes; some causal claims tested against holdouts
  high: Predictions made from attribution have been validated across multiple cycles; the model improves as new data arrives
---

# M.A.P. Attribution Framework

## Purpose
Move the business from **tracking activity** to **understanding causality** to **predicting where effort, money, and attention should go next.**

Most businesses get stuck at measurement: more dashboards, more metrics, more reports. Measurement is necessary but not sufficient. Without attribution, measurement produces correlation. Without prediction, attribution produces a postmortem. M.A.P. is the staircase: **Measurement → Attribution → Prediction.**

## Problem It Solves
Operators routinely confuse three things:

- **Analytics** tells you *what happened*. (Clicks, leads, revenue.)
- **Attribution** tells you *why it happened*. (Which touchpoint, message, system created the outcome.)
- **Prediction** tells you *what to do next*. (Where to invest, what to cut, what to test.)

When a team operates only at the analytics layer, it accumulates dashboards without compounding judgment. M.A.P. forces the team up the staircase deliberately.

## Core Components

### M — Measurement
**Goal:** Build the minimum viable measurement system — only metrics that support a decision.

**Operational questions:**
- What are we tracking?
- Why are we tracking it?
- Does this metric connect to revenue, trust, or action?
- Is this signal or noise?
- What decision does this metric support?

**Output:** A clean signal dashboard with only decision-relevant metrics. Everything else gets retired.

### A — Attribution
**Goal:** Move from correlation to causation.

**Operational questions:**
- What created the lead?
- What increased trust?
- What moved the prospect from awareness to action?
- What channel assisted conversion?
- What touchpoint created belief?
- What are we over-crediting?

**Output:** A causal map of the buyer journey — the actual sequence and weight of touchpoints that produce outcomes, with named uncertainties.

### P — Prediction
**Goal:** Use what caused previous outcomes to make better future decisions.

**Operational questions:**
- Where should we invest next?
- What should we stop doing?
- What signal predicts conversion?
- What activity compounds?
- What bottleneck limits growth?

**Output:** A prioritized growth plan based on causal confidence — explicit about which bets are derived from strong attribution and which are still hypotheses.

## Related Skills
- **Attribution Analysis** — the atomic skill of separating cause from correlation in a given outcome stream
- **Causal Inference Analysis** — the atomic skill of stress-testing a claimed causal relationship
- **Signal Hierarchy Analysis** — the atomic skill of ranking metrics by their decision relevance
- **Ghost Note Detection** — used to surface the metrics that *should* be measured but aren't
- **Decision Compression** — used when M.A.P. produces a long list of candidate next moves and the team needs the smallest one that matters

## Operating Logic
1. Inventory every metric currently being tracked across the business
2. For each metric, name the decision it supports — discard the ones without one
3. For each remaining metric, classify it as activity, leading, or outcome
4. For the outcomes the team cares most about, run an attribution pass: list candidate causes, weight them by evidence, name the gaps
5. Stress-test the strongest attribution claims (holdouts, ablation, incrementality tests where feasible)
6. From the validated attribution map, produce a prediction layer: where to invest next, what to stop, what to test
7. Score the three layers (measurement / attribution / prediction) — the lowest score is the bottleneck

## Inputs
- The business outcome the team wants to drive
- An inventory of current metrics and dashboards
- A list of channels, touchpoints, and systems suspected of contributing
- Historical outcome data with enough cycles for attribution to be possible

## Outputs
- A signal dashboard (decision-relevant metrics only)
- A causal map of the buyer or operational journey
- A prioritized growth decision model

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Pure activity tracking; no attribution; no predictive model |
| 3 | Measurement layer is decent; attribution is hand-wavy |
| 5 | Attribution claims exist but are unvalidated |
| 7 | Validated attribution across at least one cycle; predictions are explicit |
| 10 | All three layers are running continuously; predictions improve as new data arrives |

## M.A.P. Diagnostic Table

| Stage | Question | Output |
|---|---|---|
| Measurement | What matters? | Signal dashboard |
| Attribution | What caused it? | Causal map |
| Prediction | What should happen next? | Growth decision model |

## Failure Modes
- Treating clicks/views/sessions as attribution rather than as activity
- Over-relying on last-click in multi-touch journeys
- Adding more dashboards instead of a smaller, signal-dense one
- Confusing high-confidence correlation with causation
- Letting attribution debates be won by seniority rather than evidence
- Using attribution to assign blame rather than to update the model

## Strategic Value
A business that operates the M.A.P. loop continuously compounds judgment cycle over cycle. A business that operates only the measurement layer accumulates dashboards. The first produces growth that survives leadership transitions; the second produces growth that depends on the founder remembering which dashboard mattered.

## Example Applications
- Marketing ROI clarity (which channel actually creates qualified demand)
- Lead-source attribution and disqualifying low-causal channels
- Campaign performance evaluation against holdouts
- Revenue intelligence baselines before deploying AI agents into the funnel
- Quarterly planning grounded in causal evidence rather than narrative

## Compression Summary
**Analytics tells you what happened. Attribution tells you why. Prediction tells you what to do next. Most teams stop at the first.**
