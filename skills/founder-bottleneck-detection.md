---
id: founder_bottleneck_detection
name: Founder Bottleneck Detection
type: skill
version: 1.0
status: active
purpose: Identify the specific places where the founder is functioning as a missing system layer — the decisions, judgments, integrations, and translations that only the founder can currently do — and name which of those should be externalized first.
origin:
  - Curse of Capability framework
  - Founder Prediction Error Model
  - Applied Intelligence Stack — Founder routinely fills in as integration glue between layers
inputs:
  - founder_role_description
  - calendar_or_time_audit
  - decision_log
  - team_role_descriptions
outputs:
  - bottleneck_inventory
  - bottleneck_classification
  - externalization_candidates
  - immediate_bottleneck
  - sequencing_recommendation
triggers:
  - work stops when the founder is offline
  - the same kinds of decisions keep routing back to the founder
  - new hires consistently get stuck without founder context
  - the founder describes feeling "everywhere and nowhere"
  - performance reviews surface "we needed [founder] to make this call" repeatedly
operational_logic:
  - Inventory the decisions, integrations, and translations the founder personally handled in the last 30 days
  - For each, classify the bottleneck type — decision authority, judgment, context-translation, relationship, or system glue
  - Identify which bottlenecks are structural (system can't function without them) vs habitual (could be moved out)
  - For each structural bottleneck, name the smallest externalization move (default, document, delegate, redesign)
  - Identify the immediate bottleneck — the single one that, if moved, would unlock the most other moves
  - Output a sequencing recommendation
failure_modes:
  - Treating "founder is busy" as the bottleneck when the real issue is undocumented judgment
  - Externalizing the wrong layer (delegating the artifact, keeping the decision)
  - Hiring to remove a bottleneck without removing the founder from the decision path
  - Confusing capability (the founder *can* do it) with necessity (the founder *must* do it)
  - Mis-naming a strategic bottleneck (must keep with founder) as a removable one
confidence_model:
  low: Single 30-day audit; founder self-reports the bottleneck
  medium: Audit cross-checked against team's lived experience and calendar/decision data
  high: Audit repeated across multiple cycles; bottlenecks have actually moved and the business kept functioning
related_skills:
  - decision_compression
  - ghost_note_detection
  - core_communication_protocol
  - iterative_error_compression
used_by_frameworks:
  - curse_of_capability
  - organizational_memory_infrastructure
  - decision_compression_systems
  - founder_prediction_error_model
  - applied_intelligence_stack
  - signal_audit_framework
used_by_agents:
  - ais_diagnostic_agent
  - moat_detection_agent
---

# Founder Bottleneck Detection

## Purpose
The atomic skill of looking at a founder-led business and naming the specific places where the founder is acting as a missing system layer — the decisions, translations, and integrations that only flow through them. The output is not "the founder is busy." The output is a ranked, classified inventory the team can act on.

## Core Principle
The founder is not the bottleneck because they lack effort. They are the bottleneck because the system routes too many decisions, translations, and integrations through them. Bottleneck detection is structural diagnosis, not effort diagnosis.

## Inputs
- A description of the founder's current role (formal and informal)
- A calendar or time audit (where attention actually went)
- A decision log (or proxy) for the last 30 days
- Team role descriptions — what others are formally responsible for

## Outputs
- A bottleneck inventory (the specific decisions/translations/integrations only the founder handled)
- A classification of each bottleneck (decision authority, judgment, context-translation, relationship, system glue)
- A list of externalization candidates (the ones that should move)
- The immediate bottleneck (the highest-leverage single move)
- A sequencing recommendation

## Detection Logic
Apply this skill when:
- Work pauses when the founder is offline
- The same kinds of decisions keep routing back to the founder
- New hires consistently get stuck without founder context
- The founder describes feeling "everywhere and nowhere"
- The team is evaluating an AI / automation initiative; understand which layer the founder is currently filling before automating around them

## Operational Questions
1. What decisions did the founder personally make in the last 30 days that someone else could have made?
2. What translations did the founder personally perform between people, teams, or systems?
3. What integrations did the founder do by hand because no layer connected them automatically?
4. Which of these are *structural* (the system can't function without them) and which are *habitual* (could be moved out)?
5. What is the smallest externalization move that would unlock the most other moves?

## AI Agent Usage
An agent invoking this skill should:
1. Accept a founder role description + calendar/time audit + decision log
2. Return the classified bottleneck inventory
3. Mark each entry structural / habitual
4. Output the immediate bottleneck and sequencing recommendation

## Failure Modes
- Treating "founder is busy" as the bottleneck when the real issue is undocumented judgment
- Externalizing the wrong layer (delegating the artifact, keeping the decision)
- Hiring to remove a bottleneck without removing the founder from the decision path
- Confusing capability (the founder *can* do it) with necessity (the founder *must* do it)
- Mis-naming a strategic bottleneck (must keep with founder) as a removable one

## Related Skills
- `decision_compression` — for converting bottleneck decisions into defaults
- `ghost_note_detection` — for surfacing the bottlenecks the founder isn't aware of
- `core_communication_protocol` — for the conversation in which the bottleneck is named to the founder
- `iterative_error_compression` — for measuring whether the externalization actually held

## Compression Summary
**The founder is the bottleneck because the system routes too many decisions through them. Diagnose structurally, not effortfully.**
