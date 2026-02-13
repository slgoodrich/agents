# Quantitative Research Methods & Synthesis Guide

Deep dive into quantitative research methods and research synthesis techniques.

## Table of Contents

- [Surveys](#surveys)
- [Analytics (Behavioral Data)](#analytics-behavioral-data)
- [A/B Testing](#ab-testing)
- [Research Synthesis](#research-synthesis)

---

## Surveys

**Types**:

- **NPS (Net Promoter Score)**: "Likelihood to recommend" (0-10)
- **CSAT (Customer Satisfaction)**: "How satisfied?" (1-5)
- **CES (Customer Effort Score)**: "How easy?" (1-7)
- **Custom**: Specific questions

### Survey Design

```
Good Question:
"How often do you use [feature]?"
[] Daily
[] Weekly
[] Monthly
[] Rarely
[] Never

Bad Question:
"Do you love our amazing new feature?"
(Leading, biased)
```

### Best Practices

- Keep short (< 10 questions)
- One question per topic
- Mix question types
- Avoid double-barreled questions
- Pilot test first

### Sample Sizes

- 100+ for directional insights
- 384+ for 95% confidence, +/-5% margin
- Calculator: surveymonkey.com/mp/sample-size-calculator

---

## Analytics (Behavioral Data)

**Metrics to Track**:

- **Engagement**: DAU, WAU, MAU, session duration
- **Conversion**: Funnel drop-offs, completion rates
- **Retention**: Cohort retention curves
- **Feature Adoption**: % users using feature

**Tools**: Mixpanel, Amplitude, Heap, Google Analytics

---

## A/B Testing

### Process

1. Hypothesis
2. Design variants
3. Determine sample size
4. Run test (1-2 weeks)
5. Analyze (significance)
6. Ship or iterate

(See experiment-designer skill for details)

---

## Research Synthesis

### Affinity Mapping

**Process**:

1. Write observations on sticky notes
2. Group similar notes
3. Label themes
4. Identify patterns
5. Extract insights

**Tool**: Miro, FigJam, physical wall

### Thematic Analysis

**Steps**:

1. **Familiarize**: Read all data
2. **Code**: Tag recurring concepts
3. **Theme**: Group codes into themes
4. **Review**: Refine themes
5. **Define**: Name and describe themes
6. **Report**: Write findings

### Jobs-to-be-Done Framework

**Job Statement**:
"When [situation], I want to [motivation], so I can [outcome]"

**Example**:
"When I'm preparing for a client meeting, I want to quickly find relevant past conversations, so I can provide informed recommendations"

**Interview Questions**:

- "What job were you trying to get done?"
- "What were you using before?"
- "What triggered you to switch?"
- "What obstacles did you face?"
