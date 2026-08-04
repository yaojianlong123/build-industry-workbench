# Page and interaction design

## Navigation map

Organize pages by user intent, not database tables. Prefer 4–7 primary navigation items. Typical groups are Today, Customers, Work, Calendar, Money, Resources, and Settings; rename or remove them to match the industry.

For each navigation item state its primary user, frequency, key question answered, and related records.

## Page specification

For every core page define:

1. user and job-to-be-done;
2. entry points and next destinations;
3. information hierarchy;
4. primary and secondary actions;
5. filters, search, sorting, and saved views;
6. permissions and sensitive information;
7. desktop and mobile behavior;
8. empty, loading, error, offline, success, and permission-denied states when relevant;
9. acceptance criteria.

## Text wireframe

Use this format when a visual canvas is unavailable:

```text
[Page title]                         [Primary action]
[Context / urgent alert]

[Key metric] [Key metric] [Key metric]

[Priority work / main table ----------------------]
  Filters | Search | View switch
  Row/card with status, owner, next action, due time

[Secondary panel]        [Recent activity / reminders]
```

Annotate what is fixed, scrollable, clickable, conditional, or role-specific. A wireframe must communicate priority and behavior, not decoration.

## Dashboard rules

- Put urgent work and next actions above retrospective charts.
- Keep decision metrics limited and link them to underlying records.
- Make status color supportive, never the only signal.
- Put the most frequent action within one interaction on mobile.
- Avoid showing all modules on the homepage.

## Review checkpoint

Review the page map and one representative page before detailing every page. Ask whether anything important is missing, whether the priority order matches daily work, and whether the terminology feels natural.

