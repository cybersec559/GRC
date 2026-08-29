# HIPAA Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable HIPAA Security Rule (and relevant Privacy Rule) reference material and
templates for security professionals building or operating a HIPAA compliance program. Nothing
in this folder is specific to any one organization, and no example row contains real PHI — copy
what's useful into your own tracker and adapt it.

## Contents

- [`HIPAA-Security-Rule-Framework.md`](HIPAA-Security-Rule-Framework.md) — reference guide to
  what HIPAA is (a US federal law, not a certification), who it applies to (Covered Entities and
  Business Associates), the Required vs. Addressable distinction (addressable does not mean
  optional), the three Security Rule safeguard categories, an implementation roadmap, and a
  cross-mapping to ISO/IEC 27001:2022, SOC 2, and PCI DSS.
- [`controls.csv`](controls.csv) — 58 rows covering every Security Rule standard and
  implementation specification (45 CFR 164.308, 164.310, 164.312, 164.314, 164.316), each marked
  Required or Addressable, plus 8 key Privacy Rule rows and 1 Breach Notification Rule row,
  clearly labeled by category.
- [`templates/`](templates) — 18 fillable templates covering the HIPAA compliance lifecycle,
  including two HIPAA-specific artifacts: a Business Associate Agreement Register (replacing the
  generic vendor risk register given HIPAA's specific legal BAA requirement) and a Contingency
  Plan Test Log using HIPAA's own terminology. See [`templates/README.md`](templates/README.md)
  for the full list and a suggested workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, and PCI DSS material in the parent
[`GRC`](../README.md) repo so all frameworks' cross-mapping sections stay easy to
cross-reference.
