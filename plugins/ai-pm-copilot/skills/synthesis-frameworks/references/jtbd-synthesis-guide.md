# Jobs-to-be-Done (JTBD) Synthesis Guide

How to synthesize research data using the Jobs-to-be-Done framework to understand customer motivations and drive product strategy.

## Table of Contents

- [What is Jobs-to-be-Done?](#what-is-jobs-to-be-done)
- [JTBD vs Traditional Research](#jtbd-vs-traditional-research)
- [The Job Statement Format](#the-job-statement-format)
- [Finding Jobs in Research Data](#finding-jobs-in-research-data)
- [The Forces Framework](#the-forces-framework)
- [Analyzing Forces](#analyzing-forces)
- [Example: Full JTBD Analysis](#example-full-jtbd-analysis)
- [JTBD in Different Research Contexts](#jtbd-in-different-research-contexts)
- [Common JTBD Mistakes](#common-jtbd-mistakes)
- [From Jobs to Product Strategy](#from-jobs-to-product-strategy)
- [JTBD Synthesis Deliverable](#jtbd-synthesis-deliverable)

## What is Jobs-to-be-Done?

**Core Concept:**
People don't buy products - they "hire" products to do a job. Understanding the job reveals what customers really want.

**Famous example:**
"People don't want a quarter-inch drill. They want a quarter-inch hole."

- The product: Drill
- The job: Make holes
- The deeper job: Hang pictures (to make home feel like theirs)

## JTBD vs Traditional Research

**Traditional approach:**
"What features do you want in a project management tool?"

- Users give solution ideas ("I want Gantt charts")
- Solutions are often wrong
- Focuses on product, not problem

**JTBD approach:**
"When do you struggle to manage projects today?"

- Users describe situations and motivations
- Reveals underlying jobs
- Focuses on progress, not features

## The Job Statement Format

### Basic Template

```
When [situation],
I want to [motivation],
So I can [expected outcome]
```

**Example:**

```
When my CEO asks me for project status,
I want to quickly generate a summary,
So I can respond confidently without scrambling
```

### Why This Format Works

**When [situation]:**

- Context matters: Same user, different jobs in different situations
- Triggers: What prompts the need?

**I want to [motivation]:**

- The job itself
- Not a solution (don't say "I want a feature X")
- A desired capability or outcome

**So I can [expected outcome]:**

- The why behind the what
- Often reveals deeper job

### Bad vs Good Job Statements

**Bad:** "I want a reporting feature"

- This is a solution, not a job

**Good:** "I want to look prepared in front of my CEO"

- This is the actual job
- Many solutions possible (not just reporting feature)

**Bad:** "I want to use your product"

- Too generic, not a job

**Good:** "I want to coordinate my team without constant meetings"

- Specific job, clear outcome

## Finding Jobs in Research Data

### 1. Listen for Struggle

Jobs emerge from struggle and friction.

**Questions that reveal jobs:**

- "When do things go wrong today?"
- "What's frustrating about your current approach?"
- "Walk me through the last time you struggled with X"
- "What workarounds have you created?"

**Example from interview:**

> "Every Friday I spend 2 hours copying data from Jira, GitHub, and Slack into a spreadsheet to send to my CEO. It's so tedious, and I'm always worried I'll miss something."

**Job identified:**

```
When I need to report project status to leadership,
I want to quickly compile multi-source data,
So I can be confident I'm not missing anything important
```

### 2. Look for Workarounds

Current workarounds reveal unmet jobs.

**What to notice:**

- Duct-tape solutions
- Manual processes
- Multiple tools combined
- Spreadsheets (universal workaround tool)

**Example:**
User maintains elaborate spreadsheet tracking customer requests across email, support tickets, and Slack.

**Job:**

```
When customers make feature requests,
I want to track and prioritize them in one place,
So I can make informed roadmap decisions without losing requests
```

### 3. Identify Context Switches

When do users change tools, processes, or approaches? That's often a job boundary.

**Example:**
User writes specs in Google Docs, then manually copies to Jira, then discusses in Slack, then tracks in spreadsheet.

**Jobs revealed:**

- Write clear specifications (Google Docs)
- Track work progress (Jira)
- Discuss with team (Slack)
- Report status to leadership (Spreadsheet)

Each context switch = potentially different job

### 4. Probe for Outcomes

"So I can..." statements reveal what users actually value.

**Ask:**

- "Why does that matter to you?"
- "What would that enable?"
- "What would be different if you had that?"

**Example dialogue:**

> Researcher: "Why do you want faster reports?"
> User: "So I can respond to my CEO faster"
> R: "Why does that matter?"
> U: "So I look prepared and on top of things"
> R: "Why does that matter?"
> U: "It builds trust that I'm a competent PM"

**Deep job:** Build credibility/trust with leadership

## The Forces Framework

For each job, analyze the four forces that drive or prevent switching to new solution.

### Force Diagram

```
         PUSH              PULL
    (Current pain)    (New solution)
         ↓                 ↓

    CURRENT ----?---→ NEW

         ↑                 ↑
       HABITS          ANXIETIES
    (Inertia)      (Fear of change)
```

**Switch happens when:** Push + Pull > Habits + Anxieties

### 1. Push Forces (Why change from current?)

**What frustrates users about current solution?**

- Pain points
- Limitations
- Time wasted
- Workarounds needed
- Error-prone processes

**Example (Project status reporting):**

- Takes 2 hours every week (time)
- Manual copy-paste from 3 tools (tedious)
- Prone to errors (missing data)
- Always feels rushed (stress)
- CEO constantly asks for updates (annoying)

### 2. Pull Forces (Why choose new solution?)

**What attracts users to proposed solution?**

- Benefits
- New capabilities
- Time savings
- Better outcomes
- Aspirational identity

**Example:**

- Auto-generated in seconds (time savings)
- Always up-to-date (accuracy)
- Professional-looking output (looks good)
- No more scrambling (peace of mind)
- "I'll look so prepared" (identity)

### 3. Anxieties (What holds users back?)

**What worries users about switching?**

- Fear of change
- Learning curve
- Risk of failure
- Cost concerns
- Loss of control
- "What if it doesn't work?"

**Example:**

- Will it look unprofessional? (quality concern)
- What if the data is wrong? (accuracy concern)
- Will I lose control over messaging? (control concern)
- Will my CEO trust an auto-generated report? (credibility concern)
- What if I can't customize it? (flexibility concern)

### 4. Habits (What keeps users where they are?)

**Why is current solution "good enough"?**

- Familiarity
- Switching costs
- Comfort with known approach
- Team expectations
- Already have process

**Example:**

- "My spreadsheet works fine" (familiarity)
- "I know exactly where everything is" (mastery)
- "My team expects this format" (team habits)
- "I'd have to learn a new tool" (switching cost)
- "The devil you know..." (risk aversion)

## Analyzing Forces

### Amplify the Pull

Make new solution more attractive:

- Emphasize time savings: "2 hours → 2 minutes"
- Show quality: Professional templates, customizable
- Reduce learning curve: Familiar interface, guided setup
- Demonstrate value: Free trial, before/after comparison

### Increase the Push

Make current solution pain more salient:

- Quantify waste: "100+ hours/year on manual reporting"
- Surface hidden costs: "Missing data = bad decisions"
- Show opportunity cost: "What else could you do with 2 hours?"

### Reduce Anxieties

Address fears directly:

- Quality concerns → Show examples, allow customization, human review
- Control concerns → Customizable templates, edit before sending
- Accuracy concerns → Data validation, audit trail, source links
- Credibility concerns → Professional output, company branding

### Overcome Habits

Make switching easier:

- Import existing format (reduce change)
- Gradual adoption (use alongside current, not instead)
- Quick wins first (easy success builds confidence)
- Make new way easier than old way

## Example: Full JTBD Analysis

### Job Statement

```
When I need to report project status to leadership,
I want to quickly compile accurate data from multiple sources,
So I can respond confidently and look prepared
```

### Forces Analysis

**Push (Current pain):**

- Takes 2 hours weekly
- Manual copy-paste from Jira, GitHub, Slack
- Error-prone (sometimes miss things)
- Stressful when CEO asks unexpectedly
- Constant requests disrupt flow

**Pull (New solution):**

- Auto-generated in <2 minutes
- Pulls from all sources automatically
- Always up-to-date and accurate
- Professional formatting
- On-demand generation
- Customizable for audience

**Anxieties:**

- Will it look unprofessional?
- What if data is wrong?
- Will I lose control of messaging?
- Will CEO trust automated report?
- What if I can't customize it?

**Habits:**

- "My spreadsheet works fine"
- Team expects current format
- Already have process down
- Know where to find everything
- CEO is used to this format

### Strategy

**To drive adoption:**

1. **Amplify Pull:**
   - Lead with time savings: "2 hours → 2 minutes"
   - Show professional output examples
   - Offer customization demo
   - Free trial: "Try alongside current approach"

2. **Increase Push:**
   - Calculate annual time waste: "100+ hours/year"
   - Surface error rate: "How often do you catch mistakes?"
   - Opportunity cost: "What else could you ship with 100 hours?"

3. **Reduce Anxieties:**
   - Professional templates: Show CEO-ready examples
   - Human review: Edit before sending
   - Data validation: Show sources, allow overrides
   - Customization: Match current format exactly

4. **Address Habits:**
   - Import current format
   - Use alongside spreadsheet initially
   - Quick setup (<10 min)
   - Make new way easier than old way

## JTBD in Different Research Contexts

### In Interviews

**Instead of:** "What features do you want?"
**Ask:**

- "Walk me through the last time you struggled with X"
- "What workarounds have you created?"
- "Why did you choose your current solution?"

### In Usability Tests

**Look for:**

- When do users get stuck? (job not being done)
- What workarounds do they create? (unmet job)
- What do they expect but doesn't exist? (job to be done)

### In Surveys

**Questions to include:**

- "What were you trying to accomplish when you first looked for a solution like ours?"
- "What would make you switch to a different tool?"
- "What almost prevented you from signing up?"

## Common JTBD Mistakes

**Mistake 1: Confusing jobs with solutions**

- Bad: "Job is to use Gantt charts"
- Good: "Job is to understand project timeline at a glance"

**Mistake 2: Too broad**

- Bad: "Job is to be productive"
- Good: "Job is to find relevant information quickly without breaking flow"

**Mistake 3: Too narrow**

- Bad: "Job is to click the blue button"
- Good: "Job is to complete signup quickly"

**Mistake 4: Ignoring context**

- Jobs are contextual - same person has different jobs in different situations

**Mistake 5: Forgetting forces**

- Knowing the job isn't enough - must understand what drives/prevents switching

## From Jobs to Product Strategy

### Prioritize by Job Importance

Which jobs are:

- Most frequent?
- Most painful?
- Least well-served by current solutions?
- Most valuable to business?

### Design for Jobs, Not Features

**Wrong:** "We need a Gantt chart feature"
**Right:** "Users need to see project timelines at a glance. Gantt chart is one solution, but timeline view, calendar view, or milestone list might work better for our users"

### Validate by Jobs

**Test:** Does new feature help users accomplish job better?

**Measure:** Time to complete job, success rate, user satisfaction with outcome

### Communicate by Jobs

**Marketing:** "Finally, prepare for leadership meetings in 2 minutes, not 2 hours"
**Not:** "Advanced automated reporting dashboard"

## JTBD Synthesis Deliverable

**Template:**

### Job: [Job statement]

**Context:**

- When this job arises
- How often
- Who has this job

**Current Solutions:**

- What users do today
- Limitations
- Workarounds

**Forces:**

- Push: Why change?
- Pull: Why us?
- Anxieties: What holds back?
- Habits: Why stay?

**Opportunity:**

- Market size (how many have this job?)
- How well-served today? (gap analysis)
- Strategic fit (does this align with strategy?)

**Recommendation:**

- Should we pursue this job?
- How to position solution?
- What to build/change?
