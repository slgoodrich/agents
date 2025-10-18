# Experiment Designer

Design rigorous A/B tests and growth experiments with hypothesis, metrics, and analysis plans.

## Usage

```
/pm:experiment [hypothesis or feature to test] [optional: context, metrics]
```

## What This Command Does

1. Formulates testable hypotheses using structured format
2. Designs experiment variants (control vs treatment) with clear differences
3. Defines primary, secondary, and guardrail metrics
4. Calculates sample size and experiment duration for statistical power
5. Creates analysis plan with success criteria and decision tree
6. Takes 30 minutes vs 2 hours of manual experiment design

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Experiment Context**:
- What are you trying to test? (feature, flow, copy, design)
- What's the expected impact? (increase conversion, reduce churn, improve engagement)
- Why do you think this will work? (user research, competitive analysis, intuition)
- What's the risk if you're wrong?

**Metrics Context**:
- What's the primary metric you care about?
- What's the baseline value of that metric?
- What lift would make this experiment worth it? (Minimum detectable effect)
- What metrics should NOT get worse? (Guardrails)

**Traffic & Timeline**:
- How much traffic do you get? (users/day, sessions/day)
- What percentage can you expose to experiment?
- How long can you run the experiment?
- Any seasonal effects to consider?

**Technical Context**:
- What experimentation platform do you use? (Optimizely, LaunchDarkly, custom)
- How are users randomized? (user ID, session, device)
- Can you track users cross-session?

**Example Input**:
```
Hypothesis: Adding social proof ("Join 100K users") on signup page will increase conversions
Current conversion: 12% (baseline)
Traffic: 10K visitors/day
Exposure: Can allocate 50% to experiment
Platform: Optimizely
Goal: Looking for 10% relative lift (12% → 13.2%)
Guardrails: Page load time, bounce rate
Duration: Can run 2-4 weeks
```

### 2. Formulate Hypothesis

**Hypothesis Format** (Specific, measurable, testable):
```
We believe that [specific change]
Will result in [expected outcome with magnitude]
For [user segment]
Because [rationale based on data/research]
We will measure [primary metric]
```

**Good vs Bad Hypotheses**:
- ❌ Bad: "New UI will be better"
- ✅ Good: "Adding progress indicator will increase trial-to-paid conversion by 10% because users understand how close they are to value"

### 3. Design Variants

**Variant Design**:
- **Control (A)**: Current experience (unchanged baseline)
- **Treatment (B)**: Single change hypothesis predicts will improve metric
- **Optional Treatment (C)**: Alternative approach (multivariate testing)

**Best Practices**:
- Test ONE variable at a time (unless multivariate)
- Make change meaningful and user-visible
- Ensure technical implementation is identical except for test variable

### 4. Define Metrics

**Primary Metric**: The ONE metric you're trying to move
**Secondary Metrics**: Related metrics that provide context
**Guardrail Metrics**: Metrics that should NOT get worse

**Metric Requirements**:
- Measurable and trackable
- Sensitive to change
- Meaningful to business

### 5. Calculate Sample Size

**Statistical Parameters**:
- **Baseline Conversion**: Current metric value
- **Minimum Detectable Effect (MDE)**: Smallest change you care about
- **Statistical Power**: Typically 80% (chance of detecting real effect)
- **Significance Level**: Typically 95% (p < 0.05)

**Sample Size Formula** (for conversion metrics):
Sample size per variant ≈ 16 × (baseline × (1 - baseline)) / (MDE²)

**Duration Calculation**:
Days to reach sample = (Sample size per variant × 2) / (Daily traffic × % exposed)

## Template

```markdown
# Experiment Design: [Experiment Name]

**Experiment ID**: EXP-[XXX]
**Owner**: [Your Name]
**Status**: 📝 Draft | 🚀 Running | ✅ Complete | 🚫 Stopped Early
**Created**: [YYYY-MM-DD]

---

## Executive Summary

**What**: [One sentence: what we're testing]
**Why**: [One sentence: why we think this will work]
**Expected Impact**: [Primary metric expected to move by X%]
**Duration**: [Start] - [End] ([X] days)
**Decision**: [TBD until experiment completes]

---

## Hypothesis

**We believe that** [specific change to product/feature]
**Will result in** [quantifiable outcome - e.g., "15% increase in signup conversion"]
**For** [specific user segment - e.g., "new visitors from paid ads"]
**Because** [rationale based on data, research, or theory]
**We will measure** [primary metric - e.g., "signup conversion rate"]

**Risk if Wrong**: [What happens if hypothesis is incorrect - wasted eng time, user confusion, etc.]

**Example**:
*We believe that* adding social proof ("Join 100,000 users") above the signup form
*Will result in* 10% relative increase in signup conversion (12% → 13.2%)
*For* new visitors landing on homepage
*Because* user research showed visitors hesitate due to trust concerns, and social proof increases perceived credibility
*We will measure* signup conversion rate (% of visitors who complete signup)

---

## Experiment Design

### Variants

#### Variant A: Control (Baseline)

**Traffic Allocation**: 50%

**Description**: Current experience with no changes

**User Experience**:
[Description or screenshot of control]

**Example**: Homepage with existing headline "Start your free trial" and standard signup form

---

#### Variant B: Treatment

**Traffic Allocation**: 50%

**Description**: [What changes in this variant]

**User Experience**:
[Description or screenshot of treatment]

**Example**: Homepage with headline "Join 100,000 users - Start your free trial" and identical signup form

**Hypothesis**: Social proof element will increase trust and encourage signup

---

#### Variant C: Alternative Treatment (Optional)

**Traffic Allocation**: [If multivariate, specify %]

**Description**: [Alternative approach to test]

---

### Randomization

**Randomization Unit**: [User ID | Session ID | Device ID]
- **Why**: [Rationale for choice]

**Traffic Split**: [50/50 | 33/33/34 | Custom]

**Exclusions**:
- [Exclude existing customers - only test new visitors]
- [Exclude mobile app - web only]
- [Exclude countries: [list]]

---

## Success Metrics

### Primary Metric

**Metric**: [Metric name - e.g., "Signup Conversion Rate"]

**Definition**: [How metric is calculated - e.g., "% of homepage visitors who complete signup"]

**Baseline Performance**:
- **Current Value**: [X]% (measured over last [Y] days)
- **Variance**: [Standard deviation or range]

**Target Performance**:
- **Minimum Detectable Effect (MDE)**: [Smallest lift we care about - e.g., "10% relative lift"]
- **Absolute Target**: [Goal value - e.g., "13.2% conversion"]
- **Why This MDE**: [Justification - e.g., "10% lift worth eng investment"]

**Measurement**:
- **Tracking Event**: [Event name in analytics]
- **Attribution Window**: [How long user has to convert - e.g., "24 hours"]

---

### Secondary Metrics

**Metric 2**: [Supporting metric - e.g., "Trial activation rate"]
- **Expected Direction**: [Increase | Decrease | No change]
- **Rationale**: [Why we're tracking this]

**Metric 3**: [Another metric - e.g., "Time to first value"]
- **Expected Direction**: [Increase | Decrease | No change]

---

### Guardrail Metrics

**Guardrail 1**: [Metric we don't want to harm - e.g., "Page load time"]
- **Threshold**: Should not increase by >10%
- **Why**: Poor performance hurts all conversions

**Guardrail 2**: [e.g., "Bounce rate"]
- **Threshold**: Should not increase by >5%
- **Why**: Indicates user confusion or poor UX

**Guardrail 3**: [e.g., "Trial-to-paid conversion"]
- **Threshold**: Should not decrease
- **Why**: More signups only valuable if quality doesn't drop

---

## Sample Size & Power Analysis

**Statistical Parameters**:
- **Baseline Conversion**: [X]%
- **Minimum Detectable Effect (MDE)**: [Y]% relative ([Z]% absolute)
- **Statistical Power**: 80% (probability of detecting real effect)
- **Significance Level**: 95% confidence (α = 0.05)

**Sample Size Calculation**:

Using formula: n = 16 × σ² / (MDE)²

**Sample Size Needed**: [N] users per variant ([2N] total)

**Example**:
- Baseline: 12%
- MDE: 10% relative (1.2% absolute)
- Power: 80%, α = 0.05
- **Sample size**: 16,000 per variant (32,000 total)

---

## Experiment Timeline

**Traffic Available**: [X] users/day

**Exposure Rate**: [Y]% of traffic (remaining traffic sees control by default)

**Users in Experiment per Day**: [X] × [Y%] = [Z] users/day

**Days to Reach Sample Size**: [2N] / [Z] = [Days]

**Ramp-Up Plan**:
- **Day 1-2**: 10% of target exposure (verify tracking, no critical issues)
- **Day 3-5**: 50% of target exposure (monitor for unexpected behavior)
- **Day 6+**: 100% of target exposure (full experiment)

**Timeline**:
- **Prep & QA**: [Start Date - 3 days]
- **Ramp Start**: [Start Date]
- **Full Exposure**: [Start Date + 5 days]
- **Earliest Read**: [Date when minimum sample size reached]
- **Planned End**: [End Date - allows for extension if needed]

**Duration**: [X] days total

---

## Experiment Execution

### Pre-Launch Checklist

**Technical Setup**:
- [ ] Feature flag created and tested
- [ ] Variants implemented correctly
- [ ] Tracking events firing (verified in dev/staging)
- [ ] Randomization working (users stay in same variant)
- [ ] Sample ratio check (50/50 split confirmed)

**Stakeholder Alignment**:
- [ ] Eng lead reviewed experiment design
- [ ] Data analyst can access metrics
- [ ] CS/support team notified (may see questions)
- [ ] Legal/compliance approved (if applicable)

**Analytics Setup**:
- [ ] Dashboard created for real-time monitoring
- [ ] Alerts configured for guardrail violations
- [ ] Baseline data captured (pre-experiment period)

---

### During Experiment

**Daily Monitoring**:
- [ ] Check sample ratio (should be ~50/50)
- [ ] Monitor guardrail metrics (any red flags?)
- [ ] Check for implementation bugs
- [ ] Verify sufficient traffic hitting experiment

**Early Stop Criteria** (Stop experiment early if):
- ❌ **Critical Bug**: Experiment causes errors or poor UX
- ❌ **Guardrail Violation**: Key metric degrades >10%
- ❌ **Sample Ratio Mismatch**: Traffic split significantly off (e.g., 60/40 instead of 50/50)
- ✅ **Decisive Win**: Treatment clearly winning with high confidence (rare)

**Mid-Experiment Checkpoint** ([Date - halfway through]):
- Review preliminary results (DO NOT make decision yet)
- Check if experiment is running as expected
- Extend duration if sample size not reached

---

## Analysis Plan

### Statistical Approach

**Test Type**: [Two-sample t-test | Chi-square test | Mann-Whitney U test]

**Success Criteria**:
- **Primary metric shows**: [+X%] lift
- **Statistical significance**: p-value < 0.05
- **Practical significance**: Lift meets or exceeds MDE
- **Guardrails**: No metrics degraded beyond thresholds

**Confidence Level**: 95% (α = 0.05)

**Multiple Testing Correction**: [Bonferroni | None - explain]

---

### Decision Tree

**Scenario 1: Statistically Significant Positive Result**
- **Condition**: p < 0.05, Treatment > Control, Lift ≥ MDE
- **Decision**: ✅ **Ship to 100%**
- **Next Steps**: Implement treatment for all users, document learnings

**Scenario 2: No Significant Difference**
- **Condition**: p ≥ 0.05, or Lift < MDE
- **Decision**: 🔄 **Iterate or Kill**
- **Next Steps**: Analyze why hypothesis failed, consider alternative approaches

**Scenario 3: Statistically Significant Negative Result**
- **Condition**: p < 0.05, Treatment < Control
- **Decision**: 🚫 **Kill Immediately**
- **Next Steps**: Revert to control, understand why hypothesis was wrong

**Scenario 4: Guardrail Violation**
- **Condition**: Any guardrail metric degraded beyond threshold
- **Decision**: 🚫 **Kill** (even if primary metric improved)
- **Next Steps**: Cannot harm user experience for marginal gains

---

### Segmented Analysis (Secondary Analysis)

**Segments to Analyze**:
1. **New vs Returning Users**: Did effect differ?
2. **Desktop vs Mobile**: Platform-specific effects?
3. **Traffic Source**: Organic vs paid vs direct?
4. **Geographic**: US vs international?

**Rationale**: May reveal that treatment works well for specific segment

**Note**: Segmented analysis is exploratory, do not make decisions solely on segment results

---

## Risk Management

**Risks**:

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Experiment harms conversion | Medium | High | Guardrail metrics, early stop criteria |
| Insufficient traffic to reach sample size | Low | Medium | Extend duration, increase exposure |
| Tracking implementation error | Low | High | QA in staging, verify events day 1 |
| Novelty effect (users react to "new" not better) | Medium | Medium | Run long enough for novelty to fade (2+ weeks) |

---

## Results (To Be Filled After Experiment)

### Primary Metric Results

| Variant | Sample Size | Conversion Rate | Lift vs Control | p-value | Confidence Interval |
|---------|-------------|-----------------|-----------------|---------|---------------------|
| Control A | [N] | [X]% | - | - | - |
| Treatment B | [N] | [Y]% | +[Z]% | [p] | [[Low] - [High]] |

**Statistical Significance**: [Yes | No]

**Practical Significance**: [Yes | No] (Did lift meet MDE?)

**Winner**: [Control | Treatment | No Winner]

---

### Secondary Metrics Results

| Metric | Control | Treatment | Change | p-value |
|--------|---------|-----------|--------|---------|
| [Metric 2] | [X] | [Y] | [+/-Z%] | [p] |
| [Metric 3] | [X] | [Y] | [+/-Z%] | [p] |

---

### Guardrail Metrics Results

| Guardrail | Control | Treatment | Change | Threshold | Pass/Fail |
|-----------|---------|-----------|--------|-----------|-----------|
| [Metric A] | [X] | [Y] | [+/-Z%] | <10% | ✅ Pass |
| [Metric B] | [X] | [Y] | [+/-Z%] | <5% | ✅ Pass |

**All Guardrails Passed**: [Yes | No]

---

## Final Decision

**Decision**: ✅ Ship | 🔄 Iterate | 🚫 Kill

**Rationale**:
[Why this decision based on results]

**Confidence**: [High | Medium | Low]

**Next Steps**:
1. [Action 1]
2. [Action 2]
3. [Action 3]

---

## Learnings & Insights

**What We Learned**:
1. [Insight 1 - what worked or didn't work]
2. [Insight 2 - unexpected findings]
3. [Insight 3 - implications for future experiments]

**Why Hypothesis Was Right/Wrong**:
[Analysis of why outcome matched or didn't match prediction]

**Implications for Roadmap**:
[How this changes product priorities or approach]

**Follow-Up Experiments**:
- [Experiment idea 1 based on learnings]
- [Experiment idea 2]

```

---

## Best Practices

### DO ✅

- **Test one variable** - Isolate what's causing the effect
- **Run to completion** - Don't stop early unless critical issue
- **Calculate sample size upfront** - Know how long experiment needs to run
- **Use guardrail metrics** - Prevent harming user experience for marginal gains
- **Document everything** - Record hypothesis, results, learnings
- **Run long enough** - Typically 1-2 full business cycles minimum
- **Check sample ratio** - 50/50 split should stay 50/50
- **Consider seasonality** - Avoid starting experiments before holidays/events

### DON'T ❌

- **Don't peek and stop** - Checking results mid-experiment increases false positive rate
- **Don't test multiple things** - Can't tell which change caused effect
- **Don't ignore guardrails** - Small primary metric win + big guardrail harm = bad outcome
- **Don't run underpowered experiments** - Too small sample = can't detect real effects
- **Don't assume causation** - Correlation ≠ causation, confirm hypothesis makes sense
- **Don't forget mobile** - Test on all platforms users use
- **Don't ignore segment differences** - Effect may be strong for one segment, weak for others

---

## Model

Use: Sonnet

---

## Related

- `/pm:impact` - Estimate expected impact before experiment
- `/pm:metrics` - Define KPIs and success metrics
- `/workflows:growth-sprint` - Growth experimentation workflow
- `data-scientist` agent - Statistical analysis and experiment design
- `growth-pm` agent - Growth strategy and experiment prioritization
