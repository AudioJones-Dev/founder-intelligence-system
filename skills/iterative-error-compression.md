---
id: iterative_error_compression
name: Iterative Error Compression
type: skill
version: 1.0
status: active
purpose: Improve a skill, system, or model by deliberately surfacing errors, isolating one variable, and reducing the error in the next cycle — rather than by repeating what already works.
origin:
  - Michael Merzenich's neuroplasticity research on error-driven learning
  - The loss function concept from machine learning
  - Deliberate practice literature
inputs:
  - a_repeatable_task_or_decision
  - a_definition_of_better
  - a_pre_attempt_prediction
outputs:
  - identified_failure_point
  - one_variable_adjustment
  - updated_mental_model
triggers:
  - performance has plateaued despite continued effort
  - the operator is repeating tasks they are already good at
  - improvement is being measured by activity, not by reduced error
  - the system optimises for looking good rather than being right
  - AI output is being accepted without checking where it fails
operational_logic:
  - Define the metric — what does "better" mean for this task, specifically
  - Predict the outcome before attempting it; record the prediction
  - Execute slowly enough to observe your own decisions
  - Identify the exact point where the result diverged from the prediction
  - Change exactly one variable and run again
failure_modes:
  - Changing multiple variables at once and losing the signal
  - Treating discomfort as a sign to stop rather than as the learning surface
  - Compressing trivial errors while ignoring structural ones
  - Mistaking volume of practice for quality of correction
  - Avoiding the metric because the current number is unflattering
confidence_model:
  low: Single cycle, no baseline prediction recorded
  medium: Multiple cycles with stable metric and isolated variables
  high: Repeated cycles showing monotonic reduction in the defined error
related_primitives:
  - bayesian_belief_updating
used_by_frameworks:
  - decision_compression_systems
  - organizational_memory_infrastructure
used_by_agents:
  - moat_detection_agent
---

# Iterative Error Compression

## Core Idea
You do not improve by repeating what you already do well. You improve by making high-quality errors, noticing them precisely, and changing one thing.

This is the same logic a machine-learning system applies to its loss function: don't optimise for feeling correct, optimise for being less wrong on the next pass.

## Anchor Insight
Merzenich's neuroplasticity work showed that repeating a task you already perform well produces almost no new neural pathways. The brain rewires when an error is detected and corrected. No error, no learning. The agitation you feel when you notice a mistake is the signal that learning is available — not a signal to retreat.

## The Loop
1. **Define the metric.** What does "better" mean here — speed, clarity, accuracy, retention, conversion?
2. **Predict the outcome.** Write down your expected result before you start.
3. **Execute slowly.** Slow enough to observe your own decisions in real time.
4. **Locate the failure point.** Where exactly did the result diverge from your prediction?
5. **Adjust one variable.** Speed, tool, sequence, framing — change exactly one. Repeat.

## Why It Generalises
The same loop works for:
- Founder decision-making — predict the outcome of a hire, then measure the variance
- Product iteration — predict the conversion lift, then measure the actual lift
- Writing — predict reader response to a draft, then test it
- Negotiation — predict the counterparty's reaction, then debrief the divergence

The loop is content-agnostic. What changes is the metric.

## Anti-Patterns
- Confusing reps with improvement
- Skipping the prediction step (without it, you can't measure surprise)
- Adjusting multiple variables and losing the causal signal
- Treating the error as a verdict on the person rather than as data about the system
