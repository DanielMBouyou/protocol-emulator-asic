# Gate G00, condition 1, third evaluation

Third evaluation of condition 1 of the gate of [S00](../PREBENCH_PLAN.md#s00-methodological-setup), and of nothing else. It supersedes the result of [gate-g00-condition-1.md](gate-g00-condition-1.md), which supersedes the condition 1 section of [gate-g00.md](gate-g00.md). Neither earlier record is edited; each remains the record of what was evaluated on its own date, and each describes the repository as it then stood.

- **evaluated on**: 2026-09-18
- **artifact version checked**: the working tree of this repository as committed in the commit that carries this record.
- **occasioned by**: the minimal fix below, applied to the sole violation the second evaluation confirmed.

**Result: NOT MET.** Condition 3 was not touched, [LIM-0002](limitation-register.md#lim-0002-the-reading_confidence-field-does-not-use-its-own-vocabulary) was not modified, and no S01 artifact was touched.

## The fix that was applied

The second evaluation confirmed one violation: item 16 of the [atomic fact rule](../EVIDENCE_POLICY.md#atomic-fact-rule) requires every span quoted anywhere in the extraction to be recorded as a fact, and SRC-0004's `version` field quoted `4 min read`, which no claim recorded.

One clause was removed from that field and nothing else changed:

```diff
-- **version**: Published Sep 10, 2026; retrieved 2026-09-17; page states "4 min read"
+- **version**: Published Sep 10, 2026; retrieved 2026-09-17
```

No claim was created to preserve the reading time. The figure is page furniture, and it is not lost: the retained copy of the page still prints it, so anyone who needs it can read it at the source, which is where the [root of evidence](../EVIDENCE_POLICY.md#root-of-evidence) rule says the root sits. After the edit, SRC-0004 carries no double-quoted span in any field.

An independent operator confirmed against git that this is the only change to any tracked file since the preceding commit.

## What the per-rule re-run found, and why it does not stand

The condition was re-run at the established standard: a fresh enumeration of EVIDENCE_POLICY.md, every binding rule checked against the dry-run pair, three skeptics per claimed violation. It produced 115 rules, 46 binding, 48 checks, **41 satisfied, 7 not applicable, zero violations claimed**. Half one, the register-wide field existence test, was satisfied by parse over all 13 source records and all 202 claim records.

That pass was then attacked. Five operators were set on the verdict rather than on individual rules, four hunting for a missed violation across different parts of the policy and one attacking the scope reading the check had been given. **Four of the five found a violation.** Two of their findings survive an independent check of the underlying files.

A per-rule sweep and an attack on the verdict are not the same instrument. The sweep asks of each rule whether the records satisfy it and is satisfied by a plausible answer; the attack asks what would have to be true for the pass to be wrong. This condition has now been passed by the first and failed by the second, which is a fact about the method and not only about these two records.

## The violations

### Item 19, the excerpt is not from a verbatim retrieval

> Excerpts are taken from a verbatim retrieval of the source. An excerpt that could only be obtained through a rendering that may have altered the text is marked unverified in reading_confidence and may not support a CONFIRMED_FACT.

CLM-0048's `excerpt` reads `"Design an open-source, general-purpose protocol emulator ASIC."` That string occurs **zero times** in the retained copy of SRC-0004, whose hash and byte count were recomputed and matched. What the retained bytes print is:

```html
<p>Design an <strong>open-source, general-purpose protocol emulator ASIC</strong>.</p>
```

The excerpt is obtainable only by removing the markup, which is the rendering SRC-0004's own `retrieval note` describes as "Body text extracted by tag-stripping". Both limbs of the rule are breached. The `reading_confidence` does not mark the excerpt unverified; it reads `high; printed imperative retrieved verbatim from the raw HTML`, and the span was not retrieved verbatim. And the claim supports FCT-0042, whose status label is CONFIRMED_FACT, which the rule forbids for such an excerpt.

The project's own evidence already showed this. [OBS-0004](observation-register.md#obs-0004-re-check-of-every-s00-claim-against-its-retained-copy), written the day before, gives this exact case its own weaker class, FOUND ACROSS MARKUP, and counts seven of them on SRC-0004 alone. The per-rule sweep checked item 19 without testing the excerpt against the retained bytes, and so did not reach what the register next door had already recorded.

### Item 11, a date not in ISO 8601, in the field the fix touched

> Dates in ISO 8601.

SRC-0004's `version` now reads `Published Sep 10, 2026; retrieved 2026-09-17`. It carries two dates in two formats, one of them not ISO. Two skeptics reached this independently. The field is the one the fix edited, and the fix removed the clause it was asked to remove without examining what stayed behind.

The reading that would excuse it, that the RESEARCH_METHOD.md source record table asks for a publication date "as printed", is the reading this condition already rejects: the condition names EVIDENCE_POLICY.md, and item 11's date clause is unconditional where its number clause is not. The project applies item 11 exactly this way elsewhere: CLM-0004 records the same printed string and sets its value to 2026-09-10.

## A challenge finding that did not survive

One operator argued on three independent routes that SRC-0004's `redistribution` value is a value born from absence, because no claim records any licence for the page and the project's own CLM-0007 records that the page does not contain the token "license".

Checked against the retained copy, it does not hold. The page prints, in its footer, `© Copyright 2015-2026 Jane Street Group, LLC. All rights reserved.` The field's characterization of the page as copyrighted rests on printed text, not on absence. It is recorded here because a finding that was investigated and rejected is worth as much to a later reader as one that stood.

## Findings left open, and out of scope

Several operators raised item 16 against CLM-0048's `locator`, which quotes the span `open-source, general-purpose protocol emulator ASIC`, a piece of body text that no fact statement records. Most rated it arguable, on the ground that the span is the `value` field of the very claim whose locator quotes it and is the object of FCT-0042. It is not relied on here, since two verified violations already settle the verdict, and it is recorded so it is not lost.

Defects were also reported that this condition does not test, because they rest on RESEARCH_METHOD.md rather than on EVIDENCE_POLICY.md: the `kind` value of SRC-0004 falls outside the field's enumerated vocabulary, `found_by` names no query identifier, CLM-0048's `source_version` is a pointer rather than a copy, and the source register carries a `source_key` field that no canonical file and no decision defines. They are real and they are untidiness in the records, not condition 1 failures.

## Consequence

Condition 1 is NOT MET, for the third time, now on two verified grounds. S00 stays open under the [slip rule](../PREBENCH_PLAN.md#slip-rule), which is what assigns the remaining work to S00. Nothing was changed in a gate or a rule to obtain a pass, and nothing will be.

The two violations both touch the dry-run entry only, and both have a remedy inside S00. Item 19 asks that the `reading_confidence` of a claim whose excerpt crosses markup say so, and that a fact resting on such a claim not carry CONFIRMED_FACT. Item 11 asks that a date be written in ISO 8601. Neither remedy is applied here: this task's mandate was the fix the previous audit identified, and a new violation is recorded rather than chased, so that the record shows what each evaluation found rather than a single tidied outcome.
