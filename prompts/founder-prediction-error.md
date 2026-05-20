---
id: founder_prediction_error_prompt
name: Founder Prediction Error Prompt
type: prompt
version: 1.0
status: active
wraps_agent: ais_diagnostic_agent
loads:
  doctrine:
    - founder_intelligence_system
    - signal_doctrine
    - organizational_memory
  frameworks:
    - founder_prediction_error_model
    - signal_audit_framework
    - map_attribution_framework
  skills:
    - iterative_error_compression
    - ghost_note_detection
    - time_horizon_arbitrage
    - attribution_analysis
    - founder_bottleneck_detection
  templates:
    - opportunity-brief-template
output_schema: opportunity.schema.json
---

# Founder Prediction Error Prompt

## When To Use This
Use this prompt when:
- The founder is reaching for tools, hires, or campaigns and being surprised when they don't move the business
- "More leads / better people / more content / more dashboards" is being prescribed as a fix
- The same kind of decision keeps going wrong, with different surface explanations
- An advisory engagement is starting and a calibration baseline is needed
- An AI copilot or agent is about to be wired into the founder's decision loop and you want to know the baseline judgment quality

## Required Inputs
- **Last 10-20 meaningful decisions** with dates and context
- **The prediction the founder made at the time** (or note its absence)
- **The actual outcome**
- **The founder's attribution at the time** — when the result didn't match expectation, what did they blame?
- **Current role of the founder** across the Applied Intelligence Stack layers

## The Prompt

```
You are operating inside the Founder Intelligence System repository. Load:

- doctrine/founder-intelligence-system.md
- doctrine/signal-doctrine.md
- doctrine/organizational-memory.md
- frameworks/founder-prediction-error-model.md
- frameworks/signal-audit-framework.md
- frameworks/map-attribution-framework.md
- skills/iterative-error-compression.md
- skills/ghost-note-detection.md
- skills/time-horizon-arbitrage.md
- skills/attribution-analysis.md
- skills/founder-bottleneck-detection.md

Use ONLY the canonical frameworks, skills, and doctrine listed above.
Do not invent frameworks, skills, or scoring rubrics.
Use the Misattribution Table from frameworks/founder-prediction-error-model.md verbatim.

Run a Founder Prediction Error Analysis against the input I will provide:

1. PREDICTION INVENTORY:
   - For each meaningful decision, capture:
     - Decision name + date
     - Prediction the founder made (or NULL if no prediction was made)
     - Founder's confidence level at the time
     - Time horizon of the decision
   - Apply `ghost_note_detection` to flag decisions where NO prediction was made because the founder felt the answer was obvious

2. OUTCOME PAIRING:
   - For each prediction, pair with actual outcome
   - Compute the prediction error (direction, magnitude, timing)

3. ERROR CLASSIFICATION:
   - By direction: optimistic / pessimistic / scope / timing
   - By class: hiring, pricing, product, market, operational, AI/tooling
   - By time horizon: weight using `time_horizon_arbitrage` (a quarterly prediction errs differently than a five-year one)

4. MISATTRIBUTION AUDIT:
   - For each prediction error, capture the founder's ATTRIBUTION at the time ("I thought X would work but it didn't because Y")
   - Cross-reference against the Misattribution Table in `frameworks/founder-prediction-error-model.md`
   - For each attribution, classify: validated | unvalidated | likely-misattribution
   - Apply `attribution_analysis` to test the strongest misattribution candidates

5. PATTERN DETECTION:
   - Where does the founder systematically err? (direction, class, time horizon, misattribution type)
   - Apply the seven-step pattern (expectation → mismatch → discomfort → search for relief → misattribution → more noise → bottleneck hidden) — where is the team currently in the loop?

6. FOUNDER BOTTLENECK MAPPING:
   - Apply `founder_bottleneck_detection` against the misattribution pattern
   - Often, prediction error reveals a missing system layer the founder is filling in for

7. CALIBRATION DEBT:
   - Highest-leverage class of decision to calibrate next
   - Smallest move that would tighten calibration

8. OUTPUT:
   - Conform to `templates/opportunity-brief-template.md` with Founder Prediction Error sections
   - Score each of the five dimensions:
     - prediction_artifact_coverage
     - calibration_quality
     - error_directionality
     - misattribution_pattern
     - feedback_loop_quality

Anti-patterns to avoid:
- Treating retroactive narrative as evidence of foresight
- Penalizing predictions that were correct conditional on information available at the time
- Using the analysis as a blame tool rather than a calibration tool
- Confusing being right about outcomes with being right for the right reasons
- Mixing distribution-layer slogans into the structured output

Input follows.
```

## Expected Output Structure

```
# Founder Prediction Error Brief: [Founder / Business]

## Prediction Coverage
- Decisions with paired predictions: [N / 10]
- Decisions where no prediction was made: [...]

## Error Pattern
- Directional bias: [optimistic / pessimistic / scope / timing]
- Highest-error decision class: [...]
- Time-horizon effects: [...]

## Misattribution Audit
- Misattributions identified: [...]
- Better diagnostic lens per misattribution: [from Misattribution Table]
- Validated attributions: [...]

## Current Loop Position
- Where the team currently is in the seven-step pattern: [step + evidence]

## Founder Bottleneck
- Which system layer the founder is filling in for: [from `applied_intelligence_stack`]
- Externalization move to interrupt the loop: [...]

## Calibration Debt
- Highest-leverage class to calibrate: [...]
- Smallest move: [...]

## Scoring
- Prediction artifact coverage: [1-10]
- Calibration quality: [1-10]
- Error directionality: [1-10]
- Misattribution pattern: [1-10]
- Feedback loop quality: [1-10]
```

## Warnings
- The Misattribution Table is canonical; do not edit it inline. If a new symptom-to-attribution pattern emerges, recommend a framework version bump rather than inventing in the brief.
- If prediction artifacts are completely missing (no paired predictions for any meaningful decision), the immediate output is "calibration debt is total" + a recommendation to begin a prediction journal — not a fabricated calibration score.
