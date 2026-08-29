# COBIT 2019 Framework — Reference Guide for IT Governance Professionals

A working reference for building, assessing, or auditing an enterprise governance of information
and technology (EGIT) system against COBIT 2019, ISACA's framework for the governance and
management of enterprise IT. Covers the governance/management distinction, the design factor
concept, the 40 governance and management objectives across 5 domains, the capability level model,
an implementation roadmap, and a cross-mapping to security-specific frameworks commonly run
alongside it (ISO/IEC 27001:2022, SOC 2, NIST CSF).

---

## 1. What COBIT Is — and Isn't

COBIT is broader than a security framework. It governs the **entire enterprise use of information
and technology** — strategy alignment, value delivery, resource management, risk, and performance —
of which information security is one component (concentrated mainly in APO13 and DSS05, with risk
management in APO12 touching security risk as one risk category among several).

This is why COBIT sits differently in a GRC toolkit than ISO 27001, SOC 2, or PCI DSS:

- **ISO 27001 / SOC 2 / PCI DSS** are scoped to protecting information and systems — they answer
  "is this environment secure?"
- **COBIT** is scoped to governing IT as a whole — it answers "is IT delivering value, at
  acceptable risk and cost, in a way the enterprise can direct and monitor?" Security is a subset
  of that question, not the whole of it.

COBIT is the framework most often used by **boards, audit committees, and IT governance/internal
audit professionals** — the people accountable for whether IT investment and risk decisions are
sound — rather than by practitioners configuring a specific control. If your audience is "prove we
protect data," reach for ISO/SOC 2/PCI/NIST CSF. If your audience is "prove the board is properly
directing and monitoring IT," reach for COBIT.

COBIT 2019 (the current edition, succeeding COBIT 5) is published by ISACA and organized around
five components: principles for a governance system, governance and management objectives,
design factors, focus areas, and a performance management model (capability levels replacing
COBIT 5's process maturity model).

## 2. Governance vs. Management — the Core Distinction

COBIT draws a hard line between two categories of objectives, each with a different accountable
party:

| | Governance | Management |
|---|---|---|
| Who is accountable | Governing body (board / executive committee) | Executive management |
| Purpose | Evaluate stakeholder needs, direct priorities and decisions, monitor performance | Plan, build, run and monitor activities in alignment with governance direction |
| COBIT domain | EDM (Evaluate, Direct and Monitor) | APO, BAI, DSS, MEA |
| Analogy | Setting direction and holding management to account | Executing against that direction |

Every one of the 40 objectives below is either a **governance objective** (EDM — 5 total) or a
**management objective** (APO/BAI/DSS/MEA — 35 total).

## 3. Design Factors — Why COBIT Rejects "One Size Fits All"

Unlike a fixed control baseline, COBIT 2019 does not assume every objective matters equally to
every enterprise. Instead, it provides **design factors** — inputs used to tailor which governance
and management objectives should be prioritized and to what target capability level. Design
factors include:

- Enterprise strategy (growth, innovation, cost leadership, client service, etc.)
- Enterprise goals cascading from that strategy
- Risk profile (the enterprise's actual IT-related risk exposure by category)
- I&T-related issues currently affecting the enterprise
- Threat landscape
- Compliance requirements
- Role of IT (support vs. factory vs. turnaround vs. strategic)
- Sourcing model for IT (outsourced, cloud, hybrid, insourced)
- IT implementation methods (Agile, DevOps, traditional)
- Enterprise size

The practical output of running these design factors is a **prioritized subset of the 40
objectives** with target capability levels — not a demand to fully mature all 40 at once. This is
the single most important mindset shift from a fixed-control-list framework: COBIT expects you to
tailor, and provides the design factors as the mechanism for doing so, rather than leaving
prioritization ad hoc.

## 4. The 5 Domains — 40 Governance and Management Objectives

| Domain | Full Name | Type | # of Objectives | Focus |
|---|---|---|---|---|
| **EDM** | Evaluate, Direct and Monitor | Governance | 5 | Governing body sets direction and monitors outcomes |
| **APO** | Align, Plan and Organize | Management | 14 | Strategy, architecture, risk, resourcing, vendor and portfolio planning |
| **BAI** | Build, Acquire and Implement | Management | 11 | Solution delivery, change, project and configuration management |
| **DSS** | Deliver, Service and Support | Management | 6 | Day-to-day IT operations, incidents, continuity, security services |
| **MEA** | Monitor, Evaluate and Assess | Management | 4 | Performance monitoring, internal control, compliance, assurance |

See [`controls.csv`](controls.csv) for the full flat catalog of all 40 objectives with
descriptions (Objective ID, Domain, Title, Description).

## 5. The Capability Level Model (0–5)

COBIT 2019 replaced COBIT 5's CMMI-derived process maturity model with a **capability level**
scale, assessed per objective, conceptually similar to CMMI but simplified for direct use:

| Level | Description |
|---|---|
| 0 | Incomplete process — process is not implemented or fails to achieve its purpose |
| 1 | Performed process — process achieves its purpose but is largely ad hoc |
| 2 | Managed process — process is planned, monitored and adjusted; work products established, controlled and maintained |
| 3 | Established process — process is well-defined using a standard process, deployed consistently enterprise-wide |
| 4 | Predictable process — process operates within defined limits and achieves consistent, predictable results |
| 5 | Optimizing process — process is continuously improved to meet current and projected enterprise goals |

Target capability levels are set per objective based on the design factor analysis — not every
objective needs to reach Level 5, and pushing every objective there is typically not a good use of
resources.

## 6. Implementation Roadmap

1. **Understand enterprise context via design factors** — work through strategy, risk profile,
   I&T-related issues, threat landscape, compliance obligations, sourcing model, and the other
   design factors above with governance and executive stakeholders.
2. **Prioritize governance and management objectives** — use the design factor output to identify
   which of the 40 objectives matter most right now, and provisionally set target capability
   levels for each.
3. **Assess current capability levels** — for each prioritized objective, assess current-state
   capability (0–5) through interviews, process walkthroughs, and evidence review.
4. **Define target state** — confirm target capability level per objective (usually 3, sometimes
   4–5 for objectives tied to critical risk or regulatory exposure).
5. **Gap analysis** — document the delta between current and target capability per objective,
   including root causes and dependencies between objectives.
6. **Build the improvement roadmap** — sequence initiatives to close gaps, factoring in resource
   constraints, dependencies (e.g., APO03 Enterprise Architecture often needs to mature before
   BAI03 Solutions Build), and quick wins.
7. **Execute and monitor** — implement improvement initiatives, track progress against target
   capability levels, and report to the governing body (EDM05) on status.
8. **Reassess periodically** — design factors change (new strategy, new risk profile, new
   regulation); revisit prioritization and targets on a regular cycle rather than treating the
   roadmap as a one-time exercise.

## 7. Cross-Mapping: COBIT Security Objectives to Security-Specific Frameworks

Only a subset of COBIT's 40 objectives maps tightly to pure security frameworks — the rest (e.g.,
APO02 Managed Strategy, BAI01 Managed Programs, APO06 Managed Budget and Costs) cover broader IT
governance territory that ISO 27001, SOC 2, and NIST CSF simply don't address. The table below
focuses on the two COBIT objectives most directly concerned with information security:

| COBIT Objective | ISO/IEC 27001:2022 | SOC 2 | NIST CSF 2.0 |
|---|---|---|---|
| **APO13** Managed Security (security management system) | Clause 5 (Leadership), A.5.1 (Policies for information security) | CC1 (Control Environment) | Govern |
| **DSS05** Managed Security Services (roles, access rights, monitoring) | A.5.15-A.5.18 (Access Control), A.8.16 (Monitoring Activities) | CC6 (Logical and Physical Access Controls), CC7 (System Operations) | Protect, Detect |
| APO12 Managed Risk (IT risk, of which security risk is one category) | Clause 6.1 (Planning — risk assessment/treatment) | CC3 (Risk Assessment) | Identify |
| DSS02 Managed Service Requests and Incidents | A.5.24-A.5.28 (Incident Management) | CC7.3-CC7.5 | Respond |
| MEA03 Managed Compliance With External Requirements | A.5.31 (Legal/Statutory/Regulatory Requirements) | CC1.1, CC2.3 | Govern |

**Practical use:** if an organization already maintains ISO 27001, SOC 2, or NIST CSF evidence,
much of that evidence (access reviews, incident logs, risk registers, compliance trackers) can
satisfy an assessor's request for APO13/DSS05 evidence directly. The remaining 35+ COBIT
objectives — strategy, architecture, portfolio, budget, vendor management, projects, quality,
performance monitoring — have no equivalent in a pure security framework and must be assessed on
their own terms using COBIT's design factors and capability model.

## 8. Templates in This Folder

See [`templates/README.md`](templates/README.md) for the full set of 19 fillable templates
adapted to COBIT terminology — a Capability Assessment Matrix in place of a control checklist, a
RACI template reflecting COBIT's native practice-level RACI charts, and a board-oriented
Governance Review Agenda in place of a generic management review.

---
*This is a reference framework, not a substitute for a formal design factor workshop with your
actual governing body and executive stakeholders. Validate objective prioritization and target
capability levels against your organization's actual strategy and risk profile before treating any
objective above as a mandatory baseline.*
