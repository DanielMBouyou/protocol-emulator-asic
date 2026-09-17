# Claim register

Register `CLM-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). The field list is canonical in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#claim-record-fields).

The register is held in three files, one per source group, because a single file exceeded what a reviewer can check in one pass and so fired the revisit trigger of [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store). The split is recorded in [DEC-0011](decision-log.md#dec-0011-splitting-the-claim-register-by-source-group). Identifiers run in one sequence across the three files and are never reused.

| File | Source group | Claims | Range |
| --- | --- | --- | --- |
| [claim-register-organizer.md](claim-register-organizer.md) | organizer page | 75 | CLM-0001 to CLM-0075 |
| [claim-register-tinytapeout.md](claim-register-tinytapeout.md) | Tiny Tapeout sources | 105 | CLM-0076 to CLM-0180 |
| [claim-register-ihp.md](claim-register-ihp.md) | IHP sources | 22 | CLM-0181 to CLM-0202 |

Total 202 claims, over the 13 documents of [source-register.md](source-register.md).

## What the double_extraction field says

Read it before relying on any record. Two operators read every source independently; this field records what the pairing of their two sets found.

| double_extraction | Claims | Meaning |
| --- | --- | --- |
| AGREED | 15 | both operators produced the same statement after normalization |
| AGREED ON CONTENT | 101 | both read the source the same way; their statements differed in rendering, and the reconciler recorded the common reading |
| SINGLE OPERATOR | 67 | only one operator recorded the span; it is not independently confirmed |
| CONTESTED EXTRACTION | 19 | the operators reported the source differently; the claim cannot support a CONFIRMED_FACT until it is re-read |

Only the first two categories carry independent confirmation, and what that confirmation is worth is bounded by [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators). The gate condition that tests agreement did not pass: see [gate-g00.md](gate-g00.md).

