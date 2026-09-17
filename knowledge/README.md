# Knowledge base

The registers defined by [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers), instantiated at [S00](../PREBENCH_PLAN.md#s00-methodological-setup). The rules that govern what may enter them are canonical in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md) and [RESEARCH_METHOD.md](../RESEARCH_METHOD.md); this file is an index and does not restate them.

Primary documents remain the root of evidence. Nothing here replaces reading a source, and no statement here is admissible unless it can be followed back to a claim record and a retained document.

## Registers

| File | Register | Identifier |
| --- | --- | --- |
| [source-register.md](source-register.md) | source register | SRC-nnnn |
| [claim-register.md](claim-register.md) | claim register | CLM-nnnn |
| [fact-register.md](fact-register.md) | fact register | FCT-nnnn |
| [observation-register.md](observation-register.md) | observation register | OBS-nnnn |
| [hypothesis-register.md](hypothesis-register.md) | hypothesis register | HYP-nnnn |
| [decision-log.md](decision-log.md) | decision log | DEC-nnnn |
| [contradiction-register.md](contradiction-register.md) | contradiction register | CTR-nnnn |
| [query-log.md](query-log.md) | query log | QRY-nnnn |
| [question-log.md](question-log.md) | question log | QST-nnnn |
| [limitation-register.md](limitation-register.md) | limitation register | LIM-nnnn |

Record format is fixed by [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store). Retained copies of primary documents live outside this repository, at the location that decision names; a source record identifies its copy by content hash, so two people can confirm they hold the same document without sharing a store.

## Stage artifacts

| File | What it is |
| --- | --- |
| [identifier-mapping.md](identifier-mapping.md) | the bootstrap entries of [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known) mapped to canonical register identifiers |
| [coverage-map.md](coverage-map.md) | stages against research questions, and the record that the two directions agree |
| [contact-plan.md](contact-plan.md) | per open question, a drafted question text and the channel assigned to it |
| [gate-g00.md](gate-g00.md) | the G00 evaluation, each condition MET or NOT MET with its evidence |

## Operators

Provenance fields name an operator. The identifiers below are what those fields use. An operator identifier records who or what performed a step, so that independence can be checked rather than assumed.

| Identifier | Who |
| --- | --- |
| OP-OWNER | the project owner |
| OP-EXT-1, OP-EXT-2 | the two extraction operators of the S00 double extraction. Each is a separate automated extraction run that read the sources directly and had no access to the other's output, to the other's existence as a source of text, or to any existing claim record beyond the bootstrap statement it was asked to re-enter |
| OP-REC | the reconciliation operator of the S00 double extraction. It saw both claim sets and produced neither |
| OP-VER | a verification operator: an operator that evaluates a gate condition or re-reads a source location, and that did not produce the artifact it checks |

Where a canonical rule says a step is performed by a second person, what it requires is a second operator that did not produce the artifact and could not see the first operator's output. The identity of each operator is recorded on the record so a reader can judge the independence for themselves rather than taking it on trust. This reading is fixed by [DEC-0009](decision-log.md#dec-0009-meaning-of-an-independent-operator).

## Derived files

[coverage-map.md](coverage-map.md) is generated from the `Serves` and `Addressed in` lines of the plan and the research questions. It is regenerated when either changes and is never edited on its own.
