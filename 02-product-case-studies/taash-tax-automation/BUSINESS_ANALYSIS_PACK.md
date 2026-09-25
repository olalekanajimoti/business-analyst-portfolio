# Taash: Business Analysis Pack

## Business objectives

| ID | Objective |
|---|---|
| OBJ-01 | Classify taxpayer and entity type correctly |
| OBJ-02 | Explain calculations and the evidence behind them |
| OBJ-03 | Keep tax rules versioned and current |
| OBJ-04 | Track File, Pay, Confirm and Certificate |
| OBJ-05 | Protect taxpayers through data security and a human review route |

## Scope

### In scope

- Guided onboarding and taxpayer classification
- Individual/PAYE and freelancer data capture
- Business-name and registered-company routing
- Relief and deduction capture
- Calculation explanation
- Document/evidence checklist
- Filing, payment, confirmation and certificate status
- Educational content and TIN guidance

### Outside initial scope

- Guaranteeing a tax authority outcome
- Replacing professional tax advice for complex cases
- Filing in unsupported jurisdictions
- Applying rules without an effective-date/version check

## Requirements catalogue

| ID | Requirement | Priority | Objective | Acceptance criterion |
|---|---|---|---|---|
| BR-01 | Identify taxpayer or entity type | Must | OBJ-01 | Validated answers route the user to the correct journey |
| BR-02 | Distinguish business-name (BN) and incorporated-company (RC) routes | Must | OBJ-01 | The relevant state or federal journey appears |
| BR-03 | Capture income, deductions and evidence status | Must | OBJ-02 | Required values and evidence flags are retained |
| BR-04 | Show the rules and values applied in each result | Must | OBJ-02 | An itemised explanation is available for review |
| BR-05 | Version rules by effective date | Must | OBJ-03 | Each result records the active rule version |
| BR-06 | Track File, Pay, Confirm and Certificate stages | Should | OBJ-04 | Current stage and next action are visible |
| BR-07 | Sensitive data is access controlled | Must | OBJ-05 | Unauthorised access is rejected and access events are logged |
| BR-08 | Uncertain or complex cases have an escalation route | Must | OBJ-05 | User receives a clear referral or review option |
| BR-09 | Guidance content is editable without code deployment | Should | OBJ-03 | Authorised editor updates and publishes controlled content |

Functional requirements FR-01 to FR-09 are in the [FRD](Docs/FRD.pdf).

## User stories

- As a freelancer, I want to record income and allowable costs so that I can understand my estimated taxable position.
- As a business owner, I want the system to identify whether my filing route is state or federal so that I do not begin the wrong process.
- As a taxpayer, I want to see how reliefs and deductions affected the result so that I can review it before proceeding.
- As a tax reviewer, I want to see the rule version and supporting evidence so that I can assess the calculation.
- As a content administrator, I want to update guidance with an effective date so that published information remains controlled.

## Stakeholder register

| Stakeholder | Interest | Influence | Engagement |
|---|---|---:|---|
| Users/taxpayers | Clarity, accuracy and privacy | High impact | Research, usability tests and support feedback |
| Tax specialists | Rule interpretation and exceptions | High | Rule review and sign-off |
| Tax authorities | Compliance and submission quality | High | Process alignment and formal guidance |
| Engineering | Implementable, testable rules | High | Decision tables and acceptance criteria |
| Content team | Accurate and current guidance | Medium | Editorial workflow and version controls |
| Business leadership | Adoption, risk and sustainability | High | KPI, risk and roadmap reviews |

## RAID snapshot

| Type | Description | Response |
|---|---|---|
| Risk | Regulation changes after implementation | Version rules and effective dates; scheduled review |
| Risk | User treats estimate as professional advice | Clear disclosures and escalation |
| Risk | Sensitive information is exposed | Least-privilege access and secure storage design |
| Risk | Incorrect classification leads to wrong route | Confirmation screen and review controls |
| Dependency | Authoritative interpretation of tax rules | Specialist/legal validation |
| Assumption | Integrations will support required status updates | Validate during technical discovery |

## UAT scenarios

| Test | Requirement | Given | When | Then | Status |
|---|---|---|---|---|---|
| UAT-01 | BR-01 | a user with salary and freelance income | they complete the questionnaire | they are asked to confirm their primary route | Planned |
| UAT-02 | BR-02 | a user selects business name | the journey starts | the state route and its evidence list are shown | Planned |
| UAT-03 | BR-02 | a user selects registered company | the journey starts | the federal company route is shown | Planned |
| UAT-04 | BR-03 | a deduction without evidence | the user continues | the entry is flagged Pending | Planned |
| UAT-05 | BR-04 | declared rent where 20% of it is below the ₦500,000 rent-relief cap (DR-06) | relief is calculated | the 20% value is applied and shown in the explanation | Planned |
| UAT-06 | BR-04 | declared rent where 20% of it is above the ₦500,000 rent-relief cap (DR-06) | relief is calculated | the ₦500,000 cap is applied and shown | Planned |
| UAT-07 | BR-05 | a rule changes effective date | a prior result is reopened | it keeps the original rule version | Planned |
| UAT-08 | BR-06 | payment is confirmed | the tracker refreshes | the stage moves to Confirm with the next action | Planned |
| UAT-09 | BR-07 | an unauthorised user | they request a taxpayer record | access is rejected and the event is logged | Planned |
| UAT-10 | BR-08 | an unsupported case | the result is produced | the escalation option and limitation message appear | Planned |
| UAT-11 | BR-09 | a draft guidance update | it is approved with a future effective date | users see it only from that date | Planned |

## Success measures

- Journey completion rate
- Classification correction rate
- Calculation-review/escalation rate
- Evidence completeness
- Average time to complete each stage
- Rule-related defect rate
- Content update turnaround
- User confidence and support-contact rate
