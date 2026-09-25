# BOZ Jewelry: Business Analysis Pack

## Objectives

1. Improve the consistency and usability of the online shopping journey.
2. Create clearer ownership and visibility across digital workstreams.
3. Support colleagues adopting Microsoft 365 and new working practices.
4. Reduce avoidable customer-service effort while protecting the quality of sales support.
5. Improve custom-order requirement capture and expectation management.

## Stakeholder register

| Stakeholder | Interest | Influence | Information need | Engagement approach |
|---|---|---:|---|---|
| Business owner | Commercial value, cost and risk | High | Milestones, options, decisions, benefits | Decision-focused updates |
| Customer-service/store teams | Usability and workload | Medium | Process changes, support, escalation | Demonstrations and feedback |
| Developers | Feasible and testable scope | High | Workflows, data, acceptance criteria | Detailed requirements and reviews |
| Creatives | Brand and content requirements | Medium | Priorities, assets, dependencies | Visual briefs and checkpoints |
| Technology providers | Integration and configuration | Medium | Technical scope and access | Structured implementation updates |
| Customers | Clear and reliable journey | High impact | Product, order and support information | User-centred content and validation |

## Key risks and controls

| Risk | Impact | Response |
|---|---|---|
| Users revert to fragmented communication | Reduced traceability | Clear ownership, demonstrations and reinforced channels |
| Custom requirements are misunderstood | Dissatisfaction and rework | Structured capture and customer confirmation |
| Automated answers become inaccurate | Poor customer experience | Approved knowledge content and escalation route |
| Permissions expose information incorrectly | Security and trust risk | Role-based access and validation |
| Success is assumed at launch | Benefits not evidenced | Post-implementation KPI review |

## UAT scenarios

| Test | Requirement | Given | When | Then | Status |
|---|---|---|---|---|---|
| UAT-01 | BR-01 | items exist on the delivery board | the owner opens the weekly summary | blocked and overdue items show owner, due date and dependency | Passed |
| UAT-02 | BR-02 | a colleague without the finance role | they open the finance library | access is denied and the attempt is logged | Passed |
| UAT-03 | BR-03 | a customer asks a delivery-time question | the chatbot receives it | the approved answer is returned | Passed |
| UAT-04 | BR-04 | a custom request without confirmation | staff try to move it to production | the move is blocked until confirmation is recorded | Passed |
| UAT-05 | BR-05 | release candidate is ready | the scenario pack is run with business users | all Must scenarios pass and exceptions are logged | Passed |

## Measures

- Digital engagement
- Website/customer-journey performance
- Volume and type of repeat enquiries
- Custom-order exceptions or rework
- Adoption of agreed collaboration channels
- Delivery status completeness
