# Sprint Planner

Plan agile sprints with realistic capacity, strategic story selection, inspiring goals, and clear success criteria that balance delivery with team health.

## Usage

```
/pm:sprint-plan [sprint number or name] [optional: team capacity]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. **Facilitates sprint planning** with structured agenda and capacity-driven story selection (saves 1-2 hours per planning session)
2. **Calculates realistic capacity** accounting for PTO, meetings, context switching, and team-specific factors
3. **Selects stories strategically** based on priority, dependencies, and capacity while balancing feature work with tech debt
4. **Defines inspiring sprint goals** that connect team work to product strategy and user outcomes
5. **Identifies risks and dependencies** proactively to prevent mid-sprint blockers and surprises
6. **Creates sustainable commitments** that teams can reliably achieve (avoiding burnout from over-commitment)

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Sprint Context**:
- What sprint number is this? (Sprint 47, Sprint 2025-03, etc.)
- What are the sprint dates? (start date, end date, duration in days)
- What's the sprint duration? (1 week, 2 weeks - most teams use 2 weeks)
- Is this a regular sprint or special? (holiday sprint, hackathon, planning sprint)

**Team Composition**:
- Who's on the team? (names, roles: engineers, designers, QA, PM)
- What's each person's role and seniority? (senior, mid, junior - affects capacity)
- Is anyone new to the team? (new hires have lower initial capacity)
- Any planned PTO or absences? (vacations, conferences, appointments)

**Capacity Factors**:
- What's the team's historical velocity? (average story points over last 3-5 sprints)
- Was last sprint typical? (did anything unusual happen that affected velocity)
- What's the meeting load? (standups, planning, retro, review, other meetings)
- Any large interruptions planned? (company all-hands, training, interviews)
- What percentage of time goes to unplanned work? (bugs, support, production issues)

**Backlog State**:
- Is the backlog groomed and ready? (stories have acceptance criteria, estimates)
- What's the top priority? (strategic initiative, OKR, customer commitment)
- Are there any must-have commitments? (demos, deadlines, dependencies)
- What's the mix of work? (features, bugs, tech debt, research)

**Sprint Goal Direction**:
- What's the strategic theme for this sprint? (e.g., "Enterprise readiness", "Mobile experience")
- Are there any OKRs or goals this sprint should advance?
- Any customer demos or releases planned?
- What did the team accomplish last sprint? (for continuity)

**Constraints**:
- Any external dependencies? (other teams, vendors, approvals needed)
- Any technical dependencies? (platform work, infrastructure, migrations)
- Any holidays or company events during sprint? (affects capacity)

### 2. Calculate Team Capacity

**Formula**:
```
Individual Capacity (points) = (Available Days × Focus Factor × Role Multiplier) × Team Velocity / Total Team Days
```

**Step-by-Step Capacity Calculation**:

1. **Calculate Available Days**:
   - Start with sprint duration days (typically 10 days for 2-week sprint)
   - Subtract PTO days
   - Subtract holidays/company events
   - Subtract partial days for appointments/interviews

2. **Apply Focus Factor** (70-85%):
   - 85%: Senior, experienced, focused role
   - 75%: Mid-level, typical distractions
   - 70%: Junior, learning mode, or high meeting load
   - 60%: New hire (first sprint)
   - 50%: On-call rotation sprint

3. **Apply Role Multiplier**:
   - Engineer: 1.0x (baseline)
   - Designer: 0.8x (more collaboration overhead)
   - QA: 1.0x
   - PM: Not counted in engineering capacity

4. **Account for Unplanned Work**:
   - Reduce total capacity by 10-20% for bugs/support
   - Higher for customer-facing products
   - Lower for internal tools

**Example Calculation**:
```
Senior Engineer:
- 10 sprint days - 2 PTO = 8 days available
- 8 days × 0.85 focus factor = 6.8 effective days
- If team velocity is 30 pts and total team has 40 effective days
- This person's capacity = 6.8 / 40 × 30 = 5.1 points

Round to: 5 points
```

### 3. Select Stories Strategically

**Prioritization Framework**:

1. **Must-Have** (30-40% of capacity):
   - Customer commitments with deadlines
   - Critical bugs blocking users
   - Dependencies for other teams
   - Regulatory/compliance requirements

2. **Should-Have** (40-50% of capacity):
   - High-priority features from roadmap
   - Important user requests
   - Strategic OKR-aligned work
   - Moderate bugs affecting UX

3. **Nice-to-Have** (10-20% of capacity):
   - Tech debt reduction
   - Developer experience improvements
   - Small UX enhancements
   - Exploratory/learning tasks

4. **Stretch Goals** (buffer, not committed):
   - Additional features if ahead of schedule
   - Opportunistic improvements
   - Never committed to stakeholders

**Selection Process**:
1. Start with highest priority stories
2. Check Definition of Ready (story complete, estimated, testable)
3. Verify no blockers or missing dependencies
4. Consider story size vs remaining capacity
5. Balance across themes (don't cluster all work in one area)
6. Include mix of feature work + bugs + tech debt (70/20/10 typical)
7. Stop when 90-95% of capacity is filled (buffer for unknowns)

**Red Flags** (don't pull into sprint):
- Story not estimated or too large (>8 points - needs breakdown)
- Missing acceptance criteria or design
- Blocked by external dependency not yet resolved
- Team lacks required expertise (need spike/pairing)

### 4. Define an Inspiring Sprint Goal

**Good Sprint Goal Characteristics**:
- **Singular**: One clear objective, not a list
- **Outcome-Focused**: User/business value, not tasks
- **Achievable**: Team believes they can do it
- **Inspiring**: Team cares about achieving it
- **Measurable**: Clear success criteria

**Formula**:
```
[Action Verb] + [User/Business Outcome] + [So That Benefit]
```

**Examples**:

❌ **Bad**:
- "Complete stories 1-15"
- "Work on authentication and dashboard"
- "Ship features and fix bugs"

✅ **Good**:
- "Ship OAuth login so beta users can securely access the product"
- "Reduce onboarding drop-off by 50% by simplifying first-time setup"
- "Enable offline mode so mobile users can work without internet"

⭐ **Excellent**:
- "Ship SSO integration so enterprise customers can manage team access centrally, unblocking 5 sales deals"
- "Reduce API latency from 500ms to <100ms so users experience instant interactions"
- "Launch Spanish localization so we can enter Mexican market (target: 10K new users)"

### 5. Identify Dependencies and Risks

**Dependencies to Surface**:
- **Technical**: Platform work, infrastructure, database migrations
- **Cross-Team**: APIs, services, resources from other teams
- **External**: Vendors, partners, legal approvals
- **Design**: Mockups, prototypes, user research needed
- **Product**: Decisions, specs, acceptance criteria

**Risk Assessment**:

For each risk:
1. **What**: Describe the risk
2. **Impact**: High/Medium/Low - what happens if it materializes
3. **Likelihood**: High/Medium/Low - how probable
4. **Mitigation**: What you'll do to reduce/prevent
5. **Owner**: Who's tracking this risk

**Common Sprint Risks**:
- Underestimated complexity (most common)
- Key person unavailable (PTO, sick)
- Scope creep mid-sprint
- External dependency delayed
- Production issues pull team away
- Requirements unclear/changing

### 6. Plan Sprint Ceremonies

**Standard Agile Ceremonies** (2-week sprint):

**Daily Standup** (15 min, every day):
- Time: Same time daily (typically morning)
- Format: Each person shares (1-2 min):
  - What I shipped yesterday
  - What I'm shipping today
  - Any blockers
- Anti-patterns: Status reports, problem-solving (take offline)

**Mid-Sprint Check-In** (30 min, mid-week):
- Review burndown chart
- Are we on track for sprint goal?
- Any risks materializing?
- Adjust if needed

**Sprint Review/Demo** (60 min, last day):
- Demo completed work to stakeholders
- Gather feedback
- Accept/reject stories
- Update product backlog based on learnings

**Sprint Retrospective** (45-60 min, last day):
- What went well? (keep doing)
- What didn't go well? (stop doing)
- What should we try? (start doing)
- Action items with owners
- Review last retro action items

**Sprint Planning** (Next Sprint) (2-4 hours):
- Review last sprint results
- Define new sprint goal
- Calculate capacity
- Select and estimate stories
- Identify dependencies and risks

### 7. Track Progress During Sprint

**Burndown Chart**:
- Plot remaining story points vs days
- Ideal: Straight line from total capacity to zero
- Reality: Will fluctuate
- Warning signs: Flat line (no progress), increasing (scope creep)

**Daily Progress Checks**:
- Are stories moving through the board?
- Any stories stuck >2 days? (needs help)
- Any blockers discovered?
- Sprint goal still achievable?

**Adjustments Mid-Sprint**:
- **Add scope**: Only if ahead + PM approves + team agrees
- **Remove scope**: If behind, descope nice-to-haves first
- **Focus shift**: If blocker discovered, swarm to unblock

## Template

```markdown
# Sprint [Number] Plan

**Team**: [Team name] | **Duration**: [Start - End dates] | **Capacity**: [X] points

---

## Sprint Goal

**Goal**: [One sentence - what we're achieving this sprint]

**Why This Matters**: [How this ties to OKRs/roadmap/strategy]

**Success Criteria**: [How we'll know we succeeded]

---

## Team Capacity

**Team Availability**:
- [Name]: [X] days available ([Y]% - reason if <100%)
- [Name]: [X] days available
- **Total**: [X] person-days

**Velocity**:
- Last 3 sprints: [A], [B], [C] points
- Average: [Avg] points
- **Target for this sprint**: [X] points ([reason if different from avg])

**Capacity Adjustments**:
- Holidays: [-X] points
- Meetings/overhead: [-Y] points
- **Adjusted capacity**: [Z] points

---

## Committed Stories

| Story | Priority | Points | Owner | Notes |
|-------|----------|--------|-------|-------|
| [Story 1] | P0 | 5 | [Name] | [Dependencies/risks] |
| [Story 2] | P0 | 3 | [Name] | |
| [Story 3] | P1 | 2 | [Name] | Nice to have |

**Total Committed**: [X] points
**Stretch Goals** (if capacity allows): [Story Y] ([Z] points)

---

## Sprint Backlog by Theme

**Theme 1: [e.g., User Onboarding]** ([X] points):
- [Story A] - [Points]
- [Story B] - [Points]

**Theme 2: [e.g., Performance]** ([Y] points):
- [Story C] - [Points]

**Tech Debt** ([Z] points):
- [Story D] - [Points]

---

## Dependencies & Risks

**External Dependencies**:
- [ ] [Dependency 1] - Needed by: [Date] - Owner: [Team/Person] - Status: [On track/At risk]
- [ ] [Dependency 2] - Needed by: [Date] - Owner: [Team/Person] - Status: [On track/At risk]

**Risks**:
- 🟡 [Risk 1]: [Description] - Likelihood: [H/M/L] - Mitigation: [Plan]
- 🟡 [Risk 2]: [Description] - Likelihood: [H/M/L] - Mitigation: [Plan]

**Blockers Identified**:
- 🚨 [Blocker 1] - Impact: [What's blocked] - Resolution: [Plan] - By: [Date/Person]

---

## Sprint Schedule

**Key Dates**:
- Sprint start: [Date]
- Mid-sprint check-in: [Date]
- Code freeze: [Date]
- Demo/review: [Date]
- Retrospective: [Date]
- Sprint end: [Date]

**Ceremonies**:
- Daily standup: [Time, Location]
- Backlog refinement: [Day, Time]
- Demo: [Day, Time]
- Retro: [Day, Time]

---

## Definition of Done

Sprint is complete when:
- [ ] All committed stories meet Definition of Done
- [ ] Code reviewed and merged
- [ ] Tests passing (unit, integration, E2E)
- [ ] Deployed to staging and validated
- [ ] Demo prepared
- [ ] Documentation updated
- [ ] Sprint metrics recorded

---

## Metrics to Track

- Velocity: [Target] points
- Story completion: [X]/[Y] stories
- Bugs created: [N]
- Bugs fixed: [N]
- Cycle time: [Avg days per story]
- Team satisfaction: [1-5 scale]

---

## Out of Scope

Explicitly NOT in this sprint:
- [Item 1] - Deferred to Sprint [N+1]
- [Item 2] - Moved to backlog
- [Item 3] - Deprioritized

---

## Notes & Decisions

- [Decision 1]: [What was decided and why]
- [Agreement 1]: [Team agreement or working agreement]
- [Concern 1]: [Noted concern and how addressed]
```


## Best Practices

✅ **DO**: Set ONE clear sprint goal, commit to realistic capacity (use velocity avg), include 20-30% buffer, identify dependencies early, define DoD upfront, balance features with tech debt (80/20 rule), involve whole team in planning, timebox planning (2hrs max for 2-week sprint), prioritize ruthlessly (P0 must-haves first), document decisions and agreements

❌ **DON'T**: Pack sprint to 100% capacity, change goal mid-sprint without team agreement, commit to unknowns (needs discovery first), skip dependency check, take on work without acceptance criteria, ignore tech debt completely, let one person dominate story selection, go over time in planning (continue async if needed), commit to stretch goals as if they're P0, forget to track velocity and learnings

**Related**: `/pm:backlog-groom`, `/pm:user-stories`, `/pm:capacity`, `/pm:sprint-goal`, `/pm:retrospective`
