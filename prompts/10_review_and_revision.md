# 10 Review And Revision

## Purpose

Evaluate the blueprint before implementation.

## Input

- agent_blueprint
- evaluation rubric

## Output

- required_revisions
- optional_improvements
- readiness_judgment

## Constraints

Review the Agent Blueprint against the rubric.

Check:

- Does it avoid implementation-first failure?
- Does it start from a real life loop?
- Is the life loop missing or vague?
- Are broken_points present and clear?
- Is memory bounded and consensual?
- Does it avoid memory hoarding?
- Is the ritual repeatable on a normal day?
- Is a ritual missing?
- Are roles specific and non-overlapping?
- Does it avoid over-agentification?
- Does the agent preserve the user's voice?
- Is the MVP small enough to build and test?
- Is the MVP oversized?
- Are commands specific enough?
- Are success_metrics present?
- Are risks_and_limits present?

Return required revisions, optional improvements, and a final readiness judgment.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
