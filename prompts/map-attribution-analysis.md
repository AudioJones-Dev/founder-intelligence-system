---
id: map_attribution_analysis_prompt
name: M.A.P. Attribution Analysis Prompt
type: prompt
version: 1.0
status: active
wraps_agent: ais_diagnostic_agent
loads:
  doctrine:
    - signal_doctrine
    - founder_intelligence_system
  frameworks:
    - map_attribution_framework
    - signal_audit_framework
  skills:
    - attribution_analysis
    - causal_inference_analysis
    - signal_hierarchy_analysis
    - ghost_note_detection
  templates:
    - opportunity-brief-template
output_schema: opportunity.schema.json
---

# M.A.P. Attribution Analysis Prompt

## When To Use This
Use this prompt when:
- A founder or operator cannot confidently answer "why did this work?"
- The team is making spend, hiring, or strategic decisions based on last-click / last-touch attribution
- An AI tool or campaign was added and "isn't moving the business"
- The next quarter's plan is being built and you want a causal model behind it

## Required Inputs
- **Outcome:** the business outcome to attribute (revenue, retention, qualified lead, trust signal). Name it precisely.
- **Metric inventory:** every metric currently being tracked across the business
- **Channel / touchpoint inventory:** every channel, message, system, or decision suspected of contributing
- **Historical data:** at least one cycle of outcome data plus the timeline of touchpoints
- **Decision log (or proxy):** what changed in the last 30 days based on what we thought we knew

## The Prompt

```
You are operating inside the Founder Intelligence System repository. Load:

- doctrine/signal-doctrine.md
- doctrine/founder-intelligence-system.md
- frameworks/map-attribution-framework.md
- frameworks/signal-audit-framework.md
- skills/attribution-analysis.md
- skills/causal-inference-analysis.md
- skills/signal-hierarchy-analysis.md
- skills/ghost-note-detection.md

Use ONLY the canonical frameworks, skills, and doctrine listed above.
Do not invent frameworks, skills, or scoring rubrics.
Do not promote draft-status frameworks (e.g., niche_framework) to canonical claims.
If a needed concept is missing, name the gap rather than fabricating it.

Run a M.A.P. Attribution Analysis against the input I will provide:

1. MEASUREMENT layer:
   - Apply `signal_hierarchy_analysis` to the metric inventory.
   - Produce the minimum viable signal set (decision-relevant metrics only).
   - Name what is being measured that does NOT change behavior; list it as noise to retire.

2. ATTRIBUTION layer:
   - Apply `attribution_analysis` against the outcome and candidate causes.
   - Produce a weighted causal map with explicit confidence levels (low / medium / high per `confidence_model`).
   - Name what is being over-credited and under-credited.
   - For the strongest causal claim, apply `causal_inference_analysis` (confounders, alternative explanations, reverse-causation paths, falsifiers).

3. PREDICTION layer:
   - From the validated attribution map, produce a prioritized growth decision model:
     - Where to invest next
     - What to stop
     - What signal predicts conversion
     - What activity compounds
     - What bottleneck limits growth
   - Mark each prediction as derived from "validated attribution" or "hypothesis" — do not blur the line.

4. GAPS:
   - Apply `ghost_note_detection` to identify the metrics, touchpoints, and causes that SHOULD be in the model but are missing.
   - List the smallest validation moves (holdout / ablation / incrementality) that would tighten attribution next cycle.

5. OUTPUT:
   - Conform to `templates/opportunity-brief-template.md` with M.A.P.-specific sections.
   - Conform to `schemas/opportunity.schema.json` for the structured output.
   - Include the maturity flag on any draft-status framework if invoked.

Anti-patterns to avoid:
- Treating clicks/views/sessions as attribution rather than activity
- Over-relying on last-click in multi-touch journeys
- Producing a causal map without uncertainty labels
- Using attribution to assign blame rather than to update the model
- Substituting more dashboards for the minimum viable signal set
- Mixing distribution-layer language ("you don't have an AI problem, you have a signal problem") into the structured output (that's for `meta/distribution-notes.md`, not canonical output)

Input follows.
```

## Expected Output Structure

```
# M.A.P. Attribution Brief: [Outcome]

## Measurement
- Minimum viable signal set: [...]
- Noise sources retired: [...]

## Attribution
- Causal map: [touchpoint → weighted contribution with confidence]
- Over-credited: [...]
- Under-credited: [...]
- Causal Inference pass on strongest claim:
  - Confounders: [...]
  - Alternative explanations: [...]
  - Falsifiers: [...]
  - Revised confidence: [...]

## Prediction
- Invest next: [validated | hypothesis]
- Stop doing: [validated | hypothesis]
- Compounding signals: [...]
- Limiting bottleneck: [...]

## Gaps + Next Moves
- Missing signals: [...]
- Validation moves (ranked): [...]

## Confidence
- Measurement: [low | medium | high]
- Attribution: [low | medium | high]
- Prediction: [low | medium | high]
```

## Warnings
- Do not allow the prompt to produce a prediction layer that isn't grounded in the attribution layer
- Do not allow the agent to invent a new framework if the existing M.A.P. framework feels incomplete — name the gap, escalate to a framework-extraction pass
