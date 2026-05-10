---
title: Outbound – Mobile Add-On Offer
aliases:
  - Mobile Add-On Script
tags:
  - script
  - outbound
  - mobile
  - upsell
script-type: outbound
product: "[PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)"
status: approved
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related:
  - "[SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)"
  - "[PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)"
  - "[PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md)"
  - "[PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)"
  - "[PROD-ClearTelComCoX1ProHandset](../Products/PROD-ClearTelComCoX1ProHandset.md)"
license: "CC BY-NC 4.0"
---

## Purpose

Used when calling existing broadband-only customers who have no ClearTelComCo mobile product. Goal is to introduce a SIM-only or handset bundle deal as a complementary add-on, creating a multi-product household.

## Before You Start

- Confirm customer has no existing ClearTelComCo mobile product in the CRM
- Check whether the customer's address has 5G coverage (use the Coverage Checker tool before calling)
- Have current SIM-only pricing to hand: [PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md) · [PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)
- Note whether the customer is eligible for a loyalty multi-product discount (check CRM offer flags)
- Do **not** call customers flagged as vulnerable without a manager briefing first

---

## Script

> **Agent:** "Good [morning/afternoon], could I speak with [Customer Name] please?"

> **[If customer confirms]**
> **Agent:** "Hi [Customer Name], my name is [Agent Name] from ClearTelComCo. I'm calling because, as one of our broadband customers, you qualify for an exclusive deal we're running on our mobile plans — and I thought you'd want to hear about it. Is now a good time?"

> **[If customer says they're busy]**
> **Agent:** "Of course, no problem. Can I arrange a callback? What time works best for you? [Log callback in CRM]"

> **[If customer agrees to hear more]**
> **Agent:** "Brilliant. We've just launched our 5G SIM-only plans, and because you're already with us for broadband, we can offer you our Unlimited 5G SIM for £22 a month on a 12-month plan — that includes unlimited calls, texts and data, plus 25 GB of EU roaming included. You can also tether from the SIM if you ever need a backup connection."

> **[Pause — let the customer respond]**

> **[If the customer wants a lower-data option]**
> **Agent:** "If you'd prefer something lighter, our 10 GB 5G plan is just £12 a month on a rolling one-month contract — no commitment, and any unused data rolls over to the following month."

> **[If the customer asks about a new handset]**
> **Agent:** "We also have our own ClearTelComCo handsets if you're looking for a new phone. Our X1 Pro is our flagship — a 200-megapixel camera, five-day battery and IP68 water resistance — available on 0% finance at £30 a month, which you combine with any SIM plan. Or if you're looking for great value, our X1 Budget comes in at £10 a month and is a really solid everyday device."

> **Agent (to confirm):** "Would you like me to go ahead and get that SIM set up for you today? We can post a SIM to your address on file within two working days, or I can arrange an e-SIM activation if your handset supports it."

> **[Cooling-off reminder before close]**
> **Agent:** "You also have a 14-day cooling-off period once the order is placed, so there's absolutely no risk in giving it a try."

> **Agent (closing):** "Brilliant — I'll email a confirmation to [customer email]. Is there anything else I can help with today?"

---

## Branching Paths

| Customer Response | Go To |
| ------------------- | ------- |
| Wants to think it over | Offer to email an overview; log follow-up in CRM |
| Asks about handset finance | [PROD-ClearTelComCoX1ProHandset](../Products/PROD-ClearTelComCoX1ProHandset.md) · Consumer Credit Act note applies — see Compliance Notes |
| Wants broadband upgrade at same time | [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md) |
| Wants to cancel broadband | [PROC-GEN-CustomerCancellation](../Procedures/PROC-GEN-CustomerCancellation.md) |
| Complaint or escalation | [PROC-GEN-CustomerSupport](../Procedures/PROC-GEN-CustomerSupport.md) |

## Compliance Notes

- **Coverage check is mandatory** before the call — do not promote 5G to a customer without confirmed 5G coverage; offer 4G equivalent if 5G is unavailable
- **Cooling-off period must be communicated** before every sale (Consumer Contracts Regulations 2013)
- **KFI must be emailed** for any contract of 12 months or more — see [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md) step 6
- If quoting handset finance, confirm the agent is operating under ClearTelComCo's Consumer Credit Act licence; do not advise on personal affordability — direct to the online eligibility checker
- Tethering is included on the Unlimited plan; confirm it is **not** included on the 10 GB plan
- If customer asks why they are being called: confirm this is a proactive outbound offer and offer opt-out from marketing calls at any time
- Log outcome in CRM: `MOBILE-ACQUIRED`, `MOBILE-DECLINED`, or `CALLBACK-REQUESTED`

---

## Related

- [PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md)
- [PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)
- [PROD-ClearTelComCoX1ProHandset](../Products/PROD-ClearTelComCoX1ProHandset.md)
- [PROD-ClearTelComCoX1HandsetBudget](../Products/PROD-ClearTelComCoX1HandsetBudget.md)
- [PROC-GEN-SalesProcedure](../Procedures/PROC-GEN-SalesProcedure.md)
- [SCR-OB-BroadbandUpgrade](SCR-OB-BroadbandUpgrade.md)
