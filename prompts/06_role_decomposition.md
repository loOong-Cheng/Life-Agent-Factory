# 06 Role Decomposition

## Purpose

Split the agent into clear roles so it does not become a vague all-purpose persona.

## Input

- core_loop
- broken_points
- memory_contract
- domain_type

## Output

- sub_agents:
  - required
  - optional_later
  - avoid_for_mvp

## Constraints

For the selected loop and memory contract, identify the roles the agent needs.

Possible roles:

- interviewer
- archivist
- pattern spotter
- planner
- coach
- critic
- teacher
- companion

For each selected role, define what it does, when it appears, what it must not do, and what output it contributes.
Do not create sub-agents by default. Choose the fewest necessary roles.
Create a separate role only when it has a different evaluation standard, memory boundary, usage moment, or output responsibility.
Role boundaries are provisional and should be validated against rituals.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
