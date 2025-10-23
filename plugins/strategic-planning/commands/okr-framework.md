# OKR Framework

Create quarterly or annual OKRs (Objectives and Key Results) aligned to company strategy using Google's proven methodology.

## Usage

```
/strategic-planning:okr [period: Q1 2025, H1 2025, 2025] [optional: strategic focus, team]
```

## What This Command Does

1. Generates OKRs following Google's framework and best practices
2. Creates measurable, ambitious key results with clear success criteria
3. Cascades from company to team to individual OKRs with alignment
4. Provides tracking framework, check-in templates, and scoring guides
5. Ensures OKRs are stretch goals (60-70% confidence) not business-as-usual
6. Takes 45 minutes vs 2-3 hours of manual OKR creation

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**OKR Context**:
- What time period? (Q1 2025, H1 2025, full year 2025)
- What level? (company-wide, product team, specific team, individual)
- Who owns these OKRs? (CEO, VP Product, team lead, IC)
- First time using OKRs or continuing from previous period?

**Strategic Context**:
- What's the company's top priority this period? (growth, retention, new market)
- What company OKRs exist? (how do team OKRs connect)
- What was achieved last period? (previous OKR scores, learnings)
- Any strategic initiatives or bets this period?

**Current State**:
- What are baseline metrics? (current performance on key metrics)
- What's working well? (what to double down on)
- What's not working? (what to fix or stop)
- What changed? (market, competition, team, resources)

**Resources & Constraints**:
- Team size and composition (headcount, roles, skills)
- Budget available (for this period)
- Technical capacity (velocity, technical debt load)
- Dependencies (what you need from other teams)

**Example Input**:
```
Period: Q2 2025 (Apr-Jun)
Level: Product team (Growth squad)
Owner: Sarah Chen, Growth PM
Company OKR: Reach $10M ARR by EOY
Strategic Focus: User acquisition and activation
Last Quarter: Achieved 0.6 on activation OKRs, missed on retention (0.3)
Baseline: 20K MAU, 25% DAU/MAU, 12% signup→paid conversion
Team: 6 engineers, 1 designer, 1 PM, 2-week sprints
Budget: $50K for growth experiments
Dependencies: Need analytics instrumentation from platform team
```

### 2. Understand OKR Fundamentals

**OKR Structure**:
- **Objective**: Inspiring, qualitative goal (what you want to achieve)
- **Key Results**: Measurable outcomes that prove you achieved the objective (how you'll know)

**OKR Principles** (Google's framework):
1. **Objectives are inspirational**: Motivate the team, qualitative
2. **Key Results are measurable**: Numbers, percentages, milestones
3. **OKRs are ambitious**: 60-70% confidence (not 100%)
4. **OKRs are time-bound**: Clear deadline (end of period)
5. **OKRs are aligned**: Connect to company goals
6. **OKRs are public**: Visible to entire company

**Scoring**:
- **0.0-0.3**: Failed (need to understand why)
- **0.4-0.6**: Made progress but fell short
- **0.7-0.9**: Succeeded (target zone - ambitious but achievable)
- **1.0+**: Exceeded (may have sandbagged - set more ambitious goals next time)

### 3. Write Effective Objectives

**Good Objectives**:
- Inspirational and motivating
- Qualitative (not a number)
- Time-bound (this quarter, this year)
- Aligned to strategy
- Team-focused (we, not I)

**Objective Examples**:
- ✅ "Become the go-to solution for mid-market sales teams"
- ✅ "Make the product indispensable for daily workflows"
- ✅ "Delight customers with world-class support"
- ❌ "Increase revenue by 20%" (this is a KR, not objective)
- ❌ "Ship dark mode" (this is a task/initiative)

**How Many**: 3-5 objectives per period (focus, not exhaustive)

### 4. Write Measurable Key Results

**Good Key Results**:
- Measurable (number, percentage, milestone)
- Outcome-focused (not output)
- Time-bound (by [date])
- Ambitious (60-70% confident)
- Owned (clear owner)

**Key Result Formats**:
- **Metric increase**: "[Metric] increases from [X] to [Y] by [Date]"
- **Milestone achievement**: "[Deliverable] launched by [Date]"
- **Percentage/adoption**: "[Behavior] reaches [Z]% by [Date]"

**Key Result Examples**:
- ✅ "NPS increases from 35 to 50 by June 30"
- ✅ "Mobile app launched in iOS App Store by May 15"
- ✅ "Enterprise tier adoption reaches 25% of customer base"
- ❌ "Work on improving NPS" (not measurable)
- ❌ "Build 10 new features" (output, not outcome)

**How Many**: 3-5 key results per objective

### 5. Cascade and Align OKRs

**Cascading** (Top-down alignment):
```
Company OKR: Reach $10M ARR
  ↓
Product OKR: Improve trial→paid conversion from 12% to 20%
  ↓
Growth Team OKR: Increase activation (first value in 7 days) from 40% to 65%
  ↓
Engineer OKR: Ship onboarding redesign by April 30
```

**Alignment Check**:
- How do team OKRs support company OKRs?
- Do individual OKRs support team OKRs?
- Are there gaps (company priorities not covered)?

## Template

```markdown
# [Period] OKRs: [Product/Team Name]

**Owner**: [Name, Title]
**Period**: [Start Date] - [End Date] ([Duration])
**Status**: 📝 Draft | 🚀 Active | ✅ Completed | 🔄 In Review

**Last Updated**: [YYYY-MM-DD]

---

## Executive Summary

**Strategic Focus**: [Top 1-2 priorities this period]

**Success Definition**: [What "success" looks like at end of period]

**Key Bets**: [1-2 sentence on biggest initiatives]

**Confidence**: [Overall confidence level 0-1.0 with reasoning]

---

## Alignment to Company Goals

**Company OKRs This Period**:
1. [Company Objective 1] → [How our OKRs support this]
2. [Company Objective 2] → [How our OKRs support this]

**Strategic Initiatives**:
- [Initiative 1]: [How OKRs connect]
- [Initiative 2]: [How OKRs connect]

---

## Objective 1: [Inspiring, Qualitative Goal]

**Why This Matters**: [Strategic importance - why this is a priority]

**Current State**: [Where we are today]

**Desired Future State**: [Where we want to be]

---

### Key Results

#### KR 1.1: [Metric Name] increases from [Baseline] to [Target] by [Date]

**Current Performance**: [X] (as of [Date])
**Target**: [Y]
**Required Change**: [Percentage or absolute increase]
**Tracking**: [How we measure - tool, dashboard, frequency]

**Owner**: [Name]
**Confidence**: [0-1.0] - [Reasoning]

**Dependencies**:
- [Dependency 1]: [What we need from whom]
- [Dependency 2]: [Blocker to address]

**Initiatives** (how we'll achieve this):
1. [Initiative 1]: [Description, owner, timeline]
2. [Initiative 2]: [Description, owner, timeline]
3. [Initiative 3]: [Description, owner, timeline]

---

#### KR 1.2: [Achievement/Milestone] completed by [Date]

**Definition of Done**:
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

**Owner**: [Name]
**Confidence**: [0-1.0] - [Reasoning]

**Milestones**:
- [Date 1]: [Milestone 1]
- [Date 2]: [Milestone 2]
- [Date 3]: [Final delivery]

**Initiatives**:
1. [Initiative]
2. [Initiative]

---

#### KR 1.3: [Percentage/Adoption] reaches [Target]% by [Date]

**Baseline**: [X]% (as of [Date])
**Target**: [Y]%
**Gap to Close**: [Y-X] percentage points

**Owner**: [Name]
**Confidence**: [0-1.0] - [Reasoning]

**Measurement Method**: [How we calculate this percentage]

**Initiatives**:
1. [Initiative]
2. [Initiative]

---

### Objective 1 Summary

**Total Confidence**: [Average of KR confidences]

**Resources Required**:
- **Team**: [X] engineers, [Y] designers for [Z] sprints
- **Budget**: $[Amount] for [Purpose]
- **Tools/Infrastructure**: [New tools or systems needed]

**Risks**:
- 🔴 [High risk]: [Description, mitigation]
- 🟡 [Medium risk]: [Description, mitigation]

**What Could Go Wrong**:
- [Risk scenario 1]: [Impact, probability, mitigation]
- [Risk scenario 2]: [Impact, probability, mitigation]

---

## Objective 2: [Another Inspiring Goal]

**Why This Matters**: [Strategic importance]

**Current State**: [Baseline]

**Desired Future State**: [Target end state]

---

### Key Results

#### KR 2.1: [Key Result]

[Same structure as Objective 1 KRs]

---

#### KR 2.2: [Key Result]

[Repeat structure]

---

#### KR 2.3: [Key Result]

[Repeat structure]

---

### Objective 2 Summary

[Same structure as Objective 1 summary]

---

## Objective 3: [Third Goal - Optional]

[Repeat structure]

---

## Cross-Team Dependencies

**What We Need From Others**:

| Team/Function | What We Need | By When | Status | Owner |
|---------------|--------------|---------|--------|-------|
| Platform Team | Analytics instrumentation | April 15 | ⏳ Pending | Sarah |
| Marketing | Landing page redesign | May 1 | 🟢 Committed | Mike |
| Sales | Enterprise pilot customers | June 1 | 🟡 At risk | Jessica |

**What Others Need From Us**:

| Team/Function | What They Need | By When | Status | Owner |
|---------------|----------------|---------|--------|-------|
| Customer Success | Feature training | April 30 | 🟢 On track | Team |
| Sales | Pricing calculator | May 15 | ⏳ Pending | PM |

---

## Resources & Budget

**Team Allocation**:
- Engineering: [X] FTE (Full-Time Equivalent)
- Design: [Y] FTE
- Product: [Z] FTE

**Budget**:
- Experiments/Testing: $[Amount]
- Tools/Infrastructure: $[Amount]
- External contractors: $[Amount]
- **Total**: $[Total Budget]

**Hiring Needs**:
- [Role 1]: Start date [Date] (required for [OKR])
- [Role 2]: Start date [Date]

---

## Tracking & Check-ins

### Weekly Check-in Schedule

**Every Monday 10 AM**: Team OKR review (30 min)

**Agenda**:
1. Review progress on each KR (5 min per KR)
2. Identify blockers (10 min)
3. Adjust priorities if needed (5 min)

**Check-in Template**:

| Objective | Key Result | Week | Score | On Track? | Blockers | Next Actions |
|-----------|------------|------|-------|-----------|----------|--------------|
| O1 | KR 1.1: DAU/MAU 40% | Week 4/13 | 0.25 | 🟢 Yes | None | Continue |
| O1 | KR 1.2: Push engagement 35% | Week 4/13 | 0.15 | 🟡 At risk | ML model delayed | Fast-follow simple rules-based |
| O1 | KR 1.3: 24h return 60% | Week 4/13 | 0.05 | 🔴 Behind | Feature not shipped | Escalate to eng lead |
| O2 | KR 2.1: K-factor 0.7 | Week 4/13 | 0.10 | 🟡 At risk | UX not finalized | Design review Friday |

**Status Indicators**:
- 🟢 **On Track**: Projected to hit 0.7-1.0 by end of period
- 🟡 **At Risk**: May fall short (projected 0.4-0.6), needs intervention
- 🔴 **Behind**: Unlikely to achieve (projected <0.4), consider pivoting

---

### Monthly Review

**End of Each Month**: Deep dive on OKRs (1 hour)

**Agenda**:
1. Score each KR (where are we today vs target?)
2. What's working? What's not?
3. Do we need to adjust OKRs? (valid if context changed)
4. What help do we need from leadership?

---

### Scoring Guide

**How to Score Key Results**:

**0.0 - 0.3 (Failed)**:
- We made little to no progress
- Need to understand: Was goal unrealistic? Wrong approach? Blockers we couldn't remove?
- Action: Root cause analysis, don't repeat same mistakes

**0.4 - 0.6 (Made Progress)**:
- We made meaningful progress but fell short
- This is OKAY for ambitious OKRs
- Action: Understand gap, carry over to next period if still strategic

**0.7 - 0.9 (Succeeded)**:
- **This is the target zone for OKRs**
- Ambitious but achievable
- Action: Celebrate! Then set next ambitious goal.

**1.0+ (Exceeded)**:
- We over-achieved
- Possible reasons: Sandbagged (set too easy), got lucky, context changed
- Action: Next time, set more ambitious targets

**Example Scoring**:
```
KR: DAU/MAU increases from 25% to 40% by June 30

April 30: 28% → Score 0.2 (3/15 percentage points = 20%)
May 31: 33% → Score 0.53 (8/15 percentage points = 53%)
June 30: 38% → Score 0.87 (13/15 percentage points = 87%) ✅ Success!
```

---

## OKR Review & Retrospective

**End of Period Retrospective**:

### Final Scores

| Objective | Key Result | Target | Actual | Score | Status |
|-----------|------------|--------|--------|-------|--------|
| O1 | KR 1.1 | 40% | 38% | 0.87 | ✅ |
| O1 | KR 1.2 | 35% | 28% | 0.57 | 🟡 |
| O1 | KR 1.3 | 60% | 52% | 0.68 | 🟡 |
| O2 | KR 2.1 | 0.7 | 0.5 | 0.50 | 🟡 |
| O2 | KR 2.2 | 25% | 18% | 0.55 | 🟡 |

**Overall Score**: [Average] = 0.63 ✅ (Target zone: 0.7-0.9, close!)

---

### What We Learned

**What Went Well** (Keep doing):
- [Success 1]: [Why it worked]
- [Success 2]: [Why it worked]

**What Didn't Go Well** (Stop doing):
- [Failure 1]: [Root cause, what we learned]
- [Failure 2]: [Root cause, what we learned]

**What to Try Next Time** (Experiment):
- [Learning 1]: [What we'll do differently]
- [Learning 2]: [What we'll do differently]

---

### Carryover to Next Period

**Incomplete Work to Continue**:
- [OKR 1]: Scored 0.5, still strategic → Continue in Q3
- [OKR 2]: Scored 0.3, deprioritized → Drop

**New Priorities for Next Period**:
- [Priority 1]: [Why this is now important]
- [Priority 2]: [Why this is now important]

```

---

## Best Practices

### DO ✅

- **Set ambitious goals** - 60-70% confidence, not 100%
- **Focus on outcomes** - "Increase retention" not "Build feature X"
- **Make KRs measurable** - Numbers, percentages, yes/no milestones
- **Align to strategy** - Every OKR connects to company goals
- **Review weekly** - Don't set-and-forget, track progress
- **Be public** - Share OKRs across company for transparency
- **Celebrate 0.7 scores** - This is success for ambitious OKRs!
- **Learn from misses** - Understand why, don't punish team

### DON'T ❌

- **Don't make OKRs your entire job** - OKRs are top priorities, not exhaustive todo list
- **Don't set safe goals** - If you always hit 1.0, you're sandbagging
- **Don't tie to compensation** - OKRs are stretch goals, not performance targets
- **Don't set and forget** - Check in weekly, adjust if context changes
- **Don't confuse tasks with OKRs** - "Ship dark mode" is initiative, not objective
- **Don't have too many OKRs** - 3-5 objectives max, focus over breadth
- **Don't ignore low scores** - Understand root cause, adjust next time
- **Don't change OKRs mid-period** - Only if context fundamentally changes

---

## Examples

### Example 1: Product Team Growth OKRs

**Input**: "Create Q2 2025 OKRs for product growth team"

**Output**:

```markdown
# Q2 2025 OKRs: Growth Team

**Owner**: Sarah Chen, Growth PM
**Period**: April 1 - June 30, 2025 (13 weeks)
**Status**: 🚀 Active

---

## Objective 1: Make the product indispensable for daily workflows

**Why This Matters**: DAU/MAU of 25% means users find us useful weekly, not daily. Need habit formation to increase retention and LTV.

**Current State**: 25% DAU/MAU (5K DAU / 20K MAU)
**Desired Future State**: 40% DAU/MAU (industry best-in-class)

### Key Results

**KR 1.1: DAU/MAU ratio increases from 25% to 40% by June 30**
- Current: 25%
- Target: 40%
- Gap: 15 percentage points
- Confidence: 0.6 (Medium)
- Initiatives: Daily digest, home screen widgets, push notifications

**KR 1.2: Push notification engagement reaches 35% open rate**
- Baseline: 12%
- Target: 35%
- Confidence: 0.5 (Medium - depends on ML model)
- Initiatives: Smart timing ML model, personalized content

**KR 1.3: Users returning within 24 hours grows to 60%**
- Current: 35%
- Target: 60%
- Confidence: 0.7 (Medium-High)
- Initiatives: Quick actions, saved workflows, collaboration features

---

## Objective 2: Achieve viral product growth

**Why This Matters**: CAC is high ($150). Viral growth reduces acquisition cost and accelerates growth.

**KR 2.1: Viral coefficient (k-factor) reaches 0.7 from 0.3**
**KR 2.2: Share rate grows to 25% of users sharing monthly (from 8%)**
**KR 2.3: Invite conversion improves from 30% to 50%**

Initiatives: In-product sharing, referral incentives, team collaboration
```

---

## Model

Use: Sonnet

---

## Related

- `/strategic-planning:roadmap` - Create product roadmap aligned to OKRs
- `/strategic-planning:quarterly-planning` - Full quarterly planning process
- `/product-analytics:kpi-dashboard` - Track metrics for key results
- `/stakeholder-management:decision-log` - Document strategic decisions behind OKRs
- `product-strategist` agent - Strategic planning and OKR alignment
- `data-scientist` agent - Define measurable key results and tracking
