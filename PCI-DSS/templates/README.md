# PCI DSS Templates

Generic, fillable templates supporting a PCI DSS v4.0 compliance program. Pair with
`../controls.csv` (the 63-requirement reference catalog) and `../PCI-DSS-4.0-Framework.md`. None
of these files contain any organization-specific data — copy them into your own tracker and fill
in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `PCI_DSS_Compliance_Matrix_Template.csv` | Pre-populated with all 63 requirements; track in-scope status, validation approach, implementation status, evidence, owner. | Report/SAQ scoping |
| `Asset_Inventory_Template.csv` | Asset register with CIA ratings and explicit CDE flag. | 12.5 |
| `Risk_Register_Template.csv` | Risk identification, scoring, treatment decision, requirement linkage. | 12.3 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 63 requirements; track conformance per readiness review/ROC cycle. | Internal readiness review |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per requirement. | QSA/ROC evidence support |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for PCI-relevant roles. | 12.6, 12.7 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring PCI activities. | Across all requirements |
| `Incident_Management_Tracker.csv` | Log of security incidents, flagging CDE impact. | 12.10 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable media, flagged for cardholder data content. | 9.4 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site. | 9.4 |
| `Compensating_Controls_Worksheet_Template.csv` | PCI-specific: documents an alternative control when a requirement can't be met directly, with QSA/ISA validation. | Compensating control validation |
| `Quarterly_ASV_Scan_and_Pentest_Log.csv` | PCI-specific: tracks the required quarterly external scans and annual/semi-annual penetration/segmentation tests. | 11.3, 11.4 |
| `Policy_Inventory_Register.csv` | Master list of every policy — owner, version, approval date, next review date. | 12.1 |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log, flagged for CDE systems. | 7.2, 7.3 |
| `Vendor_ThirdParty_Risk_Register.csv` | TPSP risk tier, attestation-on-file status, data access level. | 12.8, 12.9 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | Program management |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination checklist. | 7.2, 8.2, 9.3, 12.7 |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log. | 12.10 (supporting) |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/card brand mandates and compliance status. | 12.4 |
| `PCI_DSS_Compliance_Review_Agenda_Template.md` | Standing agenda for periodic PCI compliance program review. | 12.4 |

## Suggested workflow

1. **Determine scope** — identify the CDE and complete the **Asset Inventory** flagging CDE
   membership.
2. Run a **risk assessment** into the **Risk Register**.
3. Complete the **PCI DSS Compliance Matrix** for all 63 requirements.
4. Document any **Compensating Controls Worksheets** for requirements not met directly.
5. Begin the **Quarterly ASV Scan & Pentest Log** cadence — this has hard 90-day/annual clocks
   unlike most other framework testing cycles.
6. Log ongoing proof in the **Evidence Submission Log**.
7. Run **internal readiness reviews** using the checklist before ROC/SAQ submission or QSA
   engagement.
8. Track gaps via **Compensating Controls** or standard remediation through to closure.
9. Bring review results into the **PCI DSS Compliance Review** on a recurring cadence.
