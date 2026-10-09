# Design contract

Read existing material before asking questions. A narrow change needs only the affected contract.

| Item | Establish |
|---|---|
| Task | Who investigates what and which decision follows |
| Required information | Basic identity/context, target, state, and relevant time |
| Navigation | Overview/search → scope → target list → detail → return/reset |
| Data meaning | Actual fields, grain, stable keys, denominator, time, missing states |
| Operations | Source/serving/model/view windows, freshness, fallback, existing assets |
| Acceptance | Required field/task checks, quality rubric, draft vs implementation evidence |

Mark confirmed/proposed/unresolved. For each required item show `requirement → source/key → basic screen position → owner → verification`. Surface missing fields and realistic remedies. Do not replace required identity with a technical statistic.

For person-linked investigations, default to display name and account identifier, with organizational context. Preserve IDs for matching and navigation. Respect masking/role requirements and aggregate or anonymous tasks. Preserve unmatched fact rows and describe the missing association. Current directory ownership/department is not historical ownership/department.

Specify the cards, charts, and lists each selection filters. Label fixed totals. Define empty/single/multiple/clear/reset/Back states and single-target selection requirements.

## Metric admission

Each primary metric needs (1) question/audience, (2) decision or follow-up, (3) actual fields/denominator/exclusions/time/comparison, (4) inspectable evidence.

A technical attribute may be useful in detail without being useful as a total. For example, a management-agent version can aid device diagnosis while a total version-change count has no clear operational decision. Do not invent risk thresholds or normalize unknown/unsupported/failed collection to zero. Label provisional policy assumptions.

Preserve historical comparison, distribution, and selected-event evidence when redesigning. Similar shapes can answer different questions.

Overview needs comparison and investigation entry. Investigation needs visible evidence, direct search, and useful columns. Detail needs target and context. Large desktop canvases, mobile screens, wallboards, and accessibility tasks need different density choices. Use the request language; do not infer time zone from language alone.

## Private learning record

Keep `problem | why it mattered | principle | scope | verification | current decision` in the user's selected workspace. Separate reusable preferences from project platform exclusions, schedules, coordinates, and applied state. Later decisions override old proposals. Questioning an aggregate's value does not permanently forbid its underlying field.
