---
id: ghost_note_detection
name: Ghost Note Detection
aliases:
  - absence_detection
type: skill
version: 1.1
status: active
purpose: Detect informational, evidential, or behavioral gaps where something should logically be present but is not — the strategic signal often lives in what is missing.
origin:
  - Abraham Wald's survivorship bias analysis (1943)
  - Bayesian inference over missing data
  - "Ghost notes" framing from musical performance
inputs:
  - meeting_transcripts
  - founder_pitches
  - dashboards_and_reports
  - sales_calls
  - investor_updates
  - marketing_narratives
outputs:
  - missing_signal_list
  - asymmetry_flags
  - candidate_diligence_questions
triggers:
  - narrative is conspicuously one-sided
  - metric is presented without its natural counterpart (retention without CAC, growth without churn)
  - failure cases or downsides are absent from a discussion of a system
  - the speaker can list wins but not losses
  - dashboard shows outputs but not the decisions they enable
  - everyone in the room is looking at the same slide
operational_logic:
  - List the signals you would expect to see if the narrative were complete
  - Compare to the signals actually present
  - For each gap, ask whether the absence is innocuous, accidental, or strategic
  - Generate one or two calm, curious questions that surface the gap without accusation
  - Treat the gap itself as data, not as evidence of bad faith
failure_modes:
  - Pattern hallucination — seeing absence where none exists
  - Excessive skepticism that corrodes trust without yielding insight
  - Confusing "I wasn't told" with "they hid it"
  - Treating absence as proof rather than as a question to investigate
confidence_model:
  low: One expected signal is missing; many plausible benign explanations
  medium: Multiple correlated omissions; the missing signals cluster around a coherent topic
  high: A signal whose absence would be operationally impossible if the narrative were true
related_primitives:
  - bayesian_belief_updating
used_by_frameworks:
  - organizational_memory_infrastructure
  - curse_of_capability
  - simplicity_arbitrage
used_by_agents:
  - transcript_synthesis_agent
  - moat_detection_agent
---

# Ghost Note Detection
*(also known as: absence detection)*

## Why "Ghost Notes"
In music, a ghost note is a note that is implied but barely played — felt in the rhythm rather than heard. The listener registers it as a hole the beat shapes itself around. Strategic intelligence has the same texture: the most consequential signal is often the one that *should be there and isn't*.

## Core Idea
Strategic insight often lives in the data that isn't there. The signals that survive into a conversation, a deck, or a dashboard are the ones that survived selection. The interesting question is what got filtered out — and why.

## Anchor Story
In 1943, the US military asked statisticians how to armor planes that returned from missions covered in bullet holes. Abraham Wald observed that the bullet holes on the returning planes were not where armor was needed — those were the survivable hits. The hits that mattered were in the engines and cockpits of the planes that *didn't* return, and which the data therefore didn't contain.

The lesson generalises: when you only see survivors, you must reason about what is missing.

## How To Apply

### In meetings
Before walking in, list three signals you would expect to see if the situation is as described. In the meeting, note which of those three never come up. After the meeting, ask one calm question about the most consequential gap.

### In diligence
For any pitch, write the symmetrical counterpart of each headline metric. Growth → churn. Retention → CAC. Pipeline → close rate. NPS → cancellation reasons. Flag every counterpart that is missing.

### In hiring
A candidate who can list wins fluently but stalls on failures is showing you an absence. The absence is the signal.

### In your own thinking
Periodically ask: what would I expect to see if I were wrong about this? If you can't name it, you haven't stress-tested the position.

## Anti-Patterns
- Demanding the missing data in a way that feels like an accusation
- Treating one missing signal as a verdict instead of a question
- Building a worldview where everything missing is suspicious — that's paranoia, not analysis
