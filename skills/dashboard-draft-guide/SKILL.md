---
name: dashboard-draft-guide
description: Design or resume operational Power BI and Fabric dashboards from business tasks, required investigation fields, data-loading choices, an editing plan, and evidence-based acceptance. Use for dashboard briefs and design reviews; implementation uses the host's available authoring tools.
---

# Operational dashboard draft guide

Help the audience find targets, narrow the scope, inspect evidence, and make decisions. Preserve useful existing analysis and retain the reasons behind approved design decisions.

This instruction-only skill works with supplied briefs and schemas. Authoring tools are optional and not bundled. Design-only requests do not authorize publication, scheduling, or data changes.

## Recover the design contract

Inspect supplied sources, actual fields, the user's profile, and the latest handoff before asking questions. Resume from current artifacts and last successful checks. Ask only about unresolved choices that materially change the result. Mark confirmed requirements, reasoned proposals, and assumptions separately.

Read [design contract](references/design-contract.md) for briefs and page redesigns; [loading and editing](references/loading-and-editing.md) for architecture or implementation; [review](references/review.md) for evaluation. Use [request templates](references/request-template.md) when useful.

Recover who investigates which target and for what decision; required basic columns and interaction; actual sources, grain, keys, denominators, time, and missing states; source/serving/model/view windows and refresh; execution scope and acceptance evidence. Existing examples are not current requirements or permissions.

## Prioritize the operator's task

Map `business question → required information → source/relationship → page position → next action → verification`.

For person-linked account/device investigations, normally include readable display name and account identifier as distinct basic columns, with organization context. Follow current required fields and masking/access rules. Aggregate tables may use category labels with navigation to the person-level list. Do not hide required identities only in detail or tooltips. Preserve unmatched targets and explain missing associations; never fabricate a person. Use stable relationship keys, not names.

Each primary KPI needs an audience, a decision or investigation, actual calculation basis, and inspectable targets. Otherwise use it as a contextual attribute or optional proposal. Source availability, technical relevance, and inherited visuals do not establish importance. Technical change counts do not automatically indicate risk or improvement.

Preserve useful existing business questions. Compare the answers provided when removing repetition. Apply later user decisions over earlier drafts and retain reasons for excluding or relocating metrics.

## Design by page role

Use the current language, time zone, viewport, accessibility, and task needs. Do not impose fixed resolution, font, page count, platform scope, or score.

- Overview: readable comparisons, meaningful statistics, clear investigation entry.
- Investigation: useful basic columns, direct search, sufficient visible evidence, preserved selection context.
- Detail: selected target, evidence, observation time, understandable return path.

Spend space on answers. Scale statistics and dense tables by role rather than enlarging all text uniformly. Check long values, counts, legends, clipping, and scrolling in the target viewport. Keep domain colors consistent and labels concise; retain necessary scope/calculation meaning when moving explanations to help.

Plan search, date changes, clear/reset, single-target detail, and Back. Distinguish selected-scope statistics from fixed totals. Define empty, single, and multiple-selection results.

## Choose loading and editing from actual needs

Separate source retention, serving-table retention, model loading, and view filters. Reuse sufficient assets before adding collection or processing layers. State the current structure, proposed change, business/performance reason, added operational burden, and verification.

Distinguish event/observation/collection times, source snapshot, actual model data date, refresh, time zone, missing data, and failure. A last-good fallback must identify the data actually in use.

For implementation, state target artifact, available capability, edit layer/method, scope, and affected checks. Route report files, models, transforms, and browser operations to corresponding installed tools. When unavailable, finish the independent design and identify unperformed implementation; never invent commands or bypass host contracts.

Use one writer per artifact/live UI and read-only reviewers when useful. Batch related edits and expand from representative overview/investigation pages. Protect unsaved human work under the host's rules. Formatting changes do not automatically require ETL rebuilds or model refresh.

Verify current product constraints with official documentation when material. Technical documentation does not determine the user's business priorities.

## Deliver and review

Provide scope, short contract, field/metric mapping, page plan, representative table/layout, loading choice, editing plan, acceptance evidence, assumptions, and next work at an appropriate scale.

Before a passing quality score, classify required fields, target identification, main investigation paths, time/calculation meaning, and preserved analysis as pass/fail/unverified. Missing required columns or unusable tasks cannot be offset by formatting. Separate draft design scores from actual implementation scores. Use the user's rubric with evidence and deductions; do not tell reviewers to achieve a target score. Unmeasured performance stays unmeasured.

Distinguish design, staged changes, applied files, actual render, interactions, publication, schedules, and successful execution. Old evidence does not verify the current artifact.

Record corrections as `problem → reason → principle → applicable scope → verification`. Keep user preferences, project decisions, and applied state in the user's own workspace, not this shared package.
