# Health Complaints Track Plan

## Phase 1: Complaints Skill
*Dependencies: health-core*
*Estimated: 1-2 sessions*

- [ ] Create `health/skills/complaints-management/SKILL.md`
  - Acceptance: Distinguishes clinician vs service complaints
  - Acceptance: Severity framework adapted for healthcare (P1-P4 with patient safety context)
  - Acceptance: Investigation workflow with timelines
  - Acceptance: Escalation triggers to legal/regulatory
  - Acceptance: Resolution documentation requirements
  - Source patterns: `customer-support/ticket-triage`, `customer-support/escalation`

## Phase 2: Complaints Command
*Dependencies: Phase 1*
*Estimated: 1 session*

- [ ] Create `health/commands/submit-complaint.md`
  - Acceptance: Collects complaint type
  - Acceptance: Captures patient/staff safety concerns
  - Acceptance: Routes to appropriate skill path
  - Acceptance: Generates intake documentation

**Checkpoint:** `conductor(checkpoint): Health complaints workflow complete`

## Notes

- May need to coordinate with `health-incidents` track - some complaints may trigger incident reports
- Regulatory reporting requirements vary by jurisdiction - parameterize
