# Komfort Place Signature: Business Analysis Pack

## Objectives

1. Turn website visits into WhatsApp booking conversations.
2. Measure which pages and buttons produce booking enquiries.
3. Grow organic visibility for local service searches.
4. Encourage repeat visits.
5. Respect visitor consent and platform content policies.

## Stakeholder register

| Stakeholder | Interest | Influence | Information need | Engagement approach |
|---|---|---|---|---|
| Spa owner and management | Bookings, brand and repeat clients | High | Booking sources and trends | Dashboard review |
| Front desk and WhatsApp team | Qualified, clear booking messages | Medium | What visitors ask and book | Demonstration and feedback |
| Therapists | Accurate, respectful representation | Low | How they are presented | Review before publishing |
| New clients | Clear services, prices and trust signals | Low | Services, prices, reviews | Website and assistant |
| Returning clients | Rewards and easy rebooking | Low | Loyalty rules | Website and WhatsApp |
| Search and ad platforms | Policy-compliant content | High | Content policies | Search Console and ad tools |

## Key risks and controls

| Risk | Impact | Response |
|---|---|---|
| Content breaches search or ad policy | High | Review before publishing; withdraw non-compliant posts |
| Assistant gives a wrong price or availability | High | Approved content only and handoff to WhatsApp |
| Roster changes leave the site out of date | Medium | One roster list drives every page and prompt |
| Declined consent reduces third-party data | Medium | First-party click analytics as the baseline |
| Staff images published without agreement | Medium | Approval before any photo goes live |

## UAT scenarios

| Test | Requirement | Given | When | Then | Status |
|---|---|---|---|---|---|
| UAT-01 | BR-01 | a mobile visitor on any page | they scroll | the booking button stays visible and opens WhatsApp | Released |
| UAT-02 | BR-02 | the spa is closed | a visitor asks about prices | the assistant answers and offers the booking link | Released |
| UAT-03 | BR-03 | a visitor taps a booking button | the manager opens Today | the tap appears under that page and hour | Released |
| UAT-04 | BR-04 | a new guide is published | the sitemap is regenerated | the URL is listed with a canonical tag | Released |
| UAT-05 | BR-05 | a returning visitor | the Spin & Win prompt opens | it can be closed and does not overlap the assistant | Released |
| UAT-06 | BR-06 | a first-time visitor | they have not accepted cookies | no GA4 or Meta request is sent | Released |
| UAT-07 | BR-07 | an article that breaches policy | it is reviewed | it is withdrawn before or after publishing | Released |

## Measures

- Booking taps per page and per service
- Assistant conversations that end in a booking tap
- Organic visits to service guides
- Share of bookings from returning clients
- Consent acceptance rate
