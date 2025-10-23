---
description: Calculate TAM, SAM, and SOM for market opportunity assessment
category: Analysis
model: haiku
---

# Market Sizing

Comprehensive market sizing analysis using TAM, SAM, and SOM frameworks to evaluate market opportunity.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: Haiku).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Product/Service**: What are you sizing the market for?
- **Target market**: Geographic, industry, or customer segment
- **Business model**: Pricing model and customer type (B2B/B2C)
- **Context**: New market, expansion, or validation
- **Known data** (optional): Any market research or data points

## Output

### Market Size Summary

**TAM** (Total Addressable Market): $[X] - Total revenue if 100% market share
**SAM** (Serviceable Addressable Market): $[Y] ([%] of TAM) - Realistic addressable segment
**SOM** (Serviceable Obtainable Market): $[Z] ([%] of SAM) - Achievable short-term (1-3yr)

```
TAM: $[X] (all potential customers)
  ↓ (geographic/segment/channel constraints)
SAM: $[Y] ([%] of TAM)
  ↓ (realistic penetration [X]% market share)
SOM: $[Z] ([%] of SAM)
```

**Market Attractiveness**: [High/Medium/Low] based on size, growth, competition

### TAM Calculation

**Top-Down** (industry reports): Market size $[X]B × segment [Y]% × geography [Z]% = $[TAM]
**Bottom-Up** (unit economics): [N] potential customers × $[ACV] = $[TAM]
**Value Theory**: Total value $[X] × value chain % [Y] = $[TAM]

**Cross-validation**: Top-down $[X], Bottom-up $[Y], Value $[Z] → **Final TAM**: $[validated]
**Sources**: [Gartner/Forrester/IDC/IBISWorld reports cited]

### SAM Calculation

**Narrowing TAM to SAM**:
```
SAM = TAM × Geographic% × Product% × Channel% × Regulatory% × Segment%
SAM = $[TAM] × [multipliers] = $[SAM] ([X]% of TAM)
```

**Constraints**: [Geographic: regions served], [Product: solution fit], [Channel: go-to-market], [Regulatory: compliance], [Segment: target customers]

### SOM Calculation

**Realistic Capture** (Yr 1-3):
- Yr 1: SAM × [1-3]% share = $[X]
- Yr 3: SAM × [3-10]% share = $[Y]

**Factors**: Competition ([N] competitors, [H/M/L] concentration), GTM capability ($[X] budget, team size), Product maturity ([stage])

**Reality Check**: [N] customers needed @ $[ACV] = [X] customers/month acquisition rate (feasible?)

### Growth & Segmentation

**Market Growth**: Historical [X]% CAGR, Projected [Y]% CAGR → [Growing/Stable/Declining]

| Year | TAM | SAM | SOM |
|------|-----|-----|-----|
| 2024 | $[X] | $[Y] | $[Z] |
| 2025 | $[X] | $[Y] | $[Z] |
| 2026 | $[X] | $[Y] | $[Z] |

**Segmentation** (by size/industry/geography):
- [Segment 1]: $[X] ([Y]% of SAM) - [Target/Not target]
- [Segment 2]: $[X] ([Y]% of SAM) - [Target/Not target]
- **Initial Target**: [Segment], $[X], [Rationale]

### Customer Economics

**Yr 1 Targets**: SOM $[X] ÷ $[ACV] = [N] customers = [X]/month acquisition
**Feasibility**: CAC $[X], [N]mo sales cycle, [X]% conversion → Pipeline: [N] leads/month (achievable?)

| Quarter | New Customers | Cumulative | ARR |
|---------|---------------|------------|-----|
| Q1-Q4 | [progression shown] | [build-up] | [growth] |

### Key Assumptions & Validation

**Assumptions**: [N] customers, $[ACV] pricing, [X]% adoption, [Y]% penetration
**Critical to Validate**: [List 2-3 most important assumptions]
**Data Quality**: [High/Medium/Low] confidence based on [sources and recency]
**Sensitivity**: If TAM 50% smaller → SOM $[X] (still attractive? [Y/N])

## Example

```
/market-sizing Product: AI sales forecasting. Market: B2B SaaS NA. Model: $15-100K ACV. Context: New launch, need investment justification. Data: Gartner estimates sales tech $15B, 12% growth.
```

## Methodologies

**Top-Down**: Industry reports → segment → geography (fast, less accurate)
**Bottom-Up**: Count customers × revenue/customer (accurate, labor-intensive)
**Value Theory**: Total value × value chain % (new categories)
**Best practice**: Use multiple, triangulate

## Common Mistakes

❌ Overestimating TAM (non-customers, wrong pricing), Confusing TAM/SAM/SOM, Ignoring competition, Static sizing, False precision
✅ Be conservative (esp. SOM), show your work, use ranges, validate with data, update regularly

**Related**: `/tools/competitive-positioning`, `/workflows/market-entry`, `/tools/roi-calculator`, `/tools/assumption-mapping`
