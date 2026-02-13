# Opportunity Scoring Template (Jobs-to-be-Done)

## Overview

Opportunity Scoring identifies underserved customer needs by measuring the gap between importance and satisfaction for each job-to-be-done.

## Formula

**Opportunity Score = Importance + Max(Importance - Satisfaction, 0)**

Range: 0-10 (higher = more opportunity)

## Step 1: Identify Customer Jobs

List the outcomes customers want to achieve (not features).

### Example Jobs (Project Management Tool)

1. Quickly find past tasks and decisions
2. Understand project progress at a glance
3. Coordinate work across team members
4. Prioritize tasks based on impact
5. Track time spent on different activities
6. Share project status with the team
7. Ensure nothing falls through the cracks

## Step 2: Survey Customers

For each job, ask two questions:

### Importance Question

"How important is it that you can **[job]**?"

Scale: 1 (not important) to 5 (extremely important)

### Satisfaction Question

"How satisfied are you with your current ability to **[job]**?"

Scale: 1 (very dissatisfied) to 5 (very satisfied)

## Step 3: Calculate Opportunity Scores

### Opportunity Scoring Template

| Job   | Importance (1-5) | Satisfaction (1-5) | Gap | Opportunity Score | Priority |
| ----- | ---------------- | ------------------ | --- | ----------------- | -------- |
| Job 1 | 4.5              | 2.0                | 2.5 | 7.0               | High     |
| Job 2 | 3.0              | 2.8                | 0.2 | 3.2               | Low      |
| Job 3 | 4.8              | 4.2                | 0.6 | 5.4               | Medium   |
| Job 4 | 5.0              | 3.5                | 1.5 | 6.5               | High     |

**Calculation Examples**:

Job 1: Opportunity = 4.5 + (4.5 - 2.0) = 7.0
Job 2: Opportunity = 3.0 + (3.0 - 2.8) = 3.2
Job 3: Opportunity = 4.8 + (4.8 - 4.2) = 5.4

## Step 4: Interpret Scores

### Opportunity Segments

**Overserved (Low Opportunity < 4.0)**

- Low importance OR high satisfaction
- **Strategy**: Maintain, don't over-invest

**Appropriately Served (Medium 4.0-7.0)**

- Balanced importance and satisfaction
- **Strategy**: Incremental improvements

**Underserved (High Opportunity > 7.0)**

- High importance + low satisfaction = big gap
- **Strategy**: Major innovation opportunity

## Complete Example

### Product: Team Collaboration Tool

Survey Results (20 users):

| Job                             | Importance | Satisfaction | Opportunity | Interpretation                  |
| ------------------------------- | ---------- | ------------ | ----------- | ------------------------------- |
| Quickly find past conversations | 4.5        | 2.0          | 7.0         | **UNDERSERVED** → Build search  |
| Share files with team           | 4.2        | 4.5          | 4.2         | Appropriately served            |
| Get notified of mentions        | 3.8        | 4.0          | 3.8         | Appropriately served            |
| See who's online now            | 2.5        | 2.2          | 2.8         | Overserved → Low priority       |
| Track project milestones        | 4.8        | 3.2          | 6.4         | **UNDERSERVED** → Build tracker |
| Integrate with other tools      | 4.0        | 2.5          | 5.5         | Underserved → Add integrations  |
| Customize notification settings | 3.5        | 4.2          | 3.5         | Appropriately served            |

### Priority Recommendations

**P0 (Opportunity > 7.0)**:

- Quickly find past conversations (7.0) → Build powerful search

**P1 (Opportunity 6.0-7.0)**:

- Track project milestones (6.4) → Build milestone tracker

**P2 (Opportunity 5.0-6.0)**:

- Integrate with other tools (5.5) → Add top integrations

**Low Priority (Opportunity < 5.0)**:

- Everything else is appropriately/overserved

## Opportunity Matrix Visualization

```
High Importance
      │
      │ Underserved     │ Appropriately
      │ (Big Gap)       │ Served
      │ INVEST HERE     │ (Satisfied)
      │                 │
──────┼─────────────────┼──────────
      │                 │
      │ Overserved      │ Low Priority
      │ (Low Import)    │
      │                 │
    Low ←──────────────→ High
           Satisfaction
```

## Tips

- **Focus on jobs, not features** - "Find information fast" not "Add search"
- **Survey 15-30 customers** for reliable patterns
- **Segment by persona** - Different users, different opportunities
- **Use exact quotes** - Understand the job in customer language
- **Validate with usage data** - Do behaviors match stated importance?
- **Track over time** - Opportunity scores change as you build
- **Combine with RICE** - Opportunity informs impact, add reach/effort

## When to Use Opportunity Scoring

- **Outcome-driven innovation** - Focus on customer jobs, not features
- **Understanding underserved needs** - Where's the biggest gap?
- **Feature gap analysis** - What to build vs competitors?
- **Roadmap planning** - Prioritize by customer opportunity
- **Validation before building** - Is this job actually important?

## Common Patterns

### High Importance + Low Satisfaction = Opportunity

Users desperately need this, current solutions fail
→ **Your biggest opportunity for impact**

### High Importance + High Satisfaction = Competitive

Others already serve this well
→ **Table stakes, don't differentiate here**

### Low Importance + Low Satisfaction = Ignore

Users don't care AND aren't satisfied
→ **Don't invest, won't move needle**

### Low Importance + High Satisfaction = Over-Investing

You're solving a problem users don't prioritize
→ **Redirect resources to high-importance jobs**

## Next Steps

1. Identify 8-12 customer jobs (outcomes, not features)
2. Create survey with importance + satisfaction questions
3. Survey 15-30 target customers
4. Calculate opportunity scores for each job
5. Prioritize: High opportunity (>7.0) → Medium (5-7) → Low (<5.0)
6. Map jobs to features: "To help users [job], we'll build [feature]"
7. Build roadmap focused on highest-opportunity jobs
8. Track satisfaction over time, iterate
