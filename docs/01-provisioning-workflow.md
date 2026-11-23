# 01: Provisioning workflow (current state)

## Purchase-to-account flow

```mermaid
flowchart TD
    A[Prospect clicks plan sale link] --> B[Stripe checkout]
    B --> C[GHL SaaS: sub-account created]
    C --> D{Snapshot attached<br/>to this plan?}
    D -- yes --> E[Snapshot loaded:<br/>pipelines, workflows, templates]
    D -- no --> E2[Blank account ⚠️<br/>manual setup needed]
    E & E2 --> F[Automation 03a starts]
    F --> G[Set custom field 'SaaS Plan']
    G --> H[Add to Pipeline 2:<br/>New Customer Overview]
    H --> I[Add to Pipeline 3:<br/>Features & Fulfilment]
    I --> J[Stage: AI Voice & workflow triggers set-up]
    J --> K[Stage: Reviews with AI response set-up]
    K --> L[Send contract + terms of business]
```

## Steps in Automation 03a

| # | Step | Type |
|---|---|---|
| 1 | Create sub-account | SaaS (automatic) |
| 2 | Apply the correct SaaS plan | SaaS (automatic) |
| 3 | Load the correct snapshot | SaaS (automatic, if attached) |
| 4 | Update custom field "SaaS Plan" | Workflow action |
| 5 | Add client to Pipeline 2: New Customer Overview | Workflow action |
| 6 | Add client to Pipeline 3: Features and Fulfilment | Workflow action |
| 7 | Move to stage "AI Voice and WF Triggers (set up)" | Workflow action / human task |
| 8 | Move to stage "Reviews with AI Response (set up)" | Workflow action / human task |
| 9 | Send contract | Workflow action |
| 10 | Send terms of business | Workflow action |

## Key insight

**A feature being enabled is not the same as a feature being provisioned.** A plan's toggles make a feature *available* in the account. Whether it's *configured* (an AI voice agent with a phone number and script, a review-response workflow) depends on the snapshot or on human work. The audit treated those as two separate questions.
