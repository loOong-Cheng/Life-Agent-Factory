# 03 Domain Diagnosis

## Purpose

Classify the life area so the agent design matches the kind of human work involved.

## Input

- normalized_desire
- life_goal
- life_area
- candidate_loops

## Output

- domain_type
- secondary_domain_types
- domain_implications:
  - memory
  - tone
  - rituals
  - evaluation

## Constraints

Given the candidate loops, diagnose the domain pattern. Choose one primary pattern and optional secondary patterns:

- practice lab
- taste and craft lab
- thinking lab
- care and maintenance lab
- identity reflection lab

Explain what this diagnosis implies for memory, tone, rituals, and evaluation.

Do not choose a domain because it sounds impressive. Choose the pattern that best fits the user's recurring loop.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
