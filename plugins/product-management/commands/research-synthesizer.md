# Research Synthesizer

Analyze and synthesize user research into actionable insights and themes.

## Usage

```
/pm:research-synthesize [research notes or transcript]
```

## What This Command Does

Transforms raw research data (interviews, surveys, usability tests) into structured insights, patterns, and recommendations.

## Instructions

1. Analyze research input for:
   - Recurring themes
   - Pain points mentioned
   - User goals and motivations
   - Behavioral patterns
   - Surprising findings
   - Contradictions

2. Create synthesis with:
   - Key findings (top 3-5)
   - Supporting evidence (quotes, observations)
   - Thematic analysis
   - Opportunity mapping
   - Actionable recommendations

## Template

```markdown
# Research Synthesis: [Study Name]

## Executive Summary
**Key Insight**: [One-sentence main finding]
**Primary Recommendation**: [Top action]

---

## Study Overview
- **Dates**: [Period]
- **Method**: [Interviews/Survey/Testing]
- **Participants**: [N participants, demographics]
- **Objective**: [Research goals]

---

## Key Findings

### Finding 1: [Theme Title]
**Insight**: [What we learned]

**Evidence**:
- Quote: "[User quote]" - Participant 7
- Observation: [Pattern seen]
- Data: X% of participants mentioned [theme]

**Impact**: [Product implications]
**Opportunity**: [What we could build]

### Finding 2: [Theme]
[Same structure]

---

## Themes & Patterns

| Theme | Frequency | Severity | Quotes |
|-------|-----------|----------|--------|
| [Theme 1] | 12/15 users | High | "[Quote]" |
| [Theme 2] | 8/15 users | Medium | "[Quote]" |

---

## User Needs

**Must-Have**:
- [Need 1]: [Why critical]

**Important**:
- [Need 2]: [Value]

**Nice-to-Have**:
- [Need 3]: [Future consideration]

---

## Recommendations

**Immediate** (This Sprint):
1. [Quick fix based on research]

**Short-term** (Next Quarter):
2. [Feature to address main pain]
3. [Process improvement]

**Long-term** (6-12 months):
4. [Strategic initiative]

---

## Opportunity Map
```
Core Problem: [User need]
├── Opportunity 1: [Specific opportunity]
├── Opportunity 2: [Specific opportunity]
└── Opportunity 3: [Specific opportunity]
```

---

## Next Steps
- [Follow-up research needed]
- [Additional validation]
- [Prototype to test]
```

## Model
claude-sonnet-4-5

## Related
- `/pm:interview-guide` - Plan research
- `/pm:persona` - Create personas from insights
- `/pm:journey-map` - Map user journeys
