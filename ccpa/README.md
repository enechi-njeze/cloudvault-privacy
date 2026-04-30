# CCPA Compliance Program

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** ccpa
**Framework Reference:** California Consumer Privacy Act (Cal. Civ. Code 1798.100-1798.199) / CPRA 2020
**Document ID:** FHX-PRIV-CCPA-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

The California Consumer Privacy Act (CCPA) as amended by the California Privacy Rights Act (CPRA) grants California residents specific rights regarding their personal information. CloudVault FHX processes personal information of an estimated 142,000 California residents who are federal health program beneficiaries, triggering CCPA compliance obligations.

Importantly, CCPA contains exemptions for HIPAA-covered information and for information covered by the Gramm-Leach-Bliley Act. FHX health data (PHI) processed in compliance with HIPAA is generally exempt from CCPA's main requirements. However, non-PHI personal information about California residents — such as employment data, portal usage data, and some contact information — remains subject to CCPA. This folder documents FHX's CCPA compliance program for in-scope personal information.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| ccpa-privacy-notice.md | FHX CCPA privacy notice at collection | CCPA 1798.100(b), 1798.130(a)(5) | Active |
| ccpa-consumer-rights-procedure.md | CCPA consumer rights request procedure: access, deletion, opt-out, correction | CCPA 1798.100-1798.135 | Active |
| ccpa-data-inventory.md | CCPA-specific personal information inventory: what is collected, why, and with whom shared | CCPA 1798.110 | Active |
| ccpa-service-provider-register.md | Register of CCPA service providers with in-scope personal information | CCPA 1798.140(v) | Active |
| ccpa-annual-metrics.md | Annual CCPA consumer request metrics report | CPRA 1798.135(a)(7) | Active |

---

## CCPA Scope Analysis

| Personal Information Category | Volume Estimate | CCPA Coverage | HIPAA Exemption Applies? |
|---|---|---|---|
| PHI (all 18 identifiers) for California residents | ~142,000 individuals | HIPAA exemption applies (1798.145(c)) | Yes: exempt from CCPA DSR rights but notification on breach required |
| Contact information (non-PHI: portal email, communication preferences) | ~142,000 individuals | In scope | No |
| Internet activity data (patient portal clickstream, log-in times) | ~142,000 individuals | In scope | No |
| Employment data for California-based FHX contractors | ~8 individuals | In scope (B2B exemption sunset January 2023 under CPRA) | No |
| Payment data (cardholder information) | Individuals who submit copayments | PCI/HIPAA dual exemption | Yes: HIPAA; PCI data exempt separately |

---

## CCPA Consumer Rights (In-Scope Personal Information)

For non-PHI personal information about California residents, FHX provides the following CCPA rights:

| Right | Provision | FHX Implementation | Response Time |
|---|---|---|---|
| Right to Know (access) | 1798.110 | Consumer may request the categories and specific pieces of personal information FHX has collected about them | 45 days (extendable 45 days with notice) |
| Right to Delete | 1798.105 | Consumer may request deletion of personal information FHX holds, subject to exemptions | 45 days |
| Right to Correct | 1798.106 (CPRA) | Consumer may request correction of inaccurate personal information | 45 days |
| Right to Opt-Out of Sale/Sharing | 1798.120 | FHX does not sell or share personal information for cross-context behavioral advertising; formal opt-out mechanism maintained | Immediate upon request |
| Right to Limit Use of Sensitive PI | 1798.121 (CPRA) | FHX does not use sensitive personal information beyond the purposes permitted by CPRA; no additional limitation needed | N/A |
| Right to Non-Discrimination | 1798.125 | FHX does not discriminate against consumers who exercise CCPA rights | N/A |

**FHX does not sell or share personal information.** The "Do Not Sell or Share My Personal Information" link is maintained on the FHX website per 1798.135(a)(1), and all consumer requests are fulfilled through the FHX privacy request portal (privacy.fhx.gov).

---

## FY2025 CCPA Annual Metrics (Q1)

CPRA Section 1798.135(a)(7) requires businesses to disclose, in their privacy policy, metrics regarding consumer privacy requests received in the prior calendar year. FHX tracks these metrics quarterly and reports annually.

| Metric | Q1 2025 Count |
|---|---|
| Access requests received | 7 |
| Access requests fulfilled | 7 |
| Access requests denied (whole or partial) | 0 |
| Average response time (access requests) | 22 days |
| Deletion requests received | 3 |
| Deletion requests fulfilled | 1 |
| Deletion requests denied (HIPAA retention applies to PHI portion) | 2 |
| Average response time (deletion requests) | 30 days |
| Opt-out requests received | 0 |
| Correction requests received (CPRA) | 2 |
| Correction requests fulfilled | 2 |
| Average response time (correction requests) | 18 days |

---

## CCPA Service Provider Register

The following vendors process California residents' personal information as CCPA service providers. CCPA service providers may only process personal information for the specific business purpose for which they are engaged.

| Vendor | Personal Information Processed | Service | CCPA Addendum Executed |
|---|---|---|---|
| Amazon Web Services (AWS GovCloud) | All FHX personal information (infrastructure) | Cloud hosting | Yes |
| Cornerstone OnDemand | Workforce training records (CA contractors) | LMS | Yes |
| Apogee Analytics Group | Aggregated analytics (de-identified; CCPA not applicable) | Analytics | N/A |

---

## Related Documents

- [Data Subject Rights](../data-subject-rights/README.md)
- [Breach Notification](../breach-notification/README.md)
- [ROPA](../ropa/README.md)
- [HIPAA Privacy Program](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
