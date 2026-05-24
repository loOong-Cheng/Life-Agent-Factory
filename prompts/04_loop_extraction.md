# 04 Loop Extraction

## Purpose

Select the smallest repeatable life loop worth supporting.

## Input

- normalized_desire
- domain_type
- candidate_loops
- domain_implications

## Output

- core_loop:
  - name
  - trigger
  - current_pattern
  - desired_pattern
  - output
- broken_points:
  - point
  - impact

## Constraints

From the candidate loops, choose one MVP loop. It should be concrete enough to run this week.

Describe:

- loop name
- when it begins
- what the user does
- what the agent asks or observes
- what artifact is produced
- how the next loop improves because of it
- where the loop breaks, stalls, gets forgotten, or loses value

Reject loops that require too much setup, too much memory, or too much behavior change.
Do not propose implementation, code, automations, database schemas, or full agent architecture at this stage.
