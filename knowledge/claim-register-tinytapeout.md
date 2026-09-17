# Claim register: Tiny Tapeout sources

An excerpt is verbatim source text. Where it contains markup that a renderer would reinterpret, it is wrapped in inline code so that every character is shown as the source prints it.

Part of the claim register, split by source group per [DEC-0011](decision-log.md#dec-0011-splitting-the-claim-register-by-source-group). Index and the meaning of the `double_extraction` field: [claim-register.md](claim-register.md).

Every record comes from the second S00 double extraction, [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule). Two operators read each source independently under the amended [atomic fact rule](../EVIDENCE_POLICY.md#atomic-fact-rule), and a third operator, which produced neither set, paired the claims. Read `double_extraction` before relying on any record.

`subject_tags` and `rq_ids` were assigned at consolidation from the vocabulary of [DEC-0007](decision-log.md#dec-0007-s00-d7-controlled-vocabulary-of-subject-tags), not by the extracting operators. They are retrieval keys, not evidence.


### CLM-0076

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 10, comment line immediately preceding the tiles key, first sentence
- **excerpt**: "# How many tiles your design occupies? A single tile is about 167x108 uM."
- **statement**: How many tiles your design occupies?
- **kind**: QUAL
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw file; printed as an interrogative comment and reproduced exactly as printed
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only (seq 13). Rule 16 did not require it: an interrogative asserts nothing, so it neither is asserted by the statement under examination nor contradicts, qualifies or conditions it - extracting it breaches rule 16's first direction. But rule 12 has no entry for an interrogative, which is why Op2 could file it as QUAL rather than discard it.
- **re-enters bootstrap entry**: CTR-01-A

### CLM-0077

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 10, comment line immediately preceding the tiles key, second sentence
- **excerpt**: "A single tile is about 167x108 uM."
- **statement**: A single tile is about 167x108 uM
- **kind**: QUANT
- **value**: about 167x108
- **unit**: uM
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw file; the precision qualifier about kept per rule 7; the printed unit symbol uM reproduced without translation per rule 4
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-A

### CLM-0078

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 11, tiles key under the project mapping
- **excerpt**: "tiles: "1x1"          # Valid values: 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2"
- **statement**: tiles is set to "1x1"
- **kind**: QUAL
- **value**: 1x1
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim from the raw file in the fixed frame of rule 6
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-A

### CLM-0079

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 11, trailing comment on the tiles key
- **excerpt**: "Valid values: 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2"
- **statement**: Valid values for tiles are 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2
- **kind**: QUAL
- **value**: 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - one predicate with a printed list, recorded as a single fact whose object is the list in printed order including the printed disjunction before the last item
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-A

### CLM-0080

- **source_id**: SRC-0013 (TT-TILESIZES)
- **locator**: line 1, first key of the mapping; the file has no header comment and begins with this line
- **excerpt**: "1x1: "0 0 202.08 154.98""
- **statement**: 1x1 is set to "0 0 202.08 154.98"
- **kind**: QUANT
- **value**: 0 0 202.08 154.98
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim; the file prints no unit for the four numbers, so DIMENSIONLESS, stated once for the file per rules 11 and 14
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0013
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-C

### CLM-0081

- **source_id**: SRC-0013 (TT-TILESIZES)
- **locator**: line 14, the 6x4 key, printed between the 6x2 and 8x1 entries
- **excerpt**: "6x4: "0 0 1289.28 710.64""
- **statement**: 6x4 is set to "0 0 1289.28 710.64"
- **kind**: QUANT
- **value**: 0 0 1289.28 710.64
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim from the raw file; no unit printed
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0013
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-C

### CLM-0082

- **source_id**: SRC-0013 (TT-TILESIZES)
- **locator**: whole file, all 16 lines, each line one key. Case-sensitive and case-insensitive search for 8x4 returned no matches; variants tried 8x4, 8X4. The keys printed are 1x1, 1x2, 2x1, 2x2, 3x1, 3x2, 3x4, 4x1, 4x2, 4x4, 5x4, 6x1, 6x2, 6x4, 8x1, 8x2.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The tile_sizes.yaml does not contain 8x4
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - deterministic substring search over the verbatim raw file; no excerpt exists because the token is absent
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0013
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: CTR-01-C

### CLM-0083

- **source_id**: SRC-0013 (TT-TILESIZES)
- **locator**: lines 1-16, the complete list of keys in file order
- **excerpt**: "1x1: "0 0 202.08 154.98" 1x2: "0 0 202.08 313.74" 2x1: "0 0 419.52 154.98" 2x2: "0 0 419.52 313.74" 3x1: "0 0 636.96 154.98" 3x2: "0 0 636.96 313.74" 3x4: "0 0 636.96 710.64" 4x1: "0 0 854.40 154.98" 4x2: "0 0 854.40 313.74" 4x4: "0 0 854.40 710.64" 5x4: "0 0 1071.84 710.64" 6x1: "0 0 1289.28 154.98" 6x2: "0 0 1289.28 313.74" 6x4: "0 0 1289.28 710.64" 8x1: "0 0 1724.16 154.98" 8x2: "0 0 1724.16 313.74""
- **statement**: The tile size keys printed are 1x1, 1x2, 2x1, 2x2, 3x1, 3x2, 3x4, 4x1, 4x2, 4x4, 5x4, 6x1, 6x2, 6x4, 8x1, 8x2
- **kind**: QUANT
- **value**: 16
- **unit**: keys
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - the file prints no total, so the count of 16 was obtained by enumerating the printed keys per rule 11; keys listed in printed order
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0013
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only (seq 26). Op2 puts the identical enumeration inside the locator of its ABSENCE claim instead of recording it as a claim. Rule 16's final sentence required the claim: a span quoted inside a locator is expressly to be recorded. Rule 17 does not shelter it - a key list is data, not provenance. Reciprocal of the T1/8 conflict where rule 17 did apply.
- **re-enters bootstrap entry**: CTR-01-C

### CLM-0084

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, first sentence
- **excerpt**: "IHP has several variations of SRAM macros which can be used in shuttles which they will manufacture (i.e. specifically being taped out with their PDK)."
- **statement**: IHP has several variations of SRAM macros which can be used in shuttles which they [IHP] will manufacture (i.e. specifically being taped out with their PDK)
- **kind**: QUAL
- **value**: several variations of SRAM macros
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified because its rendering returned the sentence without terminating punctuation
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0085

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, second sentence, first clause
- **excerpt**: "One of these macros, 1024x8, has been successfully taped out and tested to be working - read more about it in the ttihp0p2 SRAM (1024x8) test project datasheet."
- **statement**: One of these macros [SRAM macros], 1024x8, has been successfully taped out and tested to be working
- **kind**: QUAL
- **value**: 1024x8
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose clause extracted verbatim; the demonstrative these macros kept as printed with its referent from the preceding sentence per rule 5; the evaluative adverb successfully is the source's own per rule 9
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: it qualifies the preceding sentence both operators recorded by singling out which of the 'several variations' is proven. Coverage failure by Op2.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0086

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, third sentence, first clause
- **excerpt**: "The tables below are not exhaustive - you should visit IHP's PDK repository to see their full SRAM macro selection."
- **statement**: The tables below are not exhaustive
- **kind**: QUAL
- **value**: not exhaustive
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose clause extracted verbatim from the HTML markup
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as the span that most directly qualifies any claim about which macros the page lists - including Op2's own claim about the macro sections. Coverage failure by Op2.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0087

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, third sentence, second clause
- **excerpt**: "The tables below are not exhaustive - you should visit IHP's PDK repository to see their full SRAM macro selection."
- **statement**: you should visit IHP's PDK repository to see their [IHP's] full SRAM macro selection
- **kind**: RULE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: should
- **reading_confidence**: high - prose clause extracted verbatim; the deontic modal should governs the main predicate and is kept as printed per rule 8; the possessive their kept with its referent per rule 5
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as the continuation of the qualifying sentence at I5-SUPPORT/97. Rule 12 makes it a RULE (deontic modal). Coverage failure by Op2.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0088

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, the single-port and dual-port SRAM comparison tables, and the section headings naming the process
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: UNRESOLVED
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 medium, enumerating rows of the verbatim HTML tables; Op2 unverified, its rendering not reproducing the heading lines with their original formatting
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: They disagree about what the page prints in this section. Op1 records two enumerated QUANT claims - 12 single-port macros (256x8, 512x8, 1024x8, 256x16, 512x16, 1024x16, 256x32, 512x32, 1024x32, 256x48, 256x64, 512x64) and 9 dual-port macros (256x8, 512x8, 256x16, 512x16, 1024x16, 64x32, 256x32, 512x32, 1024x32) - naming the tables 'IHP SG13G2 single-port' and 'dual-port SRAM comparison table'. Op
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0089

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, the dual-port SRAM comparison table, SRAM macro column, all data rows in printed order
- **excerpt**: "256x8"
- **statement**: The IHP SG13G2 dual-port SRAM macros printed are 256x8, 512x8, 256x16, 512x16, 1024x16, 64x32, 256x32, 512x32, 1024x32
- **kind**: QUANT
- **value**: 9
- **unit**: SRAM macros
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - macro names taken verbatim from the HTML markup but their grouping under the process node comes from the table heading; the page prints no total, so the count of 9 was obtained by enumerating the printed rows per rule 11
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only; Op2 has no macro enumeration at all. Consequent orphan of the disagreement at I5-SUPPORT/99, and on Op2's side a rule-16 coverage failure if the statement under examination concerns which SRAM macros are available.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0090

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, footnote line printed immediately below each of the two SRAM comparison tables
- **excerpt**: "* = requires rotating macro by 90 degrees to fit"
- **statement**: * = requires rotating macro by 90 degrees to fit
- **kind**: QUANT
- **value**: 90
- **unit**: degrees
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - the same footnote line is printed identically below both tables and is recorded once as a single fact; reproduced verbatim including the asterisk key
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: the asterisk keys individual macro rows and qualifies whether those macros fit, conditioning any claim about macro availability. Op2 took nothing from the tables. Op1 also records one fact for a line printed twice - the aggregation question of T2/30, here resolved by identical values as at T2/35.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0091

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, For other PDKs section, first sentence
- **excerpt**: "For SkyWater shuttles, the density of memory macros is significantly lower."
- **statement**: For SkyWater shuttles, the density of memory macros is significantly lower
- **kind**: QUAL
- **value**: significantly lower
- **unit**: DIMENSIONLESS
- **conditions**: For SkyWater shuttles
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a rendering
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0092

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, For other PDKs section, second sentence, first clause
- **excerpt**: "There is an experimental 32x32 register file created by Sylvain Munaut which has a density of 1200 bits per tile - see the datasheet for more information."
- **statement**: There is an experimental 32x32 register file created by Sylvain Munaut which has a density of 1200 bits per tile
- **kind**: QUANT
- **value**: 1200
- **unit**: bits per tile
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose clause extracted verbatim; the descriptor experimental is the source's own per rule 9
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as the span qualifying the 'significantly lower' density claim both operators recorded, by giving the one concrete SkyWater figure. Coverage failure by Op2.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0093

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY body, Using pregenerated SRAM macros section, callout paragraph between the introductory sentences and the first table, third sentence
- **excerpt**: "The table below should be used as rough guidance only, and is subject to change at any time."
- **statement**: The table below should be used as rough guidance only, and is subject to change at any time
- **kind**: RULE
- **value**: rough guidance only
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: should
- **reading_confidence**: high - prose sentence extracted verbatim; the deontic modal should governs the main predicate and is kept as printed per rule 8
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it in the strongest terms: it qualifies every figure taken from the tables on this page and is printed as a callout rather than buried. Op2's rendering-only retrieval did not surface it. Coverage failure.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0094

- **source_id**: SRC-0011 (TT-MEMORY)
- **locator**: TT-MEMORY whole page as retrieved. Case-insensitive search for cmos5l; variants tried CMOS5L, cmos5l, sg13cmos5l; 0 matches. The only IHP process node named on the page is SG13G2.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The Memory page does not contain CMOS5L
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high, having searched the verbatim HTML source (98453 bytes including head metadata); Op2 unverified, having searched a rendering of the visible body and headings only
- **subject_tags**: TECH-MEMORY
- **rq_ids**: RQ-05
- **source_version**: see SRC-0011
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: The fourth instance of the T3/65 scope disagreement: same conclusion, incomparable evidence, and different names in the rule-15 frame ('The Memory page' versus 'The TT-MEMORY page'). Op1's whole-document search over the raw HTML settles it in favour of the stronger claim. Both note independently that the page's only IHP process node is SG13G2.
- **re-enters bootstrap entry**: I5-SUPPORT

### CLM-0095

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 22, comment line immediately preceding the pinout key, second sentence
- **excerpt**: "Leave unused pins blank."
- **statement**: Leave unused pins blank.
- **kind**: PROCEDURE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw file; printed imperative in a YAML comment; no unit printed, so DIMENSIONLESS
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0096

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 22, comment line immediately preceding the pinout key, third sentence
- **excerpt**: "DO NOT delete or add any pins."
- **statement**: DO NOT delete or add any pins.
- **kind**: PROCEDURE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - printed imperative in a YAML comment; capitalisation DO NOT reproduced as printed
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0097

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 23, second comment line immediately preceding the pinout key, first sentence
- **excerpt**: "This section is for the datasheet/website."
- **statement**: This section [pinout] is for the datasheet/website.
- **kind**: QUAL
- **value**: the datasheet/website
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - printed declarative comment; the deictic 'This section' kept as printed with its referent in square brackets per rule 5
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0098

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: line 23, second comment line preceding the pinout key, second sentence
- **excerpt**: "Use descriptive names (e.g., RX, TX, MOSI, SCL, SEG_A, etc.)."
- **statement**: Use descriptive names (e.g., RX, TX, MOSI, SCL, SEG_A, etc.).
- **kind**: PROCEDURE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - printed imperative in a YAML comment
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0099

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: lines 26-33, 36-43, 46-53: the pin key lines under the pinout key, grouped by the comments # Inputs (line 25), # Outputs (line 35) and # Bidirectional pins (line 45)
- **excerpt**: "ui[0]: """
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: QUAL
- **value**: ""
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - key/value lines reproduced verbatim from the raw file
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Disagreement about the unit of aggregation, which changes the claim count. Op1 emits three facts (seq 5,6,7 - one per printed block ui/uo/uio); Op2 emits one fact of 24 keys spanning all three blocks. The excerpts bearing on it are line 35 '  # Outputs' and line 45 '  # Bidirectional pins', comment lines physically interrupting the key run, which both operators acknowledge (Op1 in locators, Op2 in
- **re-enters bootstrap entry**: T1

### CLM-0100

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: lines 36-43, second block of keys under the pinout key, introduced by the # Outputs comment on line 35
- **excerpt**: "uo[0]: ""   uo[1]: ""   uo[2]: ""   uo[3]: ""   uo[4]: ""   uo[5]: ""   uo[6]: ""   uo[7]: """
- **statement**: uo[0], uo[1], uo[2], uo[3], uo[4], uo[5], uo[6], uo[7] are each set to ""
- **kind**: QUAL
- **value**: ""
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - eight instances of one key/value predicate printed together, recorded as one fact in printed order
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only (seq 6). Op2 has no counterpart because it merged all 24 pin keys into its seq 5. Consequent orphan of the aggregation disagreement at T1/5: rule 16 requires the uo keys to be covered, and Op2 does cover them inside a larger fact.
- **re-enters bootstrap entry**: T1

### CLM-0101

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: lines 46-53, third block of keys under the pinout key, introduced by the # Bidirectional pins comment on line 45
- **excerpt**: "uio[0]: ""   uio[1]: ""   uio[2]: ""   uio[3]: ""   uio[4]: ""   uio[5]: ""   uio[6]: ""   uio[7]: """
- **statement**: uio[0], uio[1], uio[2], uio[3], uio[4], uio[5], uio[6], uio[7] are each set to ""
- **kind**: QUAL
- **value**: ""
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - eight instances of one key/value predicate printed together, recorded as one fact in printed order
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only (seq 7). Same consequent orphan as T1/6, arising from the aggregation disagreement at T1/5.
- **re-enters bootstrap entry**: T1

### CLM-0102

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: lines 25, 35 and 45, the comment lines inside the pinout mapping, in printed order
- **excerpt**: "# Inputs"
- **statement**: The pinout mapping groups its pin keys under the printed comments "# Inputs", "# Outputs" and "# Bidirectional pins", in that printed order.
- **kind**: QUAL
- **value**: # Inputs, # Outputs, # Bidirectional pins
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-text retrieval of comment lines
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only (seq 6). Op1 records the same three comments inside its locators for seq 5/6/7 but not as claims. Rule 16's final sentence (every span quoted anywhere, including inside a locator, is itself recorded as a claim) required it, so on Op1's side the omission is a rule-16 breach; but rule 17 says a section heading or callout label stays in the locator unless the statement is about the document'
- **re-enters bootstrap entry**: T1

### CLM-0103

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: whole file. Case-sensitive and case-insensitive substring search for clk over every line including comments; variants tried clk, CLK, Clk; 0 matches. The only related strings printed are clock_hz and the comment word Clock.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The info.yaml does not contain clk
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - deterministic substring search over the verbatim raw file; no excerpt exists because the token is absent
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0104

- **source_id**: SRC-0009 (TT-INFOYAML)
- **locator**: whole file. Case-sensitive search for rst_n and case-insensitive searches for rst and reset over every line including comments; 0 matches. Variants tried: rst_n, RST_N, rst, reset.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The info.yaml does not contain rst_n
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - deterministic substring search over the verbatim raw file; no excerpt exists because the token is absent
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0009
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1

### CLM-0105

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, sentence introducing the pin table
- **excerpt**: "There are total of 26 I/O pins available for your design:"
- **statement**: There are total of 26 I/O pins available for your design
- **kind**: QUANT
- **value**: 26
- **unit**: I/O pins
- **conditions**: available for your design
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted from the verbatim HTML markup by tag stripping; wording unaltered
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only (seq 10). Rule 16 required it: the sentence conditions the pin table the statement under examination is about and prints the governing total. Op2's omission traces to its rendering-only retrieval, not to a rule gap.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0106

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, the row whose first cell is clk; columns in printed order Pin, Count, Direction, Description
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 medium from verbatim HTML with a read table structure; Op2 unverified from a markdown rendering per rule 19
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Disagreement on granularity and on what the source prints. Op1 emits three claims for the clk row (Count is 1 QUANT, Direction is Input QUAL, Description is Clock input DEFINITION), each with excerpt 'clk' - the row label, not the cell quoted. Op2 emits one row claim, excerpt 'clk | 1 | Input | Clock input', pipes admittedly a rendering artefact. Cell contents agree. What differs is whether a tabl
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0107

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, clk row, Direction column
- **excerpt**: "Input"
- **statement**: clk Direction is Input
- **kind**: QUAL
- **value**: Input
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 seq 12 has no separate Op2 counterpart; Op2 folds it into its row-level claim. Consequent orphan of the granularity disagreement at T1-GPIO/12.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0108

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, clk row, Description column
- **excerpt**: "Clock input"
- **statement**: clk Description is Clock input
- **kind**: DEFINITION
- **value**: Clock input
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 seq 13 only; folded into Op2's row-level claim. Consequent orphan of T1-GPIO/12.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0109

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, the row whose first cell is rst_n
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - medium (Op1, verbatim HTML) versus unverified (Op2, markdown rendering)
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: The T1-GPIO/12 disagreement repeated for the rst_n row: Op1 three cell claims, Op2 one row claim. Cell contents agree (1, Input, Active low reset). UNRESOLVED on the rule as written.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0110

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, rst_n row, Direction column
- **excerpt**: "Input"
- **statement**: rst_n Direction is Input
- **kind**: QUAL
- **value**: Input
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 seq 15 only; folded into Op2's row claim. Consequent orphan of T1-GPIO/15.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0111

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, pin table, rst_n row, Description column
- **excerpt**: "Active low reset"
- **statement**: rst_n Description is Active low reset
- **kind**: DEFINITION
- **value**: Active low reset
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 seq 16 only; folded into Op2's row claim. Consequent orphan of T1-GPIO/15.
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0112

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, paragraph immediately after the pin table, first sentence
- **excerpt**: "Internally, both the clk and rst_n pins are handled like any other input pins."
- **statement**: Internally, both the clk and rst_n pins are handled like any other input pins
- **kind**: QUAL
- **value**: handled like any other input pins
- **unit**: DIMENSIONLESS
- **conditions**: Internally
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a markdown rendering per rule 19
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0113

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, paragraph immediately after the pin table, second sentence
- **excerpt**: "However, they have special meaning to the Tiny Tapeout devkit."
- **statement**: However, they [the clk and rst_n pins] have special meaning to the Tiny Tapeout devkit
- **kind**: QUAL
- **value**: special meaning to the Tiny Tapeout devkit
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim; the pronoun they kept as printed with its referent from the preceding sentence per rule 5
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only (seq 18). Rule 16 required it: the sentence directly qualifies the immediately preceding sentence both operators extracted, and 'However' marks it as the qualification. Op2's omission breaches rule 16's second direction ('Do not stop short of it').
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0114

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: body, GPIO pins section, paragraph immediately after the pin table, third sentence
- **excerpt**: "For more information on the clk pin and input synchronization, see the Clock section."
- **statement**: For more information on the clk pin and input synchronization, see the Clock section.
- **kind**: PROCEDURE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: For more information on the clk pin and input synchronization
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a markdown rendering
- **subject_tags**: TECH-IO
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T1-GPIO

### CLM-0115

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: line 17, uses key of the Build GDS step in the gds job
- **excerpt**: "uses: TinyTapeout/tt-gds-action@ihp-cmos5l"
- **statement**: uses is set to "TinyTapeout/tt-gds-action@ihp-cmos5l"
- **kind**: QUAL
- **value**: TinyTapeout/tt-gds-action@ihp-cmos5l
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim; the value is printed unquoted and the quotation marks are the rule-6 frame, not part of the printed value
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T2

### CLM-0116

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: lines 17, 26, 38 and 47, the uses keys of the Build GDS step (gds job), the Run Tiny Tapeout Precheck step (precheck job), the GL test step (gl_test job) and the single step of the viewer job
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: QUAL
- **value**: UNRESOLVED
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value lines reproduced verbatim from the raw file
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Disagreement on how many facts the four uses lines yield. Op1 emits four separate key/value facts, one per line, same key different values. Op2 emits one aggregate fact listing all four values in printed order AND separately keeps the first line as its own fact, so the Build GDS reference is recorded twice. The four values agree exactly. Rule 1's 'repeated instances of one predicate printed togeth
- **re-enters bootstrap entry**: T2

### CLM-0117

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: line 26, uses key of the Run Tiny Tapeout Precheck step in the precheck job
- **excerpt**: "uses: TinyTapeout/tt-gds-action/precheck@ihp-cmos5l"
- **statement**: uses is set to "TinyTapeout/tt-gds-action/precheck@ihp-cmos5l"
- **kind**: QUAL
- **value**: TinyTapeout/tt-gds-action/precheck@ihp-cmos5l
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim from the raw file
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; Op2 covers the same value inside its aggregate (and quotes this very line as that claim's excerpt). Consequent orphan of the aggregation disagreement at T2/30.
- **re-enters bootstrap entry**: T2

### CLM-0118

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: line 38, uses key of the GL test step in the gl_test job
- **excerpt**: "uses: TinyTapeout/tt-gds-action/gl_test@ihp-cmos5l"
- **statement**: uses is set to "TinyTapeout/tt-gds-action/gl_test@ihp-cmos5l"
- **kind**: QUAL
- **value**: TinyTapeout/tt-gds-action/gl_test@ihp-cmos5l
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim from the raw file
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; covered inside Op2's aggregate. Consequent orphan of T2/30.
- **re-enters bootstrap entry**: T2

### CLM-0119

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: line 47, uses key of the single step in the viewer job
- **excerpt**: "- uses: TinyTapeout/tt-gds-action/viewer@ihp-cmos5l"
- **statement**: uses is set to "TinyTapeout/tt-gds-action/viewer@ihp-cmos5l"
- **kind**: QUAL
- **value**: TinyTapeout/tt-gds-action/viewer@ihp-cmos5l
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim from the raw file
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; covered inside Op2's aggregate. Consequent orphan of T2/30.
- **re-enters bootstrap entry**: T2

### CLM-0120

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: line 19, pdk key under the with mapping of the Build GDS step in the gds job
- **excerpt**: "pdk: ihp-sg13cmos5l"
- **statement**: pdk is set to "ihp-sg13cmos5l"
- **kind**: QUAL
- **value**: ihp-sg13cmos5l
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - machine-readable key and value reproduced verbatim; the value is printed unquoted and the quotation marks are the rule-6 frame
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T2

### CLM-0121

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: lines 9, 23, 30 and 42, the runs-on key of the gds, precheck, gl_test and viewer jobs; the identical value is printed at all four
- **excerpt**: "runs-on: ubuntu-24.04"
- **statement**: runs-on is set to "ubuntu-24.04"
- **kind**: QUAL
- **value**: ubuntu-24.04
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - one key/value predicate repeated identically at four locations, recorded as a single fact; value reproduced verbatim
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T2

### CLM-0122

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: whole file. Case-insensitive substring search for librelane over every line including comments and job names; 0 matches. Variants tried: LibreLane, librelane, LIBRELANE, libre-lane.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The gds.yaml does not contain LibreLane
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - deterministic case-insensitive substring search over the verbatim raw file; no excerpt exists because the token is absent
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T2

### CLM-0123

- **source_id**: SRC-0006 (TT-GDSYAML)
- **locator**: whole file. Case-insensitive substring search for openlane over every line including comments and job names; 0 matches. Variants tried: OpenLane, openlane, OPENLANE, open-lane, OpenLane2.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The gds.yaml does not contain OpenLane
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - deterministic case-insensitive substring search over the verbatim raw file; no excerpt exists because the token is absent
- **subject_tags**: TECH-FLOW
- **rq_ids**: RQ-05, RQ-30
- **source_version**: see SRC-0006
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T2

### CLM-0124

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: lines 1-3 of the LICENSE file, the centred header block
- **excerpt**: "Apache License                            Version 2.0, January 2004                         http://www.apache.org/licenses/"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - formulaic licence notice reproduced verbatim from the raw file; the leading whitespace of the centred header is not reproduced inside the value
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Disagreement about the unit of the printed notice. Op1 records the three header lines as one fact (QUAL, value with embedded newlines). Op2 records three facts, one per line, and assigns three different kinds to one notice - DEFINITION, QUANT, QUAL. Rule 6 calls a licence header a single 'formulaic notice line', suggesting the line is the unit; rule 1's aggregation suggests the block is. The three
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0125

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: line 2 of the LICENSE file, centred heading line directly below the Apache License line
- **excerpt**: "Version 2.0, January 2004"
- **statement**: The LICENSE file states "Version 2.0, January 2004"
- **kind**: QUANT
- **value**: Version 2.0, January 2004
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-text retrieval; formulaic version line recorded verbatim as a value per rule 6; the printed number 2.0 carries no unit
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only as a standalone fact; the same text sits inside Op1's three-line block. Consequent orphan of the block-versus-line disagreement at T2-LICENCE/38.
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0126

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: line 3 of the LICENSE file, centred heading line directly below the version line
- **excerpt**: "http://www.apache.org/licenses/"
- **statement**: The LICENSE file states "http://www.apache.org/licenses/"
- **kind**: QUAL
- **value**: http://www.apache.org/licenses/
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-text retrieval; formulaic notice line recorded verbatim as a value per rule 6
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only as a standalone fact; inside Op1's block. Consequent orphan of T2-LICENCE/38. This is also the claim Op2 marks matches_bootstrap false - see the bootstrap_mismatches entry for T2-LICENCE.
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0127

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: line 189, inside the APPENDIX boilerplate block at the end of the file
- **excerpt**: "Copyright [yyyy] [name of copyright owner]"
- **statement**: The LICENSE file states "Copyright [yyyy] [name of copyright owner]"
- **kind**: QUAL
- **value**: Copyright [yyyy] [name of copyright owner]
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - formulaic notice line reproduced verbatim from the raw file; the bracketed placeholders are printed literally and are not filled in
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Op2 could not have produced it: its own source record states only the opening 30 lines were retrieved. If the statement under examination concerns the repository's licence grant, the unfilled copyright placeholder qualifies it and rule 16 required it. The omission traces to an incomplete retrieval and to a gap in rule 19.
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0128

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: lines 191-192, inside the APPENDIX boilerplate block
- **excerpt**: "Licensed under the Apache License, Version 2.0 (the "License");    you may not use this file except in compliance with the License."
- **statement**: you may not use this file except in compliance with the License
- **kind**: RULE
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: except in compliance with the License
- **modality**: may not
- **reading_confidence**: high - deontic sentence reproduced verbatim from the raw file; the modal may not kept as printed per rule 8
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Same cause as T2-LICENCE/41: line 191 lies outside Op2's 30-line retrieval. Rule 12 makes this a RULE (deontic modal) and rule 16 required it if the statement under examination concerns the licence terms.
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0129

- **source_id**: SRC-0010 (TT-LICENSE)
- **locator**: line 1 of the LICENSE file, centred heading line
- **excerpt**: "Apache License"
- **statement**: The LICENSE file states "Apache License"
- **kind**: DEFINITION
- **value**: Apache License
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-text retrieval; formulaic licence header line recorded verbatim as a value per rule 6; the subject is the document itself, the exception allowed by rule 2
- **subject_tags**: LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0010
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only as a standalone fact; inside Op1's three-line block. Consequent orphan of T2-LICENCE/38, and the clearest instance of the kind instability: Op2 files line 1 DEFINITION, line 2 QUANT, line 3 QUAL, for one notice.
- **re-enters bootstrap entry**: T2-LICENCE

### CLM-0130

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, first sentence
- **excerpt**: "The chip uses the sky130_ef_io_gpiov2_pad macro for the I/O pads."
- **statement**: The chip uses the sky130_ef_io_gpiov2_pad macro for the I/O pads
- **kind**: QUAL
- **value**: sky130_ef_io_gpiov2_pad macro
- **unit**: DIMENSIONLESS
- **conditions**: for the I/O pads
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a markdown rendering per rule 19
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0131

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, second sentence, introducing the limitations table
- **excerpt**: "The documentation lists the following limitations:"
- **statement**: The documentation lists the following limitations
- **kind**: QUAL
- **value**: NONE
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Op2 paraphrases this sentence inside a locator rather than quoting it, so rule 16's final sentence is not strictly triggered on its side. Whether rule 16 required the claim is genuinely unclear: the sentence asserts only that a list follows, which is closer to a structural label (rule 17) than to a fact about the world.
- **re-enters bootstrap entry**: T3

### CLM-0132

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, the Maximum output frequency entry
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: QUANT
- **value**: 33
- **unit**: MHz
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 medium from verbatim HTML table structure, Op2 unverified from a markdown rendering
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: They disagree about what the source prints, not merely how to phrase it. Op1 says it is a table: locator 'limitations table, first data row', excerpt the row label 'Maximum output frequency', statement supplying the column header ('... Limitation is 33 MHz'). Op2 says it is a list: locator 'in the list of pad limitations', excerpt 'Maximum output frequency: 33 MHz'. Value 33 and unit MHz agree. Op
- **re-enters bootstrap entry**: T3

### CLM-0133

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, the Maximum input frequency entry
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: QUANT
- **value**: 66
- **unit**: MHz
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 medium, Op2 unverified
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Identical structural disagreement to T3/46 for the input-frequency entry: Op1 a table row with supplied column header, Op2 'Maximum input frequency: 66 MHz' as a list line. Value 66 and unit MHz agree. UNRESOLVED for the same reason.
- **re-enters bootstrap entry**: T3

### CLM-0134

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, limitations table, third data row
- **excerpt**: "Drive strength (source/sink)"
- **statement**: Drive strength (source/sink) Limitation is 4 mA
- **kind**: QUANT
- **value**: 4
- **unit**: mA
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it if the statement under examination is about the pad limitations as printed - the limitations table is one printed enumeration and stopping after two of its four rows is stopping short. Coverage failure by Op2, aggravated by its rendering-only retrieval.
- **re-enters bootstrap entry**: T3

### CLM-0135

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, limitations table, fourth data row; the row label carries a printed asterisk keyed to the footnote below the table
- **excerpt**: "IO supply voltage *"
- **statement**: IO supply voltage * Limitation is 1.71V - 5.5V
- **kind**: QUANT
- **value**: 1.71V - 5.5V
- **unit**: V
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure; the unit symbol V is printed attached to each number
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Same coverage failure by Op2 as at T3/48. Note that Op1's value here repeats the unit inside the value ('1.71V - 5.5V') while its unit field also reads V, whereas at other QUANT claims it strips the unit from the value - an internal inconsistency the rule does not prevent.
- **re-enters bootstrap entry**: T3

### CLM-0136

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, footnote line immediately below the limitations table, first sentence
- **excerpt**: "* The demo board provides 3.3V IO supply voltage. The input pins are not 5V tolerant."
- **statement**: The demo board provides 3.3V IO supply voltage
- **kind**: QUANT
- **value**: 3.3
- **unit**: V
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose footnote extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: the footnote is keyed by the printed asterisk to the IO supply voltage row and narrows that row's 1.71V - 5.5V range to what the demo board provides - the textbook case of a qualifying span. Op2 omitted the whole footnote.
- **re-enters bootstrap entry**: T3

### CLM-0137

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, Limitations section, footnote line immediately below the limitations table, second sentence
- **excerpt**: "* The demo board provides 3.3V IO supply voltage. The input pins are not 5V tolerant."
- **statement**: The input pins are not 5V tolerant
- **kind**: QUAL
- **value**: not 5V tolerant
- **unit**: V
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose footnote extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span contradicting the upper bound of the 1.71V - 5.5V row. It also exposes a kind question: Op1 files it QUAL though rule 12 lists 'a recorded non-occurrence' as ABSENCE - a printed negative statement is not the same as a non-occurrence, but rule 12 does not say so.
- **re-enters bootstrap entry**: T3

### CLM-0138

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, second paragraph, first sentence
- **excerpt**: "The maximum IO frequency is dictated by the IO pads themselves and the infrastructure that we put in the path of the signal."
- **statement**: The maximum IO frequency is dictated by the IO pads themselves and the infrastructure that we put in the path of the signal
- **kind**: QUAL
- **value**: the IO pads themselves and the infrastructure that we put in the path of the signal
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Op2 extracted only the two rating figures from this section and none of the surrounding prose. Rule 16 required the sentence if the statement under examination concerns the maximum IO frequency, since it states what governs that figure.
- **re-enters bootstrap entry**: T3

### CLM-0139

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, first sentence
- **excerpt**: "The maximum input frequency is the maximum frequency you can input a signal into the pad and still expect to get that signal to your tile with minimal distortion."
- **statement**: The maximum input frequency is the maximum frequency you can input a signal into the pad and still expect to get that signal to your tile with minimal distortion
- **kind**: DEFINITION
- **value**: the maximum frequency you can input a signal into the pad and still expect to get that signal to your tile with minimal distortion
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose copula sentence extracted verbatim; the modal can sits in a relative clause so the modality field reads NONE per rule 8
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. This is the copula defining the term whose value Op2 records (66 MHz), so rule 16 required it as a span that conditions the figure. Coverage failure by Op2.
- **re-enters bootstrap entry**: T3

### CLM-0140

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, second sentence, first clause
- **excerpt**: "For SKY130 the IO pads themselves are rated to 66 MHz - and we expect our infrastructure to work fine there too."
- **statement**: For SKY130 the IO pads themselves are rated to 66 MHz
- **kind**: QUANT
- **value**: 66
- **unit**: MHz
- **conditions**: For SKY130
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified because its rendering returned the clause without surrounding punctuation so the printed span boundaries were not established
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0141

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, second sentence, second clause
- **excerpt**: "For SKY130 the IO pads themselves are rated to 66 MHz - and we expect our infrastructure to work fine there too."
- **statement**: we expect our infrastructure to work fine there [For SKY130 the IO pads themselves are rated to 66 MHz] too
- **kind**: QUAL
- **value**: to work fine
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose clause extracted verbatim; the deictic there kept as printed with its referent per rule 5; the evaluative word fine is the source's own and is attributed to the page's first-person we per rule 9
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: it is the second half of the very sentence Op2 extracted and it qualifies the 66 MHz rating. Op2 stopped at the dash.
- **re-enters bootstrap entry**: T3

### CLM-0142

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, third sentence, first clause
- **excerpt**: "This doesn't mean that it stops working if you go above 66 MHz - that is just the official rating given by SkyWater."
- **statement**: This [the IO pads themselves are rated to 66 MHz] doesn't mean that it [the IO pads] stops working if you go above 66 MHz
- **kind**: QUAL
- **value**: NONE
- **unit**: MHz
- **conditions**: if you go above 66 MHz
- **modality**: NONE
- **reading_confidence**: medium - prose clause extracted verbatim, but the pronouns This and it are resolved by reading the preceding sentence; the resolution of it is the reader's, not the page's
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span qualifying the 66 MHz rating both operators recorded. Two rule problems surface: rule 14 makes reading_confidence a property of the printed form, yet Op1 lowers it because the anaphora needed resolving - a property of the extraction; and the unit field reads MHz for a claim whose value is NONE.
- **re-enters bootstrap entry**: T3

### CLM-0143

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, third sentence, second clause
- **excerpt**: "This doesn't mean that it stops working if you go above 66 MHz - that is just the official rating given by SkyWater."
- **statement**: that [66 MHz] is just the official rating given by SkyWater
- **kind**: DEFINITION
- **value**: the official rating given by SkyWater
- **unit**: MHz
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - prose clause extracted verbatim; the demonstrative that kept as printed with its referent from the same sentence
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span qualifying the 66 MHz figure. Same rule-14 objection as T3/56 to the medium level, and the unit field reads MHz although the value is a noun phrase.
- **re-enters bootstrap entry**: T3

### CLM-0144

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, third paragraph, fourth sentence
- **excerpt**: "Above 66 MHz, the signal can start to distort, mostly because falling edges propagate faster than rising edges (due to NMOS transistors being better than PMOS ones)."
- **statement**: Above 66 MHz, the signal can start to distort, mostly because falling edges propagate faster than rising edges (due to NMOS transistors being better than PMOS ones)
- **kind**: QUAL
- **value**: start to distort
- **unit**: MHz
- **conditions**: Above 66 MHz
- **modality**: can
- **reading_confidence**: high - prose sentence extracted verbatim; the modal can governs the main predicate and is kept as printed per rule 8; the evaluative word better is the source's own per rule 9
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: it states what happens beyond the 66 MHz figure and so qualifies it. Coverage failure by Op2.
- **re-enters bootstrap entry**: T3

### CLM-0145

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fourth paragraph, first sentence
- **excerpt**: "The maximum output frequency is the maximum frequency you can toggle an output pad at."
- **statement**: The maximum output frequency is the maximum frequency you can toggle an output pad at
- **kind**: DEFINITION
- **value**: the maximum frequency you can toggle an output pad at
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose copula sentence extracted verbatim; the modal can sits in a relative clause so the modality field reads NONE per rule 8
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. The copula defining the term whose value Op2 records (33 MHz); rule 16 required it. Coverage failure by Op2.
- **re-enters bootstrap entry**: T3

### CLM-0146

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fourth paragraph, second sentence
- **excerpt**: "Again, limited by the provided output pads, our infrastructure and the actual loading of the pad."
- **statement**: Again, limited by the provided output pads, our infrastructure and the actual loading of the pad
- **kind**: QUAL
- **value**: the provided output pads, our infrastructure and the actual loading of the pad
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - the source prints this as a verbless fragment continuing the preceding sentence; reproduced as printed without supplying a subject
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span conditioning the maximum output frequency. It also exposes a gap Op1 had to improvise around: rule 1 demands one subject and one predicate, and rule 3 supplies a subject-free treatment only for imperatives, so a verbless fragment has no sanctioned treatment.
- **re-enters bootstrap entry**: T3

### CLM-0147

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fourth paragraph, third sentence, first clause
- **excerpt**: "For SKY130 the official rating is 33 MHz, however the documentation is unclear whether that means the toggle rate of the pad or if a 33 MHz square wave can be output."
- **statement**: For SKY130 the official rating is 33 MHz
- **kind**: QUANT
- **value**: 33
- **unit**: MHz
- **conditions**: For SKY130
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified because the rendering returned the clause without surrounding punctuation
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0148

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fourth paragraph, third sentence, second clause
- **excerpt**: "For SKY130 the official rating is 33 MHz, however the documentation is unclear whether that means the toggle rate of the pad or if a 33 MHz square wave can be output."
- **statement**: the documentation is unclear whether that [33 MHz] means the toggle rate of the pad or if a 33 MHz square wave can be output
- **kind**: QUAL
- **value**: unclear
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose clause extracted verbatim; the evaluative word unclear is the source's own and is attributed to the page per rule 9; the demonstrative that kept with its referent per rule 5
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it in the strongest terms: it is the clause, printed in the same sentence Op2 extracted, that qualifies the 33 MHz rating by saying the documentation does not settle what it measures. Op2 recorded the figure and dropped its qualification - the clearest single coverage failure in the pair.
- **re-enters bootstrap entry**: T3

### CLM-0149

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fourth paragraph, fourth sentence
- **excerpt**: "In practice, you can output a 33 MHz square wave and it still looks acceptable - albeit with some asymmetry - if the load isn't large."
- **statement**: In practice, you can output a 33 MHz square wave and it [a 33 MHz square wave] still looks acceptable - albeit with some asymmetry - if the load isn't large
- **kind**: QUAL
- **value**: acceptable
- **unit**: MHz
- **conditions**: In practice; if the load isn't large
- **modality**: can
- **reading_confidence**: high - prose sentence extracted verbatim; the evaluative word acceptable is the source's own; the pronoun it kept as printed with its referent from the same sentence
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span qualifying the 33 MHz rating. The conditions field here holds two independent restrictions joined by a semicolon; the classification rule forgives their order but no rule prescribes the separator.
- **re-enters bootstrap entry**: T3

### CLM-0150

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: TT-GPIO body, f_max versus IO Maximum Frequency section, fifth paragraph, second sentence
- **excerpt**: "The slow slew rate of the pads means that if you have several symbols (0, 1) of the same value, the output will go to the full 0V/3.3V."
- **statement**: The slow slew rate of the pads means that if you have several symbols (0, 1) of the same value, the output will go to the full 0V/3.3V
- **kind**: QUAL
- **value**: 0V/3.3V
- **unit**: V
- **conditions**: if you have several symbols (0, 1) of the same value
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim; the modal will sits in the subordinate clause so the modality field reads NONE per rule 8; the evaluative word slow is the source's own
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as a span qualifying the output-frequency discussion. Coverage failure by Op2, which took nothing from this paragraph.
- **re-enters bootstrap entry**: T3

### CLM-0151

- **source_id**: SRC-0007 (TT-GPIO)
- **locator**: whole page as retrieved. Case-insensitive search for cmos5l; variants tried CMOS5L, cmos5l, sg13cmos5l; 0 matches.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The GPIO pins page does not contain CMOS5L
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high, having searched the verbatim HTML source (91104 bytes, head metadata included); Op2 unverified, having searched only a markdown rendering of the visible body
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0007
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Same conclusion reached by different searches, and they disagree about what was searched. Op1 searched the raw HTML including head metadata; Op2 searched a rendering of the visible body and says expressly that a token hidden in markup or a collapsed element would not have been seen. Since an ABSENCE claim asserts something about the whole document, the scope is part of what the claim says, so thes
- **re-enters bootstrap entry**: T3

### CLM-0152

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Clock section, first line beneath the heading, printed as a callout
- **excerpt**: "The information in this document applies to Tiny Tapeout 4 and beyond."
- **statement**: The information in this document [Clock] applies to Tiny Tapeout 4 and beyond
- **kind**: QUAL
- **value**: Tiny Tapeout 4 and beyond
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim; the deictic this document kept as printed with the page's own subject name in square brackets per rule 5
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it in the strongest terms: it conditions the applicability of every other claim taken from this page, including the clock-range and latency figures Op2 did record. Coverage failure by Op2, not a rule gap. (Borderline rule-2 case - the subject is the document - but the exception is visible from the predicate 'applies to'.)
- **re-enters bootstrap entry**: T3

### CLM-0153

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Clock section, first paragraph
- **excerpt**: "Tiny Tapeout includes a clock input signal (clk), provided externally through the mprj_io[6] pin of the chip (pin number 37 in the QFN-64 chip package)."
- **statement**: Tiny Tapeout includes a clock input signal (clk), provided externally through the mprj_io[6] pin of the chip (pin number 37 in the QFN-64 chip package)
- **kind**: QUAL
- **value**: a clock input signal (clk)
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: They disagree about what the source prints as the span. Op1 quotes the complete sentence beginning 'Tiny Tapeout includes...'. Op2 quotes only the trailing participial phrase, invents the subject 'The clock input', puts it in the states-frame with rendering backticks, and gives a value field 'mprj_io[6], pin number 37, QFN-64' that reorders and abbreviates the printed text - while recording that i
- **re-enters bootstrap entry**: T3

### CLM-0154

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Limitations section, first paragraph, first sentence
- **excerpt**: "Internally, both the clk and rst_n pins are handled like any other input pins."
- **statement**: Internally, both the clk and rst_n pins are handled like any other input pins
- **kind**: QUAL
- **value**: handled like any other input pins
- **unit**: DIMENSIONLESS
- **conditions**: Internally
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim; the same sentence is printed on the GPIO pins page and is recorded separately there with its own locator
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0155

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Limitations section, first paragraph, second sentence
- **excerpt**: "We expect a latency (insertion delay) of up to 10 nanoseconds between the chip's I/O pad and your project's clock."
- **statement**: We expect a latency (insertion delay) of up to 10 nanoseconds between the chip's I/O pad and your project's clock
- **kind**: QUANT
- **value**: up to 10
- **unit**: nanoseconds
- **conditions**: between the chip's I/O pad and your project's clock
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a markdown rendering
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0156

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Limitations section, second paragraph, first sentence
- **excerpt**: "The chip uses the sky130_ef_io_gpiov2_pad macro for the I/O pads."
- **statement**: The chip uses the sky130_ef_io_gpiov2_pad macro for the I/O pads
- **kind**: QUAL
- **value**: sky130_ef_io_gpiov2_pad macro
- **unit**: DIMENSIONLESS
- **conditions**: for the I/O pads
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high, Op2 unverified from a rendering
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0157

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Limitations section, second paragraph, second sentence
- **excerpt**: "The documentation specifies a maximum input frequency of 66 MHz."
- **statement**: The documentation specifies a maximum input frequency of 66 MHz
- **kind**: QUANT
- **value**: 66
- **unit**: MHz
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high, Op2 unverified from a rendering
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0158

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Limitations section, second paragraph, third sentence
- **excerpt**: "Therefore, we believe that the maximum clock frequency for your designs will be around 66 MHz."
- **statement**: Therefore, we believe that the maximum clock frequency for your designs will be around 66 MHz
- **kind**: QUANT
- **value**: around 66
- **unit**: MHz
- **conditions**: for your designs
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim; the precision qualifier around kept per rule 7
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: They disagree on the modality field for one printed sentence, which rule 8 is written to prevent. Op1 reads the main predicate as 'we believe' and records NONE, the modal will sitting in the complement clause; Op2 records 'will'. The printed sentence settles it: 'we believe' is the matrix predicate and 'that ... will be' its complement, so rule 8's second sentence gives NONE - Op1 is correct. They
- **re-enters bootstrap entry**: T3

### CLM-0159

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Clock Generation section, first sentence
- **excerpt**: "The Tiny Tapeout Demo board can generate the clock signal for your design."
- **statement**: The Tiny Tapeout Demo board can generate the clock signal for your design
- **kind**: QUAL
- **value**: the clock signal for your design
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: can
- **reading_confidence**: high - prose sentence extracted verbatim; the modal can governs the main predicate and is recorded as printed per rule 8
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it: it introduces and conditions the configurable clock range both operators recorded - the range is a property of the demo board's generator, not of the chip. Coverage failure by Op2.
- **re-enters bootstrap entry**: T3

### CLM-0160

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Clock Generation section, second sentence
- **excerpt**: "The frequency of the clock signal can be configured by the user, between 1 Hz and 66.5 MHz."
- **statement**: The frequency of the clock signal can be configured by the user, between 1 Hz and 66.5 MHz
- **kind**: QUANT
- **value**: between 1 Hz and 66.5 MHz
- **unit**: Hz, MHz
- **conditions**: by the user
- **modality**: can
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high from verbatim HTML, Op2 unverified from a rendering
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T3

### CLM-0161

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Clock Generation section, third sentence
- **excerpt**: "The clock is generated by the on-board RP2040 microcontroller, using the PWM or PIO hardware peripherals to divide the RP2040 system clock."
- **statement**: The clock is generated by the on-board RP2040 microcontroller, using the PWM or PIO hardware peripherals to divide the RP2040 system clock
- **kind**: QUAL
- **value**: the on-board RP2040 microcontroller
- **unit**: DIMENSIONLESS
- **conditions**: using the PWM or PIO hardware peripherals to divide the RP2040 system clock
- **modality**: NONE
- **reading_confidence**: high - prose sentence extracted verbatim from the HTML markup
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it as the span explaining what produces the range recorded at T3/74 and thereby conditioning it. Coverage failure by Op2.
- **re-enters bootstrap entry**: T3

### CLM-0162

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: TT-CLOCK body, Low Frequency Clock section, first sentence
- **excerpt**: "In case you need a very slow clock like 1Hz, you can generate it with a simple MicroPython program like this:"
- **statement**: In case you need a very slow clock like 1Hz, you can generate it [a very slow clock like 1Hz] with a simple MicroPython program like this
- **kind**: QUAL
- **value**: 1Hz
- **unit**: Hz
- **conditions**: In case you need a very slow clock like 1Hz
- **modality**: can
- **reading_confidence**: high - prose sentence extracted verbatim; the pronoun it kept as printed with its referent per rule 5; the evaluative words very slow and simple are the source's own per rule 9
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Op2's source record states expressly that the page's 1Hz MicroPython example and its 25.179 MHz figure caption 'fall outside the statement under examination and are not extracted' - a deliberate rule-16 first-direction judgement opposite to Op1's. Whether rule 16 required it turns on whether the low bound of the configurable range (1 Hz) is conditioned by this sentence; arguable both way
- **re-enters bootstrap entry**: T3

### CLM-0163

- **source_id**: SRC-0005 (TT-CLOCK)
- **locator**: whole page as retrieved. Case-insensitive search for cmos5l; variants tried CMOS5L, cmos5l, sg13cmos5l; 0 matches.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The Clock page does not contain CMOS5L
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high, having searched the verbatim HTML source (88701 bytes, head metadata and code blocks included); Op2 unverified, having searched a markdown rendering of the visible body only
- **subject_tags**: TECH-IO, TECH-CLOCK
- **rq_ids**: RQ-06
- **source_version**: see SRC-0005
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Same disagreement as T3/65: conclusions coincide but the searched scopes differ (raw HTML including metadata versus rendered visible body), so the two claims do not assert the same thing. Op1's locator, stating the byte count of the raw retrieval and a zero-match search over it, settles it in favour of the stronger claim.
- **re-enters bootstrap entry**: T3

### CLM-0164

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 page heading; the same string is printed as the page title
- **excerpt**: "Tiny Tapeout IHP 0.4"
- **statement**: The shuttle is named "Tiny Tapeout IHP 0.4".
- **kind**: DEFINITION
- **value**: Tiny Tapeout IHP 0.4
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: unverified - excerpt obtained through a markdown rendering of the HTML page, per rule 19
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op2 only. Rule 16 did not require it and rule 17 forbids it: a page title and heading are provenance, recorded in the locator, unless the statement under examination is about the document's structure. Op1 instead uses the heading as the subject of its own claims, which is what rule 17 contemplates. The omission is correct on Op1's side and the claim is a rule-17 breach on Op2's.
- **re-enters bootstrap entry**: T4

### CLM-0165

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 visible body, Launch stats section, first list item
- **excerpt**: "Experimental shuttle"
- **statement**: Tiny Tapeout IHP 0.4 is listed as "Experimental shuttle"
- **kind**: DEFINITION
- **value**: Experimental shuttle
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - printed as a standalone list item with no verb; recorded verbatim as a value rather than paraphrased into a predicate; subject taken from the page's own heading
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. Rule 16 required it if the statement under examination concerns the shuttle's status: 'Experimental shuttle' conditions every other fact about the run and is consistent with the runs-table cell 'None - test shuttle' both operators saw. Op2's rendering returned only the two date lines and the PDK line for this block.
- **re-enters bootstrap entry**: T4

### CLM-0166

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 visible body, Launch stats section, second list item
- **excerpt**: "Launched: 27 March 2026"
- **statement**: Tiny Tapeout IHP 0.4 Launched: 27 March 2026
- **kind**: QUANT
- **value**: 2026-03-27
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high, Op2 unverified from a rendering
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T4

### CLM-0167

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 visible body, Launch stats section, third list item
- **excerpt**: "Submission closed: 28 March 2026"
- **statement**: Tiny Tapeout IHP 0.4 Submission closed: 28 March 2026
- **kind**: QUANT
- **value**: 2026-03-28
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high, Op2 unverified
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T4

### CLM-0168

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 visible body, Launch stats section, fourth list item
- **excerpt**: "Submitted to IHP using sg13cmos5l 130nm open source PDK"
- **statement**: Tiny Tapeout IHP 0.4 Submitted to IHP using sg13cmos5l 130nm open source PDK
- **kind**: QUANT
- **value**: sg13cmos5l 130nm open source PDK
- **unit**: nm
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED as to level - content agreed; Op1 high, Op2 unverified because its rendering returned the line without terminating punctuation
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: T4

### CLM-0169

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4: head metadata, the meta name=description, og:description and itemprop=description elements carrying the same content value; and the visible body
- **excerpt**: "40 designs, closed 2026-03-28"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: UNRESOLVED
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high, reading the head metadata of the verbatim HTML; Op2 unverified, having seen only a markdown rendering of the visible body
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: A direct disagreement about what the page prints. Op1 records 'Tiny Tapeout IHP 0.4 has 40 designs', QUANT, value 40, unit designs, locating it in three head meta elements and noting the visible body prints no design count. Op2 records the opposite as an ABSENCE claim, 'The TT-IHP0P4 page does not contain Designs', having searched only a rendering of the visible body across three retrievals whose 
- **re-enters bootstrap entry**: T4

### CLM-0170

- **source_id**: SRC-0008 (TT-IHP0P4)
- **locator**: TT-IHP0P4 head metadata, second half of the description content value carried by meta name=description, og:description and itemprop=description
- **excerpt**: "40 designs, closed 2026-03-28"
- **statement**: Tiny Tapeout IHP 0.4 closed 2026-03-28
- **kind**: QUANT
- **value**: 2026-03-28
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: high - read from the head metadata of the verbatim HTML source; the date is printed in ISO 8601 there, unlike the visible body which prints 28 March 2026
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0008
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only. This is the rule-18 case done properly: the same element is printed in two different forms in one retrieved document - '28 March 2026' in the body, '2026-03-28' in the metadata - and Op1 records both readings with their own locators. Op2 never saw the metadata. The omission traces to the rendering-only retrieval and to rule 19's silence about metadata.
- **re-enters bootstrap entry**: T4

### CLM-0171

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, the row whose first cell is TTIHP0p4; columns in printed order Run, Launched, Closed, Shuttle, Designs, Chips expected, Estimated delivery date
- **excerpt**: "UNRESOLVED"
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: UNRESOLVED
- **value**: UNRESOLVED
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 medium from verbatim HTML with a read table structure; Op2 unverified from a markdown rendering whose pipe separators are an artefact
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: The T1-GPIO/12 granularity disagreement again, on a seven-column row. Op1 emits six cell claims (Launched 2026-03-27, Closed 2026-03-28, Shuttle IHP-2603, Designs 40, Chips expected -, Estimated delivery date None - test shuttle). Op2 emits one row claim listing all seven cells with pipe separators it admits are artefacts, kind QUANT for a row that is mostly non-numeric. Cell contents agree exactl
- **re-enters bootstrap entry**: T4

### CLM-0172

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Closed column
- **excerpt**: "2026-03-28"
- **statement**: TTIHP0p4 Closed is 2026-03-28
- **kind**: QUANT
- **value**: 2026-03-28
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85. Op1's own excerpt field reads 'TTIHP0p4', the row label rather than the cell - the excerpt-boundary defect of T1-GPIO/12 again.
- **re-enters bootstrap entry**: T4

### CLM-0173

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Shuttle column
- **excerpt**: "IHP-2603"
- **statement**: TTIHP0p4 Shuttle is IHP-2603
- **kind**: QUAL
- **value**: IHP-2603
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85.
- **re-enters bootstrap entry**: T4

### CLM-0174

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Designs column
- **excerpt**: "40"
- **statement**: TTIHP0p4 Designs is 40
- **kind**: QUANT
- **value**: 40
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure; the column header is Designs and no unit is printed in the cell
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85. This cell is also the external corroboration of the metadata figure disputed at T4/83, and Op2's own note on its row claim points out the tension with its ABSENCE claim.
- **re-enters bootstrap entry**: T4

### CLM-0175

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Chips expected column
- **excerpt**: "-"
- **statement**: TTIHP0p4 Chips expected is -
- **kind**: QUAL
- **value**: -
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - the cell prints a single hyphen and no date; recorded as the printed character rather than interpreted as unknown or none
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85. Op1's treatment - a printed placeholder recorded as printed rather than interpreted - is right but has no rule behind it.
- **re-enters bootstrap entry**: T4

### CLM-0176

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Estimated delivery date column
- **excerpt**: "None - test shuttle"
- **statement**: TTIHP0p4 Estimated delivery date is None - test shuttle
- **kind**: QUAL
- **value**: None - test shuttle
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85.
- **re-enters bootstrap entry**: T4

### CLM-0177

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTIHP0p4 row, Launched column
- **excerpt**: "2026-03-27"
- **statement**: TTIHP0p4 Launched is 2026-03-27
- **kind**: QUANT
- **value**: 2026-03-27
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure; the date is printed in ISO 8601 form and no unit is printed
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only as a standalone fact; inside Op2's row claim. Consequent orphan of T4/85.
- **re-enters bootstrap entry**: T4

### CLM-0178

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS body, Current chips table, TTSKY26c row, Chips expected column
- **excerpt**: "2027-03-27"
- **statement**: TTSKY26c Chips expected is 2027-03-27
- **kind**: QUANT
- **value**: 2027-03-27
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: medium - cell value taken from the verbatim HTML markup; row/column association read from the table structure
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: Op1 only, recorded expressly because it is the only 2027-03 date on the page and therefore qualifies the March 2027 absence claim - a correct rule-16 application. Op2 lists the 2027 dates it saw inside the locator of its own absence claim (2027-06-25, 2027-08-16, 2027-02-28, 2027-04-10) - conspicuously not 2027-03-27. Two consequences: Op2 breached rule 16's final sentence by quoting those dates i
- **re-enters bootstrap entry**: T4

### CLM-0179

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS whole page as retrieved, both the Current chips and Future chips tables
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: NOT ESTABLISHED. The two operators reported this span differently and the reconciliation could not settle it from their excerpts. No statement is recorded, because recording one would pick a reading the evidence does not support. What each operator reported is in the caveats below.
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high from the verbatim HTML source, Op2 unverified from a markdown rendering
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: They record different absence tokens and different underlying facts. Op1 claims the page does not contain 'March 2027', its locator stating the 2027 values printed include 2027-03-27. Op2 claims the page does not contain '2027-03', its locator listing the 2027 dates as 2027-06-25, 2027-08-16, 2027-02-28 and 2027-04-10 - omitting 2027-03-27. These cannot both be right: if 2027-03-27 is printed, as 
- **re-enters bootstrap entry**: T4

### CLM-0180

- **source_id**: SRC-0012 (TT-RUNS)
- **locator**: TT-RUNS whole page as retrieved. Case-insensitive search for cmos5l; variants tried CMOS5L, cmos5l, sg13cmos5l; 0 matches.
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The Tiny Tapeout Chips page does not contain CMOS5L
- **kind**: ABSENCE
- **value**: NOT PRESENT
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **modality**: NONE
- **reading_confidence**: UNRESOLVED - Op1 high, having searched the verbatim HTML source (98017 bytes including head metadata and both tables); Op2 unverified, having searched a rendering of the visible table and surrounding body
- **subject_tags**: SHUTTLE
- **rq_ids**: RQ-07
- **source_version**: see SRC-0012
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: Same scope disagreement as T3/65 and T3/77: identical conclusion, incomparable evidence, and a different page name in the rule-15 frame ('The Tiny Tapeout Chips page' from the page's own title versus 'The TT-RUNS page' from the source_key). Op1's whole-document search settles it in favour of the stronger claim.
- **re-enters bootstrap entry**: T4
