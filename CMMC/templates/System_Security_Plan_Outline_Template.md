# System Security Plan (SSP) — Outline Template

A System Security Plan is a **required artifact** under NIST SP 800-171 Rev 2 (practice
CA.L2-3.12.4) and is a foundational document for any CMMC Level 2 assessment (self-assessment or
C3PAO). This outline follows the standard structure used across published SSP templates (e.g.,
the NIST SP 800-171 SSP template structure referenced by DoD guidance). Replace every bracketed
placeholder with your organization's actual information — nothing below is real data.

---

## 1. System Identification

- **System Name:** [System/enclave name]
- **System Owner:** [Role/title]
- **Information System Security Officer (ISSO):** [Role/title]
- **Date of Plan:** [Date]
- **Plan Approved By:** [Role/title]

## 2. System Description and Purpose

- Describe the system's function, the FCI/CUI it processes, stores, or transmits, and why it is
  in scope for CMMC/NIST SP 800-171.

## 3. System Environment and Boundary

- Network diagram reference: [Link/file reference]
- System boundary description: hardware, software, cloud services, and interconnections in scope.
- CUI data flow description: where CUI enters, is processed, stored, and exits the environment.

## 4. Applicable CUI Categories

- List the specific CUI category/categories (per the CUI Registry) relevant to the contract(s)
  driving this SSP.

## 5. Roles and Responsibilities

| Role | Name/Title | Responsibilities |
|---|---|---|
| System Owner | [Placeholder] | Overall accountability for the system |
| ISSO | [Placeholder] | Day-to-day security oversight |
| IT Operations | [Placeholder] | Implementation of technical controls |

## 6. Security Requirements Implementation (by Domain)

For each of the 14 NIST SP 800-171 domains (see `../controls.csv`), document:

- **Implementation status** (Implemented / Planned / Not Applicable, with justification)
- **Implementation description** — how the practice is actually met in this environment
- **Responsible role**
- **Reference to supporting artifacts** (policy, configuration standard, screenshot, log sample)

| Domain | Practice ID | Implementation Status | Implementation Description | Responsible Role |
|---|---|---|---|---|
| Access Control | AC.L2-3.1.1 | | | |
| Awareness and Training | AT.L2-3.2.1 | | | |
| Audit and Accountability | AU.L2-3.3.1 | | | |
| Configuration Management | CM.L2-3.4.1 | | | |
| Identification and Authentication | IA.L2-3.5.1 | | | |
| Incident Response | IR.L2-3.6.1 | | | |
| Maintenance | MA.L2-3.7.1 | | | |
| Media Protection | MP.L2-3.8.1 | | | |
| Personnel Security | PS.L2-3.9.1 | | | |
| Physical Protection | PE.L2-3.10.1 | | | |
| Risk Assessment | RA.L2-3.11.1 | | | |
| Security Assessment | CA.L2-3.12.1 | | | |
| System and Communications Protection | SC.L2-3.13.1 | | | |
| System and Information Integrity | SI.L2-3.14.1 | | | |

*(Repeat/expand this table to cover all 110 practices — one row per practice, matching
`../controls.csv`.)*

## 7. Plan of Action and Milestones (POA&M) Summary

- Reference: `../templates/POAM_Template.csv`
- Summarize any practice marked "Not Met" or "Planned" here, with a pointer to the detailed POA&M
  entry.

## 8. SPRS Score Summary

- Current self-assessment score and date. Reference: `../templates/SPRS_Score_Tracker.csv`

## 9. External Systems and Services

- List any external/cloud service providers in the CUI boundary (e.g., cloud hosting, managed
  security service providers) and their FedRAMP-equivalency status, where applicable.

## 10. Plan Maintenance

- Review cadence: [e.g., annually and upon significant change]
- Change history log:

| Version | Date | Author | Summary of Change |
|---|---|---|---|
| 1.0 | | | Initial plan |

---
*This SSP outline is a generic starting skeleton, not a substitute for the officially published
NIST SP 800-171 SSP template or your organization's actual system boundary and control
implementation detail. Validate structure and required fields against current DoD/NIST guidance
before submission.*
