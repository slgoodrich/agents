---
description: Systematic evaluation of costs versus benefits for product decisions and investments
category: Analysis
model: haiku
---

# Cost-Benefit Analysis

Comprehensive cost-benefit analysis to evaluate whether a product initiative, feature, or investment is worthwhile.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Initiative**: What are you evaluating? (feature, product, project, investment)
- **Context**: Current situation, why considering this
- **Timeframe**: Planning horizon (e.g., 12 months, 3 years)
- **Known costs/benefits** (optional): Information you already have

## Output

Cost-benefit analysis with recommendation:

### Executive Summary
- **Initiative**: [Description]
- **Net benefit**: $[Benefits - Costs]
- **Benefit-cost ratio**: [Benefits ÷ Costs]:1 (>2:1 is strong)
- **Payback period**: [Months]
- **Recommendation**: Go / No-go / Need more data
- **Key insight**: [Main takeaway]

### Benefits Analysis

**Quantitative Benefits** ($):
- Revenue: New customers $[X], increased conversion $[Y], reduced churn $[Z], upsell $[W]
- Cost savings: Support $[X], operations $[Y], infrastructure $[Z]
- Productivity: Team time $[X], faster TTM $[Y]
- **Total Quantified**: $[Sum]

**Qualitative Benefits** (H/M/L importance):
- Customer satisfaction, brand perception, competitive differentiation, strategic positioning, market learning, team morale, platform capabilities, risk mitigation

### Cost Analysis

**Development**: Engineering $[X], design $[Y], PM $[Z], QA $[W] = $[Sum]
**Infrastructure**: Cloud $[X]/mo, third-party $[Y]/mo, tools $[Z]/mo
**Go-to-Market**: Marketing $[X], sales $[Y], docs $[Z]
**Operational** (ongoing): Support $[X]/mo, monitoring $[Y]/mo, CS $[Z]/mo
**Opportunity Cost**: Delayed initiatives $[X]
**Risk/Contingency** (20%): $[X]

**Total Costs**: $[One-time] + $[Recurring × timeframe] = $[Total]

### Timeline & ROI

| Timeframe | Cumulative Benefits | Cumulative Costs | Net |
|-----------|---------------------|------------------|-----|
| Q1 (building) | $0 | $50K | -$50K |
| Q2 | $10K | $75K | -$65K |
| Q3 | $50K | $90K | -$40K |
| Q4 | $120K | $100K | +$20K |
| Year 2 | $300K | $130K | +$170K |

**Break-even**: Month [X] | **Time to positive ROI**: Month [Y]

### Scenario Analysis

| Scenario | Benefits | Costs | Net Benefit | BCR | Probability |
|----------|----------|-------|-------------|-----|-------------|
| Best case (+30% benefits, -15% costs) | $[X] | $[Y] | $[X-Y] | [R]:1 | 20% |
| Expected (base) | $[X] | $[Y] | $[X-Y] | [R]:1 | 60% |
| Worst case (-30% benefits, +30% costs) | $[X] | $[Y] | $[X-Y] | [R]:1 | 20% |

**Sensitivity**: Adoption ±10% = $[X] change | Dev time +2mo = $[Y] cost | Conversion ±5% = $[Z] change

### Strategic Considerations

**Strategic value** (beyond numbers):
- Strategy alignment: [How supports vision/goals]
- Competitive position: [Strengthens/maintains/no impact]
- Market learning: [What we'll learn]
- Platform investment: [Future capabilities enabled]
- Customer relationships: [Impact on trust/loyalty]
- Team development: [Critical capabilities built]

**Qualitative factors**: Technical debt, organizational complexity, change management, cultural fit

### Alternatives Comparison

| Option | Net Benefit | BCR | Payback | Strategic Value |
|--------|-------------|-----|---------|-----------------|
| **Option A** (This) | $[X] | [R]:1 | [M]mo | High/Med/Low |
| **Option B** (Alt) | $[Y] | [R]:1 | [M]mo | High/Med/Low |
| **Option C** (Do nothing) | $0 | N/A | N/A | Declining |

**Recommended**: [Option and why]

### Risk Assessment

**Execution risks**: Technical complexity, resource availability, timeline uncertainty, third-party dependencies
**Market risks**: Lower adoption, competition response, timing, economic conditions
**Impact**: [Likelihood × Impact for each | Mitigation strategies]

### Decision Framework

**Go if**: Net benefit >$[threshold], BCR >2:1, Payback <18mo, High strategic alignment, Acceptable risk
**No-go if**: Negative net benefit, BCR <1:1, Payback >3yrs, High risk + low strategic value
**Need more data if**: Unclear estimates, high sensitivity, strategic value uncertain

### Recommendation

**Decision**: [Go / No-go / Pilot / Defer]

**Rationale**:
- Financial case: [Strong/Moderate/Weak] - [1-2 sentences]
- Strategic case: [Strong/Moderate/Weak] - [1-2 sentences]
- Risk assessment: [Acceptable/Manageable/High] - [Key risks]
- Confidence level: [High/Medium/Low] - [Based on what]

**Conditions for success**:
1. [Assumption 1 must hold]
2. [Execution requirement 2]
3. [Critical success factor 3]

**Next steps**:
- [Validation needed]
- [De-risking actions]
- [When to revisit decision]

**Monitoring plan**: Track [metrics], review [frequency], adjust if [conditions]

## Example

```
/cost-benefit-analysis Building native mobile app (iOS + Android). Context: Web-only SaaS, competitors have apps, 20% users on mobile web, $200K MRR, 15 eng team. Timeframe: 3 years.
```

## Tips

✅ **DO**: Be realistic (conservative benefits, generous costs), quantify when possible, include all costs (opportunity + ongoing), consider timing and cash flow, acknowledge uncertainty (scenarios), capture strategic value

❌ **DON'T**: Overestimate benefits (optimistic adoption), underestimate costs (forget ongoing/opportunity), ignore timing (discount future), analysis paralysis (80% confidence enough), sunk cost fallacy (past costs don't matter)

**Related**: `/tools/roi-calculator`, `/tools/trade-off-analysis`, `/tools/assumption-mapping`
