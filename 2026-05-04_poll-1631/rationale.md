# Analysis: Atlas Edit Weekly Cycle Proposal - May 4, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-05-04T17:17:53.579Z | **Atlas:** 2026-05-04

## Summary

This Atlas Edit Weekly Cycle proposal would merge Atlas PR #237, adding Ecosystem Accord 10 between Sky and Grove with ongoing USDS compensation to Grove tied to the Chronicle Point Reward Instance and the Base Rate, plus retroactive compensation from July 24, 2025 through March 31, 2026. It also documents how to query the current Sky Savings Rate, updates Governance Facilitator references and removes the inactive Sky Ecosystem Liquidity Bootstrapping section, simplifies the Pattern Freezer Multisig description, and fixes malformed `RateLimits` Solidity identifiers.

## Atlas Alignment

**Assessment:** aligned

The proposal is aligned with the Atlas Edit Weekly Cycle and appears substantively consistent with the Spirit of the Atlas.

- **Process fit:** A.1.10.2.1.1 allows multiple Atlas edits in a single Weekly Cycle Proposal during the transition to Endgame, provided the edits adhere to the Spirit of the Atlas and Universal Alignment. A.1.10.2.2 authorizes three-day Atlas Edit Weekly Cycle Governance Polls whose successful outcome directly edits the Atlas, and A.1.10.2.4 sets the 480,000,000 SKY Minimum Positive Participation used in the poll.
- **Substantive fit:** The Grove compensation terms use the Monthly Settlement Cycle, an established Atlas mechanism for calculating and settling recurring amounts through executive actions under A.2.4. The use of the Base Rate is anchored in A.3.1.2.1, and the new SSR-query documentation supports A.3.1.2.2 by making the current SSR value more legible.
- **Accord pattern:** A.2.8.2.2 already records detailed economic terms in an Ecosystem Accord involving Grove, so adding another Accord with clear parties, duration, formula, accrual method, and settlement mechanism is consistent with existing Atlas structure.
- **Housekeeping and consistency:** Updating Governance Facilitator references to Core Council/Core Facilitator is consistent with current role definitions in A.0.1.1.46 and A.0.1.1.51. Removing obsolete A.5.5.1.1 liquidity bootstrapping language and fixing malformed `RateLimits` identifiers improve clarity without creating independent misalignment concerns.
- **Disclosure check:** The short portal metadata summary is terse, but the full voting proposal text shown for the poll includes the author’s detailed summary of the Grove compensation percentage, Base Rate linkage, and retroactive start date. At the policy/action level, the canonical text and PR diff match, and no material PR-diff action remains undisclosed in the proposal text.

**Relevant sections:** A.0.1.1.6, A.0.1.1.9, A.0.1.1.46, A.0.1.1.51, A.1.10.2.1.1, A.1.10.2.1.2, A.1.10.2.2, A.1.10.2.4, A.2.4, A.2.8.2.2, A.3.1.2.1, A.3.1.2.2, A.5.5.1.1, A.6.1.1.2.3

## Risk Assessment

**Level:** medium

- Economic impact: Accord 10 creates an indefinite ongoing USDS compensation obligation to Grove and a retroactive entitlement for a prior period.
- Operational/calculation complexity: compensation depends on continuously varying USDS deposited in the Chronicle Point Reward Instance and changes to the Base Rate, though the Monthly Settlement Cycle includes reconciliation and true-up mechanisms.
- Live baseline context: the `REWARDS_USDS_01` StakingRewards contract currently reports about 26.53 million USDS staked, so the compensation formula has a present economic basis.
- Low direct smart-contract risk: the poll merges Atlas text only and does not itself execute on-chain code.

## Finding Verification Pass

This analysis required active false-positive elimination before finalization. One or more initial FINDING checks were re-verified and downgraded after additional scrutiny.

- **Original findings:** 1
- **Remaining findings after verification:** 0

### Eliminated Or Downgraded Findings

#### Portal Summary vs Canonical Text

- **Original status:** FINDING
- **Final status:** OK

- The short metadata summary identifies the five policy/action categories in the proposal, including adding Ecosystem Accord 10 between Sky and Grove.
- The full voting proposal text immediately includes the author’s detailed Review summary, which discloses that Accord 10 establishes compensation to Grove at **20% of Base Rate** on USDS deposited in the Rewards contract, retroactive to **July 24, 2025**.
- The compensation percentage, Base Rate linkage, and retroactive date are parameters of the disclosed top-line action: adding Ecosystem Accord 10. They are not an additional independent action omitted from the voting proposal body.
- The concise metadata summary is less detailed than the full proposal text, but after cross-checking the full displayed poll body and PR body, the disclosure is adequate at the policy/action level.

## Validation Checks

### Atlas Scope Loaded

**Status:** OK

- Loaded A.0 and A.1 as the core interpretive and governance scopes.
- Consulted A.1.10.2.1.1, A.1.10.2.1.2, and A.1.10.2.2 for Atlas Edit Weekly Cycle proposal and publication requirements.
- Consulted A.2.4 for Monthly Settlement Cycle payment mechanics.
- Consulted A.2.8.2.2 for existing Ecosystem Accord structure involving Grove.
- Consulted A.3.1.2.1 and A.3.1.2.2 for Base Rate and Sky Savings Rate context.
- Consulted A.5.5.1.1 for the removed liquidity bootstrapping section.
- Consulted A.6.1.1.2.3 for Grove’s Agent Artifact context.

**Evidence**

- read_atlas_scope(scope='A.0') returned definitions for Universal Alignment, Alignment Artifact Strength, Letter vs Spirit, Core Council, and Core Facilitator.
- read_atlas_scope(scope='A.1') returned Governance Scope rules including A.1.10.2 Atlas Edit Weekly Cycle, A.1.10.2.4 Minimum Positive Participation, and related governance-process provisions.
- read_atlas_section(sectionId='A.1.10.2.1.1') returned that multiple amendments to multiple Atlas components may be included in one Weekly Cycle Proposal and must adhere to the Spirit of the Atlas and Universal Alignment.
- read_atlas_section(sectionId='A.1.10.2.1.2') returned the Forum origination requirement for Atlas Edit Weekly Cycle Proposals.
- read_atlas_section(sectionId='A.1.10.2.2') returned that Atlas Edit Weekly Cycle polls run for three days and successful polls trigger direct Atlas edits.
- read_atlas_section(sectionId='A.2.4') returned the Monthly Settlement Cycle process and settlement-through-executive provisions.
- read_atlas_section(sectionId='A.2.8.2.2') returned Ecosystem Accord 2 terms involving Sky, Grove, Spark, and Moonbow, including economic terms and indefinite duration.
- read_atlas_section(sectionId='A.3.1.2.1') returned that the Base Rate is the key annual percentage rate.
- read_atlas_section(sectionId='A.3.1.2.2') returned SSR definition, relationship to Base Rate, and modification process.
- read_atlas_section(sectionId='A.5.5.1.1') returned the current Sky Ecosystem Liquidity Bootstrapping section being removed.
- read_atlas_section(sectionId='A.6.1.1.2.3') returned Grove Omni Documents and existing Grove Ecosystem Accord references.

**Raw log refs:** tool-0011, tool-0018, tool-0012, tool-0013, tool-0014, tool-0015, tool-0016, tool-0017, tool-0020, tool-0021, tool-0022, tool-0025

### Minimum Positive Participation

**Status:** OK

- The poll victory condition requires Yes votes to exceed No votes and Yes vote-weight to be at least **480,000,000 SKY**.
- A.1.10.2.4 states that Atlas Edit Weekly Cycle Proposals must have at least **480,000,000 SKY** equivalents of Yes votes to be accepted.

**Evidence**

- fetch_proposal(pollId=1631) returned victory condition `{ type: comparison, comparator: '>=', value: 480000000 }` and text stating Minimum Positive Participation is 480,000,000 SKY.
- read_atlas_scope(scope='A.1') returned A.1.10.2.4: 'Atlas Edit Weekly Cycle Proposals must have at least 480,000,000 SKY equivalents of Yes votes to be accepted.'

### Portal Summary vs Canonical Text

**Status:** OK

- The short metadata summary identifies the five policy/action categories in the proposal, including adding Ecosystem Accord 10 between Sky and Grove.
- The full voting proposal text immediately includes the author’s detailed Review summary, which discloses that Accord 10 establishes compensation to Grove at **20% of Base Rate** on USDS deposited in the Rewards contract, retroactive to **July 24, 2025**.
- The compensation percentage, Base Rate linkage, and retroactive date are parameters of the disclosed top-line action: adding Ecosystem Accord 10. They are not an additional independent action omitted from the voting proposal body.
- The concise metadata summary is less detailed than the full proposal text, but after cross-checking the full displayed poll body and PR body, the disclosure is adequate at the policy/action level.

**Evidence**

- fetch_proposal(pollId=1631) returned portal Summary: 'This Atlas edit proposal 1) adds Ecosystem Accord 10 between Sky and Grove...' and lists the other four top-level actions.
- fetch_proposal(pollId=1631) returned Full Proposal Text Review bullet: 'Add Ecosystem Accord Between Sky And Grove — Adds Ecosystem Accord 10, establishing compensation to Grove for the Chronicle Point Reward Instance at 20% of Base Rate on USDS deposited in the Rewards contract, retroactive to July 24, 2025.'
- fetch_atlas_pr_diff(prNumber=237) returned PR body with the same detailed Grove Accord summary as the full proposal text.
- read_atlas_section(sectionId='A.1.10.2.2') returned publication requirements for the Governance Poll but did not impose a separate requirement that the frontmatter metadata summary reproduce every parameter in the proposal body.

**Raw log refs:** tool-0001, tool-0023

### Canonical Text vs PR Diff

**Status:** OK

- The canonical proposal links Atlas PR #237 and its detailed author summary matches the PR body.
- PR #237 adds A.2.8.2.10, specifying Accord 10 parties, indefinite duration, the Chronicle Point Reward Instance, compensation formula, accrual method, monthly settlement, and retroactive compensation.
- PR #237 adds A.3.1.2.2.3 documenting the sUSDS address, `ssr()` function, RAY precision, and annualized-rate formula.
- PR #237 updates Governance Facilitator references, removes A.5.5, simplifies the Pattern Freezer Multisig wording, and fixes `RateLimits` identifier spacing in Keel, Obex, and Pattern sections.
- Supporting edits such as removing dangling cross-references to the deleted A.5.5 section and adding the Grove Accord 10 link under Grove are derivative of disclosed top-line changes and were not treated as separate material omissions.

**Evidence**

- fetch_proposal(pollId=1631) returned canonical proposal text linking https://github.com/sky-ecosystem/next-gen-atlas/pull/237 and listing the five author-provided edit bullets.
- fetch_atlas_pr_diff(prNumber=237) returned PR body with the same five bullets as the canonical proposal text.
- fetch_atlas_pr_diff(prNumber=237) returned diff adding A.2.8.2.10 with compensation formula `Chronicle_Point_Reward_Instance_USDS_Deposited × 20% × Base_Rate`, monthly settlement, and retroactive compensation.
- fetch_atlas_pr_diff(prNumber=237) returned diff adding A.3.1.2.2.3 with sUSDS address `0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD`, `ssr()`, and annualized-rate formula.
- fetch_atlas_pr_diff(prNumber=237) returned one changed file with 139 additions and 73 deletions.

**Raw log refs:** tool-0001, tool-0023, tool-0002, tool-0024

### False-Positive Elimination Review

**Status:** OK

- Re-tested the prior disclosure concern against the full voting proposal text, not only the short frontmatter metadata summary.
- Confirmed that the full poll body contains the detailed author-provided Grove Accord bullet with compensation percentage, Base Rate linkage, and retroactive start date.
- Confirmed that PR #237’s body and diff match the detailed canonical proposal text.
- Confirmed that the detailed economic terms are parameters of the disclosed top-line action to add Accord 10, not a separate hidden policy/action item.
- The prior concern does not survive adversarial verification as a validation finding.

**Evidence**

- fetch_proposal(pollId=1631) was rerun and returned both the short Summary and the Full Proposal Text with detailed Review bullets.
- fetch_atlas_pr_diff(prNumber=237) was rerun and returned the PR body and diff showing the same Grove Accord economic terms.
- read_atlas_section(sectionId='A.1.10.2.1.1') returned that multiple amendments can be submitted in a single Weekly Cycle Proposal, supporting policy/action-level review.
- read_atlas_section(sectionId='A.1.10.2.2') returned the poll publication rule but no separate requirement that a short metadata summary reproduce all detailed parameters.

### On-Chain Address Baseline

**Status:** OK

- The sUSDS address proposed for SSR querying matches the Chainlog `SUSDS` entry: `0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD`.
- The Chronicle Point Reward Instance is described as the contract corresponding to Chainlog key `REWARDS_USDS_01`; Chainlog returns `0x10ab606B067C9C461d8893c47C7512472E19e2Ce`.
- The `REWARDS_USDS_01` contract source is verified as `StakingRewards`, consistent with the PR description.
- The `REWARDS_USDS_01` staking token is the Chainlog `USDS` address `0xdC035D45d973E3EC169d2276DDab16f1e407384F`.

**Evidence**

- read_chainlog(key='SUSDS') returned `0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD`.
- read_chainlog(key='REWARDS_USDS_01') returned `0x10ab606B067C9C461d8893c47C7512472E19e2Ce`.
- fetch_spell_source(address='0x10ab606B067C9C461d8893c47C7512472E19e2Ce', chainId=1) returned Contract Name `StakingRewards`, verified source, compiler v0.8.16, optimizer enabled 200 runs.
- fetch_atlas_pr_diff(prNumber=237) returned A.2.8.2.10.2.1 defining the Chronicle Point Reward Instance as the verified `StakingRewards` contract at the `REWARDS_USDS_01` Chainlog key.
- call_verified_contract(address='0x10ab606B067C9C461d8893c47C7512472E19e2Ce', functionName='stakingToken', args=[], chainId=1) returned `0xdC035D45d973E3EC169d2276DDab16f1e407384F`.
- read_chainlog(key='USDS') returned `0xdC035D45d973E3EC169d2276DDab16f1e407384F`.

**Raw log refs:** tool-0003, tool-0005, tool-0029, tool-0007, tool-0009

### On-Chain Parameter Baseline

**Status:** OK

- The Chronicle Point Reward Instance currently has nonzero USDS deposits.
- `totalSupply()` on `REWARDS_USDS_01` returned `26527001419189626409408240`, or about **26,527,001.419 USDS** assuming 18 decimals.
- This supports treating the compensation formula as having present economic relevance, which is disclosed in the full proposal text and PR.

**Evidence**

- call_verified_contract(address='0x10ab606B067C9C461d8893c47C7512472E19e2Ce', functionName='totalSupply', args=[], chainId=1) returned `26527001419189626409408240`.
- fetch_spell_source(address='0x10ab606B067C9C461d8893c47C7512472E19e2Ce', chainId=1) returned `StakingRewards` source with `uint256 private _totalSupply` and `function totalSupply() external view returns (uint256)`.

**Raw log refs:** tool-0007, tool-0009, tool-0003, tool-0005, tool-0029

### On-Chain SSR Function Baseline

**Status:** OK

- The sUSDS address is an ERC1967 proxy whose implementation slot points to `0x4e7991e5c547ce825bdeb665ee14a3274f9f61e0`.
- The implementation source is verified as `SUsds` and includes `uint256 public ssr`, which exposes an `ssr()` getter.
- The implementation also uses `ssr` in per-second compounding calculations, consistent with the PR’s documentation.
- The proxy storage slot for `ssr` was read at slot `0x6`, returning raw value `0x0000000000000000000000000000000000000000033b2e3caf972c34ac403686`.
- A direct `call_verified_contract` attempt against the proxy did not find `ssr` because the verified ABI on Etherscan is the ERC1967 proxy ABI; this was resolved by inspecting the implementation address, source, and proxy storage.

**Evidence**

- call_verified_contract(address='0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD', functionName='ssr', args=[]) returned 'Function ssr was not found in the verified ABI' because the proxy ABI was used.
- fetch_spell_source(address='0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD', chainId=1) returned Contract Name `ERC1967Proxy`, Proxy `yes`, implementation constructor argument `0x4e7991e5c547ce825bdeb665ee14a3274f9f61e0`.
- read_contract_storage(address='0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD', slot='0x360894a13ba1a3210667c828492db98dca3e2076cc3735a920a3ca505d382bbc') returned value ending in `4e7991e5c547ce825bdeb665ee14a3274f9f61e0`.
- fetch_spell_source(address='0x4e7991e5c547ce825bdeb665ee14a3274f9f61e0', chainId=1) returned Contract Name `SUsds` and source containing `uint256 public ssr;` and `_rpow(ssr, block.timestamp - rho)`.
- read_contract_storage(address='0xa3931d71877C0E7a3148CB7Eb4463524FEc27fbD', slot='0x6') returned `0x0000000000000000000000000000000000000000033b2e3caf972c34ac403686`.

**Raw log refs:** tool-0004, tool-0026, tool-0027, tool-0028

### Derivative Sync Context

**Status:** OK

- Governance Facilitator reference updates are consistency edits reflecting the current Core Council/Core Facilitator role architecture.
- Removing references to A.5.5 is derivative of the disclosed removal of the inactive liquidity bootstrapping section.
- The Pattern Freezer Multisig edit removes a redundant controlling-party clause while leaving the Signers subsection to identify controllers.
- `RateLimits` spacing fixes are clerical corrections to malformed Solidity identifiers and do not create independent authorization or economic effects.

**Evidence**

- fetch_atlas_pr_diff(prNumber=237) showed Governance Facilitator references changed to Core Council or Core Facilitator in SparkLend multisig and Liquidity Layer Freezer contexts.
- read_atlas_scope(scope='A.0') returned A.0.1.1.46 defining Core Council and A.0.1.1.51 defining Core Council Executor Facilitator / Core Facilitator.
- fetch_atlas_pr_diff(prNumber=237) showed A.5.5 deleted and two remaining cross-references to A.5.5 removed from text.
- read_atlas_section(sectionId='A.5.5.1.1') returned the existing short-term liquidity bootstrapping language proposed for deletion.
- fetch_atlas_pr_diff(prNumber=237) showed `Rate Limits` / `Rate LimitData` / function-name spacing corrected to `RateLimits`, `RateLimitData`, and `getRateLimitData` style identifiers.

**Raw log refs:** tool-0007, tool-0009, tool-0003, tool-0005, tool-0029

### Alignment Assessment

**Status:** OK

- The proposed Atlas text is within the Atlas Edit Weekly Cycle process and is substantively grounded in existing Atlas mechanisms.
- The new Grove compensation terms are clear in the canonical text and PR diff, and settlement through the MSC is an established Atlas process.
- The SSR and address documentation increases legibility of an existing Stability Scope rate.
- Cleanup edits reduce outdated or malformed Atlas language.
- No validation findings remain after additional cross-checking.

**Evidence**

- read_atlas_scope(scope='A.1') returned A.1.10.2.1.1 allowing multiple amendments to multiple Atlas components in a single Weekly Cycle Proposal, subject to Spirit of Atlas and Universal Alignment.
- read_atlas_section(sectionId='A.2.4') returned MSC processes for calculating and settling amounts due to and from Primes and other ecosystem participants.
- read_atlas_section(sectionId='A.2.8.2.2') returned existing Ecosystem Accord 2 terms involving Grove, including economic provisions recorded in the Atlas.
- read_atlas_section(sectionId='A.3.1.2.1') returned Base Rate definition as annual percentage rate.
- read_atlas_section(sectionId='A.3.1.2.2') returned SSR definition and modification process.
- fetch_atlas_pr_diff(prNumber=237) returned the full PR diff with no material policy/action changes beyond those disclosed in the canonical proposal text.

**Raw log refs:** tool-0011, tool-0018, tool-0012, tool-0013, tool-0014, tool-0015, tool-0016, tool-0017, tool-0020, tool-0021, tool-0022, tool-0025

## Recommendation

**Position:** YES
**Assessment:** Medium

I recommend **YES**.

The proposal follows the Atlas Edit Weekly Cycle, the canonical proposal text accurately reflects PR #237 at the policy/action level, and the material Grove compensation terms are disclosed in the poll body. The edits are either clear Atlas-authorized economic terms or housekeeping improvements that strengthen clarity and consistency.

## LLM Usage

- **Provider/Model:** openai-codex / gpt-5.5 (thinking: high)
- **Turns:** 18 (30 tool calls)
- **Tokens:** 733,632 in / 17,485 out / 1,938,445 total
- **Cache:** 1,187,328 read / 0 write
- **Cost:** $4.7864
- **Duration:** 6.2m

## Evidence Trace

- **File:** analysis.evidence.json
- **Tool logs captured:** 30
