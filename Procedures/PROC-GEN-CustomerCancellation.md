---
title: Customer Cancellation Procedure
aliases:
  - Cancellation Process
  - Churn Procedure
  - Retention Process
  - Cooling-Off Cancellation
tags:
  - procedure
  - cancellation
  - retention
  - telecoms
area: general
status: draft
owner: Retention Team Lead
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related-policy: "[POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)"
related:
  - "[POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)"
  - "[POL-DISC-DisciplinaryAndGrievance](../Policies/POL-DISC-DisciplinaryAndGrievance.md)"
  - "[PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md)"
  - "[PROC-GEN-SalesProcedure](PROC-GEN-SalesProcedure.md)"
  - "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
  - "[PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)"
  - "[PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)"
  - "[PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md)"
  - "[PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)"
  - "[PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md)"
  - "[PROD-HomePhone](../Products/PROD-HomePhone.md)"
---

## Purpose

Handle customer cancellation requests fairly, compliantly, and with genuine care — whether the customer is within the cooling-off period, in contract, or at end of contract — while making appropriate and non-pressurising retention offers where relevant.

## Scope

All agents handling inbound cancellation requests, retentions, and disconnections across all ClearWave products and customer types.

## Prerequisites

- Access to CRM (Salesforce) to locate the account and log the interaction
- Access to OMS to check contract end dates and active services
- Access to the current retention offers tool (live offers change regularly — do not use offers from memory)
- Identity verification required before any account action — see [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)
- Familiarity with [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md): agents must not use pressure tactics, create false urgency, or obstruct a customer's right to cancel

---

## Steps

### 1. Verify Identity and Locate the Account

- Greet the customer and confirm your name and ClearWave
- Verify identity: full name, date of birth, and postcode
- Locate the account in CRM; note all active products and contract status (in-contract end date, or rolling)

### 2. Acknowledge and Listen

- Acknowledge the cancellation request without challenging it immediately
- Ask one open question to understand the reason: *"To help me with your request, could I ask what's prompted you to cancel today?"*
- Listen without interrupting; log the cancellation reason in CRM (use the reason code taxonomy)
- Do not begin a retention pitch before you understand the customer's situation

### 3. Determine Cancellation Type

| Type | Criteria | Key Considerations |
| ------ | ---------- | -------------------- |
| Cooling-off cancellation | Within 14 calendar days of contract start | No early termination charge; must be processed immediately on request |
| End-of-contract cancellation | Contract term complete, or rolling monthly | No charge; 30 days notice standard for monthly rolling products |
| Mid-contract cancellation | Customer is within a fixed-term contract | Early termination charges apply; must be clearly communicated |
| Service fault-driven cancellation | Customer citing ongoing unresolved fault | Check CRM for open fault tickets; may be eligible for no-fault exit — see Decision Points |

### 4. Communicate Charges (Mid-Contract Only)

- If the customer is mid-contract, calculate and clearly state the early termination charge (ETС) before any further discussion
- Formula: `ETC = remaining months × monthly charge`
- Do not obscure or delay disclosing the ETC — the customer has a right to know this before making a decision
- If the ETC is disputed, do not waive it without Team Leader authorisation

### 5. Make a Retention Offer (Where Appropriate)

- Only make a retention offer **after** understanding the cancellation reason — the offer must be relevant to the reason given
- Consult the live retention offers tool for current approved offers
- Present the offer once, clearly and honestly; do not repeat it if the customer declines

> **Conduct requirement**: agents must not use pressure tactics, countdown timers, or false claims about offer availability. A customer who says "no" to a retention offer must be respected.  
> See [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)

**Common retention approaches by reason:**

| Cancellation Reason | Possible Retention Approach |
| -------------------- | ----------------------------- |
| Price — too expensive | Check for a lower-tier product (e.g. [PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md) vs [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)); offer a loyalty discount if available |
| Moving house | Check if ClearWave coverage is available at the new address; offer a house move transfer |
| Unhappy with speed / service | Check for unresolved fault tickets; offer an engineer visit or temporary credit |
| Switching to a competitor | Ask what the competitor is offering; match or contextualise where possible — do not disparage the competitor |
| No longer needs the service | Acknowledge; a pause/suspension may be available for up to 3 months on some products |
| Bereavement / account holder deceased | Transfer immediately to the Bereavement team; do not attempt retention |

### 6. Process the Cancellation (if proceeding)

**Cooling-off cancellation:**
- Process immediately; no questions or barriers
- Confirm the end date (14-day cooling-off expires at midnight on day 14 from contract start)
- For broadband: cancel the installation appointment via OMS; notify the provisioning team
- For SIM/handset: initiate the returns process; provide the Freepost returns label reference
- Confirm no charges will be applied; log in CRM as `CANCEL-COOLING-OFF`

**End-of-contract / rolling cancellation:**
- Confirm the 30-day notice period; provide the exact service end date
- For broadband: equipment return instructions (Smart Hub must be returned within 14 days of service end; failure to return incurs a £49.99 fee)
- For SIM/handset: service ends at end of notice period; SIM can be retained but becomes inactive
- Provide a PAC code (mobile) or STAC code (if porting away) if requested — must be provided within 1 working day of request, by law
- Log in CRM as `CANCEL-END-OF-CONTRACT`

**Mid-contract cancellation (ETC agreed):**
- Confirm the ETC and the customer's acceptance in CRM before processing
- Do not process if the customer disputes the ETC — escalate to Team Leader
- Process the cancellation in OMS; confirm the service end date
- Provide equipment return instructions if applicable
- Log in CRM as `CANCEL-MID-CONTRACT`

### 7. Confirm and Close

- Confirm the cancellation details in writing: service end date, any charges, equipment return requirements
- OMS will trigger an automated confirmation email — advise the customer to expect it within 1 hour
- Ask if there is anything else the customer needs
- Thank the customer for being with ClearWave
- Log the full interaction in CRM with reason code and outcome

---

## Decision Points

| Situation | Action |
| ----------- | -------- |
| Customer is within cooling-off period | Process immediately; no ETC; no retention pressure |
| Customer cites an unresolved service fault as reason | Check CRM for open tickets; if a fault is open for >14 days, escalate to Team Leader — customer may be eligible for a no-fault contract exit |
| Customer requests a PAC or STAC code | Provide within 1 working day (legal obligation); log request in CRM |
| Account holder is deceased | Do not continue with standard cancellation; transfer to Bereavement team immediately |
| Customer is aggressive or abusive during the call | Follow [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md); agents may end the call if abuse continues; log in CRM |
| Customer has a ClearWave Protect or add-on insurance claim in progress | Note this; cancellation of the base product may affect the claim — advise the customer to contact the claims team before proceeding |
| ETC is disputed | Do not waive without Team Leader authorisation; escalate |
| Customer requests immediate same-day cancellation (mid-contract) | Not available for fixed-term contracts outside cooling-off; standard notice applies |
| House move — new address is in ClearWave coverage | Offer a house move transfer before processing as a cancellation |

## Escalation

- **Disputed ETC**: escalate to Team Leader; do not process or waive without authorisation
- **Service fault-driven exit** (potential no-fault exit): escalate to Team Leader with fault ticket reference
- **Formal complaint** lodged during cancellation: follow [PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md); do not attempt to resolve informally
- **Suspected fraudulent cancellation request** (e.g. caller cannot verify identity but requests immediate cancellation): do not proceed; escalate to the Fraud team
- **Bereavement**: transfer to Bereavement team; do not handle within this procedure

## Common Errors

- Attempting retention before understanding the cancellation reason — this creates an adversarial tone
- Failing to disclose the ETC clearly upfront during a mid-contract cancellation
- Delaying or refusing to provide a PAC/STAC code — this is a legal obligation with a 1 working day deadline
- Applying a cooling-off cancellation charge — there must be no charge within 14 days
- Not logging the cancellation reason code in CRM — this data is used for churn analysis and performance management
- Attempting to retain a customer who has cited bereavement — always transfer

---

## Related

- [PROC-GEN-CustomerSupport](PROC-GEN-CustomerSupport.md)
- [PROC-GEN-SalesProcedure](PROC-GEN-SalesProcedure.md)
- [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)
- [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)
- [POL-DISC-DisciplinaryAndGrievance](../Policies/POL-DISC-DisciplinaryAndGrievance.md)
