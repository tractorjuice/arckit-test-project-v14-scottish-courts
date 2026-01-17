# Algorithmic Transparency Recording Standard (ATRS) Record

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-ATRS-v1.0 |
| **Document Type** | Algorithmic Transparency Recording Standard |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-01-17 |
| **Last Modified** | 2026-01-17 |
| **Review Cycle** | Annual |
| **Next Review Date** | 2027-01-17 |
| **Owner** | Chief Digital Information Officer, SCTS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | Public (upon publication) |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.atrs` command | [PENDING] | [PENDING] |

---

# TIER 1: PUBLIC SUMMARY

*This section provides a plain-English summary of the algorithmic tool for public understanding.*

---

## 1. Basic Information

### 1.1 Tool Name
**SCTS GenAI Platform**

### 1.2 Organisation
**Scottish Courts and Tribunals Service (SCTS)**

A Scottish public body responsible for administering Scotland's courts and tribunals.

- **Website**: https://www.scotcourts.gov.uk
- **Parent Department**: Scottish Government (Justice portfolio)
- **Sector**: Justice / Public Administration

### 1.3 Function Area
**Justice Administration**

The tool supports the administrative functions of the Scottish courts, including document processing, language support services, and information retrieval.

### 1.4 Geographic Coverage
**Scotland**

The tool operates across all Scottish courts and tribunals.

### 1.5 Phase
- [ ] Idea or concept
- [x] In design or development
- [ ] In pilot testing
- [ ] In limited production
- [ ] In full production
- [ ] Retired

**Current Status**: Pre-deployment (PoC phase planned for 2026-Q2)

### 1.6 Publication Date
**[DATE TO BE CONFIRMED]** - Target: 2026-Q2 (before production deployment)

### 1.7 Last Updated
2026-01-17

---

## 2. Purpose and Scope

### 2.1 What does this tool do?

The SCTS GenAI Platform uses artificial intelligence to help the Scottish Courts and Tribunals Service:

1. **Process court documents faster** - The AI reads and categorises documents (such as court submissions, evidence, and applications) so court staff can process them more quickly.

2. **Support people who don't speak English** - The AI provides real-time transcription (converting speech to text) and translation services during court proceedings, helping people who speak other languages participate in court.

3. **Help find information** - The AI powers an intelligent search system that helps court staff and legal professionals find relevant documents and case law more easily.

**What this tool does NOT do:**
- It does NOT make legal decisions or judgements
- It does NOT replace judges or judicial decision-making
- It does NOT automatically progress cases without human approval
- It does NOT replace human interpreters for complex or sensitive matters

### 2.2 Why are we using this tool?

**Problem we're solving:**
- Court document processing is time-consuming, creating backlogs and delays
- Non-English speakers face barriers to accessing justice
- Finding relevant documents and case law takes considerable time

**Benefits we expect:**
- 60% reduction in document processing time
- Support for 10 languages used in Scottish courts
- Faster, more accurate document searches
- Improved access to justice for non-English speakers

**Why AI is appropriate:**
- AI can process large volumes of documents faster than manual methods
- AI translation can provide immediate support when human interpreters aren't available
- AI-powered search understands meaning, not just keywords
- Human staff remain in control of all important decisions

### 2.3 Who uses this tool?

**Internal users:**
- Court Clerks (primary users for document processing)
- Court Administration Managers (oversight and quality review)
- Legal professionals (search capabilities)

**External users:**
- Court users who need translation services (with their consent)

### 2.4 Who is affected by this tool?

**People affected:**
- Anyone involved in court proceedings (approximately 80,000+ individuals per year)
- Court staff (approximately 500+)
- Legal professionals

**Vulnerable groups identified:**
- Witnesses (may be in stressful situations)
- Victims (may be vulnerable or traumatised)
- Non-English speakers (may face communication barriers)
- Children (in family court and child protection cases)
- People with disabilities (accessibility needs)

---

## 3. How It Works (Plain English)

### 3.1 Document Classification

**What happens:**
1. A court clerk uploads or scans a document
2. The AI reads the document and suggests what type it is (e.g., "claim form", "defence", "evidence")
3. The AI also extracts key information like names, dates, and case numbers
4. The clerk reviews the AI's suggestion and confirms or corrects it
5. The document is then filed in the correct place

**Human involvement:** A court clerk ALWAYS reviews and confirms what the AI suggests. The AI never files documents without human approval.

### 3.2 Translation Services

**What happens:**
1. Before a court session, the participant is asked if they consent to AI translation
2. If they agree, the AI listens to what is said in court
3. The AI converts speech to text, then translates it to the participant's language
4. The translation appears on a screen for the participant
5. A human interpreter is always available if the AI translation is unclear or if the participant prefers human translation

**Human involvement:** Participants can request a human interpreter at any time. For complex legal matters or sensitive issues, human interpreters are always used.

### 3.3 Intelligent Search

**What happens:**
1. A user types a search question in normal language (e.g., "cases about landlord disputes")
2. The AI understands the meaning of the question, not just the words
3. The AI returns relevant documents, ranked by how well they match
4. The user reviews the results and selects what they need

**Human involvement:** The search helps users find information, but users decide which documents are relevant to their work.

### 3.4 How confident is the AI?

The AI provides a "confidence score" with every suggestion. This tells staff how certain the AI is about its answer:
- **High confidence (80%+):** AI is fairly sure
- **Lower confidence (<80%):** Staff should review more carefully

Staff are trained to pay extra attention when confidence is low.

---

## 4. Human Control

### 4.1 Who makes the decisions?

**Humans make all important decisions.** The AI only provides suggestions and assistance.

| Task | AI Role | Human Role |
|------|---------|------------|
| Document classification | Suggests category | Clerk confirms or corrects |
| Translation | Provides translated text | Participant can request human interpreter |
| Search results | Ranks relevant documents | User decides what's relevant |
| Court records | Read-only access | Human approval required for any changes |

### 4.2 Can humans override the AI?

**Yes, always.** Every AI suggestion can be changed by a human. Staff are trained to:
- Check AI suggestions carefully
- Override the AI when they know better
- Report when the AI makes mistakes (so it can be improved)

### 4.3 What if the AI isn't working?

If the AI system is unavailable:
- Document processing continues using manual methods
- Human interpreters handle all translation
- Search uses basic keyword matching

Court operations never depend on AI being available.

---

## 5. Data and Privacy

### 5.1 What data does the AI use?

The AI processes:
- Court documents (which may contain personal information about people involved in cases)
- Speech in court proceedings (when translation is used, with consent)
- Search queries from court staff and legal professionals

### 5.2 What personal data is involved?

Court documents may contain:
- Names and contact details
- Information about legal disputes
- In some cases: health information, criminal records, family circumstances

This is **sensitive information** and is protected accordingly.

### 5.3 How is data protected?

- **UK data only:** All data stays in UK data centres (never transferred abroad)
- **Encryption:** All data is encrypted (scrambled) when stored and when moving between systems
- **Access controls:** Only authorised staff can access the systems
- **Audit trail:** Every AI operation is logged so we can check what happened
- **Separate storage:** AI outputs are stored separately from official court records

### 5.4 Data Protection Impact Assessment

A full Data Protection Impact Assessment (DPIA) has been completed.

**Key finding:** The processing is lawful under UK GDPR because it supports SCTS's public task of administering justice.

**Residual risk level:** MEDIUM (after mitigations applied)

**Reference:** `projects/001-scts-genai-programme/dpia.md`

### 5.5 Your rights

If you're involved in court proceedings and the AI processes your data, you have the right to:
- **Know** if AI was used in processing your documents
- **Access** your personal data (subject access request)
- **Correct** inaccurate information
- **Request human translation** instead of AI translation

Contact the SCTS Data Protection Officer to exercise these rights.

---

## 6. Fairness and Bias

### 6.1 How do we ensure fairness?

We're committed to ensuring the AI treats everyone fairly:

- **Bias testing:** Before deployment, we test the AI across different groups to check for unfair differences
- **Multiple languages:** We support 10 languages used in Scottish courts
- **Accuracy monitoring:** We track how accurate the AI is for each language
- **Human oversight:** Human review catches any unfair or incorrect AI outputs

### 6.2 Protected characteristics

We specifically check that the AI performs fairly regardless of:
- Language or nationality
- Any protected characteristic that might affect outcomes

### 6.3 What if there's a problem?

If the AI is found to treat any group unfairly:
1. We investigate immediately
2. We can disable the affected capability
3. We fix the problem before re-enabling
4. We report serious issues to the appropriate regulator

---

## 7. Accountability

### 7.1 Who is responsible?

| Role | Name/Position | Responsibility |
|------|---------------|----------------|
| **Senior Responsible Owner** | Chief Executive, SCTS | Overall accountability |
| **Programme Owner** | Chief Digital Information Officer | Day-to-day operation |
| **Technical Lead** | Senior AI Technical Architect | Technical implementation |
| **Data Protection** | Data Protection Officer, SCTS | Privacy compliance |
| **Legal Compliance** | Legal Services Director, SCTS | Legal risk |

### 7.2 How to raise concerns

If you have concerns about how the AI is being used:

1. **General enquiries:** Contact SCTS via https://www.scotcourts.gov.uk
2. **Data protection concerns:** Contact the SCTS Data Protection Officer
3. **Complaints:** Use the SCTS complaints procedure
4. **Regulatory concerns:** Contact the Information Commissioner's Office (ICO)

### 7.3 Review and updates

This record will be reviewed:
- **Annually** (at minimum)
- **When significant changes** are made to the AI system
- **If issues are identified** that need to be communicated

---

## 8. More Information

### 8.1 Related documents (public)

- SCTS Privacy Notice: https://www.scotcourts.gov.uk/about-the-scottish-court-service/contact-us/privacy-notice
- Scottish Government AI Strategy: https://www.gov.scot/policies/digital/artificial-intelligence/

### 8.2 Technical details

For technical specialists, detailed information is provided in **Tier 2** below.

---

# TIER 2: DETAILED TECHNICAL INFORMATION

*This section provides detailed technical information for specialists, auditors, and regulators.*

---

## 9. Organisation and Ownership

### 9.1 Organisation Details

| Field | Value |
|-------|-------|
| **Organisation Name** | Scottish Courts and Tribunals Service (SCTS) |
| **Organisation Type** | Scottish Public Body |
| **Parent Organisation** | Scottish Government |
| **Portfolio** | Justice |
| **Registration** | N/A (public body) |
| **Data Controller** | Scottish Courts and Tribunals Service |
| **ICO Registration Number** | [SCTS ICO Registration] |

### 9.2 Ownership and Accountability

| Role | Name/Position | Organisation | Contact |
|------|---------------|--------------|---------|
| **Data Controller** | Scottish Courts and Tribunals Service | SCTS | dpo@scotcourts.gov.uk |
| **Senior Responsible Owner (SRO)** | Chief Executive | SCTS | [Office contact] |
| **Programme Owner** | Chief Digital Information Officer | CDi Function, SCTS | [Office contact] |
| **Technical Owner** | Senior AI Technical Architect | CDi Function, SCTS | [Office contact] |
| **Data Protection Officer** | Data Protection Officer | Corporate Services, SCTS | dpo@scotcourts.gov.uk |
| **Legal Owner** | Legal Services Director | Corporate Services, SCTS | [Office contact] |

### 9.3 Vendor/Supplier Information

| Supplier | Product/Service | Contract Type | Data Processing |
|----------|-----------------|---------------|-----------------|
| Microsoft Azure | Azure AI Services (Document Intelligence, Speech, Translator, AI Search) | G-Cloud Framework Agreement | Data Processor (UK data centres only) |

**Supplier Certifications:**
- ISO 27001:2022
- ISO 27017:2015
- ISO 27018:2019
- SOC 2 Type II
- Cyber Essentials Plus

**Data Processing Agreement:** Microsoft Azure Data Processing Addendum (UK) applies via G-Cloud terms.

**UK Data Residency:** Contractually guaranteed - Azure UK South and UK West regions only.

---

## 10. Detailed System Description

### 10.1 System Architecture Overview

The SCTS GenAI Platform comprises four primary AI capabilities:

```
┌─────────────────────────────────────────────────────────────────┐
│                    SCTS GenAI Platform                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐ │
│  │   Document      │  │    Speech       │  │   Translation   │ │
│  │  Intelligence   │  │   Services      │  │    Services     │ │
│  │                 │  │                 │  │                 │ │
│  │  - Classification│  │  - Transcription│  │  - Real-time   │ │
│  │  - Entity Extract│  │  - Speaker ID   │  │  - 10 languages│ │
│  │  - OCR          │  │  - Confidence   │  │  - Legal terms  │ │
│  └────────┬────────┘  └────────┬────────┘  └────────┬────────┘ │
│           │                    │                    │           │
│  ┌────────┴────────────────────┴────────────────────┴────────┐ │
│  │                    Cognitive Search                        │ │
│  │  - Semantic search  - Citation detection  - Similarity     │ │
│  └────────────────────────────────────────────────────────────┘ │
│                                                                 │
│  ┌────────────────────────────────────────────────────────────┐ │
│  │         Integration Layer (APIs, Event Queues)             │ │
│  └────────────────────────────────────────────────────────────┘ │
│                                                                 │
│  ┌────────────────────────────────────────────────────────────┐ │
│  │     Audit & Governance (Logging, Access Control, RBAC)     │ │
│  └────────────────────────────────────────────────────────────┘ │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 10.2 AI Capabilities Detail

#### 10.2.1 Document Intelligence

| Attribute | Value |
|-----------|-------|
| **Capability** | Automated document classification and entity extraction |
| **Technology** | Azure AI Document Intelligence |
| **AI Type** | Machine Learning (Document Classification), Natural Language Processing (Entity Extraction), Computer Vision (OCR) |
| **Model Type** | Pre-trained Azure models with custom training for Scottish legal taxonomy |
| **Input** | PDF, TIFF, JPEG, PNG, DOCX documents up to 100MB |
| **Output** | Document classification label, confidence score (0.00-1.00), extracted entities (parties, dates, case numbers, amounts) |
| **Performance Target** | 90% classification accuracy; <10 seconds (p95) for documents up to 50 pages |

**Training Data:**
- Azure pre-trained models (public document corpus)
- Custom training: Scottish court document taxonomy (using representative SCTS documents)
- Training data provenance documented
- No personal data retained in model training

#### 10.2.2 Speech Services

| Attribute | Value |
|-----------|-------|
| **Capability** | Real-time speech-to-text transcription |
| **Technology** | Azure AI Speech Services |
| **AI Type** | Deep Learning (Speech Recognition), Machine Learning (Speaker Diarisation) |
| **Model Type** | Pre-trained Azure models |
| **Input** | Audio stream (courtroom microphones) |
| **Output** | Transcript text, timestamps, speaker labels, confidence scores |
| **Performance Target** | 95% word accuracy (English); <500ms latency |

**Supported Languages for Transcription:**
- English (primary)
- Polish, Urdu, Punjabi, Arabic, Mandarin Chinese, Cantonese, Romanian, Bengali, Russian

#### 10.2.3 Translation Services

| Attribute | Value |
|-----------|-------|
| **Capability** | Real-time text translation with legal terminology |
| **Technology** | Azure Translator |
| **AI Type** | Neural Machine Translation (Deep Learning) |
| **Model Type** | Pre-trained Azure models with custom legal glossary |
| **Input** | Source text, source language, target language |
| **Output** | Translated text, confidence score, terminology flags |
| **Performance Target** | 85% accuracy (legal terminology); <2 seconds latency |

**Supported Language Pairs:**
| Source | Target Languages |
|--------|------------------|
| English | Polish, Urdu, Punjabi, Arabic, Mandarin Chinese, Cantonese, Romanian, Bengali, Russian |
| [Above languages] | English |

#### 10.2.4 Cognitive Search

| Attribute | Value |
|-----------|-------|
| **Capability** | Semantic search, citation detection, document similarity |
| **Technology** | Azure AI Search |
| **AI Type** | Natural Language Processing, Vector Embeddings, Machine Learning (Ranking) |
| **Model Type** | Pre-trained Azure models |
| **Input** | Natural language search query, filters (date, case type, court level) |
| **Output** | Ranked document list, relevance scores, snippets, facets |
| **Performance Target** | <2 seconds (simple query); 80% user satisfaction |

**Index Scope:**
- Civil case documents
- Criminal case documents
- Estimated 5 million documents initial, growing 500K per year
- 7-year retention in active index; older documents archived

### 10.3 Decision-Making Framework

#### 10.3.1 Decision Types

| Decision | AI Role | Human Role | Authority | Reversible? |
|----------|---------|------------|-----------|-------------|
| Document classification | Recommends category with confidence | Reviews, confirms or overrides | Clerk of Court | Yes |
| Entity extraction | Extracts entities with confidence | Validates extracted data | Clerk of Court | Yes |
| Translation output | Provides translation | Reviews, requests human interpreter if needed | Participant (with consent) | Yes |
| Search ranking | Ranks results by relevance | Selects relevant documents | User | N/A |
| Court record entry | Read-only (no write) | Approves any entry via separate workflow | Clerk of Court | Yes |

#### 10.3.2 Human Oversight Model

**Primary Model: Human-in-the-Loop**
- Human reviews EVERY consequential AI output before action
- AI cannot modify court records without human approval
- AI classification is recommendation only

**Secondary Model: Human-in-Command**
- Humans can override AI decisions at any time
- Human interpreters mandatory for complex/sensitive matters
- Manual fallback available when AI unavailable

**Escalation Triggers:**
- Confidence score < 80%: Highlighted for careful review
- Legal terminology flagged: Human interpreter alerted
- Complex/sensitive matter: Human interpreter mandatory (BC-2)
- System error: Automatic fallback to manual processing

### 10.4 Data Flow

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Document   │────▶│   Upload    │────▶│  AI        │────▶│   Human    │
│  Received   │     │   System    │     │  Processing│     │   Review   │
└─────────────┘     └─────────────┘     └─────────────┘     └─────────────┘
                                               │                   │
                                               ▼                   ▼
                                        ┌─────────────┐     ┌─────────────┐
                                        │   Audit    │     │   Case     │
                                        │   Log      │     │   File     │
                                        └─────────────┘     └─────────────┘

Data Flow Notes:
- All data encrypted in transit (TLS 1.3) and at rest (AES-256)
- AI outputs stored separately from authoritative court records
- Audit log captures: user, action, input reference, output, model version, human decision
- No data leaves UK jurisdiction
```

---

## 11. Data Processing

### 11.1 Personal Data Inventory

| Data Category | Source | Purpose | Lawful Basis | Special Category? | Retention |
|---------------|--------|---------|--------------|-------------------|-----------|
| Court documents (text) | Case Management System | Document classification, search indexing | Public Task (Art. 6(1)(e)) | Yes (may contain health, criminal, ethnic data) | 7 years |
| Court proceedings (audio) | Courtroom audio | Transcription, translation | Public Task + Consent (translation) | Yes (speech content) | 7 years |
| User actions | System interaction | Audit trail | Public Task | No | 7 years |
| Translation consent | Participant declaration | Consent tracking | Consent (Art. 6(1)(a)) | No | 7 years |

### 11.2 Special Category Data

**GDPR Article 9 Categories Processed:**

| Category | Context | Legal Basis | Safeguards |
|----------|---------|-------------|------------|
| Health data | Medical evidence in court documents | DPA 2018 Schedule 1, Part 2, Para 6 (Administration of Justice) | Human review, access controls, encryption |
| Criminal conviction data | Criminal case proceedings | DPA 2018 Part 3 (Law Enforcement) | Human review, access controls, encryption |
| Racial/ethnic origin | May appear in case narratives | DPA 2018 Schedule 1, Part 2, Para 6 (Administration of Justice) | Human review, bias monitoring |

### 11.3 Data Processing Principles Compliance

| GDPR Principle | Implementation | Evidence |
|----------------|----------------|----------|
| **Lawfulness** | Public Task basis documented; consent for translation | DPIA Section 4.1 |
| **Fairness** | Human-in-the-loop; bias testing; transparency | Architecture Principle 2, 7 |
| **Transparency** | ATRS published; AI labelling on outputs | FR-011, this document |
| **Purpose limitation** | Processing only for court administration | DPIA Section 2.3 |
| **Data minimisation** | Only court-submitted documents processed | DPIA Section 4.4 |
| **Accuracy** | Human review; correction processes | FR-003, data model |
| **Storage limitation** | 7-year retention aligned with court records | Data model retention policy |
| **Integrity/confidentiality** | Encryption, access controls, audit logging | NFR-SEC requirements |
| **Accountability** | Named owners, DPIA, ATRS, governance | This document, DPIA |

### 11.4 Data Subject Rights Implementation

| Right | Implemented | Mechanism | Response Time |
|-------|-------------|-----------|---------------|
| Access (Art. 15) | Yes | SAR process via DPO | 30 days |
| Rectification (Art. 16) | Yes | Admin portal / DPO | 30 days |
| Erasure (Art. 17) | Limited | After retention period (legal obligation) | N/A |
| Restriction (Art. 18) | Yes | Processing flag | 72 hours |
| Portability (Art. 20) | No | Not applicable (public task) | N/A |
| Object (Art. 21) | Yes (translation) | Opt-out, human interpreter | Immediate |
| Automated decisions (Art. 22) | Yes | Human review always available | Immediate |

### 11.5 International Transfers

**International Data Transfers:** NONE

All data processing occurs within UK jurisdiction:
- Azure UK South and UK West data centres
- Contractual guarantee of UK-only processing
- No cross-border data flows

---

## 12. Impact Assessments

### 12.1 Data Protection Impact Assessment (DPIA)

| Field | Value |
|-------|-------|
| **DPIA Status** | Completed |
| **DPIA Date** | 2026-01-17 |
| **DPIA Reference** | ARC-001-DPIA-v1.0 |
| **DPIA Location** | `projects/001-scts-genai-programme/dpia.md` |
| **Outcome** | PROCEED WITH CONDITIONS |
| **Residual Risk Level** | MEDIUM |
| **ICO Consultation Required** | No |

**Key DPIA Findings:**
- 5/9 ICO screening criteria met (DPIA mandatory)
- 10 risks identified, all mitigated to MEDIUM or below
- Human-in-the-loop significantly reduces automated decision-making risks
- Special category data processing lawful under Administration of Justice basis

**DPIA Conditions:**
1. Complete bias audit for all 10 priority languages
2. Update SCTS privacy notice with AI processing details
3. Publish ATRS record (this document)
4. Complete staff training before rollout
5. Establish quarterly bias monitoring

### 12.2 Equality Impact Assessment (EqIA)

| Field | Value |
|-------|-------|
| **EqIA Status** | Planned |
| **EqIA Target Date** | 2026-Q1 |
| **Protected Characteristics** | All (with focus on race/nationality via language) |

**Preliminary Assessment:**
- Translation services specifically address language barriers (positive impact on access)
- Accessibility requirements (WCAG 2.2 AA) address disability
- Bias testing for all languages addresses potential discrimination

### 12.3 Human Rights Assessment

| Field | Value |
|-------|-------|
| **Status** | Planned |
| **Target Date** | 2026-Q1 |

**Rights Considered:**
- Right to a fair trial (ECHR Article 6): Human oversight ensures AI doesn't affect trial fairness
- Right to private life (ECHR Article 8): DPIA addresses privacy; UK data residency
- Right to non-discrimination (ECHR Article 14): Bias testing and monitoring

---

## 13. Fairness and Bias Assessment

### 13.1 Bias Risk Assessment

| Bias Type | Risk Level | Affected Groups | Mitigation |
|-----------|------------|-----------------|------------|
| **Language bias** | MEDIUM | Non-English speakers | Accuracy testing per language; human interpreter backup |
| **Training data bias** | LOW | Underrepresented document types | Azure pre-trained models; custom training review |
| **Proxy discrimination** | MEDIUM | Groups correlated with language | Fairness metrics by language; human oversight |
| **Historical bias** | LOW | Groups underrepresented in training data | Azure managed models trained on diverse data |

### 13.2 Fairness Metrics

**Metrics to be calculated before deployment:**

| Metric | Description | Threshold | Measurement Frequency |
|--------|-------------|-----------|----------------------|
| **Translation accuracy by language** | Word/sentence accuracy per language | ≥85% for all languages, ≤10% variance between languages | Quarterly |
| **Classification accuracy by document type** | Accuracy per document category | ≥90% for all categories | Monthly |
| **Human override rate by category** | How often humans override AI | Monitor for anomalies | Monthly |
| **Error rate by user group** | Errors affecting different user groups | No statistically significant difference | Quarterly |

### 13.3 Bias Mitigation Measures

| Measure | Implementation Status | Owner |
|---------|----------------------|-------|
| Pre-deployment bias testing for all languages | Planned (2026-Q2) | AI Architect |
| Diverse training data review | Planned | AI Architect |
| Regular bias monitoring in production | Planned | AI Architect + DPO |
| Human oversight for edge cases | Designed | Court Admin |
| Feedback mechanism for users | Designed (FR-013) | CDiO |
| Third-party ethics review (translation) | Planned | DPO |

### 13.4 Bias Testing Results

**Status:** Not yet completed (pre-deployment)

| Test | Languages | Date | Result | Actions |
|------|-----------|------|--------|---------|
| Translation accuracy | 10 priority | TBD | TBD | TBD |
| Speech recognition accuracy | 10 priority | TBD | TBD | TBD |
| Legal terminology accuracy | English | TBD | TBD | TBD |

---

## 14. Technical Details

### 14.1 AI/ML Technologies

| Component | Technology | Provider | Version | Model Type |
|-----------|------------|----------|---------|------------|
| Document Classification | Azure AI Document Intelligence | Microsoft | Latest GA | Pre-trained + Custom |
| OCR | Azure AI Document Intelligence | Microsoft | Latest GA | Pre-trained |
| Speech-to-Text | Azure AI Speech Services | Microsoft | Latest GA | Pre-trained |
| Translation | Azure Translator | Microsoft | Latest GA | Neural MT |
| Semantic Search | Azure AI Search | Microsoft | Latest GA | Vector Embeddings |
| Embeddings | Azure OpenAI (text-embedding) | Microsoft | Latest GA | Pre-trained |

### 14.2 Model Information

**Document Classification Model:**
- **Type:** Multi-class classification (neural network)
- **Architecture:** Azure pre-trained with transfer learning
- **Training data:** Public document corpus + SCTS legal taxonomy
- **Retraining schedule:** As needed based on accuracy drift

**Translation Model:**
- **Type:** Neural machine translation (Transformer)
- **Architecture:** Azure Translator (Microsoft proprietary)
- **Training data:** Large-scale parallel corpus (Azure managed)
- **Customisation:** Legal terminology glossary

**No custom model training on personal data** - all models are pre-trained or trained on anonymised/synthetic data.

### 14.3 System Performance Specifications

| Metric | Requirement | Measurement |
|--------|-------------|-------------|
| **Availability** | 99.5% during court hours (Mon-Fri 09:00-17:00) | Uptime monitoring |
| **Document processing latency** | <10 seconds (p95) for docs up to 50 pages | APM |
| **Translation latency** | <2 seconds | APM |
| **Transcription latency** | <500ms | APM |
| **Search latency** | <2 seconds (simple query) | APM |
| **Concurrent users** | 100 peak | Load testing |
| **Recovery Time Objective (RTO)** | 4 hours | DR testing |
| **Recovery Point Objective (RPO)** | 1 hour | Backup verification |

### 14.4 Security Architecture

| Control | Implementation | Standard |
|---------|----------------|----------|
| **Authentication** | SAML 2.0 SSO with SCTS Active Directory | NFR-SEC-001 |
| **MFA** | Required for admin access | NFR-SEC-001 |
| **Authorisation** | Role-based access control (RBAC) | NFR-SEC-002 |
| **Encryption (transit)** | TLS 1.3 | NFR-SEC-003 |
| **Encryption (rest)** | AES-256 | NFR-SEC-003 |
| **Key management** | Azure Key Vault (SCTS-managed keys) | NFR-SEC-003 |
| **Network security** | Azure Virtual Network, NSGs | Architecture design |
| **Vulnerability management** | CI/CD scanning, monthly DAST, annual pentest | NFR-SEC-005 |
| **Audit logging** | Immutable, 7-year retention | NFR-C-002 |

### 14.5 Integration Points

| System | Integration Type | Data Flow | Authentication |
|--------|-----------------|-----------|----------------|
| SCTS Case Management System | REST API | Bidirectional (read-write with approval) | OAuth 2.0 |
| SCTS Document Management System | REST API + Webhooks | Inbound (documents) | mTLS |
| SCTS Identity Provider | SAML 2.0 | User identity | Certificate |
| Court Scheduling System | REST API | Inbound (session details) | OAuth 2.0 |
| Azure AI Services | REST/gRPC API | Outbound (content), Inbound (results) | API Key + mTLS |

---

## 15. Testing and Validation

### 15.1 Testing Approach

| Test Type | Scope | Frequency | Status |
|-----------|-------|-----------|--------|
| **Functional testing** | All AI capabilities | Per release | Planned |
| **Accuracy testing** | Classification, translation | Per release | Planned |
| **Bias testing** | All languages, document types | Pre-deployment + quarterly | Planned |
| **Performance testing** | Load, latency | Per release | Planned |
| **Security testing** | Vulnerability, penetration | Monthly/annually | Planned |
| **Accessibility testing** | WCAG 2.2 AA | Per release | Planned |
| **User acceptance testing** | End-to-end workflows | Pre-deployment | Planned |
| **Disaster recovery testing** | Failover, restore | Quarterly | Planned |

### 15.2 Validation Criteria

| Criterion | Target | Measurement |
|-----------|--------|-------------|
| Document classification accuracy | ≥90% | Sample review by domain experts |
| Translation accuracy (legal terms) | ≥85% | Professional linguist review |
| Speech recognition accuracy (English) | ≥95% | Sample transcription review |
| Human override rate | Monitor (no target) | System analytics |
| User satisfaction | ≥80% | User surveys |
| Zero court record incidents | 0 | Incident tracking |

### 15.3 Test Results

**Status:** Pre-deployment (PoC testing planned for 2026-Q2)

| Test | Date | Result | Issues | Actions |
|------|------|--------|--------|---------|
| PoC Document Classification | TBD | TBD | TBD | TBD |
| PoC Translation Accuracy | TBD | TBD | TBD | TBD |
| Security Penetration Test | TBD | TBD | TBD | TBD |

---

## 16. Transparency Measures

### 16.1 Public Transparency

| Measure | Implementation | Location |
|---------|----------------|----------|
| **ATRS Record** | This document | SCTS website (upon publication) |
| **Privacy Notice** | To be updated with AI processing | SCTS website |
| **AI Use Statement** | Court user information | Court premises, SCTS website |
| **Model Information** | Published in ATRS Tier 2 | This document |

### 16.2 Operational Transparency

| Measure | Implementation | Users |
|---------|----------------|-------|
| **AI output labelling** | "AI-Assisted" label on all outputs (FR-011) | All users |
| **Confidence scores** | Displayed with all AI suggestions | Staff |
| **Human review confirmation** | Logged in audit trail | Auditors |
| **Model version tracking** | Recorded with each operation | Technical staff |

### 16.3 Contestability

| Pathway | Mechanism | Response Time |
|---------|-----------|---------------|
| **Override AI suggestion** | Clerk can correct classification | Immediate |
| **Request human translation** | Participant can request interpreter | Immediate |
| **Quality feedback** | Flag issues via interface (FR-013) | Acknowledged within 24 hours |
| **Formal complaint** | SCTS complaints procedure | 20 working days |
| **Data protection complaint** | DPO / ICO | 30 days (SAR) |

---

## 17. Governance and Oversight

### 17.1 Governance Structure

```
┌─────────────────────────────────────────┐
│        Scottish Ministers               │
│     (Cabinet Secretary for Justice)     │
└───────────────────┬─────────────────────┘
                    │
┌───────────────────▼─────────────────────┐
│           SCTS Board                    │
│        (Strategic Oversight)            │
└───────────────────┬─────────────────────┘
                    │
┌───────────────────▼─────────────────────┐
│          Chief Executive                │
│     (Senior Responsible Owner)          │
└───────────────────┬─────────────────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
┌───────────┐ ┌───────────┐ ┌───────────┐
│   CDiO    │ │  Legal    │ │   DPO     │
│Programme  │ │ Services  │ │  Privacy  │
│  Owner    │ │Compliance │ │Compliance │
└─────┬─────┘ └───────────┘ └───────────┘
      │
      ▼
┌───────────┐
│Senior AI  │
│ Architect │
│ Technical │
│   Lead    │
└───────────┘
```

### 17.2 Governance Checkpoints

| Phase | Review | Reviewers | Status |
|-------|--------|-----------|--------|
| Requirements | Stakeholder sign-off | Chief Executive, CDiO, Legal, DPO | Pending |
| Design | Architecture review | CDiO, AI Architect, Security | Planned |
| Pre-deployment | DPIA, security, ethics | DPO, Legal, Chief Executive | Planned |
| Go-live | Production readiness | CDiO, Chief Executive | Planned |
| Post-deployment | Performance review | CDiO, Court Admin | Planned |

### 17.3 Ongoing Monitoring

| Activity | Frequency | Owner | Escalation |
|----------|-----------|-------|------------|
| Performance monitoring | Continuous | AI Architect | CDiO |
| Accuracy metrics review | Monthly | AI Architect | CDiO |
| Bias metrics review | Quarterly | AI Architect + DPO | CDiO, Chief Executive |
| Incident review | As needed | CDiO | Chief Executive |
| Governance review | Quarterly | Chief Executive | SCTS Board |
| ATRS review | Annually | CDiO | Chief Executive |
| DPIA review | Annually | DPO | Legal Services |

### 17.4 Incident Response

**AI Incident Categories:**

| Category | Example | Response | Escalation |
|----------|---------|----------|------------|
| **Critical** | AI corrupts court record | Immediate shutdown, investigation, Chief Executive notified | Lord President |
| **High** | Significant bias detected | Capability paused, investigation | Chief Executive |
| **Medium** | Accuracy below threshold | Enhanced monitoring, remediation plan | CDiO |
| **Low** | Minor user complaint | Investigation, resolution | AI Architect |

**Incident Response Process:**
1. Detection (monitoring, user report, audit)
2. Triage and classification
3. Containment (disable capability if needed)
4. Investigation (root cause analysis)
5. Remediation (fix, retrain, process change)
6. Communication (stakeholders, public if warranted)
7. Lessons learned (ATRS update if significant)

---

## 18. Compliance and Standards

### 18.1 Legal and Regulatory Compliance

| Requirement | Compliance Status | Evidence |
|-------------|-------------------|----------|
| **UK GDPR** | Compliant (by design) | DPIA, lawful basis documented |
| **Data Protection Act 2018** | Compliant (by design) | DPIA, Schedule 1 basis |
| **Equality Act 2010** | Compliant (by design) | Accessibility (WCAG 2.2), bias testing |
| **Human Rights Act 1998** | Compliant (by design) | Human oversight, fair trial protections |
| **Freedom of Information (Scotland) Act 2002** | Compliant | ATRS publication, transparency |
| **Scottish Government AI Strategy** | Compliant (by design) | Architecture principles, governance |
| **Scottish Cyber Resilience Framework** | Compliant (by design) | Security controls, NFR-SEC |

### 18.2 Standards Alignment

| Standard | Alignment | Evidence |
|----------|-----------|----------|
| **CDDO Algorithmic Transparency Standard** | Fully aligned | This ATRS record |
| **ISO 27001** | Aligned (vendor certified) | Azure certification |
| **ISO 27701** | Aligned | Privacy controls in design |
| **WCAG 2.2 Level AA** | Aligned | Accessibility requirements (NFR-U-001) |
| **NCSC Cloud Security Principles** | Aligned | Azure UK compliance |

### 18.3 Audit Trail

| Audit Field | Captured | Retention | Location |
|-------------|----------|-----------|----------|
| User identity | Yes | 7 years | Audit log |
| Timestamp (UTC, ms) | Yes | 7 years | Audit log |
| Operation type | Yes | 7 years | Audit log |
| Input reference | Yes | 7 years | Audit log |
| AI output summary | Yes | 7 years | Audit log |
| Confidence score | Yes | 7 years | Audit log |
| Model version | Yes | 7 years | Audit log |
| Human decision | Yes | 7 years | Audit log |

---

## 19. Performance Monitoring

### 19.1 Key Performance Indicators

| KPI | Target | Current | Trend | Status |
|-----|--------|---------|-------|--------|
| Document classification accuracy | ≥90% | TBD | TBD | Pre-deployment |
| Translation accuracy (legal terms) | ≥85% | TBD | TBD | Pre-deployment |
| System availability | ≥99.5% | TBD | TBD | Pre-deployment |
| Document processing time | <10s (p95) | TBD | TBD | Pre-deployment |
| Human override rate | Monitor | TBD | TBD | Pre-deployment |
| User satisfaction | ≥80% | TBD | TBD | Pre-deployment |
| Court record incidents | 0 | 0 | N/A | ✅ |

### 19.2 Model Performance Monitoring

| Metric | Baseline | Current | Threshold | Action |
|--------|----------|---------|-----------|--------|
| Classification accuracy | 90% | TBD | <85% | Retrain |
| Translation accuracy (per language) | 85% | TBD | <80% | Review, escalate |
| Transcription WER | 5% | TBD | >10% | Investigate |
| Confidence score distribution | TBD | TBD | Significant shift | Investigate |

### 19.3 Drift Detection

**Model Drift Monitoring:**
- Confidence score distribution monitored for shifts
- Accuracy metrics tracked against baseline
- Human override rate monitored for anomalies
- Automated alerts when thresholds exceeded

**Data Drift Monitoring:**
- Document type distribution tracked
- Language usage patterns tracked
- Input quality metrics monitored

---

## 20. Review and Updates

### 20.1 Review Schedule

| Review Type | Frequency | Next Due | Owner |
|-------------|-----------|----------|-------|
| ATRS content review | Annual | 2027-01-17 | CDiO |
| Technical accuracy review | 6-monthly | 2026-07-17 | AI Architect |
| Compliance review | Annual | 2027-01-17 | DPO |
| Governance review | Quarterly | 2026-04-17 | Chief Executive |

### 20.2 Update Triggers

This ATRS record must be updated when:
- [ ] Significant change to AI capabilities (new model, new use case)
- [ ] Change to data processing (new data types, new sources)
- [ ] Governance structure changes
- [ ] Incident requiring public communication
- [ ] Regulatory guidance changes
- [ ] Annual review due

### 20.3 Version History

| Version | Date | Author | Summary of Changes |
|---------|------|--------|-------------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation |

---

## 21. Traceability to ArcKit Artifacts

### 21.1 Source Artifacts

| Artifact | Reference | Information Used |
|----------|-----------|------------------|
| Architecture Principles | `.arckit/memory/architecture-principles.md` | Principles 2, 7, 8, 9, 11, 12 |
| Stakeholder Drivers | `projects/001-scts-genai-programme/stakeholder-drivers.md` | Accountability, affected parties |
| Requirements | `projects/001-scts-genai-programme/requirements.md` | Functional and non-functional requirements |
| Data Model | `projects/001-scts-genai-programme/data-model.md` | Data entities, PII inventory |
| DPIA | `projects/001-scts-genai-programme/dpia.md` | Risk assessment, lawful basis |
| AI Playbook Assessment | `projects/001-scts-genai-programme/ai-playbook-assessment.md` | Compliance status, blocking issues |
| Research Findings | `projects/001-scts-genai-programme/research-findings.md` | Technology selection, vendor details |

### 21.2 Requirements Traceability

| ATRS Section | Requirement ID | Requirement Summary |
|--------------|----------------|---------------------|
| Human Control | FR-003 | Human review and override |
| Human Control | BR-003 | Court record protection |
| Transparency | FR-011 | AI output labelling |
| Audit | FR-012, NFR-C-002 | Audit trail |
| Security | NFR-SEC-001 to 006 | Security controls |
| Accessibility | NFR-U-001 | WCAG 2.2 AA |
| Data Residency | TC-4, NFR-SEC-004 | UK data only |
| Consent | FR-015 | Translation consent |
| Fallback | FR-014 | Manual fallback mode |

---

## 22. Publication Checklist

### 22.1 Pre-Publication Requirements

| Requirement | Status | Owner | Date |
|-------------|--------|-------|------|
| [ ] Tier 1 plain English review | Pending | Comms team | TBD |
| [ ] Tier 2 technical accuracy review | Pending | AI Architect | TBD |
| [ ] Legal review | Pending | Legal Services | TBD |
| [ ] DPO review | Pending | DPO | TBD |
| [ ] SRO approval | Pending | Chief Executive | TBD |
| [ ] Accessibility check | Pending | CDiO | TBD |
| [ ] Welsh/Gaelic translation (if required) | TBD | Comms team | TBD |

### 22.2 Publication Details

| Field | Value |
|-------|-------|
| **Publication URL** | TBD (SCTS website) |
| **Publication Date** | TBD (Target: 2026-Q2) |
| **Format** | HTML (web) + PDF (download) |
| **Contact for queries** | dpo@scotcourts.gov.uk |

### 22.3 Next Steps

1. **Immediate (2026-Q1)**
   - [ ] Complete DPO review of ATRS
   - [ ] Complete Legal review of ATRS
   - [ ] Complete plain English review of Tier 1
   - [ ] Obtain SRO approval

2. **Before Production (2026-Q2)**
   - [ ] Complete bias audit results (add to Section 13.4)
   - [ ] Complete test results (add to Section 15.3)
   - [ ] Publish ATRS on SCTS website
   - [ ] Update privacy notice

3. **Post-Publication**
   - [ ] Monitor for public enquiries
   - [ ] Schedule first annual review (2027-01-17)

---

## Sign-Off

### Draft Approval

| Role | Name | Decision | Date | Signature |
|------|------|----------|------|-----------|
| **Senior Responsible Owner** | Chief Executive, SCTS | [PENDING] | | ____________ |
| **Programme Owner** | Chief Digital Information Officer | [PENDING] | | ____________ |
| **Data Protection Officer** | DPO, SCTS | [PENDING] | | ____________ |
| **Legal Review** | Legal Services Director, SCTS | [PENDING] | | ____________ |

### Publication Approval

| Approver | Decision | Date |
|----------|----------|------|
| Chief Executive | [PENDING] | |

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.atrs` command
**Generated on**: 2026-01-17
**ArcKit Version**: 0.6.0
**Project**: SCTS GenAI Programme (Project 001)
**AI Model**: Claude Opus 4.5

**Traceability**: This ATRS record is traceable to architecture principles, stakeholder drivers, requirements, data model, DPIA, and AI Playbook assessment via the ArcKit governance framework.

---

**END OF ATRS RECORD**
