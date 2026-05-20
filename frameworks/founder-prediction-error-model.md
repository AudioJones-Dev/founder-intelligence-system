---
id: founder_prediction_error_model
name: Founder Prediction Error Model
type: strategic_framework
version: 1.0
status: active
use_when:
  - calibrating a founder's strategic judgment
  - diligence on a founder's track record where the wins are loud and the misses are silent
  - building an externalized memory layer where decisions feed back into improvement
  - coaching or being coached on decision quality
avoid_when:
  - the founder operates in a domain where prediction is structurally impossible (pure discovery, frontier R&D)
  - the predictions involved are one-off and unrepeatable
related_frameworks:
  - curse_of_capability
  - organizational_memory_infrastructure
  - success_simulation_mapping
skills_used:
  - iterative_error_compression
  - ghost_note_detection
  - time_horizon_arbitrage
related_doctrine:
  - founder_intelligence_system
  - signal_doctrine
  - organizational_memory
inputs_required:
  - prior_predictions_with_dates
  - actual_outcomes
  - context_at_time_of_prediction
outputs:
  - prediction_error_per_decision_class
  - calibration_drift
  - directional_error_pattern
  - feedback_loop_quality_score
diagnostic_questions:
  - For your last ten meaningful decisions, what did you predict the outcome would be?
  - How does your prediction compare to the actual outcome?
  - In what direction do you systematically err — optimistic, pessimistic, scope, timing?
  - Which decision class shows the highest error?
  - When was the last time you updated your model of your own prediction error?
triggers:
  - founder claims pattern-recognition strength without artifacts
  - the same kind of decision goes wrong repeatedly
  - "I knew it" appears retroactively without prior evidence
  - hiring, pricing, or product bets are made on intuition that has never been calibrated
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
  - name: feedback_loop_quality
    description: How reliably actual outcomes are compared to predictions and used to update the model
    scale: 1-10
failure_modes:
  - Treating retroactive narrative as evidence of foresight
  - Calibrating on a single class of decisions and over-generalizing
  - Confusing being right about outcomes with being right for the right reasons
  - Penalizing predictions that were correct conditional on information available at the time
confidence_model:
  low: Fewer than five paired predictions and outcomes; no clear pattern visible
  medium: Ten or more paired predictions; directional bias visible across a single decision class
  high: Many paired predictions across multiple decision classes; calibration improving cycle over cycle
---

# Founder Prediction Error Model

## Purpose
Calibrate a founder's strategic judgment by measuring the gap between what they predicted and what actually happened — across a representative sample of meaningful decisions. The output is a structural assessment of where their model of the world is reliable, where it is biased, and where the feedback loop has decayed.

## Problem It Solves
Most founder track records are reported as a list of wins. Survivorship bias means the misses are silent, the wins are loud, and the actual quality of judgment is invisible. Without paired prediction-and-outcome data, "I have great judgment" is unfalsifiable.

This framework forces the paired data into existence — and gives it a scoring rubric.

## Core Components
1. **Prediction inventory** — for each meaningful decision, what was the prediction?
2. **Outcome inventory** — what actually happened?
3. **Pairing** — match predictions to outcomes, accounting for incomplete information
4. **Error classification** — by direction (optimistic/pessimistic), by class (hiring, pricing, product, market), by timing (early/late)
5. **Feedback loop audit** — how reliably does the founder go back and check?

## Related Skills
- **Iterative Error Compression** — the underlying loop this framework operationalizes at the strategic level
- **Ghost Note Detection** — to find the predictions that were never made because the founder felt the answer was obvious
- **Time Horizon Arbitrage** — to weight predictions by their natural time horizon (a quarterly prediction errs differently than a five-year one)

## Operating Logic
1. Collect the last 10–20 meaningful decisions
2. Reconstruct the prediction the founder made at the time (or note its absence)
3. Pair each prediction with the actual outcome
4. Classify errors by direction, class, and timing
5. Score each of the four dimensions
6. Identify the highest-leverage *calibration debt* — the class of decision where error is large, recurring, and directional

## Inputs
- Prior predictions with dates and context
- Actual outcomes
- The reasoning available at the time of prediction

## Outputs
- Prediction error per decision class
- Calibration drift over time
- Directional error pattern (where the founder systematically errs)
- Feedback loop quality score
- Recommended calibration moves

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | No paired prediction/outcome data exists; judgment is unmeasurable |
| 3 | Partial data; errors are large and directional but uncorrected |
| 5 | Calibration baseline exists; corrections are inconsistent |
| 7 | Calibration is routine; errors compressed across at least one cycle |
| 10 | Founder operates with explicit, versioned prediction artifacts; calibration improves monotonically |

## Failure Modes
- Treating retroactive narrative as evidence of foresight
- Calibrating on a single class of decisions and over-generalizing
- Confusing being right about outcomes with being right for the right reasons
- Penalizing predictions that were correct conditional on information available at the time

## Strategic Value
A founder with measurable calibration is a structurally different asset from one without. The first compounds judgment; the second does not. In an AI era where many agents and copilots will *amplify* founder judgment, calibration quality determines whether amplification is leverage or noise.

## Example Applications
- Founder diligence in an acquisition or investment context
- Self-applied calibration discipline by a working founder
- Coaching engagements where the coach needs an artifact, not a vibe
- Baseline before an AI copilot is wired into the founder's decision loop

## Compression Summary
**Pair predictions to outcomes. Calibrate. Anything else is a story.**
