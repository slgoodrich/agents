# OKR Framework

Create quarterly or annual OKRs (Objectives and Key Results) aligned to strategy.

## Usage

```
/pm:okr [period: Q1 2025, H1 2025, 2025] [optional: strategic focus]
```

## What This Command Does

1. Generates OKRs following Google's framework
2. Creates measurable, ambitious key results
3. Cascades from company to team to individual OKRs
4. Provides tracking framework and success criteria
5. Aligns OKRs to product strategy

## Instructions

1. **Gather Context**:
   - Time period (quarter, half, year)
   - Company/product strategy
   - Current metrics baseline
   - Team size and capacity
   - Previous OKR performance

2. **Create OKRs**:
   - **Objectives**: Inspiring, qualitative goals (3-5 per period)
   - **Key Results**: Measurable outcomes (3-5 per objective)
   - Mix of output and outcome metrics
   - Stretch goals (70% achievement is success)

3. **Structure**:
   ```
   Objective: [Inspiring, qualitative goal]

   Key Result 1: [Metric] from [X] to [Y] by [Date]
   Key Result 2: [Milestone/Achievement] by [Date]
   Key Result 3: [Percentage/Number] reaches [Target]

   Initiatives: [How we'll achieve this]
   ```

4. **Ensure Quality**:
   - Objectives are inspirational, not tasks
   - Key Results are measurable and time-bound
   - Ambitious but achievable (60-70% confidence)
   - Clear ownership
   - Aligned to company goals

## Template

```markdown
## [Period] OKRs: [Product/Team Name]

**Owner**: [Name]
**Period**: [Dates]
**Status**: Draft | Active | Completed

---

### Objective 1: [Inspiring Goal]

**Why this matters**: [Strategic importance]

**Key Results**:
1. **[Metric Name]** increases from [Baseline] to [Target] by [Date]
   - Current: [X]
   - Target: [Y]
   - Tracking: [How measured]

2. **[Achievement/Milestone]** completed by [Date]
   - Definition of done: [Criteria]
   - Dependencies: [What's needed]

3. **[Percentage/Adoption]** reaches [Target]%
   - Baseline: [X]%
   - Target: [Y]%
   - Measurement: [Method]

**Initiatives** (how we'll get there):
- [Initiative 1]: [Description]
- [Initiative 2]: [Description]
- [Initiative 3]: [Description]

**Confidence**: [Low/Medium/High] - [Reasoning]

---

### Objective 2: [Another Goal]
[Same structure]

---

## Alignment

**Company OKRs**: [How this connects to company goals]

**Dependencies**:
- [Team/Function]: [What we need from them]
- [Team/Function]: [What they need from us]

**Resources Required**:
- Team: [Headcount, skills]
- Budget: [$ amount]
- Tools/Infrastructure: [Technical needs]

---

## Scoring Guide

**0.0-0.3**: We failed (need to understand why)
**0.4-0.6**: Made progress but fell short
**0.7-0.9**: Succeeded (target zone)
**1.0+**: Over-achieved (sandbagged?)

---

## Weekly Check-in Template

| Key Result | Week | Progress | On Track? | Blockers |
|------------|------|----------|-----------|----------|
| KR 1.1 | Week 4 | 0.3 | 🟢 Yes | None |
| KR 1.2 | Week 4 | 0.1 | 🟡 At risk | Need design |
| KR 1.3 | Week 4 | 0.0 | 🔴 Behind | Blocked |
```

## Example

**Input**: "Create Q2 2025 OKRs for growth"

**Output**:

```markdown
## Q2 2025 OKRs: Growth Team

### Objective 1: Make the product indispensable for daily workflows

**Why**: Current DAU/MAU is 25% (industry best 40%+). Need habit formation.

**Key Results**:
1. **DAU/MAU ratio** increases from 25% to 40% by June 30
   - Current: 25% (5K DAU / 20K MAU)
   - Target: 40% (8K DAU / 20K MAU)
   - Tracking: Mixpanel daily

2. **Push notification engagement** reaches 35% open rate
   - Baseline: 12%
   - Target: 35%
   - Smart timing ML model deployed

3. **Users returning within 24 hours** grows to 60%
   - Current: 35%
   - Target: 60%
   - Sticky features shipped

**Initiatives**:
- Daily digest feature with personalized content
- Smart push notification system
- Quick-action home screen widgets
- Improved onboarding to showcase daily value

**Confidence**: Medium-High (0.65)

---

### Objective 2: Achieve viral growth through product

**Key Results**:
1. **Viral coefficient (k-factor)** reaches 0.7 from current 0.3
2. **Share rate** grows to 25% of users sharing monthly
3. **Invite conversion** improves from 30% to 50%

**Initiatives**:
- In-product sharing at "aha moment"
- Referral incentive program (both parties win)
- Team collaboration features

**Confidence**: Medium (0.5) - Requires product changes
```

## Model

Use: claude-sonnet-4-5

## Related

- `/pm:roadmap` - Roadmap aligned to OKRs
- `/pm:quarterly-planning` - Detailed quarterly plan
- `/pm:metrics` - Define KPIs to track
