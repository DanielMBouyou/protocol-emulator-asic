# Source register

Register `SRC-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). The field list is canonical in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#source-record-fields). Record format per [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store).

Every document below was retrieved twice on 2026-09-17, once by each operator of the S00 double extraction, and each retrieval has its own entry in [query-log.md](query-log.md).

`retained_copy` was PENDING until 2026-09-18, when every document was retrieved as raw bytes, written to the primary-document store and hashed under [DEC-0014](decision-log.md#dec-0014-retention-is-s00-work-and-the-documents-read-on-2026-09-17-were-never-retained). That decision also corrects the earlier statement, made here and in three other records, that the store is populated at S01. Retention is S00 work under the [slip rule](../PREBENCH_PLAN.md#slip-rule).

**The copy is not the document the claims were read from.** Every record below was accessed on 2026-09-17 and retained on 2026-09-18. The bytes read on the 17th were never hashed, so identity across the two dates is not established and cannot now be established. The `retained_copy` field therefore carries the date the copy was taken, so that no record asserts otherwise. What the retained copies do and do not support is measured in [OBS-0004](observation-register.md#obs-0004-re-check-of-every-s00-claim-against-its-retained-copy), and the permanent loss is [LIM-0003](limitation-register.md#lim-0003-the-documents-the-s00-claims-were-read-from-were-never-retained).


### SRC-0001 IHP-GmbH/ihp-sg13cmos5l (repository landing page)

- **source_key**: IHP-CMOS5LREPO
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: code repository landing page (rendered HTML)
- **title**: IHP-GmbH/ihp-sg13cmos5l (repository landing page)
- **publisher_or_author**: IHP GmbH
- **identifier**: github.com/IHP-GmbH/ihp-sg13cmos5l
- **url**: https://github.com/IHP-GmbH/ihp-sg13cmos5l
- **version**: default branch rendering, retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0001_IHP-CMOS5LREPO.html`, sha256 `d8e79eb2ea8d868caf2af92339d51397cefb5f52d5779b825f83a54694fda695`, 258830 bytes, copy taken 2026-09-18. This page embeds a per-request `request-id` and `html-safe-nonce`, so two retrievals minutes apart differ in bytes. The hash identifies this copy and is not an identity for the document
- **redistribution**: Repository lists an Apache-2.0 licence file; short excerpts quoted for analysis
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Fetched twice via WebFetch; content available only as GitHub's rendered HTML converted to markdown, so excerpts are marked unverified. README body consists of the H1 heading, a Warning callout, a "## How to use it during development stage" section with a git clone code block and one following paragraph; no licence section appears in that body.

### SRC-0002 IHP Open Source PDK README (dev branch)

- **source_key**: IHP-DEVREADME
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: raw markdown README
- **title**: IHP Open Source PDK README (dev branch)
- **publisher_or_author**: IHP GmbH / IHP PDK Authors
- **identifier**: IHP-GmbH/IHP-Open-PDK, dev branch, README.md
- **url**: https://raw.githubusercontent.com/IHP-GmbH/IHP-Open-PDK/dev/README.md
- **version**: dev branch, retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0002_IHP-DEVREADME.md`, sha256 `d62b7266f2ff8ef7640e19c0655fc518333019e36431d00aff60b24e06103030`, 9496 bytes, copy taken 2026-09-18
- **redistribution**: Apache-2.0 (per the README's own License section); short excerpts quoted for analysis
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Verbatim raw markdown retrieved in full; contains the sections "# SG13G2 Process Node", "# SG13CMOS5L Process Node", "# Current status -- Preview" and "## Supported Devices".

### SRC-0003 IHP-GmbH/IHP-Open-PDK (repository landing page)

- **source_key**: IHP-REPO
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: code repository landing page (rendered HTML)
- **title**: IHP-GmbH/IHP-Open-PDK (repository landing page)
- **publisher_or_author**: IHP GmbH
- **identifier**: github.com/IHP-GmbH/IHP-Open-PDK
- **url**: https://github.com/IHP-GmbH/IHP-Open-PDK
- **version**: default branch rendering, retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0003_IHP-REPO.html`, sha256 `5be7a79aad867ce664c2afdca9b4086aace7e9428cd4cd877da68aa7253e35f1`, 339851 bytes, copy taken 2026-09-18. This page embeds a per-request `request-id` and `html-safe-nonce`, so two retrievals minutes apart differ in bytes. The hash identifies this copy and is not an identity for the document
- **redistribution**: Repository released under Apache-2.0; short excerpts quoted for analysis
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Fetched twice via WebFetch; content available only as GitHub's rendered HTML converted to markdown, so excerpts are marked unverified. The rendered README shows the sentence "As of March 2023, this repository is targeting the SG13G2 process node." with no following SG13CMOS5L sentence, and no SG13CMOS5L or ihp-sg13cmos5l token anywhere on the page.

### SRC-0004 Can you design a chip? Announcing the protocol emulator ASIC competition

- **source_key**: ORG-BLOG
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: Organizational blog post (corporate engineering blog, competition announcement)
- **title**: Can you design a chip? Announcing the protocol emulator ASIC competition
- **publisher_or_author**: Jane Street Blog; By: Benjamin Devlin, By: Anish Singhani
- **identifier**: blog.janestreet.com/protocol-emulator-asic-competition/
- **url**: https://blog.janestreet.com/protocol-emulator-asic-competition/
- **version**: Published Sep 10, 2026; retrieved 2026-09-17; page states "4 min read"
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0004_ORG-BLOG.html`, sha256 `b01497ccf9bb8636f62e9b4433f3af884637e8d46048bd71b4bef5ffc988a909`, 36703 bytes, copy taken 2026-09-18
- **redistribution**: Copyrighted corporate blog content. Short verbatim quotation for citation and fact-checking only; full reproduction not permitted. The WebFetch summarizer explicitly declined to reproduce the page in full on copyright grounds.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: WebFetch returned targeted quotations but refused a full verbatim reproduction. The page was therefore retrieved verbatim as raw HTML with curl (36,703 bytes) to a local scratchpad file, and all excerpts and absence searches were taken from that raw source rather than from a summarizing rendering. Body text extracted by tag-stripping; markup (strong/em) inspected directly in the raw HTML. Only one version of the page was retrieved.

### SRC-0005 Clock

- **source_key**: TT-CLOCK
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: web page, HTML documentation
- **title**: Clock
- **publisher_or_author**: Tiny Tapeout
- **identifier**: tinytapeout.com/specs/clock/
- **url**: https://tinytapeout.com/specs/clock/
- **version**: retrieved 2026-09-17; site generator meta value Hugo 0.160.1
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0005_TT-CLOCK.html`, sha256 `0a4a6c0fae703330cbcdd1c000925602b44c84b3ce7b30bfd19318b596aaba3e`, 88701 bytes, copy taken 2026-09-18
- **redistribution**: Quoted verbatim in short excerpts for analysis; site terms not reproduced here.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: HTML retrieved directly over HTTPS (HTTP 200, 88701 bytes); text extracted by tag stripping and HTML-entity unescaping. Typographic apostrophes are encoded as &rsquo; in the markup and are reproduced here as U+2019.

### SRC-0006 .github/workflows/gds.yaml

- **source_key**: TT-GDSYAML
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: repository file, GitHub Actions workflow YAML
- **title**: .github/workflows/gds.yaml
- **publisher_or_author**: Tiny Tapeout (TinyTapeout GitHub organisation)
- **identifier**: TinyTapeout/ttihp-verilog-template
- **url**: https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/.github/workflows/gds.yaml
- **version**: branch cmos5l; retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0006_TT-GDSYAML.yaml`, sha256 `070480c2c2bc08f9c972161c0f424dc9238a8f3c3c3aafdc67851edd61eadbd3`, 1007 bytes, copy taken 2026-09-18
- **redistribution**: Repository ships an Apache License Version 2.0 LICENSE file; short verbatim excerpts quoted here for analysis.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Retrieved byte-for-byte over HTTPS (HTTP 200, 47 lines). Raw text, no rendering layer.

### SRC-0007 GPIO pins

- **source_key**: TT-GPIO
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: web page, HTML documentation
- **title**: GPIO pins
- **publisher_or_author**: Tiny Tapeout
- **identifier**: tinytapeout.com/specs/gpio/
- **url**: https://tinytapeout.com/specs/gpio/
- **version**: retrieved 2026-09-17; site generator meta value Hugo 0.160.1
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0007_TT-GPIO.html`, sha256 `6d0f75beaf46d0e9e28ab5fccb0205c778074f479d0b8f6d5120eaa076c41e6d`, 91104 bytes, copy taken 2026-09-18
- **redistribution**: Quoted verbatim in short excerpts for analysis; site terms not reproduced here.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: WebFetch declined to reproduce the page verbatim, so the HTML was retrieved directly over HTTPS (HTTP 200, 91104 bytes) and text extracted by removing script/style/svg blocks, stripping tags and unescaping HTML entities. Prose is byte-identical to the source markup; table cell boundaries are a rendering of the markup.

### SRC-0008 Tiny Tapeout IHP 0.4

- **source_key**: TT-IHP0P4
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: web page, HTML shuttle page
- **title**: Tiny Tapeout IHP 0.4
- **publisher_or_author**: Tiny Tapeout
- **identifier**: tinytapeout.com/chips/ttihp0p4/
- **url**: https://tinytapeout.com/chips/ttihp0p4/
- **version**: retrieved 2026-09-17; page metadata itemprop dateModified 2026-09-15T20:16:23+01:00
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0008_TT-IHP0P4.html`, sha256 `b14e9c2b52dfc015af7af9a531e2a07ee318e769dffeaec050c44afbafffc785`, 130605 bytes, copy taken 2026-09-18
- **redistribution**: Quoted verbatim in short excerpts for analysis; site terms not reproduced here.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: HTML retrieved directly over HTTPS (HTTP 200, 130605 bytes); both the visible body text and the head metadata were inspected separately so the two can be distinguished in locators.

### SRC-0009 info.yaml

- **source_key**: TT-INFOYAML
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: repository file, YAML
- **title**: info.yaml
- **publisher_or_author**: Tiny Tapeout (TinyTapeout GitHub organisation)
- **identifier**: TinyTapeout/ttihp-verilog-template
- **url**: https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/info.yaml
- **version**: branch cmos5l; retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0009_TT-INFOYAML.yaml`, sha256 `3b149957d61b8516f55e0d613919691eb04c1728daa762e17343b919f13b78f2`, 1584 bytes, copy taken 2026-09-18
- **redistribution**: Repository ships an Apache License Version 2.0 LICENSE file; short verbatim excerpts quoted here for analysis.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Retrieved byte-for-byte over HTTPS (HTTP 200, 56 lines). Raw text, no rendering layer.

### SRC-0010 LICENSE

- **source_key**: TT-LICENSE
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: repository file, plain-text licence
- **title**: LICENSE
- **publisher_or_author**: Apache Software Foundation licence text as shipped in TinyTapeout/ttihp-verilog-template
- **identifier**: TinyTapeout/ttihp-verilog-template
- **url**: https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/LICENSE
- **version**: branch cmos5l; retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0010_TT-LICENSE.txt`, sha256 `c71d239df91726fc519c6eb72d318ec65820627232b2f796219e87dcf35d0ab4`, 11357 bytes, copy taken 2026-09-18
- **redistribution**: Apache License Version 2.0 text; freely redistributable.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Retrieved byte-for-byte over HTTPS (HTTP 200, 201 lines). Unmodified Apache-2.0 template including the APPENDIX boilerplate.

### SRC-0011 Memory

- **source_key**: TT-MEMORY
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: web page, HTML documentation
- **title**: Memory
- **publisher_or_author**: Tiny Tapeout
- **identifier**: tinytapeout.com/specs/memory/
- **url**: https://tinytapeout.com/specs/memory/
- **version**: retrieved 2026-09-17; site generator meta value Hugo 0.160.1
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0011_TT-MEMORY.html`, sha256 `3ccdf268dfeb692a79ce26b8bcfb78da99391d6f3175be33b025413fdac6c203`, 98453 bytes, copy taken 2026-09-18
- **redistribution**: Quoted verbatim in short excerpts for analysis; site terms not reproduced here.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: HTML retrieved directly over HTTPS (HTTP 200, 98453 bytes); text extracted by tag stripping and HTML-entity unescaping. The micro sign and superscript two in the table headers are encoded as entities in the markup.

### SRC-0012 Tiny Tapeout Chips

- **source_key**: TT-RUNS
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: web page, HTML table of shuttle runs
- **title**: Tiny Tapeout Chips
- **publisher_or_author**: Tiny Tapeout
- **identifier**: tinytapeout.com/runs/
- **url**: https://tinytapeout.com/runs/
- **version**: retrieved 2026-09-17; site generator meta value Hugo 0.160.1
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0012_TT-RUNS.html`, sha256 `f1d081be2ac30a5e92beb18a0138684525bb4df4f57fe155a79e1159bf6a8257`, 98017 bytes, copy taken 2026-09-18
- **redistribution**: Quoted verbatim in short excerpts for analysis; site terms not reproduced here.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: HTML retrieved directly over HTTPS (HTTP 200, 98017 bytes); table cells extracted from the markup in document order.

### SRC-0013 tech/ihp-sg13cmos5l/tile_sizes.yaml

- **source_key**: TT-TILESIZES
- **tier**: 1, by assignment rule (a): the document is published by the party that owns or standardizes the subject
- **kind**: repository file, YAML mapping
- **title**: tech/ihp-sg13cmos5l/tile_sizes.yaml
- **publisher_or_author**: Tiny Tapeout (TinyTapeout GitHub organisation)
- **identifier**: TinyTapeout/tt-support-tools
- **url**: https://raw.githubusercontent.com/TinyTapeout/tt-support-tools/ihp-sg13cmos5l/tech/ihp-sg13cmos5l/tile_sizes.yaml
- **version**: branch ihp-sg13cmos5l; retrieved 2026-09-17
- **accessed_on**: 2026-09-17
- **retained_copy**: `SRC-0013_TT-TILESIZES.yaml`, sha256 `b70060737ca784124602a6104041055d5245175d3ca2c08519226abcfd577c63`, 406 bytes, copy taken 2026-09-18
- **redistribution**: Short verbatim excerpts quoted here for analysis; upstream repository licence not fetched in this pass.
- **derived_from**: NONE
- **relations**: NONE
- **found_by**: the query log entries recording this URL
- **screening**: not screened; this document was named by a bootstrap statement, not found by a search
- **aliases**: NONE
- **retrieval note**: Retrieved byte-for-byte over HTTPS (HTTP 200, 16 lines, one key per line).
