# Routing Logic

Routing maps incoming reasoning tasks to the right doctrine context, framework path, and skill primitives.

## Routing order

1. Classify intent type (diagnostic, strategic, operational, epistemic).
2. Load relevant doctrine constraints.
3. Select framework(s) that fit the problem shape.
4. Execute required skill sequence.
5. Return structured outputs aligned to schema contracts.

## Design rules

- Prefer deterministic routing over implicit heuristic jumps.
- Keep route definitions explicit and inspectable.
- Record fallback routes for ambiguity handling.
