# CIS Controls v8 Reference Library

**Author:** Joshna Yarlagadda

Generic, reusable CIS Controls v8 (Center for Internet Security) reference material and templates
for security professionals building or maturing a security program using the CIS Critical
Security Controls. Nothing in this folder is specific to any one organization — copy what's
useful into your own tracker and adapt it.

## Contents

- [`CIS-Controls-v8-Framework.md`](CIS-Controls-v8-Framework.md) — reference guide to what CIS
  Controls is (and isn't), the Implementation Group (IG1/IG2/IG3) self-selection model, the 18
  Controls, an implementation roadmap, and a cross-mapping to ISO/IEC 27001:2022, SOC 2, PCI DSS,
  and NIST CSF.
- [`controls.csv`](controls.csv) — all 153 CIS Controls v8 Safeguards as a flat reference catalog
  (Safeguard ID, Control Title, Safeguard Title, Description, Implementation Group, Asset Type,
  Security Function).
- [`templates/`](templates) — 19 fillable templates covering the CIS Controls implementation
  lifecycle: implementation matrix, asset inventory, risk register, internal audit checklist,
  evidence log, nonconformity/corrective action register, policy inventory, access reviews,
  service provider risk, security objectives, onboarding/offboarding, data recovery testing, legal
  & regulatory requirements, incident management, media handling, competence records, RACI, and
  the Implementation Group review agenda. See [`templates/README.md`](templates/README.md) for
  the full list and a suggested workflow.

## Relationship to the parent GRC repo

This folder lives alongside the ISO/IEC 27001:2022, SOC 2, and PCI DSS material in the parent
[`GRC`](../README.md) repo so all frameworks' cross-mapping sections stay easy to
cross-reference. It is unrelated to the separate `CIS` folder elsewhere in this repo, which holds
macOS/JAMF configuration baseline material from a different project.
