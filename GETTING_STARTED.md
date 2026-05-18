# Getting Started with Solution Architect Toolkit

Welcome! This guide will get you up and running in under 5 minutes.

## Quick Start

### Step 1: Install

**Linux/Mac:**
```bash
git clone <repository-url> solution-architect-toolkit
cd solution-architect-toolkit
cp skills/phase-1/*.md ~/.claude/skills/
cp skills/phase-2/*.md ~/.claude/skills/
cp skills/phase-3/*.md ~/.claude/skills/
cp skills/utilities/*.md ~/.claude/skills/
pip install -r requirements.txt
```

**Windows:**
```powershell
git clone <repository-url> solution-architect-toolkit
cd solution-architect-toolkit
Copy-Item -Path "skills\phase-1\*.md" -Destination "$env:USERPROFILE\.claude\skills\"
Copy-Item -Path "skills\phase-2\*.md" -Destination "$env:USERPROFILE\.claude\skills\"
Copy-Item -Path "skills\phase-3\*.md" -Destination "$env:USERPROFILE\.claude\skills\"
Copy-Item -Path "skills\utilities\*.md" -Destination "$env:USERPROFILE\.claude\skills\"
pip install -r requirements.txt
```

### Step 2: Verify

Open Claude Code and type `/` — you should see:

**Phase 1 — Individual Capabilities:**
- `/adr`
- `/solution-doc`
- `/tech-stack`
- `/design-review`
- `/stressor`

**Phase 2 — Organisational Capabilities:**
- `/arch-learning`
- `/capability-assessor`
- `/patterns`
- `/evolve`

**Phase 3 — Specialised Tools:**
- `/cloud`
- `/capacity`

**Utilities:**
- `/excel`

✅ If you see these, installation was successful!

> **Note:** Excel reading requires Python and openpyxl. If `/excel` commands fail, run: `pip install -r requirements.txt`

### Step 3: Try Your First Command

Let's create your first Architecture Decision Record:

```
/adr create Use PostgreSQL for database
```

Claude will ask you questions, then generate a complete ADR saved to `docs/adr/ADR-001-use-postgresql-for-database.md`.

**Congratulations!** 🎉 You've just documented your first architecture decision.

---

## Your First Hour

### Start with Phase 1 — Individual Capabilities

#### 1. Technology Stack Advisor (5 min)
```
/tech-stack recommend
```
Answer questions about what you're building, get a complete stack recommendation with justification.

#### 2. Solution Documentation (10 min)
```
/solution-doc hld
```
Generate a comprehensive High-Level Design for your system.

#### 3. Stressor Analysis (10 min)
```
/stressor walk checkout        # map your primary path — actors and intentions
/stressor generate             # generate diverse stressors including absurd ones
/stressor analyze              # build the impact matrix
/stressor residues             # identify high-leverage residuals
```
Walk your primary path to map actors and intentions, then stress-test it. Identify vulnerabilities and residuals — new actors, intentions, or paths that make your system antifragile.

#### 4. Design Review (10 min)
```
/design-review complete
```
Get a scored review across 8 dimensions with prioritised recommendations.

### Explore Phase 2 — Organisational Capabilities

#### Assess your team (5 min)
```
/capability-assessor assess
```
Understand where your team's architectural maturity is today and where to focus.

#### Extract patterns from your decisions (5 min)
```
/patterns extract
```
Build a pattern library from your ADRs and codebase.

### Try Phase 3 — Specialised Tools

#### Design a cloud architecture (10 min)
```
/cloud design <your system>
```
Get a cloud-native architecture with Well-Architected review across all 6 pillars.

#### Plan capacity (5 min)
```
/capacity estimate
```
Translate user and load requirements into concrete resource estimates.

---

## Common First Tasks

### Document a New Project (30-40 min)

```
/tech-stack recommend
/adr create Use Node.js for backend
/adr create Use PostgreSQL for database
/solution-doc hld
/stressor walk                 # walk your primary paths first
/stressor generate             # generate stressors
/stressor analyze              # build impact matrix
/stressor residues             # identify residuals
/design-review architecture
```

**Result:** Complete architecture documentation with stress-tested resilience.

### Review an Existing System (15-20 min)

```
/design-review complete
/design-review security    # if security was flagged
/solution-doc runbook
/solution-doc deployment
```

**Result:** Full picture of strengths and improvement areas.

### Plan a Cloud Migration (20-30 min)

```
/cloud migrate to AWS
/cloud design <target architecture>
/cloud review
/cloud iac terraform
/cloud dr
```

**Result:** Migration strategy, target architecture, IaC, and DR plan.

### Run a Compliance-Aware Stressor Analysis

```
/stressor compliance gdpr     # inject GDPR stressors (when pack available)
/stressor walk                # walk your paths under the compliance stressors
/stressor analyze             # build impact matrix
/stressor residues            # residuals address compliance structurally
/adr create [document key residuals]
```

**Result:** Compliance requirements addressed as architectural residues — not a checklist.

---

## Understanding the Philosophy

This toolkit is built on **Residuality Theory**. Skills are designed to transfer capability to you — not create dependency on the tool.

**The measure of success is how little you need the toolkit** because you've internalised the thinking.

Key principles:
- **Antifragility over risk mitigation** — design systems that benefit from stress, not just resist it
- **Compliance as a byproduct** — good antifragile design addresses regulatory requirements structurally
- **Capability transfer** — every skill builds a thinking pattern you carry forward

---

## Where Files Are Saved

```
docs/
  adr/                    # Architecture Decision Records
  architecture/           # HLD.md, LLD-*.md
  deployment/             # DEPLOYMENT.md
  operations/             # RUNBOOK.md
  reviews/                # Design review reports
  technology/             # Tech stack reports
  stressor-analysis/      # Stressor matrices, residue recommendations
  cloud/                  # Cloud architecture docs
  capacity/               # Capacity estimates
```

---

## Tips for Success

1. **Start with what you need today** — don't try all skills at once
2. **Iterate** — generated docs are starting points, refine them
3. **Use stressor analysis during design**, not just after
4. **Link everything** — ADRs → HLD → LLD → code
5. **Share with your team** — the best architecture thinking is collaborative

---

## Getting Help

- 📖 [Quick Reference](QUICKREF.md) — all commands at a glance
- 📚 [Usage Guide](docs/USAGE.md) — detailed examples
- 🗺️ [Roadmap](ROADMAP.md) — what's built and what's next
- 🤝 [Contributing](CONTRIBUTING.md) — how to add compliance packs and skills

---

## Your First Hour Checklist

- [ ] Install the toolkit and verify with `/`
- [ ] Create your first ADR (`/adr create`)
- [ ] Get a tech stack recommendation (`/tech-stack recommend`)
- [ ] Run a stressor analysis — walk your paths, embrace the absurd! (`/stressor walk` then `/stressor analyze`)
- [ ] Run a design review (`/design-review complete`)
- [ ] Try a cloud design (`/cloud design`)
- [ ] Read the [Quick Reference](QUICKREF.md)
- [ ] Star the repository ⭐

---

**Welcome to the Solution Architect Toolkit. Let's build antifragile systems together.** 🐉
