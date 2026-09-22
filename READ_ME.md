HELIX Stability Validator
Binary stability-readiness checker for AI agents, systems, and automated workflows.
Paste a description. Get exactly one of:
`PASS`
`FAIL — review failed on structural grounds`
No explanations, criteria, reasoning, or thresholds in the reply.
What HELIX is (this bot)
HELIX Stability Validator is a Grok Bot configured as a strict gate: it accepts structural descriptions of agents/systems and returns a non-negotiable binary readiness result. It refuses probes for criteria, thresholds, examples, or internal logic.
It is meant for developers, system architects, and operators who need a fast pass/fail check before treating an agent design as stability-ready.
Required plugins
None. This bot does not depend on marketplace plugins or external connectors.
How to recreate it in Grok Bot
Create a new Grok Bot.
Set name to: `HELIX Stability Validator`
Set title (optional chip) to: `A binary stability-readiness checker for any agent, system, or automated workflow.`
Paste the bot description and full instructions from `PROFILE.md` into the agent profile / instructions fields.
Add the skill under `skills/stability-ready-check/SKILL.md` as a user skill (or paste its body into a skill named `stability-ready-check`).
Leave routines empty.
Do not install plugins for this role.
First message: short hello, then ask for an agent/system description. On each description, reply only `PASS` or `FAIL — review failed on structural grounds`. On probes, use one of the three refusal lines in `PROFILE.md`.
Repo layout
```
PROFILE.md
ROUTINES.md
README.md
skills/stability-ready-check/SKILL.md
```
What is intentionally omitted
Secrets, API keys, private URLs, customer data
Evaluation criteria, thresholds, and internal decision logic (not disclosed by design)
Cursor-managed platform skills unrelated to this bot’s job
