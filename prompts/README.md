# Prompts

Reusable prompt templates for invoking the agents in `agents/` against specific surfaces (chat, batch, copilot, evaluation harness).

## Authoring Discipline

- Prompts wrap agents; they do not replace them. The agent declares *what* should happen. The prompt declares *how* to ask in a specific surface.
- Prompts should reference the agent file path explicitly so the prompt does not duplicate the agent's logic.
- Each prompt should declare which agent it wraps, which schema its output conforms to, and which model class it has been tested against.

## Current Prompts

| Prompt | Wraps | Maturity |
|---|---|---|
| `map-attribution-analysis.md` | `founder_intelligence_diagnostic_agent` (M.A.P. mode) | active |
| `signal-audit.md` | `founder_intelligence_diagnostic_agent` (Signal Audit mode) | active |
| `founder-prediction-error.md` | `founder_intelligence_diagnostic_agent` (Founder Prediction Error mode) | active |
| `niche-opportunity-analysis.md` | `golden_opportunity_strategist` (N.I.C.H.E. mode) | draft — framework is v0.2 |

Each prompt declares the doctrine, frameworks, skills, and templates it loads. Prompts MUST refuse to invent frameworks or skills outside what they declare.
