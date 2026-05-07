# Obsidian Property Schemas — Reference

## Obsidian Property Types

Obsidian's Properties panel (and Bases plugin) infers or assigns each property a type. Use the right value format to ensure correct typing.

| Obsidian Type | YAML Format | Example |
|---|---|---|
| Text | Bare string or quoted string | `owner: HR Team` |
| List | YAML list (`- item`) | `tags:\n  - policy` |
| Number | Unquoted number | `version: 1` |
| Checkbox | `true` or `false` | `archived: false` |
| Date | `YYYY-MM-DD` (quoted or unquoted) | `created: 2026-05-07` |
| Date & time | `YYYY-MM-DDTHH:mm` | `created: 2026-05-07T09:30` |
| Link (single) | `"[[Note Title]]"` | `related-policy: "[[ATT Policy]]"` |
| Links (multiple) | List of `"[[Note Title]]"` | `related:\n  - "[[Note A]]"` |

> Always quote wikilink values to prevent YAML parsing errors on the `[` character.

---

## Shared Properties (All Note Types)

| Property | Type | Required | Valid Values / Notes |
|---|---|---|---|
| `title` | text | yes | Human-readable title; may differ from filename |
| `aliases` | list | optional | Alternative names; used by Obsidian switcher |
| `tags` | list | yes | See tag conventions below |
| `status` | text | yes | See per-type valid values below |
| `owner` | text | yes | Team or named person responsible |
| `version` | text | yes | Semantic version string, e.g. `"1.0"` |
| `created` | date | yes | ISO 8601: `YYYY-MM-DD` |
| `reviewed` | date | yes | Date of last review; set to `created` date on first draft |
| `review-due` | date | yes | Must be ≤ 2 years after `created` |
| `related` | links | optional | List of `"[[Note]]"` wikilinks to related notes |

---

## Policy Properties

| Property | Type | Required | Valid Values |
|---|---|---|---|
| `area` | text | yes | `attendance` · `conduct` · `performance` · `absence` · `disciplinary` · `data-protection` · `schedule-adherence` · `health-safety` · `edi` · `acceptable-use` · `general` |
| `status` | text | yes | `draft` · `review` · `approved` · `retired` |

**Tag conventions for policies:**
```yaml
tags:
  - policy
  - HR
  - <area>        # e.g. attendance, data-protection
```

---

## Procedure Properties

| Property | Type | Required | Valid Values |
|---|---|---|---|
| `area` | text | yes | Same area codes as Policy |
| `status` | text | yes | `draft` · `review` · `approved` · `retired` |
| `related-policy` | link | recommended | `"[[Parent Policy Note]]"` — the policy this procedure implements |

**Tag conventions for procedures:**
```yaml
tags:
  - procedure
  - <area>        # e.g. complaints, data-protection
```

---

## Product Properties

| Property | Type | Required | Valid Values |
|---|---|---|---|
| `product-type` | text | yes | `insurance` · `savings` · `loan` · `current-account` · `investment` · `utility` · `telecoms` · `other` |
| `status` | text | yes | `active` · `discontinued` · `coming-soon` · `suspended` |
| `launched` | date | yes | Date product became available |
| `discontinued` | date | optional | Date product was withdrawn; leave `""` if still active |
| `provider` | text | yes | Brand or provider name |

**Tag conventions for products:**
```yaml
tags:
  - product
  - <product-type>     # e.g. insurance, savings
  - <brand-tag>        # e.g. if multi-brand operation
```

---

## Script Properties

| Property | Type | Required | Valid Values |
|---|---|---|---|
| `script-type` | text | yes | `inbound` · `outbound` · `objection-handling` · `complaint` · `transfer` · `verification` · `opening` · `closing` · `upsell` |
| `product` | link | recommended | `"[[Product Note]]"` — the product this script relates to |
| `status` | text | yes | `draft` · `approved` · `retired` |

**Tag conventions for scripts:**
```yaml
tags:
  - script
  - <script-type>      # e.g. objection-handling, complaint
  - <product-tag>      # e.g. home-insurance
```

---

## Tag Conventions Summary

- All tags **lowercase**, words separated by **hyphens**
- No `#` symbols inside the YAML block (only used in body text)
- First tag always identifies the note type: `policy`, `procedure`, `product`, `script`
- Subsequent tags add area/topic context — these power the Bases plugin filters

### Example: approved HR policy
```yaml
tags:
  - policy
  - HR
  - attendance
```

### Example: active inbound sales script
```yaml
tags:
  - script
  - inbound
  - upsell
  - home-insurance
```

---

## Bases Plugin Compatibility

The Bases plugin queries properties as structured data. To ensure notes appear correctly in Base views:

- `status`, `area`, `script-type`, `product-type` should be **consistent text values** (not free-text variations)
- `created`, `reviewed`, `review-due` must be proper **date format** — not text strings
- Wikilinks in properties must use the `"[[...]]"` format — bare `[[...]]` will not be recognised as a link type by Bases
