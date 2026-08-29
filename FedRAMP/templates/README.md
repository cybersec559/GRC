# FedRAMP Templates

Generic, fillable templates supporting a FedRAMP authorization and continuous monitoring program.
Pair with `../controls.csv` (the 39-requirement FedRAMP program catalog) and
`../FedRAMP-Framework.md`. For control-by-control (NIST SP 800-53) tracking, pair these with the
catalog in the sibling `NIST-800-53` folder. None of these files contain any organization-specific
data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `FedRAMP_Compliance_Matrix_Template.csv` | Pre-populated with all 39 FedRAMP program requirements; track applicability to your authorization path, implementation status, evidence, owner. | Authorization package scoping |
| `Asset_Inventory_Template.csv` | System inventory / authorization boundary component register with CIA ratings and explicit boundary flag. | CAT-2, BND-1 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, requirement linkage. | CAT-1, CAT-2 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 39 requirements; framed as a pre-3PAO-assessment readiness review. | 3PAO-1 |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per requirement, e.g. for SSP/SAR support or ConMon deliverables. | DOC-1 through DOC-10 |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for FedRAMP-relevant roles (ISSO, CSO Program Manager). | PS-1 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring FedRAMP activities. | Across all requirements |
| `Incident_Management_Tracker.csv` | Log of security incidents, with an explicit US-CERT notification deadline field. | INC-1, INC-2 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable media, flagged for federal data content. | BND-2 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site. | BND-2 |
| `POAM_Template.csv` | FedRAMP-specific: Plan of Action and Milestones — weaknesses, risk level, milestones, resources, scheduled completion, status. | DOC-4, CONMON-2 |
| `Policy_Inventory_Register.csv` | Master list of every policy — owner, version, approval date, next review date. | DOC-1 through DOC-8 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log, flagged for authorization-boundary systems. | PS-1 |
| `Vendor_ThirdParty_Risk_Register.csv` | Leveraged/underlying provider risk tier, FedRAMP authorization-on-file status, data access level. | BND-3 |
| `Continuous_Monitoring_ConMon_Log.csv` | FedRAMP-specific: tracks the required monthly vuln scan / monthly POA&M update / annual assessment / annual pentest cadence. | CONMON-1 through CONMON-6 |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination checklist. | PS-1, DOC-8 |
| `Contingency_Plan_Test_Log.csv` | Contingency Plan test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | DOC-5, CONMON-5 |
| `Significant_Change_Request_Log.csv` | FedRAMP-specific: tracks major system changes requiring agency/JAB notification before implementation. | SCR-1, SCR-2 |
| `Authorization_Review_Agenda_Template.md` | Standing agenda for periodic authorization/ConMon status review. | CONMON-6 |

## Suggested workflow

1. **Categorize and scope** — complete FIPS 199 categorization, then populate the **Asset
   Inventory** as your system inventory / authorization boundary component register.
2. Run a **risk assessment** into the **Risk Register**, linking risks to requirements.
3. Complete the **FedRAMP Compliance Matrix** for all 39 program requirements, marking applicability
   to your chosen authorization path (JAB, Agency, or Tailored/LI-SaaS).
4. Engage a **3PAO** and run a pre-assessment readiness review using the **Internal Audit
   Checklist** before the formal Security Assessment.
5. Log supporting proof continuously in the **Evidence Submission Log** as the SSP, SAP, and SAR
   come together.
6. Open and track findings in the **POA&M Template** — this becomes a living document immediately
   after the initial assessment and stays open through the ConMon lifecycle.
7. Once authorized, begin the **Continuous Monitoring (ConMon) Log** cadence — monthly scans,
   monthly POA&M updates, annual assessment, annual penetration test — these have hard recurring
   deadlines, not "periodic" ones.
8. Log any planned major changes in the **Significant Change Request Log** and notify the AO/JAB
   before implementation.
9. Track incidents in the **Incident Management Tracker**, watching the explicit US-CERT
   notification deadline field.
10. Bring compliance matrix status, POA&M status, ConMon results, and SCR activity into the
    **Authorization Review** meeting on a recurring cadence.
