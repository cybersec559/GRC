# NIST SP 800-53 Rev 5 Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable NIST SP 800-53 Revision 5 reference material and templates for security
professionals building or operating a control implementation program under the Risk Management
Framework (RMF). Nothing in this folder is specific to any one organization — copy what's useful
into your own tracker and adapt it.

## Contents

- [`NIST-800-53-Framework.md`](NIST-800-53-Framework.md) — reference guide to the control catalog
  structure, the 20 control families, impact baselines (Low/Moderate/High), the RMF implementation
  roadmap, and a cross-mapping to ISO/IEC 27001:2022, SOC 2, and PCI DSS.
- [`controls.csv`](controls.csv) — 302 NIST SP 800-53 Rev 5 **base controls** across all 20
  families, as a flat reference catalog (Control ID, Family, Title, Description). **Scope note:**
  this catalog is base-control-level only — the full standard defines well over a thousand
  additional control enhancements (e.g. `AC-2(1)`, `AC-2(2)`, …) not itemized here. See Section 2
  of the framework doc for detail.
- [`templates/`](templates) — 19 fillable templates covering the RMF lifecycle: a Control
  Implementation Summary (pre-populated with all 302 controls), a Plan of Action and Milestones
  (POA&M), a System Security Plan outline, an Authorization Review agenda, a system component
  inventory, risk register, internal audit checklist, evidence log, policy inventory, access
  reviews, supply chain/vendor risk, security objectives, onboarding/offboarding, contingency plan
  testing, incident management, media handling, competence records, and RACI. See
  [`templates/README.md`](templates/README.md) for the full list and a suggested workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, and PCI DSS material in the parent
[`GRC`](../README.md) repo so all four frameworks' cross-mapping sections stay easy to
cross-reference.
