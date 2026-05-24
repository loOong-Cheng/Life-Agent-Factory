# Domain Patterns

Use domain patterns to classify the life loop before designing an agent. A pattern is not a persona; it is a recurring human loop with typical failure points, memory needs, and boundaries.

## How To Choose A Domain Pattern

- Choose based on the life loop, not the topic name.
- One topic may contain multiple patterns.
- Prefer the smallest pattern that closes the most important broken loop.
- Mark `sensitivity_level` when privacy, health, relationships, addiction, or identity are involved.

## practice_domain

when_to_use: Skill practice like dance, language, instrument, coding, fitness technique, sport, drawing, or craft repetition.

core_loop: practice -> feedback -> correction -> repeat -> progress review

typical_broken_points:
- practice is not recorded
- feedback is not carried forward
- progress is invisible
- user practices too broadly without focus

suitable_agent_roles:
- practice reflector
- pattern tracker
- focus setter

memory_considerations:
- remember practice focus, feedback, corrections, felt sense, drills, wins, and next focus
- keep progress summaries modest and evidence-bound
- avoid turning practice into constant scoring

risks_and_boundaries:
- do not replace a teacher, coach, clinician, or embodied practice
- do not claim objective skill level from weak evidence
- treat video or sensor feedback as provisional

mvp_bias: One short post-practice log and one lightweight weekly progress review.

## experiment_domain

when_to_use: Cooking, skincare, sleep experiments, productivity experiments, setup experiments, or repeated personal trials.

core_loop: hypothesis -> attempt -> observe result -> reflect -> revise -> repeat

typical_broken_points:
- variables are not recorded
- failures repeat
- versions are not tracked
- results are not connected to next attempt

suitable_agent_roles:
- experiment reflector
- version archivist
- next-attempt planner

memory_considerations:
- remember versions, variables, constraints, observed results, repeated failures, preferences, and next attempt
- distinguish repeated patterns from one-off impressions
- avoid overfitting from a single attempt

risks_and_boundaries:
- do not make unconfirmed health, diet, or safety claims
- do not turn experiments into admin work
- keep the loop playful and practical where appropriate

mvp_bias: One experiment log and one next-attempt recommendation from prior self-reports.

## knowledge_domain

when_to_use: Research, paper reading, books, courses, PKM, strategy thinking, or complex learning.

core_loop: collect -> summarize -> connect -> question -> synthesize -> output

typical_broken_points:
- notes accumulate without synthesis
- ideas scatter
- reading does not become writing
- uncertainty is not tracked

suitable_agent_roles:
- question synthesizer
- evidence archivist
- uncertainty tracker

memory_considerations:
- remember questions, claims, evidence, uncertainties, sources, discarded paths, and next inquiry
- keep uncertainty attached to claims
- summarize by active question or output, not note volume

risks_and_boundaries:
- do not treat synthesis as certainty
- do not reward accumulation without thinking
- do not flatten weak evidence into strong claims

mvp_bias: One capture ritual for an active thread and one periodic synthesis into an output.

## behavior_change_domain

when_to_use: Habits such as smoking reduction, alcohol reduction, phone overuse, sleep schedule, spending impulses, or other high-friction behavior loops.

core_loop: trigger -> urge -> pause -> choose -> log -> reflect -> plan next high-risk moment

typical_broken_points:
- agent cannot observe unreported behavior
- user feels shame after slips
- triggers are not identified
- next high-risk moment is not planned

suitable_agent_roles:
- urge companion
- slip recovery guide
- pattern planner

memory_considerations:
- remember only self-reported urges, slips, triggers, coping actions, reflections, and next high-risk plans
- acknowledge incomplete self-report
- focus on low-friction honesty and correction
- avoid surveillance or passive inference by default

risks_and_boundaries:
- no shame or moralizing
- no surveillance by default
- acknowledge incomplete self-report
- suggest professional support when dependency or health risk is possible
- do not provide diagnosis or medication instructions

mvp_bias: One urge log, one slip recovery log, and one daily or weekly reflection.

## relationship_reflection_domain

when_to_use: Reflecting on relationships, maintaining meaningful contact, remembering important people, noticing distance or closeness, or deciding whether to reach out.

core_loop: notice -> record interaction or thought -> reflect -> decide action or release -> review relationship pattern

typical_broken_points:
- meaningful interactions are forgotten
- important people disappear from attention
- relationship maintenance becomes guilt-driven
- user cannot distinguish natural distance from neglected care

suitable_agent_roles:
- relationship reflector
- contact memory keeper
- boundary checker

memory_considerations:
- remember user-confirmed relationship context, meaningful interactions, desired care rhythms, boundaries, and unresolved questions
- avoid storing sensitive details about other people without care
- keep reminders consent-based and non-guilt-driven

risks_and_boundaries:
- do not treat people as tasks
- do not infer others' intentions with certainty
- protect privacy and consent
- avoid manipulation or optimization of other people
- avoid guilt-based reminders

mvp_bias: One reflective contact or interaction log and one gentle review of desired care, distance, or next action.

## health_reflection_domain

when_to_use: Wellness summaries, Apple Health or wearable data reflection, body state review, medical document preparation, symptom context gathering, or doctor-visit preparation.

core_loop: collect data -> summarize -> detect pattern -> reflect on context -> prepare questions or habit adjustment -> review

typical_broken_points:
- data exists but is not summarized
- daily signals are disconnected from lived context
- reports are hard to interpret
- user does not know what to ask a doctor

suitable_agent_roles:
- health reflection guide
- data summarizer
- question preparer

memory_considerations:
- treat health data as high-sensitivity private data
- remember user-approved summaries, context, questions, and professional follow-ups
- avoid retaining raw sensitive data unless clearly needed and consented
- preserve uncertainty around patterns

risks_and_boundaries:
- not a doctor
- no diagnosis
- no medication instructions
- no false reassurance
- no panic from single data points
- recommend professional care when appropriate
- handle health data as high-sensitivity private data

mvp_bias: One health-context summary and one question-preparation ritual for a review or appointment.

## meaning_values_reflection_domain

when_to_use: Meaning, values, direction, identity, life choices, career direction, transitions, ambition, grief, or value conflict.

core_loop: lived experience -> reflection -> value clarification -> tension mapping -> small action experiment -> review

typical_broken_points:
- feelings are not reflected on
- stated values and daily actions diverge
- user gets stuck in abstract reflection
- decisions are driven by anxiety or external validation
- value conflicts remain implicit

suitable_agent_roles:
- reflection guide
- tension mapper
- experiment planner

memory_considerations:
- remember language that resonates, recurring tensions, value hypotheses, small experiments, and what felt true or false afterward
- treat identity claims as provisional
- preserve multiple interpretations

risks_and_boundaries:
- do not decide the user's purpose
- do not agree by default
- use constructive friction
- reframe strong claims into questions
- offer multiple interpretations
- avoid turning temporary moods into identity claims
- encourage small action experiments
- avoid therapy replacement

mvp_bias: One reflection ritual that ends in a small action experiment and later review.
