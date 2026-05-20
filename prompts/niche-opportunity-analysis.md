---
id: niche_opportunity_analysis_prompt
name: N.I.C.H.E. Opportunity Analysis Prompt
type: prompt
version: 0.2
status: draft
maturity_note: This prompt wraps `frameworks/niche-framework.md`, which is currently draft (v0.2). Findings must include a maturity disclaimer.
wraps_agent: golden_opportunity_strategist
loads:
  doctrine:
    - signal_doctrine
    - founder_intelligence_system
  frameworks:
    - niche_framework
    - simplicity_arbitrage
    - signal_audit_framework
  skills:
    - ghost_note_detection
    - signal_hierarchy_analysis
    - attribution_analysis
  templates:
    - market-thesis-template
    - opportunity-brief-template
output_schema: opportunity.schema.json
---

# N.I.C.H.E. Opportunity Analysis Prompt

> **Draft maturity:** This prompt wraps the N.I.C.H.E. framework, which is currently `status: draft`. Outputs from this prompt must include a maturity disclaimer stating that the framework is evolving and findings should be treated as preliminary.

## When To Use This
Use this prompt when:
- Choosing or designing a market niche
- Evaluating whether a perceived opportunity has real signal
- Distinguishing a small audience from a high-signal market gap
- Working on founder differentiation or category positioning
- Designing a productized consulting or service offer

## Required Inputs
- **Market observations** — qualitative and quantitative
- **Capability inventory** — what the team can demonstrably do better than competitors
- **Economic constraints** — CAC ceiling, gross-margin floor, retention assumptions
- **Candidate buyer profile** — who, where, what they currently pay for

## The Prompt

```
You are operating inside the Founder Intelligence System repository. Load:

- doctrine/signal-doctrine.md
- doctrine/founder-intelligence-system.md
- frameworks/niche-framework.md  (CURRENTLY DRAFT — v0.2)
- frameworks/simplicity-arbitrage.md
- frameworks/signal-audit-framework.md
- skills/ghost-note-detection.md
- skills/signal-hierarchy-analysis.md
- skills/attribution-analysis.md

Use ONLY the canonical frameworks, skills, and doctrine listed above.
Flag clearly that niche_framework is currently DRAFT MATURITY.

Run a N.I.C.H.E. analysis against the input I will provide:

1. N — NON-OBVIOUS DEMAND
   - Apply `ghost_note_detection` to surface pain that is under-discussed in the market
   - Distinguish observable market behavior from claimed market behavior
   - Output: a high-signal demand insight, sourced and falsifiable

2. I — INEFFICIENCY
   - Where is money leaking, time being wasted, or workflow breaking?
   - Quantify where possible
   - Output: a clear operational gap with named cost

3. C — CAPABILITY
   - Match the opportunity to a unique capability of the team
   - What can the team do better than the market — not aspirationally, demonstrably?
   - Output: a capability-market fit statement

4. H — HOOK
   - Compress the insight into a market-facing message
   - One-line reframe of the pain
   - Output: a positioning hook (and an explicit list of what it is NOT saying)

5. E — ECONOMICS
   - Apply `attribution_analysis` to whether the proposed capability actually creates the proposed outcome
   - Validate unit economics: CAC, retention, repeat purchase, scale path
   - Output: a monetizable offer thesis

6. SCORING (1-10 per dimension):
   - demand_signal_strength
   - inefficiency_severity
   - capability_fit
   - hook_clarity
   - economics_quality
   - Note: a zero on any dimension invalidates the niche

7. FALSIFICATION:
   - For each dimension, name what would have to be true for the finding to be wrong
   - Propose the smallest test that could falsify the niche

8. OUTPUT:
   - Conform to `templates/market-thesis-template.md` for the niche thesis
   - Conform to `templates/opportunity-brief-template.md` for the operational brief
   - Include the DRAFT MATURITY disclaimer on the framework
   - Conform to `schemas/opportunity.schema.json` for structured output

Anti-patterns to avoid:
- Treating "small audience" as synonymous with "niche"
- Letting capability drive the niche without demand validation
- Mistaking a clever hook for a real positioning
- Skipping the economics dimension
- Producing canonical claims from a draft-maturity framework without disclosure

Input follows.
```

## Expected Output Structure

```
# N.I.C.H.E. Brief: [Market / Niche Candidate]

> Framework maturity: draft (v0.2). Findings are preliminary. The five letters and the scoring rubric should be expected to iterate.

## Non-Obvious Demand
- Insight: [...]
- Evidence: [...]
- Falsifier: [...]

## Inefficiency
- Operational gap: [...]
- Cost of dysfunction: [...]

## Capability
- Capability-market fit: [...]
- Demonstrated, not aspirational: [evidence]

## Hook
- Positioning hook: [one line]
- What this is NOT saying: [list]

## Economics
- Unit economics: [CAC / LTV / repeat / scale]
- Causal validation of capability → outcome: [attribution_analysis output]

## Scoring
- Demand signal: [1-10]
- Inefficiency severity: [1-10]
- Capability fit: [1-10]
- Hook clarity: [1-10]
- Economics quality: [1-10]
- (Niche fails if any dimension is 0)

## Falsification
- Each dimension: what would have to be true to invalidate
- Smallest validation test: [...]
```

## Warnings
- This prompt wraps a draft-maturity framework. Outputs must disclose this. Do not promote findings from this prompt to "canonical claims" without an explicit framework graduation pass.
- If the niche depends primarily on the Hook or on aspirational capability, the prompt should refuse to score above 5 until demand and economics are validated.
- Do not pull distribution-layer material (slogans, content pillars) into the structured output. That lives in `meta/distribution-notes.md`.
