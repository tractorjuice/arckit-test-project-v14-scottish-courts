# Email: SCTS GenAI Programme - Governance Artifacts Overview

**To:** SCTS Digital Leadership Team
**From:** Enterprise Architecture Team
**Date:** 20 January 2026
**Subject:** SCTS GenAI Programme - Complete Governance Documentation Package

---

Dear Colleagues,

I am pleased to share the complete governance documentation package for the **SCTS GenAI Programme**. This email provides an overview of each document, organised in the logical order you should review them to understand our architecture governance approach.

We have produced **17 comprehensive artifacts** covering the full lifecycle from strategic principles through to delivery planning. Below is a summary of each document and its purpose.

---

## 1. Foundation Documents

### 1.1 Architecture Principles
**File:** `.arckit/memory/architecture-principles.md`

This foundational document establishes the **20 enterprise architecture principles** that guide all decisions for the GenAI Programme. The principles are organised into six categories:

- **Strategic Alignment** (6 principles): Including Justice-Centred Design, Human-in-the-Loop AI, and Accessibility First
- **AI-Specific** (4 principles): Ethical AI, AI Transparency, AI Model Governance, Data Quality
- **Security & Compliance** (3 principles): Security by Design, Data Protection, Scottish Standards
- **Data Management** (3 principles): Court Records Integrity, Data Sovereignty, Single Source of Truth
- **Operational** (2 principles): Observability, Cost Transparency
- **Development** (2 principles): Iterative Delivery, Automation

**Key principle for SCTS:** *"AI must never influence or automate judicial decisions"* - this ensures the judiciary retains full authority over all court matters.

---

### 1.2 Stakeholder Drivers Analysis
**File:** `stakeholder-drivers.md`

This document identifies **who we are building for** and **what they need**. It includes:

- **13 stakeholders** identified (6 internal, 7 external)
- **6 strategic goals** with measurable targets:
  - G-1: Reduce document processing time by 60%
  - G-2: Enable multilingual access for 10 priority languages
  - G-3: Achieve consistent case law application across courts
  - G-4: Maintain zero court record integrity incidents
  - G-5: Full regulatory compliance (GDPR, AI Playbook, Scottish standards)
  - G-6: Staff development and upskilling without job losses
- **5 measurable outcomes** with KPIs
- **RACI matrix** showing governance responsibilities
- **Communication plan** for stakeholder engagement

**Why this matters:** Every requirement and design decision traces back to these stakeholder needs, ensuring we build what SCTS actually needs.

---

## 2. Requirements Documents

### 2.1 Requirements Specification
**File:** `requirements.md`

This comprehensive document defines **what the system must do**. It contains:

- **6 Business Requirements (BR-001 to BR-006):** High-level capabilities the system must deliver
- **15 Functional Requirements (FR-001 to FR-015):** Specific features including:
  - Document upload, AI classification, and human review workflow
  - Speech-to-text transcription and real-time translation
  - Semantic search and case law citation detection
  - Audit trails and AI output labelling
- **22 Non-Functional Requirements (NFR):** Performance, security, scalability, compliance, and usability standards
- **6 Integration Requirements (INT-001 to INT-006):** Connections to Case Management, Document Management, Azure AD, and other SCTS systems
- **5 User Personas:** Court Clerk, Judicial Officer, Court Manager, Non-English Speaker, Public User
- **3 Use Cases:** Document Processing, Real-Time Translation, Case Research

**Priority breakdown:** 30 requirements are CRITICAL/MUST-HAVE, 16 are HIGH/SHOULD-HAVE, and 3 are COULD-HAVE.

---

## 3. Research & Technology Selection

### 3.1 Research Findings
**File:** `research-findings.md`

This document presents our **technology evaluation** across four capability areas:

| Capability | Recommendation | Rationale |
|------------|----------------|-----------|
| Document Intelligence | Azure Document Intelligence | UK data residency, G-Cloud approved |
| Speech Services | Azure Speech Services | Real-time transcription, 10+ languages |
| Translation | Azure Translator | Court terminology customisation |
| Cognitive Search | Azure AI Search | Semantic vectors, hybrid search |

**Build vs Buy Decision:** **BUY** (Azure AI Services)

**3-Year Total Cost of Ownership:** £715,610 (compared to £2.5M+ for a custom build)

The research confirms Azure AI Services meets all technical constraints including UK data residency (Azure UK South/UK West regions) and G-Cloud procurement pathway.

---

### 3.2 Architecture Decision Record - ADR-001
**File:** `decisions/ADR-001-azure-ai-platform-selection.md`

This formal decision record documents our **platform selection** following the MADR v4.0 format:

- **Decision:** Select Azure AI Services as the AI platform
- **Status:** PROPOSED (awaiting formal approval)
- **Context:** Need for AI capabilities within UK jurisdiction
- **Consequences:**
  - Positive: UK data residency, proven technology, G-Cloud approved
  - Negative: Vendor lock-in risk (mitigated by abstraction layers)

This ADR provides the audit trail for why Azure was selected over alternatives.

---

## 4. Data Governance Documents

### 4.1 Data Model
**File:** `data-model.md`

This document defines **what data the system will manage** and how it complies with GDPR:

- **9 data entities** including:
  - USER (staff identities)
  - AI_PROCESSING_REQUEST and AI_PROCESSING_RESULT (AI operations)
  - DOCUMENT_REFERENCE (links to DMS)
  - COURT_SESSION and TRANSLATION_SESSION (translation tracking)
  - PARTICIPANT (court participants - **RESTRICTED** classification)
  - AUDIT_LOG (immutable audit trail)
  - SEARCH_INDEX_ENTRY (semantic search data)

- **Data classification:** 3 Internal, 4 Confidential, 1 Restricted
- **PII inventory:** 15 attributes across 5 entities identified
- **Special category data:** Court proceedings may contain health data, criminal data
- **Retention periods:** 7 years aligned with court records requirements
- **Data governance:** Business owners, stewards, and custodians assigned

**Entity-Relationship Diagram** included showing all relationships.

---

### 4.2 Data Protection Impact Assessment (DPIA)
**File:** `dpia.md`

This **legally required assessment** under UK GDPR Article 35 documents:

- **Why DPIA is required:** 5 of 9 ICO screening criteria met (large-scale processing, AI/ML, vulnerable subjects, special category data, systematic monitoring)
- **Legal basis:** Public Task (GDPR Article 6(1)(e)) - SCTS statutory function
- **Special category basis:** Administration of Justice (DPA 2018 Schedule 1)
- **10 privacy risks identified** with mitigations
- **Residual risk level:** MEDIUM
- **ICO consultation:** NOT REQUIRED (risks adequately mitigated)
- **DPO recommendation:** PROCEED with safeguards

**Action required:** DPO and SIRO sign-off before production deployment.

---

### 4.3 Algorithmic Transparency Recording Standard (ATRS)
**File:** `atrs-record.md`

This document meets the **UK Government requirement for algorithmic transparency**:

- **Tier 1 (Public Summary):** Plain English explanation of what the AI does, suitable for publication on GOV.UK
- **Tier 2 (Technical Details):** Model specifications, training data, fairness assessment framework

Key transparency points:
- AI assists but never decides - humans review all outputs
- AI cannot modify court records
- All AI outputs are labelled with confidence scores
- Bias monitoring and quarterly audits planned

**Action required:** Publish to GOV.UK before production go-live.

---

## 5. Risk & Security Documents

### 5.1 Risk Register
**File:** `risk-register.md`

This document follows the **HM Treasury Orange Book** framework:

- **20 risks identified** across Strategic, Operational, Financial, Compliance, and Technology categories
- **Risk score reduction:** Inherent total 267 → Residual total 168 (**37% improvement**)
- **Risk profile improvement:**
  - Critical risks: 4 → 0 (100% mitigated)
  - High risks: 8 → 4 (50% reduced)

**Top risks requiring attention:**
| Risk | Description | Residual Score | Appetite | Status |
|------|-------------|----------------|----------|--------|
| R-001 | Judicial confidence loss | 15 | 12 | Exceeds appetite |
| R-004 | AI quality damages reputation | 16 | 12 | Exceeds appetite |
| R-007 | Security breach of court data | 15 | 12 | Exceeds appetite |
| R-010 | UK GDPR non-compliance | 15 | 12 | Exceeds appetite |

**Action required:** Escalate these 4 risks to Steering Committee for acceptance or additional mitigation.

---

### 5.2 Secure by Design Assessment
**File:** `secure-by-design-assessment.md`

This document assesses security against **NCSC Cyber Assessment Framework**:

- **NCSC CAF Score:** 10/14 principles achieved
- **Security architecture:** Zero-trust network design, defence in depth
- **Key controls:**
  - Azure AD SSO with MFA
  - Role-based access control (RBAC)
  - AES-256 encryption at rest, TLS 1.2+ in transit
  - UK data residency (Azure UK South/West only)
  - Read-only access to court records (AI cannot modify)

**Pending actions:**
- Penetration testing (before production)
- SIEM implementation (security monitoring)
- SIRO sign-off on residual risks

---

### 5.3 AI Playbook Assessment
**File:** `ai-playbook-assessment.md`

This document assesses compliance with the **UK Government AI Playbook**:

- **Risk classification:** MEDIUM-RISK AI deployment
- **Overall score:** 126/160 (79%)
- **Status:** APPROVED WITH CONDITIONS

**10 Core Principles Assessment:**
- 7 principles: Fully compliant
- 3 principles: Partially compliant (data quality, bias/fairness, skills)

**Conditions for approval:**
1. DPIA must be approved before deployment
2. Equality Impact Assessment (EqIA) must be completed for translation services
3. Bias audit must be completed for all 10 priority languages

---

## 6. Design Documents

### 6.1 High-Level Design (HLD)
**File:** `high-level-design.md`

This document describes **how the system will be built**:

- **Architecture style:** Cloud-native microservices on Azure
- **Deployment platform:** Azure Kubernetes Service (AKS) with auto-scaling
- **Core components:**
  - Web Application (React, TypeScript, WCAG 2.2 AA)
  - API Gateway (Azure API Management)
  - Document Service (Python/FastAPI + Azure Document Intelligence)
  - Speech Service (Python/FastAPI + Azure Speech/Translator)
  - Search Service (Python/FastAPI + Azure AI Search)
  - Audit Service (immutable logging)

**C4 architecture diagrams** included:
- Context Diagram (system in its environment)
- Container Diagram (major components)

**Requirements coverage:** 100% of functional requirements mapped to design components.

---

## 7. Delivery Planning Documents

### 7.1 Project Plan
**File:** `project-plan.md`

This document provides the **delivery roadmap**:

- **Total duration:** 18 months (January 2026 - July 2027)
- **6 delivery phases:**
  1. Discovery & Foundation (2 months)
  2. Document Intelligence MVP (4 months)
  3. Speech & Translation Services (4 months)
  4. Cognitive Search (3 months)
  5. Integration & Hardening (3 months)
  6. Go-Live & Transition (2 months)

**Key milestones:**
- M1: Foundation Complete (February 2026)
- M2: Document Intelligence Live (June 2026)
- M3: Translation Services Live (October 2026)
- M4: Search Services Live (January 2027)
- M5: Full Platform Live (July 2027)

---

### 7.2 Product Backlog
**File:** `backlog.md`

This document breaks requirements into **deliverable work items**:

- **184 user stories** in GDS format ("As a [user], I need to [action], so that [benefit]")
- **22 sprints** (2-week sprints)
- **Estimated duration:** 44 weeks of development

**Story distribution by capability:**
| Epic | Stories | Priority |
|------|---------|----------|
| Document Intelligence | 45 | Mostly Must-have |
| Speech Services | 35 | Must/Should-have |
| Translation Services | 30 | Should-have |
| Cognitive Search | 35 | Should-have |
| Platform Infrastructure | 25 | Must-have |
| Security & Compliance | 14 | Must-have |

**Priority breakdown:** 53% Must-have, 30% Should-have, 16% Could-have

---

## 8. Governance & Traceability Documents

### 8.1 Traceability Matrix
**File:** `traceability-matrix.md`

This document demonstrates **end-to-end traceability** from stakeholder needs to delivery:

- **Traceability score:** 72/100
- **Coverage achieved:**
  - Stakeholder → Goals: 100%
  - Goals → Requirements: 100%
  - Requirements → HLD: 100%
  - Requirements → User Stories: 100%
  - Requirements → Tests: 0% (test plan pending)

**Why this matters:** Every feature can be traced back to a stakeholder need, ensuring we build the right thing.

---

### 8.2 Governance Analysis Report
**File:** `analysis-report.md`

This document provides an **independent quality assessment** of all artifacts:

- **Overall governance score:** 82/100 (Grade B)
- **Status:** Issues Found - address before production

**Score breakdown:**
| Category | Score |
|----------|-------|
| Requirement Quality | 95% |
| Architecture Alignment | 92.5% |
| Stakeholder Alignment | 100% |
| Risk Management | 90% |
| UK Gov Compliance | 80% |
| Security | 65% |
| Traceability | 50% |

**Critical issues (must resolve):**
1. DPIA approval required
2. EqIA completion required
3. Bias audit required

**High priority issues:**
4. Escalate 4 appetite-exceeding risks
5. Complete penetration testing
6. Implement SIEM monitoring
7. Create test plan (0% test coverage currently)
8. Obtain SIRO sign-off

---

### 8.3 Project Story
**File:** `PROJECT-STORY.md`

This comprehensive document provides a **complete narrative** of the project journey:

- **9 chapters** covering the full lifecycle
- **Timeline visualisations** (Gantt chart, flowchart, milestones)
- **Traceability diagrams** showing how everything connects
- **Key metrics and achievements**
- **Appendices** with artifact register and glossary

This document serves as both a historical record and an executive summary of the governance work completed.

---

## Summary of Actions Required

Before proceeding to production, the following actions are required:

### Critical (Blocking)
1. **DPIA Approval** - DPO and SIRO sign-off
2. **Equality Impact Assessment** - For translation services
3. **Bias Audit** - Testing for 10 priority languages

### High Priority
4. **Risk Escalation** - 4 risks exceed appetite, need Steering Committee review
5. **Penetration Testing** - Security validation
6. **SIEM Implementation** - Security monitoring
7. **Test Plan Creation** - ~290 test cases needed
8. **SIRO Sign-off** - Formal risk acceptance

### Medium Priority
9. **ATRS Publication** - Publish to GOV.UK
10. **Additional ADRs** - Document data and security decisions
11. **Detailed Design (DLD)** - Before implementation begins

---

## Document Access

All documents are available in the project repository:
```
projects/001-scts-genai-programme/
├── README.md
├── stakeholder-drivers.md
├── requirements.md
├── research-findings.md
├── data-model.md
├── dpia.md
├── atrs-record.md
├── risk-register.md
├── secure-by-design-assessment.md
├── ai-playbook-assessment.md
├── high-level-design.md
├── project-plan.md
├── backlog.md
├── traceability-matrix.md
├── analysis-report.md
├── PROJECT-STORY.md
└── decisions/
    └── ADR-001-azure-ai-platform-selection.md
```

Architecture principles are stored at:
```
.arckit/memory/architecture-principles.md
```

---

## Next Steps

1. **Review** the documents in the order presented above
2. **Schedule** a walkthrough session if you would like us to present the key findings
3. **Approve** the architecture principles and ADR-001 (Azure platform selection)
4. **Initiate** the critical actions (DPIA approval, EqIA, bias audit)
5. **Confirm** the delivery timeline and resource allocation

Please do not hesitate to contact us if you have any questions about these documents.

Kind regards,

**Enterprise Architecture Team**

---

*This governance package was produced using the ArcKit Architecture Governance Framework, ensuring compliance with UK Government standards including the Technology Code of Practice, AI Playbook, and HM Treasury Green/Orange Book guidance.*
