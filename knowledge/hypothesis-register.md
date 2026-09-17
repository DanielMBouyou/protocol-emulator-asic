# Hypothesis register

Register `HYP-nnnn`, defined in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#registers-and-identifiers). A HYPOTHESIS, what it requires, where it may appear and what it may never do are canonical in [EVIDENCE_POLICY.md](../EVIDENCE_POLICY.md#hypothesis). What that rule covers in this project is fixed in [PROJECT_SCOPE.md](../PROJECT_SCOPE.md#hypothesis-isolation-scope).

Field list per record, in this order:

- **statement**
- **supporting evidence would be**
- **refuting evidence would be**
- **targets**: the research question or stage it bears on
- **author**
- **date**
- **state**: UNTESTED, TESTING, SUPPORTED, REFUTED or WITHDRAWN

## Entries

None. The register is empty at the close of [S00](../PREBENCH_PLAN.md#s00-methodological-setup).

S00 fixed the method and re-entered the bootstrap facts as claims. It produced no conjecture, so there is nothing to isolate here yet. An empty register is the expected state at this point and is not a gap to be filled; a record is created when a conjecture actually arises, not to demonstrate the format.

Condition AG-12 of the [ARCHITECTURE GATE](../PROJECT_SCOPE.md#architecture-gate) audits, at benchmark freeze, that every statement labelled HYPOTHESIS anywhere in the repository has a record here.
