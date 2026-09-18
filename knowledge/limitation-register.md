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

## LIM-0003 The documents the S00 claims were read from were never retained

- **statement**: The 202 claims of S00 were extracted on 2026-09-17 from documents that were fetched, read and then discarded. No copy was kept and no hash was taken. Retention was performed on 2026-09-18 under [DEC-0014](decision-log.md#dec-0014-retention-is-s00-work-and-the-documents-read-on-2026-09-17-were-never-retained), so every source now has a retained copy with a content hash, but that copy was taken a day after the claims. Identity between the two is not established and cannot now be established. A claim whose excerpt is found in the retained copy is consistent with it; it is not verified against the document the operator actually read.

  Three further limits sit inside this one.
  - Three claims are not supported by the retained copy of the source they cite. CLM-0200 and CLM-0201 cite SRC-0001, and CLM-0181 cites SRC-0003; all three quote Markdown source, and the source records name the rendered repository landing page, which serves that file as HTML. The excerpt and the URL point at two different representations. The claims are not rewritten; two of them support proposed facts, which therefore rest on a source record that does not name the document the excerpt came from.
  - SRC-0001 and SRC-0003 return different bytes on every retrieval, because the page embeds a per-request identifier and nonce. For those two a content hash identifies the copy and is not an identity for the document, which is what the [handling of revisions](../RESEARCH_METHOD.md#handling-of-revisions-and-versions) assumes when it versions a page by accessed_on and retained copy hash.
  - The 25 absence claims were not re-run against the retained copies. Nothing recorded here bears on whether a token the project recorded as absent is still absent.

  The counts and the method are in [OBS-0004](observation-register.md#obs-0004-re-check-of-every-s00-claim-against-its-retained-copy).
- **affects**: all 13 source records, all 202 claims and all 114 proposed facts. The retention half of G00 condition 1 is now satisfied; what remains is this limitation, which is about the value of the evidence rather than the presence of a field.
- **detected at**: [S00](../PREBENCH_PLAN.md#s00-methodological-setup), while checking the dry-run entry against every rule of the evidence policy. The record originally said the remedy was retrieval at S01. That was wrong and is corrected by DEC-0014: the plan assigns retention to no stage, and the slip rule assigns remedial work to the stage whose gate failed, which is S00. The earlier wording was the only thing that made the condition look unreachable.
- **why it is not fixed**: it cannot be. A document that was read and not kept has no recoverable identity, and no later act produces one. What could be done has been done: the sources are retained and hashed from 2026-09-18 onwards, and every claim has been compared against its retained copy. The three mismatched claims could be repaired by correcting the URL of SRC-0001 and SRC-0003 to the raw file each excerpt came from, but that would rewrite the provenance of claims already recorded, so it is left for a decision rather than done here.
- **what would remove it**: nothing removes the loss for these 202 claims. It stops recurring once retrieval and retention happen in one step, which is what [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) and every later stage do under DEC-0014.
- **state**: OPEN, and permanently so for the claims of S00.
