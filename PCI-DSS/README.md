# PCI DSS Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable PCI DSS v4.0 reference material and templates for security professionals
building or operating a cardholder data protection program. Nothing in this folder is specific to
any one organization — copy what's useful into your own tracker and adapt it.

## Contents

- [`PCI-DSS-4.0-Framework.md`](PCI-DSS-4.0-Framework.md) — reference guide to the 12 requirements
  across 6 goals, SAQ vs. ROC validation paths, distinctive PCI concepts (compensating controls,
  quarterly ASV scans), an implementation roadmap, and a cross-mapping to ISO/IEC 27001:2022,
  SOC 2, and NIST CSF.
- [`controls.csv`](controls.csv) — all 63 PCI DSS v4.0 first-level sub-requirements as a flat
  reference catalog (Requirement ID, Goal, Title, Description).
- [`templates/`](templates) — 19 fillable templates, including two PCI-specific artifacts with no
  ISO/SOC2 equivalent: a Compensating Controls Worksheet and a Quarterly ASV Scan & Penetration
  Test Log. See [`templates/README.md`](templates/README.md) for the full list and a suggested
  workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022 and SOC 2 material in the parent
[`GRC`](../README.md) repo so all three frameworks' cross-mapping sections stay easy to
cross-reference.
