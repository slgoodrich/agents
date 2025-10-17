# Experiment Designer

Design A/B tests and growth experiments with hypothesis, metrics, and analysis plan.

## Usage

```
/pm:experiment [hypothesis or feature to test]
```

## What This Command Does

Creates rigorous experiment design including hypothesis, variants, success metrics, sample size, and analysis plan.

## Instructions

1. Formulate hypothesis:
   - We believe [change]
   - Will result in [outcome]
   - For [user segment]
   - We'll measure [metric]

2. Design experiment:
   - Control vs treatment variants
   - Primary and secondary metrics
   - Sample size calculation
   - Duration needed
   - Success criteria

3. Analysis plan:
   - Statistical significance threshold
   - Minimum detectable effect
   - Guardrail metrics

## Template

```markdown
# Experiment: [Name]

**Status**: Draft | Running | Complete
**Owner**: [Name]
**Duration**: [Weeks]

---

## Hypothesis

**We believe that** [specific change]
**Will result in** [expected outcome]
**For** [user segment]
**We will measure** [primary metric]

**Example**:
*We believe that* adding social proof (# of users) on signup page
*Will result in* 15% increase in conversion
*For* new visitors from paid ads
*We will measure* signup conversion rate

---

## Experiment Design

### Variants

**Control (A)**: [Current experience - 50% traffic]
[Description or screenshot]

**Treatment (B)**: [Proposed change - 50% traffic]
[Description or screenshot]

---

## Success Metrics

### Primary Metric
**Metric**: [Metric name]
- **Baseline**: [Current value]
- **Minimum Detectable Effect**: [% change needed]
- **Target**: [Goal value]
- **Significance**: 95% confidence, p < 0.05

### Secondary Metrics
- **[Metric 2]**: Expected to [increase/decrease]
- **[Metric 3]**: Expected to [increase/decrease]

### Guardrail Metrics
- **[Metric A]**: Should not decrease
- **[Metric B]**: Should not increase

---

## Sample Size

**Calculation**:
- Baseline conversion: [X]%
- Minimum detectable effect: [Y]%
- Power: 80%
- Significance: 95%

**Sample size needed**: [N per variant]
**Expected duration**: [Days to reach sample]

---

## Experiment Plan

**Start Date**: [Date]
**Traffic Split**: 50/50
**Ramp**: 10% → 50% over 2 days
**Duration**: [Days]
**End Date**: [Date]

**Feature Flag**: `experiment_[name]_[variant]`

---

## Analysis Plan

**Success Criteria**:
- Primary metric shows +[X]% lift
- p-value < 0.05
- No negative impact on guardrails

**Decision Tree**:
- If significant positive: Ship to 100%
- If no difference: Iterate or kill
- If significant negative: Kill immediately

---

## Results (Post-Experiment)

**Primary Metric**:
- Control: [X]%
- Treatment: [Y]%
- **Lift**: +[Z]% (p=[value])

**Decision**:  Ship | 🔄 Iterate |  Kill

**Learnings**:
- [Insight 1]
- [Insight 2]

**Next Steps**:
- [Action based on results]
```

## Model
claude-sonnet-4-5

## Related
- `/pm:kpi-dashboard` - Metrics to test
- `/pm:growth` - Growth strategies
