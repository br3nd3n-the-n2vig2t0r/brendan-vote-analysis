# Analysis: Atlas Edit Weekly Cycle Proposal - July 13, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-07-13T17:57:17.929Z | **Atlas:** 2026-07-13
**Atlas interpretation:** version 2026-07-13 | subtrees read: A.0, A.1.1, A.1.2, A.1.6, A.1.11 | derived in isolated context Codex fresh isolated subagent:/root/atlas_interpretation
**Phase 3 review:** APPROVED | checks reviewed: 13

## Summary

Poll 1641 asks governance to approve Atlas PR 277, a ten-part edit covering the Monthly Settlement Cycle, Aligned Delegate vote timeliness, Genesis Capital phase-out language, the Sky Frontier Foundation multisig, JAAA Avalanche CRR, Osero SparkLend USDS limits, spell-validation communications, the Risk Capital Rental Primitive, stale URLs, and relocation of SkyLink Bridges. The Forum and PR summaries match, all 224 changed Atlas section views across five review batches were covered, and the poll is configured for the required three-day window and 480,000,000 SKY minimum positive participation. The trigger-time rank and buffer check relies on the user's explicit consent to use June month-end data as an assumption because no July tracker or explicit Core Facilitator confirmation is available.

## Atlas Alignment

**Assessment:** aligned

The proposal uses the Atlas Edit Weekly Cycle Governance Poll path and the complete PR diff corresponds to the ten disclosed changes without detected exclusivity language, undisclosed parameter changes, or substantive conflict with Universal Alignment. The changes clarify governance and settlement procedures, record or update operational facts and links, broaden a documented capital primitive, set disclosed risk parameters, and relocate bridge documentation without changing its substantive content. GitHub history establishes that PR 277 had a single commit before the trigger and that the Monday community poll file remained byte-identical through analysis. Process evidence is complete except for the explicitly consented BLUE trigger-time rank and buffer assumption; poll acceptance and direct editing remain conditional on the active vote's final outcome.

**Relevant sections:** A.1.11.2, A.1.11.2.1.1, A.1.11.2.1.2, A.1.11.2.1.3, A.1.11.2.2, A.1.11.2.4, A.1.11.2.5.1, A.1.11.2.5.2, A.1.6.2.1.1, A.1.6.2.2

## Risk Assessment

**Level:** medium

- PR 277 is broad: 318 files, 224 changed Atlas section views, 991 additions, and 1,033 deletions.
- The edit reduces JAAA on Avalanche Instance Financial CRR from 2.1% to 1.6% and adds Osero SparkLend USDS Maximum Exposure of 5,000,000 USDS with a 100% Capital Ratio Requirement.
- The spell-validation communication edit removes a distinct potentially-malicious-Core-Facilitator escalation route in favor of public Sky Forum reporting.
- Trigger-time BLUE rank and AD Buffer evidence uses an explicitly consented assumption based on June month-end data; July tracker data and an explicit Core Facilitator confirmation were unavailable.
- The poll remains active, so the 480,000,000 SKY acceptance threshold and subsequent direct Atlas edit are not yet resolved.

## Validation Checks

### Atlas Poll Validation

#### A.1.11.2 - Atlas Edit Weekly Cycle

**Status:** OK

> This Section defines the Atlas Edit Weekly Cycle which provides a predictable framework for weekly edits to the Atlas. The Atlas Edit Weekly Cycle is implemented via Governance Polls.

Poll 1641 is a single-choice Governance Poll implementing direct Atlas edits through PR 277. GitHub's PR commit history returns exactly one commit, 57b87141534078f1eed26f0960fc5d3b873a8b50 at 2026-07-11T19:26:44Z, before BLUE's 2026-07-12T13:26:10.733Z trigger; fetch-atlas-pr-diff pinned the same commit as the analysis head. The trigger-time and analysis-time implementing PR refs are therefore identical.

**Evidence**

- fetch-proposal 1641: active Governance Poll at https://vote.sky.money/polling/Qmd3yk9L linking https://github.com/sky-ecosystem/next-gen-atlas/pull/277
- evidence-github-timeline.json: PR 277 commit API returned exactly one commit, 57b87141534078f1eed26f0960fc5d3b873a8b50 at 2026-07-11T19:26:44Z, before the trigger
- fetch-atlas-pr-diff 277: base b943bc3b66a08f1284ecb8cb8a22ce74d3a46abb; head 57b87141534078f1eed26f0960fc5d3b873a8b50; unified diff SHA-256 6ffd96054666a0638512d043835dd286773056d9aa23316aa2639947eded94ed
- read-atlas-pr-diff-batch 277 1 through 5: all 224 changed Atlas section views covered

#### A.1.11.2.1.1 - Proposals In General

**Status:** OK

> Atlas Edits must always adhere to the Spirit of the Atlas and remain within the bounds of Universal Alignment.

The complete proposed diff was reviewed against Universal Alignment and the Spirit of the Atlas. It corresponds to the ten disclosed changes and contains no detected loophole exploitation, hidden substantive item, or scope-boundary abuse. The SkyLink material is relocated with identifiers and cross-references adjusted while its operative content remains unchanged; other changes are disclosed procedural, factual, parameter, communication, URL, or primitive-generalization edits.

**Evidence**

- read-atlas-section A.0.1.1.4 and A.0.1.1.9: Universal Alignment and spirit-versus-letter definitions
- fetch-atlas-pr-diff 277: 318 files, 991 additions, 1,033 deletions, 224 changed Atlas sections
- read-atlas-pr-diff-batch 277 1 through 5: complete review; batch SHA-256 values 896f8f240ad6786bf2edbe07be8f823bc7bb0b2a00b4dade002b32f7a20cda49, 28f516ce571c7fb7d3b6916a491c4264de70e2137942dbe2b4dce22b513a6069, 1dc8229fc83aef75367d42bf2d403cc7fff440731683bbc453fde6a3c4fc81b4, ca6e20e5db2144e4e0e44d6fe66007cb73e224b2777c52cb5ba06ebf2c134103, 5eed72a4fd50fbd0b03b605b07c131f181a92301dedbefdcdf515c89e22a8515
- diff-sources portal summary versus Forum summary: all ten topics correspond; the Forum supplies the disclosed parameters and mechanisms
- diff-sources Forum summary versus PR summary: Sources are identical

#### A.1.11.2.1.2 - Origination Via Forum Post

**Status:** OK

> The Author of an Atlas Edit Weekly Cycle Proposal (also "Weekly Cycle Proposal" or "Proposal") must post the Proposal in the Sky Forum in the appropriate category and signal their intent to submit the Proposal to the Weekly Cycle.

The author posted the proposal in the Sky Forum's Sky Core category with the atlas-edit-weekly-proposal tag and expressly submitted it to the Atlas Edit Weekly Cycle before the vote.

**Evidence**

- fetch-forum-thread topic 28043: post 1 by adamfraser at 2026-07-11T19:39:29.932Z, version 1, states 'we are submitting the Atlas Edit Weekly Cycle proposal below' and links PR 277
- evidence-forum-metadata.json: topic API category_id 92; categories API identifies 92 as Sky Core; tag atlas-edit-weekly-proposal
- fetch-proposal 1641: poll opened 2026-07-13T16:00:00Z

#### A.1.11.2.1.3 - Triggering Requirement

**Status:** ASSUMPTION

> An Atlas Edit Weekly Cycle Proposal (also "Weekly Cycle Proposal" or "AEW Proposal") can proceed to a vote only if it is triggered by a Ranked Delegate whose AD Buffer contains at least the Triggering Threshold (see [A.1.6.4.4.2.1.1 - Triggering Threshold](2c2b201e-b95f-4852-8e76-6dfe4c3c6a4f)) at the time of triggering the Proposal. The Core Facilitator is responsible for confirming that these requirements are met.

Condition resolution: BLUE triggered at 2026-07-12T13:26:10.733Z. The Triggering Threshold was 4,000 USDS. The latest available Core Facilitator tracker shows BLUE was Level 1 and held 33,333 USDS at 2026-06-30, well above the threshold, but no July tracker tab or explicit Core Facilitator confirmation was available. With the user's explicit consent, the June month-end evidence is accepted as good enough for BLUE's trigger-time Ranked Delegate and buffer status. Poll publication on behalf of Ranked Delegate BLUE is corroborating but not treated as exact balance evidence.

**Evidence**

- fetch-forum-thread topic 28043: BLUE trigger reply at 2026-07-12T13:26:10.733Z
- read-atlas-section A.1.6.4.1.3.2 and A.1.6.4.4.2.1.1: Level 3 annual budget 48,000 USDS, making the one-month Triggering Threshold 4,000 USDS
- fetch-ad-compensation-sheet 2026-06 --tab daily-data --date 2026-06-30: BLUE rank 2 with 2,084,657,111 delegated SKY-equivalent units; snapshot SHA-256 b139d0396b248f5fd7e418a69ca9b73f64a20f38ddbd21226f459e18efd5dd7c
- fetch-ad-compensation-sheet 2026-06 --tab compensation: BLUE Level 1 for 30 days and 33,333 USDS scaled buffer contents post payment; snapshot SHA-256 43df966bad5370e641a4b1e21580f67f72567afb08e5ad0ec0b5e9b8d7373820
- fetch-ad-compensation-sheet 2026-07 attempts: no July 2026 tracker tabs available
- fetch-proposal 1641: community poll file says the Core Facilitators placed the poll on behalf of Ranked Delegate BLUE
- Explicit user consent: 'Accept June data as good enough' at 2026-07-13T17:42:14Z

**How To Verify**

1. When July 2026 tracker data becomes available, verify BLUE's rank and AD Buffer at or immediately before 2026-07-12T13:26:10.733Z.
2. Check the Forum thread or Core Facilitator records for an explicit confirmation of the trigger requirements.

#### A.1.11.2.1.3 - Triggering Requirement

**Status:** OK

> To trigger a Proposal, the Ranked Delegate must post a reply to the Author's Weekly Cycle Proposal on the Forum. The Ranked Delegate’s post should signal their intent to trigger the Weekly Cycle Proposal.

Where more than one Ranked Delegate posts an intention to trigger a Weekly Cycle Proposal, the first Ranked Delegate to post a reply to the Author’s Forum post shall be treated as the triggering Ranked Delegate.

BLUE's unedited post 2 is a reply in the author's proposal thread and clearly signals intent to trigger. It is the only trigger reply, so it is the first qualified trigger.

**Evidence**

- fetch-forum-thread topic 28043: post 2 by BLUE at 2026-07-12T13:26:10.733Z, version 1, states 'I am hereby triggering this AEW Proposal.'
- fetch-forum-thread topic 28043: complete two-post thread, with no competing trigger reply

#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK

> An Atlas Edit Weekly Cycle Proposal should be posted to the Forum by Friday at 8:00 am UTC to ensure the Core Facilitator has sufficient time to prepare the needed polls for the following Monday.

The Forum proposal was posted after the recommended Friday 08:00 UTC preparation target, at Saturday 19:39 UTC. However, the decision rule requires a finding only when the late post impaired the prescribed preparation window. Path-specific GitHub history shows the community poll file was created at 11:30:42 UTC Monday, and the portal poll opened at 16:00 UTC Monday, so no preparation impairment is evidenced.

**Evidence**

- fetch-forum-thread topic 28043: proposal created 2026-07-11T19:39:29.781Z
- evidence-github-timeline.json: path-specific commit history identifies creation commit d875a427fa6755d471d89b5657c5741ed2b25665 at 2026-07-13T11:30:42Z
- read-github-path sky-ecosystem/polls d875a427fa6755d471d89b5657c5741ed2b25665 2026/2026-07-13-Atlas-edit-weekly-cycle-proposal.md: immutable created file, content SHA-256 5ec16a1a9ea737ffb92c1c557684d6e3f421e6cbdeda9e5db14b69b5e64e8a3b
- fetch-proposal 1641: poll opened Monday 2026-07-13T16:00:00Z

#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK

> Every Monday, the Atlas Edit Weekly Cycle is carried out via Governance Polls. The Core Facilitator must publish the set of Governance Polls to the community Github and the official Voting Portal.

The poll was published on Monday to the community GitHub and official Voting Portal. Path-specific history identifies the file's single creation commit at 11:30:42 UTC Monday. The creation and analysis-time versions have the same object SHA and content SHA-256, and diff-github-path reports an empty diff. The immutable GitHub poll file and fetched portal proposal text correspond in title, summary, options, dates, 480,000,000 SKY victory threshold, discussion URL, PR 277 link, and ten disclosed edits.

**Evidence**

- evidence-github-timeline.json: path history has one creation commit, d875a427fa6755d471d89b5657c5741ed2b25665 at 2026-07-13T11:30:42Z
- read-github-path at d875a427fa6755d471d89b5657c5741ed2b25665: object 7e6b4872f03e3587e88661e6e342f683beef8e43 and content SHA-256 5ec16a1a9ea737ffb92c1c557684d6e3f421e6cbdeda9e5db14b69b5e64e8a3b
- diff-github-path d875a427fa6755d471d89b5657c5741ed2b25665 to 3276a771548e776e3d44fe1c5a2eee13c3d78796: identical true, empty diff SHA-256 e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
- fetch-proposal 1641: official portal publication opened 2026-07-13T16:00:00Z with matching full proposal text

#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK

> The Polls run for three days. Successful polls trigger direct edits to the Atlas.

Condition resolution: the active poll is configured from 2026-07-13T16:00:00Z through 2026-07-16T16:00:00Z, exactly three days. Its planned successful outcome is direct merger of PR 277 into the Atlas. Because the poll remains active, the actual direct edit is not yet due and is not claimed as completed.

**Evidence**

- fetch-proposal 1641: active status, start 2026-07-13T16:00:00Z, end 2026-07-16T16:00:00Z
- fetch-proposal 1641 Outcomes: successful poll causes the associated Pull Request to be merged into the Atlas
- fetch-atlas-pr-diff 277: PR state open and not merged at analysis time

#### A.1.11.2.4 - Minimum Positive Participation

**Status:** N/A

> Atlas Edit Weekly Cycle Proposals must have at least 480,000,000 SKY equivalents of Yes votes to be accepted.

The acceptance condition is not yet applicable because the poll is active until 2026-07-16T16:00:00Z. The poll configuration correctly requires Yes plurality and at least 480,000,000 SKY. No claim of acceptance is made before final vote totals exist.

**Evidence**

- fetch-proposal 1641: status active and end 2026-07-16T16:00:00Z
- fetch-proposal 1641 victory_conditions: plurality AND comparison >= 480000000, default No

**How To Verify**

1. After poll closure, verify final Yes votes exceed No votes and are at least 480,000,000 SKY before treating PR 277 as accepted.

#### A.1.11.2.5.1 - Language Disallowing Simultaneous Edits Not Allowed

**Status:** OK

> Atlas Edit Weekly Cycle Proposals cannot include language that aims to prevent other Atlas Edit Weekly Cycle Proposals from editing the same component of the Atlas within the same Governance Cycle.

Neither the canonical Forum proposal nor the complete implementing diff contains language aimed at preventing another Atlas Edit Weekly Cycle Proposal from editing the same component in this cycle.

**Evidence**

- fetch-forum-thread topic 28043: complete unedited proposal text
- read-atlas-pr-diff-batch 277 1 through 5: complete diff coverage
- Targeted search of the composed atlas.diff and Forum summary for simultaneous/prevent other/exclusive/exclusivity returned no matches

#### A.1.11.2.5.2 - Simultaneous Edit Reconciliation Process Definition

**Status:** N/A

> Where voters approve multiple Atlas Edit Weekly Cycle Proposals that seek to edit the same component or components of the Atlas within the same Governance Cycle, the process described below must be followed.

Condition resolution: all seven governance API pages covering 136 polls were reviewed, and poll 1641 is the only poll with a July 13 start date or matching July 13 Atlas Edit Weekly Cycle title. No second same-cycle proposal exists, so no approved overlap can presently arise and reconciliation is inapplicable. The condition should be reassessed if another same-cycle proposal is introduced or identified.

**Evidence**

- evidence-same-cycle-polls.json: all seven vote.sky.money governance API pages and 136 polls reviewed; only poll 1641 matched the July 13 cycle date/title
- monitor rerun after evidence gathering: no new governance activity detected
- fetch-atlas-pr-diff 277: the sole implementing Atlas PR identified by poll 1641

**How To Verify**

1. Before final implementation, confirm no additional proposal in the same Governance Cycle was approved with overlapping Atlas components.

### Atlas Vote Recommendation

#### A.1.6.2.1.1 - Excessive Abstention

**Status:** OK

> Casting an Abstain vote is appropriate when an Aligned Delegate has a conflict of interest or lacks sufficient expertise on a specialized matter, but abstaining should be the exception rather than the norm.

The evidence supports a substantive YES rather than Abstain. No conflict of interest or lack of expertise on a specialized matter has been identified. The remaining trigger uncertainty is handled through explicit assumption consent and human review, not by routine abstention.

**Evidence**

- fetch-proposal 1641 and fetch-forum-thread topic 28043: proposal mechanisms and process provenance
- fetch-atlas-pr-diff 277 plus read-atlas-pr-diff-batch 277 1 through 5: complete implementing content review
- diff-sources Forum summary versus PR summary: identical
- Explicit assumption consent for check-004

#### A.1.6.2.2 - Aligned Delegate Communication Responsibilities

**Status:** OK

> Aligned Delegates must provide substantive reasoning when explaining their votes. A compliant vote explanation must:

1. Demonstrate understanding of the proposal's core mechanisms or changes;
2. Articulate a reasoned basis for the vote position; and
3. Address at least one substantive aspect of the proposal (benefits, risks, implementation, or alignment with ecosystem goals).

Vote explanations must be posted within one (1) week of the end of the voting period for the applicable vote.

The recommendation reasoning demonstrates the ten core changes, explains the YES basis, and addresses substantive implementation, risk, and alignment considerations. It is prepared during the voting period for posting no later than one week after the 2026-07-16T16:00:00Z close, i.e. by 2026-07-23T16:00:00Z. Analysis does not publish it.

**Evidence**

- Draft summary and recommendation reasoning cite the complete poll, Forum, PR diff, parameters, risks, process assumption, and acceptance condition
- proposal compliance.json: explanationDeadline 2026-07-23T16:00:00.000Z
- fetch-proposal 1641: voting end 2026-07-16T16:00:00Z

## Assumption Consent Audit

### Atlas Poll Validation

#### A.1.11.2.1.3 - Triggering Requirement

**Consented:** 2026-07-13T17:42:14Z

Accept June data as good enough

## Recommendation

**Position:** YES
**Assessment:** Medium

Support the proposal because the pinned PR 277 diff implements the ten changes disclosed consistently in the Voting Portal, Sky Core Forum thread, community poll file, and PR body. GitHub history shows PR 277's sole commit predates BLUE's trigger and equals the analysis head, while the Monday community poll file is byte-identical from its 11:30:42 UTC creation commit through analysis. The edits improve process documentation and operational references, add clearly disclosed parameters and a canonical multisig address, generalize the risk-capital rental framework, and move SkyLink bridge documentation without substantive content changes. No hidden parameter mismatch, simultaneous-edit restriction, or Universal Alignment conflict was found in the complete five-batch diff review. This recommendation is subject to human review because exact July 12 trigger-time eligibility is supported by the user's explicit assumption that BLUE's June 30 Level 1 status and 33,333 USDS buffer remained good enough for the 4,000 USDS threshold. The active poll must still exceed No votes and obtain at least 480,000,000 SKY in Yes votes before PR 277 may be merged.

## LLM Usage

- **Provider/Model:** openai / gpt-5.6-sol
- **Tokens:** 9,812,245 in / 28,065 out / 6,648 reasoning / 9,846,958 total
- **Cache:** 9,450,240 read / 0 write
