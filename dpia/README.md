# Data Protection Impact Assessment (DPIA)

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** dpia
**Framework Reference:** GDPR Article 35 / OMB Circular A-130 Privacy Impact Assessment
**Document ID:** FHX-PRIV-DPIA-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

GDPR Article 35 requires a Data Protection Impact Assessment (DPIA) when processing is likely to result in a high risk to the rights and freedoms of individuals, particularly when processing special categories of data (health data) on a large scale. CloudVault FHX clearly meets this threshold: it processes health data for 890,000+ individuals using automated means and large-scale data sharing across 47 federal agencies.

A DPIA is not merely a compliance checkbox — it is a structured risk assessment process that identifies privacy risks, assesses their severity and likelihood, implements mitigation measures, and documents residual risk. For federal systems, the DPIA aligns with the OMB Circular A-130 Privacy Impact Assessment (PIA) requirement.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| dpia-fhx-main.md | Main DPIA for CloudVault FHX core PHI processing operations | GDPR Art. 35 | Active |
| dpia-analytics.md | DPIA for the FHX health analytics and aggregate reporting program | GDPR Art. 35 | Active |
| dpia-payment.md | DPIA for FHX payment processing activities | GDPR Art. 35, PCI-DSS | Active |
| pia-omb-a130.md | OMB Circular A-130 Privacy Impact Assessment | OMB A-130 | Active |
| dpia-screening-checklist.md | DPIA necessity screening checklist for new processing activities | GDPR Art. 35(1) | Active |

---

## DPIA Summary: CloudVault FHX Core PHI Processing

### Step 1: Necessity and Proportionality Assessment

**Processing Description:** CloudVault FHX collects, stores, processes, and exchanges health records for 890,000+ federal health program beneficiaries. Data includes all 18 HIPAA PHI identifier types. Processing occurs continuously as patients interact with the federal health system.

**Necessity:** Processing is necessary to fulfill the federal mandate to coordinate health care for federal program beneficiaries. No less privacy-intrusive means exist to achieve this purpose while maintaining data accessibility across 47 agencies.

**Proportionality:** The volume and sensitivity of data processed are proportionate to the public health coordination purpose. Data minimization is applied: only data necessary for the specific healthcare purpose is requested and retained. Aggregated and de-identified data are used for analytics wherever possible.

**Legal Basis:** GDPR Art. 6(1)(e) — public task of official authority. GDPR Art. 9(2)(h) — health data processed for medical diagnosis, treatment, and management of health and social care systems.

### Step 2: Risk Identification

| Risk ID | Risk Description | Data Categories Affected | Likelihood | Severity | Initial Risk |
|---|---|---|---|---|---|
| FHX-PR-001 | Unauthorized access to PHI by external threat actors (hacking, phishing) | All PHI categories | Medium (strong controls but persistent threat) | Very High (890,000+ individuals) | High |
| FHX-PR-002 | Unauthorized disclosure by insider (malicious or negligent) | All PHI categories | Low (strong access controls, monitoring) | Very High | High |
| FHX-PR-003 | Data breach during transit between FHX and agency partners | PHI transmitted via FHIR API | Low (TLS 1.3, mTLS) | High | Medium |
| FHX-PR-004 | Inadequate access controls allow unauthorized agency personnel to access PHI | PHI for specific agencies | Low (quarterly access reviews) | High | Medium |
| FHX-PR-005 | Data retention exceeding necessity (failure to delete expired records) | All stored PHI | Low (automated retention controls) | Medium | Low |
| FHX-PR-006 | Analytics re-identification risk (de-identified data re-identified) | Aggregated analytics data | Very Low (HIPAA Safe Harbor applied) | High (if re-identified) | Low |
| FHX-PR-007 | Vendor/processor data breach (AWS, HealthPay, Apogee) | All PHI types | Very Low (FedRAMP High, PCI-DSS processors) | Very High | Medium |

### Step 3: Risk Mitigation Measures

| Risk ID | Mitigation Measures | Residual Risk |
|---|---|---|
| FHX-PR-001 | AES-256 encryption, MFA, WAF, GuardDuty, 24/7 SOC monitoring, annual penetration testing | Low |
| FHX-PR-002 | Least-privilege RBAC, quarterly access reviews, SOD enforcement, CloudTrail audit logging, UBA | Low |
| FHX-PR-003 | TLS 1.3 minimum, mutual TLS authentication, API scoping, full transmission logging | Very Low |
| FHX-PR-004 | Agency-specific FHIR scopes, need-to-know enforcement, quarterly access review by agency | Low |
| FHX-PR-005 | S3 Lifecycle policies, automated retention enforcement, annual data minimization review | Very Low |
| FHX-PR-006 | HIPAA Safe Harbor de-identification applied; expert determination before any analytics release | Very Low |
| FHX-PR-007 | AWS FedRAMP High authorization, PCI-DSS Level 1 for HealthPay, vendor risk assessments, DPAs | Low |

### Step 4: Consultation and Approval

The FHX DPIA was reviewed by: Privacy Officer Sandra Voss (lead reviewer), ISSO Enechi P.C. Njeze, CISO Angela Torres, and Legal Counsel Marcus Webb. The DPIA was approved by System Owner Dr. Patricia Owens and AO Deputy Director Henry Kline on March 15, 2025.

**No supervisory authority consultation was required:** The residual risk assessment concluded that all risks have been reduced to a level deemed acceptable, and the FHX DPIA does not identify a high residual risk requiring pre-processing supervisory authority consultation under GDPR Art. 36.

### Step 5: DPIA Review Schedule

The FHX DPIA is reviewed annually and upon any material change to processing activities, system architecture, or identified risk factors. Next scheduled review: March 2026.

---

## OMB Circular A-130 PIA Summary

The FHX Privacy Impact Assessment under OMB Circular A-130 was last updated in January 2025 and covers the same processing activities documented in the DPIA. The PIA is published on the FHX system website and in the federal privacy program registry. The PIA confirms that: (1) information is handled in accordance with applicable legal authorities, (2) privacy risks are identified and mitigated, (3) the system collects only information necessary for the stated purpose, and (4) appropriate notice is provided to individuals.

---

## Related Documents

- [ROPA](../ropa/README.md)
- [Data Subject Rights](../data-subject-rights/README.md)
- [Breach Notification](../breach-notification/README.md)
- [HIPAA PHI Safeguards](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/safeguards/README.md)
- [FedRAMP PT Controls](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)
- [NIST RMF Risk Assessment](https://github.com/enechi-njeze/cloudvault-nist-rmf/blob/main/step4-assess/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
