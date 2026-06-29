# Analysis: Atlas Edit Weekly Cycle Proposal - June 22, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-22T21:51:03.154Z | **Atlas:** 2026-06-22
**Analysis guidance reviewed against Atlas:** 2026-06-19

## Summary

This poll asks SKY holders to approve Atlas PR #265, a weekly-cycle Atlas edit with twelve disclosed change groups: Core Council discretionary authority, short-term Treasury Allocation modification authority, standing Sky Frontier Foundation transfer authorizations from specified Executor Agents, AD repeat-breach timing clarification, Grove Diamond PAU documentation, BUIDL/JTRSY Tokenized Treasury Basin documentation, Agent Rate scope clarification, July 2026 Grove and Skybase foundation grants, Distribution Reward Code ranges, Core Council Risk Advisor real-time data scope, and removal of Elodin as Keel's named Development Company.

## Atlas Alignment

**Assessment:** aligned

The proposal uses the Atlas Edit Weekly Cycle process, is triggered by Ranked Delegate Bonapublica, and uses the disclosed 480,000,000 SKY minimum positive participation threshold. The material edits are governance-heavy but are presented transparently in the poll text, forum thread, PR body, and composed PR diff. The discretionary-authority and Treasury Allocation changes increase Core Council latitude and therefore deserve medium risk treatment, but they retain public forum-post and confirmation steps and still require Executive Vote execution for implementation. The grants, transfer authorizations, allocator documentation, tokenized treasury records, reward-code records, and Agent Rate clarifications are disclosed in the PR diff and appear bounded to the stated policy or documentation purposes.

**Relevant sections:** A.0.1.1.18, A.0.1.2.1, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.2, A.1.11.2.1.3, A.1.11.2.4, A.2.3.1.5, A.2.8.2.5.2.4, A.2.8.2.7.2.2.3.1, A.2.8.2.8.2.2, A.2.8.2.9.2.2, A.3.1.2.3, A.6.1.1.2.2.6.1.2.1.1.1.4, A.6.1.1.2.2.6.1.3.1.14.2

## Risk Assessment

**Level:** medium

- The proposal materially shifts some discretionary authority from the Core Facilitator to the Core Council and adds short-term authority for Core Council Treasury Allocation modifications that may proceed directly to an Executive Vote without a prior Governance Poll.
- The proposal creates standing authorizations for Amatsu, Ozone, and Core Council Executor Agent 1 to transfer funds from Genesis Capital Allocations to the Sky Frontier Foundation without a separate governance decision for each transfer.
- The July 2026 grants are economically material: 800,000 USDS from Grove's Prime Treasury to the Grove Foundation Multisig and 700,000 USDS from Skybase's SubProxy to the Skybase Foundation Operational Multisig.
- The Grove Diamond PAU and Tokenized Treasury Basin documentation introduces many contract addresses, role records, rate limits, and operational procedures, but the poll itself merges Atlas documentation and does not execute on-chain changes.
- The BUIDL/JTRSY interim deployment documentation sets a combined 5 million USDS maximum allocation across the two Tokenized Treasury Basin instances and documents 5 million USDS/day inflow rate limits plus unlimited outflow limits.
- The AD repeat-breach, Agent Rate, Distribution Reward Code, risk-data scope, and Keel Development Company edits are bounded clarifications or records updates.

## Validation Checks

### Analysis Run and Atlas State

**Status:** OK

Analysis run marker: brendan-analysis:1638:2026-06-22T21-48-38-556Z:bbf423

- `analysis start 1638` created local proposal directory `2026-06-22_poll-1638` for this rerun.
- `atlas refresh` reported active Atlas version `2026-06-22`.
- `atlas current` confirmed active Atlas version `2026-06-22`.
- The analysis guidance marker in `skills/sky-delegate/references/analyze.md` is `2026-06-19`, so guidance is stale against the active downloaded Atlas.
- Active `2026-06-22` Atlas reads resolve the A.0/A.1 process and AD sections used by this analysis directly.

**Evidence**

- Command: `bun run src/index.ts analysis start 1638` returned marker `Analysis run marker: brendan-analysis:1638:2026-06-22T21-48-38-556Z:bbf423`.
- Command: `bun run src/index.ts atlas refresh` returned `Atlas active version: 2026-06-22`.
- Command: `bun run src/index.ts atlas current` returned `Atlas active version: 2026-06-22`.
- File check: `skills/sky-delegate/references/analyze.md` records `_Analysis Review State: 2026-06-19_`.
- Commands: `read-atlas-section A.0.1.1.18`, `read-atlas-section A.1.6.2.2`, `read-atlas-section A.1.6.6.2`, `read-atlas-section A.1.11.2.1.3`, and `read-atlas-section A.1.11.2.4` all resolved from the active `2026-06-22` Atlas.

### Proposal Fetched

**Status:** OK

- `resolve-target 1638` resolved the target as poll ID 1638 and directory `2026-06-22_poll-1638`.
- `fetch-proposal 1638` returned active poll `Atlas Edit Weekly Cycle Proposal - June 22, 2026`.
- Voting window: starts `2026-06-22T16:00:00.000Z`, ends `2026-06-25T16:00:00.000Z`.
- Options are `0: Abstain`, `1: Yes`, `2: No`.
- Portal URL: `https://vote.sky.money/polling/QmdXjfm6`.
- Proposal source URL: `https://raw.githubusercontent.com/sky-ecosystem/polls/refs/heads/main/2026/2026-06-22-Atlas-edit-weekly-cycle-proposal.md`.
- Discussion URL: `https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-22/27983`.

**Evidence**

- Command: `bun run src/index.ts resolve-target 1638` returned `{ "type": "poll", "pollId": 1638, "dirName": "2026-06-22_poll-1638" }`.
- Command: `bun run src/index.ts fetch-proposal 1638` returned poll metadata, portal summary, canonical proposal text, proposal source URL, and discussion link.

### Governance Process and Trigger

**Status:** OK

- The canonical proposal says the Core Facilitators placed an Atlas Edit Weekly Cycle Proposal into the voting system on behalf of Ranked Delegate Bonapublica.
- Forum topic `27983` post #2 by `Bonapublica` at `2026-06-22T09:47:04.401Z` says `bonapublica_AD` triggers the `Atlas_Edit_Weekly_Proposal` for the week of `2026-06-22` under `A.1.11.2.1.3 - Triggering Requirement`.
- The vote.sky.money delegates API returned Bonapublica with `status: aligned`, `communication: 100%`, `combinedParticipation: 100%`, and `skyDelegated: 1075288126.766152512174361897`.
- The active `2026-06-22` Atlas identifies Bonapublica as the current Level 2 Ranked Delegate under `A.1.6.4.1.2.3.1`, and `A.1.11.2.1.3` states the Core Facilitator is responsible for confirming the Ranked Delegate and AD Buffer trigger requirements.
- The active poll's existence and canonical text provide Core Facilitator placement evidence. I did not independently observe a public AD Buffer balance, but the public process evidence is sufficient for this analysis because the Atlas assigns that confirmation duty to the Core Facilitator.

**Evidence**

- Command: `bun run src/index.ts fetch-proposal 1638` returned canonical text: the poll was placed by Core Facilitators on behalf of Ranked Delegate Bonapublica.
- Command: `curl https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-22/27983.json` returned post #2 by `Bonapublica` triggering PR #265 under `A.1.11.2.1.3`.
- Command: `curl https://vote.sky.money/api/delegates` filtered for Bonapublica returned status `aligned`, 100% communication, 100% combined participation, and about 1.075B SKY delegated.
- Commands: `read-atlas-section A.1.11.2.1.3` and `read-atlas-section A.1.6.4.1.2.3.1` resolved from active Atlas `2026-06-22`; `A.1.6.4.1.2.3.1` names Bonapublica as the current Level 2 Ranked Delegate.

### Governance Process and Threshold

**Status:** OK

- The poll uses the Atlas Edit Weekly Cycle process and a three-day window from Monday June 22, 2026 at 16:00 UTC to Thursday June 25, 2026 at 16:00 UTC.
- The canonical text says this is a binary vote and that PR #265 will be merged if Yes exceeds No and Yes is at least 480,000,000 SKY.
- The active `2026-06-22` Atlas states under `A.1.11.2.4 - Minimum Positive Participation` that Atlas Edit Weekly Cycle Proposals must have at least 480,000,000 SKY equivalents of Yes votes to be accepted.

**Evidence**

- Command: `bun run src/index.ts fetch-proposal 1638` returned victory conditions including `comparison >= 480000000` and options Abstain/Yes/No.
- Command: `read-atlas-section A.1.11.2.4` resolved from active Atlas `2026-06-22` and returned the 480,000,000 SKY threshold.

### Portal Summary vs Canonical Text

**Status:** OK

- The portal summary lists the same twelve change groups as the canonical proposal and forum post.
- The canonical proposal expands those groups with links to PR #265 and the discussion thread, explains the binary voting format, and states the merge outcome.
- I did not identify a substantive omission in the portal summary relative to the canonical proposal text.

**Evidence**

- Command: `bun run src/index.ts fetch-proposal 1638` returned both the portal summary and full canonical proposal text.
- The summary and canonical text both enumerate: Core Council discretionary authority, Treasury Allocation modification, Sky Frontier transfers, AD repeat-breach timing, Grove Diamond PAU, BUIDL/JTRSY Tokenized Treasury Basins, Agent Rate scope, Grove grant, Skybase grant, reward-code ranges, Risk Advisor real-time data scope, and Keel/Elodin removal.

### Canonical Text vs Atlas PR Diff

**Status:** OK

- `fetch-atlas-pr-diff 265` returned PR #265 as open, authored by `adamgfraser`, created `2026-06-22T03:12:23Z`, with 224 files changed, 1,761 additions, and 308 deletions.
- GitHub's direct diff was too large, so the tool composed a pinned diff from base SHA `bb4d09838c52adb180dce4023b82c54e7c22f6e1` to head SHA `338a368fad5745ac6f9bb79850e43fc77f33d962`.
- The composed diff has SHA-256 `16c92fb9b1f06d123a13b8bfd9e712f10229537cbd3926fdd3bd9badfe5c6423`, 168 changed Atlas sections, and 4 review batches.
- I reviewed batches 1/4 through 4/4. The diff matches the twelve disclosed change groups and I did not find an undisclosed independent policy change.
- The large Grove section contains many supporting renumberings, role-document relocations, and controller/function documentation. These support the disclosed Grove Diamond PAU and Tokenized Treasury Basin changes rather than introducing a separate hidden action.

**Evidence**

- Command: `bun run src/index.ts fetch-atlas-pr-diff 265` returned composed diff metadata, artifact paths, PR body, changed-section count, and batch manifest.
- Command: `bun run src/index.ts read-atlas-pr-diff-batch 265 1` covered A.0/A.1/A.2/A.3 changes plus the first Grove Diamond PAU contract sections.
- Command: `bun run src/index.ts read-atlas-pr-diff-batch 265 2` covered Grove Diamond PAU facets, rate limits, role hierarchy, and Tokenized Treasury role hierarchy changes.
- Command: `bun run src/index.ts read-atlas-pr-diff-batch 265 3` covered Diamond PAU role/functions, JTRSY address/rate-limit updates, and most BUIDL instance configuration.
- Command: `bun run src/index.ts read-atlas-pr-diff-batch 265 4` covered the BUIDL Redeemer Role Holder section.

### Governance Authority and Economic Impact

**Status:** OK

- PR #265 changes `A.0.1.2.1` from Facilitators' broad discretionary capacity to Core Council's broad discretionary capacity, preserving Core Facilitator interpretive authority while moving Atlas supersession authority to Core Council through a public Forum post confirmed by Core GovOps and the Core Council Risk Advisor.
- PR #265 adds `A.2.3.1.5 - Allocation Modification`, allowing short-term Core Council reductions/restorations of Step 1 and Step 2 Capital and modifications of Step 3 Capital allocation, proceeding directly to Executive Vote without a prior Governance Poll.
- PR #265 authorizes Amatsu, Ozone, and Core Council Executor Agent 1 to transfer Genesis Capital Allocation funds to the Sky Frontier Foundation without a separate governance decision per transfer.
- PR #265 authorizes an 800,000 USDS July 2026 Grove Foundation grant and a 700,000 USDS July 2026 Skybase Foundation grant.
- These are material governance/economic changes but are disclosed in the poll and remain subject to later execution paths where funds or on-chain state change.

**Evidence**

- Command: `read-atlas-pr-diff-batch 265 1` showed changes to `A.0.1.2.1`, new `A.2.3.1.5`, transfer authorizations in `A.2.8.2.5.2.4`, `A.2.8.2.8.2.2`, and `A.2.8.2.9.2.2`, plus Grove and Skybase grant authorization sections.
- Command: `fetch-proposal 1638` disclosed these same items in the summary and full canonical text.

### Technical and Documentation Review

**Status:** OK

- Grove Diamond PAU documentation adds a modular Controller/facet architecture, contract addresses, roles, rate limits, and Controller functions for deposits, withdrawals, USDS mint/burn, and PSM swaps.
- BUIDL and JTRSY Tokenized Treasury Basin documentation includes contract addresses, role holders, interim deployment status, 5 million USDS combined maximum allocation, 5 million USDS/day inflow limits, and unlimited outflow limits.
- Agent Rate edits limit rewards to Prime Agent SubProxy balances except Spark PSM balances, avoid double counting, and clarify that Integration Boost or USDS Token Rewards balances do not also earn Agent Rate.
- Distribution Reward Code ranges, Core Council Risk Advisor data scope, AD repeat-breach timing, and Keel/Elodin edits are documentation/process clarifications.
- The poll does not itself execute the Grove PAU, Tokenized Treasury, grant, or transfer actions, so direct smart-contract execution risk belongs to later executive or agent spells.

**Evidence**

- Commands: `read-atlas-pr-diff-batch 265 1`, `265 2`, `265 3`, and `265 4` returned the Grove Diamond PAU and Tokenized Treasury Basin sections.
- Command: `read-atlas-pr-diff-batch 265 1` returned Agent Rate changes under `A.3.1.2.3`, Reward Code ranges under `A.2.2.9.1.2.1.1.4`, Risk Advisor data scope under `A.3.2.2.5.1.1.1.1`, AD repeat-breach timing under `A.1.6.2.1`, and Keel/Elodin edits under A.2 sections.

### On-Chain Baseline

**Status:** N/A

This poll authorizes an Atlas PR merge and does not itself execute on-chain actions. The PR documents many contract and multisig addresses and authorizes later grant/transfer/spell payloads, but those later transactions must be reviewed when they appear in an executive or agent spell. No live on-chain state claim was necessary to validate the poll's immediate action: merging PR #265 if the poll passes.

**Evidence**

- Command: `fetch-proposal 1638` states the action on passing is that the associated Pull Request will be merged into the Atlas.
- Command: `fetch-atlas-pr-diff 265` shows documentation changes only; no spell execution is part of this poll.

### Atlas Alignment

**Status:** OK

- The proposal uses the Atlas Edit Weekly Cycle process and the required MPP threshold.
- The edits are broad but transparent and mainly clarify authority, document agent infrastructure, authorize bounded grants/transfers, and update Atlas records.
- The largest alignment risk is governance concentration/flexibility: Core Council gains explicit supersession and Treasury Allocation modification authority. The proposal mitigates this by naming confirmation steps and retaining later Executive Vote execution for implementation.
- I did not find a Slippery Slope Misalignment concern strong enough to recommend NO, because the poll itself asks token holders to ratify these authorities through the recognized Atlas Edit path.

**Evidence**

- Command: `fetch-proposal 1638` returned the canonical proposal text and outcome conditions.
- Command: `fetch-atlas-pr-diff 265` and review batches 1-4 confirmed the PR contents.
- Commands: `read-atlas-section A.0.1.1.18`, `read-atlas-section A.1.11.2.1.3`, and `read-atlas-section A.1.11.2.4` resolved from active Atlas `2026-06-22`.

### AD Role Compliance

**Status:** OK

- Voting YES is consistent with active stewardship because the proposal's core mechanisms have been reviewed: process trigger, threshold, authority shifts, economic grants/transfers, Grove PAU/Basin documentation, Agent Rate clarification, and documentation cleanups.
- Abstention discipline is satisfied because there is no conflict of interest, missing core evidence, or specialized implementation ambiguity that prevents an accountable YES/NO view at the poll level.
- The recommendation can support a public AD vote explanation under `A.1.6.2.2` because it identifies the material governance discretion risk and explains why disclosure/process evidence still supports YES.
- Voting-estoppel confidence under `A.1.6.6.2` is met for the poll action: the analysis understands that approval merges PR #265 into the Atlas, while later executive/spell execution still requires separate review.

**Evidence**

- Commands: `read-atlas-section A.0.1.1.18`, `read-atlas-section A.1.6.2.1.1`, `read-atlas-section A.1.6.2.2`, and `read-atlas-section A.1.6.6.2` resolved from active Atlas `2026-06-22`.
- Commands: `fetch-proposal 1638`, `fetch-atlas-pr-diff 265`, and `read-atlas-pr-diff-batch 265 1-4` provide the substantive evidence needed for an AD explanation.

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote YES. The poll is procedurally framed as an Atlas Edit Weekly Cycle Proposal, has public trigger evidence from Bonapublica, uses the expected 480,000,000 SKY minimum positive participation threshold, and discloses the same twelve change groups across the portal summary, canonical proposal text, forum thread, PR body, and all four composed Atlas PR diff review batches. The proposal is not routine: it expands standing discretion and future direct-to-executive pathways for Core Council/Treasury Allocation and Executor Agent transfers, so risk is medium. But the changes are explicit, bounded by named actors and process steps, and remain subject to later Executive Vote execution where funds or contracts are moved. I found no material disclosure mismatch, unresolved implementation contradiction, or Atlas-process conflict that would justify NO or ABSTAIN.

## LLM Usage

- **Provider/Model:** openai / gpt-5.5
- **Tokens:** 3,243,466 in / 5,601 out / 555 reasoning / 3,249,622 total
- **Cache:** 3,196,544 read / 0 write
- **Cost:** $2.0176 USD estimated
- **Pricing:** openai-api-pricing-2026-06-10-standard-short-context
