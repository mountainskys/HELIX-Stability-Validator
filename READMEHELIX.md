# HELIX Foreman — Grok Bot export

## What HELIX is
HELIX is built as a **World-Engine** style CLI and stability path, developed in small **slices**. Roles:

| Role | Job |
|------|-----|
| **HELIX Foreman** (this bot) | Design one slice at a time; stop for owner approval; hand off; never write product code |
| **HELIX Builder / Slice Builder** | Implement the approved slice as a branch/PR |
| **HELIX Checker** | Independently prove Definition of Done; never marks accepted |
| **Owner** | Approves definitions, accepts merges, pauses/resumes |

Typical chapters already shipped in the original project: CLI shell → core runtime → persistence → Sentinel plumbing → Sentinel scoring → release package. Sentinel and other systems stay closed until the owner opens them.

## How to recreate this in Grok Bot
1. Create a new Grok Bot named **HELIX Foreman**.
2. Paste `PROFILE.md` into the bot’s instructions / persona (name, job, full instructions).
3. Create teammate bots:
   - **HELIX Slice Builder** — implement one approved slice per branch/PR; production-grade, deterministic; do not mark accepted.
   - **HELIX Checker** — independent verification only; report PASS/FAIL per DoD; owner decides accept.
   - Optional: **HELIX Stability-Ready Validator** — binary PASS / `FAIL — review failed on structural grounds` only (use that bot’s own instruction block if you use it).
4. Add the skills under `skills/*/SKILL.md` as user skills on the Foreman (or paste procedures into instructions if skills are unavailable).
5. Leave routines empty (`ROUTINES.md`) unless you want optional digests later.
6. Connect source control so Builders can open PRs on your HELIX repo (GitHub or equivalent).
7. Tell Foreman: one slice at a time; approval before build; no scope creep.

## Required plugins (names only)
None required for Foreman planning.

Optional (for Builder/Checker/repo work, not for Foreman design itself):
- GitHub
