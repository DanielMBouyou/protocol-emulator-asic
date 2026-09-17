# Stage to question coverage map

Output of [S00](../PREBENCH_PLAN.md#s00-methodological-setup). Derived from the `Serves` line of each stage in [PREBENCH_PLAN.md](../PREBENCH_PLAN.md) and the `Addressed in` line of each question in [RESEARCH_QUESTIONS.md](../RESEARCH_QUESTIONS.md). The plan requires the two to agree; this map is the record that they do.

This file is derived, not authored. When a `Serves` or `Addressed in` line changes, this map is regenerated and the gate condition is re-checked; it is never edited on its own.

## Stage to questions

| Stage | Title | Serves |
| --- | --- | --- |
| [S00](../PREBENCH_PLAN.md#s00-methodological-setup) | Methodological setup | none; S00 fixes the method and answers no research question |
| [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) | Challenge and PDK constraints | [RQ-01](../RESEARCH_QUESTIONS.md#rq-01-submission-rules-and-eligibility), [RQ-02](../RESEARCH_QUESTIONS.md#rq-02-functional-acceptance-and-protocol-scope), [RQ-03](../RESEARCH_QUESTIONS.md#rq-03-judging-criteria), [RQ-04](../RESEARCH_QUESTIONS.md#rq-04-area-budget-and-tile-geometry), [RQ-05](../RESEARCH_QUESTIONS.md#rq-05-technology-flow-and-pdk-status), [RQ-06](../RESEARCH_QUESTIONS.md#rq-06-electrical-clock-power-and-board-constraints), [RQ-07](../RESEARCH_QUESTIONS.md#rq-07-schedule-and-shuttle-risk), [RQ-08](../RESEARCH_QUESTIONS.md#rq-08-verification-and-software-deliverable-expectations), [RQ-09](../RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze), [RQ-23](../RESEARCH_QUESTIONS.md#rq-23-area-measurement-procedure-on-the-target-flow), [RQ-30](../RESEARCH_QUESTIONS.md#rq-30-requirements-of-the-tiny-tapeout-verification-pipeline) |
| [S02](../PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art) | Programmable IO state of the art | [RQ-19](../RESEARCH_QUESTIONS.md#rq-19-inventory-of-programmable-io-families), [RQ-20](../RESEARCH_QUESTIONS.md#rq-20-documented-protocol-coverage-per-family), [RQ-21](../RESEARCH_QUESTIONS.md#rq-21-published-cost-figures-per-family) |
| [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) | Protocol and workload corpus | [RQ-13](../RESEARCH_QUESTIONS.md#rq-13-enumeration-of-the-protocol-population), [RQ-14](../RESEARCH_QUESTIONS.md#rq-14-roles-modes-and-variants-as-corpus-entries), [RQ-15](../RESEARCH_QUESTIONS.md#rq-15-definition-of-a-workload), [RQ-17](../RESEARCH_QUESTIONS.md#rq-17-detection-of-familiarity-bias) |
| [S04](../PREBENCH_PLAN.md#s04-feature-schema) | Feature schema | [RQ-10](../RESEARCH_QUESTIONS.md#rq-10-architecture-independent-dimensions-of-a-protocol), [RQ-11](../RESEARCH_QUESTIONS.md#rq-11-source-fixed-versus-implementation-defined-values), [RQ-12](../RESEARCH_QUESTIONS.md#rq-12-timing-quantities-of-each-protocol) |
| [S05](../PREBENCH_PLAN.md#s05-dataset) | Dataset | [RQ-11](../RESEARCH_QUESTIONS.md#rq-11-source-fixed-versus-implementation-defined-values), [RQ-12](../RESEARCH_QUESTIONS.md#rq-12-timing-quantities-of-each-protocol), [RQ-17](../RESEARCH_QUESTIONS.md#rq-17-detection-of-familiarity-bias), [RQ-18](../RESEARCH_QUESTIONS.md#rq-18-construction-of-the-holdout-set) |
| [S06](../PREBENCH_PLAN.md#s06-reduction-and-redundancy) | Reduction and redundancy | [RQ-25](../RESEARCH_QUESTIONS.md#rq-25-redundancy-reduction-methods-for-the-corpus), [RQ-26](../RESEARCH_QUESTIONS.md#rq-26-reproducible-selection-of-the-benchmark-subset) |
| [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) | Representative benchmark | [RQ-16](../RESEARCH_QUESTIONS.md#rq-16-definition-and-measurement-of-representativeness), [RQ-22](../RESEARCH_QUESTIONS.md#rq-22-metric-set-for-the-benchmark), [RQ-23](../RESEARCH_QUESTIONS.md#rq-23-area-measurement-procedure-on-the-target-flow), [RQ-24](../RESEARCH_QUESTIONS.md#rq-24-measurability-of-organizer-interest-statements), [RQ-32](../RESEARCH_QUESTIONS.md#rq-32-axes-of-the-pareto-front), [RQ-33](../RESEARCH_QUESTIONS.md#rq-33-bias-resistant-comparison-protocol) |
| [S08](../PREBENCH_PLAN.md#s08-verification-methodologies) | Verification methodologies | [RQ-28](../RESEARCH_QUESTIONS.md#rq-28-verification-methodologies-applicable-to-the-problem), [RQ-29](../RESEARCH_QUESTIONS.md#rq-29-pin-level-conformance-testing-from-normative-sources), [RQ-30](../RESEARCH_QUESTIONS.md#rq-30-requirements-of-the-tiny-tapeout-verification-pipeline), [RQ-31](../RESEARCH_QUESTIONS.md#rq-31-verification-workload-per-benchmark-entry) |
| [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) | Holdout and sensitivity audit | [RQ-18](../RESEARCH_QUESTIONS.md#rq-18-construction-of-the-holdout-set), [RQ-27](../RESEARCH_QUESTIONS.md#rq-27-stability-of-the-benchmark-under-corpus-perturbation), [RQ-33](../RESEARCH_QUESTIONS.md#rq-33-bias-resistant-comparison-protocol), [RQ-34](../RESEARCH_QUESTIONS.md#rq-34-dominance-under-uncertainty-and-moving-constraints) |
| [S10](../PREBENCH_PLAN.md#s10-benchmark-freeze) | Benchmark freeze | [RQ-09](../RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze), [RQ-35](../RESEARCH_QUESTIONS.md#rq-35-entry-conditions-for-a-future-candidate) |

## Questions to stages


### Group A: exact constraints of the challenge and the technology

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-01](../RESEARCH_QUESTIONS.md#rq-01-submission-rules-and-eligibility) | Submission rules and eligibility | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-02](../RESEARCH_QUESTIONS.md#rq-02-functional-acceptance-and-protocol-scope) | Functional acceptance and protocol scope | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-03](../RESEARCH_QUESTIONS.md#rq-03-judging-criteria) | Judging criteria | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-04](../RESEARCH_QUESTIONS.md#rq-04-area-budget-and-tile-geometry) | Area budget and tile geometry | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-05](../RESEARCH_QUESTIONS.md#rq-05-technology-flow-and-pdk-status) | Technology flow and PDK status | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-06](../RESEARCH_QUESTIONS.md#rq-06-electrical-clock-power-and-board-constraints) | Electrical clock power and board constraints | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-07](../RESEARCH_QUESTIONS.md#rq-07-schedule-and-shuttle-risk) | Schedule and shuttle risk | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-08](../RESEARCH_QUESTIONS.md#rq-08-verification-and-software-deliverable-expectations) | Verification and software deliverable expectations | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) |
| [RQ-09](../RESEARCH_QUESTIONS.md#rq-09-constraints-still-moving-at-freeze) | Constraints still moving at freeze | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints), [S10](../PREBENCH_PLAN.md#s10-benchmark-freeze) |

### Group B: architecture-independent dimensions of the protocol space

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-10](../RESEARCH_QUESTIONS.md#rq-10-architecture-independent-dimensions-of-a-protocol) | Architecture independent dimensions of a protocol | [S04](../PREBENCH_PLAN.md#s04-feature-schema) |
| [RQ-11](../RESEARCH_QUESTIONS.md#rq-11-source-fixed-versus-implementation-defined-values) | Source fixed versus implementation defined values | [S04](../PREBENCH_PLAN.md#s04-feature-schema), [S05](../PREBENCH_PLAN.md#s05-dataset) |
| [RQ-12](../RESEARCH_QUESTIONS.md#rq-12-timing-quantities-of-each-protocol) | Timing quantities of each protocol | [S04](../PREBENCH_PLAN.md#s04-feature-schema), [S05](../PREBENCH_PLAN.md#s05-dataset) |
| [RQ-13](../RESEARCH_QUESTIONS.md#rq-13-enumeration-of-the-protocol-population) | Enumeration of the protocol population | [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) |
| [RQ-14](../RESEARCH_QUESTIONS.md#rq-14-roles-modes-and-variants-as-corpus-entries) | Roles modes and variants as corpus entries | [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) |
| [RQ-15](../RESEARCH_QUESTIONS.md#rq-15-definition-of-a-workload) | Definition of a workload | [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus) |

### Group C: representativeness of the corpus

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-16](../RESEARCH_QUESTIONS.md#rq-16-definition-and-measurement-of-representativeness) | Definition and measurement of representativeness | [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) |
| [RQ-17](../RESEARCH_QUESTIONS.md#rq-17-detection-of-familiarity-bias) | Detection of familiarity bias | [S03](../PREBENCH_PLAN.md#s03-protocol-and-workload-corpus), [S05](../PREBENCH_PLAN.md#s05-dataset) |
| [RQ-18](../RESEARCH_QUESTIONS.md#rq-18-construction-of-the-holdout-set) | Construction of the holdout set | [S05](../PREBENCH_PLAN.md#s05-dataset), [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) |

### Group D: capabilities and costs of existing programmable-I/O systems

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-19](../RESEARCH_QUESTIONS.md#rq-19-inventory-of-programmable-io-families) | Inventory of programmable IO families | [S02](../PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art) |
| [RQ-20](../RESEARCH_QUESTIONS.md#rq-20-documented-protocol-coverage-per-family) | Documented protocol coverage per family | [S02](../PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art) |
| [RQ-21](../RESEARCH_QUESTIONS.md#rq-21-published-cost-figures-per-family) | Published cost figures per family | [S02](../PREBENCH_PLAN.md#s02-programmable-io-state-of-the-art) |

### Group E: relevant metrics

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-22](../RESEARCH_QUESTIONS.md#rq-22-metric-set-for-the-benchmark) | Metric set for the benchmark | [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) |
| [RQ-23](../RESEARCH_QUESTIONS.md#rq-23-area-measurement-procedure-on-the-target-flow) | Area measurement procedure on the target flow | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints), [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) |
| [RQ-24](../RESEARCH_QUESTIONS.md#rq-24-measurability-of-organizer-interest-statements) | Measurability of organizer interest statements | [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) |

### Group F: methods to reduce redundancy and build a benchmark

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-25](../RESEARCH_QUESTIONS.md#rq-25-redundancy-reduction-methods-for-the-corpus) | Redundancy reduction methods for the corpus | [S06](../PREBENCH_PLAN.md#s06-reduction-and-redundancy) |
| [RQ-26](../RESEARCH_QUESTIONS.md#rq-26-reproducible-selection-of-the-benchmark-subset) | Reproducible selection of the benchmark subset | [S06](../PREBENCH_PLAN.md#s06-reduction-and-redundancy) |
| [RQ-27](../RESEARCH_QUESTIONS.md#rq-27-stability-of-the-benchmark-under-corpus-perturbation) | Stability of the benchmark under corpus perturbation | [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) |

### Group G: verification methods suited to the problem

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-28](../RESEARCH_QUESTIONS.md#rq-28-verification-methodologies-applicable-to-the-problem) | Verification methodologies applicable to the problem | [S08](../PREBENCH_PLAN.md#s08-verification-methodologies) |
| [RQ-29](../RESEARCH_QUESTIONS.md#rq-29-pin-level-conformance-testing-from-normative-sources) | Pin level conformance testing from normative sources | [S08](../PREBENCH_PLAN.md#s08-verification-methodologies) |
| [RQ-30](../RESEARCH_QUESTIONS.md#rq-30-requirements-of-the-tiny-tapeout-verification-pipeline) | Requirements of the Tiny Tapeout verification pipeline | [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints), [S08](../PREBENCH_PLAN.md#s08-verification-methodologies) |
| [RQ-31](../RESEARCH_QUESTIONS.md#rq-31-verification-workload-per-benchmark-entry) | Verification workload per benchmark entry | [S08](../PREBENCH_PLAN.md#s08-verification-methodologies) |

### Group H: criteria to later compare architectures on a Pareto front

| Question | Title | Addressed in |
| --- | --- | --- |
| [RQ-32](../RESEARCH_QUESTIONS.md#rq-32-axes-of-the-pareto-front) | Axes of the Pareto front | [S07](../PREBENCH_PLAN.md#s07-representative-benchmark) |
| [RQ-33](../RESEARCH_QUESTIONS.md#rq-33-bias-resistant-comparison-protocol) | Bias resistant comparison protocol | [S07](../PREBENCH_PLAN.md#s07-representative-benchmark), [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) |
| [RQ-34](../RESEARCH_QUESTIONS.md#rq-34-dominance-under-uncertainty-and-moving-constraints) | Dominance under uncertainty and moving constraints | [S09](../PREBENCH_PLAN.md#s09-holdout-and-sensitivity-audit) |
| [RQ-35](../RESEARCH_QUESTIONS.md#rq-35-entry-conditions-for-a-future-candidate) | Entry conditions for a future candidate | [S10](../PREBENCH_PLAN.md#s10-benchmark-freeze) |

## Checks

| Check | Result |
| --- | --- |
| Research questions defined | 35 |
| Research questions with no stage | 0 |
| Research questions addressed in more than one stage | 8 |
| Stages S01 to S10 with no research question | 0 |
| Stage `Serves` entries not matched by an `Addressed in` entry | 0 |
| `Addressed in` entries not matched by a stage `Serves` entry | 0 |

S00 is excluded from the third and fourth checks by the gate condition itself, which names stages S01 to S10. S00 fixes the method and answers no research question.

