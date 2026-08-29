# HIPAA Templates

Generic, fillable templates supporting a HIPAA Security Rule (and relevant Privacy Rule) compliance
program. Pair with `../controls.csv` (the 58-row reference catalog) and
`../HIPAA-Security-Rule-Framework.md`. None of these files contain any organization-specific data
or real PHI — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `HIPAA_Compliance_Matrix_Template.csv` | Pre-populated with all 58 rows from `controls.csv`; track implementation approach (Implemented/Equivalent Alternative/Not Applicable - Documented), status, evidence, owner. | All standards |
| `Asset_Inventory_Template.csv` | ePHI-focused asset register — flags whether each asset contains ePHI, with CIA (Confidentiality/Integrity/Availability) ratings. | 164.308(a)(1)(i) |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, standard linkage. | 164.308(a)(1)(i)-(ii) |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 58 rows from `controls.csv`; track conformance findings per audit/evaluation cycle. | 164.308(a)(8) |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per standard — what, when, by whom, review status, renewal date. | 164.316(b) |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence (education, certification, training, experience) for HIPAA-relevant roles (Security Officer, Privacy Officer). | 164.308(a)(2) |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring HIPAA program activities. | Across all standards |
| `Incident_Management_Tracker.csv` | Log of security incidents (164.308(a)(6) framing) from detection through containment, root cause, and closure — includes breach determination and the Breach Notification Rule's 60-day notification clock. | 164.308(a)(6)(i), 164.400-414 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, flagged for ePHI content, classification, encryption status, and lifecycle status. | 164.310(d)(1) |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site (courier, hand-carry, electronic transfer), with protection and receipt confirmation. | 164.310(d)(1)(iii) |
| `Nonconformity_Corrective_Action_Register.csv` | Tracks corrective/preventive actions from any source (audit, incident, complaint, management review) through root cause to verified closure. | 164.308(a)(8), 164.316 |
| `Policy_Inventory_Register.csv` | Master list of every HIPAA policy — owner, version, approval date, next review date. | 164.316(a) |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | 164.308(a)(4)(iii), 164.312(a)(1)(i) |
| `Business_Associate_Agreement_Register.csv` | HIPAA-specific: tracks each business associate, BAA execution/renewal dates, and PHI access level — replaces the generic vendor risk register given HIPAA's specific legal BAA requirement. | 164.308(b)(1), 164.314(a)(1) |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | Program management |
| `Workforce_Onboarding_Offboarding_Checklist.csv` | New-workforce-member security setup and termination task checklist (HIPAA uses "workforce," not just employees/contractors). | 164.308(a)(3), 164.308(a)(4)(ii) |
| `Contingency_Plan_Test_Log.csv` | HIPAA-specific contingency plan test log — Data Backup Plan, Disaster Recovery Plan, Emergency Mode Operation Plan, and Applications/Data Criticality Analysis, with RTO/RPO targets vs. achieved. | 164.308(a)(7) |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts (HIPAA, Breach Notification Rule, state law) and current compliance status. | 164.308, 164.400-414 |
| `Compliance_Review_Agenda_Template.md` | Standing agenda for leadership's periodic HIPAA compliance review. | 164.308(a)(8), 164.316 |

## Suggested workflow

1. Populate the **Asset Inventory** first, flagging every asset that contains ePHI — everything
   else references assets.
2. Run a **risk analysis** into the **Risk Register**, linking risks to assets and to standards
   in `controls.csv`. This is the Required foundation the rest of the program builds on.
3. Complete the **HIPAA Compliance Matrix** — for each standard/implementation specification,
   record the implementation approach (implemented as written, equivalent alternative, or
   documented non-applicability for addressable items) and current status.
4. Inventory every **Business Associate** and execute BAAs before any ePHI flows; track
   renewal/review dates in the **Business Associate Agreement Register**.
5. As controls are implemented, log supporting proof in the **Evidence Submission Log**.
6. Run periodic **internal audits/evaluations** using the checklist, referencing the same
   evidence log.
7. Test contingency plans on a recurring cadence using the **Contingency Plan Test Log**.
8. Bring audit results, risk register changes, BAA status, and incident/breach determinations
   into the **Compliance Review**.
