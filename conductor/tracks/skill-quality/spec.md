# Skill Quality Improvement Track Specification

## Overview

Systematically improve existing skills across all plugins to ensure consistency, depth, and practical utility. This track establishes quality standards and implements them across the 50+ existing skills.

## Problems Identified

### 1. Inconsistent Structure
- Some skills have explicit "Triggers" sections, others don't
- Varying levels of detail (90 lines to 867 lines)
- No standard section ordering

### 2. Missing Key Sections
- No "Anti-Patterns" / "Common Mistakes" in most skills
- No "Related Skills" cross-references
- No "Success Criteria" or quality gates
- No tool integration hints

### 3. Depth Imbalance
- Short skills (< 120 lines) lack sufficient guidance
- Very long skills need quick-start options
- Technical skills missing practical examples

### 4. Discoverability
- Skills operate in isolation
- No cross-plugin references
- Hard to find related capabilities

## Proposed Standards

### Standard Skill Structure

```markdown
---
name: skill-name
description: One-line description. Use when [trigger condition 1], [trigger condition 2].
---

# Skill Name

Brief introduction (1-2 sentences).

## When to Use This Skill

Invoke when:
- User mentions X
- User asks about Y
- Context indicates Z

## Quick Reference

[For simple cases - condensed guidance in 5-10 bullet points]

## Detailed Guidance

[Main content - organized with clear headers]

### Step-by-Step Process

1. ...
2. ...

## Common Mistakes

| Mistake | Why It's Wrong | Instead |
|---------|----------------|---------|
| ... | ... | ... |

## Tool Requirements

- `~~category` - Purpose
- `~~category` - Purpose

## Success Indicators

You've applied this skill well when:
- [ ] Criterion 1
- [ ] Criterion 2

## Related Skills

- `~~plugin/skill-name` - Brief description of relationship
- `~~plugin/skill-name` - Brief description of relationship
```

### Section Guidelines

| Section | Required | Min Lines | Purpose |
|---------|----------|-----------|---------|
| Frontmatter | ✓ | 3 | Name, description with triggers |
| When to Use | ✓ | 5 | Explicit invocation conditions |
| Quick Reference | For complex skills | 10 | Fast path for simple cases |
| Detailed Guidance | ✓ | 50+ | Main instructional content |
| Common Mistakes | ✓ | 10 | Anti-patterns and corrections |
| Tool Requirements | ✓ | 5 | MCP connector dependencies |
| Success Indicators | ✓ | 5 | Quality gate checklist |
| Related Skills | ✓ | 3 | Cross-references |

### Quality Gates

Before any skill is considered complete:

- [ ] Minimum 150 lines total
- [ ] All required sections present
- [ ] At least 3 "Common Mistakes" documented
- [ ] At least 2 "Related Skills" referenced
- [ ] At least 3 "Success Indicators" defined
- [ ] Frontmatter description includes trigger conditions
- [ ] Practical examples included (not just theory)
- [ ] No placeholder content (e.g., "TODO", "TBD")

## Additional Improvements

### 5. Accessibility & Internationalization
- Use plain language (avoid jargon without definition)
- Consider non-native English speakers
- Define acronyms on first use
- Use consistent terminology across skills

### 6. Versioning & Changelog
Add to each skill:
```markdown
## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.1.0 | 2026-02-11 | Added anti-patterns section |
```

### 7. Example Gallery
For visual/creative skills, include:
```markdown
## Examples

### Example 1: [Scenario Name]
**Context:** ...
**Input:** ...
**Output:** ...
**Why it works:** ...
```

### 8. Error Handling Guidance
```markdown
## Troubleshooting

| Error | Cause | Solution |
|-------|-------|----------|
| ... | ... | ... |
```

### 9. Performance Considerations
For skills involving large data or complex operations:
```markdown
## Performance Tips

- For datasets > 10K rows, use X approach
- Cache Y for repeated operations
- Avoid Z pattern with large files
```

### 10. Security & Privacy Notes
For skills handling sensitive data:
```markdown
## Security Considerations

- Never log PII
- Sanitize inputs before processing
- Use environment variables for credentials
- Data retention: delete after X days
```

### 11. Skill Composition
Enable skills to build on each other:
```markdown
## Workflow Integration

This skill is often used as part of:

1. **[Workflow Name]**
   - Start with: `~~plugin/skill-a`
   - Then: `~~plugin/skill-b` (this skill)
   - End with: `~~plugin/skill-c`
```

### 12. Confidence Levels
Help users know when to trust the output:
```markdown
## Confidence Indicators

| Scenario | Confidence | Action |
|----------|------------|--------|
| Standard inputs | High | Use directly |
| Edge case X | Medium | Review before sharing |
| Novel situation | Low | Flag for human review |
```

### 13. Input/Output Contracts
```markdown
## Expected Inputs

| Input | Type | Required | Description |
|-------|------|----------|-------------|
| data | file | ✓ | CSV, JSON, or Excel |
| config | object | | Override defaults |

## Outputs

| Output | Type | Description |
|--------|------|-------------|
| report | markdown | Analysis summary |
| data | file | Cleaned dataset |
```

### 14. Testing & Validation
Add skill self-tests where applicable:
```markdown
## Self-Validation

Before delivering output, verify:
1. [Specific check 1]
2. [Specific check 2]

If validation fails: [Recovery steps]
```

## Plugin-Specific Improvements

### Productivity Plugin
- `task-management`: Add prioritization matrix, Eisenhower framework
- `memory-management`: Add memory decay curves, retention strategies

### Data Plugin
- `sql-queries`: Add query performance optimization section
- `data-validation`: Add statistical significance checks
- All skills: Add sample datasets for practice

### Customer Support Plugin
- `ticket-triage`: Add sentiment analysis indicators
- `response-drafting`: Add tone calibration for different cultures
- `escalation`: Add executive communication templates

### Legal Plugin
- `compliance`: Add jurisdiction-specific quick reference
- `contract-review`: Add red flag checklist by contract type
- All skills: Add regulatory update monitoring guidance

### Finance Plugin
- `reconciliation`: Add common discrepancy patterns
- `audit-support`: Add audit trail documentation standards
- All skills: Add SOX compliance considerations

### Sales Plugin
- `create-an-asset`: Add quick-start path for simple assets
- `competitive-intelligence`: Add source credibility assessment
- All skills: Add CRM integration patterns

### Marketing Plugin
- `content-creation`: Add brand voice consistency checklist
- `campaign-planning`: Add channel-specific considerations
- All skills: Add A/B testing guidance

### Bio-Research Plugin
- All skills: Add reproducibility checklist
- All skills: Add data provenance tracking
- `scvi-tools`: Add computational requirements section

### Enterprise Search Plugin
- `search-strategy`: Add query expansion techniques
- `knowledge-synthesis`: Add source quality assessment

## Deliverables

### Phase 1: Standards & Templates
- Skill template with all required sections
- Style guide for consistent voice/tone
- Quality checklist for reviewers
- Automated validation script

### Phase 2: High-Impact Skills
- Update top 20 most-used skills to new standard
- Focus on cross-plugin skills first
- Add comprehensive cross-references

### Phase 3: Complete Coverage
- Update remaining 30+ skills
- Create skill composition documentation
- Build skill relationship graph

## Success Metrics

| Metric | Current | Target |
|--------|---------|--------|
| Skills with "When to Use" section | ~30% | 100% |
| Skills with "Common Mistakes" | ~15% | 100% |
| Skills with "Related Skills" | ~5% | 100% |
| Average skill length | ~200 lines | 200-400 lines |
| Cross-skill references | ~10 total | 150+ total |
| Skills < 150 lines | 15 | 0 |

## Dependencies

None - this track improves existing content without blocking other work.

## Risks

- **Scope creep**: Limit to documented improvements, avoid feature additions
- **Breaking changes**: Preserve existing skill behavior, only add sections
- **Inconsistency**: Use templates and automated checks to enforce standards
