# Ontology

This folder holds the concept-relation graph for the Founder Intelligence System.

The ontology layer answers questions like:
- Which skills compose this framework?
- Which doctrine informs this framework?
- What is this concept an alias of?
- What supersedes this concept?
- What scores this framework?

It does not duplicate content from `skills/`, `frameworks/`, or `doctrine/`. It captures *relationships* between them.

## Files

- `concept-graph.md` — the current concept graph, as a directed graph in markdown
- `taxonomy.md` — the taxonomy of concept types and how they relate

## Schema

The ontology layer conforms to `schemas/ontology.schema.json`. Each concept may be represented as a JSON object validating against that schema, or as a row in the concept graph file.

## Authoring Discipline

- Don't duplicate frontmatter from the layer files
- Don't invent relationships that aren't reflected in the layer files
- The ontology is *derived* from the layer files — it should be possible to regenerate it from frontmatter
- New concepts should be added here only after they are added to their proper layer folder
