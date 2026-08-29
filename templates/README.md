# ISMS Templates

Generic, fillable templates supporting an ISO/IEC 27001:2022 ISMS. Pair with `../controls.csv`
(the 93-control reference catalog) and `../ISO-27001-2022-Framework.md`. None of these files
contain any organization-specific data — copy them into your own tracker and fill in the blanks.

| Template | Purpose | Ties to |
|---|---|---|
| `SoA_Template.csv` | Statement of Applicability — pre-populated with all 93 controls; mark applicability, justification, status, evidence, owner. | Clause 6.1.3 |
| `Asset_Inventory_Template.csv` | Asset register with CIA (Confidentiality/Integrity/Availability) ratings per asset, driving classification. | A.5.9, A.5.12 |
| `Risk_Register_Template.csv` | Risk identification, scoring (inherent → residual), treatment decision, control linkage. | Clause 6.1 |
| `Internal_Audit_Checklist_Template.csv` | Pre-populated with management clauses (4-10) + all 93 controls; track conformance findings per audit cycle. | Clause 9.2 |
| `Evidence_Submission_Log_Template.csv` | Track evidence submitted per control — what, when, by whom, review status, renewal date. | Clause 7.5 (Documented Information) |
| `Management_Review_Agenda_Template.md` | Standing agenda for leadership's periodic ISMS review. | Clause 9.3 |

## Suggested workflow

1. Populate the **Asset Inventory** first — everything else references assets.
2. Run a **risk assessment** into the **Risk Register**, linking risks to assets and to controls
   in `controls.csv`.
3. Complete the **SoA** — for each control, decide applicability based on the risk register's
   treatment decisions, and record implementation status.
4. As controls are implemented, log supporting proof in the **Evidence Submission Log**.
5. Run periodic **internal audits** using the checklist, referencing the same evidence log.
6. Bring audit results, risk register changes, and SoA status into the **Management Review**.
