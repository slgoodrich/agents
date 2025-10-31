---
name: user-research-techniques
description: Master user interviews, usability testing, surveys, and research synthesis. Use when planning research, gathering user insights, or validating assumptions.
---

# User Research Techniques

## Overview

Comprehensive guide to qualitative and quantitative research methods for understanding users, validating ideas, and informing product decisions.

## When to Use This Skill

**Auto-loaded by agents**:
- `research-ops` - For research methods, planning, and best practices

**Use when you need**:
- Planning research studies
- Choosing research methods
- Conducting interviews or tests
- Analyzing research data
- Validating product decisions

## Research Methods Matrix

```
           Quantitative ← → Qualitative
           (What & How Many)  (Why & How)
              │
Behavioral ─┼─ Analytics        Usability Testing
(What they  │  Surveys          Field Studies
  do)       │  A/B Tests        Diary Studies
              │
Attitudinal ─┼─ Surveys          Interviews
(What they  │  NPS              Focus Groups
  say)      │  Questionnaires   Concept Tests
```

## Qualitative Methods

### 1. User Interviews

**Types**:
- **Discovery**: Understand problems and needs
- **Validation**: Test solution fit
- **Evaluative**: Assess existing product

**Best Practices**:
- Open-ended questions
- Listen more than talk (80/20 rule)
- Ask "why" 5 times
- Avoid leading questions
- Record and take notes

**Interview Structure** (60 min):
```
Introduction (5 min)
- Build rapport
- Explain purpose
- Get consent

Warm-up (5 min)
- Background questions
- Context setting

Main Questions (40 min)
- Behavioral: "Walk me through..."
- Pain points: "Tell me about a time when..."
- Goals: "What are you trying to achieve?"

Wrap-up (10 min)
- Anything missed?
- Who else to talk to?
- Thank you
```

**Sample Questions**:
```
Discovery:
- "Walk me through the last time you [task]"
- "What's most frustrating about [process]?"
- "Tell me about a time when [problem] occurred"

Validation:
- [Show concept] "What's your initial reaction?"
- "How would you use this?"
- "What concerns do you have?"
```

---

### 2. Usability Testing

**Types**:
- **Moderated**: Facilitator guides session
- **Unmoderated**: User completes alone
- **Remote**: Video call or tool-based
- **In-person**: Lab or coffee shop

**Process**:
1. **Recruit**: 5-8 participants (80% of issues)
2. **Prepare**: Tasks, scenarios, prototype
3. **Test**: Think-aloud protocol
4. **Analyze**: Issues, patterns, severity
5. **Report**: Findings and recommendations

**Task Format**:
```
Scenario: "You want to [goal]"
Task: "Using this prototype, [specific action]"

Example:
Scenario: "You want to find last month's sales report"
Task: "Find and download the December 2024 sales report"
```

**Think-Aloud Protocol**:
- "Please speak your thoughts out loud"
- "What are you looking for?"
- "What do you expect to happen?"
- Don't help unless stuck >2 minutes

**Metrics**:
- Task completion rate
- Time on task
- Errors
- Satisfaction (SEQ: Single Ease Question)

---

### 3. Field Studies (Ethnography)

**When**: Understand context and environment

**Methods**:
- **Contextual Inquiry**: Observe in natural setting
- **Shadowing**: Follow user through day
- **Diary Studies**: Users log activities

**Process**:
1. Observe silently
2. Take field notes
3. Ask clarifying questions
4. Look for workarounds
5. Identify pain points

---

### 4. Card Sorting

**Purpose**: Understand mental models, organize information

**Types**:
- **Open**: Users create categories
- **Closed**: Users sort into given categories
- **Hybrid**: Start closed, allow new categories

**Tools**: OptimalSort, UserZoom, Miro

---

### 5. Focus Groups

**Format**: 6-10 participants, moderated discussion

**When to Use**: Explore opinions, generate ideas

**When NOT to Use**: Validation (groupthink risk)

---

## Quantitative Methods

### 1. Surveys

**Types**:
- **NPS (Net Promoter Score)**: "Likelihood to recommend" (0-10)
- **CSAT (Customer Satisfaction)**: "How satisfied?" (1-5)
- **CES (Customer Effort Score)**: "How easy?" (1-7)
- **Custom**: Specific questions

**Survey Design**:
```
Good Question:
"How often do you use [feature]?"
□ Daily
□ Weekly
□ Monthly
□ Rarely
□ Never

Bad Question:
"Do you love our amazing new feature?"
(Leading, biased)
```

**Best Practices**:
- Keep short (< 10 questions)
- One question per topic
- Mix question types
- Avoid double-barreled questions
- Pilot test first

**Sample Sizes**:
- 100+ for directional insights
- 384+ for 95% confidence, ±5% margin
- Calculator: surveymonkey.com/mp/sample-size-calculator

---

### 2. Analytics (Behavioral Data)

**Metrics to Track**:
- **Engagement**: DAU, WAU, MAU, session duration
- **Conversion**: Funnel drop-offs, completion rates
- **Retention**: Cohort retention curves
- **Feature Adoption**: % users using feature

**Tools**: Mixpanel, Amplitude, Heap, Google Analytics

---

### 3. A/B Testing

**Process**:
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

---

### Thematic Analysis

**Steps**:
1. **Familiarize**: Read all data
2. **Code**: Tag recurring concepts
3. **Theme**: Group codes into themes
4. **Review**: Refine themes
5. **Define**: Name and describe themes
6. **Report**: Write findings

---

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

---

## Research Planning

### Define Research Questions

**Good Research Questions**:
- "How do users currently [task]?"
- "What prevents users from [goal]?"
- "Which features drive retention?"

**Bad Research Questions**:
- "Will users like this?" (too vague)
- "Should we build X?" (not research question)

---

### Choose Method

**Decision Tree**:
```
What vs Why?
├─ What/How Many? → Quantitative
│  ├─ Behavior → Analytics
│  └─ Attitudes → Survey
└─ Why/How? → Qualitative
   ├─ Discover → Interviews
   ├─ Validate → Usability Test
   └─ Context → Field Study
```

---

### Recruit Participants

**Screener Questions**:
```
1. How often do you [relevant behavior]?
   ○ Daily (CONTINUE)
   ○ Weekly (CONTINUE)
   ○ Monthly (SCREEN OUT)
   ○ Never (SCREEN OUT)

2. Do you work at [Competitor/Partner]?
   ○ Yes (SCREEN OUT)
   ○ No (CONTINUE)
```

**Incentives**:
- $50-100 for 1-hour consumer interview
- $150-300 for B2B professional
- Gift cards, credits, or cash

**Sources**:
- User Interviews, Respondent.io
- Your user base (email list)
- Social media, communities

---

## Best Practices

### 1. Avoid Bias

**Confirmation Bias**: Seek disconfirming evidence
**Leading Questions**: Ask neutral questions
**Selection Bias**: Recruit diverse participants
**Observer Effect**: Users behave differently when watched

---

### 2. Sample Sizes

**Qualitative**:
- 5-8 users per segment (diminishing returns)
- 15-20 total for diverse product

**Quantitative**:
- 100+ for trends
- 384+ for statistical significance
- Use power calculations

---

### 3. Triangulate

**Combine Methods**:
- Interviews (why) + Analytics (what)
- Usability tests + Surveys
- Quantitative → Qualitative → Quantitative

---

### 4. Continuous Discovery (Teresa Torres)

**Weekly Touchpoints**:
- Talk to 2-3 customers per week
- Mix research types
- Share with team
- Document insights
- Map to opportunities

---

## Common Mistakes

###  Avoid

- Asking what users want (they don't know)
- Leading questions ("Do you love this?")
- Only talking to power users
- Research without action
- Skipping synthesis

###  Do

- Observe behavior, not just opinions
- Ask open-ended questions
- Recruit diverse participants
- Act on findings
- Share insights widely

---

## Tools

**Research Platforms**:
- UserTesting, Maze (unmoderated testing)
- User Interviews, Respondent.io (recruitment)
- Lookback, Zoom (moderated testing)

**Analysis**:
- Dovetail, Airtable (synthesis)
- Miro, FigJam (affinity mapping)
- Typeform, SurveyMonkey (surveys)

**Analytics**:
- Mixpanel, Amplitude (product analytics)
- Hotjar, FullStory (session replay)
- Google Analytics (web analytics)

---

## Templates

### Research Plan

```markdown
# Research Plan: [Topic]

## Goals
- [Research question 1]
- [Research question 2]

## Method
- Type: [Interviews / Testing / Survey]
- Timeline: [Dates]
- Participants: [N, criteria]

## Questions/Tasks
1. [Question/Task 1]
2. [Question/Task 2]

## Analysis
- [How we'll synthesize]
- [Key metrics]

## Deliverables
- [Report, insights, recommendations]
```

---

## Resources

**Books**:
- "The Mom Test" - Rob Fitzpatrick
- "Just Enough Research" - Erika Hall
- "Continuous Discovery Habits" - Teresa Torres
- "Don't Make Me Think" - Steve Krug

**Online**:
- Nielsen Norman Group articles
- IDEO Design Kit
- Google Ventures Research Sprint

---

## Quick Guide

```
Need to understand why? → Interviews
Testing usability? → Usability Tests
Measure satisfaction? → Survey (NPS/CSAT)
Understand behavior? → Analytics
Validate solution? → Prototype Test
Deep context? → Field Study

Always: Define questions, recruit right users, synthesize, act on insights
```
