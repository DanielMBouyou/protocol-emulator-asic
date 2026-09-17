# RESEARCH_QUESTIONS

The first research questions of PREBENCH. Each has a stable anchor (its heading), states what would count as an answer (the evidence type and the artifact that carries it), names the stage of [PREBENCH_PLAN.md](PREBENCH_PLAN.md) that addresses it in its "Addressed in" line, and has status OPEN. No question is answered here; answers live in the registers and stage artifacts under [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md). Questions that follow from an open question of [PROJECT_SCOPE.md](PROJECT_SCOPE.md#open-questions) link to it and do not repeat the fact. A question is closed only by the saturation procedure of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#stop-and-saturation-rule).

Adding a question: append it to its group with the next identifier and add its stage to the "Serves" line of that stage in PREBENCH_PLAN.md; identifiers are never reused. Changing a question: retire it with a pointer to its replacement.

## Group A: exact constraints of the challenge and the technology

### RQ-01 Submission rules and eligibility
- Question: What are the exact rules of submission: template obligation, acceptable licenses, complete submission contents, submission channel, deadline time zone and hardness, eligibility and team limits, precheck and gate-level test requirements, reuse of cores, prior art and generated RTL, repository hosting and naming?
- Counts as an answer: a Tier 1 claim per item (organizer page revision, written organizer reply, or Tiny Tapeout documentation), or a question-log state ASKED or UNANSWERABLE_UNTIL that leads to a DECISION of subtype ASSUMPTION for every item a benchmark artifact depends on.
- Linked open questions: [OQ-01](PROJECT_SCOPE.md#oq-01-template-obligation), [OQ-02](PROJECT_SCOPE.md#oq-02-acceptable-licenses), [OQ-03](PROJECT_SCOPE.md#oq-03-complete-submission-contents), [OQ-04](PROJECT_SCOPE.md#oq-04-submission-channel), [OQ-05](PROJECT_SCOPE.md#oq-05-deadline-time-zone-and-hardness), [OQ-06](PROJECT_SCOPE.md#oq-06-eligibility-and-team-limits), [OQ-07](PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests), [OQ-08](PROJECT_SCOPE.md#oq-08-reuse-of-cores-prior-art-and-generated-rtl), [OQ-28](PROJECT_SCOPE.md#oq-28-repository-hosting-and-naming).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-02 Functional acceptance and protocol scope
- Question: For each protocol named by the organizer, what counts as supporting it (rates, roles, simulation or silicon level), by which mechanism does the organizer expect a design to be reprogrammed after fabrication ([F4](PROJECT_SCOPE.md#organizer-facts)) and do any pins used for it count against the fixed pinout, and are stretch protocols expected from the pads or through an external PHY?
- Counts as an answer: Tier 1 claims from the organizer; failing that, the question-log state and an ASSUMPTION DECISION per item, each listing the benchmark artifacts that depend on it.
- Linked open questions: [OQ-09](PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol), [OQ-10](PROJECT_SCOPE.md#oq-10-reprogramming-mechanism-and-pin-accounting), [OQ-11](PROJECT_SCOPE.md#oq-11-stretch-protocols-pads-or-external-phy).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints). Consumed by S07 and S08.
- Status: OPEN.

### RQ-03 Judging criteria
- Question: What are the judging criteria, their weighting, the jury and the number of winners?
- Counts as an answer: a Tier 1 claim from the organizer; if none exists, the record states NOT STATED and the project derives no weight from it.
- Linked open questions: [OQ-12](PROJECT_SCOPE.md#oq-12-judging-rubric-winners-and-weighting).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-04 Area budget and tile geometry
- Question: Which tile geometry and count apply to the competition shuttle, when will the 6x4 versus 8x4 question be decided, what is the usable core area after power grid and routing overhead, and on what basis does the cells-per-tile estimate rest?
- Counts as an answer: Tier 1 claims from Tiny Tapeout (tile definitions of the shuttle flow) and from the organizer, with value, unit and conditions; resolution of [CTR-01](PROJECT_SCOPE.md#recorded-contradictions) by a responsible party. Any usable-area figure computed by the team is an OBSERVATION with its procedure, not a FACT.
- Linked open questions: [OQ-13](PROJECT_SCOPE.md#oq-13-tile-budget-decision-date), [OQ-14](PROJECT_SCOPE.md#oq-14-usable-core-area), [OQ-15](PROJECT_SCOPE.md#oq-15-basis-of-the-cells-per-tile-estimate), [OQ-29](PROJECT_SCOPE.md#oq-29-tile-dimensions-and-valid-tile-sizes).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-05 Technology flow and PDK status
- Question: Which toolchain and PDK versions will the shuttle pin, which standard-cell set and Liberty corners apply, are SRAM macros available in the CMOS5L flow, and when does the PDK move from dev to main?
- Counts as an answer: Tier 1 claims from IHP repositories and Tiny Tapeout flow files or documentation, each with version identifier and locator, recorded in the technology observation record where they are observed rather than stated; the question-log state otherwise.
- Linked open questions: [OQ-16](PROJECT_SCOPE.md#oq-16-toolchain-and-pdk-version-pinning), [OQ-17](PROJECT_SCOPE.md#oq-17-standard-cell-set-and-liberty-corners), [OQ-18](PROJECT_SCOPE.md#oq-18-sram-availability), [OQ-25](PROJECT_SCOPE.md#oq-25-pdk-promotion-from-dev-to-main).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-06 Electrical clock power and board constraints
- Question: What are the CMOS5L IO electrical limits, the clock source, range and maximum design clock, the power budget, the applicability of the sky130 pinout description, and the board and package?
- Counts as an answer: Tier 1 claims from Tiny Tapeout or IHP with value, unit and conditions; each item without a source recorded NOT STATED.
- Linked open questions: [OQ-19](PROJECT_SCOPE.md#oq-19-io-electrical-specification), [OQ-20](PROJECT_SCOPE.md#oq-20-clock-source-range-and-maximum-design-clock), [OQ-21](PROJECT_SCOPE.md#oq-21-power-budget), [OQ-22](PROJECT_SCOPE.md#oq-22-applicability-of-the-sky130-pinout-description), [OQ-23](PROJECT_SCOPE.md#oq-23-board-and-package).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-07 Schedule and shuttle risk
- Question: What are the shuttle logistics, the fallback if the March 2027 shuttle slips, and when will the shuttle be listed; how do the organizer deadline and the shuttle date relate?
- Counts as an answer: Tier 1 claims from Tiny Tapeout and the organizer, dated; a listing of the shuttle on the Tiny Tapeout runs page registered as a Tier 1 claim.
- Linked open questions: [OQ-24](PROJECT_SCOPE.md#oq-24-shuttle-logistics-and-fallback), [OQ-30](PROJECT_SCOPE.md#oq-30-listing-of-the-march-2027-shuttle).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints).
- Status: OPEN.

### RQ-08 Verification and software deliverable expectations
- Question: Does the organizer expect a particular verification framework, and are a firmware toolchain and an instruction set document, which the organizer's framing ([F3](PROJECT_SCOPE.md#organizer-facts)) does not name as deliverables, expected as deliverables?
- Counts as an answer: Tier 1 claims from the organizer; otherwise NOT STATED. The answer constrains deliverables only; it selects nothing covered by the [prohibition](PROJECT_SCOPE.md#temporary-prohibition-of-microarchitectural-choices).
- Linked open questions: [OQ-26](PROJECT_SCOPE.md#oq-26-expected-verification-framework), [OQ-27](PROJECT_SCOPE.md#oq-27-firmware-toolchain-and-isa-document-as-deliverable).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints). Consumed by S08.
- Status: OPEN.

### RQ-09 Constraints still moving at freeze
- Question: Which entries of the constraints register remain MOVING_CONSTRAINT at benchmark freeze, and what monitoring channel and revisit trigger does each carry?
- Counts as an answer: the freeze record's list of MOVING_CONSTRAINT entries, each with its last verification date, monitoring channel, revisit trigger, and the artifacts that depend on it.
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) for the register, [S10](PREBENCH_PLAN.md#s10-benchmark-freeze) for the freeze record.
- Status: OPEN.

## Group B: architecture-independent dimensions of the protocol space

### RQ-10 Architecture independent dimensions of a protocol
- Question: Which measurable dimensions describe a protocol and its workloads without reference to any implementation, and how is each read from a normative document?
- Counts as an answer: a feature schema in which every field has a definition, unit or value domain, an extraction rule pointing to the kind of normative table or clause it is read from, and a written NO to "does the value change if the implementation changes?" with justification; verified by identical double extraction.
- Addressed in: [S04](PREBENCH_PLAN.md#s04-feature-schema).
- Status: OPEN.

### RQ-11 Source fixed versus implementation defined values
- Question: For each schema field, which values does the normative source fix, and which does it leave to implementations or to tolerances?
- Counts as an answer: the schema marker "constrained by source or left to implementation" per field, and per dataset cell the marker filled with a claim identifier.
- Addressed in: [S04](PREBENCH_PLAN.md#s04-feature-schema) for the marker, [S05](PREBENCH_PLAN.md#s05-dataset) for the values.
- Status: OPEN.

### RQ-12 Timing quantities of each protocol
- Question: What timing quantities does each normative specification impose, in which units and under which conditions?
- Counts as an answer: dataset cells with value, unit, conditions and claim identifier per corpus entry, or NOT STATED with the search logged in the missing-value register.
- Addressed in: [S04](PREBENCH_PLAN.md#s04-feature-schema) for the fields, [S05](PREBENCH_PLAN.md#s05-dataset) for the values.
- Status: OPEN.

### RQ-13 Enumeration of the protocol population
- Question: What is the population of protocols from which the corpus is drawn, and by which documented procedure is it enumerated beyond the organizer's list?
- Counts as an answer: the corpus universe definition (DECISION S03-D1) and an enumeration procedure (venues, standards body catalogues, inclusion criteria) that a second operator applies to produce the same list, with the exclusion log and saturation declared.
- Addressed in: [S03](PREBENCH_PLAN.md#s03-protocol-and-workload-corpus).
- Status: OPEN.

### RQ-14 Roles modes and variants as corpus entries
- Question: When do roles (controller or peripheral, host or device), modes and speed grades of one protocol constitute separate corpus entries?
- Counts as an answer: a splitting rule expressed in schema terms, recorded as DECISION S03-D2 with rationale, and shown to be applied uniformly across the corpus.
- Addressed in: [S03](PREBENCH_PLAN.md#s03-protocol-and-workload-corpus).
- Status: OPEN.

### RQ-15 Definition of a workload
- Question: What is a workload as distinct from a protocol: which transactions or sequences, drawn from the normative document, represent the protocol's use, and which workloads does the organizer's statement leave undefined?
- Counts as an answer: per corpus entry, the workload definition with the clause of the normative document it is drawn from; the undefined set recorded explicitly against [F4](PROJECT_SCOPE.md#organizer-facts) and [F5](PROJECT_SCOPE.md#organizer-facts).
- Addressed in: [S03](PREBENCH_PLAN.md#s03-protocol-and-workload-corpus).
- Status: OPEN.

## Group C: representativeness of the corpus

### RQ-16 Definition and measurement of representativeness
- Question: What does it mean for a benchmark subset to represent the dataset, and by which measure is it assessed?
- Counts as an answer: a definition in terms of the feature schema, a measurement procedure, OBSERVATIONs of that measure on candidate subsets, and the choice of measure recorded as DECISION S07-D1 with alternatives, in the representativeness record.
- Addressed in: [S07](PREBENCH_PLAN.md#s07-representative-benchmark).
- Status: OPEN.

### RQ-17 Detection of familiarity bias
- Question: How is bias toward well-known protocols detected in the enumeration and in the dataset, and where do the organizer-named protocols ([F5](PROJECT_SCOPE.md#organizer-facts)) sit in the feature space relative to the rest of the corpus?
- Counts as an answer: the enumeration coverage record (comparison of the enumerated population against every catalogue of the venue list, coverage per catalogue as OBSERVATIONs) and the seed position OBSERVATION computed from the dataset with its procedure; neither confers any status on any entry.
- Addressed in: [S03](PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) for the enumeration, [S05](PREBENCH_PLAN.md#s05-dataset) for the feature-space position.
- Status: OPEN.

### RQ-18 Construction of the holdout set
- Question: How is a holdout partition of the dataset constructed and withheld before reduction, and how is a benchmark scored against it?
- Counts as an answer: a partition rule recorded as DECISION S05-D1 dated before [S06](PREBENCH_PLAN.md#s06-reduction-and-redundancy) runs, a scoring procedure and acceptance conditions recorded as DECISION S09-D1 dated before the audit, and the holdout audit report.
- Addressed in: [S05](PREBENCH_PLAN.md#s05-dataset) for the partition, [S09](PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) for the scoring.
- Status: OPEN.

## Group D: capabilities and costs of existing programmable-I/O systems

Families are named only as families to investigate; no product is summarized in this file.

### RQ-19 Inventory of programmable IO families
- Question: Which families of programmable I/O systems exist (initial list to investigate: RP2040 PIO, PRU, FlexIO, XMOS, PSoC; extended by search), and which Tier 1 or Tier 2 documents describe each?
- Counts as an answer: a family catalogue entry per family with source records and claims, saturation declared.
- Addressed in: [S02](PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art).
- Status: OPEN.

### RQ-20 Documented protocol coverage per family
- Question: Which protocols has each family demonstrably implemented according to Tier 1 to Tier 3 sources, under which stated conditions?
- Counts as an answer: claims with locator and conditions per family and protocol; absence recorded NOT STATED.
- Addressed in: [S02](PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art).
- Status: OPEN.

### RQ-21 Published cost figures per family
- Question: Which capability and cost dimensions do the sources of each family document, with which units and conditions, and which values do they publish?
- Counts as an answer: the documented dimension list and quantitative claims with value, unit, conditions and locator; a note on comparability limits per figure, without any cross-family ranking.
- Addressed in: [S02](PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art).
- Status: OPEN.

## Group E: relevant metrics

### RQ-22 Metric set for the benchmark
- Question: Which measurable quantities are needed to express the requirement stated in [F4](PROJECT_SCOPE.md#organizer-facts) (support of protocols after fabrication within timing and I/O constraints) and the constraints of the register, each with unit and measurement procedure, without presupposing an implementation?
- Counts as an answer: the metric table of [S07](PREBENCH_PLAN.md#s07-representative-benchmark) with every row complete.
- Addressed in: [S07](PREBENCH_PLAN.md#s07-representative-benchmark); candidates are listed at S04.
- Status: OPEN.

### RQ-23 Area measurement procedure on the target flow
- Question: By which procedure is area to be measured on the target flow so that two measurements of the same input agree: which report, which stage of the flow, which cell library and corners, and which overheads are included?
- Counts as an answer: a procedure referencing Tier 1 flow documentation and the technology observation record, consistent with [RQ-04](#rq-04-area-budget-and-tile-geometry) and [RQ-05](#rq-05-technology-flow-and-pdk-status); an OBSERVATION of repeatability on the non-candidate flow run if DECISION S01-D1 authorizes it.
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) for the observation record, [S07](PREBENCH_PLAN.md#s07-representative-benchmark) for the procedure.
- Status: OPEN.

### RQ-24 Measurability of organizer interest statements
- Question: Which of the organizer's stated interests ([F13](PROJECT_SCOPE.md#organizer-facts)) can be turned into measurable criteria, and which cannot and must be recorded as unmeasurable?
- Counts as an answer: the organizer interest record: for each stated interest, either a metric row or an explicit statement that no measurable criterion is derivable, with the reasoning logged and any weighting deferred to a DECISION.
- Addressed in: [S07](PREBENCH_PLAN.md#s07-representative-benchmark).
- Status: OPEN.

## Group F: methods to reduce redundancy and build a benchmark

### RQ-25 Redundancy reduction methods for the corpus
- Question: Which of the candidate method families of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#statistical-and-data-methods-to-study-later) are applicable to the dataset given its value types and missing markers, and what are their assumptions and failure modes for this data?
- Counts as an answer: the evaluation record per family as defined in [RESEARCH_METHOD.md](RESEARCH_METHOD.md#statistical-and-data-methods-to-study-later), and DECISION S06-D1.
- Addressed in: [S06](PREBENCH_PLAN.md#s06-reduction-and-redundancy).
- Status: OPEN.

### RQ-26 Reproducible selection of the benchmark subset
- Question: How is the benchmark subset selected so that a second operator regenerates it exactly from the dataset and the documented method, and how is every removed entry accounted for?
- Counts as an answer: a documented method with parameters, seeds and software versions, the mapping of every removed entry to its representative with a computed reason, and an OBSERVATION of an independent regeneration matching the original.
- Addressed in: [S06](PREBENCH_PLAN.md#s06-reduction-and-redundancy).
- Status: OPEN.

### RQ-27 Stability of the benchmark under corpus perturbation
- Question: How much does the selected subset change when entries are removed, features are perturbed, missing-value treatment changes or method parameters vary, and what acceptance condition applies?
- Counts as an answer: perturbation procedures and OBSERVATIONs in the sensitivity report; the stability measure and its acceptable level fixed as DECISION S09-D2 before the audit; every instability in the limitation register.
- Addressed in: [S09](PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit).
- Status: OPEN.

## Group G: verification methods suited to the problem

### RQ-28 Verification methodologies applicable to the problem
- Question: Which verification methodologies, including the three technique families the organizer names as welcome ([F15](PROJECT_SCOPE.md#organizer-facts)), are documented as applicable to a device whose supported protocols are defined after fabrication, what does each establish, and what does each require as input?
- Counts as an answer: a catalogue entry per methodology with Tier 1 to Tier 3 sources, documented uses, prerequisites and inputs that presuppose no microarchitecture, limits, cost dimensions and acceptance criteria; no selection of a design flow.
- Addressed in: [S08](PREBENCH_PLAN.md#s08-verification-methodologies).
- Status: OPEN.

### RQ-29 Pin level conformance testing from normative sources
- Question: For each benchmark entry, which clauses, timing tables or test procedures of the normative specification define conformance observable at the pins, and for which entries does no official conformance reference exist?
- Counts as an answer: a conformance source table with locator per benchmark entry, or NOT STATED with the search logged.
- Addressed in: [S08](PREBENCH_PLAN.md#s08-verification-methodologies).
- Status: OPEN.

### RQ-30 Requirements of the Tiny Tapeout verification pipeline
- Question: What does the Tiny Tapeout CMOS5L flow require or provide for verification (precheck, gate-level simulation, test conventions), and is any of it mandatory for the competition?
- Counts as an answer: Tier 1 claims from Tiny Tapeout flow files and documentation in the technology observation record, and the organizer answer under [RQ-01](#rq-01-submission-rules-and-eligibility) and [RQ-08](#rq-08-verification-and-software-deliverable-expectations).
- Linked open questions: [OQ-07](PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests), [OQ-26](PROJECT_SCOPE.md#oq-26-expected-verification-framework).
- Addressed in: [S01](PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) for the flow facts, [S08](PREBENCH_PLAN.md#s08-verification-methodologies) for the catalogue.
- Status: OPEN.

### RQ-31 Verification workload per benchmark entry
- Question: How is each benchmark entry turned into an architecture-independent verification workload: reference behaviour, stimulus classes, checker requirements, roles covered and observation level, drawn from normative clauses?
- Counts as an answer: a verification workload definition per benchmark entry traceable to normative clauses, with every pending alternative recorded where [OQ-09](PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol) is not ANSWERED.
- Addressed in: [S08](PREBENCH_PLAN.md#s08-verification-methodologies).
- Status: OPEN.

## Group H: criteria to later compare architectures on a Pareto front

These questions define comparison criteria before any candidate exists. They name no candidate and select none.

### RQ-32 Axes of the Pareto front
- Question: Which metrics of [RQ-22](#rq-22-metric-set-for-the-benchmark) form the axes on which future candidates will be compared, in which direction, and how is each axis shown to be independent of any particular architecture and free of arbitrary weights?
- Counts as an answer: DECISION S07-D3 listing the axes, directions, dominance rule and independence justification, dated before the ARCHITECTURE GATE.
- Addressed in: [S07](PREBENCH_PLAN.md#s07-representative-benchmark).
- Status: OPEN.

### RQ-33 Bias resistant comparison protocol
- Question: What comparison protocol prevents the first candidate examined from shaping the criteria, and how is the protocol audited?
- Counts as an answer: DECISION S07-D4 (pre-registration, fixed benchmark version, blinding of evaluators where possible, order of evaluation) and the audit of that protocol in the S09 reports against acceptance conditions fixed before the audit.
- Addressed in: [S07](PREBENCH_PLAN.md#s07-representative-benchmark) for the protocol, [S09](PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) for the audit.
- Status: OPEN.

### RQ-34 Dominance under uncertainty and moving constraints
- Question: How is dominance between two points computed when a metric carries measurement uncertainty, depends on a contested value ([CTR-01](PROJECT_SCOPE.md#recorded-contradictions)) or on a MOVING_CONSTRAINT such as the tile budget ([F8](PROJECT_SCOPE.md#organizer-facts)), and how is a constraint change propagated through a comparison already made?
- Counts as an answer: a rule referencing the candidate methods of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#statistical-and-data-methods-to-study-later), recorded as DECISION S09-D3 with rationale, and OBSERVATIONs of its behaviour on the contested and moving values of the constraints register.
- Addressed in: [S09](PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit).
- Status: OPEN.

### RQ-35 Entry conditions for a future candidate
- Question: What minimum evidence must a future candidate provide to be placed on the comparison at all: which benchmark entries, which metrics, which verification evidence, reproduced by whom, under which flow state?
- Counts as an answer: an entry-condition list referencing the frozen benchmark, the metric table and the verification methodology catalogue, recorded as DECISION S10-D1 at freeze.
- Addressed in: [S10](PREBENCH_PLAN.md#s10-benchmark-freeze).
- Status: OPEN.
