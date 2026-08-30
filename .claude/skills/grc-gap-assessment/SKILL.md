---
name: grc-gap-assessment
description: Generate a filled-in gap/readiness assessment (applicability matrix) for one framework in this GRC reference library, by walking the user through each control's implementation status. Use when the user asks for a "gap assessment", "readiness assessment", "applicability matrix", "SoA" (Statement of Applicability), or "where do we stand against SOC 2 / ISO 27001 / PCI DSS / etc."
---

# GRC gap assessment

Target framework: **$ARGUMENTS** (e.g. "SOC 2", "ISO 27001", "PCI DSS", "NIST CSF")

## Step 1 — resolve the framework and its files

Match the argument against the 12 frameworks (case-insensitively, allow common aliases —
"ISO", "ISO27001" → ISO/IEC 27001:2022; "PCI" → PCI DSS v4.0; "CSF" → NIST CSF 2.0; "800-53"
→ NIST SP 800-53). ISO 27001 lives at the repo root; the other 11 each have their own
folder. Locate:

- `<folder>/controls.csv` (or root `controls.csv` for ISO) — the full control list.
- The framework's applicability-style template, named by convention:
  - ISO 27001 → `templates/SoA_Template.csv`
  - SOC 2 → `SOC2/templates/TSC_Controls_Matrix_Template.csv`
  - NIST CSF 2.0 → `NIST-CSF/templates/Current_Target_Profile_Template.csv`
  - NIST SP 800-53 → `NIST-800-53/templates/Control_Implementation_Summary_Template.csv`
  - COBIT 2019 → `COBIT/templates/COBIT_Capability_Assessment_Matrix_Template.csv`
  - Everything else → `<Folder>/templates/<Framework>_Compliance_Matrix_Template.csv`

Read both in full before proceeding.

## Step 2 — collect status per control

Don't guess implementation status — ask. For a framework with a large control count
(NIST 800-53, CIS v8, CMMC), batch controls by category/family rather than asking one at a
time. For each control, you need at minimum:

- **Applicable** (Y/N) — some controls won't apply to every environment/scope.
- **Implementation status** (Not started / In progress / Implemented / Not applicable).
- **Evidence** — a short description of what would demonstrate this, if any exists.
- **Owner** — who is responsible, if the user knows.

If the user gives you a batch description up front ("we use Okta for SSO, have a written
IR policy, no formal vendor risk process yet") instead of answering control-by-control,
infer draft statuses from that and clearly flag every inferred (vs. user-confirmed) row so
they know what to double check.

## Step 3 — write the filled assessment OUTSIDE this repo

**This repo (`GRC/`) is generic reference material only — never write a filled-in,
organization-specific assessment back into it.** A completed gap assessment describing a
real environment's actual controls is exactly the kind of proprietary content this repo
must not contain, no matter how the request is phrased.

Save the output using the applicability template's column structure to a path outside
`GRC/` — ask the user where (their own compliance tracker location, a scratchpad, etc.) if
not already clear from context. Never default to writing inside this repo's directory tree.

## Step 4 — summarize

Give a short rollup: counts by status (Implemented / In progress / Not started / N/A), and
call out the highest-risk "Not started" items (access control, encryption, incident
response, logging — these are the ones auditors and attackers both look at first).
