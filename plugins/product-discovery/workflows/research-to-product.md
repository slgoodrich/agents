---
name: Research to Product Workflow
description: Transform user research into actionable product roadmap items
category: Discovery
duration: 1 week
model: sonnet
---

# Research to Product Workflow

Transform user research into actionable product roadmap items.

## Usage
```
/research-to-product [research study or findings]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- What research was conducted (user interviews, surveys, usability tests, analytics review)
- Key findings or insights summary
- How many participants or data points
- What problem or opportunity does this research address
- Who conducted the research and when
- What decisions this research should inform

## Overview

**Timeline**: 1 week
**Goal**: Convert research insights into prioritized features and roadmap updates

## Workflow Phases

### Step 1: Research Synthesis (Day 1-2)

**Agents**: `user-researcher`

**Activities**:
1. **Aggregate Data**
   - Interview transcripts
   - Survey results
   - Usability tests
   - Analytics
   - Support tickets

2. **Thematic Analysis**
   - Affinity mapping
   - Pattern identification
   - Frequency analysis

3. **Extract Insights**
   - Pain points
   - User goals
   - Unmet needs
   - Behavioral patterns
   - Surprising findings

**Deliverables**: Research synthesis report

**Commands**:
```
/pm:research-synthesize [research data]
```

**Template Output**:
```
## Key Findings

### Finding 1: [Theme]
- Mentioned by 12/15 users
- Quote: "[User quote]"
- Impact: High frustration, workflow blocker

### Finding 2: [Theme]
[...continue]
```

---

### Step 2: Opportunity Mapping (Day 3)

**Agents**: `user-researcher`, `product-strategist`

**Activities**:
1. **Map Problems to Opportunities**
   ```
   Problem: Users spend 2 hours manually creating reports
   Opportunity: Automated report generation
   Potential Impact: Save 10 hours/week per user
   ```

2. **Create Opportunity Tree** (Teresa Torres)
   ```
   Desired Outcome
   ├── Opportunity 1
   │   ├── Solution A
   │   └── Solution B
   ├── Opportunity 2
   └── Opportunity 3
   ```

3. **Jobs-to-be-Done Mapping**
   - What job are users trying to do?
   - Current solutions
   - Pain points with current approach
   - Desired outcome

**Deliverables**: Opportunity map

**Commands**:
```
Tell user-researcher: "Map research findings to product opportunities"
```

---

### Step 3: Solution Ideation (Day 4)

**Agents**: `product-strategist`, `requirements-engineer`

**Activities**:
1. **Brainstorm Solutions**
   - 3-5 solutions per opportunity
   - Range from quick wins to big bets

2. **Rough Scoping**
   - T-shirt sizing
   - Complexity assessment
   - Dependencies

3. **Create Feature Concepts**
   - Feature description
   - User value
   - High-level requirements

**Deliverables**: Feature concept list

**Template**:
```
## Feature Concept: [Name]

**Problem Solved**: [From research]
**Solution**: [Description]
**User Value**: [Benefit]
**Effort**: [XS/S/M/L/XL]
**Dependencies**: [Any blockers]
```

---

### Step 4: Prioritization (Day 5)

**Agents**: `feature-prioritizer`, `product-strategist`

**Activities**:
1. **RICE Scoring**
   - Reach: Users impacted
   - Impact: Problem severity (from research)
   - Confidence: Based on research strength
   - Effort: From scoping

2. **Opportunity Scoring** (JTBD method)
   - Importance (from survey)
   - Satisfaction (current state)
   - Opportunity = Importance + max(Importance - Satisfaction, 0)

3. **Strategic Fit**
   - Alignment to OKRs
   - Competitive positioning
   - Market timing

**Deliverables**: Prioritized feature list with scores

**Commands**:
```
Tell feature-prioritizer: "Score these research-driven features with RICE"
```

---

### Step 5: Roadmap Integration (Day 6-7)

**Agents**: `product-strategist`, `stakeholder-manager`

**Activities**:
1. **Slot into Roadmap**
   - High RICE → Now
   - Medium RICE → Next
   - Low RICE → Later
   - No-go → Archive with rationale

2. **Create PRDs** (for Now items)
   - Use research as evidence
   - Reference specific findings
   - Include user quotes

3. **Stakeholder Communication**
   - Present findings
   - Show research → insights → features flow
   - Get buy-in

4. **Update Roadmap**
   - Add new items
   - Adjust priorities
   - Document decisions

**Deliverables**: Updated roadmap, PRDs, stakeholder update

**Commands**:
```
/pm:roadmap "Updated with Research Insights"
/pm:prd [top priority feature]
Tell stakeholder-manager: "Present research findings and roadmap updates"
```

---

## From Research to Roadmap Example

### Research Input
```
Study: 15 user interviews on reporting workflow
Finding: "Creating weekly reports takes 2-4 hours of manual work"
Evidence: 12/15 users mentioned, high frustration
Quote: "I spend every Monday morning copying data into slides"
```

### Opportunity
```
Opportunity: Automated report generation
Impact: Save 10-40 hours/month per user
Job-to-be-Done: "Quickly create professional reports for stakeholders"
```

### Solution Concepts
```
1. Report templates (S) - Pre-built templates, RICE: 800
2. Auto-populated reports (M) - Scheduled generation, RICE: 2400
3. AI report writer (L) - Natural language summaries, RICE: 1800
```

### Prioritization
```
Top Priority: Auto-populated reports (RICE: 2400)
- Reach: 500 users
- Impact: 3 (massive time save)
- Confidence: 100% (strong research)
- Effort: 2 person-months
```

### Roadmap
```
Now (Q2):
✅ Auto-populated reports feature
- Based on interview finding #3
- RICE: 2400
- Will reduce reporting time by 80%

Next (Q3):
- AI report writer (if auto-reports successful)

Later:
- Advanced customization
```

---

## Research Quality Checks

Before proceeding, ensure:

✅ **Sample Size Adequate**:
- Qual: 5-8 users per segment
- Quant: 100+ for trends

✅ **Representative Users**:
- Matches target personas
- Diverse perspectives

✅ **Strong Evidence**:
- Multiple data sources
- Triangulated findings
- Specific examples

✅ **Actionable Insights**:
- Clear problems
- Measurable impact
- Solutions feasible

---

## Outputs

### 1. Research Synthesis
- Key findings (3-5)
- Themes and patterns
- User quotes
- Recommendations

### 2. Opportunity Map
- Problems → Opportunities → Solutions
- Opportunity tree
- JTBD mapping

### 3. Feature Concepts
- 10-20 feature ideas
- Rough scoped
- Linked to research

### 4. Prioritized Backlog
- RICE scored
- Ranked
- Roadmap ready

### 5. Updated Roadmap
- Research-validated features
- Evidence-based priorities
- Stakeholder buy-in

---

## Best Practices

✅ **Direct Quotes**: Use verbatim user quotes in PRDs
✅ **Quantify Impact**: "Saves 10 hours/week" > "Saves time"
✅ **Multiple Solutions**: Explore range of solutions per opportunity
✅ **Validate Assumptions**: Test solution concepts before building
✅ **Track Back**: Link features to original research

❌ **Don't**:
- Cherry-pick findings that confirm bias
- Skip synthesis (raw data → features)
- Ignore negative findings
- Build everything (prioritize!)

---

## Success Metrics

**Research Quality**:
- Insights are actionable
- Clear user problems identified
- Multiple data sources converge

**Roadmap Impact**:
- 3-5 research-driven features added
- High-confidence priorities
- Stakeholder alignment

**Feature Success** (post-launch):
- Solves validated problem
- High adoption (>50% of target users)
- Positive feedback references research

---

**Model**: Sonnet
