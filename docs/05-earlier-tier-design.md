# 05: Earlier tier-design exploration (October 2025)

Before the live plans were set, I explored a three-tier model (Essential, Growth, Accelerator) and how each tier could map to its own GHL snapshot. This was a **design exploration, drafted with AI assistance from the business's tier document, and not built**. The live plans later took different names and features (see 02).

## The pattern it established

- **One snapshot per tier, built cumulatively:** Essential → clone → Growth → clone → Accelerator. Each step adds features, so the tiers stay consistent.
- **Tier recorded in a field or tag** on the sub-account, so workflows can branch on it.
- **Limits enforced through three levers:** platform limits (users, contacts), snapshot contents (pipelines, workflows), and monitoring (contact-count alerts through the API to prompt upgrades).
- **Provisioning options:** manual snapshot selection, or API-driven (create location → apply snapshot → tag → trigger onboarding).

That cumulative-snapshot pattern carried into the later audit.
