---
id: founder_prediction_error_model
name: Founder Prediction Error Model
type: strategic_framework
version: 1.1
status: active
use_when:
  - calibrating a founder's strategic judgment
  - diligence on a founder's track record where the wins are loud and the misses are silent
  - building an externalized memory layer where decisions feed back into improvement
  - coaching or being coached on decision quality
  - diagnosing why the founder is reactive, stressed, or stuck in a loop of misattribution
  - explaining why "more leads" or "better tools" isn't fixing the underlying problem
avoid_when:
  - the founder operates in a domain where prediction is structurally impossible (pure discovery, frontier R&D)
  - the predictions involved are one-off and unrepeatable
related_frameworks:
  - curse_of_capability
  - organizational_memory_infrastructure
  - success_simulation_mapping
  - signal_audit_framework
  - map_attribution_framework
  - applied_intelligence_stack
skills_used:
  - iterative_error_compression
  - ghost_note_detection
  - time_horizon_arbitrage
  - attribution_analysis
  - founder_bottleneck_detection
related_doctrine:
  - founder_intelligence_system
  - signal_doctrine
  - organizational_memory
inputs_required:
  - prior_predictions_with_dates
  - actual_outcomes
  - context_at_time_of_prediction
  - founder_role_description
outputs:
  - prediction_error_per_decision_class
  - calibration_drift
  - directional_error_pattern
  - misattribution_pattern
  - feedback_loop_quality_score
diagnostic_questions:
  - For your last ten meaningful decisions, what did you predict the outcome would be?
  - How does your prediction compare to the actual outcome?
  - In what direction do you systematically err — optimistic, pessimistic, scope, timing?
  - Which decision class shows the highest error?
  - When was the last time you updated your model of your own prediction error?
  - When the result did not match expectation, what did you attribute the gap to — and was that attribution validated?
triggers:
  - founder claims pattern-recognition strength without artifacts
  - the same kind of decision goes wrong repeatedly
  - "I knew it" appears retroactively without prior evidence
  - the founder is reaching for tools, hires, or campaigns and being surprised when they don't move the business
  - "more leads / better people / more content / more dashboards" is being prescribed as a fix for problems those things don't actually solve
  - AI tools are being deployed to "augment judgment" without a baseline of judgment quality
scoring_dimensions:
  - name: prediction_artifact_coverage
    description: Fraction of meaningful decisions for which a prior prediction exists
    scale: 1-10
  - name: calibration_quality
    description: How accurate the predictions are versus actual outcomes
    scale: 1-10
  - name: error_directionality
    description: Whether errors cluster in one direction (systemic bias) or distribute randomly
    scale: 1-10
  - name: misattribution_pattern
    description: How often the founder mis-diagnoses the cause of the prediction error
    scale: 1-10
  - name: feedback_loop_quality
    description: How reliably actual outcomes are compared to predictions and used to update the model
    scale: 1-10
failure_modes:
  - Treating retroactive narrative as evidence of foresight
  - Calibrating on a single class of decisions and over-generalizing
  - Confusing being right about outcomes with being right for the right reasons
  - Penalizing predictions that were correct conditional on information available at the time
  - Letting the framework be used as a blame tool rather than a calibration tool
confidence_model:
  low: Fewer than five paired predictions and outcomes; no clear pattern visible
  medium: Ten or more paired predictions; directional bias visible across a single decision class
  high: Many paired predictions across multiple decision classes; calibration improving cycle over cycle
---

# Founder Prediction Error Model

## Purpose
Diagnose what happens when a founder's expectation of how the business should behave **does not match** how the business actually behaves. The gap between mental model and reality is **prediction error**. Unmanaged, it produces confusion, stress, misattribution, and reactive decision-making — each of which compounds.

## Problem It Solves
Most founder track records are reported as a list of wins. Survivorship bias means the misses are silent, the wins are loud, and the actual quality of judgment is invisible. More importantly: when a prediction fails, founders routinely *misattribute* the cause — reaching for tools, hires, or campaigns that don't address the underlying issue. The model below names that pattern and gives the team a way to interrupt it.

## The Pattern (Seven Steps)

1. **Founder expects growth** from a tactic, hire, campaign, or tool.
2. **The expected result does not happen.**
3. **The founder experiences prediction error** — an uncomfortable mismatch between mental model and reality.
4. **The founder searches for relief.** The discomfort is the driver, not the diagnosis.
5. **The founder misattributes the problem.** Often to surface causes: tools, talent, content volume, more dashboards.
6. **The business adds more noise.** New tools, hires, automations, dashboards stack onto an already unclear system.
7. **The real bottleneck remains hidden** — and the cycle repeats next quarter with louder symptoms.

This pattern is the single most common reason founder-led businesses plateau without anyone naming the plateau.

## Common Misattributions

| Symptom | Wrong Attribution | Better Diagnostic Lens |
|---|---|---|
| Leads are low | "We need more ads" | Offer / message / channel mismatch |
| AI is not working | "We need better tools" | Broken system architecture (`applied_intelligence_stack`) |
| Team is slow | "We need better people" | Process ambiguity, undocumented judgment |
| Content is not converting | "We need more content" | Weak positioning, missing hook |
| Data is confusing | "We need more dashboards" | No signal hierarchy |
| Sales is stalling | "We need a better closer" | Trust gap upstream of the call |
| Customers don't renew | "We need a CSM" | Outcome attribution unclear; product not embedded in workflow |

The Founder Prediction Error Model exists to catch these substitutions before they become operating decisions.

## Core Components
1. **Prediction inventory** — for each meaningful decision, what was the prediction?
2. **Outcome inventory** — what actually happened?
3. **Pairing** — match predictions to outcomes, accounting for incomplete information
4. **Error classification** — by direction (optimistic/pessimistic), by class (hiring, pricing, product, market), by timing (early/late)
5. **Misattribution audit** — when the founder explained the prediction error, did the explanation hold up against the data?
6. **Feedback loop audit** — how reliably does the founder go back and check?

## Related Skills
- **Iterative Error Compression** — the underlying loop this framework operationalizes at the strategic level
- **Ghost Note Detection** — to find the predictions that were never made because the founder felt the answer was obvious
- **Time Horizon Arbitrage** — to weight predictions by their natural time horizon (a quarterly prediction errs differently than a five-year one)
- **Attribution Analysis** — to validate or invalidate the founder's misattribution candidates
- **Founder Bottleneck Detection** — to surface the structural source of the prediction error (often the founder is the missing system layer)

## Operating Logic
1. Collect the last 10–20 meaningful decisions
2. Reconstruct the prediction the founder made at the time (or note its absence)
3. Pair each prediction with the actual outcome
4. Classify errors by direction, class, and timing
5. For each error, capture the founder's *attribution* at the time and validate it against the Misattribution Table
6. Score each of the five dimensions
7. Identify the highest-leverage *calibration debt* — the class of decision where error is large, recurring, directional, and misattributed

## Inputs
- Prior predictions with dates and context
- Actual outcomes
- The reasoning available at the time of prediction
- The founder's current role across the Applied Intelligence Stack layers

## Outputs
- Prediction error per decision class
- Calibration drift over time
- Directional error pattern (where the founder systematically errs)
- Misattribution pattern (which kinds of wrong-causes the founder reaches for)
- Feedback loop quality score
- Recommended calibration moves

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | No paired prediction/outcome data exists; judgment is unmeasurable |
| 3 | Partial data; errors are large, directional, and misattributed |
| 5 | Calibration baseline exists; corrections are inconsistent |
| 7 | Calibration is routine; errors compressed across at least one cycle |
| 10 | Founder operates with explicit, versioned prediction artifacts; calibration improves monotonically |

## Failure Modes
- Treating retroactive narrative as evidence of foresight
- Calibrating on a single class of decisions and over-generalizing
- Confusing being right about outcomes with being right for the right reasons
- Penalizing predictions that were correct conditional on information available at the time
- Letting the framework be used as a blame tool rather than a calibration tool

## Strategic Value
A founder with measurable calibration is a structurally different asset from one without. The first compounds judgment; the second does not. In an AI era where many agents and copilots will *amplify* founder judgment, calibration quality determines whether amplification is leverage or noise.

The misattribution table also doubles as a sales / advisory diagnostic: when a founder describes one of those symptoms, the better diagnostic lens points to the framework that actually addresses the problem.

## Example Applications
- Founder diligence in an acquisition or investment context
- Self-applied calibration discipline by a working founder
- Coaching engagements where the coach needs an artifact, not a vibe
- Baseline before an AI copilot is wired into the founder's decision loop
- Quarterly review structure that catches misattribution before it becomes a budget decision

## Core Claim

> **Founders do not only need more information. They need a better predictive model of their own business.**

## Compression Summary
**Pair predictions to outcomes. Audit the attribution. Calibrate. Anything else is a story.**
