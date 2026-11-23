# 02: Plan-to-feature matrix and gap analysis

Plan names are generic. Prices are removed.

## Commercial definition of the entry plan (as defined by the owner)

Target: freelancers and solo operators. Includes an AI voice employee (replaces voicemail), CRM, 1 workflow automation, 1 pipeline, 3,000 contacts, 1 user and chat support.

## Configuration checks for each plan

| Check | Why |
|---|---|
| Feature toggles ON match the offer | Customer gets what was sold |
| Feature toggles OFF for everything not sold | Prevents giving away higher-tier features |
| User limit and contact limit set | Enforced by the platform |
| Workflow and pipeline counts | **Not hard-limited by the platform.** They have to be enforced through snapshot contents and onboarding scope |
| Snapshot attached | Without one, provisioning creates an empty account |
| Snapshot contents ⊆ offer | A snapshot with extra assets quietly over-delivers |

## Findings

| Plan | Snapshot attached | Notes |
|---|---|---|
| Entry (Pro) | ✅ | Check the snapshot holds only 1 pipeline and 1 workflow; confirm how AI voice is provisioned (feature toggle vs phone number and agent set-up) |
| Premium AI | ❌ | Purchases would create a blank account |
| Elite | ❌ | Largest feature set (conversations, reputation, social planner, memberships, communities, reporting …) with no snapshot |
| Community | ✅ | No branch in Automation 03a |

## Gap summary

1. Two plans had no snapshot, so their provisioning was incomplete.
2. Workflow and pipeline limits rely on governance, not platform enforcement.
3. "AI voice employee" needed a clear owner: it isn't fully provisioned by the toggle alone.
4. The Community plan had no workflow branch.
5. No written split of who enables what (see 03).
