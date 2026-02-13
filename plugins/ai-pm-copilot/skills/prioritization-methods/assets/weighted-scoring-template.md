# Weighted Scoring Template

## Overview

Weighted scoring allows you to define custom criteria and their relative importance, then score features against each criterion to calculate a total weighted score.

## Step 1: Define Criteria and Weights

Criteria must sum to 100%.

| Criterion              | Weight   | Rationale                         |
| ---------------------- | -------- | --------------------------------- |
| User Value             | 40%      | Primary driver of product success |
| Revenue Impact         | 30%      | Business sustainability           |
| Strategic Fit          | 20%      | Alignment with company goals      |
| Ease of Implementation | 10%      | Resource constraints              |
| **Total**              | **100%** |                                   |

## Step 2: Score Each Feature

Score each feature on each criterion (1-10 scale).

### Feature Scoring Template

| Feature   | User Value (1-10) | Revenue Impact (1-10) | Strategic Fit (1-10) | Ease (1-10) | Weighted Score | Rank |
| --------- | ----------------- | --------------------- | -------------------- | ----------- | -------------- | ---- |
| Feature A | 8                 | 6                     | 9                    | 5           |                |      |
| Feature B | 6                 | 9                     | 7                    | 8           |                |      |
| Feature C | 9                 | 4                     | 8                    | 3           |                |      |
| Feature D |                   |                       |                      |             |                |      |

## Step 3: Calculate Weighted Scores

**Formula**: (Criterion1 Score × Weight1) + (Criterion2 Score × Weight2) + ...

### Example Calculation

**Feature: Analytics Dashboard**

Scores:

- User Value: 8/10
- Revenue Impact: 6/10
- Strategic Fit: 9/10
- Ease: 5/10

Calculation:

```
Weighted Score = (8 × 0.40) + (6 × 0.30) + (9 × 0.20) + (5 × 0.10)
               = 3.2 + 1.8 + 1.8 + 0.5
               = 7.3/10
```

## Complete Example

### Criteria Weights

- User Value: 40%
- Revenue Impact: 30%
- Strategic Fit: 20%
- Ease: 10%

### Feature Scores

| Feature             | User Value | Revenue | Strategic | Ease | Weighted Score | Rank |
| ------------------- | ---------- | ------- | --------- | ---- | -------------- | ---- |
| Analytics Dashboard | 8          | 6       | 9         | 5    | 7.3            | 2    |
| Email Notifications | 7          | 5       | 6         | 8    | 6.5            | 3    |
| API Access          | 6          | 9       | 8         | 4    | 7.1            | 3    |
| Dark Mode           | 9          | 3       | 5         | 7    | 6.6            | 4    |
| Mobile App          | 10         | 8       | 9         | 2    | 7.9            | 1    |

**Priority Order**: Mobile App (7.9) → Analytics (7.3) → API (7.1) → Dark Mode (6.6) → Email (6.5)

## Custom Criteria Examples

### B2B SaaS Product

- Customer Value: 35%
- Revenue Impact: 30%
- Competitive Differentiation: 20%
- Implementation Cost: 15%

### Consumer Mobile App

- User Engagement: 40%
- Virality Potential: 25%
- Monetization: 20%
- Development Effort: 15%

### Internal Tool

- Time Savings: 50%
- User Adoption Likelihood: 25%
- Maintenance Cost: 15%
- Implementation Effort: 10%

### Platform/API Product

- Developer Value: 35%
- Platform Adoption: 30%
- Revenue Model Fit: 20%
- Technical Complexity: 15%

## Scoring Guides

### User Value (1-10)

- 10: Solves critical pain, users will switch for this
- 7-9: Significant improvement to experience
- 4-6: Nice improvement, not game-changing
- 1-3: Marginal benefit

### Revenue Impact (1-10)

- 10: Direct revenue driver, proven monetization
- 7-9: Likely revenue increase, strong logic
- 4-6: Indirect revenue benefit
- 1-3: No clear revenue impact

### Strategic Fit (1-10)

- 10: Directly advances key strategic goal
- 7-9: Supports strategic direction
- 4-6: Loosely aligned
- 1-3: Off-strategy

### Ease of Implementation (1-10)

- 10: Hours to 1 day
- 7-9: 2-5 days
- 4-6: 1-2 weeks
- 1-3: 3+ weeks

## Tips

- **Define criteria collaboratively** - Get clarity on weights
- **Be transparent** - Show calculation, not just final score
- **Document assumptions** - Why these weights? Why these scores?
- **Avoid gaming** - Use ranges, discuss outliers
- **Combine with qualitative** - Scores inform, don't dictate
- **Re-weight periodically** - Criteria importance changes over time

## When to Use Weighted Scoring

- **Multiple priorities** to balance (product, sales, eng, exec)
- **Complex decisions** with many factors
- **Executive alignment** needed (transparent, defensible)
- **Custom criteria** that standard frameworks don't capture

## Common Mistakes

❌ **Too many criteria** (8+ makes it unwieldy)
✓ **4-5 key criteria** that matter most

❌ **Equal weights** (defeats the purpose)
✓ **Meaningful weights** that reflect priorities

❌ **Hidden criteria** (unstated biases)
✓ **Explicit criteria** everyone agrees on

❌ **Set and forget** (criteria stale)
✓ **Refresh quarterly** as strategy evolves

## Next Steps

1. Define 4-5 key criteria for your product
2. Assign weights (must sum to 100%)
3. Define and agree on criteria/weights
4. Score each feature (1-10) on each criterion
5. Calculate weighted scores
6. Sort by score, validate top priorities
7. Document and communicate decisions
8. Track accuracy, refine scoring over time
