# Quick Prioritize

Fast priority scoring for incoming requests, bugs, and feature ideas using RICE, ICE, or simple priority matrices.

## Usage

```
/pm:quick-prioritize [item description] [optional: framework (RICE/ICE/simple)]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Quickly scores individual items for prioritization
2. Uses lightweight frameworks (RICE, ICE, or Priority Matrix)
3. Provides clear accept/defer/reject recommendation
4. Documents reasoning for transparency
5. Optimized for speed (2-3 minutes per item)
6. Can be used in batches for triage sessions

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Item Details**:
- What is the item? (feature request, bug, improvement, technical debt)
- Who requested it? (customer name, internal team, stakeholder, leadership)
- What's the ask? (specific capability or fix being requested)
- Why do they want it? (problem it solves, goal it achieves, pain it addresses)

**Context for Scoring**:
- How many people would this affect? (1 customer, 10%, all users, specific segment)
- How much value would it provide? (critical, important, nice-to-have)
- How confident are we in the estimates? (high, medium, low)
- How much effort would it take? (hours, days, weeks, months)

**Strategic Context**:
- Does this align with current strategy/roadmap?
- Is there a deadline or urgency? (customer commitment, competitive pressure)
- What happens if we don't do this? (churn risk, lost revenue, technical risk)
- Are there dependencies or prerequisites?

**Historical Context**:
- Has this been requested before? (how many times, by whom)
- Have we considered this before? (was it rejected, why)
- Are there alternatives or workarounds? (what can users do instead)

### 2. Choose Framework

- **RICE** (default) - Reach × Impact × Confidence / Effort
- **ICE** - Impact + Confidence + Ease (faster, simpler)
- **Simple** - High/Medium/Low on Value and Effort (fastest)

### 3. Gather Minimal Context
   - What is being requested
   - Who requested it (internal team, customer, stakeholder)
   - Why they want it (problem/goal)
   - Urgency or deadline if any

3. **Score Quickly**:
   - Use rough estimates, not precision
   - 5-minute rule: if unclear after 5 min, defer for more research
   - Document assumptions
   - Bias toward action (decide vs postpone)

4. **Provide Recommendation**:
   - **Accept** - Add to backlog with priority
   - **Defer** - Need more info/research
   - **Reject** - Not aligned, explain why

## Framework Details

### RICE Scoring

**Formula**: (Reach × Impact × Confidence) / Effort = RICE Score

**Reach**: How many users affected per quarter?
- 10,000+ users = 10
- 5,000-10,000 = 5
- 1,000-5,000 = 3
- 100-1,000 = 1
- <100 = 0.5

**Impact**: How much does it move the needle?
- Massive (3x) = 3.0
- High (2x) = 2.0
- Medium (1.5x) = 1.0
- Low (1.25x) = 0.5
- Minimal = 0.25

**Confidence**: How sure are we?
- High (have data) = 100%
- Medium (some data) = 80%
- Low (hypothesis) = 50%

**Effort**: Person-months to ship
- 0.25 (1 week)
- 0.5 (2 weeks)
- 1 (1 month)
- 2, 3, 6+ (larger efforts)

**RICE Score Interpretation**:
- >10 = High priority (top 10%)
- 5-10 = Medium-high priority
- 2-5 = Medium priority
- <2 = Low priority

---

### ICE Scoring

**Formula**: (Impact + Confidence + Ease) / 3 = ICE Score

Each dimension scored 1-10:

**Impact** (1-10):
- 9-10: Transformative, major user/business impact
- 7-8: Significant improvement
- 5-6: Noticeable benefit
- 3-4: Small improvement
- 1-2: Minimal impact

**Confidence** (1-10):
- 9-10: Strong data/evidence
- 7-8: Good evidence
- 5-6: Some evidence
- 3-4: Weak evidence
- 1-2: Pure speculation

**Ease** (1-10):
- 9-10: < 1 week, trivial
- 7-8: 1-2 weeks
- 5-6: 1 month
- 3-4: 2-3 months
- 1-2: > 3 months

**ICE Score Interpretation**:
- >8 = High priority
- 6-8 = Medium-high priority
- 4-6 = Medium priority
- <4 = Low priority

---

### Simple Priority Matrix

**Value** (High/Medium/Low):
- High: Major user/business impact
- Medium: Noticeable improvement
- Low: Nice to have

**Effort** (High/Medium/Low):
- High: > 1 month
- Medium: 2-4 weeks
- Low: < 2 weeks

**Priority Mapping**:
| Value/Effort | Low Effort | Medium Effort | High Effort |
|--------------|------------|---------------|-------------|
| High Value   | **P0** (Do now) | **P1** (Schedule soon) | **P2** (Consider) |
| Medium Value | **P1** (Schedule soon) | **P2** (Consider) | **P3** (Defer) |
| Low Value    | **P2** (If time) | **P3** (Defer) | **P4** (Reject) |

## Template

```markdown
# Quick Prioritization: [Feature/Decision]

**Date**: [Date] | **Method**: RICE|ICE|Value vs Effort

---

## Items to Prioritize

| Item | Reach | Impact | Confidence | Effort | RICE Score |
|------|-------|--------|------------|--------|------------|
| [Item 1] | [N] users | [H/M/L] | [%] | [weeks] | [Score] |
| [Item 2] | [N] users | [H/M/L] | [%] | [weeks] | [Score] |

**Scoring**:
- Reach: # of users/customers affected (per quarter)
- Impact: 3=Massive, 2=High, 1=Medium, 0.5=Low, 0.25=Minimal  
- Confidence: % confidence in estimates (100%, 80%, 50%)
- Effort: person-months

**RICE = (Reach × Impact × Confidence) / Effort**

---

## Recommended Priority

**Priority Order**:
1. [Item X] - RICE: [Score] - Rationale: [Why top priority]
2. [Item Y] - RICE: [Score] - Rationale: [Why second]
3. [Item Z] - RICE: [Score] - Rationale: [Why third]

**Do Now**: [Items 1-2]
**Do Next**: [Items 3-4]
**Consider Later**: [Items 5+]
**Don't Do**: [Items below threshold or negative value]

---

## Decision

**Prioritized**: [What we're doing first]
**Deferred**: [What we're postponing]
**Rejected**: [What we're not doing]
```

## Best Practices

✅ **DO**: Score collaboratively (not solo), be honest about effort, use data for reach/impact, update scores as you learn, explain assumptions, use same method consistently, make decisions quickly, document rationale

❌ **DON'T**: Game the scores to justify pet projects, use different methods each time (inconsistent), argue over decimal points (rough is fine), skip effort estimation, forget to revisit scores, prioritize based only on loudest voice

**Related**: `/pm:backlog-groom`, `/tools/roi-calculator`
