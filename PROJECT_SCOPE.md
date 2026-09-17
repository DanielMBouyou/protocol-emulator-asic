# PROJECT_SCOPE

Canonical location for: the scope of PREBENCH, the temporary prohibition of microarchitectural choices and the scope of the HYPOTHESIS isolation rule, the note on deliberately absent architecture and RTL, the ARCHITECTURE GATE, and the challenge constraints as currently known with their contradictions and open questions. Other files link to the sections below and do not restate them.

## Scope of PREBENCH

PREBENCH is the phase that builds the measurable problem before any solution is searched for. Its calendar, stages, artifacts and gates are in [PREBENCH_PLAN.md](PREBENCH_PLAN.md); it ends only when the [ARCHITECTURE GATE](#architecture-gate) is passed.

| Belongs to PREBENCH | Does not belong to PREBENCH |
| --- | --- |
| Primary corpus: the retained primary and normative documents (challenge, technology, protocols, existing systems), collected under [RESEARCH_METHOD.md](RESEARCH_METHOD.md) and recorded under [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md) | Any choice covered by the [prohibition below](#temporary-prohibition-of-microarchitectural-choices) |
| Constraints: the register of challenge and technology constraints, each with status label and source ([below](#challenge-constraints-as-currently-known)) | RTL, HDL, netlists, firmware, toolchains, testbenches or an instruction set document for a candidate design |
| Workload and protocol space: the protocol population enumerated from normative sources and described by architecture-independent features | Synthesis, place-and-route or timing of a candidate design (see the flow characterization note below the table) |
| State of the art: existing programmable-I/O systems treated as families to investigate, with sourced claims on documented capabilities and costs, not ranked | Selecting protocols by intuition or familiarity; the benchmark is determined by the dataset and the documented reduction method |
| Benchmark methods: reduction of redundancy, selection of a representative subset, holdout and sensitivity audit | Metric weights, scores or thresholds fixed without a recorded DECISION |
| Verification methods: the catalogue of applicable verification methodologies with acceptance criteria, and the conformance sources per benchmark entry | Summaries of any product's internals; families are named only as families to investigate until stage S02 produces sourced claims |
| Metrics: measurable quantities with units and measurement procedures | Answering research questions inside [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md); answers live in the registers and stage artifacts |
| Provenance, deduplication and reproducibility of every record and computed result, per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md) | |
| Reproducible benchmark: a frozen, versioned specification that a second person regenerates from the dataset and the documented method | |
| Questions to the organizer and to Tiny Tapeout, logged per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log) | |

Flow characterization note: a run of the target flow on the unmodified template, with no HDL written by the team, whose only purpose is to observe what the flow provides (versions, cell library names, corners, reported area of the empty design, overheads), is permitted only if a DECISION at stage S01 authorizes it, and its result is recorded as an OBSERVATION, never as a FACT about the process.

## Temporary prohibition of microarchitectural choices

Until the [ARCHITECTURE GATE](#architecture-gate) is passed and recorded as a DECISION, no document, issue, artifact or register of this repository may choose, recommend, rank, compare in favour of, or imply:

- an instruction set or an instruction width;
- a CPU, processor type or execution model;
- a datapath, a pipeline, or a number of engines, cores or state machines;
- a memory organization, a memory technology choice, or an accelerator;
- a microarchitecture, a block diagram, or candidate RTL.

The organizer's framing of a protocol emulator ([F3](#organizer-facts)) is recorded as a fact about the challenge; it is not a project decision. How the reprogrammability required by [F4](#organizer-facts) is realized remains open until benchmark freeze. The organizer's advice on SRAM, synthesis and FPGA testing ([F16](#organizer-facts)) is recorded as advice; it does not select a memory technology or a flow for this project.

Violations are handled per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#hypothesis).

## HYPOTHESIS isolation scope

The definition of a HYPOTHESIS, the only locations where one may appear, and the rule that it is never presented as a conclusion are canonical in [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#hypothesis). This section fixes only what that rule covers in this project:

- every architectural idea listed in the [prohibition above](#temporary-prohibition-of-microarchitectural-choices);
- every conjecture about which protocols, features or workloads will dominate the benchmark;
- every conjecture about the judging beyond the organizer's printed words ([F13](#organizer-facts)).

Condition AG-12 of the [ARCHITECTURE GATE](#architecture-gate) audits this at freeze.

## Deliberately absent architecture and RTL

This repository contains no architecture directory, no RTL, no firmware, no testbench and no microarchitectural decision, by design, until benchmark freeze and the ARCHITECTURE GATE. Their absence is not an omission to be fixed by a contributor. Creating such content before the gate is passed is a violation of the [prohibition](#temporary-prohibition-of-microarchitectural-choices).

## ARCHITECTURE GATE

The architecture phase opens only when every condition below is MET. Conditions are evaluated per the gate rules of [PREBENCH_PLAN.md](PREBENCH_PLAN.md#rules-of-the-plan), by two verifiers. Any numeric threshold referenced by a condition must exist as a DECISION record dated before the gate review; a condition whose threshold has no such record is NOT MET. Sampling is not accepted for any condition; every check is exhaustive over the artifact it names.

| Id | Condition | How it is verified |
| --- | --- | --- |
| AG-1 | The floor date of [PREBENCH_PLAN.md](PREBENCH_PLAN.md#calendar) is reached or passed. | Date of the gate DECISION compared with the calendar. |
| AG-2 | The benchmark freeze record of [S10](PREBENCH_PLAN.md#s10-benchmark-freeze) exists, is versioned, and carries the content hash of every artifact it depends on. | Hashes recomputed by the verifiers match the record. |
| AG-3 | Every entry of the constraints register has a status label; every open question is in exactly one question-log state per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log); every OPEN_QUESTION that a benchmark artifact depends on has either a sourced answer (a claim from an included source, including a written organizer or Tiny Tapeout reply) or a DECISION of subtype ASSUMPTION with a revisit trigger and the list of dependent artifacts. | Scan of the constraints register for entries without a status label; scan of the question log for open questions with zero or several states; search of the constraints register, the benchmark specification and the metric table for values attributed to an OQ, where any such value without a claim identifier or an ASSUMPTION identifier fails the condition. |
| AG-4 | No benchmark entry, pass condition or metric procedure depends on picking one candidate value of a contradiction record that is still open per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#contradictions). | Search of the benchmark specification and the metric table for the subject of every open contradiction (for CTR-01: tile dimensions and area figures). |
| AG-5 | Every MOVING_CONSTRAINT of the constraints register has been re-verified within stage S10 with the date recorded, and every artifact that depends on one records the dependence. | Verification dates in the fact register fall within the S10 date range; dependence fields of the freeze record cross-checked. |
| AG-6 | Every protocol or workload entry of the corpus traces to at least one Tier 1 source record ([RESEARCH_METHOD.md](RESEARCH_METHOD.md#source-priority)) with locator; every excluded candidate is in the exclusion log with a criterion code; no KNOWN-UNRETRIEVED entry is in the dataset. | Exhaustive trace of every entry and every exclusion. |
| AG-7 | The feature schema passes the architecture-independence check of [S04](PREBENCH_PLAN.md#s04-feature-schema): no field presupposes an execution model, memory organization or instruction set. | Field-by-field review recorded in the schema artifact, with the written YES or NO independence answer per field. |
| AG-8 | The reduction and selection method is documented such that a second person, using only the dataset and the method description, regenerates the same benchmark subset. | The regeneration is performed by a verifier and its result recorded as an OBSERVATION. |
| AG-9 | The gate DECISION of [G09](PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) is recorded MET for the audit report version cited in the freeze record. | The G09 gate DECISION referenced by identifier; the audit report identifier and version it names match the freeze record. |
| AG-10 | Every row of the metric table of [S07](PREBENCH_PLAN.md#s07-representative-benchmark) is complete per its column list; any aggregation or weighting of metrics has a DECISION record with rationale and alternatives. | Metric table review; search for weights. |
| AG-11 | The verification methodology catalogue and the conformance source table of [S08](PREBENCH_PLAN.md#s08-verification-methodologies) exist, with acceptance criteria per methodology and a verification workload definition per benchmark entry. | Catalogue and table referenced by id and version. |
| AG-12 | Every statement labelled HYPOTHESIS anywhere in the repository has a hypothesis register entry, and no gate artifact, DECISION or metric depends on a HYPOTHESIS. | Search of every file for the label HYPOTHESIS, each hit matched to a register entry; search of gate artifacts, the decision log and the metric table for HYP identifiers and for the vocabulary of the [prohibition](#temporary-prohibition-of-microarchitectural-choices). |
| AG-13 | The Pareto comparison criteria and the comparison protocol for later architectures are pre-registered as DECISIONs before any candidate exists. | Decision log entries dated before the gate DECISION. |
| AG-14 | Every research question closed by a stage has a saturation record per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#stop-and-saturation-rule); the reproduction set fixed by DECISION at S00 has been re-run by a second person and compared per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#reproducibility), with differences recorded as OBSERVATIONs; every research question still OPEN is listed in the freeze record with its revisit trigger. | Saturation records, the reproduction OBSERVATION and the freeze record cross-checked against [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md). |

If any condition fails, the gate is not passed and the failing condition is recorded with the corrective stage; the schedule shifts per [PREBENCH_PLAN.md](PREBENCH_PLAN.md#slip-rule).

## Challenge constraints as currently known

All entries were verified on 2026-09-15 against the cited URL. Status labels (CONFIRMED_FACT, MOVING_CONSTRAINT, OPEN_QUESTION) and their re-verification rule are defined in [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#status-labels). The identifiers F, T, I, CTR, OBS-B and OQ are bootstrap identifiers; at stage S00 each entry receives a canonical register identifier and this table records the mapping.

### Organizer facts

Source for all entries: https://blog.janestreet.com/protocol-emulator-asic-competition/ (published 2026-09-10).

| Id | Status | Statement |
| --- | --- | --- |
| F1 | CONFIRMED_FACT | Organizer is Jane Street; announcement post titled "Can you design a chip? Announcing the protocol emulator ASIC competition". |
| F2 | CONFIRMED_FACT | Task statement: "Design an open-source, general-purpose protocol emulator ASIC." |
| F3 | CONFIRMED_FACT | The organizer describes a protocol emulator as "a tiny CPU with an instruction set designed for reading pins, writing pins, counting cycles, and hitting timing precisely enough that you can implement a real protocol in firmware" rather than in fixed logic. Recorded as the organizer's framing; not a project decision. |
| F4 | CONFIRMED_FACT | "Your chip should be reprogrammable enough to support new protocols after fabrication, within its timing and I/O constraints." Stated non-goal: a UART block, an SPI block and an I2C block on one die "and call it done". |
| F5 | CONFIRMED_FACT | Starting protocols: UART, SPI, I2C. Stretch goals: low-speed USB, 10 Mbit Ethernet. "Other interesting protocols to consider": JTAG, SWD, PS/2, CAN bus (suggestions, not requirements). |
| F6 | CONFIRMED_FACT and MOVING_CONSTRAINT | "We're targeting IHP's 130nm CMOS5L process through our friends at Tiny Tapeout." Fabrication targets the March 2027 CMOS5L Tiny Tapeout shuttle, "subject to the foundry schedule". |
| F7 | MOVING_CONSTRAINT | Stated starting point: the Tiny Tapeout CMOS5L Verilog template (github.com/TinyTapeout/ttihp-verilog-template, branch cmos5l) with "Set the tile size in info.yaml to 6x4". Whether the template or flow is mandatory is not stated ([OQ-01](#oq-01-template-obligation)). |
| F8 | MOVING_CONSTRAINT | "The current maximum area is 6x4 tiles per design. We are working on the possibility of scaling up to 8x4 tiles (~30% more area)." Organizer: approximately 200 um x 150 um per tile, "about 0.7 mm² of nominal tile area" for 6x4 (24 tiles). See [CTR-01](#recorded-contradictions). |
| F9 | CONFIRMED_FACT (organizer's rough estimate) | "budget for about 1K logic cells per tile". Basis (cell library, utilization) not stated ([OQ-15](#oq-15-basis-of-the-cells-per-tile-estimate)). |
| F10 | CONFIRMED_FACT | The submission "should be open source so others can use and build on it". No specific license named ([OQ-02](#oq-02-acceptable-licenses)). |
| F11 | CONFIRMED_FACT | Building in public before the deadline is allowed. Teams strongly recommended; no team-size limit stated ([OQ-06](#oq-06-eligibility-and-team-limits)). |
| F12 | MOVING_CONSTRAINT | "Submit your design by January 18th, 2027." A final submission form will be added to the page "closer to the deadline"; a sign-up form (Google Form) is used for updates. Contact: asic-competition@janestreet.com. Time zone and hardness of the deadline not stated ([OQ-05](#oq-05-deadline-time-zone-and-hardness)). |
| F13 | CONFIRMED_FACT | Jane Street will pay to tape out "the most novel designs" and is "particularly interested in projects with unique functionality, as well as those that demonstrate novel approaches to design and verification methodologies." No rubric, weights, jury or number of winners published ([OQ-12](#oq-12-judging-rubric-winners-and-weighting)). |
| F14 | CONFIRMED_FACT | Winners receive their fabricated chip mounted on a dev board. |
| F15 | CONFIRMED_FACT | Any HDL and verification techniques are welcome, "including formal methods, random constrained tests, AI-assisted verification". Jane Street uses Hardcaml internally; it is not required. |
| F16 | CONFIRMED_FACT (organizer advice, not rules) | SRAM may be more area-efficient than flip-flops for instruction memory; run synthesis early, check mapped cell area, leave room for clock tree buffers and routing, then full place-and-route and timing; FPGA testing suggested if available. |

### Tiny Tapeout facts

| Id | Status | Statement | Source |
| --- | --- | --- | --- |
| T1 | CONFIRMED_FACT | The template info.yaml fixes the pinout at 8 inputs ui[7:0], 8 outputs uo[7:0], 8 bidirectional uio[7:0] ("DO NOT delete or add any pins"), plus clk and active-low rst_n in the template module. Its tile-size comment is one claim of [CTR-01](#recorded-contradictions). | https://github.com/TinyTapeout/ttihp-verilog-template/blob/cmos5l/info.yaml |
| T2 | CONFIRMED_FACT | The template's GitHub Actions flow hardens with LibreLane through TinyTapeout/tt-gds-action@ihp-cmos5l with pdk ihp-sg13cmos5l; template license Apache-2.0. | Same repository, branch cmos5l |
| T3 | MOVING_CONSTRAINT | The Tiny Tapeout GPIO and clock specification pages document sky130 pads and the RP2040 demo-board clock (1 Hz to 66.5 MHz) and do not mention CMOS5L. CMOS5L IO electrical limits, maximum design clock, power budget, board and package are OPEN_QUESTION ([OQ-19](#oq-19-io-electrical-specification) to [OQ-23](#oq-23-board-and-package)). | https://tinytapeout.com/specs/gpio/ and https://tinytapeout.com/specs/clock/ |
| T4 | CONFIRMED_FACT | Tiny Tapeout IHP 0.4 was an experimental shuttle on sg13cmos5l with 64 projects (launched 27 March 2026). As of 2026-09-15 no March 2027 CMOS5L shuttle is listed on the runs page; the target shuttle exists only as the organizer's stated target ([OQ-30](#oq-30-listing-of-the-march-2027-shuttle)). | https://tinytapeout.com/chips/ttihp0p4/ and https://tinytapeout.com/runs/ |

### IHP PDK facts

| Id | Status | Statement | Source |
| --- | --- | --- | --- |
| I1 | CONFIRMED_FACT | IHP Open PDK is Apache-2.0; the main branch targets SG13G2 only; the CMOS5L PDK (ihp-sg13cmos5l) is on the dev branch, selected by the PDK environment variable. | https://github.com/IHP-GmbH/IHP-Open-PDK and https://github.com/IHP-GmbH/IHP-Open-PDK/blob/dev/README.md |
| I2 | CONFIRMED_FACT | SG13CMOS5L is a CMOS-only 0.13 um node of the same platform as SG13G2 without SiGe HBTs; 1.2 V thin-oxide logic and 3.3 V thick-oxide devices; 4 thin aluminium metals plus 1 thick top metal; no MIM capacitor. | https://github.com/IHP-GmbH/IHP-Open-PDK/blob/dev/README.md |
| I3 | MOVING_CONSTRAINT | IHP's dev README states the open-source PDK content is "preview only", not intended for production "at this moment", and CMOS5L models are not yet validated on CMOS5L silicon. | https://github.com/IHP-GmbH/IHP-Open-PDK/blob/dev/README.md |
| I4 | CONFIRMED_FACT | A standalone repository ihp-sg13cmos5l (Apache-2.0) exists and describes itself as temporary storage during migration-script development. | https://github.com/IHP-GmbH/ihp-sg13cmos5l |
| I5 | OPEN_QUESTION | SRAM macro availability and integration in the CMOS5L Tiny Tapeout flow; the Tiny Tapeout memory page documents only SG13G2 macros ([OQ-18](#oq-18-sram-availability)). | https://tinytapeout.com/specs/memory/ |

### Recorded contradictions

Contradictions are kept as they are, per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#contradictions).

| Id | Subject | Claim A | Claim B | Claim C | Resolution path |
| --- | --- | --- | --- | --- | --- |
| CTR-01 | Tile dimensions and valid tile sizes for CMOS5L | Template info.yaml comment: "A single tile is about 167x108 uM"; valid tiles "1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2" (https://github.com/TinyTapeout/ttihp-verilog-template/blob/cmos5l/info.yaml) | Organizer: approximately 200 um x 150 um per tile, and 6x4 ([F8](#organizer-facts)) | tt-support-tools branch ihp-sg13cmos5l tile_sizes.yaml: 1x1 = 202.08 x 154.98 um; 6x4 present with bounding box 1289.28 x 710.64 um; no 8x4 (https://raw.githubusercontent.com/TinyTapeout/tt-support-tools/ihp-sg13cmos5l/tech/ihp-sg13cmos5l/tile_sizes.yaml) | Ask the organizer and Tiny Tapeout; see [OQ-29](#oq-29-tile-dimensions-and-valid-tile-sizes) and [OQ-13](#oq-13-tile-budget-decision-date) |

### Bootstrap observations

Team computations are OBSERVATIONs per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#quantitative-data); they are not source statements.

| Id | Statement | Procedure | Inputs |
| --- | --- | --- | --- |
| OBS-B1 | The 6x4 bounding box of CTR-01 claim C has an area of 916,213.94 um², about 0.916 mm². This is a bounding-box area; no usable core area is derived from it. | Product of the two printed bounding-box dimensions (1289.28 um x 710.64 um), then conversion to mm² (division by 1,000,000), computed on 2026-09-15. | CTR-01 claim C. |

### Open questions

Each open question has a stable anchor and is an OPEN_QUESTION per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#status-labels). Its question-log state is tracked per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log). The research question that will address it is in [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md); the corresponding stage is in [PREBENCH_PLAN.md](PREBENCH_PLAN.md). None is answered here.

#### OQ-01 Template obligation
Is the Tiny Tapeout CMOS5L Verilog template and its flow (F7, T2) mandatory or only recommended?

#### OQ-02 Acceptable licenses
Which licenses satisfy "open source so others can use and build on it" (F10)?

#### OQ-03 Complete submission contents
What constitutes a complete submission: RTL, GDS, documentation, testbenches, or the firmware, toolchain and instruction set document that the organizer's framing mentions (F3), or a subset?

#### OQ-04 Submission channel
Is the submission made through the form announced on the blog page (F12), through app.tinytapeout.com, or both?

#### OQ-05 Deadline time zone and hardness
In which time zone is 2027-01-18 (F12) interpreted, and is the deadline hard?

#### OQ-06 Eligibility and team limits
Who is eligible, and is there a team-size limit (F11: no limit stated)?

#### OQ-07 Precheck and gate level tests
Are the Tiny Tapeout precheck and gate-level tests required for the competition submission (T2)?

#### OQ-08 Reuse of cores prior art and generated RTL
What are the rules on reusing existing cores, on prior art, and on AI-generated RTL?

#### OQ-09 Functional acceptance per protocol
What counts as supporting a protocol (F5): which rates, which roles (controller or peripheral, host or device), and at which simulation or silicon level?

#### OQ-10 Reprogramming mechanism and pin accounting
By which mechanism does the organizer expect a design to be reprogrammed after fabrication (F4), and do any pins used for it count against the pins fixed by T1?

#### OQ-11 Stretch protocols pads or external PHY
Are the stretch protocols (F5) expected directly from the pads or through an external PHY?

#### OQ-12 Judging rubric winners and weighting
What are the judging criteria, their weighting, the jury, and the number of winners (F13)?

#### OQ-13 Tile budget decision date
When will the 6x4 versus 8x4 question (F8) be decided?

#### OQ-14 Usable core area
What is the usable core area after power grid and routing overhead? Known inputs: the organizer's "about 0.7 mm² of nominal tile area" (F8) and the bounding-box area computed in OBS-B1 from CTR-01 claim C; neither is a usable-area value.

#### OQ-15 Basis of the cells per tile estimate
On which cell library and utilization is the estimate of about 1K logic cells per tile (F9) based?

#### OQ-16 Toolchain and PDK version pinning
Which toolchain and PDK versions will the shuttle use, and are they pinned?

#### OQ-17 Standard cell set and Liberty corners
Which CMOS5L standard-cell set and which Liberty corners are used by the shuttle flow?

#### OQ-18 SRAM availability
Are SRAM macros available and integrated in the CMOS5L Tiny Tapeout flow (I5)?

#### OQ-19 IO electrical specification
What are the CMOS5L IO electrical limits (T3)?

#### OQ-20 Clock source range and maximum design clock
What clock source, range and maximum design clock apply to CMOS5L designs (T3)?

#### OQ-21 Power budget
What power budget applies to a CMOS5L design on the shuttle (T3)?

#### OQ-22 Applicability of the sky130 pinout description
Does the sky130 pinout and GPIO description (T3) apply to CMOS5L?

#### OQ-23 Board and package
Which board and package will carry CMOS5L chips (T3, F14)?

#### OQ-24 Shuttle logistics and fallback
What are the shuttle logistics, and what is the fallback if the March 2027 shuttle slips (F6)?

#### OQ-25 PDK promotion from dev to main
When will the CMOS5L PDK be promoted from the dev branch to main (I1, I3)?

#### OQ-26 Expected verification framework
Is a particular verification framework expected or evaluated by the organizer (F15)?

#### OQ-27 Firmware toolchain and ISA document as deliverable
Are a firmware toolchain and an instruction set document expected as deliverables (F3, F4)?

#### OQ-28 Repository hosting and naming
Are there hosting or naming requirements for the submitted repository?

#### OQ-29 Tile dimensions and valid tile sizes
Which of the three tile descriptions in CTR-01 applies to the competition shuttle?

#### OQ-30 Listing of the March 2027 shuttle
When will the March 2027 CMOS5L shuttle targeted by the organizer (F6) be listed by Tiny Tapeout (T4)?
