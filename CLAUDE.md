# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **Solution Architect Toolkit** - a comprehensive collection of Claude Code skills designed to enhance Solution Architect capabilities. The toolkit provides specialized skills for architecture design, documentation, analysis, and implementation guidance.

## Architecture

### Project Structure

```
.
├── skills/           # Claude Code skills (*.md files)
│   ├── phase-1/     # Capability-building skills (✅ Complete)
│   │   ├── adr.md                  # Architecture Decision Records
│   │   ├── solution-doc.md         # Solution Documentation Generator
│   │   ├── tech-stack.md           # Technology Stack Advisor
│   │   ├── design-review.md        # Design Review
│   │   └── stressor-analysis.md    # Stressor Analysis
│   ├── phase-2/     # Organizational capabilities (🔄 In Progress)
│   │   └── arch-learning.md        # Architecture Learning Analyzer
│   ├── utilities/   # Infrastructure skills (✅ Complete)
│   │   └── excel-reader.md         # Excel/CSV Reader
│   └── phase-3/     # Specialized tools (🔄 Planned)
├── helpers/          # Python utilities
│   └── read_spreadsheet.py         # Excel/CSV reading helper
├── templates/        # Document templates
│   ├── adr-template.md
│   ├── hld-template.md
│   ├── tech-comparison-template.md
│   └── stressor-analysis-template.md
├── examples/         # Example outputs
├── requirements.txt  # Python dependencies
└── docs/            # Generated documentation location
    ├── adr/         # Architecture Decision Records
    ├── arch-learning/ # Learning analysis outputs
    └── ...
```

### Skill Development Pattern

Each skill follows this structure:
1. **Frontmatter**: YAML with description and model
2. **Role Definition**: Clear description of the skill's purpose
3. **Commands**: Available slash commands and their usage
4. **Templates**: Document templates and formats
5. **Best Practices**: Guidelines for effective use
6. **Workflow**: Step-by-step process the skill follows

## Development Commands

### Testing Skills

To test a skill locally (before installing to ~/.claude/skills):
```bash
# View skill content
cat skills/phase-1/adr.md

# Test by creating a symlink (optional)
ln -s $(pwd)/skills/phase-1/adr.md ~/.claude/skills/adr.md
```

### Adding New Skills

1. Create skill file in appropriate phase directory
2. Follow the naming convention: `skill-name.md`
3. Include frontmatter with description and model
4. Test the skill with Claude Code
5. Add documentation to README.md

### Git Workflow

```bash
# Create feature branch
git checkout -b feature/new-skill-name

# Commit with descriptive messages
git commit -m "feat(phase-1): add new-skill-name skill"

# Push and create PR
git push origin feature/new-skill-name
```

## Skill Usage

### Phase 1 Skills (Available Now)

**Architecture Decision Records**
```bash
/adr create <title>        # Create new ADR
/adr list                  # List all ADRs
/adr update <number>       # Update existing ADR
/adr search <term>         # Search ADRs
```

**Solution Documentation**
```bash
/solution-doc hld          # Generate High-Level Design
/solution-doc lld          # Generate Low-Level Design
/solution-doc deployment   # Generate Deployment Guide
/solution-doc runbook      # Generate Operations Runbook
/solution-doc complete     # Generate all documentation
```

**Technology Stack Advisor**
```bash
/tech-stack recommend      # Recommend complete tech stack
/tech-stack evaluate <tech> # Evaluate specific technology
/tech-stack compare <tech1> vs <tech2>  # Compare technologies
/tech-stack migrate from <old> to <new> # Analyze migration
/tech-stack report         # Generate selection report
```

**Design Review**
```bash
/design-review architecture   # Review system architecture
/design-review api           # Review API design
/design-review data          # Review data architecture
/design-review security      # Security-focused review
/design-review performance   # Performance-focused review
/design-review complete      # Comprehensive review
```

**Stressor Analysis**
```bash
/stressor generate [count]        # Generate creative stressors
/stressor analyze                 # Map impacts to components
/stressor vulnerabilities         # Identify high-impact areas
/stressor residues                # Suggest improvements
/stressor iterate                 # Re-analyze after changes
/stressor workshop                # Facilitate team workshop
/stressor import <file> [sheet]   # Import from Excel/CSV
```

### Utility Skills (Available Now)

**Excel Reader**
```bash
/excel read <file> [sheet]        # Read spreadsheet as markdown
/excel preview <file> [rows]      # Preview first N rows
/excel sheets <file>              # List available sheets
/excel convert <file> [sheet]     # Save to docs/imports/
```

**Helper Script** (advanced usage):
```bash
python helpers/read_spreadsheet.py data.xlsx
python helpers/read_spreadsheet.py data.xlsx --sheet "Sheet2"
python helpers/read_spreadsheet.py data.xlsx --rows 10
python helpers/read_spreadsheet.py data.xlsx --list-sheets
```

### Phase 2 Skills (Available Now)

**Architecture Learning Analyzer**
```bash
/arch-learning analyze            # Analyze ADR history
/arch-learning patterns           # Extract patterns from decisions
/arch-learning outcomes           # Review decision outcomes
/arch-learning retrospective      # Facilitate team retrospective
/arch-learning lessons            # Generate lessons learned report
/arch-learning trends             # Identify trends over time
```

**Capability:** Builds organizational learning from architectural history, extracts patterns, tracks outcomes, creates feedback loops

## Key Principles

### For Solution Architect Work

1. **Document Decisions**: Use ADRs for significant architectural decisions
2. **Context First**: Always start with business context and requirements
3. **Trade-offs Matter**: Document pros, cons, and alternatives
4. **Think Long-term**: Consider maintainability, scalability, evolution
5. **Be Specific**: Avoid vague statements, provide concrete recommendations
6. **Link Everything**: Reference related ADRs, docs, and resources

### For Skill Development

1. **Clear Commands**: Skills should have clear slash commands
2. **Ask Questions**: Skills should gather context through questions
3. **Use Templates**: Provide consistent, high-quality output formats
4. **Be Thorough**: Skills should be comprehensive but focused
5. **Include Examples**: Show users what good looks like
6. **Consider Workflow**: Skills should follow natural work patterns

## Installation

Users can install these skills by:

1. **Symlink Method** (for development):
   ```bash
   ln -s /path/to/this/repo/skills/phase-1/*.md ~/.claude/skills/
   ln -s /path/to/this/repo/skills/phase-2/*.md ~/.claude/skills/
   ln -s /path/to/this/repo/skills/utilities/*.md ~/.claude/skills/
   pip install -r requirements.txt
   ```

2. **Copy Method** (for stable use):
   ```bash
   cp /path/to/this/repo/skills/phase-1/*.md ~/.claude/skills/
   cp /path/to/this/repo/skills/phase-2/*.md ~/.claude/skills/
   cp /path/to/this/repo/skills/utilities/*.md ~/.claude/skills/
   pip install -r requirements.txt
   ```

3. **Git Clone Method**:
   ```bash
   cd ~/.claude
   mkdir -p skills
   cd skills
   git clone <repo-url> solution-architect-toolkit
   ln -s solution-architect-toolkit/skills/phase-1/*.md .
   ```

## Phase Roadmap

### Phase 1: Immediate Impact ✅
- [x] Architecture Decision Records
- [x] Solution Documentation Generator
- [x] Technology Stack Advisor
- [x] Design Review

### Phase 2: Deep Analysis 🔄
- [ ] Tech Debt Analyzer
- [ ] System Mapper
- [ ] Migration Planner
- [ ] API Designer

### Phase 3: Specialized 🔄
- [ ] Cloud Architect
- [ ] Compliance Checker
- [ ] Capacity Planner
- [ ] Risk Assessor

## Contributing

When adding new skills:
1. Follow existing skill patterns
2. Include comprehensive templates
3. Add examples to examples/ directory
4. Update README.md with new skill
5. Test thoroughly before committing
6. Create ADR for significant decisions
