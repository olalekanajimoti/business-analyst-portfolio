# NaijaFoodFestival: Business Analysis Pack

## Business requirements

| ID | Requirement | Priority | Objective | Acceptance criterion |
|---|---|---|---|---|
| BR-01 | Each user group follows a route relevant to its purpose | Must | OBJ-01 | Only relevant fields and guidance appear for the chosen route |
| BR-02 | Submissions cannot be completed with missing mandatory data | Must | OBJ-02 | Incomplete submissions are blocked with a clear correction message |
| BR-03 | Organisers can view every submission status | Must | OBJ-03 | Route, status, date and next action are visible for each record |
| BR-04 | Vendor decisions trigger the correct communication | Must | OBJ-04 | Message sent and record status agree |
| BR-05 | Volunteer allocation uses availability and need | Should | OBJ-03 | Allocation is visible to authorised organisers |
| BR-06 | Attendees receive purchase or registration confirmation | Must | OBJ-04 | Confirmation and transaction status are recorded |

## Traceability

| Objective | Requirement | Test | Evidence |
|---|---|---|---|
| OBJ-01: Separate the three user journeys | BR-01 | UAT-01 | Only relevant fields and guidance appear for the chosen route |
| OBJ-02: Reduce incomplete records and manual follow-up | BR-02 | UAT-02 | Incomplete submissions are blocked with a clear correction message |
| OBJ-03: Give organisers status and exception visibility | BR-03 | UAT-03 | Route, status, date and next action are visible for each record |
| OBJ-04: Validate end-to-end communications before launch | BR-04 | UAT-04 | Message sent and record status agree |
| OBJ-03: Give organisers status and exception visibility | BR-05 | UAT-05 | Allocation is visible to authorised organisers |
| OBJ-04: Validate end-to-end communications before launch | BR-06 | UAT-06 | Confirmation and transaction status are recorded |

## RAID snapshot

| Type | Item | Response |
|---|---|---|
| Risk | One form collects irrelevant or incomplete information | Separate user journeys |
| Risk | Email status and database status diverge | Trigger tests and exception checks |
| Assumption | Organisers will define approval rules before build | Decision checkpoint |
| Dependency | Ticketing and email services remain available | Fallback communication process |
| Issue | Missing requirement discovered during workflow review | Clarify, update and retest |

## KPI framework

- Completion rate by journey
- Incomplete application rate
- Time from vendor submission to decision
- Automation exception rate
- Confirmation delivery rate
- Manual follow-up volume
