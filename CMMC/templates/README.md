# CMMC / NIST SP 800-171 Templates

Generic, fillable templates supporting a CMMC 2.0 / NIST SP 800-171 compliance program. Pair with
`../controls.csv` (the 110-practice Level 2 reference catalog plus illustrative Level 3 rows) and
`../CMMC-2.0-Framework.md`. None of these files contain any organization-specific data — copy them
into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `CMMC_Compliance_Matrix_Template.csv` | Pre-populated with all 118 catalog rows (110 Level 2 + 8 illustrative Level 3); track implementation status, SPRS score impact, evidence, owner. | Program scoping / SPRS prep |
| `Asset_Inventory_Template.csv` | Asset register flagged for FCI/CUI content, driving classification. | AC, MP |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, practice linkage. | RA (Risk Assessment) |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 118 catalog rows; track conformance findings per readiness review cycle. | CA (Security Assessment) |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per practice — what, when, by whom, review status, renewal date. | Assessment evidence support |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for CMMC-relevant roles. | PS, AT |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring CMMC activities. | Across all domains |
| `Incident_Management_Tracker.csv` | Log of security incidents, including the DoD/DIBNet 72-hour cyber incident reporting timeline. | IR (Incident Response) |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, flagged for CUI content. | MP (Media Protection) |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site. | MP (Media Protection) |
| `POAM_Template.csv` | CMMC/NIST-specific required artifact: Plan of Action & Milestones for any practice not yet met. | CA.L2-3.12.2 |
| `Policy_Inventory_Register.csv` | Master list of every policy — owner, version, approval date, next review date. | Cross-domain |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | AC (Access Control) |
| `Vendor_ThirdParty_Risk_Register.csv` | Subcontractor/vendor risk tier, FCI/CUI handling, flow-down clause and CMMC level requirement tracking. | Supply-chain flow-down |
| `SPRS_Score_Tracker.csv` | CMMC-specific: tracks the DoD Supplier Performance Risk System self-assessment score over time. | SPRS submission |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist. | PS (Personnel Security) |
| `Contingency_Plan_Test_Log.csv` | Contingency/backup recovery test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | MP, CA |
| `System_Security_Plan_Outline_Template.md` | CMMC/NIST SP 800-171-specific required artifact: SSP section skeleton. | CA.L2-3.12.4 |
| `Compliance_Review_Agenda_Template.md` | Standing agenda for periodic leadership compliance review. | CA (Security Assessment) |

## Suggested workflow

1. **Determine your required CMMC level** from the contract or anticipated solicitation before
   doing anything else — it sets the practice scope (17 vs. 110 vs. 110 + enhanced) and the
   assessment path.
2. Populate the **Asset Inventory**, explicitly flagging which assets touch FCI vs. CUI.
3. Run a **risk assessment** into the **Risk Register**, linking risks to practices in
   `../controls.csv`.
4. Complete the **CMMC Compliance Matrix** for all 110 (or 118, if tracking illustrative Level 3
   rows) practices — this is your working gap-assessment artifact.
5. Draft the **System Security Plan**, describing how each practice is actually implemented in
   your environment.
6. Calculate your **SPRS score** and log it in the **SPRS Score Tracker** — start this early, since
   score trend over time is itself useful evidence of program maturity.
7. Open a **POA&M** entry for every practice not yet met, with real milestones and dates.
8. Log ongoing proof in the **Evidence Submission Log** as controls are implemented.
9. Run periodic **internal readiness reviews** using the checklist before a self-assessment
   affirmation or C3PAO/DIBCAC engagement.
10. Track subcontractor flow-down obligations continuously in the **Vendor/Third-Party Risk
    Register** — a prime's certification can be undermined by an unassessed subcontractor.
11. Bring compliance matrix status, POA&M progress, SPRS trend, and incident history into the
    **Compliance Review** on a recurring cadence.
