# Ghost Note Detection

## Purpose
Identify notes, commitments, or assumptions that are repeatedly referenced in decisions but absent from the canonical knowledge base.

## Core Principle
If a decision depends on information that cannot be reliably retrieved, that information is a ghost note and a strategic risk.

## Inputs
- Meeting transcript excerpts
- Decision logs
- Task assignments referencing prior context
- Existing knowledge base entries

## Outputs
- Ghost note candidate list
- Confidence score per candidate
- Recommended extraction actions

## Detection Logic
Find references to "as discussed", "already decided", or implicit assumptions without linkable source artifacts. Flag patterns with repeated downstream dependency.

## Operational Questions
- Which active decisions depend on non-retrievable context?
- What missing notes have the highest operational consequence?
- Which teams are carrying unrecorded assumptions?

## AI Agent Usage
Use before planning, escalation, or strategic review cycles to reduce hidden-context errors.

## Failure Modes
- Over-flagging harmless shorthand as missing context
- Ignoring verbal-only commitments with high impact
- Confusing inaccessible data with nonexistent data

## Related Skills
- decision-compression
- moat-detection

## Compression Summary
Surface decision-critical context that exists socially but not structurally.
