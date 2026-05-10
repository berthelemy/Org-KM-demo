---
title: Outbound – Broadband Upgrade Offer
aliases:
  - Broadband Upgrade Script
tags:
  - script
  - outbound
  - broadband
  - upsell
script-type: outbound
product: "[PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)"
status: approved
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related:
  - "[SCR-OB-ContractRenewal](SCR-OB-ContractRenewal.md)"
  - "[PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)"
  - "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
  - "[PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)"
  - "[PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)"
license: "CC BY-NC 4.0"
---

## Purpose

Used when calling existing broadband customers who are on a lower-tier plan (Fibre 100) and are eligible for an upgrade offer. Goal is to present the benefit of a faster tier and convert to a new 24-month contract.

## Before You Start

- Confirm the customer's current plan and monthly charge in the CRM
- Check upgrade eligibility: customer must be ≥ 6 months into their current contract
- Note any previous contact or objections logged against the account
- Have the Fibre 500 and Fibre 1000 pricing to hand: [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md) · [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)
- Do **not** call customers flagged as vulnerable without a manager briefing first

---

## Script

> **Agent:** "Good [morning/afternoon], could I speak with [Customer Name] please?"

> **[If customer confirms]**
> **Agent:** "Hi [Customer Name], my name is [Agent Name] calling from ClearTelComCo. I'm calling because we've got some great news — as one of our valued customers, you're eligible for an exclusive upgrade offer on your broadband. Do you have a couple of minutes?"

> **[If customer says they're busy]**
> **Agent:** "No problem at all — I can call back at a time that suits you. What would be a good time? [Log callback in CRM]"

> **[If customer agrees to hear more]**
> **Agent:** "Brilliant. You're currently on our Fibre 100 plan, giving you speeds up to 100 Mbps for [£X] a month. We can upgrade you today to our Fibre 500 plan — that's up to 500 Mbps, ideal if you've got multiple people streaming, gaming, or working from home — for just £38 a month on a new 24-month agreement. That's our best available price, and we'd include our latest Wi-Fi 6 Smart Hub as well."

> **[Pause — let the customer respond]**

> **[If customer asks about the Fibre 1000 option]**
> **Agent:** "Great question — our Gigabit Fibre 1000 plan gives you a full 1,000 Mbps upload and download for £52 a month. That also includes a dedicated onboarding call with one of our technical specialists to get everything set up perfectly. A lot of our customers with smart home devices or a home office find that one really appeals."

> **Agent (to confirm the upgrade):** "So I can get that upgrade processed for you today — there's no engineer visit required, it activates remotely within 24 hours. Shall I go ahead and set that up?"

> **[Cooling-off reminder before close]**
> **Agent:** "Just to let you know, once we process this, you'll have a 14-day cooling-off period — so if for any reason it doesn't suit you, you can contact us within that window and we'll revert you at no cost. Does that sound good?"

> **Agent (closing):** "Perfect. I'll send you a confirmation email to [customer email on file] now. Is there anything else I can help you with today?"

---

## Branching Paths

| Customer Response | Go To |
| ------------------- | ------- |
| Wants more time to think | Offer to email a summary; log follow-up in CRM |
| Already planning to leave | [SCR-OB-WinBack](SCR-OB-WinBack.md) |
| Asks about adding mobile | [SCR-OB-MobileAddOn](SCR-OB-MobileAddOn.md) |
| Contract renewal question | [SCR-OB-ContractRenewal](SCR-OB-ContractRenewal.md) |
| Requests manager or complains | [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md) |
| Wants to cancel current plan | [PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md) |

## Compliance Notes

- **Do not misrepresent current pricing** — always confirm the customer's actual current charge from CRM before quoting savings
- **Cooling-off period must be communicated** before every sale (Consumer Contracts Regulations 2013)
- **Key Facts Indicator (KFI)** must be read or emailed for every new contract — see [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md) step 6
- Do **not** describe speed tiers as "guaranteed" — use "up to" language in line with Ofcom advertising guidance
- If the customer asks why they are being called, confirm this is a proactive outbound offer and that they may opt out of marketing calls at any time
- Log outcome in CRM: `UPGRADE-ACCEPTED`, `UPGRADE-DECLINED`, or `CALLBACK-REQUESTED`

---

## Related

- [PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)
- [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)
- [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)
- [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)
- [SCR-OB-ContractRenewal](SCR-OB-ContractRenewal.md)
- [SCR-OB-MobileAddOn](SCR-OB-MobileAddOn.md)
