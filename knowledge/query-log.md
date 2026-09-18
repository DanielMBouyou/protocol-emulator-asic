# Query log

Register `QRY-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). The field list is canonical in [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#query-log-fields); the venue list per research question group is fixed by [DEC-0003](decision-log.md#dec-0003-s00-d3-venue-list-per-research-question-group) and the screening depth by [DEC-0002](decision-log.md#dec-0002-s00-d2-screening-depth-per-venue).

Every entry below is a direct retrieval of one named document, not a ranked search. Under DEC-0002 a direct retrieval is a one-item enumerable venue: the listing is the document itself, `screened_depth` is 1, and `screened_list` is that document. No ranked venue has been searched yet; searching begins at [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints), and the query construction procedure of [RESEARCH_METHOD.md](../RESEARCH_METHOD.md#query-construction) applies from there.

`rq_ids` reads NOT APPLICABLE throughout. These retrievals serve no research question: they re-enter statements the project already held, for the double extraction that S00 requires. A retrieval that serves a research question begins at S01.

Each source was retrieved twice, once by each operator of the S00 double extraction, so each document carries two entries. They are separate executions and are logged separately, as the method requires for a repeated query.

| Record | Date | Venue | Query string (the retrieved URL) | Filters | Result count | Screened depth | Included | rq_ids | Executed by |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| QRY-0001 | 2026-09-17 | ORGANIZER-BLOG | https://blog.janestreet.com/protocol-emulator-asic-competition/ | NONE | NOT REPORTED | 1 | ORG-BLOG | NOT APPLICABLE | OP-EXT-1 |
| QRY-0002 | 2026-09-17 | ORGANIZER-BLOG | https://blog.janestreet.com/protocol-emulator-asic-competition/ | NONE | NOT REPORTED | 1 | ORG-BLOG | NOT APPLICABLE | OP-EXT-2 |
| QRY-0003 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/clock/ | NONE | NOT REPORTED | 1 | TT-CLOCK | NOT APPLICABLE | OP-EXT-1 |
| QRY-0004 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/clock/ | NONE | NOT REPORTED | 1 | TT-CLOCK | NOT APPLICABLE | OP-EXT-2 |
| QRY-0005 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/.github/workflows/gds.yaml | NONE | NOT REPORTED | 1 | TT-GDSYAML | NOT APPLICABLE | OP-EXT-1 |
| QRY-0006 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/.github/workflows/gds.yaml | NONE | NOT REPORTED | 1 | TT-GDSYAML | NOT APPLICABLE | OP-EXT-2 |
| QRY-0007 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/gpio/ | NONE | NOT REPORTED | 1 | TT-GPIO | NOT APPLICABLE | OP-EXT-1 |
| QRY-0008 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/gpio/ | NONE | NOT REPORTED | 1 | TT-GPIO | NOT APPLICABLE | OP-EXT-2 |
| QRY-0009 | 2026-09-17 | TT-SITE | https://tinytapeout.com/chips/ttihp0p4/ | NONE | NOT REPORTED | 1 | TT-IHP0P4 | NOT APPLICABLE | OP-EXT-1 |
| QRY-0010 | 2026-09-17 | TT-SITE | https://tinytapeout.com/chips/ttihp0p4/ | NONE | NOT REPORTED | 1 | TT-IHP0P4 | NOT APPLICABLE | OP-EXT-2 |
| QRY-0011 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/info.yaml | NONE | NOT REPORTED | 1 | TT-INFOYAML | NOT APPLICABLE | OP-EXT-1 |
| QRY-0012 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/info.yaml | NONE | NOT REPORTED | 1 | TT-INFOYAML | NOT APPLICABLE | OP-EXT-2 |
| QRY-0013 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/LICENSE | NONE | NOT REPORTED | 1 | TT-LICENSE | NOT APPLICABLE | OP-EXT-1 |
| QRY-0014 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/LICENSE | NONE | NOT REPORTED | 1 | TT-LICENSE | NOT APPLICABLE | OP-EXT-2 |
| QRY-0015 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/memory/ | NONE | NOT REPORTED | 1 | TT-MEMORY | NOT APPLICABLE | OP-EXT-1 |
| QRY-0016 | 2026-09-17 | TT-SITE | https://tinytapeout.com/specs/memory/ | NONE | NOT REPORTED | 1 | TT-MEMORY | NOT APPLICABLE | OP-EXT-2 |
| QRY-0017 | 2026-09-17 | TT-SITE | https://tinytapeout.com/runs/ | NONE | NOT REPORTED | 1 | TT-RUNS | NOT APPLICABLE | OP-EXT-1 |
| QRY-0018 | 2026-09-17 | TT-SITE | https://tinytapeout.com/runs/ | NONE | NOT REPORTED | 1 | TT-RUNS | NOT APPLICABLE | OP-EXT-2 |
| QRY-0019 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/tt-support-tools/ihp-sg13cmos5l/tech/ihp-sg13cmos5l/tile_sizes.yaml | NONE | NOT REPORTED | 1 | TT-TILESIZES | NOT APPLICABLE | OP-EXT-1 |
| QRY-0020 | 2026-09-17 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/tt-support-tools/ihp-sg13cmos5l/tech/ihp-sg13cmos5l/tile_sizes.yaml | NONE | NOT REPORTED | 1 | TT-TILESIZES | NOT APPLICABLE | OP-EXT-2 |
| QRY-0021 | 2026-09-17 | IHP-GITHUB | https://github.com/IHP-GmbH/ihp-sg13cmos5l | NONE | NOT REPORTED | 1 | IHP-CMOS5LREPO | NOT APPLICABLE | OP-EXT-1 |
| QRY-0022 | 2026-09-17 | IHP-GITHUB | https://github.com/IHP-GmbH/ihp-sg13cmos5l | NONE | NOT REPORTED | 1 | IHP-CMOS5LREPO | NOT APPLICABLE | OP-EXT-2 |
| QRY-0023 | 2026-09-17 | IHP-GITHUB | https://raw.githubusercontent.com/IHP-GmbH/IHP-Open-PDK/dev/README.md | NONE | NOT REPORTED | 1 | IHP-DEVREADME | NOT APPLICABLE | OP-EXT-1 |
| QRY-0024 | 2026-09-17 | IHP-GITHUB | https://raw.githubusercontent.com/IHP-GmbH/IHP-Open-PDK/dev/README.md | NONE | NOT REPORTED | 1 | IHP-DEVREADME | NOT APPLICABLE | OP-EXT-2 |
| QRY-0025 | 2026-09-17 | IHP-GITHUB | https://github.com/IHP-GmbH/IHP-Open-PDK | NONE | NOT REPORTED | 1 | IHP-REPO | NOT APPLICABLE | OP-EXT-1 |
| QRY-0026 | 2026-09-17 | IHP-GITHUB | https://github.com/IHP-GmbH/IHP-Open-PDK | NONE | NOT REPORTED | 1 | IHP-REPO | NOT APPLICABLE | OP-EXT-2 |

| QRY-0027 | 2026-09-18 | IHP-GITHUB | https://github.com/IHP-GmbH/ihp-sg13cmos5l | NONE | NOT REPORTED | 1 | IHP-CMOS5LREPO | NOT APPLICABLE | OP-OWNER |
| QRY-0028 | 2026-09-18 | IHP-GITHUB | https://raw.githubusercontent.com/IHP-GmbH/IHP-Open-PDK/dev/README.md | NONE | NOT REPORTED | 1 | IHP-DEVREADME | NOT APPLICABLE | OP-OWNER |
| QRY-0029 | 2026-09-18 | IHP-GITHUB | https://github.com/IHP-GmbH/IHP-Open-PDK | NONE | NOT REPORTED | 1 | IHP-REPO | NOT APPLICABLE | OP-OWNER |
| QRY-0030 | 2026-09-18 | ORGANIZER-BLOG | https://blog.janestreet.com/protocol-emulator-asic-competition/ | NONE | NOT REPORTED | 1 | ORG-BLOG | NOT APPLICABLE | OP-OWNER |
| QRY-0031 | 2026-09-18 | TT-SITE | https://tinytapeout.com/specs/clock/ | NONE | NOT REPORTED | 1 | TT-CLOCK | NOT APPLICABLE | OP-OWNER |
| QRY-0032 | 2026-09-18 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/.github/workflows/gds.yaml | NONE | NOT REPORTED | 1 | TT-GDSYAML | NOT APPLICABLE | OP-OWNER |
| QRY-0033 | 2026-09-18 | TT-SITE | https://tinytapeout.com/specs/gpio/ | NONE | NOT REPORTED | 1 | TT-GPIO | NOT APPLICABLE | OP-OWNER |
| QRY-0034 | 2026-09-18 | TT-SITE | https://tinytapeout.com/chips/ttihp0p4/ | NONE | NOT REPORTED | 1 | TT-IHP0P4 | NOT APPLICABLE | OP-OWNER |
| QRY-0035 | 2026-09-18 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/info.yaml | NONE | NOT REPORTED | 1 | TT-INFOYAML | NOT APPLICABLE | OP-OWNER |
| QRY-0036 | 2026-09-18 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/ttihp-verilog-template/cmos5l/LICENSE | NONE | NOT REPORTED | 1 | TT-LICENSE | NOT APPLICABLE | OP-OWNER |
| QRY-0037 | 2026-09-18 | TT-SITE | https://tinytapeout.com/specs/memory/ | NONE | NOT REPORTED | 1 | TT-MEMORY | NOT APPLICABLE | OP-OWNER |
| QRY-0038 | 2026-09-18 | TT-SITE | https://tinytapeout.com/runs/ | NONE | NOT REPORTED | 1 | TT-RUNS | NOT APPLICABLE | OP-OWNER |
| QRY-0039 | 2026-09-18 | TT-GITHUB | https://raw.githubusercontent.com/TinyTapeout/tt-support-tools/ihp-sg13cmos5l/tech/ihp-sg13cmos5l/tile_sizes.yaml | NONE | NOT REPORTED | 1 | TT-TILESIZES | NOT APPLICABLE | OP-OWNER |

39 entries. The first 26 are the S00 double extraction, two per document. QRY-0027 to QRY-0039 are the retention retrievals of 2026-09-18, performed under [DEC-0014](decision-log.md#dec-0014-retention-is-s00-work-and-the-documents-read-on-2026-09-17-were-never-retained), one per document, each written to the primary-document store and hashed. The hash of each is in its source record, as the [handling of revisions](../RESEARCH_METHOD.md#handling-of-revisions-and-versions) requires of a logged re-access.

## Notes on venue behaviour

- ORG-BLOG: WebFetch returned targeted quotations but refused a full verbatim reproduction. The page was therefore retrieved verbatim as raw HTML with curl (36,703 bytes) to a local scratchpad file, and all excerpts and absence searches were taken from that raw source rather than from a summarizing rendering. Body text extracted by tag-stripping; markup (strong/em) inspected directly in the raw HTML. Only one version of the page was retrieved.
- TT-CLOCK: HTML retrieved directly over HTTPS (HTTP 200, 88701 bytes); text extracted by tag stripping and HTML-entity unescaping. Typographic apostrophes are encoded as &rsquo; in the markup and are reproduced here as U+2019.
- TT-GDSYAML: Retrieved byte-for-byte over HTTPS (HTTP 200, 47 lines). Raw text, no rendering layer.
- TT-GPIO: WebFetch declined to reproduce the page verbatim, so the HTML was retrieved directly over HTTPS (HTTP 200, 91104 bytes) and text extracted by removing script/style/svg blocks, stripping tags and unescaping HTML entities. Prose is byte-identical to the source markup; table cell boundaries are a rendering of the markup.
- TT-IHP0P4: HTML retrieved directly over HTTPS (HTTP 200, 130605 bytes); both the visible body text and the head metadata were inspected separately so the two can be distinguished in locators.
- TT-INFOYAML: Retrieved byte-for-byte over HTTPS (HTTP 200, 56 lines). Raw text, no rendering layer.
- TT-LICENSE: Retrieved byte-for-byte over HTTPS (HTTP 200, 201 lines). Unmodified Apache-2.0 template including the APPENDIX boilerplate.
- TT-MEMORY: HTML retrieved directly over HTTPS (HTTP 200, 98453 bytes); text extracted by tag stripping and HTML-entity unescaping. The micro sign and superscript two in the table headers are encoded as entities in the markup.
- TT-RUNS: HTML retrieved directly over HTTPS (HTTP 200, 98017 bytes); table cells extracted from the markup in document order.
- TT-TILESIZES: Retrieved byte-for-byte over HTTPS (HTTP 200, 16 lines, one key per line).
- IHP-CMOS5LREPO: Fetched twice via WebFetch; content available only as GitHub's rendered HTML converted to markdown, so excerpts are marked unverified. README body consists of the H1 heading, a Warning callout, a "## How to use it during development stage" section with a git clone code block and one following paragraph; no licence section appears in that body.
- IHP-DEVREADME: Verbatim raw markdown retrieved in full; contains the sections "# SG13G2 Process Node", "# SG13CMOS5L Process Node", "# Current status -- Preview" and "## Supported Devices".
- IHP-REPO: Fetched twice via WebFetch; content available only as GitHub's rendered HTML converted to markdown, so excerpts are marked unverified. The rendered README shows the sentence "As of March 2023, this repository is targeting the SG13G2 process node." with no following SG13CMOS5L sentence, and no SG13CMOS5L or ihp-sg13cmos5l token anywhere on the page.

