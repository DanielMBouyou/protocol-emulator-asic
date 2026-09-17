# Contradiction register

Register `CTR-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). How a contradiction is opened, what it does to the facts it touches, and the only way it may be resolved are canonical in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#contradictions). Nothing here is resolved by preference, recency, tier or plausibility.

Field list per record, in this order:

- **subject**: the shared subject and predicate the claims disagree about
- **claims**: one row per claim, each with its claim identifier, its source and what it prints
- **dimension of disagreement**
- **candidate causes**: each marked as a conjecture, none asserted
- **resolution path**: the party that can settle it, and how
- **effect while open**: what the project may and may not do with the contested value
- **state**: OPEN or RESOLVED, with the resolving claim when RESOLVED

## CTR-0001 Tile dimensions and valid tile sizes for CMOS5L

- **subject**: the dimensions of one Tiny Tapeout CMOS5L tile, and which tile sizes a design may select.
- **claims**:

  | Claim | Claim records | Source | What it prints |
  | --- | --- | --- | --- |
  | A | CLM-0076 to CLM-0079 | info.yaml on branch cmos5l of TinyTapeout/ttihp-verilog-template (SRC-0009) | a single tile is about 167x108 uM, and the valid tiles values are 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2, the largest being 8x2 |
  | B | CLM-0066 to CLM-0071 | the organizer's announcement page (SRC-0004) | approximately 200 um x 150 um per tile, a 6x4 maximum, 24 tiles, and about 0.7 mm2 of nominal tile area |
  | C | CLM-0080 to CLM-0083 | tile_sizes.yaml on branch ihp-sg13cmos5l of TinyTapeout/tt-support-tools (SRC-0013) | 1x1 is 202.08 x 154.98, a 6x4 entry exists with a bounding box of 1289.28 x 710.64, and no 8x4 entry exists |

- **dimension of disagreement**: two dimensions at once. First, the printed size of a single tile, where A gives roughly two thirds of the linear dimensions that B and C give. Second, which tile sizes are selectable, where A lists none taller than two rows, B instructs a 6x4, and C defines a 6x4 but no 8x4 although B says 8x4 is being worked on.
- **candidate causes**: each of the following is a conjecture and none is asserted. The template comment may predate the CMOS5L tile definitions and describe a different node. The three sources may describe different layers of the same thing, a drawn tile against a pitch against a bounding box including the surrounding structure. The valid list in the template may be a template-side restriction rather than a flow-side one. The organizer may be quoting a figure agreed with Tiny Tapeout that no public file yet prints.
- **resolution path**: Tiny Tapeout for A and C, which it publishes, and the organizer for B, which it publishes. Recorded as [OQ-29](../PROJECT_SCOPE.md#oq-29-tile-dimensions-and-valid-tile-sizes) with a drafted question and an assigned channel in [contact-plan.md](contact-plan.md#oq-29-tile-dimensions-and-valid-tile-sizes), and as [OQ-13](../PROJECT_SCOPE.md#oq-13-tile-budget-decision-date) for the 6x4 against 8x4 part. A resolution requires a new claim from a Tier 1 source or a written reply from the responsible party.
- **effect while open**: every use of a tile dimension or a tile area names CTR-0001, and any computation that depends on one runs once per candidate value and reports the spread as an OBSERVATION. No benchmark entry, pass condition or metric procedure may depend on picking one of A, B or C; condition AG-4 of the [ARCHITECTURE GATE](../PROJECT_SCOPE.md#architecture-gate) tests exactly that at freeze. [OBS-0002](observation-register.md#obs-0002-bounding-box-area-of-a-6x4-cmos5l-tile-allocation) computes an area from claim C alone and is scoped to claim C alone.
- **state**: OPEN
- **maps bootstrap entry**: CTR-01
