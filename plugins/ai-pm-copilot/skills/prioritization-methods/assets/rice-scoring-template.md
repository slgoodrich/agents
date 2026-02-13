# RICE Scoring Template

## Formula

**RICE Score = (Reach × Impact × Confidence) / Effort**

## Scoring Guide

### Reach

How many users/customers will this impact per time period (typically per quarter)?

- Enter as a number (e.g., 5000, 10000)
- Be specific about the time period

### Impact

How much will this move the key metric when a user encounters it?

- **3.0** = Massive impact
- **2.0** = High impact
- **1.0** = Medium impact
- **0.5** = Low impact
- **0.25** = Minimal impact

### Confidence

How confident are you in your Reach and Impact estimates?

- **100%** = High confidence (strong data, user research, past experience)
- **80%** = Medium confidence (some data, reasonable assumptions)
- **50%** = Low confidence (little data, many assumptions)

### Effort

How much total team time will this take to build, test, and launch?

- Enter in person-months (e.g., 0.5, 1, 2, 3)
- Include design, engineering, QA, launch effort
- Factor in complexity and unknowns

## Scoring Template

| Feature   | Reach | Impact | Confidence | Effort | RICE Score | Rank |
| --------- | ----- | ------ | ---------- | ------ | ---------- | ---- |
| Feature A | 10000 | 2.0    | 80%        | 2.0    | 8000       |      |
| Feature B | 5000  | 3.0    | 100%       | 1.5    | 10000      |      |
| Feature C | 2000  | 1.0    | 50%        | 0.5    | 2000       |      |
| Feature D | 8000  | 0.5    | 80%        | 3.0    | 1067       |      |
| Feature E |       |        |            |        |            |      |

## Example

**Feature: Dark Mode**

- **Reach**: 10,000 users/quarter (50% of 20,000 MAU use product in evening)
- **Impact**: 2.0 (High - reduces eye strain, table stakes feature many request)
- **Confidence**: 80% (user research shows demand + 50 support requests)
- **Effort**: 1.5 person-months (design 0.5 + engineering 0.75 + testing 0.25)

**RICE Score = (10,000 × 2.0 × 0.80) / 1.5 = 10,667**

## Tips

- **Be consistent** with time periods (always quarterly, or always monthly)
- **Document assumptions** in a notes column
- **Calibrate as a team** - discuss scoring together to align
- **Update regularly** as you learn more about reach and impact
- **Don't game the system** - honest estimates produce better decisions
- **Combine with qualitative factors** - RICE is input, not the only input

## Next Steps

1. Fill in the template for all features in your backlog
2. Sort by RICE score (highest to lowest)
3. Validate top priorities align with strategy
4. Adjust for dependencies and sequencing
5. Document prioritization rationale for future reference
