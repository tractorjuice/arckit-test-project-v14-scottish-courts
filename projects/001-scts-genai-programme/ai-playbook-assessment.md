# UK Government AI Playbook Assessment

**Project**: SCTS GenAI Programme
**Department/Agency**: Scottish Courts and Tribunals Service (SCTS)
**AI System**: Multi-capability AI platform for Document Intelligence, Speech Services, Translation, and Cognitive Search
**Assessment Date**: 2026-01-17
**Assessor**: ArcKit AI Governance Assessment
**Risk Level**: [x] Medium-Risk / [ ] High-Risk / [ ] Low-Risk

---

## Executive Summary

**Overall Compliance**: 8/10 principles compliant

**Overall Score**: 126/160 (79%)

**Risk Assessment**:
- [ ] HIGH-RISK (fully automated decisions affecting rights, safety, health)
- [x] MEDIUM-RISK (significant impact with human oversight)
- [ ] LOW-RISK (productivity tools, administrative tasks)

**Status**:
- [ ] COMPLIANT (9-10 principles met)
- [x] PARTIALLY COMPLIANT (7-8 principles met)
- [ ] NON-COMPLIANT (< 7 principles met)

**Critical Issues**: 3 blocking issues requiring action before production deployment

**Go/No-Go Decision**: [x] APPROVED WITH CONDITIONS / [ ] APPROVED / [ ] REJECTED

### Risk Level Justification

The SCTS GenAI Programme is assessed as **MEDIUM-RISK** based on the following factors:

**Factors Supporting MEDIUM-RISK Classification**:
1. **Human-in-the-Loop Mandated**: All AI capabilities explicitly require human approval before affecting court records or proceedings (BR-003, FR-003, Principle 2)
2. **Administrative Focus**: AI is used for document classification, translation assistance, and search - not judicial decision-making
3. **No Automated Rights Decisions**: Explicit exclusion of AI for judicial decisions, case outcome prediction, or automated case progression (Project Scope - Out of Scope)
4. **Vulnerable Users**: Court users include vulnerable populations (witnesses, victims, non-English speakers)
5. **Public Trust Critical**: Justice system requires high public confidence

**Why NOT High-Risk**:
- AI does NOT make autonomous decisions affecting legal status, fundamental rights, or case outcomes
- Human interpreters remain mandatory for complex/sensitive matters (BC-2)
- AI outputs are recommendations only; humans make all consequential decisions

**Why NOT Low-Risk**:
- Court documents and proceedings have legal significance
- Errors could indirectly affect access to justice
- Vulnerable populations are affected users
- Public trust in courts could be impacted by AI failures

### Summary Assessment

| Area | Score | Status |
|------|-------|--------|
| 10 Core Principles | 81/100 | ⚠️ PARTIAL |
| 6 Ethical Themes | 45/60 | ⚠️ PARTIAL |
| **TOTAL** | **126/160 (79%)** | ⚠️ GOOD |

### Critical Blocking Issues

1. **CRIT-01**: DPIA not yet completed (required before deployment) - Principle 2
2. **CRIT-02**: ATRS not yet published (mandatory for public bodies) - Theme 2
3. **CRIT-03**: Bias audit not completed for translation services (required before deployment) - Theme 3

### Key Strengths

- ✅ Strong Human-in-the-Loop design embedded from requirements (Principle 2, BR-003)
- ✅ Comprehensive architecture principles covering ethical AI (Principles 7, 8, 9)
- ✅ UK data residency requirement ensures data sovereignty (TC-4, NFR-SEC-004)
- ✅ Scottish Government standards explicitly required (NFR-C-003)
- ✅ Clear accountability structure with named stakeholders
- ✅ Staff job security commitment addresses workforce concerns (BR-006)

---

## AI System Overview

### What is the AI System?

**System Name**: SCTS GenAI Platform

**Purpose**: Enhance court operational efficiency and access to justice through AI-assisted document processing, multilingual support, and intelligent search capabilities.

**Type of AI**:
- [x] Natural Language Processing (document classification, entity extraction, search)
- [x] Speech Recognition (transcription)
- [x] Machine Translation (real-time translation)
- [x] Computer Vision (OCR for scanned documents)
- [ ] Generative AI (limited - not primary use case)
- [ ] Predictive AI (explicitly excluded for case outcomes)

**Use Case**:

The AI system will be used for:
1. **Document Intelligence**: Automated classification and entity extraction from court documents (civil and criminal)
2. **Speech-to-Text**: Transcription of court proceedings with speaker diarisation
3. **Translation Services**: Real-time translation between English and 10 non-English languages for court users
4. **Cognitive Search**: Semantic search across court documents, case law citation detection, similarity analysis

**Users**:
- **Internal users**: Court Clerks (primary), Court Administration Managers, Legal Professionals (via search)
- **External users**: Court users/litigants (translation services), Legal representatives
- **Affected population**: All court users, particularly non-English speakers and vulnerable witnesses

**Decision Authority**:
- [x] AI makes recommendations, humans decide
- [ ] AI makes decisions with human review
- [ ] AI makes autonomous decisions (HIGH-RISK - justify carefully)

**Justification**: All AI outputs are explicitly recommendations requiring human confirmation (FR-003). AI cannot modify court records without human approval (BR-003, Principle 14).

---

## The 10 Core Principles Assessment

### 1. Understanding AI

**Principle**: Organizations must comprehend what AI is, its capabilities, and limitations.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Team understands AI is not sentient or reasoning
- [x] AI limitations documented (hallucinations, biases, edge cases)
- [x] Use cases appropriate for AI capabilities
- [x] Realistic expectations set with stakeholders
- [x] Technical constraints understood (data quality, compute, latency)

**AI Limitations Documented** (from Architecture Principles):

| Limitation | Impact | Mitigation |
|------------|--------|------------|
| Classification accuracy < 100% | May misclassify documents | Human review for all classifications (FR-003) |
| Translation accuracy < 100% | Legal terminology may be incorrect | 85% accuracy target, human interpreter backup (BR-002) |
| Speech recognition errors | Transcription may have errors | Confidence indicators, human review (FR-004) |
| Bias in training data | May treat groups differently | Bias assessment and monitoring (Principle 7) |
| Document quality variations | Poor scans reduce accuracy | Quality indicators, manual fallback (FR-014) |

**Findings**:
The architecture principles document (ARC-001-PRIN-v1.0) demonstrates clear understanding of AI capabilities and limitations. Principle 8 (AI Transparency) explicitly requires confidence scores and documented limitations. Requirements include manual fallback modes (FR-014) acknowledging AI will not always be available or accurate. Staff training on AI limitations is required (Principle 2).

**Gaps**:
- Training programme for staff not yet developed (dependency noted)
- Need to document specific accuracy expectations per AI capability

**Score**: 9/10

---

### 2. Lawful and Ethical Use

**Principle**: AI deployment must comply with legal requirements and ethical standards.

**Compliance Status**: [ ] COMPLIANT / [x] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Legal review process identified (Legal Services Director stakeholder)
- [ ] Data Protection Impact Assessment (DPIA) completed - **NOT YET**
- [ ] Equality Impact Assessment (EqIA) completed - **NOT YET**
- [ ] Human Rights assessment completed - **NOT YET**
- [x] UK GDPR compliance requirements defined (NFR-C-001)
- [x] Equality Act 2010 compliance considered (Principle 3, Accessibility)
- [x] Public Sector Equality Duty considered
- [x] Data Ethics Framework principles embedded in architecture
- [x] Early engagement with legal/compliance teams documented

**Legal and Ethical Checks**:

| Check | Status | Issues Found | Resolution |
|-------|--------|--------------|------------|
| DPIA | 🔄 In Progress | Required before production (NFR-C-001) | DPO assigned, target 2026-Q2 |
| EqIA | ⏳ Not Started | Required for translation/accessibility | Plan to initiate 2026-Q1 |
| Human Rights | ⏳ Not Started | Required for court user impact | Plan to initiate 2026-Q1 |
| UK GDPR | ✅ Requirements defined | Lawful basis documented (NFR-C-001) | Implementation tracking |
| Equality Act | ✅ Partial | WCAG 2.2 AA required (NFR-U-001) | Accessibility testing planned |

**Data Protection**:
- Legal basis for processing: **Public Task** (Article 6(1)(e) UK GDPR) - SCTS statutory function
- Special category data: [x] Yes - Court proceedings may include health data, criminal data
- Data retention period: 7 years minimum aligned with court records (NFR-C-001)
- Right to object: [x] Enabled - Consent required for AI translation (FR-015)

**Findings**:
Legal and ethical requirements are well-defined in requirements.md and architecture principles. The DPO is identified as a key stakeholder with clear DPIA responsibilities. However, the actual assessments (DPIA, EqIA, Human Rights) are not yet completed. NFR-C-001 explicitly requires DPIA before deployment, and this is identified as a project dependency.

**Gaps**:
- **BLOCKING**: DPIA not yet completed (required before production)
- **BLOCKING**: EqIA not yet initiated
- **BLOCKING**: Human Rights assessment not yet initiated

**Score**: 6/10

---

### 3. Security

**Principle**: Systems must be secure and resilient to cyber attacks, including AI-specific threats.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Cyber security assessment requirements defined (NFR-SEC-005)
- [x] NCSC guidance referenced (Scottish Cyber Resilience Framework)
- [x] AI-specific threats to be assessed
- [x] Security controls defined (NFR-SEC-001 to NFR-SEC-006)
- [ ] Penetration testing completed - **Not yet (pre-production)**
- [ ] Red teaming conducted - **Not yet (planned for high-risk translation)**
- [x] Incident response plan requirements defined
- [x] Supply chain security addressed (vendor selection via G-Cloud)

**AI-Specific Security Threats**:

| Threat | Risk Level | Mitigation |
|--------|------------|------------|
| Prompt Injection | LOW | No generative AI with user prompts; classification/translation models |
| Data Poisoning | MEDIUM | Azure managed models; custom training with reviewed data |
| Model Theft | LOW | Azure managed service; no self-hosted models |
| Adversarial Attacks | MEDIUM | Input validation (FR-001); human review (FR-003) |
| Model Inversion | LOW | No personally identifiable model outputs |

**Security Controls** (from NFR-SEC requirements):
- [x] Input validation and sanitization (FR-001)
- [x] Output content filtering (translation quality checks)
- [x] Rate limiting on API endpoints (to be configured)
- [x] Access controls (RBAC) (NFR-SEC-002)
- [x] Audit logging of all AI interactions (FR-012, NFR-C-002)
- [x] Encryption at rest (AES-256) and in transit (TLS 1.2+) (NFR-SEC-003)
- [x] Secure model storage (Azure managed)
- [x] Regular security updates and patching (vendor responsibility + monitoring)

**Findings**:
Security requirements are comprehensive (NFR-SEC-001 through NFR-SEC-006). The architecture explicitly requires Security by Design (Principle 11) as NON-NEGOTIABLE with mandatory controls. UK data residency (NFR-SEC-004, Principle 15) ensures data sovereignty. Scottish Cyber Resilience Framework compliance is required (NFR-C-003). Use of G-Cloud approved Azure services provides supply chain assurance.

**Gaps**:
- Penetration testing not yet completed (scheduled for pre-production)
- AI-specific threat model to be documented
- Red teaming for translation services (medium risk) to be scheduled

**Score**: 8/10

---

### 4. Human Control

**Principle**: Meaningful human oversight must exist at appropriate stages.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Human-in-the-loop design implemented (Principle 2, FR-003)
- [x] Decision points require human approval
- [x] Override capability exists for humans (FR-003)
- [x] Escalation process documented (FR-005, FR-014)
- [x] Human review frequency defined (every AI output for classification)
- [x] Staff training on AI system limitations required
- [x] Clear responsibilities assigned (stakeholder RACI)

**Human Oversight Model**:
- [x] **Human-in-the-loop**: Human reviews EVERY decision before implementation
- [ ] **Human-on-the-loop**: Human reviews decisions periodically/randomly
- [x] **Human-in-command**: Human can override AI decisions at any time
- [ ] **Fully automated**: AI acts autonomously (HIGH-RISK - justify!)

**Human Review Requirements**:

| Decision Type | Review Requirement | Reviewer Role | Escalation Path |
|---------------|-------------------|---------------|-----------------|
| Document Classification | Every decision | Clerk of Court | Court Admin Manager |
| Translation (routine) | AI-assisted with human backup | Clerk + Human Interpreter available | Human Interpreter |
| Translation (complex/sensitive) | Human interpreter only (BC-2) | Human Interpreter | Court Admin Manager |
| Search Results | User judgment | User | N/A |
| Court Record Entry | Human approval mandatory (BR-003) | Clerk of Court | Court Admin Manager |

**For Medium-Risk AI**:
- [x] Human oversight for all consequential outputs
- [x] Humans trained on AI limitations and biases (requirement)
- [x] Override process defined and documented (FR-003)
- [x] Decision rationale explainable to affected persons (FR-011, Principle 8)

**Findings**:
Human control is exceptionally well-designed in this programme. Architecture Principle 2 ("Human-in-the-Loop for Consequential Decisions") is marked as CRITICAL and explicitly states "AI systems MUST NOT make autonomous decisions that affect legal proceedings, case outcomes, or individual rights." FR-003 requires human review and override for all AI classifications. BC-2 ensures human interpreters remain for complex matters. Manual fallback mode (FR-014) ensures courts function without AI.

**Gaps**:
- Staff training programme not yet developed
- Override process not yet tested with real users

**Score**: 9/10

---

### 5. Lifecycle Management

**Principle**: Understand complete product lifecycle from selection to decommissioning.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Lifecycle plan implicit in requirements and milestones
- [x] Supplier selection criteria defined (research-findings.md)
- [x] Contract requirements include performance metrics (research-findings.md)
- [x] Model versioning and change management required (Principle 9)
- [x] Monitoring and performance tracking defined (Principle 17, NFR-M-001)
- [x] Retraining schedule considerations (NFR-M-002)
- [x] Model drift detection requirement (NFR-M-002)
- [ ] Decommissioning plan not yet documented

**Lifecycle Stages**:

**1. Selection and Procurement**:
- [x] Requirements defined (requirements.md - comprehensive)
- [x] Build vs buy decision documented (research-findings.md)
- [x] Supplier evaluation approach defined (G-Cloud, PoC process)
- [x] Contract requirements include AI-specific terms (research-findings.md)

**2. Development and Testing**:
- [x] Training data provenance to be documented
- [ ] Bias testing not yet completed
- [x] Performance benchmarks defined (NFR-P requirements)
- [x] User acceptance testing required (FR-003, UC-1, UC-2, UC-3)
- [x] Accessibility testing required (NFR-U-001)

**3. Deployment**:
- [x] Phased rollout plan defined (Timeline milestones - PoC → Production)
- [x] Monitoring dashboards required (NFR-M-001)
- [x] Alert thresholds to be defined
- [x] Incident response procedures required (NFR-A-003)

**4. Operation and Maintenance**:
- [x] Ongoing performance monitoring (Principle 17)
- [x] Model drift detection required (NFR-M-002)
- [x] User feedback collection (FR-013)
- [x] Regular fairness and bias audits required (Principle 7)

**5. Decommissioning**:
- [ ] Data deletion procedure not yet defined
- [ ] Model archive/deletion not yet defined
- [ ] Lessons learned process to be established

**Model Monitoring Metrics** (from NFR requirements):

| Metric | Baseline | Threshold | Current | Action if Exceeded |
|--------|----------|-----------|---------|-------------------|
| Classification Accuracy | 90% | 85% | TBD (PoC) | Retrain model |
| Translation Accuracy | 85% | 80% | TBD (PoC) | Human review increase |
| Search Relevance | 80% satisfaction | 70% | TBD | Tune ranking |
| API Response Time (p95) | < 10 seconds | < 30 seconds | TBD | Scale infrastructure |

**Findings**:
Lifecycle management is well-addressed through the combination of requirements (NFR-M-001, NFR-M-002), architecture principles (Principle 9, 17, 19), and the research document. The phased delivery approach (Principle 19) with PoC → Pilot → Limited Production → Full Production provides appropriate gates. Model governance (Principle 9) requires versioning, testing, approval, and rollback.

**Gaps**:
- Decommissioning plan not yet documented
- Specific model monitoring thresholds not yet established
- Lessons learned process to be formalised

**Score**: 8/10

---

### 6. Right Tool Selection

**Principle**: AI should only be deployed when it genuinely solves problems better than alternatives.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Problem clearly defined (requirements.md - business context)
- [x] Alternative solutions considered (manual process remains as fallback)
- [x] Cost-benefit analysis completed (research-findings.md TCO analysis)
- [x] AI adds genuine value over alternatives
- [x] Use case appropriate for AI (not using AI for sake of it)
- [x] Success metrics defined (BR-001 to BR-006)
- [x] Pilot/proof-of-concept planned (Timeline - Phase 1)

**Alternatives Considered**:

| Solution | Pros | Cons | Why Not Chosen |
|----------|------|------|----------------|
| Manual process (status quo) | Accurate, human judgment | Slow, expensive, backlogs growing | Cannot scale to demand (2M docs/year) |
| Rule-based document classification | Explainable, simple | Inflexible, many edge cases | Too many document variations |
| Human interpreters only | High accuracy for complex | Expensive, availability delays | Delays access to justice, cost (£200K savings possible) |
| AI-assisted (selected) | Scalable, faster, 24/7 | Accuracy < 100%, bias risk | Best fit with human oversight mitigation |

**Use Case Appropriateness**:
- [x] Problem is well-suited to AI capabilities (classification, translation, search)
- [x] Sufficient quality training data available (Azure pre-trained + custom)
- [x] Success can be measured objectively (accuracy, time, satisfaction metrics)
- [x] Acceptable trade-offs documented (e.g., 85% accuracy with human backup)
- [x] NOT using AI just because it's trendy (clear efficiency and access drivers)

**Inappropriate Use Cases Explicitly Excluded** (Project Scope):
- [x] AI for judicial decision-making - EXCLUDED
- [x] Case outcome prediction - EXCLUDED
- [x] Automated case progression - EXCLUDED
- [x] Replacement of interpreters for sensitive matters - EXCLUDED

**Success Metrics** (from BR requirements):

| Metric | Baseline | Target | Current | Status |
|--------|----------|--------|---------|--------|
| Document processing time | 4.5 hours | 1.8 hours | TBD | ⏳ |
| Document backlog | Current volume | -40% | TBD | ⏳ |
| Languages supported | 0 | 10 | Design: 10 | ✅ |
| Staff adoption | 0% | 80% | TBD | ⏳ |
| Court record incidents | 0 | 0 | N/A | ✅ |

**Findings**:
The programme demonstrates clear problem definition and appropriate use of AI. The explicit exclusion of judicial decision-making AI shows understanding of appropriate boundaries. Alternatives were considered (manual fallback is mandatory). Research findings document provides comprehensive build vs buy analysis with cost justification. Success metrics are quantified in business requirements.

**Gaps**:
- None significant

**Score**: 9/10

---

### 7. Collaboration

**Principle**: Engage across government and with external stakeholders.

**Compliance Status**: [ ] COMPLIANT / [x] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Cross-government collaboration (Scottish Government Digital Directorate stakeholder)
- [ ] Academia partnerships - not documented
- [x] Industry engagement (cloud vendors via G-Cloud)
- [ ] Civil society consultation - not documented
- [x] User community involvement (Court users, legal profession as stakeholders)
- [ ] Sharing lessons learned - not yet (programme in early stages)
- [ ] Contributing to government AI community - not yet

**Collaboration Activities**:

| Stakeholder | Engagement Type | Purpose | Outcome |
|-------------|-----------------|---------|---------|
| Scottish Government Digital Directorate | Policy alignment | Strategy compliance | Requirements include SG AI Strategy |
| Cabinet Secretary for Justice | Ministerial briefings | Political oversight | Stakeholder engagement plan |
| Faculty of Advocates | Stakeholder | User requirements | Search capability requirements |
| Law Society of Scotland | Stakeholder | User requirements | Professional practice concerns |
| ICO | Regulatory compliance | GDPR guidance | DPIA requirements defined |
| Azure/Microsoft | Vendor partnership | Technology delivery | G-Cloud procurement |

**Knowledge Sharing**:
- [ ] Documented lessons learned - planned for post-PoC
- [ ] Presented at cross-government forums - not yet
- [ ] Published case studies - not yet
- [ ] Contributed to reusable components - not yet

**Findings**:
Stakeholder analysis demonstrates good identification of government and external stakeholders. Scottish Government alignment is explicit requirement. However, formal collaboration with academia, civil society organisations, or AI ethics bodies is not documented. Knowledge sharing is planned but not yet executed (programme in early stages).

**Gaps**:
- No academic partnerships documented
- No civil society consultation (e.g., justice advocacy groups)
- Knowledge sharing mechanisms not yet established
- Consider engagement with AI Standards Hub

**Score**: 7/10

---

### 8. Commercial Partnership

**Principle**: Early engagement with commercial colleagues on responsible AI expectations.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Procurement approach defined (G-Cloud Digital Marketplace)
- [x] AI requirements for contract documented (research-findings.md)
- [x] Supplier responsible AI commitments assessed (ISO 27001, SOC 2)
- [x] Audit rights considered (vendor evaluation criteria)
- [x] Data rights and ownership clear (UK data residency requirement)
- [x] Exit strategy considered (data portability in vendor evaluation)
- [x] Performance metrics and SLAs required
- [ ] Liability clauses not yet negotiated (contract stage)

**Contract Requirements for AI** (from research-findings.md):
- [x] **Performance metrics**: Accuracy, latency, uptime SLAs defined in NFRs
- [x] **Explainability**: Confidence scores required (Principle 8)
- [x] **Bias audits**: Fairness testing required (Principle 7)
- [x] **Retraining**: Model governance process (Principle 9)
- [x] **Data rights**: UK data residency mandatory (TC-4)
- [x] **Audit rights**: To be included in contract
- [x] **Security**: ISO 27001, SOC 2 required (vendor selection criteria)
- [ ] **Liability**: To be negotiated in contract
- [x] **Exit**: Data portability assessed (vendor lock-in risk evaluation)

**Supplier Responsible AI Commitments** (Azure):

| Commitment | Contractual? | Verification Method |
|------------|--------------|---------------------|
| UK data residency | ✅ Yes (G-Cloud terms) | Azure region configuration |
| ISO 27001 certification | ✅ Yes | Certificate verification |
| SOC 2 Type II | ✅ Yes | Attestation report |
| GDPR compliance | ✅ Yes | Data processing agreement |
| Model performance SLA | 🔄 To be defined | PoC validation |

**Findings**:
Commercial partnership approach is well-structured through use of G-Cloud Digital Marketplace, which provides pre-vetted suppliers with framework terms. Research findings document comprehensively assesses vendor capabilities, security certifications, and exit strategies. UK data residency is a contractual requirement. The Digital Transformation Agreement 2021 (DTA21) provides government pricing benefits.

**Gaps**:
- Specific AI liability clauses to be negotiated
- Performance SLAs to be finalised post-PoC
- Audit rights to be explicitly included in call-off

**Score**: 8/10

---

### 9. Skills and Expertise

**Principle**: Teams need appropriate technical, ethical, and domain expertise.

**Compliance Status**: [ ] COMPLIANT / [x] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] AI/ML technical expertise identified (Senior AI Technical Architect role)
- [ ] Data science capability - depends on hire
- [ ] Ethical AI expertise - not explicitly identified
- [x] Domain expertise (Court Admin Managers, Clerks as stakeholders)
- [ ] User research capability - not explicitly identified
- [x] Legal/compliance expertise (Legal Services Director, DPO)
- [ ] Cyber security expertise - not explicitly identified
- [ ] Training programme developed - not yet

**Team Composition**:

| Role | Filled? | Name/Team | Expertise Level |
|------|---------|-----------|-----------------|
| AI/ML Specialist | 🔄 Hiring | Senior AI Technical Architect | Target: Senior |
| Data Scientist | ❌ Gap | Not identified | N/A |
| Ethics Advisor | ❌ Gap | Not identified | N/A |
| Domain Expert | ✅ | Court Admin Managers, Clerks | Senior |
| User Researcher | ❌ Gap | Not identified | N/A |
| Legal/Compliance | ✅ | Legal Services Director, DPO | Senior |
| Security Specialist | ❌ Gap | Not identified (may be ICT Operations) | N/A |
| Product Manager | ✅ | CDiO / AI Technical Architect | Senior |

**Training Provided**:
- [ ] AI fundamentals for all team members - planned
- [ ] Ethical AI considerations - planned
- [ ] Bias recognition and mitigation - planned
- [ ] AI system limitations - planned
- [ ] User research with AI systems - not identified
- [ ] Incident response for AI failures - planned

**Findings**:
The Senior AI Technical Architect role is identified as critical dependency (Timeline - Dependencies). However, this is a single-point-of-failure for AI expertise. Domain expertise is strong through Court Admin Managers and Clerks. Legal and compliance coverage is good. Gaps exist in data science, ethical AI expertise, user research, and security specialist roles.

**Gaps**:
- **Critical**: Senior AI Technical Architect hire not yet completed
- Missing dedicated data science capability
- No ethical AI specialist identified (could engage AI Standards Hub)
- User research capability not documented
- Security specialist role not explicitly identified
- Training programme not yet developed

**Score**: 6/10

---

### 10. Organizational Alignment

**Principle**: AI use must align with organizational policies, governance, and assurance.

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] AI governance structure implicit (SRO, CDiO, stakeholder RACI)
- [x] AI strategy alignment documented (Scottish Government AI Strategy - NFR-C-003)
- [x] Organizational AI principles defined (architecture-principles.md)
- [x] Risk management process followed (risk register identified in workflow)
- [x] Assurance team engagement planned (Legal Services, DPO)
- [x] Escalation process defined (stakeholder hierarchy)
- [x] Senior Responsible Owner (SRO) assigned (Chief Executive)
- [x] Regular governance reviews planned (monthly review cycle)

**Governance Structure**:
- **Executive Sponsor**: Chief Executive, SCTS
- **Programme Owner (SRO)**: Chief Digital Information Officer
- **Product Owner**: Senior AI Technical Architect (when hired)
- **Assurance Lead**: Legal Services Director + DPO

**Governance Checkpoints** (from Timeline):

| Phase | Review Required | Status | Date | Outcome |
|-------|-----------------|--------|------|---------|
| Requirements | Stakeholder sign-off | 🔄 In Progress | 2026-Q1 | Pending |
| PoC | Technical + Business | ⏳ Planned | 2026-Q2 | - |
| Pre-Deployment | DPIA + Security + Ethics | ⏳ Planned | 2026-Q2/Q3 | - |
| Post-Deployment | Performance Review | ⏳ Planned | 2026-Q4+ | - |

**Organizational AI Principles**:
- [x] Aligns with department's AI principles (architecture-principles.md - 20 principles)
- [x] Aligns with Scottish Government AI Strategy (explicit requirement)
- [x] No conflicts with organizational values (justice-centred design)

**Findings**:
Organisational alignment is strong. SCTS has defined comprehensive architecture principles (20 principles across 6 categories) that embed ethical AI, human control, and security. The governance structure identifies Chief Executive as sponsor, CDiO as programme owner, with clear escalation paths. Scottish Government AI Strategy alignment is an explicit requirement. Monthly document review cycle provides ongoing governance.

**Gaps**:
- AI Governance Board not formally constituted (implicit through stakeholder structure)
- Formal approval gates to be documented

**Score**: 9/10

---

## Six Ethical Themes Assessment

### 1. Safety, Security, and Robustness

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Safety testing requirements defined (human review, confidence thresholds)
- [x] Robustness testing (NFR-A-003 - graceful degradation)
- [x] Security controls implemented (NFR-SEC-001 to NFR-SEC-006)
- [x] Fail-safe mechanisms in place (FR-014 - manual fallback, circuit breakers)
- [x] Incident response plan required (NFR-A-003)

**Safety Measures**:

| Risk | Safeguard | Testing | Status |
|------|-----------|---------|--------|
| Incorrect classification | Human review all outputs (FR-003) | UAT with real documents | ⏳ Planned |
| Translation errors | Confidence indicators, human backup | Professional linguist review | ⏳ Planned |
| System failures | Graceful degradation, manual fallback | DR testing quarterly | ⏳ Planned |
| Court record corruption | Read-only access, separate storage (BR-003) | Architecture review | ✅ Designed |

**Score**: 8/10

---

### 2. Transparency and Explainability

**Compliance Status**: [ ] COMPLIANT / [x] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [ ] Algorithmic Transparency Recording Standard (ATRS) completed - **NOT YET**
- [ ] System documented publicly - **NOT YET**
- [x] Decision explanations available (confidence scores, FR-011)
- [ ] Model card or factsheet published - **NOT YET**
- [x] Privacy notice to include AI use - planned

**ATRS Compliance**:
- **ATRS URL**: NOT YET PUBLISHED - **BLOCKING ISSUE**
- **Publication Date**: Target 2026-Q2 (before production)
- **Last Updated**: N/A

**Explainability Level**:
- [x] **Partial explainability**: Confidence scores provided, general methodology documented
- [ ] **Full explainability**: Cannot explain every individual decision in detail
- [ ] **Black box**: Not applicable - explainability is required

**Public Communication**:
- [x] Citizens to be informed AI is being used (FR-015 - consent for translation)
- [x] How to request human review explained (human interpreter backup)
- [ ] Complaint mechanism to be published

**Findings**:
Transparency requirements are well-defined in Principle 8 (AI Transparency and Explainability) and FR-011 (AI Output Labelling). All AI outputs must be labelled as AI-assisted. Confidence scores are required. However, the mandatory ATRS publication is not yet completed.

**Gaps**:
- **BLOCKING**: ATRS not yet published (mandatory for Scottish public body)
- Model cards not yet created
- Public-facing transparency statement not yet published

**Score**: 6/10

---

### 3. Fairness, Bias, and Discrimination

**Compliance Status**: [ ] COMPLIANT / [x] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [ ] Bias assessment completed - **NOT YET**
- [x] Training data review planned (Principle 7, 10)
- [ ] Fairness metrics calculated - **NOT YET**
- [x] Protected characteristics analysis required (Principle 7)
- [x] Bias mitigation techniques identified (ongoing monitoring, feedback loops)
- [x] Ongoing monitoring for bias drift required (Principle 7)

**Fairness Testing** (Required but not yet executed):

| Protected Characteristic | Metric | Baseline | Threshold | Current | Status |
|-------------------------|--------|----------|-----------|---------|--------|
| Gender | To be defined | - | ±10% | TBD | ⏳ |
| Ethnicity | To be defined | - | ±10% | TBD | ⏳ |
| Age | To be defined | - | ±10% | TBD | ⏳ |
| Disability | To be defined | - | ±10% | TBD | ⏳ |
| Language/Nationality | Critical for translation | - | ±10% | TBD | ⏳ |

**Bias Mitigation** (from Principle 7):
- [x] Bias assessment during design, before deployment, and ongoing - required
- [x] Training data to be audited for representation - required
- [x] Model outputs to be monitored for differential impact - required
- [ ] Third-party ethics review for high-risk applications - not yet arranged

**Findings**:
Principle 7 (Ethical AI and Bias Prevention) is marked as CRITICAL and requires comprehensive bias assessment. However, actual bias testing has not yet been conducted. Translation services are particularly sensitive as they serve non-English speakers (potential discrimination by language/nationality). The use of Azure managed models provides some baseline, but custom model training requires bias validation.

**Gaps**:
- **BLOCKING**: Bias audit not completed for translation services
- Fairness metrics not yet defined
- No third-party ethics review arranged
- Translation accuracy per language not yet validated

**Score**: 6/10

---

### 4. Accountability and Responsibility

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Clear ownership assigned (Chief Executive SRO, CDiO Programme Owner)
- [x] Decision-making process documented (RACI in stakeholder analysis)
- [x] Audit trail of all AI decisions required (FR-012, NFR-C-002)
- [x] Incident response procedures required (NFR-A-003)
- [x] Accountability for errors defined (human approver responsible)

**Accountability Structure**:
- **Senior Responsible Owner**: Chief Executive, SCTS - Strategic oversight
- **Programme Owner**: Chief Digital Information Officer - Day-to-day operation
- **Technical Lead**: Senior AI Technical Architect - Technical implementation
- **Ethics Lead**: To be assigned (gap)
- **Compliance Lead**: Legal Services Director + DPO

**Incident Response** (from NFR-A-003):
- [x] Process for reporting AI errors (to be documented)
- [x] Root cause analysis procedure (to be documented)
- [x] Corrective action tracking (to be documented)
- [x] Learning and improvement loop (FR-013)

**Findings**:
Accountability is well-structured through the stakeholder RACI and governance hierarchy. The Chief Executive is the Senior Responsible Owner with clear ministerial accountability to Cabinet Secretary. Audit trail requirements (FR-012, NFR-C-002) are comprehensive, capturing who, what, when, input, output, model version, and human decision. Human approvers are accountable for all AI outputs that affect records (FR-003, BR-003).

**Gaps**:
- Ethics Lead role not explicitly assigned
- Incident response procedures not yet documented in detail

**Score**: 8/10

---

### 5. Contestability and Redress

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Right to contest AI decisions enabled (human review always available)
- [x] Human review process for contested decisions (FR-003, FR-005)
- [x] Appeal mechanism through standard court processes
- [x] Redress process exists (human interpreter backup)
- [ ] Response times not explicitly defined

**Contestability Process**:
1. **How users can contest**: Request human interpreter, override AI classification
2. **Information required**: Flag issue via user interface (FR-005, FR-013)
3. **Review timeline**: Immediate for translation (human interpreter available)
4. **Human reviewer**: Court Clerk (classification), Human Interpreter (translation)
5. **Appeal if unsatisfied**: Court Administration Manager, standard complaints process
6. **Redress options**: Human processing, correction of errors, complaint resolution

**Testing**:
- [ ] Contestability process tested with real users - planned in UAT
- [ ] Response times meet targets - to be validated
- [ ] Users satisfied with process - to be validated

**Findings**:
Contestability is inherently strong due to the Human-in-the-Loop design. All AI outputs require human confirmation (FR-003), so users can always reject AI recommendations. Translation services explicitly require consent (FR-015) and provide human interpreter backup (BC-2). Court users can request human interpreters for any matter. Quality feedback mechanism (FR-013) allows users to flag issues.

**Gaps**:
- Response time targets for contestability not explicitly defined
- Contestability process not yet tested with users

**Score**: 8/10

---

### 6. Societal Wellbeing and Public Good

**Compliance Status**: [x] COMPLIANT / [ ] PARTIAL / [ ] NON-COMPLIANT

**Evidence**:
- [x] Positive societal impact assessment (improved access to justice - BR-002)
- [x] Environmental impact considered (cloud services efficiency)
- [x] Benefits distributed fairly (multilingual support for non-English speakers)
- [x] Negative impacts mitigated (job security commitment - BR-006)
- [x] Alignment with public values (justice-centred design - Principle 1)

**Societal Impact**:

| Impact | Positive/Negative | Magnitude | Mitigation/Enhancement |
|--------|-------------------|-----------|------------------------|
| Improved access to justice | Positive | HIGH | 10 languages, 20% access improvement target |
| Reduced interpreter delays | Positive | HIGH | 30% delay reduction target |
| Efficiency gains | Positive | HIGH | 60% processing time reduction |
| Job displacement concerns | Negative | MEDIUM | Explicit no redundancy commitment (BR-006) |
| Environmental (cloud compute) | Negative | LOW | Azure UK regions, efficient managed services |
| Staff workload | Positive | HIGH | Net workload reduction (BR-006) |
| Digital exclusion risk | Negative | LOW | Non-digital alternatives required (Principle 3) |

**Public Good**:
- [x] Solves real problem for citizens (access to justice for non-English speakers)
- [x] Accessible to all (WCAG 2.2 AA, multilingual, non-digital alternatives)
- [x] Maintains human dignity and autonomy (human-in-the-loop)
- [x] Strengthens democratic values (fair access to courts)

**Findings**:
The programme demonstrates strong alignment with public good. The explicit focus on improving access to justice for non-English speakers (BR-002) addresses a genuine societal need. The commitment to zero job losses (BR-006) addresses workforce concerns. Justice-centred design (Principle 1) ensures all AI serves the public mission. The programme supports Scottish Government AI Strategy commitment to responsible AI.

**Gaps**:
- Environmental impact not quantified (carbon footprint of AI processing)
- Long-term societal impact assessment not documented

**Score**: 9/10

---

## Overall Assessment Summary

### Compliance Scorecard

| Assessment Area | Score /10 | Status |
|-----------------|-----------|--------|
| **10 Core Principles** | | |
| 1. Understanding AI | 9 | ✅ |
| 2. Lawful and Ethical Use | 6 | ⚠️ |
| 3. Security | 8 | ✅ |
| 4. Human Control | 9 | ✅ |
| 5. Lifecycle Management | 8 | ✅ |
| 6. Right Tool Selection | 9 | ✅ |
| 7. Collaboration | 7 | ⚠️ |
| 8. Commercial Partnership | 8 | ✅ |
| 9. Skills and Expertise | 6 | ⚠️ |
| 10. Organizational Alignment | 9 | ✅ |
| **Principles Subtotal** | **79/100** | |
| | | |
| **6 Ethical Themes** | | |
| 1. Safety, Security, Robustness | 8 | ✅ |
| 2. Transparency, Explainability | 6 | ⚠️ |
| 3. Fairness, Bias, Discrimination | 6 | ⚠️ |
| 4. Accountability, Responsibility | 8 | ✅ |
| 5. Contestability, Redress | 8 | ✅ |
| 6. Societal Wellbeing, Public Good | 9 | ✅ |
| **Ethics Subtotal** | **45/60** | |
| | | |
| **TOTAL SCORE** | **126/160** | |

**Percentage Score**: 79%

### Compliance Levels

- [ ] **90-100%** (144-160 points): Excellent - Exemplary responsible AI
- [x] **75-89%** (120-143 points): Good - Compliant with minor improvements needed
- [ ] **60-74%** (96-119 points): Adequate - Significant gaps to address
- [ ] **< 60%** (< 96 points): Poor - Major compliance issues

### Risk-Based Decision

**For MEDIUM-RISK AI** (this programme):
- [x] SHOULD score ≥ 75% to proceed - **ACHIEVED (79%)**
- [x] Critical principles must be met (2, 3, 4) - **2 is PARTIAL (blocking issues)**
- [x] Human oversight required - **ACHIEVED**
- [ ] Annual audits - to be scheduled

### Critical Issues (Blocking)

1. **CRIT-01: DPIA Not Completed** (Principle 2)
   - **Impact**: Cannot deploy without DPIA for AI processing personal data
   - **Remediation**: DPO to complete DPIA before production deployment
   - **Target**: 2026-Q2 (before Phase 1 production)

2. **CRIT-02: ATRS Not Published** (Theme 2)
   - **Impact**: Mandatory for Scottish public body deploying algorithmic tools
   - **Remediation**: Publish ATRS entry on SCTS website
   - **Target**: 2026-Q2 (before production)

3. **CRIT-03: Bias Audit Not Completed** (Theme 3)
   - **Impact**: Translation services may discriminate by language/nationality
   - **Remediation**: Conduct fairness testing across all 10 languages
   - **Target**: 2026-Q2 (during PoC phase)

### Recommendations

#### High Priority (Address before deployment)

1. **Complete DPIA** for all AI capabilities processing personal data (DPO responsibility)
2. **Publish ATRS** entry on SCTS website documenting AI use
3. **Conduct Bias Audit** for translation services across all 10 priority languages
4. **Complete EqIA** and Human Rights Assessment
5. **Hire Senior AI Technical Architect** to address single-point-of-failure for AI expertise

#### Medium Priority (Address within 3 months of production)

6. **Develop staff training programme** on AI capabilities, limitations, and appropriate use
7. **Engage AI Standards Hub** for ethics guidance and community connection
8. **Document decommissioning plan** for AI model lifecycle
9. **Establish formal AI Governance Board** with defined terms of reference
10. **Arrange third-party ethics review** for translation services

#### Low Priority (Continuous improvement)

11. **Establish knowledge sharing mechanisms** with other government AI programmes
12. **Quantify environmental impact** (carbon footprint) of AI processing
13. **Consider academic partnerships** for ongoing bias research
14. **Publish case studies** post-deployment to contribute to government AI community

---

## Action Plan

| Action | Principle/Theme | Owner | Due Date | Status |
|--------|----------------|-------|----------|--------|
| Complete DPIA for Document Intelligence | P2, T3 | DPO | 2026-Q2 | 🔄 In Progress |
| Complete DPIA for Speech/Translation | P2, T3 | DPO | 2026-Q2 | ⏳ Planned |
| Publish ATRS entry | T2 | CDiO | 2026-Q2 | ⏳ Not Started |
| Conduct bias audit (translation) | T3 | AI Architect + Linguists | 2026-Q2 | ⏳ Not Started |
| Complete EqIA | P2 | Legal Services | 2026-Q1 | ⏳ Not Started |
| Human Rights Assessment | P2 | Legal Services | 2026-Q1 | ⏳ Not Started |
| Hire Senior AI Technical Architect | P9 | CDiO / HR | 2026-Q1 | 🔄 In Progress |
| Develop staff training programme | P1, P4 | HR / AI Architect | 2026-Q2 | ⏳ Planned |
| Establish AI Governance Board | P10 | Chief Executive | 2026-Q1 | ⏳ Not Started |
| Engage AI Standards Hub | P7 | CDiO | 2026-Q1 | ⏳ Not Started |

---

## Mandatory Documentation

### Required Assessments (attach or link)

- [ ] **ATRS** (Algorithmic Transparency Recording Standard): NOT YET PUBLISHED
- [ ] **DPIA** (Data Protection Impact Assessment): IN PROGRESS (DPO)
- [ ] **EqIA** (Equality Impact Assessment): NOT STARTED
- [ ] **Human Rights Assessment**: NOT STARTED
- [x] **Security Risk Assessment**: Requirements defined in NFR-SEC (full assessment pending)
- [ ] **Bias Audit Report**: NOT STARTED
- [ ] **User Research Report**: Planned for PoC phase

### Governance Approvals

- [ ] AI Governance Board approval: NOT YET CONSTITUTED
- [x] Senior Responsible Owner identified: Chief Executive
- [ ] Legal review: IN PROGRESS (Legal Services Director engaged)
- [ ] Security review: PLANNED (pre-production)
- [ ] Ethics review: NOT STARTED

---

## Go/No-Go Decision

**Decision**: [x] APPROVED WITH CONDITIONS / [ ] APPROVED / [ ] REJECTED

**Conditions for Approval**:

1. **CRIT-01**: Complete and approve DPIA before production deployment
2. **CRIT-02**: Publish ATRS before production deployment
3. **CRIT-03**: Complete bias audit for translation services before production deployment of translation capability
4. **EqIA**: Complete Equality Impact Assessment before production deployment
5. **Architect Hire**: Senior AI Technical Architect hired before PoC completion

**Deployment Approval**: [ ] Yes / [x] Conditional

**Ongoing Monitoring Required**:
- [x] Weekly performance reviews (first month after each capability launch)
- [x] Monthly bias audits (translation services)
- [x] Quarterly governance reviews
- [x] Annual comprehensive AI Playbook reassessment

---

## Sign-Off

**Assessed By**: ArcKit AI Governance Assessment
**Date**: 2026-01-17

**Senior Responsible Owner**:
Name: Chief Executive, SCTS
Date: ________________
Signature: ________________

**Programme Owner**:
Name: Chief Digital Information Officer, SCTS
Date: ________________
Signature: ________________

---

## Review Schedule

**Next Review**: 2026-04-17 (Quarterly)
**Review Frequency**:
- [ ] Monthly (high-risk)
- [x] Quarterly (medium-risk)
- [ ] Annually (low-risk)

**Trigger for Earlier Review**:
- Any AI-related incident affecting court users or records
- Significant change to AI capabilities or scope
- Regulatory guidance changes (AI Playbook updates)
- DPIA/EqIA findings requiring remediation

---

## Appendix: Traceability to ArcKit Artifacts

### Link to Requirements (requirements.md)

| AI Playbook Principle | Requirements Traceability |
|----------------------|---------------------------|
| P2 (Lawful) | NFR-C-001 (UK GDPR), NFR-C-003 (Scottish Gov Standards) |
| P3 (Security) | NFR-SEC-001 to NFR-SEC-006 |
| P4 (Human Control) | FR-003 (Human Review), BR-003 (Court Records) |
| Theme 3 (Fairness) | Principle 7 (Ethical AI), BR-002 (Multilingual) |
| Theme 2 (Transparency) | FR-011 (AI Labelling), Principle 8 (Transparency) |

### Link to Architecture Principles (architecture-principles.md)

| AI Playbook Principle | SCTS Architecture Principle |
|----------------------|-----------------------------|
| P1 (Understanding AI) | Principle 8 (AI Transparency) |
| P2 (Lawful) | Principle 12 (Data Protection), Principle 13 (Standards) |
| P3 (Security) | Principle 11 (Security by Design) |
| P4 (Human Control) | Principle 2 (Human-in-the-Loop) |
| P5 (Lifecycle) | Principle 9 (Model Governance), Principle 19 (Iterative) |
| Theme 3 (Fairness) | Principle 7 (Ethical AI and Bias Prevention) |

---

**Generated by**: ArcKit `/arckit.ai-playbook` command
**Generated on**: 2026-01-17 GMT
**ArcKit Version**: 0.6.0
**Project**: SCTS GenAI Programme (Project 001)
**AI Model**: Claude Opus 4.5
