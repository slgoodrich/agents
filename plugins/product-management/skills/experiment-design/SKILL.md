---
name: experiment-design
description: A/B testing, multivariate testing, and experiment frameworks for product optimization.
---

# Experiment Design

## Overview
Scientific approach to testing hypotheses and making data-driven product decisions through controlled experiments.

## Experiment Types

### A/B Testing
**Compare two variants**
- Control (A) vs Treatment (B)
- Single variable change
- Clear winner determination

### Multivariate Testing
**Test multiple variables**
- Multiple changes simultaneously
- Interaction effects
- Requires more traffic

### Multi-Armed Bandit
**Adaptive allocation**
- Dynamically shift traffic to winners
- Minimize opportunity cost
- Good for content optimization

## Experiment Framework

### 1. Hypothesis Formation
**Format**: If [change], then [outcome], because [rationale]

**Example**: If we add social proof to signup page, then conversion will increase by 15%, because users trust validated products

### 2. Experiment Design
- **Independent variable** - What you change
- **Dependent variable** - What you measure
- **Success metrics** - Primary and secondary
- **Sample size** - Required for significance

### 3. Implementation
- Random assignment
- Proper instrumentation
- QA and validation
- Monitoring for bugs

### 4. Analysis
- Statistical significance (p < 0.05)
- Practical significance (meaningful impact)
- Segment analysis
- Guardrail metrics

### 5. Decision
- Ship, iterate, or abandon
- Document learnings
- Plan follow-up experiments

## Statistical Concepts

### Sample Size Calculation
Factors:
- Baseline conversion rate
- Minimum detectable effect (MDE)
- Statistical power (typically 80%)
- Significance level (typically 5%)

### Common Pitfalls
- **Peeking** - Checking results too early
- **Multiple comparisons** - Testing too many variants
- **Novelty effect** - Initial excitement bias
- **Simpson's paradox** - Segment contradictions

## Experiment Velocity

### Rapid Experimentation
- Small, focused tests
- Quick iterations
- Learning > winning
- Build experiment culture

### Prioritization
- **ICE Score**: Impact × Confidence × Ease
- Expected value
- Risk assessment
- Resource requirements

## Guardrail Metrics
Ensure no harm while optimizing
- User experience metrics
- Technical performance
- Brand metrics
- Business KPIs

## Experiment Documentation

### Experiment Brief
- Hypothesis
- Design and variants
- Success metrics
- Timeline

### Results Report
- Data and analysis
- Statistical significance
- Learnings
- Recommendations
- Next steps

## When to Use
Feature optimization, conversion optimization, messaging tests, pricing experiments, UX improvements
