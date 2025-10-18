---
name: prioritization-methods
description: Apply RICE, ICE, MoSCoW, Kano, and Value vs Effort frameworks. Use when prioritizing features, roadmap planning, or making trade-off decisions.
---

# Prioritization Methods & Frameworks

## Overview

Comprehensive guide to product prioritization frameworks used to make data-driven decisions about feature development, roadmap planning, and resource allocation.

## When to Use This Skill

- Choosing between competing features
- Building quarterly roadmaps
- Backlog prioritization
- Saying "no" with evidence
- Stakeholder alignment on priorities
- Resource allocation decisions

## Core Frameworks

### 1. RICE Scoring (Intercom)

**Formula**: (Reach × Impact × Confidence) / Effort

**Components**:
- **Reach**: How many users per time period (e.g., per quarter)
- **Impact**: 0.25 (minimal), 0.5 (low), 1 (medium), 2 (high), 3 (massive)
- **Confidence**: 100% (high data), 80% (medium), 50% (low data)
- **Effort**: Person-months to build

**Example**:
```
Feature: Dark Mode
- Reach: 10,000 users/quarter (50% of MAU use in evening)
- Impact: 2 (high - reduces eye strain, table stakes)
- Confidence: 80% (user research + requests)
- Effort: 1.5 person-months

RICE = (10,000 × 2 × 0.80) / 1.5 = 10,667
```

**When to Use**:
- Large backlog needs ranking
- Data-driven team culture
- Quantifiable user reach

**Pros**: Objective, forces estimation, scales well
**Cons**: Requires data, effort estimation can be inaccurate

---

### 2. ICE Scoring (Sean Ellis)

**Formula**: (Impact + Confidence + Ease) / 3

**Components** (each scored 1-10):
- **Impact**: How much will this move the needle?
- **Confidence**: How sure are we it will work?
- **Ease**: How simple is it to implement?

**Example**:
```
Feature: Email Notifications
- Impact: 8/10 (drives re-engagement)
- Confidence: 9/10 (proven pattern)
- Ease: 7/10 (1 week build)

ICE = (8 + 9 + 7) / 3 = 8.0
```

**When to Use**:
- Early-stage products (limited data)
- Growth experiments
- Quick prioritization

**Pros**: Simple, fast, intuitive
**Cons**: Subjective, harder to defend

---

### 3. Value vs Effort Matrix (2×2)

**Quadrants**:
```
     High Value
         │
    ┌────┼────┐
    │ Quick│ Big │
    │ Wins│ Bets│
    ┼─────┼────┤
    │ Fill│Time│
    │ -Ins│Sink│
    └────┼────┘
      Low  →  High
         Effort
```

**Process**:
1. Score each feature on Value (1-10)
2. Score each on Effort (1-10)
3. Plot on matrix
4. Prioritize:
   - Quick Wins (high value, low effort) - Do first
   - Big Bets (high value, high effort) - Strategic
   - Fill-Ins (low value, low effort) - If capacity
   - Time Sinks (low value, high effort) - Avoid

**When to Use**:
- Visual stakeholder presentations
- Portfolio planning
- Quick assessments

**Pros**: Visual, intuitive, fast
**Cons**: Binary thinking, doesn't capture nuance

---

### 4. MoSCoW Method

**Categories**:
- **Must Have**: Critical for launch (P0)
- **Should Have**: Important but not critical (P1)
- **Could Have**: Nice-to-have (P2)
- **Won't Have**: Out of scope (this time)

**Process**:
1. List all requirements
2. Categorize each
3. Negotiate until ~60% are Must, ~20% Should, ~20% Could

**Example**:
```
Must Have:
- User login
- Core workflow
- Data persistence

Should Have:
- Email notifications
- Export feature

Could Have:
- Dark mode
- Keyboard shortcuts

Won't Have (v1):
- Mobile app
- Advanced analytics
```

**When to Use**:
- MVP scoping
- Release planning
- Stakeholder alignment

**Pros**: Clear, forces hard choices, collaborative
**Cons**: No quantitative ranking within categories

---

### 5. Kano Model

**Categories**:
- **Basic Needs (Must-be)**: Expected features (dissatisfiers if absent)
- **Performance Needs (One-dimensional)**: More is better, linear satisfaction
- **Excitement Needs (Delighters)**: Unexpected joy, non-linear satisfaction
- **Indifferent**: Users don't care
- **Reverse**: Users prefer without it

**Survey Approach**:
Ask two questions for each feature:
1. "How would you feel if [feature] was present?"
2. "How would you feel if [feature] was absent?"

**Responses**: I like it | I expect it | I'm neutral | I can tolerate it | I dislike it

**Classification**:
```
         Functional (Present)
         Like | Expect | Neutral | Tolerate | Dislike
Absent   ────┼────────┼─────────┼──────────┼────────
Like     Q   │   E    │    E    │    E     │   P
Expect   R   │   I    │    I    │    I     │   M
Neutral  R   │   I    │    I    │    I     │   M
Tolerate R   │   I    │    I    │    I     │   M
Dislike  R   │   R    │    R    │    R     │   Q

E = Excitement, P = Performance, M = Must-be
I = Indifferent, R = Reverse, Q = Questionable
```

**Roadmap Strategy**:
- **Phase 1**: Build all Must-be features (table stakes)
- **Phase 2**: Competitive Performance features
- **Phase 3**: Differentiated Excitement features

**When to Use**:
- Understanding user expectations
- Competitive analysis
- Roadmap sequencing

**Pros**: User-centric, reveals expectations
**Cons**: Requires research, time-intensive

---

### 6. Weighted Scoring

**Process**:
1. Define criteria (e.g., User Value, Revenue, Strategic Fit, Effort)
2. Assign weights to each (must sum to 100%)
3. Score each feature on each criterion (1-10)
4. Calculate weighted score

**Example**:
```
Criteria Weights:
- User Value: 40%
- Revenue Impact: 30%
- Strategic Fit: 20%
- Ease of Implementation: 10%

Feature: Analytics Dashboard
- User Value: 8 × 40% = 3.2
- Revenue: 6 × 30% = 1.8
- Strategic: 9 × 20% = 1.8
- Ease: 5 × 10% = 0.5
Total Score = 7.3/10
```

**When to Use**:
- Multiple stakeholder priorities
- Complex decisions
- Custom criteria needed

**Pros**: Flexible, transparent criteria
**Cons**: Setup overhead, gaming possible

---

### 7. Opportunity Scoring (Jobs-to-be-Done)

**Process**:
1. Identify customer jobs (outcomes they want)
2. Survey: Rate importance (1-5) and satisfaction (1-5)
3. Calculate Opportunity = Importance + Max(Importance - Satisfaction, 0)
4. Prioritize high-opportunity jobs

**Example**:
```
Job: "Quickly find past conversations"
- Importance: 4.5
- Satisfaction: 2.0
- Opportunity = 4.5 + (4.5 - 2.0) = 7.0

Job: "Share conversations with team"
- Importance: 3.0
- Satisfaction: 2.8
- Opportunity = 3.0 + (3.0 - 2.8) = 3.2

Priority: Focus on "find past conversations" (7.0 > 3.2)
```

**When to Use**:
- Outcome-driven innovation
- Understanding underserved needs
- Feature gap analysis

**Pros**: User outcome focus, reveals gaps
**Cons**: Requires research, learning curve

---

## Choosing the Right Framework

### Use RICE when:
- You have quantitative data
- Large backlog (20+ items)
- Need defendable priorities

### Use ICE when:
- Growth experiments
- Limited data
- Need speed

### Use Value/Effort when:
- Stakeholder presentation
- Portfolio view
- Quick assessment

### Use MoSCoW when:
- MVP scoping
- Release planning
- Binary go/no-go

### Use Kano when:
- Understanding expectations
- Competitive positioning
- Multi-release planning

### Use Weighted Scoring when:
- Complex criteria
- Executive alignment
- Custom priorities

### Use Opportunity Scoring when:
- JTBD methodology
- Outcome-focused
- Innovation prioritization

---

## Best Practices

**1. Be Consistent**
- Use same framework across team
- Document assumptions
- Update scores as you learn

**2. Combine Frameworks**
- RICE for ranking + Value/Effort for visualization
- MoSCoW for release + RICE for roadmap
- Kano for strategy + ICE for tactics

**3. Avoid Common Pitfalls**
- Don't prioritize by HIPPO (Highest Paid Person's Opinion)
- Don't ignore effort (value alone insufficient)
- Don't set-and-forget (re-prioritize regularly)
- Don't game the system (honest scoring)

**4. Stakeholder Communication**
- Show your work (transparent criteria)
- Visualize priorities
- Explain trade-offs
- Document "why not" for rejected items

**5. Iterate and Learn**
- Track actual vs estimated impact
- Refine scoring over time
- Calibrate team estimates
- Learn from misses

---

## Templates

### RICE Scoring Template

```markdown
| Feature | Reach | Impact | Confidence | Effort | RICE | Priority |
|---------|-------|--------|------------|--------|------|----------|
| Feature A | 5000 | 2 | 80% | 2 | 4000 | 1 |
| Feature B | 2000 | 3 | 100% | 1 | 6000 | 2 |
```

### Value/Effort Matrix Template

```markdown
Quick Wins (High Value, Low Effort):
- Feature X: Value 9, Effort 3
- Feature Y: Value 8, Effort 2

Big Bets (High Value, High Effort):
- Feature Z: Value 10, Effort 9
```

### MoSCoW Template

```markdown
Must Have (60%):
- Feature 1
- Feature 2

Should Have (20%):
- Feature 3

Could Have (20%):
- Feature 4

Won't Have:
- Feature 5
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

## Quick Reference

```
Problem: Too many features, limited resources
Solution: Use prioritization framework

Lots of data? → RICE
Need speed? → ICE
Visual presentation? → Value/Effort
MVP scoping? → MoSCoW
User expectations? → Kano
Complex criteria? → Weighted Scoring
Outcome-focused? → Opportunity Scoring

Always: Document, communicate, iterate
```
