# Analysis: Atlas Edit Weekly Cycle Proposal - June 15, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-15T19:23:47.490Z | **Atlas:** 2026-06-15

## Summary

Poll 1637 is an active Atlas Edit Weekly Cycle Proposal for PR #258. The proposal would merge Atlas edits covering Core Facilitator final Spell inclusion authority, Ethereum SkyLink Freezer Multisig documentation, Spark Foundation Q3 2026 grant authorization, Grove Prime allocator vault and buffer documentation, SKY oracle documentation, Grove Monad and Spark Base Aave address corrections, Discord-to-Slack coordination language, and a Technical Scope Template cross-reference.

## Atlas Alignment

**Assessment:** aligned

The disclosed Atlas edits are governance-process, documentation, or authorization changes that are facially consistent with Atlas stewardship and process maintenance. The original review found that PR #258 changes the Ethereum SkyLink Freezer Multisig text from a live 2/4 configuration to a present-tense 2/5 configuration while direct live checks still show the Safe at threshold 2 with 4 owners. That concern was resolved by forum post #4 from ldr, published 2026-06-15T18:32:57Z, stating: The updated configuration will be actioned if this edit is approved. With that clarification, the edit is reasonably understood as governance approval for a follow-up Safe signer update rather than an accidental current-state documentation mismatch.

**Relevant sections:** A.0.1.1.18, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.2, A.1.10.4.1.1, A.1.10.4.1.1.5, A.1.11.2.1.3, A.2.11.1.3.2.1.1.2.2

## Risk Assessment

**Level:** medium

- The PR affects 122 Atlas sections across governance process, Spark authorization, Grove allocator documentation, oracle documentation, and address corrections.
- The direct economic authorization for Spark Q3 2026 grants is material: 1,100,000 USDS per month to the Spark Foundation and 155,000 USDS per month to the Spark Asset Foundation for three months from Spark's Prime Treasury.
- The Ethereum SkyLink Freezer Multisig Safe remains 2/4 at review time, but the Core Facilitator clarified publicly that the updated 2/5 configuration will be actioned if the edit is approved.
- The proposal is not an executive spell and does not itself perform on-chain Safe owner changes.
- The remaining dependency is operational follow-through on the Safe signer update after approval.

## Finding Verification Pass

This analysis included active false-positive elimination before finalization. One or more initial FINDING checks were re-verified and downgraded after additional scrutiny.

- **Original findings:** 2
- **Remaining findings after verification:** 0

### Eliminated Or Downgraded Findings

#### Ethereum SkyLink Freezer Live Baseline

- **Original status:** FINDING
- **Final status:** OK

PR #258 changes A.1.10.4.1.1.2 from a 2/4 signing requirement to 2/5 and A.1.10.4.1.1.3 from two Core Facilitator plus two Core GovOps signers to two Core Facilitator plus three Core GovOps signers. It also rewrites A.1.10.4.1.1.5 to permit five signers and label 2/5 as a Threshold Exception. Direct live checks show the Safe at 0x38d1114b4cE3e079CC0f627df6aC2776B5887776 still has threshold 2 and four owners at review time, but forum post #4 by ldr, published 2026-06-15T18:32:57Z, states: The updated configuration will be actioned if this edit is approved. This resolves the earlier concern that the edit was an unexplained current-state documentation mismatch.

#### Technical Soundness

- **Original status:** FINDING
- **Final status:** OK

The technical documentation edits are coherent: PIP_SKY and src were verified, Base Aave token/underlying fields are corrected in the Atlas diff, and the Monad instance is moved into Monad directories with Monad-specific USDC and broker address documentation. The SkyLink Freezer Safe remains 2/4 at review time, but forum post #4 by ldr clarifies that the updated configuration will be actioned if the edit is approved.

## Validation Checks

### Proposal Fetched

**Status:** OK

fetch-proposal 1637 returned an active single-choice poll titled Atlas Edit Weekly Cycle Proposal - June 15, 2026. The vote window is 2026-06-15T16:00:00.000Z to 2026-06-18T16:00:00.000Z, options are Abstain/Yes/No, and the outcome threshold is Yes plurality plus at least 480,000,000 SKY Minimum Positive Participation.

**Evidence**

- bun run src/index.ts fetch-proposal 1637
- Portal URL: https://vote.sky.money/polling/QmdYpnYS
- Proposal source URL: https://raw.githubusercontent.com/sky-ecosystem/polls/refs/heads/main/2026/2026-06-15-Atlas-edit-weekly-cycle-proposal.md
- Discussion URL: https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-15/27965

### Atlas Version

**Status:** OK

sync-atlas completed before proposal review and activated Atlas version 2026-06-15.

**Evidence**

- bun run src/index.ts sync-atlas
- Returned details.atlasVersion: 2026-06-15

### Governance Process Provenance

**Status:** OK

The proposal is an Atlas Edit Weekly Cycle Proposal. The canonical text says Core Facilitators placed it on behalf of Ranked Delegate cloaky. Forum post #2 by cloaky, published 2026-06-13T17:05:11Z, states: I am hereby triggering this. Atlas A.1.6.4.1.1.3.1 identifies Cloaky as a current Level 1 Ranked Delegate, and A.1.11.2.1.3 requires a Ranked Delegate forum reply to trigger a Weekly Cycle Proposal.

**Evidence**

- bun run src/index.ts fetch-proposal 1637
- curl -s https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-15/27965/2
- bun run src/index.ts read-atlas-section A.1.6.4.1.1.3.1
- bun run src/index.ts read-atlas-section A.1.11.2.1.3
- bun run src/index.ts read-atlas-section A.1.6.4.4.2.1.1

### Portal Summary vs Canonical Text

**Status:** OK

The portal summary and canonical proposal text disclose the same nine top-line edit categories: Core Facilitator final Spell inclusion authority, SkyLink Freezer 2/4 to 2/5 configuration, Spark Q3 grants, Grove Prime second allocator vault and buffer, SKY Price Oracle documentation, Grove Monad Uniswap correction, Spark Base Aave address fix, Discord-to-Slack migration, and Technical Scope Template cross-reference.

**Evidence**

- bun run src/index.ts fetch-proposal 1637
- Canonical proposal text lists PR #258 and the same nine summarized edits.

### Atlas PR Diff Coverage

**Status:** OK

fetch-atlas-pr-diff 258 returned COMPOSED_DIFF_READY for PR #258 with base SHA f114a09955f639e3f61e298e42ec6e413df51e69, head SHA 957222b32b4cd923d2eef4ea6f272e995c614c91, unified diff SHA-256 4b61e6722c93d05e0b802494d0d4afb3e755375b7fe1698b48ab64b5ea1a95d9, 122 changed sections, and 2 review batches. Both read-atlas-pr-diff-batch 258 1 and 258 2 were reviewed.

**Evidence**

- bun run src/index.ts fetch-atlas-pr-diff 258
- bun run src/index.ts read-atlas-pr-diff-batch 258 1
- bun run src/index.ts read-atlas-pr-diff-batch 258 2
- Manifest artifact: data/cache/atlas-pr-diffs/258/f114a09955f639e3f61e298e42ec6e413df51e69-957222b32b4cd923d2eef4ea6f272e995c614c91/summary.json

### Canonical Text vs Atlas PR Diff

**Status:** OK

The composed diff implements the nine disclosed edit categories and did not show an additional independent policy change outside the disclosed scope. The changed sections include A.1.10 spell-process Slack and final-inclusion edits, A.1.10.4.1.1 SkyLink Freezer text, A.2.8.2.2.2.4.5.1.4 Spark Q3 grant authorization, A.3.7.1.2.1.3 and A.3.7.1.3.3.4 Grove allocator parameters, A.4.4.1.3.9.1 and A.4.4.1.3.9.1.1 SKY oracle documentation, and A.6.1.1.* Grove/Spark address and instance-location corrections.

**Evidence**

- bun run src/index.ts read-atlas-pr-diff-batch 258 1
- bun run src/index.ts read-atlas-pr-diff-batch 258 2
- Changed section count: 122
- Review batch hashes: 737ca3aa0aba4ef5c00e77deb355857e2b30c3c7af2b8512d983df4bad50acc0 and b5c505000d57a8f604d8c3074f5fb4017f7a87aa7bb8f01c58a3bba6f9c02743

### SKY Oracle Baseline

**Status:** OK

The SKY Price Oracle documentation added in PR #258 matches supported mainnet checks: ChainLog key PIP_SKY resolves to 0x511485bBd96e7e3a056a8D1b84C5071071C52D6F, and OSM src() at that address returns 0xc2ffbbDCCF1466Eb8968a846179191cb881eCdff.

**Evidence**

- bun run src/index.ts read-chainlog PIP_SKY
- bun run src/index.ts call-verified-contract 0x511485bBd96e7e3a056a8D1b84C5071071C52D6F src
- read-chainlog returned Address: 0x511485bBd96e7e3a056a8D1b84C5071071C52D6F
- call-verified-contract returned 0xc2ffbbDCCF1466Eb8968a846179191cb881eCdff

### Ethereum SkyLink Freezer Live Baseline

**Status:** OK

PR #258 changes A.1.10.4.1.1.2 from a 2/4 signing requirement to 2/5 and A.1.10.4.1.1.3 from two Core Facilitator plus two Core GovOps signers to two Core Facilitator plus three Core GovOps signers. It also rewrites A.1.10.4.1.1.5 to permit five signers and label 2/5 as a Threshold Exception. Direct live checks show the Safe at 0x38d1114b4cE3e079CC0f627df6aC2776B5887776 still has threshold 2 and four owners at review time, but forum post #4 by ldr, published 2026-06-15T18:32:57Z, states: The updated configuration will be actioned if this edit is approved. This resolves the earlier concern that the edit was an unexplained current-state documentation mismatch.

**Evidence**

- bun run src/index.ts read-atlas-section A.1.10.4.1.1
- bun run src/index.ts read-atlas-section A.1.10.4.1.1.5
- bun run src/index.ts read-atlas-pr-diff-batch 258 1
- curl -s -L https://safe-transaction-mainnet.safe.global/api/v1/safes/0x38d1114b4cE3e079CC0f627df6aC2776B5887776/
- cast call 0x38d1114b4cE3e079CC0f627df6aC2776B5887776 getThreshold()(uint256)
- cast call 0x38d1114b4cE3e079CC0f627df6aC2776B5887776 getOwners()(address[])
- curl -s https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-15/27965
- curl -s https://api.github.com/repos/sky-ecosystem/next-gen-atlas/pulls/258
- curl -s https://api.github.com/repos/sky-ecosystem/next-gen-atlas/issues/258/comments
- curl -s https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-15/27965/4
- Safe API and direct cast both confirm threshold 2 with four owners: 0xA4A4B73c38a19c3D6DA8EC4b6Be0F60580CD08d5, 0xf2ffaf948f1e184ebEd8d6F5DCEDF35Bcb85eC6D, 0xe62Ca0fcA6EC4227a40108A558988Fc24044357B, 0x188c52aDa9a984F461746B4dBa4805f6b9b3a9e1
- Forum post #4 by ldr states: The updated configuration will be actioned if this edit is approved.

### Economic Impact

**Status:** OK

The main disclosed economic authorization is Spark Q3 2026 grant funding from Spark's Prime Treasury: 1,100,000 USDS per month to the Spark Foundation and 155,000 USDS per month to the Spark Asset Foundation for three months. The Grove allocator additions document ALLOCATOR-GROVE-A parameters with duty set by SP-BEAM, line controlled by DC-IAM, DC-IAM gap/line/ttl deferred to an upcoming spell, and SP-BEAM max/min/step/tau values. These items are disclosed in the canonical proposal and PR body.

**Evidence**

- bun run src/index.ts fetch-proposal 1637
- bun run src/index.ts read-atlas-pr-diff-batch 258 1
- Spark grant section: A.2.8.2.2.2.4.5.1.4
- Grove allocator sections: A.3.7.1.2.1.3 and A.3.7.1.3.3.4

### Technical Soundness

**Status:** OK

The technical documentation edits are coherent: PIP_SKY and src were verified, Base Aave token/underlying fields are corrected in the Atlas diff, and the Monad instance is moved into Monad directories with Monad-specific USDC and broker address documentation. The SkyLink Freezer Safe remains 2/4 at review time, but forum post #4 by ldr clarifies that the updated configuration will be actioned if the edit is approved.

**Evidence**

- bun run src/index.ts read-chainlog PIP_SKY
- bun run src/index.ts call-verified-contract 0x511485bBd96e7e3a056a8D1b84C5071071C52D6F src
- bun run src/index.ts read-atlas-pr-diff-batch 258 1
- bun run src/index.ts read-atlas-pr-diff-batch 258 2
- cast call getThreshold returned 2; cast call getOwners returned four owner addresses for the SkyLink Freezer Safe
- Forum topic and PR body describe the change as updating from 2/4 to 2/5; PR comments were empty.
- Forum post #4 by ldr states: The updated configuration will be actioned if this edit is approved.

### AD Role Compliance

**Status:** OK

A.0.1.1.18 requires ADs to uphold the Spirit of the Atlas and maintain Universal Alignment. A.1.6.2.2 requires a substantive vote explanation, and A.1.6.6.2 creates voting-estoppel risk for votes in favor. After the forum clarification that the SkyLink Freezer updated configuration will be actioned if the edit is approved, the recommendation has enough public evidence for an accountable YES vote explanation.

**Evidence**

- bun run src/index.ts read-atlas-section A.0.1.1.18
- bun run src/index.ts read-atlas-section A.1.6.2.1.1
- bun run src/index.ts read-atlas-section A.1.6.2.2
- bun run src/index.ts read-atlas-section A.1.6.6.2

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote YES. The proposal is procedurally valid, the portal/canonical text and PR diff disclose the material edit categories, and the reviewed diff matches the stated scope. The earlier SkyLink Freezer concern has been clarified publicly: ldr stated that the updated configuration will be actioned if the edit is approved. That makes the 2/5 Threshold Exception language an approval for a follow-up Safe configuration update rather than an unexplained mismatch with the current 2/4 Safe state. The remaining items are disclosed governance-process, grant-authorization, allocator-documentation, oracle-documentation, and address-correction edits, with no surviving finding that would justify voting No or Abstain.

## LLM Usage

- **Provider/Model:** openai / gpt-5.5
- **Tokens:** 6,419,903 in / 29,143 out / 5,808 reasoning / 6,454,854 total
- **Cache:** 5,924,480 read / 0 write
- **Cost:** $6.4879 USD estimated
- **Pricing:** openai-api-pricing-2026-06-10-standard-short-context
