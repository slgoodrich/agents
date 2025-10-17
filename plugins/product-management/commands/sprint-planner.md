# Sprint Planner

Plan agile sprints with capacity, story selection, and goal setting.

## Usage

```
/pm:sprint-plan [sprint number or name] [optional: team capacity]
```

## What This Command Does

1. Facilitates sprint planning process
2. Calculates team capacity
3. Selects stories based on priority and capacity
4. Defines sprint goal
5. Identifies risks and dependencies
6. Creates sprint commitment

## Instructions

1. **Gather Sprint Context**:
   - Sprint duration (typically 2 weeks)
   - Team composition and roles
   - Individual capacity (PTO, meetings, etc.)
   - Historical velocity
   - Sprint goal or theme

2. **Calculate Capacity**:
   - Available person-days per team member
   - Subtract PTO, holidays, meetings
   - Convert to story points based on velocity
   - Build capacity buffer (10-20%)

3. **Select Stories**:
   - Start with highest priority
   - Consider dependencies
   - Mix of features, bugs, tech debt
   - Ensure stories meet Definition of Ready
   - Fit within capacity

4. **Define Sprint Goal**:
   - One clear objective
   - Ties to product strategy/OKR
   - Achievable within sprint
   - Inspires the team

5. **Plan Tasks**:
   - Break stories into tasks
   - Estimate hours
   - Assign owners
   - Identify dependencies

## Template

```markdown
## Sprint [Number] Planning

**Sprint Goal**: [One sentence - what are we achieving?]
**Sprint Duration**: [Start Date] - [End Date]
**Team**: [Team name]

---

### Team Capacity

| Team Member | Role | Total Days | PTO | Meetings | Available | Capacity (pts) |
|-------------|------|------------|-----|----------|-----------|----------------|
| Alice | Senior Dev | 10 | 0 | 2 | 8 | 8 |
| Bob | Mid Dev | 10 | 2 | 2 | 6 | 6 |
| Carol | Junior Dev | 10 | 0 | 2 | 8 | 5 |
| Dave | Designer | 10 | 0 | 3 | 7 | - |

**Total Capacity**: 19 story points
**Velocity (last 3 sprints)**: 18, 20, 17 (avg: 18)
**Target Commitment**: 17-19 points (95-105% of velocity)

---

### Sprint Backlog

#### Theme 1: User Authentication (12 points)

**Story 1**: OAuth2 Login Integration - 8 points
- **Owner**: Alice
- **Tasks**:
  - [ ] Google OAuth setup (4h)
  - [ ] GitHub OAuth setup (4h)
  - [ ] Callback handling (8h)
  - [ ] Error states (4h)
- **Dependencies**: OAuth apps created in Google/GitHub console
- **Risk**: OAuth provider downtime

**Story 2**: Password Reset Flow - 4 points
- **Owner**: Carol
- **Tasks**:
  - [ ] Email template (2h)
  - [ ] Reset token generation (4h)
  - [ ] Reset form UI (4h)
  - [ ] Security testing (2h)

---

#### Theme 2: Dashboard MVP (6 points)

**Story 3**: Dashboard Layout - 3 points
- **Owner**: Bob
- **Design**: Dave (2 days)
- **Tasks**:
  - [ ] Grid system (4h)
  - [ ] Responsive breakpoints (4h)
  - [ ] Widget containers (4h)

**Story 4**: Metrics Widget - 3 points
- **Owner**: Bob
- **Tasks**:
  - [ ] API integration (4h)
  - [ ] Data visualization (6h)
  - [ ] Real-time updates (2h)

---

### Total Commitment

**Story Points**: 18 (within capacity of 19)
**Distribution**:
- New features: 14 points (78%)
- Bug fixes: 0 points
- Tech debt: 4 points (22%)

---

### Sprint Goal

**Primary**: Ship working authentication so beta users can register and log in

**Success Criteria**:
- [ ] Users can sign up with email/Google/GitHub
- [ ] Password reset flow works end-to-end
- [ ] Zero critical security issues
- [ ] All code reviewed and merged to main

**Stretch Goal** (if ahead):
- Session management improvements
- Remember me functionality

---

### Dependencies & Risks

**External Dependencies**:
- [ ] OAuth apps created - Alice (by Monday)
- [ ] Email service configured - DevOps (by Tuesday)
- [ ] Design mockups ready - Dave (by Wednesday)

**Risks**:
| Risk | Impact | Mitigation |
|------|--------|------------|
| Bob's PTO late in sprint | Medium | Front-load his work, Carol backup |
| OAuth complexity underestimated | High | Daily check-ins, spike if needed |
| Email deliverability issues | Low | Use reliable service, test early |

---

### Sprint Ceremonies

**Daily Standup**: 9:30 AM daily (15 min max)
- What shipped yesterday
- What's shipping today
- Blockers

**Mid-Sprint Check-in**: Thursday (30 min)
- Progress review
- Adjust if needed

**Sprint Review**: Last day (60 min)
- Demo to stakeholders
- Gather feedback

**Retrospective**: Last day (45 min)
- What went well
- What to improve
- Action items

---

### Definition of Done

Before marking story as done:
- [ ] Code reviewed by 1+ team member
- [ ] Unit tests written (>80% coverage)
- [ ] Integration tests pass
- [ ] Deployed to staging
- [ ] PM sign-off on functionality
- [ ] Documentation updated
- [ ] No new critical bugs

---

### Sprint Board

**Columns**: To Do → In Progress → Code Review → Testing → Done

**WIP Limits**:
- In Progress: 3 items max
- Code Review: 2 items max
```

## Example

**Input**: "Plan sprint 47 for 5-person team, velocity 32"

**Output**: Complete sprint plan with:
- Calculated capacity per person
- 32 points of stories selected
- Clear sprint goal
- Task breakdown
- Risk assessment
- Ceremony schedule

## Model

Use: claude-sonnet-4-5

## Related

- `/pm:backlog-groomer` - Prepare backlog for sprint
- `/pm:user-stories` - Generate stories
- `/pm:retrospective` - Sprint retro
