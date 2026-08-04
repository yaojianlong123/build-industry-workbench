# Industry modeling guide

Use this reference to turn an unfamiliar occupation into a coherent workbench.

## 1. Classify the operating pattern

Choose one primary pattern and any secondary patterns:

| Pattern | Core record | Typical examples | Critical concern |
|---|---|---|---|
| Appointment | booking | salon, clinic, tutor | capacity and no-shows |
| Project | project/job | photographer, designer | milestones and deliverables |
| Field service | work order | appliance repair, installation | dispatch, parts, proof of service |
| Case | case | legal, consulting, social service | history, deadlines, confidentiality |
| Product/order | order | retail, wholesale | inventory, fulfillment, returns |
| Subscription | account/plan | maintenance contract, membership | renewal, entitlement, churn |
| Asset care | asset | vehicle, appliance, equipment | service history, warranty, condition |

## 2. Discover the business objects

Look for nouns repeatedly created, updated, assigned, scheduled, paid, delivered, or audited. Common objects include Customer, Lead, Job, Booking, Site, Asset, Quote, Contract, Task, Expense, Invoice, Payment, Deliverable, Part, Supplier, Warranty, and Follow-up.

Merge objects when users never need to track them independently. Split objects when they have their own lifecycle, owner, or many-to-one relationship.

## 3. Map the value stream

Model the shortest truthful path:

`Inquiry -> Qualification -> Quote/Booking -> Delivery -> Acceptance -> Payment -> Follow-up`

Rename stages using industry language. For each stage define:

- entry condition;
- responsible role;
- required information;
- next action and due date;
- exit condition;
- exception path.

## 4. Choose modules by evidence

Include a module only if at least one is true:

- it is used weekly;
- missing it causes lost revenue, delay, rework, safety risk, or poor customer experience;
- it is the source of a required document or recurring decision;
- it replaces duplicated tracking.

## 5. Examples

### Photographer

Primary pattern: project plus appointment. Core objects: Client, Inquiry, Shoot, Package, Booking, Contract, Payment, Shot list, Deliverable, and Follow-up. The Today view emphasizes upcoming shoots, preparation gaps, editing deadlines, unpaid balances, and delivery promises.

### Appliance repair

Primary pattern: field service plus asset care. Core objects: Customer, Address, Appliance, Fault report, Work order, Technician, Appointment, Diagnosis, Part, Quote, Service proof, Payment, and Warranty. The Today view emphasizes dispatch, parts readiness, overdue arrivals, unresolved diagnoses, callbacks, and unpaid work.

