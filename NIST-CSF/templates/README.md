# NIST CSF 2.0 Templates

Generic, fillable templates supporting a NIST Cybersecurity Framework (CSF) 2.0 program. Pair
with `../controls.csv` (the 106-subcategory reference catalog) and
`../NIST-CSF-2.0-Framework.md`. None of these files contain any organization-specific data — copy
them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `Current_Target_Profile_Template.csv` | CSF's equivalent of a Statement of Applicability / compliance matrix — pre-populated with all 106 subcategories; record Current Tier, Target Tier, gap description, implementation status, evidence, and owner. | All Functions |
| `Asset_Inventory_Template.csv` | Asset register with CIA (Confidentiality/Integrity/Availability) ratings per asset, driving prioritization. | ID.AM |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, subcategory linkage. | ID.RA |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 106 subcategories; track conformance findings per review cycle. | GV.OV |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per subcategory — what, when, by whom, review status, renewal date. | GV.OV |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence (education, certification, training, experience) for security-relevant roles. | GV.RR-04 |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring CSF activities (Profile development, Tier assessment, gap analysis, etc.). | GV.RR, supports role clarity across all Functions |
| `Incident_Management_Tracker.csv` | Log of security incidents from detection through containment, root cause, corrective action, and closure. | RS.MA-RS.MI |
| `Media_Inventory_Log.csv` | Inventory of physical/removable storage media, classification, encryption status, and lifecycle status. | PR.PS-03 |
| `Media_Transport_Log.csv` | Chain-of-custody log for media moved off-site (courier, hand-carry, electronic transfer), with protection and receipt confirmation. | PR.PS-03 |
| `Nonconformity_Gap_Register.csv` | Tracks corrective/preventive actions from any source (gap analysis, internal review, incident, Tier assessment) through root cause to verified closure. CSF calls these "gaps" rather than nonconformities. | GV.OV, ID.IM |
| `Policy_Inventory_Register.csv` | Master list of every cybersecurity policy — owner, version, approval date, next review date. | GV.PO |
| `Access_Review_Recertification_Log.csv` | Periodic user-access review log — accounts reviewed, findings, access revoked. | PR.AA-05, PR.AA-01 |
| `Vendor_ThirdParty_Risk_Register.csv` | Vendor risk tier, data access level, security questionnaire status, contract review dates. | GV.SC |
| `Security_Objectives_KPI_Tracker.csv` | Measurable cybersecurity objectives with target vs. actual performance. | GV.RM, ID.IM |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire security setup and termination task checklist (access, assets, agreements). | GV.RR-04, PR.AT-01, PR.AA |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log — scenario, RTO/RPO targets vs. achieved, issues, remediation. | PR.IR-03, RC.RP |
| `Legal_Regulatory_Requirements_Register.csv` | Applicable laws/regulations/contracts and current compliance status. | GV.OC-03 |
| `Profile_Review_Agenda_Template.md` | Standing agenda for leadership's periodic Profile review (CSF's equivalent of ISO's Management Review / SOC 2's Compliance Review). | GV.OV |

## Suggested workflow

1. Populate the **Asset Inventory** first — everything else references assets.
2. Run a **risk assessment** into the **Risk Register**, linking risks to assets and to
   subcategories in `controls.csv`.
3. Build the **Current Profile** — for each subcategory in `Current_Target_Profile_Template.csv`,
   record the Current Tier and implementation status based on what's actually in place today.
4. Define the **Target Profile** — for each subcategory, record the Target Tier reflecting the
   organization's risk tolerance and objectives.
5. Run the **gap analysis** — the difference between Current and Target Tier per subcategory
   becomes a row in the **Gap Register**, with an owner and target completion date.
6. As controls are implemented, log supporting proof in the **Evidence Submission Log**.
7. Run periodic **internal reviews** using the checklist, referencing the same evidence log.
8. Bring Tier assessment results, gap register changes, and Profile status into the **Profile
   Review** meeting.
