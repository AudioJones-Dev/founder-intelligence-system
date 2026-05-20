---
id: signal_hierarchy_analysis
name: Signal Hierarchy Analysis
type: skill
version: 1.0
status: active
purpose: Rank a set of metrics, observations, or signals by their decision relevance — separating decision-supporting signals from attention-consuming noise, and producing a minimum viable signal set the operator can actually use.
origin:
  - Signal Doctrine
  - The signal vs. noise test ("a metric is signal only if it changes the next decision")
  - Audio Jones Signal Audit Framework
inputs:
  - metric_inventory
  - dashboard_inventory
  - reporting_routine_inventory
  - decision_inventory
outputs:
  - true_signals
  - false_signals
  - missing_signals
  - noise_sources
  - minimum_viable_signal_set
triggers:
  - the team has more dashboards than decisions
  - the same metric appears on every report but is cited in no decisions
  - "more data" is being prescribed for a clarity problem
  - someone is asking which KPI to look at next
  - AI tools have been added to the dashboard layer without a baseline
operational_logic:
  - List every metric currently being tracked across the business
  - For each metric, name the decision it supports — if none, it is a candidate for the noise list
  - Classify surviving metrics as activity, leading, or outcome
  - For each remaining metric, score: how often is it consulted, how often does it change behavior, how confident is the team in its reliability
  - Identify the missing metrics — the signals that should exist given the team's thesis but do not
  - Output the ranked signal set (true / false / missing / noise) plus a minimum viable signal set
failure_modes:
  - Confusing "lots of metrics" with "lots of signal"
  - Keeping metrics out of inertia rather than evidence
  - Treating activity metrics (clicks, opens, sessions) as outcome signals
  - Allowing political pressure to keep noise metrics on the dashboard
  - Producing a long list of true signals without naming the noise sources to retire
confidence_model:
  low: Single-pass triage; no historical evidence of which metrics actually changed behavior
  medium: Triage cross-checked against a decision log for the last quarter
  high: Triage validated across multiple cycles; minimum viable signal set has held up
related_skills:
  - ghost_note_detection
  - attribution_analysis
  - decision_compression
used_by_frameworks:
  - signal_audit_framework
  - map_attribution_framework
  - applied_intelligence_stack
  - niche_framework
used_by_agents:
  - golden_opportunity_strategist
  - founder_intelligence_diagnostic_agent
---

# Signal Hierarchy Analysis

## Purpose
The atomic skill of taking a sprawling set of metrics, observations, and signals and producing the smallest set the operator actually needs to make better decisions. Everything else gets named as noise and retired.

## Core Principle
A metric is **signal** only if it changes the next decision. Anything else is noise — even if it is technically correct, well-tracked, and historically interesting.

## Inputs
- Inventory of every metric currently tracked
- Inventory of every dashboard currently consulted
- Inventory of recurring reporting routines (which reports, who reads them, when)
- A decision log (or proxy) for the last quarter

## Outputs
- **True signals** — metrics that demonstrably support decisions
- **False signals** — metrics being trusted that should not be
- **Missing signals** — what should be measured but isn't
- **Noise sources** — what consumes attention without changing action
- **Minimum viable signal set** — the smallest set the operator can run the business with

## Detection Logic
Apply this skill when:
- The team is producing more dashboards than decisions
- "More data" is being prescribed as the fix for a clarity problem
- A founder describes feeling overwhelmed by metrics without knowing which ones matter
- An AI / tooling investment is being made on top of an unclear signal layer

## Operational Questions
1. For each metric, name the decision it supports — if you can't, retire it
2. Is this an activity metric, a leading indicator, or an outcome?
3. How often is this metric consulted, and how often does the team's behavior change as a result?
4. What metric would *change our next decision* that we are not currently tracking?
5. What metric is on the dashboard out of inertia rather than evidence?

## AI Agent Usage
An agent invoking this skill should:
1. Accept a structured metric inventory + decision log
2. Return four lists (true / false / missing / noise) plus the minimum viable signal set
3. For each retired metric, name the decision it failed to support
4. Conform to a future `signal-hierarchy.schema.json` (planned)

## Failure Modes
- Confusing "lots of metrics" with "lots of signal"
- Keeping metrics out of inertia rather than evidence
- Treating activity metrics (clicks, opens, sessions, leads) as outcome signals
- Allowing political pressure to keep noise metrics on the dashboard
- Producing a long list of true signals without naming the noise sources to retire

## Related Skills
- `ghost_note_detection` — for surfacing the missing-signal list
- `attribution_analysis` — for promoting a leading-indicator candidate to true-signal status
- `decision_compression` — for retiring metrics that fail the decision-support test

## Compression Summary
**Signal supports a decision. Noise consumes attention. Keep the first list short. Retire the second list aggressively.**
