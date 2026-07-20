# Analysis: Atlas Edit Weekly Cycle Proposal - July 20, 2026

**Recommendation:** YES (Medium assessment)
**Analyzed:** 2026-07-20T22:28:56.282Z | **Atlas:** 2026-07-16
**Atlas interpretation:** version 2026-07-16 | subtrees read: A.0, A.1.1, A.1.2, A.1.6, A.1.11, A.1.10.2.5.2, A.2.2.5.1.2.3, A.2.2.5.1.2.4, A.2.8.2.2.2.3.3, A.3.1.2.2.1, A.3.2.1.1.1, A.3.2.1.2.2.1.1.2, A.3.2.2.4.2.3.2, A.3.2.2.4.2.3.3.1, A.6.1.1.1.2.6.1.3.1.12, A.6.1.1.2.2.6.1.3.1.15 | derived in isolated context Codex collaboration sub-agent:/root/atlas_interpret_1642

## Summary

Poll 1642 asks voters to approve Atlas PR #280, which reduces the Sky Spread to 0%, replaces Treasury Bill Rate references with SOFR in two mechanisms, promotes Agent Foundation and Development Company entries into standard parameters, corrects one RRC/CRR label, renames SEJRC to PEJRC, renames four Spark Paxos transfer instances, and repoints operational-reference links to Soter Labs. The poll is open from 2026-07-20 16:00 UTC through 2026-07-23 16:00 UTC.

## Atlas Alignment

**Assessment:** aligned

The portal, canonical poll document, forum proposal, and complete 85-file implementing diff describe the same six edits. The edits preserve Agent associations and Paxos parameters, confine the RRC/CRR correction to the ratio sentence, consistently update rate formulas and terminology, and remain within the affected Scope artifacts. Weekly-cycle process evidence is complete except for the explicitly consented Cloaky trigger-state and Core Facilitator confirmation assumption.

**Relevant sections:** A.1.11.2.1.1, A.1.11.2.1.2, A.1.11.2.1.3, A.1.11.2.2, A.1.6.2.2, A.3.2.2.4.2.3.3.1, A.2.2.5.1.2.3, A.2.2.5.1.2.4, A.3.2.1.1.1, A.3.2.1.2.2.1.1.2, A.6.1.1.1.2.6.1.3.1.12, A.1.10.2.5.2

## Risk Assessment

**Level:** medium

- The change spans 85 Atlas files and modifies rate definitions and formulas as well as structural and terminology references.
- The July 2026 AD tracker tabs and an explicit Core Facilitator trigger confirmation were unavailable; trigger eligibility is covered by explicit user consent to a named assumption.
- The forum proposal missed the advisory Friday 08:00 UTC preparation target by 7 hours 47 minutes, although the trigger, review discussion, canonical publication, and Monday poll publication all completed before the vote opened.
- PR #280 is still open and should be merged only if the poll satisfies plurality and the 480,000,000 SKY Minimum Positive Participation threshold.

## Validation Checks

### Atlas Poll Validation

<!-- validation-check:check-001 -->
#### A.1.11.2.1.1 - Proposals In General

**Status:** OK — Portal metadata and the canonical poll document correspond on title, six-edit scope, options, dates, and linked implementation.

<!-- validation-check:check-002 -->
#### A.1.11.2.1.1 - Proposals In General

**Status:** OK — All six canonical amendments are implemented across the complete 85-file PR diff without an undisclosed semantic change.

<!-- validation-check:check-003 -->
#### A.0.1.1.15 - Scope Alignment Artifact (Scope Artifact)

**Status:** OK — The edits remain within their containing Scope functions and do not transfer authority across Scope boundaries.

<!-- validation-check:check-004 -->
#### A.1.11.2.1.2 - Origination Via Forum Post

**Status:** OK — The author posted the proposal in its Sky Forum thread and expressly submitted it to the Weekly Cycle before publication.

<!-- validation-check:check-005 -->
#### A.1.11.2.1.3 - Triggering Requirement

**Status:** ASSUMPTION — Trigger eligibility is accepted by explicit user consent because July rank/buffer evidence and an explicit CF confirmation are unavailable.

> An Atlas Edit Weekly Cycle Proposal (also "Weekly Cycle Proposal" or "AEW Proposal") can proceed to a vote only if it is triggered by a Ranked Delegate whose AD Buffer contains at least the Triggering Threshold (see [A.1.6.4.4.2.1.1 - Triggering Threshold](2c2b201e-b95f-4852-8e76-6dfe4c3c6a4f)) at the time of triggering the Proposal.

Cloaky's unedited trigger reply was posted at 2026-07-17T17:03:49.653Z. The active Triggering Threshold is one month of the Level 3 annual budget: 48,000 / 12 = 4,000 USDS. June 30 fallback evidence ranked cloaky first and the June compensation snapshot recorded a 33,333 USDS buffer, but no July 2026 Compensation or Daily Data tab exists. The user explicitly accepted the named assumption that Cloaky remained ranked with at least 4,000 USDS at trigger time and that poll publication reflects Core Facilitator confirmation.

**Evidence**

- fetch-forum-thread topic 28062 post #3, cloaky, 2026-07-17T17:03:49.653Z: I am hereby triggering this.
- read-atlas-section A.1.6.4.4.2.1.1 and A.1.6.4.1.3.2: threshold equals one month of a 48,000 USDS annual Level 3 budget, or 4,000 USDS
- fetch-ad-compensation-sheet 2026-06: Cloaky Level 1, 33,333 USDS post-payment buffer at June month end, snapshot SHA-256 43df966bad5370e641a4b1e21580f67f72567afb08e5ad0ec0b5e9b8d7373820
- fetch-ad-compensation-sheet 2026-06 --tab daily-data --date 2026-06-30: cloaky rank 1, snapshot SHA-256 b139d0396b248f5fd7e418a69ca9b73f64a20f38ddbd21226f459e18efd5dd7c
- July 2026 compensation and daily-data requests both returned no matching tab
- Explicit user consent recorded at 2026-07-20T22:26:03Z

**How To Verify**

1. When the July 2026 tracker is published, verify Cloaky's Ranked Delegate status and AD Buffer on 2026-07-17.
2. Locate or request the Core Facilitator's contemporaneous confirmation of the trigger requirements.

<!-- validation-check:check-006 -->
#### A.1.11.2.1.3 - Triggering Requirement

**Status:** OK — Cloaky triggered by replying directly in the author's proposal thread and identified the exact proposal.

<!-- validation-check:check-007 -->
#### A.1.11.2.1.3 - Triggering Requirement

**Status:** N/A — Only one Ranked Delegate posted an intention to trigger, so first-trigger ordering does not apply.

<!-- validation-check:check-008 -->
#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK — The post missed the advisory Friday 08:00 UTC target, but concrete timeline evidence shows no impairment to trigger, review, or Monday publication.

<!-- validation-check:check-009 -->
#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK — The same poll content was published Monday to the community polls repository and official Voting Portal.

<!-- validation-check:check-010 -->
#### A.1.11.2.2 - Preparation And Publication of Governance Poll

**Status:** OK — The poll window is exactly three days: July 20 16:00 UTC through July 23 16:00 UTC.

<!-- validation-check:check-011 -->
#### A.1.11.2.5.1 - Language Disallowing Simultaneous Edits Not Allowed

**Status:** OK — Neither the canonical proposal nor PR #280 attempts to prevent other same-cycle edits.

<!-- validation-check:check-012 -->
#### A.1.11.2.5.2 - Simultaneous Edit Reconciliation Process Definition

**Status:** N/A — Reconciliation is not yet applicable because poll 1642 is active and therefore cannot yet be one of multiple approved overlapping proposals.

<!-- validation-check:check-013 -->
#### A.1.11.2.5.2 - Simultaneous Edit Reconciliation Process Definition

**Status:** N/A — No approved same-cycle conflicting edit exists while poll 1642 remains active, so voter-facing conflict reconciliation is not applicable.

### Atlas Vote Recommendation

<!-- validation-check:check-014 -->
#### A.1.6.2.1.1 - Excessive Abstention

**Status:** OK — The complete evidence review supports a YES/NO determination; no conflict of interest or residual expertise gap requires abstention.

<!-- validation-check:check-015 -->
#### A.1.6.2.2 - Aligned Delegate Communication Responsibilities

**Status:** OK — The prepared recommendation explains all six changes, its YES basis, material benefits, implementation risks, and the trigger assumption.

### Atlas Poll Validation

<!-- validation-check:check-016 -->
#### A.3.2.2.4.2.3.3.1 - Sky Spread

**Status:** OK — The diff sets Sky Spread to 0% and replaces Treasury Bill Rate with SOFR consistently in the disclosed dependent formulas.

<!-- validation-check:check-017 -->
#### A.2.2.5.1.2.3 - Agent Foundation

**Status:** OK — Foundation entries are promoted to standard parameters without changing the associated entities.

<!-- validation-check:check-018 -->
#### A.2.2.5.1.2.4 - Agent Development Company

**Status:** OK — Development Company entries are promoted to standard parameters without changing the associated entities.

<!-- validation-check:check-019 -->
#### A.3.2.1.1.1 - Capital Ratio Requirement

**Status:** OK — The single 100% ratio label changes from Instance Total RRC to Instance Total CRR while monetary RRC terms remain unchanged.

<!-- validation-check:check-020 -->
#### A.3.2.1.2.2.1.1.2 - Prime-External Junior Risk Capital (SEJRC)

**Status:** OK — SEJRC is consistently renamed to PEJRC across titles, definitions, formulas, reports, links, and implementation prose without changing meaning.

<!-- validation-check:check-021 -->
#### A.6.1.1.1.2.6.1.3.1.12 - Paxos

**Status:** OK — All four Spark Paxos instances use the Via-Paxos convention consistently while preserving direction, links, and parameters.

<!-- validation-check:check-022 -->
#### A.1.10.2.5.2 - Operational Reference Materials

**Status:** OK — All four changed operational-reference links move from Atlas-Axis to the resolvable soterlabs repository at an immutable commit.

<!-- validation-check:check-023 -->
#### A.1.11.2.1.3 - Triggering Requirement

**Status:** ASSUMPTION — Core Facilitator confirmation is accepted by explicit user consent because no contemporaneous confirmation or July tracker exists.

> The Core Facilitator is responsible for confirming that these requirements are met.

The canonical poll says the Core Facilitators placed the proposal into the voting system on behalf of Ranked Delegate cloaky, but neither the four-post forum record nor an available July tracker explicitly confirms rank and buffer at the trigger timestamp. The user explicitly accepted the named assumption that publication reflects Core Facilitator confirmation of those requirements.

**Evidence**

- Canonical poll commit 8295b242432b44a98031ae935a5e87a8561ca34a: Core Facilitators placed the poll on behalf of Ranked Delegate cloaky
- fetch-forum-thread topic 28062 complete four-post record contains no separate Core Facilitator confirmation
- July 2026 compensation and daily-data requests returned no matching tab
- Explicit user consent recorded at 2026-07-20T22:26:03Z

**How To Verify**

1. Locate or request the Core Facilitator's contemporaneous public confirmation and factual basis.
2. Reconcile that confirmation against the July tracker when published.

<!-- validation-check:check-024 -->
#### A.1.11.2.1.3 - Triggering Requirement

**Status:** OK — Cloaky's reply unambiguously signals intent to trigger this exact Weekly Cycle proposal.

### Atlas Vote Recommendation

<!-- validation-check:check-025 -->
#### A.1.6.2.2 - Aligned Delegate Communication Responsibilities

**Status:** OK — The prepared explanation demonstrates the mechanisms, gives a reasoned YES basis, and addresses benefits, risks, implementation, and alignment.

<!-- validation-check:check-026 -->
#### A.1.6.2.2 - Aligned Delegate Communication Responsibilities

**Status:** OK — The poll closes July 23 at 16:00 UTC, establishing a vote-explanation deadline of July 30 at 16:00 UTC.

## Assumption Consent Audit

### Atlas Poll Validation

#### A.1.11.2.1.3 - Triggering Requirement

**Consented:** 2026-07-20T22:26:03Z

At 2026-07-17T17:03:49.653Z, Cloaky remained a Ranked Delegate with at least 4,000 USDS in its AD Buffer, and publication of poll 1642 reflects Core Facilitator confirmation of those requirements. User accepted this previously named Cloaky assumption by stating: I'm acceptinh the assumption about cloaky.

#### A.1.11.2.1.3 - Triggering Requirement

**Consented:** 2026-07-20T22:26:03Z

At 2026-07-17T17:03:49.653Z, Cloaky remained a Ranked Delegate with at least 4,000 USDS in its AD Buffer, and publication of poll 1642 reflects Core Facilitator confirmation of those requirements. User accepted this previously named Cloaky assumption by stating: I'm acceptinh the assumption about cloaky.

## Recommendation

**Position:** YES
**Assessment:** Medium

Vote YES. The complete diff implements all six disclosed edits without changing Agent associations or Paxos transfer parameters. Moving the Sky Spread to an explicit 0% parameter makes the Base Rate, Agent Rate, Sky Savings Rate, and Distribution Reward Fee relationship clearer; SOFR replaces Treasury Bill Rate consistently in the subsidized-borrowing and Actively Stabilizing Collateral formulas. The remaining changes normalize Agent metadata, correct a ratio label, standardize PEJRC and Via-Paxos terminology, and repair operational-reference links. The principal review risks are the breadth of the 85-file edit and reliance on the explicitly accepted trigger-state assumption; neither reveals a substantive implementation mismatch. A forum comment notes pre-existing base_rate/Base_Rate notation inconsistency, but PR #280 does not introduce or alter that variable and it can be handled separately.

## LLM Usage

- **Provider/Model:** openai / gpt-5.6-sol
- **Tokens:** 4,200,910 in / 23,962 out / 9,281 reasoning / 4,234,153 total
- **Cache:** 4,015,872 read / 0 write
