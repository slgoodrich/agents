---
name: prioritization-methods
description: Apply RICE, ICE, MoSCoW, Kano, and Value vs Effort frameworks. Use when prioritizing features, roadmap planning, or making trade-off decisions.
---

# Prioritization Methods & Frameworks

## Overview

Data-driven frameworks for feature prioritization, backlog ranking, and MVP scoping. Choose the right framework based on your context: data availability, team size, and decision type.

## When to Use This Skill

**Auto-loaded by agents**:

- `feature-prioritizer` - For RICE/ICE scoring, MVP scoping, and backlog ranking

**Use when you need**:

- Choosing between competing features
- Building quarterly roadmaps
- Backlog prioritization
- Saying "no" with evidence
- Clear prioritization decisions
- Resource allocation decisions
- MVP scoping decisions

---

## Seven Core Frameworks

### 1. RICE Scoring (Intercom)

**Formula**: (Reach × Impact × Confidence) / Effort

**Best for**: Large backlogs (20+ items) with quantitative data

**Components**:

- **Reach**: Users impacted per quarter
- **Impact**: 0.25 (minimal) to 3 (massive)
- **Confidence**: 50% (low data) to 100% (high data)
- **Effort**: Person-months to ship

**Example**:

```
Dark Mode: (10,000 × 2.0 × 0.80) / 1.5 = 10,667
```

**When to use**: Post-PMF with metrics, need defendable priorities, data-driven culture

**Template**: `assets/rice-scoring-template.md`

---

### 2. ICE Scoring (Sean Ellis)

**Formula**: (Impact + Confidence + Ease) / 3

**Best for**: Quick experiments, early-stage products, limited data

**Components** (each 1-10):

- **Impact**: How much will this move the needle?
- **Confidence**: How sure are we?
- **Ease**: How simple to implement?

**Example**:

```
Email Notifications: (8 + 9 + 7) / 3 = 8.0
```

**When to use**: Growth experiments, startups, need speed over rigor

**Template**: `assets/ice-scoring-template.md`

---

### 3. Value vs Effort Matrix (2×2)

**Quadrants**:

- **Quick Wins** (high value, low effort) - Do first
- **Big Bets** (high value, high effort) - Strategic
- **Fill-Ins** (low value, low effort) - If capacity
- **Time Sinks** (low value, high effort) - Avoid

**Best for**: Visual presentations, portfolio planning, quick assessments

**When to use**: Clear communication, strategic planning, need visualization

**Template**: `assets/value-effort-matrix-template.md`

---

### 4. MoSCoW Method

**Categories**:

- **Must Have** (60%) - Critical for launch
- **Should Have** (20%) - Important but not critical
- **Could Have** (20%) - Nice-to-have
- **Won't Have** - Explicitly out of scope

**Best for**: MVP scoping, release planning, clear scope decisions

**When to use**: Fixed timeline, need to cut scope, binary go/no-go decisions

**Template**: `assets/moscow-prioritization-template.md`

---

### 5. Kano Model

**Categories**:

- **Basic Needs (Must-Be)**: Expected, dissatisfiers if absent
- **Performance Needs**: More is better, linear satisfaction
- **Excitement Needs (Delighters)**: Unexpected joy
- **Indifferent**: Users don't care
- **Reverse**: Users prefer without it

**Best for**: Understanding user expectations, competitive positioning, roadmap sequencing

**When to use**: Strategic planning, differentiation strategy, multi-release planning

**Template**: `assets/kano-model-template.md`

---

### 6. Weighted Scoring

**Process**:

1. Define criteria (User Value, Revenue, Strategic Fit, Effort)
2. Assign weights (must sum to 100%)
3. Score features (1-10) on each criterion
4. Calculate weighted score

**Example**:

```
Criteria: User Value 40%, Revenue 30%, Strategic 20%, Ease 10%
Feature: (8 × 0.40) + (6 × 0.30) + (9 × 0.20) + (5 × 0.10) = 7.3
```

**Best for**: Multiple criteria, complex trade-offs, custom needs

**When to use**: Balancing priorities, transparent decisions

**Template**: `assets/weighted-scoring-template.md`

---

### 7. Opportunity Scoring (Jobs-to-be-Done)

**Formula**: Importance + Max(Importance - Satisfaction, 0)

**Process**:

1. Identify customer jobs (outcomes, not features)
2. Survey: Rate importance (1-5) and satisfaction (1-5)
3. Calculate opportunity = importance + gap
4. Prioritize high-opportunity jobs (>7.0)

**Best for**: Outcome-driven innovation, understanding underserved needs, feature gap analysis

**When to use**: JTBD methodology, finding innovation opportunities, validation

**Template**: `assets/opportunity-scoring-template.md`

---

## Choosing the Right Framework

**Need speed?** → ICE (fastest)

**Have user data?** → RICE (most rigorous)

**Visual presentation?** → Value/Effort (clear visualization)

**MVP scoping?** → MoSCoW (forces cuts)

**User expectations?** → Kano (strategic insights)

**Complex criteria?** → Weighted Scoring (custom)

**Outcome-focused?** → Opportunity Scoring (JTBD)

**Detailed comparison**: `references/framework-selection-guide.md`

Complete decision tree, framework comparison table, combining strategies

---

## Best Practices

**1. Be Consistent**

- Use same framework across team
- Document assumptions explicitly
- Update scores as you learn

**2. Combine Frameworks**

- RICE for ranking + Value/Effort for visualization
- MoSCoW for release + RICE for roadmap
- Kano for strategy + ICE for tactics

**3. Avoid Common Pitfalls**

- Don't prioritize by HiPPO (Highest Paid Person's Opinion)
- Don't ignore effort (value alone insufficient)
- Don't set-and-forget (re-prioritize regularly)
- Don't game the system (honest scoring)

**4. Clear Communication**

- Show your work (transparent criteria)
- Visualize priorities clearly
- Explain trade-offs explicitly
- Document "why not" for rejected items

**5. Iterate and Learn**

- Track actual vs estimated impact
- Refine scoring over time
- Calibrate team estimates
- Learn from misses

---

## Templates and References

### Assets (Ready-to-Use Templates)

Copy-paste these for immediate use:

- `assets/rice-scoring-template.md` - Reach × Impact × Confidence / Effort
- `assets/ice-scoring-template.md` - Impact + Confidence + Ease / 3
- `assets/value-effort-matrix-template.md` - 2×2 visualization
- `assets/moscow-prioritization-template.md` - Must/Should/Could/Won't
- `assets/kano-model-template.md` - Expectation analysis
- `assets/weighted-scoring-template.md` - Custom criteria scoring
- `assets/opportunity-scoring-template.md` - Jobs-to-be-done prioritization

### References (Deep Dives)

When you need comprehensive guidance:

- `references/framework-selection-guide.md` - Choose the right framework, comparison table, combining strategies, decision tree

---

## Quick Reference

```
Problem: Too many features, limited resources
Solution: Use prioritization framework

Context-Based Selection:
├─ Lots of data? → RICE
├─ Need speed? → ICE
├─ Visual presentation? → Value/Effort
├─ MVP scoping? → MoSCoW
├─ User expectations? → Kano
├─ Complex criteria? → Weighted Scoring
└─ Outcome-focused? → Opportunity Scoring

Always: Document, communicate, iterate
```

---

## Resources

**Books**:

- "Intercom on Product Management" (RICE framework)
- "Hacking Growth" by Sean Ellis (ICE scoring)
- "Jobs to be Done" by Anthony Ulwick (Opportunity scoring)

**Tools**:

- Airtable/Notion for scoring
- ProductPlan for roadmaps
- Aha!, ProductBoard for frameworks

**Articles**:

- "RICE: Simple prioritization for product managers" - Intercom
- "How to use ICE Scoring" - Sean Ellis
- "The Kano Model" - UX Magazine

---

## Related Skills

- `roadmap-frameworks` - Turn priorities into roadmaps
- `specification-techniques` - Spec prioritized features
- `product-positioning` - Strategic positioning and differentiation

---

**Key Principle**: Choose one framework, use it consistently, iterate. Don't over-analyze - prioritization should enable decisions, not paralyze them.
