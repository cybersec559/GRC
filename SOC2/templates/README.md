# SOC 2 Templates

Generic, fillable templates supporting a SOC 2 readiness and audit program. Pair with
`../controls.csv` (the 43-criteria reference catalog) and
`../SOC2-Trust-Services-Criteria-Framework.md`. None of these files contain any
organization-specific data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `TSC_Controls_Matrix_Template.csv` | SOC 2's equivalent of an SoA — pre-populated with all 43 criteria; mark in-scope status, control description, implementation status, evidence, owner. | Report scoping |
| `Asset_Inventory_Template.csv` | Asset register with CIA ratings driving classification. | CC6.1, C1.1 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, criteria linkage. | CC3.1-CC3.4 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 43 criteria; track effectiveness findings per readiness review/audit cycle. | CC4.1 |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per criterion across the observation period. | Type II sampling support |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for security-relevant roles. | CC1.4 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring SOC 2 activities. | Across all criteria |
| `Incident_Management_Tracker.csv` | Log of security incidents from detection through containment, root cause, and closure. | CC7.3-CC7.5 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, classification, encryption status. | C1.2 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site. | C1.2 |
| `Control_Exception_Remediation_Register.csv` | Tracks control exceptions from any source through root cause to verified closure — SOC 2's term for what ISO calls a "nonconformity." | CC4.2 |
| `Policy_Inventory_Register.csv` | Master list of every policy — owner, version, approval date, next review date. | CC5.3 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — one of the most commonly sampled evidence items in a Type II audit. | CC6.2, CC6.3 |
| `Vendor_ThirdParty_Risk_Register.csv` | Vendor risk tier, data access level, security questionnaire status. | CC9.2 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | CC4.1 |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination checklist. | CC1.4, CC6.2, CC6.5 |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log. | CC9.1, A1.3 |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts and compliance status. | C1.1 |
| `Compliance_Review_Agenda_Template.md` | Standing agenda for periodic leadership compliance review. | CC4.2 |

## Suggested workflow

1. Scope the report — decide which Trust Service Categories beyond mandatory Security apply,
   using `../SOC2-Trust-Services-Criteria-Framework.md` Section 3.
2. Populate the **Asset Inventory**.
3. Run a **risk assessment** into the **Risk Register**, linking risks to criteria.
4. Complete the **TSC Controls Matrix** — for each criterion, record in-scope status and
   implementation.
5. As controls operate, log supporting proof continuously in the **Evidence Submission Log** —
   Type II auditors sample evidence across the whole observation period, so this needs to be an
   ongoing habit, not a pre-audit scramble.
6. Run periodic **internal readiness reviews** using the checklist.
7. Track any gaps in the **Control Exception & Remediation Register** through to verified closure.
8. Bring review results, risk register changes, and matrix status into the **Compliance Review**.
