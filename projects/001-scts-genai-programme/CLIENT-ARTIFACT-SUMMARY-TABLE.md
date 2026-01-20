# SCTS GenAI Programme - Governance Artifacts Summary

**To:** SCTS Digital Leadership Team | **Date:** 20 January 2026 | **Subject:** Complete Governance Documentation Package

---

## Document Overview

| # | Category | Document | File | Purpose | Key Metrics |
|---|----------|----------|------|---------|-------------|
| 1 | Foundation | **Architecture Principles** | `.arckit/memory/architecture-principles.md` | Establishes governance principles guiding all decisions | 20 principles across 6 categories |
| 2 | Foundation | **Stakeholder Drivers** | `stakeholder-drivers.md` | Identifies who we're building for and their needs | 13 stakeholders, 6 goals, 5 outcomes |
| 3 | Requirements | **Requirements Specification** | `requirements.md` | Defines what the system must do | 49 requirements (6 BR, 15 FR, 22 NFR, 6 INT) |
| 4 | Research | **Research Findings** | `research-findings.md` | Technology evaluation and build vs buy analysis | Azure AI recommended, £716K 3-year TCO |
| 5 | Research | **ADR-001: Azure Platform** | `decisions/ADR-001-azure-ai-platform-selection.md` | Formal architecture decision record | Status: PROPOSED |
| 6 | Data | **Data Model** | `data-model.md` | Defines data entities and GDPR compliance | 9 entities, 67 attributes, 15 PII fields |
| 7 | Data | **DPIA** | `dpia.md` | Data Protection Impact Assessment (UK GDPR Art 35) | MEDIUM residual risk, ICO consultation not required |
| 8 | Data | **ATRS Record** | `atrs-record.md` | Algorithmic transparency for GOV.UK publication | Tier 1 & Tier 2 complete |
| 9 | Risk | **Risk Register** | `risk-register.md` | HM Treasury Orange Book risk management | 20 risks, 37% score reduction after mitigations |
| 10 | Security | **Secure by Design** | `secure-by-design-assessment.md` | NCSC Cyber Assessment Framework evaluation | 10/14 CAF principles achieved |
| 11 | Compliance | **AI Playbook Assessment** | `ai-playbook-assessment.md` | UK Government AI Playbook compliance | 79% score, APPROVED WITH CONDITIONS |
| 12 | Design | **High-Level Design** | `high-level-design.md` | Solution architecture with C4 diagrams | Microservices on AKS, 100% requirements coverage |
| 13 | Delivery | **Project Plan** | `project-plan.md` | Delivery roadmap and milestones | 18 months, 6 phases, 5 milestones |
| 14 | Delivery | **Product Backlog** | `backlog.md` | User stories organised into sprints | 184 stories, 22 sprints |
| 15 | Governance | **Traceability Matrix** | `traceability-matrix.md` | End-to-end requirements traceability | 72% score, 100% HLD coverage |
| 16 | Governance | **Analysis Report** | `analysis-report.md` | Independent governance quality assessment | 82/100 (Grade B) |
| 17 | Governance | **Project Story** | `PROJECT-STORY.md` | Comprehensive project narrative | 9 chapters, full timeline |

---

## Compliance Scorecard

| Framework | Score | Status | Key Gaps |
|-----------|-------|--------|----------|
| UK AI Playbook | 79% | ⚠️ Approved with Conditions | EqIA, Bias audit pending |
| NCSC CAF (Security) | 71% | ⚠️ Partial | Pen testing, SIEM pending |
| UK GDPR | 90% | ⚠️ Partial | DPIA approval pending |
| ATRS | 75% | ⚠️ Draft | GOV.UK publication pending |
| Technology Code of Practice | ~85% | ⚠️ Partial | Open source documentation |
| **Overall Governance** | **82/100** | **Grade B** | Address critical issues |

---

## Risk Summary

| Risk ID | Description | Inherent | Residual | Appetite | Status |
|---------|-------------|----------|----------|----------|--------|
| R-001 | Judicial confidence loss | 20 | 15 | 12 | ⚠️ Exceeds |
| R-004 | AI quality damages reputation | 20 | 16 | 12 | ⚠️ Exceeds |
| R-007 | Security breach of court data | 20 | 15 | 12 | ⚠️ Exceeds |
| R-010 | UK GDPR non-compliance | 20 | 15 | 12 | ⚠️ Exceeds |
| Others | 16 additional risks | Various | Various | Various | ✅ Within appetite |

**Total Risk Score:** 267 (inherent) → 168 (residual) = **37% improvement**

---

## Requirements Coverage

| Requirement Type | Count | Priority Breakdown | HLD Coverage | Test Coverage |
|------------------|-------|-------------------|--------------|---------------|
| Business (BR) | 6 | 4 Critical, 2 High | ✅ 100% | ❌ 0% |
| Functional (FR) | 15 | 10 Critical, 4 High, 1 Could | ✅ 100% | ❌ 0% |
| Non-Functional (NFR) | 22 | 12 Critical, 8 High, 2 Could | ✅ 100% | ❌ 0% |
| Integration (INT) | 6 | 4 Critical, 2 High | ✅ 100% | ❌ 0% |
| **Total** | **49** | **30 Critical, 16 High, 3 Could** | **100%** | **0%** |

---

## Delivery Summary

| Metric | Value |
|--------|-------|
| Total Duration | 18 months (Jan 2026 - Jul 2027) |
| Delivery Phases | 6 phases |
| User Stories | 184 |
| Sprints | 22 (2-week sprints) |
| Sprint Velocity | ~8 stories/sprint |
| Priority Split | 53% Must, 30% Should, 16% Could |

### Phase Timeline

| Phase | Duration | Deliverable | Target |
|-------|----------|-------------|--------|
| 1. Discovery & Foundation | 2 months | Foundation complete | Feb 2026 |
| 2. Document Intelligence MVP | 4 months | Doc processing live | Jun 2026 |
| 3. Speech & Translation | 4 months | Translation live | Oct 2026 |
| 4. Cognitive Search | 3 months | Search live | Jan 2027 |
| 5. Integration & Hardening | 3 months | Full integration | Apr 2027 |
| 6. Go-Live & Transition | 2 months | Platform live | Jul 2027 |

---

## Actions Required

### Critical (Must resolve before production)

| # | Action | Owner | Target |
|---|--------|-------|--------|
| 1 | Obtain DPIA approval from DPO and SIRO | DPO | Q1 2026 |
| 2 | Complete Equality Impact Assessment (EqIA) for translation | Legal Services | Q1 2026 |
| 3 | Conduct bias audit for 10 priority languages | AI Architect | Q2 2026 |

### High Priority

| # | Action | Owner | Target |
|---|--------|-------|--------|
| 4 | Escalate 4 appetite-exceeding risks to Steering Committee | CDiO | Immediate |
| 5 | Complete penetration testing | Security Team | Q2 2026 |
| 6 | Implement SIEM security monitoring | ICT Operations | Q2 2026 |
| 7 | Create test plan (~290 test cases) | QA Lead | Q2 2026 |
| 8 | Obtain SIRO sign-off on residual risks | CDiO | Q1 2026 |

### Medium Priority

| # | Action | Owner | Target |
|---|--------|-------|--------|
| 9 | Publish ATRS record to GOV.UK | CDiO | Before go-live |
| 10 | Create additional ADRs (data, security, integration) | AI Architect | Q1 2026 |
| 11 | Create Detailed Design (DLD) document | AI Architect | Q1 2026 |

---

## Document Location

```
projects/001-scts-genai-programme/
├── stakeholder-drivers.md          # Stakeholder analysis
├── requirements.md                 # All requirements
├── research-findings.md            # Technology research
├── data-model.md                   # Data entities & GDPR
├── dpia.md                         # Privacy impact assessment
├── atrs-record.md                  # Algorithmic transparency
├── risk-register.md                # Risk management
├── secure-by-design-assessment.md  # Security assessment
├── ai-playbook-assessment.md       # AI compliance
├── high-level-design.md            # Solution architecture
├── project-plan.md                 # Delivery roadmap
├── backlog.md                      # User stories & sprints
├── traceability-matrix.md          # Requirements traceability
├── analysis-report.md              # Governance analysis
├── PROJECT-STORY.md                # Complete narrative
└── decisions/
    └── ADR-001-azure-ai-platform-selection.md

.arckit/memory/
└── architecture-principles.md      # Foundation principles
```

---

**Contact:** Enterprise Architecture Team | **Generated:** 20 January 2026 | **ArcKit Version:** 0.6.0
