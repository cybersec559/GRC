# GRC Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable Governance, Risk & Compliance (GRC) reference material and templates for
security professionals building or operating a compliance program. Nothing in this repository is
specific to any one organization — copy what's useful into your own tracker and adapt it.

## Contents

This repo covers 12 compliance frameworks, each with the same structure: a framework reference
doc, a flat `controls.csv` catalog, and a `templates/` folder of fillable artifacts adapted to
that framework's own terminology.

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

### NIST CSF 2.0 (`NIST-CSF/`)

- [`NIST-CSF/NIST-CSF-2.0-Framework.md`](NIST-CSF/NIST-CSF-2.0-Framework.md) — the six Functions
  (GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER), the Current/Target Profile and
  Implementation Tier model, cross-mapping to ISO 27001 / SOC 2 / PCI DSS.
- [`NIST-CSF/controls.csv`](NIST-CSF/controls.csv) — 106 CSF 2.0 Subcategories.
- [`NIST-CSF/templates/`](NIST-CSF/templates) — 18 templates adapted to CSF terms (Current/Target
  Profile matrix, Gap Register, Profile Review agenda).

### HIPAA Security Rule (`HIPAA/`)

- [`HIPAA/HIPAA-Security-Rule-Framework.md`](HIPAA/HIPAA-Security-Rule-Framework.md) — Covered
  Entity/Business Associate scope, Required vs. Addressable distinction, the three safeguard
  categories, cross-mapping to ISO 27001 / SOC 2 / PCI DSS.
- [`HIPAA/controls.csv`](HIPAA/controls.csv) — 58 Security Rule standards/implementation
  specifications plus key Privacy Rule and Breach Notification Rule references.
- [`HIPAA/templates/`](HIPAA/templates) — 19 templates including HIPAA-specific artifacts: a
  Business Associate Agreement Register and a Contingency Plan Test Log.

### GDPR (`GDPR/`)

- [`GDPR/GDPR-Framework.md`](GDPR/GDPR-Framework.md) — extraterritorial scope, Controller/Processor
  roles, principles/rights/obligations catalog, cross-mapping to ISO 27001 / SOC 2.
- [`GDPR/controls.csv`](GDPR/controls.csv) — 50 Articles/principles covering lawful bases, data
  subject rights, breach notification, DPIAs, DPO requirements, and international transfers.
- [`GDPR/templates/`](GDPR/templates) — 19 templates including four GDPR-specific artifacts: a
  Records of Processing Activities register (Art. 30), a DPIA template (Art. 35), a Data Subject
  Request Log, and an International Transfer Register.

### CCPA / CPRA (`CCPA/`)

- [`CCPA/CCPA-CPRA-Framework.md`](CCPA/CCPA-CPRA-Framework.md) — applicability thresholds, consumer
  rights, business/service provider/contractor roles, cross-mapping to GDPR / ISO 27001 / SOC 2.
- [`CCPA/controls.csv`](CCPA/controls.csv) — 37 rows covering consumer rights, business
  obligations, sensitive PI, and CPRA-added risk assessment/audit requirements.
- [`CCPA/templates/`](CCPA/templates) — 18 templates including a Personal Information Inventory,
  Consumer Request Log, and Cybersecurity Audit & Risk Assessment Log.

### NIST SP 800-53 Rev 5 (`NIST-800-53/`)

- [`NIST-800-53/NIST-800-53-Framework.md`](NIST-800-53/NIST-800-53-Framework.md) — the 20 control
  families, baselines (Low/Moderate/High), the RMF roadmap, cross-mapping to ISO 27001 / SOC 2 /
  PCI DSS. **Scope note:** catalogs base controls only, not the 1000+ control enhancements in the
  full standard.
- [`NIST-800-53/controls.csv`](NIST-800-53/controls.csv) — 302 base controls across all 20 families.
- [`NIST-800-53/templates/`](NIST-800-53/templates) — 19 templates including a Plan of Action &
  Milestones (POA&M) and a System Security Plan outline.

### CIS Controls v8 (`CIS-Controls-v8/`)

- [`CIS-Controls-v8/CIS-Controls-v8-Framework.md`](CIS-Controls-v8/CIS-Controls-v8-Framework.md)
  — the 18 Controls, the Implementation Group (IG1/IG2/IG3) self-selection model, implementation
  roadmap, cross-mapping to ISO 27001 / SOC 2 / PCI DSS / NIST CSF.
- [`CIS-Controls-v8/controls.csv`](CIS-Controls-v8/controls.csv) — 153 Safeguards across 18
  Controls.
- [`CIS-Controls-v8/templates/`](CIS-Controls-v8/templates) — 19 templates including a
  CIS-specific Data Recovery Test Log.

Note: this is unrelated to the separate `CIS/` folder in this repo, which holds macOS/JAMF
configuration baseline material from a different project.

### COBIT 2019 (`COBIT/`)

- [`COBIT/COBIT-2019-Framework.md`](COBIT/COBIT-2019-Framework.md) — governance vs. management
  objectives, the design-factor tailoring concept, the 0-5 capability model, cross-mapping to
  ISO 27001 / SOC 2 / NIST CSF via APO13/DSS05.
- [`COBIT/controls.csv`](COBIT/controls.csv) — 40 governance/management objectives across 5
  domains (EDM, APO, BAI, DSS, MEA).
- [`COBIT/templates/`](COBIT/templates) — 19 templates including a board-level Governance Review
  Agenda and a capability-level RACI matrix.

### FedRAMP (`FedRAMP/`)

- [`FedRAMP/FedRAMP-Framework.md`](FedRAMP/FedRAMP-Framework.md) — impact levels, JAB vs. Agency
  authorization paths, relationship to NIST SP 800-53 (see that folder for the base control
  catalog), cross-mapping to ISO 27001 / SOC 2.
- [`FedRAMP/controls.csv`](FedRAMP/controls.csv) — 39 program-level requirements (3PAO assessment,
  ConMon cadence, significant change management, incident reporting, and more).
- [`FedRAMP/templates/`](FedRAMP/templates) — 19 templates including a POA&M, a Continuous
  Monitoring (ConMon) log, and a Significant Change Request log.

### CMMC 2.0 (`CMMC/`)

- [`CMMC/CMMC-2.0-Framework.md`](CMMC/CMMC-2.0-Framework.md) — 3-level structure, self-assessment
  vs. C3PAO vs. DIBCAC assessment paths, relationship to NIST SP 800-171/800-172, implementation
  roadmap, cross-mapping to NIST SP 800-53 / ISO 27001 / SOC 2.
- [`CMMC/controls.csv`](CMMC/controls.csv) — 118 rows: 110 Level 2 practices (mirrors NIST SP
  800-171 Rev 2 exactly) flagged for Level 1 (FAR 52.204-21) overlap, plus 8 illustrative Level 3
  (NIST SP 800-172 enhanced requirement) rows.
- [`CMMC/templates/`](CMMC/templates) — 19 templates including a POA&M, a System Security Plan
  outline, and an SPRS Score Tracker.

## Cross-Framework Control Mapping

[`Framework-Control-Mapping.csv`](Framework-Control-Mapping.csv) is a single crosswalk across
all 12 frameworks above: one row per common control domain (access control, encryption,
vendor risk, incident response, business continuity, and so on), one column per framework,
each cell holding the real control ID(s) in that framework addressing that domain. Each
framework doc's own "Cross-Mapping" section stays theme-level and narrative; this file is the
control-ID-level companion — useful for filtering in a spreadsheet to find every control that
maps to a given domain across all 12 standards at once, or to answer "if an auditor asks for
evidence under Framework X, what else does this same evidence satisfy?"

Blank cells are expected and meaningful: a privacy-specific domain (data subject rights,
lawful basis, breach notification) will genuinely have no equivalent in, say, CIS Controls v8
or COBIT — that's not a gap in the mapping, it's an accurate reflection of scope.

## Skills

This repo ships three Claude Code skills under [`.claude/skills/`](.claude/skills) for working
with it directly:

- **`grc-crosswalk`** — look up a control ID or topic and get its equivalents across all 12
  frameworks, using `Framework-Control-Mapping.csv`.
- **`grc-gap-assessment`** — walk through a chosen framework's controls and produce a filled
  applicability/readiness matrix. Always writes the filled-in result outside this repo — a
  completed assessment describes a real environment and is exactly the proprietary content
  this library is not meant to hold.
- **`grc-add-framework`** — scaffold a 13th (or later) framework into this repo following the
  existing folder/doc/template/crosswalk pattern.
