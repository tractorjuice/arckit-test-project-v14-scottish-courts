# Wardley Map: SCTS GenAI Programme - Current State & Procurement Strategy

## Document Information

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-WARD-v1.0 |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Document Type** | Strategic Wardley Map |
| **Classification** | OFFICIAL |
| **Version** | 1.0 |
| **Status** | DRAFT |
| **Date** | 2026-01-21 |
| **Owner** | Chief Digital Information Officer, SCTS |

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-01-21 | ArcKit AI | Initial creation from `/arckit.wardley` command |

---

## Executive Summary

This Wardley Map provides strategic situational awareness for the SCTS GenAI Programme, mapping all components from user needs to infrastructure. The analysis supports build vs buy decisions, UK Government procurement strategy via G-Cloud, and identifies areas of competitive advantage versus commodity consumption.

### Key Strategic Insights

1. **User-Facing AI Capabilities are Custom** (0.35-0.45): Document classification, translation workflows, and search interfaces require custom development to meet Scottish court-specific requirements
2. **AI Services are Products** (0.65-0.75): Azure AI services (Document Intelligence, Speech, Translator, Search) are mature products - **BUY via G-Cloud**
3. **Cloud Infrastructure is Commodity** (0.85-0.95): AKS, storage, networking - **use utility services via G-Cloud**
4. **Human-in-the-Loop is Non-Negotiable**: Custom component required for Principle 2 compliance - **BUILD**
5. **Court Records Integrity is Sacrosanct**: Read-only AI access architecture is custom - **BUILD**

### Procurement Strategy Summary

| Approach | Components | 3-Year TCO | Route |
|----------|-----------|------------|-------|
| **BUILD** | 6 Custom components | £180,000 | In-house/DOS Outcomes |
| **BUY** | 4 AI Services | £485,000 | G-Cloud (Azure) |
| **RENT** | 8 Infrastructure | £384,000 | G-Cloud (Azure) |
| **REUSE** | 2 Cross-Gov services | £0 | Existing contracts |
| **TOTAL** | 20 components | **£1,049,000** | |

---

## Map Visualization

**View this map**: Paste the code below into [https://create.wardleymaps.ai](https://create.wardleymaps.ai)

```wardley
title SCTS GenAI Programme - Strategic Map

anchor Court User [0.97, 0.25]

annotation 1 [0.42, 0.42] BUILD - Human oversight mandatory (Principle 2)
annotation 2 [0.65, 0.72] BUY - Azure AI Services via G-Cloud
annotation 3 [0.25, 0.92] RENT - Commodity cloud via G-Cloud
annotation 4 [0.88, 0.25] Scottish Courts specific user needs

note Court operations must continue if AI unavailable (Principle 5) [0.78, 0.15]

component Court User [0.97, 0.25]
component Access to Justice [0.94, 0.28]
component Efficient Court Operations [0.91, 0.32]

component Document Processing Workflow [0.85, 0.38]
component Translation Service [0.82, 0.35]
component Court Search Portal [0.80, 0.42]

component Human Review Interface [0.75, 0.45]
component AI Classification Display [0.72, 0.48]
component Confidence Scoring [0.70, 0.52]
component Manual Fallback Mode [0.68, 0.42]

component Document Intelligence Service [0.62, 0.68]
component Speech Transcription Service [0.60, 0.65]
component Translation Engine [0.58, 0.70]
component Cognitive Search Service [0.56, 0.72]

component Audit Trail Service [0.52, 0.55]
component Court Records Gateway [0.50, 0.48]
component Consent Management [0.48, 0.45]

component Azure AI Document Intelligence [0.45, 0.75]
component Azure Speech Services [0.43, 0.72]
component Azure Translator [0.41, 0.78]
component Azure AI Search [0.39, 0.75]
component Azure OpenAI Service [0.37, 0.68]

component Case Management API [0.32, 0.58]
component Document Management API [0.30, 0.55]
component SCTS Identity Provider [0.28, 0.62]

component Azure Kubernetes Service [0.22, 0.92]
component Azure SQL Database [0.20, 0.90]
component Azure Blob Storage [0.18, 0.95]
component Azure Key Vault [0.16, 0.92]
component Azure Monitor [0.14, 0.88]
component Azure Private Endpoints [0.12, 0.85]

Court User -> Access to Justice
Court User -> Efficient Court Operations
Access to Justice -> Translation Service
Access to Justice -> Court Search Portal
Efficient Court Operations -> Document Processing Workflow

Document Processing Workflow -> Human Review Interface
Document Processing Workflow -> AI Classification Display
Document Processing Workflow -> Manual Fallback Mode
Translation Service -> Speech Transcription Service
Translation Service -> Translation Engine
Translation Service -> Consent Management
Court Search Portal -> Cognitive Search Service

Human Review Interface -> Confidence Scoring
AI Classification Display -> Document Intelligence Service
Confidence Scoring -> Document Intelligence Service

Document Intelligence Service -> Azure AI Document Intelligence
Speech Transcription Service -> Azure Speech Services
Translation Engine -> Azure Translator
Cognitive Search Service -> Azure AI Search
Document Intelligence Service -> Azure OpenAI Service

Azure AI Document Intelligence -> Azure Kubernetes Service
Azure Speech Services -> Azure Kubernetes Service
Azure Translator -> Azure Kubernetes Service
Azure AI Search -> Azure Kubernetes Service
Azure OpenAI Service -> Azure Kubernetes Service

Audit Trail Service -> Azure SQL Database
Court Records Gateway -> Case Management API
Court Records Gateway -> Document Management API
Human Review Interface -> SCTS Identity Provider

Azure Kubernetes Service -> Azure Blob Storage
Azure Kubernetes Service -> Azure Key Vault
Azure Kubernetes Service -> Azure Monitor
Azure Kubernetes Service -> Azure Private Endpoints

pipeline Document Intelligence Service [0.62, 0.45, 0.75]
pipeline Translation Engine [0.58, 0.42, 0.78]

evolve Azure AI Document Intelligence 0.82 label Commoditizing
evolve Azure Speech Services 0.80 label Commoditizing
evolve Human Review Interface 0.55 label Standardizing

style wardley
```

---

## Evolution Stages Reference

| Stage | Range | Characteristics | SCTS Strategic Action |
|-------|-------|-----------------|----------------------|
| **Genesis** | 0.00-0.25 | Novel, uncertain, rapidly changing | Build only if court-specific innovation |
| **Custom** | 0.25-0.50 | Bespoke, competitive advantage | Build for Scottish legal workflows |
| **Product** | 0.50-0.75 | Products with differentiation | Buy Azure AI via G-Cloud |
| **Commodity** | 0.75-1.00 | Utility, standardized | Rent cloud via G-Cloud |

---

## Component Inventory

### User Needs (Visibility 0.90-1.00)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Court User | 0.97 | 0.25 | Genesis | Court users (clerks, public, legal professionals) | Diverse user base with accessibility needs |
| Access to Justice | 0.94 | 0.28 | Custom | Improved access for non-English speakers | BR-002: Multilingual support, Scottish court context |
| Efficient Court Operations | 0.91 | 0.32 | Custom | Reduced document processing time | BR-001: 60% efficiency improvement target |

### User-Facing Capabilities (Visibility 0.75-0.90)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Document Processing Workflow | 0.85 | 0.38 | Custom | End-to-end document classification workflow | UC-1: Custom workflow for Scottish court documents |
| Translation Service | 0.82 | 0.35 | Custom | Real-time translation in court proceedings | UC-2: Court-specific consent and fallback flows |
| Court Search Portal | 0.80 | 0.42 | Custom | Semantic search for legal professionals | UC-3: Scottish case law and citation context |
| Human Review Interface | 0.75 | 0.45 | Custom | Interface for human override of AI decisions | **BUILD**: FR-003, Principle 2 (Human-in-the-Loop) |

### AI Coordination Layer (Visibility 0.60-0.75)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| AI Classification Display | 0.72 | 0.48 | Custom | Presents AI classification with confidence | FR-011: AI output labelling requirement |
| Confidence Scoring | 0.70 | 0.52 | Product | Displays confidence for human review | Standard pattern, buy as part of AI service |
| Manual Fallback Mode | 0.68 | 0.42 | Custom | Graceful degradation when AI unavailable | **BUILD**: FR-014, Principle 5 critical |
| Document Intelligence Service | 0.62 | 0.68 | Product | Custom service wrapping Azure AI | Integration layer, moderate customization |
| Speech Transcription Service | 0.60 | 0.65 | Product | Custom service wrapping Azure Speech | Integration layer, language configuration |
| Translation Engine | 0.58 | 0.70 | Product | Custom service wrapping Azure Translator | Legal terminology customization |
| Cognitive Search Service | 0.56 | 0.72 | Product | Custom service wrapping Azure AI Search | Scottish case law vector embeddings |

### Governance & Compliance Layer (Visibility 0.48-0.55)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Audit Trail Service | 0.52 | 0.55 | Product | Comprehensive AI operation logging | **BUILD**: FR-012, NFR-C-002 (7-year retention) |
| Court Records Gateway | 0.50 | 0.48 | Custom | Read-only access to court records | **BUILD**: NFR-SEC-006, Principle 14 critical |
| Consent Management | 0.48 | 0.45 | Custom | Translation consent workflow | **BUILD**: FR-015, GDPR requirement |

### AI Platform Services (Visibility 0.35-0.45)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Azure AI Document Intelligence | 0.45 | 0.75 | Product→Commodity | Microsoft document AI service | **BUY**: G-Cloud, UK data centres |
| Azure Speech Services | 0.43 | 0.72 | Product | Microsoft speech-to-text | **BUY**: G-Cloud, 10+ languages supported |
| Azure Translator | 0.41 | 0.78 | Commodity | Microsoft translation service | **BUY**: G-Cloud, legal terminology training |
| Azure AI Search | 0.39 | 0.75 | Product→Commodity | Microsoft cognitive search | **BUY**: G-Cloud, vector search included |
| Azure OpenAI Service | 0.37 | 0.68 | Product | GPT models for summarization | **BUY**: G-Cloud, UK data residency |

### Integration Layer (Visibility 0.28-0.35)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Case Management API | 0.32 | 0.58 | Product | SCTS existing system API | Existing, INT-001 integration |
| Document Management API | 0.30 | 0.55 | Product | SCTS DMS API | Existing, INT-002 integration |
| SCTS Identity Provider | 0.28 | 0.62 | Product | Azure AD / SCTS IdP | Existing, INT-003 integration |

### Cloud Infrastructure (Visibility 0.10-0.25)

| Component | Visibility | Evolution | Stage | Description | Strategic Notes |
|-----------|-----------|-----------|-------|-------------|-----------------|
| Azure Kubernetes Service | 0.22 | 0.92 | Commodity | Container orchestration | **RENT**: G-Cloud, UK South/West |
| Azure SQL Database | 0.20 | 0.90 | Commodity | Managed SQL database | **RENT**: G-Cloud, audit trail storage |
| Azure Blob Storage | 0.18 | 0.95 | Commodity | Object storage | **RENT**: G-Cloud, document storage |
| Azure Key Vault | 0.16 | 0.92 | Commodity | Secrets management | **RENT**: G-Cloud, encryption keys |
| Azure Monitor | 0.14 | 0.88 | Commodity | Observability platform | **RENT**: G-Cloud, NFR-M-001 |
| Azure Private Endpoints | 0.12 | 0.85 | Commodity | Network security | **RENT**: G-Cloud, NFR-SEC-003 |

---

## Evolution Analysis

### Components in Genesis (0.00-0.25)

**Novel, unproven, high uncertainty**

| Component | Position | Risk | Opportunity | Action |
|-----------|----------|------|-------------|--------|
| Court User (as anchor) | 0.25 | Low | High | User research to understand court-specific needs |

**Strategic Recommendations**:
- User needs are well understood through stakeholder analysis
- No true Genesis components in this map - AI services are mature
- Innovation focused on Scottish legal context, not technology R&D

### Components in Custom (0.25-0.50)

**Emerging practices, competitive advantage for SCTS**

| Component | Position | Competitive Advantage? | Action |
|-----------|----------|------------------------|--------|
| Access to Justice | 0.28 | Yes - Scottish courts context | BUILD workflow customization |
| Efficient Court Operations | 0.32 | Yes - court document types | BUILD classification training |
| Document Processing Workflow | 0.38 | Yes - Scottish legal workflow | BUILD custom workflow |
| Translation Service | 0.35 | Yes - court consent model | BUILD consent + fallback |
| Court Search Portal | 0.42 | Yes - Scottish case law | BUILD search customization |
| Human Review Interface | 0.45 | Yes - Principle 2 compliance | **BUILD** - mandatory |
| Manual Fallback Mode | 0.42 | Yes - Principle 5 compliance | **BUILD** - mandatory |
| AI Classification Display | 0.48 | Moderate - FR-011 labelling | BUILD UI component |
| Court Records Gateway | 0.48 | Yes - Principle 14 critical | **BUILD** - mandatory |
| Consent Management | 0.45 | Yes - GDPR specific | BUILD consent workflow |

**Strategic Recommendations**:
- **BUILD** these components - they provide Scottish court-specific value
- Human Review Interface and Court Records Gateway are **non-negotiable** builds
- Consider DOS Outcomes framework for discovery and build phases
- Invest in UX design for Human Review Interface (critical for adoption)

### Components in Product (0.50-0.75)

**Maturing market, feature differentiation**

| Component | Position | Market Options | Action |
|-----------|----------|----------------|--------|
| Confidence Scoring | 0.52 | Built into Azure AI | BUY as part of service |
| Audit Trail Service | 0.55 | Custom + Azure SQL | BUILD with Azure storage |
| Case Management API | 0.58 | SCTS existing | REUSE existing |
| Document Management API | 0.55 | SCTS existing | REUSE existing |
| SCTS Identity Provider | 0.62 | Azure AD | REUSE existing |
| Document Intelligence Service | 0.68 | Azure, AWS, Google | BUY Azure (G-Cloud) |
| Speech Transcription Service | 0.65 | Azure, AWS, Google, Whisper | BUY Azure (G-Cloud) |
| Azure OpenAI Service | 0.68 | Azure OpenAI, AWS Bedrock | BUY Azure (G-Cloud) |
| Translation Engine | 0.70 | Azure, DeepL, Google | BUY Azure (G-Cloud) |
| Cognitive Search Service | 0.72 | Azure, Elastic, Algolia | BUY Azure (G-Cloud) |

**Strategic Recommendations**:
- **BUY** AI services from Azure via G-Cloud - TC-2 constraint mandates Azure
- Azure AI services are well-positioned (UK data centres, G-Cloud approved)
- Standardize on Azure ecosystem for integrated monitoring and management
- Use G-Cloud framework for straightforward procurement

### Components in Commodity (0.75-1.00)

**Industrialized, utility services**

| Component | Position | Provider | Action |
|-----------|----------|----------|--------|
| Azure AI Document Intelligence | 0.75 | Microsoft Azure | RENT via G-Cloud |
| Azure Translator | 0.78 | Microsoft Azure | RENT via G-Cloud |
| Azure AI Search | 0.75 | Microsoft Azure | RENT via G-Cloud |
| Azure Private Endpoints | 0.85 | Microsoft Azure | RENT via G-Cloud |
| Azure Monitor | 0.88 | Microsoft Azure | RENT via G-Cloud |
| Azure SQL Database | 0.90 | Microsoft Azure | RENT via G-Cloud |
| Azure Kubernetes Service | 0.92 | Microsoft Azure | RENT via G-Cloud |
| Azure Key Vault | 0.92 | Microsoft Azure | RENT via G-Cloud |
| Azure Blob Storage | 0.95 | Microsoft Azure | RENT via G-Cloud |

**Strategic Recommendations**:
- **RENT** all commodity services via G-Cloud
- Focus on cost efficiency, not feature differentiation
- Use Azure consumption-based pricing with Savings Plans
- No custom development - use out-of-box functionality

---

## Build vs Buy Analysis

### BUILD (In-House Development via DOS Outcomes)

**Candidates for Building**:

| Component | Evolution | Rationale | Risk | Investment |
|-----------|-----------|-----------|------|------------|
| Human Review Interface | 0.45 | **Principle 2 mandatory** - human-in-the-loop | Low | £30,000 |
| Court Records Gateway | 0.48 | **Principle 14 mandatory** - read-only access | Low | £25,000 |
| Manual Fallback Mode | 0.42 | **Principle 5 mandatory** - graceful degradation | Low | £20,000 |
| Consent Management | 0.45 | GDPR/FR-015 specific workflow | Medium | £15,000 |
| Document Processing Workflow | 0.38 | Scottish court document types | Medium | £40,000 |
| Audit Trail Service | 0.55 | 7-year retention, immutable | Low | £25,000 |
| AI Classification Display | 0.48 | FR-011 AI labelling UX | Low | £15,000 |
| Translation Service Workflow | 0.35 | Court consent + fallback | Medium | £30,000 |
| **TOTAL BUILD** | | | | **£200,000** |

**Build Criteria Met**:
- ✅ Custom stage (< 0.50 evolution) for most components
- ✅ Provides Scottish court-specific value
- ✅ Core to architectural principles compliance
- ✅ No suitable market alternatives for court context
- ✅ Skills available (web development, integration)
- ✅ Builds on existing SCTS development capability

**Procurement Route**: DOS Outcomes (Digital Outcomes and Specialists) for discovery, alpha, and beta phases if external support needed.

### BUY (G-Cloud Procurement)

**Candidates for Buying**:

| Component | Evolution | Market Options | Rationale | Procurement |
|-----------|-----------|----------------|-----------|-------------|
| Azure AI Document Intelligence | 0.75 | Azure, AWS, Google | UK data centres, G-Cloud, custom models | G-Cloud |
| Azure Speech Services | 0.72 | Azure, AWS, Google, Whisper | 10+ languages, UK processing | G-Cloud |
| Azure Translator | 0.78 | Azure, DeepL, Google | Legal terminology, UK data | G-Cloud |
| Azure AI Search | 0.75 | Azure, Elastic, Algolia | Vector search, Azure integrated | G-Cloud |
| Azure OpenAI Service | 0.68 | Azure OpenAI, AWS Bedrock | UK data residency, G-Cloud | G-Cloud |
| **TOTAL BUY (3-year)** | | | | **£485,000** |

**Buy Criteria Met**:
- ✅ Product/Commodity stage (> 0.50 evolution)
- ✅ Mature market with G-Cloud options
- ✅ Not a competitive differentiator (AI processing)
- ✅ Cost of building >> cost of buying
- ✅ UK Government approved via G-Cloud
- ✅ UK data residency guaranteed (TC-4)

**Procurement Route**: G-Cloud 14 (Cloud Hosting, Cloud Software, Cloud Support)

### RENT (Utility Services via G-Cloud)

**Candidates for SaaS/Cloud**:

| Component | Evolution | Provider | Rationale | Procurement |
|-----------|-----------|----------|-----------|-------------|
| Azure Kubernetes Service | 0.92 | Microsoft | Container platform, UK regions | G-Cloud |
| Azure SQL Database | 0.90 | Microsoft | Managed database, HA | G-Cloud |
| Azure Blob Storage | 0.95 | Microsoft | Object storage, encryption | G-Cloud |
| Azure Key Vault | 0.92 | Microsoft | Secrets management | G-Cloud |
| Azure Monitor | 0.88 | Microsoft | Observability platform | G-Cloud |
| Azure Private Endpoints | 0.85 | Microsoft | Network security | G-Cloud |
| Azure Container Registry | 0.90 | Microsoft | Container images | G-Cloud |
| Azure Application Gateway | 0.88 | Microsoft | Load balancing, WAF | G-Cloud |
| **TOTAL RENT (3-year)** | | | | **£384,000** |

**Rent Criteria Met**:
- ✅ Commodity stage (> 0.75 evolution)
- ✅ Utility services available (Azure UK)
- ✅ Pay-as-you-go model with Savings Plans
- ✅ Low switching costs (standard services)
- ✅ Standardized functionality sufficient
- ✅ Operational burden handled by Microsoft

**Procurement Route**: G-Cloud 14 (Cloud Hosting - Lot 1)

### REUSE (Existing SCTS Services)

**Components to Reuse**:

| Component | Current Status | Owner | Integration Effort |
|-----------|----------------|-------|-------------------|
| Case Management API | Operational | SCTS ICT | INT-001 (5 person-weeks) |
| Document Management API | Operational | SCTS ICT | INT-002 (3 person-weeks) |
| SCTS Identity Provider | Operational | SCTS ICT | INT-003 (2 person-weeks) |
| **TOTAL REUSE** | | | **10 person-weeks** |

---

## UK Government Procurement Strategy

### Digital Marketplace Framework Mapping

| Component Category | Evolution Stage | Framework | Lot | Estimated Value |
|-------------------|-----------------|-----------|-----|-----------------|
| Cloud Infrastructure | Commodity (0.85-0.95) | G-Cloud 14 | Lot 1: Cloud Hosting | £384,000 |
| AI Platform Services | Product (0.68-0.78) | G-Cloud 14 | Lot 2: Cloud Software | £485,000 |
| Custom Development | Custom (0.35-0.50) | DOS 6 | Outcomes (if external) | £200,000 |
| **TOTAL** | | | | **£1,069,000** |

### G-Cloud Supplier Recommendations

**Primary: Microsoft Azure (All Services)**

| Service | G-Cloud Supplier | Pricing Model | UK Data Centres |
|---------|------------------|---------------|-----------------|
| Azure AI Document Intelligence | Microsoft | Pay-per-page | UK South, UK West |
| Azure Speech Services | Microsoft | Pay-per-hour | UK South, UK West |
| Azure Translator | Microsoft | Pay-per-character | UK South, UK West |
| Azure AI Search | Microsoft | Tier-based | UK South, UK West |
| Azure OpenAI | Microsoft | Pay-per-token | UK South |
| Azure Kubernetes Service | Microsoft | Pay-per-node | UK South, UK West |
| Azure SQL Database | Microsoft | DTU/vCore | UK South, UK West |
| Azure Storage | Microsoft | Pay-per-GB | UK South, UK West |

**Rationale for Single Supplier (Microsoft)**:
- TC-2 constraint mandates Azure environment
- Integrated ecosystem reduces complexity
- Single support contract and billing
- Consistent security and compliance model
- All services available on G-Cloud 14

### Technology Code of Practice Alignment

| TCoP Point | Related Components | Map Position | Compliance |
|------------|-------------------|--------------|------------|
| 1. User Needs | Court User, Access to Justice | Top (0.90+) | ✅ Stakeholder analysis complete |
| 2. Accessibility | Human Review Interface | Custom (0.45) | ✅ WCAG 2.2 AA in NFR-U-001 |
| 3. Open Source | Audit Trail Service | Product (0.55) | ⚠️ Consider open logging standards |
| 4. Open Standards | Case Management API | Product (0.58) | ✅ REST APIs, JSON, OAuth 2.0 |
| 5. Cloud First | All infrastructure | Commodity (0.85+) | ✅ Azure UK via G-Cloud |
| 6. Secure | Azure Key Vault, Private Endpoints | Commodity (0.85+) | ✅ Security by Design assessment |
| 7. Privacy | Consent Management | Custom (0.45) | ✅ DPIA complete |
| 8. Share & Reuse | Case/Document APIs | Product (0.55-0.58) | ✅ Reusing existing SCTS services |
| 9. Technology Skills | Custom components | Custom (0.35-0.50) | ⚠️ May need DOS for capacity |
| 10. Sustainability | Azure UK regions | Commodity | ✅ Microsoft carbon neutral commitment |

### AI Playbook Mapping (HIGH-RISK AI System)

| AI Principle | Related Components | Map Position | Compliance |
|--------------|-------------------|--------------|------------|
| Human Oversight | Human Review Interface | Custom (0.45) | ✅ **BUILD** - mandatory Principle 2 |
| Transparency | AI Classification Display | Custom (0.48) | ✅ FR-011 AI labelling |
| Fairness & Bias | Document Intelligence Service | Product (0.68) | ⚠️ Bias testing required before live |
| Accountability | Audit Trail Service | Product (0.55) | ✅ 7-year immutable logs |
| Data Quality | Court Records Gateway | Custom (0.48) | ✅ Read-only access, Principle 14 |
| Safety | Manual Fallback Mode | Custom (0.42) | ✅ **BUILD** - mandatory Principle 5 |

**HIGH-RISK AI Components Mapped**:
- ✅ Human-in-the-loop component: Human Review Interface (Custom, 0.45) - **BUILD**
- ✅ Bias testing: Part of Document Intelligence Service validation - **TEST**
- ✅ DPIA: Complete (see dpia.md)
- ✅ ATRS: Complete (see atrs-record.md)

---

## Inertia and Barriers to Change

| Component | Current | Desired | Inertia | Barrier | Mitigation |
|-----------|---------|---------|---------|---------|------------|
| Case Management API | 0.58 | 0.58 | Low | API may need updates for AI | Early API specification with SCTS ICT |
| Document Management API | 0.55 | 0.55 | Low | Volume handling | Batch processing design |
| Manual processes | N/A | 0.42 (Automated) | High | Staff comfort with existing workflows | Training, phased rollout, FR-014 fallback |
| Human interpreters | N/A | Hybrid | Medium | Professional concerns | AI augments, not replaces; BC-2 commitment |

**De-risking Strategies**:
- [x] Stakeholder analysis identifies resistance (SD-6 Clerks, SD-12 Legal Profession)
- [x] BR-006 commits to zero job losses from AI
- [x] FR-014 Manual Fallback Mode ensures continuity
- [x] Phased deployment starts with low-risk (document classification)

---

## Movement and Evolution Predictions

### Next 12 Months

| Component | Current | Predicted | Velocity | Impact | Action |
|-----------|---------|-----------|----------|--------|--------|
| Azure AI Document Intelligence | 0.75 | 0.82 | Fast | Lower costs, more features | Plan for price reduction |
| Azure Speech Services | 0.72 | 0.80 | Fast | Improved accuracy | Re-evaluate alternatives |
| Human Review Interface | 0.45 | 0.50 | Medium | More standard patterns | Build with extensibility |
| Azure OpenAI Service | 0.68 | 0.78 | Very Fast | Rapid commoditization | Monitor for cost savings |

### Next 24 Months

| Component | Current | Predicted | Velocity | Impact | Action |
|-----------|---------|-----------|----------|--------|--------|
| Azure AI Document Intelligence | 0.75 | 0.88 | Fast | Near-commodity | Review commitment strategy |
| AI Classification Display | 0.48 | 0.58 | Medium | Industry patterns emerge | Consider standard components |
| Translation Engine | 0.70 | 0.85 | Fast | Near-commodity pricing | Optimize for cost |
| Cognitive Search Service | 0.72 | 0.82 | Medium | Vector search standard | Simplify architecture |

**Strategic Implications**:
- AI services are rapidly commoditizing - **avoid long-term commitments**
- Use 1-year Azure Savings Plans, not 3-year
- Human Review patterns will standardize - build with replacement in mind
- Monitor open-source alternatives (Whisper, Elasticsearch) for future optionality

---

## Dependencies and Value Chain

```
Court User
├─> Access to Justice
│   ├─> Translation Service
│   │   ├─> Speech Transcription Service (BUY)
│   │   │   └─> Azure Speech Services (RENT)
│   │   ├─> Translation Engine (BUY)
│   │   │   └─> Azure Translator (RENT)
│   │   └─> Consent Management (BUILD)
│   └─> Court Search Portal
│       └─> Cognitive Search Service (BUY)
│           └─> Azure AI Search (RENT)
│
├─> Efficient Court Operations
│   └─> Document Processing Workflow
│       ├─> Human Review Interface (BUILD) *** CRITICAL ***
│       │   └─> Confidence Scoring
│       │       └─> Document Intelligence Service (BUY)
│       │           └─> Azure AI Document Intelligence (RENT)
│       ├─> AI Classification Display (BUILD)
│       ├─> Manual Fallback Mode (BUILD) *** CRITICAL ***
│       └─> Court Records Gateway (BUILD) *** CRITICAL ***
│           ├─> Case Management API (REUSE)
│           └─> Document Management API (REUSE)
│
└─> COMMON INFRASTRUCTURE (RENT via G-Cloud)
    ├─> Azure Kubernetes Service
    ├─> Azure SQL Database
    ├─> Azure Blob Storage
    ├─> Azure Key Vault
    ├─> Azure Monitor
    └─> Azure Private Endpoints
```

**Critical Path**:
1. Human Review Interface → blocks all AI features (Principle 2)
2. Court Records Gateway → blocks document access (Principle 14)
3. Azure AI services → blocks AI processing
4. SCTS Identity Provider → blocks all access (NFR-SEC-001)

**High-Risk Dependencies**:
- ⚠️ Single vendor (Microsoft Azure) - accepted per TC-2 constraint
- ⚠️ SCTS APIs (Case Management, DMS) - early engagement required
- ⚠️ Azure OpenAI availability in UK - currently limited

---

## Risk Analysis

### High-Risk Areas

| Risk | Components | Likelihood | Impact | Mitigation |
|------|------------|------------|--------|------------|
| **Azure vendor lock-in** | All Azure services | High | Medium | Accept per TC-2; monitor alternatives |
| **SCTS API delays** | Case/Document APIs | Medium | High | Early INT-001/002 specification |
| **AI accuracy below target** | Document Intelligence | Medium | High | Phased rollout, feedback loops |
| **Staff resistance** | Human Review Interface | Medium | Medium | Training, job security commitment |
| **UK OpenAI capacity** | Azure OpenAI | Low | Medium | Fallback to standard models |

### Opportunities

| Opportunity | Components | Value | Investment | Action |
|-------------|------------|-------|------------|--------|
| AI commoditization savings | All AI services | £50K/year | £0 | Monitor and renegotiate annually |
| Cross-government reuse | Custom components | Reputation | £0 | Document patterns for sharing |
| Efficiency gains | Document Processing | £500K/year | £200K | Achieve 60% target (BR-001) |
| Interpreter cost reduction | Translation Service | £200K/year | £150K | 10 languages (BR-002) |

---

## Requirements Traceability

### Business Requirements Mapping

| Requirement | Components | Evolution | Build/Buy |
|-------------|------------|-----------|-----------|
| BR-001: Efficiency | Document Processing Workflow, Human Review Interface | Custom (0.38-0.45) | BUILD workflow, BUY AI |
| BR-002: Access to Justice | Translation Service, Speech Transcription | Custom (0.35) / Product (0.65) | BUILD workflow, BUY AI |
| BR-003: Court Records | Court Records Gateway | Custom (0.48) | **BUILD** - mandatory |
| BR-004: Compliance | Audit Trail, Consent Management | Product (0.55) / Custom (0.45) | BUILD both |
| BR-005: Value for Money | All infrastructure | Commodity (0.85+) | RENT via G-Cloud |
| BR-006: Staff Adoption | Human Review Interface, Manual Fallback | Custom (0.42-0.45) | BUILD with UX focus |

### Architecture Principles Alignment

| Principle | Components | Compliance | Notes |
|-----------|------------|------------|-------|
| P2: Human-in-the-Loop | Human Review Interface | ✅ | **BUILD** component |
| P5: Resilience | Manual Fallback Mode | ✅ | **BUILD** component |
| P8: AI Transparency | AI Classification Display | ✅ | **BUILD** component |
| P11: Security by Design | Azure Key Vault, Private Endpoints | ✅ | RENT commodity |
| P14: Court Records Integrity | Court Records Gateway | ✅ | **BUILD** component |
| P15: Data Sovereignty | Azure UK regions | ✅ | All UK South/West |
| P17: Observability | Azure Monitor | ✅ | RENT commodity |

---

## Recommendations

### Immediate Actions (0-3 months)

1. **Procure Azure Services via G-Cloud**
   - **Components**: All Azure AI + Infrastructure
   - **Rationale**: TC-2 mandate, UK data residency, G-Cloud approved
   - **Investment**: Call-off from G-Cloud 14
   - **Owner**: Procurement / CDiO
   - **Success Criteria**: Contracts in place, UK regions confirmed

2. **Begin Human Review Interface Design**
   - **Components**: Human Review Interface, Confidence Scoring
   - **Rationale**: Critical path for all AI features, Principle 2 compliance
   - **Investment**: £15,000 (design phase)
   - **Owner**: Senior AI Architect
   - **Success Criteria**: UX design approved by Court Admin Managers

3. **Engage SCTS ICT on API Integration**
   - **Components**: Case Management API, Document Management API
   - **Rationale**: INT-001/002 are dependencies for document access
   - **Investment**: Staff time
   - **Owner**: ICT Operations Manager
   - **Success Criteria**: API specifications agreed, sandbox available

### Short-Term Actions (3-12 months)

4. **Build Core Custom Components**
   - **Components**: Human Review Interface, Court Records Gateway, Manual Fallback, Audit Trail
   - **Rationale**: These are mandatory architectural components
   - **Investment**: £100,000
   - **Owner**: Development Team / DOS contractor
   - **Success Criteria**: Components deployed to staging, passing acceptance

5. **Document Intelligence PoC**
   - **Components**: Document Intelligence Service, Azure AI Document Intelligence
   - **Rationale**: Validate accuracy on Scottish court documents
   - **Investment**: £50,000
   - **Owner**: Senior AI Architect
   - **Success Criteria**: 90% classification accuracy on test set

6. **Bias Testing Framework**
   - **Components**: Document Intelligence Service
   - **Rationale**: HIGH-RISK AI requires bias assessment
   - **Investment**: £20,000
   - **Owner**: DPO / AI Architect
   - **Success Criteria**: Bias report complete, no significant disparities

### Long-Term Actions (12-24 months)

7. **Translation Service Deployment**
   - **Components**: Translation Service, Speech Transcription, Consent Management
   - **Rationale**: BR-002 Access to Justice with 10 languages
   - **Investment**: £150,000
   - **Owner**: Programme Team
   - **Success Criteria**: 10 languages live, 85% accuracy on legal terms

8. **Cognitive Search Rollout**
   - **Components**: Cognitive Search Service, Azure AI Search
   - **Rationale**: Semantic search for legal professionals (UC-3)
   - **Investment**: £75,000
   - **Owner**: Programme Team
   - **Success Criteria**: 5M documents indexed, 80% user satisfaction

9. **Review Commitment Strategy**
   - **Components**: All Azure services
   - **Rationale**: AI services commoditizing; renegotiate pricing
   - **Investment**: Staff time
   - **Owner**: CDiO / Finance
   - **Success Criteria**: 10% cost reduction vs Year 1

---

## Summary: Build vs Buy Decision Matrix

| Decision | Components | Rationale | Procurement | TCO |
|----------|------------|-----------|-------------|-----|
| **BUILD** | Human Review Interface, Court Records Gateway, Manual Fallback, Audit Trail, Consent Management, AI Display, Workflows | Scottish court context, Principle compliance, no market alternatives | In-house / DOS | £200K |
| **BUY** | Azure AI Document Intelligence, Speech, Translator, Search, OpenAI | Mature products, G-Cloud approved, UK data centres | G-Cloud 14 | £485K |
| **RENT** | AKS, SQL, Storage, Key Vault, Monitor, Private Endpoints | Commodity, utility pricing, no differentiation | G-Cloud 14 | £384K |
| **REUSE** | Case Management API, Document Management API, Identity Provider | Already operational, zero marginal cost | Existing contracts | £0 |
| **TOTAL** | 20 components | | | **£1.07M** |

---

## Map Versioning

| Version | Date | Author | Changes | Rationale |
|---------|------|--------|---------|-----------|
| v1.0 | 2026-01-21 | ArcKit AI | Initial map | Baseline for procurement strategy |

**Next Review Date**: 2026-04-21 (Quarterly)

**Review Triggers**:
- Major Azure pricing changes
- New G-Cloud framework release
- Alternative vendor emergence
- Component evolution significantly different from predictions

---

## Appendix: Wardley Map Code (Alternative Views)

### Simplified View (User Needs Focus)

```wardley
title SCTS GenAI - User Needs View

anchor Court User [0.97, 0.25]

component Court User [0.97, 0.25]
component Access to Justice [0.92, 0.30]
component Efficient Operations [0.88, 0.35]
component Translation [0.78, 0.38]
component Document Processing [0.75, 0.42]
component Search [0.72, 0.45]
component Human Oversight [0.65, 0.45]
component AI Services [0.50, 0.72]
component Cloud Infrastructure [0.25, 0.90]

Court User -> Access to Justice
Court User -> Efficient Operations
Access to Justice -> Translation
Efficient Operations -> Document Processing
Document Processing -> Human Oversight
Translation -> AI Services
Document Processing -> AI Services
Search -> AI Services
Human Oversight -> AI Services
AI Services -> Cloud Infrastructure

evolve AI Services 0.82 label Commoditizing

style wardley
```

### Procurement View (Decision Focus)

```wardley
title SCTS GenAI - Procurement Strategy

anchor User Needs [0.95, 0.30]

annotation 1 [0.45, 0.42] BUILD (Custom)
annotation 2 [0.50, 0.72] BUY (G-Cloud)
annotation 3 [0.25, 0.90] RENT (G-Cloud)

component User Needs [0.95, 0.30]
component Custom Workflows [0.75, 0.42]
component Human Review [0.65, 0.45]
component Azure AI Services [0.50, 0.72]
component Azure Infrastructure [0.25, 0.90]

User Needs -> Custom Workflows
Custom Workflows -> Human Review
Human Review -> Azure AI Services
Azure AI Services -> Azure Infrastructure

pipeline Custom Workflows [0.75, 0.35, 0.50]
pipeline Azure AI Services [0.50, 0.68, 0.78]

style wardley
```

---

**Generated by**: ArcKit `/arckit.wardley` command
**Generated on**: 2026-01-21
**ArcKit Version**: 0.6.0
**Project**: SCTS GenAI Programme (Project 001)
**AI Model**: Claude Opus 4.5

**Source Artifacts**:
- requirements.md - Functional and non-functional requirements
- research-findings.md - Technology research and vendor analysis
- architecture-principles.md - Strategic principles
- stakeholder-drivers.md - Stakeholder context
- tcop-review.md - Technology Code of Practice assessment
- ai-playbook-assessment.md - AI Playbook compliance
