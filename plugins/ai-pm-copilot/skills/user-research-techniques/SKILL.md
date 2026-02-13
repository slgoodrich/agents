---
name: user-research-techniques
description: Master user interviews, usability testing, surveys, and research synthesis. Use when planning research, gathering user insights, or validating assumptions.
---

# User Research Techniques

Guide to qualitative and quantitative research methods for understanding users, validating ideas, and informing product decisions.

## Table of Contents

- [When to Use This Skill](#when-to-use-this-skill)
- [Research Methods Matrix](#research-methods-matrix)
- [Qualitative Methods](#qualitative-methods)
- [Quantitative Methods](#quantitative-methods)
- [Best Practices](#best-practices)
- [Common Mistakes](#common-mistakes)
- [Tools](#tools)
- [Templates and References](#templates-and-references)
- [Quick Guide](#quick-guide)

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
           Quantitative <-- --> Qualitative
           (What & How Many)    (Why & How)
              |
Behavioral --+-- Analytics        Usability Testing
(What they  |    Surveys          Field Studies
  do)       |    A/B Tests        Diary Studies
              |
Attitudinal -+-- Surveys          Interviews
(What they  |    NPS              Focus Groups
  say)      |    Questionnaires   Concept Tests
```

## Qualitative Methods

### User Interviews

Understand problems, validate solutions, assess products. Use open-ended questions, listen more than talk (80/20 rule), and ask "why" 5 times. 5-8 participants per segment.

### Usability Testing

Test product usability with moderated or unmoderated sessions. Recruit 5-8 participants, use think-aloud protocol, measure task completion, time on task, and satisfaction.

### Field Studies

Observe users in their natural environment through contextual inquiry, shadowing, or diary studies. Best for understanding context and discovering workarounds.

### Card Sorting

Understand mental models and information architecture. Open (users create categories), closed (sort into given categories), or hybrid.

### Focus Groups

6-10 participant moderated discussions. Good for exploring opinions and generating ideas. Avoid for validation (groupthink risk).

**Comprehensive guide**: `references/qualitative-methods-guide.md`

---

## Quantitative Methods

### Surveys

Measure attitudes at scale with NPS (0-10), CSAT (1-5), CES (1-7), or custom questions. Keep short (<10 questions), avoid leading/double-barreled questions. 100+ respondents for directional insights, 384+ for statistical significance.

### Analytics

Track behavioral data: engagement (DAU/WAU/MAU), conversion funnels, retention cohorts, feature adoption.

### A/B Testing

Test variants with statistical rigor. Hypothesis, design, sample size, run 1-2 weeks, analyze significance.

### Research Synthesis

Combine findings through affinity mapping, thematic analysis, or Jobs-to-be-Done framework.

**Comprehensive guide**: `references/quantitative-methods-guide.md`

---

## Best Practices

### 1. Avoid Bias

**Confirmation Bias**: Seek disconfirming evidence
**Leading Questions**: Ask neutral questions
**Selection Bias**: Recruit diverse participants
**Observer Effect**: Users behave differently when watched

### 2. Sample Sizes

**Qualitative**:

- 5-8 users per segment (diminishing returns)
- 15-20 total for diverse product

**Quantitative**:

- 100+ for trends
- 384+ for statistical significance
- Use power calculations

### 3. Triangulate

**Combine Methods**:

- Interviews (why) + Analytics (what)
- Usability tests + Surveys
- Quantitative -> Qualitative -> Quantitative

### 4. Continuous Discovery (Teresa Torres)

**Weekly Touchpoints**:

- Talk to 2-3 customers per week
- Mix research types
- Share with team
- Document insights
- Map to opportunities

---

## Common Mistakes

**Avoid**:

- Asking what users want (they don't know)
- Leading questions ("Do you love this?")
- Only talking to power users
- Research without action
- Skipping synthesis

**Do**:

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

## Templates and References

### Assets (Ready-to-Use)

- `assets/research-plan-template.md` - Research plan template with goals, methods, questions, and deliverables

### References (Deep Dives)

- `references/qualitative-methods-guide.md` - User interviews, usability testing, field studies, card sorting, focus groups
- `references/quantitative-methods-guide.md` - Surveys, analytics, A/B testing, research synthesis methods
- `references/research-planning-guide.md` - Defining research questions, choosing methods, recruiting participants

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
Need to understand why? -> Interviews
Testing usability? -> Usability Tests
Measure satisfaction? -> Survey (NPS/CSAT)
Understand behavior? -> Analytics
Validate solution? -> Prototype Test
Deep context? -> Field Study

Always: Define questions, recruit right users, synthesize, act on insights
```
