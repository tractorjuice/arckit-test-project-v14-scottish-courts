# Scottish Courts and Tribunals Service (SCTS) Architecture Principles

## Document Information

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-PRIN-v1.0 |
| **Project** | SCTS GenAI Strategy (Project 001) |
| **Document Type** | Enterprise Architecture Principles |
| **Classification** | OFFICIAL |
| **Version** | 1.0 |
| **Status** | DRAFT |
| **Date** | 2026-01-17 |
| **Owner** | Chief Digital Information Officer, SCTS |

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.principles` command |

---

## Executive Summary

This document establishes the architecture principles governing all technology decisions for the Scottish Courts and Tribunals Service (SCTS) AI and Automation programme. These principles ensure that AI capabilities are delivered safely, ethically, and in alignment with the justice mission of supporting legal professionals and improving public access to justice.

**Scope**: All AI/ML systems, cognitive services, and automation initiatives within SCTS
**Authority**: Enterprise Architecture Review Board / CDi Function
**Compliance**: Mandatory unless exception approved by Chief Digital Officer

**Philosophy**: These principles are **technology-agnostic** - they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

---

## I. Strategic Principles

### 1. Justice-Centred Design

**Principle Statement**:
All AI systems MUST demonstrably support the administration of justice, improving outcomes for legal professionals, court users, and the public.

**Rationale**:
SCTS exists to support the judiciary and provide access to justice. Technology investments must directly advance this mission, not simply introduce innovation for its own sake. Every AI capability must trace back to improved justice outcomes.

**Implications**:
- AI use cases must articulate clear benefits for justice delivery or access
- User research must include legal professionals, court staff, and public users
- Success metrics must include justice-related outcomes, not just efficiency
- No AI system should impede or complicate access to justice for any user group
- Human oversight required for any AI decisions affecting legal proceedings

**Validation Gates**:
- [ ] Use case traces to justice mission objectives
- [ ] User research conducted with affected stakeholder groups
- [ ] Justice outcome metrics defined alongside efficiency metrics
- [ ] Human oversight mechanisms documented for consequential decisions
- [ ] Impact on access to justice assessed (positive and negative)

---

### 2. Human-in-the-Loop for Consequential Decisions

**Principle Statement**:
AI systems MUST NOT make autonomous decisions that affect legal proceedings, case outcomes, or individual rights. Humans MUST remain in control of all consequential decisions.

**Rationale**:
The justice system requires human judgement, accountability, and the ability to exercise discretion. AI must augment human capability, not replace human decision-making in matters affecting rights and legal outcomes.

**Implications**:
- AI outputs are recommendations, not decisions, for legal matters
- Clear escalation paths to human decision-makers
- No automated actions that affect case progression without human approval
- Audit trails showing which human approved AI-assisted decisions
- Override mechanisms for all AI recommendations

**Validation Gates**:
- [ ] Decision boundaries documented (what AI can/cannot decide)
- [ ] Human approval workflow for consequential outputs
- [ ] Override mechanisms tested and documented
- [ ] Audit trail captures human accountability
- [ ] Training provided to staff on appropriate AI reliance

---

### 3. Accessibility and Inclusive Design

**Principle Statement**:
All AI systems MUST meet public sector accessibility standards and MUST NOT create barriers for users with disabilities, language differences, or digital skill limitations.

**Rationale**:
Public sector services must be accessible to all. SCTS serves diverse populations including vulnerable court users, witnesses, and those for whom English is not a first language. AI must reduce, not increase, barriers to justice.

**Implications**:
- Comply with WCAG 2.2 AA as minimum standard
- Multilingual support for key user-facing AI capabilities
- Alternative access methods for users who cannot use digital services
- Plain language outputs avoiding legal jargon where possible
- Testing with users who have diverse accessibility needs

**Validation Gates**:
- [ ] WCAG 2.2 AA compliance verified
- [ ] Multilingual requirements assessed and addressed
- [ ] Non-digital alternatives documented
- [ ] User testing includes accessibility-focused participants
- [ ] Plain language review completed for public-facing outputs

---

### 4. Scalability and Elasticity

**Principle Statement**:
All AI systems MUST be designed to scale to meet variable demand patterns, including peak court sitting periods and high-volume case processing.

**Rationale**:
Court activity varies significantly by day, season, and case type. Systems must handle peak loads without degradation while operating efficiently during quieter periods.

**Implications**:
- Design for stateless, horizontally scalable components
- Capacity planning based on court calendars and historical patterns
- Auto-scaling to handle batch processing of document backlogs
- Graceful degradation under extreme load rather than failure
- Cost-efficient scaling down during low-demand periods

**Validation Gates**:
- [ ] Peak demand scenarios identified and capacity modelled
- [ ] Horizontal scaling demonstrated under load testing
- [ ] Batch processing capabilities for document backlogs
- [ ] Degradation behaviour defined for overload scenarios
- [ ] Cost model accounts for variable demand

---

### 5. Resilience and Continuity

**Principle Statement**:
AI systems MUST gracefully degrade when dependencies fail and MUST NOT disrupt core court operations. Courts MUST be able to function if AI services are unavailable.

**Rationale**:
Court proceedings cannot be delayed due to technology failures. AI capabilities are enhancements, not replacements for core court functions. Systems must fail safely without impacting justice delivery.

**Implications**:
- Manual fallback procedures for all AI-assisted processes
- Circuit breakers to isolate failing AI services
- No AI system as single point of failure for court operations
- Recovery procedures tested and documented
- Staff trained on operation without AI assistance

**Validation Gates**:
- [ ] Manual fallback procedures documented for each AI capability
- [ ] AI service failure does not block court proceedings
- [ ] Recovery time objectives defined (RTO < 4 hours for critical services)
- [ ] Disaster recovery procedures tested quarterly
- [ ] Business continuity plans updated for AI dependencies

---

### 6. Interoperability and Integration

**Principle Statement**:
AI capabilities MUST integrate with existing SCTS systems through well-defined, versioned interfaces. AI services MUST NOT require replacement of core court systems.

**Rationale**:
SCTS has established case management and document systems. AI capabilities must augment these systems, not create parallel data silos or require wholesale system replacement.

**Implications**:
- Standard API contracts for all AI service interfaces
- Integration with existing case management systems
- Document processing outputs compatible with current storage systems
- No duplication of master data in AI systems
- Event-driven integration for loose coupling

**Validation Gates**:
- [ ] API specifications published (OpenAPI, AsyncAPI)
- [ ] Integration with existing systems demonstrated
- [ ] No new master data stores created
- [ ] Versioning and backward compatibility strategy defined
- [ ] Event schemas documented for async integration

---

## II. AI-Specific Principles

### 7. Ethical AI and Bias Prevention

**Principle Statement**:
AI systems MUST be designed to prevent discrimination and MUST be regularly assessed for bias across protected characteristics. Systems MUST NOT perpetuate or amplify existing inequities in the justice system.

**Rationale**:
AI systems can inadvertently encode biases from training data or design decisions. In a justice context, biased AI could have severe consequences for individuals and undermine public trust in the courts.

**Implications**:
- Bias assessment during design, before deployment, and ongoing
- Training data audited for representation and fairness
- Model outputs monitored for differential impact by protected characteristics
- Explainability requirements for any AI influencing case handling
- Third-party ethics review for high-risk AI applications

**Validation Gates**:
- [ ] Bias assessment completed for all protected characteristics
- [ ] Training data provenance and composition documented
- [ ] Ongoing monitoring for differential outcomes
- [ ] Ethics review completed for consequential AI applications
- [ ] Remediation plan for identified bias issues

---

### 8. AI Transparency and Explainability

**Principle Statement**:
AI system capabilities, limitations, and confidence levels MUST be transparent to users. AI-generated outputs MUST be clearly labelled as AI-assisted.

**Rationale**:
Users must understand when they are interacting with AI and have appropriate expectations. Legal professionals need to understand AI limitations to maintain professional accountability.

**Implications**:
- Clear labelling of AI-generated content
- Confidence scores or uncertainty indicators where applicable
- Documented limitations for each AI capability
- Explanation of AI methodology accessible to non-technical users
- Training materials on appropriate use and limitations

**Validation Gates**:
- [ ] AI outputs clearly labelled as AI-assisted
- [ ] Confidence/uncertainty indicators provided where meaningful
- [ ] System limitations documented and communicated to users
- [ ] User guidance materials developed
- [ ] Staff training includes AI limitations

---

### 9. AI Model Governance

**Principle Statement**:
AI models MUST be version-controlled, tested before deployment, and subject to approval before use in production. Model updates MUST not introduce regression in accuracy or fairness.

**Rationale**:
AI models evolve over time. Without proper governance, model changes could introduce errors or bias. Formal change management ensures quality and accountability.

**Implications**:
- Model versioning with clear change documentation
- Testing requirements before model deployment
- Approval workflow for model changes
- Rollback capability for model updates
- Performance and fairness baselines for regression testing

**Validation Gates**:
- [ ] Model versioning and change log maintained
- [ ] Pre-deployment testing requirements defined
- [ ] Approval workflow for model changes implemented
- [ ] Rollback procedures documented and tested
- [ ] Baseline metrics established for regression detection

---

### 10. Data Quality for AI

**Principle Statement**:
AI systems MUST operate on data of known quality. Data quality issues MUST be addressed at source, not masked by AI post-processing.

**Rationale**:
AI systems are only as good as their input data. Poor quality inputs produce unreliable outputs. In a court context, data quality directly affects the reliability of AI-assisted case handling.

**Implications**:
- Data quality assessment before AI processing
- Input validation and rejection of poor-quality inputs
- Quality metrics tracked for all AI data sources
- Source system improvements prioritised over AI workarounds
- Clear feedback loops for data quality issues

**Validation Gates**:
- [ ] Data quality requirements defined for each AI capability
- [ ] Input validation rules implemented
- [ ] Quality metrics tracked and reported
- [ ] Feedback mechanism to source system owners
- [ ] Data quality issues logged and escalated

---

## III. Security and Compliance Principles

### 11. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All AI systems MUST implement defence-in-depth security with zero-trust principles. Security controls MUST be appropriate to the sensitivity of court and personal data being processed.

**Rationale**:
Court systems process highly sensitive information including personal data, legal documents, and potentially vulnerable witness information. Security is paramount to maintain public trust.

**Mandatory Controls**:
- [ ] Multi-factor authentication for all administrative access
- [ ] Role-based access control aligned with job functions
- [ ] Encryption at rest for all stored data
- [ ] Encrypted transport for all network communication
- [ ] Audit logging of all access to sensitive data and AI functions
- [ ] Regular penetration testing and vulnerability assessment
- [ ] Security incident response procedures

**Validation Gates**:
- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to data sensitivity
- [ ] Penetration testing completed before production
- [ ] Incident response procedures documented and tested
- [ ] Security training completed by all staff with AI access

---

### 12. Data Protection and Privacy

**Principle Statement**:
All AI systems MUST comply with UK GDPR and the Data Protection Act 2018. Personal data processing MUST have a lawful basis, and data subject rights MUST be supported.

**Rationale**:
SCTS processes personal data under statutory functions. AI systems must maintain compliance with data protection law and support the rights of individuals whose data is processed.

**Privacy Requirements**:
- Lawful basis identified for all personal data processing
- Privacy impact assessment for new AI capabilities
- Data minimisation - process only what is necessary
- Retention aligned with court record requirements
- Subject access request processes include AI-processed data

**Validation Gates**:
- [ ] Lawful basis documented for personal data processing
- [ ] DPIA completed for AI systems processing personal data
- [ ] Data minimisation review completed
- [ ] Retention schedules aligned with legal requirements
- [ ] SAR process covers AI-processed data

---

### 13. Scottish Public Sector Standards

**Principle Statement**:
All AI systems MUST comply with Scottish Government Digital Strategy, Scottish Public Sector Cyber Resilience Framework, and relevant public sector technology standards.

**Rationale**:
SCTS is a Scottish public body and must align with Scottish Government policy and standards for digital, cyber security, and AI governance.

**Compliance Requirements**:
- Scottish Government AI Strategy alignment
- Cyber Resilience Framework compliance
- Digital Scotland Service Standard
- Records management and archiving requirements
- Scottish Government cloud policy

**Validation Gates**:
- [ ] Scottish Government AI Strategy alignment confirmed
- [ ] Cyber Resilience Framework assessment completed
- [ ] Digital Scotland Service Standard compliance verified
- [ ] Records management requirements addressed
- [ ] Cloud deployment aligned with Scottish Government policy

---

## IV. Data Principles

### 14. Court Records Integrity

**Principle Statement**:
AI systems MUST NOT alter court records. AI-generated content MUST be clearly distinguished from official court records and MUST NOT be presented as authoritative court documentation without proper review and approval.

**Rationale**:
Court records are legal documents with evidentiary weight. AI-generated content must never be confused with or corrupt official records.

**Implications**:
- Read-only access to court records for AI processing
- AI outputs stored separately from official records
- Clear metadata distinguishing AI-generated from official content
- Approval workflow before any AI content enters official records
- Audit trail for any AI contribution to court documentation

**Validation Gates**:
- [ ] Court record systems accessed read-only by AI
- [ ] AI outputs stored in separate repositories
- [ ] Metadata clearly identifies AI-generated content
- [ ] Human approval required before AI content becomes record
- [ ] Audit trail captures all AI contributions

---

### 15. Data Sovereignty and Residency

**Principle Statement**:
All court data and personal data MUST remain within UK jurisdiction. AI processing MUST occur within UK data centres with no transfer to non-UK locations.

**Rationale**:
Court data is subject to UK jurisdiction. Cross-border data transfers introduce legal complexity and risk. UK data residency ensures compliance with Scottish and UK law.

**Implications**:
- Cloud services must offer UK data residency
- AI model training and inference within UK
- No data export to overseas AI services
- Third-party AI services must guarantee UK processing
- Backup and disaster recovery sites within UK

**Validation Gates**:
- [ ] Data residency confirmed as UK only
- [ ] Cloud service contracts specify UK data centres
- [ ] Third-party AI services provide UK processing guarantees
- [ ] No cross-border data transfer identified
- [ ] DR/backup sites confirmed within UK

---

### 16. Single Source of Truth

**Principle Statement**:
Court case management systems remain the authoritative source for case data. AI systems MUST consume data from these sources and MUST NOT create competing data stores.

**Rationale**:
Data consistency is critical in a court environment. Multiple sources of truth create confusion, errors, and potential legal issues.

**Implications**:
- AI systems read from authoritative case systems
- No case data duplication in AI repositories
- AI insights feed back to authoritative systems via approved channels
- Cache/index data clearly labelled as derived, not authoritative
- Synchronisation with source systems for any persisted AI data

**Validation Gates**:
- [ ] Case management system identified as source of truth
- [ ] AI systems consume from, not duplicate, authoritative sources
- [ ] Derived data clearly labelled and synchronised
- [ ] No AI system becomes de facto source of truth
- [ ] Data flow diagrams show source-to-AI relationships

---

## V. Operational Principles

### 17. Observability and Monitoring

**Principle Statement**:
All AI systems MUST emit comprehensive telemetry enabling real-time monitoring, performance tracking, and audit of AI operations.

**Rationale**:
We cannot operate what we cannot observe. AI systems require monitoring for performance, fairness, and compliance with operational standards.

**Telemetry Requirements**:
- **Performance metrics**: Response times, throughput, error rates
- **Quality metrics**: AI accuracy, confidence distributions
- **Fairness metrics**: Outcome distributions by relevant categories
- **Usage metrics**: Adoption, feature usage, user feedback
- **Security metrics**: Access patterns, anomalies, policy violations

**Validation Gates**:
- [ ] Monitoring dashboards configured for all AI services
- [ ] Alerting configured for performance degradation
- [ ] Quality metrics tracked and reviewed regularly
- [ ] Fairness metrics monitored for drift
- [ ] Security monitoring integrated with SOC

---

### 18. Cost Transparency and Optimisation

**Principle Statement**:
AI service costs MUST be transparent, attributed to consuming services, and regularly reviewed for optimisation opportunities.

**Rationale**:
AI services, particularly cloud-based cognitive services, can incur significant and variable costs. Cost transparency enables informed decisions and efficient resource use.

**Implications**:
- Cost allocation tagging for all AI resources
- Regular cost review and optimisation
- Cost thresholds and alerts for unexpected increases
- Unit cost metrics (cost per document, per transaction)
- Efficiency improvements tracked as cost savings

**Validation Gates**:
- [ ] Cost allocation model defined
- [ ] Cost monitoring and alerting configured
- [ ] Monthly cost review process established
- [ ] Unit cost metrics calculated and tracked
- [ ] Optimisation opportunities identified and pursued

---

## VI. Development and Delivery Principles

### 19. Iterative Delivery and Learning

**Principle Statement**:
AI capabilities SHOULD be delivered iteratively through proof-of-concept, pilot, and progressive rollout phases. Learning from each phase MUST inform subsequent phases.

**Rationale**:
AI systems often perform differently in production than in development. Iterative delivery reduces risk and enables learning before full-scale deployment.

**Delivery Phases**:
1. **Proof of Concept**: Technical feasibility, limited scope
2. **Pilot**: Real users, controlled environment, success criteria
3. **Limited Production**: Gradual rollout with monitoring
4. **Full Production**: Organisation-wide deployment

**Validation Gates**:
- [ ] Success criteria defined for each phase
- [ ] Learning captured and documented between phases
- [ ] Go/no-go decision points with clear criteria
- [ ] Rollback plan for each phase
- [ ] User feedback mechanisms in place

---

### 20. Automation and Repeatability

**Principle Statement**:
AI system deployment, testing, and configuration MUST be automated and repeatable. Manual processes SHOULD be eliminated except where human judgement is required.

**Rationale**:
Manual processes introduce errors and inconsistency. Automated, repeatable processes enable reliable delivery and rapid response to issues.

**Implications**:
- Infrastructure as code for all AI infrastructure
- Automated testing including model validation
- Deployment pipelines for model and application updates
- Configuration management for AI parameters
- Automated documentation and change logs

**Validation Gates**:
- [ ] Infrastructure defined as code
- [ ] Automated test suite for AI components
- [ ] CI/CD pipeline for deployments
- [ ] Configuration versioned and auditable
- [ ] No manual steps in production deployments

---

## VII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:
- Technical constraints that prevent compliance
- Regulatory or legal requirements
- Transitional state during migration
- Pilot/proof-of-concept with defined end date

**Exception Request Requirements**:
- [ ] Justification with business/technical rationale
- [ ] Risk assessment for the exception
- [ ] Compensating controls where applicable
- [ ] Expiration date (exceptions are time-bound, max 12 months)
- [ ] Remediation plan to achieve compliance

**Approval Process**:
1. Submit exception request to Enterprise Architecture team
2. Review by architecture review board
3. CDO approval for exceptions to critical principles
4. Document exception in project architecture documentation
5. Quarterly review of all active exceptions

---

## VIII. Principle Summary

| Principle | Category | Criticality | Key Validation |
|-----------|----------|-------------|----------------|
| Justice-Centred Design | Strategic | CRITICAL | Use case traces to justice mission |
| Human-in-the-Loop | Strategic | CRITICAL | Human approval for consequential decisions |
| Accessibility and Inclusive Design | Strategic | HIGH | WCAG 2.2 AA compliance |
| Scalability and Elasticity | Strategic | HIGH | Load testing demonstrates scaling |
| Resilience and Continuity | Strategic | HIGH | Manual fallbacks documented |
| Interoperability | Strategic | HIGH | API specifications published |
| Ethical AI and Bias Prevention | AI-Specific | CRITICAL | Bias assessment completed |
| AI Transparency | AI-Specific | HIGH | AI outputs clearly labelled |
| AI Model Governance | AI-Specific | HIGH | Model versioning and approval |
| Data Quality for AI | AI-Specific | HIGH | Input validation implemented |
| Security by Design | Security | CRITICAL | Threat model and pen testing |
| Data Protection | Security | CRITICAL | DPIA completed |
| Scottish Public Sector Standards | Security | HIGH | Framework compliance verified |
| Court Records Integrity | Data | CRITICAL | Read-only access to records |
| Data Sovereignty | Data | CRITICAL | UK data residency confirmed |
| Single Source of Truth | Data | HIGH | No data duplication |
| Observability | Operational | HIGH | Monitoring dashboards live |
| Cost Transparency | Operational | MEDIUM | Cost allocation in place |
| Iterative Delivery | Delivery | MEDIUM | Phase gates defined |
| Automation | Delivery | HIGH | CI/CD pipeline exists |

---

## Appendix: AI Use Cases and Principle Application

The following AI capabilities are planned for SCTS. This table maps each to critical principles:

| Capability | Critical Principles | Special Considerations |
|------------|--------------------|-----------------------|
| Document Intelligence | Court Records Integrity, Data Quality, AI Transparency | Read-only access; accuracy validation |
| Speech Transcription | Accessibility, Human-in-the-Loop, Data Protection | Multilingual support; privacy for courtroom audio |
| Translation Services | Accessibility, AI Transparency, Data Sovereignty | UK processing; quality assurance |
| Cognitive Search | Interoperability, Single Source of Truth, Security | Index vs source data distinction |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-01-17
**ArcKit Version**: 0.6.0
**Project**: SCTS GenAI Strategy (Project 001)
**AI Model**: Claude Opus 4.5
