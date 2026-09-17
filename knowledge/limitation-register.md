# Limitation register

Register `LIM-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers): instabilities, coverage gaps and known limits, each with the artifact and version it affects.

Field list per record, in this order:

- **statement**: the limit, stated plainly
- **affects**: the artifacts and versions it applies to
- **detected at**: the stage and how it came to light
- **why it is not fixed**
- **what would remove it**
- **state**: OPEN or CLOSED, with the closing record when CLOSED

## LIM-0001 Correlated error between automated extraction operators

- **statement**: The two operators of a double extraction, OP-EXT-1 and OP-EXT-2, are separate runs of the same kind of automated reader. They are independent in the sense [DEC-0009](decision-log.md#dec-0009-meaning-of-an-independent-operator) requires, in that neither saw the other's output, but they are not independent in the way two different people would be. An error that this kind of reader makes systematically, such as a consistent misreading of a table layout or a shared tendency to normalise a phrase the same way, can appear in both extractions and be recorded as agreement. Agreement between them is therefore weaker evidence of correctness than agreement between two people would be, and the double-extraction agreement rate must not be read as an error rate.
- **affects**: every claim record produced under DEC-0009 whose operators are both automated, beginning with the S00 bootstrap claims; and every gate condition that rests on two operators agreeing.
- **detected at**: [S00](../PREBENCH_PLAN.md#s00-methodological-setup), when DEC-0009 replaced the person-count wording of the canonical rules with operator wording. It is a cost of that decision, recorded when the decision was taken rather than after it caused a problem.
- **why it is not fixed**: the project has one person. Requiring a human second reading of every double-extracted claim would stop the phase at S05, where the schema is populated over the whole corpus. The alternative considered and rejected in DEC-0009 was to mark every affected condition NOT MET, which would end PREBENCH without removing the underlying limit.
- **what would remove it**: a second person performing the second extraction, for a claim or for a class of claims. The owner can act as that second operator on any record by recording OP-OWNER, and the claims that gate conditions depend on are the ones where doing so is worth the time.
- **state**: OPEN

## LIM-0002 The reading_confidence field does not use its own vocabulary

- **statement**: [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#claim-record-fields) fixes the `reading_confidence` field to one of two values: UNAMBIGUOUS, or NEEDS-INTERPRETATION with the interpretation written out. None of the 202 records of the claim register uses either. The operators wrote a level word and a justification instead, most often "high" followed by a note on how the span was retrieved, while 26 records carry no level at all, 14 of them reading "UNRESOLVED as to level" and 12 reading "UNRESOLVED". The field therefore cannot be read as the closed vocabulary it is defined to be, and a reader cannot tell from it which claims carried an interpretive judgement.
- **affects**: every record of [claim-register.md](claim-register.md) and, through them, the 114 proposed facts of [fact-register.md](fact-register.md). It is one of the two reasons gate G00 did not pass, recorded in [gate-g00.md](gate-g00.md).
- **detected at**: [S00](../PREBENCH_PLAN.md#s00-methodological-setup), while checking the designated dry-run entry against every rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md) for the first G00 condition.
- **why it is not fixed**: the values are operator output and rewriting them here would be the project editing records to make its own gate pass. The gate's instruction to resolve a difference by correcting the rule text rather than the records covers differences between operators; it does not license the project to restate what an operator recorded. Mapping "high" to UNAMBIGUOUS is mechanical and probably faithful, but the 26 records that carry no level have no faithful mapping at all, and applying the easy half would leave the field looking compliant where it is not.
- **what would remove it**: a conformance check run on each operator's output before the two sets are compared, rejecting any record whose field values fall outside a closed vocabulary, so that the operator fixes it rather than the project. That check does not exist yet. Until it does, the field is read as free text and the claims that depend on an interpretive judgement are not identifiable from it.
- **state**: OPEN

## LIM-0003 No primary document has a retained copy

- **statement**: [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#retention-of-primary-documents) requires that every included source have a retained copy with a content hash in its source record. All 13 records of [source-register.md](source-register.md) read `retained_copy: PENDING`. No copy of any source has been written to the primary-document store that [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store) fixes, and no content hash exists for any of them. Every claim in the register can therefore be re-checked only against a live URL, and a live page can change or disappear between the extraction and the check.
- **affects**: all 13 source records, all 202 claims and all 114 proposed facts. It is one of the two rules the designated dry-run entry fails, and so part of why G00 condition 1 is NOT MET; see [gate-g00.md](gate-g00.md).
- **detected at**: [S00](../PREBENCH_PLAN.md#s00-methodological-setup), while checking the dry-run entry against every rule of the evidence policy.
- **why it is not fixed**: S00's retrievals were performed to re-enter the bootstrap statements as claims, and the store was fixed by DEC-0004 in the same stage rather than before it. Writing the copies now would produce retrievals of a later date than the claims they support, which would misdate the provenance of every record. The correct sequence is to retrieve and retain in one step, which is what S01 does.
- **what would remove it**: retrieval at [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) that writes each document to the store and records its hash in the source record, at which point every S00 claim is re-checked against the retained copy and any difference is recorded rather than overwritten.
- **state**: OPEN
