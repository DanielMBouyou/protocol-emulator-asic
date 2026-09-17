# Gate G00

Evaluation of the gate of [S00](../PREBENCH_PLAN.md#s00-methodological-setup), whose conditions are canonical there.

- **evaluated on**: 2026-09-17
- **evaluating operator**: OP-VER, an operator that did not produce the artifacts it checked. Every count below was recomputed from the extraction data rather than taken from a summary.
- **artifact version checked**: the working tree of this repository as committed in the commit that carries this record.
- **recorded as a DECISION**: [DEC-0012](decision-log.md#dec-0012-record-of-the-g00-evaluation), as [the plan](../PREBENCH_PLAN.md#rules-of-the-plan) requires. That record carries the verdict; this file carries the evidence.

**Result: NOT PASSED.** Four conditions MET, two NOT MET.

Under the [slip rule](../PREBENCH_PLAN.md#slip-rule), S00 stays open until the failing conditions pass, every downstream stage shifts by the same number of days, and no stage is skipped or merged. The floor date does not move. [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) has not opened, and no research beyond what S00 itself required has been done.

| Id | Condition, abbreviated | Result |
| --- | --- | --- |
| 1 | Every canonical field exists in the corresponding register, and the dry-run entry on the organizer page satisfies every rule of the evidence policy | NOT MET |
| 2 | Every deferred DECISION S00-D1 to S00-D7 has a decision log entry with rationale and alternatives | MET |
| 3 | The bootstrap facts re-entered as claims by two independent operators, the two claim sets identical after normalization | NOT MET |
| 4 | CTR-01 has a contradiction register entry and OBS-B1 an observation register entry | MET |
| 5 | The coverage map complete in both directions and matching the plan and the research questions one to one | MET |
| 6 | Every open question OQ-01 to OQ-30 has a drafted question text and an assigned channel | MET |

## Condition 1: fields and the dry-run entry

**NOT MET**, on the second half.

The first half holds. A check over the registers found every field of the [source record](../RESEARCH_METHOD.md#source-record-fields) list in all 13 records of [source-register.md](source-register.md), and every field of the [claim record](../RESEARCH_METHOD.md#claim-record-fields) list in all 202 records of the [claim register](claim-register.md). The `source_id` of a source record and the `claim_id` of a claim record are carried by the record heading rather than by a field line, which is the format [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store) fixes.

The dry-run entry is CLM-0048 in [claim-register-organizer.md](claim-register-organizer.md), with its source record SRC-0004, the pair that [DEC-0008](decision-log.md#dec-0008-meaning-of-instantiating-a-register-and-of-the-dry-run-entry) requires. It re-enters the organizer's task statement, both operators produced the same statement from it, and every field carries a value. It fails two rules of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md).

First, its `reading_confidence` reads `high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value`, and the field is defined to take UNAMBIGUOUS, or NEEDS-INTERPRETATION with the interpretation written out. No record in the register uses either value, and 26 carry no level at all. Recorded as [LIM-0002](limitation-register.md#lim-0002-the-reading_confidence-field-does-not-use-its-own-vocabulary).

Second, SRC-0004 has `retained_copy: PENDING`, as do all 13 source records, and the [retention rule](../EVIDENCE_POLICY.md#retention-of-primary-documents) requires every included source to have a retained copy with a content hash. Recorded as [LIM-0003](limitation-register.md#lim-0003-no-primary-document-has-a-retained-copy).

Both are non-compliance with rules that already decide the case, not gaps in a rule. The gate's instruction to resolve a difference by correcting the rule text rather than the records governs differences between operators; it does not license the project to rewrite what an operator recorded, nor to backdate a retrieval, in order to pass its own gate.

## Condition 2: the deferred decisions

**MET.**

[DEC-0001](decision-log.md#dec-0001-s00-d1-stop-rule-k) to [DEC-0007](decision-log.md#dec-0007-s00-d7-controlled-vocabulary-of-subject-tags) carry S00-D1 to S00-D7 in order: the stop rule K, screening depth per venue, the venue list per research question group, register format and storage and the primary-document store, the double-extraction set, the reproduction set for AG-14, and the controlled vocabulary of subject tags. Each states the choice, the options considered with why each was rejected, the facts and observations relied on or NONE where the choice rests on none, the rationale, the scope and a revisit trigger.

Four further decisions were taken during the stage and are recorded in the same log: [DEC-0008](decision-log.md#dec-0008-meaning-of-instantiating-a-register-and-of-the-dry-run-entry) on what instantiating a register means, [DEC-0009](decision-log.md#dec-0009-meaning-of-an-independent-operator) on what an independent operator is, [DEC-0010](decision-log.md#dec-0010-atomic-fact-rule-amendment) on the amendment of the atomic fact rule, and [DEC-0011](decision-log.md#dec-0011-splitting-the-claim-register-by-source-group) on splitting the claim register.

DEC-0009 changes what a canonical rule requires and should be read before this gate record is relied on. Several rules required a step to be performed by two persons. This project has one person, so the wording was replaced by operator wording with the conditions of independence written out and the operator recorded on every record. That is a real change, not a clarification, and its cost is recorded as [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators).

## Condition 3: two independent extractions, identical after normalization

**NOT MET.** This is the substantive failure.

Two full cycles were run. Each used two operators that fetched the sources themselves and could not see each other's output, and a third operator that produced neither set and paired them.

| | Operator 1 claims | Operator 2 claims | Identical | Wording | Substantive | Orphan | Bootstrap statements contradicted by their source |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Cycle 1, [OBS-0001](observation-register.md#obs-0001-first-double-extraction-of-the-bootstrap-statements) | 168 | 159 | 28 | 87 | 22 | 53 | 11 |
| Cycle 2, [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule) | 191 | 142 | 15 | 101 | 19 | 67 | 4, all trivial |

Cycle 1 tied almost every difference to a specific thing the seven-item atomic fact rule did not say, so the rule was amended to nineteen items under DEC-0010 and the eleven contradicted statements were corrected in [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known). The largest of those corrections replaced a design count of 64 with the 40 that the sources print.

Cycle 2 ran under the amended rule. Substance improved and textual agreement did not. Statements contradicted by their source fell from eleven to four trivia, substantive disagreement fell from 22 to 19, and identical statements fell from 28 to 15 while claim volume rose and the two operators diverged further in how much they extracted.

The 187 remaining differences were then classified. 129 are presentation, where both operators report the same thing about the source and differ in how the record renders it. 41 are coverage, where one operator recorded material the other did not. 17 are evidential, where the two report the source itself differently. The Tiny Tapeout group holds 34 of the 41 coverage differences and 14 of the 17 evidential ones, and the stated cause is that one operator read the raw document including its metadata while the other read a rendering of the visible body. Two operators reading different byte streams cannot produce identical claim sets, and no wording rule changes that.

A diagnosis was drafted proposing that the project stop amending the rule and instead fix the source snapshot, anchor claims to byte offsets, add a conformance check and make normalization executable. Three independent reviewers were asked to refute it and **all three did**. One found that the reported partition does not close; checked directly, it closes exactly for the organizer and IHP groups and is four rows over in the Tiny Tapeout group, where the reconciler filed four orphan rows for claims already counted in a pair. One found that the diagnosis concedes in its own text that a further amendment built of choice-deleting rules would raise agreement sharply, which contradicts its conclusion that no amendment converges. One found that the proposal has the project write the program that decides which differences count, on a gate whose pass condition is the phrase that program would define.

No structural change has therefore been made to this gate or to what it tests. The condition is recorded as NOT MET, the evidence is in the observation register, and the decision about how to proceed is the owner's and is not taken here.

## Condition 4: the bootstrap contradiction and observation

**MET.**

CTR-01 is [CTR-0001](contradiction-register.md#ctr-0001-tile-dimensions-and-valid-tile-sizes-for-cmos5l), holding the three sources that disagree about CMOS5L tile dimensions and valid tile sizes side by side, with no candidate preferred, and naming the party that can settle each. OBS-B1 is [OBS-0002](observation-register.md#obs-0002-bounding-box-area-of-a-6x4-cmos5l-tile-allocation), the bounding-box area computation, scoped to the one claim it was computed from. The mapping is in [identifier-mapping.md](identifier-mapping.md).

## Condition 5: the coverage map

**MET.**

[coverage-map.md](coverage-map.md) is generated from the `Serves` line of each stage and the `Addressed in` line of each question, and checked in both directions. All 35 research questions have a stage. All ten stages S01 to S10 serve at least one research question. No `Serves` entry lacks a matching `Addressed in` entry and none the other way round. S00 serves no research question, which the condition allows, since it names stages S01 to S10.

## Condition 6: the contact plan

**MET.**

[contact-plan.md](contact-plan.md) carries an entry for each of OQ-01 to OQ-30, each with a drafted question text and a channel from a closed vocabulary, and each with the reason that channel is the party that publishes or decides the answer. Every draft was written to presuppose no answer and no architecture and was then checked by a second operator against those rules; all 30 were rewritten in that pass, and what changed is recorded under each entry. 15 entries are marked as blocking a benchmark artifact. Nothing has been sent: sending is S01 work, and gate G01, not this one, tests the question-log states.

A thirty-first open question, [OQ-31](../PROJECT_SCOPE.md#oq-31-licence-of-the-standalone-cmos5l-repository), was opened during the stage when the re-extraction found that the Apache-2.0 attribution carried by bootstrap entry I4 rested on no claim record. It has an entry and a channel like the others. The condition names OQ-01 to OQ-30 and is met on those; OQ-31 is covered as well.

## What S00 produced

| Artifact | Content |
| --- | --- |
| [source-register.md](source-register.md) | 13 documents, each retrieved twice |
| [claim-register.md](claim-register.md) | 202 claims in three files, each carrying what the double extraction found |
| [fact-register.md](fact-register.md) | 114 facts from the 116 independently confirmed claims: 108 PROPOSED, 6 CONTESTED by CTR-0001, none CANONICAL |
| [observation-register.md](observation-register.md) | 3 observations |
| [contradiction-register.md](contradiction-register.md) | 1 contradiction, OPEN |
| [decision-log.md](decision-log.md) | 13 decisions |
| [hypothesis-register.md](hypothesis-register.md) | empty, as expected at this point |
| [limitation-register.md](limitation-register.md) | 3 limitations, all OPEN |
| [query-log.md](query-log.md) | 26 retrievals |
| [question-log.md](question-log.md) | 31 records, none sent |
| [identifier-mapping.md](identifier-mapping.md) | every bootstrap identifier mapped |
| [coverage-map.md](coverage-map.md) | stages against questions, both directions |
| [contact-plan.md](contact-plan.md) | 31 drafted questions with channels |

No fact is CANONICAL. Promotion requires the independent check that condition 3 tests, so the [constraints register](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known) remains the project's working statement of what is known, and it now reflects the eleven corrections the double extraction forced.

This record was itself reviewed before the commit that carries it, by five lenses over the repository with each finding checked by three skeptics. Twenty-one findings survived and were applied. They corrected, among other things, a misplaced quotation mark that put the organizer's firmware-over-fixed-logic contrast into the project's own voice, a status label that was really a lifecycle state, a corroboration justification that was false for two records, and this file's own account of a counting discrepancy.

## What the failing conditions need

Condition 1 needs two things. A conformance check that rejects a record whose field values fall outside the closed vocabulary the field is defined to take, run on each operator's output before the two sets are compared, so that the operator corrects the record and the project does not. And retrieval at S01 that writes each document to the primary-document store and records its hash, at which point the S00 claims are re-checked against the retained copies.

Condition 3 needs a decision that is the owner's to take. The evidence says the two operators were not reading the same bytes, that most of what remains is presentation rather than evidence, and that a third amendment of the same clarifying kind would repeat the result of the second. It does not say which of those to fix first, and the one proposal drafted here was refuted on all three angles it was attacked from.
