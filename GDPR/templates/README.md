# GDPR Templates

Generic, fillable templates supporting a GDPR compliance program. Pair with `../controls.csv`
(the 50-entry reference catalog) and `../GDPR-Framework.md`. None of these files contain any
organization-specific data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `GDPR_Compliance_Matrix_Template.csv` | Pre-populated with all 50 catalog entries; track applicability, implementation status, evidence, owner. | Program-wide scoping |
| `Records_of_Processing_Activities_Template.csv` | GDPR-specific: the mandatory RoPA — purpose, data subject/data categories, lawful basis, recipients, transfers, retention, security measures. | Art. 30 |
| `Data_Protection_Impact_Assessment_Template.csv` | GDPR-specific: necessity/proportionality assessment, risks to data subjects, mitigations, DPO consultation, residual risk, approval. | Art. 35-36 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, article linkage. | Art. 24, Art. 32 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 50 catalog entries; track conformance findings per audit/readiness review cycle. | Accountability (Art. 5(2), Art. 24) |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per article — what, when, by whom, review status, renewal date. | Art. 5(2) (Accountability) |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for privacy-relevant roles (DPO, privacy engineering, etc.). | Art. 37-39 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring GDPR activities. | Across all articles |
| `Data_Breach_Incident_Tracker.csv` | GDPR-specific: incident log with an explicit 72-hour supervisory authority notification clock and a separate data subject notification decision field. | Art. 33-34 |
| `Data_Subject_Request_Log.csv` | GDPR-specific: tracks access/erasure/portability/rectification requests against the statutory 1-month response clock. | Art. 12-22 |
| `Nonconformity_Corrective_Action_Register.csv` | Tracks corrective/preventive actions from any source through root cause to verified closure. | Art. 24 |
| `Policy_Inventory_Register.csv` | Master list of every privacy policy — privacy notice, retention policy, DSR procedure, breach response plan — owner, version, approval, next review date. | Art. 12-14, Art. 5(1)(e) |
| `Vendor_ThirdParty_Risk_Register.csv` | Vendor/sub-processor risk tier, data access level, DPA status, sub-processor approval status, contract review dates. | Art. 28 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable privacy objectives with target vs. actual performance (e.g. DSR turnaround, breach notification timeliness). | Program management |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire privacy/data-handling setup and termination task checklist. | Art. 5(2), Art. 28, Art. 32 |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log for systems processing personal data. | Art. 5(1)(f), Art. 32 |
| `International_Transfer_Register.csv` | GDPR-specific: tracks each international transfer, destination country, transfer mechanism/safeguard (adequacy/SCCs/BCR/derogation), and transfer impact assessment status. | Art. 44-49 |
| `Compliance_Review_Agenda_Template.md` | Standing agenda for periodic leadership review of the GDPR program, including a DPO report. | Art. 24, Art. 39 |

## Suggested workflow

1. Build the **Records of Processing Activities (RoPA)** first — it is the mandatory foundation
   every other artifact references.
2. For each processing activity, confirm the **lawful basis** and complete a **DPIA** where the
   processing is likely to be high-risk.
3. Run a **risk assessment** into the **Risk Register**, linking risks to processing activities
   and articles.
4. Complete the **GDPR Compliance Matrix** — for each of the 50 catalog entries, record
   applicability and implementation status.
5. Stand up the **Data Subject Request Log** and **Data Breach Incident Tracker** before you need
   them — both carry hard statutory clocks (1 month for DSRs, 72 hours for breach notification)
   that are much harder to meet if the process is built during a live event.
6. Populate the **Vendor/Third-Party Risk Register** and **International Transfer Register** for
   every processor, sub-processor, and cross-border data flow.
7. Log ongoing proof in the **Evidence Submission Log**.
8. Run periodic **internal audits** using the checklist, referencing the same evidence log.
9. Track gaps in the **Nonconformity & Corrective Action Register** through to verified closure.
10. Bring audit results, DSR/breach metrics, DPIA status, and transfer register changes into the
    **Compliance Review**, including the DPO's report.
