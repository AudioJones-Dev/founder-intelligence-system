# Taxonomy

The types of concept that exist in the Founder Intelligence System, and how they relate.

## Concept Types

| Type | Folder | Purpose | Composes | Composed by |
|---|---|---|---|---|
| `doctrine` | `doctrine/` | Worldview, falsifiable thesis | nothing (root layer) | informs frameworks and skills |
| `framework` | `frameworks/` | Composed strategic lens, scorable diagnostic | skills | invoked by agents |
| `skill` | `skills/` | Atomic, content-agnostic reasoning capability | nothing (atomic) | frameworks, agents |
| `agent` | `agents/` | Workflow router | skills, frameworks | external invocation |
| `scoring_rubric` | `scoring/` | Composite scoring logic | framework outputs | invoked at composite-score time |
| `output_template` | `templates/` | Reusable document structure | nothing | filled in by agents |
| `concept` | `ontology/` | Pure ontology node | varies | varies |

## Relations

The allowed relation types (from `schemas/ontology.schema.json`):

| Relation | Meaning |
|---|---|
| `composes` | Source uses target as a component |
| `composed_by` | Target uses source as a component |
| `informs` | Source's worldview underlies target |
| `informed_by` | Target's worldview underlies source |
| `derives_from` | Source's claim emerges from target's substrate |
| `operationalizes` | Source turns target's abstraction into a runnable process |
| `routes_to` | Source hands off to target in a workflow |
| `depends_on` | Source cannot run cleanly without target |
| `detects` | Source surfaces conditions named by target |
| `attributes` | Source produces causal explanations consumed by target |
| `predicts` | Source produces forward claims consumed by target |
| `compresses` | Source reduces the surface area of target |
| `amplifies` | Source increases the effect of target (good or bad) |
| `evaluates_with` | Source uses target as its scoring or judgment instrument |
| `produces` | Source's output conforms to or fills target |
| `supports` | Source provides material that strengthens target |
| `scores` | Source produces scoring of target |
| `scored_by` | Target produces scoring of source |
| `applies_to` | Source is run against target as input |
| `related_to` | Generic semantic relation; weakest claim — use only when no typed relation fits |
| `supersedes` | Source replaces target (target is deprecated) |
| `superseded_by` | Target replaces source (source is deprecated) |
| `alias_of` | Source is a renamed reference to target |

**Authoring rule:** prefer the most specific typed relation. `related_to` is the relation of last resort; if a stronger relation fits, use it.

## Maturity States

| Maturity | Meaning |
|---|---|
| `seed` | Idea named, not yet authored |
| `draft` | Authored, not yet validated against schema |
| `active` | Validated, in use |
| `stable` | Validated, in use across multiple cycles, low expected churn |
| `deprecated` | Superseded; kept for traceability, not for use |

## Authoring Order

When introducing a new concept:

1. Place it in its layer folder with appropriate frontmatter
2. Validate against the layer's schema
3. Add the edges to `ontology/concept-graph.md`
4. Update `meta/routing.md` if the concept changes routing
5. Update `meta/system-map.md` if the concept changes layer composition
