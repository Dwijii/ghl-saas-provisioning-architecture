# 04: Target design

## Branching by plan

```mermaid
flowchart TD
    T[Trigger: SaaS plan purchased] --> S{SaaS Plan field}
    S -->|Entry| E1[Load entry snapshot] --> E2[Onboarding tasks: AI voice set-up] --> X
    S -->|Premium AI| P1[Load Premium AI snapshot ⬅ new] --> P2[Onboarding + build tasks] --> X
    S -->|Elite| L1[Load Elite snapshot ⬅ new] --> L2[Onboarding + build tasks] --> X
    S -->|Community| C1[Load community snapshot] --> C2[Portal access + community base ⬅ new branch] --> C3[Onboarding: groups, rules, moderation] --> X
    X[Common tail: pipelines 2 & 3, contract, terms, notify team]
```

## Change list proposed

1. Build and attach snapshots for Premium AI and Elite.
2. Add a Community branch to Automation 03a.
3. For each branch, create onboarding-call and build-team tasks from the responsibility model.
4. Notify the team on purchase (internal message plus a task) so no new account waits.
5. Document which limits the platform enforces and which governance enforces.

## Sign-off process

Owner and build team review the matrix → agree the A/B/C split per plan → update Automation 03a → test-purchase each plan in Stripe test mode → check the account contents against the offer.
