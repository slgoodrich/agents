---
name: Discovery Sprint Workflow
description: Rapid problem/solution validation inspired by Teresa Torres and Google Design Sprint
category: Discovery
duration: 1-2 weeks
model: sonnet
---

# Discovery Sprint Workflow

Rapid problem/solution validation inspired by Teresa Torres' Continuous Discovery and Google Design Sprint.

## Usage
```
/discovery-sprint [problem or opportunity]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Problem statement or opportunity to validate
- Current evidence (data, customer feedback, metrics showing the problem)
- Target users affected
- Why this matters now (urgency, business impact)
- Timeline constraints

## Overview

**Timeline**: 1-2 weeks
**Goal**: Validate problem, explore solutions, reduce risk before building

## Workflow Phases

### Day 1-2: Problem Framing

**Agents**: `user-researcher`, `product-strategist`

**Activities**:
1. **Define Problem**
   - Problem statement
   - Assumptions to test
   - Success criteria

2. **Gather Evidence**
   - Existing data/analytics
   - Customer feedback
   - Support tickets
   - Competitive research

3. **Identify Users**
   - Who has this problem most?
   - Recruitment criteria
   - Schedule 5-8 interviews

**Deliverables**: Problem brief, research plan

**Commands**:
```
/pm:interview-guide "Problem discovery for [problem]"
Tell user-researcher: "Design discovery research plan"
```

---

### Day 3-5: User Research

**Agents**: `user-researcher`

**Activities**:
1. **Conduct Interviews** (5-8 users)
   - Current behavior
   - Pain points
   - Workarounds
   - Goals and needs

2. **Synthesize Findings**
   - Affinity mapping
   - Pattern identification
   - Opportunity areas

3. **Validate Problem**
   - Is it real?
   - How severe?
   - For whom?

**Deliverables**: Research synthesis, validated problem

**Commands**:
```
/pm:research-synthesize [interview notes]
/pm:persona [target user]
/pm:journey-map [scenario]
```

---

### Day 6-7: Solution Ideation

**Agents**: `product-strategist`, `requirements-engineer`

**Activities**:
1. **Crazy 8s**: Sketch 8 solutions (quick)
2. **Solution Mapping**
   - Organize ideas
   - Identify patterns
   - Cluster themes

3. **Evaluate Solutions**
   - Feasibility
   - Impact
   - Effort

4. **Choose Direction** (1-2 solutions to prototype)

**Deliverables**: Solution sketches, chosen concept(s)

---

### Day 8-9: Prototyping

**Agents**: `requirements-engineer`

**Activities**:
1. **Create Prototype**
   - Figma mockup
   - Clickable prototype
   - OR written concept

2. **Define Test Scenarios**
   - Key tasks to test
   - Success criteria

**Deliverables**: Testable prototype, test plan

**Commands**:
```
/pm:user-stories [solution concept]
```

---

### Day 10: User Testing

**Agents**: `user-researcher`

**Activities**:
1. **Test with 5 Users**
   - Show prototype
   - Task-based testing
   - Gather feedback

2. **Capture Results**
   - Task completion
   - Comprehension
   - Desirability
   - Concerns

**Deliverables**: Test results

**Commands**:
```
Tell user-researcher: "Synthesize usability test findings"
```

---

### Day 11-12: Decision & Next Steps

**Agents**: `feature-prioritizer`, `product-strategist`

**Activities**:
1. **Evaluate Results**
   - Problem validated?
   - Solution resonates?
   - Effort justified?

2. **Decision**
   - ✅ Build it → Create PRD
   - 🔄 Iterate → Another sprint
   - ❌ Kill it → Move on

3. **If Build**:
   - RICE score
   - Roadmap placement
   - PRD creation

**Deliverables**: Go/no-go decision, next steps

**Commands**:
```
Tell feature-prioritizer: "Score this validated solution"
/pm:prd [validated solution]
```

---

## Success Metrics

**Problem Validation**:
- ✅ 5+ users confirm problem
- ✅ Severity is high
- ✅ No good existing solution

**Solution Validation**:
- ✅ 4/5 users understand it
- ✅ Would use if available
- ✅ Prefer to current approach

---

## Templates

### Problem Statement
```
[User type] struggles to [task]
Because [underlying reason]
This causes [negative impact]
We know this because [evidence]
```

### Solution Hypothesis
```
We believe that [solution]
Will help [users]
Achieve [outcome]
We'll know we're right when [measurable signal]
```

---

## Variations

**1-Week Sprint**: Compress to 5 days, fewer interviews
**2-Week Sprint**: More research, multiple solutions tested
**Continuous**: Run mini-sprints weekly

---

**Model**: Sonnet
