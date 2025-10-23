# Impact Estimator

Estimate feature impact on key metrics with data-driven projections and confidence intervals.

## Usage

```
/product-analytics:impact [feature or initiative] [target metrics]
```

## What This Command Does

1. Estimates feature impact on business and product metrics
2. Provides optimistic, realistic, and conservative projections
3. Documents assumptions and confidence levels
4. Creates measurement plan to validate impact
5. Helps prioritize features based on expected ROI
6. Takes 20 minutes vs 2 hours of manual impact analysis

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Feature/Initiative Details**:
- Feature or initiative description
- Target user segment
- Problem being solved
- How the feature works (mechanism)

**Current Baseline Metrics**:
- Current metric values (what are we measuring from?)
- Historical trends (growing, flat, declining?)
- Recent changes that affected metrics

**Target Metrics**:
- Which metrics should this feature impact?
- Why these metrics? (logic/mechanism)
- What does success look like?

**Supporting Data**:
- Similar features you've shipped (historical data)
- Competitor benchmarks (if available)
- User research insights
- Market data or industry benchmarks

**Example Input**:
```
Feature: Onboarding tutorial (interactive walkthrough)
Target Users: New signups (currently 500/month)
Problem: Only 35% of signups activate (complete first task)
Mechanism: Guide users through first task step-by-step
Target Metric: Activation rate (currently 35%)
Historical Data: Previous onboarding emails improved activation 5%
```

### 2. Identify Impact Mechanism

**How will this feature change behavior?**
- What user action changes?
- Why will users behave differently?
- What friction is removed?
- What value is added?

**Example**:
```
Mechanism: Interactive tutorial reduces confusion
- Currently: Users don't know where to start (35% figure it out)
- After: Tutorial guides every user through first task
- Expected: Fewer users drop off due to confusion
```

### 3. Develop Impact Model

**Three Scenarios**:

**Conservative** (Pessimistic):
- Worst-case realistic outcome
- Use when: New feature type, high uncertainty

**Realistic** (Most Likely):
- Expected outcome based on best data
- Use for: Planning and commitments

**Optimistic** (Best Case):
- Best-case realistic outcome
- Use when: Strong evidence, low risk

### 4. Document Assumptions

**Critical Assumptions**:
- What must be true for this impact to happen?
- What could invalidate the estimate?
- What dependencies exist?

### 5. Create Measurement Plan

**How will we measure actual impact?**
- What metrics to track?
- How long to measure?
- How to isolate this feature's impact?

## Template

```markdown
# Impact Estimate: [Feature Name]

**Date**: [YYYY-MM-DD]
**Analyst**: [Your Name]
**Feature**: [Brief description]
**Target Metrics**: [Primary metrics this affects]

---

## Executive Summary

**Expected Impact** (Realistic):
[Primary metric] from [current] to [projected] ([+X%])

**Confidence Level**: High | Medium | Low

**Timeline to Impact**: [X weeks/months to see results]

**Recommendation**: Build | Don't Build | Test First

---

## Feature Details

**What**: [Description of feature]

**Who**: [Target user segment]

**Problem Solved**: [User pain point addressed]

**Mechanism**: [How feature changes user behavior]
- **Current State**: [What users do today]
- **After Feature**: [What users will do]
- **Why Different**: [Why behavior changes]

---

## Current Baseline

**Primary Metric**: [Metric Name]
- **Current Value**: [X]
- **Trend**: ↗️ Growing | → Flat | ↘️ Declining ([% change over last 3 months])
- **Seasonality**: [Any seasonal patterns to account for]

**Secondary Metrics**:
- [Metric 2]: [Current value]
- [Metric 3]: [Current value]

**Data Sources**: [Where metrics come from - analytics tool, database, etc.]

---

## Impact Projections

### Primary Metric: [Metric Name]

| Scenario | Projected Value | Change | Rationale |
|----------|----------------|--------|-----------|
| **Conservative** | [X] | +[Y%] | [Why this is worst-case realistic] |
| **Realistic** | [X] | +[Y%] | [Why this is most likely] |
| **Optimistic** | [X] | +[Y%] | [Why this is best-case realistic] |

**Confidence Level**:
- 🟢 **High** (70-90% confident) - Strong evidence, similar features shipped
- 🟡 **Medium** (40-70% confident) - Some evidence, moderate uncertainty
- 🔴 **Low** (<40% confident) - Weak evidence, high uncertainty

**Our Assessment**: [High/Medium/Low] - [Explain why]

---

### Secondary Metrics

| Metric | Current | Projected | Change | Impact Type |
|--------|---------|-----------|--------|-------------|
| [Metric 2] | [X] | [Y] | +[Z%] | Positive ↗️ | Neutral → | Negative ↘️ |
| [Metric 3] | [X] | [Y] | +[Z%] | Positive ↗️ | Neutral → | Negative ↘️ |

---

## Supporting Evidence

### Historical Data

**Similar Features We've Shipped**:
1. **[Feature Name]** (Shipped [Date])
   - Impact: [Metric] improved [X%]
   - Similarity: [How similar to current feature]
   - Learnings: [What we learned]

2. **[Feature Name]** (Shipped [Date])
   - Impact: [Metric] improved [X%]
   - Similarity: [How similar]

**Takeaway**: [What historical data suggests about this feature]

---

### Competitor Benchmarks

**Competitor**: [Company Name]
- **Feature**: [Similar feature they have]
- **Reported Impact**: [If public]
- **Source**: [Where you got this data]

**Industry Benchmarks**:
- [Metric] industry average: [X%]
- Top quartile: [Y%]
- Our current: [Z%] (room to improve)

---

### User Research Insights

**From User Interviews** (n=[X]):
- [Quote or insight supporting impact]
- [% of users mentioning this pain point]

**From Surveys** (n=[X]):
- [Survey finding supporting impact]

**From Usage Data**:
- [Behavioral data showing problem]
- [Drop-off point this feature addresses]

---

## Assumptions

**Critical Assumptions** (must be true for impact):

1. **[Assumption 1]**
   - **If False**: [How estimates change]
   - **Validation**: [How to test this assumption]

2. **[Assumption 2]**
   - **If False**: [Impact]
   - **Validation**: [How to test]

3. **[Assumption 3]**
   - **If False**: [Impact]
   - **Validation**: [How to test]

**Dependencies**:
- [Dependency 1] must be in place
- [Dependency 2] must work correctly

---

## Risks to Impact

**High Risk**:
- 🔴 **[Risk 1]**: [What could go wrong]
  - **Probability**: High | Medium | Low
  - **Mitigation**: [How to reduce risk]

**Medium Risk**:
- 🟡 **[Risk 2]**: [What could go wrong]
  - **Probability**: Medium
  - **Mitigation**: [How to reduce risk]

---

## Timeline to Impact

**When will we see results?**

| Milestone | Timeline | Metric Impact |
|-----------|----------|---------------|
| Launch | Week 0 | Baseline measurement |
| Early Signal | Week 2-4 | [X% of expected impact] |
| Measurable Impact | Week 6-8 | [Y% of expected impact] |
| Full Impact | Week 12+ | [100% of expected impact] |

**Note**: [Explain why this timeline - user adoption curve, behavior change time, etc.]

---

## Measurement Plan

### Success Criteria

**Primary Success Metric**:
- **Metric**: [Metric Name]
- **Goal**: Achieve [X] (from [current] baseline)
- **Threshold**: [Minimum for "success"]

**Secondary Metrics**:
- [Metric 2]: Achieve [X]
- [Metric 3]: Achieve [X]

**Counter Metrics** (ensure we don't hurt):
- [Metric to watch]: Should not drop below [X]

---

### Measurement Methodology

**How We'll Measure**:
1. **Cohort Analysis**: Compare users with feature vs without
2. **A/B Test**: [If applicable] X% get feature, Y% control
3. **Before/After**: Compare [time period] before vs after

**Sample Size Needed**: [X] users to detect [Y%] change with 95% confidence

**Duration**: Measure for [X] weeks to account for [adoption curve, seasonality, etc.]

---

### Data Collection

**Metrics to Track**:
- [Metric 1]: [Tool/Source] - [Frequency]
- [Metric 2]: [Tool/Source] - [Frequency]

**Instrumentation Required**:
- [ ] Event tracking for [action]
- [ ] Funnel for [user journey]
- [ ] Dashboard for [metrics]

**Responsible**: [Who sets up tracking]

---

## Business Impact

### Revenue Impact (if applicable)

**Projected Revenue Impact**:
- **Realistic**: [+$X/month] from [mechanism]
- **Calculation**: [Show your work]
  - [Metric change] × [users] × [conversion rate] × [price]

**Payback Period**: [X months]

**Lifetime Value Impact**: [How this affects LTV]

---

### Cost Impact

**Development Cost**:
- Engineering: [X weeks] × [Y engineers] = [Z eng-weeks]
- Design: [X weeks]
- PM: [X weeks]
- **Total**: [Estimated cost]

**Ongoing Costs**:
- Maintenance: [X/month]
- Infrastructure: [Y/month]
- Support: [Z/month]

**ROI**: [Revenue impact / Total cost] = [X:1]

---

## Recommendation

**Build** | **Don't Build** | **Test First** | **Needs More Data**

**Rationale**:
[Explain recommendation based on impact, confidence, cost, strategic fit]

**If Build**:
- Prioritize as: P0 | P1 | P2
- Expected timeline: [X weeks to ship]
- Success = [Metric] reaches [Y] in [Z] weeks

**If Test First**:
- Run experiment with [X% of users] for [Y weeks]
- Go/no-go criteria: [Metric] > [threshold]

**If Needs More Data**:
- Research needed: [What data would increase confidence]
- How to get it: [User research, prototype, analysis]

---

## Review & Updates

**Review Checkpoint**: [Date to review estimates]

**Update Triggers**:
- New user research data
- Competitive intelligence
- Changed assumptions
- Feature scope changes

**Actual Results** (to be filled after launch):
- **[Metric]**: Projected [X], Actual [Y] ([Variance])
- **Learnings**: [What we learned for future estimates]
```

---

## Best Practices

### DO ✅

- **Use three scenarios** - Conservative, realistic, optimistic gives range
- **Ground in data** - Use historical data, benchmarks, research
- **Show your work** - Document assumptions and calculations
- **State confidence levels** - Be honest about uncertainty
- **Plan measurement upfront** - Know how you'll validate estimates
- **Include counter-metrics** - Watch for unintended negative impacts
- **Update after launch** - Compare actual to estimate, learn

### DON'T ❌

- **Cherry-pick data** - Don't only use evidence that supports high impact
- **Ignore uncertainty** - Low confidence estimates need bigger ranges
- **Forget indirect effects** - Feature may impact metrics you didn't expect
- **Assume linear adoption** - User adoption curves matter for timeline
- **Over-precision** - "+47.3%" is false precision, use "+40-50%"
- **Skip counter-metrics** - Some improvements hurt other metrics
- **Estimate without measurement plan** - If you can't measure, don't estimate

---

## Examples

### Example 1: Onboarding Tutorial

**Input**: "Estimate impact of interactive onboarding tutorial on activation rate"

**Output**:

```markdown
# Impact Estimate: Interactive Onboarding Tutorial

**Target Metric**: Activation Rate (complete first task)
**Current**: 35% of signups activate
**Mechanism**: Step-by-step tutorial reduces confusion

---

## Impact Projections

| Scenario | Activation Rate | Change | Rationale |
|----------|----------------|--------|-----------|
| **Conservative** | 42% | +7% pts | Tutorial helps confused users, not everyone completes it |
| **Realistic** | 48% | +13% pts | Most users follow tutorial, similar to email drip (+5% historical) |
| **Optimistic** | 55% | +20% pts | Tutorial + reduced friction = strong lift |

**Confidence**: 🟡 Medium (50%)
- ✅ Strong user research (40% mention "don't know where to start")
- ✅ Historical data: Onboarding emails improved activation 5%
- ⚠️ No direct comparable (interactive tutorial is new for us)

---

## Supporting Evidence

**Historical**: Onboarding email drip improved activation from 30% → 35% (+5% pts)

**User Research**: 40% of churned users said "didn't know where to start" (n=50 interviews)

**Industry**: Benchmark activation rate for similar products: 40-60%

---

## Assumptions

1. **Tutorial completion rate: 70%**
   - If only 50% complete → Impact drops to +8% pts (conservative scenario)

2. **Users who complete tutorial have 80% activation**
   - If only 60% → Impact drops to +10% pts

3. **No technical issues or bugs**
   - Critical - bugs could reduce impact or hurt metrics

---

## Measurement Plan

**Method**: A/B test, 50% get tutorial for 4 weeks

**Success Criteria**:
- ✅ Activation rate >45% (realistic scenario achieved)
- ✅ Tutorial completion >60%
- ✅ Time to first value <10 min (improved from 15 min)

**Counter Metrics**:
- Tutorial should not increase signup-to-activate time >20%
- Should not hurt retention (still measure D7, D30)

---

## Recommendation

**BUILD** - High impact, medium confidence, low cost

**Prioritize as**: P1 (high impact on critical metric)

**Success = Activation reaches 45%+ in 8 weeks**
```

---

### Example 2: Dashboard Customization

**Input**: "Estimate impact of custom dashboards on daily active users"

**Output**:

```markdown
# Impact Estimate: Custom Dashboards

**Target Metric**: DAU/MAU (Daily Active Users / Monthly Active Users)
**Current**: 25% (2,500 DAU / 10,000 MAU)
**Mechanism**: Personalized dashboards increase daily habit formation

---

## Impact Projections

| Scenario | DAU/MAU | Change | Rationale |
|----------|---------|--------|-----------|
| **Conservative** | 27% | +2% pts | Only power users customize, they already engaged |
| **Realistic** | 30% | +5% pts | 30% of users customize, they check daily vs 2x/week |
| **Optimistic** | 35% | +10% pts | Viral effect - users share dashboards, team engagement |

**Confidence**: 🟡 Medium (60%)
- ✅ User requests: Top feature request (45 customers)
- ✅ Competitor data: Customization drives engagement
- ⚠️ No direct historical data (new feature type for us)

---

## Recommendation

**BUILD** - Strategic feature with medium-high impact

**Success = DAU/MAU reaches 30% in 3 months**
```

---

## Model

Use: Sonnet

---

## Related

- `/continuous-discovery:mvp` - Scope MVP based on impact estimates
- `/feature-prioritization:prioritize` - Prioritize features by impact
- `/product-analytics:experiment` - Test impact with experiments before full build
- `/product-analytics:kpi-dashboard` - Track metrics mentioned in impact estimate
- `/strategic-planning:okr` - Connect feature impact to OKR progress
- `/continuous-discovery:discovery-sprint` - Validate impact assumptions before building
- `data-scientist` agent - Statistical analysis and impact modeling
- `feature-prioritizer` agent - Prioritization frameworks using impact estimates
- `product-strategist` agent - Strategic decisions based on impact
