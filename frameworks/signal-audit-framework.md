---
id: signal_audit_framework
name: Signal Audit Framework
type: strategic_framework
version: 1.1
status: active
use_when:
  - assessing the health of a company's perception layer
  - auditing what a founder, team, or board is and is not noticing
  - diligence on an opportunity where the narrative seems too clean
  - establishing a baseline before deploying AI agents into a business
  - separating decision-relevant metrics from vanity metrics
  - sequencing where to invest before adding more tools or headcount
avoid_when:
  - the business is in pure execution mode against a settled thesis
  - the audit would consume more attention than the decision it informs
related_frameworks:
  - map_attribution_framework
  - applied_intelligence_stack
  - complexity_compression_theory
  - organizational_memory_infrastructure
  - decision_compression_systems
  - founder_prediction_error_model
skills_used:
  - ghost_note_detection
  - iterative_error_compression
  - core_communication_protocol
  - signal_hierarchy_analysis
  - founder_bottleneck_detection
related_doctrine:
  - signal_doctrine
  - founder_intelligence_system
inputs_required:
  - meeting_transcripts_or_recordings
  - dashboard_inventory
  - reporting_routines
  - decision_log_or_proxy
outputs:
  - perception_gap_map
  - signal_routing_diagnosis
  - listening_surface_score
  - true_signals
  - false_signals
  - missing_signals
  - noise_sources
  - immediate_leverage_points
  - recommended_listening_investments
diagnostic_questions:
  - What signals does this team look at every week, and which never come up?
  - Which dashboards are produced and never acted on?
  - When was the last time the team updated a belief based on data?
  - Where does the founder describe being "surprised" — and was that a signal someone else saw earlier?
  - What contrary signal has the team actively dismissed in the last 90 days?
  - What are we measuring that does not change behavior?
  - What do we believe is working but cannot prove?
  - What process creates repeated friction?
  - What activity gets credit without causal evidence?
  - What insight would change our next decision?
triggers:
  - decisions are surprising the founder repeatedly
  - the same kind of failure recurs across projects
  - dashboards exist without decisions attached
  - the team cannot list signals they would expect to see if their thesis were wrong
  - AI tooling has been added but no new signal has been routed to the team
  - "more data" is treated as the answer to a clarity problem
scoring_dimensions:
  - name: detection_coverage
    description: Fraction of expected signals (positive and contrary) that are actively monitored
    scale: 1-10
  - name: routing_quality
    description: How reliably detected signals reach a person who can act on them
    scale: 1-10
  - name: update_velocity
    description: How fast new signals translate into updated beliefs and decisions
    scale: 1-10
  - name: contrary_signal_tolerance
    description: Does the team metabolize contrary signal or dismiss it
    scale: 1-10
  - name: signal_to_noise_ratio
    description: How dense the dashboard layer is with decision-relevant metrics vs vanity metrics
    scale: 1-10
failure_modes:
  - Treating the audit as a one-time exercise instead of a routine
  - Auditing dashboards without auditing the meetings that interpret them
  - Confusing volume of monitored signals with quality of signal routing
  - Letting the audit become a witch hunt rather than a structural diagnosis
  - Producing a long list of true signals without naming the noise sources
confidence_model:
  low: Single audit cycle, signal map self-reported by the team
  medium: Multiple cycles, signal map cross-checked against actual decisions made
  high: Repeated audits showing measurable change in detection coverage and update velocity
---

# Signal Audit Framework

## Purpose
Diagnose the health of a company's *perception layer* — what signals it sees, what it misses, how reliably the seen signals reach decision-makers, and how fast the company updates its beliefs in response. The Signal Audit is to the listening surface what a financial audit is to the books.

## Problem It Solves
Most operators audit output. Few audit perception. The result is a class of failure that looks like execution problems but is actually noticing problems: the data was available, but nobody looked at it, nobody routed it, nobody updated.

This framework gives the noticing problem an explicit diagnostic — and a ranked output the team can act on.

## The Signal vs. Noise Test
> **A metric is signal if it supports a decision. A metric is noise if it creates attention without action.**

Apply this test to every metric, dashboard, channel, and behavior under audit. Anything that fails the test is a candidate for the noise list.

## Audit Categories

| Category | Signal Question |
|---|---|
| Revenue | What actually creates money? |
| Marketing | What creates qualified demand? |
| Sales | What creates trust and conversion? |
| Operations | What slows execution? |
| Data | What can be trusted? |
| AI | What should be augmented, automated, or ignored? |
| Founder | Where is judgment being overloaded? |

Each category produces its own signal/noise split plus a list of missing signals (the category's ghost notes).

## Core Components
1. **Detection inventory** — what is the team actively monitoring across the seven categories?
2. **Expected-signal map** — what *should* the team be monitoring, given its thesis?
3. **Routing trace** — when a signal is detected, who sees it and how quickly?
4. **Update trace** — when a signal is seen, how fast does a belief or decision change?
5. **Contrary-signal stress test** — what was the most recent piece of contrary signal, and what happened to it?

## Related Skills
- **Ghost Note Detection** — to identify the expected signals that are missing from the detection inventory
- **Signal Hierarchy Analysis** — to rank surviving signals by decision relevance
- **Iterative Error Compression** — to measure prediction-error reduction over audit cycles
- **Founder Bottleneck Detection** — for the Founder category
- **CORE Communication Protocol** — used when the audit surfaces a person whose perception is structurally degraded; the conversation matters

## Operating Logic
1. Gather one week of meeting transcripts, dashboards in active use, and reporting routines
2. For each of the seven audit categories, list the signals the team would expect to see if its current thesis is correct (positive and contrary)
3. Compare to the signals actually being routed and discussed
4. For each gap, classify: not collected, collected-but-not-routed, routed-but-not-acted-on
5. Apply the signal vs. noise test to every metric currently being tracked
6. Score each of the five dimensions; aggregate to a listening surface score
7. Produce the ranked output (see below) and the three highest-leverage routing investments

## Inputs
- Meeting recordings or transcripts (one week minimum)
- Dashboard inventory (URL or screenshot list)
- Recurring reporting routines (which reports, who reads them, when)
- Decision log or proxy (what changed in the last 30 days based on new information)

## Outputs
The audit produces a ranked list:
1. **True signals** — metrics and observations that actually change decisions
2. **False signals** — metrics being trusted that should not be
3. **Missing signals** — what should be measured but isn't
4. **Noise sources** — what consumes attention without changing action
5. **Immediate leverage points** — the smallest changes with the largest perception lift

Plus:
- A perception gap map (expected signal → status)
- Signal routing diagnosis (where the routing is breaking)
- Listening surface score (1–10)

## Scoring Logic
| Score | Meaning |
|---|---|
| 1 | Perception layer is structurally broken; team is flying blind |
| 3 | Detection happens; routing is poor; updates rare |
| 5 | Detection and routing OK; update velocity is the bottleneck |
| 7 | Strong listening surface; contrary signal is metabolized inconsistently |
| 10 | Listening surface is institutional; signals reach decisions reliably; contrary signal is actively sought |

## Failure Modes
- One-time audit instead of routine
- Auditing dashboards without auditing the meetings that interpret them
- Confusing volume of monitored signals with quality of signal routing
- Letting the audit become a witch hunt rather than a structural diagnosis
- Producing a long list of true signals without naming the noise sources

## Strategic Value
This framework treats *noticing* as an auditable, improvable capability — and gives the operator the artifacts to invest against it. Most other diagnostics treat noticing as a personal trait. It is not. It is infrastructure.

## Example Applications
- Pre-investment diligence on a founder whose thesis looks suspiciously clean
- Board-level audit before a year-end strategy planning cycle
- Baseline assessment before deploying an internal AI agent layer
- Diagnostic lead-in to a M.A.P. Attribution Framework engagement
- Lead magnet for founder-cognition advisory work

## Compression Summary
**Output gets audited every quarter. Perception is what needs the audit. A metric is signal only if it changes the next decision.**
