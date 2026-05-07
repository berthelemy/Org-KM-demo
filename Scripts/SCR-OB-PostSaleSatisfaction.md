---
title: Outbound – Post-Sale Satisfaction Check
aliases:
  - Post-Sale Satisfaction Script
  - Post-Install Follow-Up Script
tags:
  - script
  - outbound
  - satisfaction
  - post-sale
script-type: outbound
product: "[[PROD-Fibre100Broadband]]"
status: approved
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related:
  - "[[PROC-GEN-CustomerOnboarding]]"
  - "[[PROC-GEN-CustomerSupport]]"
  - "[[SCR-OB-BroadbandUpgrade]]"
  - "[[SCR-OB-MobileAddOn]]"
---

## Purpose

Used 7–14 days after a new customer's service has gone live, or after an existing customer's upgrade or new product has been activated. The primary goal is to confirm the customer's experience is positive and resolve any issues early. A secondary goal is to identify upsell or cross-sell opportunities where appropriate.

## Before You Start

- Confirm the service activation date in the CRM — this call should be made 7–14 days after go-live
- Check for any open support tickets or complaints on the account — if any exist, lead with the issue, not the satisfaction check; this call must not feel dismissive of known problems
- Check what product(s) the customer has and any recent interactions logged
- Do **not** attempt upsell if the customer has an open complaint or has contacted support more than once in the past 14 days
- Review the onboarding checklist status in the CRM: [[PROC-GEN-CustomerOnboarding]]

---

## Script

> **Agent:** "Good [morning/afternoon], could I speak with [Customer Name] please?"

> **[If customer confirms]**
> **Agent:** "Hi [Customer Name], my name is [Agent Name] from ClearWave. I'm calling because your [service name] went live [X] days ago, and we like to do a quick check-in with all our new customers to make sure everything is working well and you're happy. Do you have a moment?"

> **[If customer says they're busy]**
> **Agent:** "No problem at all — I can call back at a better time. Is there a day or time that works well for you? [Log callback in CRM]"

> **[If customer agrees]**
> **Agent:** "Brilliant. First of all — how's the service been? Have you had any issues with [broadband speed / mobile signal / device setup], or has everything been working as expected?"

> **[If customer says everything is fine]**
> **Agent:** "That's great to hear — really glad it's all gone smoothly. Just so you know, if you ever need help you can reach us on our live chat, app, or by calling. Our app also lets you run a speed test and manage your account at any time."

> **[If customer reports an issue]**
> **Agent:** "I'm sorry to hear that — thank you for letting me know. Let me pull up your account now and we'll get that sorted. [Follow [[PROC-GEN-CustomerSupport]] fault-handling steps as appropriate.]"

> **[Optional upsell — only if no issues reported and customer is positive]**
> **Agent:** "That's brilliant. While I have you — I noticed you're on our [current plan]. A lot of our [Fibre 100 / 10 GB SIM] customers find that after a couple of weeks they want a bit more speed / data. Is that something you've thought about at all?"
> — *[If yes, continue with [[SCR-OB-BroadbandUpgrade]] or [[SCR-OB-MobileAddOn]] as appropriate]*
> — *[If no, accept graciously — do not push]*

> **[CSAT survey prompt]**
> **Agent:** "Before I let you go, we'll be sending a short text survey in the next hour or so — just two or three questions about your experience. We really do read every response, and it helps us improve. Would that be okay?"

> **Agent (closing):** "Brilliant — thanks so much for your time today, [Customer Name]. It's been great speaking with you. Don't hesitate to get in touch if you ever need anything."

---

## Branching Paths

| Customer Response | Go To |
|-------------------|-------|
| All fine, satisfied | Deliver positive close; optionally introduce upsell |
| Minor issue — can resolve now | Work through [[PROC-GEN-CustomerSupport]] |
| Major issue — ongoing fault | Escalate in CRM; create or link support ticket; book callback |
| Wants to upgrade | [[SCR-OB-BroadbandUpgrade]] |
| Wants to add mobile | [[SCR-OB-MobileAddOn]] |
| Wants to cancel | Do not attempt retention on this call; route to [[PROC-GEN-CustomerCancellation]] |
| Formal complaint | Route to [[PROC-GEN-CustomerSupport]] complaints process |

## Compliance Notes

- **This call must never be used to pressurise a customer** — it is a service call first; upsell is strictly secondary and only appropriate when the customer confirms they are satisfied
- If an issue is raised, the call **must** pivot to resolution — logging it as resolved without attempting to fix it is a breach of [[POL-CON-CodeOfConduct]]
- **Do not send the CSAT survey link without the customer's verbal consent** on this call
- Vulnerability check: if the customer mentions any personal difficulty (bereavement, health, financial stress), follow the vulnerability protocol in [[PROC-GEN-CustomerSupport]] and do **not** continue with any sales activity
- Log outcome in CRM: `SATISFACTION-POSITIVE`, `SATISFACTION-ISSUE-RESOLVED`, `SATISFACTION-ISSUE-ESCALATED`, or `CALLBACK-REQUESTED`

---

## Related

- [[PROC-GEN-CustomerOnboarding]]
- [[PROC-GEN-CustomerSupport]]
- [[SCR-OB-BroadbandUpgrade]]
- [[SCR-OB-MobileAddOn]]
- [[POL-CON-CodeOfConduct]]
- [[POL-DP-DataProtectionAndGDPR]]
