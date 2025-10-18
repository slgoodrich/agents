# Backlog Groomer

Refine, organize, and prioritize product backlog to keep it healthy and sprint-ready.

## Usage

```
/pm:backlog-groom [optional: epic, theme, or "all"]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Reviews backlog for relevance, clarity, and readiness
2. Assesses each story against Definition of Ready criteria
3. Sizes stories and identifies oversized items to break down
4. Prioritizes using RICE, ICE, or MoSCoW frameworks
5. Identifies dependencies, blockers, and quick wins
6. Organizes stories into epics and sprint-ready groups
7. Takes 45 minutes vs 2-3 hours of manual backlog grooming

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Backlog Context**:
- How many items in backlog? (rough count)
- When was last grooming session?
- What epic or theme to focus on? (or groom all)
- Any specific pain points? (stale items, unclear stories, bloated backlog)

**Team Context**:
- Team velocity (story points per sprint)
- Sprint length (1 week, 2 weeks, 3 weeks)
- Upcoming sprint capacity
- Team composition (engineers, designers, QA)

**Prioritization Criteria**:
- What prioritization framework do you use? (RICE, ICE, MoSCoW, Kano, Value vs Effort)
- What business goals drive priority? (revenue, retention, growth, tech debt)
- Any hard deadlines or commitments?

**Definition of Ready** (What makes a story ready for sprint):
- Your team's DoR checklist (if custom)
- Standard: User story format, acceptance criteria, sized, no blockers, team understands

**Example Input**:
```
Backlog: ~200 items, last groomed 4 weeks ago
Focus: "Search & Discovery" epic (30 items)
Team: 6 engineers, Fibonacci points, 32 point velocity, 2-week sprints
Next Sprint: Capacity 32 points, starts in 1 week
Prioritization: RICE scoring (Reach, Impact, Confidence, Effort)
Goals: Improve user retention (top priority), increase engagement
```

### 2. Review Backlog Health

**Backlog Health Indicators**:
- **Age**: How many items >6 months old? (Likely stale)
- **Size**: How many items >8 points? (Need to break down)
- **Readiness**: % of top 10 items that are sprint-ready
- **Relevance**: Are all items still aligned with current strategy?

**Actions**:
- **Close/Archive**: Stale, no longer relevant, or duplicate items
- **Refresh**: Update old items with current context
- **Break Down**: Split large stories (>8 points)
- **Clarify**: Add missing ACs, mockups, or context

### 3. Assess Story Readiness

**Definition of Ready Checklist** (All must be Yes for sprint-ready):
- [ ] **User Story Format**: "As a [persona], I want [action], so that [benefit]"
- [ ] **Acceptance Criteria**: Clear Given-When-Then scenarios
- [ ] **Sized**: Estimated (< 13 points, ideally <8)
- [ ] **Dependencies Clear**: No blockers or dependencies documented
- [ ] **Team Understanding**: Team can estimate and understands scope
- [ ] **Design Available**: Mockups for UI stories (if needed)
- [ ] **Technical Clarity**: Approach understood, no major unknowns

### 4. Prioritize Stories

**RICE Prioritization** (Most common):
- **Reach**: How many users impacted per quarter?
- **Impact**: How much does it improve user experience? (0.25, 0.5, 1, 2, 3)
- **Confidence**: How confident are we? (50%, 80%, 100%)
- **Effort**: Story points or person-months

**RICE Score** = (Reach × Impact × Confidence) / Effort

**Alternative Frameworks**:
- **ICE**: Impact × Confidence / Effort (simpler than RICE)
- **MoSCoW**: Must have, Should have, Could have, Won't have
- **Value vs Effort**: 2x2 matrix (high value/low effort = quick wins)

### 5. Organize and Sequence

**Group By**:
- **Epic/Theme**: Related stories together
- **Priority**: P0 (Must have) → P1 (Should have) → P2 (Nice to have)
- **Dependencies**: Sequential order if dependent

**Identify**:
- **Quick Wins**: High value, low effort (do first)
- **Major Bets**: High value, high effort (plan carefully)
- **Fill-Ins**: Low effort items to fill sprint gaps
- **Deprioritize**: Low value items (move to backlog bottom or close)

## Template

```markdown
# Backlog Grooming - [Date]

**Team**: [Name] | **Participants**: [List] | **Duration**: [Xmin]

---

## Grooming Stats

**Items Reviewed**: [N]
**Items Ready**: [N]
**Items Need Refinement**: [N]
**Items Removed**: [N]

---

## Ready for Sprint

| Story | Priority | Points | Notes |
|-------|----------|--------|-------|
| [Story 1] | P0 | 5 | All ACs clear, design ready |
| [Story 2] | P0 | 3 | Dependencies resolved |

**Total Ready**: [X] points

---

## Need Refinement

| Story | Blocker | Owner | Target Date |
|-------|---------|-------|-------------|
| [Story 1] | Missing design | [Designer] | [Date] |
| [Story 2] | Unclear ACs | [PM] | [Date] |

---

## Removed/Deferred

- [Story 1] - Reason: [Deprioritized / Duplicate / No longer relevant]
- [Story 2] - Reason: [Moved to icebox]

---

## Decisions Made

- [Decision 1]: [What was decided]
- [Decision 2]: [What was decided]

---

## Next Grooming

**Date**: [Date]
**Focus**: [Top N stories to prepare]
```

## Best Practices

✅ **DO**: Groom regularly (weekly), review top 2 sprints worth, ensure ACs complete, estimate collaboratively, identify dependencies, remove stale items, keep it timeboxed (1hr max), involve whole team, make decisions quickly

❌ **DON'T**: Groom entire backlog (focus on top items), skip regularly, estimate without team, leave unclear ACs, keep "zombie" stories (dead but not removed), go over time, let PM dictate estimates, defer all hard decisions

**Related**: `/pm:sprint-plan`, `/pm:user-stories`, `/pm:quick-prioritize`
