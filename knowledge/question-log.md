# Question log

Register `QST-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). The three states and what each requires are canonical in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#personal-communication-and-the-question-log).

Field list per record, in this order:

- **verbatim question**: the text as sent, which is the drafted text in [contact-plan.md](contact-plan.md) until it is sent
- **addressee**
- **channel**
- **date sent**
- **serves**: the open question and research question identifiers
- **state**: ANSWERED, ASKED or UNANSWERABLE_UNTIL
- **state history**: each check for a reply, with its date

At the close of [S00](../PREBENCH_PLAN.md#s00-methodological-setup) every record is opened but none is in a state yet, because no question has been sent. S00 drafts and assigns; [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) sends, and gate G01 requires every open question to be in exactly one of the three states. A record below carries NOT SENT in place of a state, which is not one of the three states and is why G01, not G00, is the gate that tests them.

| Record | Serves | Addressee and channel | Date sent | State |
| --- | --- | --- | --- | --- |
| QST-0001 | [OQ-01](../PROJECT_SCOPE.md#oq-01-template-obligation) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0002 | [OQ-02](../PROJECT_SCOPE.md#oq-02-acceptable-licenses) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0003 | [OQ-03](../PROJECT_SCOPE.md#oq-03-complete-submission-contents) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0004 | [OQ-04](../PROJECT_SCOPE.md#oq-04-submission-channel) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0005 | [OQ-05](../PROJECT_SCOPE.md#oq-05-deadline-time-zone-and-hardness) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0006 | [OQ-06](../PROJECT_SCOPE.md#oq-06-eligibility-and-team-limits) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0007 | [OQ-07](../PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0008 | [OQ-08](../PROJECT_SCOPE.md#oq-08-reuse-of-cores-prior-art-and-generated-rtl) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0009 | [OQ-09](../PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0010 | [OQ-10](../PROJECT_SCOPE.md#oq-10-reprogramming-mechanism-and-pin-accounting) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0011 | [OQ-11](../PROJECT_SCOPE.md#oq-11-stretch-protocols-pads-or-external-phy) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0012 | [OQ-12](../PROJECT_SCOPE.md#oq-12-judging-rubric-winners-and-weighting) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0013 | [OQ-13](../PROJECT_SCOPE.md#oq-13-tile-budget-decision-date) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0014 | [OQ-14](../PROJECT_SCOPE.md#oq-14-usable-core-area) | TT-GITHUB-ISSUE | NOT SENT | NOT SENT |
| QST-0015 | [OQ-15](../PROJECT_SCOPE.md#oq-15-basis-of-the-cells-per-tile-estimate) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0016 | [OQ-16](../PROJECT_SCOPE.md#oq-16-toolchain-and-pdk-version-pinning) | TT-GITHUB-ISSUE (TinyTapeout/tt-gds-action) | NOT SENT | NOT SENT |
| QST-0017 | [OQ-17](../PROJECT_SCOPE.md#oq-17-standard-cell-set-and-liberty-corners) | TT-GITHUB-ISSUE (TinyTapeout/tt-gds-action) | NOT SENT | NOT SENT |
| QST-0018 | [OQ-18](../PROJECT_SCOPE.md#oq-18-sram-availability) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0019 | [OQ-19](../PROJECT_SCOPE.md#oq-19-io-electrical-specification) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0020 | [OQ-20](../PROJECT_SCOPE.md#oq-20-clock-source-range-and-maximum-design-clock) | TT-GITHUB-ISSUE (TinyTapeout/ttihp-verilog-template) | NOT SENT | NOT SENT |
| QST-0021 | [OQ-21](../PROJECT_SCOPE.md#oq-21-power-budget) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0022 | [OQ-22](../PROJECT_SCOPE.md#oq-22-applicability-of-the-sky130-pinout-description) | TT-GITHUB-ISSUE (TinyTapeout/ttihp-verilog-template) | NOT SENT | NOT SENT |
| QST-0023 | [OQ-23](../PROJECT_SCOPE.md#oq-23-board-and-package) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0024 | [OQ-24](../PROJECT_SCOPE.md#oq-24-shuttle-logistics-and-fallback) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0025 | [OQ-25](../PROJECT_SCOPE.md#oq-25-pdk-promotion-from-dev-to-main) | IHP-GITHUB-ISSUE (IHP-GmbH/IHP-Open-PDK) | NOT SENT | NOT SENT |
| QST-0026 | [OQ-26](../PROJECT_SCOPE.md#oq-26-expected-verification-framework) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0027 | [OQ-27](../PROJECT_SCOPE.md#oq-27-firmware-toolchain-and-isa-document-as-deliverable) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0028 | [OQ-28](../PROJECT_SCOPE.md#oq-28-repository-hosting-and-naming) | ORGANIZER-EMAIL (asic-competition@janestreet.com) | NOT SENT | NOT SENT |
| QST-0029 | [OQ-29](../PROJECT_SCOPE.md#oq-29-tile-dimensions-and-valid-tile-sizes) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0030 | [OQ-30](../PROJECT_SCOPE.md#oq-30-listing-of-the-march-2027-shuttle) | TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools) | NOT SENT | NOT SENT |
| QST-0031 | [OQ-31](../PROJECT_SCOPE.md#oq-31-licence-of-the-standalone-cmos5l-repository) | REPO-OBSERVATION | NOT SENT | NOT SENT |

The verbatim question of each record is the drafted text under the matching heading of [contact-plan.md](contact-plan.md). When a question is sent, its text is copied into this register as sent, because a draft that was edited before sending would otherwise leave no record of what the addressee actually read.

