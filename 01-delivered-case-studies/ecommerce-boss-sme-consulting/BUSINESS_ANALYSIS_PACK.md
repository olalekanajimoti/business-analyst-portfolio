# The Ecommerce Boss: Business Analysis Pack

## Objectives

1. Agree the business goal and success measure before anything is built.
2. Deliver websites and tools that fit the business's budget and capacity.
3. Capture every enquiry in one traceable record with a clear next step.
4. Make marketing and website performance measurable.
5. Leave the owner able to run the solution after handover.

## Stakeholder register

| Stakeholder | Interest | Influence | Information need | Engagement approach |
|---|---|---|---|---|
| Business owners and founders | Growth, cost and time | High | Options, costs, progress and results | Discovery workshop and weekly check-ins |
| Client staff (sales, marketing, admin) | Tools that save time | Medium | New processes and how to use them | Walkthroughs and handover guides |
| Customers of the business | Easy buying and quick replies | Low | Journey and communication | Usability checks |
| Freelance designers and developers | Clear, buildable requirements | Medium | Acceptance criteria and priorities | Backlog walkthrough |
| Platform providers | Correct configuration | Low | Integration and account settings | Provider documentation |

## Key risks and controls

| Risk | Impact | Response |
|---|---|---|
| Scope grows beyond a fixed small-business budget | High | MoSCoW prioritisation and a change log agreed with the owner |
| Owner has little time for discovery and testing | High | Short, structured sessions and clear decision points |
| Tools are abandoned after handover | Medium | Simple tools, training and a written guide |
| Poor data quality in legacy spreadsheets | Medium | Validation at intake and a one-off clean-up |
| Tracking set up without consent | High | Consent-gated tags checked in UAT |

## UAT scenarios

| Test | Requirement | Given | When | Then | Status |
|---|---|---|---|---|---|
| UAT-01 | BR-01 | a new engagement | discovery is complete | the owner has signed off goal, measure and scope | Passed |
| UAT-02 | BR-02 | a backlog over budget | priorities are reviewed | Must items fit the budget and the rest are recorded | Passed |
| UAT-03 | BR-03 | an enquiry through the website form | it is submitted | a record appears with source, status and owner | Passed |
| UAT-04 | BR-03 | the same customer enquires twice | the second record is created | it is flagged as a possible duplicate | Passed |
| UAT-05 | BR-04 | a new enquiry | the automation runs | the customer receives a confirmation | Passed |
| UAT-06 | BR-05 | a visitor who has not accepted cookies | they browse the site | no analytics tag loads | Passed |
| UAT-07 | BR-07 | handover is complete | the owner updates a page and a record alone | both changes succeed | Passed |

## Measures

- Share of engagements with a signed-off success measure
- Enquiry response time before and after
- Enquiries without an owner or next step
- Enquiries and sales by source channel
- Change requests absorbed within budget
