# Analysis: Atlas Edit Weekly Cycle Proposal - June 8, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-08T19:49:31.992Z | **Atlas:** 2026-06-08

## Summary

Poll 1636 asks Sky Governance to approve Atlas PR #255, an Atlas Edit Weekly Cycle proposal that adds a new audit process for smart contract code and deployment scripts, authorizes Grove to swap USD stablecoins in its SubProxy Account into USDS at approximately 1:1 with public Technical Scope documentation, updates Atlas wording for a single Core Facilitator, and performs housekeeping edits for duplicate text and a broken cross-reference.

## Atlas Alignment

**Assessment:** aligned

The proposal uses the Atlas Edit Weekly Cycle process and stays within the kinds of Atlas amendments allowed during the transition to Endgame. The audit-process edits strengthen implementation safety and disclosure for smart contract code before Spell inclusion. The Grove swap authorization creates a standing permission, but it is constrained to Grove SubProxy-held USD stablecoins, a maximum 0.1% price divergence from 1:1, and public Technical Scope documentation before direct Grove Spell inclusion. The single-Core-Facilitator edits are consistency updates that preserve public escalation when the Core Facilitator is malicious or compromised. These changes are consistent with Aligned Delegate stewardship obligations to support Atlas-aligned process clarity and risk controls.

**Relevant sections:** A.0.1.1.18, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.2, A.1.11.2.1.1, A.1.11.2.1.3, A.1.6.4.1.2.3.1, A.1.6.4.4.2.1.1, A.6.1.1.2.2.1.1.3.1.1.2, A.1.10.2.3.2.2.3.2.2

## Risk Assessment

**Level:** medium

- The proposal includes a new standing authorization for Grove to swap USD stablecoins into USDS without a separate prior token-holder vote for each qualifying swap.
- The Grove authorization is bounded by source of funds, approximately 1:1 execution with divergence not to exceed 0.1%, and public Technical Scope documentation in the Grove Prime forum category.
- The audit process reduces execution risk for new smart contract code, deployment scripts, and initialization scripts by requiring audit intake, review, remediation, acceptance, and recordkeeping before deployment or Spell inclusion.
- The single-Core-Facilitator edits reduce outdated plural wording but retain a public reporting path if the Core Facilitator is malicious or compromised.
- Housekeeping edits remove duplicate sentences and fix a broken reference without creating independent policy risk.

## Validation Checks

### Proposal Fetched

**Status:** OK

- `fetch-proposal 1636` returned active poll metadata for `Atlas Edit Weekly Cycle Proposal - June 8, 2026`.
- Vote window: starts `2026-06-08T16:00:00.000Z`, ends `2026-06-11T16:00:00.000Z`.
- Options: `0=Abstain`, `1=Yes`, `2=No`; portal URL `https://vote.sky.money/polling/Qme7Pt6e`.
- Canonical proposal URL is the raw polls repository markdown for `2026-06-08-Atlas-edit-weekly-cycle-proposal.md`.
- The canonical proposal states the outcome: if Yes exceeds No and reaches at least `480,000,000 SKY`, Atlas PR #255 will be merged.

**Evidence**

- bun run src/index.ts fetch-proposal 1636
- Poll status active; voteType single-choice; startDate 1780934400; endDate 1781193600.
- Proposal Source URL: https://raw.githubusercontent.com/sky-ecosystem/polls/refs/heads/main/2026/2026-06-08-Atlas-edit-weekly-cycle-proposal.md

### Portal Summary vs Canonical Text

**Status:** OK

- The portal summary and canonical proposal both disclose the same four edit groups: add Audit Process; add Grove USD stablecoin-to-USDS swap authorization; update documents for a single Core Facilitator; remove duplicate sentences and fix a broken cross-reference.
- The canonical text expands each item with voter-relevant details: the Grove swap authorization is approximately 1:1, requires Technical Scope documentation, and can be included directly in a Grove Spell without a prior token-holder vote.
- No material economic, governance, authorization, or scope change found in the canonical text that is omitted from the portal summary at the policy level.

**Evidence**

- bun run src/index.ts fetch-proposal 1636
- Portal summary: `This Atlas edit proposal 1) adds Audit Process, 2) adds USD Stablecoin to USDS swap authorization for Grove, 3) updates documents to reflect a single Core Facilitator, 4) removes duplicate sentences and fixes a broken cross-reference.`
- Canonical Review section lists the same four emphasized bullets and links Atlas PR #255.

### Weekly Cycle Trigger and Process

**Status:** OK

- `read-atlas-section A.1.11.2.1` confirms weekly proposals may include multiple amendments and must remain within the Spirit of the Atlas and Universal Alignment.
- `read-atlas-section A.1.11.2.1.3` requires a Ranked Delegate trigger post and Core Facilitator confirmation that the Triggering Threshold is met.
- Forum topic `27951.json` shows post #2 by `Bonapublica` at `2026-06-06T21:10:30.216Z` expressly triggering the weekly proposal for PR #255 under `A.1.11.2.1.3`.
- `read-atlas-section A.1.6.4.1` identifies Bonapublica as the current Level 2 Ranked Delegate; `A.1.6.4.4.2.1.1` defines the Triggering Threshold as one month of Level 3 Ranked Delegate compensation.
- The Atlas assigns buffer confirmation to the Core Facilitator; the poll text states the Core Facilitators placed the proposal into the voting system on behalf of Ranked Delegate Bonapublica.

**Evidence**

- bun run src/index.ts read-atlas-section A.1.11.2.1
- bun run src/index.ts read-atlas-section A.1.11.2.1.3
- curl -L https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-08/27951.json
- Forum post #2 username Bonapublica; created_at 2026-06-06T21:10:30.216Z; text begins `bonapublica_AD hereby triggers the Atlas_Edit_Weekly_Proposal for the week of 2026-06-08`.
- bun run src/index.ts read-atlas-section A.1.6.4.1
- A.1.6.4.1.2.3.1: current Level 2 Ranked Delegate is Bonapublica.

### Atlas PR Diff Coverage

**Status:** OK

- `fetch-atlas-pr-diff 255` returned PR #255 metadata and a direct unified diff, so no composed fallback or batch review was required.
- PR state: open, not merged; author `adamgfraser`; created `2026-06-05T21:58:34Z`; files changed `36`; additions `294`; deletions `37`.
- The diff was reviewed across all changed-policy groups: A.1.10.2 audit-process additions and references; A.6.1.1.2.2.6.1.2.1.2.3 Grove swap authorization; single-Core-Facilitator edits in A.1.10.2.4.12.4.5/.6/.7 and A.1.12.2.1.7.1; retired A.1.11.2.3.0.4.1; duplicate sentence removals in A.2.2.9.2.2.3.5.4.2 and A.6.1.1.1.2.5.2.2.1.3.4; and reference repair in A.6.1.1.6.2.
- The PR body, canonical poll text, and forum author post describe the same four material edit categories as the actual diff.

**Evidence**

- bun run src/index.ts fetch-atlas-pr-diff 255
- Diff headers reviewed for changed files under content/A/1/10/2, content/A/1/11, content/A/1/12, content/A/2/2/9, and content/A/6/1/1.
- PR body lists: Add Audit Process; Add USD Stablecoin To USDS Swap Authorization For Grove; Update Documents To Reflect A Single Core Facilitator; Remove Duplicate Sentences And Fix Broken Cross-Reference.

### Audit Process Review

**Status:** OK

- PR #255 adds new section `A.1.10.2.7 - Audit Process` and child sections `A.1.10.2.7.1` through `A.1.10.2.7.6`.
- The new rules require audits before new smart contract code is introduced, including smart contracts, module onboardings, and deployment/initialization scripts.
- The process covers deployment and initialization script structure, no hardcoded addresses, test coverage expectations, deployment ownership handoff, audit request/intake with repository and exact commit hash, auditor report delivery, report acceptance before deployment/Spell/governance vote, remediation of findings, and public audit recordkeeping.
- Existing process documents are updated to point to `A.1.10.2.7`, including module deployment preparation, interim deployments, Prime Spell forms, and novel Spell item technical feasibility work.
- This is an implementation-safety strengthening, not a weakening of review controls.

**Evidence**

- bun run src/index.ts fetch-atlas-pr-diff 255
- Added A.1.10.2.7.1: audit required before new smart contract code is introduced.
- Added A.1.10.2.7.4: audited artifact must not proceed to deployment, Spell inclusion, or governance vote until accepted.
- Added A.1.10.2.7.5: medium-or-higher findings must be fixed and re-audited before proceeding.
- Added A.1.10.2.7.6: associated Forum post or Technical Scope must include final audit report links, audited commit hash, and deployed-code match confirmation.

### Grove Swap Authorization Review

**Status:** OK

- PR #255 adds `A.6.1.1.2.2.6.1.2.1.2.3 - USD Stablecoin To USDS Swap Authorization`.
- The authorization is limited to USD stablecoins held in Grove's SubProxy Account and swaps to USDS.
- `read-atlas-section A.6.1.1.2.2.1.1.3.1.1.2` identifies Grove's SubProxy Account as `0x1369f7b2b38c76B6478c0f0E66D94923421891Ba`.
- The added section requires approximately 1:1 execution with divergence not to exceed `0.1%` and each swap to be documented in a Grove Prime Forum post containing the Technical Scope.
- `read-atlas-section A.1.10.2.3.2.2.3.2.2` confirms Technical Scope forum posts must contain the Technical Scope, Financial Risk Assessment, and, if relevant, Technical Risk Assessment.
- The direct-inclusion-in-Grove-Spell permission is material, but the constraints and public documentation requirement make the authorization reviewable and bounded.

**Evidence**

- bun run src/index.ts fetch-atlas-pr-diff 255
- bun run src/index.ts read-atlas-section A.6.1.1.2.2.1.1.3.1.1.2
- bun run src/index.ts read-atlas-section A.1.10.2.3.2.2.3.2.2
- Added A.6.1.1.2.2.6.1.2.1.2.3 text: swaps must be approximately 1:1 with divergence not to exceed 0.1%; documented in Grove Prime forum Technical Scope; eligible for direct Grove Spell inclusion with no prior token-holder vote.

### Single Core Facilitator and Housekeeping Review

**Status:** OK

- The single-Core-Facilitator edits update outdated plural wording without removing public escalation when the Core Facilitator may be malicious or compromised.
- A.1.10.2.4.12.4.5 changes reporting issues to `the Core Facilitator`; A.1.10.2.4.12.4.6 preserves public reporting to Sky Governance if the Core Facilitator is malicious or compromised; A.1.10.2.4.12.4.7 generalizes private reporting to `multiple trusted parties` instead of a group of Core Facilitators.
- A.1.11.2.3.0.4.1 is retired because unanimity among multiple Core Facilitators is no longer applicable.
- A.1.12.2.1.7.1 removes plural/unanimity wording and keeps the Core Facilitator block-for-misalignment procedure.
- Duplicate sentence removals in A.2.2.9.2.2.3.5.4.2 and A.6.1.1.1.2.5.2.2.1.3.4 are non-substantive.
- A.6.1.1.6.2 fixes a broken reference from `cde2604...` to `fcde2604-a138-4c1b-9d9a-14895835c907` for `A.2.2 - Sky Primitives`.

**Evidence**

- bun run src/index.ts fetch-atlas-pr-diff 255
- Diff shows A.1.10.2.4.12.4.6 updated to: if a validator suspects the Core Facilitator is malicious or compromised, they must notify Sky Governance publicly.
- Diff deletes A.1.11.2.3.0.4.1 `Unanimity Is Not Required To Block Proposal For Misalignment`.
- Forum trigger post #2 UUID accounting states minted 15, retired 1, net +14, duplicate UUIDs within HEAD 0, relocations 0, re-creations 0.

### Technical Soundness

**Status:** OK

- This is an Atlas-text PR, not an executable spell or direct on-chain parameter update, so spell integrity and on-chain storage checks are not required for the poll itself.
- The material technical content was reviewed through the PR diff and relevant Atlas sections.
- The new audit process adds technical controls for future code introductions; the Grove authorization constrains future spell actions by source account, swap type, price divergence, and documentation requirements.
- No proxy spell, contract address migration, rate change, cap change, allowlist change, or live storage baseline claim was made by the poll.

**Evidence**

- bun run src/index.ts fetch-proposal 1636
- bun run src/index.ts fetch-atlas-pr-diff 255
- No executable spell address in poll text; outcome is merge of Atlas PR #255.

### Atlas Alignment

**Status:** OK

- `A.1.11.2.1.1` allows multiple amendments in a single Weekly Cycle Proposal and requires Atlas Edits to adhere to the Spirit of the Atlas and Universal Alignment.
- The audit-process edit strengthens governance-controlled technical safety and transparency before code deployment or Spell inclusion.
- The Grove authorization supports operational efficiency for converting Grove-held USD stablecoins into USDS, while bounding execution price and documentation.
- The Core Facilitator wording updates align the Atlas with the current single-Core-Facilitator operating model while retaining safety reporting paths.
- The proposal does not show Slippery Slope Misalignment on the reviewed evidence because the only future-action authorization is constrained and publicly documented.

**Evidence**

- bun run src/index.ts read-atlas-section A.1.11.2.1
- bun run src/index.ts read-atlas-section A.0.1.1.18
- bun run src/index.ts fetch-atlas-pr-diff 255

### AD Role Compliance

**Status:** OK

- `A.0.1.1.18` states ADs must use delegated power to uphold the Spirit of the Atlas and maintain Universal Alignment.
- `A.1.6.2.1.1` treats abstention as exceptional; the evidence is sufficient for an accountable yes/no vote, so abstention is not needed.
- `A.1.6.2.2` requires a substantive explanation demonstrating understanding, a reasoned basis, and at least one substantive aspect; the recommendation addresses the audit-process benefit, Grove authorization risk and constraints, implementation/documentation requirements, and Atlas alignment.
- `A.1.6.6.2` estops a YES voter from later claiming non-understanding. The reviewed evidence covers the key governance implications: PR #255 scope, process trigger, audit controls, Grove direct-spell authorization, single-Core-Facilitator cleanup, and housekeeping edits.
- A YES recommendation is therefore consistent with active stewardship and voting-estoppel confidence.

**Evidence**

- bun run src/index.ts read-atlas-section A.0.1.1.18
- bun run src/index.ts read-atlas-section A.1.6
- bun run src/index.ts fetch-proposal 1636
- bun run src/index.ts fetch-atlas-pr-diff 255

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote YES. PR #255 is disclosed consistently in the portal, canonical poll text, forum thread, and PR body, and the reviewed diff matches the four stated edit groups. The new audit process is a substantive safety improvement for code entering the Sky Ecosystem. The Grove swap authorization is a real delegation of future execution authority, but the permission is narrow, value-preserving, and requires public Technical Scope documentation before Grove Spell inclusion. The remaining edits are process-consistency and housekeeping changes. On the reviewed evidence, the proposal is Atlas-aligned and sufficiently bounded for an accountable AD YES vote.
