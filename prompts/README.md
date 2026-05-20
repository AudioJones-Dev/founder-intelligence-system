# Prompts

Reusable prompt templates for invoking the agents in `agents/` against specific surfaces (chat, batch, copilot, evaluation harness).

## Authoring Discipline

- Prompts wrap agents; they do not replace them. The agent declares *what* should happen. The prompt declares *how* to ask in a specific surface.
- Prompts should reference the agent file path explicitly so the prompt does not duplicate the agent's logic.
- Each prompt should declare which agent it wraps, which schema its output conforms to, and which model class it has been tested against.

## Status

This layer is intentionally empty in v0.1. Prompts will be added as the operational pipeline (transcript → extraction → brief) is exercised against real source material.
