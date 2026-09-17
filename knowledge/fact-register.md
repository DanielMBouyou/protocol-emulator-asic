# Fact register

Register `FCT-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). What a FACT requires, its status labels and its lifecycle states are canonical in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#fact). Record format per [DEC-0004](decision-log.md#dec-0004-s00-d4-register-format-storage-and-primary-document-store).

## What is here, and what is not

No record below is CANONICAL.

Promotion to CANONICAL requires, among other things, that a second operator who did not extract the claim re-read the source location and check each promotion item, and that the atomic fact rule be satisfied. Gate G00 tests whether two independent extractions agree, and it did not pass: see [gate-g00.md](gate-g00.md). Promoting these records while that condition is open would assert exactly the thing the gate failed to establish, so they stay PROPOSED and the [constraints register](../PROJECT_SCOPE.md#challenge-constraints-as-currently-known) remains the project's working statement of what is known.

A fact whose bootstrap entry is one of the conflicting tile descriptions carries lifecycle state CONTESTED, because [CTR-0001](contradiction-register.md#ctr-0001-tile-dimensions-and-valid-tile-sizes-for-cmos5l) references it. Its status label is still one of the three the evidence policy defines, since CONTESTED is a lifecycle state and not a status label.

A claim becomes a candidate fact here only when two operators independently confirmed the same reading of the span, that is when its `double_extraction` field reads AGREED or AGREED ON CONTENT. Claims recorded by a single operator, and claims where the two operators reported the source differently, are in the [claim register](claim-register.md) and are not proposed as facts.

What the confirmation is worth is bounded by [LIM-0001](limitation-register.md#lim-0001-correlated-error-between-automated-extraction-operators).


### FCT-0001

- **statement**: title is set to "Jane Street Blog - Can you design a chip? Announcing the protocol emulator ASIC competition "
- **kind**: DEFINITION
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0002
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F1

### FCT-0002

- **statement**: The post is dated "Sep 10, 2026".
- **kind**: QUANT
- **value**: 2026-09-10
- **unit**: DIMENSIONLESS
- **conditions**: NOT STATED
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0004
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F1

### FCT-0003

- **statement**: The post's byline states "By: Benjamin Devlin" and "By: Anish Singhani", in that printed order
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0005
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F1

### FCT-0004

- **statement**: Your submission should be open source so others can use and build on it [Your submission].
- **kind**: RULE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0006
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F10

### FCT-0005

- **statement**: The ORG-BLOG does not contain "license"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0007
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F10

### FCT-0006

- **statement**: Unlike the reverse-engineering puzzle, there’s no need to keep your work hidden until the deadline
- **kind**: RULE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0008
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F11

### FCT-0007

- **statement**: feel free to build in public!
- **kind**: RULE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0009
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F11

### FCT-0008

- **statement**: This [Design an open-source, general-purpose protocol emulator ASIC] is a much bigger project than the puzzle [the reverse-engineering puzzle]
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0010
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F11

### FCT-0009

- **statement**: we strongly recommend working in teams.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0011
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F11

### FCT-0010

- **statement**: The ORG-BLOG does not contain "team size"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0012
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F11

### FCT-0011

- **statement**: Submit your design by January 18th, 2027.
- **kind**: PROCEDURE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0013
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0012

- **statement**: We’ll add a final submission form to this page [Can you design a chip? Announcing the protocol emulator ASIC competition] closer to the deadline!
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0014
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0013

- **statement**: If you’re interested, please fill out our sign-up form.
- **kind**: PROCEDURE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0015
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0014

- **statement**: We’ll send updates about the tapeout template, deadlines, as well as providing the final submission link.
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0016
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0015

- **statement**: Note that filling out the form is not a commitment to participating, it’s [filling out the form] just to receive updates!
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0017
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0016

- **statement**: If you have questions along the way, reach out to asic-competition@janestreet.com.
- **kind**: PROCEDURE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0018
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0017

- **statement**: The ORG-BLOG does not contain "time zone"
- **kind**: ABSENCE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0019
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0018

- **statement**: The ORG-BLOG does not contain "hard deadline"
- **kind**: ABSENCE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0020
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F12

### FCT-0019

- **statement**: We’ll pay to tape out the most novel designs on a Tiny Tapeout shuttle.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0021
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0020

- **statement**: We’re particularly interested in projects with unique functionality, as well as those [projects] that demonstrate novel approaches to design and verification methodologies!
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0023
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0021

- **statement**: The ORG-BLOG does not contain "rubric"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0024
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0022

- **statement**: The ORG-BLOG does not contain "weight"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0025
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0023

- **statement**: The ORG-BLOG does not contain "jury"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0026
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0024

- **statement**: The ORG-BLOG does not contain "number of winners"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0027
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F13

### FCT-0025

- **statement**: Winners will receive a fabricated copy of their chip, mounted on a dev boards, so they can test their design in real silicon.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0028
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F14

### FCT-0026

- **statement**: Winners will receive chips and dev boards back after fabrication, so you can test your design in silicon.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0029
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F14

### FCT-0027

- **statement**: At Jane Street, we use Hardcaml to generate the RTL for our FPGA and ASIC designs.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0030
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F15

### FCT-0028

- **statement**: We are excited to see the languages and verification techniques you use, including formal methods, random constrained tests, AI-assisted verification, and more.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0031
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F15

### FCT-0029

- **statement**: As AI-assisted chip design becomes more common, we believe verification will be an extremely important aspect of the ASIC design flow going forwards.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0032
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F15

### FCT-0030

- **statement**: The ORG-BLOG does not contain "not required"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0033
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F15

### FCT-0031

- **statement**: For instruction memory, SRAM can be more area-efficient than flip-flops.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0034
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0032

- **statement**: Tiny Tapeout has examples of SRAM running on this process node [IHP’s 130nm CMOS5L process] you can reference.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0035
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0033

- **statement**: Run synthesis early.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0036
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0034

- **statement**: Then run the full place-and-route flow.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0039
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0035

- **statement**: A design that looks small enough after synthesis can still be difficult to route or too slow at your chosen clock frequency.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0041
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0036

- **statement**: If you have access to an FPGA, consider using it [an FPGA] to test your RTL before the ASIC flow.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0042
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0037

- **statement**: If you’ve never taped out a chip before, the Tiny Tapeout documentation walks through the process end to end
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0043
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0038

- **statement**: the tools are all free and open source.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0044
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0039

- **statement**: Start by getting a UART transmitter out of a pin.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0045
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0040

- **statement**: Then make it [a UART transmitter] programmable.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0046
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0041

- **statement**: The ORG-BLOG does not contain "binding"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT (statements the page prints as guidance; it nowhere prints that they are binding)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0047
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F16

### FCT-0042

- **statement**: Design an open-source, general-purpose protocol emulator ASIC.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0048
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F2

### FCT-0043

- **statement**: Hardware protocols like UART, SPI, and I2C are simple enough that people routinely “bit-bang” them [Hardware protocols like UART, SPI, and I2C]: toggle pins from software with careful timing instead of using a dedicated peripheral.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0049
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F3

### FCT-0044

- **statement**: A protocol emulator is a small chip built to do exactly that [toggle pins from software with careful timing instead of using a dedicated peripheral]: a tiny CPU with an instruction set designed for reading pins, writing pins, counting cycles, and hitting timing precisely enough that you can implement a real protocol in firmware rather than in fixed logic.
- **kind**: DEFINITION
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0050
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F3

### FCT-0045

- **statement**: Something like that [A protocol emulator] is a useful tool for hardware debugging and reverse engineering, which is a good part of what we do.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0051
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F3

### FCT-0046

- **statement**: The hard part is flexibility.
- **kind**: DEFINITION
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0052
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F4

### FCT-0047

- **statement**: The goal isn’t to put a UART block, an SPI block, and an I2C block on one die and call it [a UART block, an SPI block, and an I2C block on one die] done.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0053
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F4

### FCT-0048

- **statement**: Your chip should be reprogrammable enough to support new protocols after fabrication, within its [Your chip] timing and I/O constraints.
- **kind**: RULE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0054
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F4

### FCT-0049

- **statement**: Start with UART, SPI, and I2C.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0056
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F5

### FCT-0050

- **statement**: Stretch goals include low-speed USB and 10Mbit Ethernet.
- **kind**: QUANT
- **value**: low-speed USB; 10Mbit Ethernet
- **unit**: Mbit
- **conditions**: NOT STATED
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0057
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F5

### FCT-0051

- **statement**: Other interesting protocols to consider: JTAG, SWD, PS/2, CAN bus
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0058
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F5

### FCT-0052

- **statement**: Show us anything else your architecture makes possible that we haven’t thought of.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0060
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F5

### FCT-0053

- **statement**: We’re targeting IHP’s 130nm CMOS5L process through our friends at Tiny Tapeout.
- **kind**: QUANT
- **value**: 130
- **unit**: nm
- **conditions**: NOT STATED
- **status label**: CONFIRMED_FACT and MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0061
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F6

### FCT-0054

- **statement**: We’re targeting the March 2027 CMOS5L shuttle, subject to the foundry schedule.
- **kind**: QUANT
- **value**: 2027-03
- **unit**: DIMENSIONLESS
- **conditions**: subject to the foundry schedule
- **status label**: CONFIRMED_FACT and MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0062
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F6

### FCT-0055

- **statement**: Start with the CMOS5L Verilog template, which takes you from RTL to GDS.
- **kind**: PROCEDURE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0063
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F7

### FCT-0056

- **statement**: Set the tile size in info.yaml to 6x4.
- **kind**: PROCEDURE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0064
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F7

### FCT-0057

- **statement**: The ORG-BLOG does not contain "mandatory"
- **kind**: ABSENCE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0065
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F7

### FCT-0058

- **statement**: The current maximum area is 6x4 tiles per design.
- **kind**: QUANT
- **value**: 6x4
- **unit**: tiles per design
- **conditions**: current
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0066
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F8

### FCT-0059

- **statement**: We are working on the possibility of scaling up to 8x4 tiles (~30% more area).
- **kind**: QUANT
- **value**: 8x4
- **unit**: tiles
- **conditions**: NOT STATED
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0067
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F8

### FCT-0060

- **statement**: An 6x4 allocation is 24 tiles.
- **kind**: QUANT
- **value**: 24
- **unit**: tiles
- **conditions**: NOT STATED
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0069
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F8

### FCT-0061

- **statement**: A tile is approximately 200um × 150um.
- **kind**: QUANT
- **value**: approximately 200um × 150um
- **unit**: um
- **conditions**: per tile
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0070
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F8

### FCT-0062

- **statement**: At approximately 200um × 150um per tile, that’s [24 tiles] about 0.7 mm² of nominal tile area.
- **kind**: QUANT
- **value**: about 0.7
- **unit**: mm²
- **conditions**: At approximately 200um × 150um per tile
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0071
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F8

### FCT-0063

- **statement**: As a rough estimate, budget for about 1K logic cells per tile.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT (organizer's rough estimate)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0072
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F9

### FCT-0064

- **statement**: You may need to get creative to fit the functionality you want.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT (organizer's rough estimate)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0073
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F9

### FCT-0065

- **statement**: The ORG-BLOG does not contain "cell library"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT (organizer's rough estimate)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0074
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F9

### FCT-0066

- **statement**: The ORG-BLOG does not contain "utilization"
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT (organizer's rough estimate)
- **lifecycle state**: PROPOSED
- **claims**: CLM-0075
- **sources**: SRC-0004
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: F9

### FCT-0067

- **statement**: A single tile is about 167x108 uM
- **kind**: QUANT
- **value**: about 167x108
- **unit**: uM
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0077
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-A

### FCT-0068

- **statement**: tiles is set to "1x1"
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0078
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-A

### FCT-0069

- **statement**: Valid values for tiles are 1x1, 1x2, 2x2, 3x2, 4x2, 6x2 or 8x2
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0079
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-A

### FCT-0070

- **statement**: 1x1 is set to "0 0 202.08 154.98"
- **kind**: QUANT
- **value**: 0 0 202.08 154.98
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0080
- **sources**: SRC-0013
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-C

### FCT-0071

- **statement**: 6x4 is set to "0 0 1289.28 710.64"
- **kind**: QUANT
- **value**: 0 0 1289.28 710.64
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0081
- **sources**: SRC-0013
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-C

### FCT-0072

- **statement**: The tile_sizes.yaml does not contain 8x4
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: CONTESTED
- **claims**: CLM-0082
- **sources**: SRC-0013
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: CTR-0001
- **re-enters bootstrap entry**: CTR-01-C

### FCT-0073

- **statement**: IHP has several variations of SRAM macros which can be used in shuttles which they [IHP] will manufacture (i.e. specifically being taped out with their PDK)
- **kind**: QUAL
- **status label**: OPEN_QUESTION
- **lifecycle state**: PROPOSED
- **claims**: CLM-0084
- **sources**: SRC-0011
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I5-SUPPORT

### FCT-0074

- **statement**: For SkyWater shuttles, the density of memory macros is significantly lower
- **kind**: QUAL
- **status label**: OPEN_QUESTION
- **lifecycle state**: PROPOSED
- **claims**: CLM-0091
- **sources**: SRC-0011
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I5-SUPPORT

### FCT-0075

- **statement**: Leave unused pins blank.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0095
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0076

- **statement**: DO NOT delete or add any pins.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0096
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0077

- **statement**: This section [pinout] is for the datasheet/website.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0097
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0078

- **statement**: Use descriptive names (e.g., RX, TX, MOSI, SCL, SEG_A, etc.).
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0098
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0079

- **statement**: The info.yaml does not contain clk
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0103
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0080

- **statement**: The info.yaml does not contain rst_n
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0104
- **sources**: SRC-0009
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1

### FCT-0081

- **statement**: Internally, both the clk and rst_n pins are handled like any other input pins
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0112, CLM-0154
- **sources**: SRC-0005, SRC-0007
- **corroboration count**: 1. The supporting claims come from 2 documents, but both are published by Tiny Tapeout, so test 2 of the [independence tests](../EVIDENCE_POLICY.md#independence-of-sources) fails and the pairwise independent count is one.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1-GPIO, T3

### FCT-0082

- **statement**: For more information on the clk pin and input synchronization, see the Clock section.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0114
- **sources**: SRC-0007
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T1-GPIO

### FCT-0083

- **statement**: uses is set to "TinyTapeout/tt-gds-action@ihp-cmos5l"
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0115
- **sources**: SRC-0006
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T2

### FCT-0084

- **statement**: pdk is set to "ihp-sg13cmos5l"
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0120
- **sources**: SRC-0006
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T2

### FCT-0085

- **statement**: runs-on is set to "ubuntu-24.04"
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0121
- **sources**: SRC-0006
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T2

### FCT-0086

- **statement**: The gds.yaml does not contain LibreLane
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0122
- **sources**: SRC-0006
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T2

### FCT-0087

- **statement**: The gds.yaml does not contain OpenLane
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0123
- **sources**: SRC-0006
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T2

### FCT-0088

- **statement**: The chip uses the sky130_ef_io_gpiov2_pad macro for the I/O pads
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0130, CLM-0156
- **sources**: SRC-0005, SRC-0007
- **corroboration count**: 1. The supporting claims come from 2 documents, but both are published by Tiny Tapeout, so test 2 of the [independence tests](../EVIDENCE_POLICY.md#independence-of-sources) fails and the pairwise independent count is one.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0089

- **statement**: For SKY130 the IO pads themselves are rated to 66 MHz
- **kind**: QUANT
- **value**: 66
- **unit**: MHz
- **conditions**: For SKY130
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0140
- **sources**: SRC-0007
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0090

- **statement**: For SKY130 the official rating is 33 MHz
- **kind**: QUANT
- **value**: 33
- **unit**: MHz
- **conditions**: For SKY130
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0147
- **sources**: SRC-0007
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0091

- **statement**: We expect a latency (insertion delay) of up to 10 nanoseconds between the chip's I/O pad and your project's clock
- **kind**: QUANT
- **value**: up to 10
- **unit**: nanoseconds
- **conditions**: between the chip's I/O pad and your project's clock
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0155
- **sources**: SRC-0005
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0092

- **statement**: The documentation specifies a maximum input frequency of 66 MHz
- **kind**: QUANT
- **value**: 66
- **unit**: MHz
- **conditions**: NONE
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0157
- **sources**: SRC-0005
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0093

- **statement**: The frequency of the clock signal can be configured by the user, between 1 Hz and 66.5 MHz
- **kind**: QUANT
- **value**: between 1 Hz and 66.5 MHz
- **unit**: Hz, MHz
- **conditions**: by the user
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0160
- **sources**: SRC-0005
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T3

### FCT-0094

- **statement**: Tiny Tapeout IHP 0.4 Launched: 27 March 2026
- **kind**: QUANT
- **value**: 2026-03-27
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0166
- **sources**: SRC-0008
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T4

### FCT-0095

- **statement**: Tiny Tapeout IHP 0.4 Submission closed: 28 March 2026
- **kind**: QUANT
- **value**: 2026-03-28
- **unit**: DIMENSIONLESS
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0167
- **sources**: SRC-0008
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T4

### FCT-0096

- **statement**: Tiny Tapeout IHP 0.4 Submitted to IHP using sg13cmos5l 130nm open source PDK
- **kind**: QUANT
- **value**: sg13cmos5l 130nm open source PDK
- **unit**: nm
- **conditions**: NONE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0168
- **sources**: SRC-0008
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: T4

### FCT-0097

- **statement**: This repository [IHP Open Source PDK] is targeting the SG13G2 process node.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0183
- **sources**: SRC-0003
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I1

### FCT-0098

- **statement**: The IHP-Open-PDK repository landing page does not contain SG13CMOS5L.
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0184
- **sources**: SRC-0003
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I1

### FCT-0099

- **statement**: The IHP-Open-PDK repository landing page does not contain ihp-sg13cmos5l.
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0185
- **sources**: SRC-0003
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I1

### FCT-0100

- **statement**: It [IHP Open Source PDK] also hosts the SG13CMOS5L process node, a CMOS-only variant with a reduced metal stack.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0187
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I1-DEV

### FCT-0101

- **statement**: Switch between the process nodes by setting the `$PDK` environment variable to `ihp-sg13g2` or `ihp-sg13cmos5l`.
- **kind**: PROCEDURE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0188
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I1-DEV

### FCT-0102

- **statement**: SG13CMOS5L is a CMOS-only 0.13 μm process node from the same platform as SG13G2, but without the SiGe:C npn-HBT devices.
- **kind**: DEFINITION
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0189
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I2

### FCT-0103

- **statement**: It [SG13CMOS5L] provides the same [as SG13G2] 2 gate oxides: A thin gate oxide for the 1.2 V digital logic and a thick oxide for a 3.3 V supply voltage.
- **kind**: QUANT
- **value**: 2 gate oxides: A thin gate oxide for the 1.2 V digital logic and a thick oxide for a 3.3 V supply voltage
- **unit**: V
- **conditions**: NOT STATED
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0190
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I2

### FCT-0104

- **statement**: The aluminium backend offers 4 thin metal layers and one thick top metal layer (M1-M4-TM1).
- **kind**: QUANT
- **value**: 4 thin metal layers and one thick top metal layer (M1-M4-TM1)
- **unit**: metal layers
- **conditions**: NOT STATED
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0191
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I2

### FCT-0105

- **statement**: The MIM layer is not available.
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0192
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I2

### FCT-0106

- **statement**: metal-oxide-metal capacitors are offered instead [of The MIM layer]
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0193
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I2

### FCT-0107

- **statement**: IHP is currently treating the existing content as a preview only.
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0194
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I3

### FCT-0108

- **statement**: the SG13G2 process node and the PDK from which this open source release [IHP Open Source PDK] was derived have been used to create many designs that have been successfully manufactured in significant quantities
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0195
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I3

### FCT-0109

- **statement**: the open source PDK is not intended to be used for production at this moment
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0196
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I3

### FCT-0110

- **statement**: The same [the open source PDK is not intended to be used for production at this moment] applies to the SG13CMOS5L process node.
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0197
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I3

### FCT-0111

- **statement**: Neither [`cap_cmomi` (interdigitated, with feed topology) and `cap_cmomf` (metal fringe / finger)] is validated on CMOS5L silicon yet
- **kind**: QUAL
- **status label**: MOVING_CONSTRAINT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0199
- **sources**: SRC-0002
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I3

### FCT-0112

- **statement**: The ihp-sg13cmos5l README's title is "IHP SG13CMOS5L PDK (M1-M4-TM1 stack)".
- **kind**: QUAL
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0200
- **sources**: SRC-0001
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I4

### FCT-0113

- **statement**: This repo [IHP SG13CMOS5L PDK (M1-M4-TM1 stack)] is meant to be used **only** as a temporary storage during the development of the `build/compile` migration script for the sg13 cmos5l PDK.
- **kind**: RULE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0201
- **sources**: SRC-0001
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I4

### FCT-0114

- **statement**: The ihp-sg13cmos5l README does not contain License.
- **kind**: ABSENCE
- **status label**: CONFIRMED_FACT
- **lifecycle state**: PROPOSED
- **claims**: CLM-0202
- **sources**: SRC-0001
- **corroboration count**: 1. All claims supporting this fact come from a single document, so the independence tests of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#independence-of-sources) yield one independent source.
- **date of last verification**: 2026-09-17
- **contradictions**: NONE
- **re-enters bootstrap entry**: I4

## Counts

| State | Facts |
| --- | --- |
| PROPOSED | 108 |
| CANONICAL | 0 |
| CONTESTED | 6 |
| REVERIFY | 0 |
| RETIRED | 0 |

Consolidated from 116 independently confirmed claims; 2 were duplicates of a statement already proposed and were attached to the existing record rather than creating a new one, per the deduplication rule of [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#deduplication).

