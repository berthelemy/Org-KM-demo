---
title: Sales Procedure
aliases:
  - New Sale Process
  - Outbound Sales Process
  - Inbound Sales Process
tags:
  - procedure
  - sales
  - telecoms
area: general
status: draft
owner: Sales Team Lead
version: "1.0"
created: 2026-05-07
reviewed: 2026-05-07
review-due: 2028-05-07
related-policy: "[POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)"
related:
  - "[POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)"
  - "[POL-PERF-PerformanceManagement](../Policies/POL-PERF-PerformanceManagement.md)"
  - "[PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md)"
  - "[PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md)"
  - "[PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)"
  - "[PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md)"
  - "[PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md)"
  - "[PROD-ClearTelComCoX1ProHandset](../Products/PROD-ClearTelComCoX1ProHandset.md)"
  - "[PROD-ClearTelComCoX1HandsetBudget](../Products/PROD-ClearTelComCoX1HandsetBudget.md)"
  - "[PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md)"
  - "[PROD-HomePhone](../Products/PROD-HomePhone.md)"
  - "[PROC-CustomerOnboarding](PROC-CustomerOnboarding.md)"
license: "CC BY-NC 4.0"
---

## Purpose

Guide agents through a compliant, customer-centred sale of any ClearTelComCo product — broadband, mobile SIM, handset, mobile broadband, or home phone — from initial contact to confirmed order.

## Scope

All inbound and outbound sales agents handling new customer acquisitions or existing customer upgrades/additions.

## Prerequisites

- Access to the CRM (Salesforce) and the order management system (OMS)
- Completed product training for all products in scope
- Access to the live coverage checker tool
- Familiarity with [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md) — identity verification is mandatory before discussing or amending any account
- Key Facts Indicator (KFI) documents available in the document library for all regulated products

---

## Steps

### 1. Open the Call and Verify Identity

- Greet the customer warmly and confirm your name and that you are calling from ClearTelComCo
- For inbound calls: confirm the customer's full name, date of birth, and postcode against the CRM record before proceeding
- For outbound calls: state the purpose of the call clearly; do not misrepresent the reason for contact
- Log the call start in CRM

> **Data Protection**: Never discuss account details until identity is verified. If the caller fails verification, offer them the option to call back with the correct details. Do not proceed.  
> See [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)

### 2. Understand the Customer's Needs

- Ask open questions to understand the customer's current situation and requirements:
  - Current provider and contract status
  - Household size and usage habits (for broadband)
  - Number of lines / devices (for mobile)
  - Key pain points with their current service
- Listen actively; do not jump to a product recommendation before understanding the need

### 3. Run an Availability Check

- For broadband products: run the coverage checker using the customer's full postcode before recommending any fibre product
  - If FTTP is not available at the address, do not sell [PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md), [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md), or [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md)
- For mobile products: check 5G coverage at the customer's most-used locations if they are on a 5G plan
- Record the availability check result in CRM

### 4. Recommend a Product

- Recommend the product that best fits the customer's stated needs — not the highest-value product
- Present key features and benefits relevant to the customer's situation (not a full product recital)
- Quote the correct price including any current promotions; refer to the live pricing tool — do not quote from memory
- Refer to the relevant product note for full details:

| Product | Note |
| --------- | ------ |
| Fibre broadband | [PROD-Fibre100Broadband](../Products/PROD-Fibre100Broadband.md), [PROD-Fibre500Broadband](../Products/PROD-Fibre500Broadband.md), [PROD-Fibre1000Broadband](../Products/PROD-Fibre1000Broadband.md) |
| SIM only | [PROD-SIMOnly10GB5G](../Products/PROD-SIMOnly10GB5G.md), [PROD-SIMOnlyUnlimited5G](../Products/PROD-SIMOnlyUnlimited5G.md) |
| Handsets | [PROD-ClearTelComCoX1ProHandset](../Products/PROD-ClearTelComCoX1ProHandset.md), [PROD-ClearTelComCoX1HandsetBudget](../Products/PROD-ClearTelComCoX1HandsetBudget.md) |
| Mobile broadband | [PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md) |
| Home phone | [PROD-HomePhone](../Products/PROD-HomePhone.md) |

### 5. Handle Objections

- Use the objection-handling table in the relevant product note as a guide
- Never use pressure tactics, false urgency, or misleading comparisons
- If a customer is unsure, offer to send information by email and agree a callback time — do not push for an immediate decision
- Comply with [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md): do not make promises outside authorised product terms

### 6. Present the Key Facts Indicator (KFI)

- For all broadband and mobile contract sales, the KFI **must** be provided before the order is confirmed
- For remote sales: email the KFI document to the customer's registered email address and confirm receipt before proceeding
- Record KFI sent/confirmed in CRM — this is a regulatory requirement and will be audited

### 7. Complete the Credit Check (where applicable)

- Handset contracts and 12-month mobile plans require a credit check
- Explain to the customer that a credit check will be performed (soft or hard as applicable — see product note)
- Record consent in CRM before running the check
- If the credit check fails: advise the customer politely; do not speculate on the reason; offer a SIM-only or rolling monthly alternative where appropriate

### 8. Confirm the Order

- Read back the key order details: product, price, contract length, start date, and any upfront costs
- Confirm the customer's billing address, payment method, and Direct Debit details (where applicable)
- For broadband: confirm the installation appointment date and time window
- For number ports (mobile or home phone): take the PAC or STAC code; advise the expected porting timeframe
- Create the order in OMS and confirm the order reference number to the customer

### 9. Communicate the Cooling-Off Period

- Remind the customer of their **14-day cooling-off right** for all remotely sold contracts
- Explain how to cancel within the cooling-off period (phone or written notice to ClearTelComCo)
- This must be communicated verbally and is included in the order confirmation email automatically sent by OMS

### 10. Close and Hand Off

- Summarise next steps for the customer (installation date, SIM dispatch, number port timeline)
- Ask if there is anything else the customer needs
- Transfer to onboarding if required (see [PROC-CustomerOnboarding](PROC-CustomerOnboarding.md)) or confirm that the confirmation email and welcome pack will follow
- Log call outcome and order details in CRM; set a follow-up task if applicable

---

## Decision Points

| Situation | Action |
| ----------- | -------- |
| Customer fails identity verification | Do not proceed; offer callback |
| FTTP not available at address | Do not sell fibre products; discuss [PROD-MobileBroadband5G](../Products/PROD-MobileBroadband5G.md) as alternative |
| Customer is in contract with another provider | Note end date; offer to call back; do not encourage breach of contract |
| Credit check fails | Offer rolling/SIM-only alternatives; do not speculate on reason for failure |
| Customer requests time to consider | Send KFI by email, agree callback date, log in CRM |
| Customer mentions vulnerability (financial difficulty, health) | Follow the Vulnerable Customer procedure; do not pressure |
| Customer wants to add home phone | Check compatibility and present [PROD-HomePhone](../Products/PROD-HomePhone.md); deliver Ofcom VoIP emergency call disclosure |
| Handset sale involves trade-in | Direct customer to ClearTelComCo.co.uk/trade-in for valuation; do not guarantee a trade-in value verbally |

## Escalation

- **Pricing queries outside standard rate card**: escalate to Team Leader — do not offer ad-hoc discounts without authorisation
- **Customer complaint during sale**: stop the sales process; follow the Customer Support procedure ([PROC-CustomerSupport](PROC-CustomerSupport.md))
- **Suspected fraud** (e.g. identity details don't match, unusual payment details): do not proceed; escalate immediately to the Fraud team and log in CRM
- **Regulatory breach** (e.g. KFI not provided, credit consent not obtained): self-report to Team Leader immediately; do not attempt to resolve without guidance

## Common Errors

- Quoting prices from memory rather than the live pricing tool — always use the tool
- Skipping the KFI step because the customer says "just get on with it" — this is non-negotiable
- Running a hard credit check without explicit customer consent
- Describing 5G as available everywhere — always check coverage at the customer's specific location
- Describing the [PROD-HomePhone](../Products/PROD-HomePhone.md) VoIP service as working during power cuts — it does not

---

## Related

- [PROC-CustomerOnboarding](PROC-CustomerOnboarding.md)
- [PROC-CustomerSupport](PROC-CustomerSupport.md)
- [POL-CON-CodeOfConduct](../Policies/POL-CON-CodeOfConduct.md)
- [POL-DP-DataProtectionAndGDPR](../Policies/POL-DP-DataProtectionAndGDPR.md)
- [POL-PERF-PerformanceManagement](../Policies/POL-PERF-PerformanceManagement.md)
