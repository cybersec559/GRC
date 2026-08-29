# FedRAMP Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable FedRAMP (Federal Risk and Authorization Management Program) reference material
and templates for security professionals building or operating a federal cloud authorization
program. Nothing in this folder is specific to any one organization — copy what's useful into your
own tracker and adapt it.

## Contents

- [`FedRAMP-Framework.md`](FedRAMP-Framework.md) — reference guide to what FedRAMP is, the impact
  levels and authorization paths (JAB P-ATO, Agency ATO, FedRAMP Tailored/LI-SaaS), the
  implementation roadmap, and a cross-mapping to NIST SP 800-53, ISO/IEC 27001:2022, and SOC 2.
- [`controls.csv`](controls.csv) — 39 FedRAMP **program-level** requirements as a flat reference
  catalog (Requirement ID, Category, Title, Description): categorization, authorization paths,
  required documentation artifacts, the 3PAO independent assessment mandate, continuous monitoring
  cadence, significant change management, incident reporting timelines, Marketplace status,
  boundary/data-flow documentation, and personnel security.
- [`templates/`](templates) — 18 fillable templates covering the FedRAMP authorization and
  continuous monitoring lifecycle, including three FedRAMP-specific artifacts with no ISO/SOC2
  equivalent: a **POA&M Template**, a **Continuous Monitoring (ConMon) Log**, and a **Significant
  Change Request Log**. See [`templates/README.md`](templates/README.md) for the full list and a
  suggested workflow.

### Relationship to the `NIST-800-53` folder

FedRAMP is built **on top of** NIST SP 800-53 — it does not have its own control catalog. This
folder deliberately does **not** re-list the underlying 800-53 controls; for that catalog (control
families, control IDs, control text, and implementation tracking), see the **`NIST-800-53` folder**
in the parent GRC repo. Use that folder's catalog for control-by-control tracking, and use this
folder's `controls.csv` and templates for the FedRAMP-specific program mechanics layered on top of
the control baseline (categorization, authorization paths, 3PAO assessment, ConMon cadence,
significant change requests, incident reporting timelines, and Marketplace status).

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, PCI DSS, and NIST-800-53 material in the
parent [`GRC`](../README.md) repo so all frameworks' cross-mapping sections stay easy to
cross-reference.
