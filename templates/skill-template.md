---
id: [snake_case_id]
name: [Human Readable Name]
type: skill
version: 0.1
status: draft
purpose: [One sentence stating the cognitive capability this skill provides.]
origin:
  - [Source idea, paper, story, or observation 1]
  - [Source idea 2]
inputs:
  - [Artifact or signal type this skill operates on]
outputs:
  - [What the skill produces when applied]
triggers:
  - [Observable signal that this skill should be invoked]
operational_logic:
  - [Step 1 of applying the skill]
  - [Step 2]
failure_modes:
  - [Known ways this skill misfires or is misapplied]
confidence_model:
  low: [What "low confidence" looks like]
  medium: [What "medium confidence" looks like]
  high: [What "high confidence" looks like]
related_skills: []
used_by_frameworks: []
used_by_agents: []
---

# [Name]

## Purpose
*One paragraph. What is this skill for, in plain language?*

## Core Principle
*One paragraph. The single idea this skill rests on.*

## Inputs
*The types of source material this skill takes in.*

## Outputs
*What the skill produces when correctly applied.*

## Detection Logic
*How an operator (human or AI) recognizes when to invoke this skill.*

## Operational Questions
*The 3–5 questions an operator should ask while applying it.*

## AI Agent Usage
*How an AI agent should invoke this skill, and what input/output schema it should conform to.*

## Failure Modes
*The named ways this skill misfires — overconfidence, pattern hallucination, misapplied context, etc.*

## Related Skills
*Other skills this one combines with or substitutes for.*

## Compression Summary
*One sentence the operator can carry into the moment of decision.*
