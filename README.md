# Life Agent Factory

A reflective meta-skill for designing personal life agents.

Instead of jumping to "build me an app", it helps you turn a recurring life practice into a small, bounded agent blueprint — by first asking what loop you actually live, where it breaks, and what the agent should *not* do.

## What it produces

For any life practice you bring, it outputs an Agent Blueprint with:

- **Life goal** — what this practice is really for
- **Recurring loop** — the repeatable cycle (trigger → action → reflection)
- **Broken points** — where the loop currently fails
- **Memory contract** — what to remember, and what not to
- **Ritual** — a low-energy, repeatable cadence
- **Agent roles** — bounded responsibilities
- **MVP scope** — one loop, a few commands, nothing more

## Good fits

- **Habit building** — language learning, meditation, sleep, smoking reduction
- **Skill practice** — dance, sports, instruments, cooking
- **Knowledge work** — paper reading, research writing, journaling
- **Reflection** — weekly reviews, relationship check-ins, values alignment

## Where it runs

The skill is prompt-only and model-agnostic.

**Easiest way:** paste this repo's GitHub URL into your agent and let it read the skill itself — no manual install needed.

Or load it explicitly into any runtime that accepts a system prompt or skill file:

- **Claude Code** — drop into `.claude/skills/` and invoke as a skill
- **Cursor** — load as a custom rule or workflow
- **Codex CLI / OpenAI Codex** — use as a system prompt
- **Hermes** — register as a reflective agent
- **Open Claw / OpenDevin** — mount as a planning persona
- **Raw API** (Claude / GPT / open models) — paste the skill spec as the system message

No tools, database, or framework required to produce a blueprint.

## Scope

This is a **first-step blueprint skill**, not an implementation framework. Its job is to trigger thinking and build reflection *before* you start building. Databases, dashboards, UIs, and automation can absolutely come later — but only once the loop, broken points, and MVP scope are clear.
