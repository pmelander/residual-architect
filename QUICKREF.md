# Solution Architect Toolkit - Quick Reference

## Quick Start

### Installation
```bash
git clone <repo-url> solution-architect-toolkit
cp solution-architect-toolkit/skills/phase-1/*.md ~/.claude/skills/
```

### Available Commands

#### Architecture Decision Records
```bash
/adr create <title>      # Create new ADR
/adr list                # List all ADRs  
/adr update <number>     # Update existing ADR
/adr search <term>       # Search ADRs
/adr template            # Show ADR template
```

#### Solution Documentation
```bash
/solution-doc hld                # High-Level Design
/solution-doc lld [component]    # Low-Level Design
/solution-doc deployment         # Deployment Guide
/solution-doc runbook            # Operations Runbook
/solution-doc complete           # Generate all docs
/solution-doc update <type>      # Update existing doc
```

#### Technology Stack Advisor
```bash
/tech-stack recommend                      # Full stack recommendation
/tech-stack evaluate <technology>          # Evaluate specific tech
/tech-stack compare <tech1> vs <tech2>     # Compare technologies
/tech-stack migrate from <old> to <new>    # Migration analysis
/tech-stack report                         # Generate tech report
```

#### Design Review
```bash
/design-review architecture   # Review system architecture
/design-review api           # Review API design
/design-review data          # Review data architecture
/design-review security      # Security review
/design-review performance   # Performance review
/design-review complete      # Comprehensive review
```

#### Stressor Analysis
```bash
/stressor generate [count]        # Generate creative stressors
/stressor analyze                 # Map impacts to components
/stressor vulnerabilities         # Identify high-impact areas
/stressor residues                # Suggest improvements
/stressor iterate                 # Re-analyze after changes
/stressor workshop                # Facilitate team workshop
/stressor import <file> [sheet]   # Import from Excel/CSV
```

#### Excel Reader (Utility)
```bash
/excel read <file> [sheet]        # Read spreadsheet as markdown
/excel preview <file> [rows]      # Preview first N rows
/excel sheets <file>              # List available sheets
/excel convert <file> [sheet]     # Save to docs/imports/
```

#### Architecture Learning (Phase 2)
```bash
/arch-learning analyze            # Analyze ADR history
/arch-learning patterns           # Extract patterns
/arch-learning outcomes           # Review outcomes
/arch-learning retrospective      # Facilitate retro
/arch-learning lessons            # Generate lessons learned
/arch-learning trends             # Identify trends
```

#### Team Capability Assessor (Phase 2)
```bash
/capability-assessor assess       # Assess team maturity
/capability-assessor gaps         # Identify capability gaps
/capability-assessor roadmap      # Create development plan
/capability-assessor track        # Track growth over time
/capability-assessor exercises    # Get capability-building activities
/capability-assessor compare      # Compare to benchmarks
```

#### Pattern Extractor (Phase 2)
```bash
/patterns extract                 # Extract patterns from knowledge
/patterns catalog                 # View pattern library
/patterns suggest <scenario>      # Get pattern recommendations
/patterns effectiveness           # Track pattern success
/patterns anti-patterns           # Document what doesn't work
/patterns evolve                  # Update patterns based on learning
```

#### Evolutionary Architecture Coach (Phase 2)
```bash
/evolve assess                    # Assess evolutionary readiness
/evolve fitness-functions         # Define fitness functions
/evolve brittleness               # Identify brittle areas
/evolve increment                 # Plan incremental improvements
/evolve health                    # Track architectural health
/evolve coach                     # Interactive coaching
```

## Common Workflows

### Starting New Project
```bash
1. /tech-stack recommend
2. /adr create [for major decisions]
3. /solution-doc hld
4. /stressor analyze [stress-test design]
5. /design-review architecture
6. /solution-doc deployment
```

### Pre-Production Review
```bash
1. /design-review complete
2. [Fix critical issues]
3. /design-review [specific areas that were flagged]
4. /solution-doc complete
```

### Technology Evaluation
```bash
1. /tech-stack compare <option1> vs <option2>
2. /tech-stack evaluate <chosen-option>
3. /adr create <technology-decision>
```

### Ongoing Maintenance
```bash
Monthly:  /design-review complete
Quarterly: /tech-stack evaluate [current stack]
As-needed: /adr update [when decisions change]
           /solution-doc update [keep docs current]
```

### Building Organizational Capabilities (Phase 2)

#### Initial Team Assessment
```bash
1. /capability-assessor assess     # Understand current maturity
2. /capability-assessor gaps       # Identify priorities
3. /capability-assessor roadmap    # Create 3-6 month plan
4. /capability-assessor exercises  # Start capability building
```

#### Pattern Library Creation
```bash
1. /patterns extract               # Extract patterns from ADRs/code
2. /patterns catalog               # Review extracted patterns
3. /patterns anti-patterns         # Document what doesn't work
4. /patterns suggest <scenario>    # Test pattern recommendations
```

#### Evolutionary Architecture Setup
```bash
1. /evolve assess                  # Assess current readiness
2. /evolve fitness-functions       # Define 5-10 key functions
3. /evolve brittleness             # Identify improvement areas
4. /evolve increment               # Plan first improvements
```

#### Organizational Learning Practice
```bash
1. /arch-learning analyze          # Analyze decision history
2. /arch-learning patterns         # Extract decision patterns
3. /arch-learning outcomes         # Track what worked
4. /arch-learning lessons          # Generate lessons report
```

#### Quarterly Review Rhythm (Phase 2)
```bash
Month 1-2: Execute improvement roadmaps
Month 3 (mid-cycle):
  - /capability-assessor track
  - /patterns effectiveness
  - /evolve health
  
Month 6 (end of cycle):
  - /capability-assessor assess [reassess]
  - /capability-assessor roadmap [next quarter]
  - /arch-learning retrospective
  - /patterns evolve [update patterns]
  - /evolve assess [measure improvement]
```

## Output Locations

```
docs/
  adr/                    # Architecture Decision Records
    ADR-001-*.md
    ADR-002-*.md
  architecture/           # Architecture docs
    HLD.md
    LLD-*.md
  deployment/             # Deployment guides
    DEPLOYMENT.md
  operations/             # Operations docs
    RUNBOOK.md
  reviews/                # Review reports
    design-review-*.md
    tech-evaluation-*.md
  stressor-analysis/      # Stressor analyses
    stressor-*.md
  imports/                # Imported Excel/CSV data
    *.md
  arch-learning/          # Organizational learning (Phase 2)
    adr-analysis-*.md
    pattern-catalog.md
    learning-session-*.md
  capability-assessments/ # Team maturity (Phase 2)
    assessment-*.md
    gap-analysis-*.md
    roadmap-*.md
    growth-tracking.md
  patterns/               # Pattern library (Phase 2)
    pattern-catalog.md
    architectural/*.md
    decision/*.md
    technology/*.md
    anti-patterns/*.md
    pattern-effectiveness.md
  evolutionary-architecture/ # Evolutionary practices (Phase 2)
    assessment-*.md
    fitness-functions.md
    brittleness-analysis-*.md
    incremental-plan-*.md
    health-dashboard.md
```
    architecture-review-*.md
    api-review-*.md
  technology/             # Technology docs
    tech-stack-recommendation.md
    tech-comparison-*.md
  stressor-analysis/      # Stressor analysis results
    stressor-matrix-*.md
    impact-analysis-*.md
    residue-recommendations-*.md
```

## Best Practices

### ADRs
- ✅ Create for significant decisions only
- ✅ Document trade-offs honestly
- ✅ Update status when superseded
- ✅ Link related ADRs

### Documentation
- ✅ Keep current with code
- ✅ Use diagrams liberally
- ✅ Target appropriate audience
- ✅ Version control everything

### Technology Selection
- ✅ Consider team expertise
- ✅ Start simple
- ✅ Evaluate total cost
- ✅ Plan exit strategy

### Design Reviews
- ✅ Review early and often
- ✅ Address critical issues immediately
- ✅ Track moderate issues
- ✅ Learn from review findings

### Stressor Analysis
- ✅ Be creative with stressors
- ✅ Include unknown unknowns
- ✅ Map impacts honestly
- ✅ Iterate after improvements
- ✅ Facilitate as team exercise

### Phase 2: Organizational Capabilities

#### Capability Development
- ✅ Focus on 1-2 dimensions at a time
- ✅ Practice on real work, not toy problems
- ✅ Track progress quarterly
- ✅ Celebrate improvements
- ✅ Integrate with daily work

#### Pattern Management
- ✅ Start with 10-15 high-value patterns
- ✅ Include real examples from your codebase
- ✅ Document context (when to use/not use)
- ✅ Track effectiveness over time
- ✅ Evolve patterns based on outcomes

#### Evolutionary Architecture
- ✅ Define 5-10 critical fitness functions first
- ✅ Automate fitness function checks
- ✅ Make architectural changes incrementally
- ✅ Design for reversibility
- ✅ Track evolutionary readiness quarterly

#### Organizational Learning
- ✅ Review ADR outcomes regularly
- ✅ Extract patterns from successful decisions
- ✅ Document failures as anti-patterns
- ✅ Share learnings across team
- ✅ Build institutional memory
- ✅ Share findings with team

## Tips

**For Maximum Effectiveness:**
- Document as you go, not at the end
- Use ADRs for team alignment
- Review in phases, don't wait for "done"
- Keep documentation current
- Link everything together

**Common Mistakes to Avoid:**
- ❌ Creating ADRs for minor decisions
- ❌ Letting documentation go stale
- ❌ Picking technology based on hype
- ❌ Waiting until end to review
- ❌ Ignoring critical review findings

## Keyboard Shortcuts

In Claude Code:
- `/` - Show available skills
- `Ctrl+Enter` - Submit message
- `Esc` - Cancel current operation

## Getting Help

- 📖 Full documentation: `docs/USAGE.md`
- 📥 Installation help: `docs/INSTALLATION.md`
- 📝 Examples: `examples/`
- 📋 Templates: `templates/`
- 🏗️ Architecture: `CLAUDE.md`

## Phase Roadmap

**Phase 1** ✅ - Immediate Impact
- Architecture Decision Records
- Solution Documentation
- Technology Stack Advisor
- Design Review
- Stressor Analysis

**Utilities** ✅ - Infrastructure
- Excel Reader (import spreadsheets)

**Phase 2** 🔄 - Organizational Capabilities (In Progress)
- ✅ Architecture Learning Analyzer
- 📋 Team Capability Assessor
- 📋 Pattern Extractor
- 📋 Evolutionary Coach

**Phase 3** 🔄 - Specialized (Planned)
- Cloud Architect
- Compliance Checker
- Capacity Planner
- Risk Assessor

## Quick Examples

### Create an ADR
```
/adr create Use microservices architecture

Claude will guide you through:
- Context and problem
- Decision details
- Trade-offs
- Alternatives considered
```

### Get Tech Recommendations
```
/tech-stack recommend

Answer questions about:
- What you're building
- Scale requirements
- Team expertise
- Constraints

Receive full stack recommendation with justification
```

### Review Your Architecture
```
/design-review complete

Claude analyzes:
- Architecture principles
- Scalability
- Performance
- Security
- And 4 more dimensions

Provides scored assessment with recommendations
```

### Stress-Test Your System
```
/stressor analyze

Claude guides you through:
- Generating diverse stressors (including absurd ones!)
- Mapping impacts to architecture components
- Identifying vulnerabilities
- Recommending high-leverage improvements

Build antifragile systems that benefit from stress 🐉
```

---

**For detailed information, see the full documentation in `docs/USAGE.md`**
