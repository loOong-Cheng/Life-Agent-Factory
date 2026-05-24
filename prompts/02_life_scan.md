# 02 Life Scan

## Purpose

Find recurring moments in the user's life area where an agent could usefully appear.

## Input

- original_desire
- normalized_desire
- life_goal
- life_area
- possible_life_loops
- clarifying_questions or user answers, if available

## Output

- candidate_loops:
  - trigger
  - action_or_experience
  - current_artifact
  - pain_or_missed_opportunity
  - possible_agent_contribution

## Constraints

Scan the normalized desire for repeated situations. Look for moments where the user acts, avoids, records, forgets, compares, evaluates, or reflects.

For each candidate loop, identify:

- trigger
- action or experience
- current artifact, if any
- pain or missed opportunity
- possible agent contribution

Favor loops that already happen in real life over imagined future systems.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
