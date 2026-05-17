# ADR-001: Use Markdown Format for Claude Code Skills

**Status:** Accepted

**Date:** 2026-05-17

**Deciders:** Solution Architect Team

**Technical Story:** Phase 1 Implementation - Skill Development

## Context

We need to create a set of Solution Architect skills for Claude Code. Claude Code supports skills written in Markdown format with YAML frontmatter. We must decide on the format and structure for our skills to ensure consistency, maintainability, and ease of use.

Key considerations:
- Skills need to be editable by any text editor
- Must integrate seamlessly with Claude Code
- Should be version-controllable
- Need to provide clear guidance to Claude
- Must support templates and structured output

## Decision

We will use **Markdown (.md) format** for all Claude Code skills with the following structure:

1. **YAML Frontmatter**: Contains metadata (description, model)
2. **Role Definition**: Clear description of skill purpose
3. **Commands Section**: Available slash commands
4. **Templates Section**: Document formats and examples
5. **Best Practices**: Guidelines for usage
6. **Workflow Section**: Step-by-step processes

Example structure:
```markdown
---
description: Short description of the skill
model: sonnet
---

# Skill Name

You are an expert...

## Commands
/command-name - Description

## Templates
[Template content]

## Best Practices
[Guidelines]
```

## Consequences

### Positive
- **Simple and Accessible**: Plain text format editable in any editor
- **Version Control**: Easy to track changes in Git
- **Portable**: Can be easily shared and distributed
- **Flexible**: Supports rich formatting for templates and examples
- **Claude-Native**: Direct integration with Claude Code skill system
- **Documentable**: Self-documenting format with clear sections
- **No Build Step**: No compilation or processing required

### Negative
- **Limited Validation**: No compile-time checking of skill correctness
- **Manual Testing Required**: Must test skills manually with Claude Code
- **No Type Safety**: Can't enforce skill contract at development time
- **Potential Inconsistency**: Developers might deviate from standard structure

### Neutral
- Skills are loaded dynamically by Claude Code at runtime
- Updates require replacing the skill file
- Large skills can become lengthy documents

## Alternatives Considered

### Alternative 1: JSON/YAML Configuration Files
- **Pros:** 
  - Machine-readable format
  - Could add schema validation
  - Structured data easier to parse programmatically
- **Cons:** 
  - Less human-readable
  - Poor for long-form templates and instructions
  - Doesn't match Claude Code's native format
  - Would require custom tooling
- **Why rejected:** Claude Code uses Markdown natively; JSON/YAML doesn't support rich content well

### Alternative 2: Python/JavaScript Scripts
- **Pros:**
  - Full programming capabilities
  - Type checking and validation
  - Could include logic and helpers
- **Cons:**
  - Claude Code doesn't execute scripts
  - More complex development process
  - Requires runtime environment
  - Higher barrier to contribution
- **Why rejected:** Claude Code skills are prompt-based, not executable code

### Alternative 3: Custom DSL (Domain-Specific Language)
- **Pros:**
  - Tailored exactly to our needs
  - Could enforce structure
  - Potential for advanced features
- **Cons:**
  - Significant development effort
  - Learning curve for contributors
  - Maintenance burden
  - Tooling development required
- **Why rejected:** Overkill for current needs; Markdown is sufficient and widely understood

## References

- [Claude Code Skill Documentation](https://docs.anthropic.com/claude-code/skills)
- [Markdown Specification](https://commonmark.org/)
- [YAML Frontmatter Convention](https://jekyllrb.com/docs/front-matter/)
- Project README.md
