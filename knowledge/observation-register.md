# Observation register

Register `OBS-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). What an OBSERVATION is, what it requires and what it may never become are canonical in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#observation). An OBSERVATION states nothing about the world beyond the run it describes.

Field list per record, in this order:

- **statement**: what was observed, scoped to the run
- **procedure**: inputs by identifier and version, tool, exact steps
- **operator**
- **date**
- **raw output**: where it is retained
- **scope limit**: what the observation does not establish

## OBS-0001 First double extraction of the bootstrap statements

- **statement**: Two operators independently re-entered the bootstrap statements of [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known) as claims, reading the cited sources directly under the seven-item atomic fact rule then in force. Operator 1 produced 168 claims and operator 2 produced 159, across three source groups. A third operator, which saw both sets and produced neither, paired them and classified 28 pairs identical, 87 as differing only in wording, 22 as substantive disagreements about what a source prints, and 53 as present in one set only. Almost every wording difference and almost every orphan was traced to a specific thing the rule did not say, and the reconciliation proposed the missing sentence in each case. Eleven bootstrap statements were reported as not supported by their source as written.

  | Source group | Operator 1 claims | Operator 2 claims | Identical | Wording | Substantive | Orphan |
  | --- | --- | --- | --- | --- | --- | --- |
  | Organizer page | 64 | 54 | 13 | 29 | 9 | 14 |
  | Tiny Tapeout | 65 | 55 | 2 | 39 | 8 | 24 |
  | IHP | 39 | 50 | 13 | 19 | 5 | 15 |
  | Total | 168 | 159 | 28 | 87 | 22 | 53 |
- **procedure**: three source groups, each extracted twice. Each operator was given the source URLs, the bootstrap statements to re-enter, and the atomic fact rule as it stood before [DEC-0010](decision-log.md#dec-0010-atomic-fact-rule-amendment). Each fetched the sources itself and had no access to the other's output. The reconciliation operator received both complete outputs and the same rule text, and was instructed to classify rather than to choose.
- **operator**: OP-EXT-1 and OP-EXT-2 extracting, OP-REC reconciling
- **date**: 2026-09-17
- **raw output**: retained outside the repository per [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store); the classification totals are reproduced in the table above and the eleven bootstrap corrections are recorded in the entries of PROJECT_SCOPE.md that they changed.
- **scope limit**: this observation describes one extraction run under one version of the rule. It does not establish an error rate for the method, and the agreement it reports is subject to [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators). Its claim sets were not admitted to the claim register: they were the evidence that the rule needed amending, and the claims that were admitted come from the run recorded in [OBS-0003](#obs-0003-second-double-extraction-under-the-amended-rule).

## OBS-0002 Bounding-box area of a 6x4 CMOS5L tile allocation

- **statement**: The 6x4 bounding box printed as claim C of [CTR-0001](contradiction-register.md#ctr-0001-tile-dimensions-and-valid-tile-sizes-for-cmos5l), 1289.28 by 710.64, has a product of 916,213.94 and, divided by 1,000,000, about 0.916. This is the area of the printed bounding box and nothing else.
- **procedure**: the two printed bounding-box dimensions multiplied, then divided by 1,000,000 to convert square micrometres to square millimetres. Inputs: CTR-0001 claim C as printed in tile_sizes.yaml on branch ihp-sg13cmos5l of TinyTapeout/tt-support-tools.
- **operator**: OP-OWNER
- **date**: 2026-09-15
- **raw output**: the computation is the two operations stated above and is reproducible from the printed inputs.
- **scope limit**: a bounding box is not a usable core area. Nothing here establishes how much of it a design can occupy, and the figure may not be compared with the organizer's "about 0.7 mm2 of nominal tile area" without settling [CTR-0001](contradiction-register.md#ctr-0001-tile-dimensions-and-valid-tile-sizes-for-cmos5l) first. Usable area is [OQ-14](../PROJECT_SCOPE.md#oq-14-usable-core-area), still open.
- **maps bootstrap entry**: OBS-B1

## OBS-0003 Second double extraction under the amended rule

- **statement**: The same bootstrap statements, corrected against their sources after [OBS-0001](#obs-0001-first-double-extraction-of-the-bootstrap-statements), were re-entered as claims by two operators reading the sources independently under the atomic fact rule as amended by [DEC-0010](decision-log.md#dec-0010-atomic-fact-rule-amendment). Operator 1 produced 191 claims and operator 2 produced 142. A third operator paired them into 202 records and classified 15 identical, 101 as differing only in rendering, 19 as substantive disagreements about what a source prints, and 67 as recorded by one operator only. Four bootstrap statements were still reported as not matching their source, all in wording rather than in substance: a dropped "our friends at", an unhyphenated "clock tree buffers", the extent of the Apache licence boilerplate, and whether the shuttle page states its design count in visible text or in metadata.

  | Source group | Operator 1 claims | Operator 2 claims | Identical | Wording | Substantive | Orphan |
  | --- | --- | --- | --- | --- | --- | --- |
  | Organizer page | 72 | 70 | 11 | 55 | 1 | 8 |
  | Tiny Tapeout | 97 | 53 | 0 | 34 | 16 | 55 |
  | IHP | 22 | 19 | 4 | 14 | 1 | 3 |
  | Total | 191 | 142 | 15 | 103 | 18 | 66 |

  The table above reproduces the reconciler's own per-group summaries. They do not agree with the verdicts the rows themselves carry, which give 15 identical, 101 wording, 19 substantive and 67 orphan over 202 rows. The two tallies differ in three columns, by two records in wording and by one each in substantive and orphan, and every difference sits in the Tiny Tapeout group, where the rows give 0, 32, 17 and 56 against the summary's 0, 34, 16 and 55. The cause is that the reconciler counted two of its own Tiny Tapeout rows, one substantive and one orphan, as wording. The register uses the per-row verdicts throughout, because those are what each record carries.

  Compared with OBS-0001, substance improved and textual agreement did not. Statements contradicted by their source fell from 11 to 4 trivia, and substantive disagreement fell from 22 to 19 while claim volume rose. Identical statements fell from 28 to 15, and the two operators diverged further in how much they extracted, most sharply on the Tiny Tapeout group at 97 claims against 53.
- **procedure**: as OBS-0001, with three changes: the atomic fact rule as amended by DEC-0010; the bootstrap statements as corrected in PROJECT_SCOPE.md after the first cycle; and an explicit instruction that the coverage rule binds in both directions. The reconciliation of the Tiny Tapeout group failed once on a network error and was re-run from cached extractions, so its two claim sets are the same ones the first attempt saw.
- **operator**: OP-EXT-1 and OP-EXT-2 extracting, OP-REC reconciling
- **date**: 2026-09-17
- **raw output**: retained outside the repository per [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store). The claims it produced are the [claim register](claim-register.md); the 116 that two operators independently confirmed are consolidated in the [fact register](fact-register.md).
- **scope limit**: one run under one version of the rule. It does not establish an error rate, and its agreement is bounded by [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators). It is the evidence behind the G00 condition that did not pass, recorded in [gate-g00.md](gate-g00.md).
