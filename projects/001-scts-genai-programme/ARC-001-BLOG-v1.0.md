# Product Backlog: SCTS GenAI Programme

> **Template Status**: Beta | **Version**: 0.11.2 | **Command**: `/arckit.backlog`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-BLOG-v1.1 |
| **Document Type** | Product Backlog |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-01-17 |
| **Last Modified** | 2026-01-27 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-02-27 |
| **Owner** | Chief Digital Information Officer, SCTS |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | CDi Function, Development Team, Scrum Masters |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.backlog` command | PENDING | PENDING |
| 1.1 | 2026-01-27 | ArcKit AI | Updated to template v0.11.2 format | PENDING | PENDING |

---

## Executive Summary

**Total Stories**: 45
**Total Epics**: 6
**Total Story Points**: 298
**Estimated Duration**: 15 sprints (30 weeks)

### Priority Breakdown
- Must Have: 25 stories (172 points) - 58%
- Should Have: 14 stories (89 points) - 30%
- Could Have: 6 stories (37 points) - 12%

### Epic Breakdown
1. Document Intelligence (58 points, 10 stories)
2. Real-Time Translation (53 points, 10 stories)
3. Cognitive Search (47 points, 9 stories)
4. Security & Compliance (52 points, 12 stories)
5. Platform Infrastructure (48 points, 11 stories)
6. Staff Training & Adoption (40 points, 10 stories)

---

## How to Use This Backlog

### For Product Owners:
1. Review epic priorities - adjust based on business needs
2. Refine story acceptance criteria before sprint planning
3. Validate user stories with court staff
4. Adjust sprint sequence based on stakeholder priorities

### For Development Teams:
1. Review stories in upcoming sprint (Sprint Planning)
2. Break down stories into tasks if needed
3. Estimate effort using team velocity
4. Identify technical blockers early
5. Update story status as work progresses

### For Scrum Masters:
1. Track velocity after each sprint
2. Adjust future sprint loading based on actual velocity
3. Monitor dependency chains
4. Escalate blockers early
5. Facilitate backlog refinement sessions

### Backlog Refinement Schedule:
- **Weekly**: Review and refine next 2 sprints
- **Bi-weekly**: Groom backlog beyond 2 sprints
- **Monthly**: Reassess epic priorities
- **Per sprint**: Update based on completed work and learnings

---

## Epics

### Epic 1: Document Intelligence (BR-001)

**Business Requirement**: BR-001 - Improve Court Operational Efficiency
**Priority**: Must Have
**Business Value**: High - 60% reduction in document processing time
**Risk**: Medium - AI accuracy must meet 90% threshold
**Dependencies**: None (foundation epic)
**Total Story Points**: 58
**Estimated Duration**: 3 sprints

**Description**:
Deploy AI-powered document classification and entity extraction to reduce manual document processing time by 60%. Covers document upload, AI classification, human review workflow, and audit trail.

**Success Criteria**:
- Document classification accuracy ≥ 90%
- Processing time reduced from 4.5 hours to 1.8 hours average
- Human-in-the-loop review for all classifications
- Full audit trail for GDPR compliance

**Stories in this Epic**:
1. Story-001: Document upload and validation (5 points) - Sprint 2
2. Story-002: AI document classification (8 points) - Sprint 2
3. Story-003: Human review workflow (5 points) - Sprint 3
4. Story-004: AI output labelling (3 points) - Sprint 3
5. Story-005: Audit trail for AI operations (5 points) - Sprint 3
6. Story-006: Quality feedback mechanism (3 points) - Sprint 7
7. Story-007: Manual fallback mode (5 points) - Sprint 7
8. Task-INT-001: Case Management integration (8 points) - Sprint 2
9. Task-INT-002: Document Management integration (8 points) - Sprint 2
10. Task-NFR-001: Document processing response time (5 points) - Sprint 3

---

### Epic 2: Real-Time Translation (BR-002)

**Business Requirement**: BR-002 - Enhance Access to Justice for Non-English Speakers
**Priority**: Must Have
**Business Value**: High - 20% improvement in Access to Justice Index
**Risk**: High - Translation accuracy critical for court proceedings
**Dependencies**: Epic 1 (platform foundation)
**Total Story Points**: 53
**Estimated Duration**: 2.5 sprints

**Description**:
Enable multilingual court access through AI-assisted transcription and real-time translation for 10 priority languages. Includes speech-to-text, translation, consent management, and human interpreter escalation.

**Success Criteria**:
- 10 languages supported
- English transcription 95% accuracy
- Translation latency < 2 seconds
- Legal terminology accuracy ≥ 85%
- Human interpreter escalation available

**Stories in this Epic**:
1. Story-008: Speech-to-text transcription (8 points) - Sprint 4
2. Story-009: Speaker diarisation (5 points) - Sprint 4
3. Story-010: Real-time translation (8 points) - Sprint 5
4. Story-011: Legal terminology glossary (5 points) - Sprint 5
5. Story-012: Language configuration (3 points) - Sprint 5
6. Story-013: Consent management (5 points) - Sprint 5
7. Story-014: Human interpreter escalation (5 points) - Sprint 7
8. Task-INT-004: Court Scheduling integration (5 points) - Sprint 4
9. Task-INT-005: Interpreter Booking integration (5 points) - Sprint 7
10. Task-NFR-002: Translation latency optimisation (4 points) - Sprint 5

---

### Epic 3: Cognitive Search (BR-001)

**Business Requirement**: BR-001 - Improve Court Operational Efficiency
**Priority**: Must Have
**Business Value**: High - Enables rapid case research
**Risk**: Medium - Search relevance requires tuning
**Dependencies**: Epic 1 (documents must be indexed)
**Total Story Points**: 47
**Estimated Duration**: 2 sprints

**Description**:
Implement semantic search across court documentation enabling natural language queries, case law citation detection, and document similarity analysis. Integrates with Azure AI Search.

**Success Criteria**:
- Semantic search with 80%+ user satisfaction
- Query response < 5 seconds
- Citation detection for Scottish and UK cases
- Document similarity analysis available

**Stories in this Epic**:
1. Story-015: Document indexing (5 points) - Sprint 6
2. Story-016: Semantic search (8 points) - Sprint 6
3. Story-017: Search filters and facets (5 points) - Sprint 6
4. Story-018: Case law citation detection (5 points) - Sprint 6
5. Story-019: Document similarity analysis (8 points) - Sprint 9
6. Story-020: Search results ranking (5 points) - Sprint 9
7. Story-021: Search analytics (3 points) - Sprint 9
8. Task-NFR-003: Search response time (5 points) - Sprint 6
9. Task-NFR-004: Data volume scaling (3 points) - Sprint 6

---

### Epic 4: Security & Compliance (BR-003, BR-004)

**Business Requirement**: BR-003 - Protect Court Record Integrity, BR-004 - Achieve Regulatory Compliance
**Priority**: Must Have
**Business Value**: Critical - Mandatory for court operations
**Risk**: Critical - Non-compliance is blocking
**Dependencies**: None (cross-cutting)
**Total Story Points**: 52
**Estimated Duration**: Distributed across all sprints

**Description**:
Implement zero-trust security architecture, UK GDPR compliance, court record protection, and algorithmic transparency requirements.

**Success Criteria**:
- Zero court record integrity incidents
- UK GDPR compliant (DPIA approved)
- ATRS record published
- Audit logging for 7 years
- Penetration testing passed

**Stories in this Epic**:
1. Task-NFR-SEC-001: Azure AD SSO implementation (5 points) - Sprint 1
2. Task-NFR-SEC-002: RBAC authorization (5 points) - Sprint 1
3. Task-NFR-SEC-003: Data encryption (rest + transit) (5 points) - Sprint 1
4. Task-NFR-SEC-004: UK data residency enforcement (3 points) - Sprint 1
5. Task-NFR-SEC-005: Vulnerability management (5 points) - Sprint 8
6. Task-NFR-SEC-006: Court record protection (5 points) - Sprint 2
7. Task-NFR-C-001: GDPR consent tracking (5 points) - Sprint 5
8. Task-NFR-C-002: Immutable audit logging (5 points) - Sprint 3
9. Task-NFR-C-003: Scottish Gov standards compliance (3 points) - Sprint 8
10. Task-NFR-C-004: AI transparency implementation (3 points) - Sprint 7
11. Task-NFR-U-001: WCAG 2.2 AA accessibility (5 points) - Sprint 8
12. Task-NFR-U-002: Multilingual interface (3 points) - Sprint 5

---

### Epic 5: Platform Infrastructure (Technical Foundation)

**Business Requirement**: N/A - Technical enabler
**Priority**: Must Have
**Business Value**: Foundation for all capabilities
**Risk**: High - Blocks all other work
**Dependencies**: None
**Total Story Points**: 48
**Estimated Duration**: Sprint 1 + ongoing

**Description**:
Establish Azure infrastructure including AKS cluster, API Management, databases, storage, monitoring, and CI/CD pipeline.

**Success Criteria**:
- AKS cluster operational
- CI/CD pipeline deployed
- Monitoring dashboards live
- DR environment ready

**Stories in this Epic**:
1. Task-INFRA-001: AKS cluster setup (8 points) - Sprint 1
2. Task-INFRA-002: Azure API Management (5 points) - Sprint 1
3. Task-INFRA-003: Azure SQL Database (3 points) - Sprint 1
4. Task-INFRA-004: Azure Blob Storage (2 points) - Sprint 1
5. Task-INFRA-005: Azure Redis Cache (3 points) - Sprint 1
6. Task-INFRA-006: Azure AI Search provisioning (3 points) - Sprint 6
7. Task-INFRA-007: CI/CD pipeline (Azure DevOps) (5 points) - Sprint 1
8. Task-INFRA-008: Monitoring (Azure Monitor) (5 points) - Sprint 1
9. Task-INFRA-009: Disaster recovery setup (5 points) - Sprint 8
10. Task-INT-003: Identity Provider integration (5 points) - Sprint 1
11. Task-INT-006: Azure AI Services integration (4 points) - Sprint 2

---

### Epic 6: Staff Training & Adoption (BR-005, BR-006)

**Business Requirement**: BR-005 - Demonstrate Value for Money, BR-006 - Enable Staff Adoption
**Priority**: Should Have
**Business Value**: Medium - Critical for adoption
**Risk**: Medium - Staff resistance if not addressed
**Dependencies**: Epics 1-3 (features must exist)
**Total Story Points**: 40
**Estimated Duration**: 2 sprints (later phases)

**Description**:
Training materials, user documentation, and operational handover for court staff.

**Success Criteria**:
- 75% staff satisfaction with AI tools
- Training completion for all pilot users
- Operational runbooks complete
- Support model established

**Stories in this Epic**:
1. Story-022: User training portal (5 points) - Sprint 9
2. Story-023: In-app guidance tooltips (3 points) - Sprint 9
3. Story-024: Video tutorials (5 points) - Sprint 10
4. Story-025: Admin documentation (3 points) - Sprint 10
5. Story-026: Operational runbooks (5 points) - Sprint 8
6. Story-027: Support knowledge base (3 points) - Sprint 10
7. Task-NFR-M-001: Observability dashboards (5 points) - Sprint 8
8. Task-NFR-M-002: Model governance procedures (5 points) - Sprint 8
9. Task-NFR-M-003: API documentation (3 points) - Sprint 7
10. Task-OPS-001: Hypercare support plan (3 points) - Sprint 8

---

## Prioritized Backlog

### Story-001: Document upload and validation

**As a** Court Clerk
**I want** to upload court documents in multiple formats
**So that** I can process them efficiently without format conversion

**Acceptance Criteria**:
- It's done when PDF documents are uploaded and processing initiated within 5 seconds
- It's done when scanned images (TIFF, JPEG, PNG) have OCR applied automatically
- It's done when Word documents (DOCX, DOC) are accepted and text extracted
- It's done when unsupported formats show clear error message with fallback options
- It's done when file size validation rejects files over 100MB with helpful message
- It's done when virus scan is performed before processing begins

**Technical Tasks**:
- Task-001-A: Implement file upload API endpoint (2 points)
- Task-001-B: Configure Azure Blob Storage with encryption (1 point)
- Task-001-C: Implement virus scanning integration (2 points)

**Requirements Traceability**: FR-001, NFR-SEC-003
**Component**: Document Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 2
**Dependencies**: TASK-INFRA-001, TASK-INFRA-004

---

### Story-002: AI document classification

**As a** Court Clerk
**I want** documents to be automatically classified by AI
**So that** I can reduce manual categorisation time by 60%

**Acceptance Criteria**:
- It's done when civil documents are classified (claim, defence, evidence, etc.) with 90%+ accuracy
- It's done when criminal documents are classified (indictment, plea, judgement, etc.) with 90%+ accuracy
- It's done when key entities are extracted (parties, dates, case numbers, amounts)
- It's done when confidence score is displayed alongside classification
- It's done when low-quality scans show quality warning with confidence impact

**Technical Tasks**:
- Task-002-A: Integrate Azure Document Intelligence API (3 points)
- Task-002-B: Train custom classification model for Scottish documents (3 points)
- Task-002-C: Implement entity extraction pipeline (2 points)

**Requirements Traceability**: FR-002, BR-001
**Component**: Document Service
**Story Points**: 8
**Priority**: Must Have
**Sprint**: 2
**Dependencies**: STORY-001, TASK-INT-006

---

### Story-003: Human review workflow

**As a** Court Clerk
**I want** to review and approve AI classifications
**So that** I maintain control over document categorisation decisions

**Acceptance Criteria**:
- It's done when AI classification is displayed with confidence score prominently visible
- It's done when I can accept the AI recommendation with one click
- It's done when I can select an alternative classification from approved taxonomy
- It's done when low confidence (<80%) items are visually highlighted for priority review
- It's done when both original AI classification and my decision are logged

**Technical Tasks**:
- Task-003-A: Build review queue UI component (2 points)
- Task-003-B: Implement classification override API (2 points)
- Task-003-C: Create confidence threshold configuration (1 point)

**Requirements Traceability**: FR-003, BR-003, P-2 (Human-in-the-Loop)
**Component**: Web Application, Document Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 3
**Dependencies**: STORY-002

---

### Story-004: AI output labelling

**As a** Legal Professional
**I want** AI-generated outputs to be clearly labelled
**So that** I understand the provenance of information

**Acceptance Criteria**:
- It's done when AI classifications show "AI-Assisted" label
- It's done when AI translations show "AI Translation" label with accuracy note
- It's done when AI search results show "AI-Ranked" indicator
- It's done when exported/printed documents include AI provenance metadata
- It's done when labels are accessible (screen reader compatible)

**Technical Tasks**:
- Task-004-A: Create AI label component library (2 points)
- Task-004-B: Implement labelling in all AI output views (1 point)

**Requirements Traceability**: FR-011, BR-003, P-8 (AI Transparency)
**Component**: Web Application
**Story Points**: 3
**Priority**: Must Have
**Sprint**: 3
**Dependencies**: STORY-002, STORY-010

---

### Story-005: Audit trail for AI operations

**As an** AI Administrator
**I want** comprehensive audit logs for all AI operations
**So that** we meet GDPR and governance requirements

**Acceptance Criteria**:
- It's done when every AI operation creates an audit record with timestamp
- It's done when audit records include: user, action, input reference, output, model version
- It's done when human overrides capture both original AI output and correction
- It's done when audit logs are immutable (append-only, no deletion)
- It's done when authorised users can query audit history by date, user, or operation type

**Technical Tasks**:
- Task-005-A: Design audit log schema (1 point)
- Task-005-B: Implement audit logging service (2 points)
- Task-005-C: Build audit query API and UI (2 points)

**Requirements Traceability**: FR-012, NFR-C-002, BR-004
**Component**: Audit Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 3
**Dependencies**: TASK-INFRA-003

---

### Story-006: Quality feedback mechanism

**As a** Court Clerk
**I want** to provide feedback on AI output quality
**So that** the system can improve over time

**Acceptance Criteria**:
- It's done when I can rate AI output quality (good/needs improvement/incorrect)
- It's done when feedback is logged with the original AI output
- It's done when aggregated feedback generates model performance reports
- It's done when consistent error patterns trigger alerts for model review

**Technical Tasks**:
- Task-006-A: Create feedback component (1 point)
- Task-006-B: Implement feedback analytics (2 points)

**Requirements Traceability**: FR-013, P-10 (Data Quality)
**Component**: Web Application, Audit Service
**Story Points**: 3
**Priority**: Should Have
**Sprint**: 7
**Dependencies**: STORY-002, STORY-005

---

### Story-007: Manual fallback mode

**As a** Court Clerk
**I want** to continue working when AI services are unavailable
**So that** court operations are not disrupted

**Acceptance Criteria**:
- It's done when document upload works with manual classification workflow if AI is down
- It's done when translation requests notify human interpreter service automatically
- It's done when search falls back to keyword-only mode with clear indicator
- It's done when AI services automatically resume when available
- It's done when fallback events are logged for operational review

**Technical Tasks**:
- Task-007-A: Implement circuit breaker pattern (2 points)
- Task-007-B: Create fallback UI components (2 points)
- Task-007-C: Configure health checks and alerts (1 point)

**Requirements Traceability**: FR-014, BR-003, P-5 (Resilience)
**Component**: All Services
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 7
**Dependencies**: STORY-002, STORY-010, STORY-016

---

### Story-008: Speech-to-text transcription

**As a** Court Clerk
**I want** courtroom audio transcribed to text in real-time
**So that** I can provide live captions for court users

**Acceptance Criteria**:
- It's done when English audio is transcribed with 95%+ word accuracy
- It's done when non-English audio (10 languages) is transcribed with 90%+ accuracy
- It's done when background noise triggers confidence indicators for uncertain segments
- It's done when transcription latency is under 500 milliseconds
- It's done when transcription can be paused and resumed during proceedings

**Technical Tasks**:
- Task-008-A: Integrate Azure Speech Services (3 points)
- Task-008-B: Implement WebSocket audio streaming (3 points)
- Task-008-C: Create transcription UI with real-time display (2 points)

**Requirements Traceability**: FR-004, BR-002
**Component**: Speech Service
**Story Points**: 8
**Priority**: Must Have
**Sprint**: 4
**Dependencies**: TASK-INT-006, TASK-NFR-SEC-001

---

### Story-009: Speaker diarisation

**As a** Court Clerk
**I want** different speakers identified in the transcript
**So that** I can attribute statements to the correct parties

**Acceptance Criteria**:
- It's done when up to 10 speakers are distinguished in the transcript
- It's done when speaker changes are marked clearly in the output
- It's done when I can label speakers with role names (Judge, Defence, etc.)
- It's done when speaker labels persist across the session

**Technical Tasks**:
- Task-009-A: Enable Azure Speech diarisation feature (2 points)
- Task-009-B: Create speaker labelling interface (2 points)
- Task-009-C: Store speaker mappings per session (1 point)

**Requirements Traceability**: FR-004
**Component**: Speech Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 4
**Dependencies**: STORY-008

---

### Story-010: Real-time translation

**As a** Court User (non-English speaker)
**I want** court proceedings translated in real-time
**So that** I can understand and participate fully

**Acceptance Criteria**:
- It's done when English text is translated to target language within 2 seconds
- It's done when legal terminology uses approved glossary for accuracy
- It's done when original text is available alongside translation for comparison
- It's done when uncertain translations are flagged for human interpreter review
- It's done when translation quality meets 85% accuracy for legal terms

**Technical Tasks**:
- Task-010-A: Integrate Azure Translator API (3 points)
- Task-010-B: Implement legal glossary custom training (3 points)
- Task-010-C: Create dual-language display interface (2 points)

**Requirements Traceability**: FR-005, BR-002
**Component**: Speech Service
**Story Points**: 8
**Priority**: Must Have
**Sprint**: 5
**Dependencies**: STORY-008, TASK-INT-006

---

### Story-011: Legal terminology glossary

**As an** AI Administrator
**I want** to manage legal terminology translations
**So that** domain-specific terms are translated accurately

**Acceptance Criteria**:
- It's done when I can add, edit, and remove glossary entries
- It's done when glossary supports all 10 priority languages
- It's done when glossary entries override generic translations
- It's done when changes are version-controlled with audit trail
- It's done when glossary can be exported/imported for backup

**Technical Tasks**:
- Task-011-A: Create glossary management API (2 points)
- Task-011-B: Build glossary admin interface (2 points)
- Task-011-C: Configure Azure Translator custom dictionary (1 point)

**Requirements Traceability**: FR-005
**Component**: Speech Service
**Story Points**: 5
**Priority**: Should Have
**Sprint**: 5
**Dependencies**: STORY-010

---

### Story-012: Language configuration

**As an** AI Administrator
**I want** to configure supported languages
**So that** new languages can be added without system changes

**Acceptance Criteria**:
- It's done when system supports 10+ languages as configured
- It's done when new languages can be added via configuration (no code change)
- It's done when per-language accuracy metrics are displayed
- It's done when language demand data generates prioritisation recommendations

**Technical Tasks**:
- Task-012-A: Create language configuration service (2 points)
- Task-012-B: Build language metrics dashboard (1 point)

**Requirements Traceability**: FR-006
**Component**: Speech Service
**Story Points**: 3
**Priority**: Should Have
**Sprint**: 5
**Dependencies**: STORY-010

---

### Story-013: Consent management for translation

**As a** Court User
**I want** to consent to AI translation before proceedings
**So that** I understand the service and its limitations

**Acceptance Criteria**:
- It's done when consent form explains AI translation and limitations clearly
- It's done when consent is captured digitally with timestamp and user ID
- It's done when I can decline AI translation and request human interpreter
- It's done when consent status is visible to court staff throughout session
- It's done when consent records are retained for 7 years (GDPR)

**Technical Tasks**:
- Task-013-A: Create consent capture workflow (2 points)
- Task-013-B: Build consent management API (2 points)
- Task-013-C: Implement consent status display (1 point)

**Requirements Traceability**: FR-015, BR-004, NFR-C-001
**Component**: Speech Service, Web Application
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 5
**Dependencies**: STORY-010

---

### Story-014: Human interpreter escalation

**As a** Court Clerk
**I want** to escalate to a human interpreter when AI translation is insufficient
**So that** complex legal matters are handled accurately

**Acceptance Criteria**:
- It's done when I can request human interpreter with one click
- It's done when interpreter booking system is notified automatically
- It's done when AI translation pauses until human takes over
- It's done when handover is logged with reason code
- It's done when AI can resume if human interpreter departs

**Technical Tasks**:
- Task-014-A: Create escalation trigger API (2 points)
- Task-014-B: Integrate with interpreter booking system (2 points)
- Task-014-C: Build handover UI and logging (1 point)

**Requirements Traceability**: FR-015, BC-2
**Component**: Speech Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 7
**Dependencies**: STORY-010, TASK-INT-005

---

### Story-015: Document indexing

**As an** AI Administrator
**I want** documents indexed for search automatically
**So that** users can find documents without manual tagging

**Acceptance Criteria**:
- It's done when new documents are searchable within 15 minutes of processing
- It's done when document updates trigger re-indexing with version tracking
- It's done when document deletion removes from search index
- It's done when security classifications are preserved in index
- It's done when index statistics show document count and freshness

**Technical Tasks**:
- Task-015-A: Configure Azure AI Search indexer (2 points)
- Task-015-B: Create incremental indexing pipeline (2 points)
- Task-015-C: Implement security filtering (1 point)

**Requirements Traceability**: FR-008, INT-002
**Component**: Search Service
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 6
**Dependencies**: STORY-002, TASK-INFRA-006

---

### Story-016: Semantic search

**As a** Legal Professional
**I want** to search court documents using natural language
**So that** I can find relevant information without knowing exact keywords

**Acceptance Criteria**:
- It's done when natural language queries return semantically relevant results
- It's done when legal terminology is understood contextually
- It's done when ambiguous queries suggest related concepts
- It's done when relevance scores are shown for each result
- It's done when search results include highlighted matching snippets

**Technical Tasks**:
- Task-016-A: Implement Azure AI Search semantic configuration (3 points)
- Task-016-B: Create search API with query parsing (3 points)
- Task-016-C: Build search results UI with highlighting (2 points)

**Requirements Traceability**: FR-007, BR-001
**Component**: Search Service, Web Application
**Story Points**: 8
**Priority**: Must Have
**Sprint**: 6
**Dependencies**: STORY-015

---

### Story-017: Search filters and facets

**As a** Legal Professional
**I want** to filter search results by case attributes
**So that** I can narrow down to relevant documents quickly

**Acceptance Criteria**:
- It's done when I can filter by date range
- It's done when I can filter by case type (civil, criminal)
- It's done when I can filter by court level (Sheriff, Court of Session, etc.)
- It's done when I can filter by document type (judgement, evidence, etc.)
- It's done when facet counts update dynamically as filters applied

**Technical Tasks**:
- Task-017-A: Configure search facets (2 points)
- Task-017-B: Build filter UI components (2 points)
- Task-017-C: Implement facet count aggregation (1 point)

**Requirements Traceability**: FR-007
**Component**: Search Service, Web Application
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 6
**Dependencies**: STORY-016

---

### Story-018: Case law citation detection

**As a** Legal Professional
**I want** case citations identified and linked in documents
**So that** I can navigate to referenced cases easily

**Acceptance Criteria**:
- It's done when Scottish case citations are detected and linked to case records
- It's done when UK Supreme Court/England & Wales citations are detected with external links
- It's done when clicking a citation shows case summary popup
- It's done when documents list all detected citations in metadata panel

**Technical Tasks**:
- Task-018-A: Implement citation regex patterns (2 points)
- Task-018-B: Create citation link resolution service (2 points)
- Task-018-C: Build citation UI components (1 point)

**Requirements Traceability**: FR-009
**Component**: Search Service, Web Application
**Story Points**: 5
**Priority**: Should Have
**Sprint**: 6
**Dependencies**: STORY-015

---

### Story-019: Document similarity analysis

**As a** Legal Professional
**I want** to find documents similar to one I'm viewing
**So that** I can discover related cases and precedents

**Acceptance Criteria**:
- It's done when I can request "Similar Documents" for any document
- It's done when top 10 similar documents are returned ranked by similarity
- It's done when similarity score and matching aspects are displayed
- It's done when cross-case-type similarities are identified where relevant

**Technical Tasks**:
- Task-019-A: Implement vector similarity search (4 points)
- Task-019-B: Create similarity explanation logic (2 points)
- Task-019-C: Build similar documents UI panel (2 points)

**Requirements Traceability**: FR-010
**Component**: Search Service
**Story Points**: 8
**Priority**: Could Have
**Sprint**: 9
**Dependencies**: STORY-015

---

### Story-020: Search results ranking

**As a** Legal Professional
**I want** search results ranked by relevance
**So that** most pertinent documents appear first

**Acceptance Criteria**:
- It's done when results are ranked by semantic relevance
- It's done when recency can be factored into ranking (optional)
- It's done when I can see why a result ranked highly
- It's done when ranking can be tuned per search type

**Technical Tasks**:
- Task-020-A: Configure semantic ranking profiles (2 points)
- Task-020-B: Implement relevance explanation (2 points)
- Task-020-C: Create ranking configuration admin (1 point)

**Requirements Traceability**: FR-007
**Component**: Search Service
**Story Points**: 5
**Priority**: Should Have
**Sprint**: 9
**Dependencies**: STORY-016

---

### Story-021: Search analytics

**As an** AI Administrator
**I want** to see how users are searching
**So that** I can improve search quality over time

**Acceptance Criteria**:
- It's done when popular search queries are tracked (anonymised)
- It's done when zero-result queries are flagged for review
- It's done when click-through rates on results are tracked
- It's done when analytics dashboard shows search trends

**Technical Tasks**:
- Task-021-A: Implement search logging (1 point)
- Task-021-B: Create analytics dashboard (2 points)

**Requirements Traceability**: FR-007
**Component**: Search Service
**Story Points**: 3
**Priority**: Should Have
**Sprint**: 9
**Dependencies**: STORY-016

---

### Story-022: User training portal

**As a** Court Clerk
**I want** access to training materials for AI tools
**So that** I can learn to use the system effectively

**Acceptance Criteria**:
- It's done when training portal is accessible from main navigation
- It's done when training is organised by capability (Document, Translation, Search)
- It's done when completion status is tracked per user
- It's done when I can search for specific topics

**Requirements Traceability**: BR-005, BR-006
**Component**: Web Application
**Story Points**: 5
**Priority**: Should Have
**Sprint**: 9
**Dependencies**: STORY-002, STORY-010, STORY-016

---

### Story-023: In-app guidance tooltips

**As a** Court Clerk
**I want** contextual help when using AI features
**So that** I understand what actions to take

**Acceptance Criteria**:
- It's done when first-time users see guided tour
- It's done when hover tooltips explain AI features
- It's done when help icons link to relevant documentation
- It's done when guidance can be dismissed and re-enabled

**Requirements Traceability**: BR-006
**Component**: Web Application
**Story Points**: 3
**Priority**: Should Have
**Sprint**: 9
**Dependencies**: STORY-002, STORY-016

---

### Story-024: Video tutorials

**As a** Court Clerk
**I want** video tutorials for complex workflows
**So that** I can learn visually

**Acceptance Criteria**:
- It's done when videos cover document classification workflow
- It's done when videos cover translation session setup
- It's done when videos cover search best practices
- It's done when videos are captioned (accessibility)

**Requirements Traceability**: BR-006
**Component**: Training Materials
**Story Points**: 5
**Priority**: Could Have
**Sprint**: 10
**Dependencies**: STORY-002, STORY-010, STORY-016

---

### Story-025: Admin documentation

**As an** AI Administrator
**I want** comprehensive admin documentation
**So that** I can manage the system effectively

**Acceptance Criteria**:
- It's done when system architecture is documented
- It's done when configuration guides are available
- It's done when troubleshooting guides exist for common issues
- It's done when API documentation is complete (OpenAPI)

**Requirements Traceability**: NFR-M-003
**Component**: Documentation
**Story Points**: 3
**Priority**: Should Have
**Sprint**: 10
**Dependencies**: All core features

---

### Story-026: Operational runbooks

**As an** ICT Operations Manager
**I want** runbooks for operational procedures
**So that** my team can support the system in production

**Acceptance Criteria**:
- It's done when incident response procedures are documented
- It's done when backup and recovery procedures exist
- It's done when scaling procedures are documented
- It's done when monitoring alert response guides exist
- It's done when runbooks are tested before go-live

**Requirements Traceability**: NFR-A-002, P-5
**Component**: Operations
**Story Points**: 5
**Priority**: Must Have
**Sprint**: 8
**Dependencies**: TASK-INFRA-008, TASK-INFRA-009

---

### Story-027: Support knowledge base

**As a** Support Agent
**I want** a knowledge base for user issues
**So that** I can resolve problems quickly

**Acceptance Criteria**:
- It's done when common issues are documented with solutions
- It's done when knowledge base is searchable
- It's done when articles can be linked from support tickets
- It's done when usage analytics show popular articles

**Requirements Traceability**: BR-006
**Component**: Documentation
**Story Points**: 3
**Priority**: Could Have
**Sprint**: 10
**Dependencies**: All core features

---

## Sprint Plan

### Sprint 1: Foundation (Weeks 1-2)

**Velocity**: 20 story points
**Theme**: Technical foundation and security

#### Must Have Stories (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| TASK-INFRA-001 | AKS cluster setup | Technical | 8 |
| TASK-INFRA-002 | Azure API Management | Technical | 5 |
| TASK-INFRA-003 | Azure SQL Database | Technical | 3 |
| TASK-INFRA-004 | Azure Blob Storage | Technical | 2 |
| TASK-INFRA-005 | Azure Redis Cache | Technical | 3 |

**Parallel Work** (included in above):
- TASK-NFR-SEC-001: Azure AD SSO (5 points - starts week 1)
- TASK-NFR-SEC-002: RBAC authorization (5 points - starts week 1)
- TASK-NFR-SEC-003: Data encryption (5 points - starts week 2)

### Sprint Goals:
- AKS cluster operational in UK South
- API Management configured with OAuth 2.0
- SQL Database deployed with encryption
- Blob Storage configured with CMK
- Redis Cache for session management
- Azure AD SSO working

### Dependencies Satisfied:
✅ None (foundation sprint)

### Dependencies Created for Sprint 2:
→ Infrastructure ready for services
→ Authentication working
→ Storage available

### Risks:
⚠️ Azure provisioning delays
⚠️ Security configuration complexity

### Definition of Done:
- [ ] Code reviewed and approved
- [ ] Unit tests written (80% coverage minimum)
- [ ] Integration tests written for critical paths
- [ ] Security scan passed (no critical/high issues)
- [ ] Deployed to dev environment
- [ ] Demo-able to stakeholders
- [ ] Documentation updated

---

### Sprint 2: Document Intelligence Core (Weeks 3-4)

**Velocity**: 20 story points
**Theme**: Document upload and AI classification

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-001 | Document upload and validation | Story | 5 |
| STORY-002 | AI document classification | Story | 8 |
| TASK-INT-001 | Case Management integration | Technical | 4 |
| TASK-INT-006 | Azure AI Services integration | Technical | 3 |

### Sprint Goals:
- Documents can be uploaded via API
- AI classification working with Azure Document Intelligence
- Case Management API connected
- Azure AI Services credentials configured

### Dependencies Satisfied:
✅ Sprint 1 infrastructure

### Dependencies Created for Sprint 3:
→ Document classification available for UI
→ AI integration patterns established

---

### Sprint 3: Document Intelligence UI (Weeks 5-6)

**Velocity**: 20 story points
**Theme**: Human review and audit

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-003 | Human review workflow | Story | 5 |
| STORY-004 | AI output labelling | Story | 3 |
| STORY-005 | Audit trail for AI operations | Story | 5 |
| TASK-NFR-C-002 | Immutable audit logging | Technical | 5 |
| TASK-NFR-001 | Document processing response time | Technical | 2 |

### Sprint Goals:
- Clerks can review and approve AI classifications
- AI outputs clearly labelled
- Audit trail operational
- Response times meeting NFR-P-001

### Dependencies Satisfied:
✅ Sprint 2 AI classification

---

### Sprint 4: Speech Services (Weeks 7-8)

**Velocity**: 20 story points
**Theme**: Transcription and diarisation

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-008 | Speech-to-text transcription | Story | 8 |
| STORY-009 | Speaker diarisation | Story | 5 |
| TASK-INT-004 | Court Scheduling integration | Technical | 5 |
| TASK-NFR-SEC-004 | UK data residency enforcement | Technical | 2 |

### Sprint Goals:
- Real-time transcription working
- Speaker identification operational
- Court session schedule integration
- All audio processed in UK region only

### Dependencies Satisfied:
✅ Sprint 1 infrastructure, Azure AI integration

---

### Sprint 5: Translation Services (Weeks 9-10)

**Velocity**: 20 story points
**Theme**: Real-time translation and consent

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-010 | Real-time translation | Story | 8 |
| STORY-011 | Legal terminology glossary | Story | 5 |
| STORY-013 | Consent management for translation | Story | 5 |
| TASK-NFR-002 | Translation latency optimisation | Technical | 2 |

### Sprint Goals:
- Translation working for all 10 languages
- Legal glossary integrated
- Consent workflow operational
- Latency under 2 seconds

### Dependencies Satisfied:
✅ Sprint 4 transcription

---

### Sprint 6: Cognitive Search (Weeks 11-12)

**Velocity**: 20 story points
**Theme**: Semantic search and indexing

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-015 | Document indexing | Story | 5 |
| STORY-016 | Semantic search | Story | 8 |
| STORY-017 | Search filters and facets | Story | 5 |
| TASK-INFRA-006 | Azure AI Search provisioning | Technical | 2 |

### Sprint Goals:
- Documents indexed and searchable
- Semantic search working
- Filters and facets operational
- Search response under 5 seconds

### Dependencies Satisfied:
✅ Sprint 2 document processing

---

### Sprint 7: Integration & Governance (Weeks 13-14)

**Velocity**: 20 story points
**Theme**: External integrations and AI governance

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-006 | Quality feedback mechanism | Story | 3 |
| STORY-007 | Manual fallback mode | Story | 5 |
| STORY-014 | Human interpreter escalation | Story | 5 |
| TASK-INT-005 | Interpreter Booking integration | Technical | 5 |
| TASK-NFR-C-004 | AI transparency implementation | Technical | 2 |

### Sprint Goals:
- Feedback mechanism operational
- Fallback modes tested
- Interpreter escalation working
- Transparency requirements met

### Dependencies Satisfied:
✅ All core features

---

### Sprint 8: Hardening & UAT Prep (Weeks 15-16)

**Velocity**: 20 story points
**Theme**: Security, operations, and UAT preparation

#### Items (20 points):

| ID | Title | Type | Points |
|----|-------|------|--------|
| STORY-026 | Operational runbooks | Story | 5 |
| TASK-NFR-SEC-005 | Vulnerability management | Technical | 5 |
| TASK-INFRA-009 | Disaster recovery setup | Technical | 5 |
| TASK-NFR-M-001 | Observability dashboards | Technical | 5 |

### Sprint Goals:
- Runbooks complete and tested
- Security vulnerabilities addressed
- DR tested successfully
- Monitoring dashboards live
- Ready for UAT

### Dependencies Satisfied:
✅ All core features

---

## Appendices

### A. Requirements Traceability Matrix

| Requirement | Type | User Stories | Sprint | Status | Notes |
|-------------|------|-------------|--------|--------|-------|
| BR-001 | Business | Story-001,002,003,015,016 | 2,3,6 | Planned | Document Intelligence, Search |
| BR-002 | Business | Story-008,009,010,011,012,013 | 4,5 | Planned | Translation Services |
| BR-003 | Business | Story-003,004,005,007 | 3,7 | Planned | Court Record Integrity |
| BR-004 | Business | Story-005,013, TASK-NFR-C-* | 3,5 | Planned | Regulatory Compliance |
| BR-005 | Business | Story-022,024,025 | 9,10 | Planned | Value for Money |
| BR-006 | Business | Story-022,023,024,026,027 | 8-10 | Planned | Staff Adoption |
| FR-001 | Functional | Story-001 | 2 | Planned | Document Upload |
| FR-002 | Functional | Story-002 | 2 | Planned | AI Classification |
| FR-003 | Functional | Story-003 | 3 | Planned | Human Review |
| FR-004 | Functional | Story-008,009 | 4 | Planned | Speech-to-Text |
| FR-005 | Functional | Story-010,011 | 5 | Planned | Translation |
| FR-006 | Functional | Story-012 | 5 | Planned | Language Config |
| FR-007 | Functional | Story-016,017,020,021 | 6,9 | Planned | Semantic Search |
| FR-008 | Functional | Story-015 | 6 | Planned | Document Indexing |
| FR-009 | Functional | Story-018 | 6 | Planned | Citation Detection |
| FR-010 | Functional | Story-019 | 9 | Planned | Document Similarity |
| FR-011 | Functional | Story-004 | 3 | Planned | AI Output Labelling |
| FR-012 | Functional | Story-005 | 3 | Planned | Audit Trail |
| FR-013 | Functional | Story-006 | 7 | Planned | Quality Feedback |
| FR-014 | Functional | Story-007 | 7 | Planned | Manual Fallback |
| FR-015 | Functional | Story-013,014 | 5,7 | Planned | Consent Management |
| INT-001 | Integration | TASK-INT-001 | 2 | Planned | Case Management |
| INT-002 | Integration | TASK-INT-002 | 2 | Planned | Document Management |
| INT-003 | Integration | TASK-INT-003 | 1 | Planned | Identity Provider |
| INT-004 | Integration | TASK-INT-004 | 4 | Planned | Court Scheduling |
| INT-005 | Integration | TASK-INT-005 | 7 | Planned | Interpreter Booking |
| INT-006 | Integration | TASK-INT-006 | 2 | Planned | Azure AI Services |
| NFR-SEC-* | Security | TASK-NFR-SEC-* | 1,2,8 | Planned | Security Controls |
| NFR-C-* | Compliance | TASK-NFR-C-* | 3,5,7,8 | Planned | Compliance |
| NFR-P-* | Performance | TASK-NFR-001,002,003 | 3,5,6 | Planned | Performance |
| NFR-M-* | Maintainability | TASK-NFR-M-* | 7,8 | Planned | Maintainability |

**Coverage Summary**:
- Total Requirements: 49
- Mapped to Stories: 49 (100%)
- Scheduled in Sprints 1-8: 40 (82%)
- Remaining for Future Sprints: 9 (18%)

---

### B. Dependency Graph

```
Sprint 1 (Foundation)
  ├─ TASK-INFRA-001: AKS Cluster
  │    ↓ (blocks)
  │  Sprint 2: All services deployment
  │
  ├─ TASK-INFRA-004: Blob Storage
  │    ↓ (blocks)
  │  Sprint 2: STORY-001 (Document Upload)
  │
  └─ TASK-NFR-SEC-001: Azure AD SSO
       ↓ (blocks)
     Sprint 2+: All authenticated features
```

---

### C. Epic Overview

| Epic ID | Epic Name | Priority | Stories | Points | Sprints | Status | Dependencies |
|---------|-----------|----------|---------|--------|---------|--------|--------------|
| EPIC-001 | Document Intelligence | Must Have | 10 | 58 | 2-3 | Planned | None |
| EPIC-002 | Real-Time Translation | Must Have | 10 | 53 | 4-5 | Planned | EPIC-001 |
| EPIC-003 | Cognitive Search | Must Have | 9 | 47 | 6 | Planned | EPIC-001 |
| EPIC-004 | Security & Compliance | Must Have | 12 | 52 | 1-8 | Planned | None |
| EPIC-005 | Platform Infrastructure | Must Have | 11 | 48 | 1+ | Planned | None |
| EPIC-006 | Staff Training | Should Have | 10 | 40 | 8-10 | Planned | EPIC-001,002,003 |

**Total**: 6 epics, 62 items, 298 story points

---

### D. Story Points Distribution

```
Sprint 1:  ████████████████████ 20 points
Sprint 2:  ████████████████████ 20 points
Sprint 3:  ████████████████████ 20 points
Sprint 4:  ████████████████████ 20 points
Sprint 5:  ████████████████████ 20 points
Sprint 6:  ████████████████████ 20 points
Sprint 7:  ████████████████████ 20 points
Sprint 8:  ████████████████████ 20 points
Total: 160 points allocated / 298 points total
Remaining: 138 points (7 more sprints needed)
```

---

### E. Risk-Based Prioritization

**High Risk Items (Addressed Early)**:
- Sprint 1: TASK-NFR-SEC-001 - Azure AD SSO (security foundation)
- Sprint 2: TASK-NFR-SEC-006 - Court record protection (compliance critical)
- Sprint 3: STORY-005 - Audit trail (GDPR requirement)

**Medium Risk Items**:
- Sprint 5: STORY-013 - Consent management (legal requirement)
- Sprint 7: STORY-007 - Manual fallback mode (resilience)

**Low Risk Items**:
- Sprint 9: STORY-019 - Document similarity (enhancement)

---

### F. Definition of Done (from Architecture Principles)

Every story must meet these criteria before marking "Done":

#### Code Quality
- [ ] Code reviewed by 2+ team members
- [ ] No merge conflicts
- [ ] Follows coding standards (linting passed)
- [ ] No code smells or technical debt introduced

#### Testing
- [ ] Unit tests written (minimum 80% coverage)
- [ ] Integration tests written for API endpoints
- [ ] Manual testing completed
- [ ] Acceptance criteria verified and signed off

#### Security
- [ ] Security scan passed (no critical/high vulnerabilities)
- [ ] OWASP Top 10 checks completed
- [ ] Secrets not hardcoded (use environment variables)
- [ ] Authentication and authorization tested

#### Performance
- [ ] Performance tested (meets NFR thresholds)
- [ ] No N+1 query issues
- [ ] Caching implemented where appropriate
- [ ] Response times within acceptable limits

#### Compliance
- [ ] GDPR requirements met (if handling user data)
- [ ] Accessibility tested (WCAG 2.1 AA)
- [ ] Audit logging in place (if required)

#### Documentation
- [ ] API documentation updated (OpenAPI/Swagger)
- [ ] Code comments for complex logic
- [ ] README updated if needed
- [ ] Runbook updated (if operational changes)

#### Deployment
- [ ] Deployed to dev environment
- [ ] Deployed to staging environment
- [ ] Database migrations tested (if applicable)
- [ ] Configuration updated in all environments

#### Stakeholder
- [ ] Demoed to Product Owner at sprint review
- [ ] Acceptance criteria validated by PO
- [ ] User feedback incorporated (if available)

---

## Future Sprints (Beyond Sprint 8)

**Remaining Backlog**: 138 story points
**Estimated Duration**: 7 sprints (at 20 points/sprint)

**High Priority Items for Sprint 9+**:
1. Story-018: Case law citation detection (5 points) - Epic: Cognitive Search
2. Story-019: Document similarity analysis (8 points) - Epic: Cognitive Search
3. Story-020: Search results ranking (5 points) - Epic: Cognitive Search
4. Story-021: Search analytics (3 points) - Epic: Cognitive Search
5. Story-022: User training portal (5 points) - Epic: Staff Training

**Could Have Items (Deferred)**:
- Story-024: Video tutorials (5 points) - Resource dependent
- Story-027: Support knowledge base (3 points) - Lower priority

---

## Backlog Maintenance

### Velocity Tracking
After each sprint, update:
- Actual velocity vs planned
- Velocity trend (improving, stable, declining)
- Adjust future sprint capacity accordingly

### Backlog Grooming Sessions
- **Weekly**: Refine next 2 sprints (add details, update estimates)
- **Bi-weekly**: Groom backlog beyond 2 sprints (reprioritize)
- **Monthly**: Review epic priorities (business changes)

### When to Re-Generate Backlog
- Requirements significantly changed
- New epics added
- Business priorities shifted
- Architecture redesigned

---

## Integration with Other ArcKit Commands

**This backlog was generated from**:
- `/arckit.requirements` - Source of all stories
- `/arckit.hld` - Component mapping
- `/arckit.stakeholders` - User personas
- `/arckit.risk-register` - Risk priorities

**Use this backlog with**:
- `/arckit.traceability` - Track requirements through implementation
- `/arckit.analyze` - Validate backlog completeness

---

**Important Notes**:

⚠️ **Story Points Are Estimates**: AI-generated estimates should be validated by your team based on actual velocity and capacity. Use team poker for consensus estimation.

⚠️ **Velocity Will Vary**: Initial velocity (20 points) is assumed. Track actual velocity after Sprint 1 and adjust future sprints accordingly.

⚠️ **Dependencies May Change**: Technical dependencies are identified automatically but may need adjustment based on your team's approach and constraints.

⚠️ **Regular Refinement Required**: This backlog is a starting point. Teams should refine weekly and adapt based on learnings.

---

**Generated by**: ArcKit `/arckit.backlog` command
**Generated on**: 2026-01-27
**ArcKit Version**: 0.11.2
**Project**: SCTS GenAI Programme (Project 001)
**Model**: Claude Opus 4.5

---

**End of Backlog**
