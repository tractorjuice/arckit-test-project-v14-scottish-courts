# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is **arckit-test-project-v14-scottish-courts** - a test repository demonstrating ArcKit governance artifacts for the Scottish Courts and Tribunals Service (SCTS) GenAI Programme.

**This is NOT the main arc-kit CLI repository** - it's a generated project containing architecture documentation artifacts. The CLI source code lives at [github.com/tractorjuice/arc-kit](https://github.com/tractorjuice/arc-kit).

## Project Status

| Field | Value |
|-------|-------|
| **Project ID** | 001-scts-genai-programme |
| **Phase** | Alpha Complete |
| **Governance Score** | 82/100 (Grade B) |
| **Artifacts** | 25+ documents |

## Repository Structure

```
.arckit/
├── memory/                    # Global context
│   └── architecture-principles.md   # 20 architecture principles
├── templates/                 # 40+ document templates
└── scripts/bash/              # Project management scripts

.claude/commands/              # 40 slash commands (arckit.*.md)
.gemini/commands/              # Gemini equivalents (TOML)
.codex/prompts/                # Codex prompts

projects/001-scts-genai-programme/   # Generated artifacts
├── stakeholder-drivers.md           # 13 stakeholders, 6 goals
├── requirements.md                  # 49 requirements
├── risk-register.md                 # 20 risks (Orange Book)
├── data-model.md                    # 9 entities, GDPR compliant
├── high-level-design.md             # C4 architecture
├── dpia.md                          # Data Protection Impact Assessment
├── tcop-review.md                   # Technology Code of Practice
├── secure-by-design-assessment.md   # NCSC CAF
├── ai-playbook-assessment.md        # UK AI Playbook (79%)
├── backlog.md                       # 184 user stories
├── decisions/ADR-*.md               # Architecture decisions
├── wardley-maps/                    # Strategic maps
└── PROJECT-STORY.md                 # Complete narrative

docs/                          # GitHub Pages site
├── index.html
└── manifest.json

source-documents/              # Input reference documents
```

## Common Commands

**Project Management:**
```bash
./.arckit/scripts/bash/create-project.sh --name "Project Name"  # Create new project
./.arckit/scripts/bash/list-projects.sh                         # List projects
```

**Generate Artifacts (slash commands in Claude Code):**
```
/arckit.principles      # Architecture principles (do first)
/arckit.stakeholders    # Stakeholder analysis
/arckit.requirements    # Business/technical requirements
/arckit.risk            # Risk register (Orange Book)
/arckit.sobc            # Strategic Outline Business Case
/arckit.data-model      # Data model with ERD
/arckit.research        # Technology research
/arckit.wardley         # Wardley maps
/arckit.diagram         # Architecture diagrams (Mermaid)
/arckit.backlog         # Sprint backlog from requirements
/arckit.traceability    # Requirements traceability matrix
/arckit.analyze         # Governance quality analysis
/arckit.pages           # Generate GitHub Pages site
```

**UK Government Compliance:**
```
/arckit.tcop            # Technology Code of Practice (13 points)
/arckit.secure          # Secure by Design (NCSC CAF)
/arckit.dpia            # Data Protection Impact Assessment
/arckit.ai-playbook     # AI Playbook compliance
/arckit.atrs            # Algorithmic Transparency Record
/arckit.service-assessment  # GDS Service Standard (14 points)
```

## Slash Command Pattern

Commands read templates from `.arckit/templates/` and generate artifacts in `projects/NNN-*/`:

```yaml
---
description: Brief description
---

## User Input
$ARGUMENTS

## Instructions
1. Check prerequisites (principles exist)
2. Create/find project via create-project.sh --json
3. Read template from .arckit/templates/{type}-template.md
4. Generate artifact using template structure
5. Use Write tool to save (avoids 32K token limit)
6. Show summary only
```

## Key Patterns

**Token Limit Handling**: For large documents, use Write tool directly:
```
/arckit.requirements but write directly to file, show me only a summary
```

**Template-Driven**: All artifacts follow templates in `.arckit/templates/`

**Traceability Chain**: Stakeholders → Goals → Requirements (BR/FR/NFR/INT/DR) → Data Model → Components → User Stories

**Requirement ID Prefixes**:
- BR-xxx: Business Requirements
- FR-xxx: Functional Requirements
- NFR-xxx: Non-Functional (NFR-P-xxx Performance, NFR-SEC-xxx Security)
- INT-xxx: Integration Requirements
- DR-xxx: Data Requirements

**Wardley Map Format**: OnlineWardleyMaps syntax for https://create.wardleymaps.ai

## Project Context: SCTS GenAI Programme

The Scottish Courts and Tribunals Service GenAI Programme introduces:
- **Document Intelligence** - AI-powered classification and entity extraction
- **Speech Services** - Real-time transcription with speaker diarisation
- **Translation Services** - 10 priority languages
- **Cognitive Search** - Semantic search across court documents

**Design Principles**:
- Human-in-the-loop for all consequential decisions
- AI augments but never replaces judicial decision-making
- UK data residency (Azure UK South/West)
- Zero modifications to court records by AI

**Technology**: Microsoft Azure AI Services via G-Cloud

## Critical Actions Before Production

1. DPIA Approval from DPO/SIRO
2. Bias Audit for 10 translation languages
3. Penetration Testing
4. Equality Impact Assessment (EqIA)
5. SIEM Implementation
