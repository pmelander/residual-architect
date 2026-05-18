# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **Solution Architect Toolkit** — a comprehensive collection of Claude Code skills built on **Residuality Theory**, designed to build antifragile systems thinking and Solution Architect capabilities that compound over time.

The toolkit covers three phases of capability building:
- **Phase 1:** Individual architect capabilities
- **Phase 2:** Organisational and team capabilities
- **Phase 3:** Specialised domain tools (cloud, capacity)

## Architecture

### Project Structure

```
.
├── skills/
│   ├── phase-1/                    # Individual capability skills (✅ Complete)
│   │   ├── adr.md                  # Architecture Decision Records
│   │   ├── solution-doc.md         # Solution Documentation Generator
│   │   ├── tech-stack.md           # Technology Stack Advisor
│   │   ├── design-review.md        # Design Review
│   │   ├── stressor-analysis.md    # Stressor Analysis (antifragility)
│   │   └── compliance-packs/       # Regulatory stressor packs (extension point)
│   │       └── README.md
│   ├── phase-2/                    # Organisational capability skills (✅ Complete)
│   │   ├── arch-learning.md        # Architecture Learning Analyzer
│   │   ├── capability-assessor.md  # Team Capability Assessor
│   │   ├── pattern-extractor.md    # Pattern Extractor & Institutionalizer
│   │   └── evolutionary-coach.md   # Evolutionary Architecture Coach
│   ├── phase-3/                    # Specialised tools (✅ Complete)
│   │   ├── cloud-architect.md      # Cloud Architect
│   │   └── capacity-planner.md     # Capacity Planner
│   └── utilities/                  # Infrastructure skills (✅ Complete)
│       └── excel-reader.md         # Excel/CSV Reader
├── helpers/
│   └── read_spreadsheet.py         # Python helper for Excel reading
├── templates/                      # Document templates
│   ├── adr-template.md
│   ├── hld-template.md
│   ├── tech-comparison-template.md
│   ├── stressor-analysis-template.md
│   ├── capability-assessment-template.md
│   ├── pattern-template.md
│   ├── anti-pattern-template.md
│   └── fitness-function-template.md
├── examples/                       # Example outputs
├── requirements.txt                # Python dependencies (openpyxl)
└── docs/
    ├── adr/                        # ADRs documenting toolkit decisions
    │   ├── ADR-001-incorporate-residuality-theory.md
    │   ├── ADR-002-redesign-phase-2-for-capability-building.md
    │   ├── ADR-003-add-stressor-analysis-skill.md
    │   ├── ADR-004-add-excel-reading-utility.md
    │   ├── ADR-005-add-architecture-learning-analyzer.md
    │   ├── ADR-006-exclude-risk-assessor-skill.md
    │   └── ADR-007-compliance-via-stressor-packs.md
    └── ...                         # Generated documentation location
```

### Skill Development Pattern

Each skill follows this structure:
1. **Frontmatter** — YAML with `description` and `model: sonnet`
2. **Role Definition** — clear statement of the skill's purpose
3. **Capability Being Built** — what thinking the skill transfers to the architect
4. **Residuality Goal** — what success looks like when the capability is internalised
5. **Core Concept** — the key idea and compound effect
6. **Commands** — slash commands with capability focus for each
7. **Templates/Reference** — frameworks, patterns, and output formats
8. **Workflow** — step-by-step process
9. **Reflection Prompts** — questions that build the capability

### Key Design Principle

Skills are **capability transfer tools**, not dependency-creating tools. Every skill should build thinking that architects carry forward independently. The measure of success is how rarely the skill needs to be invoked because the thinking has been internalised.

## Development Commands

### Testing Skills

```bash
# View skill content
cat skills/phase-1/adr.md

# Symlink for development (changes reflected immediately)
ln -s $(pwd)/skills/phase-1/adr.md ~/.claude/skills/adr.md

# Copy for stable use
cp skills/phase-1/*.md ~/.claude/skills/
```

### Adding New Skills

1. Create skill file in the appropriate phase directory
2. Follow the naming convention: `skill-name.md`
3. Include frontmatter: `description` and `model: sonnet`
4. Follow the Skill Development Pattern above
5. Document any significant design decisions as an ADR in `docs/adr/`
6. Update `README.md`, `QUICKREF.md`, `GETTING_STARTED.md`, and `CLAUDE.md`

### Adding Compliance Packs

1. Create `skills/phase-1/compliance-packs/<framework>.md`
2. Follow the pack structure defined in `skills/phase-1/stressor-analysis.md`
3. Each stressor must be a concrete scenario (not a control statement)
4. Include regulation reference and explanation of the real harm
5. List common residues that emerge from the analysis

### Git Workflow

```bash
git checkout -b feature/new-skill-name
git commit -m "feat(phase-N): add skill-name skill"
git push origin feature/new-skill-name
```

## Skill Usage

### Phase 1 Skills

```bash
/adr create <title>              # Architecture Decision Records
/solution-doc hld                # Solution Documentation
/tech-stack recommend            # Technology Stack Advisor
/design-review complete          # Design Review
/stressor walk [path-name]       # Walk a path, evaluating each actor in sequence
/stressor analyze                # Stressor Analysis — build impact matrix
/stressor compliance <pack>      # Inject compliance stressor pack
```

### Phase 2 Skills

```bash
/arch-learning analyze           # Architecture Learning Analyzer
/capability-assessor assess      # Team Capability Assessor
/patterns extract                # Pattern Extractor
/evolve assess                   # Evolutionary Architecture Coach
```

### Phase 3 Skills

```bash
/cloud design <architecture>     # Cloud Architect
/cloud iac <provider>
/cloud review
/cloud cost
/cloud migrate <to-cloud>
/cloud dr

/capacity estimate               # Capacity Planner
/capacity scale <strategy>
/capacity bottleneck
/capacity load-test
/capacity forecast
/capacity right-size
```

### Utility Skills

```bash
/excel read <file> [sheet]       # Excel/CSV Reader
```

## Key Principles

### Residuality Theory Foundation

1. **Design for unknown unknowns** — not just known risks
2. **Antifragility over robustness** — systems that benefit from stress
3. **Residues over mitigations** — architectural improvements that protect against classes of stressors
4. **Compliance as byproduct** — regulatory requirements addressed structurally, not procedurally
5. **Risk assessment replaced** — stressor analysis covers risk and more

### For Skill Development

1. **Capability first** — every command should build a thinking skill, not just produce output
2. **Clear residuality goal** — state what success looks like when the skill is no longer needed
3. **Reflection prompts** — include questions that deepen the thinking
4. **Consistent philosophy** — new skills must align with Residuality Theory; if a skill would train architects to think in checklists or registers, reconsider the approach

## Installation

```bash
# Copy method (stable use)
cp skills/phase-1/*.md ~/.claude/skills/
cp skills/phase-2/*.md ~/.claude/skills/
cp skills/phase-3/*.md ~/.claude/skills/
cp skills/utilities/*.md ~/.claude/skills/
pip install -r requirements.txt

# Symlink method (development — changes reflected immediately)
ln -s /path/to/repo/skills/phase-1/*.md ~/.claude/skills/
ln -s /path/to/repo/skills/phase-2/*.md ~/.claude/skills/
ln -s /path/to/repo/skills/phase-3/*.md ~/.claude/skills/
ln -s /path/to/repo/skills/utilities/*.md ~/.claude/skills/
```

## Phase Status

| Phase | Status | Skills |
|-------|--------|--------|
| Phase 1: Individual Capabilities | ✅ Complete | adr, solution-doc, tech-stack, design-review, stressor-analysis |
| Utilities | ✅ Complete | excel-reader |
| Phase 2: Organisational Capabilities | ✅ Complete | arch-learning, capability-assessor, pattern-extractor, evolutionary-coach |
| Phase 3: Specialised Tools | ✅ Complete | cloud-architect, capacity-planner |

## Contributing

When adding new skills:
1. Follow existing skill patterns — especially the Capability Being Built and Residuality Goal sections
2. Create an ADR in `docs/adr/` for any significant design decision (including decisions *not* to build something)
3. Update all documentation files: README.md, QUICKREF.md, GETTING_STARTED.md, CLAUDE.md
4. Test thoroughly before committing
