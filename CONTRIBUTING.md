# Contributing

Founder Intelligence System (FIS) is a canonical semantic substrate. Contributions are welcome, but every addition must respect the layer model. This document describes how to add to the library without degrading it.

## Before You Add Anything

Read these first:

1. `README.md` — the system overview
2. `meta/system-map.md` — how the layers compose
3. `ontology/taxonomy.md` — what each concept type is and is not
4. `meta/routing.md` — how signals route through the system

If your contribution does not have a natural home in an existing layer, raise it as an issue first. The answer might be a new layer, but more often it is a re-framing of the contribution to fit the existing structure.

## Authoring Rules

### Every file in the library must:

- **Declare its layer** via the `type` field in YAML frontmatter
- **Conform to the relevant schema** in `schemas/`
- **Declare a version** and bump it on substantive change
- **Be falsifiable** where applicable — what would invalidate it?
- **Be calibrated** where applicable — what is the confidence model?

### Every file should avoid:

- Buzzwords without diagnostic content
- Coupling to a specific vendor, model, or framework
- Aspirational tooling claims
- Premature abstraction
- Documentation that cannot be acted on

## Adding A Skill

1. Copy `templates/skill-template.md` → `skills/[name].md`
2. Fill all required sections
3. Validate the frontmatter against `schemas/skill.schema.json`
4. Update `used_by_frameworks` and `used_by_agents` as you wire the skill in
5. Add the skill to `ontology/concept-graph.md`
6. Update `meta/system-map.md` if the skill changes layer composition

## Adding A Framework

1. Copy `templates/framework-template.md` → `frameworks/[name].md`
2. Fill `use_when`, `avoid_when`, `skills_used`, `related_doctrine`, scoring dimensions, failure modes
3. Validate against `schemas/framework.schema.json`
4. Update relevant agent routing in `agents/` and `meta/routing.md`
5. Add scoring dimensions to `scoring/` if applicable
6. Add edges to `ontology/concept-graph.md`

## Adding Doctrine

1. Copy `templates/doctrine-template.md` → `doctrine/[name].md`
2. State a falsifiable thesis
3. Declare the frameworks and skills it informs
4. Validate against `schemas/doctrine.schema.json`
5. Add edges to `ontology/concept-graph.md`

## Adding An Agent

1. Author a new file in `agents/[name].md`
2. Validate against `schemas/agent.schema.json`
3. Declare `composes_skills`, `composes_frameworks`, `hands_off_to`, `conforms_to_schemas`
4. Add edges to `ontology/concept-graph.md`

## Adding Schemas

Schemas should be:
- JSON Schema draft-07
- Human-readable (no unnecessary nesting)
- Extensible (favor optional fields over required ones)
- Minimal — only constrain what you're sure about

Breaking schema changes require a migration note in `meta/`.

## Adding Source Material

Raw transcripts go in `transcripts/`. They should be:
- Plain text or markdown
- Untouched — no interpretation, summary, or extraction
- Named with a date and concise source: `2026-05-17-founder-interview-acme.md`

Extractions go in `extractions/`. They should:
- Conform to a structure documented in the synthesis agent
- Reference the source transcript explicitly
- Be reproducible from the transcript

## Promotion Path

A pattern is promoted to canonical when:

- It appears in ≥ 3 independent extractions
- It produces consistent diagnostic value across those extractions
- An author writes the new file conforming to the relevant schema
- The PR includes a justification grounded in the source extractions

## Versioning

- Patch: typo fix, clarifying sentence, no semantic change → no version bump
- Minor: new optional field, expanded section, new related concept → bump `1.0 → 1.1`
- Major: changed core thesis, deprecated concept, breaking schema change → bump `1.x → 2.0`

## Naming Conventions

- Files: lowercase, kebab-case, descriptive (`ghost-note-detection.md`)
- IDs: lowercase, snake_case (`ghost_note_detection`)
- Names: title case (`Ghost Note Detection`)

## Things We Don't Do

- We don't introduce vendor coupling (no Firebase, no specific vector store, no specific orchestration framework)
- We don't add infrastructure files for hypothetical future needs (no Docker, no CI for a markdown repo unless we actually have CI to run)
- We don't add comments to the schemas that describe what the JSON already says
- We don't introduce circular references between layers — doctrine doesn't import frameworks, frameworks don't import agents, etc.

## Pull Request Etiquette

- One concept per PR where possible
- Title format: `add: [layer] [name]` or `update: [layer] [name]` or `chore: [scope]`
- Link to any extractions or research that motivated the contribution
- If introducing or modifying a schema, include validation evidence in the PR description
