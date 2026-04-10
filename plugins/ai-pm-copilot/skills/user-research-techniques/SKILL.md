---
name: user-research-techniques
description: "User research methods including interviews, usability testing, surveys, and analytics. Use when planning user research, choosing a research method, gathering user insights, or validating assumptions with data. Trigger on: 'plan user research', 'which research method should I use', 'how do I talk to users', 'conduct user research', 'how many participants do I need'."
---

# User Research Techniques

Guide to qualitative and quantitative research methods for understanding users, validating ideas, and informing product decisions.

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

Test variants with statistical rigor. Requires a clear hypothesis ("Changing CTA color from blue to green will increase click-through by 10%"), a single variable change, sufficient sample size (use an online calculator -- typically 1,000+ per variant for small effects), and a 1-2 week runtime. Only test when you have enough traffic; for early-stage products with <1,000 weekly visitors, use qualitative methods instead.

**Key pitfalls**: Stopping tests early when results look promising (peeking problem), testing too many variants at once (diluted significance), and ignoring segment effects (overall neutral but positive for one cohort).

### Research Synthesis

Combine findings across studies to identify patterns. Three core approaches:

- **Affinity mapping**: Group observations by similarity, name the clusters, identify themes. Start here when you have raw interview notes.
- **Thematic analysis**: Code data into themes using a three-level system (codes → categories → themes). More rigorous than affinity mapping.
- **Jobs-to-be-Done**: Frame findings around the job users are hiring your product to do. Structure: "When [situation], I want to [motivation], so I can [outcome]."

For deeper synthesis methods, see `synthesis-frameworks`.

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

---

## Troubleshooting

**"I don't know which research method to use"**: Start with your question type. Exploring "why" = interviews. Testing usability = usability test. Measuring satisfaction = survey. If you're unsure, default to 5 user interviews -- they're the highest insight-per-hour method.

**"I can't recruit enough participants"**: Lower the bar. For qualitative research, 5 is enough. Use your existing users, social media, or offer small incentives ($25 gift cards). For guerrilla testing, find people at coffee shops or coworking spaces.

**"Leadership wants data but we have no budget for research"**: Use free methods: 5-second tests (UsabilityHub free tier), unmoderated testing (Maze free plan), or analyze existing support tickets and app reviews as proxy research data.

---

## Related Skills

- `interview-frameworks` - Deep-dive interview techniques and question design
- `usability-frameworks` - Usability testing methodology and heuristic evaluation
- `synthesis-frameworks` - Turning research data into actionable insights
- `validation-frameworks` - Experiment design for validating assumptions
