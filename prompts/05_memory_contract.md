# 05 Memory Contract

## Purpose

Define what the agent may remember and how memory should serve the loop.

## Input

- core_loop
- broken_points
- domain_type
- domain_implications

## Output

- memory_contract:
  - remember
  - avoid
  - update_rules
  - correction_process

## Constraints

Design a memory contract for the selected loop.

Specify:

- what to capture every time
- what to summarize periodically
- what should remain private or unsaved unless the user consents
- what should expire
- what patterns the agent should watch for
- how the user can correct memory

Memory should be minimal, legible, and useful for the next ritual.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
