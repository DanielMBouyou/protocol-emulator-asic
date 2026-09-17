# Claim register: IHP sources

An excerpt is verbatim source text. Where it contains markup that a renderer would reinterpret, it is wrapped in inline code so that every character is shown as the source prints it.

Part of the claim register, split by source group per [DEC-0011](decision-log.md#dec-0011-splitting-the-claim-register-by-source-group). Index and the meaning of the `double_extraction` field: [claim-register.md](claim-register.md).

Every record comes from the second S00 double extraction, [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule). Two operators read each source independently under the amended [atomic fact rule](../EVIDENCE_POLICY.md#atomic-fact-rule), and a third operator, which produced neither set, paired the claims. Read `double_extraction` before relying on any record.

`subject_tags` and `rq_ids` were assigned at consolidation from the vocabulary of [DEC-0007](decision-log.md#dec-0007-s00-d7-controlled-vocabulary-of-subject-tags), not by the extracting operators. They are retrieval keys, not evidence.


### CLM-0181

- **source_id**: SRC-0003 (IHP-REPO)
- **locator**: IHP-Open-PDK README.md, License section, line 147 of the raw default-branch (main) README.md, as rendered on the repository landing page
- **excerpt**: `"The IHP Open Source PDK is released under the [Apache 2.0 license](LICENSE)."`
- **statement**: The IHP Open Source PDK is released under the Apache 2.0 license.
- **kind**: QUAL
- **value**: Apache 2.0 license
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-Markdown retrieval of the file the landing page renders; the span prints 'Apache 2.0 license' as a Markdown link to LICENSE; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0003
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: `"O1 seq 1 vs O2 seq 1. The statements are word-for-word identical, but the operators disagree about what the source prints at this span: O1's excerpt is 'The IHP Open Source PDK is released under the Apache 2.0 license.' (no link markup, reading_confidence 'unverified'), O2's is 'The IHP Open Source PDK is released under the [Apache 2.0 license](LICENSE).' (reading_confidence 'HIGH'). O2's excerpt"`
- **re-enters bootstrap entry**: I1

### CLM-0182

- **source_id**: SRC-0003 (IHP-REPO)
- **locator**: Repository landing page, right-hand sidebar licence label
- **excerpt**: "Apache-2.0"
- **statement**: The IHP-Open-PDK repository's licence label is "Apache-2.0".
- **kind**: DEFINITION
- **value**: Apache-2.0
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: unverified - the sidebar label exists only in the rendered landing page, not in any raw file retrieved; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0003
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 seq 2 only; O2 produced no claim from the landing page's sidebar licence label. Rule 16 did require it once O1 quoted the span 'Apache-2.0' in its output, but the prior question - whether the code-hosting platform's own sidebar metadata is source content that qualifies the licence statement, or page furniture - is not decided by the rule, so the omission is not by itself an error by O2.
- **re-enters bootstrap entry**: I1

### CLM-0183

- **source_id**: SRC-0003 (IHP-REPO)
- **locator**: IHP-Open-PDK README.md, introductory paragraph above the IHP logo image, line 21 of the raw default-branch (main) README.md, as rendered on the repository landing page
- **excerpt**: "As of March 2023, this repository is targeting the SG13G2 process node."
- **statement**: This repository [IHP Open Source PDK] is targeting the SG13G2 process node.
- **kind**: QUAL
- **value**: SG13G2 process node
- **unit**: DIMENSIONLESS
- **conditions**: As of March 2023
- **modality**: is targeting
- **reading_confidence**: high - verbatim raw-Markdown retrieval of the file the landing page renders; on this version the sentence is printed as a complete paragraph with no continuation; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0003
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I1

### CLM-0184

- **source_id**: SRC-0003 (IHP-REPO)
- **locator**: Full HTML of https://github.com/IHP-GmbH/IHP-Open-PDK retrieved 2026-09-17 (341308 bytes) and the raw default-branch README.md it renders; substring search for the token: case-sensitive 0 matches, case-insensitive 0 matches; variants tried sg13cmos5l, Sg13Cmos5L and the shorter stem cmos5l, all 0 matches; the control token SG13G2 returned 7 case-sensitive matches on the same retrieval, confirming the search reached the README body
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The IHP-Open-PDK repository landing page does not contain SG13CMOS5L.
- **kind**: ABSENCE
- **value**: not present
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - non-occurrence established by exhaustive substring search, case-sensitive and case-insensitive, over a verbatim byte-level retrieval of the page, with a positive control token; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0003
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I1

### CLM-0185

- **source_id**: SRC-0003 (IHP-REPO)
- **locator**: Full HTML of https://github.com/IHP-GmbH/IHP-Open-PDK retrieved 2026-09-17 (341308 bytes) and the raw default-branch README.md it renders; substring search for the token: case-sensitive 0 matches, case-insensitive 0 matches; variants tried IHP-SG13CMOS5L, ihp_sg13cmos5l and the shorter stem cmos5l, all 0 matches; the control token SG13G2 returned 7 case-sensitive matches on the same retrieval, confirming the search reached the README body
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The IHP-Open-PDK repository landing page does not contain ihp-sg13cmos5l.
- **kind**: ABSENCE
- **value**: not present
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - non-occurrence established by exhaustive substring search, case-sensitive and case-insensitive, over a verbatim byte-level retrieval of the page, with a positive control token; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0003
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I1

### CLM-0186

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, paragraph following "IHP Open Source PDK project goal ...", first sentence
- **excerpt**: "As of March 2023, this repository is targeting the SG13G2 process node."
- **statement**: this repository [IHP Open Source PDK] is targeting the SG13G2 process node
- **kind**: QUAL
- **value**: SG13G2 process node
- **unit**: DIMENSIONLESS
- **conditions**: As of March 2023
- **modality**: is targeting
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative sentence; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 seq 6 only. O1 recorded the SG13G2 targeting sentence a second time from the dev-branch README, citing rule 18 on the ground that the two retrieved versions print the surrounding paragraph differently (the dev version is followed by the SG13CMOS5L sentence, the main version is not). O2 recorded that sentence only once, under IHP-REPO, and recorded from the dev paragraph only its second sentence
- **re-enters bootstrap entry**: I1-DEV

### CLM-0187

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, paragraph following "IHP Open Source PDK project goal ...", second sentence, lines 21-22 (hard-wrapped across the two lines)
- **excerpt**: "It also hosts the SG13CMOS5L process node, a CMOS-only variant with a reduced metal stack."
- **statement**: It [IHP Open Source PDK] also hosts the SG13CMOS5L process node, a CMOS-only variant with a reduced metal stack.
- **kind**: QUAL
- **value**: SG13CMOS5L process node, a CMOS-only variant with a reduced metal stack
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative sentence, the source's hard line wrap rendered as a single space; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I1-DEV

### CLM-0188

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, line 62, closing line of the "# SG13CMOS5L Process Node" section
- **excerpt**: "Switch between the process nodes by setting the `$PDK` environment variable to `ihp-sg13g2` or `ihp-sg13cmos5l`."
- **statement**: Switch between the process nodes by setting the `$PDK` environment variable to `ihp-sg13g2` or `ihp-sg13cmos5l`.
- **kind**: PROCEDURE
- **value**: `ihp-sg13g2` or `ihp-sg13cmos5l`
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; printed imperative reproduced as printed, with the source's backtick code spans kept; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I1-DEV

### CLM-0189

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, "# SG13CMOS5L Process Node" section, first sentence, lines 56-57
- **excerpt**: "SG13CMOS5L is a CMOS-only 0.13 μm process node from the same platform as SG13G2, but without the SiGe:C npn-HBT devices."
- **statement**: SG13CMOS5L is a CMOS-only 0.13 μm process node from the same platform as SG13G2, but without the SiGe:C npn-HBT devices.
- **kind**: DEFINITION
- **value**: a CMOS-only 0.13 μm process node from the same platform as SG13G2, but without the SiGe:C npn-HBT devices
- **unit**: μm
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; copula sentence naming the term, the source's hard line wrap rendered as a single space; the unit symbol μm is the one printed inside the defining phrase
- **subject_tags**: TECH-PROCESS
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: I2

### CLM-0190

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, "# SG13CMOS5L Process Node" section, second sentence, lines 57-58
- **excerpt**: "It provides the same 2 gate oxides: A thin gate oxide for the 1.2 V digital logic and a thick oxide for a 3.3 V supply voltage."
- **statement**: It [SG13CMOS5L] provides the same [as SG13G2] 2 gate oxides: A thin gate oxide for the 1.2 V digital logic and a thick oxide for a 3.3 V supply voltage.
- **kind**: QUANT
- **value**: 2 gate oxides: A thin gate oxide for the 1.2 V digital logic and a thick oxide for a 3.3 V supply voltage
- **unit**: V
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; printed numerals and the printed unit symbol V read directly from the span; the two gate oxides are printed together under one predicate and are recorded as a single fact in printed order
- **subject_tags**: TECH-PROCESS
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I2

### CLM-0191

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, "# SG13CMOS5L Process Node" section, fourth sentence, lines 59-60
- **excerpt**: "The aluminium backend offers 4 thin metal layers and one thick top metal layer (M1-M4-TM1)."
- **statement**: The aluminium backend offers 4 thin metal layers and one thick top metal layer (M1-M4-TM1).
- **kind**: QUANT
- **value**: 4 thin metal layers and one thick top metal layer (M1-M4-TM1)
- **unit**: metal layers
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; the counts are printed by the source, one as a numeral and one as a word, and the stack designation is printed in parentheses within the same predicate; the source prints no unit symbol, so the counted noun is the unit
- **subject_tags**: TECH-PROCESS
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: I2

### CLM-0192

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, "# SG13CMOS5L Process Node" section, final sentence, line 60, first clause
- **excerpt**: "The MIM layer is not available"
- **statement**: The MIM layer is not available.
- **kind**: QUAL
- **value**: not available
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative clause, the printed sentence carrying two predicates and recorded as two facts under rule 1; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PROCESS
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: I2

### CLM-0193

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, "# SG13CMOS5L Process Node" section, final sentence, line 60, second clause
- **excerpt**: "metal-oxide-metal capacitors are offered instead"
- **statement**: metal-oxide-metal capacitors are offered instead [of The MIM layer]
- **kind**: QUAL
- **value**: metal-oxide-metal capacitors
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative clause; the anaphoric 'instead' is resolved to the noun phrase printed in the immediately preceding clause of the same sentence; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PROCESS
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I2

### CLM-0194

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "# Current status -- Preview", inside the blockquoted Warning callout, line 30
- **excerpt**: `"IHP is currently treating the existing content as a **preview only**."`
- **statement**: IHP is currently treating the existing content as a preview only.
- **kind**: QUAL
- **value**: preview only
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative sentence; the source's blockquote marker and bold emphasis are markup and are dropped from the statement; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I3

### CLM-0195

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "# Current status -- Preview", paragraph after the Warning blockquote, concessive clause opening the sentence spanning lines 32-35; recorded because it qualifies the not-intended-for-production statement in the same sentence
- **excerpt**: "While the SG13G2 process node and the PDK from which this open source release was derived have been used to create many designs that have been successfully manufactured in significant quantities,"
- **statement**: the SG13G2 process node and the PDK from which this open source release [IHP Open Source PDK] was derived have been used to create many designs that have been successfully manufactured in significant quantities
- **kind**: QUAL
- **value**: many designs that have been successfully manufactured in significant quantities
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative clause, hard line wraps rendered as single spaces; the evaluative wording 'many' and 'significant quantities' is the source's own and is reproduced unchanged; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I3

### CLM-0196

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "# Current status -- Preview", paragraph after the Warning blockquote, main clause of the sentence spanning lines 32-35
- **excerpt**: "the open source PDK is not intended to be used for production at this moment"
- **statement**: the open source PDK is not intended to be used for production at this moment
- **kind**: QUAL
- **value**: not intended to be used for production
- **unit**: DIMENSIONLESS
- **conditions**: at this moment
- **modality**: is not intended to be used
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative main clause, hard line wraps rendered as single spaces; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I3

### CLM-0197

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "# Current status -- Preview", closing sentence of the paragraph after the Warning blockquote, lines 35-36
- **excerpt**: "The same applies to the SG13CMOS5L process node."
- **statement**: The same [the open source PDK is not intended to be used for production at this moment] applies to the SG13CMOS5L process node.
- **kind**: QUAL
- **value**: SG13CMOS5L process node
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative sentence; the anaphor 'The same' is resolved to the main clause of the preceding sentence, itself recorded as a claim; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: I3

### CLM-0198

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "## Supported Devices", Capacitors bullet, first sentence
- **excerpt**: "Capacitors: metal-oxide-metal on the Metal1-Metal4 stack, `cap_cmomi` (interdigitated, with feed topology) and `cap_cmomf` (metal fringe / finger)."
- **statement**: Capacitors: metal-oxide-metal on the Metal1-Metal4 stack, `cap_cmomi` (interdigitated, with feed topology) and `cap_cmomf` (metal fringe / finger).
- **kind**: QUAL
- **value**: `cap_cmomi` (interdigitated, with feed topology) and `cap_cmomf` (metal fringe / finger)
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; printed list reproduced in printed order under one predicate as a single fact; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 seq 18 only. Rule 16 required it of both operators, and the requirement is unambiguous here: O2 quoted the device names 'cap_cmomi and cap_cmomf' inside the bracketed referent of its own seq 16 statement, and rule 16's second sentence says every span quoted anywhere in the output, including inside a locator or a note, is itself recorded as a claim. Having quoted the span, O2 owed a claim for it
- **re-enters bootstrap entry**: I3

### CLM-0199

- **source_id**: SRC-0002 (IHP-DEVREADME)
- **locator**: Raw dev-branch README.md, section "## Supported Devices", Capacitors bullet, third sentence (beginning on line 74), first predicate
- **excerpt**: "Neither is validated on CMOS5L silicon yet"
- **statement**: Neither [`cap_cmomi` (interdigitated, with feed topology) and `cap_cmomf` (metal fringe / finger)] is validated on CMOS5L silicon yet
- **kind**: QUAL
- **value**: not validated on CMOS5L silicon yet
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw markdown retrieval; plain declarative clause; the negative pronoun 'Neither' is resolved to the two device names printed verbatim earlier in the same bullet; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK
- **rq_ids**: RQ-05
- **source_version**: see SRC-0002
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I3

### CLM-0200

- **source_id**: SRC-0001 (IHP-CMOS5LREPO)
- **locator**: ihp-sg13cmos5l README.md, top-level heading, line 1 of the raw default-branch README.md, as rendered on the repository landing page https://github.com/IHP-GmbH/ihp-sg13cmos5l
- **excerpt**: "# IHP SG13CMOS5L PDK (M1-M4-TM1 stack)"
- **statement**: The ihp-sg13cmos5l README's title is "IHP SG13CMOS5L PDK (M1-M4-TM1 stack)".
- **kind**: QUAL
- **value**: IHP SG13CMOS5L PDK (M1-M4-TM1 stack)
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - verbatim raw-Markdown retrieval of the file the landing page renders; the heading marker is markup and is dropped from statement and value; the subject is the document itself because the predicate is the document's own title, the exception allowed by rule 2; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0001
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I4

### CLM-0201

- **source_id**: SRC-0001 (IHP-CMOS5LREPO)
- **locator**: ihp-sg13cmos5l README.md, blockquoted WARNING callout immediately below the title heading, line 3 of the raw default-branch README.md, as rendered on the repository landing page
- **excerpt**: ``"> This repo is meant to be used **only** as a temporary storage during the development of the `build/compile` migration script for the sg13 cmos5l PDK."``
- **statement**: This repo [IHP SG13CMOS5L PDK (M1-M4-TM1 stack)] is meant to be used **only** as a temporary storage during the development of the `build/compile` migration script for the sg13 cmos5l PDK.
- **kind**: RULE
- **value**: a temporary storage during the development of the `build/compile` migration script for the sg13 cmos5l PDK
- **unit**: DIMENSIONLESS
- **conditions**: during the development of the `build/compile` migration script for the sg13 cmos5l PDK
- **modality**: is meant to be used
- **reading_confidence**: high - verbatim raw-Markdown retrieval of the file the landing page renders; the blockquote marker is markup and is dropped from the statement, the backtick code span around build/compile is kept; the deictic 'This repo' is resolved to a referent printed verbatim in the same document; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0001
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I4

### CLM-0202

- **source_id**: SRC-0001 (IHP-CMOS5LREPO)
- **locator**: Raw default-branch README.md in full (683 bytes, 12 lines, commit 0ebb6c0ef30235e057001fe03650ba521cbbe6d7) retrieved 2026-09-17, together with the same body as rendered on the repository landing page; case-insensitive substring search for the stem licen returned 0 matches, and the variants License, license, Licence, licence and LICENSE each returned 0 matches; the search covered the README body only and not the repository's file list or sidebar, where a LICENSE file may be listed
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ihp-sg13cmos5l README does not contain License.
- **kind**: ABSENCE
- **value**: not present
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high - non-occurrence established by exhaustive case-insensitive substring search over a verbatim raw-Markdown retrieval of the entire 12-line file; the source prints no unit, so unit is DIMENSIONLESS
- **subject_tags**: TECH-PDK, LICENSE
- **rq_ids**: RQ-05
- **source_version**: see SRC-0001
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: I4
