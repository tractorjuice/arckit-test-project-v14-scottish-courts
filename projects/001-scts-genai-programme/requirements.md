# Project Requirements: SCTS GenAI Programme

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Business and Technical Requirements |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-01-17 |
| **Last Modified** | 2026-01-17 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-02-17 |
| **Owner** | Chief Digital Information Officer, SCTS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | CDi Function, Architecture Team, Legal Services, DPO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.requirements` command | [PENDING] | [PENDING] |

## Document Purpose

This document defines the business, functional, non-functional, data, and integration requirements for the Scottish Courts and Tribunals Service (SCTS) GenAI Programme. These requirements will guide vendor selection, architecture design, development, and acceptance testing for AI capabilities in document intelligence, speech services, translation, and cognitive search.

---

## Executive Summary

### Business Context

The Scottish Courts and Tribunals Service (SCTS) is embarking on a pioneering programme to introduce AI and automation across key services. The justice system faces growing demand, case backlogs, and the need to improve access for diverse populations including non-English speakers and vulnerable court users. Manual document processing consumes significant staff time and creates bottlenecks in case progression.

This programme aims to deploy responsible AI capabilities that enhance operational efficiency while maintaining the integrity of judicial processes and court records. Initial focus areas include document intelligence for automated extraction and classification, multilingual speech transcription and translation, and cognitive search across court documentation.

The programme must balance innovation ambition with the conservative risk appetite appropriate for a justice environment. All AI capabilities must support—never replace—human decision-making, particularly for matters affecting legal proceedings or individual rights.

### Objectives

- **OBJ-1**: Deploy AI-powered document intelligence to reduce manual document processing time by 60%
- **OBJ-2**: Enable multilingual court access through AI-assisted transcription and translation for the 10 most common non-English languages in Scottish courts
- **OBJ-3**: Implement cognitive search enabling semantic search, case law citation, and document similarity analysis
- **OBJ-4**: Establish enterprise AI platform capabilities that can be extended to future use cases
- **OBJ-5**: Maintain zero AI-related court record integrity incidents throughout the programme

### Expected Outcomes

- **O-1**: Improved access to justice - 20% improvement in Access to Justice Index (Traces to Goal G-1, G-2)
- **O-2**: Operational efficiency gains - 25% improvement in cases processed per FTE (Traces to Goal G-1, G-3)
- **O-3**: Maintained judicial confidence - Zero incidents affecting judicial independence or court records (Traces to Goal G-4)
- **O-4**: Regulatory compliance and trust - 100% compliance with Scottish Government AI Strategy and UK GDPR (Traces to Goal G-5)

### Project Scope

**In Scope**:
- Document Intelligence for civil and criminal case documents
- Speech-to-text transcription with multilingual support
- Translation services for court proceedings (AI-assisted with human oversight)
- Cognitive search across court document repositories
- Integration with existing case management systems
- AI platform infrastructure and governance framework

**Out of Scope**:
- AI for judicial decision-making or case outcome prediction
- Replacement of human interpreters for complex/sensitive matters
- Automated case progression without human approval
- AI processing of restricted security classification documents
- AI systems for other Scottish Government bodies

---

## Stakeholders

| Stakeholder | Role | Organization | Involvement Level |
|-------------|------|--------------|-------------------|
| Chief Executive | Executive Sponsor | SCTS Leadership | Decision maker |
| Chief Digital Information Officer | Programme Owner | CDi Function | Day-to-day leadership |
| Lord President | Judicial Oversight | Judiciary | Judicial confidence |
| Senior AI Technical Architect | Technical Lead | CDi Function | Architecture, PoC delivery |
| Legal Services Director | Compliance | Corporate Services | Legal risk assessment |
| Data Protection Officer | Privacy Compliance | Corporate Services | DPIA, UK GDPR |
| Finance Director | Budget Approval | Corporate Services | ROI validation |
| Court Administration Managers | Business SME | Court Operations | Requirements input |
| Clerks of Court | End Users | Court Operations | User acceptance |
| Cabinet Secretary for Justice | Ministerial Accountability | Scottish Government | Political oversight |

---

## Business Requirements

### BR-001: Improve Court Operational Efficiency

**Description**: The system must demonstrably improve operational efficiency by automating repetitive document processing tasks, reducing staff time spent on manual activities.

**Rationale**: SCTS faces case backlogs and resource constraints. Automation can release staff capacity for higher-value work without reducing headcount. This addresses stakeholder driver SD-2 (Chief Executive efficiency) and SD-5 (Court Admin workload).

**Success Criteria**:
- Reduce average document processing time by 60% (from 4.5 hours to 1.8 hours)
- Reduce document backlog by 40% within 12 months of deployment
- Achieve 80% staff adoption rate within 6 months
- Demonstrate net workload reduction in staff surveys

**Priority**: MUST_HAVE

**Stakeholder**: Chief Executive (Traces to Goal G-1, Outcome O-2)

**Principle Alignment**: Aligns with Principle 4 (Scalability), Principle 5 (Resilience)

---

### BR-002: Enhance Access to Justice for Non-English Speakers

**Description**: The system must reduce language barriers for non-English speaking court users through AI-assisted translation and transcription services.

**Rationale**: Scotland's courts serve diverse populations. Non-English speakers face barriers to justice participation. AI translation can improve access while reducing reliance on interpreter availability. This addresses stakeholder driver SD-11 (Court user access) and SD-10 (Cabinet Secretary commitment).

**Success Criteria**:
- Support real-time transcription and translation for 10 most common non-English languages
- Reduce interpreter booking delays by 30% for supported languages
- Achieve 85% accuracy in legal terminology translation (validated by human interpreters)
- Maintain human interpreter backup for complex or sensitive matters

**Priority**: MUST_HAVE

**Stakeholder**: Cabinet Secretary for Justice (Traces to Goal G-2, Outcome O-1)

**Principle Alignment**: Aligns with Principle 3 (Accessibility), Principle 8 (AI Transparency)

---

### BR-003: Protect Court Record Integrity

**Description**: The system must never alter, corrupt, or misattribute official court records. AI-generated content must be clearly distinguished from authoritative court documentation.

**Rationale**: Court records are legal documents with evidentiary weight. Any AI-related integrity failure would undermine judicial confidence and could affect case outcomes. This is non-negotiable. This addresses stakeholder driver SD-1 (Lord President judicial confidence) and SD-7 (Legal Services risk).

**Success Criteria**:
- Zero incidents where AI processing corrupts or alters court records
- 100% audit trail coverage for all AI operations on court documents
- All AI outputs stored separately from official court records
- Human approval required before any AI content enters official records

**Priority**: MUST_HAVE

**Stakeholder**: Lord President (Traces to Goal G-4, Outcome O-3)

**Principle Alignment**: Aligns with Principle 14 (Court Records Integrity), Principle 2 (Human-in-the-Loop)

---

### BR-004: Achieve Regulatory Compliance

**Description**: The system must comply with UK GDPR, Data Protection Act 2018, Scottish Government AI Strategy, and Cyber Resilience Framework.

**Rationale**: SCTS is a Scottish public body accountable to Scottish Government. Compliance protects SCTS from regulatory action and ensures ethical AI deployment. This addresses stakeholder driver SD-8 (DPO compliance) and SD-13 (ICO compliance).

**Success Criteria**:
- Complete DPIA for each AI capability before deployment
- Achieve 100% compliance with Scottish Government AI Strategy requirements
- Pass Cyber Resilience Framework assessment
- Zero ICO enforcement actions or regulatory findings

**Priority**: MUST_HAVE

**Stakeholder**: Data Protection Officer (Traces to Goal G-5, Outcome O-4)

**Principle Alignment**: Aligns with Principle 12 (Data Protection), Principle 13 (Scottish Public Sector Standards)

---

### BR-005: Demonstrate Value for Money

**Description**: The system must deliver demonstrable return on investment through quantified efficiency gains and cost savings.

**Rationale**: Public sector finance requires demonstrable value for money. AI investment must compete with other priorities and show quantifiable benefits. This addresses stakeholder driver SD-9 (Finance Director value).

**Success Criteria**:
- Achieve positive ROI within 24 months of initial deployment
- Demonstrate £500K annual productivity value through efficiency gains
- Reduce interpreter costs by £200K annually through supported language coverage
- Maintain predictable, controllable operational costs with monthly variance <10%

**Priority**: SHOULD_HAVE

**Stakeholder**: Finance Director (Traces to Outcome O-2)

**Principle Alignment**: Aligns with Principle 18 (Cost Transparency)

---

### BR-006: Enable Staff Adoption and Confidence

**Description**: The system must achieve high staff adoption through intuitive tools, comprehensive training, and clear communication about job security.

**Rationale**: Staff adoption determines AI success. If staff resist or don't use AI tools, benefits won't materialise. This addresses stakeholder driver SD-5 (Court Admin workload) and SD-6 (Clerk job security).

**Success Criteria**:
- Achieve 75% positive staff satisfaction within 6 months of each deployment
- Complete training for 100% of affected staff before rollout
- Demonstrate net workload reduction in staff surveys
- Zero job losses directly attributed to AI automation

**Priority**: MUST_HAVE

**Stakeholder**: HR Director (Traces to Goal G-6, Outcome O-2)

**Principle Alignment**: Aligns with Principle 19 (Iterative Delivery)

---

## Functional Requirements

### User Personas

#### Persona 1: Court Clerk (Primary User)
- **Role**: Clerk of Court, processes documents, schedules hearings, handles enquiries
- **Goals**: Complete document processing efficiently, reduce repetitive tasks, serve court users well
- **Pain Points**: Manual document categorisation, large backlogs, time pressure, varying document quality
- **Technical Proficiency**: Medium (experienced with court systems, varying digital skills)
- **Stakeholder Driver**: SD-6 (Reliable tools and job security)

#### Persona 2: Court Administration Manager
- **Role**: Manages court operations, supervises clerks, responsible for service delivery
- **Goals**: Reduce backlogs, improve team efficiency, ensure quality, manage change
- **Pain Points**: Resource constraints, overtime, staff fatigue, performance pressure
- **Technical Proficiency**: Medium-High
- **Stakeholder Driver**: SD-5 (Workload reduction)

#### Persona 3: Legal Professional (External User)
- **Role**: Advocate, solicitor, or legal representative appearing in court
- **Goals**: Access case information, search precedents, understand AI involvement in documents
- **Pain Points**: Finding relevant documents, understanding AI-processed content, professional liability
- **Technical Proficiency**: Medium (legal expertise, varying digital skills)
- **Stakeholder Driver**: SD-12 (Professional practice)

#### Persona 4: Court User (Public)
- **Role**: Litigant, witness, or member of public accessing court services
- **Goals**: Understand proceedings, access services in preferred language, receive fair treatment
- **Pain Points**: Language barriers, complex processes, lack of information, intimidating environment
- **Technical Proficiency**: Low-Medium (diverse population)
- **Stakeholder Driver**: SD-11 (Access to justice)

#### Persona 5: AI Technical Architect (System Administrator)
- **Role**: Senior AI Technical Architect, designs and maintains AI platform
- **Goals**: Deliver reliable AI capabilities, establish architecture patterns, ensure compliance
- **Pain Points**: Integration complexity, governance requirements, technology selection
- **Technical Proficiency**: High (AI/ML expertise)
- **Stakeholder Driver**: SD-4 (Technical excellence)

---

### Use Cases

#### UC-1: Automated Document Classification

**Actor**: Court Clerk

**Preconditions**:
- Document received (physical or digital)
- Clerk logged into case management system
- AI Document Intelligence service available

**Main Flow**:
1. Clerk uploads or scans document into system
2. System sends document to AI Document Intelligence service
3. AI extracts document type, key entities, and metadata
4. AI returns classification with confidence score
5. System displays AI classification for clerk review
6. Clerk confirms or corrects classification
7. System attaches document to case file with audit trail

**Postconditions**:
- Document classified and attached to correct case
- Audit trail records AI classification and human confirmation
- Processing time logged for efficiency metrics

**Alternative Flows**:
- **Alt 5a**: If confidence score < 80%, system highlights for manual review
- **Alt 6a**: If clerk corrects classification, feedback logged for model improvement

**Exception Flows**:
- **Ex 1**: If AI service unavailable, fallback to manual classification with notification

**Business Rules**:
- AI classification is recommendation only; clerk has final authority
- Court record documents require separate storage for AI outputs
- Confidence score must be displayed with classification

**Priority**: CRITICAL

---

#### UC-2: Real-Time Translation in Court Proceedings

**Actor**: Court Clerk, Court User (non-English speaker)

**Preconditions**:
- Court session scheduled with non-English speaking participant
- Language identified and supported by AI translation
- Human interpreter on standby for complex matters

**Main Flow**:
1. Clerk activates translation service for session
2. System begins real-time speech capture
3. AI transcribes speech to text in source language
4. AI translates text to target language
5. System displays translated text on participant's screen
6. Participant can flag translation issues
7. Session ends; transcript saved with translation

**Postconditions**:
- Full transcript with translations available for record
- Translation quality logged for review
- Human interpreter involvement documented if escalated

**Alternative Flows**:
- **Alt 3a**: If speech quality poor, system requests clarification
- **Alt 6a**: If participant flags issue, human interpreter reviews and corrects

**Exception Flows**:
- **Ex 1**: If AI service unavailable, revert to human interpreter only
- **Ex 2**: If legal terminology unclear, escalate to human interpreter

**Business Rules**:
- AI translation for routine procedural matters only
- Complex legal testimony requires human interpreter verification
- Participant consent required for AI translation use
- Translation marked as AI-assisted in court record

**Priority**: HIGH

---

#### UC-3: Cognitive Search for Case Research

**Actor**: Legal Professional, Court Clerk

**Preconditions**:
- User authenticated with appropriate access permissions
- Search index up to date with court documents
- User has valid search query

**Main Flow**:
1. User enters search query in natural language
2. System processes query using semantic understanding
3. AI returns ranked results with relevance scores
4. User reviews results and previews documents
5. User selects relevant documents for detailed review
6. System logs search and selection for analytics

**Postconditions**:
- User has found relevant documents
- Search analytics updated
- No unauthorised document access occurred

**Alternative Flows**:
- **Alt 3a**: If no results found, system suggests alternative search terms
- **Alt 4a**: User can filter by date, case type, court level

**Exception Flows**:
- **Ex 1**: If user attempts to access restricted document, access denied with audit log

**Business Rules**:
- Search results respect document security classifications
- User access limited to documents within their authorised scope
- Search index is derived data, not authoritative source

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-001: Document Upload and Ingestion

**Description**: The system must accept documents in multiple formats for AI processing.

**Relates To**: BR-001, UC-1

**Acceptance Criteria**:
- [ ] Given a PDF document, when uploaded, then AI processing initiated within 5 seconds
- [ ] Given a scanned image (TIFF, JPEG, PNG), when uploaded, then OCR applied before AI processing
- [ ] Given a Word document (DOCX, DOC), when uploaded, then text extracted for AI processing
- [ ] Given an unsupported format, when uploaded, then user notified and manual processing triggered

**Data Requirements**:
- **Inputs**: Document file (PDF, TIFF, JPEG, PNG, DOCX, DOC), case reference, user ID
- **Outputs**: Processing status, document ID, initial metadata
- **Validations**: File size < 100MB, file type in allowed list, virus scan passed

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: Infrastructure for file storage (DR-001)

---

#### FR-002: AI Document Classification

**Description**: The system must automatically classify documents by type and extract key metadata.

**Relates To**: BR-001, UC-1

**Acceptance Criteria**:
- [ ] Given a civil court document, when processed, then correct document type identified (claim, defence, evidence, etc.)
- [ ] Given a criminal court document, when processed, then correct document type identified (indictment, plea, judgement, etc.)
- [ ] Given any document, when processed, then key entities extracted (parties, dates, case numbers, amounts)
- [ ] Given low-quality scan, when processed, then quality warning displayed with confidence score

**Data Requirements**:
- **Inputs**: Document content, document format
- **Outputs**: Document classification, confidence score, extracted entities, quality assessment
- **Validations**: Confidence score provided, classification from approved taxonomy

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-001 (Document Upload), trained classification model

---

#### FR-003: Human Review and Override

**Description**: The system must display AI outputs for human review and allow override of AI recommendations.

**Relates To**: BR-003, UC-1, Principle 2 (Human-in-the-Loop)

**Acceptance Criteria**:
- [ ] Given AI classification, when displayed, then confidence score visible alongside recommendation
- [ ] Given AI classification, when clerk disagrees, then clerk can select alternative classification
- [ ] Given override, when submitted, then original AI classification and override both logged
- [ ] Given low confidence (<80%), when displayed, then visual indicator highlighting need for review

**Data Requirements**:
- **Inputs**: AI classification, confidence score, user decision
- **Outputs**: Final classification (human-approved), audit record
- **Validations**: User confirmation required for all classifications

**Priority**: MUST_HAVE

**Complexity**: LOW

**Dependencies**: FR-002 (AI Classification)

---

#### FR-004: Speech-to-Text Transcription

**Description**: The system must transcribe spoken audio to text with support for multiple accents and languages.

**Relates To**: BR-002, UC-2

**Acceptance Criteria**:
- [ ] Given clear audio in English, when transcribed, then 95% word accuracy achieved
- [ ] Given clear audio in supported non-English language, when transcribed, then 90% word accuracy achieved
- [ ] Given audio with background noise, when transcribed, then confidence indicators shown for uncertain segments
- [ ] Given multiple speakers, when transcribed, then speaker diarisation identifies different speakers

**Data Requirements**:
- **Inputs**: Audio stream or file, language code, speaker count (if known)
- **Outputs**: Transcript text, timestamps, speaker labels, confidence scores
- **Validations**: Audio quality assessment before processing

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Audio capture infrastructure, supported language models

---

#### FR-005: Real-Time Translation

**Description**: The system must translate transcribed text between supported languages in near real-time.

**Relates To**: BR-002, UC-2

**Acceptance Criteria**:
- [ ] Given English text, when translated to supported language, then translation appears within 2 seconds
- [ ] Given legal terminology, when translated, then legal glossary applied for accuracy
- [ ] Given translation, when displayed, then original text also available for comparison
- [ ] Given uncertain translation, when detected, then flagged for human interpreter review

**Data Requirements**:
- **Inputs**: Source text, source language, target language
- **Outputs**: Translated text, confidence score, terminology flags
- **Validations**: Language pair in supported list

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-004 (Transcription), translation models for supported languages

---

#### FR-006: Supported Languages Configuration

**Description**: The system must support configuration of languages for transcription and translation.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given language list requirement, when configured, then system supports 10+ languages
- [ ] Given new language requirement, when added, then deployable without core system change
- [ ] Given language accuracy data, when available, then accuracy metrics displayed per language
- [ ] Given language demand data, when analysed, then prioritisation recommendations generated

**Priority Languages** (based on Scottish court demographics):
1. Polish
2. Urdu
3. Punjabi
4. Arabic
5. Mandarin Chinese
6. Cantonese
7. Romanian
8. Bengali
9. Russian
10. British Sign Language (BSL) interpretation support

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: Language model availability

---

#### FR-007: Semantic Search

**Description**: The system must support natural language search queries with semantic understanding.

**Relates To**: BR-001, UC-3

**Acceptance Criteria**:
- [ ] Given natural language query, when searched, then semantically relevant results returned
- [ ] Given legal terminology query, when searched, then domain-specific understanding applied
- [ ] Given ambiguous query, when searched, then related concepts suggested
- [ ] Given search results, when displayed, then relevance score shown for each result

**Data Requirements**:
- **Inputs**: Search query text, filters (date range, case type, court level)
- **Outputs**: Ranked document list, relevance scores, snippets, facets
- **Validations**: Query length limits, authorised scope filtering

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Document indexing (FR-008), access control (NFR-SEC-2)

---

#### FR-008: Document Indexing

**Description**: The system must index documents for search with extracted text and metadata.

**Relates To**: FR-007, UC-3

**Acceptance Criteria**:
- [ ] Given new document added to case management, when indexed, then searchable within 15 minutes
- [ ] Given document update, when re-indexed, then previous version marked and new version searchable
- [ ] Given document deletion, when processed, then removed from search index
- [ ] Given document with security classification, when indexed, then access restrictions preserved

**Data Requirements**:
- **Inputs**: Document content, metadata, security classification, case reference
- **Outputs**: Search index entry with vectors, metadata, access control list
- **Validations**: Index synchronised with source system

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: Integration with case management (INT-001)

---

#### FR-009: Case Law Citation Detection

**Description**: The system must identify and link case law citations within documents.

**Relates To**: UC-3

**Acceptance Criteria**:
- [ ] Given document with case citations, when processed, then citations extracted and linked
- [ ] Given Scottish case citation format, when detected, then linked to case record if available
- [ ] Given UK Supreme Court/England & Wales citation, when detected, then external reference provided
- [ ] Given citation, when clicked, then target case summary displayed

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: FR-007 (Search), case citation database/API

---

#### FR-010: Document Similarity Analysis

**Description**: The system must identify documents similar to a selected document.

**Relates To**: UC-3

**Acceptance Criteria**:
- [ ] Given a document, when similarity requested, then top 10 similar documents returned
- [ ] Given similar documents, when displayed, then similarity score and matching aspects shown
- [ ] Given different case types, when compared, then cross-type similarities identified where relevant

**Priority**: COULD_HAVE

**Complexity**: HIGH

**Dependencies**: FR-008 (Document Indexing), vector similarity capability

---

#### FR-011: AI Output Labelling

**Description**: All AI-generated or AI-assisted outputs must be clearly labelled as such.

**Relates To**: BR-003, Principle 8 (AI Transparency)

**Acceptance Criteria**:
- [ ] Given AI classification, when displayed, then "AI-Assisted" label visible
- [ ] Given AI translation, when displayed, then "AI Translation" label visible with accuracy note
- [ ] Given AI search results, when displayed, then "AI-Ranked" indicator shown
- [ ] Given any AI output, when exported/printed, then AI provenance included in output

**Priority**: MUST_HAVE

**Complexity**: LOW

**Dependencies**: All AI functional requirements

---

#### FR-012: Audit Trail for AI Operations

**Description**: The system must maintain comprehensive audit trail for all AI operations.

**Relates To**: BR-003, BR-004, Principle 2 (Human-in-the-Loop)

**Acceptance Criteria**:
- [ ] Given any AI operation, when executed, then audit record created with timestamp
- [ ] Given audit record, when queried, then includes: user, action, input, output, model version
- [ ] Given human override, when recorded, then original AI output and override both captured
- [ ] Given audit query, when authorised user requests, then full history retrievable

**Data Requirements**:
- **Inputs**: Operation type, input data reference, user ID, timestamp
- **Outputs**: Audit record with all required fields
- **Validations**: Audit records immutable (append-only)

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: Audit logging infrastructure (NFR-C-2)

---

#### FR-013: Quality Feedback Mechanism

**Description**: Users must be able to provide feedback on AI output quality for continuous improvement.

**Relates To**: Principle 10 (Data Quality for AI)

**Acceptance Criteria**:
- [ ] Given AI output, when reviewed, then user can rate quality (good/needs improvement/incorrect)
- [ ] Given quality feedback, when submitted, then logged for model improvement analysis
- [ ] Given aggregated feedback, when analysed, then model performance reports generated
- [ ] Given consistent errors, when detected, then alert raised for model review

**Priority**: SHOULD_HAVE

**Complexity**: LOW

**Dependencies**: FR-012 (Audit Trail)

---

#### FR-014: Manual Fallback Mode

**Description**: The system must support operation without AI services when unavailable.

**Relates To**: BR-003, Principle 5 (Resilience and Continuity)

**Acceptance Criteria**:
- [ ] Given AI service unavailable, when document uploaded, then manual classification workflow available
- [ ] Given AI service unavailable, when translation needed, then human interpreter notification triggered
- [ ] Given AI service unavailable, when search attempted, then keyword search fallback available
- [ ] Given AI service restored, when detected, then automatic resumption of AI-assisted mode

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: All AI functional requirements

---

#### FR-015: Consent Management for Translation

**Description**: Court users must consent to AI translation use and understand limitations.

**Relates To**: BR-004, Principle 8 (AI Transparency)

**Acceptance Criteria**:
- [ ] Given court session with AI translation, when participant arrives, then consent form presented
- [ ] Given consent form, when displayed, then explains AI use, accuracy, and human backup
- [ ] Given participant declines AI, when recorded, then human interpreter only used
- [ ] Given consent, when given, then recorded in session record

**Priority**: MUST_HAVE

**Complexity**: LOW

**Dependencies**: UC-2 (Translation use case)

---

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Document Processing Response Time

**Requirement**: AI document classification must return results within acceptable time limits.
- Document classification: < 10 seconds (95th percentile) for documents up to 50 pages
- Large document (>50 pages): < 30 seconds (95th percentile)
- Batch processing: 500 documents per hour minimum

**Measurement Method**: Application performance monitoring with timestamp logging

**Load Conditions**:
- Peak load: 100 concurrent document uploads
- Average load: 2,000 documents per day
- Document size: 80% < 20 pages, 15% 20-50 pages, 5% > 50 pages

**Priority**: HIGH

**Principle Alignment**: Principle 4 (Scalability)

**Stakeholder Traceability**: Supports Goal G-1 (Document processing time reduction)

---

#### NFR-P-002: Translation Latency

**Requirement**: Real-time translation must provide near-synchronous output.
- Transcription latency: < 500ms from speech to text display
- Translation latency: < 2 seconds from source text to translated text
- End-to-end: < 3 seconds from speech to translated text

**Measurement Method**: Timestamp logging at each processing stage

**Priority**: HIGH

**Stakeholder Traceability**: Supports Goal G-2 (Multilingual access)

---

#### NFR-P-003: Search Response Time

**Requirement**: Cognitive search must return results quickly.
- Simple query: < 2 seconds (95th percentile)
- Complex query with filters: < 5 seconds (95th percentile)
- Typeahead suggestions: < 200ms

**Measurement Method**: Search latency metrics in application monitoring

**Load Conditions**:
- Index size: 5 million documents initial, growing 500K per year
- Concurrent searches: 50 peak

**Priority**: HIGH

**Stakeholder Traceability**: Supports Goal G-3 (Cognitive search)

---

### Availability and Resilience Requirements

#### NFR-A-001: System Availability

**Requirement**: AI services must achieve high availability during court operating hours.
- Availability target: 99.5% during court hours (Mon-Fri 09:00-17:00)
- Maximum planned downtime: 4 hours per month (outside court hours)
- Maximum unplanned downtime: 2 hours per month during court hours

**Maintenance Windows**: Saturday 22:00 - Sunday 06:00

**Priority**: HIGH

**Principle Alignment**: Principle 5 (Resilience and Continuity)

---

#### NFR-A-002: Disaster Recovery

**Requirement**: AI systems must be recoverable within defined objectives.

**RPO (Recovery Point Objective)**: Maximum 1 hour data loss for AI audit logs

**RTO (Recovery Time Objective)**: Maximum 4 hours for AI service restoration

**Backup Requirements**:
- AI model backups: Daily
- Configuration backups: With every change
- Audit log backups: Real-time replication
- Geographic backup: UK secondary region

**Priority**: HIGH

**Principle Alignment**: Principle 5 (Resilience and Continuity)

---

#### NFR-A-003: Graceful Degradation

**Requirement**: AI service failures must not block court operations.

**Resilience Patterns Required**:
- [x] Circuit breaker for AI service calls (trip after 5 failures in 30 seconds)
- [x] Retry with exponential backoff (3 retries, 1s/2s/4s)
- [x] Timeout on all AI calls (30 second maximum)
- [x] Fallback to manual processing when AI unavailable
- [x] Health check endpoints for monitoring

**Priority**: CRITICAL

**Principle Alignment**: Principle 5 (Resilience and Continuity)

**Stakeholder Traceability**: Supports SD-1 (Lord President - courts must function without AI)

---

### Scalability Requirements

#### NFR-S-001: Horizontal Scaling

**Requirement**: AI services must scale horizontally to meet demand.

**Growth Projections**:
- Year 1: 500K documents processed, 100 translation sessions
- Year 2: 1M documents processed, 500 translation sessions
- Year 3: 2M documents processed, 1,000 translation sessions

**Scaling Triggers**: Auto-scale when CPU > 70% or request queue > 100

**Priority**: HIGH

**Principle Alignment**: Principle 4 (Scalability and Elasticity)

---

#### NFR-S-002: Data Volume Scaling

**Requirement**: Search index must handle growing document volumes.

**Requirement**: System must handle search index growth to 10TB over 5 years

**Data Archival Strategy**: Documents > 7 years moved to cold storage, excluded from active search

**Priority**: MEDIUM

---

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: All AI system access must be authenticated via SCTS identity system.

**Authentication Method**: SAML 2.0 SSO integration with SCTS Active Directory

**Multi-Factor Authentication (MFA)**:
- Required for: Administrative access, model deployment, configuration changes
- MFA methods: Microsoft Authenticator, hardware token

**Session Management**:
- Session timeout: 30 minutes inactivity
- Absolute session timeout: 8 hours
- Re-authentication required for: Model deployment, bulk export

**Priority**: CRITICAL

**Principle Alignment**: Principle 11 (Security by Design)

---

#### NFR-SEC-002: Authorization

**Requirement**: Role-based access control with least privilege principle.

**Roles**:
- **Clerk**: Document upload, classification review, basic search
- **Manager**: All clerk functions plus reporting, quality review
- **Legal Professional**: Search, document view (within authorised cases)
- **AI Administrator**: Model deployment, configuration, monitoring
- **Auditor**: Read-only audit log access

**Priority**: CRITICAL

**Principle Alignment**: Principle 11 (Security by Design)

---

#### NFR-SEC-003: Data Encryption

**Requirement**: All data must be encrypted in transit and at rest.

- Data in transit: TLS 1.2+ minimum, TLS 1.3 preferred
- Data at rest: AES-256 encryption for all data stores
- Key management: Cloud provider key management with SCTS-managed keys

**Encryption Scope**:
- [x] AI model storage encryption
- [x] Document storage encryption
- [x] Search index encryption
- [x] Audit log encryption
- [x] Backup encryption

**Priority**: CRITICAL

**Principle Alignment**: Principle 11 (Security by Design)

---

#### NFR-SEC-004: Data Residency

**Requirement**: All court data must remain within UK jurisdiction.

**UK Data Residency Requirements**:
- [x] All AI processing in UK data centres
- [x] No data transfer to non-UK locations
- [x] AI model training on UK infrastructure only
- [x] Third-party AI services must guarantee UK processing
- [x] Backup and DR sites within UK

**Priority**: CRITICAL

**Principle Alignment**: Principle 15 (Data Sovereignty and Residency)

---

#### NFR-SEC-005: Vulnerability Management

**Requirement**: Continuous security testing and vulnerability management.

- Dependency scanning: In CI/CD pipeline, block critical/high vulnerabilities
- SAST: Static analysis on all code changes
- DAST: Monthly dynamic testing of deployed services
- Penetration testing: Annual by approved external provider

**Remediation SLA**:
- Critical vulnerabilities: 24 hours
- High vulnerabilities: 7 days
- Medium vulnerabilities: 30 days

**Priority**: HIGH

**Principle Alignment**: Principle 11 (Security by Design)

---

#### NFR-SEC-006: Court Record Protection

**Requirement**: AI systems must have read-only access to court records.

**Access Controls**:
- [x] AI services access court records read-only via API
- [x] No direct database access from AI systems
- [x] AI outputs stored in separate repository from court records
- [x] Write to court record system only through approved integration with human approval

**Priority**: CRITICAL

**Principle Alignment**: Principle 14 (Court Records Integrity)

**Stakeholder Traceability**: Supports Goal G-4 (Zero record integrity incidents)

---

### Compliance and Regulatory Requirements

#### NFR-C-001: UK GDPR Compliance

**Requirement**: Full compliance with UK GDPR and Data Protection Act 2018.

**Applicable Regulations**: UK GDPR, Data Protection Act 2018, Law Enforcement Directive (for criminal data)

**Compliance Requirements**:
- [x] Lawful basis documented for all personal data processing
- [x] Data minimisation - process only necessary data
- [x] Privacy by design in all AI development
- [x] Data subject rights supported (access, deletion, portability)
- [x] DPIA completed before each AI capability deployment
- [x] Data breach notification within 72 hours

**Data Retention**: Aligned with court records retention schedules (minimum 7 years for most case documents)

**Priority**: CRITICAL

**Principle Alignment**: Principle 12 (Data Protection and Privacy)

---

#### NFR-C-002: Audit Logging

**Requirement**: Comprehensive audit trail for all AI operations.

**Audit Log Contents** (for all AI operations):
- Who: User identity (or service account)
- What: AI operation performed (classification, translation, search)
- When: Timestamp (UTC, millisecond precision)
- Input: Reference to input document/data (not content)
- Output: AI result summary with confidence score
- Model: AI model version used
- Decision: Human confirmation/override if applicable

**Log Retention**: 7 years minimum (immutable storage)

**Log Integrity**: Append-only logging with cryptographic integrity

**Priority**: CRITICAL

**Principle Alignment**: Principle 17 (Observability and Monitoring)

---

#### NFR-C-003: Scottish Government Standards

**Requirement**: Compliance with Scottish Government technology and AI standards.

**Standards Required**:
- [x] Scottish Government AI Strategy alignment
- [x] Scottish Cyber Resilience Framework compliance
- [x] Digital Scotland Service Standard
- [x] Scottish Government Cloud First Policy

**Priority**: HIGH

**Principle Alignment**: Principle 13 (Scottish Public Sector Standards)

---

#### NFR-C-004: Algorithmic Transparency

**Requirement**: AI decision-making must be transparent and explainable.

**Transparency Requirements**:
- [x] AI model purpose and limitations documented
- [x] Confidence scores provided with all AI outputs
- [x] Model version tracked and auditable
- [x] Bias assessment completed before deployment
- [x] Public transparency statement about AI use in courts

**Priority**: HIGH

**Principle Alignment**: Principle 8 (AI Transparency and Explainability)

---

### Usability Requirements

#### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all user interfaces.

**Accessibility Features**:
- [x] Keyboard navigation for all functions
- [x] Screen reader compatibility
- [x] High contrast mode
- [x] Adjustable font sizes
- [x] Alt text for images and icons
- [x] Captions for audio content

**Testing**: Automated accessibility testing in CI/CD plus manual testing with assistive technology users

**Priority**: CRITICAL

**Principle Alignment**: Principle 3 (Accessibility and Inclusive Design)

---

#### NFR-U-002: Multilingual Interface

**Requirement**: User interface available in English, Gaelic, and other languages.

**Localization Scope**:
- [x] UI text in English and Scottish Gaelic
- [x] Date/time format per locale
- [x] Error messages localised
- [x] Help content localised

**Priority**: SHOULD_HAVE

**Principle Alignment**: Principle 3 (Accessibility and Inclusive Design)

---

### Maintainability Requirements

#### NFR-M-001: Observability

**Requirement**: Comprehensive monitoring and alerting for AI services.

**Telemetry Requirements**:
- **Logging**: Structured JSON logs, centralised aggregation
- **Metrics**: Request volume, latency (p50/p95/p99), error rates, model confidence distributions
- **Tracing**: Distributed tracing for end-to-end request flows
- **Dashboards**: Real-time operational dashboards for AI services
- **Alerts**: SLO-based alerting with runbooks

**Priority**: HIGH

**Principle Alignment**: Principle 17 (Observability and Monitoring)

---

#### NFR-M-002: Model Governance

**Requirement**: AI models must be version-controlled with formal deployment process.

**Governance Requirements**:
- [x] Model versioning with semantic versioning
- [x] Model testing requirements before deployment
- [x] Approval workflow for model changes
- [x] Rollback capability for model updates
- [x] Performance and fairness baselines for regression testing

**Priority**: HIGH

**Principle Alignment**: Principle 9 (AI Model Governance)

---

#### NFR-M-003: Documentation

**Requirement**: Comprehensive documentation for operators and developers.

**Documentation Types**:
- [x] Architecture documentation (C4 model)
- [x] API documentation (OpenAPI specs)
- [x] Runbooks for operational procedures
- [x] Model cards for each AI model
- [x] User guides for court staff
- [x] Training materials

**Priority**: HIGH

---

---

## Integration Requirements

### INT-001: Case Management System Integration

**Purpose**: Integrate with SCTS case management systems to access documents and case metadata.

**Integration Type**: Real-time API

**Data Exchanged**:
- **From Case Management to AI**: Documents, case metadata, party information
- **From AI to Case Management**: Classification results, extracted metadata (via human approval)

**Integration Pattern**: Request/response API with event notification for new documents

**Authentication**: Service account with OAuth 2.0 client credentials

**Access Mode**: Read-only for AI document access; write-back only for approved outputs via separate integration

**Error Handling**: Retry with circuit breaker; fallback to manual processing

**SLA**: < 1 second response for document retrieval, 99.5% availability

**Owner**: SCTS ICT Operations

**Priority**: CRITICAL

**Principle Alignment**: Principle 6 (Interoperability)

---

### INT-002: Document Management System Integration

**Purpose**: Access documents stored in SCTS document management systems.

**Integration Type**: Real-time API + Event-driven

**Data Exchanged**:
- **From DMS to AI**: Document content, metadata, security classification
- **From AI to DMS**: None directly (AI outputs stored separately)

**Integration Pattern**: REST API for document retrieval; webhook notification for new documents

**Authentication**: Service account with mutual TLS

**Access Mode**: Read-only

**Priority**: CRITICAL

---

### INT-003: Identity Provider Integration

**Purpose**: Authenticate users via SCTS identity system.

**Integration Type**: SAML 2.0 SSO

**Data Exchanged**:
- **From IdP to AI System**: User identity, roles, attributes
- **From AI System to IdP**: Authentication requests

**Integration Pattern**: SAML 2.0 service provider

**Authentication**: SAML assertions with X.509 certificate validation

**Priority**: CRITICAL

---

### INT-004: Court Scheduling System Integration

**Purpose**: Access court session schedules for translation service activation.

**Integration Type**: Real-time API

**Data Exchanged**:
- **From Scheduling to AI**: Session details, language requirements, participant list
- **From AI to Scheduling**: Translation service availability status

**Integration Pattern**: REST API

**Priority**: HIGH

---

### INT-005: Interpreter Booking System Integration

**Purpose**: Coordinate with human interpreter services when AI escalates.

**Integration Type**: Event-driven notification

**Data Exchanged**:
- **From AI to Booking**: Escalation requests, language, urgency, session details
- **From Booking to AI**: Interpreter availability, confirmation

**Integration Pattern**: Message queue for escalation requests

**Priority**: HIGH

---

### INT-006: Cloud AI Services Integration

**Purpose**: Integrate with cloud cognitive services for AI processing.

**Integration Type**: Real-time API

**Data Exchanged**:
- **To Cloud AI**: Document content, audio streams (encrypted)
- **From Cloud AI**: Classification, transcription, translation results

**Integration Pattern**: REST/gRPC API calls

**Authentication**: API keys managed in secrets vault, rotated monthly

**Data Residency**: UK data centres only (contractual requirement)

**Priority**: CRITICAL

**Principle Alignment**: Principle 15 (Data Sovereignty)

---

---

## Data Requirements

### Data Entities

#### Entity: AI Processing Request

**Description**: Record of each AI processing operation.

**Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| request_id | UUID | Yes | Unique identifier | Primary key |
| request_type | Enum | Yes | Type of AI operation | ['classification', 'transcription', 'translation', 'search'] |
| source_document_id | UUID | No | Reference to source document | Foreign key to DMS |
| case_reference | String(50) | No | Court case reference | Case number format |
| user_id | String(100) | Yes | User who initiated request | |
| requested_at | Timestamp | Yes | Request timestamp | UTC |
| status | Enum | Yes | Processing status | ['pending', 'processing', 'completed', 'failed'] |
| completed_at | Timestamp | No | Completion timestamp | UTC |
| model_version | String(50) | Yes | AI model version used | Semantic version |

**Data Classification**: INTERNAL

**Data Retention**: 7 years

---

#### Entity: AI Processing Result

**Description**: Output from AI processing operation.

**Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| result_id | UUID | Yes | Unique identifier | Primary key |
| request_id | UUID | Yes | Link to processing request | Foreign key |
| result_type | Enum | Yes | Type of result | ['classification', 'transcript', 'translation', 'search_results'] |
| result_data | JSON | Yes | Structured result | Schema per result_type |
| confidence_score | Decimal(3,2) | Yes | AI confidence | 0.00 - 1.00 |
| human_reviewed | Boolean | Yes | Whether human reviewed | |
| human_decision | Enum | No | Human override decision | ['accepted', 'modified', 'rejected'] |
| reviewed_by | String(100) | No | User who reviewed | |
| reviewed_at | Timestamp | No | Review timestamp | UTC |

**Data Classification**: INTERNAL

**Data Retention**: 7 years

---

#### Entity: Search Index Entry

**Description**: Indexed document for cognitive search (derived data).

**Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| index_id | UUID | Yes | Unique identifier | Primary key |
| source_document_id | UUID | Yes | Reference to source document | Foreign key to DMS |
| case_reference | String(50) | Yes | Court case reference | |
| document_type | String(100) | Yes | Classified document type | |
| extracted_text | Text | Yes | Full text for search | |
| entities | JSON | No | Extracted entities | |
| embedding_vector | Vector(1536) | Yes | Semantic embedding | |
| indexed_at | Timestamp | Yes | Index timestamp | UTC |
| source_modified_at | Timestamp | Yes | Source document modification | UTC |
| security_classification | Enum | Yes | Access level | ['public', 'internal', 'confidential', 'restricted'] |

**Data Classification**: As per source document

**Data Retention**: Matches source document (derived data)

**Note**: This is derived data, not authoritative source. Source document in DMS is system of record.

---

### Data Quality Requirements

**Data Accuracy**: AI classification accuracy target 90% (measured via human review feedback)

**Data Completeness**: All required fields populated; null handling documented

**Data Consistency**: Search index synchronised with source within 15 minutes

**Data Timeliness**: Real-time for new documents; batch refresh for updates

**Data Lineage**: Source-to-AI-output lineage tracked in audit records

**Principle Alignment**: Principle 10 (Data Quality for AI), Principle 16 (Single Source of Truth)

---

### Data Migration Requirements

**Migration Scope**: No legacy AI data to migrate (new capability)

**Historical Indexing**: Backfill search index with existing documents
- Priority: Civil case documents from last 2 years initially
- Approach: Batch processing during off-peak hours
- Timeline: 3 months for initial backfill

---

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: Must integrate with existing SCTS case management and document systems via their published APIs.

**TC-2**: Must deploy within approved SCTS cloud environment (currently Microsoft Azure).

**TC-3**: Must use SCTS identity system (Active Directory) for authentication.

**TC-4**: All AI processing must occur in UK data centres only.

**TC-5**: AI models must be updateable without core system redevelopment.

---

### Business Constraints

**BC-1**: AI must not make autonomous decisions affecting legal proceedings.

**BC-2**: Human interpreters must remain available for complex/sensitive matters.

**BC-3**: Court operations must continue without disruption if AI services fail.

**BC-4**: Staff cannot be made redundant as direct result of AI automation.

**BC-5**: Must achieve compliance approvals before production deployment.

---

### Assumptions

**A-1**: Cloud AI services meeting UK data residency requirements are available.

**A-2**: Existing case management system APIs provide necessary document access.

**A-3**: Staff will engage with training and change management programme.

**A-4**: Scottish Government AI Strategy guidance will remain stable during implementation.

**A-5**: Network bandwidth sufficient for real-time audio/video processing in courtrooms.

**Validation Plan**: Assumptions validated during PoC phase before production commitment.

---

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Innovation Speed vs Legal Review Thoroughness

**Conflicting Requirements**:
- **Requirement A**: FR-001-015 - Deploy AI capabilities rapidly to demonstrate value
- **Requirement B**: NFR-C-001-004 - Complete thorough compliance and legal review

**Stakeholders Involved**:
- **CDiO (SD-3)**: Wants rapid delivery to establish SCTS as AI leader
- **Legal Services Director (SD-7)**: Requires thorough legal review before deployment

**Nature of Conflict**: Legal review timeline (2-4 months per capability) conflicts with desire for quick PoC delivery.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| Option 1: Prioritise Speed | ✅ Faster value demonstration | ❌ Legal risk, potential rework | CDiO happy, Legal unhappy |
| Option 2: Prioritise Legal | ✅ Reduced legal risk | ❌ Delayed benefits, competitive pressure | Legal happy, CDiO frustrated |
| Option 3: Phase by Risk | ✅ Balance speed and diligence | ❌ Complex planning | Both partially satisfied |

**Resolution Strategy**: PHASE

**Decision**: Start with low-risk use cases (document classification for internal efficiency) while parallel legal review of higher-risk capabilities (speech in proceedings). Legal review timeline built into project plan as dependency.

**Rationale**: Document classification is internal administrative function with lower legal risk. Speech/translation in proceedings requires more legal scrutiny. Phasing enables early wins while ensuring proper review.

**Decision Authority**: Chief Executive (per RACI matrix)

**Impact on Requirements**:
- FR-001-003 (Document Classification): Phase 1 - proceed with standard review
- FR-004-005 (Speech/Translation): Phase 2 - extended legal review required
- Added milestone: Legal approval gate before Phase 2 production

**Stakeholder Management**:
- CDiO: Document classification PoC proceeds on original timeline
- Legal Services: Full review for speech services before any courtroom use

---

### Conflict C-2: Efficiency Automation vs Staff Job Security

**Conflicting Requirements**:
- **Requirement A**: BR-001 - Reduce document processing time by 60%
- **Requirement B**: BR-006 - Zero job losses from AI automation

**Stakeholders Involved**:
- **Court Admin Managers (SD-5)**: Want workload reduction and efficiency
- **Clerks of Court (SD-6)**: Fear job displacement from automation

**Nature of Conflict**: Significant efficiency gains could imply need for fewer staff.

**Resolution Strategy**: INNOVATE

**Decision**: AI automates tasks, not roles. Efficiency gains enable more cases processed, not fewer staff. Explicitly commit that no redundancies will result from AI programme.

**Rationale**: SCTS has case backlogs; efficiency gains address backlogs rather than reduce headcount. Staff redeployed to higher-value activities (public assistance, complex case support).

**Impact on Requirements**:
- BR-001: Success criteria clarified - efficiency enables backlog reduction, not headcount reduction
- BR-006: Explicit statement added - "Zero job losses directly attributed to AI automation"
- Added NFR-U: Training requirements for staff skill development

**Stakeholder Management**:
- Court Admin: Efficiency benefits clearly messaged as backlog reduction
- Clerks: Early communication on job security, involvement in design, skill development opportunities

---

### Conflict C-3: Political Visibility vs Judicial Caution

**Conflicting Requirements**:
- **Requirement A**: Ministerial progress visibility (Cabinet Secretary SD-10)
- **Requirement B**: Conservative deployment protecting judicial confidence (Lord President SD-1)

**Stakeholders Involved**:
- **Cabinet Secretary**: Wants visible progress for parliamentary accountability
- **Lord President**: Requires cautious approach to maintain judicial confidence

**Nature of Conflict**: Ministerial desire for quick announcements conflicts with judicial need for careful, proven deployment.

**Resolution Strategy**: PHASE

**Decision**: Sequence deployment to start with administrative AI (visible progress) before any AI that touches court proceedings (judicial sensitivity).

**Rationale**: Document processing and search are administrative functions that can be announced as progress without judicial concern. Speech/translation in courtrooms requires more judicial buy-in.

**Impact on Requirements**:
- Phase 1 (visible, ministerial-friendly): Document Intelligence, Cognitive Search
- Phase 2 (judicial consultation required): Speech transcription, Translation in proceedings
- Ministerial briefing materials focus on Phase 1 administrative efficiency

**Stakeholder Management**:
- Cabinet Secretary: Positive announcements on Phase 1 administrative AI
- Lord President: Quarterly briefings, consultation before Phase 2 courtroom deployment

---

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Document processing time | 4.5 hours avg | 1.8 hours avg | 18 months post-deploy | Case management timestamps |
| Document backlog | Current volume | 40% reduction | 12 months | Weekly backlog reports |
| Languages supported | 0 | 10 | 24 months | System capability |
| Interpreter cost | Current spend | £200K reduction annually | 24 months | Procurement data |
| Staff satisfaction with AI | N/A | 75% positive | 6 months post-deploy | Staff surveys |
| Court record incidents | 0 | 0 | Ongoing | Incident management |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| AI service availability | 99.5% | Uptime monitoring |
| Document classification accuracy | 90% | Human review feedback |
| Translation accuracy | 85% (legal terms) | Human interpreter validation |
| API response time (p95) | < 10 seconds | APM tooling |
| Search result relevance | 80% satisfaction | User surveys |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| Senior AI Architect | Hire technical lead for programme | CDiO | 2026-Q1 | In progress | HIGH - delays all delivery |
| Case Management API | API access for document retrieval | ICT Operations | 2026-Q2 | Not started | HIGH - blocks document processing |
| Cloud AI Services | UK data residency contracts | Procurement | 2026-Q2 | In progress | HIGH - blocks AI development |
| Legal Review | Compliance approval for speech services | Legal Services | 2026-Q3 | Not started | MEDIUM - delays Phase 2 |
| DPIA Completion | Data protection approval | DPO | 2026-Q2 | Not started | HIGH - blocks production |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | AI classification accuracy below target | MEDIUM | HIGH | Phased rollout with human review, feedback loop | AI Architect |
| R-2 | Staff resistance to AI adoption | MEDIUM | HIGH | Early engagement, training, job security commitment | HR Director |
| R-3 | Judicial loss of confidence | LOW | CRITICAL | Clear scope boundaries, regular briefings, conservative approach | Chief Executive |
| R-4 | UK data residency not achievable | LOW | CRITICAL | Validate cloud provider contracts early, alternative providers | Procurement |
| R-5 | Integration complexity exceeds estimates | MEDIUM | MEDIUM | PoC validation, contingency budget | AI Architect |
| R-6 | Translation accuracy insufficient | MEDIUM | HIGH | Human interpreter backup, accuracy testing, user consent | AI Architect |

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Requirements Approved | Stakeholder sign-off on this document | 2026-Q1 | This document |
| Senior AI Architect Hired | Technical lead in place | 2026-Q1 | Recruitment |
| Document Intelligence PoC | Working prototype for classification | 2026-Q2 | Architect, Cloud services |
| DPIA Approved | Data protection approval | 2026-Q2 | DPO review |
| Phase 1 Production | Document Intelligence live | 2026-Q3 | PoC success, DPIA |
| Speech Services PoC | Translation prototype | 2026-Q3 | Phase 1 learnings |
| Legal Review Complete | Approval for courtroom use | 2026-Q4 | Legal Services |
| Phase 2 Production | Translation services live | 2027-Q1 | Legal approval |
| Cognitive Search Live | Search capability deployed | 2027-Q2 | Document indexing |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| Chief Executive | Business Sponsor | [ ] Approved | | |
| CDiO | Programme Owner | [ ] Approved | | |
| Legal Services Director | Compliance | [ ] Approved | | |
| DPO | Privacy | [ ] Approved | | |
| Lord President (delegate) | Judicial | [ ] Approved | | |

### Sign-Off

By signing below, stakeholders confirm that requirements are complete, understood, and approved to proceed to design phase.

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| Chief Executive | _________ | |
| Chief Digital Information Officer | _________ | |
| Legal Services Director | _________ | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|------------|
| SCTS | Scottish Courts and Tribunals Service |
| CDi | Chief Digital Information (function within SCTS) |
| PoC | Proof of Concept |
| DPIA | Data Protection Impact Assessment |
| UK GDPR | UK General Data Protection Regulation |
| Cognitive Search | AI-powered semantic search with natural language understanding |
| Document Intelligence | AI-powered document classification and entity extraction |
| Human-in-the-Loop | Requirement for human oversight of AI decisions |

### Appendix B: Reference Documents

- Architecture Principles (ARC-001-PRIN-v1.0)
- Stakeholder Drivers Analysis (ARC-001-STKE-v1.0)
- Scottish Government AI Strategy
- Scottish Government Cyber Resilience Framework
- Source document: Senior AI Technical Architect job specification

### Appendix C: Requirements Traceability

| Requirement ID | Stakeholder Driver | Goal | Outcome | Principle |
|----------------|-------------------|------|---------|-----------|
| BR-001 | SD-2, SD-5 | G-1 | O-2 | P4, P5 |
| BR-002 | SD-11, SD-10 | G-2 | O-1 | P3, P8 |
| BR-003 | SD-1, SD-7 | G-4 | O-3 | P14, P2 |
| BR-004 | SD-8, SD-13 | G-5 | O-4 | P12, P13 |
| BR-005 | SD-9 | - | O-2 | P18 |
| BR-006 | SD-5, SD-6 | G-6 | O-2 | P19 |
| FR-001 to FR-003 | SD-5 | G-1 | O-2 | P4, P10 |
| FR-004 to FR-006 | SD-11 | G-2 | O-1 | P3, P8 |
| FR-007 to FR-010 | SD-4, SD-12 | G-3 | O-1, O-2 | P6, P16 |
| FR-011 to FR-012 | SD-1, SD-7 | G-4 | O-3 | P2, P8, P17 |
| NFR-SEC-* | SD-8, SD-7 | G-5 | O-4 | P11, P15 |
| NFR-C-* | SD-8, SD-13 | G-5 | O-4 | P12, P13 |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-01-17 GMT
**ArcKit Version**: 0.6.0
**Project**: SCTS GenAI Programme (Project 001)
**AI Model**: Claude Opus 4.5
**Generation Context**: Based on source document (Senior AI Technical Architect job specification), architecture principles, and stakeholder drivers analysis
