---
name: grc-add-framework
description: Scaffold a new compliance framework into this GRC reference library, following the same structure as the existing 12 (ISO 27001, SOC 2, PCI DSS, NIST CSF, HIPAA, GDPR, CCPA/CPRA, NIST SP 800-53, CIS Controls v8, COBIT 2019, FedRAMP, CMMC 2.0). Use when the user asks to "add a framework", "add NIST 800-171", "add ISO 27701", "add [some standard] to the GRC repo", or similar.
---

# Add a new framework to the GRC library

New framework: **$ARGUMENTS**

## Before starting

Confirm you actually know this standard's real control structure well enough to catalog
it accurately — control IDs, categories, and titles must come from genuine knowledge of the
public standard, never invented to fill out a template. If uncertain about specifics (exact
wording, current version/revision), say so and use your best public knowledge rather than
fabricating precise-looking text. This repo is a generic reference library used by security
professionals — inaccurate control catalogs are worse than a smaller, accurate one.

## Step 1 — create the folder and framework doc

Create `<Framework>/<Framework>-Framework.md`. Match the structure of existing docs (read
`SOC2/SOC2-Trust-Services-Criteria-Framework.md` or `PCI-DSS/PCI-DSS-4.0-Framework.md` as a
template for section order): scope/applicability, structure of the standard, a walkthrough
of its major categories, an implementation roadmap, and a "Cross-Mapping to Other
Frameworks" section (theme-level, referencing ISO 27001 / SOC 2 / PCI DSS at minimum — the
three most commonly run in parallel).

## Step 2 — create the control catalog

Create `<Framework>/controls.csv`. Use the column pattern already established:
`Control ID,Category,Title,Description` (or the closest framework-native equivalent — e.g.
SOC 2 uses `Criteria ID,Category,Title,Description`). One row per control/requirement, real
IDs from the actual standard.

## Step 3 — create the templates folder

Create `<Framework>/templates/` and populate it by adapting the common template set from an
existing framework folder (e.g. `SOC2/templates/`) — read a few of the existing template
CSVs' headers and adapt terminology (e.g. "criteria" vs. "controls" vs. "requirements") to
this framework's own vocabulary:

Asset_Inventory_Template.csv, Risk_Register_Template.csv, Internal_Audit_Checklist_Template.csv,
Evidence_Submission_Log_Template.csv, Competence_Records_Template.csv, RACI_Template.csv,
Incident_Management_Tracker.csv, Media_Inventory_Log.csv, Media_Transport_Log.csv,
Policy_Inventory_Register.csv, Access_Review_Recertification_Log.csv,
Vendor_ThirdParty_Risk_Register.csv, Security_Objectives_KPI_Tracker.csv,
Onboarding_Offboarding_Security_Checklist.csv, BC_DR_Test_Log.csv,
Legal_Regulatory_Requirements_Register.csv, plus a standing-agenda `.md` template.

Add one framework-specific applicability/readiness template, pre-populated with every
control ID from Step 2, named `<Framework>_Compliance_Matrix_Template.csv` (this is the
naming convention `grc-gap-assessment` expects — keep it consistent so that skill keeps
working for the new framework without changes).

Add a `<Framework>/templates/README.md` listing every template, its purpose, and which
control(s) it ties to (mirror `SOC2/templates/README.md`'s table format).

## Step 4 — create the folder README

Create `<Framework>/README.md` mirroring `SOC2/README.md`: what the framework doc covers,
what's in controls.csv (count + ID format), what's in templates/, and a one-line note on
this folder's relationship to the parent GRC repo.

## Step 5 — update the root README

Add a new `### <Framework Name> (`<Framework>/`)` section to the root `README.md`, in the
same style as the existing per-framework entries, and update the "Contents" intro line
("This repo covers N compliance frameworks...") to the new count.

## Step 6 — extend the master crosswalk

Read `Framework-Control-Mapping.csv`. Add a new column for this framework at the end. For
every existing domain row this framework addresses, add the real matching control ID(s) —
pull from the controls.csv you just built in Step 2, not from memory. If this framework has
a domain none of the other 12 cover, add a new row rather than forcing a fit into an
existing one.

## Constraints

- Everything generic-only — no organization-specific content anywhere in this repo, per this
  library's whole purpose. See the root README's opening paragraph if in doubt.
- Don't skip Step 6 — a framework that's cataloged but missing from the crosswalk defeats
  the point of `grc-crosswalk`.
