# Analysis: Onboard ALLOCATOR-GROVE-A Vault, Update LitePSM Parameters, Replace STUSDS_MOM, Monthly Settlement Cycle for May 2026, Staking Rewards Normalization, Update Safe Harbor Agreement, Prime Agent Proxy Spell - June 18, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-19T18:19:53.424Z | **Atlas:** 2026-06-19

## Summary

This executive onboards ALLOCATOR-GROVE-A, increases LitePSM `buf` and AutoLine `gap` to 800 million, replaces STUSDS_MOM, executes May 2026 Monthly Settlement Cycle transfers, normalizes LSSKY-to-SKY reward vesting, updates Safe Harbor coverage, and whitelists a Spark Prime Agent proxy spell in Spark StarGuard. The core spell source maps to the disclosed actions, the proxy spell source was reviewed, the previously failed forge tests passed individually, and the Core Facilitator-waived Spark Agent checklist gap no longer remains a validation finding.

## Atlas Alignment

**Assessment:** aligned

The disclosed actions are within recognizable Atlas authorities and the implementation evidence has been reviewed: A.2.4 authorizes Monthly Settlement Cycle settlement through Executive Votes; A.4.4.1.2 and A.4.4.1.4.2 authorize SKY staking reward distribution and parameter modification through Executive Votes; A.2.11.1.2.3 requires Safe Harbor maintenance when new contracts are added; A.6.1.1.1.2.6.1.2.1.2.3 authorizes Spark reserve claims and transfers; and A.1.10.2.2.5 describes Prime Agent spell items moving through the Executive Process. The remaining checklist concern was resolved by public clarification that the missing registered Spark checklist is waived for this one June 18 spell as a transitionary measure.

**Relevant sections:** A.0.1.1.18, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.2, A.1.10.2.2.5, A.2.4, A.2.11.1.2.3, A.4.4.1.2, A.4.4.1.4.2, A.6.1.1.1.2.6.1.2.1.2.3

## Risk Assessment

**Level:** medium

- The executive is broad and touches allocator onboarding, LitePSM liquidity parameters, settlement transfers, reward vesting, Safe Harbor registry updates, and a Spark proxy spell.
- Core spell integrity and source/archive comparison passed. The full forge run was interrupted by RPC 429 errors, but each of the nine previously failed tests passed when rerun individually.
- The Spark Agent spell review evidence is substantive but not detected as canonical Agent Spell Reviewer Checklist evidence for a June 18, 2026 Agent spell; however, Lex clarified publicly that this was an internal communication oversight and that the checklist requirement is waived for this one Spark spell in consultation with the Core Facilitator.
- The executive remains broad and proxy-spell dependent, so risk remains medium even though all validation checks now pass.

## Finding Verification Pass

This analysis included active false-positive elimination before finalization. One or more initial FINDING checks were re-verified and downgraded after additional scrutiny.

- **Original findings:** 2
- **Remaining findings after verification:** 0

### Eliminated Or Downgraded Findings

#### Spell Checklist and Reviewer Signoff

- **Original status:** FINDING
- **Final status:** OK

- Sky Core PR #553 had 21 review events, 5 unique reviewers, 2 latest formal approvals, no latest changes requested, CI checks succeeded, and explicit `Good to deploy` and `Good to handover` comments from `SidestreamIcedMango`; `amusingaxl` also posted approval/handover evidence.
- Spark PR #169 had 22 review events, 6 unique reviewers, 2 latest formal approvals, and no latest changes requested. It included substantive Agent spell review evidence from `deluca-mike` and `TheMj0ln1r`, plus a formal approval from `certora-spark-review` confirming deployment address `0xe08BD6D9016EAC522903FC68c80F809664C2692A`.
- `fetch-pr-reviews 169 --repo sparkdotfi/spark-spells` reported `Agent Checklist Status: substantive_unclear`, `Canonical Agent Checklist Evidence: no`, and `Agent Checklist Evidence: no`; this initially blocked automatic YES validation because the June 18, 2026 executive is when the registered Agent checklist requirement came into force.
- Public clarification by Lex on June 19, 2026 states that the Spark June 18 review evidence was substantive, the missing registered checklist was an internal communication oversight, and the checklist requirement is waived for this one Spark spell in consultation with the Core Facilitator. The requirement applies to Spark and all Agents going forward, starting with the July 2, 2026 spell.

#### Forge Test Evidence

- **Original status:** FINDING
- **Final status:** OK

- `run-forge-tests 032e61aa74308f830f59d44f0a6dfb24deec3eca --pr 553` compiled successfully but the full run exited code `2` with 20 passed, 9 failed, and 26 skipped because fork/RPC reads hit Infura HTTP 429 `Too Many Requests`.
- The nine failed tests were rerun individually at exact merge commit `032e61aa74308f830f59d44f0a6dfb24deec3eca`, with `ETH_RPC_URL` mapped from `ETHEREUM_RPC_URL` and `FOUNDRY_THREADS=1`.
- Individual rerun results all passed: `testStarknet` passed 2/0/0 in `164.19s`; `testChainlogIntegrity` passed 1/0/0 in `344.58s`; `testChainlogValues` passed 1/0/0 in `348.54s`; `testGeneral` passed 1/0/0 in `365.88s`; `testPSMs` passed 1/0/0 in `190.79s`; `testPayments` passed 1/0/0 in `159.07s`; `testPrimeAgentSpellExecutions` passed 1/0/0 in `280.89s`; `testSplitter` passed 1/0/0 in `165.37s`; and `testSystemTokens` passed 1/0/0 in `163.91s`.
- This eliminates the prior forge-test evidence gap as a surviving validation finding.

## Validation Checks

### Executive Fetched and Action Enumeration

**Status:** OK

- `fetch-executive 0xC136C3` returned address `0xC136C3c419746c2e8c0B95100ac866a747e3e04b`, date `2026-06-18T00:00:00.000Z`, office hours true, not scheduled, not cast, and SKY support `1567983981.494724750866506436`.
- The canonical document enumerates ALLOCATOR-GROVE-A onboarding, LitePSM `buf`/`gap` increases, STUSDS_MOM replacement, May 2026 MSC settlement, LSSKY-to-SKY reward normalization, Safe Harbor update, and Spark proxy spell whitelisting.

**Evidence**

- fetch-executive 0xC136C3 returned proposal link https://raw.githubusercontent.com/sky-ecosystem/executive-votes/main/2026/executive-vote-2026-06-18-onboard-allocator-grove-a-update-stusds-mom.md
- Executive spell address `0xC136C3c419746c2e8c0B95100ac866a747e3e04b`; executive hash `0xf5380dae78ce04cd57b4ac9be4b0b5dc4b0413dbd138f02bd0dbfc07800ed5d9`.

### Portal Summary vs Canonical Executive Text

**Status:** OK

The vote portal/API summary is shorter but materially consistent with the canonical executive text. It discloses the allocator onboarding, LitePSM parameter increases, STUSDS_MOM update, MSC execution, reward normalization, Safe Harbor update, and Spark proxy spell whitelisting.

**Evidence**

- fetch-executive summary: `Onboard a new ALLOCATOR-GROVE-A vault, increase LitePSM buf and gap parameters, replace the existing STUSDS_MOM with a new version, execute the Monthly Settlement Cycle for May 2026, normalize LSSKY-SKY staking rewards after MSC execution, update the Safe Harbor Agreement with new contracts, whitelist a proxy spell for Spark.`

### Spell Integrity and Executive Document Hash

**Status:** OK

- `check-spell-integrity` returned `action()` `0x240b327125633219B53Dafa7E416e0B18Fc43F34`.
- `tag()` and `extcodehash(action)` both equal `0x069afd263f9ad0453ff3eaae2fe64b8bfe5a8be21ec3dcf23a136c6f830081e0`.
- `sig()` is `0x61461954`, `eta()` is `0`, `done()` is `false`, office hours are true, and expiration is `2026-07-18T11:38:47.000Z`.
- `keccak256-url` on the pinned raw GitHub URL returned `0xf5380dae78ce04cd57b4ac9be4b0b5dc4b0413dbd138f02bd0dbfc07800ed5d9`, matching the spell `description()` hash.

**Evidence**

- check-spell-integrity 0xC136C3c419746c2e8c0B95100ac866a747e3e04b
- keccak256-url https://raw.githubusercontent.com/sky-ecosystem/executive-votes/144cb5e786f0fb860c13f14d98fe19794e190011/2026/executive-vote-2026-06-18-onboard-allocator-grove-a-update-stusds-mom.md returned content length 14663 and matching hash.

### Verified Source and Source Archive Diff

**Status:** OK

- `fetch-spell-source` verified the Ethereum spell source as contract `DssSpell`, compiler `v0.8.16+commit.07a7930e`, optimizer enabled with 200 runs, proxy false, and linked `DssExecLib` `0x8de6ddbcd5053d32292aaa0d2105a32d108484a6`.
- `flatten-spell 032e61aa... --pr 553` compared Etherscan source to `src/DssSpell.sol` at merge commit `032e61aa74308f830f59d44f0a6dfb24deec3eca`: both were 328436 chars and 7095 lines, and sources were identical.
- `fetch-contract-creation` reported the core spell was deployed by EOA `0xb9240679ffdc72d3c2f409be34d30ce361770fc8` through standard CREATE.

**Evidence**

- fetch-spell-source 0xC136C3c419746c2e8c0B95100ac866a747e3e04b --chain-id 1
- flatten-spell 032e61aa74308f830f59d44f0a6dfb24deec3eca 0xC136C3c419746c2e8c0B95100ac866a747e3e04b --pr 553
- fetch-contract-creation 0xC136C3c419746c2e8c0B95100ac866a747e3e04b --chain-id 1

### Action-to-Code Mapping

**Status:** OK

- The reviewed `DssSpellAction.actions()` source implements the disclosed ALLOCATOR-GROVE-A setup, chainlog removal, LINE_MOM and SPBEAM updates, LitePSM `buf` and AutoLine changes, STUSDS_MOM replacement, MSC `_takeAllocatorPayment` and `_transferUsds` amounts, `TreasuryFundedFarmingInit.updateFarmVest` with `240_862_942 * WAD` and `90 days`, Safe Harbor calldata updates, and `StarGuardLike(SPARK_STARGUARD).plot(SPARK_SPELL, SPARK_SPELL_HASH)`.
- The live `buf()` call on `MCD_LITE_PSM_USDC_A` returned `400000000000000000000000000`, matching the disclosed 400 million baseline before the spell sets 800 million.
- ChainLog reads returned key addresses used in the spell, including `MCD_LITE_PSM_USDC_A` `0xf6e72Db5454dd049d0788e411b06CfAF16853042`, `MCD_IAM_AUTO_LINE` `0xC7Bdd1F2B16447dcf3dE045C4a039A60EC2f0ba3`, `MCD_PAUSE_PROXY` `0xBE8E3e3618f7474F8cB1d074A26afFef007E98FB`, `REWARDS_DIST_LSSKY_SKY` `0x675671A8756dDb69F7254AFB030865388Ef699Ee`, `SAFE_HARBOR_AGREEMENT` `0xf17bB418B4EC251f300Aa3517Cb37349f17697A1`, `GROVE_SUBPROXY` `0x1369f7b2b38c76B6478c0f0E66D94923421891Ba`, and `SPARK_STARGUARD` `0x6605aa120fe8b656482903E7757BaBF56947E45E`.

**Evidence**

- fetch-spell-source core spell source review
- call-verified-contract 0xf6e72Db5454dd049d0788e411b06CfAF16853042 buf --chain-id 1
- read-chainlog MCD_LITE_PSM_USDC_A; read-chainlog MCD_IAM_AUTO_LINE; read-chainlog MCD_PAUSE_PROXY; read-chainlog REWARDS_DIST_LSSKY_SKY; read-chainlog SAFE_HARBOR_AGREEMENT; read-chainlog GROVE_SUBPROXY; read-chainlog SPARK_STARGUARD

### Proxy Spell Source Review

**Status:** OK

- The core spell discloses Spark proxy spell `0xe08BD6D9016EAC522903FC68c80F809664C2692A` and hash `0xdf7cca8d640cde5f2f8184ccb03f76031a024cb8ab2c192092acfe329b5aebf5`; `check-proxy-spell-codehash` matched the runtime codehash.
- `fetch-spell-source` verified Ethereum contract `SparkEthereum_20260618`, compiler `v0.8.25+commit.b61c2a91`, optimizer 200, EVM `cancun`, proxy false. Its source configures Binance OTC limits, max slippage, OTC buffer/recharge, USDC/USDT allowlisting, and transfers `1,100,000` and `155,000` USDS grants.
- `fetch-spell-source` on Base, Optimism, and Unichain verified `SparkBase_20260618`, `SparkOptimism_20260618`, and `SparkUnichain_20260618` at `0x9A56C59453a2fBAe01Ba46045441490e5C7a664d`; each withdraws `10,000` USDS and `10,000` sUSDS to Ethereum via the local token bridge and then revokes its temporary controller role.

**Evidence**

- check-proxy-spell-codehash 0xe08BD6D9016EAC522903FC68c80F809664C2692A 0xdf7cca8d640cde5f2f8184ccb03f76031a024cb8ab2c192092acfe329b5aebf5
- fetch-spell-source 0xe08BD6D9016EAC522903FC68c80F809664C2692A --chain-id 1
- fetch-spell-source 0x9A56C59453a2fBAe01Ba46045441490e5C7a664d --chain-id 8453
- fetch-spell-source 0x9A56C59453a2fBAe01Ba46045441490e5C7a664d --chain-id 10
- fetch-spell-source 0x9A56C59453a2fBAe01Ba46045441490e5C7a664d --chain-id 130

### Spell Checklist and Reviewer Signoff

**Status:** OK

- Sky Core PR #553 had 21 review events, 5 unique reviewers, 2 latest formal approvals, no latest changes requested, CI checks succeeded, and explicit `Good to deploy` and `Good to handover` comments from `SidestreamIcedMango`; `amusingaxl` also posted approval/handover evidence.
- Spark PR #169 had 22 review events, 6 unique reviewers, 2 latest formal approvals, and no latest changes requested. It included substantive Agent spell review evidence from `deluca-mike` and `TheMj0ln1r`, plus a formal approval from `certora-spark-review` confirming deployment address `0xe08BD6D9016EAC522903FC68c80F809664C2692A`.
- `fetch-pr-reviews 169 --repo sparkdotfi/spark-spells` reported `Agent Checklist Status: substantive_unclear`, `Canonical Agent Checklist Evidence: no`, and `Agent Checklist Evidence: no`; this initially blocked automatic YES validation because the June 18, 2026 executive is when the registered Agent checklist requirement came into force.
- Public clarification by Lex on June 19, 2026 states that the Spark June 18 review evidence was substantive, the missing registered checklist was an internal communication oversight, and the checklist requirement is waived for this one Spark spell in consultation with the Core Facilitator. The requirement applies to Spark and all Agents going forward, starting with the July 2, 2026 spell.

**Evidence**

- fetch-pr-reviews 553 returned latest formal approvals 2, latest changes requested 0, explicit sign-off comments 2, checklist evidence comments 2.
- fetch-pr-ci-status 553 returned total checks 2, both `tests: success` for head SHA `41ca53f1edb49d422f670680b7575f378639a9ad`.
- fetch-pr-reviews 169 --repo sparkdotfi/spark-spells returned latest formal approvals 2, latest changes requested 0, `hasSubstantiveAgentChecklistEvidence: true`, `agentChecklistStatus: substantive_unclear`, `hasCanonicalAgentChecklistEvidence: false`.
- https://forum.skyeco.com/t/clarification-requested-required-form-of-agent-spell-reviewer-checklist-in-spell-review-prs/27974/2

### Forge Test Evidence

**Status:** OK

- `run-forge-tests 032e61aa74308f830f59d44f0a6dfb24deec3eca --pr 553` compiled successfully but the full run exited code `2` with 20 passed, 9 failed, and 26 skipped because fork/RPC reads hit Infura HTTP 429 `Too Many Requests`.
- The nine failed tests were rerun individually at exact merge commit `032e61aa74308f830f59d44f0a6dfb24deec3eca`, with `ETH_RPC_URL` mapped from `ETHEREUM_RPC_URL` and `FOUNDRY_THREADS=1`.
- Individual rerun results all passed: `testStarknet` passed 2/0/0 in `164.19s`; `testChainlogIntegrity` passed 1/0/0 in `344.58s`; `testChainlogValues` passed 1/0/0 in `348.54s`; `testGeneral` passed 1/0/0 in `365.88s`; `testPSMs` passed 1/0/0 in `190.79s`; `testPayments` passed 1/0/0 in `159.07s`; `testPrimeAgentSpellExecutions` passed 1/0/0 in `280.89s`; `testSplitter` passed 1/0/0 in `165.37s`; and `testSystemTokens` passed 1/0/0 in `163.91s`.
- This eliminates the prior forge-test evidence gap as a surviving validation finding.

**Evidence**

- run-forge-tests 032e61aa74308f830f59d44f0a6dfb24deec3eca --pr 553 returned exit code 2, passed 20, failed 9, skipped 26.
- Individual reruns with `make test no-match=testFail match=<testName>` passed for `testStarknet`, `testChainlogIntegrity`, `testChainlogValues`, `testGeneral`, `testPSMs`, `testPayments`, `testPrimeAgentSpellExecutions`, `testSplitter`, and `testSystemTokens`.

### Atlas Authorization

**Status:** OK

- `read-atlas-section A.2.4` describes the Monthly Settlement Cycle and settlement through Sky Core Executive Votes.
- `read-atlas-section A.4.4.1.2` and `A.4.4.1.4.2` cover SKY staking rewards and short-term SKY reward implementation, including rewards distribution contract `0x675671A8756dDb69F7254AFB030865388Ef699Ee`.
- `read-atlas-section A.2.11.1.2.3` requires Safe Harbor maintenance when new contracts are added.
- `read-atlas-section A.6.1.1.1.2.6.1.2.1.2.3` authorizes Phoenix Labs to propose Spark reserve claim transfers and non-USD reserve liquidation routing.
- `read-atlas-section A.1.10.2.2.5` recognizes Prime Agent spell items moving through the Executive Process.

**Evidence**

- read-atlas-section A.2.4
- read-atlas-section A.4.4.1.2
- read-atlas-section A.4.4.1.4.2
- read-atlas-section A.2.11.1.2.3
- read-atlas-section A.6.1.1.1.2.6.1.2.1.2.3
- read-atlas-section A.1.10.2.2.5

### AD Role Compliance

**Status:** OK

A YES vote is supportable because the executive's key governance implications have been reviewed, all validation checks now pass, proxy spell behavior was reviewed, and the public checklist clarification resolves the only remaining evidence gap. The recommendation is consistent with A.1.6.2.1.1 and A.1.6.6.2 because the AD can defend a yes/no vote on the available evidence, and the explanation is substantive under A.1.6.2.2 because it identifies the proposal mechanisms, implementation evidence, risk factors, and the resolved review gap.

**Evidence**

- read-atlas-section A.0.1.1.18
- read-atlas-section A.1.6
- All validation checks passed after forum clarification and individual forge test reruns.

## Recommendation

**Position:** YES
**Assessment:** Medium

Recommend YES. The core spell source matches the reviewed merge commit, the document hash matches, the proxy spell source and downstream payloads were reviewed, the failed forge tests from the full run passed individually on rerun, and the remaining Spark Agent checklist concern was resolved by public clarification waiving the registered checklist requirement for this one June 18 Spark spell. With no surviving validation findings, the analysis supports voting-estoppel confidence under A.1.6.6.2.

## Proxy Spell Review

**Required:** yes
**Status:** satisfied

- Detected proxy spell addresses: 0xe08BD6D9016EAC522903FC68c80F809664C2692A, 0x9A56C59453a2fBAe01Ba46045441490e5C7a664d
- Proxy spell addresses backed by Action-to-Code source-review evidence: 0xe08BD6D9016EAC522903FC68c80F809664C2692A, 0x9A56C59453a2fBAe01Ba46045441490e5C7a664d

## LLM Usage

- **Provider/Model:** openai / gpt-5.5
- **Tokens:** 13,868,034 in / 28,713 out / 5,821 reasoning / 13,902,568 total
- **Cache:** 13,271,040 read / 0 write
- **Cost:** $10.6565 USD estimated
- **Pricing:** openai-api-pricing-2026-06-10-standard-short-context
