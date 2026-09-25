# MyTicketSeller: Business Analysis Pack

## Objectives

1. Take payment reliably and deliver tickets immediately.
2. Report revenue, balances and payouts accurately in each currency.
3. Control event access through ticket ownership, team roles and scanning.
4. Protect buyers, organisers and the platform through refunds, dispute evidence and security.
5. Measure marketing performance only with visitor consent.

## Stakeholder register

| Stakeholder | Interest | Influence | Information need | Engagement approach |
|---|---|---|---|---|
| Event organisers | Payouts, sales visibility, door control | High | Earnings rules, payout timing | Dashboard messages and release notes |
| Ticket buyers | Fast checkout, instant tickets, refunds | Low | Order status, refund outcome | Transactional email |
| Door and scanning staff | Simple, fast scanning | Low | Their role and event | Invite email and in-app guidance |
| Platform admin and finance | Accurate revenue, withdrawals, disputes | High | Currency totals, pending approvals | Admin panel |
| Contract developers | Clear, testable requirements | High | Acceptance criteria and priorities | Backlog walkthrough |
| Payment providers | Correct integration and dispute handling | Medium | Webhook and dispute data | Provider dashboards |

## Key risks and controls

| Risk | Impact | Response |
|---|---|---|
| Payment callbacks arrive late or not at all | High | Verify on return page and reconcile pending orders |
| Currency errors misstate organiser earnings | High | Per-currency ledger and display rules |
| Security gaps left by rapid early builds | High | Audit: remove debug endpoints, move secrets, rate limit auth |
| Chargebacks lost without evidence | Medium | Log terms consent and export evidence per dispute |
| Dependence on individual contract developers | Medium | Single codebase, written requirements and owner-led fixes |

## UAT scenarios

| Test | Requirement | Given | When | Then | Status |
|---|---|---|---|---|---|
| UAT-01 | BR-01 | a buyer whose payment succeeded but whose webhook is delayed | they land on the return page | the order is verified and tickets are emailed | Released |
| UAT-02 | BR-01 | an order left pending for a future event | reconciliation runs | a paid order completes and an unpaid one stays pending | Released |
| UAT-03 | BR-02 | an event with naira and pound sales | the organiser opens the wallet | each currency shows its own balance | Released |
| UAT-04 | BR-03 | a refund issued in Stripe | the webhook arrives | the ticket is cancelled and the buyer is emailed | Released |
| UAT-05 | BR-04 | door staff invited to event A | they scan a ticket for event B | the scan is refused | Released |
| UAT-06 | BR-05 | an organiser swaps a sold ticket | revenue is recalculated | the total is unchanged and no new sale appears | Released |
| UAT-07 | BR-06 | a chargeback on a completed order | admin exports evidence | the PDF shows consent time, reason code and prior orders | Released |
| UAT-08 | BR-07 | a first-time visitor | they have not accepted cookies | no GA4, Meta or TikTok request is sent | Released |

## Measures

- Share of orders completed by reconciliation rather than on return, per gateway
- Duplicate-charge complaints
- Refund and dispute rate by event and currency
- Time from payment to ticket email
- Scans refused as duplicate or wrong event
- Consented conversion rate by marketing channel
