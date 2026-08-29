# CMMC Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable CMMC 2.0 (Cybersecurity Maturity Model Certification) reference material and
templates for security professionals building or operating a Defense Industrial Base (DIB)
cybersecurity compliance program. Nothing in this folder is specific to any one organization —
copy what's useful into your own tracker and adapt it.

## Contents

- [`CMMC-2.0-Framework.md`](CMMC-2.0-Framework.md) — reference guide to the 3-level structure and
  assessment paths (self-assessment / C3PAO / DIBCAC), the relationship to NIST SP 800-171/800-172,
  an implementation roadmap (contract requirement → gap assessment → implementation → SSP/SPRS
  score → POA&M → assessment → affirmation), and a cross-mapping to NIST SP 800-53, ISO/IEC
  27001:2022, and SOC 2.
- [`controls.csv`](controls.csv) — the full CMMC Level 2 practice catalog (110 practices mirroring
  NIST SP 800-171 Rev 2 exactly, across 14 domains), each flagged if it's also one of the 17 Level
  1 (FAR 52.204-21) practices, plus 8 illustrative Level 3 (NIST SP 800-172 enhanced requirement)
  rows clearly marked as a representative sample rather than an exhaustive catalog.
- [`templates/`](templates) — 19 fillable templates covering the CMMC readiness-to-assessment
  lifecycle, including two CMMC/NIST-specific required artifacts with no ISO/SOC2 equivalent: a
  **Plan of Action & Milestones (POA&M)** and a **System Security Plan (SSP) outline**, plus a
  CMMC-specific **SPRS Score Tracker**. See [`templates/README.md`](templates/README.md) for the
  full list and a suggested workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, and PCI DSS material in the parent
[`GRC`](../README.md) repo so all frameworks' cross-mapping sections stay easy to cross-reference.
