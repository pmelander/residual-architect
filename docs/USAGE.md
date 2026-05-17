# Usage Guide

This guide provides detailed examples and best practices for using the Solution Architect Toolkit skills.

## Table of Contents

1. [Architecture Decision Records](#architecture-decision-records)
2. [Solution Documentation](#solution-documentation)
3. [Technology Stack Advisor](#technology-stack-advisor)
4. [Design Review](#design-review)
5. [Workflow Examples](#workflow-examples)

---

## Architecture Decision Records

### Creating Your First ADR

**Scenario:** You need to choose a database for your new application.

```
User: /adr create Choose PostgreSQL for primary database

Claude will ask:
- What is the current approach (if migrating)?
- What problems are you solving?
- What are your constraints (scale, budget, team)?
- What alternatives did you consider?
- Who are the decision makers?

After answering, Claude generates:
docs/adr/ADR-001-choose-postgresql-for-primary-database.md
```

### Listing ADRs

```
User: /adr list

Claude shows:
┌────────┬───────────────────────────────┬──────────┬────────────┐
│ Number │ Title                         │ Status   │ Date       │
├────────┼───────────────────────────────┼──────────┼────────────┤
│ ADR-001│ Choose PostgreSQL for DB      │ Accepted │ 2026-05-17 │
│ ADR-002│ Use React for Frontend        │ Proposed │ 2026-05-17 │
└────────┴───────────────────────────────┴──────────┴────────────┘
```

### Updating ADR Status

```
User: /adr update 2

Claude will:
1. Read ADR-002
2. Ask what changes are needed
3. Update the ADR (e.g., change status to "Accepted")
```

### Best Practices for ADRs

1. **Create ADRs Early:** Document decisions while context is fresh
2. **Be Specific:** "Use PostgreSQL 15 with RDS" vs "Use a database"
3. **Update Status:** Mark as Deprecated or Superseded when things change
4. **Link Related ADRs:** Reference earlier decisions
5. **Include Trade-offs:** Be honest about downsides

### When to Create an ADR

✅ **Do create ADRs for:**
- Technology selections (database, framework, language)
- Architecture patterns (microservices, event-driven)
- Major design decisions (API style, data model)
- Infrastructure choices (cloud provider, CI/CD)
- Security approaches (authentication, encryption)

❌ **Don't create ADRs for:**
- Minor implementation details
- Easily reversible choices
- Team preferences without technical impact
- Temporary workarounds

---

## Solution Documentation

### Generating High-Level Design

**Scenario:** You need to document a new microservices system.

```
User: /solution-doc hld

Claude will:
1. Analyze your codebase (if available)
2. Ask about:
   - System purpose and scope
   - Key components
   - Technology stack
   - Non-functional requirements
   - Integration points
3. Generate comprehensive HLD
4. Save to docs/architecture/HLD.md
```

### Generating Low-Level Design

**For specific component:**
```
User: /solution-doc lld payment-service

Claude will:
1. Focus on payment-service details
2. Generate API specs, data models, logic
3. Save to docs/architecture/LLD-payment-service.md
```

**For entire system:**
```
User: /solution-doc lld

Claude generates LLD for all major components.
```

### Creating Deployment Guide

```
User: /solution-doc deployment

Claude will:
1. Ask about infrastructure (AWS, Azure, GCP, on-prem)
2. Document prerequisites
3. Create step-by-step deployment process
4. Include configuration and verification
5. Save to docs/deployment/DEPLOYMENT.md
```

### Generating Operations Runbook

```
User: /solution-doc runbook

Claude will:
1. Document common operations
2. Create troubleshooting guides
3. Include monitoring and alerts
4. Add backup/recovery procedures
5. Save to docs/operations/RUNBOOK.md
```

### Complete Documentation Set

```
User: /solution-doc complete

Claude generates:
- High-Level Design
- Low-Level Design (for each component)
- Deployment Guide
- Operations Runbook

Perfect for new projects or comprehensive documentation updates!
```

### Documentation Best Practices

1. **Keep Updated:** Documentation should match reality
2. **Use Diagrams:** Visual representations are crucial
3. **Target Audience:** Adjust detail for readers (executives vs developers)
4. **Link Documents:** Reference ADRs and related docs
5. **Version Control:** Track changes in Git
6. **Review Regularly:** Schedule quarterly documentation reviews

---

## Technology Stack Advisor

### Recommending a Complete Stack

**Scenario:** Starting a new project and need technology recommendations.

```
User: /tech-stack recommend

Claude will ask:
- What are you building?
- Expected scale and performance needs?
- Team size and expertise?
- Timeline and budget?
- Compliance requirements?

Then provides:
- Frontend recommendation
- Backend recommendation
- Database recommendation
- Infrastructure recommendation
- Complete justification with alternatives
```

### Comparing Technologies

**Scenario:** Deciding between React and Vue for frontend.

```
User: /tech-stack compare React vs Vue

Claude generates:
┌─────────────────────┬──────────┬──────────┐
│ Criteria            │ React    │ Vue      │
├─────────────────────┼──────────┼──────────┤
│ Learning Curve      │ ⭐⭐⭐    │ ⭐⭐⭐⭐⭐ │
│ Ecosystem           │ ⭐⭐⭐⭐⭐ │ ⭐⭐⭐⭐  │
│ Performance         │ ⭐⭐⭐⭐  │ ⭐⭐⭐⭐  │
│ Job Market          │ ⭐⭐⭐⭐⭐ │ ⭐⭐⭐    │
└─────────────────────┴──────────┴──────────┘

Recommendation: [Based on your context]
```

### Evaluating a Specific Technology

**Scenario:** Considering Kubernetes but unsure if it's right for you.

```
User: /tech-stack evaluate Kubernetes

Claude will:
1. Ask about your scale and operations maturity
2. Analyze if Kubernetes is appropriate
3. List pros and cons for YOUR context
4. Suggest alternatives if not a fit
5. Provide implementation guidance if it is a fit
```

### Planning a Technology Migration

**Scenario:** Migrating from monolith to microservices.

```
User: /tech-stack migrate from Monolith to Microservices

Claude will:
1. Analyze migration complexity
2. Identify benefits and risks
3. Suggest phased migration strategy
4. Estimate timeline and effort
5. Provide cost-benefit analysis
6. Recommend whether to proceed
```

### Technology Selection Best Practices

1. **Context Matters:** No universal "best" technology
2. **Team First:** Consider team expertise heavily
3. **Start Simple:** Don't over-engineer early
4. **Prove It:** Do POCs for uncertain choices
5. **Consider Total Cost:** Include learning, operations, migration
6. **Plan Exit:** Know how to migrate away if needed
7. **Document Decision:** Create an ADR!

---

## Design Review

### Comprehensive Architecture Review

**Scenario:** Complete review before production launch.

```
User: /design-review complete

Claude will:
1. Analyze your codebase and architecture
2. Evaluate across 8 dimensions:
   - Architecture principles
   - Scalability
   - Performance
   - Security
   - Maintainability
   - Testability
   - Observability
   - Operational readiness
3. Generate scorecard with ratings
4. Identify critical issues, moderate issues, and improvements
5. Provide prioritized recommendations
6. Save to docs/reviews/architecture-review-YYYY-MM-DD.md
```

### Focused Reviews

**API Design Review:**
```
User: /design-review api

Claude focuses on:
- REST/GraphQL best practices
- Endpoint design
- Error handling
- Versioning strategy
- Documentation quality
```

**Security Review:**
```
User: /design-review security

Claude focuses on:
- Authentication and authorization
- Data protection
- OWASP Top 10
- Compliance requirements
- Secrets management
```

**Performance Review:**
```
User: /design-review performance

Claude focuses on:
- Bottleneck identification
- Caching strategy
- Database optimization
- Scalability limits
```

**Data Architecture Review:**
```
User: /design-review data

Claude focuses on:
- Database design
- Data consistency
- Schema design
- Query optimization
```

### Understanding the Scorecard

```
┌────────────────────────┬───────┬────────┐
│ Dimension              │ Score │ Status │
├────────────────────────┼───────┼────────┤
│ Architecture Principles│ 8/10  │ 🟢     │
│ Scalability            │ 6/10  │ 🟡     │
│ Performance            │ 4/10  │ 🔴     │
│ Security               │ 9/10  │ 🟢     │
└────────────────────────┴───────┴────────┘

🟢 Strong (8-10): Meets or exceeds standards
🟡 Adequate (5-7): Acceptable but has issues
🔴 Needs Improvement (0-4): Must be addressed
```

### Acting on Review Findings

**Critical Issues (🔴):**
- Must fix before production
- Schedule immediate work
- Consider delaying launch if severe

**Moderate Issues (🟡):**
- Fix in next sprint
- Document as technical debt
- Create tracking tickets

**Improvements (🔵):**
- Add to backlog
- Consider for future iterations
- Evaluate ROI

### Design Review Best Practices

1. **Review Early:** Catch issues before implementation
2. **Review Often:** Periodic reviews catch drift
3. **Be Honest:** Document real issues, not what sounds good
4. **Actionable Feedback:** Specific, actionable recommendations
5. **Follow Up:** Track whether issues get fixed
6. **Learn:** Review findings inform future designs

---

## Workflow Examples

### Example 1: Starting a New Project

**Step 1:** Get technology recommendations
```
/tech-stack recommend
```

**Step 2:** Document major technology decisions
```
/adr create Use Node.js for backend services
/adr create Use PostgreSQL for primary database
/adr create Use React for frontend
```

**Step 3:** Generate initial architecture documentation
```
/solution-doc hld
```

**Step 4:** Review the initial design
```
/design-review architecture
```

**Step 5:** Address issues and create deployment guide
```
/solution-doc deployment
```

### Example 2: Architecture Review Cycle

**Pre-Production Review:**
```
/design-review complete
```

**Address Critical Issues:**
```
[Fix identified issues]
```

**Re-review Changed Areas:**
```
/design-review security  # If security was flagged
/design-review performance  # If performance was flagged
```

**Generate Final Documentation:**
```
/solution-doc complete
```

### Example 3: Technology Migration

**Step 1:** Analyze migration
```
/tech-stack migrate from MySQL to PostgreSQL
```

**Step 2:** Document decision
```
/adr create Migrate from MySQL to PostgreSQL
```

**Step 3:** Create migration plan
```
/solution-doc deployment  # Include migration steps
```

**Step 4:** Review migration approach
```
/design-review data  # Review new data architecture
```

### Example 4: Continuous Architecture

**Monthly Architecture Review:**
```
/design-review complete
```

**Quarterly Technology Evaluation:**
```
/tech-stack evaluate [current technologies]
```

**Ongoing Documentation:**
```
/adr update [as decisions change]
/solution-doc update hld  # Keep HLD current
```

---

## Tips for Maximum Effectiveness

### For Solution Architects

1. **Document as You Go:** Don't wait until the end
2. **Use ADRs for Alignment:** Share with team for buy-in
3. **Review Regularly:** Catch issues early
4. **Keep Documentation Current:** Stale docs are worse than no docs
5. **Link Everything:** ADRs → HLD → LLD → Code

### For Teams

1. **Make ADRs Collaborative:** Discuss before finalizing
2. **Use Reviews as Learning:** Share findings with team
3. **Automate Where Possible:** Integrate into CI/CD
4. **Review in Phases:** Don't wait for "done" to review
5. **Track Technical Debt:** Use reviews to identify and track

### For Organizations

1. **Standardize Templates:** Customize templates for your org
2. **Create ADR Repository:** Central place for all decisions
3. **Regular Architecture Reviews:** Make it part of process
4. **Share Knowledge:** Use generated docs for onboarding
5. **Measure Quality:** Track review scores over time

---

## Common Questions

**Q: How long should an ADR be?**
A: 1-2 pages typically. Enough detail to understand the decision, not a novel.

**Q: Should I create ADRs for small decisions?**
A: No, only for significant decisions with lasting impact.

**Q: How often should I do design reviews?**
A: Before major milestones, quarterly for ongoing projects.

**Q: Can I customize the templates?**
A: Yes! Edit templates in `templates/` directory to match your needs.

**Q: What if the review finds critical issues?**
A: Address them before production. It's better to delay than ship with known critical issues.

**Q: How do I keep documentation current?**
A: Use `/solution-doc update` command regularly, schedule quarterly reviews.

---

## Next Steps

- Install Phase 2 skills (coming soon) for deeper analysis
- Customize templates for your organization
- Integrate into your development workflow
- Share feedback and contribute improvements!

For more information, see:
- [Installation Guide](INSTALLATION.md)
- [Examples](../examples/)
- [Templates](../templates/)
