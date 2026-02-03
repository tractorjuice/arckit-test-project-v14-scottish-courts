# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is an ArcKit-managed enterprise architecture governance project for the **Scottish Courts and Tribunals Service (SCTS) GenAI Programme**.

**This is NOT the main arc-kit CLI repository** — it's a generated project containing architecture documentation artifacts. The CLI source code lives at [github.com/tractorjuice/arc-kit](https://github.com/tractorjuice/arc-kit).

| Field | Value |
|-------|-------|
| **Project ID** | 001-scts-genai-programme |
| **Phase** | Alpha Complete |
| **Governance Score** | 82/100 (Grade B) |
| **Artifacts** | 25+ documents |
| **ArcKit Version** | 1.1.0 (43 commands) |

## How This Repository Works

All work is driven by **slash commands** (`/arckit.*`) that read templates from `.arckit/templates/` and generate markdown artifacts into `projects/001-scts-genai-programme/`. There is no build system, test suite, or application code — this repository is pure architecture documentation.

### Generating Artifacts

Run slash commands in Claude Code. Each command:
1. Checks prerequisites (e.g., principles must exist before requirements)
2. Creates/finds the project via `.arckit/scripts/bash/create-project.sh --json`
3. Reads the template from `.arckit/templates/{type}-template.md`
4. Generates the artifact following template structure
5. Writes output using the Write tool (avoids 32K token limit)
6. Shows a summary only

For large documents, append: `but write directly to file, show me only a summary`

### Command Execution Order

Commands have mandatory (M), recommended (R), and optional (O) dependencies. See `DEPENDENCY-MATRIX.md` for the full DSM and `WORKFLOW-DIAGRAMS.md` for visual paths.

**Recommended order for this UK Government AI project:**
```
plan → principles → stakeholders → risk → sobc → requirements → datascout →
data-model → research → wardley → gcloud-search → evaluate → hld-review →
dld-review → backlog → servicenow → devops → mlops → operationalize →
traceability → tcop → ai-playbook → atrs → secure → principles-compliance →
analyze → service-assessment → story → pages
```

**The three most-consumed artifacts:**
- `requirements.md` — consumed by 37 commands (mandatory for most)
- `architecture-principles.md` — consumed by 20 commands
- `stakeholder-drivers.md` — consumed by 21 commands

### Delegated Agents

Four research commands use delegated agents in `.claude/agents/`:
- `arckit-research.md` — general technology research
- `arckit-azure-research.md` — Azure research via Microsoft Learn MCP
- `arckit-aws-research.md` — AWS research via AWS Knowledge MCP
- `arckit-datascout.md` — external data source discovery

### Scripts

```bash
.arckit/scripts/bash/create-project.sh --name "Name"    # Create new project (returns JSON)
.arckit/scripts/bash/list-projects.sh                    # List all projects
.arckit/scripts/bash/generate-document-id.sh             # Generate ARC-{PID}-{TYPE}-v*.md IDs
.arckit/scripts/bash/check-prerequisites.sh              # Check command prerequisites
.arckit/scripts/bash/migrate-filenames.sh                # Migrate to new naming convention
```

## Key Patterns

**Document ID convention**: `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md`
- Multi-instance types (ADR, DIAG, WARD, DMC): `ARC-{PID}-{TYPE}-{NUM}-v{VERSION}.md`
- Architecture principles use project ID 000: `ARC-000-PRIN-v1.0.md`

**Traceability chain**: Stakeholders → Goals → Requirements (BR/FR/NFR/INT/DR) → Data Model → Components → User Stories

**Requirement ID prefixes**:
- BR-xxx: Business, FR-xxx: Functional, NFR-xxx: Non-Functional (NFR-P-xxx Performance, NFR-SEC-xxx Security), INT-xxx: Integration, DR-xxx: Data

**Wardley Map format**: OnlineWardleyMaps syntax for https://create.wardleymaps.ai

**Multi-AI support**: Commands exist for Claude (`.claude/commands/`), Gemini (`.gemini/commands/`), and Codex (`.codex/prompts/`)

## Project Context: SCTS GenAI Programme

The Scottish Courts and Tribunals Service GenAI Programme introduces:
- **Document Intelligence** — AI-powered classification and entity extraction
- **Speech Services** — Real-time transcription with speaker diarisation
- **Translation Services** — 10 priority languages
- **Cognitive Search** — Semantic search across court documents

**Design constraints**:
- Human-in-the-loop for all consequential decisions
- AI augments but never replaces judicial decision-making
- UK data residency (Azure UK South/West)
- Zero modifications to court records by AI
- Technology: Microsoft Azure AI Services via G-Cloud

## Critical Actions Before Production

1. DPIA Approval from DPO/SIRO
2. Bias Audit for 10 translation languages
3. Penetration Testing
4. Equality Impact Assessment (EqIA)
5. SIEM Implementation
