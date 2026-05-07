---
title: Customer Support Procedure
aliases:
  - Customer Service Process
  - Complaint Handling Procedure
  - Fault Handling Procedure
  - Technical Support Process
tags:
  - procedure
  - customer-support
  - complaints
  - telecoms
area: complaints
status: draft
owner: Customer Support Team Lead
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related-policy: "[[POL-CON-CodeOfConduct]]"
related:
  - "[[POL-DP-DataProtectionAndGDPR]]"
  - "[[POL-DISC-DisciplinaryAndGrievance]]"
  - "[[POL-EDI-EqualityDiversityInclusion]]"
  - "[[PROC-GEN-CustomerCancellation]]"
  - "[[PROD-Fibre100Broadband]]"
  - "[[PROD-Fibre500Broadband]]"
  - "[[PROD-Fibre1000Broadband]]"
  - "[[PROD-SIMOnly10GB5G]]"
  - "[[PROD-SIMOnlyUnlimited5G]]"
  - "[[PROD-MobileBroadband5G]]"
  - "[[PROD-HomePhone]]"
---

## Purpose

Provide consistent, fair, and compliant handling of customer support contacts — covering general queries, service faults, billing disputes, and formal complaints — ensuring every customer receives a resolution or a clear path to one.

## Scope

All customer-facing support agents handling inbound contacts (voice, chat, email) across all ClearWave products and services.

## Prerequisites

- Access to CRM (Salesforce) — all contacts must be logged
- Access to OMS for order and provisioning status
- Access to the fault management system (ServiceNow) for network and service incidents
- Access to the billing system for account and payment queries
- Identity verification required before discussing or amending any account — see [[POL-DP-DataProtectionAndGDPR]]
- Awareness of [[POL-EDI-EqualityDiversityInclusion]]: all customers must be treated with dignity and respect; agents must be alert to vulnerability indicators

---

## Steps

### 1. Verify Identity and Open the Contact
- Greet the customer and confirm your name and ClearWave
- Verify identity: full name, date of birth, and postcode before accessing or discussing the account
- Log the contact in CRM immediately with contact channel and initial reason code
- Check for any open tickets, recent contacts, or flags on the account (e.g. active fault, complaint, vulnerability flag) before the customer explains their issue

### 2. Understand the Issue
- Allow the customer to explain their issue fully before responding
- Ask clarifying questions only when necessary — do not interrupt
- Categorise the contact type:

| Contact Type | Description |
|---|---|
| General query | Account information, billing question, product query |
| Service fault | Broadband outage/slow speed, mobile signal issue, home phone fault |
| Billing dispute | Incorrect charge, Direct Debit issue, disputed ETC |
| Equipment issue | Router fault, SIM issue, handset hardware fault |
| Formal complaint | Customer explicitly uses the word "complaint", or expresses dissatisfaction with ClearWave's handling of a previous issue |

### 3. General Queries

For straightforward account, billing, or product questions:
- Resolve at first contact wherever possible
- Use the relevant product note for product-specific information:

| Product | Note |
|---------|------|
| Fibre broadband | [[PROD-Fibre100Broadband]], [[PROD-Fibre500Broadband]], [[PROD-Fibre1000Broadband]] |
| SIM only | [[PROD-SIMOnly10GB5G]], [[PROD-SIMOnlyUnlimited5G]] |
| Mobile broadband | [[PROD-MobileBroadband5G]] |
| Home phone | [[PROD-HomePhone]] |

- Log the outcome in CRM with code `QUERY-RESOLVED` or `QUERY-ESCALATED`

### 4. Service Fault Handling

**Step 4a: Check for a Known Outage**
- Before troubleshooting, check ServiceNow for any active network incident affecting the customer's area or service
- If a known outage exists: inform the customer of the incident reference, the expected resolution time (if available), and offer a proactive update callback or SMS — do not troubleshoot a network-level outage at agent level

**Step 4b: Basic Troubleshooting**

*Broadband (all fibre products):*
1. Ask the customer to confirm whether all devices are affected or just one
2. Ask the customer to restart the Smart Hub (unplug, wait 60 seconds, replug); wait 2 minutes for full reconnection
3. Check the hub lights: solid white = connected; flashing/red = fault state
4. Run a line test from the diagnostic tools in the billing system — note the result in CRM
5. If the line test shows a fault: raise a network fault ticket in ServiceNow; provide the customer with a ticket reference and a 48-hour resolution commitment
6. If the line test is clear but the customer reports slow speeds: schedule a speed test callback; advise the customer to run a wired speed test at clearwave.co.uk/speedtest and email results

*Mobile (SIM and handset):*
1. Ask whether the issue is calls, data, or both
2. Check network status for the customer's postcode in ServiceNow
3. Ask the customer to toggle aeroplane mode off/on and restart the device
4. Check the account is active and not suspended (billing system)
5. If data issue persists after basic steps: reset APN settings (advise customer on their device OS); if unresolved, arrange SIM replacement

*Home phone ([[PROD-HomePhone]]):*
1. Confirm the broadband service is working first — VoIP depends on broadband
2. Check the ATA is powered and connected to the router
3. Ask the customer to restart the ATA (unplug, wait 30 seconds, replug)
4. If fault persists: raise a VoIP fault ticket in ServiceNow; 48-hour resolution commitment

**Step 4c: Engineer Visit**
- If remote troubleshooting does not resolve the fault within one contact, offer an engineer visit
- Book via OMS; available slots typically within 3–5 working days
- Advise the customer: if the engineer finds the fault is customer-caused (e.g. damaged equipment, internal wiring), a £65.00 engineer visit charge will apply
- If the fault is on ClearWave's network or equipment: no charge

### 5. Billing Dispute Handling
- Pull up the customer's bill in the billing system and review the queried charge with the customer
- For direct debit failures or missed payments: check the reason code; do not lecture the customer; offer a payment arrangement if the account is in arrears
- For disputed charges:
  - If the charge is clearly an error: apply a credit immediately; apologise; log in CRM as `BILLING-CREDIT-APPLIED`
  - If the charge is correct but the customer disputes it: explain the charge clearly; provide the relevant contract reference; if they still dispute, raise a formal billing query (see Formal Complaint below)
- For ETC disputes arising from cancellation: refer to [[PROC-GEN-CustomerCancellation]]

### 6. Formal Complaint Handling

A contact becomes a **formal complaint** when:
- The customer explicitly uses the word "complaint"
- The customer expresses dissatisfaction with how ClearWave has handled a previous issue
- The agent judges the situation meets the severity threshold (e.g. repeated failures, financial detriment, vulnerability involved)

**Step 6a: Acknowledge the Complaint**
- Acknowledge the complaint clearly: *"I'm sorry to hear about this. I want to make sure this is treated as a formal complaint so it gets the attention it deserves."*
- Do not minimise or dismiss the customer's experience
- Assign a complaint reference number from CRM and provide it to the customer

**Step 6b: Log and Classify**
- Log in CRM with category code (see taxonomy) and priority:
  - **Standard**: resolution target **5 working days**
  - **Priority** (vulnerability, financial detriment, repeated failure): resolution target **2 working days**
- Set a callback date within the target resolution window

**Step 6c: Investigate**
- Review all relevant CRM history, ServiceNow tickets, call recordings, and billing records
- Do not rely on the customer to prove their case — the burden of investigation is on ClearWave
- Where a call recording is relevant, request it via the quality team within 24 hours

**Step 6d: Resolve and Respond**
- Contact the customer within the target resolution window with a clear outcome:
  - What was found
  - What ClearWave will do (credit, fix, apology, process change)
  - What the customer can do if they remain unhappy (see Escalation below)
- Send a written summary to the customer's registered email address
- Log outcome in CRM as `COMPLAINT-RESOLVED` or `COMPLAINT-DEADLOCKED`

---

## Decision Points

| Situation | Action |
|-----------|--------|
| Known network outage in the customer's area | Inform; provide ticket ref and ETA; do not troubleshoot at agent level |
| Customer is in evident distress or vulnerability | Slow down; offer extra time; apply vulnerability flag to CRM; escalate if risk to welfare |
| Customer is abusive | Follow [[POL-CON-CodeOfConduct]]; two verbal warnings permitted; call may be ended; log in CRM |
| Fault not resolved after 14+ days | Escalate to Network Operations; customer may be eligible for a service credit or contract exit |
| Billing error is confirmed | Apply credit immediately; apologise; no authorisation required for credits under £50 |
| Billing credit exceeds £50 | Team Leader authorisation required |
| Customer threatens Ofcom / ADR referral | Acknowledge their right; provide the Deadlock Letter process details (see below) |
| Complaint not resolved within target window | Escalate to Team Leader; contact the customer proactively with an update |
| Customer refuses all resolution offers | Issue a **Deadlock Letter** — this enables the customer to escalate to the Ombudsman Services |

## Escalation

- **Unresolved faults (14+ days)**: escalate to Network Operations Manager with full ticket history
- **Complaint not resolved within target**: escalate to Customer Support Team Lead
- **Deadlock / Ombudsman referral**: issue a Deadlock Letter (template in CRM document library); advise the customer they may refer to **Ombudsman Services: Communications** — this is a regulatory requirement under Ofcom's ADR (Alternative Dispute Resolution) scheme
- **Safeguarding concern** (e.g. customer mentions risk to themselves or others): follow the company safeguarding procedure; escalate to the Safeguarding Lead immediately
- **Regulatory breach identified** (e.g. sale made without KFI, cooling-off right not explained): report to Team Leader; do not attempt to resolve independently

## Common Errors

- Not checking for a known outage before troubleshooting — this wastes the customer's time and creates frustration
- Failing to assign a complaint reference number immediately — the customer cannot follow up without it
- Attempting to close a formal complaint informally to avoid logging it — this is a conduct issue under [[POL-CON-CodeOfConduct]]
- Missing the complaint resolution target without proactively contacting the customer — silent failures drive Ombudsman referrals
- Applying a billing credit without logging it — credits must always be recorded in CRM and the billing system
- Not flagging vulnerability in CRM — subsequent agents will not know and may not adapt their approach appropriately

---

## Related

- [[PROC-GEN-CustomerCancellation]]
- [[PROC-GEN-SalesProcedure]]
- [[PROC-GEN-CustomerOnboarding]]
- [[POL-CON-CodeOfConduct]]
- [[POL-DP-DataProtectionAndGDPR]]
- [[POL-EDI-EqualityDiversityInclusion]]
- [[POL-DISC-DisciplinaryAndGrievance]]
