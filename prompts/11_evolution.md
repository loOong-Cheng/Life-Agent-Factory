# 11 Evolution (User-Triggered)

## Purpose

Converge an existing agent's blueprint by one minor version step (vX.X -> vX.X+0.1), using evidence the user brings back from living with the agent. This is the review stage (prompt 10) re-run against a real, used agent — not a new build.

This phase runs ONLY when the user asks. The factory never initiates, schedules, reminds, or hints that a revision is due — not once, not after repeated corrections. If the user never runs it, the blueprint stays as-is.

## Input

- the named agent's current `agent_blueprint.yaml` (the prior version; the source of truth)
- the prior `review.next_revision_questions`
- evidence the user volunteers in-session: lived runs, corrections, frictions, and reports that a ritual felt heavy, untrue, or invasive

No telemetry, invocation counts, fill rates, or inferred usage. None exist, and collecting them would itself be surveillance / Memory Hoarder. If the agent happens to keep a correction log the user points to, that counts; do not assume one exists.

## Output

- per-change before/after diffs for the named blueprint parts
- on approval: the updated `agent_blueprint.yaml` at version +0.1
- one appended `review.evolution_log` entry (bounded)
- rewritten `review.next_revision_questions` for the next cycle
- if a packaged `SKILL.md` exists: a note of which sections must be hand-updated (there is no generator; sync is manual)

## Flow

00. **Lived-with check (precondition).** Has the user lived with this agent at all — at least one real or attempted use of its loop? (Even "I went to open it and the trigger felt wrong" counts.) If NO, this is still *building*, not evolving: there is no lived loop to converge toward, so any change would be spec-editing on imagination, not evidence. Revise the blueprint in place via the review stage (prompt 10), keep the version at its current value (a v0.1 draft stays v0.1 until it has met real use), and route any feature wishes to `future_extensions`. Do not run the rest of this flow. The version bumps only after the agent has been lived with at least once.

0. **Scope-fit / dissolve check.** Load the prior blueprint. Ask whether the loop the user has been *using the agent for* is still recurring and still the one they care about. (This is about the agent's use, not merely whether the life-loop exists.)
   - Recurrence gone -> propose retire/archive. No bump.
   - A genuinely different loop -> decline; route to a fresh factory run (a new sibling agent at v0.1, this one archived and cross-referenced). No bump. A split must be a real distinct recurring loop the user named, not a reframed feature wish.
   - Same loop, still recurring -> continue.

1. **Gather user-volunteered evidence only.** Ask the prior `next_revision_questions` plus one open prompt: "what felt off, heavy, untrue, or invasive since the last version — point me to a real moment." Admit absence reports the USER raises ("even the short version felt like too much on bad days"); never infer from silence, an empty field, or a never-run command. A wish with no lived moment is not evidence — offer to note it under `future_extensions`. No evidence -> no-op, no bump.

2. **Classify subtraction-first.** Map each piece of evidence to one change-type, in this fixed priority order:
   1. **re-voice** (clarify) — the user's words diverge from the blueprint's; restore THEIR language, never optimization/clinical language.
   2. **tighten memory** (prune) — remove a remembered type the user confirms never shaped a recall, add an avoid rule, add a consent gate, or shorten retention.
   3. **de-friction the ritual** (prune) — cut or optionalize steps, relax cadence, strengthen the low-energy version. The only permitted response to a missed ritual is to make it smaller — never a reminder, schedule, or streak.
   4. **harden a boundary** (tighten) — sharpen a fuzzy `must_not`, add a refusal after the agent drifted, or collapse two roles that always fire together (keep the UNION of their `must_not`s). Never collapse roles that fire in different moments with different boundaries.
   5. **promote one** (the rare, paid-for addition) — see Constraints.

   Name the blueprint part touched and the design principle that licenses each change. One evidence item can carry two defects (e.g. "the urge log felt clinical AND too long" = re-voice + de-friction); split it and file both rather than forcing one.

3. **Run the directional checklist out loud** (qualitative, never a score):
   - Fit up: does it describe the real recurring loop, in the user's words, more faithfully?
   - Load not up: same size or smaller, ritual same-or-easier on a bad day?
   - Surface paid-for: any net-add forced by a voiced lived gap AND offset by a concrete cut from the SAME ritual's required path?
   - Memory tighter-or-equal: nothing pruned on absence-of-use in a sensitive loop?
   - Roles not multiplied; boundaries tightened, not loosened?
   - Voice preserved, not re-flattened?
   - Sensitivity held: no verbatim sensitive content persisted; absence never read as deadness?
   - Evidence-gated: every change tied to a real user-volunteered moment?
   - Single coherent step?

   Surface any ambiguous signal as a QUESTION to the user, never as a silent deletion.

4. **Per-change approval.** Show each before/after. The user accepts, edits, rejects, or routes to `future_extensions`. Nothing is written unapproved. No "apply all."

5. **Apply, bump, log, re-seed.** Write only approved changes. Bump the version by +0.1 (parse the string as a decimal, add 0.1, reformat to one decimal place: `0.1` -> `0.2`, `0.9` -> `1.0`). Append one bounded `evolution_log` entry (metadata + a short user-confirmed paraphrase; never verbatim, never sensitive raw content, never the user's own domain entries; strip third-party detail). Rewrite `next_revision_questions` in fit-probing form — "what felt off / heavy / untrue / invasive" — never "should we add X." Rejected changes demote into questions rather than vanish. Then STOP. No scheduling, no follow-up. Evolution sleeps until the user runs it again.

## Constraints

- +0.1 is the only step this phase produces. One approved run = one +0.1, however many changes it bundled. There is no major-version mechanic: a change to the core-loop identity, `domain_type`, or the single ritual's fundamental shape is a different loop -> a new agent at v0.1.
- Pinned across every +0.1: `original_desire`, `domain_type`, core-loop identity, the one-loop / one-contract / one-ritual constraint, and the no-initiative stance.
- The one sanctioned loosening: in identity, meaning, or relationship loops, `original_desire` or a too-early `non_goal` may be re-opened when the user reports the underlying desire itself shifted AND that shift has recurred across sessions (not a single-session mood). Distinguish this from re-voicing: re-voicing finds truer words for the same desire; re-opening acknowledges the desire moved.
- A permitted recall-over-time view shows only entries the user logged, in their own words or numbers, with zero agent-computed aggregates, derived metrics, scores, or good/bad framing. The moment a view computes something, it is a dashboard — refuse it.
- Promotions are capped at one per +0.1, never a chart/score/streak, and never a second loop or second memory contract (those are new agents).
- `blueprint -> SKILL.md` sync is manual. After a revision, note which `SKILL.md` sections each change-type can invalidate: re-voice -> positioning, ritual wording; tighten memory -> Memory Contract, Storage; de-friction -> Commands, ritual steps; harden boundary -> Boundaries, When NOT To Use; promote -> Commands.
- Do not turn the evolve flow itself into a dashboard, score, or surface-count scoreboard.
