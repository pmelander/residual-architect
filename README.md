# Solution Architect Toolkit for Claude Code

A comprehensive collection of skills and agents designed to enhance Solution Architect capabilities when using Claude Code.

## Overview

This toolkit provides specialized skills for architecture design, documentation, analysis, and implementation guidance. Built as Claude Code skills, these tools integrate seamlessly into your architecture workflow.

## Phases

### Phase 1: Immediate Impact (In Progress)
- ✅ `arch-decision-record` - Document architectural decisions
- 🔄 `solution-doc-generator` - Generate comprehensive documentation
- 🔄 `tech-stack-advisor` - Technology selection support
- 🔄 `design-review` - Validate architecture choices

### Phase 2: Deep Analysis (Planned)
- `tech-debt-analyzer` - Analyze technical debt
- `system-mapper` - Visualize system dependencies
- `migration-planner` - Plan legacy modernization
- `api-designer` - Design and validate APIs

### Phase 3: Specialized (Planned)
- `cloud-architect` - Infrastructure as code generation
- `compliance-checker` - Regulatory compliance validation
- `capacity-planner` - Resource and scaling planning
- `risk-assessor` - Risk management and mitigation

## Installation

1. Clone this repository to your Claude Code skills directory:
   ```bash
   cd ~/.claude/skills
   git clone <repo-url> solution-architect-toolkit
   ```

2. Skills will be automatically available in Claude Code

## Usage

Each skill can be invoked using the `/` command in Claude Code:
- `/adr` - Architecture Decision Records
- `/solution-doc` - Solution Documentation
- `/tech-stack` - Technology Stack Advisor
- `/design-review` - Design Review

See individual skill documentation for detailed usage.

## Project Structure

```
.
├── skills/           # Claude Code skills
│   ├── phase-1/     # Immediate impact tools
│   ├── phase-2/     # Deep analysis tools
│   └── phase-3/     # Specialized tools
├── templates/        # Document templates
├── examples/         # Example outputs
└── docs/            # Documentation
```

## Contributing

This toolkit is designed to evolve with Solution Architect needs. Contributions welcome!

## License

MIT
