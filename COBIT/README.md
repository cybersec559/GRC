# COBIT 2019 Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable COBIT 2019 (ISACA's framework for the governance and management of enterprise
IT) reference material and templates for IT governance and security professionals. Nothing in
this folder is specific to any one organization — copy what's useful into your own tracker and
adapt it.

## Contents

- [`COBIT-2019-Framework.md`](COBIT-2019-Framework.md) — reference guide to the
  governance-vs-management distinction, the design factor concept, the 5 domains and 40 governance
  and management objectives, the 0-5 capability level model, an implementation roadmap, and a
  cross-mapping to ISO/IEC 27001:2022, SOC 2, and NIST CSF for the security-specific objectives
  (APO13, DSS05).
- [`controls.csv`](controls.csv) — all 40 governance and management objectives as a flat reference
  catalog (Objective ID, Domain, Title, Description).
- [`templates/`](templates) — 19 fillable templates adapted to COBIT terminology: a Capability
  Assessment Matrix in place of a fixed control checklist, a practice-level RACI template
  reflecting COBIT's own published RACI charts, a board/audit-committee-oriented Governance Review
  Agenda, and the standard GRC template set (risk register, asset inventory, incident tracker,
  vendor risk register, and more). See [`templates/README.md`](templates/README.md) for the full
  list and a suggested workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, PCI DSS, and NIST CSF material in the
parent [`GRC`](../README.md) repo. COBIT is broader in scope than those frameworks — it governs
the whole enterprise use of IT, of which security is one component — so its cross-mapping section
focuses specifically on the two objectives (APO13 Managed Security, DSS05 Managed Security
Services) that overlap most directly with the security-specific frameworks in this repo.
