# Workbench deliverable template

Use the sections below. Scale detail to the request; do not fill space mechanically.

## 1. One-sentence design

State who the workbench serves, which work it controls, and the primary outcome.

## 2. Assumptions

List only assumptions that materially affect the design. Mark each as confirmed or assumed.

## 3. Daily home

Describe the Today view in priority order. Include quick actions, alerts, upcoming work, stalled work, and money/customer-risk indicators.

## 4. Core workflow

Show the main stages and exception branches in industry language. Define the owner and completion condition of each stage.

## 5. Modules

For each module provide:

- purpose;
- primary users;
- essential views;
- important quick actions.

Classify modules as Core, Recommended, or Later.

## 6. Data model

For each record type provide essential fields only:

| Record | Purpose | Essential fields | Related records |
|---|---|---|---|

For choice fields, list allowed values. Identify calculated fields and unique identifiers.

## 7. Status rules

| Record | Status | Enter when | Exit when | Next action |
|---|---|---|---|---|

Keep operational, fulfillment, and payment statuses separate.

## 8. Automations

Express each automation as `trigger -> conditions -> action -> fallback`. Label it Core or Optional. Include human review for irreversible or customer-facing actions.

## 9. Templates and forms

List intake forms, checklists, quotes, reports, messages, and handoff documents. Specify which fields they read or create.

## 10. Decision metrics

Give no more than seven initial metrics. For each, state the decision it supports, formula, source records, and cadence.

## 11. Permissions and data care

Define roles, sensitive fields, retention, export/backup expectations, and local compliance questions where relevant.

## 12. Implementation plan

Split into:

- Day 1: minimum structure;
- Week 1: import and real-world trial;
- Week 2+: automation and refinement.

Include sample records and acceptance tests covering normal, exception, and repeat-customer scenarios.

## 13. Page map and wireframes

Provide primary navigation, page hierarchy, one annotated wireframe per core page, responsive priorities, states, and acceptance criteria.

## 14. Visual direction

Record the selected direction, rejected alternatives and reasons, sourced reference principles, color and typography roles, density, components, accessibility rules, and design tokens.

## 15. Decision log

Separate confirmed decisions, assumptions, open questions, and deferred ideas. Preserve this log in implementation handoffs.

## 16. Build prompt

When another AI or application will implement the workbench, finish with a standalone prompt containing the target platform, schema, relationships, page specifications, visual tokens, responsive rules, states, sample data, and acceptance criteria. Instruct it to report any unsupported feature instead of silently dropping it.
