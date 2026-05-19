# Residual Architecture Skill Set for Claude Code

A collection of Claude Code skills built on **Residuality Theory** — designed to build antifragile systems thinking and Solution Architect capabilities that compound over time.

> **Philosophy:** Skills are designed to transfer capability to architects, not create dependency on tools. The measure of success is how little you need them.

## 🚀 Quick Links

- **[Introduction to Residuality Theory](RESIDUALITY.md)** - The philosophy behind this toolkit — start here if you're new to the framework
- **[Getting Started Guide](GETTING_STARTED.md)** - Get up and running in 5 minutes
- **[Quick Reference](QUICKREF.md)** - All commands at a glance
- **[Roadmap](ROADMAP.md)** - What's built and what's next
- **[Contributing](CONTRIBUTING.md)** - How to add skills and compliance packs

---

## Start Your Journey

The first thing to do with any new engagement isn't to open a specific skill — it's to understand where you are and what the terrain demands.

```
/journey start
```

Tell Claude about the system you're working on — what you're trying to achieve, what exists today, and any constraints. It will assess the terrain and map your recommended skill sequence from there.

The journey looks different depending on the terrain:

- **Greenfield** — design paths, walk and stress them, then build what survives
- **Brownfield** — discover what exists before changing anything
- **Minefield** — discover extensively before touching anything

At the heart of every journey is an iteration loop, not a straight line:

```
walk paths → generate stressors → build matrix → find residuals
     ↑                                                  ↓
  re-walk ←← implement residuals ←← impact low enough? ←←
```

You keep iterating until the system's vulnerability is sufficiently low — not zero, but low enough given the aspiration and the cost of further improvement.

→ [Full Getting Started Guide](GETTING_STARTED.md) · [All commands](QUICKREF.md)

---

## Skills

14 skills spanning the full architectural journey:

| Category | Skills |
|----------|--------|
| Orchestration | `/journey` |
| Discovery | `/discover` |
| Stressor Analysis | `/stressor` |
| Design & Documentation | `/adr` `/solution-doc` `/tech-stack` `/design-review` |
| Cloud & Infrastructure | `/cloud` `/capacity` |
| Organisational Capabilities | `/arch-learning` `/capability-assessor` `/patterns` `/evolve` |
| Utilities | `/excel` |

> **Note on Risk and Compliance:** A standalone Risk Assessor and Compliance Checker were deliberately excluded. Residuality Theory covers risk through antifragility thinking (`/stressor`) — risk registers create false confidence in enumerated threats. Compliance is handled through **stressor compliance packs** (`/stressor compliance <pack>`), so regulatory requirements emerge as residues of antifragile design rather than a separate checklist process. See [ADR-006](docs/adr/ADR-006-exclude-risk-assessor-skill.md) and [ADR-007](docs/adr/ADR-007-compliance-via-stressor-packs.md).

---

## ⚡ Install

```bash
git clone <repo-url> solution-architect-toolkit
cd solution-architect-toolkit

# Install all skills (Claude Code expects skills/<name>/SKILL.md)
cp -R skills/* ~/.claude/skills/

# Python dependency for Excel reading
pip install -r requirements.txt
```

Open Claude Code and type `/` to see your skills.

📖 See [Installation Guide](docs/INSTALLATION.md) for detailed setup and troubleshooting.

---

## Project Structure

```
.
├── skills/                             # Claude Code layout: skills/<name>/SKILL.md
│   ├── adr/
│   │   └── SKILL.md
│   ├── solution-doc/
│   │   └── SKILL.md
│   ├── tech-stack/
│   │   └── SKILL.md
│   ├── design-review/
│   │   └── SKILL.md
│   ├── stressor/
│   │   ├── SKILL.md
│   │   └── compliance-packs/       # Regulatory stressor packs
│   │       ├── README.md
│   │       └── gdpr.md
│   ├── excel/
│   │   └── SKILL.md
│   ├── arch-learning/
│   │   └── SKILL.md
│   ├── capability-assessor/
│   │   └── SKILL.md
│   ├── patterns/
│   │   └── SKILL.md
│   ├── evolve/
│   │   └── SKILL.md
│   ├── cloud/
│   │   └── SKILL.md
│   ├── capacity/
│   │   └── SKILL.md
│   ├── discover/
│   │   └── SKILL.md
│   └── journey/
│       └── SKILL.md
├── templates/                          # Document templates
├── examples/                           # Example outputs
├── helpers/                            # Python utilities (Excel reading)
└── docs/
    ├── adr/                            # Architecture Decision Records for this toolkit
    └── ...
```

---

## 📊 Skills

| Category | Count |
|----------|-------|
| Orchestration & Discovery | 2 |
| Stressor Analysis | 1 |
| Design & Documentation | 4 |
| Cloud & Infrastructure | 2 |
| Organisational Capabilities | 4 |
| Utilities | 1 |
| **Total** | **14** |

See [Roadmap](ROADMAP.md) for future considerations.

---

## 🤝 Contributing

Contributions welcome — especially:
- 📋 **Compliance packs** for regulatory frameworks (GDPR, HIPAA, PCI DSS, ISO 27001, SOC 2) — see `skills/stressor/compliance-packs/README.md`
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
