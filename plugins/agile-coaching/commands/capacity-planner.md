# Capacity Planner

Plan team capacity and resource allocation for realistic sprint and project commitments.

## Usage

```
/agile-coaching:capacity [team name] [time period] [optional: team composition]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Calculates available team capacity accounting for PTO, meetings, and overhead
2. Maps capacity to committed work and identifies over/under allocation
3. Provides team member allocation breakdown
4. Highlights capacity risks and bottlenecks
5. Recommends capacity adjustments or scope changes
6. Takes 15 minutes vs 1 hour of manual capacity planning

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Team Information**:
- Team name and composition
- Number of team members by role (engineers, designers, PM, QA)
- Individual availability (who's on PTO, part-time, etc.)

**Time Period**:
- Planning period (sprint, month, quarter)
- Start and end dates
- Working days in period

**Historical Context**:
- Team velocity (if sprint planning)
- Historical capacity utilization
- Known time commitments (meetings, on-call, etc.)

**Committed Work**:
- Stories/tasks already committed
- Effort estimates for each
- Dependencies and blockers

**Example Input**:
```
Team: Platform Team
Period: Sprint 47 (Nov 6 - Nov 17, 2 weeks)
Team Size: 5 engineers, 1 designer, 1 QA
PTO: Jane (engineer) out Nov 13-17, Tom (designer) out Nov 6-8
Velocity: 32 points last sprint
Committed: 8 stories totaling 28 points
```

### 2. Calculate Available Capacity

**Formula**:
```
Available Capacity = (Team Size × Working Days × Hours per Day) - Overhead
```

**Overhead includes**:
- PTO/vacation/holidays
- Meetings (standups, planning, retros)
- On-call rotations
- Context switching
- Administrative tasks
- Interview time

**Industry Standard Overhead**: 20-30% for engineering teams

### 3. Map Capacity to Work

**Committed Work**:
- Stories/tasks already committed
- Effort in points or hours
- Owner assignments

**Uncommitted Capacity**:
- Buffer for unknowns
- Tech debt
- Bug fixes

### 4. Identify Risks

**Over-allocation**: Committed > Available capacity
**Under-allocation**: Significant uncommitted capacity
**Bottlenecks**: Individual team members over-allocated
**Dependencies**: Work blocked waiting on others

### 5. Recommend Adjustments

**If over-allocated**:
- Reduce scope
- Extend timeline
- Add resources

**If under-allocated**:
- Add lower-priority work
- Tech debt sprint
- Innovation time

## Template

```markdown
# Capacity Plan: [Sprint/Quarter]

**Period**: [Dates] | **Team**: [Name] | **Last Updated**: [Date]

---

## Team Capacity

| Person | Role | Availability | Capacity (pts) |
|--------|------|--------------|----------------|
| [Name] | Eng | 10d (100%) | 20 |
| [Name] | Eng | 8d (80%, PTO) | 16 |
| [Name] | Designer | 10d (100%) | 10 |

**Total Capacity**: [X] points

---

## Capacity Adjustments

**Baseline**: [Team size] × [Days] × [Pts/day] = [Y] points

**Reductions**:
- PTO/holidays: -[X] points
- Meetings/overhead: -[Y] points ([%] of time)
- Onboarding: -[Z] points
- **Adjusted Capacity**: [Total] points

---

## Allocation

| Category | Points | % of Capacity |
|----------|--------|---------------|
| Feature work | [X] | [%] |
| Bug fixes | [Y] | [%] |
| Tech debt | [Z] | [%] |
| Overhead | [W] | [%] |
| **Total** | **[Sum]** | **100%** |

**Recommended**:
- Features: 60-70%
- Bugs: 10-20%
- Tech debt: 10-20%
- Overhead: 10%

---

## Risks

- 🟡 [Risk]: [Impact on capacity]
- 🟡 [Risk]: [Impact on capacity]
```

## Best Practices

✅ **DO**: Plan conservatively (use 70-80% of theoretical capacity), account for meetings/overhead, update when people out, track actual vs planned, reserve capacity for unknowns, be transparent about constraints

❌ **DON'T**: Plan to 100% capacity (recipe for burnout), forget overhead (meetings, email, reviews), ignore historical velocity, skip PTO/holidays, commit beyond capacity, forget to reserve bug fix capacity

**Related**: `/agile-coaching:sprint-plan`, `/product-analytics:velocity-tracking`
