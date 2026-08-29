# CCPA/CPRA Templates

Generic, fillable templates supporting a CCPA/CPRA privacy compliance program. Pair with
`../controls.csv` (the 37-entry reference catalog) and `../CCPA-CPRA-Framework.md`. None of these
files contain any organization-specific data — copy them into your own tracker and fill in the
blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `CCPA_Compliance_Matrix_Template.csv` | Pre-populated with all 37 catalog entries; track applicability, implementation status, evidence, owner. | Program scoping |
| `Personal_Information_Inventory_Template.csv` | CCPA-specific: replaces a generic asset inventory — categories of personal information, sensitivity, source, purpose, sold/shared status, retention, and downstream recipients. | Civ. Code 1798.100, 1798.110, 1798.115 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, reference linkage. | Civ. Code 1798.100(c) |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with all 37 catalog entries; track conformance findings per readiness review cycle. | Program self-assessment |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per reference item — what, when, by whom, review status, renewal date. | Ongoing evidence hygiene |
| `Competence_Records_Template.csv` | Documented evidence of personnel competence for privacy-relevant roles. | Civ. Code 1798.100(c) |
| `RACI_Template.csv` | Responsible/Accountable/Consulted/Informed matrix across recurring CCPA/CPRA activities. | Across all reference items |
| `Data_Breach_Incident_Tracker.csv` | CCPA-specific: incident log flagging sensitive PI involvement, encryption status, estimated consumers affected, and private-right-of-action exposure. | Civ. Code 1798.150 |
| `Consumer_Request_Log.csv` | CCPA-specific: tracks know/delete/correct/opt-out/limit-use-of-SPI requests against the 45-day (extendable to 90-day) statutory response clock. | Civ. Code 1798.130(a)(2) |
| `Nonconformity_Corrective_Action_Register.csv` | Tracks corrective/preventive actions from any source through root cause to verified closure. | Program remediation |
| `Policy_Inventory_Register.csv` | Master list of every privacy-related policy — owner, version, approval date, next review date. | Civ. Code 1798.130 |
| `Vendor_ThirdParty_Risk_Register.csv` | Adapted for CCPA/CPRA: tracks each vendor's role (Service Provider/Contractor/Third Party) and whether its contract contains the role-appropriate required terms. | Civ. Code 1798.100(d), 1798.140(ai)(2) |
| `Security_Objectives_KPI_Tracker.csv` | Measurable privacy program objectives with target vs. actual performance. | Program management |
| `Onboarding_Offboarding_Security_Checklist.csv` | New-hire and termination task checklist for personnel with access to personal information. | Civ. Code 1798.100(c) |
| `BC_DR_Test_Log.csv` | Business continuity / disaster recovery test log for systems supporting consumer request handling. | Civ. Code 1798.130(a)(2) (supporting) |
| `Cybersecurity_Audit_and_Risk_Assessment_Log.csv` | CPRA-specific: tracks the mandated periodic risk assessments and independent cybersecurity audits for high-risk processing. | Civ. Code 1798.185(a)(15)(A)-(B) |
| `Compliance_Review_Agenda_Template.md` | Standing agenda for periodic leadership review of the privacy compliance program. | Program governance |

## Suggested workflow

1. Confirm **applicability** using the threshold test in `../CCPA-CPRA-Framework.md` Section 1
   before populating anything else.
2. Populate the **Personal Information Inventory** — everything else references its categories.
3. Run a **risk assessment** into the **Risk Register**, linking risks to reference items in
   `controls.csv`.
4. Complete the **CCPA Compliance Matrix** — for each reference item, mark applicability and
   implementation status.
5. Update the **Policy Inventory** (privacy policy, notice at collection) and confirm the opt-out
   mechanism and opt-out preference signal handling are reflected in evidence.
6. Classify every vendor in the **Vendor/Third Party Risk Register** by role and confirm contract
   terms match that role.
7. Stand up the **Consumer Request Log** as an ongoing operational log — the 45-day clock starts
   the moment a request is received, so this needs to be a daily habit, not a periodic catch-up.
8. If high-risk processing applies, begin the **Cybersecurity Audit and Risk Assessment Log**
   cadence.
9. Log any incidents in the **Data Breach Incident Tracker**, flagging private-right-of-action
   exposure immediately.
10. Run periodic **internal audits** using the checklist, referencing the same evidence log.
11. Track any gaps in the **Nonconformity & Corrective Action Register** through to verified
    closure, and bring review results into the **Compliance Review**.
