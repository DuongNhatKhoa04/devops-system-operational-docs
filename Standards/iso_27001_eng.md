# ISO/IEC 27001 – Information Security Management System (ISMS)

## Document Control

| Version | Date       | Author | Description |
|--------|------------|--------|-------------|
| 1.0.0  | 2026-01-08 | Vox    | Initial creation |

---

## 1. Purpose
ISO/IEC 27001 defines the requirements for establishing, implementing, maintaining, and continually improving an **Information Security Management System (ISMS)**.

This document is written as **operational / technical documentation**, not academic material. The goal is to provide a practical ISO 27001-aligned security framework applicable to DevOps, cloud, and enterprise IT environments.

---

## 2. Scope
This ISMS scope covers:
- Source code repositories
- CI/CD pipelines
- Infrastructure (on‑premise, cloud, hybrid)
- Deployment environments (Dev, Staging, Production)
- Secrets, credentials, and sensitive configuration
- Operational access (developers, DevOps, SRE, administrators)

Out of scope:
- End‑user device management (unless explicitly required)
- Legal or regulatory compliance outside information security

---

## 3. Core Principles
ISO 27001 follows a **risk‑based approach** rather than checklist security.

Key principles:
- **Confidentiality** – Information is accessible only to authorized entities
- **Integrity** – Information is accurate and protected from unauthorized modification
- **Availability** – Information and systems are available when required
- **Continual Improvement (PDCA)** – Plan → Do → Check → Act

---

## 4. ISMS High‑Level Architecture

```
ISMS
├── Governance & Policy
│   ├── Information Security Policy
│   ├── Risk Management Policy
│   └── Access Control Policy
│
├── Risk Management
│   ├── Asset Identification
│   ├── Risk Assessment
│   ├── Risk Treatment Plan
│   └── Statement of Applicability (SoA)
│
├── Operational Controls
│   ├── Identity & Access Management
│   ├── Secure CI/CD
│   ├── Infrastructure Security
│   └── Monitoring & Logging
│
├── Incident Management
│   ├── Detection
│   ├── Response
│   └── Lessons Learned
│
└── Audit & Improvement
    ├── Internal Audit
    ├── Management Review
    └── Continuous Improvement
```

---

## 5. Risk Management Approach
ISO 27001 requires **documented, repeatable, and auditable** risk management.

### 5.1 Asset Identification
Examples:
- Git repositories
- CI/CD runners
- Container registries
- Cloud accounts
- Secrets (API keys, certificates)

### 5.2 Risk Assessment
Each asset is evaluated based on:
- Threats
- Vulnerabilities
- Impact
- Likelihood

Risk calculation:

```
Risk = Impact × Likelihood
```

### 5.3 Risk Treatment Options
- **Mitigate** – Apply security controls
- **Avoid** – Remove the risky activity
- **Transfer** – Insurance or third‑party responsibility
- **Accept** – With documented approval

---

## 6. Statement of Applicability (SoA)
The **Statement of Applicability** maps ISO 27001 Annex A controls to implementation decisions.

Example:

| Control | Status | Justification |
|-------|--------|---------------|
| A.5.15 Access Control | Applied | Required for CI/CD and cloud access |
| A.8.12 Data Leakage | Applied | Secrets management enforced |
| A.6.3 Awareness | Planned | Security training roadmap defined |

---

## 7. DevOps‑Focused Control Mapping

| ISO 27001 Domain | DevOps Implementation |
|-----------------|-----------------------|
| Access Control | RBAC, MFA, least privilege |
| Change Management | Pull Requests, Code Review |
| Logging & Monitoring | Centralized logs, SIEM |
| Secure Development | SAST, DAST, dependency scanning |
| Incident Response | Runbooks, post‑mortems |

---

## 8. Continuous Improvement
Security controls are reviewed:
- After security incidents
- After major system changes
- On a scheduled review cycle

Example metrics:
- Number of security incidents
- Mean Time To Detect (MTTD)
- Mean Time To Respond (MTTR)
- Audit findings trend

---

## 9. Expected Outcomes
- Reduced information security risk
- Predictable and auditable security operations
- Alignment between DevOps velocity and enterprise security
- Readiness for formal ISO/IEC 27001 certification (if required)

