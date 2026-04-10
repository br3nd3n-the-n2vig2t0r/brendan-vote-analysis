[Launch Avalanche SkyLink, Update Staking Rewards, Grove Genesis Capital Transfer, Safe Harbor Update, Prime Agent Proxy Spells - April 9, 2026](https://raw.githubusercontent.com/sky-ecosystem/executive-votes/main/2026/executive-vote-2026-04-09-launch-avalanche-skylink-staking-rewards-update.md)

**Summary**

- Launches SkyLink connectivity to Avalanche for governance messaging plus USDS and sUSDS OFT configuration, including Avalanche rate limits and chainlog/Safe Harbor updates.
- Updates LSSKY→SKY staking rewards by replacing the vesting stream, transfers 20,797,477 USDS to Grove under its Genesis Capital allocation, and whitelists reviewed Spark and Grove proxy spells in their StarGuard modules.
- The Spark proxy spell implements the disclosed Ethereum actions and queues reviewed Arbitrum and Base payloads; the Grove proxy spell implements the disclosed Grove onboarding and rate-limit changes.

**Decision: YES**

Vote **YES**.

- The executive implements Atlas-consistent and governance-authorized actions, including Safe Harbor maintenance, Grove allocation transfer, and governance-set rate-limit changes.
- The deployed spell passed the required validation checks: spell wiring is intact, the Exec Doc hash matches, the deployed source matches the archived source, deployment was standard CREATE from an EOA, CI and local forge tests passed, and reviewed proxy-spell code matches the disclosed actions.
- The highest-risk components are the new Avalanche cross-chain configuration and proxy-spell whitelisting, but those components were specifically validated through source review and codehash checks.

[Full rationale](https://github.com/br3nd3n-the-n2vig2t0r/brendan-vote-analysis/blob/main/2026-04-09_exec-0x70Da14/rationale.md)