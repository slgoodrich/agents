---
description: Create flexible, outcome-focused roadmaps using the Now-Next-Later framework
category: Planning
model: haiku
---

# Now-Next-Later Roadmap

Build flexible, outcome-oriented roadmaps that communicate strategy without rigid timelines using the Now-Next-Later framework.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: Haiku).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Product/Team**: What are you roadmapping?
- **Timeframe**: Overall planning horizon (e.g., next 6-12 months)
- **Strategic goals**: OKRs or key objectives
- **Context**: Current priorities, constraints, opportunities

## Output

Three-column roadmap (Now-Next-Later):

### NOW (0-3 months) - High confidence, active work

**Initiative 1: [Name]**
- Problem: [Why this matters]
- Outcome: [What success looks like]
- Metrics: [How we measure]
- Dependencies: [What it relies on]
- Owner: [Team/person]

[Repeat for 3-5 NOW initiatives]

**NOW Characteristics**: In progress/starting, high confidence, resources committed, validated problem-solution

### NEXT (3-6 months) - Medium confidence, planned

**Initiative 1: [Name]**
- Opportunity: [Strategic importance]
- Hypothesis: [What we believe]
- Success criteria: [How we know it works]
- Open questions: [What to learn]
- Effort: [S/M/L]
- Prerequisites: [Dependencies]

[Repeat for 5-8 NEXT initiatives]

**NEXT Characteristics**: Planned not started, some discovery needed, may shift based on NOW learnings

### LATER (6+ months) - Low confidence, ideas

**Theme 1: [Broad opportunity]**
- Alignment: [How supports goals]
- Value: [Why interesting]
- Unknowns: [What we don't know]
- Exploration: [Discovery needed]

[Repeat for 8-12 LATER themes]

**LATER Characteristics**: Ideas/opportunities, significant unknowns, may or may not happen

### Strategic Themes (across columns)

**Theme 1: [e.g., Platform Scalability]**
- NOW: [Initiative(s)]
- NEXT: [Initiative(s)]  
- LATER: [Initiative(s)]

[Repeat for 2-3 key themes]

### Roadmap Metadata

**Last Updated**: [Date]
**Key Assumptions**: [What must be true]
**NOT on Roadmap**: Ops, bugs, experiments, support (ongoing work)
**How it Works**: Review [frequency], items move based on [learnings/priorities]


## Example

```
/now-next-later Product: B2B collaboration. Timeframe: 12mo. Goals: +30% activation, -20% churn, expand to enterprise. Context: 15 engineers, SMB focus, strong PMF.
```

## Benefits

**Flexibility**: No rigid dates, easy to adjust, embraces uncertainty
**Outcome-focused**: Results over features, strategic alignment visible
**Honest**: Clear confidence levels, acknowledges unknowns, realistic expectations
**Continuous**: Regular updates, learning-driven, responsive to change

## vs Other Roadmaps

- **Timeline** (Gantt): Rigid dates (use when committed deliveries)
- **Feature List**: No strategy (use for team planning)
- **Now-Next-Later**: Flexible, outcome-focused, strategic (use for agile teams)

## Maintenance

**Monthly**: Move NEXT→NOW, complete items, update confidence, add new LATER ideas
**Quarterly**: Strategic alignment check, OKR progress, major reprioritization
**Include**: Strategic initiatives, new capabilities, major improvements, platform investments
**Exclude**: Bugs, maintenance, individual stories, every experiment

**Related**: `/strategic-planning:roadmap-builder`, `/strategic-planning:okr-framework`, `/tools/impact-mapping`
