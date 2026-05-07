---
title: Customer Onboarding Procedure
aliases:
  - New Customer Onboarding
  - Post-Sale Onboarding
  - Welcome Call Process
tags:
  - procedure
  - onboarding
  - telecoms
area: general
status: draft
owner: Customer Experience Team Lead
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related-policy: "[POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)"
related:
  - "[POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)"
  - "[PROC-GEN-SalesProcedure](PROC-GEN-SalesProcedure.md)"
  - "[PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md)"
  - "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
  - "[PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)"
  - "[PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)"
  - "[PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md)"
  - "[PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)"
  - "[PROD-ClearWaveX1ProHandset](../Products/PROD-ClearWaveX1ProHandset.md)"
  - "[PROD-ClearWaveX1HandsetBudget](../Products/PROD-ClearWaveX1HandsetBudget.md)"
  - "[PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md)"
  - "[PROD-HomePhone](../Products/PROD-HomePhone.md)"
---

## Purpose

Ensure every new ClearWave customer is successfully set up, informed, and confident using their service within the first 30 days of joining — reducing early-life churn, support contacts, and complaints.

## Scope

All agents in the onboarding team handling post-sale customer contacts for new broadband, mobile SIM, handset, mobile broadband, and home phone customers. Also applies to agents taking inbound calls from customers within their first 30 days.

## Prerequisites

- Access to CRM (Salesforce) — customer record must show confirmed order before onboarding begins
- Access to OMS to check order and installation status
- Familiarity with each active product (see product notes below)
- Identity verification required before discussing any account detail — see [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)

---

## Steps

### 1. Verify Identity and Locate the Account
- Greet the customer and confirm your name and ClearWave
- Verify identity: full name, date of birth, and postcode
- Locate the customer record in CRM; confirm the order reference and product(s) purchased
- Check the order status in OMS before proceeding — know the current state before the customer asks

### 2. Confirm Order Details and Timeline

**For broadband orders ([PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md), [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md), [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)):**
- Confirm the installation appointment date and time window (AM or PM)
- Advise the customer that an engineer will attend the premises; someone aged 18+ must be present
- Explain what to expect on installation day:
  - Engineer checks/activates the Optical Network Terminal (ONT) outside the property
  - Engineer enters the property to connect and test the Smart Hub router
  - Typical visit duration: 1–3 hours
- Confirm the router will be delivered before the installation appointment, or brought by the engineer
- For [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md) customers: confirm the dedicated onboarding specialist call is booked

**For SIM-only orders ([PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md), [PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)):**
- Confirm SIM dispatch date (typically 1–3 working days by first-class post)
- If number porting: confirm the PAC code has been submitted and advise the porting window (typically 1 working day after SIM activation)
- Explain that the customer should not cancel their existing service until porting is confirmed

**For handset orders ([PROD-ClearWaveX1ProHandset](../Products/PROD-ClearWaveX1ProHandset.md), [PROD-ClearWaveX1HandsetBudget](../Products/PROD-ClearWaveX1HandsetBudget.md)):**
- Confirm dispatch and expected delivery date
- Advise on how to activate the device and insert the SIM
- If number porting: same guidance as SIM-only above

**For mobile broadband ([PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md)):**
- Confirm MiFi Hub dispatch date
- Explain device setup: insert SIM (pre-installed), power on, connect via Wi-Fi using credentials on device label

**For home phone add-on ([PROD-HomePhone](../Products/PROD-HomePhone.md)):**
- Confirm the ATA (analogue telephone adapter) will be dispatched with or before the broadband installation
- Remind the customer that the home phone requires the broadband to be active — it will not work before or during broadband outages
- Repeat the **Ofcom VoIP emergency call disclosure**: the service will not work during a power cut or broadband outage; advise the customer to keep a mobile phone available for emergencies
- If the customer has a telecare/medical alarm device: confirm the compatibility check was completed during sale; if not, initiate it now before the service goes live

### 3. Explain Account Management
- Direct the customer to the MyClearWave online account portal and mobile app
- Explain what they can do in self-serve:
  - View and pay bills
  - Monitor data usage (mobile)
  - Report a fault
  - Book an engineer visit
  - Manage add-ons
- Confirm the customer's registered email address for bill notifications and correspondence

### 4. Set Expectations on Billing
- Explain when the first bill will be generated (typically within 30 days of activation; may include a pro-rata first charge)
- Confirm the Direct Debit date
- Advise where to find itemised billing in the MyClearWave portal
- Mention that a paper bill is available on request (subject to a £1.50/month charge)

### 5. Offer a Proactive Support Prompt
- Ask if the customer has any questions about their order or products
- For broadband customers: offer to note any specific concerns for the installation engineer (e.g. preferred router placement, known access issues)
- For mobile customers: offer to walk through the SIM activation steps if needed

### 6. Check for Cooling-Off Intent
- If the customer mentions second thoughts or mentions cancelling within the first 14 days, do not immediately process the cancellation
- Acknowledge their concern, listen actively, and offer to resolve the issue first
- If they wish to proceed with cancellation within the cooling-off period, follow [PROC-GEN-CustomerCancellation](PROC-GEN-CustomerCancellation.md)

### 7. Close and Log
- Summarise next steps and the customer's expected go-live date
- Log all contact in CRM with outcome code: `ONBOARDING-COMPLETE` or `ONBOARDING-PENDING-ISSUE`
- If any issues were identified (e.g. delayed installation, missing equipment), create a follow-up task in CRM with a resolution date

---

## Decision Points

| Situation | Action |
|-----------|--------|
| Installation appointment not yet booked in OMS | Advise the customer; book the appointment or escalate to provisioning team |
| SIM not dispatched within 3 working days of order | Raise a dispatch query with the fulfilment team; do not ask the customer to wait longer |
| Customer has telecare/medical alarm device and compatibility not checked | Do not allow the home phone service to go live until check is completed |
| Customer wants to change the installation appointment | Process via OMS; minimum 48 hours notice required; availability may vary |
| Number port has not completed within 2 working days | Raise a porting escalation; advise the customer; do not tell them to contact their old provider |
| Customer expresses dissatisfaction during onboarding | Log as a complaint; follow [PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md) |
| Customer is within cooling-off period and wants to cancel | Follow [PROC-GEN-CustomerCancellation](PROC-GEN-CustomerCancellation.md) |
| Customer appears vulnerable or in distress | Apply the Vulnerable Customer guidelines; offer additional support time; escalate if required |

## Escalation

- **Provisioning failure** (e.g. installation cannot be completed, OMS error): escalate to the provisioning team; keep the customer informed with a 24-hour update commitment
- **Equipment not delivered before installation appointment**: escalate to the fulfilment team immediately; arrange a re-scheduled installation if needed
- **Complaint**: escalate to the Customer Support team ([PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md)); do not attempt to resolve a formal complaint during an onboarding call
- **Regulatory concern** (e.g. KFI not sent, cooling-off right not communicated at sale): report to Team Leader; do not attempt to remedy without guidance

## Common Errors

- Assuming the installation is booked without checking OMS first
- Failing to repeat the VoIP emergency call disclosure for [PROD-HomePhone](../Products/PROD-HomePhone.md) customers
- Advising a porting customer to cancel their old service before porting is confirmed — this can result in number loss
- Not logging the onboarding contact in CRM, which prevents the follow-up team from knowing the customer has been contacted
- Rushing through the billing explanation — unclear billing is one of the top drivers of early-life complaints

---

## Related

- [PROC-GEN-SalesProcedure](PROC-GEN-SalesProcedure.md)
- [PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md)
- [PROC-GEN-CustomerCancellation](PROC-GEN-CustomerCancellation.md)
- [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)
- [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)
