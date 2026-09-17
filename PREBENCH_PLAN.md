# PREBENCH_PLAN

Canonical location for the PREBENCH phase plan: calendar, stages, objectives, inputs, named artifacts, gates, research questions served, and the day-by-day schedule. The scope of the phase and the ARCHITECTURE GATE are canonical in [PROJECT_SCOPE.md](PROJECT_SCOPE.md); the research method and evidence rules that every stage applies are in [RESEARCH_METHOD.md](RESEARCH_METHOD.md) and [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md).

## Calendar

- Day 1: 2026-09-17.
- Day 17: 2026-10-03. This is the floor: the phase may not end before this date. The floor is a minimum, not a target; reaching it authorizes nothing by itself, and finishing the stages early does not authorize an early freeze.
- Day 21: 2026-10-07. This is the target end, at which [S10](#s10-benchmark-freeze) closes if every gate has passed.
- Organizer deadline: 2027-01-18, MOVING_CONSTRAINT ([F12](PROJECT_SCOPE.md#organizer-facts)). Nothing after PREBENCH is planned in this file.

## Rules of the plan

- Each stage has an objective; inputs; outputs as named artifacts (logical names only; their format and storage are fixed by DECISION S00-D4; nothing is created by this plan); a gate; and the research questions it serves.
- A gate is a list of verifiable completeness or consistency conditions. No gate is a count chosen without rationale. A gate is evaluated by a person who did not produce the artifact (the ARCHITECTURE GATE uses two verifiers); the evaluation is recorded as a DECISION listing each condition as MET or NOT MET with the artifact version checked. No partial credit and no waiver.
- Any numeric threshold used by a gate is fixed as a DECISION with rationale at the stage named, never in this file. The labels S00-D1, S03-D1 and so on are the plan names of those DECISION records; the records themselves carry canonical identifiers per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#registers-and-identifiers).
- A failed gate is handled by the [Slip rule](#slip-rule).
- Stages overlap where the schedule shows it; a stage starts when its inputs exist, not before. Overlapping stages on the same day are worked by different persons or in sequence.
- Artifacts named by the plan are the registers of [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#registers-and-identifiers) and the stage artifacts listed below.
- The mapping between stages and research questions is the "Addressed in" line of each question in [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md) and the "Serves" line of each stage below; the two must agree, and S00 checks that they do.

## Slip rule

If a gate fails, the stage continues until the failing condition passes; every downstream stage shifts by the same number of days; no stage is skipped or merged; the new dates are recorded as a DECISION. The floor date never moves. The target date moves with the slip.

## Stages

### S00 Methodological setup

- Days 1 to 2 (2026-09-17 to 2026-09-18).
- Objective: make the method executable by two people independently before any research is recorded.
- Inputs: [RESEARCH_METHOD.md](RESEARCH_METHOD.md), [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md), the bootstrap facts of [PROJECT_SCOPE.md](PROJECT_SCOPE.md#challenge-constraints-as-currently-known), [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md).
- Outputs:
  - the registers with their field lists instantiated, each with one dry-run entry;
  - the identifier mapping of bootstrap entries (F, T, I, CTR-01, OBS-B1, OQ) to canonical register identifiers;
  - the DECISIONs the method defers to this stage: S00-D1 (stop rule K), S00-D2 (screening depth per venue), S00-D3 (venue list per research question group), S00-D4 (register format, storage, and the primary-document store location), S00-D5 (double-extraction set and fraction), S00-D6 (reproduction set for ARCHITECTURE GATE condition AG-14), S00-D7 (controlled vocabulary of subject tags);
  - stage-to-question coverage map;
  - contact plan: for every open question of PROJECT_SCOPE.md, a drafted question text and an assigned channel;
  - the initial hypothesis register (empty, or containing only isolated entries).
- Gate G00:
  - every field listed in [RESEARCH_METHOD.md](RESEARCH_METHOD.md#structured-extraction) exists in the corresponding register, and the dry-run entry on the organizer page satisfies every rule of [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md);
  - every deferred DECISION S00-D1 to S00-D7 has a decision log entry with rationale and alternatives;
  - the bootstrap facts are re-entered as claims by two persons independently and the two claim sets are identical after normalization per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#atomic-fact-rule); any difference is resolved by correcting the rule text, not the records;
  - CTR-01 has a contradiction register entry and OBS-B1 an observation register entry;
  - the coverage map has no research question without a stage and no stage S01 to S10 without a research question, and matches the "Addressed in" lines of RESEARCH_QUESTIONS.md one to one;
  - every open question OQ-01 to OQ-30 has a drafted question text and an assigned channel in the contact plan.
- Serves: the method for all questions; no research question is answered here.

### S01 Challenge and PDK constraints

- Days 2 to 5 (2026-09-18 to 2026-09-21), then re-verification of MOVING_CONSTRAINT entries at every later gate per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#status-labels).
- Objective: complete the constraints register from the organizer, Tiny Tapeout and IHP sources, send the questions that no source answers, and log the answers as sources.
- Inputs: the open questions [OQ-01](PROJECT_SCOPE.md#oq-01-template-obligation) to [OQ-30](PROJECT_SCOPE.md#oq-30-listing-of-the-march-2027-shuttle); the contact plan of S00; the registers of S00.
- Outputs:
  - constraints register (the subset of the fact register tagged CHALLENGE or TECHNOLOGY, each entry with re-verification date);
  - question log entries for every open question, per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log);
  - updated contradiction register;
  - technology observation record: what the CMOS5L flow and PDK provide as observed in the repositories (versions, branches, cell library names, corners present, pad and tile definitions), each value with retrieval date and repository state identifier, recorded as OBSERVATIONs;
  - optionally, under DECISION S01-D1 (authorization per the flow characterization note of [PROJECT_SCOPE.md](PROJECT_SCOPE.md#scope-of-prebench)), a flow characterization OBSERVATION on the unmodified template.
- Gate G01:
  - every open question of PROJECT_SCOPE.md is in exactly one question-log state per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log);
  - every MOVING_CONSTRAINT has been re-verified against its URL on a date within this stage and the date is recorded;
  - every quantitative datum in the constraints register carries value, unit and conditions per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#quantitative-data);
  - no artifact of this stage contains a tile dimension or area figure chosen from among the CTR-01 claims; every use of a CTR-01 value complies with [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#contradictions);
  - every value of the technology observation record has a retrieval date and a repository state identifier; no value comes from memory or from a secondary source without a pointer;
  - saturation is declared per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#stop-and-saturation-rule) for each research question of group A except [RQ-09](RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze), which closes at S10.
- Serves: [RQ-01](RESEARCH_QUESTIONS.md#rq-01-submission-rules-and-eligibility), [RQ-02](RESEARCH_QUESTIONS.md#rq-02-functional-acceptance-and-protocol-scope), [RQ-03](RESEARCH_QUESTIONS.md#rq-03-judging-criteria), [RQ-04](RESEARCH_QUESTIONS.md#rq-04-area-budget-and-tile-geometry), [RQ-05](RESEARCH_QUESTIONS.md#rq-05-technology-flow-and-pdk-status), [RQ-06](RESEARCH_QUESTIONS.md#rq-06-electrical-clock-power-and-board-constraints), [RQ-07](RESEARCH_QUESTIONS.md#rq-07-schedule-and-shuttle-risk), [RQ-08](RESEARCH_QUESTIONS.md#rq-08-verification-and-firmware-deliverable-expectations), [RQ-09](RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze), [RQ-23](RESEARCH_QUESTIONS.md#rq-23-area-measurement-procedure-on-the-target-flow), [RQ-30](RESEARCH_QUESTIONS.md#rq-30-requirements-of-the-tiny-tapeout-verification-pipeline).

### S02 Programmable IO state of the art

- Days 4 to 8 (2026-09-20 to 2026-09-24).
- Objective: build the catalogue of existing programmable-I/O system families with their documented capabilities and costs, as sourced claims, without summarizing or ranking any product.
- Inputs: the initial family list to investigate (RP2040 PIO, PRU, FlexIO, XMOS, PSoC, and any family found by search); Tier 1 and Tier 2 sources per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#source-priority).
- Outputs:
  - family catalogue (one entry per family: sources, claims on capabilities, claims on documented protocol coverage with conditions, claims on cost figures with value, unit and conditions);
  - documented dimension list: the capability and cost dimensions that the sources actually document, with the unit and conditions each uses, offered as candidate input to S04 and labelled candidate;
  - query log entries; saturation record; hypothesis register entries if any idea arises, isolated.
- Gate G02:
  - every family entry cites at least one Tier 1 or Tier 2 source with locator for every claim, or is marked NO-PRIMARY-SOURCE-FOUND with the queries run;
  - the extraction fields are identical across families; a field with no documented value is NOT STATED per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#absence-of-information);
  - every cost figure complies with [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#quantitative-data);
  - the catalogue contains no comparative ranking, no recommendation and no statement that a family is a model for the project (checked by reading every entry against the [prohibition](PROJECT_SCOPE.md#temporary-prohibition-of-microarchitectural-choices));
  - saturation is declared for each research question of group D.
- Serves: [RQ-19](RESEARCH_QUESTIONS.md#rq-19-inventory-of-programmable-io-families), [RQ-20](RESEARCH_QUESTIONS.md#rq-20-documented-protocol-coverage-per-family), [RQ-21](RESEARCH_QUESTIONS.md#rq-21-published-cost-figures-per-family).

### S03 Protocol and workload corpus

- Days 5 to 10 (2026-09-21 to 2026-09-26).
- Objective: enumerate the protocol population and the workloads from normative sources, without selecting.
- Inputs: the organizer's protocol list ([F5](PROJECT_SCOPE.md#organizer-facts)) as a seed, not as the population; the standards bodies and specification owners identified per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#source-priority); the inclusion and exclusion criteria of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#inclusion-and-exclusion-criteria); the documented protocol coverage claims of S02 as a further seed.
- Outputs:
  - DECISION S03-D1: corpus universe definition, the written rule stating what counts as a candidate protocol or workload;
  - DECISION S03-D2: splitting rule stating when roles, modes, speed grades and variants are separate entries;
  - DECISION S03-D3: the stratum re-enumerated independently for the gate;
  - protocol corpus (one entry per protocol, per role, per mode or variant per S03-D2, each with its normative source record and version);
  - workload definitions (the transactions or sequences per entry, with the normative clause each is drawn from);
  - undefined workload record: per F5 protocol, the workloads the organizer's statement leaves undefined;
  - exclusion log (every candidate considered and excluded, with its criterion code);
  - enumeration coverage record (comparison of the enumerated population against every catalogue of the venue list, coverage per catalogue as OBSERVATIONs);
  - query log entries; saturation record.
- Gate G03:
  - every corpus entry cites a Tier 1 source with locator; where the Tier 1 source is unretrievable the entry is marked KNOWN-UNRETRIEVED and cannot enter the dataset;
  - S03-D1 was recorded before the corpus index was closed (timestamps in order);
  - roles, modes and variants are separate entries per S03-D2, applied uniformly across the corpus;
  - every excluded candidate is in the exclusion log with a criterion code; no exclusion reason refers to an implementation consideration;
  - every F5 protocol is either present as an ordinary member or in the exclusion log with a criterion code; none has special status;
  - the undefined workload record exists for every F5 protocol;
  - the enumeration coverage record exists for every catalogue of the venue list;
  - a second person applying S03-D1 to the stratum of S03-D3 produces the same entry list;
  - saturation is declared for [RQ-13](RESEARCH_QUESTIONS.md#rq-13-enumeration-of-the-protocol-population).
- Serves: [RQ-13](RESEARCH_QUESTIONS.md#rq-13-enumeration-of-the-protocol-population), [RQ-14](RESEARCH_QUESTIONS.md#rq-14-roles-modes-and-variants-as-corpus-entries), [RQ-15](RESEARCH_QUESTIONS.md#rq-15-definition-of-a-workload), [RQ-17](RESEARCH_QUESTIONS.md#rq-17-detection-of-familiarity-bias).

### S04 Feature schema

- Days 8 to 11 (2026-09-24 to 2026-09-27).
- Objective: define the architecture-independent features that describe every corpus entry, with units and extraction rules.
- Inputs: the corpus of S03; the constraints register of S01 (for the timing and I/O envelope the features must be able to express); the documented dimension list of S02 (for dimensions that sources expose, never for their solutions).
- Outputs:
  - feature schema: per field a name, a definition, a unit or value domain, allowed values, an extraction rule citing where in a normative document the value is read, a marker stating whether the source constrains the value or leaves it to implementations or tolerances, and a written YES or NO answer to "does the value change if the implementation changes?" with justification;
  - metric candidate list derived from the schema, labelled candidate;
  - schema change log.
- Gate G04:
  - every field has every schema element listed above;
  - every field's independence answer is NO; a field answered YES is removed;
  - two persons extract the same corpus entry independently using the schema; differences are resolved per the double-extraction rule of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#structured-extraction);
  - no field is a weight, a score or a threshold;
  - the schema is versioned and the version is referenced by the extractions.
- Serves: [RQ-10](RESEARCH_QUESTIONS.md#rq-10-architecture-independent-dimensions-of-a-protocol), [RQ-11](RESEARCH_QUESTIONS.md#rq-11-source-fixed-versus-implementation-defined-values), [RQ-12](RESEARCH_QUESTIONS.md#rq-12-timing-quantities-of-each-protocol).

### S05 Dataset

- Days 11 to 13 (2026-09-27 to 2026-09-29).
- Objective: populate the schema for every corpus entry from normative sources, and withhold the holdout partition before any reduction runs.
- Inputs: the corpus of S03; the schema of S04 at its frozen version.
- Outputs:
  - dataset (one row per corpus entry, every cell with a value and a claim identifier, or NOT STATED with the source record searched);
  - dataset provenance table;
  - missing-value register (every NOT STATED cell with the queries run to find it);
  - seed position observation: where the F5 protocols sit in the feature space relative to the rest of the corpus, as an OBSERVATION with procedure;
  - DECISION S05-D1: holdout partition rule and the resulting holdout identifiers, recorded before S06 opens.
- Gate G05:
  - every cell of the dataset traces to a claim identifier or is NOT STATED with the source record searched;
  - no cell holds an assumed value, per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#absence-of-information);
  - the dataset schema version equals the S04 frozen version;
  - the double-extraction set of S00-D5 is met and the double extractions agree after rule correction;
  - S05-D1 is dated before any S06 computation record;
  - the dataset version and hash are recorded; later corrections create a new version.
- Serves: [RQ-11](RESEARCH_QUESTIONS.md#rq-11-source-fixed-versus-implementation-defined-values), [RQ-12](RESEARCH_QUESTIONS.md#rq-12-timing-quantities-of-each-protocol), [RQ-17](RESEARCH_QUESTIONS.md#rq-17-detection-of-familiarity-bias), [RQ-18](RESEARCH_QUESTIONS.md#rq-18-construction-of-the-holdout-set).

### S06 Reduction and redundancy

- Days 13 to 15 (2026-09-29 to 2026-10-01).
- Objective: evaluate candidate reduction methods on the non-holdout part of the dataset and select, by DECISION with recorded rationale, the method used to remove redundancy.
- Inputs: the dataset of S05 minus the holdout partition of S05-D1; the candidate method families of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#statistical-and-data-methods-to-study-later).
- Outputs:
  - reduction report (methods evaluated, parameters, seeds, results as OBSERVATIONs);
  - DECISION S06-D1: the selected method and every parameter value, with rationale and alternatives;
  - reduced dataset with the mapping from every removed entry to the entry that represents it and the computed reason;
  - coverage report: per schema field, the coverage of the field's value range by the reduced dataset relative to the full non-holdout dataset (no threshold asserted at this stage);
  - limitation register entries for every limit found.
- Gate G06:
  - every evaluated method has a documented procedure, parameters, seeds and result recorded as OBSERVATIONs, or a recorded reason for not evaluating it;
  - S06-D1 exists with rationale and alternatives and names no implementation consideration;
  - every removed entry maps to a retained entry with a computed reason; no entry was removed or added by hand;
  - the coverage report exists for every schema field;
  - a second person regenerates the reduced dataset from the dataset version and the reduction report and obtains the same result.
- Serves: [RQ-25](RESEARCH_QUESTIONS.md#rq-25-redundancy-reduction-methods-for-the-corpus), [RQ-26](RESEARCH_QUESTIONS.md#rq-26-reproducible-selection-of-the-benchmark-subset).

### S07 Representative benchmark

- Days 15 to 17 (2026-10-01 to 2026-10-03).
- Objective: derive the benchmark subset, the representativeness measure, the metric set with measurement procedures, and the pre-registered comparison criteria, all from the reduced dataset and the constraints register.
- Inputs: the reduced dataset of S06; the constraints register; the metric candidate list of S04; the technology observation record of S01.
- Outputs:
  - benchmark specification (entries with trace to the reduced dataset, the workload of each, the pass condition of each stated in terms of the feature schema and the constraints register, the measurement conditions, and the list of pending open questions with how the benchmark stays valid under each pending alternative);
  - DECISION S07-D1: representativeness measure, defined in schema terms, with alternatives; representativeness record with the OBSERVATION of the measure on the benchmark subset;
  - metric table (name, definition, unit, measurement procedure naming tool class, inputs, outputs and conditions, one executed demonstration involving no candidate architecture, research question served);
  - organizer interest record: per stated interest of [F13](PROJECT_SCOPE.md#organizer-facts), either a metric row or a recorded statement that no measurable criterion is derivable;
  - DECISION S07-D2: aggregation or weighting of metrics, if any; absence of aggregation is also recorded;
  - DECISION S07-D3: Pareto criteria pre-registration (axes, direction, dominance rule, independence justification per axis), recorded before any candidate exists;
  - DECISION S07-D4: comparison protocol for later candidates (fixed benchmark version, blinding where possible, order of evaluation).
- Gate G07:
  - every benchmark entry traces to the reduced dataset and to S06-D1;
  - every pass condition is expressed only with schema fields and constraints register entries; none refers to an implementation;
  - S07-D1 exists and the representativeness OBSERVATION is recorded with its procedure;
  - every metric has a unit, a procedure, its conditions and one executed demonstration on the corpus or, where S01-D1 permits, on the unmodified-template flow run;
  - no metric uses a value attributed to an open question that is not ANSWERED, except through an ASSUMPTION DECISION named in the specification;
  - every use of a CTR-01 value complies with [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#contradictions);
  - S07-D2, S07-D3 and S07-D4 are dated and list no candidate architecture;
  - the specification lists every pending open question it depends on and how it stays valid under each pending alternative.
- Serves: [RQ-16](RESEARCH_QUESTIONS.md#rq-16-definition-and-measurement-of-representativeness), [RQ-22](RESEARCH_QUESTIONS.md#rq-22-metric-set-for-the-benchmark), [RQ-23](RESEARCH_QUESTIONS.md#rq-23-area-measurement-procedure-on-the-target-flow), [RQ-24](RESEARCH_QUESTIONS.md#rq-24-measurability-of-organizer-interest-statements), [RQ-32](RESEARCH_QUESTIONS.md#rq-32-axes-of-the-pareto-front), [RQ-33](RESEARCH_QUESTIONS.md#rq-33-bias-resistant-comparison-protocol).

### S08 Verification methodologies

- Days 12 to 17 (2026-09-28 to 2026-10-03), in parallel with S05 to S07.
- Objective: catalogue the verification methodologies applicable to a device whose supported protocols are defined after fabrication, the conformance testing available from normative sources, and an architecture-independent verification workload per benchmark entry.
- Inputs: [F15](PROJECT_SCOPE.md#organizer-facts); the Tiny Tapeout flow facts [T2](PROJECT_SCOPE.md#tiny-tapeout-facts); the question-log state of [OQ-07](PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests), [OQ-09](PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol) and [OQ-26](PROJECT_SCOPE.md#oq-26-expected-verification-framework); the corpus of S03 for conformance sources; the benchmark specification as it stabilizes; Tier 1 to Tier 3 sources.
- Outputs:
  - verification methodology catalogue (methodology, sources, documented uses, prerequisites and inputs, what it can and cannot establish, cost dimensions to record when applied, acceptance criteria to be met when it is applied);
  - conformance source table (per benchmark entry, the normative test procedures or timing tables that define pin-level conformance, or NOT STATED with the search logged);
  - verification workload definition per benchmark entry (reference behaviour, stimulus classes, checker requirements, roles covered, observation level, with pending alternatives where OQ-09 is not ANSWERED);
  - saturation record.
- Gate G08:
  - every catalogue entry cites at least one source with locator for every claim of applicability; each of the three technique families named in F15 has a recorded evaluation, either an entry or a recorded reason why it is not applicable;
  - every methodology lists inputs that presuppose no microarchitecture;
  - every benchmark entry has a conformance source or is NOT STATED with the search logged;
  - every verification workload definition traces to normative clauses; a definition depending on an unanswered open question carries every pending alternative;
  - the catalogue recommends no architecture and no design flow choice; it states acceptance criteria only;
  - saturation is declared for each research question of group G.
- Serves: [RQ-28](RESEARCH_QUESTIONS.md#rq-28-verification-methodologies-applicable-to-the-problem), [RQ-29](RESEARCH_QUESTIONS.md#rq-29-pin-level-conformance-testing-from-normative-sources), [RQ-30](RESEARCH_QUESTIONS.md#rq-30-requirements-of-the-tiny-tapeout-verification-pipeline), [RQ-31](RESEARCH_QUESTIONS.md#rq-31-verification-workload-per-benchmark-entry).

### S09 Holdout and sensitivity audit

- Days 18 to 19 (2026-10-04 to 2026-10-05).
- Objective: test the benchmark against the entries withheld by S05-D1 and against perturbations of the dataset and of the reduction parameters, with the acceptance conditions fixed before the audit runs.
- Inputs: the dataset of S05 with the holdout partition of S05-D1; the benchmark specification of S07; the reduction report and S06-D1; the candidate sensitivity methods of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#statistical-and-data-methods-to-study-later).
- Outputs:
  - DECISION S09-D1: holdout scoring procedure and acceptance conditions, dated before the first audit run;
  - DECISION S09-D2: stability measure for the sensitivity audit and its acceptable level, dated before the first sensitivity run;
  - DECISION S09-D3: dominance rule under measurement uncertainty, contested values and MOVING_CONSTRAINT changes, with OBSERVATIONs on the constraints register values;
  - holdout audit report (procedure, score per holdout entry as OBSERVATION, verdict per condition);
  - sensitivity report (every perturbation applied: method family, parameters, feature subsets, seeds; effect on the selected subset; stability measure reported against S09-D2);
  - audit of the comparison protocol S07-D4 against its own acceptance conditions;
  - limitation register entries for every instability or coverage gap found.
- Gate G09:
  - S09-D1 and S09-D2 are dated before the first audit run;
  - every holdout entry has been scored by the documented procedure and the score is an OBSERVATION;
  - every perturbation and its result are recorded such that a second person can rerun them;
  - every instability or gap is in the limitation register; the benchmark change log shows no edit after the audit that is not justified by a recorded rerun;
  - S09-D3 exists and names no candidate architecture;
  - if a condition fails, the return path is recorded: back to S06 with a new DECISION, never a manual adjustment of entries; the slip rule applies.
- Serves: [RQ-18](RESEARCH_QUESTIONS.md#rq-18-construction-of-the-holdout-set), [RQ-27](RESEARCH_QUESTIONS.md#rq-27-stability-of-the-benchmark-under-corpus-perturbation), [RQ-33](RESEARCH_QUESTIONS.md#rq-33-bias-resistant-comparison-protocol), [RQ-34](RESEARCH_QUESTIONS.md#rq-34-dominance-under-uncertainty-and-moving-constraints).

### S10 Benchmark freeze

- Days 20 to 21 (2026-10-06 to 2026-10-07).
- Objective: freeze the benchmark and its dependencies as versioned, hashed artifacts, and submit the ARCHITECTURE GATE for evaluation.
- Inputs: every artifact of S01 to S09 at its final version.
- Outputs:
  - benchmark freeze record (artifact list, versions, content hashes, the DECISIONs and ASSUMPTIONs the benchmark depends on, the MOVING_CONSTRAINT entries it depends on with their monitoring channel and revisit trigger, the open questions still OPEN with their revisit triggers, the research questions still OPEN with their revisit triggers);
  - the final re-verification of every MOVING_CONSTRAINT;
  - reproduction OBSERVATION per S00-D6;
  - DECISION S10-D1: entry conditions that a future candidate must meet to be placed on the comparison at all.
- Gate G10: the [ARCHITECTURE GATE](PROJECT_SCOPE.md#architecture-gate) conditions AG-1 to AG-14, evaluated as specified there. This plan does not restate them.
- Serves: [RQ-09](RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze), [RQ-35](RESEARCH_QUESTIONS.md#rq-35-entry-conditions-for-a-future-candidate); closure of every research question that a stage above declared saturated, the remaining ones staying OPEN with their revisit trigger in the freeze record.

## Day-by-day schedule

| Day | Date | Active stages | Checkpoint |
| --- | --- | --- | --- |
| 1 | 2026-09-17 | S00 | Registers instantiated; S00-D1 to S00-D7 opened |
| 2 | 2026-09-18 | S00, S01 | G00 evaluated; contact plan questions sent |
| 3 | 2026-09-19 | S01 | Question log states recorded |
| 4 | 2026-09-20 | S01, S02 | Family catalogue opened |
| 5 | 2026-09-21 | S01, S02, S03 | G01 evaluated; S03-D1 recorded; corpus enumeration opened |
| 6 | 2026-09-22 | S02, S03 | |
| 7 | 2026-09-23 | S02, S03 | |
| 8 | 2026-09-24 | S02, S03, S04 | G02 evaluated; schema drafting opened |
| 9 | 2026-09-25 | S03, S04 | |
| 10 | 2026-09-26 | S03, S04 | G03 evaluated |
| 11 | 2026-09-27 | S04, S05 | G04 evaluated; dataset population opened |
| 12 | 2026-09-28 | S05, S08 | S05-D1 holdout partition recorded before S06 opens |
| 13 | 2026-09-29 | S05, S06, S08 | G05 evaluated; reduction evaluation opened |
| 14 | 2026-09-30 | S06, S08 | |
| 15 | 2026-10-01 | S06, S07, S08 | G06 evaluated; benchmark derivation opened |
| 16 | 2026-10-02 | S07, S08 | S07-D3 and S07-D4 drafted |
| 17 | 2026-10-03 | S07, S08 | Floor date (see [Calendar](#calendar)); G07 and G08 evaluated |
| 18 | 2026-10-04 | S09 | S09-D1 and S09-D2 recorded, then audit run |
| 19 | 2026-10-05 | S09 | G09 evaluated |
| 20 | 2026-10-06 | S10 | Freeze record assembled; MOVING_CONSTRAINTs re-verified; reproduction run |
| 21 | 2026-10-07 | S10 | ARCHITECTURE GATE evaluated; target end |
