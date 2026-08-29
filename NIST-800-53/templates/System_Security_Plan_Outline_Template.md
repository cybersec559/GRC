# System Security Plan (SSP) — Outline Template

The System Security Plan is the master RMF document for a system: it describes the system,
its security categorization, its control implementation, and the roles responsible for it.
This is a structured skeleton to start drafting from — not a complete SSP. Populate each
section with your own system's specifics; remove the bracketed guidance text as you go.

---

## 1. System Identification

- **System Name / Acronym:** [ ]
- **System Owner:** [ ]
- **Authorizing Official (AO):** [ ]
- **ISSO (Information System Security Officer):** [ ]
- **System Description / Purpose:** [Brief narrative of what the system does and who uses it]
- **System Boundary:** [What is included/excluded from this authorization boundary]
- **Operational Status:** [Operational / Under Development / Major Modification / Undergoing a Major Change]

## 2. System Categorization (FIPS 199)

| Information Type | Confidentiality | Integrity | Availability |
|---|---|---|---|
| [Example: Customer records] | [Low/Moderate/High] | [Low/Moderate/High] | [Low/Moderate/High] |

- **Overall System Categorization:** [Low / Moderate / High] (the high-water mark across all
  information types processed, stored, or transmitted by the system)
- **Categorization Rationale:** [Reference FIPS 199 / NIST SP 800-60 guidance used]

## 3. Control Implementation Summary Reference

- **Baseline Selected:** [Low / Moderate / High] — per `PL-10` (Baseline Selection) and
  `PL-11` (Baseline Tailoring)
- **Control Implementation Summary Location:** [Link/reference to the completed
  `Control_Implementation_Summary_Template.csv` for this system — do not duplicate that detail
  here; this section only points to it]
- **Tailoring Decisions Summary:** [Brief note on any controls added, removed, or scoped
  differently from the selected baseline, and why]

## 4. System Environment and Architecture

- **Hardware/Software Inventory Reference:** [Link to System Component Inventory —
  see `Asset_Inventory_Template.csv`]
- **Network Diagram Reference:** [Link/attachment]
- **Data Flow Description:** [Brief narrative or link to data flow diagram]

## 5. Interconnections

| Connected System | Organization | Connection Type | Data Exchanged | Agreement Reference (ISA/MOU) | Authorization Status |
|---|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

## 6. Roles and Responsibilities

| Role | Name/Title | Responsibilities |
|---|---|---|
| Authorizing Official (AO) | [ ] | Accepts residual risk; issues the authorization decision |
| System Owner | [ ] | Accountable for system operation and control implementation |
| ISSO | [ ] | Day-to-day security operations and continuous monitoring |
| Common Control Provider | [ ] | Owns organization-wide inherited controls |
| Security Control Assessor (SCA) | [ ] | Independently assesses control effectiveness |

## 7. Rules of Behavior Reference

- **Rules of Behavior Document Location:** [Link — see `PL-4`]
- **Acknowledgment Process:** [How users attest they have read and agree to the rules]

## 8. Plan of Action and Milestones (POA&M) Reference

- **POA&M Location:** [Link to `POAM_Template.csv` tracking open weaknesses for this system]

## 9. Contingency Plan Reference

- **Contingency Plan Location:** [Link — see `CP-2`]
- **Last Test Date:** [Reference `Contingency_Plan_Test_Log.csv`]

## 10. Plan Approval

| Name | Role | Signature | Date |
|---|---|---|---|
| [ ] | System Owner | | |
| [ ] | ISSO | | |
| [ ] | Authorizing Official | | |

---
*This is a skeleton, not a complete SSP. Consult NIST SP 800-18 (Guide for Developing Security
Plans) for full section-by-section guidance before submitting an SSP as part of an authorization
package.*
