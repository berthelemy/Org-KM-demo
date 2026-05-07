---
name: call-centre-hr-policies
description: 'HR policy authoring and review for call centre operations. Use when creating, updating, or answering questions about HR policies covering attendance, performance, conduct, data protection, scheduling, absence management, disciplinary procedures, or agent welfare in a contact centre or call centre environment.'
argument-hint: 'Policy name or topic (e.g. attendance, conduct, performance, data protection)'
---

# Call Centre HR Policies

## When to Use
- Drafting a new HR policy document for a call centre
- Reviewing or updating an existing policy
- Answering questions about expected standards or entitlements
- Onboarding materials that reference HR rules and norms
- Manager guidance on handling employee situations

## Policy Areas Covered

| Policy Area | Reference |
|---|---|
| Attendance & Punctuality | [POL-ATT-AttendanceAndPunctuality.md](../../../Policies/POL-ATT-AttendanceAndPunctuality.md) |
| Code of Conduct | [POL-CON-CodeOfConduct.md](../../../Policies/POL-CON-CodeOfConduct.md) |
| Performance Management | [POL-PERF-PerformanceManagement.md](../../../Policies/POL-PERF-PerformanceManagement.md) |
| Absence & Sickness | [POL-ABS-AbsenceAndSickness.md](../../../Policies/POL-ABS-AbsenceAndSickness.md) |
| Disciplinary & Grievance | [POL-DISC-DisciplinaryAndGrievance.md](../../../Policies/POL-DISC-DisciplinaryAndGrievance.md) |
| Data Protection & GDPR | [POL-DP-DataProtectionAndGDPR.md](../../../Policies/POL-DP-DataProtectionAndGDPR.md) |
| Schedule Adherence | [POL-SCH-ScheduleAdherence.md](../../../Policies/POL-SCH-ScheduleAdherence.md) |
| Health, Safety & Wellbeing | [POL-HS-HealthSafetyAndWellbeing.md](../../../Policies/POL-HS-HealthSafetyAndWellbeing.md) |
| Equality, Diversity & Inclusion | [POL-EDI-EqualityDiversityInclusion.md](../../../Policies/POL-EDI-EqualityDiversityInclusion.md) |
| Acceptable Use of Technology | [POL-AU-AcceptableUseOfTechnology.md](../../../Policies/POL-AU-AcceptableUseOfTechnology.md) |

---

## Authoring Procedure

Follow these steps whenever drafting or updating a policy:

### 1. Identify Policy Scope
- Confirm which policy area is needed (see table above)
- Load the relevant reference file for standards, triggers, and example language
- Confirm whether this is a **new** policy or an **amendment** to an existing one

### 2. Apply Standard Policy Structure
Every call centre HR policy document must contain these sections (in order):

```
1. Purpose
2. Scope (who it applies to — agents, team leaders, support staff)
3. Policy Statement
4. Definitions (key terms)
5. Procedure / Standards
6. Manager Responsibilities
7. Employee Rights & Responsibilities
8. Non-Compliance Consequences
9. Review Date
10. Document Owner
```

### 3. Call Centre–Specific Considerations
When authoring, apply these context-specific checks:

- **Shift patterns**: Policies must account for rotating shifts, 24/7 operations, and split-shift teams
- **Metrics language**: Where performance is referenced, use KPI names consistent with the contact centre (AHT, CSAT, FCR, adherence %)
- **Data sensitivity**: All policies involving customer interaction must reference GDPR obligations
- **Trade union / works council**: Flag any policy that touches pay, discipline, or significant working condition changes as requiring consultation
- **Accessibility**: Policy documents must be available in accessible formats

### 4. Tone & Language Standards
- Plain English: reading age target of 12–14 years
- Active voice preferred
- Avoid legal jargon — where legal terms are necessary, define them in the Definitions section
- Gender-neutral language throughout
- Use "team member" or "agent" rather than "employee" where the organisation prefers it

### 5. Format as Obsidian Note
Once the policy content is complete, invoke the **obsidian-markdown** skill to produce the final file:

> Use the `obsidian-markdown` skill with note type **Policy** to wrap the content in the correct YAML frontmatter and apply vault conventions before saving.

Key frontmatter values to supply:
- `title:` — full policy title
- `area:` — use the area code table in the obsidian-markdown skill (e.g. `attendance`, `data-protection`)
- `owner:` — document owner (person or team)
- `status:` — `draft` on first creation; `approved` once signed off
- `created:` — today's date
- `review-due:` — maximum 2 years from today
- `related:` — wikilinks to related policies or procedures in this vault

### 6. Review Checklist
Before saving a final policy:
- [ ] All 10 structural sections present
- [ ] Review date set (maximum 2 years from creation)
- [ ] Named document owner confirmed
- [ ] Checked against relevant reference file for completeness
- [ ] GDPR relevance assessed
- [ ] Shift/scheduling nuances addressed where applicable
- [ ] Tone and language standards met
- [ ] YAML frontmatter complete and valid (all `<placeholder>` values replaced)
- [ ] `tags:` is a YAML list starting with `policy`
- [ ] All wikilinks in `related:` use `"[[...]]"` quoted syntax

### 7. Save Location
Save completed policies to `/Policies/` in this workspace, using the naming convention:
`POL-<AREA>-<ShortTitle>.md`
Example: `POL-ATT-AttendanceAndPunctuality.md`

---

## Quick-Reference: Common Policy Triggers

| Situation | Policy to Apply |
|---|---|
| Agent repeatedly late to shift | Attendance & Punctuality → triggers Disciplinary |
| Agent handling customer card data | Data Protection & GDPR |
| Agent on long-term sick leave | Absence & Sickness |
| Complaint about manager behaviour | Code of Conduct + Grievance |
| Agent failing to meet call quality targets | Performance Management |
| Agent disputes their schedule | Schedule Adherence |
| Workplace harassment reported | EDI + Disciplinary & Grievance |
