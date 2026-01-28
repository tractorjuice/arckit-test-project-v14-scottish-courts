# Risk Register

> **Template Status**: Live | **Version**: 0.11.2 | **Command**: `/arckit.risk`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.1 |
| **Document Type** | HM Treasury Orange Book Risk Register |
| **Project** | SCTS GenAI Programme (Project 001) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-01-17 |
| **Last Modified** | 2026-01-26 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-02-26 |
| **Owner** | Chief Digital Information Officer, SCTS |
| **Risk Register Owner** | Chief Executive, SCTS |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | CDi Function, Legal Services, DPO, SIRO, Steering Committee |
| **Framework** | HM Treasury Orange Book (2023) |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-01-17 | ArcKit AI | Initial creation from `/arckit.risk` command | [PENDING] | [PENDING] |
| 1.1 | 2026-01-26 | ArcKit AI | Updated to template v0.11.2 format | [PENDING] | [PENDING] |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** 20 risks across 6 categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 4 | 0 | ↓ 100% |
| **High** (13-19) | 8 | 4 | ↓ 50% |
| **Medium** (6-12) | 6 | 12 | ↑ (improved from higher) |
| **Low** (1-5) | 2 | 4 | ↑ (improved from higher) |
| **TOTAL SCORE** | 267 | 168 | **↓ 37%** |

### Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness |
|----------|-------|--------------|--------------|----------------------|
| **STRATEGIC** | 4 | 16.0 | 10.3 | 36% reduction |
| **OPERATIONAL** | 4 | 12.0 | 7.5 | 38% reduction |
| **FINANCIAL** | 3 | 13.0 | 8.0 | 38% reduction |
| **COMPLIANCE** | 3 | 14.7 | 9.0 | 39% reduction |
| **REPUTATIONAL** | 3 | 15.3 | 9.3 | 39% reduction |
| **TECHNOLOGY** | 3 | 13.3 | 8.3 | 38% reduction |

### Overall Risk Assessment

**Overall Residual Risk Score:** 168/500
**Risk Reduction from Controls:** 37% reduction from inherent risk
**Risk Profile Status:** ⚠️ Concerning - 4 high residual risks require attention before production

### Risks Exceeding Appetite

**Number of risks exceeding organizational appetite:** 4 risks

| Risk ID | Title | Category | Residual Score | Appetite | Excess | Escalation |
|---------|-------|----------|----------------|----------|--------|------------|
| R-001 | Judicial loss of confidence | STRATEGIC | 15 | 12 | +3 | Chief Executive approval required |
| R-004 | AI quality issues damage reputation | REPUTATIONAL | 16 | 12 | +4 | Steering Committee escalation |
| R-007 | Security breach of court data | TECHNOLOGY | 15 | 12 | +3 | SIRO approval required |
| R-010 | UK GDPR non-compliance enforcement | COMPLIANCE | 15 | 12 | +3 | DPO escalation to ICO |

### Top 5 Critical Risks Requiring Immediate Attention

1. **R-004** (REPUTATIONAL, High 16): AI quality issues damage reputation - Owner: Chief Executive - Status: In Progress
2. **R-001** (STRATEGIC, High 15): Judicial loss of confidence - Owner: Chief Executive - Status: In Progress
3. **R-007** (TECHNOLOGY, High 15): Security breach of court data - Owner: CDiO - Status: In Progress
4. **R-010** (COMPLIANCE, High 15): UK GDPR non-compliance enforcement - Owner: Legal Services Director - Status: In Progress
5. **R-002** (STRATEGIC, Medium 12): Staff resistance undermines adoption - Owner: CDiO - Status: Open

### Key Findings and Recommendations

**Key Findings:**
1. **Reputational and judicial confidence risks are highest** - AI errors in a court context carry severe consequences for public trust
2. **Security risks require immediate attention** - Penetration testing and SIEM implementation must complete before production
3. **Compliance framework is strong** - DPIA and ATRS completed, but EqIA and bias audit still pending
4. **Human-in-the-loop design significantly reduces risk** - Most inherent Critical risks reduced to High/Medium
5. **Staff adoption risks are material** - Change management and training critical success factors

**Recommendations:**
1. **Escalate R-001, R-004, R-007, R-010** to Steering Committee immediately (exceed appetite)
2. **Complete penetration testing and SIEM** before production deployment (blocks R-007)
3. **Accelerate bias audit** for all 10 priority languages (blocks R-004)
4. **Implement staff engagement programme** to address R-002 (job security concerns)
5. **Obtain SIRO sign-off** on residual risks before PoC completion

---

## A. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

**Likelihood × Impact Matrix - Inherent Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       |       | R-017 |       |       |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       | R-012 | R-002 | R-001 | R-004 |
       |                |       | R-018 | R-005 | R-007 |       |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       | R-020 | R-011 | R-006 | R-003 | R-009 |
       |                |       | R-019 | R-008 | R-010 |       |
       |                |       |       | R-015 |       |       |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       |       | R-014 | R-013 |       |       |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           |       |       | R-016 |       |       |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

**Risk Zones:**
- 🟥 **Critical (20-25)**: R-001, R-004, R-007, R-009 - Immediate escalation required
- 🟧 **High (13-19)**: R-002, R-003, R-005, R-006, R-008, R-010, R-017, R-018 - Senior management attention
- 🟨 **Medium (6-12)**: R-011, R-012, R-013, R-014, R-015, R-019 - Management monitoring
- 🟩 **Low (1-5)**: R-016, R-020 - Routine monitoring

### Residual Risk Matrix (After Controls)

**Likelihood × Impact Matrix - Residual Risk Positions**

```
LIKELIHOOD ↑
     5 | Almost Certain |       |       |       |       |       |
       |                |-------|-------|-------|-------|-------|
     4 | Likely         |       |       | R-004 |       |       |
       |                |-------|-------|-------|-------|-------|
     3 | Possible       |       | R-002 | R-001 | R-007 |       |
       |                |       | R-005 | R-003 | R-010 |       |
       |                |       | R-012 | R-017 |       |       |
       |                |-------|-------|-------|-------|-------|
     2 | Unlikely       | R-020 | R-011 | R-006 | R-009 |       |
       |                |       | R-014 | R-008 |       |       |
       |                |       | R-018 | R-015 |       |       |
       |                |       | R-019 |       |       |       |
       |                |-------|-------|-------|-------|-------|
     1 | Rare           |       | R-016 | R-013 |       |       |
       |________________|_______|_______|_______|_______|_______|
                            1       2       3       4       5
                        Negligible Minor  Moderate Major Catastrophic
                                      IMPACT →
```

**Risk Movement Analysis:**
- ✅ **Significant Improvement**: R-009 (20→8), R-001 (20→15), R-007 (20→15) - Controls very effective
- ⚠️ **Moderate Improvement**: R-004 (20→16), R-002 (16→12), R-010 (16→15) - Additional controls needed
- 📊 **Stable Low**: R-016, R-020 - Continue current approach

---

## B. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-004 | AI quality issues damage reputation | REPUTATIONAL | 20 | 16 | Chief Executive | In Progress | Treat |
| 2 | R-001 | Judicial loss of confidence | STRATEGIC | 20 | 15 | Chief Executive | In Progress | Treat |
| 3 | R-007 | Security breach of court data | TECHNOLOGY | 20 | 15 | CDiO | In Progress | Treat |
| 4 | R-010 | UK GDPR non-compliance enforcement | COMPLIANCE | 16 | 15 | Legal Services Director | In Progress | Treat |
| 5 | R-002 | Staff resistance undermines adoption | OPERATIONAL | 16 | 12 | CDiO | Open | Treat |
| 6 | R-003 | Scottish Government policy change | STRATEGIC | 15 | 12 | Chief Executive | Monitoring | Treat |
| 7 | R-017 | Translation accuracy fails court standard | TECHNOLOGY | 16 | 12 | CDiO | In Progress | Treat |
| 8 | R-005 | Parliamentary scrutiny of AI in courts | REPUTATIONAL | 15 | 10 | Chief Executive | Monitoring | Treat |
| 9 | R-006 | Key personnel departure | OPERATIONAL | 12 | 9 | CDiO | In Progress | Transfer |
| 10 | R-009 | Service outage during court session | TECHNOLOGY | 20 | 8 | CDiO | Monitoring | Treat |

---

## C. Detailed Risk Register

### STRATEGIC Risks

---

### Risk R-001: Judicial Loss of Confidence

**Category:** STRATEGIC
**Status:** In Progress
**Risk Owner:** Chief Executive, SCTS (from Stakeholder RACI: Accountable for Go-Live Approval)
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
An AI error, security incident, perceived overreach into judicial functions, or mishandling of court records causes the judiciary (led by the Lord President) to lose confidence in the AI programme, leading to programme suspension, termination, or severe scope restrictions that undermine strategic objectives.

**Root Cause:**
- Judiciary's constitutional independence and conservative culture towards technology
- Potential perception that AI could influence case outcomes
- Historical concerns about technology affecting judicial authority

**Trigger Events:**
- AI-generated content enters official court records without proper approval
- AI translation error causes misunderstanding in court proceedings
- Security breach exposes sensitive case data
- Negative media coverage of AI in Scottish courts
- Comparison with AI failures in other justice systems

**Consequences if Realized:**
- Programme suspension or termination (100% goal failure)
- £1M+ sunk investment lost
- Scottish Government political embarrassment
- Delay to court modernisation by 3-5 years
- Damage to SCTS-judiciary relationship

**Affected Stakeholders:**
- **Lord President** (SD-1): Primary stakeholder - confidence directly at risk
- **Chief Executive** (SD-2): Accountable for programme success and judicial relations
- **Cabinet Secretary** (SD-10): Political accountability if programme fails publicly
- **CDiO** (SD-3): Innovation leadership reputation at risk

**Related Objectives:**
- **Goal G-4**: Zero record integrity incidents (CRITICAL - directly threatened)
- **Outcome O-3**: Maintained judicial confidence (PRIMARY OUTCOME)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Judiciary inherently cautious about AI; any incident will be noticed |
| **Impact** | 5 (Catastrophic) | Programme would halt; strategic objectives unachievable |
| **Inherent Score** | **20 (Critical)** | L4 × I5 = 20 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-001.1 | Human-in-the-loop design - AI cannot modify records autonomously | Strong | AI Architect | Architecture Principle 2, FR-003 |
| C-001.2 | Read-only AI access to court records (NFR-SEC-006) | Strong | CDiO | Architecture Principle 14 |
| C-001.3 | Clear scope boundaries - administrative AI only, no judicial functions | Strong | Chief Executive | Stakeholder communication plan |
| C-001.4 | Regular judicial briefings (quarterly) | Adequate | Chief Executive | Communication plan |
| C-001.5 | Conservative deployment approach - phased rollout | Adequate | CDiO | Project plan |

**Overall Control Effectiveness:** Strong (4 of 5 controls robust)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Controls reduce but don't eliminate risk; judicial caution remains |
| **Impact** | 5 (Catastrophic) | Impact unchanged if risk materializes |
| **Residual Score** | **15 (High)** | L3 × I5 = 15 |

#### Risk Response

**Response Strategy:** **TREAT** - Mitigate through additional controls and stakeholder engagement

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-001.1 | Establish Judicial Advisory Group for AI oversight | Chief Executive | 2026-02-28 | 12 |
| A-001.2 | Conduct judicial briefing before PoC | CDiO | 2026-03-15 | 12 |
| A-001.3 | Create "AI in Courts" transparency statement for judicial approval | Legal Services | 2026-03-31 | 12 |
| A-001.4 | Define immediate incident escalation path to Lord President's office | Chief Executive | 2026-02-15 | 12 |

**Success Criteria:** Judicial confidence score maintained or improved; zero incidents escalated to Lord President; positive judicial feedback on quarterly briefings

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (STRATEGIC)** | Medium (12) |
| **Current Residual Score** | 15 |
| **Assessment** | ⚠️ **Exceeds Appetite** |
| **Escalation Required** | YES - Chief Executive approval required to proceed |
| **Justification** | Strategic risk inherent to AI in justice; mitigated through governance and engagement |

---

### Risk R-002: Staff Resistance Undermines Adoption

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** CDiO, SCTS (from Stakeholder RACI: Accountable for Staff Training)
**Action Owner:** HR Director, SCTS

#### Risk Identification

**Risk Description:**
Court clerks and administrative staff resist AI adoption due to job security fears, poor tool experience, or lack of training, resulting in low system usage, unrealised efficiency benefits, and inability to demonstrate ROI on the investment.

**Root Cause:**
- Fear of AI replacing jobs (Conflict 2 in stakeholder analysis)
- Change resistance in traditional workforce
- Previous negative technology implementation experiences
- Lack of understanding of AI capabilities and limitations

**Trigger Events:**
- Communication about AI focuses on "efficiency" without job security reassurance
- Tools are difficult to use or require significant workflow changes
- Early adopters report negative experiences
- Trade union raises concerns about job impacts
- Insufficient training before rollout

**Consequences if Realized:**
- <50% adoption rate (target is 80%)
- Efficiency goals unmet (G-1: 60% processing time reduction)
- £500K productivity gains unrealised
- Staff morale damage
- Negative perception spreads to other digital initiatives

**Affected Stakeholders:**
- **Clerks of Court** (SD-6): Primary users - job security and tools concern
- **Court Admin Managers** (SD-5): Workload reduction goal threatened
- **HR Director**: Change management accountability
- **Finance Director** (SD-9): ROI demonstration at risk

**Related Objectives:**
- **Goal G-1**: Reduce document processing time (dependent on adoption)
- **Goal G-6**: Positive staff experience (directly threatened)
- **Outcome O-2**: Operational efficiency gains (dependent on adoption)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Change resistance common; job security fears prevalent |
| **Impact** | 4 (Major) | Goals unmet but programme continues; recoverable |
| **Inherent Score** | **16 (High)** | L4 × I4 = 16 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-002.1 | Staff involvement in design and testing | Adequate | CDiO | Requirements FR-013 (feedback) |
| C-002.2 | Training programme (BR-006) | Planned | HR Director | Requirement documented |
| C-002.3 | Communication plan for clerks | Adequate | CDiO | Stakeholder communication plan |
| C-002.4 | "AI augments not replaces" messaging | Planned | Chief Executive | Conflict resolution strategy |

**Overall Control Effectiveness:** Adequate (controls planned but not implemented)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Good plan but execution uncertain |
| **Impact** | 4 (Major) | Impact unchanged |
| **Residual Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Risk Response

**Response Strategy:** **TREAT** - Comprehensive change management programme

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-002.1 | Issue Chief Executive message on job security commitment | Chief Executive | 2026-02-15 | 9 |
| A-002.2 | Identify and train AI Champions in each court | HR Director | 2026-03-31 | 9 |
| A-002.3 | Conduct staff listening sessions before rollout | HR Director | 2026-03-15 | 9 |
| A-002.4 | Create early adopter recognition programme | CDiO | 2026-04-30 | 9 |

**Success Criteria:** 75% staff satisfaction with AI tools; 80% adoption rate; net workload reduction reported

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (OPERATIONAL)** | Medium (12) |
| **Current Residual Score** | 12 |
| **Assessment** | ✅ **Within Appetite** |
| **Escalation Required** | NO |

---

### Risk R-003: Scottish Government Policy Change

**Category:** STRATEGIC
**Status:** Monitoring
**Risk Owner:** Chief Executive, SCTS
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
Scottish Government changes policy direction on AI in public services, changes ministerial priorities, or introduces new regulatory requirements that conflict with programme approach, requiring significant scope changes or programme pause.

**Root Cause:**
- Political environment can change (elections, cabinet reshuffles)
- AI policy is evolving rapidly
- Programme timeline spans multiple political cycles

**Trigger Events:**
- Ministerial reshuffle changes Cabinet Secretary for Justice
- New Scottish Government AI Strategy with different requirements
- AI incident elsewhere in public sector triggers policy tightening
- Budget constraints force digital spending cuts
- Election manifesto commitments change priorities

**Consequences if Realized:**
- Programme pause for policy review (3-6 months)
- Scope changes requiring rework
- Budget reallocated to other priorities
- Loss of momentum and team morale

**Affected Stakeholders:**
- **Cabinet Secretary** (SD-10): Policy owner
- **Scottish Government Digital Directorate**: Policy oversight
- **Chief Executive**: Accountable for alignment

**Related Objectives:**
- **Goal G-5**: Scottish Government compliance (directly affected)
- **Outcome O-4**: Regulatory compliance (dependent on stable policy)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Policy changes possible but AI agenda stable |
| **Impact** | 5 (Catastrophic) | Major scope change or pause |
| **Inherent Score** | **15 (High)** | L3 × I5 = 15 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-003.1 | Alignment with Scottish Government AI Strategy | Strong | CDiO | AI Playbook assessment completed |
| C-003.2 | Regular engagement with Digital Directorate | Adequate | Chief Executive | Stakeholder communication plan |
| C-003.3 | Ministerial briefings (quarterly) | Adequate | Chief Executive | Communication plan |

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | External factor - limited control |
| **Impact** | 4 (Major) | Strong alignment reduces scope of impact |
| **Residual Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Risk Response

**Response Strategy:** **TREAT** - Monitor and maintain alignment

**Success Criteria:** Continued alignment with Scottish Government AI Strategy; no policy conflicts requiring scope change

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (STRATEGIC)** | Medium (12) |
| **Current Residual Score** | 12 |
| **Assessment** | ✅ **Within Appetite** |

---

### Risk R-018: Programme benefits not demonstrated

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Chief Executive, SCTS
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
The programme fails to demonstrate measurable benefits (efficiency gains, access improvements) leading to questions about value for money and difficulty securing continued investment.

**Root Cause:**
- AI benefits can be difficult to measure
- Baseline measurements not established
- Benefits attribution complex (AI vs other factors)

**Trigger Events:**
- Post-implementation review shows limited measurable improvement
- Audit Office enquiry into AI investment
- Budget pressure requires ROI justification
- Comparison with other departments' AI ROI

**Consequences if Realized:**
- Future AI investment rejected
- Political embarrassment
- Inability to scale programme
- Reputational damage to CDi function

**Affected Stakeholders:**
- **Finance Director** (SD-9): Value for money accountability
- **Chief Executive**: Investment decision-maker
- **Cabinet Secretary**: Political accountability

**Related Objectives:**
- **Outcome O-2**: Operational efficiency gains (directly measured)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | AI benefits often overstated; measurement challenging |
| **Impact** | 3 (Moderate) | Financial and reputational but programme continues |
| **Inherent Score** | **12 (Medium)** | L4 × I3 = 12 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-018.1 | Clear success metrics defined in goals | Strong | CDiO | Stakeholder goals G-1 to G-6 |
| C-018.2 | Baseline measurements planned | Adequate | CDiO | Goal measurement methods |
| C-018.3 | Business case with quantified benefits | Adequate | Finance Director | Research findings £716K TCO |

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Good planning reduces likelihood |
| **Impact** | 3 (Moderate) | Impact unchanged |
| **Residual Score** | **9 (Medium)** | L3 × I3 = 9 |

#### Risk Response

**Response Strategy:** **TREAT**

**Success Criteria:** Baseline established before PoC; 60% processing time reduction demonstrated

---

### REPUTATIONAL Risks

---

### Risk R-004: AI Quality Issues Damage Reputation

**Category:** REPUTATIONAL
**Status:** In Progress
**Risk Owner:** Chief Executive, SCTS
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
AI errors (mistranslation in court proceedings, document misclassification, search failures returning wrong results) are publicised through media, FOI requests, or parliamentary questions, severely damaging SCTS reputation and public trust in AI use in courts.

**Root Cause:**
- AI systems can produce errors
- Court context amplifies error consequences
- High public interest in AI in justice
- Media focus on AI failures

**Trigger Events:**
- Mistranslation causes misunderstanding in court proceeding
- Document misclassification affects case handling
- Error discovered through subject access request
- Media investigation into AI in Scottish courts
- Comparison with AI errors in other jurisdictions

**Consequences if Realized:**
- National media coverage damaging SCTS reputation
- Parliamentary questions from opposition
- Loss of public trust in court AI
- Staff demoralised by negative publicity
- Possible ICO investigation if data error

**Affected Stakeholders:**
- **Cabinet Secretary** (SD-10): Political accountability for negative publicity
- **Court Users** (SD-11): Trust in justice system affected
- **Legal Profession** (SD-12): Confidence in AI-processed documents
- **Lord President** (SD-1): Judicial confidence damaged

**Related Objectives:**
- **Goal G-2**: Multilingual access (dependent on translation quality)
- **Goal G-3**: Cognitive search (dependent on accuracy)
- **Outcome O-1**: Improved access to justice (threatened by quality failures)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | AI errors will occur; question is detection and response |
| **Impact** | 5 (Catastrophic) | Media coverage of AI error in courts would be severe |
| **Inherent Score** | **20 (Critical)** | L4 × I5 = 20 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-004.1 | Human-in-the-loop review of AI outputs | Strong | CDiO | Architecture Principle 2, FR-003 |
| C-004.2 | Confidence scores with all AI outputs | Strong | AI Architect | FR-003, FR-011 |
| C-004.3 | AI output labelling (transparency) | Strong | CDiO | FR-011 |
| C-004.4 | User feedback mechanism | Adequate | CDiO | FR-013 |
| C-004.5 | Human interpreter mandatory for complex matters | Strong | CDiO | BC-2 |

**Overall Control Effectiveness:** Strong

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Errors may still slip through; human review imperfect |
| **Impact** | 4 (Major) | Controls reduce severity but reputational damage still significant |
| **Residual Score** | **16 (High)** | L4 × I4 = 16 |

#### Risk Response

**Response Strategy:** **TREAT** - Additional quality controls and response planning

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-004.1 | Complete bias audit for all 10 priority languages | AI Architect | 2026-04-30 | 12 |
| A-004.2 | Establish AI quality review board | CDiO | 2026-03-31 | 12 |
| A-004.3 | Create media response plan for AI incidents | Communications | 2026-03-15 | 12 |
| A-004.4 | Third-party ethics review for translation services | DPO | 2026-05-31 | 12 |

**Success Criteria:** Bias audit passed for all languages; zero publicised AI errors; rapid response capability tested

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (REPUTATIONAL)** | Medium (12) |
| **Current Residual Score** | 16 |
| **Assessment** | ⚠️ **Exceeds Appetite** |
| **Escalation Required** | YES - Steering Committee approval required |
| **Justification** | Inherent to AI deployment; comprehensive controls in place; residual risk accepted with additional mitigations |

---

### Risk R-005: Parliamentary Scrutiny of AI in Courts

**Category:** REPUTATIONAL
**Status:** Monitoring
**Risk Owner:** Chief Executive, SCTS
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
Parliamentary questions, Justice Committee inquiry, or FOI requests expose aspects of AI deployment that generate negative political scrutiny, even if no actual error has occurred.

**Root Cause:**
- High political interest in AI
- Opposition parties looking for issues
- General public concern about AI
- FOI transparency requirements

**Trigger Events:**
- MSP parliamentary question about AI in courts
- Justice Committee requests evidence on AI deployment
- FOI request reveals internal concerns or issues
- Media "investigation" into court AI
- Campaign group raises concerns about AI in justice

**Consequences if Realized:**
- Ministerial embarrassment
- Programme pause for parliamentary review
- Negative media coverage
- Resource diversion to respond
- Staff anxiety and morale impact

**Affected Stakeholders:**
- **Cabinet Secretary** (SD-10): Political accountability
- **Chief Executive**: Response accountability
- **Scottish Parliament Justice Committee**: Oversight role

**Related Objectives:**
- **Outcome O-4**: Regulatory compliance and trust (parliamentary confidence)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | AI is politically topical; questions likely |
| **Impact** | 5 (Catastrophic) | Parliamentary inquiry would significantly impact programme |
| **Inherent Score** | **15 (High)** | L3 × I5 = 15 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-005.1 | ATRS record published (transparency) | Strong | CDiO | ATRS completed |
| C-005.2 | Ministerial briefings (quarterly) | Adequate | Chief Executive | Communication plan |
| C-005.3 | Proactive parliamentary engagement | Planned | Chief Executive | To be implemented |

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Transparency reduces likelihood of negative enquiry |
| **Impact** | 5 (Catastrophic) | Impact unchanged if occurs |
| **Residual Score** | **10 (Medium)** | L2 × I5 = 10 |

#### Risk Response

**Response Strategy:** **TREAT** - Proactive transparency and engagement

**Success Criteria:** No negative parliamentary outcomes; ATRS record published; positive ministerial engagement

---

### Risk R-013: Negative comparison with other AI deployments

**Category:** REPUTATIONAL
**Status:** Monitoring
**Risk Owner:** Chief Executive, SCTS
**Action Owner:** CDiO, SCTS

#### Risk Identification

**Risk Description:**
SCTS AI deployment is unfavourably compared with AI failures in other jurisdictions or organisations, creating guilt by association even if SCTS systems work well.

**Root Cause:**
- Global AI deployments experiencing issues
- Media tendency to generalise AI stories
- Public doesn't distinguish between different AI systems

**Consequences if Realized:**
- Reputational damage by association
- Increased scrutiny
- Public resistance to AI in courts

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | External factor; can differentiate |
| **Impact** | 3 (Moderate) | Manageable with communication |
| **Inherent Score** | **6 (Medium)** | L2 × I3 = 6 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 (Rare) | Differentiation through transparency |
| **Impact** | 3 (Moderate) | Impact unchanged |
| **Residual Score** | **3 (Low)** | L1 × I3 = 3 |

#### Risk Response

**Response Strategy:** **TOLERATE** - Monitor and respond as needed

---

### TECHNOLOGY Risks

---

### Risk R-007: Security Breach of Court Data

**Category:** TECHNOLOGY
**Status:** In Progress
**Risk Owner:** CDiO, SCTS (from RACI: Accountable for Incident Response)
**Action Owner:** ICT Operations Manager

#### Risk Identification

**Risk Description:**
A security vulnerability in AI systems or supporting infrastructure is exploited, resulting in unauthorised access to sensitive court data, triggering regulatory reporting requirements and severe reputational damage.

**Root Cause:**
- AI systems introduce new attack surface
- Cloud deployments require robust security configuration
- Sensitive court data is high-value target

**Trigger Events:**
- Vulnerability in Azure AI services exploited
- Misconfigured access controls
- Insider threat or credential compromise
- Supply chain attack via third-party component
- Social engineering targeting AI admin credentials

**Consequences if Realized:**
- ICO notification required within 72 hours
- Potential ICO enforcement action (significant fines)
- Severe reputational damage (national news)
- Judicial confidence severely damaged
- Potential legal action from affected data subjects
- Criminal investigation if court proceedings compromised

**Affected Stakeholders:**
- **DPO** (SD-8): Regulatory compliance responsibility
- **ICO** (SD-13): Enforcement authority
- **Court Users** (SD-11): Data subjects affected
- **Lord President** (SD-1): Judicial confidence impacted
- **Cabinet Secretary** (SD-10): Political fallout

**Related Objectives:**
- **Goal G-4**: Zero record integrity incidents (directly threatened)
- **Goal G-5**: Compliance (ICO enforcement)
- **Outcome O-3**: Maintained judicial confidence (severely threatened)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Cyber attacks on public sector common; AI systems targeted |
| **Impact** | 5 (Catastrophic) | Court data breach would be national news; regulatory penalties |
| **Inherent Score** | **20 (Critical)** | L4 × I5 = 20 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-007.1 | Azure security certifications (ISO 27001, SOC 2) | Strong | Microsoft | Research findings |
| C-007.2 | UK data residency only (NFR-SEC-004) | Strong | CDiO | Contractual guarantee |
| C-007.3 | Encryption at rest (AES-256) and transit (TLS 1.3) | Strong | ICT Operations | NFR-SEC-003 |
| C-007.4 | RBAC with MFA for admin (NFR-SEC-001, 002) | Strong | ICT Operations | Requirements |
| C-007.5 | Read-only AI access to court records | Strong | CDiO | NFR-SEC-006 |

**Overall Control Effectiveness:** Strong (but testing incomplete)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Strong controls reduce likelihood but breach still possible |
| **Impact** | 5 (Catastrophic) | Impact unchanged if breach occurs |
| **Residual Score** | **15 (High)** | L3 × I5 = 15 |

#### Risk Response

**Response Strategy:** **TREAT** - Complete security testing and monitoring

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-007.1 | Conduct penetration testing before production | Security Team | 2026-04-30 | 10 |
| A-007.2 | Implement Azure Sentinel SIEM | ICT Operations | 2026-04-30 | 10 |
| A-007.3 | Document security incident response plan | Security Team | 2026-03-31 | 10 |
| A-007.4 | Obtain Cyber Essentials Plus certification | Security Team | 2026-07-30 | 10 |

**Success Criteria:** Penetration testing completed with no critical findings; SIEM operational; Cyber Essentials Plus obtained; zero security incidents

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (TECHNOLOGY)** | Medium (12) |
| **Current Residual Score** | 15 |
| **Assessment** | ⚠️ **Exceeds Appetite** |
| **Escalation Required** | YES - SIRO approval required |
| **Justification** | Critical security testing in progress; residual risk will reduce to 10 after mitigations complete |

---

### Risk R-009: Service Outage During Court Session

**Category:** TECHNOLOGY
**Status:** Monitoring
**Risk Owner:** CDiO, SCTS
**Action Owner:** ICT Operations Manager

#### Risk Identification

**Risk Description:**
AI services (particularly translation) become unavailable during active court session due to infrastructure failure, Azure outage, or system error, disrupting court proceedings and potentially causing delays or adjournments.

**Root Cause:**
- Dependency on cloud services
- Real-time translation requires high availability
- Complex technology stack

**Trigger Events:**
- Azure regional outage
- Network connectivity failure
- AI service API rate limiting
- Memory or capacity exhaustion
- Software bug causing crash

**Consequences if Realized:**
- Court session delayed or adjourned
- Judge and legal professionals frustrated
- Court user experience degraded
- Media story about technology failure
- Judicial confidence impacted

**Affected Stakeholders:**
- **Lord President** (SD-1): Courts disrupted
- **Court Users** (SD-11): Service failure
- **CDiO** (SD-3): Technical failure accountability

**Related Objectives:**
- **Outcome O-3**: Maintained judicial confidence

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Outages will occur; question is timing and duration |
| **Impact** | 5 (Catastrophic) | Court session disruption is high visibility |
| **Inherent Score** | **20 (Critical)** | L4 × I5 = 20 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-009.1 | Manual fallback to human interpreters (BC-2) | Strong | CDiO | FR-014 |
| C-009.2 | Circuit breaker pattern (NFR-A-003) | Strong | AI Architect | Requirements |
| C-009.3 | Graceful degradation design | Strong | AI Architect | NFR-A-003 |
| C-009.4 | Azure 99.9% SLA | Adequate | Microsoft | Contract |
| C-009.5 | UK multi-region DR | Strong | CDiO | NFR-A-002 |

**Overall Control Effectiveness:** Strong (fallback critical)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Fallback procedures make disruption unlikely |
| **Impact** | 4 (Major) | Impact reduced as fallback available |
| **Residual Score** | **8 (Medium)** | L2 × I4 = 8 |

#### Risk Response

**Response Strategy:** **TREAT** - Maintain and test fallback procedures

**Success Criteria:** Fallback procedures tested quarterly; zero court session disruptions from AI outage

---

### Risk R-017: Translation Accuracy Fails Court Standard

**Category:** TECHNOLOGY
**Status:** In Progress
**Risk Owner:** CDiO, SCTS
**Action Owner:** AI Architect

#### Risk Identification

**Risk Description:**
AI translation services fail to achieve the accuracy level required for court proceedings, particularly for legal terminology, resulting in the capability being withdrawn or severely restricted.

**Root Cause:**
- Legal terminology highly specialised
- Some languages have limited training data
- Court proceedings language is formal and precise

**Trigger Events:**
- Accuracy testing shows <85% for priority languages
- Legal terminology errors identified in testing
- Professional interpreter feedback negative
- Judicial review identifies translation concerns

**Consequences if Realized:**
- Translation capability withdrawn or restricted
- Goal G-2 (multilingual access) unmet
- Investment in translation capability lost
- Access to justice for non-English speakers not improved

**Affected Stakeholders:**
- **Court Users** (SD-11): Non-English speakers affected
- **CDiO** (SD-3): Technical capability failure
- **Cabinet Secretary** (SD-10): Access to justice commitment unmet

**Related Objectives:**
- **Goal G-2**: Enable multilingual court access (directly threatened)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Legal translation challenging; some languages harder |
| **Impact** | 4 (Major) | Major goal unmet but programme continues |
| **Inherent Score** | **16 (High)** | L4 × I4 = 16 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-017.1 | Custom legal terminology glossary | Adequate | AI Architect | Research findings |
| C-017.2 | Human interpreter backup mandatory | Strong | CDiO | BC-2 |
| C-017.3 | Accuracy testing before deployment | Planned | AI Architect | Test plan |
| C-017.4 | Phased language rollout | Adequate | CDiO | Project plan |

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Testing and glossary help but some risk remains |
| **Impact** | 4 (Major) | Impact unchanged |
| **Residual Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Risk Response

**Response Strategy:** **TREAT** - Rigorous testing and phased rollout

**Success Criteria:** 85%+ accuracy achieved for all priority languages; legal terminology test passed

---

### COMPLIANCE Risks

---

### Risk R-010: UK GDPR Non-Compliance Enforcement

**Category:** COMPLIANCE
**Status:** In Progress
**Risk Owner:** Legal Services Director, SCTS (from RACI: Accountable for Compliance Certification)
**Action Owner:** Data Protection Officer

#### Risk Identification

**Risk Description:**
AI processing of personal data (including special category data) fails to meet UK GDPR requirements, resulting in ICO investigation, enforcement notice, or significant fine.

**Root Cause:**
- AI processing of special category data (Article 9)
- Large-scale automated processing
- Vulnerable data subjects
- Novel technology with unclear precedent

**Trigger Events:**
- Data subject complaint to ICO
- ICO proactive investigation of AI in public sector
- Data breach requiring notification
- DPIA conditions not implemented
- Inadequate response to subject access request

**Consequences if Realized:**
- ICO enforcement notice requiring processing changes
- Potential fine up to £17.5 million (or 4% turnover)
- Severe reputational damage
- Programme pause for remediation
- Personal liability for DPO/SIRO if negligent

**Affected Stakeholders:**
- **DPO** (SD-8): Personal accountability
- **Legal Services Director** (SD-7): Legal risk
- **ICO** (SD-13): Regulatory authority
- **Chief Executive**: Organisational accountability

**Related Objectives:**
- **Goal G-5**: Full compliance (directly threatened)
- **Outcome O-4**: Regulatory compliance and trust

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | AI + special category data + large scale = high risk |
| **Impact** | 4 (Major) | Fines and enforcement serious but survivable |
| **Inherent Score** | **16 (High)** | L4 × I4 = 16 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-010.1 | DPIA completed (ARC-001-DPIA) | Strong | DPO | DPIA document |
| C-010.2 | Lawful basis documented (Public Task + DPA Sch 1) | Strong | DPO | DPIA Section 4 |
| C-010.3 | Human-in-the-loop (Article 22 compliance) | Strong | CDiO | Architecture Principle 2 |
| C-010.4 | Data subject rights procedures | Adequate | DPO | ATRS record |
| C-010.5 | UK data residency only | Strong | CDiO | NFR-SEC-004 |
| C-010.6 | ATRS record published | Strong | CDiO | ATRS document |

**Overall Control Effectiveness:** Strong

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Strong controls but novel processing; ICO may still investigate |
| **Impact** | 5 (Catastrophic) | ICO enforcement would be severe |
| **Residual Score** | **15 (High)** | L3 × I5 = 15 |

#### Risk Response

**Response Strategy:** **TREAT** - Complete all DPIA conditions

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-010.1 | Complete bias audit for all languages | AI Architect | 2026-04-30 | 10 |
| A-010.2 | Update SCTS privacy notice with AI processing | DPO | 2026-03-31 | 10 |
| A-010.3 | Complete staff data protection training | DPO | 2026-04-30 | 10 |
| A-010.4 | Establish quarterly compliance monitoring | DPO | 2026-04-30 | 10 |

**Success Criteria:** All DPIA conditions implemented; zero ICO enforcement actions; proactive ICO engagement

#### Risk Appetite Assessment

| Attribute | Assessment |
|-----------|------------|
| **Risk Appetite Threshold (COMPLIANCE)** | Low (8) |
| **Current Residual Score** | 15 |
| **Assessment** | ⚠️ **Significantly Exceeds Appetite** |
| **Escalation Required** | YES - DPO escalation; potential ICO consultation |
| **Justification** | Compliance threshold is low; residual risk reduces significantly after DPIA conditions complete |

---

### Risk R-011: Accessibility non-compliance

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** CDiO, SCTS
**Action Owner:** AI Architect

#### Risk Identification

**Risk Description:**
AI user interfaces fail to meet WCAG 2.2 Level AA accessibility requirements, excluding users with disabilities and potentially breaching Equality Act 2010 obligations.

**Root Cause:**
- Accessibility often overlooked in AI interfaces
- Complex AI outputs hard to make accessible

**Consequences if Realized:**
- Users with disabilities excluded
- Equality Act non-compliance
- Reputational damage
- Potential legal challenge

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Accessibility often inadequate |
| **Impact** | 3 (Moderate) | Reputational and legal risk |
| **Inherent Score** | **9 (Medium)** | L3 × I3 = 9 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-011.1 | WCAG 2.2 AA requirement (NFR-U-001) | Strong | CDiO | Requirements |
| C-011.2 | Accessibility testing in CI/CD | Planned | AI Architect | NFR-U-001 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Testing will catch issues |
| **Impact** | 3 (Moderate) | Impact unchanged |
| **Residual Score** | **6 (Medium)** | L2 × I3 = 6 |

#### Risk Response

**Response Strategy:** **TREAT** - Implement accessibility testing

---

### Risk R-012: Equality Impact Assessment not completed

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** DPO, SCTS
**Action Owner:** CDiO

#### Risk Identification

**Risk Description:**
Equality Impact Assessment (EqIA) not completed before deployment, failing to identify potential discrimination and breaching Scottish public body duties.

**Root Cause:**
- EqIA not yet prioritised
- Focus on DPIA (mandatory) first

**Consequences if Realized:**
- Discrimination not identified until post-deployment
- Public sector equality duty breach
- Reputational damage
- Required remediation

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 (Likely) | Currently not started |
| **Impact** | 3 (Moderate) | Fixable but embarrassing |
| **Inherent Score** | **12 (Medium)** | L4 × I3 = 12 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Planned but not started |
| **Impact** | 3 (Moderate) | Impact unchanged |
| **Residual Score** | **9 (Medium)** | L3 × I3 = 9 |

#### Risk Response

**Response Strategy:** **TREAT** - Complete EqIA before production

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-012.1 | Complete Equality Impact Assessment | DPO | 2026-03-31 | 6 |

---

### FINANCIAL Risks

---

### Risk R-008: Cloud Costs Exceed Budget

**Category:** FINANCIAL
**Status:** In Progress
**Risk Owner:** Finance Director, SCTS (from RACI: Accountable for Budget Allocation)
**Action Owner:** CDiO

#### Risk Identification

**Risk Description:**
Azure AI services usage exceeds budgeted amounts due to higher than expected volumes, model training costs, or inadequate cost controls, creating budget pressure and questions about value for money.

**Root Cause:**
- Cloud costs can be unpredictable
- AI services charged per transaction
- Volume projections may be inaccurate

**Trigger Events:**
- Document volumes exceed projections
- Translation usage higher than expected
- Model retraining costs accumulate
- No cost monitoring in place
- Azure pricing changes

**Consequences if Realized:**
- Budget overrun requiring additional funding
- Questions about value for money
- Scope reduction to control costs
- Audit scrutiny of spending

**Affected Stakeholders:**
- **Finance Director** (SD-9): Budget accountability
- **CDiO** (SD-3): Delivery accountability
- **Scottish Government**: Spending controls

**Related Objectives:**
- **Outcome O-2**: Operational efficiency (ROI threatened)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Cloud costs commonly exceed estimates |
| **Impact** | 4 (Major) | Budget overrun creates significant issues |
| **Inherent Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-008.1 | 3-year TCO estimated (£485K base) | Adequate | Finance Director | Research findings |
| C-008.2 | Azure cost management tools | Planned | CDiO | To be configured |
| C-008.3 | Monthly cost review process | Planned | Finance Director | To be implemented |

**Overall Control Effectiveness:** Adequate (not yet implemented)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Monitoring will catch early |
| **Impact** | 4 (Major) | Impact unchanged |
| **Residual Score** | **8 (Medium)** | L2 × I4 = 8 |

#### Risk Response

**Response Strategy:** **TREAT** - Implement FinOps controls

**Success Criteria:** Costs within 10% of budget monthly; cost alerts configured

---

### Risk R-014: Procurement Challenge Delays Programme

**Category:** FINANCIAL
**Status:** Monitoring
**Risk Owner:** Finance Director, SCTS
**Action Owner:** Procurement

#### Risk Identification

**Risk Description:**
G-Cloud procurement process is challenged or delayed due to procedural issues, complaints from unsuccessful vendors, or legal challenge.

**Root Cause:**
- Public procurement subject to challenge
- Multiple vendors competing

**Consequences if Realized:**
- Programme delayed 3-6 months
- Legal costs to defend challenge
- Reputational damage

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | G-Cloud is established framework |
| **Impact** | 3 (Moderate) | Delay but not programme failure |
| **Inherent Score** | **6 (Medium)** | L2 × I3 = 6 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Unlikely with G-Cloud |
| **Impact** | 2 (Minor) | Azure already preferred |
| **Residual Score** | **4 (Low)** | L2 × I2 = 4 |

#### Risk Response

**Response Strategy:** **TOLERATE** - Follow G-Cloud procedures correctly

---

### Risk R-015: Investment case not approved

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** Finance Director, SCTS
**Action Owner:** CDiO

#### Risk Identification

**Risk Description:**
Business case for AI investment not approved by Scottish Government spending controls, delaying or blocking programme.

**Root Cause:**
- Spending controls apply
- AI investment requires justification

**Consequences if Realized:**
- Programme blocked or delayed
- Cannot proceed to production
- Momentum lost

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Spending controls active |
| **Impact** | 4 (Major) | Programme cannot proceed |
| **Inherent Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-015.1 | Clear benefits case (research findings) | Adequate | Finance Director | Research document |
| C-015.2 | Scottish Government engagement | Adequate | Chief Executive | Stakeholder plan |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Good preparation |
| **Impact** | 3 (Moderate) | Likely approved with conditions |
| **Residual Score** | **6 (Medium)** | L2 × I3 = 6 |

#### Risk Response

**Response Strategy:** **TREAT** - Prepare robust business case

---

### OPERATIONAL Risks

---

### Risk R-006: Key Personnel Departure

**Category:** OPERATIONAL
**Status:** In Progress
**Risk Owner:** CDiO, SCTS
**Action Owner:** HR Director

#### Risk Identification

**Risk Description:**
The CDiO or Senior AI Architect (when hired) leaves the organisation, creating a critical capability gap that delays the programme or compromises technical quality.

**Root Cause:**
- AI skills in high demand
- Key person dependency
- Public sector pay constraints

**Trigger Events:**
- CDiO recruited by another organisation
- AI Architect not hired or leaves quickly
- Key technical staff poached by private sector
- Retirement or personal reasons

**Consequences if Realized:**
- 3-6 month programme delay
- Knowledge loss
- Recruitment costs
- Quality risks from new staff learning curve

**Affected Stakeholders:**
- **CDiO** (SD-3): Personal driver (career opportunity)
- **AI Architect** (SD-4): Personal driver
- **Chief Executive**: Delivery accountability

**Related Objectives:**
- All goals dependent on capable delivery team

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | AI talent market competitive |
| **Impact** | 4 (Major) | Significant delay and disruption |
| **Inherent Score** | **12 (Medium)** | L3 × I4 = 12 |

#### Current Controls and Mitigations

| Control ID | Control Description | Effectiveness | Control Owner | Evidence |
|------------|---------------------|---------------|---------------|----------|
| C-006.1 | Documentation of decisions and architecture | Planned | CDiO | To be implemented |
| C-006.2 | Succession planning | Planned | HR Director | To be developed |
| C-006.3 | Knowledge sharing | Planned | CDiO | To be implemented |

**Overall Control Effectiveness:** Weak (not implemented)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Limited ability to prevent |
| **Impact** | 3 (Moderate) | Good documentation would help |
| **Residual Score** | **9 (Medium)** | L3 × I3 = 9 |

#### Risk Response

**Response Strategy:** **TRANSFER** - Contractor backup; **TREAT** - Knowledge management

**Additional Mitigations Required:**

| Action ID | Action | Owner | Target Date | Target Score |
|-----------|--------|-------|-------------|--------------|
| A-006.1 | Identify contractor backup options | Procurement | 2026-03-31 | 6 |
| A-006.2 | Implement architecture decision records | CDiO | 2026-03-31 | 6 |
| A-006.3 | Create succession plan for key roles | HR Director | 2026-04-30 | 6 |

---

### Risk R-016: AI service integration fails

**Category:** OPERATIONAL
**Status:** Monitoring
**Risk Owner:** CDiO, SCTS
**Action Owner:** AI Architect

#### Risk Identification

**Risk Description:**
Integration between Azure AI services and existing SCTS case management/document management systems proves more complex than expected, delaying deployment.

**Root Cause:**
- Legacy systems may have integration limitations
- API compatibility issues
- Data format mismatches

**Consequences if Realized:**
- Deployment delayed 2-3 months
- Additional integration development costs
- Workarounds compromise user experience

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 (Rare) | Azure APIs well-documented; PoC will validate |
| **Impact** | 3 (Moderate) | Delay but solvable |
| **Inherent Score** | **3 (Low)** | L1 × I3 = 3 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 (Rare) | PoC validates integration |
| **Impact** | 2 (Minor) | Early detection limits impact |
| **Residual Score** | **2 (Low)** | L1 × I2 = 2 |

#### Risk Response

**Response Strategy:** **TOLERATE** - PoC will validate integration

---

### Risk R-019: Training programme not ready

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** HR Director, SCTS
**Action Owner:** CDiO

#### Risk Identification

**Risk Description:**
Staff training programme not developed or delivered in time for rollout, resulting in poor adoption and operational issues.

**Root Cause:**
- Training development takes time
- Competing HR priorities
- Uncertain system functionality until late

**Consequences if Realized:**
- Staff unable to use system effectively
- Errors due to lack of training
- Adoption goals missed
- Support burden high

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Training often delayed |
| **Impact** | 3 (Moderate) | Affects adoption but recoverable |
| **Inherent Score** | **9 (Medium)** | L3 × I3 = 9 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | Clear requirement in BR-006 |
| **Impact** | 2 (Minor) | Early focus reduces impact |
| **Residual Score** | **4 (Low)** | L2 × I2 = 4 |

#### Risk Response

**Response Strategy:** **TREAT** - Start training development early

---

### Risk R-020: Interpreter services provider resistance

**Category:** OPERATIONAL
**Status:** Monitoring
**Risk Owner:** CDiO, SCTS
**Action Owner:** Procurement

#### Risk Identification

**Risk Description:**
External interpreter service providers resist AI translation deployment as threat to their business, potentially refusing to provide backup services or generating negative publicity.

**Root Cause:**
- AI translation reduces interpreter demand
- Business model threat

**Consequences if Realized:**
- Loss of human interpreter backup capability
- Negative campaign against AI translation
- Union involvement

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 (Possible) | Legitimate business concern |
| **Impact** | 2 (Minor) | Manageable with engagement |
| **Inherent Score** | **6 (Medium)** | L3 × I2 = 6 |

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 (Unlikely) | QA role positioning helps |
| **Impact** | 1 (Negligible) | Alternative interpreters available |
| **Residual Score** | **2 (Low)** | L2 × I1 = 2 |

#### Risk Response

**Response Strategy:** **TREAT** - Position interpreters as quality assurance (per stakeholder resolution strategy)

---

## D. Risk by Category Analysis

### STRATEGIC Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 4 | 16.0 | 10.3 | 36% reduction | Judicial confidence and government alignment critical |

**Key Findings:**
- Judicial confidence (R-001) is highest strategic risk - requires constant attention
- Government policy (R-003) is external factor with limited control
- Benefits demonstration (R-018) needs measurement framework

### OPERATIONAL Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 4 | 12.0 | 7.5 | 38% reduction | Staff adoption and capability are critical success factors |

**Key Findings:**
- Staff resistance (R-002) could undermine entire programme
- Key personnel risk (R-006) needs succession planning
- Training (R-019) must start early

### FINANCIAL Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 3 | 13.0 | 8.0 | 38% reduction | Cost control and business case approval manageable |

**Key Findings:**
- Cloud costs (R-008) need FinOps controls
- Procurement risk (R-014) low with G-Cloud
- Business case (R-015) needs clear benefits

### COMPLIANCE Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 3 | 14.7 | 9.0 | 39% reduction | GDPR compliance critical; EqIA needs completion |

**Key Findings:**
- UK GDPR (R-010) highest compliance risk - DPIA helps but novel processing
- EqIA (R-012) not started - needs prioritisation
- Accessibility (R-011) has clear requirements

### REPUTATIONAL Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 3 | 15.3 | 9.3 | 39% reduction | AI quality and transparency critical for reputation |

**Key Findings:**
- AI quality (R-004) is top overall risk - quality controls essential
- Parliamentary scrutiny (R-005) addressed through ATRS transparency
- Negative comparisons (R-013) manageable through differentiation

### TECHNOLOGY Risks Summary

| Count | Avg Inherent | Avg Residual | Control Effectiveness | Key Theme |
|-------|--------------|--------------|----------------------|-----------|
| 3 | 13.3 | 8.3 | 38% reduction | Security and reliability require testing before production |

**Key Findings:**
- Security breach (R-007) critical - pen testing must complete
- Service outage (R-009) well-mitigated by fallback design
- Translation accuracy (R-017) needs thorough testing

---

## E. Risk Ownership Matrix

| Stakeholder | Owned Risks | Critical/High Risks | Notes |
|-------------|-------------|---------------------|-------|
| **Chief Executive** | R-001, R-003, R-004, R-005, R-013, R-018 | 2 High | Heavy concentration of strategic/reputational risks - appropriate at executive level |
| **CDiO** | R-002, R-006, R-007, R-009, R-011, R-016, R-017, R-019 | 2 High | Technology and operational delivery risks - appropriate for programme owner |
| **Legal Services Director** | R-010 | 1 High | Compliance risk - appropriate for legal accountability |
| **Finance Director** | R-008, R-014, R-015 | 0 | Financial risks manageable |
| **DPO** | R-012 | 0 | EqIA completion |
| **HR Director** | (Action owner only) | 0 | Training and change management actions |

---

## F. 4Ts Response Summary

| Response | Count | % | Key Examples | Commentary |
|----------|-------|---|--------------|------------|
| **Tolerate** | 3 risks | 15% | R-013, R-014, R-016 | Low residual risks within appetite |
| **Treat** | 16 risks | 80% | R-001, R-002, R-004, R-007, R-010 | Most risks require active mitigation |
| **Transfer** | 1 risk | 5% | R-006 (contractor backup) | Key personnel risk partially transferred |
| **Terminate** | 0 risks | 0% | None | No risks require activity termination |

---

## G. Risk Appetite Assessment

| Category | Appetite Threshold | Risks Within | Risks Exceeding | Action Required |
|----------|-------------------|--------------|-----------------|-----------------|
| **STRATEGIC** | Medium (12) | 2 | 2 (R-001: 15, R-018: 9) | R-001 requires Chief Executive approval |
| **OPERATIONAL** | Medium (12) | 4 | 0 | Within appetite |
| **FINANCIAL** | Medium (12) | 3 | 0 | Within appetite |
| **COMPLIANCE** | Low (8) | 1 | 2 (R-010: 15, R-012: 9) | R-010 requires DPO escalation |
| **REPUTATIONAL** | Medium (12) | 1 | 2 (R-004: 16, R-005: 10) | R-004 requires Steering Committee approval |
| **TECHNOLOGY** | Medium (12) | 2 | 1 (R-007: 15) | R-007 requires SIRO approval |

**Total Risks Exceeding Appetite:** 4 (R-001, R-004, R-007, R-010)

---

## H. Action Plan (Priority Order)

| Priority | Action | Risk(s) | Owner | Due Date | Status |
|----------|--------|---------|-------|----------|--------|
| **1** | Complete penetration testing before production | R-007 | Security Team | 2026-04-30 | Not Started |
| **2** | Implement Azure Sentinel SIEM | R-007 | ICT Operations | 2026-04-30 | Not Started |
| **3** | Complete bias audit for all 10 languages | R-004, R-010 | AI Architect | 2026-04-30 | Not Started |
| **4** | Establish Judicial Advisory Group | R-001 | Chief Executive | 2026-02-28 | Not Started |
| **5** | Document security incident response plan | R-007 | Security Team | 2026-03-31 | Not Started |
| **6** | Issue Chief Executive job security message | R-002 | Chief Executive | 2026-02-15 | Not Started |
| **7** | Complete Equality Impact Assessment | R-012 | DPO | 2026-03-31 | Not Started |
| **8** | Create media response plan for AI incidents | R-004 | Communications | 2026-03-15 | Not Started |
| **9** | Update SCTS privacy notice | R-010 | DPO | 2026-03-31 | Not Started |
| **10** | Identify contractor backup options | R-006 | Procurement | 2026-03-31 | Not Started |

---

## I. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Review Authority |
|------------|------------------|------------------|
| **Critical** (20-25) | Weekly | CDiO + Chief Executive |
| **High** (13-19) | Fortnightly | CDiO |
| **Medium** (6-12) | Monthly | Programme Manager |
| **Low** (1-5) | Quarterly | Programme Manager |

### Escalation Criteria

Escalate to next level when:
- Any risk increases by 5+ points
- Any new Critical risk identified
- Risk exceeds organisational appetite
- Mitigation deadline missed
- Risk materialises (trigger event occurs)

### Reporting Requirements

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Risk Dashboard | Weekly | CDiO | Top 5 risks, movement, actions |
| Risk Report | Monthly | Steering Committee | Full register, trends, escalations |
| Risk Summary | Quarterly | Chief Executive, SIRO | Appetite compliance, strategic risks |
| Annual Risk Review | Annually | SCTS Board | Programme risk profile, lessons learned |

### Key Risk Indicators (KRIs)

| KRI | Threshold | Measurement | Frequency |
|-----|-----------|-------------|-----------|
| Total residual risk score | <200 | Sum of residual scores | Monthly |
| Critical/High risks count | <5 | Count of scores 13+ | Weekly |
| Risks exceeding appetite | <3 | Count exceeding threshold | Monthly |
| Overdue actions | 0 | Count of missed deadlines | Weekly |
| Risks increasing | 0 | Count moving up a band | Monthly |

**Next Review Date:** 2026-02-17

**Risk Register Owner:** Chief Executive, SCTS

---

## J. Integration with SOBC

This risk register supports Strategic Outline Business Case (SOBC) preparation:

| SOBC Section | Risk Register Input |
|--------------|---------------------|
| **Strategic Case** | R-001, R-003 inform urgency and strategic context |
| **Economic Case** | R-008, R-014, R-015 inform financial assumptions; risk-adjusted costs |
| **Commercial Case** | R-014 (procurement), R-006 (supplier dependency) inform commercial strategy |
| **Financial Case** | R-008, R-015 inform budget and contingency requirements |
| **Management Case Part E** | Full risk register feeds into SOBC risk management section |

**Optimism Bias Adjustment:** Based on risk profile (4 High residual risks), recommend 10-15% optimism bias adjustment for cost estimates.

---

## K. Orange Book Compliance Checklist

| Orange Book Principle | Evidence | Status |
|-----------------------|----------|--------|
| ✅ **Governance and Leadership** | Risk owners assigned from senior stakeholders (Chief Executive, CDiO, Legal Services Director) | Compliant |
| ✅ **Integration** | Risks linked to stakeholder goals, objectives, and SOBC | Compliant |
| ✅ **Collaboration** | Risks sourced from stakeholder analysis, DPIA, Secure by Design assessment | Compliant |
| ✅ **Risk Processes** | Systematic identification, assessment (5×5 matrix), 4Ts response, monitoring | Compliant |
| ✅ **Continual Improvement** | Review framework, KRIs, action plan for ongoing management | Compliant |

---

## Approval and Sign-Off

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Risk Register Owner | Chief Executive, SCTS | | |
| Programme Owner | Chief Digital Information Officer, SCTS | | |
| Senior Information Risk Owner (SIRO) | [To be confirmed] | | |
| Data Protection Officer | DPO, SCTS | | |

---

## Appendix: Risk Assessment Scales

### Likelihood Scale

| Rating | Descriptor | Probability | Description |
|--------|------------|-------------|-------------|
| 1 | Rare | <5% | Highly unlikely to occur |
| 2 | Unlikely | 5-25% | Could happen but probably won't |
| 3 | Possible | 25-50% | Reasonable chance |
| 4 | Likely | 50-75% | More likely than not |
| 5 | Almost Certain | >75% | Expected to occur |

### Impact Scale

| Rating | Descriptor | Financial | Schedule | Reputation | Compliance |
|--------|------------|-----------|----------|------------|------------|
| 1 | Negligible | <£25K | <1 week | Internal only | Minor finding |
| 2 | Minor | £25-100K | 1-4 weeks | Local media | Audit recommendation |
| 3 | Moderate | £100-500K | 1-3 months | National mention | Regulatory enquiry |
| 4 | Major | £500K-2M | 3-6 months | National headline | Enforcement action |
| 5 | Catastrophic | >£2M | >6 months | Political crisis | Criminal/licence |

### Risk Score Matrix

|  | Impact 1 | Impact 2 | Impact 3 | Impact 4 | Impact 5 |
|--|----------|----------|----------|----------|----------|
| **Likelihood 5** | 5 | 10 | 15 | 20 | 25 |
| **Likelihood 4** | 4 | 8 | 12 | 16 | 20 |
| **Likelihood 3** | 3 | 6 | 9 | 12 | 15 |
| **Likelihood 2** | 2 | 4 | 6 | 8 | 10 |
| **Likelihood 1** | 1 | 2 | 3 | 4 | 5 |

**Risk Zones:**
- 🟩 **Low (1-5)**: Routine monitoring
- 🟨 **Medium (6-12)**: Management attention
- 🟧 **High (13-19)**: Senior management attention
- 🟥 **Critical (20-25)**: Immediate escalation

---

**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: 2026-01-26 GMT
**ArcKit Version**: 0.11.2
**Project**: SCTS GenAI Programme (Project 001)
**AI Model**: Claude Opus 4.5
**Framework**: HM Treasury Orange Book (2023)
**Source Artifacts**: Stakeholder Drivers (v1.1), DPIA, Secure by Design Assessment, Requirements (v1.2), Architecture Principles (v1.1)
