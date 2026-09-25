# Taash: Decision Rules and Traceability

> These are product-analysis rules, not personal tax advice. Every rule requires validation against authoritative guidance before release.

## Routing table

| Rule ID | Condition | Route/output |
|---|---|---|
| DR-01 | User is an employee/PAYE taxpayer | PAYE journey |
| DR-02 | User earns self-employed/freelance income | Freelancer/individual journey |
| DR-03 | Entity is registered as a business name | Relevant state route |
| DR-04 | Entity is a registered company | Relevant federal/company route |
| DR-05 | Case exceeds supported conditions | Human/professional review |

## Relief logic model

Rule set: **RULE-2026-01**, effective 1 January 2026 under the Nigeria Tax Act 2025. The Act removed the consolidated relief allowance, so the earlier CRA-based relief rules were retired and replaced by the two rules below.

| Rule ID | Input | Logic | Output |
|---|---|---|---|
| DR-06 | Annual rent paid (with evidence) | Take 20% of rent, capped at ₦500,000 | Display rent relief and whether the cap applied |
| DR-07 | Chargeable income after reliefs and deductions | Apply the configured progressive bands; the first ₦800,000 is taxed at 0% | Display tax per band |
| DR-08 | Declared deduction | Validate type, limit and evidence status | Include, exclude or refer for review |

## Requirements traceability

| Objective | Requirements | Rules | Tests |
|---|---|---|---|
| OBJ-01: Correct route | BR-01, BR-02 | DR-01 to DR-04 | UAT-01, UAT-02, UAT-03 |
| OBJ-02: Transparent estimate | BR-03, BR-04 | DR-06 to DR-08 | UAT-04, UAT-05, UAT-06 |
| OBJ-03: Controlled change | BR-05, BR-09 | Effective-date metadata | UAT-07, UAT-11 |
| OBJ-04: Visible progress | BR-06 | Stage rules | UAT-08 |
| OBJ-05: Protection and review | BR-07, BR-08 | Access control, DR-05 | UAT-09, UAT-10 |

## Open questions

- Which rules can be fully automated and which require human approval?
- What evidence is mandatory for each deduction and taxpayer type?
- How will authority acknowledgements and payment confirmations be integrated?
- What retention periods and deletion rights apply to each record type?
- How will rule owners approve and publish regulatory changes?
