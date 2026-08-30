---
name: grc-crosswalk
description: Look up how one compliance control maps to its equivalents across the 12 frameworks in this GRC reference library (ISO 27001, SOC 2, PCI DSS, NIST CSF, HIPAA, GDPR, CCPA/CPRA, NIST SP 800-53, CIS Controls v8, COBIT 2019, FedRAMP, CMMC 2.0). Use when the user gives a control ID (e.g. "CC6.1", "A.8.24", "3.4.1", "PR.AA-05") or a topic ("access reviews", "encryption at rest", "vendor risk") and asks what the equivalent control is in another framework, or wants "the crosswalk" / "cross-framework mapping" for something.
---

# GRC control crosswalk

Look up: **$ARGUMENTS**

## Step 1 — search the master mapping

Read `Framework-Control-Mapping.csv` at the repo root. It has one row per control
domain and one column per framework (`ISO 27001:2022`, `SOC 2`, `PCI DSS v4.0`,
`NIST CSF 2.0`, `HIPAA`, `GDPR`, `CCPA/CPRA`, `NIST SP 800-53`, `CIS Controls v8`,
`COBIT 2019`, `FedRAMP`, `CMMC 2.0`).

- If given a **control ID**, find the row where that ID appears in any column.
- If given a **topic/keyword**, match against the `Domain` column (fuzzy — "MFA" should
  match "Authentication (MFA/passwords)").
- Multiple IDs in a cell are semicolon-separated — a control can legitimately map to more
  than one control in another framework, and vice versa.

## Step 2 — resolve each ID to its real title

For every framework column that has a hit, look up the actual title/description in that
framework's own `<Framework>/controls.csv` (or `controls.csv` at root for ISO 27001) —
don't just echo the ID, pull the real title so the user doesn't have to cross-reference
it themselves.

## Step 3 — present the result

A table: Framework | Control ID(s) | Title. Include every one of the 12 frameworks —
for ones with a genuine blank cell (that framework doesn't address this domain), say so
explicitly ("no direct equivalent") rather than omitting the row silently. Then one line
naming the domain this falls under, so the user can spot related rows.

## If the ID isn't in the mapping file at all

The mapping file covers ~60 common domains, not every one of the ~1,100 individual
controls. If there's no row match:

1. Grep all `*/controls.csv` and the root `controls.csv` for the ID or keyword directly
   to find its title/description.
2. Read the "Cross-Mapping to Other Frameworks" section (near the end) of that control's
   own `<Framework>.md` doc — each framework doc has one, at a theme level.
3. Say plainly that this is a theme-level match from the framework doc, not a verified
   control-level crosswalk row, so the user knows the confidence level.

## Constraints

This is read-only lookup work. Don't edit `Framework-Control-Mapping.csv` or any
`controls.csv` as part of a lookup — that's a separate maintenance task (see the
`grc-add-framework` skill if a new framework needs to be added to the mapping).
