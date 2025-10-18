---
name: technical-debt-management
description: Frameworks for identifying, prioritizing, and managing technical debt.
---

# Technical Debt Management

## Overview
Systematic approach to managing the implied cost of additional rework caused by choosing quick solutions over better approaches.

## Types of Technical Debt

### Deliberate Debt
- **Strategic** - Conscious decision to move faster
- **Tactical** - Known shortcuts with plan to fix

### Accidental Debt
- **Outdated technology** - Aging systems
- **Learning** - Better approach discovered later
- **Bit rot** - Code deterioration over time

## Technical Debt Quadrant

### Reckless vs Prudent
**Reckless**: "We don't have time for design"
**Prudent**: "We must ship now and deal with consequences"

### Deliberate vs Inadvertent
**Deliberate**: Conscious decision
**Inadvertent**: "Now we know how we should have done it"

## Assessment Framework

### Impact Analysis
- **Velocity impact** - Slowing development
- **Quality impact** - Increasing bugs
- **Risk impact** - Potential failures
- **Morale impact** - Developer frustration

### Debt Metrics
- **Code complexity** - Cyclomatic complexity
- **Test coverage** - Gaps in testing
- **Code churn** - Frequent changes
- **Bug density** - Defects per module
- **Build time** - Increasing durations

## Prioritization

### Priority Matrix
- **High impact, easy fix** - Do first
- **High impact, hard fix** - Plan and schedule
- **Low impact, easy fix** - Background work
- **Low impact, hard fix** - Consider ignoring

### Business Value Alignment
- Revenue impact
- Customer satisfaction
- Team velocity
- Risk mitigation

## Management Strategies

### Dedicated Time
- 20% rule (1 day per week)
- Every Nth sprint
- Quarterly cleanup sprints

### Incremental Improvement
- Boy Scout Rule (leave code better)
- Refactor as you go
- No new debt policy

### Strategic Rewrites
- Module-by-module replacement
- Strangler pattern
- Big bang (high risk)

## Documentation
- **Debt register** - Track all debt
- **Interest calculation** - Ongoing cost
- **Repayment plan** - Remediation strategy
- **Prevention** - Avoid new debt

## When to Use
Sprint planning, quarterly planning, architecture reviews, velocity concerns
