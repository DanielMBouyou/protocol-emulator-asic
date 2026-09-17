# Contact plan

Output of [S00](../PREBENCH_PLAN.md#s00-methodological-setup). For each open question of [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#open-questions), a drafted question text and an assigned channel. Nothing here has been sent: sending is [S01](../PREBENCH_PLAN.md#s01-challenge-and-pdk-constraints) work, and each sending becomes a question log entry in [question-log.md](question-log.md) and a query log entry with venue PERSONAL-COMM.

Every draft was written to presuppose no answer and no architecture, and was then checked by a second operator against those rules. A draft the reviewer rewrote carries its findings under the text, so that the reason for the wording stays visible to whoever sends it.

Channels are defined once here and referenced by name.

| Channel | What it is |
| --- | --- |
| ORGANIZER-EMAIL | asic-competition@janestreet.com, the address the organizer states on the announcement page. For what the organizer decides and publishes: rules, eligibility, judging, deliverables, deadline, submission channel and area budget policy. |
| ORGANIZER-PAGE-MONITOR | re-reading the announcement page on a schedule. The organizer states a submission form will be added to it, so the page answers by changing. Never the only channel for a question that blocks an artifact. |
| TT-GITHUB-ISSUE | an issue on the relevant TinyTapeout repository. For the shuttle flow, tile geometry, pinout, precheck and version pinning. |
| IHP-GITHUB-ISSUE | an issue on IHP-GmbH/IHP-Open-PDK. For PDK contents, cell sets, corners, memory macros and the dev-to-main promotion. |
| REPO-OBSERVATION | not a question to anyone. The answer is read from the flow or PDK files at S01 and recorded as an OBSERVATION with a retrieval date and a repository state identifier. A file shows what the flow does today, not what the competition shuttle will pin. |

## OQ-01 Template obligation

- **open question**: [OQ-01](../PROJECT_SCOPE.md#oq-01-template-obligation)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and named the Tiny Tapeout CMOS5L Verilog template as a starting point on its own announcement page without stating it is mandatory, so it is the party that decides and publishes whether that template is required.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The protocol emulator ASIC competition page names a starting point: the Tiny Tapeout CMOS5L Verilog template at github.com/TinyTapeout/ttihp-verilog-template, branch cmos5l, and states "Set the tile size in info.yaml to 6x4".

1. What status does that template have for a competition submission?
2. What status does the build flow included in that template repository have for a competition submission?
3. Where either is required, what has to match: the repository, the branch, the contents of info.yaml, or something else?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "says to start with the CMOS5L Verilog template at github.com/TinyTapeout/ttihp-verilog-template" - paraphrase presented as the page's own instruction. The register (PROJECT_SCOPE.md F7) records it as a "Stated starting point", not as an instruction to start. "Says to start with" already tilts the answer toward the requirement reading the question exists to establish, breaking the no-presupposed-answer rule and the rule that the organizer's words be quoted and attributed rather than characterized.
- Same sentence drops the branch: F7 records the starting point as github.com/TinyTapeout/ttihp-verilog-template, branch cmos5l. Question 3 asks whether "the branch" has to match while the preamble never names one, so the addressee cannot answer part 3 from the message alone - breaks self-containedness and short-answerability.
- "without saying whether that is a requirement" - asserts an absence in the organizer's own page back at the organizer, and points at our conclusion before asking. "That" is also ambiguous across three referents (the template, its flow, the tile-size line), so a short reply may answer about the wrong one.
- "Is use of that template a requirement for a competition submission, or a recommendation?" - forced binary. It presupposes the answer space is one of two options we imagined, and invites confirmation of our framing rather than asking what the case is. Real answers such as "required for the harness only" or "required unless you ask us" have nowhere to land.
- "or may a submission be produced by other means?" - same forced binary, and "other means" is too vague to be answered precisely in a short written reply; it asks for an open-ended ruling instead of a fact.
- "the hardening flow that the template runs" - states as shared fact, to the organizer, a mechanism the project derived by reading the template repository (recorded internally as T2: LibreLane via tt-gds-action@ihp-cmos5l). It is our characterization, not the organizer's words, and asserting it as common ground presupposes a mechanism the addressee never stated.
- Borderline, kept but worth naming: the quoted "Set the tile size in info.yaml to 6x4" carries a figure that sits at the centre of the recorded contradiction CTR-01 (template info.yaml lists valid tiles 1x1, 1x2, 2x2, 3x2, 4x2, 6x2, 8x2; organizer says 6x4). It is admissible here only because it is quoted and attributed to the page and nothing is asked about its validity - that belongs to OQ-29. The rewrite keeps it strictly as attributed page wording supporting part 3.
- Minor, outside the question text: the channel_rationale repeats the same closed framing ("a competition requirement or a suggestion"). The channel assignment itself stands - only the organizer can settle a competition rule, and Tiny Tapeout owns the template but not the rules - so the channels are unchanged.

</details>

## OQ-02 Acceptable licenses

- **open question**: [OQ-02](../PROJECT_SCOPE.md#oq-02-acceptable-licenses)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: Jane Street wrote and publishes the competition's rules, so it is the party that decides what its own wording requires.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The protocol emulator ASIC competition page states that a submission "should be open source so others can use and build on it", and names no license.

1. Which licenses satisfy that statement?
2. Must the same terms cover every part of a submission, or may different parts carry different licenses?
3. To which entries does that statement apply, and from what point?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Is one specific license required, or is any OSI-approved license acceptable?" — presupposes a mechanism the organizer never stated (that OSI approval is the governing criterion) and asks the addressee to confirm a guess inside a closed either/or. Breaks the no-assumed-mechanism rule and the no-confirming-a-guess rule.
- "Which licenses satisfy that statement?" (item 1) followed by item 2 — item 2 is a narrowed restatement of item 1, not an independent part, so the numbered list does not decompose into separately answerable questions as required; item 1 already covers it openly.
- "Does this apply to all entries at the deadline, or only to entries selected for fabrication?" — a non-exhaustive binary that presupposes the requirement attaches at one of two moments the project imagined. Breaks the rule against smuggling in an assumed value/intent; ask openly to which entries and from what point it applies.
- "Does this apply..." — the bare "this" is a back-reference that weakens self-containedness of the numbered item; name the statement being asked about.

</details>

## OQ-03 Complete submission contents

- **open question**: [OQ-03](../PROJECT_SCOPE.md#oq-03-complete-submission-contents)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and states it will add the final submission form to its page, so it is the party that defines what a submission must include.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Regarding the protocol emulator ASIC competition, I have three questions about what a submission must contain to count as complete.

1. What items must a complete submission include, and which items, if any, are optional?
2. What format, file layout or naming requirements apply to those items, if any?
3. How are the submitted items used in judging?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "beyond the hardware source files" — presupposes a mechanism: that a submission is built around hardware source files and everything else is an addition to them. The fact register records no organizer statement of any deliverable set (F10 says only that the submission "should be open source"; F12 says a submission form will be added later). This smuggles in an assumed deliverable form and makes part 1's answer conditional on our framing.
- "for example documentation, test material, or software" — supplies candidate answers and converts the part into a yes/no confirmation of our own guess. The rules forbid asking the addressee to confirm a guess, and the organizer's answer to part 1 should not be steered by categories we invented.
- "Does a complete submission have to include material beyond the hardware source files" — redundant with part 1, which already asks for the complete list of required and optional items. It re-asks the same thing in closed form, i.e. whether a thing we imagined is the case rather than what is the case.
- "Is any required format, file layout or naming prescribed for these items?" — closed yes/no phrasing that asks whether an imagined requirement exists. Asking openly (what requirements apply, if any) is answerable in the same one line and presupposes nothing.
- "Are any of these items judged separately from the rest?" — presupposes a judging structure in which individual deliverables are separable scoring units. F13 records that no rubric, weights or jury are published, so this asks the organizer to confirm a structure we assumed; the neutral form is to ask how the items are used in judging.

</details>

## OQ-04 Submission channel

- **open question**: [OQ-04](../PROJECT_SCOPE.md#oq-04-submission-channel)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and states it will add the final submission form to its own page, so it is the party that publishes what the competition requires for submission.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The protocol emulator ASIC competition page states that a final submission form will be added to the page "closer to the deadline".

1. Through what route is an entry submitted?
2. If entering involves more than one step, what is each step for?
3. If entering involves more than one step, in what order must the steps be completed?
4. Does entering require registering an account anywhere? If so, where?
5. When do you expect the submission form to be published on the page?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "that form, app.tinytapeout.com, both, or something else?" — presents a closed menu of our own candidate routes and asks the organizer to pick one. Breaks "never asks the addressee to confirm a guess" and "presupposes no mechanism": it smuggles in an assumed submission mechanism rather than asking what is the case.
- "app.tinytapeout.com" — a named submission mechanism stated to the addressee as a live option, but not verified by the project. It appears in the repository only inside the text of our own open question (PROJECT_SCOPE.md line 151, OQ-04); no fact row (F1-F16, T1-T4) evidences that this route exists or is used for entry. An unverified figure must not be put in front of the organizer as a fact.
- "If more than one is involved, what does each one do, and in which order?" — two independent things fused into one numbered item (purpose of each step; sequence of steps), so the reply cannot answer them separately. Breaks the splitting rule.
- "If more than one is involved" — the conditional is scoped to the menu in question 1; if the actual route is none of the listed options, the item is unanswerable as written.
- "Is a Tiny Tapeout account or a shuttle sign-up needed in order to enter the competition?" — two independent things fused into one sentence (an account; a shuttle sign-up), and both presuppose specific mechanisms the project has not evidenced. Breaks both the splitting rule and the no-presupposed-mechanism rule.
- "The protocol emulator ASIC competition page states that a final submission form will be added to the page closer to the deadline." — the organizer's own wording "closer to the deadline" (recorded quoted in F12) is paraphrased without quotation marks while being attributed to the page. Where the organizer's words are used they must be quoted as well as attributed.
- channel_rationale: "whether that form, the Tiny Tapeout application, or both are required" — the rationale encodes the same two-option guess that spoils the question text. It should state only that the organizer owns the submission route and has said it will publish the form, so only the organizer can state what the route is.
- Not a rule break, recorded for completeness: blocks_artifact is true and ORGANIZER-PAGE-MONITOR is the fallback, not the sole channel, so the page-monitor restriction is respected. Channel assignment (ORGANIZER-EMAIL primary) is correct and is left unchanged.

</details>

## OQ-05 Deadline time zone and hardness

- **open question**: [OQ-05](../PROJECT_SCOPE.md#oq-05-deadline-time-zone-and-hardness)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and publishes updates on its competition page and by email to sign-ups, so it is the party that sets and states the deadline.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The protocol emulator ASIC competition page states: "Submit your design by January 18th, 2027."

1. Which time zone applies to that date, and at what time of day does the deadline fall?
2. What is the policy for submissions received after that time?
3. After the deadline, may submitted material still be changed?
4. If it may, which version is judged?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "After the deadline, may a submitted repository still be changed, for example further commits, documentation edits or fixes?" - presupposed mechanism. It assumes the submission IS a git repository that receives commits. PROJECT_SCOPE.md OQ-04 records the submission channel as an open question (blog form, app.tinytapeout.com, or both) and OQ-03 records the complete submission contents as open, so the draft hands the organizer a submission mechanism the project has not established. Breaks: 'must not smuggle in an assumed value, an assumed mechanism, or an assumed intent.'
- "which state of the repository is judged" - same presupposed mechanism carried into part 4; the judged object is named as a repository before the organizer has said what is submitted or how.
- "Is it a hard cutoff, or are late entries accepted under any conditions?" - a drafted binary presented as exhaustive, inviting the addressee to pick between two options the drafter imagined (it excludes, for example, a grace period, a staged or per-item deadline, or case-by-case handling). Breaks: 'Ask what is the case, not whether a thing you imagined is the case' and 'never asks the addressee to confirm a guess.'
- Not a violation, recorded for completeness: the quoted deadline "Submit your design by January 18th, 2027." is verified as F12 in PROJECT_SCOPE.md with the announcement page as source, and is attributed in the message; the channel assignment and its rationale are correct, and ORGANIZER-PAGE-MONITOR is used as a fallback rather than the only channel for a blocking question.

</details>

## OQ-06 Eligibility and team limits

- **open question**: [OQ-06](../PROJECT_SCOPE.md#oq-06-eligibility-and-team-limits)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: Jane Street set the competition and its rules and states asic-competition@janestreet.com as the contact address, so it is the party that decides and publishes eligibility and team rules.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Regarding the protocol emulator ASIC competition:

1. Who is eligible to enter? Please state any restrictions relating to age, country or residence, employment, student status, or affiliation with Jane Street.
2. Is there a limit on the number of people in a team?
3. May one person take part in more than one team?
4. May one team submit more than one entry?
5. Must a team register or announce itself before submitting, and if so how?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "May one person take part in more than one team, and may one team submit more than one entry?" - two independent questions fused into one numbered item. Whether a person may join several teams and whether a team may enter several designs are separately answerable and may have different answers; the split rule requires each to carry its own number.

</details>

## OQ-07 Precheck and gate level tests

- **open question**: [OQ-07](../PROJECT_SCOPE.md#oq-07-precheck-and-gate-level-tests)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **why this channel**: Whether a check makes an entry eligible is a competition rule, and Jane Street set the competition and its rules and publishes them on the competition page.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Four questions about the protocol emulator ASIC competition announced on the Jane Street blog on 2026-09-10. We are asking about requirements rather than recommendations.

1. Which checks, if any, must a submission pass for it to be eligible?
2. When in the process is each of those checks applied?
3. Must a submission itself include any record or result of those checks?
4. What happens to a submission that does not pass one of them?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "must the Tiny Tapeout precheck pass?" - presupposed mechanism and presupposed answer. It asks the organizer to confirm a step we supplied rather than asking what is the case, and it assumes the Tiny Tapeout flow governs eligibility at all, which the repository still records as unsettled (OQ-01: whether the template and its flow are mandatory is not stated).
- "which precheck" - presupposes that a named precheck, and a choice among several, exists for this process. The project's own Tiny Tapeout fact (T2) records only that the template's GitHub Actions flow hardens with LibreLane through tt-gds-action with pdk ihp-sg13cmos5l; no precheck is evidenced for the CMOS5L flow, so the phrase states an unverified technical mechanism as fact.
- "Must gate-level tests be run, must they pass, and must their results be part of the submission?" - three independent questions fused into one sentence; each must be separately answerable, so they belong in separate numbered items.
- "gate-level tests" - assumed verification mechanism, presented in our own words as an established requirement. The organizer's printed words on verification (F15: any HDL and verification techniques are welcome, "including formal methods, random constrained tests, AI-assisted verification") are neither quoted nor attributed, and they do not name gate-level tests.
- "Are there other automated checks" - "other" is meaningful only relative to the checks invented in items 1 and 2, so it inherits their presupposition; "automated" presupposes the mechanism is automation and invites the addressee to omit any manual or human eligibility review.
- "is it rejected, judged as is, or given a chance to fix it?" - a closed menu of three outcomes we imagined; this asks the addressee to pick among our guesses instead of stating what actually happens.
- fallback_channel "TT-GITHUB-ISSUE" - channel assigned to a party that cannot settle the question. The entry's own rationale concedes that "Tiny Tapeout can only say what its own shuttle flow requires", so a TinyTapeout issue cannot answer a competition eligibility rule; a fallback must be able to settle the same question. Replaced with ORGANIZER-PAGE-MONITOR, which is permitted here because the organizer has said submission details will be published on that page (F12) and ORGANIZER-EMAIL remains the primary channel for this artifact-blocking question.

</details>

## OQ-08 Reuse of cores prior art and generated RTL

- **open question**: [OQ-08](../PROJECT_SCOPE.md#oq-08-reuse-of-cores-prior-art-and-generated-rtl)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules, so it is the party that decides and publishes what may be reused, disclosed or submitted.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Regarding the protocol emulator ASIC competition:

1. May an entry include or build on existing open-source hardware designs written by other people? If so, under what conditions?
2. May an entry include work its own authors produced before the competition was announced?
3. Must existing designs or prior art that an entry draws on be disclosed, and if so, in what form and where?
4. The announcement page welcomes any HDL and verification techniques, "including formal methods, random constrained tests, AI-assisted verification". Does the competition place any conditions on an entry's hardware description code when it is produced with AI tools, and if so, which?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "What are the rules on hardware description code produced with AI tools?" - presupposes an answer. It assumes such rules exist, so a truthful "there are none" does not fit the question as asked. The rule is to ask what is the case, not whether a thing we imagined is the case; the neutral form must allow a null answer ("any conditions ... and if so, which").
- "The announcement page lists AI-assisted verification among the welcome techniques." - paraphrase of the organizer presented as the page's content. The register's verified wording (PROJECT_SCOPE.md F15, CONFIRMED_FACT) is the quoted fragment "including formal methods, random constrained tests, AI-assisted verification"; EVIDENCE_POLICY.md line 80 forbids inference beyond the quoted span, and the hard rules require the organizer's own words to be quoted and attributed rather than restated. The paraphrase also widens the organizer's scope from techniques he listed to a general category of "welcome techniques".
- fallback_channel "ORGANIZER-PAGE-MONITOR" - channel assigned outside its stated use. That channel is for questions the organizer has said it will publish rather than answer individually; per F12 the only thing the organizer has said will be added to that page is the final submission form. Nothing evidences that reuse, disclosure or AI-code rules will be published there, so the page cannot be expected to settle OQ-08 by changing. A fallback is optional (at most one), so it is dropped; primary ORGANIZER-EMAIL is correct and its rationale is adequate.
- No violation found on these axes, for the record: items 1-3 presuppose no answer; no instruction set, CPU, datapath, memory organization or any candidate design is mentioned or implied (the draft correctly avoids OQ-08's own internal words "cores" and "RTL"); the four parts are independent and already numbered in one message; no technical figure is stated at all, so nothing unverified is asserted; the text is self-contained, plain, flattery-free and about 95 words.

</details>

## OQ-09 Functional acceptance per protocol

- **open question**: [OQ-09](../PROJECT_SCOPE.md#oq-09-functional-acceptance-per-protocol)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: Jane Street set the competition and its rules and states asic-competition@janestreet.com as the contact address, so it is the party that decides what the competition accepts as support for a protocol, which is a contest rule rather than a property of the Tiny Tapeout flow or the IHP PDK.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

I am preparing an entry for the protocol emulator ASIC competition and have questions about the starting protocols and stretch goals named in the announcement (UART, SPI and I2C; low-speed USB and 10 Mbit Ethernet).

1. What, if anything, must a submission show for the competition to count one of these protocols as supported?
2. Are any specific bit rates or clock rates required, and if so which?
3. Are any specific roles required, such as controller or peripheral, host or device, and if so which?
4. Is any particular level of evidence required, for example simulation, FPGA or measured hardware, and if so which?
5. Do the answers differ between the starting protocols and the stretch goals?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "the protocols named in the announcement (UART, SPI and I2C as starting protocols, low-speed USB and 10 Mbit Ethernet as stretch goals)" - presents these five as the complete set of protocols the announcement names. The project's own fact register (F5, CONFIRMED_FACT) records that the same announcement also names JTAG, SWD, PS/2 and CAN bus as "other interesting protocols to consider". Stating a set as exhaustive when the repository records otherwise is an unverified claim of fact and invites an answer scoped to the wrong set.
- "what does the competition accept as evidence that a submission supports it?" - presupposes that a defined acceptance criterion for protocol support exists. A truthful answer may be that none exists and that support is judged, not tested. Breaks the rule that the question presupposes no answer.
- "Which bit rates or clock rates, if any, have to be demonstrated?" - "have to be demonstrated" presupposes that demonstration is the required mechanism, which is precisely what item 1 is still asking. Smuggles in an assumed mechanism.
- "Which roles have to be demonstrated, for example controller or peripheral, host or device?" - no "if any" qualifier, so it presupposes that specific roles are required, and it hands the addressee candidate values to tick. Breaks both the no-presupposed-answer rule and the rule against asking the addressee to confirm a guess.
- "At which level must the demonstration be made: RTL simulation, gate-level simulation, FPGA, measured silicon, or something else?" - "must" presupposes a mandated level exists, and the closed menu asks the addressee to pick from our list rather than state what is the case. Also "measured silicon" presupposes entrants have fabricated parts, which the announcement does not establish (fabrication is stated only as a prize for winners, F13/F14).
- "For each named protocol" in item 1, together with item 5 "Do the answers differ between the starting protocols and the stretch goals?" - item 1 demands a five-protocol by four-dimension matrix and item 5 then asks whether the answers differ at all, which is redundant with it. Together they push the message past "answerable in writing by the addressee in a short reply".

</details>

## OQ-10 Reprogramming mechanism and pin accounting

- **open question**: [OQ-10](../PROJECT_SCOPE.md#oq-10-reprogramming-mechanism-and-pin-accounting)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: TT-GITHUB-ISSUE
- **why this channel**: Jane Street set the competition and its rules and states asic-competition@janestreet.com as its contact address, so the organizer is the party that decides and publishes this requirement, while Tiny Tapeout's repositories cover what its own template and flow fix.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

A question about this sentence in the competition announcement: "Your chip should be reprogrammable enough to support new protocols after fabrication, within its timing and I/O constraints."

1. What must a submission do for you to consider that requirement met?
2. Does the competition require or exclude any particular way of meeting it, or is the choice left to entrants?
3. The Tiny Tapeout CMOS5L template's info.yaml lists a fixed pin set (8 inputs, 8 outputs, 8 bidirectional, plus clk and rst_n) and says "DO NOT delete or add any pins". Does the competition require entries to use that pin set as published, or do different pin rules apply to competition entries?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "by what means do you expect a submitted chip to come to support a protocol it did not support before" - presupposes an answer: it takes for granted that the organizer has a particular means in mind, and item 2 ("Is any particular means required") then asks whether such a means exists at all. The two items contradict each other, and item 1 invites the organizer to speculate about our design rather than state what the rule is.
- "and over which interface?" - presupposes a mechanism: that reprogramming happens over some interface on the chip. It is also a second, independent question fused into item 1, so the addressee cannot answer the two parts separately.
- "Is any particular means required, or is that left entirely to entrants?" - a closed either/or that is not exhaustive (a means could be neither required nor wholly free, e.g. weighed in judging or partly excluded). It pushes the addressee to confirm one of two framings we supplied.
- "The Tiny Tapeout template fixes 8 inputs, 8 outputs, 8 bidirectional pins, plus clk and rst_n." - stated to the organizer as a flat governing constraint and unattributed. The project register holds this only as what the cmos5l template's info.yaml says (T1, with its own wording "DO NOT delete or add any pins"), and whether that template is binding for competition entries is itself an open question (OQ-01). As written it presupposes the answer that the template pinout governs submissions.
- "must those come out of that fixed set, or are further pins available on the competition shuttle?" - two independent questions in one sentence (a competition rule, and the pin availability of the shuttle), and the second half is Tiny Tapeout's to answer: pinout, tile geometry and shuttle flow are the TT-GITHUB-ISSUE domain. The entry's own rationale concedes this yet still asks it of the organizer.
- "If a submission uses pins for the means in question 1" - inherits the presupposed mechanism of item 1; with item 1 rewritten there is no "means in question 1" to refer back to, and the pin question must stand on its own so the addressee can answer it without our chain of reasoning.
- fallback_channel "TT-GITHUB-ISSUE" - a fallback must be able to settle the same question. Tiny Tapeout cannot say what the organizer's reprogrammability sentence requires of an entry. For an organizer rule question that blocks an artifact, the permitted fallback is ORGANIZER-PAGE-MONITOR (the organizer publishes rules on that page), which is allowed here because it is not the only channel.
- Reviewer note, not a rule breach in the rewritten text: the dropped half - whether the shuttle exposes pins beyond the template set - should be carried as its own entry on TT-GITHUB-ISSUE, primary, since Tiny Tapeout owns and answers it in public.

</details>

## OQ-11 Stretch protocols pads or external PHY

- **open question**: [OQ-11](../PROJECT_SCOPE.md#oq-11-stretch-protocols-pads-or-external-phy)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: TT-GITHUB-ISSUE
- **why this channel**: Jane Street set the competition and its rules and publishes changes to them on its competition page and by email to sign-ups, so it is the party that decides and announces this requirement.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The competition page names UART, SPI and I2C as starting protocols and gives "low-speed USB" and "10 Mbit Ethernet" as stretch goals. Five questions on these:

1. For "low-speed USB" and "10 Mbit Ethernet", what do you expect a submitted chip to produce and receive at its own pins?
2. What, if anything, do you expect to be present outside the chip for these two?
3. If something is expected outside the chip, who is expected to provide it?
4. If a submission is evaluated or demonstrated on hardware, what do you expect to be present alongside the chip?
5. What are your answers to questions 1 to 3 for UART, SPI and I2C?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "do you expect the signalling to be produced and received directly at the chip's own pins, or through separate components outside the chip?" - forced binary. It presupposes a mechanism (that these are the only two arrangements) and presupposes the organizer already holds an expectation framed that way. Breaks 'presupposes no answer / no mechanism: ask what is the case, not whether a thing you imagined is the case.'
- "If through separate components, which ones do you assume, and who is expected to provide them?" - two independent questions (which components / who supplies them) fused into one numbered item, so they cannot be answered separately. Breaks the split-into-numbered-parts rule.
- "which ones do you assume" and "Which external components are assumed present" - 'do you assume' / 'are assumed' presupposes that an assumption exists on the organizer's side. Breaks 'presupposes no answer... no assumed intent.'
- "the board on which a submitted chip would be tested or demonstrated" - presupposes that submitted chips are tested or demonstrated on a board. The fact register evidences only F14, 'Winners receive their fabricated chip mounted on a dev board', and records board and package as open (T3, OQ-23). An unverified premise is stated as fact inside the question.
- "Does the same answer apply to the starting protocols UART, SPI and I2C?" - a yes/no that asks the addressee to carry an earlier answer across and confirm it, and it collapses parts 1 to 3 into a single binary. Breaks 'never asks the addressee to confirm a guess' and the split rule.
- "names low-speed USB and 10 Mbit Ethernet as stretch goals" - the terms are the organizer's own (F5) but are written in our voice without quotation marks. Breaks 'where the organizer's own words must be quoted, quote them and attribute them'; unquoted, '10 Mbit' reads as a figure we assert.

</details>

## OQ-12 Judging rubric winners and weighting

- **open question**: [OQ-12](../PROJECT_SCOPE.md#oq-12-judging-rubric-winners-and-weighting)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: Jane Street set the competition and its rules and states it will pay to tape out the most novel designs, so the judging criteria, any jury and the number of taped-out designs are the organizer's to decide and publish.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The competition announcement says Jane Street will pay to tape out "the most novel designs" and is "particularly interested in projects with unique functionality, as well as those that demonstrate novel approaches to design and verification methodologies."

1. How will submissions be assessed?
2. Is any weighting applied among the factors considered?
3. If so, will that weighting be published?
4. Who makes the selection?
5. How many designs will be paid for tape-out, or has that number not been fixed?
6. Will the basis for the decision be published, and if so when?
7. Will entrants be told anything about how their own submission was assessed?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Which criteria will be applied when submissions are assessed?" — presupposed answer. It assumes a defined set of criteria exists and will be applied. F13/OQ-12 (PROJECT_SCOPE.md:97,174) record that no rubric has been published. Must ask what is the case, not which items from an assumed rubric.
- "Is there a weighting among those criteria, and will it be published?" — two independent questions fused into one numbered item; existence of a weighting and its publication can be answered separately and must be separate parts.
- "Will the criteria be published before the January 18th, 2027 deadline, and will entrants receive written feedback or scores?" — two independent questions fused into one numbered item, and the publication half duplicates the second half of item 2.
- "written feedback or scores" — presupposed mechanism. It assumes submissions are scored. Ask whether entrants are told anything about the assessment of their own submission, without naming a form it takes.
- "How many submissions will be taped out?" — presupposed answer. It assumes a number has been fixed and is known. F13 records that no number of winners has been published; the question must allow "not yet fixed" as the answer.
- channel_rationale: "the jury" — presupposes a jury exists. F13 states explicitly that no jury has been published. The rationale should read "who assesses submissions" (the rationale is otherwise correct and the channel assignment stands; there is no schema field to return the corrected rationale).
- Verified, not a problem, recorded for the reviewer: the quoted organizer wording matches F13 verbatim and "January 18th, 2027" matches F12 verbatim, so no unverified technical figure is asserted. The date is nonetheless dropped in the rewrite because "if so, when" asks less and presupposes no publication schedule.

</details>

## OQ-13 Tile budget decision date

- **open question**: [OQ-13](../PROJECT_SCOPE.md#oq-13-tile-budget-decision-date)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: Jane Street set the competition's rules and published both the current 6x4 tile maximum and its statement that it is working on the possibility of 8x4, so it is the party that publishes any update to that limit.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

The competition announcement states: "The current maximum area is 6x4 tiles per design. We are working on the possibility of scaling up to 8x4 tiles (~30% more area)."

1. Has this been decided?
2. If not, is there a date by which you expect to decide?
3. How will the outcome be announced?
4. Which maximum area should entrants work to now?
5. If the larger area is adopted, what would apply to designs already built to the current maximum?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "By what date do you expect this to be settled?" - presupposes an answer: it assumes a decision date exists and asks only for its value. The draft never asks the prior question, whether the matter has been decided at all. Ask what is the case first.
- "an update to the announcement page, a message to the sign-up list, or another channel" - smuggles in an assumed mechanism by handing the addressee a menu of channels it has not said it uses for this decision. The repository evidences a sign-up form for general updates (F8/F12 in PROJECT_SCOPE.md), not that the area outcome would go out on it. The neutral form asks only how the outcome will be announced.
- "Until it is settled, which maximum area should entrants work to?" - presupposes that the matter is still unsettled as of the day the message is sent. The quoted wording is the state of the page when it was written, not a verified present-tense fact.
- "will entrants who designed to the smaller one be able to move to it, and by when?" - two independent asks fused into one sentence (whether, and by when), so the parts cannot be answered separately as required.
- "be able to move to it" - asks the addressee to confirm a guessed mechanism (a migration path for already-sized designs) rather than asking what would apply. The rewrite asks the open form.
- Channel assignment is sound and unchanged: only the organizer can settle its own area budget policy, and the page monitor is a fallback rather than the sole channel, so the blocking-artifact restriction on ORGANIZER-PAGE-MONITOR is not engaged. The quoted sentence is verbatim from fact F8 and is attributed in the text, so no unverified figure is asserted as fact.

</details>

## OQ-14 Usable core area

- **open question**: [OQ-14](../PROJECT_SCOPE.md#oq-14-usable-core-area)
- **primary channel**: TT-GITHUB-ISSUE
- **fallback channel**: REPO-OBSERVATION
- **why this channel**: Tiny Tapeout publishes tt-support-tools, whose tile_sizes.yaml defines tile dimensions, and the cmos5l Verilog template whose hardening flow the organizer names as the starting point, so it is the party that publishes and decides what a tile of a given size is.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about CMOS5L (ihp-sg13cmos5l) tile dimensions and usable area.

Three descriptions are in circulation. Quoting each with its source:

(a) ttihp-verilog-template, branch cmos5l, info.yaml: "A single tile is about 167x108 uM", valid tile sizes "1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2".
(b) Jane Street's protocol emulator ASIC competition announcement: approximately 200 um x 150 um per tile, and "about 0.7 mm2 of nominal tile area" for 6x4.
(c) tt-support-tools, branch ihp-sg13cmos5l, tech/ihp-sg13cmos5l/tile_sizes.yaml, as read on 2026-09-15: 1x1 as 202.08 x 154.98 um, and a 6x4 entry with bounding box 1289.28 x 710.64 um.

1. Which of these, if any, applies to the CMOS5L shuttle this competition targets? If none does, what are the current tile dimensions and the valid tile sizes?
2. For a tile size a project can select, how much of that area is available for the project's own logic, and what accounts for any difference from the figures above?
3. Where, if anywhere, is that recorded in the flow files or documentation?

Thanks.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Two descriptions are in circulation" - factually wrong against the project's own register and breaks the rule that all sides of a recorded contradiction be quoted. PROJECT_SCOPE.md line 127 records CTR-01 with three claims; claim A is omitted: ttihp-verilog-template branch cmos5l info.yaml, "A single tile is about 167x108 uM", valid tiles "1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2". That omitted claim is the one that lists no 6x4 at all, so dropping it removes the sharpest edge of the contradiction.
- "the area a 6x4 CMOS5L project is given" - presupposed answer. It assumes 6x4 is a tile size a project can actually select on that shuttle, which is precisely what the omitted claim A contradicts (its valid-size list stops at 8x2). The addressee is asked to price an option whose existence is the open question.
- "Which of these describes" - forced binary. Offering two options and asking which one describes reality presupposes that one of them does, leaving no way to answer "neither" or to supply a third figure. It also edges toward asking the addressee to confirm a guess.
- "once the power grid, routing obstructions and any margin the flow reserves are accounted for" - presupposed mechanism. It asserts that the flow lays down a power grid inside the tile, that routing obstructions exist there, and that a reserved margin is what consumes the difference. Any of those may be wrong, and the phrasing makes the addressee answer inside our model instead of stating theirs.
- "a project's own standard cells" - presupposed implementation. It assumes the area is filled with standard cells, excluding macros or anything else by construction. The question should ask about a project's own logic without assuming what it is made of.
- "Where in the flow is that defined" - presupposed answer. It assumes the figure is defined somewhere in the flow. If it is nowhere recorded, the question has no honest answer and invites an estimate dressed as a locator.
- "lists 1x1 as 202.08 x 154.98 um and a 6x4 bounding box of 1289.28 x 710.64 um" - technical figures stated as present-tense fact with no retrieval date. The register carries these as CTR-01 claim C read on 2026-09-15 from a moving branch (ihp-sg13cmos5l). Quoting a branch file as current fact will be stale the moment the branch moves, and invites a correction that we cannot date.
- Fallback channel REPO-OBSERVATION over-claims. By the channel's own definition a file shows what the flow does today, not what the competition shuttle will pin, so it cannot settle part 1 at all; it can only settle the locator part. The channel_rationale states why Tiny Tapeout is primary but never states this limit on the fallback.
- Scope mismatch, noted but not a hard-rule breach: the entry is filed as OQ-14 (usable core area, PROJECT_SCOPE.md line 181) while part 1 is verbatim OQ-29 (line 226, "Which of the three tile descriptions in CTR-01 applies?"). The entry should declare that it carries OQ-29 as well, or part 1 will be recorded against the wrong open question.

</details>

## OQ-15 Basis of the cells per tile estimate

- **open question**: [OQ-15](../PROJECT_SCOPE.md#oq-15-basis-of-the-cells-per-tile-estimate)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: NONE
- **why this channel**: The organizer set the competition and its rules and states the competition's area constraints on its own page, so it is the party that sets and publishes this value.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Your competition announcement says, "budget for about 1K logic cells per tile", and "We're targeting IHP's 130nm CMOS5L process through our friends at Tiny Tapeout."

Four separate questions about that cell figure:

1. How was the figure obtained?
2. What is being counted by "logic cell" there?
3. Does the figure refer to a particular standard cell library? If so, which one, and which version?
4. What does the figure already account for, and what does it leave out?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Which standard cell library, and which version of it, does that figure refer to?" - presupposes a mechanism: that the figure refers to a standard cell library at all, and that a library version was involved. It asks which one, not whether one applies. Breaks: the question presupposes no answer and no assumed mechanism.
- "What mix of cells does it assume" - presupposes that a cell mix was assumed in deriving the figure. The repository's own record (PROJECT_SCOPE.md F9) states the basis is not stated, so any derivation method is our imagination, not the organizer's claim.
- "What mix of cells does it assume, and is the count in standard cells or in some other unit?" - two independent questions fused into one numbered item. Breaks: split a question that asks several independent things so each part can be answered separately.
- "Which placement utilization does it assume" - presupposes both that the figure was derived by a utilization-based method and that a specific utilization value exists to be named. Breaks: no assumed value, no assumed mechanism.
- "and does it already account for the power grid, routing and clock tree?" - a second, independent question fused into item 3, and it narrows the answer to three overheads we selected. Breaks: split independent parts; do not smuggle in an assumed mechanism.
- "Was the figure measured on a hardened design, and if so which one, or was it estimated?" - offers the addressee two derivations we invented and asks them to pick. Breaks: the question never asks the addressee to confirm a guess. It is also three parts in one sentence.
- "advises entrants to" - ascribes an intent to the announcement that the fact register does not record. F9 records the sentence as the organizer's rough estimate, quoted, with no stated purpose. Breaks: no assumed intent.
- "on IHP's 130nm CMOS5L process through Tiny Tapeout" - the organizer's own wording (F6: "We're targeting IHP's 130nm CMOS5L process through our friends at Tiny Tapeout.") is restated as our unquoted assertion of fact. Breaks: where the organizer's words must be used, quote them and attribute them.
- channel_rationale "only the organizer can state the library, cell mix and utilization it was derived from" - the rationale itself carries the presupposed derivation. The defensible rationale is only that the organizer wrote the sentence, so only the organizer can say what it refers to. Channel itself (ORGANIZER-EMAIL) is correct and unchanged: this is about the meaning of the organizer's own published statement, not about what a tile physically holds, which would be Tiny Tapeout's.

</details>

## OQ-16 Toolchain and PDK version pinning

- **open question**: [OQ-16](../PROJECT_SCOPE.md#oq-16-toolchain-and-pdk-version-pinning)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-gds-action)
- **fallback channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **why this channel**: Tiny Tapeout publishes tt-gds-action and the cmos5l template flow that pins its action ref and PDK, so the hardening versions in use are stated in its own repositories.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about version pinning in the CMOS5L hardening flow. Context: the ttihp-verilog-template cmos5l branch hardens through TinyTapeout/tt-gds-action@ihp-cmos5l with pdk ihp-sg13cmos5l. Jane Street's competition announcement states it is "targeting IHP's 130nm CMOS5L process through our friends at Tiny Tapeout", with fabrication on a March 2027 CMOS5L shuttle "subject to the foundry schedule".

1. Which LibreLane version does that action ref resolve to today?
2. From which repository, and at which commit, tag or release, does it take the ihp-sg13cmos5l PDK?
3. Can either change while a shuttle's submission window is open, and if so, how is a change announced?
4. For a future CMOS5L shuttle, how and when are the versions used for that run made known to participants?
```

<details><summary>What the reviewing operator changed and why</summary>

- "which one will a 2027 CMOS5L shuttle use?" (and "that shuttle" in items 2 and 3) - presupposes an answer: it treats a 2027 CMOS5L shuttle as an existing, committed run. T4 records that as of 2026-09-15 no March 2027 CMOS5L shuttle is listed by Tiny Tapeout and that it exists only as the organizer's stated target (OQ-30 is open). Ask what is the case, not about a run we have assumed into existence.
- "for a March 2027 shuttle" - a schedule figure attributed to the organizer but stripped of the organizer's own qualifier. F6 records the target as the March 2027 CMOS5L Tiny Tapeout shuttle "subject to the foundry schedule". Quoting the organizer while dropping the hedge states as settled something the project has not verified.
- "Which tt-gds-action ref should a project target for that shuttle" - asks for a recommendation rather than what is the case, and presupposes that a designated ref for that shuttle exists.
- "and is it a fixed tag or a moving branch?" - asks the addressee to confirm one of two guesses we invented, and is a second independent question fused into the same sentence as the ref question.
- "Which LibreLane version does the CMOS5L flow use today, and which one will a 2027 CMOS5L shuttle use?" - two independent questions fused into one numbered item; they must be separable so each can be answered on its own. The present-state half is also settled by reading the flow files (REPO-OBSERVATION), not by asking a maintainer.
- "Which IHP-Open-PDK commit or tag does that flow use for ihp-sg13cmos5l?" - presupposes the mechanism by which the flow obtains the PDK. The register confirms only that CMOS5L PDK content sits on the IHP-Open-PDK dev branch (I1) and that a separate ihp-sg13cmos5l repository exists (I4); how tt-gds-action sources it is unverified. The question forecloses the answer to its own premise.
- "and where is the frozen set published?" - presupposes that a frozen set exists and is published; it is also a second independent question fused into item 4 with "Are these versions frozen at a stated date".
- fallback_channel "ORGANIZER-EMAIL (asic-competition@janestreet.com)" - channel assigned to a party that cannot settle the question. The organizer's remit under the allowed-channel list is rules, eligibility, judging, deliverables, deadline, submission channel and area budget policy; it cannot state which LibreLane build, action ref or PDK version Tiny Tapeout pins. The present-state parts are settled instead by reading the flow and PDK files at S01.
- channel_rationale "decides which LibreLane build, action ref and PDK commit a shuttle runs" - stated as fact but unverified. T2 confirms only that the template's GitHub Actions flow hardens with LibreLane through TinyTapeout/tt-gds-action@ihp-cmos5l with pdk ihp-sg13cmos5l; who fixes each version for a shuttle is part of what OQ-16 is asking.

</details>

## OQ-17 Standard cell set and Liberty corners

- **open question**: [OQ-17](../PROJECT_SCOPE.md#oq-17-standard-cell-set-and-liberty-corners)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-gds-action)
- **fallback channel**: REPO-OBSERVATION
- **why this channel**: Tiny Tapeout publishes the tt-gds-action hardening flow that its cmos5l template invokes at ref ihp-cmos5l with pdk ihp-sg13cmos5l, so its maintainers are the party that publishes how that flow is configured.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Questions about the standard-cell libraries and timing corners used by the IHP CMOS5L (ihp-sg13cmos5l) hardening flow in tt-gds-action.

1. Which standard-cell library or libraries does the flow use for ihp-sg13cmos5l, and under what names?
2. Which timing library files and corners, if any, does the flow use for synthesis?
3. Which timing library files and corners, if any, does it use for post-layout timing checks?
4. Which timing checks, at which corners, must pass for a project to be accepted by the flow?
5. What hold-time checking, if any, does the flow do, and at which corners?

A link to the configuration files that set these would be enough.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Is timing checked at slow and fast corners, or at a single nominal corner?" - false dichotomy. It presupposes the answer is one of two arrangements the drafter imagined and invites the addressee to confirm a guess, instead of asking what is the case. Breaks "presupposes no answer" and "never asks the addressee to confirm a guess".
- "Which Liberty files and PVT corners are used for synthesis, and which for static timing sign-off?" - presupposes a mechanism: that the flow runs a distinct static-timing sign-off step, that it uses a different corner set from synthesis, and that corners are Liberty/PVT-defined. Breaks "presupposes no assumed mechanism". The passive "are used" also hides whether the flow or the PDK selects them, which is part of what is being asked.
- "Question about sign-off libraries and corners" (opening line) - same presupposition, stated as the subject of the message: it asserts that the flow has sign-off libraries and corners before the addressee has said so.
- "Are hold checks run, and at which corner?" - the singular "at which corner" presupposes hold is checked at exactly one corner. Breaks "presupposes no assumed value".
- "If several, which ones gate acceptance of a project?" - ambiguous addressee. "Acceptance of a project" reads either as passing the Tiny Tapeout hardening flow (TT can settle) or as acceptance into the Jane Street competition (only ORGANIZER-EMAIL can settle). As written, part of the question is aimed at a party the assigned channel cannot answer for.
- "A link to the configuration file that sets this would be enough." - the singular "the configuration file" presupposes one file sets all four items.
- channel_rationale: "The libraries and corners used for synthesis and timing sign-off are set by the Tiny Tapeout flow configuration" - asserts as established fact the very mechanism question 1 and 2 are asking about; the corners may be inherited from the IHP PDK's own LibreLane configuration rather than set by Tiny Tapeout. The rationale should claim only that Tiny Tapeout owns and publishes the flow configuration that selects them.
- NOT a problem, checked and cleared: "IHP CMOS5L (ihp-sg13cmos5l)" is verified by the fact register (F6 organizer statement, T2 template flow uses tt-gds-action@ihp-cmos5l with pdk ihp-sg13cmos5l, I1 IHP dev branch), so it is not an unverified figure. No architecture, instruction set, datapath or engine-count leak is present. Channel assignment (TT primary for what the flow selects, REPO-OBSERVATION fallback for what the files show today) is sound and is retained.

</details>

## OQ-18 SRAM availability

- **open question**: [OQ-18](../PROJECT_SCOPE.md#oq-18-sram-availability)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: IHP-GITHUB-ISSUE (IHP-GmbH/IHP-Open-PDK)
- **why this channel**: Tiny Tapeout publishes the cmos5l template and tt-support-tools repositories that define its hardening flow, along with the specification pages describing available macros, so it is the party that publishes this answer.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about SRAM macros for Tiny Tapeout projects on the IHP CMOS5L PDK (ihp-sg13cmos5l). Read on 2026-09-17, the memory page at tinytapeout.com/specs/memory/ documents macros for SG13G2, and I found no equivalent CMOS5L information.

1. Are SRAM macros available to CMOS5L projects today?
2. Are such macros integrated in the CMOS5L hardening flow today?
3. Which macro configurations (words x bits) are provided?
4. From which source are those macros obtained?
5. What are the physical dimensions of each macro?
6. If macros are not available or not integrated today, is integration planned, and if so for which shuttle or date?
```

<details><summary>What the reviewing operator changed and why</summary>

- "can any of them be placed inside a 6x4 tile allocation?" - presupposes an answer and states an unverified figure as fact. CTR-01 (PROJECT_SCOPE.md line 127) is an OPEN contradiction over CMOS5L tile geometry: the template info.yaml lists valid tiles as "1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2" (no 6x4), the organizer states a 6x4 maximum, and tt-support-tools tile_sizes.yaml carries a 6x4 entry. Writing "a 6x4 tile allocation" silently picks one claim, which AG-4 (line 61) forbids for any still-open contradiction.
- "can any of them be placed inside a 6x4 tile allocation?" - also asks the addressee to confirm a fit against a floorplan premise of ours they cannot know, so it is not self-contained, and it is a design/floorplan commitment smuggled into a technology question. The fit is ours to compute as an OBSERVATION from the dimensions asked for in the same item.
- "Are SRAM macros available to CMOS5L projects, and are they integrated in the CMOS5L hardening flow today?" - two independent questions fused into one numbered item; a macro can exist in the PDK without being integrated in the hardening flow, and each half must be separately answerable.
- "which sizes (words x bits) are provided, and from which source are the macros obtained?" - two independent questions fused into one numbered item.
- "What are the physical dimensions of each macro, and can any of them be placed inside a 6x4 tile allocation?" - two things fused, the second being the presupposition above.
- "The memory page at tinytapeout.com/specs/memory/ documents macros for SG13G2 only." - a page reading asserted as a timeless, exhaustive fact with no retrieval date. The register holds this only as part of OPEN_QUESTION I5 (line 119); house style elsewhere dates page readings (T4: "As of 2026-09-15"). State it as what was found on the date read, without the absolute "only".

</details>

## OQ-19 IO electrical specification

- **open question**: [OQ-19](../PROJECT_SCOPE.md#oq-19-io-electrical-specification)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: IHP-GITHUB-ISSUE (IHP-GmbH/IHP-Open-PDK)
- **why this channel**: Tiny Tapeout publishes the cmos5l template pinout in info.yaml, the tile definitions in tt-support-tools and the GPIO, clock and memory specification pages, so it is the party that states what applies at a project tile's pins.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about the IO electrical specification for IHP CMOS5L (ihp-sg13cmos5l) Tiny Tapeout chips. The GPIO page at tinytapeout.com/specs/gpio/ describes sky130 pads.

For CMOS5L chips, please state, or link to where it is stated:
1. the IO supply voltage and the core supply voltage;
2. the output drive specification for project pins, and the conditions (load, supply, temperature) it is stated under;
3. the input voltage limits for project pins, including any absolute maximum rating;
4. which output drive modes project pins support;
5. any maximum switching rate or timing limit specified for project pins.

A link to a datasheet or to pad cell documentation is enough.
```

<details><summary>What the reviewing operator changed and why</summary>

- "whether open-drain operation is available on any project pin" - breaks "presupposes no mechanism" and "never asks the addressee to confirm a guess": it names one IO mode we imagined and asks for a yes/no on it, and it leaks a candidate signalling scheme. Ask which output drive modes the pins support.
- "whether inputs tolerate voltages above the IO supply, and up to what level" - same shape: a yes/no on an assumed property rather than a request for what is the case. Ask for the input voltage limits, including any absolute maximum rating.
- "the output drive strength, and the load it is specified into" - presupposes an answer: that a single drive strength exists and that it is specified into a load. Ask for the output drive specification and the conditions under which it is stated.
- "the maximum input and output toggle frequency specified at the chip pins" - presupposes that such a maximum is specified, and presupposes a mechanism the register does not record: that a project's IOs appear directly at chip pins on CMOS5L. The fact register has T1 (template pins ui/uo/uio) and T3 (the sky130 GPIO page does not mention CMOS5L); it has no CMOS5L chip-level IO mapping.
- channel_rationale "The pads and chip-level IO ring around a project tile are chosen and specified by Tiny Tapeout" - states an unverified integration mechanism as fact. Nothing in the register establishes a chip-level IO ring or who specifies the pads for the CMOS5L shuttle; the rationale must rest on what is evidenced (Tiny Tapeout owns the shuttle flow, the tech data under tt-support-tools branch ihp-sg13cmos5l, and the GPIO specification pages).
- channel_rationale "so only Tiny Tapeout can state the limits that apply at the chip pins" - the exclusivity is contradicted by the entry's own IHP fallback and by I1/I2 (the pad and device content is CMOS5L PDK material on the IHP dev branch). Say why Tiny Tapeout is the party that publishes the project-facing IO specification, not that it is the only party that could know.

</details>

## OQ-20 Clock source range and maximum design clock

- **open question**: [OQ-20](../PROJECT_SCOPE.md#oq-20-clock-source-range-and-maximum-design-clock)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/ttihp-verilog-template)
- **fallback channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **why this channel**: Tiny Tapeout maintains the cmos5l template, its pinout and its hardening flow, and publishes the clock specification pages, so it is the party that defines and publishes clock and timing details for a project tile.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about the clock for Tiny Tapeout projects on IHP CMOS5L (pdk ihp-sg13cmos5l), for example the ttihp 0.4 chip. Your clock page at tinytapeout.com/specs/clock/ gives 1 Hz to 66.5 MHz for the RP2040 demo board and does not mention CMOS5L, so we do not want to assume it carries over.

1. What drives the clk input of a project tile on CMOS5L chips?
2. What clock frequencies are available at that input?
3. What clock period, if any, does the CMOS5L hardening flow sign off against, and how is it set?
4. Apart from the clk input, what clock-related resources, if any, can a project use?
```

<details><summary>What the reviewing operator changed and why</summary>

- "What clock source will drive CMOS5L chips, and what frequency range will be available at the project clock input?" — two independent questions fused into one sentence; the rule requires each independently answerable thing to be its own numbered part.
- "What clock source will drive CMOS5L chips" — presupposes that there is a single clock source, and the future tense presupposes the March 2027 CMOS5L shuttle, whose existence the register records only as the organizer's stated target (T4, OQ-30), not as a fact Tiny Tapeout has confirmed.
- "is that period fixed by the flow or chosen per project?" — a forced binary that presupposes those are the only two mechanisms and asks the addressee to confirm one of our guesses; it is also a second independent question buried inside item 2.
- "Is any on-chip PLL or clock multiplier available to a CMOS5L project?" — names candidate on-chip clocking hardware, so it presupposes a mechanism, and it asks for yes/no confirmation of that guess instead of asking what is actually available.
- "describes the RP2040 demo board and a range of 1 Hz to 66.5 MHz" — detaches the figure from its recorded scope. Fact T3 records 1 Hz to 66.5 MHz as the RP2040 demo-board clock, on pages that do not mention CMOS5L, and records it as MOVING_CONSTRAINT, not as a CMOS5L figure. Stated this way it offers the range as the presupposed answer and invites confirmation.
- "fallback_channel": "ORGANIZER-EMAIL (asic-competition@janestreet.com)" — outside that channel's stated remit (rules, eligibility, judging, deliverables, deadline, submission channel, area budget policy). The organizer cannot settle the clock harness or the flow's timing target, so the fallback is assigned to a party that cannot answer it.
- "The clock reaching a project tile and the period the flow signs off against are fixed by the Tiny Tapeout board and flow" — the rationale asserts as settled the very mechanism the question asks about, and asserts a board when board and package are an open question (T3, OQ-23).
- "TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)" — tt-support-tools holds tile and tech data; the clk pin and the hardening timing target come from ttihp-verilog-template (branch cmos5l) and tt-gds-action@ihp-cmos5l per fact T2, so the issue should be filed where it can be answered.

</details>

## OQ-21 Power budget

- **open question**: [OQ-21](../PROJECT_SCOPE.md#oq-21-power-budget)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: NONE
- **why this channel**: Tiny Tapeout publishes the CMOS5L project template and the tt-support-tools branch that set the per-project pinout and tile dimensions, so it is the party that publishes the per-project limits for designs on this process.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about power for projects on an IHP CMOS5L (ihp-sg13cmos5l) Tiny Tapeout chip.

1. Is a power or current budget stated per project on a CMOS5L chip?
2. If one is stated, in what units is it expressed?
3. Is any such limit checked anywhere in the flow, and if so at which step and by what method?
4. Are there any stated constraints or assumptions about a project's switching activity?
5. Which supplies does a project receive, and at what nominal voltages?
6. Can a project switch off or otherwise control any supply it receives?

A link to documentation is enough.
```

<details><summary>What the reviewing operator changed and why</summary>

- "How many supplies and power domains reach a project, at which voltages, and can a project gate or switch any of them?" - three independent questions fused into one sentence (supply count, voltages, controllability); breaks the rule that independent parts must be split into separate numbered items so each can be answered separately.
- "power domains" - presupposes a power organization (multiple domains) rather than asking what the chip actually provides; breaks the no-presupposed-mechanism / no-presupposed-organization rule.
- "for example a toggle rate assumed for power analysis" - offers an invented mechanism for the addressee to confirm; breaks both the no-presupposed-mechanism rule and the rule against asking anyone to confirm a guess.
- "and in what units is it expressed (average current, peak current, power)" - presupposes that a budget exists and hands the addressee a menu of three guessed answer forms; the dependent part needs an explicit "if one is stated" and no candidate list.
- "checked or enforced during precheck or sign-off" - presupposes where enforcement happens; the register records OQ-07 (whether the Tiny Tapeout precheck applies to this submission at all is still open), so the step should be asked, not assumed.
- channel_rationale: "Any per-project power or current limit on a shared shuttle chip is set and checked by Tiny Tapeout, which supplies the power delivery and the precheck" - states as fact both that such a limit exists and that Tiny Tapeout sets and checks it, while T3 records that the published Tiny Tapeout GPIO/clock/power pages cover sky130 and do not mention CMOS5L, and power budget is itself OQ-21; the rationale must justify the addressee's authority without asserting the unverified answer.
- Channel itself is sound and unchanged: Tiny Tapeout owns the shuttle power delivery, tech config and precheck for ihp-sg13cmos5l (T2, CTR-01 tt-support-tools branch ihp-sg13cmos5l), so it is the party that can settle this; the process identifiers CMOS5L / ihp-sg13cmos5l are evidenced (F6, T2, I1) and are not unverified figures.

</details>

## OQ-22 Applicability of the sky130 pinout description

- **open question**: [OQ-22](../PROJECT_SCOPE.md#oq-22-applicability-of-the-sky130-pinout-description)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/ttihp-verilog-template)
- **fallback channel**: REPO-OBSERVATION
- **why this channel**: Tiny Tapeout maintains ttihp-verilog-template on branch cmos5l, whose info.yaml fixes the project pinout, so it is the party that publishes and can change that definition.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about the project pins on Tiny Tapeout CMOS5L (ihp-sg13cmos5l) tiles.

The GPIO page at tinytapeout.com/specs/gpio/ is written in terms of sky130 and does not mention CMOS5L. On branch cmos5l of TinyTapeout/ttihp-verilog-template, info.yaml and the project module define ui[7:0], uo[7:0], uio[7:0], clk and rst_n.

1. Which parts of that GPIO page apply to CMOS5L tiles as written, and which do not?
2. Besides ui, uo, uio, clk and rst_n, what other signals does the CMOS5L harness present to a project module, and what is each for?
3. Is anything else on a CMOS5L chip connected to the project pins? If so, what must a project observe about what it drives on them and when?

If CMOS5L documentation for this exists, a link answers all three.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Is the ena signal present on CMOS5L, with the same behaviour and timing?" - presupposes a mechanism (an enable signal) and asks the addressee to confirm our guess with a yes/no. The signal name is imported from sky130 without attribution, and the register's only pinout fact (T1, PROJECT_SCOPE.md line 106) lists ui[7:0], uo[7:0], uio[7:0], clk and rst_n only; no fact record covers an ena signal at all.
- "with the same behaviour and timing" - states as given a sky130 behaviour and timing that the project has not recorded anywhere, and asks for a comparison against it; the addressee cannot answer without accepting our unverified baseline.
- "What chip infrastructure shares the project pins on CMOS5L" - presupposes the answer: it asks what the shared infrastructure is rather than whether anything is connected to the project pins.
- "and what does it require of a project regarding what it may drive on those pins and when?" - fused into the same sentence as the previous clause and conditional on its presupposed answer; it is a separate question and must be separable or conditional.
- "Does that pin description apply unchanged to CMOS5L projects, or does anything differ?" - "apply unchanged" is confirm-a-guess framing, and "that pin description" is ambiguous after a preamble that names two different sources (the GPIO page and the template), so the addressee cannot tell which is being asked about. Fails self-containment.
- "The GPIO page at tinytapeout.com/specs/gpio/ describes sky130 chip infrastructure, while the CMOS5L template fixes eight inputs, eight outputs and eight bidirectional pins plus clk and rst_n" - the figures match T1 and T3, but both claims are unattributed in the outgoing text. T1 is specific to info.yaml and the module on branch cmos5l of ttihp-verilog-template; naming the file and branch lets the addressee check the claim rather than take ours.
- "primary_channel": "TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)" - right party, wrong repository. The pin list and module ports the question quotes live in ttihp-verilog-template branch cmos5l (T1); tt-support-tools holds tile and config data (it is the CTR-01 source for tile_sizes.yaml). File the issue where the artefact under discussion lives.
- "fallback_channel": "REPO-OBSERVATION" with blocks_artifact true - a file can settle which ports the CMOS5L template declares, but not what is connected to those pins on the chip, what a project must observe when driving them, or what the shuttle will pin. Keep it as a fallback only for the port list, not for parts 1 and 3.
- "the enable signal and whatever infrastructure shares project pins are part of the Tiny Tapeout chip harness" (channel_rationale) - the rationale asserts as established the two things the question is supposed to be asking about. Rewrite it to justify the party without importing the presupposition.

</details>

## OQ-23 Board and package

- **open question**: [OQ-23](../PROJECT_SCOPE.md#oq-23-board-and-package)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **why this channel**: Tiny Tapeout publishes the CMOS5L project template, the tt-support-tools branch whose tile_sizes.yaml defines tile dimensions, and the GPIO, clock and memory specification pages, so it is the party that publishes the shuttle-level specifications for projects on this process.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Question about chip delivery for Tiny Tapeout CMOS5L (ihp-sg13cmos5l) shuttles. The Tiny Tapeout GPIO and clock specification pages do not mention CMOS5L, so we could not find this there.

1. In what form are fabricated chips returned to project owners for a CMOS5L shuttle?
2. If they are packaged, which package is used, and how many pins or pads does it have?
3. If they are supplied on a board, which board is it?
4. How is that determined for a given CMOS5L shuttle, and what applies to the shuttles currently planned?
```

<details><summary>What the reviewing operator changed and why</summary>

- "the RP2040-based demo board, or a different board?" — breaks the no-guess-confirmation and no-presupposed-answer rules: it offers a candidate and reduces an open question to a binary. The register (T3) records the RP2040 demo board only on the sky130 GPIO/clock pages, which it explicitly notes "do not mention CMOS5L", so the candidate is an unverified carry-over presented to the addressee as the likely answer. Naming an MCU-based board also brushes the no-architecture-mention rule.
- "On which board are CMOS5L chips delivered" — presupposes a mechanism: that CMOS5L shuttle chips are delivered on a board at all. F14 records only the organizer's statement about what competition winners receive; nothing in the register says Tiny Tapeout delivers CMOS5L shuttle chips mounted on a board. Ask what form delivery takes, not which board.
- "so we would like to know which board that is" — presupposes a single board exists and has already been decided; it also asks Tiny Tapeout to answer for a Jane Street prize arrangement.
- "In which package are CMOS5L chips assembled, and with how many pins?" — two things in one sentence, and it presupposes assembly in a pinned package, excluding bare die or a pad-only package. State the package question so an unpackaged or pad-count answer fits.
- "Is the board and package choice the same for every CMOS5L shuttle, or decided per shuttle?" — a closed either/or that presupposes the answer set (a third possibility, e.g. not yet decided for any shuttle, has no slot), and it fuses board and package into one item so the two cannot be answered separately.
- "Jane Street's competition announcement states that winners receive their fabricated chip mounted on a dev board, so we would like to know which board that is." — channel mismatch inside the question text: what winners receive is settled only by the organizer (ORGANIZER-EMAIL), not by the primary addressee. As context for Tiny Tapeout it is project framing that does not help them answer more precisely, so under the why-it-is-needed rule it should not be there.
- channel_rationale "Tiny Tapeout assembles and ships the chips from its shuttles" — stated as fact but not evidenced anywhere in the register; the rationale rests on an assumed mechanism. The defensible rationale is that Tiny Tapeout runs the CMOS5L shuttle and publishes its chip and board specifications in public (T3, T4), with the organizer as fallback for what winners specifically receive.

</details>

## OQ-24 Shuttle logistics and fallback

- **open question**: [OQ-24](../PROJECT_SCOPE.md#oq-24-shuttle-logistics-and-fallback)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: TT-GITHUB-ISSUE
- **why this channel**: The organizer set the competition's rules, its submission deadline and the Tiny Tapeout route it states it is targeting, and it says it emails sign-ups with updates, so it is the party that states which run its competition uses and what happens to the competition if that run moves, while Tiny Tapeout publishes its own shuttle runs page as a second source.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

I am preparing an entry for the protocol emulator ASIC competition. The announcement page states that fabrication targets the March 2027 CMOS5L Tiny Tapeout shuttle, "subject to the foundry schedule", and asks entrants to "Submit your design by January 18th, 2027". Three questions:

1. What is the current status of that shuttle: which Tiny Tapeout run, if any, has been identified for it, and what dates are currently expected?
2. The page states that Jane Street will pay to tape out "the most novel designs". What costs, if any, fall on an entrant?
3. If the shuttle date changes, what happens to the competition and to the January 18th, 2027 submission date?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Which Tiny Tapeout run is this, by its name or identifier, and what are its open and close dates?" - presupposes an answer: that a specific run has already been identified, named and scheduled. The project's own register contradicts this (T4, CONFIRMED_FACT: "As of 2026-09-15 no March 2027 CMOS5L shuttle is listed on the runs page; the target shuttle exists only as the organizer's stated target"). Breaks the no-presupposed-answer rule.
- "what are its open and close dates" - presupposes an open/close submission-window mechanism for the run. No fact in the register establishes that mechanism for a CMOS5L shuttle. Breaks the no-presupposed-mechanism rule.
- "Is there a price per tile for an entrant, and if so what is it and who pays it?" - presupposes an entrant-paid, per-tile pricing mechanism. Nothing in the register records Tiny Tapeout pricing, and F13 records the opposite direction: Jane Street "will pay to tape out 'the most novel designs'". The question neither quotes nor accounts for that recorded statement, so it asks the organizer to react to a mechanism the project invented. Breaks the no-presupposed-mechanism rule and the no-unverified-figure rule.
- "Is there a price per tile for an entrant, and if so what is it and who pays it?" - also fuses three independent things (whether a charge exists, its amount, and the payer) into one sentence. Breaks the rule requiring independent things to be split into separate numbered parts.
- fallback_channel "TT-GITHUB-ISSUE" - that channel's stated scope is "the shuttle flow, tile geometry, pinout, precheck, toolchain and PDK pinning", raised as issues on ttihp-verilog-template, tt-support-tools or tt-gds-action. Run scheduling, commercial pricing, and the effect of a schedule slip on Jane Street's competition and its January 18th 2027 deadline are outside that scope, and no Tiny Tapeout repository can settle any of them. Breaks the rule against assigning a channel to a party that cannot settle the question.
- channel_rationale "Tiny Tapeout is the fallback because it publishes the run calendar and pricing itself" - an unverified claim used to justify the channel. The Tiny Tapeout fact register (T1-T4) records no run calendar and no pricing source; T4 records only the runs page, which is not an allowed channel. Breaks the no-unverified-claim rule.
- channel_rationale "which run its competition is booked on" - presupposes the competition is booked on a run. F6 records only that fabrication is "targeting" the March 2027 shuttle, "subject to the foundry schedule". Breaks the no-presupposed-answer rule.

</details>

## OQ-25 PDK promotion from dev to main

- **open question**: [OQ-25](../PROJECT_SCOPE.md#oq-25-pdk-promotion-from-dev-to-main)
- **primary channel**: IHP-GITHUB-ISSUE (IHP-GmbH/IHP-Open-PDK)
- **fallback channel**: NONE
- **why this channel**: IHP publishes IHP-Open-PDK, whose dev branch currently carries the ihp-sg13cmos5l directory and the preview-only wording, so IHP is the party that decides and announces when that content moves to main and when that wording changes.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
The README on the dev branch of IHP-Open-PDK states that the open-source PDK content is "preview only", that it is not intended for production "at this moment", and that the CMOS5L models are not yet validated on CMOS5L silicon. Questions about the CMOS5L PDK (ihp-sg13cmos5l) on that branch:

1. Is there a plan for this content to be merged into the main branch, and if so on what timeline?
2. Are release tags or version identifiers planned for it?
3. Is any state of it designated as suitable for a tapeout, and if so how is that state identified?
4. Under what conditions, if any, would the preview and not-yet-validated wording be changed?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Will a release tag or version identifier be published for CMOS5L, and how should a user tell which state is intended for a tapeout?" - two independent questions fused into one numbered item. Tagging policy and how a tapeout-suitable state is identified are separable and must be separate numbered parts so each can be answered on its own.
- "how should a user tell which state is intended for a tapeout" - presupposes an answer: it assumes some state of the CMOS5L content is (or will be) designated for a tapeout. The repository's own I3 records IHP saying the content is "preview only" and not intended for production "at this moment", so the existence of a tapeout-intended state is exactly what is unknown. Must be asked as whether any such designation exists, not how to read it.
- "What has to happen before the preview and not-validated wording changes?" - presupposes intent (that the wording is expected to change) and mechanism (that a defined set of prerequisites exists). Needs an explicit "if any" / "if it would change" so it asks what is the case rather than assuming a plan.
- "states that the open-source PDK content is preview only, that it is not intended for production at this moment, and that the CMOS5L models are not yet validated on CMOS5L silicon" - the register (PROJECT_SCOPE.md I3) holds "preview only" and "at this moment" as quoted README wording; the draft renders the source's own words as unquoted paraphrase while still attributing them to the README. Where the source's wording is relied on it must be quoted and attributed, not restated.
- "The README on the dev branch of this repository" plus "CMOS5L (ihp-sg13cmos5l)" - weak self-containment and an ambiguous identifier: I4 records a separate standalone repository also named ihp-sg13cmos5l, so "this repository" plus that name can point at two different things. Name IHP-Open-PDK and the dev branch explicitly and bind the identifier to the content on that branch.

</details>

## OQ-26 Expected verification framework

- **open question**: [OQ-26](../PROJECT_SCOPE.md#oq-26-expected-verification-framework)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and publishes no rubric, jury or winner count, so it is the party that decides and states what it expects of entries, and it has said it will add a final submission form to its announcement page.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

A question about the protocol emulator ASIC competition. The announcement states that any HDL and verification techniques are welcome, "including formal methods, random constrained tests, AI-assisted verification", and that Jane Street uses Hardcaml internally but does not require it.

1. Is any particular verification framework, language or tool expected in a submission?
2. How does verification work factor into the assessment of an entry?
3. What verification material, if any, should a submission include?
4. If verification material is included, what form should it take?

A short written answer is fine. Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "Is verification assessed separately from the design itself, and if so on what basis?" - presupposes a mechanism: that assessment is decomposed into a design component and a verification component. The repository records (F13) that no rubric, weights, jury or number of winners has been published, so the separable structure is our invention and the organizer is being asked to confirm a guess. Breaks 'presupposes no mechanism' and 'never asks the addressee to confirm a guess'.
- "Is verification assessed separately from the design itself, and if so on what basis?" - two things fused into one sentence (whether a separate assessment exists, and what its basis is). Breaks 'split a question that asks several independent things into a numbered list', since the second half is a distinct question the addressee may answer even if the first framing is wrong.
- "for example simulation sources, logs, coverage reports or proof scripts" - supplies a menu of four of our own guesses and steers the reply toward picking from them instead of asking what is the case. Breaks 'the question presupposes no answer' and 'never asks the addressee to confirm a guess'.
- "In what form should verification work be submitted" - presupposes that verification work is part of the submission at all, which is precisely what item 4 of the same message is still asking. Breaks 'presupposes no answer' (an assumed intent smuggled in ahead of the question that would establish it).
- "must contain to be considered complete" - presupposes a completeness standard against which submissions are checked. Nothing in the announcement (F10-F13, F15) states that such a standard exists; the phrase invents the mechanism the answer is supposed to describe. Breaks 'presupposes no mechanism'.

</details>

## OQ-27 Firmware toolchain and ISA document as deliverable

- **open question**: [OQ-27](../PROJECT_SCOPE.md#oq-27-firmware-toolchain-and-isa-document-as-deliverable)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules and so decides what a submission must contain, and it publishes asic-competition@janestreet.com as its contact address; the announcement page is the fallback because the organizer has said a submission form will be added there closer to the deadline.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

A question about the deliverables of the protocol emulator ASIC competition. The announcement, describing a protocol emulator, says you can "implement a real protocol in firmware", and says the submission "should be open source so others can use and build on it".

If a submitted design needs software or configuration data to operate:

1. Must the deliverable include that software or data?
2. Must the deliverable include the tools that produce it?
3. Must the deliverable include the source of those tools?
4. Must the deliverable include written documentation of the procedure for loading it onto a fabricated chip?
5. Are any of these taken into account when entries are assessed, whether or not they are required?

A short written answer is fine. Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "the tools that produce that software or data, and their source" - two independent things fused into one question. Whether a producing tool must be shipped and whether that tool's source must be shipped can be answered differently (a binary generator required, its source not). The rule requires independent things split into separate numbered parts.
- "Must the deliverable include written documentation of how the fabricated chip is programmed?" - presupposes a mechanism and a fact not in evidence: that a submitted design is programmed at all, and that a fabricated chip exists. Item 1 correctly hedges with "If a submitted design needs software or configuration data to operate"; item 2 drops that hedge and asserts the programming step. Per F14 only winning entries are fabricated, so "the fabricated chip" also presupposes an outcome at submission time.
- "If neither is required, is either taken into account when entries are assessed?" - not answerable on its own: it depends on the answers to parts 1 and 2, and its condition collapses if exactly one of the two is required, in which case the addressee can neither answer nor skip it cleanly. "either" also fuses the judging question for two distinct deliverables.
- "The announcement describes the goal as being able to implement a real protocol \"in firmware\"" - misattributes the quoted words. Per the register (F3) that sentence is the organizer's description of what a protocol emulator is, not a statement of the competition's goal. Organizer words must be quoted and attributed as what they actually are.
- "rather than in fixed logic" - presented as part of the announcement's description, but in the register (F3) this phrase sits outside the quotation marks as the repository's own paraphrase. Unverified wording should not be handed to the organizer as theirs.
- "asks that the submission be open source" - strengthens the organizer's recorded wording, which is "should be open source so others can use and build on it" (F10). Quote it rather than upgrade "should" into an "ask".
- Not a rule breach, recorded for completeness: the channel assignment is correct. Required deliverables and their weight in assessment are definitional and judging matters that only the organizer can settle (F13 publishes no rubric), so ORGANIZER-EMAIL is the party that can settle it, and ORGANIZER-PAGE-MONITOR is a permissible fallback because it is not the sole channel and blocks_artifact is false. No unverified technical figure appears in the text.

</details>

## OQ-28 Repository hosting and naming

- **open question**: [OQ-28](../PROJECT_SCOPE.md#oq-28-repository-hosting-and-naming)
- **primary channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **fallback channel**: ORGANIZER-PAGE-MONITOR
- **why this channel**: The organizer set the competition and its rules, so it decides submission hosting, visibility and naming requirements and publishes the contact address for questions about them; the announcement page is the fallback because the organizer states it will add the final submission form there closer to the deadline.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Hello,

Some questions about the requirements that apply to a submission to the protocol emulator ASIC competition.

1. If a submission is made as, or includes, a source repository, are there any requirements on where that repository is hosted?
2. What requirements, if any, apply to the submitted material being publicly available, and from which date?
3. Are there any naming requirements on the submitted material, on its files, or, where it includes HDL source, on its top-level module?
4. Are any automated checks or build workflows required to have been run and to have passed for a submission to be accepted?

A short written answer to each numbered point is fine. Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "A question about how entries to the protocol emulator ASIC competition are hosted and identified." - the framing sentence itself presupposes that entries are hosted somewhere, i.e. that the submission takes the form of hosted material. Presupposed mechanism.
- "Are there requirements on where the submitted repository is hosted" - presupposes that a submission is (or contains) a repository. The register records the submission's contents and channel as unsettled (OQ-03 Complete submission contents, OQ-04 Submission channel); the organizer's recorded words say only that the submission "should be open source" (F10). Asking what is the case would not assume the vehicle.
- "for example that it be on GitHub?" - smuggles a candidate answer into the question and invites the addressee to confirm a guess. Violates both the no-assumed-value rule and the no-confirm-a-guess rule.
- "Must the repository be public at the moment of submission, or by some later date?" - forced choice between two invented options. It presupposes that a public-availability requirement exists and that it falls at one of those two moments. F11 records only that building in public is allowed, which is a permission, not a requirement.
- "on the name of the design's top-level module" - presupposes that the deliverable takes the form of HDL source with a top-level module. OQ-01 records that whether the Tiny Tapeout template and flow are mandatory is not stated, and T1's top module is Tiny Tapeout's template artefact, not an organizer requirement.
- "Is any specific continuous integration or build workflow required to be present and passing in the repository?" - presupposes the repository again, and imports a continuous-integration mechanism that no organizer fact mentions; the GitHub Actions flow is a Tiny Tapeout template property (T2), not an organizer statement. Existence-neutral phrasing is needed.
- "Hosting, visibility and naming requirements for a submission are competition rules" (channel_rationale) - asserts that such requirements exist, the same presupposition the question must avoid; the rationale should say only that if any such requirements exist, the organizer is the party that sets them.
- No technical figure is stated as fact anywhere in the entry, and the primary/fallback channel pair is admissible: rules and deliverables are the organizer's to settle, and ORGANIZER-PAGE-MONITOR is used as a fallback only, with blocks_artifact false. Channel unchanged.

</details>

## OQ-29 Tile dimensions and valid tile sizes

- **open question**: [OQ-29](../PROJECT_SCOPE.md#oq-29-tile-dimensions-and-valid-tile-sizes)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **why this channel**: Tiny Tapeout defines the tile dimensions in tile_sizes.yaml on the ihp-sg13cmos5l branch of tt-support-tools and publishes that flow openly, so it is the party that sets and states the selectable tile sizes; the organizer is asked second because it sets the competition's own area rule of a current maximum of 6x4 tiles with 8x4 under consideration.
- **blocks an artifact**: yes
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Two Tiny Tapeout files and the Jane Street competition announcement give different tile figures for CMOS5L.

1. info.yaml on branch cmos5l of ttihp-verilog-template comments "A single tile is about 167x108 uM" and names valid tiles "1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2".
2. tech/ihp-sg13cmos5l/tile_sizes.yaml on branch ihp-sg13cmos5l of tt-support-tools gives 1x1 as 202.08 x 154.98 um and has a 6x4 entry but no 8x4.
3. Jane Street's announcement gives about 200 um by 150 um per tile and states "The current maximum area is 6x4 tiles per design. We are working on the possibility of scaling up to 8x4 tiles (~30% more area)."

Please answer separately:
a. What tile dimensions does the CMOS5L flow use today?
b. Which tile sizes are selectable today?
c. What determines the selectable set for a given shuttle run?
d. When these files differ, which one does the flow read at build time?
```

<details><summary>What the reviewing operator changed and why</summary>

- "which of these describes the tile geometry the CMOS5L flow uses today" - presupposes that one of the three quoted sources is correct. It is a closed multiple choice over values we assembled, so it asks the addressee to pick our option rather than state what is the case, and it is close to asking for confirmation of a guess. The permitted form is to quote the sides neutrally and then ask openly what the current value is.
- "which tile sizes are selectable for CMOS5L, and is that set fixed per run" - two independent questions fused into one item, against the rule that independent parts go as separate numbered items. "fixed per run" also presupposes a per-run selection mechanism we imagined and invites a yes/no confirmation of it.
- "which file should be treated as authoritative when they disagree" - not answerable by this addressee. It asks Tiny Tapeout to arbitrate between its own files and Jane Street's announcement, which only the organizer can settle for entrants; it also calls source 3 a file when it is an announcement page; and "should be treated as authoritative" asks the addressee to rule on our evidence process rather than state a fact. TT can only say which file its flow reads.
- "states about 200 um by 150 um per tile and a maximum of 6x4 tiles" - states as settled a figure the fact register carries as MOVING_CONSTRAINT (F8) and misquotes the organizer by dropping "current" and the following sentence. The register records: "The current maximum area is 6x4 tiles per design. We are working on the possibility of scaling up to 8x4 tiles (~30% more area)." Organizer wording must be quoted and attributed, not compressed into a flat maximum.
- "Three public sources give different tile descriptions for the IHP CMOS5L flow" - presupposes that the competition announcement is a description of the CMOS5L flow. It describes the competition's area budget; only sources 1 and 2 are flow files. Each source should be attributed to what it actually is.
- channel_rationale: "the organizer is the fallback only because one of the three conflicting figures is the organizer's own and only it can say what it requires of entrants" - a fallback is a second route for the same question, not a way to smuggle an organizer-only sub-question into a Tiny Tapeout issue. What the competition requires of entrants, and the 6x4 versus 8x4 decision, belong in a separate organizer entry (the register already carries OQ-13 for the 6x4/8x4 decision date). With the arbitration part removed, TT-GITHUB-ISSUE primary and ORGANIZER-EMAIL fallback are correct, so the channel itself is unchanged.
- Channel is underspecified: the entry says TT-GITHUB-ISSUE but never names the repository, while the quoted files live in two of them (ttihp-verilog-template and tt-support-tools). tile_sizes.yaml is owned by tt-support-tools, so the issue goes there.
- Secondary: the quoted file contents carry no retrieval date or commit, only branch names, so the addressee cannot tell which revision we read. Branches are kept in the rewrite; add the retrieval date when the entry is actually sent.

</details>

## OQ-30 Listing of the March 2027 shuttle

- **open question**: [OQ-30](../PROJECT_SCOPE.md#oq-30-listing-of-the-march-2027-shuttle)
- **primary channel**: TT-GITHUB-ISSUE (TinyTapeout/tt-support-tools)
- **fallback channel**: ORGANIZER-EMAIL (asic-competition@janestreet.com)
- **why this channel**: Tiny Tapeout publishes the runs page where its shuttles are listed and the cmos5l repositories themselves, and Jane Street states it is targeting CMOS5L through Tiny Tapeout and emails sign-ups with updates.
- **blocks an artifact**: no
- **reviewed**: question text rewritten by the reviewing operator; channel rationale rewritten to rest only on verified facts
- **drafted question text**:

```text
Jane Street's competition announcement at blog.janestreet.com/protocol-emulator-asic-competition says "We're targeting IHP's 130nm CMOS5L process through our friends at Tiny Tapeout", and gives the fabrication target as a March 2027 CMOS5L Tiny Tapeout shuttle, "subject to the foundry schedule". Checking tinytapeout.com/runs on 15 September 2026, we did not find a CMOS5L run for 2027 listed.

1. What CMOS5L runs, if any, are currently planned, and on what dates?
2. Where is a CMOS5L run date first made public?
3. What is published about a run when it is first listed?
4. At what point are the PDK and tool versions for a run made known?

Thank you.
```

<details><summary>What the reviewing operator changed and why</summary>

- "As of today no such run appears on tinytapeout.com/runs." — states as current a check the register dates to 2026-09-15 (fact T4), and asserts a negative about the addressee's own site as fact. Breaks the rule against stating a technical claim the project has not verified as of the stated time; it also frames the reader's site back at them rather than asking what is the case.
- "with fabrication on a March 2027 CMOS5L shuttle" — the register (F6) records the organizer's words as qualified, "subject to the foundry schedule". Dropping the qualifier states the date more firmly than the source does, and paraphrases the organizer where the rule requires the organizer's own words to be quoted and attributed (only "through our friends at Tiny Tapeout" is quoted).
- "Is a CMOS5L run planned for 2027, and if so when will it be listed on the runs page?" — two independent things fused into one numbered item (whether a run is planned; when it is listed), and "will it be listed on the runs page" presupposes the mechanism that a planned run is published there. The yes/no form also asks the addressee to confirm the project's reading of a third party's announcement rather than to state what is the case.
- "the PDK and tool versions it pins" — presupposes a mechanism: that a run pins PDK and tool versions and does so at listing time. The project's own OQ-16 records "are they pinned?" as an open question, so this smuggles an assumed mechanism into the question.
- "price per tile" and "open and close dates" — an "for example" list that supplies assumed values and mechanisms (per-tile pricing, an open/close window) into what should be an open question about what is published.
- channel_rationale: "may know the date before it is listed" — speculation about what the answer might be. The primary channel itself is sound and is left unchanged: OQ-30 asks when Tiny Tapeout will list a run, Tiny Tapeout owns its runs page and answers scheduling in public, and the organizer remains a defensible fallback because it stated the target.

</details>

## OQ-31 Licence of the standalone CMOS5L repository

- **open question**: [OQ-31](../PROJECT_SCOPE.md#oq-31-licence-of-the-standalone-cmos5l-repository)
- **primary channel**: REPO-OBSERVATION
- **fallback channel**: IHP-GITHUB-ISSUE (IHP-GmbH/ihp-sg13cmos5l)
- **why this channel**: IHP publishes the repository, so the licence it applies is read from the repository itself; the issue tracker is the fallback where the repository does not state it in a form a claim can cite.
- **blocks an artifact**: no
- **reviewed**: opened at S00 after the re-extraction; written directly against the rules the other entries were checked against
- **drafted question text**:

```text
Question about the licence of IHP-GmbH/ihp-sg13cmos5l.

The README of that repository contains no licence section and no copyright notice. Under which licence is the content of the repository released, and where is that stated in a file inside the repository?
```


## Summary

| Check | Result |
| --- | --- |
| Open questions in PROJECT_SCOPE.md | 31 |
| Entries with a drafted question text and a channel | 31 |
| Entries the reviewing operator rewrote | 30 of the 31; OQ-31 was opened afterwards |
| Questions marked as blocking a benchmark artifact | 15 |

Blocking: OQ-01, OQ-03, OQ-04, OQ-05, OQ-07, OQ-09, OQ-10, OQ-11, OQ-16, OQ-17, OQ-19, OQ-20, OQ-22, OQ-26, OQ-29. A blocking question that is still unanswered when an artifact needs it is closed by a DECISION of subtype ASSUMPTION per [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#decision), never by a supposed value.

