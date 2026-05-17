# Installation Guide

This guide will help you install the Solution Architect Toolkit skills for Claude Code.

## Prerequisites

- Claude Code installed and configured
- Git (optional, for cloning the repository)
- Text editor (for viewing/editing skills)

## Installation Methods

### Method 1: Direct Installation (Recommended)

This method copies the skills directly to your Claude Code skills directory.

```bash
# Clone the repository
git clone <repository-url> solution-architect-toolkit
cd solution-architect-toolkit

# Copy Phase 1 skills to Claude Code
cp skills/phase-1/*.md ~/.claude/skills/

# Verify installation
ls ~/.claude/skills/
```

**Result:** You should see:
- `adr.md`
- `solution-doc.md`
- `tech-stack.md`
- `design-review.md`

### Method 2: Symlink Installation (For Developers)

This method creates symbolic links, so updates to the repository automatically reflect in Claude Code.

```bash
# Clone the repository
git clone <repository-url> solution-architect-toolkit
cd solution-architect-toolkit

# Create symlinks for Phase 1 skills
ln -s "$(pwd)/skills/phase-1/adr.md" ~/.claude/skills/adr.md
ln -s "$(pwd)/skills/phase-1/solution-doc.md" ~/.claude/skills/solution-doc.md
ln -s "$(pwd)/skills/phase-1/tech-stack.md" ~/.claude/skills/tech-stack.md
ln -s "$(pwd)/skills/phase-1/design-review.md" ~/.claude/skills/design-review.md

# Verify installation
ls -la ~/.claude/skills/
```

**Advantage:** Edit skills in the repository and changes are immediately available in Claude Code.

### Method 3: Windows Installation

For Windows users without symlink support:

```powershell
# Clone the repository
git clone <repository-url> solution-architect-toolkit
cd solution-architect-toolkit

# Copy Phase 1 skills to Claude Code
Copy-Item -Path "skills\phase-1\*.md" -Destination "$env:USERPROFILE\.claude\skills\"

# Verify installation
dir "$env:USERPROFILE\.claude\skills\"
```

## Verification

1. **Open Claude Code**
2. **Type `/` in the chat**
3. **Look for these skills:**
   - `/adr` - Architecture Decision Records
   - `/solution-doc` - Solution Documentation Generator
   - `/tech-stack` - Technology Stack Advisor
   - `/design-review` - Design Review

If you see these skills, installation was successful!

## Testing Your Installation

Try creating your first ADR:

```
/adr create Use PostgreSQL for primary database
```

Claude should start asking you questions to fill in the ADR template.

## Directory Structure After Installation

```
~/.claude/
  skills/
    adr.md                  # ✅ Installed
    solution-doc.md         # ✅ Installed
    tech-stack.md           # ✅ Installed
    design-review.md        # ✅ Installed
    [other existing skills]
```

## Updating Skills

### For Direct Installation

```bash
cd solution-architect-toolkit
git pull origin main
cp skills/phase-1/*.md ~/.claude/skills/
```

### For Symlink Installation

```bash
cd solution-architect-toolkit
git pull origin main
# Changes are automatically available!
```

## Uninstallation

To remove the skills:

```bash
# Remove Phase 1 skills
rm ~/.claude/skills/adr.md
rm ~/.claude/skills/solution-doc.md
rm ~/.claude/skills/tech-stack.md
rm ~/.claude/skills/design-review.md
```

Or on Windows:

```powershell
Remove-Item "$env:USERPROFILE\.claude\skills\adr.md"
Remove-Item "$env:USERPROFILE\.claude\skills\solution-doc.md"
Remove-Item "$env:USERPROFILE\.claude\skills\tech-stack.md"
Remove-Item "$env:USERPROFILE\.claude\skills\design-review.md"
```

## Troubleshooting

### Skills Don't Appear in Claude Code

1. **Check the skills directory exists:**
   ```bash
   ls ~/.claude/skills/
   ```
   If it doesn't exist, create it:
   ```bash
   mkdir -p ~/.claude/skills/
   ```

2. **Verify file permissions:**
   ```bash
   ls -la ~/.claude/skills/*.md
   ```
   Files should be readable (at least `r--` permissions).

3. **Restart Claude Code**
   Sometimes Claude Code needs a restart to pick up new skills.

### Skill Command Not Working

1. **Check the skill file has proper frontmatter:**
   ```bash
   head -5 ~/.claude/skills/adr.md
   ```
   Should show YAML frontmatter with `---` delimiters.

2. **Check for syntax errors:**
   Open the skill file and look for any formatting issues.

### Windows Symlink Issues

If symlinks don't work on Windows:
- Use Method 3 (direct copy) instead
- Or enable Developer Mode in Windows Settings to allow symlinks

## Advanced Configuration

### Custom Skill Directory

If you use a different skills directory, adjust the paths accordingly:

```bash
# If your skills are in ~/my-skills/
cp skills/phase-1/*.md ~/my-skills/
```

### Selective Installation

Install only the skills you need:

```bash
# Install only ADR skill
cp skills/phase-1/adr.md ~/.claude/skills/

# Install only documentation skills
cp skills/phase-1/solution-doc.md ~/.claude/skills/
```

## Next Steps

1. **Read the documentation:** Check `docs/` for usage guides
2. **View examples:** See `examples/` for sample outputs
3. **Customize templates:** Edit `templates/` to match your standards
4. **Contribute:** Submit PRs for improvements or new skills!

## Support

For issues or questions:
- Check the [README.md](../README.md)
- Review [CLAUDE.md](../CLAUDE.md) for development details
- Open an issue on GitHub (if public repository)

## What's Next?

- **Phase 2 Skills** (Coming Soon): Tech Debt Analyzer, System Mapper, Migration Planner, API Designer
- **Phase 3 Skills** (Planned): Cloud Architect, Compliance Checker, Capacity Planner, Risk Assessor

Check the repository regularly for updates!
