---
name: market-sizing-frameworks
description: Master TAM/SAM/SOM calculations, market sizing methodologies, and validation frameworks. Use when assessing market opportunity, validating business viability, planning market entry, estimating revenue potential, or determining if a market is worth pursuing. Covers bottom-up, top-down, and value theory sizing methods, competitive analysis, and systematic validation approaches.
---

# Market Sizing Frameworks

Frameworks and methodologies for estimating market size and validating market opportunity.

## Overview

Market sizing answers the critical question: "Is this opportunity large enough to pursue?" It provides the foundation for strategic decisions, resource allocation, and investment prioritization.

**Core Principle:** Market sizing is educated guessing with documented assumptions. The goal is reasonable estimates and order-of-magnitude accuracy (is it $1M, $10M, or $100M?), not false precision.

**Key Insight:** Always use multiple methods (bottom-up, top-down, value theory) to triangulate and validate estimates. If methods disagree by more than 2-3x, your assumptions need scrutiny.

---

## When to Use This Skill

**Auto-loaded by agents**:
- `market-analyst` - For TAM/SAM/SOM calculation and market validation

**Use when you need to**:
- Assess if a market opportunity is worth pursuing
- Calculate TAM, SAM, and SOM for business planning
- Validate market assumptions before building
- Support fundraising or strategic planning
- Evaluate competitive landscape impact on opportunity
- Determine realistic revenue projections

---

## The Three-Tier Framework

### TAM (Total Addressable Market)

**Definition:** Total revenue opportunity if you achieved 100% market share globally.

**Purpose:** Understand the absolute ceiling of opportunity.

**Typical Range:**
- Side project: $1M+ TAM minimum
- Full-time business: $10M+ TAM minimum
- VC-backed startup: $100M+ TAM minimum

**Calculation:** See three methods below.

---

### SAM (Serviceable Addressable Market)

**Definition:** Portion of TAM you can realistically serve given your business model, geography, and product capabilities.

**Purpose:** Your realistic target market after applying real-world constraints.

**Filters to Apply:**
1. **Geographic reach:** Where can you operate?
2. **Customer segment:** Which types of customers fit your solution?
3. **Product capabilities:** Who can your product actually serve?
4. **Distribution channels:** Who can you reach?

**Typical Range:** SAM is usually 10-40% of TAM for focused products.

**Formula:**
```
SAM = TAM × Geographic % × Segment % × Product Fit % × Distribution %
```

---

### SOM (Serviceable Obtainable Market)

**Definition:** Portion of SAM you can realistically capture in the near term (1-3 years).

**Purpose:** Your achievable revenue target given resources, competition, and time constraints.

**Realistic Benchmarks:**
- Year 1: 0.1-0.5% of SAM (new products)
- Year 3: 1-5% of SAM (if successful)
- Year 5: 5-15% of SAM (market leader position)

**Formula:**
```
SOM = SAM × Realistic Market Share %
```

**Reality Check:** Convert SOM to customer count. Is that number achievable per month/week?

---

## Three Market Sizing Methods

Always use all three methods for robust validation. If they disagree significantly, investigate your assumptions.

### Method 1: Bottom-Up (Most Reliable)

**Approach:** Count actual customers and multiply by revenue per customer.

**Formula:**
```
TAM = Total Potential Customers × Average Revenue per Customer
```

**Process:**
1. Define who is a potential customer (be specific!)
2. Count them using reliable data sources
3. Apply realistic adoption/penetration filters
4. Estimate average annual revenue per customer
5. Multiply to get TAM

**Strengths:**
- Most grounded in reality
- Easy to validate assumptions
- Can name actual customers

**When to Use:** Always start here as your primary method.

**Complete methodology:** See `references/market-sizing-methodologies.md` for detailed step-by-step process with examples.

---

### Method 2: Top-Down (For Validation)

**Approach:** Start with total market size and estimate your segment percentage.

**Formula:**
```
TAM = Total Market Size × Your Segment %
```

**Process:**
1. Find comparable market size data (Gartner, IDC, etc.)
2. Identify what percentage is your specific segment
3. Apply multiple filters to narrow down
4. Compare to bottom-up calculation

**Strengths:**
- Quick sanity check
- Uses industry research
- Good for validation

**Weaknesses:**
- Often produces inflated numbers
- Hard to validate percentages
- Can feel like guesswork

**When to Use:** As secondary validation, never as primary method.

**Complete methodology:** See `references/market-sizing-methodologies.md` for examples and industry applications.

---

### Method 3: Value Theory

**Approach:** Calculate value created for customers, then estimate capture rate.

**Formula:**
```
TAM = (Value Created per Customer × Potential Customers) × Capture Rate %
```

**Process:**
1. Quantify value delivered (time saved, cost reduced, revenue increased)
2. Calculate dollar value of that benefit
3. Determine what percentage you can capture in pricing (typically 10-30%)
4. Multiply by potential customer base

**Strengths:**
- Tests pricing assumptions
- Grounds estimates in customer value
- Helps justify pricing strategy

**When to Use:** To validate pricing is reasonable relative to value created.

**Complete methodology:** See `references/market-sizing-methodologies.md` for value calculation frameworks.

---

## Validation Framework

### The Reality Check Questions

Before trusting your market sizing, validate with these critical tests:

**1. Can you name 10 specific potential customers?**
- If no: Market may be too narrow or unclear
- If yes: Proceed with confidence

**2. Are there existing competitors making money?**
- If yes: Market is validated (good!)
- If no: Either no market exists OR huge greenfield (risky)

**3. Does TAM > SAM > SOM make sense?**
- Progression should be logical
- SAM typically 10-40% of TAM
- SOM Year 1 typically 0.1-1% of SAM

**4. Is Year 1 SOM achievable with your resources?**
- Convert to customer count per month
- Is that acquisition rate realistic?
- Do you have budget/capacity?

**5. Is the market big enough to justify effort?**
- Minimum thresholds matter
- Compare to your goals (bootstrap vs VC)

**Complete validation checklist:** See `assets/market-validation-checklist.md` for comprehensive 100+ point validation framework.

---

## Common Mistakes to Avoid

1. **Confusing TAM with SAM** - Be explicit which number you're discussing
2. **Top-down only sizing** - Always validate with bottom-up
3. **Ignoring competition** - Available market is smaller than total market
4. **Assuming linear growth** - Use S-curves, not straight lines
5. **No customer names** - If you can't name 10 customers, market may not exist
6. **One-and-done sizing** - Update assumptions quarterly as you learn

**Detailed guide:** See `references/market-sizing-best-practices.md` for:
- How to avoid each mistake
- Industry-specific considerations
- Competitive landscape analysis
- Assumption management frameworks
- Sensitivity analysis approaches
- Case studies (Superhuman, Quibi, Figma, Slack)

---

## Recommended Workflow

### Step 1: Bottom-Up Calculation (Primary)

Use this as your primary estimate:

1. Define universe of potential customers (be specific)
2. Count them using reliable data sources
3. Estimate realistic adoption/penetration percentage
4. Determine average annual revenue per customer
5. Calculate: TAM = Customers × Adoption % × Price

**Tool:** Use `assets/market-sizing-calculator.md` for step-by-step worksheet with formulas.

---

### Step 2: Top-Down Validation (Secondary)

Validate your bottom-up with industry data:

1. Find comparable market size from research firms
2. Estimate what percentage is your segment
3. Compare to bottom-up calculation
4. If within 2-3x: Good confidence
5. If >5x difference: Investigate assumptions

---

### Step 3: Value Theory Check

Test pricing reasonableness:

1. Quantify value delivered to customers
2. Calculate dollar value of benefits
3. Determine capture rate (10-30% typical)
4. Validate pricing is within reasonable range

---

### Step 4: Apply SAM Filters

Narrow TAM to realistic serviceable market:

```
Starting TAM: $__________

Geographic filter: × ____% = $__________
Segment filter: × ____% = $__________
Product fit filter: × ____% = $__________
Distribution filter: × ____% = $__________

Final SAM: $__________
```

**Template:** Use `assets/tam-sam-som-template.md` for complete calculation template.

---

### Step 5: Calculate Realistic SOM

Project achievable market capture:

**Conservative Approach:**
- Year 1: 0.1-0.3% of SAM
- Year 2: 0.5-1% of SAM
- Year 3: 1-3% of SAM

**Consider:**
- Competitive intensity (high = lower %)
- Switching costs (high = lower %)
- Your differentiation (strong = higher %)
- Distribution advantage (strong = higher %)

---

### Step 6: Validate Thoroughly

Run through comprehensive validation:

1. Complete all reality checks
2. Verify unit economics work (LTV:CAC ratio)
3. Check competitive landscape math
4. Model three scenarios (pessimistic, base, optimistic)
5. Conduct sensitivity analysis on key assumptions

**Validation tool:** Use `assets/market-validation-checklist.md` for systematic validation.

---

### Step 7: Document Assumptions

Critical for updating as you learn:

```markdown
## Key Assumptions

1. Customer count: [number]
   - Source: [where this came from]
   - Confidence: [High/Medium/Low]
   - Impact if wrong: [+/- X% on TAM]

2. Pricing: $[amount]/year
   - Basis: [competitive analysis, value-based, etc.]
   - Confidence: [High/Medium/Low]
   - Impact if wrong: [direct 1:1 impact]

3. Adoption rate: [%]
   - Basis: [customer interviews, analogies, etc.]
   - Confidence: [High/Medium/Low]
   - Impact if wrong: [+/- X% on TAM]
```

---

## Templates and Tools

### Calculation Tools

**Complete TAM/SAM/SOM Template:**
- `assets/tam-sam-som-template.md`
- Full calculation framework with all filters
- Includes validation checklist
- Assumption documentation section
- Sensitivity analysis worksheet

**Step-by-Step Calculator:**
- `assets/market-sizing-calculator.md`
- All three methods with formulas
- Worked examples
- Comparison framework
- Confidence scoring

**Validation Checklist:**
- `assets/market-validation-checklist.md`
- 100+ validation points
- Reality checks and red flags
- Customer count validation
- Pricing validation
- Competitive validation

---

## Reference Guides

### Comprehensive Methodologies

**Complete Methods Guide:**
- `references/market-sizing-methodologies.md`
- Detailed bottom-up, top-down, and value theory processes
- Industry-specific approaches (B2B SaaS, Consumer, Enterprise, Marketplace, Dev Tools)
- Method comparison and triangulation
- Data source recommendations

**Best Practices Guide:**
- `references/market-sizing-best-practices.md`
- Common mistakes and how to avoid them
- Validation frameworks
- Competitive landscape analysis
- Assumption management
- Sensitivity analysis
- Case studies: Superhuman, Quibi, Figma, Slack
- Advanced considerations (timing, geographic expansion, platform effects)

---

## Summary

**Market sizing is educated guessing** - the goal is reasonable estimates with documented assumptions, not precision.

**The Three-Step Approach:**
1. **Calculate:** Use all three methods (bottom-up, top-down, value theory)
2. **Validate:** Reality-check with customers, competition, and economics
3. **Document:** Track assumptions and update quarterly

**Key Principles:**
- Always start with bottom-up (most reliable)
- Use top-down only for validation
- Can you name 10 customers? (Critical test)
- Update assumptions as you learn
- Model three scenarios (pessimistic, base, optimistic)

**Decision Framework:**
- If SAM < $10M: Too small for most ventures
- If Year 1 SOM < $50K: Question if worth effort
- If methods disagree >5x: Assumptions need work
- If no competitors exist: Either no market OR huge opportunity (validate carefully)

---

## Related Skills

- `product-positioning` - Position against competitive landscape
- `product-market-fit` - Validate market demand exists
- `competitive-analysis-templates` - Analyze market attractiveness and competitive dynamics
