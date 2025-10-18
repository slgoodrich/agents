---
name: Technical Debt Assessment
description: Evaluate technical debt, quantify impact, and prioritize remediation
category: Analysis
model: haiku
---

# Technical Debt Assessment

Comprehensive framework for identifying, measuring, and managing technical debt to balance speed with long-term code health.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: Haiku).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Scope**: Codebase, feature area, or system to assess
- **Context**: Team size, product stage, recent changes
- **Pain points** (optional): Known issues or concerns
- **Goals**: What you're trying to understand or decide

## Output

### Executive Summary

**Debt Level**: [Critical/High/Medium/Low] | **Total**: [X] eng-months | **Velocity Tax**: [Y]%
**Payback**: [Z] months | **Recommendation**: [Immediate/Planned/Monitor/Acceptable]

**Top 3 Debt Areas**:
1. [Area] - [High/Med/Low] impact
2. [Area] - [High/Med/Low] impact
3. [Area] - [High/Med/Low] impact

**Key Insight**: [Main takeaway]

### Debt Inventory

| Category | Severity | Key Issues | Effort |
|----------|----------|------------|--------|
| **Code Quality** | [H/M/L] | Complex code ([N] modules), low coverage ([X]%), poor docs, duplication | [X]wk |
| **Architecture** | [H/M/L] | Tight coupling, poor SoC, scalability bottlenecks, missing abstractions | [X]wk |
| **Infrastructure** | [H/M/L] | Outdated deps ([N] libs, [N] vulns), deployment complexity, monitoring gaps | [X]wk |
| **Data** | [H/M/L] | Schema issues, data quality, missing indexes ([N] slow queries) | [X]wk |
| **Design** | [H/M/L] | UX inconsistencies, legacy UI patterns | [X]wk |
| **Process** | [H/M/L] | Manual processes, missing tooling | [X]wk |

**Total Debt**: [Sum] eng-weeks

### Impact Analysis

| Impact Area | Current State | Cost/Year |
|-------------|---------------|-----------|
| **Velocity** | [Y]% time on debt, [Y]% slower than optimal | $[X] |
| **Quality** | [X] bugs/sprint ([Y]% debt-related), [N] incidents | $[Y] |
| **Morale** | [X]/10 satisfaction, [H/M/L] turnover risk | $[Z] |
| **Business** | [N] features delayed, [Y]% quality churn | $[W] |

**Total Annual Cost**: $[Sum] | **Interest Rate**: [X]% (debt cost / eng budget)

### Debt Quadrant (Fowler)

| | Reckless | Prudent |
|-----------|----------|---------|
| **Deliberate** | No plan, cut corners | Conscious trade-offs, documented |
| **Inadvertent** | No design thought | Learning debt, emergent |

**Implications**: Reckless = cultural fix; Prudent/Deliberate = plan payback; Prudent/Inadvertent = continuous refactoring

### Prioritization Matrix

**Priority Score** = Pain (1-10) / Effort (1-10)

| Quadrant | Pain | Effort | Action |
|----------|------|--------|--------|
| **Quick Wins** | High | Low | Do immediately |
| **Strategic** | High | High | Plan & schedule |
| **Low Priority** | Low | Low | Do when convenient |
| **Money Pits** | Low | High | Avoid/workaround |

**Top 5 Items**:
1. [Item] - Pain: [X], Effort: [Y], Score: [Z]
2-5. [Continue...]

### Root Causes & Prevention

| Category | Top Causes | Prevention |
|----------|-----------|------------|
| **Process** | No refactor time, weak reviews | Reserve 20% capacity, enforce reviews |
| **Skills** | Learning curve, missing expertise | Training, pair programming |
| **Organizational** | Ship pressure, changing reqs | Empower "no" |
| **Technical** | Domain complexity, legacy constraints | Better abstractions |

### Metrics & Trends

**Current**: Complexity [X] (target <10), Coverage [X]% (target >80%), Violations [N] (target 0)
**Trend**: [Improving/Stable/Degrading]  
**Tools**: SonarQube [X]%, CodeClimate [Grade], CodeQL [N] alerts

### Remediation Roadmap

| Timeline | Actions | Effort |
|----------|---------|--------|
| **This Sprint** | Quick wins, critical fixes | [Y]d ([Z]% capacity) |
| **Next Quarter** | Strategic projects | [Y]wk |
| **6-12 months** | Major refactors | [X]mo |
| **Continuous** | Reserve [X]% sprint, Boy Scout Rule, monthly review | Ongoing |

**Target**: Reduce from [X]wk to [Y]wk debt in 12mo ([Z]% reduction)

### Investment Options

| Option | Capacity | Duration | Outcome | Trade-off |
|--------|----------|----------|---------|-----------|
| Aggressive | 40-50% | 2-3mo | Fast cleanup | Features slow |
| Steady | 20-30% | 6-12mo | Balanced | Longer timeline |
| Minimal | 10-15% | 12-18mo | Debt stable | Slow progress |
| Rewrite | Dedicated | 6-12mo | Clean slate | High risk |

**Recommended**: [Option X] - [Rationale]

### Risk Assessment

**Not addressing**: Velocity -[X]%/yr, quality -[Y]%, turnover +[Z]%, cost $[growing]  
**Addressing**: Features -[X]% for [Y]mo, opportunity cost $[Z]  
**Mitigation**: Communicate, focus high-impact first, show progress
## Example Prompt

```
Assess technical debt for:
- Scope: Core payment processing service
- Context: 2-year-old codebase, 5 engineers, scaling from 1K to 10K transactions/day
- Pain points: Slow test suite (30 min), frequent payment failures, hard to add features
- Goals: Decide whether to refactor or rewrite, justify engineering investment
```

## Example

```
/technical-debt-assessment Scope: Payment service. Context: 2yr old, 5 engineers, scaling 1K→10K txn/day. Pain: Slow tests (30min), frequent failures, hard to add features. Goal: Refactor vs rewrite decision.
```

## Assessment Methods

**Automated**: SonarQube, CodeClimate, Snyk/Dependabot, CodeQL, coverage tools
**Manual**: Code reviews, dev surveys, architecture reviews, performance profiling, incident analysis
**Metrics**: Complexity, coverage%, build time, deployment frequency, MTTR
**Signals**: Dev complaints, velocity trends, bug rates, new hire ramp-up time

## Best Practices

✅ Make debt visible, track in backlog, reserve 15-25% capacity, prioritize by impact, celebrate improvements
❌ Not all debt must be paid, some debt acceptable, strategic trade-offs, business context matters

**Related**: `/skills/technical-debt-management`, `/pm:sprint-planner`, `/tools/trade-off-analysis`, `/pm:roadmap-builder`
