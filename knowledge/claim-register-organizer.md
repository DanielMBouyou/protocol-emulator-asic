# Claim register: organizer page

An excerpt is verbatim source text. Where it contains markup that a renderer would reinterpret, it is wrapped in inline code so that every character is shown as the source prints it.

Part of the claim register, split by source group per [DEC-0011](decision-log.md#dec-0011-splitting-the-claim-register-by-source-group). Index and the meaning of the `double_extraction` field: [claim-register.md](claim-register.md).

Every record comes from the second S00 double extraction, [OBS-0003](observation-register.md#obs-0003-second-double-extraction-under-the-amended-rule). Two operators read each source independently under the amended [atomic fact rule](../EVIDENCE_POLICY.md#atomic-fact-rule), and a third operator, which produced neither set, paired the claims. Read `double_extraction` before relying on any record.

`subject_tags` and `rq_ids` were assigned at consolidation from the vocabulary of [DEC-0007](decision-log.md#dec-0007-s00-d7-controlled-vocabulary-of-subject-tags), not by the extracting operators. They are retrieval keys, not evidence.


### CLM-0001

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post header, <h3> inside div.post-title, immediately above the date line
- **excerpt**: "Can you design a chip? Announcing the protocol emulator ASIC competition"
- **statement**: The post's title heading states "Can you design a chip? Announcing the protocol emulator ASIC competition"
- **kind**: DEFINITION
- **value**: Can you design a chip? Announcing the protocol emulator ASIC competition
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; heading text retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: CONTESTED EXTRACTION: the operators reported the source differently; this claim may not support a CONFIRMED_FACT until it is re-read
- **caveats**: O1 (seq 1) attributes the prefix-free string to the HTML <title> element ("also rendered as the post <h3>"); O2 (seq 1, seq 2) shows the <title> element prints "Jane Street Blog - ... " with a prefix and a trailing space, and the prefix-free string only in the <h3>. O1's own seq 2 excerpt of the <title> carries the "Jane Street Blog - " prefix, so that excerpt settles it against O1's seq 1 locator
- **re-enters bootstrap entry**: F1

### CLM-0002

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: HTML <head>, <title> element (trailing space before the closing tag)
- **excerpt**: "Jane Street Blog - Can you design a chip? Announcing the protocol emulator ASIC competition"
- **statement**: title is set to "Jane Street Blog - Can you design a chip? Announcing the protocol emulator ASIC competition "
- **kind**: DEFINITION
- **value**: Jane Street Blog - Can you design a chip? Announcing the protocol emulator ASIC competition
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; head element retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F1

### CLM-0003

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: HTML <head>, <meta property="og:site_name">
- **excerpt**: "Jane Street Blog"
- **statement**: og:site_name is set to "Jane Street Blog"
- **kind**: DEFINITION
- **value**: Jane Street Blog
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; meta attribute retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O2 only (seq 2 of the F1 group, claim seq 3). O1 recorded the publisher from the <title> prefix instead (its seq 2) and never quoted the meta tag.
- **re-enters bootstrap entry**: F1

### CLM-0004

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post header, <span class="date"> immediately below the title heading; printed as "Sep 10, 2026 | " with a trailing pipe separator before the read-time figure
- **excerpt**: "Sep 10, 2026"
- **statement**: The post is dated "Sep 10, 2026".
- **kind**: QUANT
- **value**: 2026-09-10
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; date string retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F1

### CLM-0005

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post header, author block, two consecutive author lines linking to /author/bdevlin and /author/asinghani
- **excerpt**: "By: Benjamin Devlin By: Anish Singhani"
- **statement**: The post's byline states "By: Benjamin Devlin" and "By: Anish Singhani", in that printed order
- **kind**: QUAL
- **value**: Benjamin Devlin; Anish Singhani
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; two repeated instances of one printed predicate recorded as a single fact whose object is the printed list in printed order; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F1

### CLM-0006

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 3 of 6, bold label "Open source:", first sentence
- **excerpt**: "Your submission should be open source so others can use and build on it."
- **statement**: Your submission should be open source so others can use and build on it [Your submission].
- **kind**: RULE
- **value**: open source
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: should
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the modal "can" sits in a subordinate purpose clause and so stays in the statement text while the modality field records only "should"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE, LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F10

### CLM-0007

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "license" (0 hits); variants also searched case-insensitively with no match: "licence", "licensed", "licensing", "MIT", "Apache", "GPL", "CERN", "OHL", "CC-BY", "SPDX"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "license"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-RULE, LICENSE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F10

### CLM-0008

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 3 of 6 ("Open source:"), second sentence, first clause
- **excerpt**: "Unlike the reverse-engineering puzzle, there’s no need to keep your work hidden until the deadline"
- **statement**: Unlike the reverse-engineering puzzle, there’s no need to keep your work hidden until the deadline
- **kind**: RULE
- **value**: no need to keep your work hidden until the deadline
- **unit**: DIMENSIONLESS
- **conditions**: Unlike the reverse-engineering puzzle; until the deadline
- **modality**: NONE
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the source uses a curly apostrophe in "there’s"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F11

### CLM-0009

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 3 of 6 ("Open source:"), second sentence, final clause, printed after the coordinator "so"
- **excerpt**: "so feel free to build in public!"
- **statement**: feel free to build in public!
- **kind**: RULE
- **value**: build in public
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed clause retrieved verbatim from the raw HTML; the source prints a leading "so" and a terminal exclamation mark; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F11

### CLM-0010

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 4 of 6, bold label "Teams:", first clause
- **excerpt**: "This is a much bigger project than the puzzle"
- **statement**: This [Design an open-source, general-purpose protocol emulator ASIC] is a much bigger project than the puzzle [the reverse-engineering puzzle]
- **kind**: QUAL
- **value**: a much bigger project than the puzzle
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the deixis "This" and the anaphor "the puzzle" are resolved with wording taken verbatim from elsewhere in the same article; "much bigger" is the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F11

### CLM-0011

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 4 of 6 ("Teams:"), final clause, printed after the coordinator "so"
- **excerpt**: "so we strongly recommend working in teams."
- **statement**: we strongly recommend working in teams.
- **kind**: QUAL
- **value**: working in teams
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; "strongly recommend" is a lexical verb rather than a modal auxiliary, so the modality field reads NONE; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F11

### CLM-0012

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "team size" (0 hits); variants also searched case-insensitively with no statement of a team-size limit: "size of", "members", "member", "per team", "limit", "maximum" (whose only match is "The current maximum area is 6x4 tiles per design"), "at most"; "team" itself occurs in the article body only in the "Teams:" rule
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "team size"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-RULE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F11

### CLM-0013

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 5 of 6, bold label "Deadline:"; "January 18th, 2027" printed in bold
- **excerpt**: "Submit your design by January 18th, 2027."
- **statement**: Submit your design by January 18th, 2027.
- **kind**: PROCEDURE
- **value**: 2027-01-18
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative in a rule bullet retrieved verbatim from the raw HTML; the source prints the date as "January 18th, 2027" and the value field renders it in ISO 8601; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0014

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", standalone paragraph immediately after the "Sign-up" paragraph
- **excerpt**: "We’ll add a final submission form to this page closer to the deadline!"
- **statement**: We’ll add a final submission form to this page [Can you design a chip? Announcing the protocol emulator ASIC competition] closer to the deadline!
- **kind**: QUAL
- **value**: a final submission form
- **unit**: DIMENSIONLESS
- **conditions**: closer to the deadline
- **modality**: ’ll
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the deixis "this page" is resolved with the document's own printed title; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0015

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", paragraph opening with the bold run-in "Sign-up", first sentence; "sign-up form" is hyperlinked to a Google Forms URL
- **excerpt**: "If you’re interested, please fill out our sign-up form."
- **statement**: If you’re interested, please fill out our sign-up form.
- **kind**: PROCEDURE
- **value**: our sign-up form
- **unit**: DIMENSIONLESS
- **conditions**: If you’re interested
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0016

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", "Sign-up" paragraph, second sentence
- **excerpt**: "We’ll send updates about the tapeout template, deadlines, as well as providing the final submission link."
- **statement**: We’ll send updates about the tapeout template, deadlines, as well as providing the final submission link.
- **kind**: QUAL
- **value**: the tapeout template, deadlines, as well as providing the final submission link
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: ’ll
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0017

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", "Sign-up" paragraph, third (final) sentence
- **excerpt**: "Note that filling out the form is not a commitment to participating, it’s just to receive updates!"
- **statement**: Note that filling out the form is not a commitment to participating, it’s [filling out the form] just to receive updates!
- **kind**: QUAL
- **value**: not a commitment to participating
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the pronoun "it’s" is resolved with wording taken verbatim from the same sentence; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0018

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", final paragraph before the "Hardware at Jane Street" heading; the address is a mailto: link
- **excerpt**: "If you have questions along the way, reach out to asic-competition@janestreet.com."
- **statement**: If you have questions along the way, reach out to asic-competition@janestreet.com.
- **kind**: PROCEDURE
- **value**: asic-competition@janestreet.com
- **unit**: DIMENSIONLESS
- **conditions**: If you have questions along the way
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0019

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "time zone" (0 hits); variants also searched case-insensitively with no time-of-day or time-zone statement found: "timezone", "UTC", "GMT", "AoE", "anywhere on earth", "Anywhere", "EST" and "ET" (whose only matches fall inside ordinary words such as "interested" and "test"), "11:59", "midnight", "a.m.", "p.m."
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "time zone"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0020

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "hard deadline" (0 hits); variants also searched case-insensitively with no match: "extension", "no extensions", "firm", "late", "strict"; the bare token "hard" occurs only in "The hard part is flexibility.", "Hardware", "hardware" and "Hardcaml"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "hard deadline"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-SCHEDULE, CHALLENGE-DELIVERABLE
- **rq_ids**: RQ-01
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F12

### CLM-0021

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 6 of 6, bold label "Prize:", first sentence
- **excerpt**: "We’ll pay to tape out the most novel designs on a Tiny Tapeout shuttle."
- **statement**: We’ll pay to tape out the most novel designs on a Tiny Tapeout shuttle.
- **kind**: QUAL
- **value**: the most novel designs
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: ’ll
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; "the most novel" is the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0022

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, second introductory paragraph (before the "The challenge" heading), first sentence, second clause
- **excerpt**: "and we’ll pay to fabricate our favorite designs!"
- **statement**: we’ll pay to fabricate our favorite designs!
- **kind**: QUAL
- **value**: pay to fabricate our favorite designs
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: ’ll
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; "our favorite" is the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O2 only (seq 48). O1 extracted the "Prize:" wording of the same undertaking (paired at 49) and the adjacent introductory sentence about what interests the judges (paired at 51), but not this clause, although it applied exactly the two-printings treatment to the F14 pair.
- **re-enters bootstrap entry**: F13

### CLM-0023

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, second introductory paragraph (before the "The challenge" heading), second sentence
- **excerpt**: "We’re particularly interested in projects with unique functionality, as well as those that demonstrate novel approaches to design and verification methodologies!"
- **statement**: We’re particularly interested in projects with unique functionality, as well as those [projects] that demonstrate novel approaches to design and verification methodologies!
- **kind**: QUAL
- **value**: projects with unique functionality; projects that demonstrate novel approaches to design and verification methodologies
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the anaphor "those" is resolved with wording taken verbatim from the same sentence; "particularly interested", "unique" and "novel" are the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0024

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "rubric" (0 hits); variants also searched case-insensitively with no match: "criteria", "criterion", "scoring", "score", "evaluation"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "rubric"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0025

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "weight" (0 hits); variants also searched case-insensitively with no match: "weights", "weighted", "percent of the score", "points"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "weight"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0026

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "jury" (0 hits); variants also searched case-insensitively with no match: "judge", "judges", "judging", "panel", "reviewers"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "jury"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0027

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "number of winners" (0 hits); "winner" occurs only twice, both as the bare plural "Winners" with no numeral attached; variants also searched case-insensitively with no match: "how many", "up to", "one winner", "first place"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "number of winners"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F13

### CLM-0028

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, second introductory paragraph (before the "The challenge" heading), third (final) sentence
- **excerpt**: "Winners will receive a fabricated copy of their chip, mounted on a dev boards, so they can test their design in real silicon."
- **statement**: Winners will receive a fabricated copy of their chip, mounted on a dev boards, so they can test their design in real silicon.
- **kind**: QUAL
- **value**: a fabricated copy of their chip, mounted on a dev boards
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: will
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the number disagreement in "a dev boards" is as printed and is not corrected; the modal "can" sits in a subordinate purpose clause and so stays in the statement text while the modality field records only "will"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F14

### CLM-0029

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 6 of 6 ("Prize:"), third (final) sentence
- **excerpt**: "Winners will receive chips and dev boards back after fabrication, so you can test your design in silicon."
- **statement**: Winners will receive chips and dev boards back after fabrication, so you can test your design in silicon.
- **kind**: QUAL
- **value**: chips and dev boards
- **unit**: DIMENSIONLESS
- **conditions**: after fabrication
- **modality**: will
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; recorded separately from the introductory printing because the same element is printed differently in the two places; the source prints no unit for this value
- **subject_tags**: CHALLENGE-JUDGING
- **rq_ids**: RQ-03
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F14

### CLM-0030

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", paragraph following the bulleted list, first sentence; "Hardcaml" is hyperlinked to hardcaml.org
- **excerpt**: "At Jane Street, we use Hardcaml to generate the RTL for our FPGA and ASIC designs."
- **statement**: At Jane Street, we use Hardcaml to generate the RTL for our FPGA and ASIC designs.
- **kind**: QUAL
- **value**: Hardcaml
- **unit**: DIMENSIONLESS
- **conditions**: At Jane Street
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE, METHOD-VERIFICATION
- **rq_ids**: RQ-08
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F15

### CLM-0031

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", paragraph following the bulleted list, second sentence
- **excerpt**: "We are excited to see the languages and verification techniques you use, including formal methods, random constrained tests, AI-assisted verification, and more."
- **statement**: We are excited to see the languages and verification techniques you use, including formal methods, random constrained tests, AI-assisted verification, and more.
- **kind**: QUAL
- **value**: formal methods, random constrained tests, AI-assisted verification, and more
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; "excited" is the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE, METHOD-VERIFICATION
- **rq_ids**: RQ-08
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F15

### CLM-0032

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", paragraph following the bulleted list, third (final) sentence
- **excerpt**: "As AI-assisted chip design becomes more common, we believe verification will be an extremely important aspect of the ASIC design flow going forwards."
- **statement**: As AI-assisted chip design becomes more common, we believe verification will be an extremely important aspect of the ASIC design flow going forwards.
- **kind**: QUAL
- **value**: an extremely important aspect of the ASIC design flow going forwards
- **unit**: DIMENSIONLESS
- **conditions**: As AI-assisted chip design becomes more common
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the modal "will" sits inside the complement clause of "we believe" rather than governing the main predicate, so the modality field reads NONE; "extremely important" is the source's own evaluative wording; the source prints no unit for this value
- **subject_tags**: CHALLENGE-RULE, METHOD-VERIFICATION
- **rq_ids**: RQ-08
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F15

### CLM-0033

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "not required" (0 hits); variants also searched case-insensitively with no match: "required", "require", "optional", "any language", "need not", "mandatory"; "Hardcaml" occurs twice, in the paragraph following the protocol bullet list and in the "Hardware at Jane Street" section
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "not required"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-RULE, METHOD-VERIFICATION
- **rq_ids**: RQ-08
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F15

### CLM-0034

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", second paragraph, first sentence
- **excerpt**: "For instruction memory, SRAM can be more area-efficient than flip-flops."
- **statement**: For instruction memory, SRAM can be more area-efficient than flip-flops.
- **kind**: QUAL
- **value**: more area-efficient than flip-flops
- **unit**: DIMENSIONLESS
- **conditions**: For instruction memory
- **modality**: can
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0035

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", second paragraph, second (final) sentence; "examples of SRAM" is hyperlinked to tinytapeout.com/chips/ttihp0p2/tt_um_urish_sram_test
- **excerpt**: "Tiny Tapeout has examples of SRAM running on this process node you can reference."
- **statement**: Tiny Tapeout has examples of SRAM running on this process node [IHP’s 130nm CMOS5L process] you can reference.
- **kind**: QUAL
- **value**: examples of SRAM running on this process node
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the deixis "this process node" is resolved with wording taken verbatim from the "Process:" rule of the same article; the modal "can" sits in a relative clause and so stays in the statement text while the modality field reads NONE; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0036

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, first sentence, first of three coordinated imperatives
- **excerpt**: "Run synthesis early, check the mapped cell area, and leave room for clock-tree buffers and routing."
- **statement**: Run synthesis early.
- **kind**: PROCEDURE
- **value**: NOT APPLICABLE
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperatives retrieved verbatim from the raw HTML; the source prints the compound as "clock-tree buffers" with a hyphen; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0037

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, first sentence, second of three coordinated imperatives
- **excerpt**: "Run synthesis early, check the mapped cell area, and leave room for clock-tree buffers and routing."
- **statement**: Check the mapped cell area.
- **kind**: PROCEDURE
- **value**: the mapped cell area
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 only (seq 62). O2 folded this predicate into its single claim for the whole sentence (seq 62) rather than omitting the material.
- **re-enters bootstrap entry**: F16

### CLM-0038

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, first sentence, third of three coordinated imperatives
- **excerpt**: "Run synthesis early, check the mapped cell area, and leave room for clock-tree buffers and routing."
- **statement**: Leave room for clock-tree buffers and routing.
- **kind**: PROCEDURE
- **value**: clock-tree buffers and routing
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints the compound as "clock-tree buffers" with a hyphen; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 only (seq 63). O2 folded this predicate into its single claim for the whole sentence (seq 62). Both operators record the hyphenated "clock-tree buffers" as printed.
- **re-enters bootstrap entry**: F16

### CLM-0039

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, second sentence, first of two coordinated imperatives
- **excerpt**: "Then run the full place-and-route flow and check timing."
- **statement**: Then run the full place-and-route flow.
- **kind**: PROCEDURE
- **value**: the full place-and-route flow
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperatives retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0040

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, second sentence, second of two coordinated imperatives
- **excerpt**: "Then run the full place-and-route flow and check timing."
- **statement**: Check timing.
- **kind**: PROCEDURE
- **value**: timing
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 only (seq 65). O2 folded this predicate into its single claim for the sentence (seq 63).
- **re-enters bootstrap entry**: F16

### CLM-0041

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", third paragraph, third (final) sentence
- **excerpt**: "A design that looks small enough after synthesis can still be difficult to route or too slow at your chosen clock frequency."
- **statement**: A design that looks small enough after synthesis can still be difficult to route or too slow at your chosen clock frequency.
- **kind**: QUAL
- **value**: difficult to route or too slow
- **unit**: DIMENSIONLESS
- **conditions**: after synthesis; at your chosen clock frequency
- **modality**: can
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0042

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 4 of 5
- **excerpt**: "If you have access to an FPGA, consider using it to test your RTL before the ASIC flow."
- **statement**: If you have access to an FPGA, consider using it [an FPGA] to test your RTL before the ASIC flow.
- **kind**: PROCEDURE
- **value**: using it to test your RTL before the ASIC flow
- **unit**: DIMENSIONLESS
- **conditions**: If you have access to an FPGA; before the ASIC flow
- **modality**: NONE
- **reading_confidence**: high; printed imperative bullet retrieved verbatim from the raw HTML; the pronoun "it" is resolved with wording taken verbatim from the same list item; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0043

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", first paragraph, first sentence, first clause; "Tiny Tapeout documentation" is hyperlinked to tinytapeout.com
- **excerpt**: "If you’ve never taped out a chip before, the Tiny Tapeout documentation walks through the process end to end"
- **statement**: If you’ve never taped out a chip before, the Tiny Tapeout documentation walks through the process end to end
- **kind**: QUAL
- **value**: walks through the process end to end
- **unit**: DIMENSIONLESS
- **conditions**: If you’ve never taped out a chip before
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0044

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", first paragraph, first sentence, final clause, printed after the coordinator "and"
- **excerpt**: "and the tools are all free and open source."
- **statement**: the tools are all free and open source.
- **kind**: QUAL
- **value**: all free and open source
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0045

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", first paragraph, second sentence
- **excerpt**: "Start by getting a UART transmitter out of a pin."
- **statement**: Start by getting a UART transmitter out of a pin.
- **kind**: PROCEDURE
- **value**: a UART transmitter out of a pin
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0046

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "Getting started", first paragraph, third (final) sentence
- **excerpt**: "Then make it programmable."
- **statement**: Then make it [a UART transmitter] programmable.
- **kind**: PROCEDURE
- **value**: programmable
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the pronoun "it" is resolved with wording taken verbatim from the preceding sentence of the same paragraph; the source prints no unit for this value
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0047

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "binding" (0 hits); variants also searched case-insensitively with no match: "must", "required", "mandatory", "you have to", "obligatory"; the only directive language the page prints nearby is "we strongly recommend" in the "Teams:" bullet
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "binding"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: CHALLENGE-ADVICE
- **rq_ids**: RQ-23
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F16

### CLM-0048

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", first paragraph; "open-source, general-purpose protocol emulator ASIC" printed in bold (<strong>)
- **excerpt**: "Design an open-source, general-purpose protocol emulator ASIC."
- **statement**: Design an open-source, general-purpose protocol emulator ASIC.
- **kind**: PROCEDURE
- **value**: open-source, general-purpose protocol emulator ASIC
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F2

### CLM-0049

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", second paragraph, first sentence
- **excerpt**: "Hardware protocols like UART, SPI, and I2C are simple enough that people routinely “bit-bang” them: toggle pins from software with careful timing instead of using a dedicated peripheral."
- **statement**: Hardware protocols like UART, SPI, and I2C are simple enough that people routinely “bit-bang” them [Hardware protocols like UART, SPI, and I2C]: toggle pins from software with careful timing instead of using a dedicated peripheral.
- **kind**: QUAL
- **value**: simple enough that people routinely “bit-bang” them
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source uses curly quotation marks around “bit-bang”; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F3

### CLM-0050

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", second paragraph, second sentence
- **excerpt**: "A protocol emulator is a small chip built to do exactly that: a tiny CPU with an instruction set designed for reading pins, writing pins, counting cycles, and hitting timing precisely enough that you can implement a real protocol in firmware rather than in fixed logic."
- **statement**: A protocol emulator is a small chip built to do exactly that [toggle pins from software with careful timing instead of using a dedicated peripheral]: a tiny CPU with an instruction set designed for reading pins, writing pins, counting cycles, and hitting timing precisely enough that you can implement a real protocol in firmware rather than in fixed logic.
- **kind**: DEFINITION
- **value**: a small chip built to do exactly that: a tiny CPU with an instruction set designed for reading pins, writing pins, counting cycles, and hitting timing precisely enough that you can implement a real protocol in firmware rather than in fixed logic
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F3

### CLM-0051

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", second paragraph, third sentence
- **excerpt**: "Something like that is a useful tool for hardware debugging and reverse engineering, which is a good part of what we do."
- **statement**: Something like that [A protocol emulator] is a useful tool for hardware debugging and reverse engineering, which is a good part of what we do.
- **kind**: QUAL
- **value**: a useful tool for hardware debugging and reverse engineering
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; "useful" and "a good part" are the source's own evaluative wording, reproduced verbatim; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F3

### CLM-0052

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", third paragraph, first sentence
- **excerpt**: "The hard part is flexibility."
- **statement**: The hard part is flexibility.
- **kind**: DEFINITION
- **value**: flexibility
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F4

### CLM-0053

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", third paragraph, second sentence
- **excerpt**: "The goal isn’t to put a UART block, an SPI block, and an I2C block on one die and call it done."
- **statement**: The goal isn’t to put a UART block, an SPI block, and an I2C block on one die and call it [a UART block, an SPI block, and an I2C block on one die] done.
- **kind**: QUAL
- **value**: isn’t to put a UART block, an SPI block, and an I2C block on one die and call it done
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source uses a curly apostrophe in "isn’t"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F4

### CLM-0054

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", third paragraph, third sentence; the word "after" printed in italics (<em>)
- **excerpt**: "Your chip should be reprogrammable enough to support new protocols after fabrication, within its timing and I/O constraints."
- **statement**: Your chip should be reprogrammable enough to support new protocols after fabrication, within its [Your chip] timing and I/O constraints.
- **kind**: RULE
- **value**: reprogrammable enough to support new protocols after fabrication
- **unit**: DIMENSIONLESS
- **conditions**: after fabrication; within its timing and I/O constraints
- **modality**: should
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the italic emphasis on "after" is not reproducible in plain text; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F4

### CLM-0055

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", third paragraph, fourth sentence
- **excerpt**: "For inspiration, look at the PIO state machines on the RP2040 or the PRU cores on TI’s Sitara parts, and consider what you’d do differently."
- **statement**: For inspiration, look at the PIO state machines on the RP2040 or the PRU cores on TI’s Sitara parts, and consider what you’d do differently.
- **kind**: PROCEDURE
- **value**: the PIO state machines on the RP2040 or the PRU cores on TI’s Sitara parts
- **unit**: DIMENSIONLESS
- **conditions**: For inspiration
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source uses curly apostrophes in "TI’s" and "you’d"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 only (seq 12). O2 produced no claim for this sentence anywhere in its output, although it extracted the sentence before it and the bullet list after it.
- **re-enters bootstrap entry**: F4

### CLM-0056

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 1 of 5
- **excerpt**: "Start with UART, SPI, and I2C."
- **statement**: Start with UART, SPI, and I2C.
- **kind**: PROCEDURE
- **value**: UART, SPI, and I2C
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative bullet retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE, PROTOCOL
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F5

### CLM-0057

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 2 of 5
- **excerpt**: "Stretch goals include low-speed USB and 10Mbit Ethernet."
- **statement**: Stretch goals include low-speed USB and 10Mbit Ethernet.
- **kind**: QUANT
- **value**: low-speed USB; 10Mbit Ethernet
- **unit**: Mbit
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed bullet retrieved verbatim from the raw HTML; the printed unit symbol "Mbit" appears only in "10Mbit Ethernet" and is reproduced without spacing as printed
- **subject_tags**: CHALLENGE-SCOPE, PROTOCOL
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F5

### CLM-0058

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 3 of 5; printed with no terminating full stop
- **excerpt**: "Other interesting protocols to consider: JTAG, SWD, PS/2, CAN bus"
- **statement**: Other interesting protocols to consider: JTAG, SWD, PS/2, CAN bus
- **kind**: QUAL
- **value**: JTAG, SWD, PS/2, CAN bus
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed bullet retrieved verbatim from the raw HTML; "interesting" is the source's own evaluative wording; the bullet prints no terminating full stop; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE, PROTOCOL
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F5

### CLM-0059

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 4 of 5
- **excerpt**: "If you have access to an FPGA, consider using it to test your RTL before the ASIC flow."
- **statement**: If you have access to an FPGA, consider using it [an FPGA] to test your RTL before the ASIC flow.
- **kind**: PROCEDURE
- **value**: using it to test your RTL before the ASIC flow
- **unit**: DIMENSIONLESS
- **conditions**: If you have access to an FPGA; before the ASIC flow
- **modality**: NONE
- **reading_confidence**: high; printed imperative bullet retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE, PROTOCOL
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O1 recorded this one span twice, under F5 (seq 16) and again under F16 (seq 67, paired at pair 70); O2 recorded it once, under F16 (seq 65). This entry is O1's second, unmatched copy under F5.
- **re-enters bootstrap entry**: F5

### CLM-0060

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The challenge", bulleted list, bullet 5 of 5 (final bullet)
- **excerpt**: "Show us anything else your architecture makes possible that we haven’t thought of."
- **statement**: Show us anything else your architecture makes possible that we haven’t thought of.
- **kind**: PROCEDURE
- **value**: anything else your architecture makes possible that we haven’t thought of
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative bullet retrieved verbatim from the raw HTML; the source uses a curly apostrophe in "haven’t"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCOPE, PROTOCOL
- **rq_ids**: RQ-02
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F5

### CLM-0061

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 1 of 6, bold label "Process:", first sentence; "Tiny Tapeout" is hyperlinked
- **excerpt**: "We’re targeting IHP’s 130nm CMOS5L process through our friends at Tiny Tapeout."
- **statement**: We’re targeting IHP’s 130nm CMOS5L process through our friends at Tiny Tapeout.
- **kind**: QUANT
- **value**: 130
- **unit**: nm
- **conditions**: NOT STATED
- **modality**: ’re targeting
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the printed value and unit are run together as "130nm"
- **subject_tags**: CHALLENGE-SCHEDULE, TECH-PROCESS, SHUTTLE
- **rq_ids**: RQ-05, RQ-07
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F6

### CLM-0062

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 6 of 6, bold label "Prize:", second sentence; "March 2027 CMOS5L shuttle" printed in bold
- **excerpt**: "We’re targeting the March 2027 CMOS5L shuttle, subject to the foundry schedule."
- **statement**: We’re targeting the March 2027 CMOS5L shuttle, subject to the foundry schedule.
- **kind**: QUANT
- **value**: 2027-03
- **unit**: DIMENSIONLESS
- **conditions**: subject to the foundry schedule
- **modality**: ’re targeting
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the source prints the month as "March 2027"; the source prints no unit for this value
- **subject_tags**: CHALLENGE-SCHEDULE, TECH-PROCESS, SHUTTLE
- **rq_ids**: RQ-05, RQ-07
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F6

### CLM-0063

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 1 of 6 ("Process:"), second sentence; "CMOS5L Verilog template" is hyperlinked to github.com/TinyTapeout/ttihp-verilog-template/tree/cmos5l
- **excerpt**: "Start with the CMOS5L Verilog template, which takes you from RTL to GDS."
- **statement**: Start with the CMOS5L Verilog template, which takes you from RTL to GDS.
- **kind**: PROCEDURE
- **value**: the CMOS5L Verilog template
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative in a rule bullet retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: TECH-FLOW, TECH-TILE
- **rq_ids**: RQ-01, RQ-05
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F7

### CLM-0064

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 1 of 6 ("Process:"), third sentence; "info.yaml" printed in inline code markup
- **excerpt**: "Set the tile size in info.yaml to 6x4."
- **statement**: Set the tile size in info.yaml to 6x4.
- **kind**: PROCEDURE
- **value**: 6x4
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed imperative in a rule bullet retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: TECH-FLOW, TECH-TILE
- **rq_ids**: RQ-01, RQ-05
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F7

### CLM-0065

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "mandatory" (0 hits); variants also searched case-insensitively with no match: "required", "require", "requirement", "must", "obligator"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "mandatory"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: TECH-FLOW, TECH-TILE
- **rq_ids**: RQ-01, RQ-05
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F7

### CLM-0066

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 2 of 6, bold label "Area:", first sentence
- **excerpt**: "The current maximum area is 6x4 tiles per design."
- **statement**: The current maximum area is 6x4 tiles per design.
- **kind**: QUANT
- **value**: 6x4
- **unit**: tiles per design
- **conditions**: current
- **modality**: NONE
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the printed unit is "tiles per design"
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F8

### CLM-0067

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 2 of 6 ("Area:"), second sentence; printed in bold (<strong>)
- **excerpt**: "We are working on the possibility of scaling up to 8x4 tiles (~30% more area)."
- **statement**: We are working on the possibility of scaling up to 8x4 tiles (~30% more area).
- **kind**: QUANT
- **value**: 8x4
- **unit**: tiles
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the printed precision qualifier "~" is retained on "~30% more area"; the printed unit for the value is "tiles"
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F8

### CLM-0068

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "The rules", bullet 2 of 6 ("Area:"), third sentence; printed in bold, with "signed up" hyperlinked to the Google Forms sign-up form
- **excerpt**: "We’ll update this page, as well as emailing everyone who has signed up if the larger tile size becomes available."
- **statement**: We’ll update this page [Can you design a chip? Announcing the protocol emulator ASIC competition], as well as emailing everyone who has signed up if the larger tile size becomes available.
- **kind**: QUAL
- **value**: update this page, as well as emailing everyone who has signed up
- **unit**: DIMENSIONLESS
- **conditions**: if the larger tile size becomes available
- **modality**: ’ll
- **reading_confidence**: high; printed rule bullet retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: SINGLE OPERATOR: only one operator recorded this span; it has not been independently confirmed
- **caveats**: O2 only (seq 24). O1 extracted the first and second sentences of the "Area:" bullet but not the third.
- **re-enters bootstrap entry**: F8

### CLM-0069

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", first paragraph, first sentence
- **excerpt**: "An 6x4 allocation is 24 tiles."
- **statement**: An 6x4 allocation is 24 tiles.
- **kind**: QUANT
- **value**: 24
- **unit**: tiles
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the article prints the determiner as "An 6x4" and it is reproduced as printed
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED: both operators produced the same statement after normalization
- **caveats**: NONE
- **re-enters bootstrap entry**: F8

### CLM-0070

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", first paragraph, second sentence, opening prepositional phrase
- **excerpt**: "At approximately 200um × 150um per tile"
- **statement**: A tile is approximately 200um × 150um.
- **kind**: QUANT
- **value**: approximately 200um × 150um
- **unit**: um
- **conditions**: per tile
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the printed precision qualifier "approximately" is retained; the source prints the unit as "um" and the multiplication sign as "×"
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F8

### CLM-0071

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", first paragraph, second sentence
- **excerpt**: "At approximately 200um × 150um per tile, that’s about 0.7 mm² of nominal tile area."
- **statement**: At approximately 200um × 150um per tile, that’s [24 tiles] about 0.7 mm² of nominal tile area.
- **kind**: QUANT
- **value**: about 0.7
- **unit**: mm²
- **conditions**: At approximately 200um × 150um per tile
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the printed precision qualifiers "about" and "approximately" are retained
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F8

### CLM-0072

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", first paragraph, third sentence
- **excerpt**: "As a rough estimate, budget for about 1K logic cells per tile."
- **statement**: As a rough estimate, budget for about 1K logic cells per tile.
- **kind**: PROCEDURE
- **value**: about 1K
- **unit**: logic cells per tile
- **conditions**: As a rough estimate
- **modality**: NONE
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the printed precision qualifiers "rough" and "about" are retained; the printed magnitude is "1K"
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F9

### CLM-0073

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Post body, section "How much fits?", first paragraph, fourth (final) sentence
- **excerpt**: "You may need to get creative to fit the functionality you want."
- **statement**: You may need to get creative to fit the functionality you want.
- **kind**: QUAL
- **value**: need to get creative
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **modality**: may
- **reading_confidence**: high; running prose retrieved verbatim from the raw HTML; the source prints no unit for this value
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F9

### CLM-0074

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "cell library" (0 hits); variants also searched case-insensitively with no match: "standard cell", "sky130", "sg13", "SG13G2", "library"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "cell library"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F9

### CLM-0075

- **source_id**: SRC-0004 (ORG-BLOG)
- **locator**: Case-insensitive substring search over the full verbatim page text (HTML tags stripped) for "utilization" (0 hits); variants also searched case-insensitively with no match: "utilisation", "density"
- **excerpt**: "" (the operators recorded no excerpt for this span)
- **statement**: The ORG-BLOG does not contain "utilization"
- **kind**: ABSENCE
- **value**: 0
- **unit**: occurrences
- **conditions**: NOT STATED
- **modality**: NONE
- **reading_confidence**: high; determined by case-insensitive substring search over the verbatim retrieved page source
- **subject_tags**: TECH-TILE
- **rq_ids**: RQ-04
- **source_version**: see SRC-0004
- **extracted_by**: OP-EXT-1 and OP-EXT-2, independently; paired by OP-REC
- **extracted_on**: 2026-09-17
- **double_extraction**: AGREED ON CONTENT: both operators read the source the same way; their statements differed in rendering and the reconciler recorded the common reading
- **caveats**: NONE
- **re-enters bootstrap entry**: F9
