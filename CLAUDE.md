# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **ArcKit architecture governance framework** for the Scottish Courts and Tribunals Service (SCTS) GenAI strategy. It is not a traditional software project - it's a documentation and artifact generation system that uses AI assistants (Claude, Gemini, Copilot) to produce UK government-compliant architecture deliverables.

## Key Concepts

- **This is not a codebase to modify** - it's a framework for generating architecture artifacts
- All user-generated content goes to `projects/NNN-*/` directories
- Use `/arckit.*` slash commands to generate artifacts (e.g., `/arckit.stakeholders`, `/arckit.requirements`)
- Templates in `.arckit/templates/` define artifact structure
- Commands in `.claude/commands/` contain the prompts that drive artifact generation

## Commands

**Project Management:**
```bash
./.arckit/scripts/bash/create-project.sh --name "Project Name"  # Create new project
./.arckit/scripts/bash/list-projects.sh                         # List all projects
./.arckit/scripts/bash/check-prerequisites.sh                   # Validate environment
```

**Architecture Artifacts (via slash commands):**
- `/arckit.principles` - Define architecture principles (prerequisite for projects)
- `/arckit.stakeholders` - Analyze stakeholder drivers and goals
- `/arckit.requirements` - Generate business and technical requirements
- `/arckit.research` - Research technology options with build vs buy analysis
- `/arckit.wardley` - Create Wardley maps for strategic decisions
- `/arckit.sobc` - Create Strategic Outline Business Case (Green Book 5-case model)
- `/arckit.evaluate` - Create vendor evaluation framework
- `/arckit.sow` - Generate Statement of Work for procurement

**Compliance & Governance:**
- `/arckit.tcop` - Technology Code of Practice assessment
- `/arckit.secure` - UK Government Secure by Design review
- `/arckit.ai-playbook` - AI Playbook compliance assessment
- `/arckit.dpia` - Data Protection Impact Assessment (GDPR Article 35)

## Architecture

```
.arckit/
├── scripts/bash/     # Project management utilities
├── templates/        # 40+ artifact templates (markdown)
└── memory/           # Organizational context and principles

.claude/commands/     # Claude command prompts
.gemini/commands/     # Gemini command definitions (TOML)
.codex/prompts/       # GitHub Copilot prompts

projects/             # Generated project artifacts
└── NNN-project-slug/
    ├── README.md
    ├── stakeholder-analysis.md
    ├── requirements.md
    ├── vendors/
    └── ...

source-documents/     # Reference documentation
```

## Typical Workflow

1. Run `/arckit.principles` to establish architecture principles (stored in `.arckit/memory/`)
2. Create project: `./.arckit/scripts/bash/create-project.sh --name "My Project"`
3. Follow the workflow phases in the generated project README:
   - **Discovery**: stakeholders → risk → business case
   - **Alpha**: requirements → data model → research → procurement
   - **Beta**: HLD review → DLD review → traceability
   - **Compliance**: secure by design, TCoP, AI playbook as needed

## UK Government Standards

This framework implements compliance with:
- Green Book 5-case business case model
- Technology Code of Practice (TCoP)
- Secure by Design principles
- GDPR/UK GDPR (DPIA)
- AI Playbook for responsible AI deployment
- MOD-specific: JSP 936 AI assurance, CAAT continuous assurance
