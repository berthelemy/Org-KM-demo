---
name: obsidian-markdown
description: 'Create or update Obsidian-flavoured markdown files with correct YAML frontmatter properties. Use when authoring new notes for Policies, Procedures, Products, or Scripts folders in this vault, or when adding/fixing YAML properties on existing notes. Understands Obsidian property types (text, list, date, link, checkbox), wikilink syntax, tags, aliases, and the bases plugin.'
argument-hint: 'Note type and title, e.g. "Policy: Data Retention" or "Script: Card Payment Handling"'
---

# Obsidian Markdown Note Authoring

## When to Use
- Creating a new note in `Policies/`, `Procedures/`, `Products/`, or `Scripts/`
- Adding or correcting YAML frontmatter on an existing note
- Ensuring notes are queryable via the Obsidian Bases plugin
- Linking notes together with wikilinks

## Note Types & Schemas

Load the appropriate template from the assets folder for the note type requested:

| Note Type | Template | Save Folder |
|-----------|----------|-------------|
| Policy | [policy-template.md](./assets/policy-template.md) | `Policies/` |
| Procedure | [procedure-template.md](./assets/procedure-template.md) | `Procedures/` |
| Product | [product-template.md](./assets/product-template.md) | `Products/` |
| Script | [script-template.md](./assets/script-template.md) | `Scripts/` |

For full property definitions and valid values, see [property-schemas.md](./references/property-schemas.md).

---

## Authoring Procedure

### 1. Identify Note Type
Determine which folder the note belongs to based on the content:
- **Policy** — organisational rules, standards, entitlements (e.g. Attendance Policy)
- **Procedure** — step-by-step operational instructions (e.g. How to Handle a Complaint)
- **Product** — product or service information (e.g. Home Insurance)
- **Script** — call scripts, objection handling, openers/closers

### 2. Load the Template
Copy the relevant template (see table above). Do not leave any template placeholder unfilled — replace every `<placeholder>` value.

### 3. Complete YAML Frontmatter
- All property names must be **lowercase with hyphens** (no underscores, no camelCase)
- `tags:` must be a YAML list — never a bare string
- `date` properties must use **ISO 8601** format: `YYYY-MM-DD`
- Wikilinks in properties use double-bracket syntax: `"[[Note Title]]"`
- Multi-value link properties are YAML lists of quoted wikilinks
- Leave no property value blank — use `""` for unknown text, `[]` for unknown lists, or omit optional properties entirely
- `review-due:` must always be set — maximum 2 years from `created:`

### 4. File Naming Convention
Use the following naming conventions:

| Type | Pattern | Example |
|------|---------|---------|
| Policy | `POL-<AREA>-<ShortTitle>.md` | `POL-ATT-AttendanceAndPunctuality.md` |
| Procedure | `PROC-<AREA>-<ShortTitle>.md` | `PROC-COMP-ComplaintHandling.md` |
| Product | `PROD-<ShortTitle>.md` | `PROD-HomeInsurance.md` |
| Script | `SCR-<TYPE>-<ShortTitle>.md` | `SCR-OBJ-PriceObjection.md` |

Area codes for Policies and Procedures:

| Code | Area |
|------|------|
| ATT | Attendance |
| CON | Conduct |
| PERF | Performance |
| ABS | Absence |
| DISC | Disciplinary |
| DP | Data Protection |
| SCH | Schedule |
| HS | Health & Safety |
| EDI | Equality & Inclusion |
| AU | Acceptable Use |
| COMP | Complaints |
| GEN | General |

### 5. Wikilinks in Body Text
- Link to related notes using `[[Note Title]]` or `[[Note Title|Display Text]]`
- Link to headings within a note: `[[Note Title#Section Heading]]`
- Link to related policies/procedures at the bottom of every note in a **Related** section

### 6. Tags
- Always include the note-type tag as the **first tag**: `policy`, `procedure`, `product`, or `script`
- Add one or more area/topic tags after the type tag (e.g. `HR`, `attendance`, `data-protection`)
- Tags must be lowercase, hyphenated — no spaces, no hash symbols in the YAML block

### 7. Add Link to Welcome Page
After saving the note, **always** add a wikilink to it in [Welcome.md](../../../Welcome.md).

- Open `Welcome.md`
- Find the section that matches the note type (`## Procedures`, `## Products`, `## Policies`, or `## Scripts`)
- For Products, also find the correct sub-heading (e.g. `### Broadband`, `### Mobile`, `### Handsets`) — add a new sub-heading if the category does not yet exist
- Add a new line in the correct section using the format:
  ```
  - [[FILENAME|Human Readable Title]]
  ```
- If the note type section does not exist yet in `Welcome.md`, add it following the existing section pattern

### 8. Review Checklist
Before saving:
- [ ] All `<placeholder>` values replaced
- [ ] `created:` date set to today
- [ ] `review-due:` set (≤ 2 years from created)
- [ ] `status:` is a valid value (not left as placeholder)
- [ ] `tags:` is a list, not a bare string
- [ ] All wikilinks reference notes that exist or will exist in this vault
- [ ] File name follows the naming convention for the note type
- [ ] Saved to the correct folder
- [ ] Link added to the correct section of `Welcome.md`
