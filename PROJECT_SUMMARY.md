# Residual Architecture Skill Set — Project Summary

## Overview

The **Residual Architecture Skill Set** is a collection of Claude Code skills built on **Residuality Theory** — designed to build antifragile systems thinking and Solution Architect capabilities that compound over time.

**Philosophy:** Skills transfer capability to architects, not create dependency on tools. The measure of success is how rarely you need the toolkit, because the thinking has been internalised.

**Current status:** All three phases complete.

---

## Project Structure

```
solution-architect-toolkit/
├── README.md
├── CLAUDE.md                       # Development guide (this project's CLAUDE.md)
├── QUICKREF.md                     # All commands at a glance
├── GETTING_STARTED.md              # New user guide
├── ROADMAP.md                      # Development history and future considerations
├── CONTRIBUTING.md
│
├── skills/
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
│   │   └── compliance-packs/
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
│
├── templates/                      # Document templates
├── examples/                       # Example outputs
├── helpers/                        # Python utilities
│   └── read_spreadsheet.py
├── requirements.txt
└── docs/
    ├── adr/                        # Toolkit's own ADRs (7 decisions documented)
    ├── INSTALLATION.md
    └── USAGE.md
```

---

## Skills by Phase

### Phase 1: Individual Capabilities ✅

Build the core thinking skills every Solution Architect needs.

| Skill | Command | Capability Built |
|-------|---------|-----------------|
| Architecture Decision Records | `/adr` | Structured decision-making and trade-off thinking |
| Solution Documentation | `/solution-doc` | Systems thinking and communication |
| Technology Stack Advisor | `/tech-stack` | Objective evaluation without hype |
| Design Review | `/design-review` | Self-assessment and pattern recognition |
| Stressor Analysis | `/stressor` | Antifragility thinking and resilience design |

**Stressor Analysis extension:** `/stressor compliance <pack>` injects regulatory frameworks as stressor sets, so compliance requirements emerge as architectural residues rather than a checklist process.

### Utilities ✅

| Skill | Command | Purpose |
|-------|---------|---------|
| Excel Reader | `/excel` | Import stressor matrices and data from Excel/CSV |

### Phase 2: Organisational Capabilities ✅

Build team and organisational meta-capabilities that compound over time.

| Skill | Command | Capability Built |
|-------|---------|-----------------|
| Architecture Learning Analyzer | `/arch-learning` | Systematic learning from past decisions |
| Team Capability Assessor | `/capability-assessor` | Team maturity self-awareness and growth |
| Pattern Extractor | `/patterns` | Institutional knowledge and pattern libraries |
| Evolutionary Coach | `/evolve` | Continuous architecture improvement mindset |

### Phase 3: Specialised Tools ✅

Domain-specific capabilities for common SA specialisms.

| Skill | Command | Capability Built |
|-------|---------|-----------------|
| Cloud Architect | `/cloud` | Cloud-native thinking, IaC discipline, Well-Architected mindset |
| Capacity Planner | `/capacity` | Demand modelling, scaling intuition, bottleneck identification |

---

## Key Design Decisions

Seven ADRs document the significant decisions made while building this toolkit:

| ADR | Decision |
|-----|---------|
| ADR-001 | Incorporate Residuality Theory as the foundation |
| ADR-002 | Redesign Phase 2 for capability-building (not tool-centric) |
| ADR-003 | Add Stressor Analysis skill |
| ADR-004 | Add Excel reading utility |
| ADR-005 | Add Architecture Learning Analyzer |
| ADR-006 | **Exclude Risk Assessor** — covered by antifragility thinking via `/stressor` |
| ADR-007 | **Replace Compliance Checker** with `/stressor compliance` packs — compliance as byproduct of antifragile design |

ADR-006 and ADR-007 are particularly important: they show the toolkit's philosophy actively shaping what *not* to build.

---

## Phase Status

| Phase | Status | Completion |
|-------|--------|-----------|
| Phase 1: Individual Capabilities | ✅ Complete | 2026-05-17 |
| Utilities | ✅ Complete | 2026-05-17 |
| Phase 2: Organisational Capabilities | ✅ Complete | 2026-05-18 |
| Phase 3: Specialised Tools | ✅ Complete | 2026-05-18 |

---

## Key Differentiators

1. **Residuality Theory foundation** — built around antifragility, not risk registers or checklists
2. **Capability transfer, not dependency** — skills build thinking that architects carry forward
3. **Compliance via antifragility** — regulatory requirements emerge as residues of good design
4. **Decisions documented** — the toolkit's own ADRs are part of the project, modelling the practice
5. **Philosophy-consistent** — skills that would undermine the mental model were deliberately excluded

---

## Contributing

The most valuable open contribution area is **compliance packs** — curated stressor sets for GDPR, HIPAA, PCI DSS, ISO 27001, and SOC 2. These require regulatory expertise and make the toolkit immediately useful for compliance-heavy organisations without compromising its philosophical consistency.

See `skills/stressor/compliance-packs/README.md` for the pack structure.

Other contributions: new Phase 4 skills, examples, template refinements. See [CONTRIBUTING.md](../CONTRIBUTING.md).

---

## Future Considerations

Phase 4 ideas (under consideration, no timeline):

- **Security Architect** — threat modelling, security architecture design
- **Team Architect** — Team Topologies, Conway's Law analysis
- **Integration Architect** — event-driven architecture, message queue design
- **Data Architect** — data modelling, governance, data lake design

Any new skill must align with Residuality Theory — if it trains architects to think in checklists or registers rather than antifragility, a different approach is needed.
