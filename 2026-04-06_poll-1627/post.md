[Atlas Edit Weekly Cycle Proposal - April 6, 2026](https://raw.githubusercontent.com/sky-ecosystem/polls/refs/heads/main/2026/2026-04-06-Atlas-edit-weekly-cycle-proposal.md)

**Summary**

This Atlas Edit Weekly Cycle Proposal (PR #219) bundles 11 disclosed top-line changes:

- **Three-Stage Staking Rewards Framework** — Replaces the current simple Step 4 Capital allocation (buybacks + surplus buffer) with a three-stage progression: Stage 0 (current), Stage 1 (reduced SKY reward rate from reserves), and Stage 2 (direct Step 4 allocation to SKY buybacks, USDS staking rewards, and surplus buffer).
- **Raise Target Aggregate Backstop Capital** from 125M to 150M USDS and introduce a Genesis Capital Phase-Out mechanism.
- **Add Avalanche SkyLink Bridge** documentation with freezer multisig (2/5), rate limits (5M USDS/day), and validator parameters.
- **Add Solana Pioneer Chain Instance to Keel** and **designate Grove as Avalanche Pioneer Prime** with associated configuration documents.
- **Add Grove's Distribution Reward Instance** (Reward Code 2002).
- **Add Maple syrupUSDC Maximum Exposure** limit of 0 USD.
- **Remove obsolete Keel Ecosystem Accord documents**, **update Scope Facilitator → Core Facilitator** references, **update SubDAO Proxy → Spark's Prime Treasury** references, and **expand SLL/GLL abbreviations**.

**Decision: YES**

The proposal contains 11 substantive and housekeeping changes that collectively advance the Sky Ecosystem's maturity and operational capabilities:

- The **three-stage staking rewards framework** creates a well-structured path from treasury-funded rewards to direct Step 4 Capital allocation, with clear activation criteria for each stage.
- The **backstop capital increase** and **Genesis Capital Phase-Out** strengthen the risk framework while encouraging Agent independence.
- **Avalanche SkyLink Bridge** and **Pioneer Prime designations** expand multi-chain capabilities using established patterns.
- **Cleanup and terminology updates** improve Atlas clarity and accuracy.

All PR diff changes that are not explicitly listed in the proposal description were verified as derivative/supporting implementation details of disclosed top-line changes — including the Pioneer Prime Requirements harmonization, which removes a clause that was never operationally enforced in the Designation Process (A.2.2.8.3.1.2). No validation checks produced FINDINGs.

[Full rationale](https://github.com/br3nd3n-the-n2vig2t0r/brendan-vote-analysis/blob/main/2026-04-06_poll-1627/rationale.md)