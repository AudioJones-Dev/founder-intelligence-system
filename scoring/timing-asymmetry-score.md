---
id: timing_asymmetry_score
name: Timing Asymmetry Score
type: scoring_rubric
version: 1.0
status: active
---

# Timing Asymmetry Score

## Purpose
Measure how favorable the *timing* is — i.e., whether the market shift creating this opportunity is early enough to capture, but real enough to act on.

## Diagnostic Questions
- Is the underlying shift already visible to incumbents?
- Is the buyer already aware of the new pain?
- Is the technology mature enough to deliver reliably?
- Is the cost of being early survivable?
- Is the cost of being late terminal?

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Too early — market does not yet exist |
| 3 | Early — requires expensive education |
| 5 | Emerging — buyers are searching but not buying |
| 7 | Window open — buyers are buying, category is forming |
| 9 | Sweet spot — buyers are buying, incumbents have not yet adapted |
| 10 | Final window — incumbents are about to adapt; act now |

## Component Dimensions
- **Buyer readiness** — are buyers actively shopping for this?
- **Technology readiness** — can the solution be delivered reliably today?
- **Incumbent latency** — how long until existing players respond?
- **Capital readiness** — is funding/buying activity warming?

## Output Format
```json
{
  "timing_asymmetry_score": 8,
  "dimensions": {
    "buyer_readiness": 8,
    "technology_readiness": 9,
    "incumbent_latency": 7,
    "capital_readiness": 7
  },
  "window_estimate": "12-24 months",
  "rationale": "..."
}
```

## Anti-Patterns
- Confusing "exciting" with "timely"
- Ignoring incumbent reaction time
- Treating buyer interest as buyer intent
