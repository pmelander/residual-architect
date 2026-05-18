# Solution Architect Toolkit for Claude Code

A collection of Claude Code skills built on **Residuality Theory** — designed to build antifragile systems thinking and Solution Architect capabilities that compound over time.

> **Philosophy:** Skills are designed to transfer capability to architects, not create dependency on tools. The measure of success is how little you need them.

## 🚀 Quick Links

- **[Introduction to Residuality Theory](RESIDUALITY.md)** - The philosophy behind this toolkit — start here if you're new to the framework
- **[Getting Started Guide](GETTING_STARTED.md)** - Get up and running in 5 minutes
- **[Quick Reference](QUICKREF.md)** - All commands at a glance
- **[Roadmap](ROADMAP.md)** - What's built and what's next
- **[Contributing](CONTRIBUTING.md)** - How to add skills and compliance packs

---

## Skills

### Phase 1: Individual Capabilities ✅

Build the core thinking skills of a Solution Architect.

| Skill | Command | What it builds |
|-------|---------|---------------|
| Architecture Decision Records | `/adr` | Structured decision-making and trade-off thinking |
| Solution Documentation | `/solution-doc` | Systems thinking and communication capability |
| Technology Stack Advisor | `/tech-stack` | Objective technology evaluation without hype |
| Design Review | `/design-review` | Self-assessment and pattern recognition |
| Stressor Analysis | `/stressor` | Antifragility thinking and resilience design |

### Utilities ✅

| Skill | Command | What it does |
|-------|---------|-------------|
| Excel Reader | `/excel` | Import Excel/CSV stressor matrices and data into markdown workflows |

### Phase 2: Organisational Capabilities ✅

Build team and organisational meta-capabilities that compound over time.

| Skill | Command | What it builds |
|-------|---------|---------------|
| Architecture Learning Analyzer | `/arch-learning` | Systematic learning from past decisions |
| Team Capability Assessor | `/capability-assessor` | Team architectural maturity and growth |
| Pattern Extractor | `/patterns` | Institutional knowledge and pattern libraries |
| Evolutionary Coach | `/evolve` | Continuous architecture improvement mindset |

### Phase 3: Specialised Tools ✅

Domain-specific capabilities for cloud, capacity, and compliance.

| Skill | Command | What it builds |
|-------|---------|---------------|
| Cloud Architect | `/cloud` | Cloud-native thinking, IaC discipline, Well-Architected mindset |
| Capacity Planner | `/capacity` | Demand modelling, scaling intuition, bottleneck identification |

> **Note on Risk and Compliance:** A standalone Risk Assessor and Compliance Checker were considered and deliberately excluded. Residuality Theory covers risk through antifragility thinking (`/stressor`) — risk registers create false confidence in enumerated threats. Compliance is handled through **stressor compliance packs** (`/stressor compliance <pack>`), so regulatory requirements emerge as residues of antifragile design rather than a separate checklist process. See [ADR-006](docs/adr/ADR-006-exclude-risk-assessor-skill.md) and [ADR-007](docs/adr/ADR-007-compliance-via-stressor-packs.md).

---

## ⚡ Install

```bash
git clone <repo-url> solution-architect-toolkit
cd solution-architect-toolkit

# Install all skills
cp skills/phase-1/*.md ~/.claude/skills/
cp skills/phase-2/*.md ~/.claude/skills/
cp skills/phase-3/*.md ~/.claude/skills/
cp skills/utilities/*.md ~/.claude/skills/

# Python dependency for Excel reading
pip install -r requirements.txt
```

Open Claude Code and type `/` to see your skills.

📖 See [Installation Guide](docs/INSTALLATION.md) for detailed setup and troubleshooting.

---

## 📖 Command Reference

### Architecture Decisions
```bash
/adr create <title>          # Create a new ADR
/adr list                    # List all ADRs
/adr update <number>         # Update an existing ADR
/adr search <term>           # Search ADRs
```

### Documentation
```bash
/solution-doc hld            # High-Level Design
/solution-doc lld            # Low-Level Design
/solution-doc deployment     # Deployment Guide
/solution-doc runbook        # Operations Runbook
/solution-doc complete       # All documentation
```

### Technology Evaluation
```bash
/tech-stack recommend        # Recommend a tech stack
/tech-stack evaluate <tech>  # Evaluate a specific technology
/tech-stack compare <a> vs <b>  # Compare two technologies
/tech-stack migrate from <old> to <new>  # Migration analysis
```

### Design Review
```bash
/design-review architecture  # Review system architecture
/design-review api           # Review API design
/design-review security      # Security-focused review
/design-review performance   # Performance-focused review
/design-review complete      # Comprehensive review
```

### Stressor Analysis
```bash
/stressor walk [path-name]          # Walk a path, evaluating each actor as intentions propagate
/stressor generate [count]          # Generate creative stressors (including absurd ones)
/stressor analyze                   # Build impact matrix (actors × stressors)
/stressor vulnerabilities           # Identify most-impacted actors
/stressor residues                  # Suggest residuals (new actors, intentions, or paths)
/stressor iterate                   # Re-walk after adding residuals
/stressor workshop                  # Facilitate team workshop
/stressor import <file> [sheet]     # Import stressor matrix from Excel/CSV
/stressor compliance <pack>         # Inject compliance stressor pack
```

### Cloud Architecture
```bash
/cloud design <architecture>        # Design cloud-native architecture
/cloud iac <provider>               # Generate Terraform/CloudFormation/Bicep/CDK
/cloud review                       # Well-Architected review (6 pillars)
/cloud cost                         # Cost analysis and optimisation
/cloud migrate <to-cloud>           # Migration strategy using the 6 R's
/cloud dr                           # Disaster recovery strategy
```

### Capacity Planning
```bash
/capacity estimate                  # Estimate resource requirements
/capacity scale <strategy>          # Design scaling approach
/capacity bottleneck                # Identify capacity constraints
/capacity load-test                 # Design load testing strategy
/capacity forecast                  # Model future capacity needs
/capacity right-size                # Identify and reduce over-provisioning
```

### Organisational Learning
```bash
/arch-learning analyze              # Analyse decision history
/arch-learning patterns             # Extract decision patterns
/arch-learning retrospective        # Facilitate team retrospective
/arch-learning lessons              # Generate lessons learned report

/capability-assessor assess         # Assess team capability maturity
/capability-assessor gaps           # Identify capability gaps
/capability-assessor roadmap        # Generate development roadmap

/patterns extract                   # Extract patterns from codebase/decisions
/patterns catalog                   # View pattern catalog
/patterns suggest <scenario>        # Suggest patterns for a situation
/patterns anti-patterns             # Document what doesn't work

/evolve assess                      # Assess evolutionary readiness
/evolve fitness-functions           # Define architectural fitness functions
/evolve brittleness                 # Identify brittle areas
/evolve increment                   # Plan incremental improvements
```

### Excel / Data
```bash
/excel read <file> [sheet]          # Read spreadsheet as markdown
/excel preview <file> [rows]        # Preview first N rows
/excel sheets <file>                # List available sheets
/excel convert <file> [sheet]       # Save to docs/imports/
```

---

## Project Structure

```
.
├── skills/
│   ├── phase-1/            # Individual capability skills
│   │   ├── compliance-packs/  # Stressor packs for regulatory frameworks
│   │   └── *.md
│   ├── phase-2/            # Organisational capability skills
│   ├── phase-3/            # Specialised skills (cloud, capacity)
│   └── utilities/          # Infrastructure skills
├── templates/              # Document templates
├── examples/               # Example outputs
├── helpers/                # Python utilities (Excel reading)
└── docs/
    ├── adr/                # Architecture Decision Records for this toolkit
    └── ...
```

---

## 📊 Project Status

| Phase | Status | Skills |
|-------|--------|--------|
| Phase 1: Individual Capabilities | ✅ Complete | 5 skills |
| Utilities | ✅ Complete | 1 skill |
| Phase 2: Organisational Capabilities | ✅ Complete | 4 skills |
| Phase 3: Specialised Tools | ✅ Complete | 2 skills |

**All phases complete.** See [Roadmap](ROADMAP.md) for future considerations.

---

## 🤝 Contributing

Contributions welcome — especially:
- 📋 **Compliance packs** for regulatory frameworks (GDPR, HIPAA, PCI DSS, ISO 27001, SOC 2) — see `skills/phase-1/compliance-packs/README.md`
- 💡 **New skill ideas** that align with Residuality Theory
- 📝 **Documentation improvements**
- 🐛 **Bug fixes and refinements**

See [Contributing Guide](CONTRIBUTING.md) for details.

---

## 📚 Documentation

- **[Residuality Theory](RESIDUALITY.md)** — The philosophy behind the toolkit
- **[Getting Started](GETTING_STARTED.md)** — New user guide
- **[Quick Reference](QUICKREF.md)** — Command cheatsheet
- **[Roadmap](ROADMAP.md)** — Development history and future plans
- **[ADRs](docs/adr/)** — Decisions made while building this toolkit
- **[Contributing](CONTRIBUTING.md)** — How to contribute

---

**Built with ❤️ for Solution Architects using Claude Code**
