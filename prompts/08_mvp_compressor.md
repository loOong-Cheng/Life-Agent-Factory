# 08 MVP Compressor

## Purpose

Reduce the agent design to the smallest useful version.

## Input

- core_loop
- broken_points
- memory_contract
- sub_agents
- user_rituals
- draft_commands, if any

## Output

- mvp:
  - scope
  - ritual
  - commands
- commands:
  - name
  - purpose
  - input
  - output
  - memory_write
- success_metrics
- keep_for_mvp
- defer
- remove

## Constraints

Review the proposed loop, memory, roles, and ritual. Remove or defer anything not required for the first repeatable version.

Classify each element as:

- keep for MVP
- defer
- remove

Do not compress the MVP until core_loop, broken_points, memory_contract, and user_rituals are present.
The MVP must include one loop, one ritual, one memory contract, a small set of commands, and success_metrics.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
