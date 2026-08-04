---
name: build-industry-workbench
description: Guide ordinary users from initial discovery through functional requirements, information architecture, page wireframes, visual style references, design system, validation, and implementation of a practical personal or small-team workbench for any trade, profession, or service industry. Use when a user wants an industry-specific workspace, dashboard, operating system, CRM, order tracker, client portal, page design, UI style, prototype, automation plan, or implementation prompt for tools such as Notion, Feishu, Airtable, spreadsheets, no-code builders, or custom web apps. Suitable for photographer, appliance-repair, consultant, clinic, retail, creator, field-service, and other industry workbenches.
---

# Build Industry Workbench

Turn a plain-language industry description into a small, usable operating system. Optimize for ordinary users: use familiar business language, minimize setup, and prioritize daily actions over decorative dashboards.

## Operating modes

Infer the mode from the request. If a non-expert asks to start from scratch, use **Guided**.

- **Quick**: Give a compact recommended structure with sensible defaults.
- **Guided**: Lead the user through short stages from needs to an approved design. Ask one decision-sized group of questions at a time.
- **Blueprint**: Produce the complete workbench specification.
- **Design**: Create page maps, wireframes, visual directions, and a design system from an approved blueprint.
- **Build**: Create or configure the workbench in the user's named platform when suitable tools are available.
- **Adapt**: Translate an existing workbench into another industry or platform without losing its business logic.

## Workflow

### 1. Run guided discovery

Read [guided-discovery.md](references/guided-discovery.md). Extract what the user already supplied. Ask only questions whose answers would materially change the design, at most five at once. Use everyday examples and selectable recommendations instead of asking users to invent product terminology.

Start with:

1. Who uses it: solo operator, shop, field team, or multi-role company?
2. What is sold: service, product, project, appointment, subscription, or a mixture?
3. What is the main journey from inquiry to completion and after-sales?
4. Which platform should host it, if any?
5. What is the most painful current problem?

Do not ask later-stage visual or technical questions during the first exchange. Do not block on missing answers when reasonable defaults are safe. State assumptions and produce a first version the user can correct.

### 2. Model the industry

Read [industry-model.md](references/industry-model.md). Identify the industry's:

- money-making unit;
- customer journey;
- recurring operational objects;
- time-critical events;
- documents and media;
- quality, safety, privacy, or compliance constraints;
- key decisions and exceptions.

Use the smallest set of modules that covers the actual workflow. Avoid copying generic CRM modules that have no daily purpose.

### 3. Define and prioritize requirements

Convert pain points into outcome statements, then into capabilities. Classify each capability as **Must now**, **Useful next**, or **Later**. Explain why each Must item matters. Detect conflicts such as “very simple” plus “full ERP” and recommend a smaller first release.

Create a short requirements confirmation containing users, goals, main workflow, Must capabilities, exclusions, and assumptions. In Guided mode, obtain confirmation before detailed page design unless the user asks for an immediate complete draft.

### 4. Design around daily work

Start with a **Today** view that answers: what needs attention, what is late, what happens next, and where money or customer trust is at risk.

Then define:

- records and relationships;
- lifecycle statuses with explicit entry and exit conditions;
- role-specific views;
- forms and templates;
- reminders and automations;
- metrics tied to decisions;
- a low-friction mobile workflow when work happens in the field.

Every field must support a decision, handoff, search, automation, audit, or report. Remove fields that do none of these.

### 5. Design pages and interactions

Read [page-design.md](references/page-design.md). Create the navigation map first, then specify each core page. Produce low-fidelity text wireframes when no visual artifact tool is available. Cover desktop and mobile priorities, empty/loading/error states, permissions, and destructive-action confirmation.

In Guided mode, present the page map and one representative core page first. Apply the user's feedback across the remaining pages.

### 6. Establish the visual direction

Read [visual-style.md](references/visual-style.md). Ask for existing brand assets or references only after the workflow and page map are stable. If none exist, recommend two or three distinct, industry-appropriate directions with tradeoffs.

When browsing or image-search tools are available and references would materially help, collect a small set of relevant current references and cite their sources. Use references for principles such as density, hierarchy, color mood, navigation, and component treatment; do not copy a product's distinctive identity or layout wholesale.

Turn the chosen direction into reusable design tokens and component rules. When image or UI-generation tools are available, create a representative mockup only after a direction is selected.

### 7. Produce the deliverable

Follow [deliverable-template.md](references/deliverable-template.md). Keep the executive summary understandable without technical knowledge. Put schemas, formulas, and implementation details after the user-facing workflow.

If the user names a platform, also read [platform-adapters.md](references/platform-adapters.md) and translate the neutral design into that platform's primitives. Do not claim implementation unless it was actually performed and verified.

### 8. Validate the design

Walk through at least three realistic scenarios:

- a normal job from first contact to payment;
- a delayed, cancelled, failed, or disputed job;
- a returning customer or after-sales case.

Check that each scenario has a clear owner, next action, status transition, and source of truth. Simplify any workflow that requires duplicate entry.

Also check visual accessibility, responsive behavior, empty/error states, and consistency between the approved requirements, pages, and components. In Guided mode, finish with a decision log and a clear next step: revise, prototype, or build.

## Design rules

- Prefer one source of truth per business object.
- Separate pipeline stage from task status and payment status.
- Use human-readable labels; introduce technical names only for implementation.
- Make defaults useful for a beginner but mark industry-specific assumptions.
- Prefer a minimum viable workbench that works this week over a comprehensive ERP.
- Treat personal data, health data, financial data, access control, backups, and retention explicitly when relevant.
- Never invent legal or regulatory requirements. Flag them for local verification.
- Show optional enhancements separately so the core does not feel mandatory.
- Do not ask the user to choose from unexplained design jargon. Show plain-language options and recommend one.
- Do not choose colors and decoration before the information hierarchy is sound.
- Distinguish inspiration from imitation and preserve source attribution for external references.

## Cross-software portability

Keep the canonical output platform-neutral. Represent the system as pages, records, fields, relationships, views, rules, and automations. This lets another AI assistant or software product translate it.

When handing off to another AI, include:

1. the neutral blueprint;
2. the target platform and constraints;
3. a build prompt with acceptance criteria;
4. sample records for testing;
5. a warning not to omit relationships or status rules.
