# Questioning Techniques Template

## Table of Contents

- [Overview](#overview)
- [The Mom Test (Rob Fitzpatrick)](#the-mom-test-rob-fitzpatrick)
- [The 5 Whys Technique](#the-5-whys-technique)
- [Jobs-to-be-Done (JTBD) Interview](#jobs-to-be-done-jtbd-interview)
- [The Laddering Technique](#the-laddering-technique)
- [Probing Techniques](#probing-techniques)
- [Question Types to Avoid](#question-types-to-avoid)
- [Technique Selection Guide](#technique-selection-guide)

## Overview

Advanced interviewing techniques for uncovering deeper insights, getting past surface-level answers, and understanding root causes. Use these techniques during interviews to probe effectively and avoid common pitfalls.

---

## The Mom Test (Rob Fitzpatrick)

### Core Principle

Ask questions that even your mom couldn't lie to you about. Focus on past behavior and facts, not future intentions or opinions.

### Why It Matters

People are naturally polite and want to be encouraging. They'll lie about future behavior ("I'd totally use that!") but are honest about past behavior ("Here's what I actually did last week").

### The Problem: Flawed Questions

These questions invite lies or are unhelpful:

#### ❌ "Would you buy this?"

**Why it's bad**:

- People lie about future behavior
- Being asked directly makes them want to be nice
- "Yes" means nothing without money changing hands

**Real behavior**:

- 90% say they'd buy
- 5% actually buy when launched

**Better question**: "Show me the last three tools you purchased. Walk me through why you bought each one."

---

#### ❌ "Do you think this is a good idea?"

**Why it's bad**:

- People want to be encouraging
- Don't want to hurt your feelings
- Opinion, not validation

**Real behavior**:

- Everyone says "great idea!"
- Nobody uses it when shipped

**Better question**: "When's the last time [problem] came up? What did you do about it?"

---

#### ❌ "Would you use this feature?"

**Why it's bad**:

- Hypothetical future behavior
- No cost to saying yes
- Features sound good in theory, different in practice

**Real behavior**:

- "I'd definitely use that!" → never uses it
- Can't predict actual usage without trying

**Better question**: "How do you currently handle [task this feature would address]? Show me your workflow."

---

### The Solution: Mom Test Questions

Ask about past behavior, current reality, and specific details.

#### ✓ "When's the last time [problem] came up?"

**Why it works**:

- Tests if problem is real and frequent
- Past behavior, not hypothetical
- Reveals severity by frequency

**Example**:

```
Researcher: "When's the last time you struggled to find a file?"

User: "Oh, this morning actually. Spent 10 minutes looking for the Q2 budget spreadsheet."

[Insight: Problem is frequent and costs real time]
```

**vs.**:

```
Researcher: "Do you have trouble finding files?"

User: "Yeah, sometimes."

[Insight: Vague, no actionable data]
```

---

#### ✓ "How much time/money did that cost you?"

**Why it works**:

- Quantifies severity
- Reveals if problem worth solving
- Facts, not opinions

**Example**:

```
Researcher: "How much time do you spend on [manual process] each week?"

User: "Ugh, probably 3-4 hours. It's brutal."

[Insight: Significant pain, worth solving]
```

**Red flag response**:

```
User: "Oh, maybe 15 minutes a month? Not a big deal."

[Insight: Problem exists but low severity, not worth solving]
```

---

#### ✓ "What are you currently doing to solve it?"

**Why it works**:

- Reveals if problem worth acting on
- Shows existing solutions (competition)
- Past behavior = real commitment

**Example**:

```
Researcher: "What are you currently doing to solve [problem]?"

User: "I built a Python script that runs nightly. It's janky but works."

[Insight: Pain is severe enough they built custom solution = validation]
```

**Red flag response**:

```
User: "Nothing really, I just live with it."

[Insight: Not severe enough to act on = weak validation]
```

---

#### ✓ "Show me your [current solution]"

**Why it works**:

- Reveals actual behavior, not claimed
- See their workarounds and hacks
- Understand their current process

**Example**:

```
Researcher: "Can you show me your current spreadsheet?"

User: [Opens 47-tab monster spreadsheet with macros and formulas]

[Insight: Pain is real - they've invested heavily in workaround]
```

---

#### ✓ "Who else should I talk to?"

**Why it works**:

- If problem is real, they know others with it
- Tests if problem is widespread
- Gets you more interviewees

**Example**:

```
Researcher: "Who else on your team deals with this?"

User: "Oh man, talk to Sarah and Mike - they have it even worse than me."

[Insight: Problem is shared, not individual edge case]
```

**Red flag response**:

```
User: "Hmm, not sure. Maybe just me?"

[Insight: Edge case or not actually a problem]
```

---

### Mom Test Rules Summary

**Talk about their life, not your idea**:

- Ask about their problems, workflows, and past behavior
- Don't pitch your solution during discovery

**Ask about specifics in the past, not generics or the future**:

- "Tell me about the last time..." ✓
- "Would you ever...?" ❌

**Listen more than you talk**:

- 80/20 rule: They talk 80%, you talk 20%
- Comfortable with silence

---

## The 5 Whys Technique

### Purpose

Get to root cause by asking "why" repeatedly. Surface-level answers rarely reveal the real problem.

### How It Works

Start with an observation, then ask "why" (or "what causes that?") 4-5 times until you reach root cause.

### Example 1: Feature Non-Adoption

```
Observation: "I don't use feature X"

Why? (1)
→ "It's too complicated"

Why is it complicated? (2)
→ "I don't understand what the buttons do"

Why don't you understand? (3)
→ "The labels are unclear"

Why are the labels unclear? (4)
→ "They use jargon I don't know"

Why don't you know the jargon? (5)
→ "I never went through onboarding, and there's no in-app help"

ROOT CAUSE: Onboarding gap + missing contextual help
SOLUTION: Better onboarding + tooltips with plain language
```

**If we'd stopped at level 1**: We'd think "simplify the feature"
**Actual root cause**: Onboarding and documentation problem

---

### Example 2: Slow Adoption

```
Observation: "Team hasn't adopted the tool yet"

Why? (1)
→ "People keep using the old spreadsheet"

Why are they still using the spreadsheet? (2)
→ "It has historical data they need"

Why is historical data in the spreadsheet? (3)
→ "We haven't migrated it to new tool"

Why haven't you migrated it? (4)
→ "Migration process isn't documented and seems risky"

Why does it seem risky? (5)
→ "No way to test migration without affecting production"

ROOT CAUSE: Migration risk and lack of staging environment
SOLUTION: Build staging environment + documented migration process
```

---

### Best Practices

**Use neutral phrasing**:

- ✓ "What causes that?"
- ✓ "Why is that?"
- ✓ "Help me understand why..."
- ❌ "Why would you do that?" (sounds accusatory)

**Stop when you reach actionable insight**:

- Sometimes root cause appears at why #3
- Sometimes need 6+ whys
- Stop when you have clear path to solution

**Don't interrogate**:

- Be genuinely curious, not confrontational
- "I'm trying to understand..." framing helps
- Okay to say "This is helpful - one more why..."

**Branch when needed**:

- Multiple causes? Follow each branch
- "Are there other reasons too?"

---

## Jobs-to-be-Done (JTBD) Interview

### Framework

Understand the "job" a user is trying to do. People don't want products - they want progress in their lives.

**Key Insight**: People "hire" products to do a job. Understanding the job (not just the product features) reveals true motivation.

### JTBD Question Structure

#### 1. Context: Triggering Event

**Purpose**: Understand what caused them to seek a solution

**Questions**:

```
"Tell me about the last time you [hired product / made decision / started using tool]"

"What was happening in your life/work at that time?"

"What triggered you to start looking for a solution?"
```

**Example**:

```
Researcher: "Tell me about when you started using a project management tool"

User: "We'd just hired our 10th employee. Projects were slipping, people were duplicating work. CEO asked me in a meeting why a project was late and I had no good answer. That was my wake-up call."

[Job context: Need visibility and accountability at scale]
```

---

#### 2. Situation: The Struggle

**Purpose**: Understand the pain point depth and context

**Questions**:

```
"What was difficult about the situation?"

"How were you handling it before?"

"What wasn't working about your old approach?"

"How did that make you feel?"
```

**Example**:

```
User: "I was spending hours every week in 1-on-1s asking 'what are you working on?' Then compiling a status report in a slide deck. It was exhausting and always out of date by the time I presented it."

[Situation: Manual status tracking not scaling]
```

---

#### 3. Desired Outcome: What "Done" Looks Like

**Purpose**: Understand success criteria and motivations

**Questions**:

```
"What were you hoping to achieve?"

"How would you know if you'd solved the problem?"

"What would success look like?"

"What would change in your day-to-day?"
```

**Example**:

```
User: "I wanted to be able to answer 'what's the status?' in 30 seconds, not 30 minutes. And I wanted the team to stay aligned without me being the bottleneck."

[Desired outcome: Real-time visibility + async coordination]
```

---

#### 4. Alternatives Considered: The Competition

**Purpose**: Understand competitive landscape and decision criteria

**Questions**:

```
"What else did you consider or try?"

"Why didn't those work?"

"What made you keep looking?"

"What almost made you choose [alternative]?"
```

**Example**:

```
User: "We tried Trello - too simple, no timeline view. Tried Jira - too complex, design team hated it. Tried staying with spreadsheets + Slack - just didn't scale. Almost went with Asana but it didn't integrate with our tools."

[Alternatives reveal: Need timeline view, simplicity, integrations]
```

---

#### 5. Decision Factors: Why This Solution

**Purpose**: Understand what sealed the deal

**Questions**:

```
"What made you choose [solution]?"

"What was the deciding factor?"

"What almost prevented you from choosing it?"

"Who else was involved in the decision?"
```

**Example**:

```
User: "Chose [tool] because it had the timeline view CEO wanted, was simple enough for non-technical team, and integrated with Slack. Almost didn't choose it because of price, but the time savings justified it."

[Key factors: Timeline view, simplicity, integrations, ROI]
```

---

### JTBD Example: Complete Interview

**Product**: Project Management Tool

```
CONTEXT:
"Tell me about when you started using a PM tool"
→ "Hit 10 employees, CEO asked why project was late, had no answer"

SITUATION:
"What wasn't working?"
→ "Hours in 1-on-1s compiling status. Always out of date."

DESIRED OUTCOME:
"What were you hoping for?"
→ "Answer 'what's the status?' in 30 seconds. Team aligned without me."

ALTERNATIVES:
"What else did you try?"
→ "Trello (too simple), Jira (too complex), spreadsheets (didn't scale)"

DECISION:
"Why did you choose [tool]?"
→ "Timeline view for CEO, simple for team, Slack integration"

JOB TO BE DONE:
"Help me maintain visibility and accountability as team scales"

NOT: "Manage tasks" (surface level)
ACTUALLY: "Look competent to CEO while enabling team autonomy"
```

---

## The Laddering Technique

### Purpose

Connect features to emotional benefits. Understand the "why behind the why."

### Structure

Move up the ladder from concrete to abstract:

1. **Attributes** (features)
2. **Consequences** (functional benefits)
3. **Values** (emotional benefits)

### How to Ladder

Start with a feature, keep asking "why does that matter?" until you reach emotional value.

### Example 1: Real-Time Collaboration

```
Feature: "Real-time collaboration"

Q: "Why is real-time collaboration important to you?"
A: "So my team can work together on the same document"
   [Consequence: Coordination]

Q: "Why does that matter?"
A: "We finish work faster when we're not waiting for email replies"
   [Consequence: Speed]

Q: "Why does speed matter?"
A: "I can leave work on time instead of working late"
   [Consequence: Work-life balance]

Q: "Why is leaving on time important?"
A: "I get to see my kids before bedtime"
   [Value: Family time]

INSIGHT: Real-time collaboration → Family time
MARKETING: Don't sell "real-time sync" - sell "more time with your family"
```

---

### Example 2: Automated Reporting

```
Feature: "Automated status reports"

Q: "Why is automated reporting important?"
A: "I don't have to spend hours compiling status updates"
   [Consequence: Time savings]

Q: "Why does saving that time matter?"
A: "I can focus on actual work instead of reporting"
   [Consequence: Productivity]

Q: "Why does that matter?"
A: "I can take on more strategic projects"
   [Consequence: Career growth]

Q: "Why is that important to you?"
A: "I want to get promoted to director"
   [Value: Career advancement]

INSIGHT: Automated reporting → Career advancement
MARKETING: Position as "spend time on work that gets you promoted"
```

---

### Example 3: Search Functionality

```
Feature: "Fast search"

Q: "Why is fast search important?"
A: "I can find information quickly"
   [Consequence: Efficiency]

Q: "Why does that matter?"
A: "I don't look incompetent in meetings when I can't find answers"
   [Consequence: Professional image]

Q: "Why is that important?"
A: "My credibility with the team"
   [Value: Respect/status]

INSIGHT: Fast search → Professional credibility
MARKETING: "Always have the answer" not "powerful search"
```

---

### When to Use Laddering

**Best for**:

- Understanding emotional drivers
- Creating marketing messaging
- Prioritizing features by emotional value
- Differentiation (competitors sell features, you sell outcomes)

**How to start**:

```
"I noticed you mentioned [feature]. Why is that important to you?"

Then keep asking "why does that matter?" until they mention:
- Feelings (stress, confidence, pride)
- Personal goals (promotion, respect, work-life balance)
- Deep values (family, achievement, autonomy)
```

---

## Probing Techniques

### The Silent Pause

**Technique**: After they answer, stay silent for 3-5 seconds

**Why it works**:

- People feel compelled to fill silence
- Often add more important details after pausing
- Shows you're listening and processing

**Example**:

```
User: "It's pretty frustrating."

[You: Stay silent, nod]

User: "Actually, I almost quit over it. It was that bad."

[Silence revealed severity]
```

---

### The Echo

**Technique**: Repeat the last few words as a question

**Why it works**:

- Encourages elaboration
- Shows you're listening
- Non-threatening way to probe

**Example**:

```
User: "The process takes forever."

You: "Takes forever?"

User: "Yeah, like 4 hours minimum. Sometimes a full day."

[Echo quantified the problem]
```

---

### The Naive Question

**Technique**: Ask "dumb" questions even when you think you know

**Why it works**:

- Reveals assumptions
- Gets their framing, not yours
- Often uncovers surprises

**Example**:

```
You: "What do you mean by 'project management'?"

User: "For us it's mostly about client visibility. Internal work we handle differently."

[Would've missed this if assumed "project management" meant internal]
```

---

### The Example Request

**Technique**: Always ask for specific examples

**Why it works**:

- Moves from abstract to concrete
- Reveals actual behavior
- Provides rich details

**Example**:

```
User: "The UI is confusing."

You: "Can you give me a specific example of when it confused you?"

User: "Yeah, yesterday I tried to archive a project and clicked 'delete' because I didn't see an archive option. Almost lost everything."

[Specific example reveals actual UX issue]
```

---

## Question Types to Avoid

### Leading Questions

**Problem**: Suggests the answer you want

❌ "Don't you think it would be better if...?"
❌ "Wouldn't it be great if...?"
❌ "I bet you'd love a feature that..."

✓ "How would you improve this?"
✓ "What's missing?"

---

### Hypothetical Questions

**Problem**: Future behavior is unreliable

❌ "Would you use this?"
❌ "If we built X, would you switch?"
❌ "How often would you...?"

✓ "How often do you currently...?"
✓ "Walk me through the last time you..."

---

### Yes/No Questions

**Problem**: Shuts down conversation

❌ "Do you like this?"
❌ "Is this useful?"
❌ "Does this make sense?"

✓ "What's your reaction to this?"
✓ "How would you use this?"
✓ "Help me understand what you're thinking"

---

### Multi-Part Questions

**Problem**: Confusing, they only answer one part

❌ "How often do you use it and what features do you use and do you like the UI?"

✓ "How often do you use it?" [pause]
✓ "Which features do you use?" [pause]
✓ "What's your take on the UI?" [pause]

---

## Technique Selection Guide

**When you need to...**

**Understand if problem is real**:
→ Use Mom Test questions (past behavior, specifics)

**Find root cause**:
→ Use 5 Whys technique

**Understand decision-making**:
→ Use JTBD interview

**Understand emotional drivers**:
→ Use Laddering technique

**Get them to elaborate**:
→ Use Silent Pause, Echo, Example Request

**Avoid bias**:
→ Avoid leading/hypothetical questions

---

**Key Principle**: Good questions reveal truth through specific past behavior, not opinions about hypothetical futures. Master these techniques to uncover what users really think, not what they think you want to hear.
