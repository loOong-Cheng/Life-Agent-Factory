# 09 Blueprint Writer

## Purpose

Write the structured Agent Blueprint from the compressed MVP.

## Input

- original_desire
- normalized_desire
- life_goal
- life_area
- domain_type
- why_agentize
- core_loop
- broken_points
- user_rituals
- memory_contract
- sub_agents
- commands
- data_sources
- storage_recommendation
- mvp
- success_metrics
- risks_and_limits
- future_extensions

## Output

- agent_blueprint YAML using `templates/agent_blueprint.yaml`

## Constraints

Create an Agent Blueprint in YAML using `templates/agent_blueprint.yaml`.

Requirements:

- include agent_name
- include one_sentence_positioning
- preserve the user's original desire
- include life_goal
- include domain_type
- include why_agentize
- name the selected life loop
- include broken_points
- include non-goals
- include memory_contract
- include user_rituals
- include sub_agents
- include only commands needed for the MVP
- include data_sources
- include storage_recommendation
- include mvp
- include success_metrics
- include risks_and_limits
- include future_extensions

Write clearly enough that a later builder could implement the agent without rediscovering the life design.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
