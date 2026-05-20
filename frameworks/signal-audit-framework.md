---
id: signal_audit_framework
name: Signal Audit Framework
type: strategic_framework
version: 1.0
status: active
use_when:
  - assessing the health of a company's perception layer
  - auditing what a founder, team, or board is and is not noticing
  - diligence on an opportunity where the narrative seems too clean
  - establishing a baseline before deploying AI agents into a business
avoid_when:
  - the business is in pure execution mode against a settled thesis
  - the audit would consume more attention than the decision it informs
related_frameworks:
  - complexity_compression_theory
  - organizational_memory_infrastructure
  - decision_compression_systems
skills_used:
  - ghost_note_detection
  - iterative_error_compression
  - core_communication_protocol
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
  - recommended_listening_investments
diagnostic_questions:
  - What signals does this team look at every week, and which never come up?
  - Which dashboards are produced and never acted on?
  - When was the last time the team updated a belief based on data?
  - Where does the founder describe being "surprised" — and was that a signal someone else saw earlier?
  - What contrary signal has the team actively dismissed in the last 90 days?
triggers:
  - decisions are surprising the founder repeatedly
  - the same kind of failure recurs across projects
  - dashboards exist without decisions attached
  - the team cannot list signals they would expect to see if their thesis were wrong
  - AI tooling has been added but no new signal has been routed to the team
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
failure_modes:
  - Treating the audit as a one-time exercise instead of a routine
  - Auditing dashboards without auditing the meetings that interpret them
  - Confusing volume of monitored signals with quality of signal routing
  - Letting the audit become a witch hunt rather than a structural diagnosis
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

This framework gives the noticing problem an explicit diagnostic.

## Core Components
1. **Detection inventory** — what is the team actively monitoring?
2. **Expected-signal map** — what *should* the team be monitoring, given the thesis?
3. **Routing trace** — when a signal is detected, who sees it, and how quickly?
4. **Update trace** — when a signal is seen, how fast does a belief or decision change?
5. **Contrary-signal stress test** — what was the most recent piece of contrary signal, and what happened to it?

## Related Skills
- **Ghost Note Detection** — used to identify the expected signals that are missing from the detection inventory
- **Iterative Error Compression** — used to measure prediction-error reduction over audit cycles
- **CORE Communication Protocol** — used when the audit surfaces a person whose perception is structurally degraded; the conversation matters

## Operating Logic
1. Gather one week of meeting transcripts, dashboards in active use, and reporting routines
2. List the signals the team would expect to see if its current thesis is correct (positive and contrary)
3. Compare to the signals actually being routed and discussed
4. For each gap, classify: not collected, collected-but-not-routed, routed-but-not-acted-on
5. Score each of the four dimensions; aggregate to a listening surface score
6. Output the perception gap map and the three highest-leverage routing investments

## Inputs
- Meeting recordings or transcripts (one week minimum)
- Dashboard inventory (URL or screenshot list)
- Recurring reporting routines (which reports, who reads them, when)
- Decision log or proxy (what changed in the last 30 days based on new information)

## Outputs
- A perception gap map (expected signal → status)
- Signal routing diagnosis (where the routing is breaking)
- Listening surface score (1–10)
- Recommended listening investments — ordered, specific

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

## Strategic Value
This framework treats *noticing* as an auditable, improvable capability — and gives the operator the artifacts to invest against it. Most other diagnostics treat noticing as a personal trait. It is not. It is infrastructure.

## Example Applications
- Pre-investment diligence on a founder whose thesis looks suspiciously clean
- Board-level audit before a year-end strategy planning cycle
- Baseline assessment before deploying an internal AI agent layer (so you can measure whether the agent actually improved perception)

## Compression Summary
**Output gets audited every quarter. Perception is what needs the audit.**
