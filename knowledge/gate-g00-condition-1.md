# Gate G00, condition 1, re-evaluated

Re-evaluation of condition 1 of the gate of [S00](../PREBENCH_PLAN.md#s00-methodological-setup), and of nothing else. Condition 3 was not touched and no other condition was re-opened. The whole-gate record of 2026-09-17 is [gate-g00.md](gate-g00.md); this file supersedes only its condition 1 section.

- **evaluated on**: 2026-09-18
- **evaluating operator**: OP-VER. It did not produce the artifacts it checked, recomputed the counts and the file hashes itself rather than reading them out of the records, and was instructed that a summary of the repository, including the one it was given, is not evidence.
- **artifact version checked**: the working tree of this repository as committed in the commit that carries this record.
- **occasioned by**: [DEC-0014](decision-log.md#dec-0014-retention-is-s00-work-and-the-documents-read-on-2026-09-17-were-never-retained), which found that retention is S00 work and had every source retrieved, stored and hashed.

**Result: NOT MET.** On one ground, and not on either of the two grounds recorded on 2026-09-17.

## What the condition says, and what it therefore tests

> every field listed in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#structured-extraction) exists in the corresponding register, and the dry-run entry on the organizer page satisfies every rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md);

Two halves, with different scopes. The first is register-wide and is about the existence of fields. The second is scoped by its own words to the dry-run entry, which [DEC-0008](decision-log.md#dec-0008-meaning-of-instantiating-a-register-and-of-the-dry-run-entry) fixes as one source record and one claim record, here SRC-0004 and CLM-0048. The other twelve source records and the other 201 claims are outside it.

The second half imports the rules of one file. A rule that lives in RESEARCH_METHOD.md is not imported by it, however real a defect its breach may be.

## Half one: SATISFIED

Every field of the [source record](../RESEARCH_METHOD.md#source-record-fields) list is present in all 13 records of [source-register.md](source-register.md), and every field of the [claim record](../RESEARCH_METHOD.md#claim-record-fields) list in all 202 records of the [claim register](claim-register.md). Nothing is missing anywhere.

The check was a parse, not a reading: each register file was split on the level-3 record heading that DEC-0004 fixes, every field key harvested by pattern, and each record's key set differenced against the canonical list. The record identifier is carried by the heading rather than by a field line, in 13 of 13 source records and 202 of 202 claim records, which is the format DEC-0004 fixes.

## Half two: one violation, confirmed

107 rules were enumerated from EVIDENCE_POLICY.md, section by section. 43 of them bind a source record or a claim record. Each was checked against SRC-0004 and CLM-0048 by an operator that read both records in full, and every claimed violation was then put to three skeptics instructed to refute it.

| Outcome | Rules |
| --- | --- |
| SATISFIED | 34 |
| NOT APPLICABLE to this pair | 5 |
| VIOLATED, claimed | 4 |
| VIOLATED, confirmed by at least two of three skeptics | 1 |

### The confirmed violation

Item 16 of the [atomic fact rule](../EVIDENCE_POLICY.md#atomic-fact-rule):

> Every span quoted anywhere in the extraction, including inside a locator or a note, is itself recorded as a fact.

SRC-0004's `version` field reads `Published Sep 10, 2026; retrieved 2026-09-17; page states "4 min read"`. The span `4 min read` is quoted there. No claim record anywhere in the register records it: a search of the organizer claim register for the string returns nothing. All three skeptics confirmed the violation, each having checked that item 16 is in EVIDENCE_POLICY.md and not in RESEARCH_METHOD.md, that DEC-0008 puts the source record inside the dry-run entry, and that item 17, which keeps provenance material out of the fact register, does not reach a reading-time figure printed in the page body.

**The minimal fix, not applied here.** `4 min read` is not version information and does not belong in a `version` field. Removing it from that field removes the quoted span and with it the violation, without adding a record. The alternative, recording a claim for the reading time, would put page furniture in the claim register. Neither is applied in this task, whose recorded decision is about retention; the choice belongs with the next work on S00.

### The two grounds recorded on 2026-09-17, and what became of them

**Retention: now satisfied.** SRC-0004's `retained_copy` names a file and a sha256. The operator recomputed the hash from the stored file and matched it, matched the byte count, and found CLM-0048's excerpt present in the retained copy. The `redistribution` field states that full reproduction is not permitted, and the copy is outside the public repository, which is what the retention rule requires in that case.

**reading_confidence: outside what this condition tests.** The value on CLM-0048 is `high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value`, where the field is defined to take UNAMBIGUOUS or NEEDS-INTERPRETATION. That definition is in the claim record field table of RESEARCH_METHOD.md. The second half of condition 1 imports the rules of EVIDENCE_POLICY.md, and the only rule there that governs this field is item 14, which requires spans of identical printed shape in one document to carry the same value. The operator tested that over all 75 claims citing SRC-0004 and found it held.

So the 2026-09-17 evaluation charged condition 1 with a breach of a rule the condition does not import. The verdict of that day was right; one of its two reasons was not. This narrows what condition 1 tests and nothing else: [LIM-0002](limitation-register.md#lim-0002-the-reading_confidence-field-does-not-use-its-own-vocabulary) remains open and remains a real defect across all 202 claims, and the conformance check it calls for is still owed.

### The three claimed violations that did not survive

One held that SRC-0004's `kind` value, `Organizational blog post (corporate engineering blog, competition announcement)`, falls outside the enumerated vocabulary of the kind field, and that `found_by` names no query identifier. Both readings apply the RESEARCH_METHOD.md field table, which this half of the condition does not import. They are real untidiness in the record and are not condition 1 failures.

The other two read the consolidation checklist as charging the pair with a value born from absence, and as failing on that basis. The skeptics found the reading strained against the fields as written.

## Consequence

Condition 1 is NOT MET. S00 stays open under the [slip rule](../PREBENCH_PLAN.md#slip-rule), which is also what assigns the remaining work to S00 rather than to a later stage. S01 is not opened by this task.

The execution path for condition 1 is now non-circular and lies entirely inside S00: the retention obstacle is cleared and recorded, and what remains is one field value in one record. Neither half of the condition depends on work that only a later stage may perform.
