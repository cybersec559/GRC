# ISMS Templates

Generic, fillable templates supporting an ISO/IEC 27001:2022 ISMS. Pair with `../controls.csv`
(the 93-control reference catalog) and `../ISO-27001-2022-Framework.md`. None of these files
contain any organization-specific data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `SoA_Template.csv` | Statement of Applicability — pre-populated with all 93 controls; mark applicability, justification, status, evidence, owner. | Clause 6.1.3 |
| `Asset_Inventory_Template.csv` | Asset register with CIA (Confidentiality/Integrity/Availability) ratings per asset, driving classification. | A.5.9, A.5.12 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, control linkage. | Clause 6.1 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with management clauses (4-10) + all 93 controls; track conformance findings per audit cycle. | Clause 9.2 |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per control — what, when, by whom, review status, renewal date. | Clause 7.5 (Documented Information) |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence (education, certification, training, experience) for security-relevant roles. | Clause 7.2 (Competence) |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring ISMS activities (risk assessment, incident response, audits, etc.). | Clause 5 (Leadership), supports role clarity across all controls |
| `Incident_Management_Tracker.csv` | Log of security incidents from detection through containment, root cause, corrective action, and closure. | A.5.24-A.5.28 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, classification, encryption status, and lifecycle status. | A.7.10 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site (courier, hand-carry, electronic transfer), with protection and receipt confirmation. | A.7.10 |
| `Nonconformity_CAPA_Register.csv` | Tracks corrective/preventive actions from any source (audit, incident, complaint, management review) through root cause to verified closure. | Clause 10 |
| `Policy_Inventory_Register.csv` | Master list of every ISMS policy — owner, version, approval date, next review date. | Clause 7.5, A.5.1 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | A.5.18, A.8.2 |
| `Vendor_ThirdParty_Risk_Register.csv` | Vendor risk tier, data access level, security questionnaire status, contract review dates. | A.5.19-A.5.22 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | Clause 6.2 |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist (access, assets, agreements). | A.6.1, A.6.2, A.6.5, A.5.11 |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | A.5.29, A.5.30 |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts and current compliance status. | Clause 4.2, A.5.31 |
| `Management_Review_Agenda_Template.md` | Standing agenda for leadership's periodic ISMS review. | Clause 9.3 |

## Suggested workflow

1. Populate the **Asset Inventory** first — everything else references assets.
2. Run a **risk assessment** into the **Risk Register**, linking risks to assets and to controls
   in `controls.csv`.
3. Complete the **SoA** — for each control, decide applicability based on the risk register's
   treatment decisions, and record implementation status.
4. As controls are implemented, log supporting proof in the **Evidence Submission Log**.
5. Run periodic **internal audits** using the checklist, referencing the same evidence log.
6. Bring audit results, risk register changes, and SoA status into the **Management Review**.
