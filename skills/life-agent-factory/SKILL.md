# Life Agent Factory

Use this skill when a user wants to turn a vague life desire, recurring friction, reflective practice, or self-improvement loop into a structured personal life agent.

The factory starts from the life loop, not from an implementation request. It asks what is broken, worth recording, worth improving, or worth reflecting on, then produces an Agent Blueprint that can later become a prompt, skill, workflow, app, or automation.

Do not use this skill as a normal skill builder when the user already has a clear implementation spec and only needs code, scaffolding, or packaging.

## Core Flow

1. Normalize the intake: preserve the user's language while clarifying the desired life area.
2. Scan for loops: identify recurring situations, inputs, decisions, outputs, and reflection points.
3. Diagnose the domain: determine whether the work is practice, planning, review, research, care, taste-making, habit support, or identity reflection.
4. Extract the smallest useful loop: choose one repeatable cycle that would create value if recorded or improved.
5. Define memory: decide what the agent should remember, forget, summarize, and ask before saving.
6. Decompose roles: separate coach, archivist, critic, planner, teacher, analyst, and companion responsibilities.
7. Design rituals: specify when the agent appears, what it asks, and what artifact it produces.
8. Compress to MVP: cut speculative capabilities until one ritual can be run repeatedly.
9. Write the blueprint: produce a concrete Agent Blueprint using the template.
10. Review and revise: test whether the agent is humane, useful, bounded, and easy to repeat.

## Output

Default output is an `agent_blueprint.yaml` populated with:

- life goal, life area, and core loop
- user desire in original language
- broken points and why the loop should become an agent
- positioning, why-agentize rationale, and non-goals
- memory contract
- restrained sub-agent or role boundaries
- rituals
- commands
- review criteria

## Operating Principles

- Begin with lived recurrence, not feature lists.
- Do not create code, prompts, workflows, apps, automations, or sub-agents until the Agent Blueprint defines the life goal, loop, broken points, memory contract, ritual, MVP scope, and success metrics.
- Prefer one useful ritual over a broad assistant persona.
- Treat memory as a contract, not a data dump.
- Keep the agent small enough to trust and repeat.
- Preserve the user's voice; do not over-professionalize intimate life language.
- Avoid over-agentification: do not turn a small broken loop into an always-on life operating system.
