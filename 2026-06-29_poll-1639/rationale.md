# Analysis: Atlas Edit Weekly Cycle Proposal - June 29, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-06-29T19:55:43.918Z | **Atlas:** 2026-06-29
**Analysis guidance reviewed against Atlas:** 2026-06-25

## Summary

Poll 1639 is an Atlas Edit Weekly Cycle Proposal tied to Atlas PR #270. The official portal, canonical proposal text, forum thread, and PR body all disclose the same five edit groups: a 100% exposure-level Capital Ratio Requirement for unauthorized lending-market exposures, a move of Galaxy Warehouse from 100% interim-deployment treatment to a 2% CRR with a 500,000,000 USD maximum exposure, a 2,528,000 USDS Grove prime-revenue credit that counts toward Total Risk Capital until the next Monthly Settlement Cycle pays it, a ten-year GROVE token reward distribution schedule totaling 4,900,000,000 tokens for USDS users, and replacement of inline spell-checklist URLs with cross-references to the registered checklist section. Risk is medium rather than low because the forum post was made on Monday, June 29, 2026 instead of by the Friday, June 26, 2026 08:00 UTC recommendation, the next-gen-atlas PR showed no public review events, the economic parameters are material, and Cloaky's AD Buffer balance was not independently public even though the official poll publication implies the Core Facilitator treated the trigger threshold as satisfied. I found no material mismatch between the portal text, canonical proposal text, forum origination, and PR diff, and the edits track existing Atlas mechanisms for interim-deployment graduation, full-reservation treatment when risk cannot be assessed, TRC formalization, and registered checklist references.

## Atlas Alignment

**Assessment:** aligned

The proposal stays within the Atlas Edit Weekly Cycle's permitted scope for multi-document amendments and does not attempt to execute on-chain actions directly. The unauthorized-exposure rule applies the existing 100% fallback when RRC cannot be calculated, the Galaxy Warehouse change follows the Atlas path from interim deployment to normal risk-assessed operation, the Grove credit is being formalized explicitly in Atlas text before it is counted toward TRC, and the checklist edits point spell-process references at the registered checklist source of truth already recognized by the Atlas. The same-day forum posting and absence of public PR review reduce confidence, but I did not find a conflict with the Spirit of the Atlas or Universal Alignment in the disclosed text.

**Relevant sections:** A.1.11.2.1.1, A.1.11.2.1.2, A.1.11.2.1.3, A.1.11.2.2, A.1.11.2.4, A.1.10.2.3.2.2.2, A.2.2.10.1.1.2.3, A.3.2.1.1.3.2, A.3.2.1.2.1, A.1.10.2.5.1.3.2.0.6.1, A.0.1.1.18, A.1.6.2.1.1, A.1.6.2.2, A.1.6.6.1.2, A.1.6.6.2

## Risk Assessment

**Level:** medium

- The proposal introduces or formalizes economically material parameters: a 500,000,000 USD maximum Galaxy Warehouse exposure, a 2,528,000 USDS Grove prime-revenue credit, and a 4,900,000,000 GROVE token reward schedule over ten years.
- The forum origination post was created on Monday, June 29, 2026, the same day the poll opened, rather than by the Friday, June 26, 2026 08:00 UTC timing recommendation in A.1.11.2.2.
- As of June 29, 2026, `fetch-pr-reviews --repo sky-ecosystem/next-gen-atlas 270` returned no public reviews or PR comments, limiting independent scrutiny of the Atlas text changes.
- Cloaky's Ranked Delegate status is public, but Cloaky's AD Buffer balance at trigger time was not independently public; the trigger-threshold conclusion therefore relies on the official poll publication and the Atlas rule that the Core Facilitator confirms threshold satisfaction.
- The proposal edits Atlas documentation only and does not itself execute a spell or move funds on-chain, which bounds immediate implementation risk.

## Validation Checks

### Atlas Poll Validation

#### A.1.11.2.1.1 - Proposals In General

**Status:** OK

This is an Atlas Edit Weekly Cycle Proposal that bundles multiple amendments across Governance, Support, Stability, Protocol, and Agent Scope documents. A.1.11.2.1.1 explicitly allows multiple amendments to multiple Atlas components in a single weekly proposal. The portal summary, canonical proposal text, forum post, and PR body all describe the same five edit groups, and nothing in the disclosed text attempts to do more than amend Atlas documents through the weekly poll route.

**Evidence**

- Tool: fetch_proposal 1639. Poll 1639 is labeled 'Atlas Edit Weekly Cycle Proposal - June 29, 2026' and lists the same five edit groups as the proposal summary.
- Tool: curl forum JSON https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-29/27996.json. Post #1 by adamfraser on behalf of @atlas-axis repeats the same five edit groups and links PR #270.
- Tool: fetch_atlas_pr_diff 270. PR #270 body matches the five disclosed edit groups and shows only Atlas text changes.

**How To Verify**

1. Open the canonical proposal text and list the disclosed edit groups.
2. Open the forum thread and PR body and confirm the same edit groups are disclosed there.
3. Confirm the changes are Atlas text edits rather than direct on-chain actions.

#### A.1.11.2.1.2 - Origination Via Forum Post

**Status:** OK

The proposal was originated on the Sky Forum in the appropriate Atlas-edit proposal thread before the poll opened. Adam Fraser created the thread at 2026-06-29T14:23:56.009Z, described the proposal, and linked the Atlas PR. That satisfies the requirement that the author post the proposal on the forum and signal intent to submit it to the weekly cycle.

**Evidence**

- Tool: curl forum JSON https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-29/27996.json. Post #1 by adamfraser at 2026-06-29T14:23:56.009Z describes the proposal and links PR #270.
- Tool: fetch_proposal 1639. The canonical proposal text points to the same forum discussion URL.

**How To Verify**

1. Open the forum thread JSON or rendered page.
2. Confirm post #1 contains the proposal description and predates the poll start time.
3. Confirm the proposal text and linked PR match the portal listing.

#### A.1.11.2.1.3 - Triggering Requirement

**Status:** OK

The forum thread contains an explicit trigger reply from Cloaky at 2026-06-29T14:38:24.575Z saying 'I am hereby triggering this.' The active Atlas lists Cloaky as a current Level 1 Ranked Delegate. The Triggering Threshold equals one month of Level 3 Ranked Delegate compensation, which is 48,000 USDS per year or 4,000 USDS for one month. I did not find a public source exposing Cloaky's exact AD Buffer balance at trigger time, so the threshold portion of this check is an inference from the official poll having been published and from the Atlas rule that the Core Facilitator is responsible for confirming that the trigger requirements are met.

**Evidence**

- Tool: curl forum JSON https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-29/27996.json. Post #2 by cloaky at 2026-06-29T14:38:24.575Z says 'I am hereby triggering this.'
- Tool: read_atlas_section A.1.6.4.1.1.3.1. 'The current Level 1 Ranked Delegates are BLUE and Cloaky.'
- Tool: read_atlas_section A.1.6.4.4.2.1.1. Triggering Threshold equals one month of Level 3 compensation.
- Tool: read_atlas_section A.1.6.4.1.3.2. Level 3 Ranked Delegate budget is 48,000 USDS per year, implying a 4,000 USDS monthly trigger threshold.
- Tool: fetch_proposal 1639. The official poll was published on the voting portal after the trigger reply.

**How To Verify**

1. Open the forum thread and confirm Cloaky's trigger reply exists and predates poll start.
2. Open the active Atlas sections for current Level 1 Ranked Delegates and the Triggering Threshold formula.
3. If a public AD Buffer balance source becomes available, compare it against the 4,000 USDS threshold at trigger time.

#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK

The poll was published to the official voting portal and runs for the expected three-day window from 2026-06-29T16:00:00Z to 2026-07-02T16:00:00Z. The forum post timing is weaker than ideal: A.1.11.2.2 says the proposal should be posted by Friday at 08:00 UTC, but this thread was opened on Monday, June 29, 2026. I am not treating that as a process failure because the section uses 'should' rather than 'must', and the official Monday publication and full three-day window were still satisfied.

**Evidence**

- Tool: fetch_proposal 1639. Poll start is 2026-06-29T16:00:00.000Z and end is 2026-07-02T16:00:00.000Z.
- Tool: fetch_proposal 1639. Portal URL is https://vote.sky.money/polling/Qmd3gCcD.
- Tool: curl forum JSON https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-29/27996.json. Origination post timestamp is 2026-06-29T14:23:56.009Z.

**How To Verify**

1. Confirm the forum post timestamp relative to the poll start time.
2. Confirm the poll is on the official portal and lasts exactly three days.
3. Compare the actual posting date against the Friday 08:00 UTC recommendation in A.1.11.2.2.

#### A.1.11.2.4 - Minimum Positive Participation

**Status:** OK

The canonical proposal text uses the expected 480,000,000 SKY minimum positive participation threshold for Atlas Edit Weekly Cycle Proposals and states that a Yes victory also requires Yes votes to exceed No votes. That matches the active Atlas requirement.

**Evidence**

- Tool: fetch_proposal 1639. The proposal text states that Yes must exceed No and meet a 480,000,000 SKY minimum positive participation threshold.
- Tool: read_atlas_section A.1.11.2.4. 'Atlas Edit Weekly Cycle Proposals must have at least 480,000,000 SKY equivalents of Yes votes to be accepted.'

**How To Verify**

1. Open the canonical proposal text and find the Outcomes section.
2. Open A.1.11.2.4 in the active Atlas.
3. Confirm the threshold values match.

#### A.1.10.2.3.2.2.2 - Interim Deployments

**Status:** OK

The Galaxy Warehouse change is consistent with the Atlas path for graduating an Interim Deployment after full risk assessment. A.1.10.2.3.2.2.2.1.8 says that once an official Capital Ratio Requirement can be calculated, the Prime can request a subsequent Atlas Edit Proposal to lift testing constraints and reduce the RRC to the Atlas-calculated value. PR #270 does exactly that by deleting the Galaxy Warehouse Interim Deployment subsection and adding a new risk-framework entry with a 2% CRR and 500,000,000 USD maximum exposure.

**Evidence**

- Tool: read_atlas_section A.1.10.2.3.2.2.2.1.8. The Atlas authorizes a later Atlas Edit Proposal to lift interim testing constraints once full risk assessment is complete.
- Tool: fetch_atlas_pr_diff 270. The diff deletes A.6.1.1.2.2.6.1.3.1.9.2.2.5.1 - Interim Deployment and its child testing-parameter documents for Galaxy Warehouse.
- Tool: fetch_atlas_pr_diff 270. The diff adds A.3.2.2.1.1.1.1.3.10 - Galaxy Warehouse with 'The Instance Financial CRR for Galaxy Warehouse is 2%. The maximum exposure is 500,000,000 USD.'

**How To Verify**

1. Open A.1.10.2.3.2.2.2.1.8 in the active Atlas.
2. Review the PR diff for the deleted Galaxy Warehouse Interim Deployment subsection.
3. Review the PR diff for the new Galaxy Warehouse risk-framework entry.

#### A.2.2.10.1.1.2.3 - Instance Setup Deployments

**Status:** OK

The unauthorized-exposure edit is anchored to the part of the Atlas that requires a Prime Agent to prepare a pro-forma Required Risk Capital estimate approved by the Core Council Risk Advisor before an instance can move into normal operation. PR #270 defines an Unauthorized Exposure as an underlying asset not included in that approved pro-forma estimate. That is a coherent extension of the existing setup-deployment rule because it distinguishes risk-assessed exposure from newly introduced, unassessed exposure.

**Evidence**

- Tool: read_atlas_section A.2.2.10.1.1.2.3. The active Atlas requires a pro-forma Required Risk Capital estimate approved by the Core Council Risk Advisor before parameters are updated for normal operation.
- Tool: fetch_atlas_pr_diff 270. The new Unauthorized Exposures text explicitly cites A.2.2.10.1.1.2.3 as the reference point for approved pro-forma RRC estimates.

**How To Verify**

1. Open A.2.2.10.1.1.2.3 in the active Atlas.
2. Open the Unauthorized Exposures hunk in the PR diff.
3. Confirm the new text uses the approved pro-forma RRC estimate as the dividing line for authorized versus unauthorized exposure.

#### A.3.2.1.1.3.2 - Inability To Calculate Types Of RRC

**Status:** OK

The 100% Capital Ratio Requirement for unauthorized exposures is aligned with the Atlas rule that if relevant RRC cannot be calculated, the Instance Total RRC is 100%. PR #270 applies that full-reservation principle at the exposure level when a Prime has invested in an underlying lending-market asset that was not part of the approved pro-forma estimate and therefore has not been assessed. The proposal text also clarifies that an instance with only a fraction of capital in unauthorized exposures would not necessarily have a full 100% instance-wide CRR, because the instance CRR remains a capital-weighted aggregate.

**Evidence**

- Tool: read_atlas_section A.3.2.1.1.3.2. If relevant RRC cannot be calculated, the Instance Total RRC is 100%.
- Tool: fetch_atlas_pr_diff 270. The new A.3.2.2.1.1.1.1.4 - Unauthorized Exposures section says unassessed unauthorized exposures carry a 100% Capital Ratio Requirement and cites A.3.2.1.1.3.2.

**How To Verify**

1. Open A.3.2.1.1.3.2 in the active Atlas.
2. Open the Unauthorized Exposures hunk in PR #270.
3. Confirm the new text applies the 100% fallback to unassessed exposure rather than changing the fallback principle itself.

#### A.3.2.1.2.1 - Total Risk Capital Definition

**Status:** OK

The Grove prime-revenue credit is being formalized directly in Atlas text before it is counted toward Total Risk Capital. The active TRC definition says future capital commitments that are not yet formally codified within the Atlas cannot count toward TRC until formalization is complete. PR #270 uses that path: it records a 2,528,000 USDS amount owed from prior Monthly Settlement Cycle true-up and states that the credit counts toward Grove's TRC until payment through the next Monthly Settlement Cycle. That is a material economic change and one reason the overall risk is medium, but the route the proposal uses is explicit rather than hidden.

**Evidence**

- Tool: read_atlas_section A.3.2.1.2.1. Future capital commitments not yet formally codified within the Atlas cannot contribute toward TRC until such formalization is complete.
- Tool: read_atlas_section A.2.8.2.10.2. The current Atlas already contains Chronicle Point Reward compensation and settlement mechanics for Grove under Ecosystem Accord 10.
- Tool: fetch_atlas_pr_diff 270. A.2.8.2.10.2.2 is changed from Compensation Formula to Prime Revenue Credit and states that Grove is owed 2,528,000 USDS that counts toward TRC until paid through the next Monthly Settlement Cycle.

**How To Verify**

1. Open the active TRC definition in A.3.2.1.2.1.
2. Open the current Ecosystem Accord 10 substantive terms to see the existing Grove compensation framework.
3. Open the PR diff hunk for A.2.8.2.10.2.2 and confirm the 2,528,000 USDS credit language.

#### A.1.10.2.5.1.3.2.0.6.1 - Registered Spell Checklists

**Status:** OK

The checklist-link cleanup is a documentation-hardening change rather than a process rewrite. The active Atlas already registers the Core Spell Crafter Mainnet Workflow and Core Spell Reviewer Mainnet Checklist as official checklist sources. PR #270 replaces scattered inline GitHub URLs in the spell-process documents with cross-references back to that registered checklist section. That reduces the chance of stale or inconsistent inline links without changing the underlying spell-review process.

**Evidence**

- Tool: read_atlas_section A.1.10.2.5.1.3.2.0.6.1. The active Atlas lists the registered Core Spell Crafter Mainnet Workflow and Core Spell Reviewer Mainnet Checklist URLs.
- Tool: fetch_atlas_pr_diff 270. The A.1.10 spell-process edits replace inline checklist URLs with references to the registered checklist section.

**How To Verify**

1. Open the active Registered Spell Checklists section.
2. Review the spell-process hunks in PR #270.
3. Confirm the new references point back to the registered checklist section rather than altering spell-process requirements.

### Atlas Vote Recommendation

#### A.0.1.1.18 - Aligned Delegate (AD)

**Status:** OK

A YES recommendation is consistent with the AD duty to uphold the Spirit of the Atlas when the proposal's core implications are understood and no material mismatch is found. The disclosed changes are concrete and bounded: unassessed lending-market exposures get 100% capital treatment, Galaxy Warehouse graduates out of interim deployment into a 2% / 500,000,000 USD risk-framework slot, Grove receives an explicitly codified 2,528,000 USDS TRC credit until next settlement, GROVE rewards are scheduled over ten years, and spell checklist links are normalized to the registered source of truth. Those are meaningful governance implications, but they are visible enough to support an accountable YES rather than a blind vote.

**Evidence**

- Tool: fetch_proposal 1639. The canonical proposal text and summary disclose all five core edit groups.
- Tool: fetch_atlas_pr_diff 270. The diff text shows the concrete Atlas language implementing each disclosed edit group.

**How To Verify**

1. List the proposal's core mechanisms from the canonical text.
2. Match each mechanism to the relevant PR diff hunk.
3. Confirm that a YES vote would be grounded in those concrete implications rather than in portal headline text alone.

#### A.1.6.2.1.1 - Excessive Abstention

**Status:** OK

Abstention is not the better fit here. I found enough public evidence to take a reasoned position, and the proposal does not present a conflict of interest that would justify abstaining. The review record is imperfect, which is why the assessment is medium rather than high, but the evidence set is still sufficient to support a YES/NO judgment rather than defaulting to Abstain.

**Evidence**

- Tool: fetch_proposal 1639. Poll metadata, canonical text, and discussion link were available.
- Tool: fetch_atlas_pr_diff 270. The full Atlas diff was available for review.
- Tool: curl forum JSON https://forum.skyeco.com/t/atlas-edit-weekly-cycle-proposal-week-of-2026-06-29/27996.json. Forum origination and trigger evidence were publicly visible.

**How To Verify**

1. Review the available public evidence set for the proposal.
2. Ask whether any unresolved gap prevents understanding the proposal's core implications.
3. Use Abstain only if the evidence set is too weak for a reasoned YES/NO recommendation or if a conflict exists.

#### A.1.6.2.2 - Aligned Delegate Communication Responsibilities

**Status:** OK

The recommendation reasoning is substantive enough to support a compliant vote explanation under A.1.6.2.2. It identifies the proposal's core mechanisms, states a reasoned YES basis, and addresses substantive aspects of the proposal including implementation path, economic parameters, disclosure quality, and governance-process risk. The explanation is not limited to a conclusion or slogan.

**Evidence**

- Draft recommendation reasoning explains the five substantive edits and why they support YES despite medium risk.
- Draft risk assessment identifies concrete benefits and risks, including same-day forum posting, missing public PR reviews, material economic parameters, and bounded implementation scope.

**How To Verify**

1. Read the recommendation reasoning line by line.
2. Confirm it explains the proposal's mechanisms rather than only the preferred vote.
3. Confirm it addresses at least one substantive aspect such as benefits, risks, implementation, or alignment.

#### A.1.6.6.1.2 - Tier 2 (Integrity) Breaches

**Status:** OK

Nothing in this review suggests that a YES vote would rest on dishonesty, undisclosed compensation, collusion, or other integrity-breach conduct described in A.1.6.6.1.2. The risk is medium because public review depth is limited, not because the proposal appears deceptive. The recommendation remains contingent on the disclosed proposal text and PR diff as reviewed here.

**Evidence**

- Tool: fetch_proposal 1639. The portal and canonical text are explicit about the proposal scope.
- Tool: fetch_atlas_pr_diff 270. The PR diff shows the Atlas language implementing the disclosed scope.
- Tool: fetch_pr_reviews --repo sky-ecosystem/next-gen-atlas 270. No public review events were found, which reduces confidence but is not evidence of integrity breach by itself.

**How To Verify**

1. Check whether the proposal text or diff appears materially misleading relative to the vote recommendation.
2. Check whether any evidence suggests undisclosed compensation, collusion, or dishonest framing.
3. If such evidence appears later, reassess whether supporting the proposal would remain defensible.

#### A.1.6.6.2 - Voting Estoppel Rule

**Status:** OK

Because a YES vote estops later claims of ignorance, the recommendation must be tied to the proposal's actual implications. This review covered the material implications that a YES would affirm: unassessed lending-market exposures receive 100% exposure-level capital treatment, Galaxy Warehouse moves from 100% interim status to a 2% / 500,000,000 USD risk-framework entry, Grove gets a 2,528,000 USDS TRC credit until next settlement, GROVE rewards are scheduled at 4,900,000,000 total tokens over ten years, and spell checklist references are moved to the Atlas-registered checklist source. Those implications are meaningful but sufficiently explicit to support a YES with a medium assessment.

**Evidence**

- Tool: fetch_proposal 1639. The proposal text lists all five change groups in plain language.
- Tool: fetch_atlas_pr_diff 270. The diff text gives the exact Atlas language for each disclosed implication.
- Tool: read_atlas_section A.1.6.6.2. The active Atlas warns that an AD who votes in favor is deemed to have read and understood the key governance implications.

**How To Verify**

1. Write down the concrete implications a YES vote would affirm.
2. Match each implication to the canonical text and PR diff.
3. Confirm there is no material implication being ignored before finalizing a YES position.

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote YES. The proposal is procedurally coherent enough to support, and the disclosed Atlas diff is understandable and bounded. Substantively, it does five clear things: it applies a 100% exposure-level Capital Ratio Requirement to unauthorized lending-market exposures, graduates Galaxy Warehouse from 100% interim status into a 2% / 500,000,000 USD risk-framework entry, formalizes a 2,528,000 USDS Grove credit toward TRC until the next Monthly Settlement Cycle pays it, specifies a 4,900,000,000 GROVE token reward schedule for USDS users over ten years, and replaces brittle inline checklist URLs with references to the registered checklist source of truth. The main negatives are reduced pre-vote review time, no public PR review evidence, and limited independent process evidence on Cloaky's buffer balance. Those issues justify a medium assessment, but they do not amount to a material disclosure mismatch, Atlas-process failure, or substantive contradiction that would justify NO or ABSTAIN.

## LLM Usage

- **Provider/Model:** openai / gpt-5.4
- **Tokens:** 2,685,027 in / 28,941 out / 16,131 reasoning / 2,730,099 total
- **Cache:** 2,401,792 read / 0 write
- **Cost:** $1.9846 USD estimated
- **Pricing:** openai-api-pricing-2026-06-10-standard-short-context
