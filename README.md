# protocol-emulator-asic

Repository of a team entering the Jane Street protocol emulator ASIC competition, announced on 2026-09-10 (https://blog.janestreet.com/protocol-emulator-asic-competition/). The organizer's task statement is: "Design an open-source, general-purpose protocol emulator ASIC." Every constraint of the challenge that this project currently knows, with its source URL and its status label, is recorded in [PROJECT_SCOPE.md](PROJECT_SCOPE.md#challenge-constraints-as-currently-known). Repository: https://github.com/DanielMBouyou/protocol-emulator-asic.

## Current state

Phase: PREBENCH, the first phase of the project; its calendar is in [PREBENCH_PLAN.md](PREBENCH_PLAN.md#calendar). Rule of the phase, in one sentence: benchmark before architecture, that is, the measurable problem is built, audited and frozen before any architecture is proposed.

Stage: S00, the methodological setup, still open. Its gate was evaluated on 2026-09-17 and did not pass: four conditions met, two not. What was produced, what failed and what the failing conditions need are in [knowledge/gate-g00.md](knowledge/gate-g00.md). No stage after S00 has opened.

## Files

| File | One line |
| --- | --- |
| [PROJECT_SCOPE.md](PROJECT_SCOPE.md) | What PREBENCH covers and excludes, the temporary prohibition of microarchitectural choices, the ARCHITECTURE GATE, and the sourced challenge constraints with their status labels, contradictions and open questions |
| [PREBENCH_PLAN.md](PREBENCH_PLAN.md) | The staged plan with its calendar, objectives, named artifacts, verifiable gates and the day-by-day schedule |
| [RESEARCH_METHOD.md](RESEARCH_METHOD.md) | How every search, screening and extraction is performed and logged so that a second operator can redo it and obtain the same records |
| [EVIDENCE_POLICY.md](EVIDENCE_POLICY.md) | Provenance and consolidation rules, the registers, and the definitions of FACT, OBSERVATION, HYPOTHESIS and DECISION |
| [RESEARCH_QUESTIONS.md](RESEARCH_QUESTIONS.md) | The open research questions with stable anchors, the evidence that would answer each, and the stage that addresses it |
| [knowledge/](knowledge/README.md) | The registers the method runs on: sources, claims, facts, observations, contradictions, decisions, limitations, queries, questions, and the gate records |

## Deliberately absent

No architecture directory, no RTL and no microarchitectural decision exist in this repository during PREBENCH; the canonical statement is in [PROJECT_SCOPE.md](PROJECT_SCOPE.md#deliberately-absent-architecture-and-rtl).
