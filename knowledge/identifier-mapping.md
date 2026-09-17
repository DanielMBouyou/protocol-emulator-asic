# Identifier mapping

Output of [S00](../PREBENCH_PLAN.md#s00-methodological-setup). The bootstrap identifiers used in [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known) mapped to canonical register identifiers, as [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers) requires.

The bootstrap identifiers F, T, I, CTR-01, OBS-B1 and OQ were scaffolding: they were written before any register existed. They are kept because PROJECT_SCOPE.md still uses them and because the corrections that S00 made to eleven of them are only legible against the original labels. They are not extended; new records take canonical identifiers only.

## Fact-bearing entries

Each bootstrap entry was re-entered as one or more claims. Claims where two operators independently confirmed the same reading were consolidated into proposed facts; the rest stay in the claim register. No proposed fact is CANONICAL, for the reason given in [fact-register.md](fact-register.md).

| Bootstrap | Claims | Where |
| --- | --- | --- |
| F1 | 5 (CLM-0001 to CLM-0005) | [claim-register-organizer.md](claim-register-organizer.md) |
| F10 | 2 (CLM-0006 to CLM-0007) | [claim-register-organizer.md](claim-register-organizer.md) |
| F11 | 5 (CLM-0008 to CLM-0012) | [claim-register-organizer.md](claim-register-organizer.md) |
| F12 | 8 (CLM-0013 to CLM-0020) | [claim-register-organizer.md](claim-register-organizer.md) |
| F13 | 7 (CLM-0021 to CLM-0027) | [claim-register-organizer.md](claim-register-organizer.md) |
| F14 | 2 (CLM-0028 to CLM-0029) | [claim-register-organizer.md](claim-register-organizer.md) |
| F15 | 4 (CLM-0030 to CLM-0033) | [claim-register-organizer.md](claim-register-organizer.md) |
| F16 | 14 (CLM-0034 to CLM-0047) | [claim-register-organizer.md](claim-register-organizer.md) |
| F2 | 1 (CLM-0048) | [claim-register-organizer.md](claim-register-organizer.md) |
| F3 | 3 (CLM-0049 to CLM-0051) | [claim-register-organizer.md](claim-register-organizer.md) |
| F4 | 4 (CLM-0052 to CLM-0055) | [claim-register-organizer.md](claim-register-organizer.md) |
| F5 | 5 (CLM-0056 to CLM-0060) | [claim-register-organizer.md](claim-register-organizer.md) |
| F6 | 2 (CLM-0061 to CLM-0062) | [claim-register-organizer.md](claim-register-organizer.md) |
| F7 | 3 (CLM-0063 to CLM-0065) | [claim-register-organizer.md](claim-register-organizer.md) |
| F8 | 6 (CLM-0066 to CLM-0071) | [claim-register-organizer.md](claim-register-organizer.md) |
| F9 | 4 (CLM-0072 to CLM-0075) | [claim-register-organizer.md](claim-register-organizer.md) |
| CTR-01-A | 4 (CLM-0076 to CLM-0079) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| CTR-01-C | 4 (CLM-0080 to CLM-0083) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| I5-SUPPORT | 11 (CLM-0084 to CLM-0094) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T1 | 10 (CLM-0095 to CLM-0104) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T1-GPIO | 10 (CLM-0105 to CLM-0114) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T2 | 9 (CLM-0115 to CLM-0123) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T2-LICENCE | 6 (CLM-0124 to CLM-0129) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T3 | 34 (CLM-0130 to CLM-0163) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| T4 | 17 (CLM-0164 to CLM-0180) | [claim-register-tinytapeout.md](claim-register-tinytapeout.md) |
| I1 | 5 (CLM-0181 to CLM-0185) | [claim-register-ihp.md](claim-register-ihp.md) |
| I1-DEV | 3 (CLM-0186 to CLM-0188) | [claim-register-ihp.md](claim-register-ihp.md) |
| I2 | 5 (CLM-0189 to CLM-0193) | [claim-register-ihp.md](claim-register-ihp.md) |
| I3 | 6 (CLM-0194 to CLM-0199) | [claim-register-ihp.md](claim-register-ihp.md) |
| I4 | 3 (CLM-0200 to CLM-0202) | [claim-register-ihp.md](claim-register-ihp.md) |

202 claims over 30 bootstrap entries. Source documents are SRC-0001 to SRC-0013 in [source-register.md](source-register.md).

## Other bootstrap entries

| Bootstrap | Canonical record |
| --- | --- |
| CTR-01 | [CTR-0001](contradiction-register.md#ctr-0001-tile-dimensions-and-valid-tile-sizes-for-cmos5l) |
| OBS-B1 | [OBS-0002](observation-register.md#obs-0002-bounding-box-area-of-a-6x4-cmos5l-tile-allocation) |

## Open questions

Each open question of PROJECT_SCOPE.md has a question log record and a contact plan entry. None has been sent, so none is in one of the three question-log states yet; that is gate G01's test, not G00's. OQ-31 was opened during S00 itself, when the re-extraction found that the Apache-2.0 attribution of bootstrap entry I4 rested on no claim record.

| Bootstrap | Question log | Contact plan |
| --- | --- | --- |
| [OQ-01](../PROJECT_SCOPE.md#oq-01-template-obligation) | QST-0001 | [OQ-01 Template obligation](contact-plan.md#oq-01-template-obligation) |
| [OQ-02](../PROJECT_SCOPE.md#oq-02-acceptable-licenses) | QST-0002 | [OQ-02 Acceptable licenses](contact-plan.md#oq-02-acceptable-licenses) |
| [OQ-03](../PROJECT_SCOPE.md#oq-03-complete-submission-contents) | QST-0003 | [OQ-03 Complete submission contents](contact-plan.md#oq-03-complete-submission-contents) |
| [OQ-04](../PROJECT_SCOPE.md#oq-04-submission-channel) | QST-0004 | [OQ-04 Submission channel](contact-plan.md#oq-04-submission-channel) |
| [OQ-05](../PROJECT_SCOPE.md#oq-05-deadline-time-zone-and-hardness) | QST-0005 | [OQ-05 Deadline time zone and hardness](contact-plan.md#oq-05-deadline-time-zone-and-hardness) |
| [OQ-06](../PROJECT_SCOPE.md#oq-06-eligibility-and-team-limits) | QST-0006 | [OQ-06 Eligibility and team limits](contact-plan.md#oq-06-eligibility-and-team-limits) |
| [OQ-07](../PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests) | QST-0007 | [OQ-07 Precheck and gate level tests](contact-plan.md#oq-07-precheck-and-gate-level-tests) |
| [OQ-08](../PROJECT_SCOPE.md#oq-08-reuse-of-cores-prior-art-and-generated-rtl) | QST-0008 | [OQ-08 Reuse of cores prior art and generated RTL](contact-plan.md#oq-08-reuse-of-cores-prior-art-and-generated-rtl) |
| [OQ-09](../PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol) | QST-0009 | [OQ-09 Functional acceptance per protocol](contact-plan.md#oq-09-functional-acceptance-per-protocol) |
| [OQ-10](../PROJECT_SCOPE.md#oq-10-reprogramming-mechanism-and-pin-accounting) | QST-0010 | [OQ-10 Reprogramming mechanism and pin accounting](contact-plan.md#oq-10-reprogramming-mechanism-and-pin-accounting) |
| [OQ-11](../PROJECT_SCOPE.md#oq-11-stretch-protocols-pads-or-external-phy) | QST-0011 | [OQ-11 Stretch protocols pads or external PHY](contact-plan.md#oq-11-stretch-protocols-pads-or-external-phy) |
| [OQ-12](../PROJECT_SCOPE.md#oq-12-judging-rubric-winners-and-weighting) | QST-0012 | [OQ-12 Judging rubric winners and weighting](contact-plan.md#oq-12-judging-rubric-winners-and-weighting) |
| [OQ-13](../PROJECT_SCOPE.md#oq-13-tile-budget-decision-date) | QST-0013 | [OQ-13 Tile budget decision date](contact-plan.md#oq-13-tile-budget-decision-date) |
| [OQ-14](../PROJECT_SCOPE.md#oq-14-usable-core-area) | QST-0014 | [OQ-14 Usable core area](contact-plan.md#oq-14-usable-core-area) |
| [OQ-15](../PROJECT_SCOPE.md#oq-15-basis-of-the-cells-per-tile-estimate) | QST-0015 | [OQ-15 Basis of the cells per tile estimate](contact-plan.md#oq-15-basis-of-the-cells-per-tile-estimate) |
| [OQ-16](../PROJECT_SCOPE.md#oq-16-toolchain-and-pdk-version-pinning) | QST-0016 | [OQ-16 Toolchain and PDK version pinning](contact-plan.md#oq-16-toolchain-and-pdk-version-pinning) |
| [OQ-17](../PROJECT_SCOPE.md#oq-17-standard-cell-set-and-liberty-corners) | QST-0017 | [OQ-17 Standard cell set and Liberty corners](contact-plan.md#oq-17-standard-cell-set-and-liberty-corners) |
| [OQ-18](../PROJECT_SCOPE.md#oq-18-sram-availability) | QST-0018 | [OQ-18 SRAM availability](contact-plan.md#oq-18-sram-availability) |
| [OQ-19](../PROJECT_SCOPE.md#oq-19-io-electrical-specification) | QST-0019 | [OQ-19 IO electrical specification](contact-plan.md#oq-19-io-electrical-specification) |
| [OQ-20](../PROJECT_SCOPE.md#oq-20-clock-source-range-and-maximum-design-clock) | QST-0020 | [OQ-20 Clock source range and maximum design clock](contact-plan.md#oq-20-clock-source-range-and-maximum-design-clock) |
| [OQ-21](../PROJECT_SCOPE.md#oq-21-power-budget) | QST-0021 | [OQ-21 Power budget](contact-plan.md#oq-21-power-budget) |
| [OQ-22](../PROJECT_SCOPE.md#oq-22-applicability-of-the-sky130-pinout-description) | QST-0022 | [OQ-22 Applicability of the sky130 pinout description](contact-plan.md#oq-22-applicability-of-the-sky130-pinout-description) |
| [OQ-23](../PROJECT_SCOPE.md#oq-23-board-and-package) | QST-0023 | [OQ-23 Board and package](contact-plan.md#oq-23-board-and-package) |
| [OQ-24](../PROJECT_SCOPE.md#oq-24-shuttle-logistics-and-fallback) | QST-0024 | [OQ-24 Shuttle logistics and fallback](contact-plan.md#oq-24-shuttle-logistics-and-fallback) |
| [OQ-25](../PROJECT_SCOPE.md#oq-25-pdk-promotion-from-dev-to-main) | QST-0025 | [OQ-25 PDK promotion from dev to main](contact-plan.md#oq-25-pdk-promotion-from-dev-to-main) |
| [OQ-26](../PROJECT_SCOPE.md#oq-26-expected-verification-framework) | QST-0026 | [OQ-26 Expected verification framework](contact-plan.md#oq-26-expected-verification-framework) |
| [OQ-27](../PROJECT_SCOPE.md#oq-27-firmware-toolchain-and-isa-document-as-deliverable) | QST-0027 | [OQ-27 Firmware toolchain and ISA document as deliverable](contact-plan.md#oq-27-firmware-toolchain-and-isa-document-as-deliverable) |
| [OQ-28](../PROJECT_SCOPE.md#oq-28-repository-hosting-and-naming) | QST-0028 | [OQ-28 Repository hosting and naming](contact-plan.md#oq-28-repository-hosting-and-naming) |
| [OQ-29](../PROJECT_SCOPE.md#oq-29-tile-dimensions-and-valid-tile-sizes) | QST-0029 | [OQ-29 Tile dimensions and valid tile sizes](contact-plan.md#oq-29-tile-dimensions-and-valid-tile-sizes) |
| [OQ-30](../PROJECT_SCOPE.md#oq-30-listing-of-the-march-2027-shuttle) | QST-0030 | [OQ-30 Listing of the March 2027 shuttle](contact-plan.md#oq-30-listing-of-the-march-2027-shuttle) |
| [OQ-31](../PROJECT_SCOPE.md#oq-31-licence-of-the-standalone-cmos5l-repository) | QST-0031 | [OQ-31 Licence of the standalone CMOS5L repository](contact-plan.md#oq-31-licence-of-the-standalone-cmos5l-repository) |

31 open questions, QST-0001 to QST-0031.

