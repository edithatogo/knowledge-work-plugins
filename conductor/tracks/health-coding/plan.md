# Health Clinical Coding Track Plan

## Phase 1: Clinical Coding Skill
*Dependencies: health-core*
*Estimated: 1-2 sessions*

- [ ] Create `health/skills/clinical-coding/SKILL.md`
  - Acceptance: ICD-10-AM coding guidance
  - Acceptance: Classification system overview
  - Acceptance: Code selection methodology
  - Acceptance: Mapping between systems
  - Acceptance: Common coding errors
  - Acceptance: Documentation requirements
  - Source patterns: `data/data-validation`
  - MCP: ICD-10 Codes connector

## Phase 2: Validate Coding Command
*Dependencies: Phase 1*
*Estimated: 0.5 sessions*

- [ ] Create `health/commands/validate-coding.md`
  - Acceptance: Code validation workflow
  - Acceptance: Generates validation report

**Checkpoint:** `conductor(checkpoint): Health clinical coding workflow complete`
