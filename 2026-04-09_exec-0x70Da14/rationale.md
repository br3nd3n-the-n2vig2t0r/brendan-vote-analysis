# Analysis: Launch Avalanche SkyLink, Update Staking Rewards, Grove Genesis Capital Transfer, Safe Harbor Update, Prime Agent Proxy Spells - April 9, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-04-10T21:01:34.725Z | **Atlas:** 2026-04-10


## Summary

- Launches SkyLink connectivity to Avalanche for governance messaging plus USDS and sUSDS OFT configuration, including Avalanche rate limits and chainlog/Safe Harbor updates.
- Updates LSSKY→SKY staking rewards by replacing the vesting stream, transfers 20,797,477 USDS to Grove under its Genesis Capital allocation, and whitelists reviewed Spark and Grove proxy spells in their StarGuard modules.
- The Spark proxy spell implements the disclosed Ethereum actions and queues reviewed Arbitrum and Base payloads; the Grove proxy spell implements the disclosed Grove onboarding and rate-limit changes.

## Atlas Alignment

**Assessment:** aligned

This executive is **aligned** with the Atlas because it implements actions that fall within existing governance-authorized scope and maintenance obligations, and the validated code matches the disclosed actions.

- The Spark and Grove rate-limit changes are governance-set operational parameters of the relevant liquidity systems, consistent with the Atlas treatment of rate limits in **A.2.2.9.1.1.1.2.2**.
- The Grove transfer is within the Atlas-defined initial allocation for Grove in **A.2.8.2.2.2.5.2**: the spell transfers **20,797,477 USDS**, which is below the stated **25,000,000 USDS** initial allocation ceiling referenced in the executive.
- The Safe Harbor update directly satisfies the maintenance requirement in **A.2.11.1.2.3**, which requires newly added covered contracts and chains to be reflected in Safe Harbor.
- The Spark reserve-claim behavior disclosed through the Spark proxy spell is consistent with **A.6.1.1.1.2.6.1.2.1.2.3**, which authorizes transfers of supported USD-denominated reserves to the Spark ALM Proxy and non-supported / non-USD reserves to the Spark Operations Multisig for liquidation.
- The executive preserves standard governance safeguards: the proposal text states the 24-hour GSM delay, and the deployed spell is wired to the pause with office hours enabled, consistent with **A.1.9.3.1**.
- Under the Voting Estoppel Rule in **A.1.5.6.2**, a YES vote requires understanding every action, including proxy-spell actions. Here, the main spell, both proxy spells, and Spark’s downstream Arbitrum/Base payloads were reviewed and mapped to the disclosed actions, so that requirement is met.

**Relevant sections:** A.1.5.6.2, A.1.9.3.1, A.2.2.9.1.1.1.2.2, A.2.8.2.2.2.5.2, A.2.11.1.2.3, A.6.1.1.1.2.6.1.2.1.2.3

## Risk Assessment

**Level:** medium

- Cross-chain configuration risk from launching Avalanche SkyLink and setting LayerZero peers, libraries, configs, enforced options, and rate limits.
- Operational batching risk because the spell combines bridge setup, treasury transfer, Safe Harbor maintenance, staking rewards reconfiguration, and proxy-spell whitelisting in one execution.
- Downstream execution risk from whitelisted Spark and Grove proxy spells, mitigated here by codehash verification and source review of the proxy payloads, including Spark’s Arbitrum and Base payload contracts.

## Validation Checks

### Spell Integrity

**Status:** OK

- `action()` = `0x525010A7Cdf29fab4957F984Aa831395CB192fcd`
- `tag()` = `0x87c3686a8a56eeff5b18fd23550e9a0a2146641f4d128cd86c49aeeb01268605`
- `extcodehash(action)` = `0x87c3686a8a56eeff5b18fd23550e9a0a2146641f4d128cd86c49aeeb01268605`
- `sig()` = `0x61461954` (`execute()` selector)
- `eta()` = `0`
- `done()` = `false`
- `officeHours()` = `true`
- `expiration()` = `1778414267` (`2026-05-10T11:57:47Z`)
- `description()` = `2026-04-09 MakerDAO Executive Spell | Hash: 0x0f87466f280de3544ae715fb2463152d7959c37902926f2069aaaccf10cef550`

**Evidence**

- `check_spell_integrity(0x70Da14478667C08320Ef65506063abba84B6990f)` returned matching `tag()` and `extcodehash(action)`, `sig() = 0x61461954`, `eta() = 0`, `done() = false`, `officeHours() = true`, and `expiration() = 1778414267`.

**Raw log refs:** tool-0002

### Exec Doc Hash

**Status:** OK

- Pinned URL in source comment: `https://raw.githubusercontent.com/sky-ecosystem/executive-votes/656d5a6d9e8041203d98823248e64d87771681d3/2026/executive-vote-2026-04-09-launch-avalanche-skylink-staking-rewards-update.md`
- Hash embedded in `description`: `0x0f87466f280de3544ae715fb2463152d7959c37902926f2069aaaccf10cef550`
- Computed keccak256 of pinned URL content: `0x0f87466f280de3544ae715fb2463152d7959c37902926f2069aaaccf10cef550`
- Result: match

**Evidence**

- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` exposed the pinned raw GitHub URL in the `description` comment above the constant.
- `keccak256_url(https://raw.githubusercontent.com/sky-ecosystem/executive-votes/656d5a6d9e8041203d98823248e64d87771681d3/2026/executive-vote-2026-04-09-launch-avalanche-skylink-staking-rewards-update.md)` returned `0x0f87466f280de3544ae715fb2463152d7959c37902926f2069aaaccf10cef550`.
- `check_spell_integrity(0x70Da14478667C08320Ef65506063abba84B6990f)` returned the same hash inside `description()`.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031, tool-0012

### Source Verified on Etherscan

**Status:** OK

- Verified source was retrievable for the deployed spell on Ethereum mainnet.
- Contract name: `DssSpell`
- Source includes flattened `DssExec`, `DssAction`, `DssSpellAction`, and linked library metadata.

**Evidence**

- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` returned verified Solidity source on chain `Ethereum (1)` for contract `DssSpell`.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### DssExecLib Library

**Status:** OK

- Etherscan-reported linked library: `DssExecLib: 0x8de6ddbcd5053d32292aaa0d2105a32d108484a6`
- Repo `foundry.toml` / flatten check reported: `DssExecLib (foundry.toml): 0x8De6DDbCd5053d32292AAA0D2105A32d108484a6`
- Result: same address ignoring checksum case

**Evidence**

- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` reported linked library `DssExecLib:0x8de6ddbcd5053d32292aaa0d2105a32d108484a6`.
- `flatten_spell(commitSha=4430ef43a722d1caaa462eadd5264959548ae05f, address=0x70Da14478667C08320Ef65506063abba84B6990f)` reported `DssExecLib (foundry.toml): 0x8De6DDbCd5053d32292AAA0D2105A32d108484a6`.

**Raw log refs:** tool-0013, tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Source/Archive Diff

**Status:** OK

- Etherscan source length: `119486` chars / `2494` lines
- Flattened repo source length: `119486` chars / `2494` lines
- Result: sources are identical

**Evidence**

- `flatten_spell(commitSha=4430ef43a722d1caaa462eadd5264959548ae05f, address=0x70Da14478667C08320Ef65506063abba84B6990f)` returned `Sources are identical`.

**Raw log refs:** tool-0013, tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Compiler Settings

**Status:** OK

- Solidity compiler: `v0.8.16+commit.07a7930e`
- Optimizer: `disabled`
- EVM version: `Default`
- Proxy: `no`

**Evidence**

- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` returned compiler version `v0.8.16+commit.07a7930e`, optimization `disabled`, EVM version `Default`, proxy `no`.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Contract Structure

**Status:** OK

- `DssSpell` inherits from `DssExec`.
- Constructor is `DssExec(block.timestamp + 30 days, address(new DssSpellAction()))`.
- `officeHours()` in `DssSpellAction` returns `true`, matching the executive text.
- `DssSpellAction` storage declarations reviewed are `constant` or `immutable`, including chainlog-derived immutables and fixed constants for addresses, codehashes, gas, and EIDs.

**Evidence**

- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` showed `contract DssSpell is DssExec` and constructor `DssExec(block.timestamp + 30 days, address(new DssSpellAction()))`.
- The same verified source showed `function officeHours() public pure override returns (bool) { return true; }` and `DssSpellAction` contract variables declared as `constant` / `immutable`.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Forbidden Patterns

**Status:** OK

- No `tx.origin` usage found in the verified spell source.
- No `delegatecall`, `callcode`, or `selfdestruct` usage found in the main spell.
- Assembly usage is limited to the standard `extcodehash` block in `DssExec` for spell tag creation.
- `actions()` contains executable calls and does not unconditionally revert.
- A low-level `.call` is used only in `_updateSafeHarbor` against the configured Safe Harbor contract, with `require(success)` on each calldata item; this is not one of the forbidden patterns listed for spell review.

**Evidence**

- Manual review of `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` source found only the known `assembly { _tag := extcodehash(_action) }` block in `DssExec`, and no `tx.origin`, `delegatecall`, `callcode`, or `selfdestruct`.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Deployment Method

**Status:** OK

- Creator address: `0xb9240679ffdc72d3c2f409be34d30ce361770fc8`
- Creator type: `EOA`
- Deployment method: `CREATE`
- Creation tx: `0x9c99bbcbe28186e0e5e6dd74d4fea424a8661f2de536ba7644ea521403812e71`

**Evidence**

- `fetch_contract_creation_tx(0x70Da14478667C08320Ef65506063abba84B6990f)` returned creator `0xb9240679ffdc72d3c2f409be34d30ce361770fc8`, creator type `EOA`, deployment method `CREATE`.

**Raw log refs:** tool-0004

### PR Reviews

**Status:** OK

- PR: `#539` (`Mainnet spell 2026-04-09`)
- Formal GitHub approvals: `0`
- Explicit workflow sign-off comments: `3`
- Distinct sign-off actors: `SidestreamStrongStrawberry`, `amusingaxl`
- Sign-off evidence included `Good to deploy` and `Good to handover` comments

**Evidence**

- `fetch_spell_pr(date=2026-04-09)` returned PR `#539` with merge commit `4430ef43a722d1caaa462eadd5264959548ae05f`.
- `fetch_pr_reviews(prNumber=539)` returned `Explicit Sign-off Comments: 3`, with sign-off authors `SidestreamStrongStrawberry, amusingaxl`, including `Good to deploy` and `Good to handover`.

**Raw log refs:** tool-0005, tool-0014

### CI Status

**Status:** OK

- Head SHA: `e8c1c274`
- Total checks: `2`
- Both `tests` checks concluded `success`

**Evidence**

- `fetch_pr_ci_status(prNumber=539)` returned two CI checks, both named `tests`, both `success`.

**Raw log refs:** tool-0005, tool-0015

### Forge Tests

**Status:** OK

- Exit code: `0`
- Passed: `32`
- Failed: `0`
- Skipped: `30`
- Repo tests completed successfully on merge commit `4430ef43a722d1caaa462eadd5264959548ae05f`

**Evidence**

- `run_forge_tests(commitSha=4430ef43a722d1caaa462eadd5264959548ae05f)` returned exit code `0`, `Passed: 32`, `Failed: 0`, `Skipped: 30`.

**Raw log refs:** tool-0005, tool-0016

### Rate Constants

**Status:** N/A

No annualized Maker stability-fee or DSR rate constants were changed in this spell, so per-second rate verification was not applicable.

**Evidence**

- `fetch_executive(0x70Da14)` and verified spell source review showed no `setDSR`, `setIlkStabilityFee`, or other annualized rate-constant updates in the executive spell.

**Raw log refs:** tool-0003, tool-0028, tool-0029, tool-0030, tool-0031, tool-0001

### Proxy Spell Codehash

**Status:** OK

- Spark proxy spell `0xFa5fc020311fCC1A467FEC5886640c7dD746deAa` runtime codehash matched expected `0x2572a97846f7a6f9f159a9a69c2707cfa4186c061de2a0ec59e7a0d46473c74c`.
- Grove proxy spell `0x679eD4739c71300f7d78102AE5eE17EF8b8b2162` runtime codehash matched expected `0x4fa1f743b3d6d2855390724459129186dd684e1c07d59f88925f0059ba1e6c84`.

**Evidence**

- `check_proxy_spell_codehash(address=0xFa5fc020311fCC1A467FEC5886640c7dD746deAa, expectedCodehash=0x2572a97846f7a6f9f159a9a69c2707cfa4186c061de2a0ec59e7a0d46473c74c)` returned `Match: YES`.
- `check_proxy_spell_codehash(address=0x679eD4739c71300f7d78102AE5eE17EF8b8b2162, expectedCodehash=0x4fa1f743b3d6d2855390724459129186dd684e1c07d59f88925f0059ba1e6c84)` returned `Match: YES`.

**Raw log refs:** tool-0026, tool-0027, tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### ChainLog Addresses

**Status:** OK

- `LZ_GOV_SENDER` = `0x27FC1DD771817b53bE48Dc28789533BEa53C9CCA`
- `LZ_GOV_RELAY` = `0x2beBFe397D497b66cB14461cB6ee467b4C3B7D61`
- `USDS_OFT` = `0x1e1D42781FC170EF9da004Fb735f56F0276d01B8`
- `SPARK_STARGUARD` = `0x6605aa120fe8b656482903E7757BaBF56947E45E`
- `GROVE_STARGUARD` = `0xfc51CAa049E8894bEcFfB68c61095C3F3Ec8a880`
- `REWARDS_DIST_LSSKY_SKY` = `0x675671A8756dDb69F7254AFB030865388Ef699Ee`
- `GROVE_SUBPROXY` = `0x1369f7b2b38c76B6478c0f0E66D94923421891Ba`
- `SAFE_HARBOR_AGREEMENT` = `0xf17bB418B4EC251f300Aa3517Cb37349f17697A1`
- `DAI_USDS` = `0x3225737a9Bbb6473CB4a45b7244ACa2BeFdB276A`
- These on-chain chainlog values match the addresses referenced in the spell source and executive text.

**Evidence**

- `read_chainlog(LZ_GOV_SENDER)` returned `0x27FC1DD771817b53bE48Dc28789533BEa53C9CCA`.
- `read_chainlog(LZ_GOV_RELAY)` returned `0x2beBFe397D497b66cB14461cB6ee467b4C3B7D61`.
- `read_chainlog(USDS_OFT)` returned `0x1e1D42781FC170EF9da004Fb735f56F0276d01B8`.
- `read_chainlog(SPARK_STARGUARD)` returned `0x6605aa120fe8b656482903E7757BaBF56947E45E`.
- `read_chainlog(GROVE_STARGUARD)` returned `0xfc51CAa049E8894bEcFfB68c61095C3F3Ec8a880`.
- `read_chainlog(REWARDS_DIST_LSSKY_SKY)` returned `0x675671A8756dDb69F7254AFB030865388Ef699Ee`.
- `read_chainlog(GROVE_SUBPROXY)` returned `0x1369f7b2b38c76B6478c0f0E66D94923421891Ba`.
- `read_chainlog(SAFE_HARBOR_AGREEMENT)` returned `0xf17bB418B4EC251f300Aa3517Cb37349f17697A1`.
- `read_chainlog(DAI_USDS)` returned `0x3225737a9Bbb6473CB4a45b7244ACa2BeFdB276A`.

**Raw log refs:** tool-0017, tool-0018, tool-0019, tool-0020, tool-0021, tool-0022, tool-0023, tool-0024, tool-0025, tool-0003, tool-0028, tool-0029, tool-0030, tool-0031

### Action-to-Code Mapping

**Status:** OK

- **Avalanche SkyLink launch**: main spell source configures `LZ_GOV_SENDER`, `USDS_OFT`, and `SUSDS_OFT` for Avalanche with the disclosed peers, LayerZero libraries, configs, enforced options, and `5,000,000 USDS` inbound / outbound rate limits.
- **Staking rewards update**: main spell calls `TreasuryFundedFarmingInit.updateFarmVest` with `dist = 0x675671A8756dDb69F7254AFB030865388Ef699Ee`, `vestTot = 192,110,322 * WAD`, `vestBgn = block.timestamp`, and `vestTau = 90 days`.
- **Grove Genesis Capital transfer**: main spell calls `_transferUsds(GROVE_SUBPROXY, 20_797_477 * WAD)`.
- **Safe Harbor update**: main spell executes `_updateSafeHarbor(calldatas)`; the source comments enumerate the Avalanche chain and contract additions plus the Ethereum `0x85A3FE4DA2a6cB98A5bdF62458B0dB8471B9f0f1` entry for `SUSDS_OFT`, matching the executive description.
- **Spark proxy spell whitelist**: main spell calls `StarGuardLike(SPARK_STARGUARD).plot(0xFa5fc020311fCC1A467FEC5886640c7dD746deAa, 0x2572...c74c)`.
- **Grove proxy spell whitelist**: main spell calls `StarGuardLike(GROVE_STARGUARD).plot(0x679eD4739c71300f7d78102AE5eE17EF8b8b2162, 0x4fa1...6c84)`.
- **Spark proxy spell reviewed source** implements the disclosed Ethereum actions: deactivations / new limits for listed Spark Liquidity Layer venues, spUSDC / spUSDT / spETH deposit-cap increases, and SparkLend reserve claims. Its constructor also queues downstream reviewed payloads on **Arbitrum** and **Base**.
- **Spark Arbitrum payload reviewed source** deactivates Aave USDC and Fluid sUSDS rate limits on Arbitrum.
- **Spark Base payload reviewed source** deactivates Aave USDC and Fluid sUSDS rate limits on Base.
- **Grove proxy spell reviewed source** onboards Maple syrupUSDC and updates the JTRSY and PSM USDS/USDC Grove rate limits exactly as disclosed.
- No extra undisclosed actions were identified in the reviewed main spell, proxy spells, or reviewed Spark downstream payloads.

**Evidence**

- `fetch_executive(0x70Da14)` disclosed the top-level actions, proxy spell addresses, and detailed Spark / Grove downstream actions.
- `fetch_spell_source(0x70Da14478667C08320Ef65506063abba84B6990f)` showed the exact main-spell function calls for Avalanche LayerZero setup, staking rewards vest update, Grove USDS transfer, Safe Harbor calldata execution, and StarGuard `plot` calls.
- `fetch_spell_source(0xFa5fc020311fCC1A467FEC5886640c7dD746deAa)` showed the Spark Ethereum proxy spell actions and constructor payload addresses `0x9a93f69f4D5867CB091eDD713f0e506B4e992299` (Arbitrum) and `0xAA9Fe63350a62572efDDAC8D1c42e4d5eb95B603` (Base).
- `fetch_spell_source(0x9a93f69f4D5867CB091eDD713f0e506B4e992299, chainId=42161)` showed Arbitrum deactivation of Aave USDC and Fluid sUSDS rate limits.
- `fetch_spell_source(0xAA9Fe63350a62572efDDAC8D1c42e4d5eb95B603, chainId=8453)` showed Base deactivation of Aave USDC and Fluid sUSDS rate limits.
- `fetch_spell_source(0x679eD4739c71300f7d78102AE5eE17EF8b8b2162)` showed Grove’s Maple syrupUSDC onboarding plus JTRSY and PSM USDS/USDC rate-limit updates.
- `read_chainlog(REWARDS_DIST_LSSKY_SKY)`, `read_chainlog(GROVE_SUBPROXY)`, `read_chainlog(SAFE_HARBOR_AGREEMENT)`, `read_chainlog(SPARK_STARGUARD)`, and `read_chainlog(GROVE_STARGUARD)` matched the spell’s referenced live addresses.

**Raw log refs:** tool-0001, tool-0003, tool-0028, tool-0029, tool-0030, tool-0031, tool-0026, tool-0027

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote **YES**.

- The executive implements Atlas-consistent and governance-authorized actions, including Safe Harbor maintenance, Grove allocation transfer, and governance-set rate-limit changes.
- The deployed spell passed the required validation checks: spell wiring is intact, the Exec Doc hash matches, the deployed source matches the archived source, deployment was standard CREATE from an EOA, CI and local forge tests passed, and reviewed proxy-spell code matches the disclosed actions.
- The highest-risk components are the new Avalanche cross-chain configuration and proxy-spell whitelisting, but those components were specifically validated through source review and codehash checks.

## Proxy Spell Review

**Required:** yes
**Status:** satisfied

- Detected proxy spell addresses: 0xFa5fc020311fCC1A467FEC5886640c7dD746deAa, 0x679eD4739c71300f7d78102AE5eE17EF8b8b2162
- Proxy spell addresses backed by Action-to-Code source-review evidence: 0x70Da14478667C08320Ef65506063abba84B6990f, 0xFa5fc020311fCC1A467FEC5886640c7dD746deAa, 0x679eD4739c71300f7d78102AE5eE17EF8b8b2162, 0x9a93f69f4D5867CB091eDD713f0e506B4e992299, 0xAA9Fe63350a62572efDDAC8D1c42e4d5eb95B603

## LLM Usage

- **Provider/Model:** openai-codex / gpt-5.4 (thinking: high)
- **Turns:** 7 (32 tool calls)
- **Tokens:** 1,984,304 in / 11,361 out / 2,017,937 total
- **Cache:** 22,272 read / 0 write
- **Cost:** $5.1367
- **Duration:** 14.8m

## Evidence Trace

- **File:** analysis.evidence.json
- **Tool logs captured:** 32
