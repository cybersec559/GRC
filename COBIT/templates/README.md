# COBIT 2019 Templates

Generic, fillable templates supporting a COBIT 2019 IT governance program. Pair with
`../controls.csv` (the 40-objective reference catalog) and `../COBIT-2019-Framework.md`. None of
these files contain any organization-specific data — copy them into your own tracker and fill in
the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `COBIT_Capability_Assessment_Matrix_Template.csv` | Pre-populated with all 40 objectives; record design-factor priority, current vs. target capability level (0-5), gap description, evidence and owner. | EDM01, all objectives |
| `Asset_Inventory_Template.csv` | Asset register with CIA (Confidentiality/Integrity/Availability) ratings per asset, driving classification and lifecycle tracking. | APO14, BAI09, DSS05 |
| `Risk_Register_Template.csv` | IT-related risk identification, scoring (inherent → residual), treatment decision, objective linkage. | APO12 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 40 objectives; track conformance findings per audit cycle. | MEA02, MEA04 |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per objective — what, when, by whom, review status, renewal date. | MEA01, MEA04 |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence (education, certification, training, experience) for IT-governance-relevant roles. | APO07 |
| `RACI_Template.csv` | Practice-level Responsible/Accountable/Consulted/Informed matrix, reflecting COBIT's own published RACI charts (one row per management practice, not just per objective). | EDM/APO/DSS/MEA practices shown per row |
| `Incident_Management_Tracker.csv` | Log of incidents from detection through containment, root cause, corrective action, and closure. | DSS02 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, classification, encryption status, and lifecycle status. | BAI09, DSS05 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site (courier, hand-carry, electronic transfer), with protection and receipt confirmation. | DSS05 |
| `Nonconformity_Corrective_Action_Register.csv` | Tracks corrective/preventive actions from any source (audit, incident, complaint, governance review) through root cause to verified closure. | MEA02 |
| `Policy_Inventory_Register.csv` | Master list of every IT-governance-relevant policy — owner, version, approval date, next review date. | APO01, APO13 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | DSS05 |
| `Vendor_ThirdParty_Risk_Register.csv` | Vendor risk tier, data access level, security questionnaire status, contract review dates. | APO10 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable objectives framed as COBIT's goals cascade metrics — target vs. actual performance. | MEA01, cascades from enterprise goals |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist (access, assets, agreements). | APO07, BAI09, DSS05 |
| `Business_Continuity_Test_Log.csv` | Business continuity test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | DSS04 |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts and current compliance status. | MEA03 |
| `Governance_Review_Agenda_Template.md` | Standing agenda for the governing body's (board/audit committee) periodic governance review — distinct from an operational management review. | EDM01-EDM05 |

## Suggested workflow

1. Run the **design factor analysis** with governing body and executive stakeholders (see
   `../COBIT-2019-Framework.md` Section 3), then populate the **Capability Assessment Matrix**
   with priority ratings for all 40 objectives.
2. Populate the **Asset Inventory** — many objectives (APO14, BAI09, DSS05) reference assets
   directly.
3. Run a **risk assessment** into the **Risk Register**, linking risks to assets and to objectives
   in `controls.csv`.
4. Assess **current capability levels** for prioritized objectives and record target levels and
   gap descriptions in the Capability Assessment Matrix.
5. As gaps are closed, log supporting proof in the **Evidence Submission Log**.
6. Run periodic **internal audits** using the checklist, referencing the same evidence log.
7. Bring capability assessment results, risk register changes, and assurance findings into the
   **Governance Review** for the governing body.
