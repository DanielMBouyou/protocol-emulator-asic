# RESEARCH_METHOD

Canonical location for how research is conducted in this project: source priority, search strategy, personal communication and the question log, inclusion and exclusion, structured extraction, version handling, reproducibility, the stop rule, and the candidate data methods. The rules that govern what an extracted record must contain and what it may become (locator, value, unit, conditions, absence, contradictions, deduplication, independence, status labels, promotion, definitions of FACT, OBSERVATION, HYPOTHESIS and DECISION) are canonical in [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md) and are not restated here. The objective of this file is that two persons applying it independently to the same research question produce the same query log, the same screening decisions and the same claim records.

## Source priority

Sources are assigned exactly one tier. The tier is recorded in the source record with the rule that assigned it.

| Tier | Name | Assignment rule (first matching rule applies, in order) |
| --- | --- | --- |
| 1 | Primary and normative | (a) the document is published by the body that owns or standardizes the subject: for a protocol, the official standards body or the specification owner; for the challenge, the organizer; for the shuttle, Tiny Tapeout; for the process, the foundry; (b) the document is a written personal communication from one of those parties, logged per [Personal communication and the question log](#personal-communication-and-the-question-log); (c) the document is the repository or file that itself constitutes the artifact described (a template, a configuration file, a PDK file). |
| 2 | Vendor documentation | The document is published by the maker of the system it describes: datasheet, reference manual, application note, errata, official example. |
| 3 | Peer-reviewed | The document passed a documented review process: journal article, conference paper with a program committee, examined thesis. |
| 4 | Secondary | Anything else: blog posts, forum threads, wikis, tutorials, news, preprints without review, community documentation, videos. |

Rules:

- A claim is extracted from the highest-tier source available for it. A lower-tier source is used for the same claim only as an additional pointer, or when no higher-tier source exists, in which case the tier is recorded on the claim; which status label such a claim can support is governed by [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#status-labels).
- For protocols, the Tier 1 source is the current normative specification of the standards body or the specification owner. A protocol without a standards body has the originating owner's specification as Tier 1 for that protocol, recorded as owner-originated. A vendor reference manual describing how one product implements a protocol is Tier 2 for the protocol and Tier 2 for the product.
- A document that reproduces or paraphrases another document is assigned the tier of its own publisher, and its source record lists the reproduced document under derived_from so that independence can be computed per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#independence-of-sources).
- When tiers disagree on a statement, the disagreement is a contradiction per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#contradictions); it is not resolved by tier.
- When the tier assignment is ambiguous, both persons record their assignment and the reason; the rule text is amended so that the case is no longer ambiguous, and the amendment is logged as a DECISION.

## Search strategy

### Query construction

1. For each research question, list the concept blocks: the object (what the question is about), the attribute (what is asked about it), and the context (the constraint or setting). Each block gets a list of synonyms and acronyms; the lists are recorded in the query log under the research question before any query is run.
2. Queries are formed as combinations of one term from each block. Every combination run is logged; combinations not run are logged as not run.
3. The venue list per research question group (search engines, publisher databases, citation indexes, code repository searches, standards body catalogues, direct URLs, personal communication) is fixed as a DECISION at S00 and recorded in the query log. A venue outside the list may be used only if it is added to the list by a logged DECISION.
4. The operators available in the venue (quotation marks, boolean operators, site or date filters) are recorded exactly as typed.

### Query log fields

Every query, including those with zero useful results, has one entry:

| Field | Content |
| --- | --- |
| query_id | QRY- followed by a sequence number |
| rq_ids | research question identifiers served |
| date | ISO 8601 date of execution |
| venue | venue name as listed in the venue list |
| query_string | exact string as typed, including operators |
| filters | date range, language, document type, or NONE |
| result_count | count reported by the venue, or NOT REPORTED |
| screened_depth | number of results screened; the depth to screen per venue is a DECISION at S00 |
| screened_list | the title and URL of every screened result, in the order shown |
| included_ids | source identifiers included from this query |
| executed_by | person |
| notes | venue behaviour observed (personalization, unavailability, captcha) |

The screened_list is what makes a non-deterministic web search reproducible: a re-run is compared against the list, not against the live results. Repeating a query on a later date is a new entry linked to the original; differences are recorded, never overwritten.

### Snowballing

- Backward: the references or links of every included source are screened. Logged as a query with venue SNOWBALL-B and the seed source identifier in query_string.
- Forward: works citing an included source, through the citation index of the venue list. Logged as SNOWBALL-F.
- Sibling: other documents of the same publisher on the same subject (for example all pages of a specification site). Logged as SNOWBALL-S.
- Snowballing continues until a pass over all included sources adds no new included source (closure). The closure pass is logged.

### Personal communication and the question log

A question sent to the organizer, to Tiny Tapeout, to a foundry or to a vendor is recorded in the question log with the verbatim question, addressee, channel, date sent, the open question or research question identifiers it serves, and exactly one state:

- ANSWERED: a written reply exists and is registered as a Tier 1 or Tier 2 source record with the reply text retained verbatim; the claims extracted from it are what answers the question.
- ASKED: sent, no written reply yet. The date of each check for a reply is appended.
- UNANSWERABLE_UNTIL: the addressee stated in writing, or the included sources show, that the answer depends on a named external event; the event is recorded.

Each sending is also a query log entry with venue PERSONAL-COMM. A verbal reply is logged as a claim with the caveat NOT_WRITTEN; it does not change the state from ASKED and does not answer an open question until confirmed in writing or on the addressee's own page. A reply that is public (a page revision, a public issue answer) is registered as an ordinary source and the state becomes ANSWERED.

## Inclusion and exclusion criteria

Screening has two passes. Pass 1 uses title, abstract or first page. Pass 2 uses the full text. Each pass records for each candidate exactly one decision code and the criterion text it applied.

Inclusion requires all of:

- C1: the document bears on at least one research question, and the research question identifier is recorded.
- C2: the document is retrievable and a copy can be retained in the primary-document store (location fixed by DECISION at S00).
- C3: the publisher or author is identifiable.
- C4: the language is one a team member reads; if a translation is used, the translator and the translated span are recorded.
- C5: for a corpus candidate, it falls inside the corpus universe definition recorded as a DECISION at S03 of [PREBENCH_PLAN.md](PREBENCH_PLAN.md#s03-protocol-and-workload-corpus).

Exclusion codes:

| Code | Meaning |
| --- | --- |
| EX-SCOPE | fails C1 |
| EX-NOSRC | fails C3 |
| EX-DUP | same document as an included source under another URL; recorded as an alias of the included source, not as a separate source |
| EX-VERSION | superseded version of an included source, not needed for history; if needed for history, it is included and marked superseded |
| EX-MARKETING | contains no verifiable claim |
| EX-DERIVED | a summary, generated or not, with no source trail, when the original is retrievable |
| EX-ACCESS | fails C2; the document is recorded as KNOWN-UNRETRIEVED with the reason and is never silently dropped |
| EX-LANG | fails C4 |
| EX-UNIVERSE | fails C5; the criterion text of the universe definition that excluded it is quoted |

No exclusion code refers to an implementation consideration. A source that supports a fact used in any gate condition is screened by two persons independently. A disagreement is resolved by both re-reading the criterion text against the document; if the text does not settle it, the criterion text is amended and the amendment logged as a DECISION. Preference is never a resolution.

## Structured extraction

Extraction produces two record types. The required content of the fields (locator format, value, unit, conditions, absence, verbatim quotation) is governed by [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md); this section fixes which fields exist.

### Source record fields

| Field | Content |
| --- | --- |
| source_id | SRC- followed by a sequence number |
| tier | 1 to 4, with the assignment rule letter |
| kind | standard, specification, datasheet, reference manual, application note, errata, paper, thesis, repository file, web page, personal communication, form response, forum post, video |
| title | verbatim |
| publisher_or_author | as printed |
| identifier | DOI, document number, ISBN, commit hash, or NONE |
| url | exact as retrieved, including fragment |
| version | version, revision, branch or publication date as printed; NOT STATED if absent |
| accessed_on | ISO 8601 date |
| retained_copy | file name in the primary-document store and its content hash |
| redistribution | the license or terms that govern storing the copy in the public repository, or NOT STATED; consequences per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#retention-of-primary-documents) |
| derived_from | source identifiers this document reproduces or cites for the claims extracted from it |
| relations | supersedes, superseded_by, cites, cited_by (source identifiers), or NONE |
| found_by | query identifier |
| screening | pass 1 and pass 2 decision codes, screeners |
| aliases | other URLs of the same document |

### Claim record fields

| Field | Content |
| --- | --- |
| claim_id | CLM- followed by a sequence number |
| source_id | the source record |
| locator | page, section, heading, line, field name or timestamp, per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#provenance-of-every-claim) |
| excerpt | verbatim minimal span, in quotation marks |
| statement | normalized single-predicate statement per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#atomic-fact-rule) |
| kind | QUANT, QUAL, RULE, DEFINITION, PROCEDURE, ABSENCE |
| value, unit, conditions | for QUANT; NOT APPLICABLE otherwise |
| modality | the modal word as printed (must, should, may, is targeting, and so on), or NONE |
| reading_confidence | UNAMBIGUOUS, or NEEDS-INTERPRETATION with the interpretation written out |
| subject_tags | from the controlled vocabulary fixed at S00; adding a tag is a logged DECISION |
| rq_ids | research question identifiers |
| source_version | copy of the source version field at extraction time |
| extracted_by and extracted_on | person and ISO 8601 date |
| double_extraction | claim identifier of the independent extraction, or NONE |
| caveats | NOT_WRITTEN for verbal replies; NONE otherwise |

Double extraction: the fraction of claims extracted independently by two persons, and which claims (at least every claim supporting a gate condition), is fixed as a DECISION at S00. Two extractions of the same span must be identical after normalization; a difference is resolved by amending the rule that produced it, then re-extracting.

## Separation of source, claim and canonical knowledge

A source record describes a document. A claim record describes what one document says at one locator. A canonical fact consolidates one or more claims into one statement of the knowledge base. Nothing enters the knowledge base except through a claim. The consolidation rules, independence, contradictions, deduplication and promotion are canonical in [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md).

## Handling of revisions and versions

1. A new version of an included document creates a new source record with supersedes set in relations; the old record is kept and marked superseded_by.
2. Every claim of the old record is compared against the new version and marked SAME, CHANGED or REMOVED, with the new locator when SAME or CHANGED.
3. A canonical fact that depends on a CHANGED or REMOVED claim moves to the REVERIFY state per [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#promotion-and-retirement).
4. Web pages and repository branches without a version identifier are versioned by accessed_on and retained copy hash; a re-access with a different hash is treated as a new version.
5. Sources supporting a MOVING_CONSTRAINT are re-accessed on the schedule of [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md#status-labels); all other sources are re-accessed at benchmark freeze. Each re-access is logged with date and hash.

## Reproducibility

Another person can redo the search when the following exist: the concept blocks and synonym lists per research question; the venue list; every query log entry with its screened_list; every screening decision with its code; every source record with its retained copy hash; every claim record with its locator and excerpt; every question log entry; every DECISION that fixed a parameter of this method; and, for every computation on the dataset, the input dataset version, the method, the parameters, the seeds, the software versions and the output hash.

A reproduction re-runs the logged queries of the reproduction set (fixed as a DECISION at S00), compares the results against the logged screened_list and included_ids, and records every difference as an OBSERVATION; it never edits the original log. The reproduction of dataset computations regenerates the output from the logged inputs and compares hashes.

## Stop and saturation rule

Saturation is declared per research question by the following procedure, and its declaration is logged with the round counts.

1. A round is one complete execution of the query combinations on every venue of the list, followed by snowball closure and extraction.
2. After each round, record: new included sources, new claims, new canonical facts, new contradictions, and new corpus entries (for corpus questions) for the research question.
3. Before a round can be counted as empty, at least one new query combination for the research question that was not used in any previous round (new synonym, new venue or new tier) is formed, run and logged; an empty round without a new combination does not count.
4. Saturation requires all of:
   - (a) every Tier 1 source that any included source names as authoritative for the subject has been retrieved or recorded KNOWN-UNRETRIEVED;
   - (b) every venue of the list and every tier has been searched at least once for the question, and, for protocol questions, the owner body of every corpus protocol concerned has been queried;
   - (c) the last K consecutive rounds added zero new canonical facts and zero new corpus entries for the research question; K is fixed as a DECISION at S00 with recorded rationale;
   - (d) two persons independently confirm (a) and (b) by listing the authoritative sources and venues and checking each against the source register and the query log;
   - (e) every open contradiction touching the research question has a resolution path logged.
5. Saturation is reopened when a new Tier 1 source appears, when an included source is revised, or when a personal communication answers or changes a question; reopening is logged and the rule applied again.

No research question is closed by elapsed time alone; the schedule of [PREBENCH_PLAN.md](PREBENCH_PLAN.md) fixes when saturation is checked, not when it is declared.

## Statistical and data methods to study later

The following families are candidates to be evaluated at stages S06, S07 and S09 of [PREBENCH_PLAN.md](PREBENCH_PLAN.md). Listing a family here does not select it; selection is a DECISION with rationale at the stage that uses it, and a family may be rejected. The list is open.

| Purpose | Candidate families |
| --- | --- |
| Corpus reduction and redundancy | distance and similarity measures on mixed-type feature vectors; hierarchical, partition-based and density-based clustering with medoid representatives; set-cover and maximum-coverage selection of representatives; duplicate detection by feature equivalence classes; correlation and mutual information between schema fields to detect redundant fields |
| Representativeness | coverage of each field's value range and of category combinations by the subset; distribution comparison between subset and full dataset per field; stratification by field; distance from each holdout entry to its nearest benchmark entry; stratified sampling as a comparison baseline for computed selections |
| Dimensionality and structure | principal component analysis; multidimensional scaling; correlation analysis between fields |
| Sensitivity analysis | one-at-a-time perturbation; variance-based global sensitivity; bootstrap resampling of entries; leave-one-out and jackknife over entries and over fields; parameter sweeps of the retained reduction method; perturbation of the treatment of missing values; set overlap and rank correlation between selections across perturbations |
| Pareto comparison | non-dominated sorting; epsilon-dominance; hypervolume and other quality indicators, each with its reference-point convention recorded; dominance under interval or distributional uncertainty; robustness of dominance under changed constraints; pre-registered comparison protocols |
| Reproducibility of computed results | fixed seeds, recorded software versions and result hashing, applied to whichever family is selected |

For each family evaluated, the evaluation record states: the Tier 3 or higher sources for its definition; its assumptions on the data types of the schema; its behaviour with missing values; the parameters that would need a DECISION; and the result on the actual dataset, recorded as an OBSERVATION.
