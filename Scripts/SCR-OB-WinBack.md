---
title: Outbound – Win-Back (Lapsed Customer)
aliases:
  - Win-Back Script
  - Re-acquisition Script
tags:
  - script
  - outbound
  - win-back
  - retention
script-type: outbound
product: "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
status: approved
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related:
  - "[SCR-OB-ContractRenewal](SCR-OB-ContractRenewal.md)"
  - "[SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)"
  - "[PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md)"
  - "[PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)"
license: "CC BY-NC 4.0"
---

## Purpose

Used when calling customers who have previously cancelled a ClearWave service and are being targeted for re-acquisition. The call should be warm, non-pressurising, and focused on understanding why the customer left before presenting a relevant offer.

## Before You Start

- Confirm the customer cancelled within the last 12 months and has not opted out of marketing contact
- Check the CRM for the stated reason for cancellation — this is critical for tailoring the conversation
- Confirm whether the customer is eligible for a win-back promotional price (check CRM offer flags — these are one-time offers and **must not** be repeated if the customer declines)
- Confirm the customer's address still has ClearWave network coverage
- **Do not** call customers who cancelled due to a complaint that is still unresolved
- **Do not** call customers who have requested no further contact — check the marketing suppression list

---

## Script

> **Agent:** "Good [morning/afternoon], could I speak with [Customer Name] please?"

> **[If customer confirms]**
> **Agent:** "Hi [Customer Name], my name is [Agent Name] calling from ClearWave. I hope you don't mind me reaching out — I can see you were a customer with us previously, and I'm calling because we've made some real improvements to our service and pricing since then, and I wanted to see if there was anything we could do to welcome you back. Is that okay?"

> **[If customer is reluctant]**
> **Agent:** "I completely understand. I won't take up more than a couple of minutes — and if at any point you'd prefer we don't call again, just let me know and I'll make sure we update your preferences straight away."

> **[If customer is open to hearing more]**
> **Agent:** "Thank you — that's really appreciated. I can see from your account that you were previously on [previous plan]. Can I ask what prompted you to move on? I'd love to understand if there was something we could have done better."

> **[If the reason was price]**
> **Agent:** "I completely understand — value is really important. We've actually introduced some new pricing since then, and I have a win-back offer I can make available exclusively to returning customers. I can offer you [plan] at [win-back price] a month for the first [X] months, then [standard price] after that on a 24-month contract. That's below what we'd offer a new customer today."

> **[If the reason was a service or reliability issue]**
> **Agent:** "I'm really sorry to hear that was your experience — that's not the standard we aim for. I want to be transparent with you: we've invested in our network in your area since then, and our customer satisfaction scores have improved significantly. I wouldn't want to make a promise I can't keep, so I'd suggest starting with a no-obligation trial — would that be something you'd consider?"

> **[If the reason was a product gap, e.g. no mobile at the time]**
> **Agent:** "That's really useful to know — and actually, that's one of the things we've expanded. We now offer 5G SIM-only plans from £12 a month, and our Unlimited 5G plan is just £22 a month on a 12-month contract. We also have our own handsets available on 0% finance."

> **Agent (to confirm re-sign):** "So if you're happy to give us another go, I can process the new order today. You'll have a full 14-day cooling-off period — so if for any reason it doesn't feel right, you can cancel with no cost. Shall I go ahead?"

> **Agent (closing):** "Fantastic — welcome back, [Customer Name]. I'll send a confirmation to [customer email], and your [service] will be active within [timeframe]. Is there anything else I can help with today?"

---

## Branching Paths

| Customer Response | Go To |
| ------------------- | ------- |
| Open to coming back | Present appropriate win-back offer from CRM |
| Price was the issue | Offer win-back promotional price (one-time only) |
| Service/reliability was the issue | Acknowledge, explain improvements; offer trial |
| Left for a competitor, happy there | Thank them; ask if okay to contact again in 6 months; log `WINBACK-NOT-NOW` |
| Has an unresolved complaint | End call; route to [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md); do not sell |
| Requests no further contact | Log marketing opt-out immediately; end call |
| Wants to order | [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md) |

## Compliance Notes

- **Marketing suppression list must be checked before every outbound call** — calling a customer who has opted out is a breach of PECR and must be reported to the Data Protection Officer
- **Win-back offers are one-time only** — if the customer declines, do not re-offer on the same call or a future call without a new CRM-authorised offer code
- **Cooling-off period must be communicated** before every sale (Consumer Contracts Regulations 2013)
- **KFI must be provided** for any fixed-term contract — see [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md) step 6
- Do **not** criticise or make comparisons with the customer's current provider
- Do **not** apply pressure — if the customer says no, accept it graciously and log the outcome
- Log outcome in CRM: `WINBACK-ACCEPTED`, `WINBACK-DECLINED`, `WINBACK-NOT-NOW`, `OPT-OUT-LOGGED`, or `COMPLAINT-REROUTED`

---

## Related

- [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)
- [PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md)
- [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md)
- [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)
- [SCR-OB-ContractRenewal](SCR-OB-ContractRenewal.md)
- [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)
