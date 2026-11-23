# SaaS Provisioning Architecture on GoHighLevel: case study

How a marketing agency sells CRM subscription plans and automatically provisions a configured client account after purchase. I audited the existing provisioning workflow, mapped each plan's features against it, found the gaps, and proposed a responsibility model across sales, onboarding and a specialist build team.

> **Portfolio note.** Contract work for a UK digital-marketing agency, October 2025 – February 2026. The client is anonymised and prices are removed. This is a documentation case study: the system lives in the client's GoHighLevel account.

## The problem

The agency ran GoHighLevel in **SaaS mode**: prospects buy a plan through a Stripe sale link, and a sub-account is created for them. The owner had defined four commercial plans, but:

- Not every plan had a snapshot (template) attached, so some purchases would create blank accounts.
- The provisioning workflow ("Automation 03a") didn't clearly match what each plan promised.
- Nobody had written down which features are switched on at purchase, which during the onboarding call, and which by the specialist build team.
- A fourth plan (Community) had no provisioning branch at all.

## What I delivered

| Deliverable | Doc |
|---|---|
| Current-state map of the provisioning workflow | [`docs/01-provisioning-workflow.md`](docs/01-provisioning-workflow.md) |
| Plan-to-feature matrix and gap analysis | [`docs/02-plan-feature-matrix.md`](docs/02-plan-feature-matrix.md) |
| Responsibility model: Sales / Onboarding / Build team | [`docs/03-responsibility-model.md`](docs/03-responsibility-model.md) |
| Target design with a fourth (Community) branch | [`docs/04-target-design.md`](docs/04-target-design.md) |
| Earlier tier-design exploration (Oct 2025) | [`docs/05-earlier-tier-design.md`](docs/05-earlier-tier-design.md) |

## Skills shown

Requirements analysis · SaaS packaging-to-configuration mapping · workflow architecture · gap analysis · RACI-style responsibility design · stakeholder alignment

## Honest scope

- The provisioning workflow already existed when I started. My work was the audit, the mapping, the gap analysis and the proposed changes.
- The agreed changes depended on sign-off from the owner and the build team. The final state of the workflow is not shown here.
- I used ChatGPT as a thinking partner to structure the analysis. The plan definitions and decisions came from the business.
