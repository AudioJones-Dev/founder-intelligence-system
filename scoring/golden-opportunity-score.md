---
id: golden_opportunity_score
name: Golden Opportunity Score
type: scoring_rubric
version: 1.0
status: active
---

# Golden Opportunity Score

## Purpose
A composite score (1–10) summarizing whether an opportunity meets the bar of "golden" — asymmetric upside, durable moat potential, scalable model.

## Inputs
- Framework scores (each 1–10)
- Moat strength score (1–10)
- Timing asymmetry score (1–10)
- Market size estimate (qualitative)

## Scoring Logic
| Score | Meaning |
|---|---|
| 1–3 | Not a golden opportunity. Pass. |
| 4–5 | Real opportunity, but not asymmetric. Consider only if execution cost is very low. |
| 6–7 | Strong opportunity. Worth a focused pursuit. |
| 8–9 | Golden opportunity. Asymmetric upside with defensibility. |
| 10 | Generational opportunity. Move fast, commit capital. |

## Component Weights
- Framework-derived strategic fit: **40%**
- Moat strength: **30%**
- Timing asymmetry: **20%**
- Market size: **10%**

## Disqualifiers (auto-cap at 5)
- No defensibility beyond execution
- Founder bottleneck unresolved
- Requires market education the founder cannot fund
- Unit economics break at projected scale

## Output Format
```json
{
  "golden_opportunity_score": 8,
  "components": {
    "strategic_fit": 9,
    "moat_strength": 8,
    "timing_asymmetry": 7,
    "market_size": "large"
  },
  "rationale": "...",
  "disqualifiers_triggered": []
}
```
