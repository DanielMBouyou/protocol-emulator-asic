# EVIDENCE_POLICY

Canonical location for the provenance and consolidation rules of the knowledge base, the registers and their identifiers, the status labels, and the definitions of FACT, OBSERVATION, HYPOTHESIS and DECISION. The search, screening and extraction procedure that produces the records governed here is canonical in [RESEARCH_METHOD.md](RESEARCH_METHOD.md). The objective of this file is that two persons consolidating the same claims independently produce identical fact records.

## Root of evidence

Primary documents (specifications, PDFs, repository files, retained copies of web pages, logged written personal communications) are the root of evidence. The Markdown knowledge base is consolidated knowledge derived from them through claim records; it is not a collection of summaries and never replaces reading the source. Any statement in the knowledge base that cannot be followed back to a claim and a retained document is removed or converted to an OPEN_QUESTION.

## Registers and identifiers

| Register | Identifier | Holds |
| --- | --- | --- |
| source register | SRC-nnnn | one record per document, fields per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#structured-extraction) |
| claim register | CLM-nnnn | one record per statement at one locator of one source |
| fact register | FCT-nnnn | canonical facts consolidated from claims |
| observation register | OBS-nnnn | results measured or computed by the team |
| hypothesis register | HYP-nnnn | isolated conjectures |
| decision log | DEC-nnnn | choices made by the team, including subtype ASSUMPTION; a record may additionally carry the plan label under which [PREBENCH_PLAN.md](PREBENCH_PLAN.md) names it |
| contradiction register | CTR-nnnn | conflicting claims kept side by side |
| query log | QRY-nnnn | searches, per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#query-log-fields) |
| question log | QST-nnnn | questions sent to external parties and their state, per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log) |
| limitation register | LIM-nnnn | instabilities, coverage gaps and known limits of a computed result, each with the artifact and version it affects |

Identifiers are never reused or renumbered. A retired record keeps its identifier and its state. The bootstrap identifiers of [PROJECT_SCOPE.md](PROJECT_SCOPE.md#challenge-constraints-as-currently-known) are mapped to these registers at stage S00.

## Definitions

Every entry belongs to exactly one category.

### FACT

A FACT is an atomic statement about the world outside the project, supported by at least one claim from an included source.

- Requires: statement per the [atomic fact rule](#atomic-fact-rule); at least one claim identifier with locator; a status label per [Status labels](#status-labels); a lifecycle state per [Promotion and retirement](#promotion-and-retirement); the date of last verification; the list of contradiction identifiers if any; for quantitative facts, value, unit and conditions.
- May appear: in the fact register; in the constraints section of PROJECT_SCOPE.md; in any document as a citation by identifier.
- May not: be created from an OBSERVATION, a HYPOTHESIS or a DECISION.

### OBSERVATION

An OBSERVATION is a result the team obtained by running a procedure: a computation on the dataset, a number derived from FACTs (a product, a conversion), a tool run, an audit, a reproduction.

- Requires: the procedure (inputs by identifier and version, tool and version, exact steps or command, environment); the raw output retained with its hash; date; operator; the statement of what was observed, scoped to the run. An OBSERVATION does not state anything about the world beyond the run it describes.
- May appear: in the observation register; in stage artifacts and audit reports; in a DECISION rationale; in PROJECT_SCOPE.md only in a section marked as observations.
- May not: be recorded as a FACT; be generalized without a new OBSERVATION that supports the generalization; be relabelled when cited by another party.

### HYPOTHESIS

A HYPOTHESIS is a conjecture that no claim or observation yet supports, including every idea within the scope fixed in [PROJECT_SCOPE.md](PROJECT_SCOPE.md#hypothesis-isolation-scope).

- Requires: statement; what evidence would support it; what evidence would refute it; the research question or stage it targets; author; date; state among UNTESTED, TESTING, SUPPORTED, REFUTED, WITHDRAWN.
- May appear: only in the hypothesis register or in a section whose heading is exactly "HYPOTHESES" inside a stage artifact, labelled HYPOTHESIS on every line where it is mentioned. This is the isolation rule; it has no other statement in the repository.
- May not: appear in a gate condition, a DECISION rationale, a metric, a benchmark entry, an inclusion or exclusion decision, a summary, a conclusion, README.md or the non-observation sections of PROJECT_SCOPE.md; be presented as a result, a recommendation or a finding. A SUPPORTED hypothesis does not become a FACT; the claims or observations that support it are what the knowledge base records. A sentence outside the permitted locations that reads as a preference or an expectation is moved to the register or removed.

### DECISION

A DECISION is a choice made by the team that binds later work.

- Requires: identifier; date; deciders; statement of the choice; options considered and why rejected; the FACT and OBSERVATION identifiers relied on; rationale; scope (what it binds); the stage; a revisit trigger (the event that reopens it).
- Subtype ASSUMPTION: a DECISION that substitutes a working value or rule for an OPEN_QUESTION. It names the OQ identifier, states that the value is not sourced, and lists every artifact that depends on it. An ASSUMPTION never enters the fact register and is never cited as a FACT.
- May appear: in the decision log; elsewhere only by identifier. A choice without a record is not a DECISION and has no standing.
- May not: create a FACT; select anything covered by the [prohibition](PROJECT_SCOPE.md#temporary-prohibition-of-microarchitectural-choices) before the ARCHITECTURE GATE. A DECISION is retired only by a later DECISION that names it; it is never edited in place.

## Status labels

Every FACT carries one or two of the following labels; an unknown needed by the project carries the third.

- CONFIRMED_FACT: supported by at least one Tier 1 claim ([RESEARCH_METHOD.md](RESEARCH_METHOD.md#source-priority)), verified on the recorded date, and the source does not itself present the statement as provisional.
- MOVING_CONSTRAINT: the source presents the statement as targeted, planned, current, subject to change, or as a schedule; or the value differed between two versions of the source. A fact may carry CONFIRMED_FACT and MOVING_CONSTRAINT together when the statement is confirmed but its value is announced as movable. MOVING_CONSTRAINT facts are re-verified at every stage gate and at benchmark freeze, and the date is updated. Every artifact that depends on a MOVING_CONSTRAINT records that dependence and, where the alternatives are known, stays valid under each alternative.
- OPEN_QUESTION: a statement the project needs that no included source provides, or that included sources contradict. It carries an OQ identifier, links to a research question, holds no value, and has a question-log state per [RESEARCH_METHOD.md](RESEARCH_METHOD.md#personal-communication-and-the-question-log).

## Atomic fact rule

A fact statement is written so that two persons produce the same text from the same claim:

1. One subject, one predicate, one value or object, optional conditions. A source sentence with two predicates yields two facts.
2. The subject and the predicate use the source's own terms; no synonym substitution, no translation of units, no rounding.
3. Qualifiers of precision printed by the source (about, approximately, ~, roughly) are kept in the statement and the precision field is set to AS_STATED.
4. Modal words (must, should, may, is targeting, will) are kept as printed; they carry the hardness of a rule and are never upgraded or downgraded.
5. Dates in ISO 8601; numbers as printed, with the printed unit symbol; an exact SI conversion may be added in a separate field, never in place of the printed value.
6. No evaluative adjective; no inference beyond the span quoted.
7. The statement contains no reference to any project artifact, only to the world described by the source.

## Provenance of every claim

Every claim records the source identifier and a locator. The locator is, in order of preference: page number; section number or heading text verbatim; line or field name for repository files; timestamp for audio or video; the URL fragment for a web page without pagination. When no locator finer than the document exists, the locator is DOCUMENT and the excerpt must be long enough to be found by text search. The excerpt is the minimal verbatim span that supports the statement, in quotation marks, with omissions marked [...].

## Quantitative data

Every quantitative claim or fact carries three fields, none of which may be empty: value (as printed), unit (as printed; DIMENSIONLESS if the source states a pure number), conditions (the circumstances the source attaches to the value: process corner, tile size, voltage, temperature, clock, configuration, or whatever the source states; NOT STATED if the source attaches none). A value whose conditions are NOT STATED is not comparable; it enters a computation only under a DECISION of subtype ASSUMPTION that records the conditions assumed, and the computation names that DECISION.

Derived numbers (a product, a conversion, a difference between two sourced values) are OBSERVATIONs that cite the FACTs or claims they are computed from and show the computation; they are never written into a fact statement or into a source column of any table.

## Absence of information

When a source does not state something the project needs, the record says NOT STATED with the source identifier searched and the locator range examined. Absence is never converted into a default, a typical value, a value from a different technology or product, an analogy with another protocol, or an inference from context. If a value is required to proceed, it is introduced only as a DECISION of subtype ASSUMPTION, never as a FACT, and every dependent artifact carries the DEC identifier.

## Independence of sources

Two sources are independent for a given statement only if all four tests pass, and the test results are recorded on the fact:

1. Lineage: neither source lists the other, directly or through a chain, in derived_from for that statement.
2. Publisher: the sources are not the same organization reproducing the same underlying document, and one is not a mirror, translation or excerpt of the other.
3. Text: the statements are not verbatim or near-verbatim (same numbers in the same sentence structure), as judged independently by two persons; a disagreement is recorded as NOT INDEPENDENT.
4. Access: each source has its own access to the underlying reality (for example, the foundry for a process figure, the organizer for a rule, an experiment for a measurement).

The corroboration count of a fact is the number of pairwise independent sources under these tests. "Several sources" that fail any test count as one: a vendor manual and a blog post that quotes it are one source; two datasheets of the same vendor are one source for a shared statement. The count is a field; no threshold on it confers a status, except that CONFIRMED_FACT requires at least one Tier 1 claim.

## Contradictions

When two claims with the same subject and predicate give different values or statements under the same conditions:

1. A contradiction record is created with the claim identifiers, the dimension of disagreement, candidate causes (version, unit, scope, conditions, error) each marked as a conjecture, and a resolution path naming the party that can settle it.
2. Both claims stay in the fact register, attached to a fact in the CONTESTED state; neither is deleted, hidden or preferred.
3. Resolution occurs only through a new claim from a Tier 1 source or a logged written communication from the responsible party. Majority, recency, tier, convenience or plausibility do not resolve a contradiction. The resolution is dated and the original claims remain visible with the resolving claim identifier.
4. Until resolution, any use of the contested value names the contradiction identifier, and any computation that depends on it runs once per candidate value and reports the spread as an OBSERVATION.

If the conditions differ, there is no contradiction; the claims become two facts with distinct conditions. The absence of a statement in one source is not a contradiction of a statement in another; it is recorded as NOT STATED or as an OPEN_QUESTION.

## Deduplication

When a new claim is consolidated:

1. Normalize the statement (subject, predicate, value in the printed unit and in SI when exact, conditions).
2. Search the fact register for the same subject and predicate.
3. Same subject, predicate, value and conditions: append the claim identifier to the existing fact; update the corroboration count with the independence tests; do not create a new fact.
4. Same subject and predicate, different conditions: create a new fact; cross-link the two.
5. Same subject, predicate and conditions, different value or statement: create a contradiction record per [Contradictions](#contradictions).
6. Claims from two versions of the same source are never merged without the version comparison of [RESEARCH_METHOD.md](RESEARCH_METHOD.md#handling-of-revisions-and-versions).

One canonical fact, several claim pointers: the fact register never contains two facts with identical normalized statements and conditions. Claim pointers are linked to the fact, never merged into one another, so that a later version change in one source stays traceable.

## Promotion and retirement

Fact lifecycle states: PROPOSED, CANONICAL, CONTESTED, REVERIFY, RETIRED.

- PROPOSED to CANONICAL requires: the atomic fact rule satisfied; at least one claim with locator and excerpt; status label assigned; for QUANT, value, unit and conditions present; deduplication performed; independence tests recorded for every source pair; a second person, not the extractor, re-read the source location and checked each of these items, and the check is recorded with date. A promotion without a second reader is invalid.
- CANONICAL to CONTESTED: a contradiction record is created that references the fact.
- CONTESTED to CANONICAL: the contradiction is resolved per [Contradictions](#contradictions); the resolving claim is attached.
- CANONICAL to REVERIFY: a supporting claim is marked CHANGED or REMOVED after a source revision, a MOVING_CONSTRAINT re-verification is overdue, or the retained copy is lost.
- REVERIFY to CANONICAL: re-verification against the current source version, recorded with date and locator.
- Any state to RETIRED: every supporting claim is REMOVED in the current source versions, or the fact is superseded by a fact with a later source version; the retiring record names the successor. A retired fact is never deleted.

Status labels are not lifecycle states: a label changes only when the source text or its version changes, and the change is recorded on the fact with the claim that caused it. Hypothesis states are in [Definitions](#hypothesis). OPEN_QUESTION entries are closed only when a claim from an included source provides the statement, which then enters the fact register as a new fact; the OQ record stays and points to it.

## Retention of primary documents

Every included source has a retained copy with a content hash in the source record. Whether the copy may be stored in the public repository follows the redistribution field of the source record; when NOT STATED, the copy is kept outside the public repository and the record says where.

## Consolidation checklist

A reviewer accepting an artifact into the knowledge base checks every entry against this file: one statement per entry; claim identifier with locator; value, unit and conditions where quantitative; correct category; corroboration counted by independence tests, not by pointer count; contradictions kept with their identifiers named wherever the value is used; no value born from absence; no derived number outside an OBSERVATION; no HYPOTHESIS outside its permitted locations; every DECISION referenced by identifier and present in the decision log. An entry that fails any item is not accepted.
