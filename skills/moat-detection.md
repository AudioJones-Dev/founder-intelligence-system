---
id: moat_detection
name: Moat Detection
type: skill
version: 1.0
status: active
purpose: Distinguish a durable, compounding competitive advantage from a temporary execution lead — by classifying the source of the advantage and stress-testing it against erosion paths.
origin:
  - Moat detection agent / workflow library
  - Hamilton Helmer's 7 Powers
  - Repeated diligence pattern observations
inputs:
  - business_model
  - source_of_current_advantage
  - competitor_landscape
  - operating_history
outputs:
  - moat_class_classification
  - moat_strength_estimate
  - deepening_moves
  - erosion_risks
triggers:
  - the operator describes "first mover advantage" as a moat
  - the only thing protecting the business is current quality of execution
  - the business has scaled fast but no asymmetry is visible
  - acquisition diligence and the value depends on something not yet named
  - AI capability is being treated as a moat
operational_logic:
  - Identify the current source of advantage in one sentence
  - Map it against the moat classes (compounding memory, decision compression ownership, simplicity lock-in, workflow embedding, judgment externalization, distribution asymmetry)
  - For each class that applies, score 0-10 on durability and depth
  - Aggregate using the moat strength rubric
  - List the moves that would deepen the strongest class and the events that would erode it
failure_modes:
  - Confusing "first mover" with moat
  - Treating capability as moat when it is just current quality
  - Ignoring distribution and workflow embedding in favor of product features
  - Counting a moat that exists only in the founder's head
confidence_model:
  low: Single moat class identified; no historical evidence of compounding
  medium: Multiple classes identified; some evidence of compounding over at least one cycle
  high: Multiple classes stacked; measurable compounding across multiple cycles; documented competitor failed-to-erode events
related_skills:
  - ghost_note_detection
  - iterative_error_compression
used_by_frameworks:
  - organizational_memory_infrastructure
  - decision_compression_systems
  - simplicity_arbitrage
used_by_agents:
  - moat_detection_agent
  - golden_opportunity_strategist
---

# Moat Detection

## Purpose
The atomic skill of looking at a business and accurately naming whether its current advantage will compound, hold, or erode. This skill exists because most operators conflate execution quality with durability.

## Core Principle
A moat is a property of the *structure* of the business, not of its current performance. Execution quality is a leading indicator. Moat is the answer to: when execution quality is matched, what remains?

## Inputs
- A one-sentence description of the current source of advantage
- The competitive landscape and the threats actively on the horizon
- A read of the business model — recurring revenue, switching costs, distribution, judgment locus

## Outputs
- Classification into one or more of the six moat classes (see below)
- A moat strength estimate, 1–10
- A list of "deepening moves" — actions that would strengthen the strongest class
- A list of "erosion risks" — events that would invalidate the moat

## Detection Logic

### The Six Moat Classes
1. **Compounding Memory** — the business gets smarter with every customer or cycle
2. **Decision Compression Ownership** — the business owns the decisions, not just the data
3. **Simplicity Lock-In** — competitor complexity feels like a downgrade
4. **Workflow Embedding** — removal would require redesigning a process
5. **Judgment Externalization** — proprietary judgment is in systems, not people
6. **Distribution Asymmetry** — the business reaches buyers at a cost competitors cannot match

For full operational definitions of each class, see `agents/moat-detection-agent.md`.

## Operational Questions
1. What is the *current* source of advantage, in one sentence?
2. If a competitor matched today's execution quality, what would remain?
3. Which of the six moat classes applies — and which is the *strongest*?
4. What event would have to occur for the moat to disappear?
5. How long does the moat hold if the founder leaves?

## AI Agent Usage
An agent invoking this skill should:
1. Accept a business model description and competitive context
2. Classify against the six moat classes with rationale per class
3. Return a moat strength score per the rubric in `scoring/moat-strength-score.md`
4. Surface the deepening moves and erosion risks

## Failure Modes
- Confusing "first mover" with moat — being first is not a structure
- Treating capability as moat when it is just current quality of execution
- Ignoring distribution and workflow embedding in favor of product features
- Counting a moat that exists only in the founder's head — that is not a moat, it is a fuse

## Related Skills
- `ghost_note_detection` — to surface the moat classes that are conspicuously *absent*
- `iterative_error_compression` — to measure whether the moat is actually compounding over time

## Compression Summary
**The moat is what remains when execution quality is matched. Everything else is a lead.**
