# SCTS GenAI Programme

**Project ID:** 001
**Created:** 2026-01-17
**Status:** Alpha Phase Complete
**Governance Score:** 82/100 (Grade B)

## Overview

The Scottish Courts and Tribunals Service (SCTS) GenAI Programme is a transformative initiative to enhance court operations through responsible AI deployment. The programme introduces:

- **Document Intelligence** - AI-powered document classification and entity extraction
- **Speech Services** - Real-time transcription with speaker diarisation
- **Translation Services** - Multilingual support for 10 priority languages
- **Cognitive Search** - Semantic search across court documents

**Key Design Principles:**
- Human-in-the-loop for all consequential decisions
- AI augments but never replaces judicial decision-making
- UK data residency (Azure UK South/West)
- Zero modifications to court records by AI

**Technology Platform:** Microsoft Azure AI Services (via G-Cloud)
**3-Year TCO:** £716K

## Project Artifacts

### Foundation & Governance
| Artifact | Description | Status |
|----------|-------------|--------|
| [stakeholder-drivers.md](projects/001-scts-genai-programme/stakeholder-drivers.md) | 13 stakeholders, 6 goals, 5 outcomes | ✅ Complete |
| [risk-register.md](projects/001-scts-genai-programme/risk-register.md) | 20 risks, Orange Book compliant | ✅ Complete |
| [security-risk-register.md](projects/001-scts-genai-programme/security-risk-register.md) | 15 security risks, NCSC CAF aligned | ✅ Complete |
| [principles-compliance-assessment-2026-01-20.md](projects/001-scts-genai-programme/principles-compliance-assessment-2026-01-20.md) | 20 principles assessed (12 GREEN, 7 AMBER) | ✅ Complete |

### Requirements & Data
| Artifact | Description | Status |
|----------|-------------|--------|
| [requirements.md](projects/001-scts-genai-programme/requirements.md) | 49 requirements (6 BR, 15 FR, 22 NFR, 6 INT) | ✅ Complete |
| [data-model.md](projects/001-scts-genai-programme/data-model.md) | 9 entities, 67 attributes, GDPR compliant | ✅ Complete |
| [traceability-matrix.md](projects/001-scts-genai-programme/traceability-matrix.md) | Requirements to design traceability (72%) | ✅ Complete |

### Research & Decisions
| Artifact | Description | Status |
|----------|-------------|--------|
| [research-findings.md](projects/001-scts-genai-programme/research-findings.md) | Build vs Buy analysis, Azure AI recommended | ✅ Complete |
| [ADR-001-azure-ai-platform-selection.md](projects/001-scts-genai-programme/decisions/ADR-001-azure-ai-platform-selection.md) | Azure AI platform decision | ✅ Complete |

### Design & Delivery
| Artifact | Description | Status |
|----------|-------------|--------|
| [high-level-design.md](projects/001-scts-genai-programme/high-level-design.md) | C4 architecture, microservices on AKS | ✅ Complete |
| [devops-strategy.md](projects/001-scts-genai-programme/devops-strategy.md) | CI/CD, IaC, GitOps, DevSecOps | ✅ Complete |
| [mlops-strategy.md](projects/001-scts-genai-programme/mlops-strategy.md) | ML lifecycle, model monitoring, responsible AI | ✅ Complete |
| [operational-readiness.md](projects/001-scts-genai-programme/operational-readiness.md) | SRE runbooks, DR/BCP, support model | ✅ Complete |
| [project-plan.md](projects/001-scts-genai-programme/project-plan.md) | 18-month roadmap, 6 phases | ✅ Complete |
| [backlog.md](projects/001-scts-genai-programme/backlog.md) | 184 user stories, 22 sprints | ✅ Complete |

### Compliance & Privacy
| Artifact | Description | Status |
|----------|-------------|--------|
| [dpia.md](projects/001-scts-genai-programme/dpia.md) | DPIA - MEDIUM residual risk | ✅ Complete |
| [atrs-record.md](projects/001-scts-genai-programme/atrs-record.md) | Algorithmic transparency (Tier 1 & 2) | ✅ Complete |
| [ai-playbook-assessment.md](projects/001-scts-genai-programme/ai-playbook-assessment.md) | UK AI Playbook - 79%, approved with conditions | ✅ Complete |
| [secure-by-design-assessment.md](projects/001-scts-genai-programme/secure-by-design-assessment.md) | NCSC CAF - 10/14 principles | ✅ Complete |
| [tcop-review.md](projects/001-scts-genai-programme/tcop-review.md) | Technology Code of Practice - 11/13 points | ✅ Complete |

### Analysis & Reporting
| Artifact | Description | Status |
|----------|-------------|--------|
| [analysis-report.md](projects/001-scts-genai-programme/analysis-report.md) | Governance analysis - 82/100, Grade B | ✅ Complete |
| [PROJECT-STORY.md](projects/001-scts-genai-programme/PROJECT-STORY.md) | Comprehensive project narrative | ✅ Complete |
| [CLIENT-EMAIL-ARTIFACT-OVERVIEW.md](projects/001-scts-genai-programme/CLIENT-EMAIL-ARTIFACT-OVERVIEW.md) | Client communication - all artifacts explained | ✅ Complete |
| [CLIENT-ARTIFACT-SUMMARY-TABLE.md](projects/001-scts-genai-programme/CLIENT-ARTIFACT-SUMMARY-TABLE.md) | Executive summary tables | ✅ Complete |

## Project Structure

```
projects/001-scts-genai-programme/
├── stakeholder-drivers.md                 # Stakeholder analysis
├── requirements.md                        # Business & technical requirements
├── research-findings.md                   # Technology research
├── data-model.md                          # Data entities & GDPR
├── dpia.md                                # Data Protection Impact Assessment
├── atrs-record.md                         # Algorithmic Transparency Record
├── risk-register.md                       # Risk management (Orange Book)
├── security-risk-register.md              # Security risks (NCSC CAF)
├── secure-by-design-assessment.md         # NCSC CAF security assessment
├── ai-playbook-assessment.md              # UK AI Playbook compliance
├── tcop-review.md                         # Technology Code of Practice review
├── high-level-design.md                   # Solution architecture (C4)
├── mlops-strategy.md                      # ML operations strategy
├── operational-readiness.md               # Operational readiness pack
├── project-plan.md                        # Delivery roadmap
├── backlog.md                             # Sprint backlog
├── traceability-matrix.md                 # Requirements traceability
├── analysis-report.md                     # Governance analysis
├── principles-compliance-assessment-*.md  # Architecture principles compliance
├── PROJECT-STORY.md                       # Complete project narrative
├── CLIENT-EMAIL-ARTIFACT-OVERVIEW.md      # Client communication
├── CLIENT-ARTIFACT-SUMMARY-TABLE.md       # Executive summary
└── decisions/
    └── ADR-001-azure-ai-platform-selection.md  # Architecture decisions
```

## Status

### Discovery Phase ✅
- [x] Stakeholder analysis complete (13 stakeholders, 6 goals)
- [x] Risk register created (20 risks, 37% score reduction)
- [x] Architecture principles established (20 principles)

### Alpha Phase ✅
- [x] Requirements defined (49 requirements)
- [x] Data model designed (9 entities, GDPR compliant)
- [x] Technology research complete (Azure AI selected)
- [x] DPIA completed (MEDIUM residual risk)
- [x] AI Playbook assessment (79%, approved with conditions)
- [x] Secure by Design assessment (NCSC CAF 10/14)
- [x] ATRS record created (Tier 1 & 2)

### Beta Phase (In Progress)
- [x] High-Level Design complete
- [ ] Detailed Design (DLD) - pending
- [x] Traceability matrix validated (72% coverage)
- [ ] Penetration testing - pending
- [ ] Bias audit for 10 languages - pending

### Pre-Production (Planned)
- [ ] DPIA approval from DPO/SIRO
- [ ] Penetration testing complete
- [ ] SIEM implementation
- [ ] Staff training programme

### Live Phase (Planned)
- [ ] PoC deployment (Q2 2026)
- [ ] Pilot rollout (Q3 2026)
- [ ] Production deployment (Q4 2026)

## Key Metrics

| Metric | Value |
|--------|-------|
| **Governance Score** | 82/100 (Grade B) |
| **Principles Compliance** | 60% GREEN, 35% AMBER |
| **Requirements Coverage** | 100% to HLD |
| **Traceability Score** | 72% |
| **AI Playbook Score** | 79% |
| **NCSC CAF Score** | 10/14 principles |
| **Risk Reduction** | 37% (inherent to residual) |

## Critical Actions Required

Before production deployment:

1. **DPIA Approval** - Obtain DPO and SIRO sign-off
2. **Bias Audit** - Complete testing for 10 translation languages
3. **Penetration Testing** - Execute security validation
4. **EqIA** - Complete Equality Impact Assessment
5. **SIEM** - Implement security monitoring

## Timeline

| Phase | Duration | Target |
|-------|----------|--------|
| Discovery & Foundation | 2 months | Feb 2026 |
| Document Intelligence MVP | 4 months | Jun 2026 |
| Speech & Translation | 4 months | Oct 2026 |
| Cognitive Search | 3 months | Jan 2027 |
| Integration & Hardening | 3 months | Apr 2027 |
| Go-Live & Transition | 2 months | Jul 2027 |

## Contact

- **Programme Owner:** Chief Digital Information Officer, SCTS
- **Technical Lead:** Senior AI Technical Architect
- **DPO:** Data Protection Officer, SCTS

---

*Generated using the ArcKit Architecture Governance Framework*
