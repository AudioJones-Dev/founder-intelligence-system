# Decision Compression

## Purpose
Condense high-noise decision discussions into minimal, durable records that preserve assumptions, tradeoffs, and chosen direction.

## Core Principle
A decision record should be short enough to retrieve quickly and rich enough to recreate reasoning.

## Inputs
- Raw transcript or notes
- Decision alternatives considered
- Stated constraints and assumptions

## Outputs
- One-page decision artifact
- Structured fields for rationale and tradeoffs
- Follow-up checkpoints

## Detection Logic
Trigger when a decision thread exceeds manageable length, involves multiple tradeoffs, or shows repeated reinterpretation across teams.

## Operational Questions
- What was decided and why?
- Which assumptions must remain true?
- Which signal would invalidate this decision?

## AI Agent Usage
Use as post-meeting extraction primitive and as pre-execution context pack for downstream agents.

## Failure Modes
- Omitting minority concerns that later become critical
- Flattening uncertainty into false certainty
- Capturing outcomes without decision logic

## Related Skills
- ghost-note-detection
- moat-detection

## Compression Summary
Convert noisy discussion into compact strategic memory without losing causality.
