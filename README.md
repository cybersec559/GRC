# GRC Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable Governance, Risk & Compliance (GRC) reference material and templates for
security professionals building or operating an ISMS. Nothing in this repository is specific to
any one organization — copy what's useful into your own tracker and adapt it.

## Contents

This repo covers multiple compliance frameworks, each with the same structure: a framework
reference doc, a flat `controls.csv` catalog, and a `templates/` folder of fillable artifacts
adapted to that framework's own terminology.

### ISO/IEC 27001:2022 (repo root)

- [`ISO-27001-2022-Framework.md`](ISO-27001-2022-Framework.md) — management-system clauses, the
  93-control Annex A structure, implementation roadmap, cross-mapping to SOC 2 / PCI DSS / NIST CSF.
- [`controls.csv`](controls.csv) — 93 Annex A controls.
- [`templates/`](templates) — 19 templates (Statement of Applicability, asset inventory, risk
  register, CAPA register, and more). See [`templates/README.md`](templates/README.md).

### SOC 2 (`SOC2/`)

- [`SOC2/SOC2-Trust-Services-Criteria-Framework.md`](SOC2/SOC2-Trust-Services-Criteria-Framework.md)
  — Type I/II reports, Common Criteria, optional Trust Service Categories, cross-mapping.
- [`SOC2/controls.csv`](SOC2/controls.csv) — 43 Trust Services Criteria.
- [`SOC2/templates/`](SOC2/templates) — 18 templates adapted to SOC 2 terms (TSC Controls Matrix,
  Control Exception Register, Compliance Review).

### PCI DSS v4.0 (`PCI-DSS/`)

- [`PCI-DSS/PCI-DSS-4.0-Framework.md`](PCI-DSS/PCI-DSS-4.0-Framework.md) — 12 requirements/6 goals,
  SAQ vs. ROC, compensating controls, cross-mapping.
- [`PCI-DSS/controls.csv`](PCI-DSS/controls.csv) — 63 first-level sub-requirements.
- [`PCI-DSS/templates/`](PCI-DSS/templates) — 19 templates including two PCI-specific artifacts:
  a Compensating Controls Worksheet and a Quarterly ASV Scan & Penetration Test Log.
