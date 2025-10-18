---
name: Backlog Optimization Workflow
description: Systematic backlog refinement, prioritization, and technical debt management
category: Operations
duration: 1 week
model: sonnet
---

# Backlog Optimization Workflow

Systematic backlog refinement, prioritization, and technical debt management.

## Usage
```
/backlog-optimization [optional: context about backlog state and goals]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Current backlog state (size, staleness, organization)
- Team context (velocity, capacity, tech stack)
- Goals for optimization (reduce size, improve quality, prioritize for upcoming work)
- Timeline and urgency

## When to Run

- **Quarterly**: Major backlog overhaul
- **Monthly**: Regular grooming
- **Before Planning**: Sprint or roadmap planning

## Timeline: 1 Week

## Workflow Phases

### Day 1: Inventory & Categorization

**Agents**: `agile-coach`, `requirements-engineer`

**Activities**:
1. **Audit Backlog**
   - Total items
   - Age distribution
   - Owner/status

2. **Categorize**
   - Features (new capabilities)
   - Improvements (enhancements)
   - Bugs (by severity)
   - Technical debt
   - Spikes/research

3. **Archive/Close**
   - Duplicates
   - No longer relevant
   - Won't do

**Deliverables**: Clean inventory

**Commands**:
```
/pm:backlog-groom
```

---

### Day 2: Technical Debt Assessment

**Agents**: `agile-coach`, engineering lead

**Activities**:
1. **Quantify Debt**
   - Impact on velocity
   - Risk to stability
   - Maintenance burden

2. **Score Debt Items**
   - Impact: High/Medium/Low
   - Effort: T-shirt sizing
   - Urgency: Critical/Important/Nice

3. **Debt Budget**
   - Allocate 20% capacity
   - Identify "must fix" items

**Deliverables**: Tech debt inventory, budget

---

### Day 3: Feature Prioritization

**Agents**: `feature-prioritizer`, `product-strategist`

**Activities**:
1. **RICE Scoring**
   - All feature items
   - Rank by score

2. **Strategic Alignment**
   - Map to OKRs
   - Filter by strategy

3. **Value vs Effort**
   - Plot on matrix
   - Identify quick wins

**Deliverables**: Prioritized feature list

**Commands**:
```
Tell feature-prioritizer: "Score all features with RICE"
```

---

### Day 4: Story Readiness Review

**Agents**: `requirements-engineer`, `agile-coach`

**Activities**:
1. **Check Top 20 Items**
   - Clear acceptance criteria?
   - Sized appropriately?
   - Dependencies identified?
   - Team understands?

2. **Refine as Needed**
   - Add details
   - Break down large stories
   - Clarify requirements

3. **Definition of Ready**
   - All criteria met
   - Mark as "Ready"

**Deliverables**: Sprint-ready backlog (top 20)

**Commands**:
```
/pm:user-stories [feature description]
/pm:backlog-groom --top 20
```

---

### Day 5: Sequencing & Planning

**Agents**: `agile-coach`, `product-strategist`

**Activities**:
1. **Sequence Items**
   - By dependencies
   - By OKR timing
   - By customer commitments

2. **Create Themes**
   - Group related items
   - Name themes
   - Assign to quarters

3. **Next 3 Sprints**
   - Tentative sprint goals
   - Story allocation
   - Capacity check

**Deliverables**: Sequenced backlog, 3-sprint preview

**Commands**:
```
/pm:sprint-plan "Next Sprint"
/pm:roadmap "Next Quarter"
```

---

## Backlog Health Metrics

**Size**:
- ✅ <100 items (manageable)
- ⚠️ 100-200 (needs cleanup)
- ❌ >200 (overwhelming)

**Staleness**:
- ✅ <20% older than 6 months
- ⚠️ 20-40% stale
- ❌ >40% stale

**Readiness**:
- ✅ Top 20 items Ready
- ⚠️ Top 10 Ready
- ❌ <10 Ready

**Technical Debt**:
- ✅ 20% of capacity allocated
- ⚠️ 10% allocated
- ❌ No allocation

---

## Prioritization Framework

### Tier 0: Critical (Do Immediately)
- P0 bugs
- Security issues
- Customer blockers
- OKR dependencies

### Tier 1: High Priority (Next 2 Sprints)
- Top RICE scores
- Quick wins
- Strategic bets
- Committed features

### Tier 2: Medium Priority (This Quarter)
- Good RICE scores
- Nice-to-haves
- Improvements

### Tier 3: Low Priority (Someday/Maybe)
- Low RICE
- Exploratory
- Future ideas

### Backlog: Archive
- Won't do
- Replaced by other solutions
- No longer relevant

---

## Technical Debt Budget

**Calculate**:
```
Sprint Capacity: 40 points
Debt Budget: 20% = 8 points

Allocate:
- 32 points features
- 8 points tech debt
```

**Debt Types**:
- **Critical**: Impacts prod reliability
- **Important**: Slows development
- **Nice-to-have**: Future improvements

**Prioritize**:
1. Critical debt first
2. Highest impact per effort
3. Enablers for features

---

## Outputs

### Prioritized Backlog
```
| Rank | Item | Type | RICE | Priority | Ready? |
|------|------|------|------|----------|--------|
| 1 | Feature A | Feature | 2400 | P0 | ✅ |
| 2 | Bug fix B | Bug | - | P0 | ✅ |
| 3 | Tech debt C | Debt | - | P1 | ⚠️ |
```

### Next 3 Sprints Preview
```
Sprint N+1 (Goal: Auth improvements)
- Feature A (8 pts)
- Feature B (5 pts)
- Tech debt C (3 pts)

Sprint N+2 (Goal: Analytics dashboard)
- Feature D (13 pts)
- Feature E (8 pts)

Sprint N+3 (Goal: Performance)
- Tech debt sprint
```

---

## Best Practices

✅ **Regular cadence**: Monthly grooming minimum
✅ **Involve team**: Eng estimates, design input
✅ **Limit WIP**: Don't start more than can finish
✅ **Archive liberally**: Kill old ideas
✅ **20% debt budget**: Consistent allocation
✅ **Top 20 ready**: Always sprint-ready backlog

❌ **Don't**: Endless backlog, no prioritization, skip tech debt

---

**Model**: Sonnet
