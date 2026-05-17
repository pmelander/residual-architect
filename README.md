# Solution Architect Toolkit for Claude Code

A comprehensive collection of skills and agents designed to enhance Solution Architect capabilities when using Claude Code.

## 🚀 Quick Links

- **[Getting Started Guide](GETTING_STARTED.md)** - Get up and running in 5 minutes
- **[Quick Reference](QUICKREF.md)** - All commands and workflows at a glance
- **[Installation Guide](docs/INSTALLATION.md)** - Detailed installation instructions
- **[Usage Guide](docs/USAGE.md)** - Comprehensive examples and best practices
- **[Roadmap](ROADMAP.md)** - Future development plans

## Overview

This toolkit provides specialized skills for architecture design, documentation, analysis, and implementation guidance. Built as Claude Code skills, these tools integrate seamlessly into your architecture workflow.

## Phases

### Phase 1: Immediate Impact (Complete) ✅
- ✅ `arch-decision-record` - Document architectural decisions
- ✅ `solution-doc-generator` - Generate comprehensive documentation
- ✅ `tech-stack-advisor` - Technology selection support
- ✅ `design-review` - Validate architecture choices
- ✅ `stressor-analysis` - Stress-test architecture for antifragility

### Phase 2: Deep Analysis (Planned)
- `learning-analyzer` - Build organizational learning capability
- `capability-assessor` - Assess and grow team maturity
- `pattern-extractor` - Institutionalize architectural knowledge
- `evolutionary-coach` - Enable continuous architecture evolution

### Phase 3: Specialized (Planned)
- `cloud-architect` - Infrastructure as code generation
- `compliance-checker` - Regulatory compliance validation
- `capacity-planner` - Resource and scaling planning
- `risk-assessor` - Risk management and mitigation

## ⚡ Quick Install

```bash
git clone <repo-url> solution-architect-toolkit
cd solution-architect-toolkit
cp skills/phase-1/*.md ~/.claude/skills/
```

**That's it!** Open Claude Code and type `/` to see your new skills.

📖 See [Installation Guide](docs/INSTALLATION.md) for detailed instructions and troubleshooting.

## 📖 Usage

### Available Commands

| Skill | Command | Description |
|-------|---------|-------------|
| 📋 ADR | `/adr create <title>` | Create Architecture Decision Records |
| 📄 Docs | `/solution-doc hld` | Generate comprehensive documentation |
| 🔧 Tech | `/tech-stack recommend` | Get technology recommendations |
| ✅ Review | `/design-review complete` | Comprehensive architecture review |

### Quick Example

```
You: /adr create Use PostgreSQL for database

Claude asks questions and generates:
docs/adr/ADR-001-use-postgresql-for-database.md

Complete with context, decision rationale, trade-offs, and alternatives!
```

📖 See [Usage Guide](docs/USAGE.md) for detailed examples and best practices.

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

## 🤝 Contributing

We welcome contributions! Whether it's:
- 🆕 New skills for Phase 2 or 3
- 🐛 Bug fixes
- 📝 Documentation improvements
- 💡 Feature suggestions

See [Contributing Guide](CONTRIBUTING.md) for details.

## 📚 Documentation

- **[Getting Started](GETTING_STARTED.md)** - New user guide (start here!)
- **[Quick Reference](QUICKREF.md)** - Command cheatsheet
- **[Usage Guide](docs/USAGE.md)** - Comprehensive examples
- **[Installation](docs/INSTALLATION.md)** - Setup instructions
- **[Roadmap](ROADMAP.md)** - Future plans
- **[Project Summary](PROJECT_SUMMARY.md)** - Complete overview
- **[Contributing](CONTRIBUTING.md)** - How to contribute
- **[Claude.md](CLAUDE.md)** - Development guide

## 📊 Project Status

| Phase | Status | Skills | Timeline |
|-------|--------|--------|----------|
| Phase 1 | ✅ Complete | 4 skills | Q2 2026 |
| Phase 2 | 📋 Planned | 4 skills | Q3-Q4 2026 |
| Phase 3 | 💡 Planned | 4 skills | Q1-Q2 2027 |

**Current Release:** Phase 1 - Released 2026-05-17

## ⭐ Star This Repository

If you find this toolkit useful, please star it! It helps others discover it.

## 📞 Support

- 📖 Check the [documentation](docs/)
- 💬 Start a [discussion](../../discussions)
- 🐛 Report [issues](../../issues)
- 💡 Request [features](../../issues/new)

## 📄 License

MIT License - See [LICENSE](LICENSE) for details.

---

**Built with ❤️ for Solution Architects using Claude Code**
