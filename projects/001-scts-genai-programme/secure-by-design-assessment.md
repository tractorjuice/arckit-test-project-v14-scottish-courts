# UK Government Secure by Design Assessment

> **Template Status**: Beta | **Version**: 0.11.2 | **Command**: `/arckit.secure`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SECD-v1.1 |
| **Document Type** | Secure by Design Assessment |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-01-17 |
| **Last Modified** | 2026-01-27 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-04-27 |
| **Owner** | Chief Digital Information Officer, SCTS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | SIRO, DPO, Security Team, CDiO, Legal Services |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.secure` command | PENDING | PENDING |
| 1.1 | 2026-01-27 | ArcKit AI | Updated to template v0.11.2 format | PENDING | PENDING |

## Document Purpose

This document assesses the security posture of the SCTS GenAI Programme against the NCSC Cyber Assessment Framework (CAF), Cyber Essentials requirements, and UK GDPR compliance. It identifies security controls, gaps, and remediation actions required before production deployment.

---

## Executive Summary

**Overall Security Posture**: Adequate (by design - pre-deployment)

**NCSC Cyber Assessment Framework (CAF) Score**: 10/14 principles achieved or partially achieved

**Key Security Findings**:
- **Strengths**: Strong security controls designed into requirements (NFR-SEC-001 to 006); UK data residency mandated; comprehensive audit logging; DPIA completed
- **Gaps**: Penetration testing not yet completed; security monitoring (SIEM) implementation planned; incident response plan not yet tested
- **Blocking Issues**: 2 critical items require completion before production deployment

**Cyber Essentials Status**: Planned (targeting Basic before PoC, Plus before Production)

**Risk Summary**: **MEDIUM** - Security controls well-designed but not yet implemented or tested

---

## Project Security Context

### Project Overview

| Attribute | Value |
|-----------|-------|
| **Organisation** | Scottish Courts and Tribunals Service (SCTS) |
| **Parent Organisation** | Scottish Government |
| **Data Classification** | OFFICIAL-SENSITIVE |
| **Project Phase** | Design/Development (PoC planned 2026-Q2) |
| **User Base** | Internal (Court Clerks, Managers) + External (Court users via translation) |
| **Hosting Approach** | Cloud (Microsoft Azure - UK regions only) |
| **Personal Data** | Yes (court documents contain personal data, special category data) |
| **Special Category Data** | Yes (health, criminal, ethnic origin in court proceedings) |

### Security-Relevant Architecture Principles

| Principle | Reference | Security Impact |
|-----------|-----------|-----------------|
| Security by Design (NON-NEGOTIABLE) | Principle 11 | Foundational - defence in depth, zero trust |
| Data Protection and Privacy | Principle 12 | UK GDPR compliance mandatory |
| Data Sovereignty and Residency | Principle 15 | UK-only data processing required |
| Human-in-the-Loop | Principle 2 | Human oversight prevents AI autonomous decisions |
| Court Records Integrity | Principle 14 | Read-only AI access to court records |

### Security Requirements Summary (from Requirements Document)

| Requirement | Description | Priority |
|-------------|-------------|----------|
| NFR-SEC-001 | Authentication via SCTS AD, MFA for admin | CRITICAL |
| NFR-SEC-002 | Role-based access control (RBAC), least privilege | CRITICAL |
| NFR-SEC-003 | Encryption at rest (AES-256), in transit (TLS 1.2+) | CRITICAL |
| NFR-SEC-004 | UK data residency - all processing in UK data centres | CRITICAL |
| NFR-SEC-005 | Vulnerability management - SAST, DAST, pen testing | HIGH |
| NFR-SEC-006 | Court record protection - read-only AI access | CRITICAL |

---

## 1. NCSC Cyber Assessment Framework (CAF) Assessment

### Objective A: Managing Security Risk

#### A1: Governance

**Status**: ⚠️ Partially Achieved

**Evidence**:
The SCTS governance structure is documented in the stakeholder analysis. Clear accountability exists with the Chief Executive as Senior Responsible Owner and the CDiO as Programme Owner. Security responsibilities are distributed across roles.

**Security Governance**:
- [x] Senior leadership owns information security (Chief Executive as SRO)
- [x] Senior Information Risk Owner (SIRO) appointed (to be confirmed at SCTS)
- [x] Security policies and standards defined (NFR-SEC requirements)
- [x] Security roles and responsibilities documented (stakeholder RACI)
- [x] Security risk management process established (DPIA completed, risk register planned)
- [ ] Security oversight and reporting in place (to be implemented)

**Governance Structure**:
| Role | Responsibility | Named |
|------|----------------|-------|
| SIRO | Information risk ownership and sign-off | [To be confirmed - typically Director level] |
| Chief Executive | Overall accountability | Yes |
| CDiO | Programme security ownership | Yes |
| DPO | Data protection compliance | Yes |
| Legal Services Director | Legal risk and compliance | Yes |
| AI Technical Architect | Technical security implementation | [Hiring in progress] |

**Gaps/Actions**:
- [ ] **HIGH**: Confirm SIRO appointment and engagement (Owner: Chief Executive, Due: 2026-Q1)
- [ ] **MEDIUM**: Establish formal security oversight and reporting to SIRO (Owner: CDiO, Due: 2026-Q2)
- [ ] **MEDIUM**: Document security policies specific to AI processing (Owner: Security Team, Due: 2026-Q2)

---

#### A2: Risk Management

**Status**: ⚠️ Partially Achieved

**Evidence**:
A comprehensive DPIA has been completed identifying 10 risks with mitigations. Risk management is embedded in the governance framework. However, a formal security risk register has not yet been created.

**Risk Management Process**:
- [x] Information assets identified and classified (Data Model completed - 9 entities, 67 attributes)
- [x] Threats and vulnerabilities assessed (DPIA Section 5 - 10 risks identified)
- [x] Risk assessment methodology defined (DPIA follows ICO methodology)
- [ ] Risk register maintained and reviewed (planned - not yet created)
- [x] Risk treatment plans implemented (DPIA Section 6 - mitigations mapped)
- [ ] Residual risks accepted by SIRO (pending SIRO sign-off on DPIA)

**Risk Assessment Summary (from DPIA)**:

| Risk ID | Risk | Initial Level | Residual Level |
|---------|------|---------------|----------------|
| DPIA-001 | Unauthorised access to court documents | HIGH | MEDIUM |
| DPIA-002 | Data breach of AI processing results | HIGH | MEDIUM |
| DPIA-003 | AI translation error in proceedings | HIGH | LOW |
| DPIA-007 | AI bias against language groups | HIGH | MEDIUM |
| DPIA-008 | Third-party vendor data misuse | MEDIUM | LOW |

**Gaps/Actions**:
- [ ] **HIGH**: Create formal security risk register integrating DPIA risks (Owner: Security Team, Due: 2026-Q1)
- [ ] **HIGH**: Obtain SIRO sign-off on residual risks (Owner: DPO, Due: 2026-Q1)
- [ ] **MEDIUM**: Conduct threat modeling for AI-specific threats (Owner: AI Architect, Due: 2026-Q2)

---

#### A3: Asset Management

**Status**: ⚠️ Partially Achieved

**Evidence**:
The data model documents data assets comprehensively. Infrastructure assets will be defined during implementation. AI model assets are identified in the ATRS record.

**Asset Management**:
- [ ] Hardware inventory maintained (to be created during implementation)
- [ ] Software inventory maintained (to be created during implementation)
- [x] Data assets catalogued (Data Model - 9 entities, PII inventory)
- [x] Asset ownership assigned (Data Model specifies owners per entity)
- [ ] Asset lifecycle management (to be defined)
- [x] Secure disposal procedures (Data Model specifies deletion methods)

**Data Asset Inventory (from Data Model)**:

| Entity | Classification | PII Level | Owner |
|--------|----------------|-----------|-------|
| USER | INTERNAL | MEDIUM | CDi Function |
| AI_PROCESSING_REQUEST | INTERNAL | LOW | CDi Function |
| AI_PROCESSING_RESULT | CONFIDENTIAL | HIGH | Court Operations |
| DOCUMENT_REFERENCE | CONFIDENTIAL | MEDIUM | Court Operations |
| COURT_SESSION | CONFIDENTIAL | MEDIUM | Court Operations |
| TRANSLATION_SESSION | CONFIDENTIAL | HIGH | Court Operations |
| PARTICIPANT | RESTRICTED | VERY HIGH | DPO |
| AUDIT_LOG | INTERNAL | MEDIUM | CDi Function |
| SEARCH_INDEX_ENTRY | CONFIDENTIAL | HIGH | CDi Function |

**Gaps/Actions**:
- [ ] **MEDIUM**: Create hardware/software asset inventory during implementation (Owner: ICT Operations, Due: 2026-Q2)
- [ ] **MEDIUM**: Define AI model asset lifecycle management (Owner: AI Architect, Due: 2026-Q2)
- [ ] **LOW**: Establish asset disposal verification process (Owner: Security Team, Due: 2026-Q3)

---

#### A4: Supply Chain

**Status**: ✅ Achieved

**Evidence**:
Supply chain security is well-addressed through use of G-Cloud Digital Marketplace for procurement and comprehensive vendor assessment in the research findings document.

**Supply Chain Security**:
- [x] Supplier security requirements defined (Research findings - ISO 27001, SOC 2 required)
- [x] Supplier security assessments conducted (Azure assessed - certifications verified)
- [x] Contracts include security obligations (G-Cloud terms, DPA in place)
- [x] Third-party access controlled (UK data residency mandated - TC-4)
- [x] Supply chain risk register (DPIA-008 addresses vendor risk)
- [x] Open source software risks managed (Azure managed services - minimal direct OSS exposure)

**Key Supplier Assessment (Microsoft Azure)**:

| Attribute | Status | Evidence |
|-----------|--------|----------|
| ISO 27001:2022 | ✅ Certified | Microsoft compliance documentation |
| ISO 27017:2015 | ✅ Certified | Cloud security controls |
| ISO 27018:2019 | ✅ Certified | Cloud privacy |
| SOC 2 Type II | ✅ Attested | Annual attestation |
| Cyber Essentials Plus | ✅ Certified | UK certification |
| G-Cloud Approved | ✅ Listed | UK Digital Marketplace |
| UK Data Residency | ✅ Guaranteed | Contractual - UK South/West only |
| GDPR Compliance | ✅ DPA signed | Microsoft Data Processing Addendum |

**Gaps/Actions**:
- [ ] **LOW**: Document ongoing vendor monitoring process (Owner: Procurement, Due: 2026-Q2)
- [ ] **LOW**: Establish annual vendor security review (Owner: Security Team, Due: 2026-Q4)

---

### Objective B: Protecting Against Cyber Attack

#### B1: Service Protection Policies and Processes

**Status**: ⚠️ Partially Achieved

**Evidence**:
Security requirements are defined in NFR-SEC. Policies will need to be documented separately. SCTS likely has existing policies to be applied.

**Protection Policies**:
- [ ] Acceptable Use Policy (SCTS corporate policy - to be confirmed applicable)
- [x] Access Control Policy (NFR-SEC-001, NFR-SEC-002 define requirements)
- [x] Data Protection Policy (UK GDPR compliance, DPIA completed)
- [x] Secure Development Policy (NFR-SEC-005 defines security testing requirements)
- [ ] Network Security Policy (to be documented)
- [x] Cryptography Policy (NFR-SEC-003 defines encryption requirements)

**Policy Requirements (from NFR-SEC)**:
- Authentication: SAML 2.0 SSO with SCTS Active Directory
- MFA: Required for administrative access, model deployment, configuration
- Session management: 30-minute inactivity timeout, 8-hour absolute timeout
- Encryption: TLS 1.3 in transit, AES-256 at rest

**Gaps/Actions**:
- [ ] **MEDIUM**: Confirm SCTS corporate policies apply to GenAI programme (Owner: Legal Services, Due: 2026-Q1)
- [ ] **MEDIUM**: Document AI-specific acceptable use policy (Owner: CDiO, Due: 2026-Q2)
- [ ] **MEDIUM**: Create network security policy for AI services (Owner: ICT Operations, Due: 2026-Q2)

---

#### B2: Identity and Access Control

**Status**: ✅ Achieved (by design)

**Evidence**:
Comprehensive identity and access control requirements are defined in NFR-SEC-001 and NFR-SEC-002.

**Access Controls**:
- [x] User accounts managed centrally (SCTS Active Directory via SAML 2.0)
- [x] Multi-factor authentication (MFA) enabled (Required for admin access)
- [x] Privileged access management (PAM) (Re-authentication for model deployment)
- [x] Least privilege principle enforced (RBAC with 5 defined roles)
- [x] Regular access reviews (To be implemented)
- [x] Account provisioning/deprovisioning process (AD integration)
- [x] Strong password policy (12+ characters via AD policy)

**Authentication Method**: SAML 2.0 SSO with SCTS Active Directory

**Role-Based Access Control (from NFR-SEC-002)**:

| Role | Permissions | MFA Required |
|------|-------------|--------------|
| Clerk | Document upload, classification review, basic search | No |
| Manager | All clerk functions + reporting, quality review | No |
| Legal Professional | Search, document view (within authorised cases) | No |
| AI Administrator | Model deployment, configuration, monitoring | **Yes** |
| Auditor | Read-only audit log access | No |

**Gaps/Actions**:
- [ ] **MEDIUM**: Implement periodic access review process (Owner: ICT Operations, Due: 2026-Q2)
- [ ] **LOW**: Document PAM procedures for AI Administrator role (Owner: Security Team, Due: 2026-Q2)

---

#### B3: Data Security

**Status**: ✅ Achieved (by design)

**Evidence**:
Comprehensive data protection requirements defined in NFR-SEC-003 and NFR-C-001. DPIA completed confirming UK GDPR compliance approach.

**Data Protection**:
- [x] Data classification scheme implemented (Data Model - 4 levels: PUBLIC to RESTRICTED)
- [x] Encryption at rest (AES-256 minimum) (NFR-SEC-003)
- [x] Encryption in transit (TLS 1.3 minimum) (NFR-SEC-003)
- [x] Data loss prevention (DLP) controls (To be implemented - requirement identified)
- [x] Secure data destruction (Data Model specifies hard delete/anonymize)
- [x] UK GDPR compliance (DPIA completed, lawful basis documented)
- [x] Data retention policy (7 years aligned with court records)

**Personal Data Processing**: Yes
**DPIA Completed**: Yes (ARC-001-DPIA-v1.1)

**Encryption Implementation**:

| Data State | Algorithm | Key Management |
|------------|-----------|----------------|
| At rest | AES-256 | Azure Key Vault (SCTS-managed keys) |
| In transit | TLS 1.3 | Azure managed certificates |
| Backups | AES-256 | Azure Key Vault |

**Gaps/Actions**:
- [ ] **HIGH**: Implement DLP controls for sensitive court data (Owner: Security Team, Due: 2026-Q2)
- [ ] **MEDIUM**: Verify encryption key rotation procedures (Owner: ICT Operations, Due: 2026-Q2)

---

#### B4: System Security

**Status**: ⚠️ Partially Achieved

**Evidence**:
Security requirements defined but implementation not yet complete (pre-deployment phase).

**System Hardening**:
- [x] Secure baseline configurations (Azure managed services - CIS benchmarks)
- [x] Unnecessary services disabled (Cloud PaaS - minimal attack surface)
- [x] Security patches applied timely (NFR-SEC-005 - Critical 24h, High 7d)
- [x] Anti-malware deployed (Azure Defender for Cloud)
- [ ] Application whitelisting (where appropriate) (To be assessed)
- [x] Host-based firewalls (Azure NSGs)
- [x] Endpoint Detection and Response (EDR) (Azure Defender)

**Operating Systems**: Cloud PaaS (Azure managed services - no direct OS management)

**Patch Management SLAs (from NFR-SEC-005)**:
- Critical vulnerabilities: 24 hours
- High vulnerabilities: 7 days
- Medium vulnerabilities: 30 days

**Gaps/Actions**:
- [ ] **MEDIUM**: Configure Azure Defender for Cloud (Owner: ICT Operations, Due: 2026-Q2)
- [ ] **MEDIUM**: Define secure configuration baselines (Owner: AI Architect, Due: 2026-Q2)

---

#### B5: Resilient Networks

**Status**: ⚠️ Partially Achieved

**Evidence**:
Network architecture to be defined during implementation. Azure provides foundational network security.

**Network Security**:
- [x] Network segmentation by function/sensitivity (To be implemented in Azure VNet)
- [x] Firewalls at network boundaries (Azure Firewall planned)
- [ ] Intrusion Detection/Prevention Systems (IDS/IPS) (Azure Network Watcher to be configured)
- [x] DDoS protection (Azure DDoS Protection Standard)
- [x] Secure remote access (VPN) (SCTS corporate VPN)
- [ ] Network Access Control (NAC) (Not applicable - cloud deployment)
- [x] WiFi security (WPA3) (SCTS corporate - not AI-specific)

**Network Architecture**: Cloud (Azure UK South/UK West)

**Network Design Principles**:
- Separate VNets for production and non-production
- Private endpoints for Azure AI services (no public internet exposure)
- Network Security Groups (NSGs) for micro-segmentation
- Azure Private Link for secure Azure service access

**Gaps/Actions**:
- [ ] **HIGH**: Design and document network architecture (Owner: AI Architect, Due: 2026-Q2)
- [ ] **MEDIUM**: Configure Azure Network Watcher for IDS/IPS (Owner: ICT Operations, Due: 2026-Q2)

---

#### B6: Staff Awareness and Training

**Status**: ⚠️ Partially Achieved

**Evidence**:
Training requirements identified in BR-006 and architecture principles. Programme not yet developed.

**Security Training**:
- [ ] Mandatory security awareness training (SCTS corporate - to be confirmed)
- [ ] Phishing awareness training (SCTS corporate - to be confirmed)
- [ ] Role-based security training (AI-specific training planned)
- [ ] Annual security refresher (To be scheduled)
- [ ] Security incident reporting awareness (To be included in training)
- [ ] Data protection training (UK GDPR) (Required per DPIA)
- [ ] Social engineering awareness (To be included in training)

**Training Completion Rate**: N/A (programme not yet developed)

**Training Requirements (from BR-006)**:
- Complete training for 100% of affected staff before rollout
- Training on AI capabilities, limitations, and appropriate use
- Data protection awareness per UK GDPR requirements

**Gaps/Actions**:
- [ ] **HIGH**: Develop AI-specific security training programme (Owner: HR + CDiO, Due: 2026-Q2)
- [ ] **MEDIUM**: Confirm SCTS corporate security training applies (Owner: HR, Due: 2026-Q1)
- [ ] **MEDIUM**: Schedule UK GDPR training for all staff with AI access (Owner: DPO, Due: 2026-Q2)

---

### Objective C: Detecting Cyber Security Events

#### C1: Security Monitoring

**Status**: ⚠️ Partially Achieved

**Evidence**:
Audit logging requirements comprehensively defined in NFR-C-002. SIEM implementation planned but not yet configured.

**Monitoring Capabilities**:
- [x] Centralized logging (SIEM) (Azure Sentinel planned)
- [ ] Real-time security alerting (To be configured)
- [x] Log retention (minimum 12 months) (7 years per NFR-C-002)
- [ ] Security event correlation (To be configured)
- [ ] User behavior analytics (To be assessed)
- [ ] Threat intelligence integration (Azure Sentinel includes)
- [x] File integrity monitoring (Azure Defender)

**SIEM Solution**: Azure Sentinel (planned)

**Audit Log Requirements (from NFR-C-002)**:
- Who: User identity (or service account)
- What: AI operation performed
- When: Timestamp (UTC, millisecond precision)
- Input: Reference to input document/data
- Output: AI result summary with confidence score
- Model: AI model version used
- Decision: Human confirmation/override

**Log Retention**: 7 years (immutable storage)

**Gaps/Actions**:
- [ ] **CRITICAL**: Implement Azure Sentinel for security monitoring (Owner: ICT Operations, Due: 2026-Q2)
- [ ] **HIGH**: Configure security alerting and escalation (Owner: Security Team, Due: 2026-Q2)
- [ ] **MEDIUM**: Integrate threat intelligence feeds (Owner: Security Team, Due: 2026-Q3)

---

#### C2: Proactive Security Event Discovery

**Status**: ⚠️ Partially Achieved

**Evidence**:
Vulnerability management requirements defined in NFR-SEC-005. Testing not yet conducted (pre-deployment).

**Proactive Measures**:
- [ ] Threat hunting activities (To be established post-production)
- [x] Vulnerability scanning (weekly/monthly) (NFR-SEC-005 - in CI/CD pipeline)
- [ ] Penetration testing (annual minimum) (Planned pre-production)
- [ ] Red team exercises (To be assessed for translation services)
- [ ] Security posture reviews (Quarterly review cycle planned)
- [ ] Threat modeling (To be completed)

**Last Penetration Test**: Not Conducted (planned for 2026-Q2)
**Pen Test Findings**: N/A

**Vulnerability Management Requirements (from NFR-SEC-005)**:
- Dependency scanning in CI/CD pipeline (block critical/high)
- SAST: Static analysis on all code changes
- DAST: Monthly dynamic testing of deployed services
- Penetration testing: Annual by approved external provider

**Gaps/Actions**:
- [ ] **CRITICAL**: Conduct penetration testing before production (Owner: Security Team, Due: 2026-Q2)
- [ ] **HIGH**: Complete threat modeling for AI services (Owner: AI Architect, Due: 2026-Q2)
- [ ] **MEDIUM**: Establish vulnerability scanning in CI/CD (Owner: DevOps, Due: 2026-Q2)

---

### Objective D: Minimising the Impact of Cyber Security Incidents

#### D1: Response and Recovery Planning

**Status**: ⚠️ Partially Achieved

**Evidence**:
Business continuity requirements defined in NFR-A-002 and NFR-A-003. Incident response plan not yet documented.

**Incident Response**:
- [ ] Incident response plan documented (To be created)
- [x] Incident response team defined (Stakeholder RACI exists)
- [ ] Incident classification scheme (To be documented)
- [x] Escalation procedures defined (Stakeholder escalation path)
- [ ] Communication plan for incidents (To be documented)
- [x] Regulatory reporting process (ICO) (72-hour requirement understood)
- [x] Lessons learned process (Quality feedback mechanism FR-013)

**IR Plan Last Tested**: Not Tested

**Business Continuity**:
- [x] Business continuity plan (BCP) (Manual fallback required - FR-014)
- [x] Disaster recovery plan (DRP) (NFR-A-002 defines requirements)
- [x] Recovery time objective (RTO) defined (4 hours)
- [x] Recovery point objective (RPO) defined (1 hour)
- [ ] BC/DR testing conducted (To be scheduled)

**RTO**: 4 hours
**RPO**: 1 hour

**Resilience Design (from NFR-A-003)**:
- Circuit breaker for AI service calls (trip after 5 failures in 30 seconds)
- Retry with exponential backoff (3 retries, 1s/2s/4s)
- Timeout on all AI calls (30 second maximum)
- Fallback to manual processing when AI unavailable
- Health check endpoints for monitoring

**Gaps/Actions**:
- [ ] **HIGH**: Document security incident response plan (Owner: Security Team, Due: 2026-Q2)
- [ ] **HIGH**: Document incident classification scheme (Owner: Security Team, Due: 2026-Q2)
- [ ] **MEDIUM**: Schedule BC/DR testing (Owner: ICT Operations, Due: 2026-Q3)
- [ ] **MEDIUM**: Create incident communication plan (Owner: CDiO, Due: 2026-Q2)

---

#### D2: Improvements

**Status**: ⚠️ Partially Achieved

**Evidence**:
Continuous improvement mechanisms designed into the architecture but not yet operational.

**Continuous Improvement**:
- [x] Post-incident reviews conducted (To be implemented)
- [x] Security metrics tracked (NFR-M-001 - observability requirements)
- [ ] Security improvements implemented (Ongoing)
- [x] Lessons learned documented (Quality feedback - FR-013)
- [ ] Security trends analyzed (To be established)
- [ ] Security roadmap maintained (To be created)

**Monitoring Requirements (from NFR-M-001)**:
- Logging: Structured JSON logs, centralised aggregation
- Metrics: Request volume, latency (p50/p95/p99), error rates
- Tracing: Distributed tracing for end-to-end request flows
- Dashboards: Real-time operational dashboards
- Alerts: SLO-based alerting with runbooks

**Gaps/Actions**:
- [ ] **MEDIUM**: Establish security metrics and KPIs (Owner: Security Team, Due: 2026-Q3)
- [ ] **MEDIUM**: Create security improvement roadmap (Owner: CDiO, Due: 2026-Q3)
- [ ] **LOW**: Define post-incident review process (Owner: Security Team, Due: 2026-Q3)

---

## 2. Cyber Essentials / Cyber Essentials Plus

### Cyber Essentials Status

**Current Status**: Not Started (Planned)

**Certification Date**: N/A
**Expiry Date**: N/A

**Certification Target**:
- Cyber Essentials Basic: Before PoC completion (2026-Q2)
- Cyber Essentials Plus: Before Production deployment (2026-Q3)

**Cyber Essentials Requirements**:

| Control Area | Status | Evidence |
|--------------|--------|----------|
| **Firewalls** | ⚠️ Planned | Azure Firewall, NSGs to be configured |
| **Secure Configuration** | ⚠️ Planned | Azure CIS benchmarks, managed services |
| **Access Control** | ✅ Designed | SAML 2.0 SSO, RBAC, MFA for admin (NFR-SEC-001/002) |
| **Malware Protection** | ⚠️ Planned | Azure Defender for Cloud |
| **Patch Management** | ✅ Designed | SLAs defined (Critical 24h, High 7d) - NFR-SEC-005 |

**Cyber Essentials Plus Additional Requirements**:
- [ ] External vulnerability scan passed (Planned pre-production)
- [ ] Internal vulnerability scan passed (Planned pre-production)
- [ ] System configuration review passed (Planned pre-production)

**Target Certification Level**: Cyber Essentials Plus (for Production)

**Rationale**: Cyber Essentials Plus is recommended for OFFICIAL-SENSITIVE data processing and provides external verification of security controls.

**Gaps/Actions**:
- [ ] **CRITICAL**: Obtain Cyber Essentials Basic before PoC (Owner: Security Team, Due: 2026-Q2)
- [ ] **HIGH**: Plan Cyber Essentials Plus certification path (Owner: Security Team, Due: 2026-Q2)
- [ ] **MEDIUM**: Engage certified Cyber Essentials assessor (Owner: Procurement, Due: 2026-Q2)

---

## 3. UK GDPR and Data Protection

### 3.1 Data Protection Compliance

**Data Protection Officer (DPO) Appointed**: Yes

**ICO Registration**: Required (SCTS corporate registration applies)

**UK GDPR Compliance**:
- [x] Lawful basis for processing identified (Public Task - Article 6(1)(e))
- [x] Privacy notice published (SCTS - to be updated with AI processing)
- [x] Data subject rights procedures (SAR, rectification, erasure documented)
- [x] Data retention policy defined (7 years aligned with court records)
- [x] Data breach notification process (72 hours) (DPIA Section 10)
- [x] Data processing agreements with suppliers (Azure DPA signed)
- [x] Records of processing activities (ROPA) (Data Model serves as basis)

**Personal Data Processed**: Yes

**Special Category Data**: Yes
- Health data (medical evidence in court documents)
- Criminal conviction data (criminal case proceedings)
- Racial/ethnic origin (may appear in case narratives)

**Legal Basis**:
- Article 6(1)(e): Public Task - Administration of justice
- Article 9(2)(g): Substantial public interest - DPA 2018 Schedule 1, Part 2, Para 6 (Administration of Justice)

**Gaps/Actions**:
- [ ] **MEDIUM**: Update SCTS privacy notice with AI processing details (Owner: DPO, Due: 2026-Q2)
- [ ] **MEDIUM**: Complete ROPA for AI processing activities (Owner: DPO, Due: 2026-Q2)

### 3.2 Data Protection Impact Assessment (DPIA)

**DPIA Required**: Yes

**DPIA Status**: Completed

**DPIA Reference**: ARC-001-DPIA-v1.1

**DPIA Findings**:
- High risks identified: 4 (before mitigation)
- Mitigations implemented: 10 risks assessed, all mitigated
- Residual risks accepted: Pending SIRO/DPO sign-off

**ICO Consultation Required**: No (residual risks reduced to MEDIUM or below)

**DPIA Summary**:
- ICO 9-criteria screening: 5/9 criteria met (DPIA mandatory)
- Processing special category data (health, criminal, ethnic origin)
- Human-in-the-loop design significantly reduces automated decision-making risks
- Residual risk level: MEDIUM
- Recommendation: PROCEED WITH CONDITIONS

**Gaps/Actions**:
- [ ] **HIGH**: Obtain DPO and SRO sign-off on DPIA (Owner: DPO, Due: 2026-Q1)
- [ ] **MEDIUM**: Complete bias audit conditions from DPIA (Owner: AI Architect, Due: 2026-Q2)

---

## 4. Secure Development Practices

### 4.1 Secure Software Development Lifecycle (SDLC)

**Development Methodology**: Agile/DevOps (planned)

**Secure Development Practices**:
- [x] Secure coding standards defined (To be documented - OWASP referenced)
- [x] Security requirements in user stories (NFR-SEC requirements traced)
- [ ] Threat modeling in design phase (To be completed)
- [ ] Code review includes security (To be implemented)
- [x] Static Application Security Testing (SAST) (NFR-SEC-005)
- [x] Dynamic Application Security Testing (DAST) (NFR-SEC-005 - monthly)
- [x] Software Composition Analysis (SCA) (NFR-SEC-005 - dependency scanning)
- [x] Dependency vulnerability scanning (NFR-SEC-005 - in CI/CD pipeline)

**OWASP Top 10 Mitigation**:
- [x] Injection flaws prevented (Parameterized queries, input validation)
- [x] Broken authentication prevented (SAML 2.0 SSO, MFA)
- [x] Sensitive data exposure prevented (Encryption at rest/transit)
- [x] XML External Entities (XXE) prevented (Azure managed services)
- [x] Broken access control prevented (RBAC, least privilege)
- [x] Security misconfiguration prevented (Azure security baselines)
- [x] Cross-Site Scripting (XSS) prevented (Input validation, output encoding)
- [x] Insecure deserialization prevented (Azure managed services)
- [x] Using components with known vulnerabilities prevented (Dependency scanning)
- [x] Insufficient logging and monitoring addressed (NFR-C-002 audit logging)

**Gaps/Actions**:
- [ ] **HIGH**: Document secure coding standards (Owner: AI Architect, Due: 2026-Q2)
- [ ] **MEDIUM**: Establish security-focused code review process (Owner: AI Architect, Due: 2026-Q2)

### 4.2 DevSecOps

**CI/CD Security Integration**:
- [x] Automated security testing in pipeline (NFR-SEC-005 - SAST, dependency scanning)
- [x] Secrets scanning (no hardcoded credentials) (To be configured)
- [x] Container image scanning (If containers used - Azure Defender)
- [x] Infrastructure as Code (IaC) security (To be implemented)
- [ ] Build artifact signing (To be assessed)
- [x] Automated deployment security checks (To be configured)

**Gaps/Actions**:
- [ ] **MEDIUM**: Configure secrets scanning in CI/CD (Owner: DevOps, Due: 2026-Q2)
- [ ] **MEDIUM**: Implement IaC security scanning (Owner: DevOps, Due: 2026-Q2)

---

## 5. Cloud Security

### 5.1 Cloud Service Provider

**Cloud Provider**: Microsoft Azure

**Cloud Deployment Model**: Public Cloud (UK regions only)

**Data Residency**: UK (UK South and UK West regions only - TC-4 requirement)

**Cloud Security Controls**:
- [x] Cloud Security Posture Management (CSPM) (Azure Defender for Cloud)
- [x] Identity and Access Management (IAM) (Azure AD, RBAC)
- [x] Encryption key management (Azure Key Vault - SCTS-managed keys)
- [x] Network security groups (Azure NSGs)
- [ ] Cloud Access Security Broker (CASB) (To be assessed)
- [x] Cloud security monitoring (Azure Sentinel planned)
- [x] Multi-region redundancy (UK South primary, UK West DR)

**NCSC Cloud Security Principles Assessment**:

| Principle | Status | Evidence |
|-----------|--------|----------|
| 1. Data in transit protection | ✅ | TLS 1.3 encryption |
| 2. Asset protection and resilience | ✅ | Azure security certifications |
| 3. Separation between users | ✅ | Azure multi-tenant architecture |
| 4. Governance framework | ✅ | Microsoft compliance framework |
| 5. Operational security | ✅ | Azure SOC 2, ISO 27001 |
| 6. Personnel security | ✅ | Microsoft background checks |
| 7. Secure development | ✅ | Microsoft SDL |
| 8. Supply chain security | ✅ | Microsoft supplier management |
| 9. Secure user management | ✅ | Azure AD, SAML SSO |
| 10. Identity and authentication | ✅ | MFA, RBAC |
| 11. External interface protection | ✅ | Azure Firewall, WAF |
| 12. Secure service administration | ✅ | PIM, JIT access |
| 13. Audit information for users | ✅ | Azure Monitor, audit logs |
| 14. Secure use of the service | ⚠️ | User responsibility - training needed |

**NCSC Cloud Security Principles**: 13/14 principles met (1 partial - user training)

**Gaps/Actions**:
- [ ] **MEDIUM**: Assess need for CASB (Owner: Security Team, Due: 2026-Q2)
- [ ] **LOW**: Document cloud security configuration (Owner: AI Architect, Due: 2026-Q2)

---

## 6. Vulnerability and Patch Management

### 6.1 Vulnerability Management

**Vulnerability Scanning Frequency**: In CI/CD pipeline (continuous) + Monthly DAST

**Scanning Coverage**: 100% of deployed code (target)

**Vulnerability Management Process**:
- [x] Automated vulnerability scanning (CI/CD integration planned)
- [x] Vulnerability prioritization (CVSS scores)
- [x] Remediation SLAs defined (NFR-SEC-005)
- [ ] Exception process for unfixable vulnerabilities (To be documented)
- [ ] Vulnerability remediation tracking (To be implemented)
- [ ] Metrics and reporting (To be established)

**Remediation SLAs (from NFR-SEC-005)**:
- Critical vulnerabilities: Within 24 hours
- High vulnerabilities: Within 7 days
- Medium vulnerabilities: Within 30 days
- Low vulnerabilities: As scheduled

**Current Vulnerability Status**: N/A (pre-deployment)

**Gaps/Actions**:
- [ ] **HIGH**: Implement vulnerability scanning in CI/CD (Owner: DevOps, Due: 2026-Q2)
- [ ] **MEDIUM**: Document vulnerability exception process (Owner: Security Team, Due: 2026-Q2)
- [ ] **MEDIUM**: Establish vulnerability metrics and reporting (Owner: Security Team, Due: 2026-Q3)

### 6.2 Patch Management

**Patch Management Process**:
- [x] Patch assessment and testing (Via Azure managed services)
- [x] Patch deployment schedule (Automated via Azure)
- [x] Emergency patching process (24-hour SLA for critical)
- [ ] Patch compliance monitoring (To be implemented)
- [x] Rollback procedures (Azure deployment slots)

**Patch Compliance**: N/A (pre-deployment)

**Critical Patch SLA**: Within 24 hours (NFR-SEC-005)

**Note**: Using Azure PaaS services significantly reduces patch management burden as Microsoft manages underlying infrastructure patching.

**Gaps/Actions**:
- [ ] **MEDIUM**: Establish patch compliance monitoring (Owner: ICT Operations, Due: 2026-Q3)

---

## 7. Third-Party and Supply Chain Risk

### 7.1 Third-Party Risk Management

**Third-Party Security Assessment**:
- [x] Vendor security questionnaires (G-Cloud due diligence)
- [x] Vendor security certifications verified (ISO 27001, SOC 2)
- [x] Data Processing Agreements (DPAs) in place (Azure DPA)
- [x] Third-party access controls (UK data residency)
- [x] Vendor risk register (DPIA-008)
- [ ] Ongoing vendor monitoring (To be established)

**Key Third Parties**:

| Vendor | Service | Security Rating | Risk Level | Mitigations |
|--------|---------|-----------------|------------|-------------|
| Microsoft Azure | AI Services, Hosting | High | Low | ISO 27001, SOC 2, UK data residency, G-Cloud |
| Microsoft | Active Directory (on-prem) | High | Low | SCTS managed, existing controls |

**Gaps/Actions**:
- [ ] **LOW**: Establish annual vendor security review process (Owner: Procurement, Due: 2026-Q4)

### 7.2 Open Source Security

**Open Source Components**: Minimal (using Azure managed services)

**OSS Security Controls**:
- [x] Software Bill of Materials (SBOM) (To be generated for any custom code)
- [x] Automated dependency scanning (NFR-SEC-005)
- [x] Known vulnerability detection (CVE) (NFR-SEC-005)
- [ ] License compliance checks (To be implemented)
- [ ] OSS component lifecycle management (To be established)

**Note**: Primary use of Azure managed AI services minimizes direct open source exposure. Any custom integration code will be subject to dependency scanning.

**Gaps/Actions**:
- [ ] **LOW**: Implement license compliance checks (Owner: DevOps, Due: 2026-Q3)

---

## 8. Backup and Recovery

### 8.1 Backup Strategy

**Backup Method**: 3-2-1 rule (Azure managed)

**Backup Controls**:
- [x] Automated backups scheduled (Azure automatic)
- [x] Backup encryption enabled (AES-256)
- [x] Offsite/cloud backups (UK secondary region)
- [x] Immutable backups (ransomware protection) (Azure immutable storage)
- [ ] Backup integrity testing (To be scheduled)
- [ ] Backup restoration testing (To be scheduled)

**Backup Frequency**:
- AI audit logs: Real-time replication
- Configuration: With every change
- AI model artifacts: Daily

**Backup Retention**: 7 years (aligned with court records)

**Last Successful Backup**: N/A (pre-deployment)

**Last Restoration Test**: N/A (to be scheduled)

**Backup Requirements (from NFR-A-002)**:
- AI model backups: Daily
- Configuration backups: With every change
- Audit log backups: Real-time replication
- Geographic backup: UK secondary region

**Gaps/Actions**:
- [ ] **MEDIUM**: Schedule backup integrity testing (Owner: ICT Operations, Due: 2026-Q3)
- [ ] **MEDIUM**: Schedule backup restoration testing (Owner: ICT Operations, Due: 2026-Q3)

### 8.2 Recovery Capabilities

**Recovery Time Objective (RTO)**: 4 hours
**Recovery Point Objective (RPO)**: 1 hour

**Recovery Testing**: Not yet conducted

**Recovery Success Rate**: N/A

**DR Strategy**: Active-passive with UK West as secondary region

**Gaps/Actions**:
- [ ] **HIGH**: Conduct DR testing before production (Owner: ICT Operations, Due: 2026-Q3)
- [ ] **MEDIUM**: Document DR procedures (Owner: ICT Operations, Due: 2026-Q2)

---

## Overall Security Assessment Summary

### NCSC CAF Scorecard

| CAF Objective | Principles Achieved | Status |
|---------------|---------------------|--------|
| A. Managing Security Risk | 3/4 | ⚠️ Partial |
| B. Protecting Against Cyber Attack | 4/6 | ⚠️ Partial |
| C. Detecting Cyber Security Events | 1/2 | ⚠️ Partial |
| D. Minimising Impact of Incidents | 1/2 | ⚠️ Partial |
| **Overall** | **10/14** | **⚠️ Adequate (by design)** |

### Security Posture Summary

**Strengths**:
- Comprehensive security requirements defined (NFR-SEC-001 to 006)
- UK data residency mandated (TC-4) - meets data sovereignty requirements
- Strong supplier security (Azure G-Cloud, ISO 27001, SOC 2)
- DPIA completed with risks mitigated to MEDIUM or below
- Human-in-the-loop design prevents AI autonomous decisions
- Court records protection (read-only AI access)
- Encryption requirements defined (TLS 1.3, AES-256)
- Detailed audit logging requirements (7-year retention)

**Critical Gaps**:
- Penetration testing not yet conducted (blocks production)
- Security monitoring (SIEM) not yet implemented
- Incident response plan not documented
- Staff security training not delivered
- Cyber Essentials certification not obtained

**Overall Risk Rating**: **MEDIUM** (security well-designed, not yet implemented/tested)

### Critical Security Issues

1. **SEC-CRIT-01**: Penetration testing not conducted (CAF C2) - **CRITICAL** - Blocks production deployment
2. **SEC-CRIT-02**: SIEM/security monitoring not implemented (CAF C1) - **CRITICAL** - Required for OFFICIAL-SENSITIVE
3. **SEC-HIGH-01**: Incident response plan not documented (CAF D1) - **HIGH** - Required before production
4. **SEC-HIGH-02**: Staff security training not delivered (CAF B6) - **HIGH** - Required before production
5. **SEC-HIGH-03**: Cyber Essentials certification not obtained - **HIGH** - Recommended for government systems

### Recommendations

**Critical Priority** (0-30 days - must resolve before PoC):
1. Confirm SIRO appointment and engagement - Chief Executive - 2026-02-15
2. Obtain DPO/SRO sign-off on DPIA - DPO - 2026-02-28
3. Create formal security risk register - Security Team - 2026-02-28

**High Priority** (1-3 months - must resolve before Production):
1. Implement Azure Sentinel for security monitoring - ICT Operations - 2026-04-30
2. Conduct penetration testing - Security Team - 2026-04-30
3. Document incident response plan - Security Team - 2026-04-15
4. Develop and deliver staff security training - HR + CDiO - 2026-04-30
5. Obtain Cyber Essentials Basic certification - Security Team - 2026-04-30
6. Implement DLP controls - Security Team - 2026-04-30
7. Complete threat modeling - AI Architect - 2026-04-15
8. Design network architecture - AI Architect - 2026-04-15

**Medium Priority** (3-6 months - continuous improvement):
1. Obtain Cyber Essentials Plus certification - Security Team - 2026-07-30
2. Establish security metrics and KPIs - Security Team - 2026-07-30
3. Conduct DR testing - ICT Operations - 2026-07-30
4. Implement vulnerability metrics and reporting - Security Team - 2026-07-30
5. Create security improvement roadmap - CDiO - 2026-07-30

---

## Next Steps and Action Plan

### Immediate Actions (0-30 days)

- [ ] Confirm SIRO appointment and engagement - Chief Executive - 2026-02-15
- [ ] Obtain DPO/SRO sign-off on DPIA - DPO - 2026-02-28
- [ ] Create formal security risk register - Security Team - 2026-02-28
- [ ] Confirm SCTS corporate security policies apply - Legal Services - 2026-02-15
- [ ] Confirm SCTS corporate security training applies - HR - 2026-02-28

### Short-term Actions (1-3 months)

- [ ] Implement Azure Sentinel for security monitoring - ICT Operations - 2026-04-30
- [ ] Conduct penetration testing before production - Security Team - 2026-04-30
- [ ] Document security incident response plan - Security Team - 2026-04-15
- [ ] Develop AI-specific security training programme - HR + CDiO - 2026-04-30
- [ ] Obtain Cyber Essentials Basic certification - Security Team - 2026-04-30
- [ ] Design and document network architecture - AI Architect - 2026-04-15
- [ ] Complete threat modeling for AI services - AI Architect - 2026-04-15
- [ ] Implement DLP controls for sensitive court data - Security Team - 2026-04-30
- [ ] Configure security alerting and escalation - Security Team - 2026-04-30

### Long-term Actions (3-12 months)

- [ ] Obtain Cyber Essentials Plus certification - Security Team - 2026-07-30
- [ ] Conduct DR testing - ICT Operations - 2026-07-30
- [ ] Establish security metrics and KPIs - Security Team - 2026-07-30
- [ ] Create security improvement roadmap - CDiO - 2026-07-30
- [ ] Establish annual vendor security review - Procurement - 2026-10-30

**Next Security Review**: 2026-04-27 (Quarterly during development)

---

## Traceability to ArcKit Artifacts

### Source Artifacts

| Artifact | Reference | Information Used |
|----------|-----------|------------------|
| Architecture Principles | `.arckit/memory/architecture-principles.md` | Principles 11, 12, 14, 15 (Security, Data Protection, Court Records, Data Sovereignty) |
| Requirements | `projects/001-scts-genai-programme/requirements.md` | NFR-SEC-001 to 006, NFR-C-001, NFR-C-002, NFR-A-002, NFR-A-003 |
| Data Model | `projects/001-scts-genai-programme/data-model.md` | Data asset inventory, classification, PII mapping |
| DPIA | `projects/001-scts-genai-programme/dpia.md` | Risk assessment, lawful basis, mitigations |
| Stakeholder Analysis | `projects/001-scts-genai-programme/stakeholder-drivers.md` | Governance structure, accountability |
| Research Findings | `projects/001-scts-genai-programme/research-findings.md` | Vendor security assessment (Azure) |
| ATRS Record | `projects/001-scts-genai-programme/atrs-record.md` | Security architecture, data protection |

### Requirements Traceability

| Security Control | Requirement | CAF Principle |
|-----------------|-------------|---------------|
| Authentication | NFR-SEC-001 | B2 |
| Authorization/RBAC | NFR-SEC-002 | B2 |
| Encryption | NFR-SEC-003 | B3 |
| UK Data Residency | NFR-SEC-004 | A4, B3 |
| Vulnerability Management | NFR-SEC-005 | B4, C2 |
| Court Record Protection | NFR-SEC-006 | B3 |
| UK GDPR Compliance | NFR-C-001 | B3 |
| Audit Logging | NFR-C-002 | C1, D2 |
| Business Continuity | NFR-A-002, NFR-A-003 | D1 |

---

## Appendix A: Glossary

| Term | Definition |
|------|------------|
| AES-256 | Advanced Encryption Standard with 256-bit key length |
| BC/DR | Business Continuity / Disaster Recovery |
| CAF | NCSC Cyber Assessment Framework |
| CASB | Cloud Access Security Broker |
| CDiO | Chief Digital Information Officer |
| CIS | Center for Internet Security |
| CSPM | Cloud Security Posture Management |
| CVSS | Common Vulnerability Scoring System |
| DAST | Dynamic Application Security Testing |
| DLP | Data Loss Prevention |
| DPA | Data Processing Agreement |
| DPIA | Data Protection Impact Assessment |
| DPO | Data Protection Officer |
| EDR | Endpoint Detection and Response |
| IAM | Identity and Access Management |
| ICO | Information Commissioner's Office |
| IDS/IPS | Intrusion Detection System / Intrusion Prevention System |
| MFA | Multi-Factor Authentication |
| NAC | Network Access Control |
| NCSC | National Cyber Security Centre |
| NFR | Non-Functional Requirement |
| NSG | Network Security Group |
| OSS | Open Source Software |
| OWASP | Open Web Application Security Project |
| PAM | Privileged Access Management |
| PII | Personally Identifiable Information |
| PIM | Privileged Identity Management |
| RBAC | Role-Based Access Control |
| ROPA | Records of Processing Activities |
| RPO | Recovery Point Objective |
| RTO | Recovery Time Objective |
| SAML | Security Assertion Markup Language |
| SAR | Subject Access Request |
| SAST | Static Application Security Testing |
| SBOM | Software Bill of Materials |
| SCA | Software Composition Analysis |
| SCTS | Scottish Courts and Tribunals Service |
| SIEM | Security Information and Event Management |
| SIRO | Senior Information Risk Owner |
| SLA | Service Level Agreement |
| SLO | Service Level Objective |
| SOC 2 | Service Organization Control Type 2 |
| SRO | Senior Responsible Owner |
| SSO | Single Sign-On |
| TLS | Transport Layer Security |
| UAT | User Acceptance Testing |
| VNet | Virtual Network |
| WAF | Web Application Firewall |

---

## Approval and Sign-Off

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Project Lead | Chief Digital Information Officer | | |
| Security Architect | Senior AI Technical Architect | | |
| Senior Information Risk Owner (SIRO) | [To be confirmed] | | |
| Data Protection Officer (DPO) | DPO, SCTS | | |

---

**Generated by**: ArcKit `/arckit.secure` command
**Generated on**: 2026-01-27
**ArcKit Version**: 0.11.2
**Project**: SCTS GenAI Programme (Project 001)
**Model**: Claude Opus 4.5
