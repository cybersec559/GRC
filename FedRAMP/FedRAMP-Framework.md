# FedRAMP — Reference Guide for Security Professionals

A working reference for building, assessing, or pursuing authorization under FedRAMP (Federal Risk
and Authorization Management Program). Covers the impact levels and authorization paths, the
relationship to NIST SP 800-53, an implementation roadmap, and a cross-mapping to ISO/IEC
27001:2022 and SOC 2.

---

## 1. What FedRAMP Is

- A **US federal government program**, not a voluntary industry standard — FedRAMP authorization is
  **mandatory** for any Cloud Service Offering (CSO) used to process, store, or transmit federal
  agency data, regardless of the vendor's location or size.
- Built **on top of NIST SP 800-53** — FedRAMP does not invent its own control catalog. It selects
  the NIST SP 800-53 Low, Moderate, or High baseline that matches the system's FIPS 199
  categorization, then layers on **FedRAMP-specific parameter values and supplemental controls**
  (stricter than the generic NIST baseline in places such as continuous monitoring cadence,
  incident reporting timelines, and specific control parameter selections).
- Distinct from a typical audit-based framework in one important way: **independent third-party
  assessment is mandatory** for the initial authorization (via a 3PAO) — there is no
  self-assessment path, unlike SAQ options in PCI DSS or self-attestation in some other regimes.
- The output of a successful process is an **Authority to Operate (ATO)** — either a Provisional ATO
  from the JAB or an agency-issued ATO — not a certificate. Authorization is tied to a specific
  sponsoring agency (Agency path) or the JAB, and to a specific system boundary.

## 2. Impact Levels and Authorization Paths

| Impact Level | FIPS 199 Basis | Typical Use Case |
|---|---|---|
| Low | Limited adverse effect on operations/assets/individuals if compromised | Low-sensitivity public-facing or administrative systems |
| Moderate | Serious adverse effect | Most CSOs handling controlled but non-sensitive federal data — the most common baseline in practice |
| High | Severe or catastrophic adverse effect | Systems supporting law enforcement, emergency services, financial, or health data at scale |
| LI-SaaS (FedRAMP Tailored) | Low-impact, low-risk SaaS carve-out | SaaS offerings storing minimal data beyond login credentials, no PII of consequence |

| Authorization Path | Issued By | Notes |
|---|---|---|
| JAB Provisional Authorization (P-ATO) | Joint Authorization Board (DoD, DHS, GSA) | Reserved for high-demand, government-wide CSOs; limited slots per year; ConMon reporting goes to the JAB |
| Agency Authorization (Agency ATO) | Sponsoring federal agency | Most common path; requires an agency partner willing to sponsor and review the package |
| FedRAMP Tailored / LI-SaaS | Sponsoring agency, streamlined process | Reduced control set and assessment scope for qualifying low-risk SaaS |

## 3. Relationship to NIST SP 800-53

FedRAMP baselines **select and tailor controls from NIST SP 800-53** — they do not replace it. For
the underlying control catalog (control families, control IDs, control text), see the
**`NIST-800-53` folder in this repo**, which catalogs the base 800-53 controls. This FedRAMP folder
intentionally does **not** re-list those controls; instead, `controls.csv` here catalogs the
**FedRAMP program-level requirements and process obligations** layered on top — categorization,
authorization paths, required artifacts, the 3PAO mandate, continuous monitoring cadence,
significant change management, incident reporting timelines, Marketplace status, boundary
documentation, and personnel security expectations.

In practice: use the NIST-800-53 folder's catalog to track control-by-control implementation
status, and use this folder's `controls.csv` and templates to track the FedRAMP-specific program
mechanics that sit above the control catalog.

## 4. Implementation Roadmap

1. **Categorize impact level** — perform FIPS 199 categorization (Low/Moderate/High) based on the
   federal data types in scope; assess LI-SaaS eligibility if applicable.
2. **Select baseline** — choose the matching FedRAMP-tailored NIST SP 800-53 baseline.
3. **Implement controls + FedRAMP-specific parameters** — implement the base 800-53 controls (see
   NIST-800-53 folder) plus FedRAMP's additional parameters, supplemental guidance, and control
   enhancements.
4. **Engage a 3PAO** — select a FedRAMP-accredited Third Party Assessment Organization; a readiness
   assessment (RAR) can earn a "FedRAMP Ready" Marketplace designation before full assessment.
5. **Complete SSP / SAP / SAR** — develop the System Security Plan, have the 3PAO produce the
   Security Assessment Plan, execute the assessment, and receive the Security Assessment Report.
6. **Obtain sponsorship** — secure a sponsoring agency (Agency path) or JAB commitment before or
   during this process; FedRAMP requires a sponsor to issue authorization.
7. **Authorization** — the AO (or JAB) reviews the full package (SSP, SAR, POA&M) and issues an ATO
   or P-ATO.
8. **Continuous monitoring** — enter the ConMon cycle: monthly vulnerability scans, monthly POA&M
   updates, annual assessment, annual penetration test, annual contingency plan test, and
   significant change request notifications as changes arise.

## 5. Cross-Mapping to Other Frameworks

Useful when an organization pursuing FedRAMP also maintains ISO 27001, SOC 2, or tracks against the
base NIST SP 800-53 catalog directly.

| FedRAMP Program Area | NIST SP 800-53 (see `NIST-800-53` folder) | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria |
|---|---|---|---|
| Categorization & baseline selection (CAT) | RA-2, RA-3, CA-2 | Clause 6.1, A.5.9 | CC3.1-CC3.2 |
| SSP / documentation artifacts (DOC) | PL-2, CP-2, IR-8, CM-9 | A.5.37, A.8.9 | CC5.3 |
| 3PAO independent assessment (3PAO) | CA-2, CA-7 | A.5.35 | CC4.1 |
| Continuous monitoring (CONMON) | CA-7, RA-5, SI-2 | A.8.8, A.8.16 | CC7.1-CC7.2 |
| Significant change management (SCR) | CM-3, CM-4 | A.8.32 | CC8.1 |
| Incident reporting (INC) | IR-6, IR-8 | A.5.24-A.5.28 | CC7.3-CC7.5 |
| Boundary & data flow documentation (BND) | CA-3, SA-9, PL-8 | A.5.9, A.8.20 | CC6.6 |
| Personnel security (PS) | PS-2, PS-3 | A.6.1 | CC1.4 |

**Practical use:** when responding to an agency data call or 3PAO assessor request, check this table
for adjacent 800-53 controls, ISO Annex A controls, or SOC 2 criteria — often the same evidence
(a boundary diagram, a POA&M, an access review) can be reused or lightly adapted to satisfy
multiple frameworks' requests simultaneously.

---
*This is a reference framework, not a substitute for the official FedRAMP Program Management Office
(PMO) documentation, templates, and guidance, or for direct consultation with your sponsoring
agency, the JAB, and your 3PAO. Confirm your actual impact level, authorization path, and current
FedRAMP PMO requirements before treating any item above as mandatory, complete, or authoritative.*
