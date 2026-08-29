# CMMC 2.0 — Reference Guide for Security Professionals

A working reference for building, assessing, or preparing for a Cybersecurity Maturity Model
Certification (CMMC) 2.0 assessment. Covers what CMMC is and why it exists, the 3-level structure
and assessment paths, the relationship to NIST SP 800-171/800-172, an implementation roadmap, and
a cross-mapping to NIST SP 800-53, ISO/IEC 27001:2022, and SOC 2.

---

## 1. What CMMC Is

- CMMC is a **DoD contractual cybersecurity requirement** for the Defense Industrial Base (DIB) —
  every organization that bids on, or performs work under, a DoD contract requiring the protection
  of Federal Contract Information (FCI) or Controlled Unclassified Information (CUI).
- It is not a law or a general-industry standard; it is imposed through the contract itself via
  **DFARS clauses** (principally DFARS 252.204-7012, 7019, 7020, and 7021), and it **flows down**
  from the prime contractor to every subcontractor, vendor, and supplier in the supply chain that
  will touch FCI or CUI in performing the work.
- CMMC 2.0 exists to give the DoD independent verification (rather than pure self-attestation)
  that contractors handling sensitive unclassified defense information have actually implemented
  the safeguarding requirements they've long been contractually obligated to meet.
- **Flow-down in practice:** a prime contractor cannot simply assume its subcontractors are
  compliant — flow-down clauses must appear in subcontracts, and the prime remains exposed to risk
  if a subcontractor's gaps compromise CUI. See `templates/Vendor_ThirdParty_Risk_Register.csv`.

## 2. The 3-Level Structure and Assessment Paths

| Level | Name | # Practices | Protects | Assessment Path |
|---|---|---|---|---|
| 1 | Foundational | 17 | Federal Contract Information (FCI) | Annual self-assessment |
| 2 | Advanced | 110 | Controlled Unclassified Information (CUI) | Self-assessment (most programs) or third-party assessment by a **C3PAO** (Certified Third-Party Assessment Organization) for select "critical" programs |
| 3 | Expert | 110 + a subset of enhanced requirements | CUI on the DoD's highest-priority programs | Government-led assessment by **DIBCAC** (Defense Industrial Base Cybersecurity Assessment Center) |

- **Level 1** practices are drawn directly from the 15 basic safeguarding requirements in **FAR
  52.204-21**, expressed here as 17 individual practices; self-assessment is performed annually
  and affirmed by a senior company official.
- **Level 2** is the level most DIB contractors need, and it is where the bulk of this suite's
  content lives — see Section 3.
- **Level 3** builds on a fully implemented Level 2 foundation by adding a subset of NIST SP
  800-172 enhanced requirements, aimed at defending against advanced persistent threats (APTs) on
  the programs the DoD considers highest-priority. Only DIBCAC — not a C3PAO — assesses Level 3.

## 3. Relationship to NIST SP 800-171 and 800-172

- **CMMC Level 2's 110 practices mirror NIST SP 800-171 Rev 2's 110 security requirements
  exactly** — same 14 control families, same numbering (e.g., practice `AC.L2-3.1.1` corresponds
  directly to NIST SP 800-171 Rev 2 requirement 3.1.1). `controls.csv` in this folder catalogs all
  110 as the authoritative Level 2 practice set.
- **CMMC Level 3 draws from NIST SP 800-172**, which defines *enhanced* security requirements
  layered on top of (not replacing) the 800-171 baseline. Because 800-172 guidance and its
  DoD-specific Level 3 scoping are less universally stable in public documentation than the
  110-practice 800-171 baseline, `controls.csv` includes only a **small, clearly-marked
  illustrative sample** of enhanced requirements rather than an exhaustive catalog — confirm the
  actual current DoD Level 3 assessment scope directly before relying on it for a real program.
- Practically: if an organization has already built its control environment against NIST SP
  800-171 Rev 2 (e.g., for an existing DFARS 252.204-7012 obligation), it has already built the
  substance of CMMC Level 2 — CMMC adds the assessment/certification and affirmation layer on top.

## 4. Implementation Roadmap

1. **Determine the required level** — read the contract (or anticipated solicitation) for its
   CMMC level requirement; confirm whether the program is flagged as requiring third-party
   (C3PAO) assessment or qualifies for self-assessment.
2. **Gap assessment against NIST SP 800-171** — assess current state against all 110 practices in
   `controls.csv`, regardless of whether the ultimate required level is 1 or 2 (Level 1 practices
   are a subset).
3. **Implement practices** — remediate gaps identified in the assessment; prioritize practices
   with the largest SPRS score impact and any tied to a hard contractual deadline.
4. **Complete a System Security Plan (SSP) and score via SPRS** — document system boundaries and
   how each of the 110 practices is implemented (`templates/System_Security_Plan_Outline_Template.md`),
   then calculate a score out of 110 using the DoD's SPRS (Supplier Performance Risk System)
   scoring methodology, which deducts points per unmet practice weighted by its assessed severity.
5. **Build a Plan of Action & Milestones (POA&M)** for any practice not yet met
   (`templates/POAM_Template.csv`) — SPRS submissions can reflect a POA&M for a limited set of
   practices and a limited time window, not a substitute for full implementation.
6. **Assessment** — self-assessment (Level 1, and Level 2 for most programs) or C3PAO third-party
   assessment (Level 2 critical programs) or DIBCAC assessment (Level 3).
7. **Affirmation/certification** — a senior company official affirms continued compliance
   (annually for self-assessments, and at defined intervals following a certification
   assessment); certifications are valid for a defined period before reassessment is required.

## 5. Cross-Mapping to Other Frameworks

Useful when a DIB contractor also carries ISO 27001, SOC 2, or a broader NIST SP 800-53-based
program (e.g., for FedRAMP-adjacent cloud services) — avoid rebuilding evidence collection per
framework where controls genuinely overlap.

| CMMC Level 2 Domain | NIST SP 800-53 Family | ISO/IEC 27001:2022 Annex A | SOC 2 Criteria |
|---|---|---|---|
| Access Control (AC) | AC | A.5.15-A.5.18, A.8.2-A.8.3 | CC6.1-CC6.3 |
| Awareness and Training (AT) | AT | A.6.3 | CC1.4 |
| Audit and Accountability (AU) | AU | A.8.15-A.8.16 | CC7.1-CC7.2 |
| Configuration Management (CM) | CM | A.8.9, A.8.32 | CC8.1 |
| Identification and Authentication (IA) | IA | A.5.16-A.5.17, A.8.5 | CC6.1 |
| Incident Response (IR) | IR | A.5.24-A.5.28 | CC7.3-CC7.5 |
| Maintenance (MA) | MA | A.7.13, A.8.1 | CC7.1 |
| Media Protection (MP) | MP | A.7.10 | C1.2 |
| Personnel Security (PS) | PS | A.6.1-A.6.2, A.6.5 | CC1.4 |
| Physical Protection (PE) | PE | A.7.1-A.7.4 | CC6.4 |
| Risk Assessment (RA) | RA | Clause 6.1 | CC3.1-CC3.4 |
| Security Assessment (CA) | CA | Clause 9.2, Clause 6.1.3 | CC4.1 |
| System and Communications Protection (SC) | SC | A.8.20-A.8.24 | CC6.6-CC6.7 |
| System and Information Integrity (SI) | SI | A.8.7-A.8.8, A.8.16 | CC7.1-CC7.2 |

**Practical use:** an access review, a vulnerability scan report, or an incident response ticket
produced for one framework typically satisfies the adjacent CMMC practice's evidence request as
well — check this table before duplicating evidence collection.

---
*This is a reference framework, not a substitute for a formal scoping determination from your
contracting officer, a gap assessment against your actual system boundary, or guidance from a
C3PAO/Registered Practitioner. Confirm your actual required CMMC level and assessment path before
treating any practice above as mandatory or non-applicable.*
