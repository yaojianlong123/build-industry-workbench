# Platform adapters

First design a platform-neutral blueprint. Then apply only the relevant adapter.

## Documents and knowledge tools

Examples: Notion-like or wiki tools.

- Map record types to databases/collections.
- Map relationships to relation fields and rollups.
- Map Today and role views to filtered linked views.
- Use templates for repeatable jobs and checklists.
- Keep automations modest unless the platform explicitly supports them.

## Spreadsheet tools

- Map each record type to a table/sheet with a stable ID column.
- Use validation lists for controlled statuses.
- Use lookup/query formulas for relationships; avoid fragile row-number references.
- Separate raw records, operational views, and metrics.
- Add an exceptions sheet for missing IDs, invalid transitions, and overdue work.

## Relational databases and low-code tools

- Create normalized tables for independently tracked objects.
- Use foreign keys or relationship fields, not duplicated names.
- Add role views, forms, and explicit status-transition actions.
- Protect calculated and audit fields from casual editing.
- Specify indexes, uniqueness, and deletion behavior when technical detail is appropriate.

## Task and project tools

- Use projects or boards for jobs with meaningful lifecycles.
- Use tasks for actions, not for customers or assets.
- Store customer, asset, and payment data in custom objects if supported; otherwise link to a source-of-truth table.
- Separate stage columns from assignee and due date.

## Custom web application

- Define navigation, responsive page behavior, empty/loading/error states, and access roles.
- Translate records into entities and APIs; translate views into queries.
- Include validation, audit history, export, backup, and test fixtures.
- Design mobile-first flows for field workers and desktop-first planning for coordinators.

## Generic AI handoff

If the target software is unknown, deliver plain Markdown plus machine-readable tables. Avoid product-specific syntax. Ask the receiving system to confirm supported features before building and to preserve IDs, relationships, statuses, and acceptance tests.

