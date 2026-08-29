# NIST SP 800-53 Rev 5 / RMF Templates

Generic, fillable templates supporting a NIST SP 800-53 Rev 5 control implementation and Risk
Management Framework (RMF) program. Pair with `../controls.csv` (the 302-base-control reference
catalog) and `../NIST-800-53-Framework.md`. None of these files contain any organization-specific
data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `Control_Implementation_Summary_Template.csv` | NIST's actual document type (CIS) — pre-populated with all 302 base controls; mark baseline, implementation status, responsible role, evidence, last assessed date. | RMF Step 4 (Implement) / Step 5 (Assess) |
| `Asset_Inventory_Template.csv` | System Component Inventory with CIA ratings per component, driving categorization. | CM-8 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, control linkage. | RA-3 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 302 base controls; self-assessment ahead of a formal Security Control Assessment. | CA-2 (preparation) |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per control — what, when, by whom, review status, renewal date. | CA-2, PL-2 |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence (education, certification, training, experience) for security-relevant roles. | AT-3, PM-13 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring RMF activities (categorization, control selection, assessment, authorization, continuous monitoring, etc.). | Across all RMF steps |
| `Incident_Management_Tracker.csv` | Log of security incidents from detection through containment, root cause, corrective action, and closure. | IR-4, IR-5, IR-6 |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, categorization, encryption status, and lifecycle status. | MP-4 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site (courier, hand-carry, electronic transfer), with protection and receipt confirmation. | MP-5 |
| `POAM_Template.csv` | NIST-specific: Plan of Action and Milestones — the required RMF artifact for tracking control weaknesses/deficiencies through remediation. | CA-5 |
| `Policy_Inventory_Register.csv` | Master list of every control policy — owner, version, approval date, next review date. | -1 controls (Policy and Procedures) across all families |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | AC-2, AC-6 |
| `Vendor_ThirdParty_Risk_Register.csv` | Supply chain risk register — vendor risk tier, data access level, security assessment status, contract review dates. | SR-2, SR-6 |
| `Security_Objectives_KPI_Tracker.csv` | Measurable security objectives with target vs. actual performance. | PM-6 |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist (access, assets, agreements). | PS-2, PS-3, PS-4, PS-5, PS-6 |
| `Contingency_Plan_Test_Log.csv` | Contingency plan test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | CP-4 |
| `System_Security_Plan_Outline_Template.md` | NIST-specific: the SSP is the master RMF document for a system; a structured skeleton covering identification, categorization, control implementation reference, interconnections, roles, and rules of behavior. | PL-2 |
| `Authorization_Review_Agenda_Template.md` | Standing agenda for the Authorizing Official's periodic authorization/ATO review. | CA-6, CA-7 |

## Suggested workflow (RMF steps)

1. **Categorize** the system — complete the **System Component Inventory** and the categorization
   section of the **System Security Plan Outline** (FIPS 199, per `RA-2`).
2. **Select** a control baseline (Low/Moderate/High) and tailor it — record the selection in the
   **Control Implementation Summary** (`PL-10`, `PL-11`).
3. Run a **risk assessment** into the **Risk Register**, linking risks to system components and to
   controls in `controls.csv` (`RA-3`).
4. **Implement** controls, logging supporting proof in the **Evidence Submission Log** as you go.
5. Track any known weaknesses or deficiencies in the **POA&M** from the moment they're identified —
   don't wait for a formal assessment to start this.
6. Run a **self-assessment** using the **Internal Audit Checklist** ahead of the formal Security
   Control Assessment (`CA-2`).
7. Bring assessment results, POA&M status, and risk register changes into the **Authorization
   Review** for the Authorizing Official's decision (`CA-6`).
8. Once authorized, run **continuous monitoring** — access reviews, contingency plan testing,
   vendor risk reviews, and KPI tracking — on a recurring cadence, feeding results back into the
   POA&M and the next Authorization Review (`CA-7`).
