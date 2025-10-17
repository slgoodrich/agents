# KPI Dashboard Builder

Define and structure product KPIs and metrics dashboards.

## Usage

```
/pm:kpi-dashboard [product or feature name]
```

## What This Command Does

Creates comprehensive KPI framework with North Star metric, primary/secondary metrics, and tracking plan.

## Instructions

1. Define metric hierarchy:
   - North Star Metric (single most important)
   - Primary metrics (3-5 key drivers)
   - Secondary metrics (supporting indicators)
   - Counter metrics (guard rails)

2. For each metric specify:
   - Definition and calculation
   - Why it matters
   - Current baseline
   - Target
   - Tracking method

## Template

```markdown
# KPI Dashboard: [Product]

## North Star Metric
**Metric**: [Single most important metric]
**Why**: [How this represents product value]
**Current**: [Baseline]
**Target**: [Goal]

---

## Primary Metrics

### 1. [Metric Name]
**Definition**: [How calculated]
**Current**: [Value]
**Target**: [Goal by when]
**Why it matters**: [Business/user impact]
**Tracking**: [Tool, frequency]

### 2. [Metric Name]
[Same structure]

---

## AARRR Framework

### Acquisition
- **Signups**: [Current] → [Target]
- **CAC**: [Current] → [Target]
- **Organic %**: [Current] → [Target]

### Activation
- **Activation Rate**: [Current] → [Target]
- **Time to Value**: [Current] → [Target]

### Retention
- **D1/D7/D30**: [Current] → [Target]
- **Churn Rate**: [Current] → [Target]

### Revenue
- **MRR**: [Current] → [Target]
- **ARPU**: [Current] → [Target]

### Referral
- **k-factor**: [Current] → [Target]
- **NPS**: [Current] → [Target]

---

## Counter Metrics (Watch for negative impact)
- **[Metric]**: Should not exceed [threshold]
- **[Metric]**: Should not drop below [threshold]

---

## Weekly Dashboard

| Metric | Week | Trend | Status | Notes |
|--------|------|-------|--------|-------|
| North Star | [Value] | ↗️ +5% | 🟢 | On track |
| Primary 1 | [Value] | → 0% | 🟡 | Flat |
| Primary 2 | [Value] | ↘️ -3% | 🔴 | Investigating |
```

## Model
claude-sonnet-4-5

## Related
- `/pm:okr` - OKRs aligned to KPIs
- `/pm:experiment` - Test metric improvements
