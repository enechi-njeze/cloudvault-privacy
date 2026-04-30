# Privacy Breach Notification Procedures

**System:** CloudVault Federal Health Exchange (FHX)
**Repository:** cloudvault-privacy
**Folder:** breach-notification
**Framework Reference:** GDPR Articles 33-34 / HIPAA Breach Notification Rule / CCPA 1798.82
**Document ID:** FHX-PRIV-BRN-001
**Prepared By:** Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, Security+, CHP, CSCS, CISSP (in progress)
**Role:** ISSO / ISSM, CloudVault Federal Health Exchange
**Privacy Officer:** Sandra Voss
**Last Updated:** April 2025
**Status:** Active

---

## Purpose

A privacy breach occurs when personal data is accessed, disclosed, altered, or destroyed in an unauthorized or unlawful manner. Different applicable laws impose different notification obligations with different timelines. For CloudVault FHX, a single breach event may trigger obligations under GDPR (72-hour notification to supervisory authority), HIPAA (60-day notification to HHS and affected individuals), CCPA (expedient notification to California residents), and federal agency reporting requirements.

This folder documents the FHX unified privacy breach notification procedure that addresses all applicable legal obligations in a coordinated fashion, avoids conflicting responses, and ensures that every required notification reaches the right recipient within the required timeframe.

---

## Documents in This Folder

| Document | Description | Reference | Status |
|---|---|---|---|
| breach-notification-procedure.md | Unified breach notification procedure covering GDPR, HIPAA, and CCPA | GDPR Art. 33-34, HIPAA 45 CFR 164.400 | Active |
| gdpr-notification-template.md | Supervisory authority notification template (GDPR Art. 33) | GDPR Art. 33 | Active |
| individual-notification-template.md | Individual notification letter template (GDPR Art. 34, HIPAA, CCPA) | GDPR Art. 34, HIPAA | Active |
| breach-incident-log.md | Cross-framework breach incident log | GDPR Art. 33(5), HIPAA 45 CFR 164.414 | Active |

---

## Multi-Framework Breach Notification Timeline

| Legal Requirement | Recipient | Deadline | Condition | FHX Internal Target |
|---|---|---|---|---|
| GDPR Art. 33 | Supervisory authority (lead DPA: likely HHS Privacy Division for US federal government) | 72 hours after awareness | Unless breach unlikely to result in risk to individuals | 48 hours |
| GDPR Art. 34 | Affected individuals | Without undue delay | High risk to individuals' rights and freedoms | 10 days (for high-risk breaches) |
| HIPAA 45 CFR 164.404 | Affected individuals | Within 60 days of discovery | Breach of unsecured PHI | 45 days |
| HIPAA 45 CFR 164.408 | HHS Secretary | Within 60 days (500+ individuals) or annually (under 500) | Breach of unsecured PHI | Simultaneous with individual notification |
| CCPA 1798.82 | California residents affected | Expedient and without unreasonable delay | Unauthorized access to California residents' personal information | 30 days |
| FedRAMP IR reporting | ISSO + AO + FedRAMP PMO | Within 1 hour of detection (major incidents); 24 hours (non-major) | Any security incident | Per FedRAMP reporting requirements |

---

## Unified Breach Response Process

When a breach involving personal data is detected, FHX follows a unified 5-phase response that addresses all applicable legal obligations simultaneously:

**Phase 1: Detection and Initial Assessment (0-4 hours)**
The ISSO is notified immediately. The ISSO makes an initial determination of whether personal data was likely involved. If yes, the Privacy Officer (Sandra Voss) is simultaneously notified. Both begin the parallel assessment process.

**Phase 2: Security Containment (0-24 hours)**
Security team (led by ISSO) implements containment: isolating affected systems, revoking compromised credentials, preserving logs. This phase is identical to the HIPAA breach response documented in [cloudvault-hipaa/breach-response](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/breach-response/README.md).

**Phase 3: Privacy and Legal Assessment (24-48 hours)**
The Privacy Officer and ISSO jointly assess the breach under all applicable frameworks:
- GDPR: Is there a risk to individuals' rights and freedoms? (triggers Art. 33 notification)
- GDPR: Is the risk high? (triggers Art. 34 individual notification)
- HIPAA: Was unsecured PHI involved? (triggers breach notification rule)
- CCPA: Were California residents' personal information involved? (triggers CCPA notification)
- FedRAMP: Is this a major or non-major incident? (triggers FedRAMP IR reporting)

**Phase 4: Notification (48-72 hours for GDPR; up to 45 days for HIPAA individuals)**
Notifications are sent in order of legal deadline: GDPR supervisory authority first (72 hours), then FedRAMP PMO, then affected individuals (HIPAA 45 days / GDPR Art. 34 high-risk without undue delay).

**Phase 5: Documentation and Post-Breach Review (within 30 days of notification completion)**
All breach documentation is finalized and retained for the legally required periods: GDPR requires indefinite retention of breach records; HIPAA requires 6 years; CCPA requires 5 years. Post-breach after-action report prepared and presented to AO.

---

## Breach Records (Summary)

| Incident | Date | Personal Data Involved | GDPR Notification | HIPAA Notification | CCPA | Status |
|---|---|---|---|---|---|---|
| FHX-BR-2023-001 | March 2023 | PHI: MRN, name, DOB (14 individuals) | Not required (risk below threshold) | Yes: notified 14 individuals and HHS | N/A (no California residents) | Closed |
| FHX-BR-2024-001 | July 2024 | None confirmed (phishing attempt, no PHI accessed) | Not required (no breach) | Not required (no breach) | N/A | Closed |
| FHX-BR-2024-002 | November 2024 | None (test data only) | Not required | Not required | N/A | Closed |

---

## Related Documents

- [ROPA](../ropa/README.md)
- [DPIA](../dpia/README.md)
- [HIPAA Breach Response](https://github.com/enechi-njeze/cloudvault-hipaa/blob/main/breach-response/README.md)
- [CCPA Compliance](../ccpa/README.md)
- [FedRAMP Incident Response](https://github.com/enechi-njeze/cloudvault-fedramp-ato/blob/main/README.md)

---

*Prepared by Enechi P.C. Njeze, CGRC, CISA, CISM, PMP, PMI-RMP, CompTIA Security+ SY0-701, CHP, CSCS, CISSP (in progress)*
*ISSO / ISSM, CloudVault Federal Health Exchange (FHX)*
*[LinkedIn](https://www.linkedin.com/in/enechi-njeze) | [Portfolio](https://github.com/enechi-njeze)*
