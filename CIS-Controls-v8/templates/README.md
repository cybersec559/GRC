# CIS Controls v8 Templates

Generic, fillable templates supporting a CIS Controls v8 implementation program. Pair with
`../controls.csv` (the 153-Safeguard reference catalog) and
`../CIS-Controls-v8-Framework.md`. None of these files contain any organization-specific data —
copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to Control(s) |
|---|---|---|
| `CIS_Controls_Implementation_Matrix_Template.csv` | CIS's equivalent of an SoA — pre-populated with all 153 Safeguards; mark whether each applies to your Implementation Group, implementation status, evidence, owner. | All 18 Controls |
| `Asset_Inventory_Template.csv` | Enterprise asset and software asset register with CIA ratings driving classification. | 1, 2 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, Safeguard linkage. | Cross-cutting |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 153 Safeguards; track conformance findings per self-assessment cycle. | All 18 Controls |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per Safeguard — what, when, by whom, review status. | Cross-cutting |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for security-relevant roles. | 14, 17 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring CIS Controls activities, by Control number. | All 18 Controls |
| `Incident_Management_Tracker.csv` | Log of security incidents from detection through containment, root cause, and closure. | 17 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, classification, encryption status. | 3 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site. | 3 |
| `Nonconformity_Corrective_Action_Register.csv` | Tracks gaps from any source (self-assessment, audit, incident, management review) through root cause to verified closure. | Cross-cutting |
| `Policy_Inventory_Register.csv` | Master list of every policy — owner, version, approval date, next review date. | 3, 4 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | 5, 6 |
| `Vendor_ThirdParty_Risk_Register.csv` | Service provider risk tier, data access level, assessment status. | 15 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | Cross-cutting |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist. | 5, 6, 14 |
| `Data_Recovery_Test_Log.csv` | CIS-specific: backup/recovery test log — scenario, isolated recovery instance used, RTO/RPO targets vs. achieved, issues, remediation. | 11 |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts and current compliance status. | Cross-cutting |
| `Implementation_Group_Review_Agenda_Template.md` | Standing agenda for leadership's periodic review of Implementation Group maturity progress. | Cross-cutting |

## Suggested workflow

1. Determine your **Implementation Group** (IG1/IG2/IG3) using
   `../CIS-Controls-v8-Framework.md` Section 2, based on organization size, risk exposure, and
   resources available.
2. Populate the **Asset Inventory** first — Controls 1 and 2 (enterprise assets and software
   assets) are the foundation every other Safeguard depends on.
3. Run a **risk assessment** into the **Risk Register**, linking risks to assets and to Safeguards
   in `controls.csv`.
4. Complete the **Implementation Matrix** — for each Safeguard, mark whether it applies to your
   IG (all Safeguards at your IG and below are in scope, cumulative) and record implementation
   status.
5. As Safeguards are implemented, log supporting proof in the **Evidence Submission Log**.
6. Begin the **Data Recovery Test Log** cadence early — Control 11 is foundational and its
   testing requirement is easy to defer if not tracked on a recurring schedule.
7. Run periodic **internal audits/self-assessments** using the checklist, optionally supported by
   CIS-CAT or similar automated assessment tooling.
8. Track any gaps in the **Nonconformity & Corrective Action Register** through to verified
   closure.
9. Bring self-assessment results, risk register changes, and matrix status into the
   **Implementation Group Review** — including a decision on whether to progress toward the next
   IG.
