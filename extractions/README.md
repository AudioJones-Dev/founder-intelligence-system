# Extractions

Structured outputs derived from `transcripts/` via the transcript-synthesis agent. Extractions are the bridge between raw source material and framework application.

## What An Extraction Contains

Per `agents/transcript-synthesis-agent.md`, each extraction should include:

- `source` — reference to the transcript, date, source type
- `claims` — atomic claims tagged with speaker, claim type, confidence
- `themes` — clustered themes
- `signals_detected` — signals matching framework triggers
- `candidate_frameworks` — frameworks to invoke against the extraction

## Naming Convention

`[YYYY-MM-DD]-[source-slug]-extraction.md`

## Status

This layer is intentionally empty in v0.1. Extractions will be added as transcripts are processed through the synthesis agent.
