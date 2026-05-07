---
title: Outbound – Contract Renewal
aliases:
  - Contract Renewal Script
  - End of Contract Script
tags:
  - script
  - outbound
  - renewal
  - retention
script-type: outbound
product: "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
status: approved
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related:
  - "[SCR-OB-WinBack](SCR-OB-WinBack.md)"
  - "[SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)"
  - "[PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md)"
  - "[PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)"
---

## Purpose

Used when calling customers whose fixed-term contract is due to expire within the next 30–60 days. Goal is to proactively renew the customer onto a new contract before they roll onto a higher out-of-contract rate or start shopping elsewhere.

## Before You Start

- Confirm the customer's contract end date in the CRM — this call should only be made within the 30–60 day renewal window
- Note their current plan, monthly charge, and whether they are in good standing (no active debt or disputes)
- Check for any available renewal offers or loyalty pricing flagged in the CRM
- Have all broadband and SIM plan pricing to hand
- Do **not** call customers with an active complaint without manager approval

---

## Script

> **Agent:** "Good [morning/afternoon], could I speak with [Customer Name] please?"

> **[If customer confirms]**
> **Agent:** "Hi [Customer Name], my name is [Agent Name] calling from ClearWave. I'm calling because your current broadband contract with us is coming to an end on [contract end date], and I wanted to make sure you had the best deal in place before that happens. Do you have a few minutes?"

> **[If customer says they're busy]**
> **Agent:** "Absolutely, no problem — can I arrange a better time to call? We do want to make sure you're not left paying the out-of-contract rate unnecessarily. [Log callback in CRM]"

> **[If customer agrees to discuss]**
> **Agent:** "Great. At the moment you're on our [current plan] at [£X] a month. If you don't renew, that would move to our standard out-of-contract rate of [£Y] a month. But because you're a loyal customer, I can offer you a renewal today on the same plan for [£X / discounted price] — locked in for another 24 months. Would that work for you?"

> **[If customer wants an upgrade instead]**
> **Agent:** "We could also look at upgrading you at the same time — for example, our Fibre 500 is available at £38 a month on a new 24-month deal, which would be a significant improvement on your current speeds. Would you like me to go through that option?"
> — *[Continue using [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md) branching if customer engages]*

> **[If customer says they're considering leaving]**
> **Agent:** "I completely understand — it's always worth reviewing your options. Before you make a decision, can I check if there's anything specific that's prompted that thought? There may be something I can do to help."
> — *[If they have a grievance, route to [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md)]*
> — *[If it's about price, explore retention offer from CRM]*

> **Agent (to confirm renewal):** "So to confirm, I'm going to renew your contract for [plan name] at [£X] a month for 24 months, starting from [renewal date]. You'll receive a confirmation email within 24 hours. Does that all sound good?"

> **[Cooling-off reminder before close]**
> **Agent:** "Just to let you know, you have a 14-day cooling-off period from today, so if you change your mind for any reason you can contact us and we'll revert you at no charge."

> **Agent (closing):** "Brilliant — thank you for staying with us, [Customer Name]. Is there anything else I can help with today?"

---

## Branching Paths

| Customer Response | Go To |
|-------------------|-------|
| Wants to renew on current plan | Confirm and process renewal in CRM |
| Wants an upgrade | [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md) |
| Wants to add mobile | [SCR-OB-MobileAddOn](SCR-OB-MobileAddOn.md) |
| Considering leaving | Explore retention offer; if unresolved → [PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md) |
| Has a complaint | [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md) |
| Already cancelled | [SCR-OB-WinBack](SCR-OB-WinBack.md) (if within 30 days of cancellation) |

## Compliance Notes

- **Do not imply the customer must renew** — they are entitled to leave at end of contract with no penalty; the out-of-contract rate applies but no Early Termination Charge (ETC)
- **Cooling-off period must be communicated** before every renewal (Consumer Contracts Regulations 2013)
- **KFI must be provided** for every new fixed-term contract — see [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md) step 6
- Do not quote the out-of-contract rate as a penalty — frame it neutrally as the standard rolling rate
- Do **not** offer a renewal price lower than the CRM-flagged minimum without manager authorisation
- Log outcome in CRM: `RENEWAL-ACCEPTED`, `RENEWAL-DECLINED`, `UPGRADE-AT-RENEWAL`, or `CALLBACK-REQUESTED`

---

## Related

- [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)
- [PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md)
- [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)
- [SCR-OB-MobileAddOn](SCR-OB-MobileAddOn.md)
- [SCR-OB-WinBack](SCR-OB-WinBack.md)
