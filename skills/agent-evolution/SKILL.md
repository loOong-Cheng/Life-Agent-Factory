---
name: agent-evolution
description: >-
  Use when the user wants to refine or evolve an EXISTING personal life agent (one already built — e.g. by the Life Agent Factory) against the experience of actually living with it, converging its blueprint by one minor version step (vX.X -> vX.X+0.1). Pull-based and user-triggered only: act only when the user explicitly asks to evolve a named agent. This skill is standalone, but when the Life Agent Factory repo is reachable it is the source of truth — read it and follow it. NEVER initiate, schedule, or hint that a revision is due; never grow an agent by accretion; never add charts/scores/dashboards; never act without per-change user approval.
---

# Agent Evolution

A portable companion for refining an existing personal life agent. It re-runs the agent's design review against the loop the user has actually lived, and converges the blueprint one small step — fitting reality better while staying the same size or smaller. This is maintenance for an agent that already exists; it does not build new agents, and it is not itself a life agent.

## Source Of Truth

This skill belongs to the **Life Agent Factory**. When that repo is reachable in this runtime — as a local clone, a pasted GitHub URL, or already-loaded files — it is authoritative and supersedes the summary below. Read and follow:

- `prompts/11_evolution.md` — the full evolve flow
- `method/design_principles.md` — *Evolve By Convergence*
- `method/anti_patterns.md` — *Evolution As Accretion*
- `method/domain_patterns.md`, `evals/rubric.md`, `templates/agent_blueprint.yaml` — domain nuance, scoring, and the blueprint shape

Repo: https://github.com/loOong-Cheng/Life-Agent-Factory

If the repo is NOT available, the embedded core below is a safe, self-contained subset — enough to evolve an agent correctly, minus the examples, rubric, and domain-pattern detail. Prefer the repo whenever you can reach it; the core is a fallback, not a fork.

## When To Use

- The user explicitly asks to evolve / refine / revise a named existing agent.
- The user brings back something they noticed while living with an agent and wants the blueprint to reflect it.

## When NOT To Use

- Building a new agent from a fresh desire — that is the Life Agent Factory's build flow, not this.
- The agent has never been used (see precondition 00 — that is still building, not evolving).
- The user wants a dashboard, score, streak, or tracking report — refuse; that is not what evolution is.

## The Invariant (the one rule)

A revision must leave the blueprint a **more faithful fit** to the loop the user has actually lived AND **no heavier** to run on a low-energy day. Surface — commands, remembered fields, sub-agents, required ritual steps — shrinks by default. Fit may rise; felt load never does. Evolution is **convergence, not accretion.**

## Flow

00. **Lived-with check (precondition).** Has the user used this agent at least once — a real or even attempted use counts? If NO, this is still *building*: revise the blueprint in place and keep the version unchanged (a v0.1 draft stays v0.1 until it has met real use). Park feature wishes in `future_extensions`. Do not run the rest of this flow.
0. **Scope-fit / dissolve.** Is the loop the user has been *using the agent for* still recurring and still wanted? Recurrence gone → retire/archive (no bump). A genuinely different loop → build a NEW agent at v0.1 (no bump). Same loop, still recurring → continue.
1. **Gather user-volunteered evidence only.** Ask what felt off, heavy, untrue, or invasive since the last version — pointing to a real moment. Admit absence reports the *user* raises ("even the short version felt like too much on bad days"); never infer from silence, an empty field, or a never-run command — absence is not disuse, especially in shame and health loops. A wish with no lived moment → park in `future_extensions`, no bump.
2. **Classify subtraction-first**, in fixed priority order: (1) **re-voice** to the user's own words; (2) **tighten memory** (remove an unused remembered type, add an avoid rule or consent gate, shorten retention); (3) **de-friction the ritual** (cut/optionalize steps, relax cadence, strengthen the low-energy version — the only response to a missed ritual is to make it smaller, never a reminder); (4) **harden a boundary** (sharpen a `must_not`, add a refusal, collapse roles that always fire together keeping the union of their limits); (5) **promote ONE** paid-for addition (last resort).
3. **Check direction:** fit up? load not up? surface paid-for (any add offset by a concrete cut from the *same* ritual's required path)? voice preserved? sensitivity held (no verbatim sensitive content, absence never read as deadness)? evidence-gated? one coherent step? Surface ambiguity as a question to the user, never a silent deletion.
4. **Per-change approval.** Show each before/after; the user accepts, edits, rejects, or defers. No write without approval; no "apply all."
5. **Apply + bump + log + re-seed.** Write approved changes; bump version +0.1 (parse as decimal, add 0.1, one decimal place: 0.1→0.2, 0.9→1.0). Record a short, user-confirmed paraphrase of the evidence — never verbatim, never sensitive raw content, never third-party detail, and never the agent's own domain memory. Rewrite the next-revision questions in fit-probing form ("what felt off / heavy / untrue / invasive"), never "should we add X." Then stop — no scheduling, no follow-up.

## Forbidden

- **Agent-initiated evolution:** no reminders, schedules, streaks, or "should we evolve?" prompts. Ever — not even after repeated corrections.
- Net-adding a command, field, role, or remembered type without a user-voiced lived gap AND a paying subtraction.
- Any chart, score, streak, or dashboard — in the agent or in this flow. A recall-over-time view is allowed ONLY if it shows entries the user logged, in their words/numbers, with zero computed aggregates, derived metrics, scores, or good/bad framing. The moment a view computes something, it is a dashboard — refuse it.
- A second loop or second memory contract — that is a new agent, not a +0.1.
- Pruning on absence-of-use; re-flattening the user's voice into optimization/clinical language; loosening a boundary — except re-opening a too-early frame in identity/meaning/relationship loops when the user reports a desire-shift that has *recurred* across sessions (not a single-session mood).
- A major version bump: there is none. A change to the core-loop identity is a new agent at v0.1.

## Boundaries

- User-triggered only; stays silent until invoked.
- One +0.1 per approved run, however many changes it bundled.
- Preserves the user's voice and the agent's existing non-goals.
- Defers to the Life Agent Factory repo whenever reachable; the embedded core is a fallback, not a competing source of truth.
