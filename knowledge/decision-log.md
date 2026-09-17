# Decision log

Register `DEC-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). Field list and record format per [DEC-0004](#dec-0004-s00-d4-register-format-storage-and-primary-document-store). Operator identifiers are defined in [README.md](README.md#operators).

A DECISION is retired only by a later DECISION that names it. No record here is edited in place once its stage gate has been evaluated.

## DEC-0001 (S00-D1) Stop rule K

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: In condition (c) of the stop and saturation rule of [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#stop-and-saturation-rule), K = 2. Saturation of a research question requires that the last 2 consecutive rounds added zero new canonical facts and zero new corpus entries for that question.
- **options considered**:
  - K = 1. Rejected: a round can return nothing because its one new query combination happened to be narrow. Conditions (a) and (b) do not protect against this, since they check coverage of tiers and venues, not yield. K = 1 would let a single unlucky round close a question.
  - K = 3. Rejected: step 3 of the stop rule already forbids counting a round as empty unless a genuinely new query combination was formed and run, so each round costs a new angle. Three such rounds for each of 35 research questions does not fit the calendar of [PREBENCH_PLAN.md](../PREBENCH_PLAN.md#calendar). Nothing the project has measured argues that the third round finds what the second missed, and the reopening clause of the stop rule already covers a source that arrives late.
  - K varying by research question group. Rejected: no evidence yet distinguishes the groups, so a per-group K would be a parameter with no basis. It may become decidable once round yields have been observed.
- **facts and observations relied on**: NONE. This is a method parameter fixed before any round has been run; it rests on the structure of the stop rule, not on measured yields. That is stated openly rather than dressed as an empirical choice.
- **rationale**: The cost of a wrong K is asymmetric. Too small closes a question early and the error is silent. Too large spends the calendar and the error is visible. K = 2 is the smallest value that requires two independent new angles to return nothing, which is the property the rule is trying to buy, and the reopening clause bounds the damage of closing early.
- **scope**: every saturation declaration in PREBENCH.
- **revisit trigger**: the first question closed at K = 2 that is later reopened by a new Tier 1 source, or the first stage at which observed round yields make an empirical choice possible.

## DEC-0002 (S00-D2) Screening depth per venue

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The `screened_depth` field of the query log is fixed by venue class.
  - Enumerable venue (a standards body catalogue, a repository file listing, the pages of one specification site, a shuttle runs page): screen the complete listing. Sampling is not permitted.
  - Ranked venue (a general web search engine, a citation index, a publisher database): screen until 10 consecutive results have produced no inclusion, with a floor of 20 results screened and a ceiling of 100. If the venue reports fewer than 30 results, screen all of them.
  - Personal communication: not applicable.
  Every result screened is recorded in `screened_list` whatever its decision, so the depth actually reached and the point at which screening stopped are both auditable from the log.
- **options considered**:
  - A fixed count per query, for example 20. Rejected: blind to yield. It over-screens a dead query and stops inside a rich one, and the number carries no reasoning.
  - Screen every result. Rejected: unbounded on a general search engine, and it would consume the calendar on the long tail of irrelevant results.
  - Screen until the first inclusion. Rejected: this closes on the first plausible hit, which is the familiarity bias the project exists to avoid.
- **facts and observations relied on**: NONE.
- **rationale**: A yield-based stopping criterion is reproducible from `screened_list` in a way a fixed count is not, because a reproduction can check both what was screened and why screening stopped. The floor prevents a stop after a few unlucky results; the ceiling bounds the cost; the complete-listing rule for enumerable venues protects condition (a) of the saturation rule, which needs every authoritative source, not a sample.
- **scope**: every query log entry in PREBENCH.
- **revisit trigger**: a reproduction under [AG-14](../PROJECT_SCOPE.md#architecture-gate) that finds an includable source beyond the depth the original run reached.

## DEC-0003 (S00-D3) Venue list per research question group

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The venue list is fixed per research question group of [RESEARCH_QUESTIONS.md](../RESEARCH_QUESTIONS.md). A venue outside the list for a group may be used only after it is added by a logged DECISION.

  | Group | Venues |
  | --- | --- |
  | A: challenge and technology constraints | ORGANIZER-BLOG (blog.janestreet.com), ORGANIZER-EMAIL, TT-SITE (tinytapeout.com, including its specs, runs, chips and faq pages), TT-GITHUB (github.com/TinyTapeout), IHP-GITHUB (github.com/IHP-GmbH), IHP-SITE (ihp-microelectronics.com), IHP-DOCS (ihp-open-pdk-docs.readthedocs.io), WEB-SEARCH |
  | B: architecture-independent dimensions of the protocol space | STANDARDS-CATALOGUE, SPEC-OWNER-SITE, SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV, WEB-SEARCH |
  | C: representativeness of the corpus | STANDARDS-CATALOGUE, SPEC-OWNER-SITE, SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV |
  | D: capabilities and costs of existing programmable-I/O systems | VENDOR-DOCS, VENDOR-GITHUB, SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV, WEB-SEARCH |
  | E: relevant metrics | TT-SITE, TT-GITHUB, IHP-DOCS, SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV |
  | F: methods to reduce redundancy and build a benchmark | SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV, METHOD-SOFTWARE-DOCS |
  | G: verification methods | STANDARDS-CATALOGUE, TT-SITE, TT-GITHUB, SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV |
  | H: criteria to compare architectures on a Pareto front | SCHOLAR, IEEE-XPLORE, ACM-DL, ARXIV |

  STANDARDS-CATALOGUE resolves, per protocol, to the catalogue of the body that owns that protocol's specification; which body that is, is itself determined at [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) and is not assumed here. SPEC-OWNER-SITE and VENDOR-DOCS resolve the same way, per specification and per family. METHOD-SOFTWARE-DOCS is the documentation of an implementation of a statistical method, used as Tier 2 for the method's definition and never as evidence about the protocol space. WEB-SEARCH is used only to discover official pages and repositories that the other venues do not already reach; a result from it is never a Tier 1 source by virtue of being found there.
- **options considered**:
  - One venue list for every group. Rejected: it would send protocol questions to citation indexes that do not hold normative specifications, and technology questions to standards catalogues that do not hold them either. Saturation condition (b) requires every venue of the list to be searched for the question, so an oversized list makes saturation unreachable and an undersized one makes it meaningless.
  - Web search only. Rejected: it cannot satisfy the Tier 1 requirement of [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#source-priority), because reaching a normative catalogue by ranking is not the same as enumerating it.
  - Leaving the list open and recording venues as they are used. Rejected: the search strategy already forbids this, and an open list makes condition (b) untestable.
- **facts and observations relied on**: FCT records for the organizer contact address and for the existence of the Tiny Tapeout and IHP repositories, as mapped in [identifier-mapping.md](identifier-mapping.md). No claim is made here about which standards body owns which protocol.
- **rationale**: The venue list is what makes the saturation rule testable: condition (b) asks whether every venue has been searched, which is a question only a fixed list can answer. Groups differ in where their Tier 1 sources live, so one list per group is the smallest structure that keeps the condition both satisfiable and meaningful.
- **scope**: every query run in PREBENCH.
- **revisit trigger**: any research question whose saturation condition (b) cannot be satisfied with the venues listed for its group.

## DEC-0004 (S00-D4) Register format, storage and primary-document store

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**:
  - Format. Every register is a Markdown file. One record per level-3 heading, whose text begins with the record identifier. Fields are lines of the form `- **field**: value`, in the order of the canonical field list for that register. A field with no content carries `NOT STATED`, `NOT APPLICABLE` or `NONE` as the canonical rules require, and is never left blank or omitted.
  - Storage. One file per register, in `knowledge/`, named after the register.
  - Primary-document store. Retained copies live outside the public repository, in a directory `primary-documents/` placed as a sibling of the repository working copy. The shared identity of a retained copy is the content hash recorded in the source record, not its path, so two people can verify they hold the same document without sharing the store. A copy whose `redistribution` field explicitly permits redistribution may additionally be committed; the path for committed copies is fixed by a later DECISION at the moment the first such copy exists, so that no empty directory is created now.
  - The dataset of [S05](../PREBENCH_PLAN.md#s05-dataset) is a stage artifact, not a register. If the computations of S06 to S09 need it in a tabular format, that format is fixed by a DECISION at S05 and does not change the register format fixed here.
- **options considered**:
  - CSV or TSV. Rejected for the registers: a claim record carries verbatim excerpts containing commas, quotation marks and line breaks, and the review of a diff is what catches a provenance error. CSV diffs of quoted multi-line fields are not reviewable. Retained as a candidate for the S05 dataset alone, where the cells are short and the file is read by a computation.
  - YAML or JSON. Rejected: structured and computable, but every review would then need a renderer, and the repository would stop being readable as a knowledge base by the people who must check it.
  - One file holding every register. Rejected: it would pass a reviewable size within the first stage, and every change to any register would touch it.
  - A database. Rejected: not diffable, not reviewable in a pull request, and it would require tooling that S00 is not permitted to build.
- **facts and observations relied on**: NONE. This is a format choice, not a claim about the world.
- **rationale**: The registers exist to be checked by a second reader, so reviewability in a diff outranks machine convenience at this stage. Separating the register format from the dataset format keeps that choice from being forced by a computation that does not exist yet. Keeping retained copies outside the repository follows the retention rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#retention-of-primary-documents), whose default for a `NOT STATED` redistribution field is that the copy is not published.
- **scope**: every register of PREBENCH and the location of every retained copy.
- **revisit trigger**: the first register file that exceeds what a reviewer can check in one pass, or the first S06 computation that cannot read the dataset in the format S05 fixed.

## DEC-0005 (S00-D5) Double-extraction set and fraction

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: A claim is extracted independently by two operators if it falls in any of the following. The union is the double-extraction set.
  - (a) every claim that a gate condition depends on, which is the floor imposed by [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#structured-extraction);
  - (b) every claim of kind QUANT, without exception;
  - (c) every claim whose `reading_confidence` is NEEDS-INTERPRETATION;
  - (d) a systematic one-in-five sample of the remaining claims, being those whose `claim_id` sequence number ends in 0 or 5.

  For S00 itself the set is every bootstrap claim, so the fraction at this stage is 1.
- **options considered**:
  - The method's floor alone, that is category (a). Rejected: a wrong value in a claim that no gate cites still flows into the dataset at S05 and into the metric table at S07, where nothing would catch it. Categories (b) and (c) cover exactly the claims where a single reader is most likely to err.
  - Every claim, at every stage. Rejected on the calendar: S05 populates a schema over the whole corpus, and doubling every cell does not fit the phase. The combination of full QUANT coverage and a systematic sample addresses the same failure modes at a cost the calendar can carry.
  - A random sample. Rejected: not reproducible without recording a seed, and a seed is a parameter where a deterministic rule on the identifier works just as well and cannot be steered by the extractor.
- **facts and observations relied on**: NONE.
- **rationale**: Double extraction is a detector, and a detector should be aimed where errors are both likely and consequential. Quantitative claims carry the value, unit and conditions that later computations consume; interpreted claims carry the reader's judgement. Tying the sample to the identifier rather than to a seed or a choice keeps the extractor from influencing which of their own claims get checked.
- **scope**: every extraction in PREBENCH.
- **revisit trigger**: the first double extraction that disagrees on a claim falling only in category (d), which would show the sample is too thin.

## DEC-0006 (S00-D6) Reproduction set for AG-14

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The reproduction set required by condition AG-14 of the [ARCHITECTURE GATE](../PROJECT_SCOPE.md#architecture-gate) is:
  - (a) every query log entry whose `included_ids` contain a source supporting a claim that any stage gate condition depends on;
  - (b) every computation named in the benchmark freeze record, namely the reduction of [S06](../PREBENCH_PLAN.md#s06-reduction-and-redundancy), the representativeness measure and the metric demonstrations of [S07](../PREBENCH_PLAN.md#s07-representative-benchmark), and the holdout and sensitivity runs of [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit);
  - (c) the enumeration of the stratum fixed by DECISION S03-D3.

  The reproduction is performed by an operator who did not perform the original run. Every difference is recorded as an OBSERVATION and the original log is never edited.
- **options considered**:
  - A fixed percentage of query log entries. Rejected: a percentage can be satisfied while missing every query that a gate depends on. The set has to be defined by what the conclusions rest on, not by a count.
  - The computations only, category (b). Rejected: a computation is deterministic given its inputs and is the easiest part to reproduce. The search is where non-determinism actually lives, because a ranked venue returns different results on a later date, which is the reason `screened_list` exists.
  - Everything in the query log. Rejected on the calendar, and a gate that can never pass is not a gate.
- **facts and observations relied on**: NONE.
- **rationale**: AG-14 exists to test whether the recorded method actually regenerates the recorded results. That test is only informative where a conclusion depends on the result, which is what categories (a) to (c) select. Requiring a different operator is what makes it a reproduction rather than a re-run.
- **scope**: the reproduction performed at [S10](../PREBENCH_PLAN.md#s10-benchmark-freeze) and evaluated at the ARCHITECTURE GATE.
- **revisit trigger**: a reproduction that fails to retrieve an included source, which widens the set to every query of that research question.

## DEC-0007 (S00-D7) Controlled vocabulary of subject tags

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The `subject_tags` field of a claim record draws from this closed list. Every claim carries at least one tag. A tag names the subject of the claim and never a judgement about it. Adding a tag is a logged DECISION, as [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#structured-extraction) requires.

  | Tag | Subject |
  | --- | --- |
  | CHALLENGE-RULE | a rule the organizer states as binding on entrants |
  | CHALLENGE-SCOPE | what the organizer asks for, including the protocols named and the stated non-goals |
  | CHALLENGE-SCHEDULE | dates, deadlines and the shuttle the competition targets |
  | CHALLENGE-JUDGING | selection, judging interests, prizes and what winners receive |
  | CHALLENGE-DELIVERABLE | what a submission must contain and through which channel it is made |
  | CHALLENGE-ADVICE | a statement the organizer offers as advice rather than as a rule |
  | PROTOCOL | a normative statement about a protocol itself |
  | WORKLOAD | a transaction or sequence drawn from a normative document |
  | TECH-PROCESS | the semiconductor process and its devices |
  | TECH-PDK | the contents, licensing and status of a process design kit |
  | TECH-FLOW | the RTL-to-GDS flow, its tools, versions and checks |
  | TECH-TILE | tile geometry, tile counts and area budgets |
  | TECH-IO | pads, pinout and electrical behaviour of the chip boundary |
  | TECH-CLOCK | clock source, range and timing constraints of the target chip |
  | TECH-POWER | supply voltages and power budgets |
  | TECH-MEMORY | memory macros available in a technology and their integration |
  | SHUTTLE | a specific shuttle run, its schedule, contents and logistics |
  | LICENSE | the licensing or redistribution terms of a document or artifact |
  | PRIOR-SYSTEM | a documented capability or cost of an existing programmable-I/O family |
  | METHOD-BENCHMARK | a method for reducing, selecting or auditing a benchmark |
  | METHOD-VERIFICATION | a verification or conformance methodology |
  | METHOD-STATISTICS | the definition or behaviour of a statistical or data method |
- **options considered**:
  - Free-text tags. Rejected: two independent extractors would tag the same claim differently, and the tag would stop being a retrieval key, which is its only purpose.
  - One tag per research question. Rejected: the `rq_ids` field already carries that link, and a subject outlives the question that prompted it. A claim about tile geometry stays a tile claim after RQ-04 closes.
  - A hierarchical taxonomy. Rejected: a flat closed list can be checked against a claim in one pass; a hierarchy needs a maintainer and invites disagreement about depth.
- **facts and observations relied on**: NONE.
- **rationale**: The vocabulary is fixed before extraction begins so that two operators tag identically, which is what the double-extraction rule of [DEC-0005](#dec-0005-s00-d5-double-extraction-set-and-fraction) checks for. A closed list makes an unfitting claim visible as a gap that a DECISION must close, rather than absorbing it silently into a vague tag.
- **scope**: every claim record in PREBENCH.
- **revisit trigger**: the first claim that no tag in the list fits.

## DEC-0008 Meaning of instantiating a register and of the dry-run entry

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: Three canonical texts pull in different directions on what S00 must put into each register. This decision fixes the reading and amends the plan to match it.
  - To instantiate a register is to create its file, state its identifier scheme and state its canonical field list. It is not to put a record in it.
  - The dry-run entry required by gate G00 is one entry, on the organizer page, consisting of one source record and one claim record in which every field of both canonical field lists carries a value. It is a real record with real provenance, designated in [gate-g00.md](gate-g00.md) as the entry that demonstrates the format.
  - A register for which no real record yet exists is instantiated and stands empty, with its field list and a line stating why it is empty. No record is invented to fill it.
  - The S00 output line of [PREBENCH_PLAN.md](../PREBENCH_PLAN.md#s00-methodological-setup) is amended from "the registers with their field lists instantiated, each with one dry-run entry" to "the registers with their field lists instantiated, and one dry-run entry on the organizer page exercising every field of the source record and the claim record".
- **options considered**:
  - One fabricated dry-run record in every register, reading the plan line literally. Rejected: it collides with the root-of-evidence rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#root-of-evidence), under which a statement that cannot be followed back to a claim and a retained document is removed. A fabricated contradiction record or limitation record would be exactly such a statement, and marking it DRY-RUN does not change what it is. It would also put invented content in a public knowledge base whose value is that everything in it is traceable.
  - Leaving the three texts as they are and satisfying whichever is most convenient at each gate. Rejected: a rule that can be read two ways is not a rule, and the gate would be unfalsifiable.
  - Amending G00 instead, to require a dry-run entry per register. Rejected: it makes the same fabrication mandatory and contradicts the evidence policy more directly.
- **facts and observations relied on**: NONE. This resolves a conflict between the project's own texts.
- **rationale**: G00 is the narrower and more precise of the two requirements. It names a single dry-run entry, names the page it must come from, and demands that it satisfy every rule of the evidence policy, which a fabricated record cannot. Reading the looser plan line in the light of the stricter gate keeps both satisfiable and keeps invented records out of the registers.
- **scope**: the instantiation of every register in PREBENCH; the amended S00 output line.
- **revisit trigger**: a later stage that needs a format demonstration in a register the organizer page cannot supply one for.

## DEC-0009 Meaning of an independent operator

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: Several canonical rules require a step to be performed by "two persons independently" or checked by "a second person". This project is run by one person working with automated assistance, so those rules are amended to state what independence requires and to make it auditable, rather than to assume a head count.
  - The person-count wording in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md) and [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md) is replaced by operator wording: two independent operators, and a second operator.
  - Two operators are independent for a step when the second had no access to the first operator's output for that step, did not know what the first concluded, and worked from the source or artifact directly.
  - A checking operator must not be the operator that produced the artifact it checks.
  - The identity of every operator is recorded on the record, using the vocabulary of [README.md](README.md#operators). Independence is therefore something a reader judges from the record, not something the record asserts.
- **options considered**:
  - Keep the wording and treat automated extraction runs as persons. Rejected: it would make the records say something untrue about who did the work, in a system whose entire value is that its provenance is exact.
  - Keep the wording and mark every affected condition NOT MET until a second person joins the project. Rejected: it would stop PREBENCH at S00 and would make the double-extraction machinery dead text, when the machinery does detect real errors, as the S00 reconciliation shows.
  - Keep the wording and have the owner personally perform every second extraction, screening and gate evaluation. Rejected as a rule for the whole phase: S05 populates a schema over the whole corpus, and the calendar cannot carry it. The owner remains free to act as the second operator on any record, and does so by recording OP-OWNER.
- **facts and observations relied on**: NONE.
- **rationale**: The rules were written to buy a property, which is that a second reading of the same source, taken without sight of the first, agrees with it. That property does not depend on the second reader being human; it depends on the second reader not having seen the first answer. Stating the conditions and recording the operator makes the property checkable, where a head count only made it assertable. The cost of this change is recorded as [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators).
- **scope**: every rule in the repository that requires a second person or two persons, including double extraction, two-person screening, the independence text test, promotion to CANONICAL, and gate evaluation.
- **revisit trigger**: a second person joining the project, or a disagreement pattern in the limitation register showing that automated operators miss a class of error that a human reader would catch.

## DEC-0010 Atomic fact rule amendment

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The atomic fact rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#atomic-fact-rule) is extended from seven numbered items to nineteen, grouped as shape, wording, values and fields, absence, and which spans become facts. The added material fixes, in order: repeated predicates printed together; the subject of a statement; imperatives; anaphora and deixis; the frame for a quoted span, a key and value, and a formulaic notice line; the scope of the modality field; evaluative wording printed by the source; counts obtained by enumeration; the unit field when no unit is printed; the assignment of the kind field by printed form; the boundary between conditions and provenance; the consistency of reading_confidence; the fixed form of an ABSENCE statement; which spans must become facts; the treatment of provenance material; two readings of one element across retrieved versions; and retrieval fidelity of excerpts.
- **options considered**:
  - Leave the seven-item rule and accept the two claim sets as they stand. Rejected: gate G00 requires the two sets to be identical after normalization, and it requires that a difference be resolved by correcting the rule text rather than the records. Accepting the records would invert the rule the gate exists to enforce.
  - Leave the rule and reconcile each difference case by case. Rejected: it would move the decision from a written rule into the judgement of whoever reconciles, which is the opposite of what the double extraction is for, and the next extraction would reproduce the same differences.
  - Amend only the items the reconciliation could tie to a numbered rule, leaving the gaps it found outside the numbering. Rejected: more than half the differences were traced to matters no numbered item covered at all, notably which spans become facts and how the kind field is assigned.
- **facts and observations relied on**: [OBS-0001](observation-register.md#obs-0001-first-double-extraction-of-the-bootstrap-statements), the first double extraction, which produced 168 claims from one operator and 159 from the other across three source groups, of which the reconciliation classified 28 identical, 87 as wording differences, 22 as substantive disagreements and 53 as present in one set only.
- **rationale**: A rule that two careful operators can follow to two different texts is not a normalization rule. The reconciliation did not report vague disagreement: it tied almost every difference to a specific thing the rule did not say, and proposed the missing sentence. Writing those sentences is cheaper than arbitrating the same differences at every later stage, and it is what the gate condition prescribes.
- **scope**: every fact statement and every claim statement in PREBENCH, including the re-extraction that follows this decision.
- **revisit trigger**: a later double extraction whose differences again trace to a gap in this rule.

## DEC-0011 Splitting the claim register by source group

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: The claim register is held in three files, one per source group: [claim-register-organizer.md](claim-register-organizer.md), [claim-register-tinytapeout.md](claim-register-tinytapeout.md) and [claim-register-ihp.md](claim-register-ihp.md), with [claim-register.md](claim-register.md) as an index. Identifiers run in one CLM sequence across the three files and are never reused. The record format of [DEC-0004](#dec-0004-s00-d4-register-format-storage-and-primary-document-store) is unchanged; only the file boundary moves.
- **options considered**:
  - One file, as DEC-0004 originally implied. Rejected: the 202 claims of the second S00 double extraction produce about 234 kilobytes in one file. That is past the point where a reviewer can check it in one pass, which is the revisit trigger DEC-0004 itself named, and a diff touching one claim would sit inside a file nobody rereads.
  - Splitting by bootstrap entry, one file per F, T or I identifier. Rejected: about thirty files, most of them a few records long, and the bootstrap identifiers are scaffolding that disappears once the mapping in [identifier-mapping.md](identifier-mapping.md) has done its work.
  - Splitting by stage of extraction. Rejected: it would file a claim by when it was recorded rather than by what it is about, so nobody looking for a claim would know which file to open.
- **facts and observations relied on**: the measured file size above, from the generation of the register.
- **rationale**: A source group is the boundary a reader actually uses, because the question being checked is almost always about one party's documents. It also keeps each file inside a size a reviewer will reread, which is the property DEC-0004 was protecting when it named the trigger.
- **scope**: the claim register. No other register is split, and none is near the threshold.
- **revisit trigger**: any one of the three files exceeding what a reviewer can check in one pass, which the Tiny Tapeout file will reach first.

## DEC-0012 Record of the G00 evaluation

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: Gate G00 is evaluated NOT PASSED. Condition 1 NOT MET, condition 2 MET, condition 3 NOT MET, condition 4 MET, condition 5 MET, condition 6 MET. The evidence for each, and what each failing condition needs, is in [gate-g00.md](gate-g00.md), which this record incorporates rather than repeats. Under the [slip rule](../PREBENCH_PLAN.md#slip-rule) S00 stays open, the downstream dates shift by the number of days S00 runs past day 2, and the floor date does not move. No stage after S00 has opened.
- **evaluating operator**: OP-VER, an operator that did not produce the artifacts it checked. The counts it reports were recomputed from the extraction data rather than taken from the reconciler's summaries, and the two disagree; the discrepancy is recorded in [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule).
- **artifact version checked**: the working tree of this repository as committed in the commit that carries this record. Every artifact named in gate-g00.md is at the state that commit contains.
- **options considered**:
  - Mark the gate PASSED and treat the two failures as minor. Rejected: condition 3 is the stage's central test and its result is not close, and condition 1 fails on a field whose vocabulary is written into the method. A gate that passes when its own conditions fail measures nothing.
  - Amend the two failing conditions so that they pass. Rejected: it is the failure mode the gate exists to prevent, and one proposal of that kind was drafted during the stage and refuted by three independent reviewers on three different grounds.
  - Defer the evaluation until the conditions pass. Rejected: the stage's findings, including eleven corrected bootstrap statements, are worth recording now, and a gate that is only evaluated once it will pass records nothing about what it cost to get there.
- **facts and observations relied on**: [OBS-0001](observation-register.md#obs-0001-first-double-extraction-of-the-bootstrap-statements), [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule), [LIM-0002](limitation-register.md#lim-0002-the-reading_confidence-field-does-not-use-its-own-vocabulary), [LIM-0003](limitation-register.md#lim-0003-no-primary-document-has-a-retained-copy).
- **rationale**: The plan requires a gate evaluation to be recorded as a DECISION listing each condition as MET or NOT MET with the artifact version checked, and this record supplies that. It does not restate gate-g00.md, because the same rule lives in one place.
- **scope**: stage S00 and the opening of S01.
- **revisit trigger**: the failing conditions passing, which requires a new evaluation and a new record; this one is not edited.

## DEC-0013 Record format for registers whose records are not field lists

- **date**: 2026-09-17
- **deciders**: OP-OWNER
- **stage**: S00
- **statement**: [DEC-0004](#dec-0004-s00-d4-register-format-storage-and-primary-document-store) fixed one record per level-3 heading with field lines. Six registers depart from it and the departures are confirmed here rather than left as silent non-compliance.
  - The decision log, observation register, contradiction register and limitation register use a level-2 heading per record. They hold few records and each record is long, so a level-3 heading under no level-2 parent would leave the file with no navigable structure.
  - The query log and the question log are tables, one row per record, because every field of those two records is short and the value of the register is being able to scan the whole of it at once.
  - The claim register and the source register follow DEC-0004 exactly, and they are the two the canonical field lists of [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#structured-extraction) govern.
  In every register, whatever the shape, each record still begins with its identifier and carries every field of its field list, and the field list is printed at the top of the file.
- **options considered**:
  - Normalize all ten registers to level-3 headings with field lines. Rejected: it would put 26 query log rows and 31 question log rows into roughly 500 lines of field blocks, which makes the two registers unusable for the scanning they exist for.
  - Leave the departures unrecorded. Rejected: a format rule that six of ten registers ignore is not a rule, and a reviewer checking the repository against DEC-0004 would find six failures with nothing explaining them.
- **facts and observations relied on**: NONE. This is a format choice.
- **rationale**: DEC-0004 was written before any register existed and assumed every record would be a long field block. Two of them are not. Naming which shape each register uses, and keeping the identifier and the field list mandatory in all of them, preserves what the rule was for.
- **scope**: the ten registers of [README.md](README.md#registers).
- **revisit trigger**: a register whose shape no longer fits its contents, or a tool that needs one parse for all of them.
