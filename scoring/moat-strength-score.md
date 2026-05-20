---
id: moat_strength_score
name: Moat Strength Score
type: scoring_rubric
version: 1.0
status: active
---

# Moat Strength Score

## Purpose
Quantify the durability of the competitive advantage on a 1–10 scale, using the moat classes from `agents/moat-detection-agent.md`.

## Inputs
For each moat class, score 0–10:
- Compounding memory
- Decision compression ownership
- Simplicity lock-in
- Workflow embedding
- Judgment externalization
- Distribution asymmetry

## Aggregation
Moat strength score = **maximum** class score, with bonus:
- +1 if two classes score ≥ 7
- +2 if three or more classes score ≥ 7
- Capped at 10

This rewards stacked moats rather than averaging strong moats down.

## Scoring Logic
| Score | Meaning |
|---|---|
| 1–3 | No durable moat |
| 4–5 | Short-term advantage |
| 6–7 | Defensible for several years |
| 8–9 | Structural, compounding moat |
| 10 | Multi-class compounding moat |

## Output Format
```json
{
  "moat_strength_score": 8,
  "class_scores": {
    "compounding_memory": 9,
    "decision_compression_ownership": 7,
    "simplicity_lock_in": 5,
    "workflow_embedding": 8,
    "judgment_externalization": 6,
    "distribution_asymmetry": 4
  },
  "rationale": "...",
  "deepening_moves": ["..."],
  "erosion_risks": ["..."]
}
```
