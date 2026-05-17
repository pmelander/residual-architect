# Utilities Category

This directory contains **utility skills** that provide infrastructure and tooling support for the Solution Architect Toolkit.

## Utilities vs Capability-Building Skills

The toolkit has two types of skills:

### Capability-Building Skills (Phase 1, 2, 3)
**Purpose:** Build lasting architect capabilities through residuality theory

**Examples:**
- `/adr` - Build decision-making capability
- `/solution-doc` - Build systems thinking and documentation capability
- `/stressor` - Build antifragility thinking

**Philosophy:**
- Focus on teaching thinking patterns
- Success = using the tool less as capability transfers
- Tool Independence Score approaches 1.0
- Reflection prompts, learning capture, capability rubrics

### Utility Skills (This Directory)
**Purpose:** Provide infrastructure that enables capability-building skills

**Examples:**
- `/excel-reader` - Read spreadsheets → markdown (enables stressor analysis, tech comparisons)
- Future: `/diagram-generator`, `/template-manager`, `/search-docs`

**Philosophy:**
- Focus on reducing friction and enabling workflows
- Success = seamless integration, not capability transfer
- Bridge from existing tools (Excel) to toolkit workflows
- Eventually becomes unnecessary as architects shift to markdown-first thinking

## Key Differences

| Aspect | Capability Skills | Utility Skills |
|--------|------------------|----------------|
| **Goal** | Teach thinking | Provide tooling |
| **Success** | Tool independence | Seamless integration |
| **Residuality** | Capability persists | Workflow efficiency |
| **Learning** | Reflection prompts | Usage documentation |
| **Evolution** | Used less over time | Used as needed |

## When to Create a Utility

Create a utility skill when:
- It provides infrastructure/tooling (file conversion, search, automation)
- It doesn't teach a thinking pattern or architect capability
- It enables multiple capability-building skills
- Success is measured by convenience, not learning

**Don't create a utility for:**
- Skills that build thinking patterns → Use Phase 1/2/3
- One-off tools → Just document in CLAUDE.md
- External tools → Just call via Bash

## Current Utilities

### excel-reader
**Purpose:** Read Excel/CSV files and convert to markdown tables

**Commands:**
- `/excel read <file> [sheet]` - Read and display as markdown
- `/excel preview <file> [rows]` - Preview first N rows
- `/excel sheets <file>` - List available sheets
- `/excel convert <file> [sheet]` - Save to docs/imports/

**Enables:**
- Stressor analysis matrix import
- Tech comparison data import
- Capacity planning data import
- Any architecture artifact in spreadsheet format

**Residuality:** Bridges Excel-first thinking → markdown-first thinking

## Adding New Utilities

When adding a new utility skill:

1. **Validate it's a utility** (not capability-building)
2. **Create helper if needed** in `helpers/` directory
3. **Follow skill pattern** (frontmatter, commands, output locations)
4. **Document integration** with capability skills
5. **Add to this README**
6. **Create ADR** for significant utilities

## Integration with Capability Skills

Utilities should be called by capability skills when needed:

```markdown
### /stressor import <excel>

Import a stressor matrix from an Excel spreadsheet.

**How it works:**
1. Calls `/excel read <file>` to load spreadsheet
2. Validates matrix format (Stressor column + component columns)
3. Converts to stressor-analysis format
4. Saves to docs/stressor-analysis/

**See also:** `/excel-reader` skill for general spreadsheet reading
```

## Philosophy: Utilities as Bridges

Utilities are **transition tools** that help architects move from:
- Excel-first → Markdown-first
- Manual → Automated
- Scattered → Structured

The ultimate goal: Architects naturally work in markdown, and utilities become less necessary.

---

**Remember:** If it teaches thinking, it's a capability skill. If it provides tooling, it's a utility.
