---
id: signal_audit_prompt
name: Signal Audit Prompt
type: prompt
version: 1.0
status: active
wraps_agent: founder_intelligence_diagnostic_agent
loads:
  doctrine:
    - signal_doctrine
    - founder_intelligence_system
  frameworks:
    - signal_audit_framework
  skills:
    - signal_hierarchy_analysis
    - ghost_note_detection
    - founder_bottleneck_detection
    - iterative_error_compression
    - core_communication_protocol
  templates:
    - opportunity-brief-template
output_schema: opportunity.schema.json
---

# Signal Audit Prompt

## When To Use This
Use this prompt when:
- The team is producing more dashboards than decisions
- "More data" or "better dashboards" is being prescribed for a clarity problem
- The founder is being repeatedly surprised by outcomes the team could have seen
- An AI initiative is about to be deployed on top of an unclear signal layer
- Lead-magnet diagnostic for a founder cognition / advisory engagement

## Required Inputs
- **Meeting transcripts or recordings** (one week minimum) — what is actually being discussed
- **Dashboard inventory** — every dashboard currently consulted
- **Reporting routines** — which reports, who reads them, when
- **Decision log (or proxy)** — what changed in the last 30 days based on new information
- **Team's current thesis** — what does the team believe is true about the business?

## The Prompt

```
You are operating inside the Founder Intelligence System repository. Load:

- doctrine/signal-doctrine.md
- doctrine/founder-intelligence-system.md
- frameworks/signal-audit-framework.md
- skills/signal-hierarchy-analysis.md
- skills/ghost-note-detection.md
- skills/founder-bottleneck-detection.md
- skills/iterative-error-compression.md
- skills/core-communication-protocol.md

Use ONLY the canonical frameworks, skills, and doctrine listed above.
Do not invent frameworks, skills, or scoring rubrics.
Apply the signal vs. noise test: a metric is signal only if it changes the next decision.

Run a Signal Audit against the input I will provide:

1. EXPECTED-SIGNAL MAP:
   - Given the team's stated thesis, list the signals (positive and contrary) that SHOULD exist if the thesis is correct
   - Use `ghost_note_detection` to surface the conspicuously missing signals

2. DETECTION INVENTORY:
   - Against the seven Signal Audit categories (Revenue, Marketing, Sales, Operations, Data, AI, Founder)
   - For each category, list:
     - What is being actively monitored
     - What is showing up in meetings or decisions
     - What is missing

3. SIGNAL HIERARCHY:
   - Apply `signal_hierarchy_analysis` to the metric inventory
   - Produce four ranked lists:
     - TRUE signals (metrics that actually change decisions)
     - FALSE signals (metrics being trusted that should not be)
     - MISSING signals (what should be measured but isn't)
     - NOISE sources (what consumes attention without changing action)

4. ROUTING + UPDATE TRACE:
   - For each detected signal, where does it land? Who sees it? How fast does a belief or decision change as a result?
   - Score detection_coverage, routing_quality, update_velocity, contrary_signal_tolerance, signal_to_noise_ratio (1-10 each)

5. FOUNDER LAYER:
   - Apply `founder_bottleneck_detection` to the Founder category specifically
   - Where is judgment being overloaded?
   - Which signals are routing through the founder unnecessarily?

6. IMMEDIATE LEVERAGE POINTS:
   - The smallest changes with the largest perception lift
   - Ordered by leverage; each one named explicitly

7. OUTPUT:
   - Conform to `templates/opportunity-brief-template.md` with Signal Audit-specific sections
   - Include the listening surface score (1-10) with rationale per dimension
   - Name the three highest-leverage routing investments

Anti-patterns to avoid:
- Producing a long list of true signals without naming noise sources to retire
- Auditing dashboards without auditing the meetings that interpret them
- Treating "more dashboards" as the output
- Conflating volume of signals with quality of routing
- Making the audit feel like a witch hunt rather than a structural diagnosis

Input follows.
```

## Expected Output Structure

```
# Signal Audit Brief: [Business / Team]

## Expected vs. Actual
- Expected signals: [...]
- Actual signals: [...]
- Gaps: [not-collected | collected-not-routed | routed-not-acted-on]

## Signal Hierarchy
- True signals (decision-relevant): [...]
- False signals (retire): [...]
- Missing signals (add): [...]
- Noise sources (retire aggressively): [...]

## Routing + Update
- Detection coverage: [1-10]
- Routing quality: [1-10]
- Update velocity: [1-10]
- Contrary-signal tolerance: [1-10]
- Signal-to-noise ratio: [1-10]
- Listening surface score (composite): [1-10]

## Founder Layer
- Bottlenecks: [classified inventory]
- Decisions misrouted through founder: [...]

## Immediate Leverage Points
1. [Smallest change, largest lift]
2. [...]
3. [...]
```

## Warnings
- Do not produce findings against draft-status frameworks without flagging maturity
- Do not promote distribution-layer language ("you do not have an AI problem...") into the structured output — that lives in `meta/distribution-notes.md`
- If the audit surfaces an attribution gap that warrants a M.A.P. pass, recommend the hand-off rather than running M.A.P. inside this prompt
