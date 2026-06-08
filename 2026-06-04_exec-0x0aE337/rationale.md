# Analysis: RWA001-A Offboarding, Keeper Network Adjustments, ALLOCATOR-SPARK-A Parameter Updates, MKR to SKY Delayed Upgrade Penalty Increase, Prime Agent Proxy Spells - June 4, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-08T19:31:23.174Z | **Atlas:** 2026-06-08

## Summary

This executive performs a multi-part June 4, 2026 spell: conditional RWA001-A offboarding step 1; Keeper Network lane and payment-adapter changes; ALLOCATOR-SPARK-A DC-IAM gap and ttl updates while keeping line at 10 billion USDS; a MKR-SKY delayed upgrade penalty increase from 3% to 4%; and StarGuard whitelisting of Spark and Grove Prime Agent proxy spells. The spell has been scheduled and cast, and vote.sky.money reports execution on 2026-06-08T14:22:59.000Z.

## Atlas Alignment

**Assessment:** aligned

The direct ALLOCATOR-SPARK-A parameter update is within the Atlas update process for Prime Allocator Vault risk parameters, and the MKR-SKY fee increase follows the Atlas schedule for gradually increasing the delayed upgrade penalty. The Spark and Grove proxy-spell items map to disclosed Prime Agent operational authorizations, including Spark reserve-claim authorization, Spark excess SubDAO Proxy funds disposition, Grove Q2 2026 foundation grant authorization, and Grove CCTP v2 relay receiver listing. The RWA001-A and keeper-network items rely on disclosed forum and poll authorization and do not conflict with the reviewed Atlas sections. No reviewed evidence showed an undisclosed material action or invalid authorization.

**Relevant sections:** A.0.1.1.18, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.2, A.3.7.1.2.1, A.3.7.1.2.2, A.4.1.2.1.1.1.1, A.6.1.1.1.2.6.1.2.1.2.3, A.6.1.1.1.3.4.2.3, A.2.8.2.2.2.4.5.2.1, A.6.1.1.2.2.6.1.2.1.1.1.1.3.3

## Risk Assessment

**Level:** medium

- The spell touches multiple operational domains: RWA offboarding, keeper automation, allocator-vault risk limits, MKR-to-SKY migration economics, and Prime Agent proxy-spell whitelisting.
- The RWA001-A sequence is conditional and contains a mitigant against a disclosed griefing vector by executing only if RWA001-A debt exceeds the expected USDC repayment amount.
- The Spark and Grove proxy spells include cross-chain payloads on Avalanche and Base, which increases review surface, but their verified source was reviewed and mapped to the executive text.
- The ALLOCATOR-SPARK-A gap increase from 500 million to 1.5 billion USDS materially accelerates available allocator capacity while keeping the 10 billion USDS line unchanged.
- The MKR-SKY delayed upgrade fee increase is predictable and Atlas-scheduled, but it directly affects remaining MKR holders who delay migration.

## Validation Checks

### Executive Metadata and Disclosure

**Status:** OK

- fetch-executive resolved address 0x0aE3371e9C4e37515259D124C685fe6722c5e253 to the June 4, 2026 executive.
- vote.sky.money metadata reports spellCast=true, spellScheduled=true, officeHours=true, SKY support 6523815983.854202060148930511, and dateExecuted 2026-06-08T14:22:59.000Z.
- Portal summary and canonical executive text disclose the same material categories: RWA001-A offboarding, keeper-network changes, ALLOCATOR-SPARK-A DC-IAM updates, MKR-SKY fee increase, and Spark/Grove proxy spell whitelisting.
- No material portal-summary omission or canonical-text mismatch was identified.

**Evidence**

- fetch-executive 0x0aE3371e9C4e37515259D124C685fe6722c5e253
- resolve-target 0x0aE3371e9C4e37515259D124C685fe6722c5e253

### Spell Integrity

**Status:** OK

- check-spell-integrity returned action() 0x89048adf3ceF4295B9EB48107bF763097B1FE370.
- tag() and extcodehash(action) both equal 0xd951fd6c755163e08b4a4293fe38919b14a76b8dcf15fb6f5f21e29acdb4d48f.
- sig() is 0x61461954, matching execute().
- eta is 1780876823, scheduled at 2026-06-08T00:00:23.000Z; done() is true.
- officeHours() is true, matching the executive document.
- expiration is 1783095839, 2026-07-03T16:23:59.000Z.
- description is 2026-06-04 MakerDAO Executive Spell | Hash: 0x308b1dd568cd214b660c3a47caf28e97685b7a3c36c81a8cdd99c885c2caf5c2.

**Evidence**

- check-spell-integrity 0x0aE3371e9C4e37515259D124C685fe6722c5e253

### Exec Doc Hash

**Status:** OK

- The verified source pins raw executive document URL https://raw.githubusercontent.com/sky-ecosystem/executive-votes/2637e6d8d97be8318922e742945d01041ad42645/2026/executive-vote-2026-06-04-rwa001-a-offboarding-keeper-adjustments.md.
- keccak256-url returned content length 19357 characters and hash 0x308b1dd568cd214b660c3a47caf28e97685b7a3c36c81a8cdd99c885c2caf5c2.
- The computed hash matches the hash embedded in the on-chain description.

**Evidence**

- fetch-spell-source 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1
- keccak256-url https://raw.githubusercontent.com/sky-ecosystem/executive-votes/2637e6d8d97be8318922e742945d01041ad42645/2026/executive-vote-2026-06-04-rwa001-a-offboarding-keeper-adjustments.md
- check-spell-integrity 0x0aE3371e9C4e37515259D124C685fe6722c5e253

### Verified Source and Source Diff

**Status:** OK

- fetch-spell-source verified DssSpell on Ethereum chain 1.
- Compiler version is v0.8.16+commit.07a7930e, optimization disabled, EVM version default, proxy=false, constructor args none.
- Etherscan-linked DssExecLib address is 0x8de6ddbcd5053d32292aaa0d2105a32d108484a6.
- flatten-spell compared deployed Etherscan source with src/DssSpell.sol at merge commit 8cec9ae8687f70dc7964b8901a832ce4f452a94e and reported identical sources: 77272 chars, 1660 lines.
- flatten-spell reported foundry.toml DssExecLib address 0x8De6DDbCd5053d32292AAA0D2105A32d108484a6, matching the verified source library address.

**Evidence**

- fetch-spell-source 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1
- flatten-spell 8cec9ae8687f70dc7964b8901a832ce4f452a94e 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --pr 551
- fetch-spell-pr 2026-06-04

### Deployment Method

**Status:** OK

- fetch-contract-creation found the main spell creation transaction on Ethereum chain 1.
- Creator address is 0x34dbf275e1df79d1fc7bf6a37fec56a8b1057490.
- Creator type is EOA.
- Deployment method is CREATE, standard deployment.
- Creation transaction hash is 0xcb658b7dc65af07aced74f12d526961ff70740faf93b4cd33a7958b700603c0d.

**Evidence**

- fetch-contract-creation 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1

### PR Reviews and CI

**Status:** OK

- fetch-spell-pr found PR #551, Mainnet spell 2026-06-04, merged 2026-06-03T19:52:31Z.
- Merge commit is 8cec9ae8687f70dc7964b8901a832ce4f452a94e; head SHA is a4af7f1da1716abda084ed1ab4b71abf70bbf731.
- fetch-pr-reviews reported 24 review events, 8 unique reviewers, latest formal approvals from pedrobergamini and SidestreamFrostyFig, latest changes requested 0, and 5 explicit sign-off comments.
- fetch-pr-ci-status reported 2 checks for head SHA a4af7f1da1716abda084ed1ab4b71abf70bbf731, both named tests and both success.

**Evidence**

- fetch-spell-pr 2026-06-04
- fetch-pr-reviews 551
- fetch-pr-ci-status 551

### Local Forge Tests

**Status:** OK

- run-forge-tests 8cec9ae8687f70dc7964b8901a832ce4f452a94e --pr 551 completed with exit code 0.
- The command reported 21 passing tests, 0 failed tests, and 36 skipped tests across 2 suites.
- StarknetTests passed 2 tests; DssSpellTest passed 19 tests and skipped 36 tests.
- Local forge-test evidence now agrees with the successful PR CI evidence.

**Evidence**

- run-forge-tests 8cec9ae8687f70dc7964b8901a832ce4f452a94e --pr 551
- fetch-pr-ci-status 551

### Forbidden Patterns and Contract Structure

**Status:** OK

- The reviewed PR #551 spell source defines DssSpellAction is DssAction and DssSpell is DssExec.
- DssSpell constructor uses DssExec(block.timestamp + 30 days, address(new DssSpellAction())).
- DssSpellAction storage values are constants or immutables.
- A narrowed static scan of data/cache/spells-mainnet/src/DssSpell.sol and archive/2026-06-04-DssSpell/DssSpell.sol found no tx.origin, delegatecall, callcode, selfdestruct, custom assembly, or unconditional revert in the spell source.

**Evidence**

- fetch-spell-source 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1
- rg -n "tx\.origin|delegatecall|callcode|selfdestruct|assembly|revert\(" data/cache/spells-mainnet/src/DssSpell.sol data/cache/spells-mainnet/archive/2026-06-04-DssSpell/DssSpell.sol -S

### Action-to-Code Mapping

**Status:** OK

- RWA001-A offboarding maps to code that reads RWA001-A Art/rate, compares debt against expectedSwapDaiRad, temporarily raises LITE-PSM-USDC-A AutoLine amount to 10014319244, executes MCD_IAM_AUTO_LINE, fills the Lite PSM if rush()>0, approves and sells 14319243.51 USDC, wipes RWA001_A_URN, sets RWA001-A line to zero, decreases global line by the previous RWA001-A line, and calls MIP21_LIQUIDATION_ORACLE.tell("RWA001-A").
- Keeper-network changes map to CRON_SEQUENCER.removeNetwork("GELATO"), payment adapter treasury zeroing for 0x0B5a34D084b6A5ae4361de033d1e6255623b41eD, removeNetwork("KEEP3R"), payment adapter treasury zeroing for 0xaeFed819b6657B3960A8515863abe0529Dfc444A, addNetwork("SKY", makerLength), and removeNetwork("MAKER").
- ALLOCATOR-SPARK-A maps to setIlkAutoLineParameters with gap 1500 * MILLION, ttl 12 hours, amount 10 * BILLION.
- MKR-SKY maps to DssExecLib.setValue(MKR_SKY, "fee", 4 * WAD / 100).
- Spark StarGuard whitelisting maps to SPARK_STARGUARD.plot(0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20, 0x7801a877c029ce6ec7dcde0d16183eef2f81fd6e8fbd04a6433f0d6c3c0ed267).
- Grove StarGuard whitelisting maps to GROVE_STARGUARD.plot(0xbE5E67C516074ba0807A3535035868cE7F2Bd372, 0xb14f6d21bb231192c44f9b868d915f8f541213a6834a72c6158efbd64ff3223c).
- No undisclosed material direct code action was identified.

**Evidence**

- fetch-executive 0x0aE3371e9C4e37515259D124C685fe6722c5e253
- fetch-spell-source 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1
- fetch-spell-archive 2026-06-04

### Proxy Spell Review

**Status:** OK

- check-proxy-spell-codehash confirmed Spark proxy spell 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20 runtime codehash equals expected 0x7801a877c029ce6ec7dcde0d16183eef2f81fd6e8fbd04a6433f0d6c3c0ed267.
- check-proxy-spell-codehash confirmed Grove proxy spell 0xbE5E67C516074ba0807A3535035868cE7F2Bd372 runtime codehash equals expected 0xb14f6d21bb231192c44f9b868d915f8f541213a6834a72c6158efbd64ff3223c.
- SparkEthereum_20260604 verified source implements BTC eMode deprecation, cap automator changes, deprecated-asset LTV/liquidation-threshold changes, USDC/USDT reserve factor increases, SLL rate-limit changes, Ethereum ALM Proxy Freezable role migration, Spark Savings and Morpho allocator updates, and 663354 USDS transfer to the ALM Ops multisig.
- SparkAvalanche_20260604 verified source grants allocator/freezer roles to the new Avalanche ALM Proxy Freezable and migrates spUSDC setter role.
- SparkBase_20260604 verified source grants allocator/freezer roles to the new Base ALM Proxy Freezable and migrates Base Spark USDC Morpho vault allocator role.
- GroveEthereum_20260604 verified source transfers 1600000 USDS to Grove Foundation, transfers 500000000 GROVE to Grove Foundation, and swaps 753649 USDC to USDS via the Lite PSM wrapper.
- GroveAvalanche_20260604 verified source grants Avalanche GROVE_EXECUTOR SUBMISSION_ROLE to CCTP v2 receiver 0x8Ea8Dff8c29f568eA1E716E2C3AfbD003EB83cfA.
- Spark proxy creation lookup did not return a creation transaction from the Etherscan API, but verified source and codehash evidence were sufficient for the whitelist/action mapping. Grove proxy creation was EOA CREATE: creator 0xf544d77337167715f5a80c20de4bc416234543af, tx 0xc25c7193cb31366dac991c77b2789b7b7c386920bf7e7fa5fe7b8c102b8cee51.

**Evidence**

- check-proxy-spell-codehash 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20 0x7801a877c029ce6ec7dcde0d16183eef2f81fd6e8fbd04a6433f0d6c3c0ed267
- check-proxy-spell-codehash 0xbE5E67C516074ba0807A3535035868cE7F2Bd372 0xb14f6d21bb231192c44f9b868d915f8f541213a6834a72c6158efbd64ff3223c
- fetch-spell-source 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20 --chain-id 1
- fetch-spell-source 0x7ac96180C4d6b2A328D3a19ac059D0E7Fc3C6d41 --chain-id 43114
- fetch-spell-source 0x1566BFA55D95686a823751298533D42651183988 --chain-id 8453
- fetch-spell-source 0xbE5E67C516074ba0807A3535035868cE7F2Bd372 --chain-id 1
- fetch-spell-source 0xa080c8fd1B68F4D3D8F36C30137913E0BD25b0B9 --chain-id 43114
- fetch-contract-creation 0xbE5E67C516074ba0807A3535035868cE7F2Bd372 --chain-id 1

### Atlas Alignment and Authorization

**Status:** OK

- A.3.7.1.2.1 lists ALLOCATOR-SPARK-A DC-IAM baseline parameters: gap 500 million USDS, line 10 billion USDS, ttl 24 hours.
- A.3.7.1.2.2 allows Core GovOps, in consultation with the Core Council Risk Advisor, to modify Prime Allocator Vault Risk Parameters directly via an Executive Vote without a prior Governance Poll.
- A.4.1.2.1.1.1.1 schedules the MKR to SKY delayed upgrade penalty to increase by 1 percentage point per 3 months after the September 18, 2025 executive set it to 1%.
- A.6.1.1.1.2.6.1.2.1.2.3 authorizes Phoenix Labs to propose Spark reserve/collector revenue transfers to the Spark ALM Proxy and transfers of non-supported reserve assets to 0x2E1b01adABB8D4981863394bEa23a1263CBaeDfC.
- A.6.1.1.1.3.4.2.3 defines Spark excess SubDAO Proxy funds disposition policy.
- A.2.8.2.2.2.4.5.2.1 authorizes 800000 USDS per month for the Grove Foundation from Grove Prime Treasury for three months beginning April 1, 2026, with transfers to 0xE3EC4CC359E68c9dCE15Bf667b1aD37Df54a5a42.
- A.6.1.1.2.2.6.1.2.1.1.1.1.3.3 lists Grove Avalanche CCTP v2 receiver 0x8Ea8Dff8c29f568eA1E716E2C3AfbD003EB83cfA.
- The RWA001-A and keeper-network actions cite disclosed forum and governance-poll authorization. No reviewed Atlas evidence conflicts with those actions.

**Evidence**

- sync-atlas -> Atlas active version 2026-06-08
- read-atlas-section A.3.7.1.2.1
- read-atlas-section A.3.7.1.2.2
- read-atlas-section A.4.1.2.1.1.1.1
- read-atlas-section A.6.1.1.1.2.6.1.2.1.2.3
- read-atlas-section A.6.1.1.1.3.4.2.3
- read-atlas-section A.2.8.2.2.2.4.5.2.1
- read-atlas-section A.6.1.1.2.2.6.1.2.1.1.1.1.3.3
- fetch-executive 0x0aE3371e9C4e37515259D124C685fe6722c5e253

### Economic and Operational Risk

**Status:** OK

- RWA001-A offboarding reduces RWA001-A line to zero and starts soft liquidation after partial debt repayment, which supports risk reduction but depends on a follow-up spell for final liquidation.
- The ALLOCATOR-SPARK-A change increases gap from 500 million to 1.5 billion USDS and reduces ttl from 24 hours to 12 hours while holding line at 10 billion USDS; this increases operational throughput without expanding the maximum line.
- The MKR-SKY delayed upgrade penalty increase from 3% to 4% is economically material to non-migrated MKR holders but follows the Atlas rate of change.
- Keeper lane removals and MAKER-to-SKY rename reduce legacy keeper-network configuration and claim paths.
- Prime Agent proxy spells add operational and cross-chain review surface, but verified code maps to disclosed actions and codehashes match the whitelist values.

**Evidence**

- fetch-executive 0x0aE3371e9C4e37515259D124C685fe6722c5e253
- fetch-spell-source 0x0aE3371e9C4e37515259D124C685fe6722c5e253 --chain-id 1
- fetch-spell-source 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20 --chain-id 1
- fetch-spell-source 0xbE5E67C516074ba0807A3535035868cE7F2Bd372 --chain-id 1

### AD Role Compliance

**Status:** OK

- A.0.1.1.18 requires ADs to use delegated power to uphold the Spirit of the Atlas and maintain Universal Alignment.
- A.1.6.2.1.1 frames abstention as an exception for conflicts or insufficient expertise, not a substitute for available due diligence.
- A.1.6.2.2 requires a vote explanation to show understanding of core mechanisms, a reasoned basis, and at least one substantive benefit, risk, implementation, or alignment aspect.
- A.1.6.6.2 states that voting in favor constitutes acknowledgment that the AD read and understood key governance implications.
- The evidence supports a YES recommendation because the analysis identifies the core mechanisms, maps the actions to code, reviews the proxy payloads, cites Atlas support, and describes material risks. No unresolved finding or high-risk condition requires abstention or human review before treating the rationale as complete.

**Evidence**

- read-atlas-section A.0.1.1.18
- read-atlas-section A.1.6.2.1.1
- read-atlas-section A.1.6.2.2
- read-atlas-section A.1.6.6.2
- all validation checks in this draft

## Recommendation

**Position:** YES
**Assessment:** Medium

Support is justified because the executive's disclosed actions map to reviewed deployed code, the spell integrity and source comparison checks passed, the canonical executive document hash matches the on-chain description, PR review and CI evidence are clean, and the proxy spell review covered the Spark and Grove Ethereum contracts plus their disclosed Avalanche/Base payloads. The main substantive risks are operational complexity and cross-chain proxy-spell surface, not identified misalignment or failed spell validation. On the evidence reviewed, voting YES is consistent with AD obligations to actively steward governance, understand the proposal, and provide a substantive explanation.

## Proxy Spell Review

**Required:** yes
**Status:** satisfied

- Detected proxy spell addresses: 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20, 0xbE5E67C516074ba0807A3535035868cE7F2Bd372
- Proxy spell addresses backed by Action-to-Code source-review evidence: 0xAb385eC0Df225D5A37F5245D2aE43D53Fe4Fed20, 0xbE5E67C516074ba0807A3535035868cE7F2Bd372
