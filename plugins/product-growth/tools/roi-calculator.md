---
name: ROI Calculator
description: Calculate return on investment for product initiatives and business cases
category: Analysis
model: haiku
---

# ROI Calculator

Calculate financial return on investment for product features, initiatives, and business cases with detailed modeling.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: Haiku).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Investment**: What are you investing in?
- **Investment amount**: Costs (one-time and recurring)
- **Expected returns**: Revenue, savings, or value created
- **Timeframe**: Period to analyze (e.g., 12 months, 3 years)
- **Context**: Industry, business model, stage

## Output

ROI analysis with key metrics:

### ROI Summary

**Simple ROI**: `(Returns - Investment) ÷ Investment × 100%` = **[X]%**
**Payback Period**: **[Z] months** (<12 good, <18 acceptable, >24 risky)
**NPV**: **$[NPV]** (positive = worthwhile)
**IRR**: **[X]%** (compare to 15-25% hurdle rate)

### Investment Breakdown

**Initial Investment**:
- Development: $[X] ([N] engineers × [M] months × $[rate])
- Infrastructure/Marketing/Training: $[Y]
- Contingency (15-20%): $[Z]
- **Total Initial**: $[Sum]

**Recurring Costs** (annual):
- Maintenance, hosting, operations, marketing: $[X]/year
- **Total over [N] years**: $[Initial + (Recurring × Years)]

### Returns Breakdown

**Revenue Returns** (Year 1):
- New customers: [N] × $[ACV] = $[X]
- Increased conversion (+[X]%): $[Y]
- Reduced churn (-[X]%): $[Z]
- Upsell/expansion (+[X]%): $[W]
- **Year 1 Total**: $[Sum]

**Years 2-3**: Apply [X]% growth rate, compounding effects
**Total Revenue ([N] years)**: $[Sum]

**Cost Savings** (annual):
- Support, efficiency, infrastructure, automation: $[X]/year
- **Total Savings ([N] years)**: $[Sum]

**Total Returns**: $[Revenue + Savings]

### Time-Based Analysis

| Period | Investment | Returns | Net | Cumulative |
|--------|-----------|---------|-----|------------|
| 0-3mo | -$50K | $0 | -$50K | -$50K |
| 4-6mo | -$25K | $5K | -$20K | -$70K |
| 7-12mo | -$20K | $40K | +$20K | -$50K |
| Yr 2 | -$30K | $150K | +$120K | +$70K |
| Yr 3 | -$30K | $250K | +$220K | +$290K |

**Break-even**: Month [X] | **ROI**: 6mo: [X]%, 12mo: [Y]%, 24mo: [Z]%

### Scenario Modeling

| Scenario | Returns | ROI | Payback | Acceptable? |
|----------|---------|-----|---------|-------------|
| Conservative (70%) | Lower adoption, higher costs | [X]% | [Y]mo | [Yes/No] |
| Expected (100%) | Most likely estimates | [X]% | [Y]mo | Base case |
| Optimistic (130%) | Higher adoption, lower costs | [X]% | [Y]mo | Stretch goal |

**Risk-adjusted ROI**: [X]% (weighted by probability)

### Key Assumptions

**Revenue**: [N] customers/mo, $[ACV], [X]% conversion, [Y]% churn, [Z]% growth
**Costs**: [N] people × [M] months × $[rate], $[X] infrastructure
**Market**: [N] potential customers, [X]% penetration achievable

**Critical assumptions to validate**: [List 2-3 most important]

### Sensitivity Analysis

| Variable Change | ROI Impact | Payback Impact | Priority |
|----------------|-----------|---------------|----------|
| Customer acq -20% | [X]% → [Y]% | [M]mo → [N]mo | High |
| Dev time +50% | [X]% → [Y]% | +$[Z] cost | Medium |
| Conversion +30% | [X]% → [Y]% | [M]mo → [N]mo | Low |

**Break-even thresholds**: Min [N] customers, max [M] months dev, min [X]% conversion

### Recommendation

**Financial**: ROI [X]%, Payback [Y]mo, NPV $[Z] → [Strong/Moderate/Weak]
**Risk**: [Low/Medium/High] based on sensitivity and downside scenarios
**Decision**: [Proceed/Defer/Reject/Pilot]

**Proceed if**: ROI >[X]%, Payback <[Y]mo
**Conditions**: Validate [key assumptions], monitor [metrics]

## Example

```
/roi-calculator Building enterprise SSO: $200K dev (4 eng, 3mo) + $30K/yr maintenance. Returns: 50 enterprise customers @ $20K ACV (vs $10K), churn 8% → 5%. Timeframe: 3 years. B2B SaaS.
```

## Formulas

- **Simple ROI**: `(Gain - Cost) / Cost × 100%`
- **NPV**: `Σ[CashFlow/(1+r)^t] - Investment` (discount rate 10-15%)
- **IRR**: Discount rate where NPV = 0 (compare to 15-25% hurdle)
- **Payback**: `Investment / Avg Annual CashFlow`

## Benchmarks

| Type | Good ROI | Payback |
|------|----------|---------|
| Product features | >200% (12mo) | <12mo |
| Enterprise features | 150-300% | 12-18mo |
| Platform investments | 300-500%+ | 18-36mo |

## Best Practices

✅ Be conservative, validate assumptions, include all costs, update regularly
❌ Avoid overoptimism, missing costs, ignoring time value, false precision

**Related**: `/tools/cost-benefit-analysis`, `/pm:impact-estimator`, `/tools/market-sizing`
