# Insight Quality Guide

How to distinguish good insights from observations and ensure your findings drive action.

## Table of Contents

- [What Makes an Insight?](#what-makes-an-insight)
- [The Five Characteristics of Good Insights](#the-five-characteristics-of-good-insights)
- [The Insight Formula](#the-insight-formula)
- [Bad Insight Examples (and How to Fix)](#bad-insight-examples-and-how-to-fix)
- [Insight Quality Checklist](#insight-quality-checklist)
- [From Weak to Strong: Transformation Examples](#from-weak-to-strong-transformation-examples)
- [Teaching Your Team Insight Quality](#teaching-your-team-insight-quality)

## What Makes an Insight?

**Observation:** What happened
**Insight:** What it means + why it matters + what to do about it

An insight connects data to understanding to action.

## The Five Characteristics of Good Insights

### 1. Specific (Not Vague)

**Bad insights are generic and fuzzy:**

- "Users don't like the UI"
- "The product needs improvement"
- "Navigation is confusing"
- "Users want more features"

**Why these are bad:**

- Too broad to act on
- No evidence provided
- Could mean anything
- Not falsifiable

**Good insights are concrete and detailed:**

- "6/8 users couldn't find 'Settings' because it's hidden in the hamburger menu, which 75% of users never opened. Moving Settings to the top navigation bar would make it discoverable."

**Why this is good:**

- Quantified (6/8 users, 75%)
- Specific behavior (couldn't find, never opened menu)
- Root cause identified (hidden in hamburger)
- Actionable solution (move to top nav)

**Making insights specific:**

- Add numbers: How many? What percentage?
- Include behavior: What did users do?
- Explain why: What caused this?
- Provide context: When/where did this occur?
- Suggest action: What should we do?

### 2. Surprising (Not Obvious)

**Bad insights state the obvious:**

- "Users want the product to work"
- "People prefer fast loading times"
- "Users like when things are easy"
- "Mobile users use mobile devices"

**Why these are bad:**

- No new information
- Everyone already knows this
- Doesn't change thinking
- Waste of research time/money

**Good insights challenge assumptions:**

- "Users prefer slower import speed (8 sec) with progress indicator over fast import (2 sec) with no feedback, because transparency builds trust more than speed"

**Why this is good:**

- Counterintuitive (slower is better?)
- Challenges assumption (speed isn't everything)
- Explains why (trust > speed)
- Changes product thinking

**More examples of surprising insights:**

- "Users abandon at signup not due to length, but because they don't understand value yet"
- "Power users want fewer features with deeper integration, not more features"
- "B2B buyers choose based on IT security, but users choose based on ease of use - creating split priorities"

**Finding surprising insights:**

- Look for contradictions (users say X but do Y)
- Challenge assumptions ("Do users really care about speed here?")
- Find non-obvious causes ("It's not A, it's actually B")
- Reveal hidden motivations ("They're not buying X, they're buying status")

### 3. Actionable (Clear Implications)

**Bad insights lack clear next steps:**

- "Users are frustrated"
- "The onboarding could be better"
- "Some people had trouble"
- "Not everyone understood the concept"

**Why these are bad:**

- So what? What do we do about it?
- No clear action
- Leaves team guessing
- Doesn't drive decisions

**Good insights tell you what to do:**

- "Users frustrated by 8-field signup form (vs 3 fields for competitors) abandon at 60% rate. Reducing to 3 required fields (name, email, password) would match competitor standards and likely halve abandonment rate."

**Why this is good:**

- Clear problem (too many fields)
- Benchmark (vs competitors)
- Impact (60% abandon)
- Specific action (reduce to 3 fields)
- Expected outcome (halve abandonment)

**Making insights actionable:**

- State the problem clearly
- Provide specific recommendation
- Estimate impact ("could increase signups by X%")
- Consider feasibility (quick win vs major project)
- Assign ownership (who should do this?)

### 4. Evidence-Based (Not Speculation)

**Bad insights are opinions disguised as findings:**

- "I think users would like dark mode"
- "It seems like people prefer option A"
- "Users probably want feature X"
- "The team feels navigation is confusing"

**Why these are bad:**

- Personal opinion, not data
- Weasel words ("think", "seems", "probably")
- No participants quoted
- Can't be verified

**Good insights are grounded in data:**

- "5/10 users requested dark mode unprompted, with 3 citing eye strain from all-day usage. Quote: 'I work 10 hours a day in your tool. A dark mode would save my eyes.' This suggests dark mode is a common need for power users, who represent 40% of our DAUs."

**Why this is good:**

- Quantified (5/10 users, 40% of DAUs)
- Unprompted (not leading question)
- Direct quote (evidence)
- Specific reason (eye strain)
- Connected to business (power users)

**Types of evidence:**

- **Quantitative:** Numbers, percentages, frequencies
- **Behavioral:** What users did, not just said
- **Quotes:** Verbatim statements from users
- **Context:** When/where/why this occurred

**Strengthening evidence:**

- Include multiple types (quant + qual)
- Show, don't just tell (video clips, screenshots)
- Quote participants directly
- Provide enough detail to verify

### 5. Prioritized (Impact + Feasibility)

**Bad insight sets overwhelm teams:**

- List of 50 findings, all equal weight
- Everything marked "high priority"
- No guidance on what to do first
- Team paralyzed by options

**Why this is bad:**

- Can't do everything
- No clear starting point
- Important buried in unimportant
- Doesn't respect team capacity

**Good insights are ranked and prioritized:**

- "Top 5 insights ranked by (frequency × severity):
  1. Onboarding abandonment: 60% drop-off at step 3 → Quick win: Make step optional
  2. Mobile experience broken: 100% mobile users failed → Major: Rebuild or block mobile
  3. [etc]"

**Why this is good:**

- Limited to top insights (manageable)
- Clear prioritization criteria
- Quick wins called out
- Effort indicated (quick vs major)

**Prioritization frameworks:**

**Impact vs Effort matrix:**

```
        Low Effort    High Effort
High    Quick Wins    Major Projects
Impact  (Do First)    (Do Next)

Low     Fill-ins      Money Pits
Impact  (Do Later)    (Avoid)
```

**Impact scoring (1-5):**

- Frequency: How many users affected?
- Severity: How painful?
- Business impact: Revenue/retention effect?

**Effort scoring (1-5):**

- Technical complexity
- Design requirements
- Dependencies
- Time to build

**Priority = Impact / Effort**

## The Insight Formula

**Good Insight = Observation + Pattern + Implication + Action**

**Template:**
"[X%/number] of users [did/said specific thing] because [reason], suggesting we should [action] to [expected outcome]"

**Examples:**

"8/10 users abandoned onboarding at 'Invite Team' step because they didn't have emails ready, suggesting we should make this step optional with a 'Skip for now' button to reduce abandonment from 60% to target 30%"

"All 5 power users requested keyboard shortcuts unprompted, with 3 specifically mentioning Slack as reference point, suggesting we should implement Slack-style shortcuts (Cmd+K, etc.) to improve efficiency for our most engaged users"

## Bad Insight Examples (and How to Fix)

### Example 1: Too Vague

**Bad:** "Users struggled with the product"

**Why it's bad:** Generic, no specifics, not actionable

**Better:** "7/10 users spent >3 minutes searching for the 'Export' button, with 4 eventually giving up and asking for help, because the icon wasn't recognizable. Adding a text label or moving to the main menu would improve discoverability."

### Example 2: Just Observation

**Bad:** "Users mentioned pricing 12 times"

**Why it's bad:** Just a count, no insight into what it means

**Better:** "Users mentioned pricing 12 times across 8 interviews, consistently comparing our $99/mo to competitors' $49/mo. Quote: 'I like your product better, but it's hard to justify double the price.' This suggests we're failing value communication or have a price-to-value perception issue to address either through pricing changes or better value demonstration."

### Example 3: Opinion, Not Data

**Bad:** "I think the new design is better"

**Why it's bad:** Personal opinion with no user evidence

**Better:** "In A/B testing, the new design achieved 35% higher conversion (45% vs 33%) and 20% faster task completion (avg 2.4 min vs 3.0 min). Users commented positively on clarity: 'Much easier to understand.' The new design should be rolled out to 100% of users."

### Example 4: Obvious/Not Surprising

**Bad:** "Users want the app to be fast"

**Why it's bad:** Everyone wants fast apps, not insightful

**Better:** "Users tolerate 5-second load times on initial app launch but abandon after 2 seconds on subsequent actions, because expectations differ: 'First time I'm patient, but after that I expect it to be instant.' We should optimize for action speed over initial load."

### Example 5: Not Actionable

**Bad:** "Users were confused"

**Why it's bad:** Doesn't say what to do about it

**Better:** "Users were confused by the term 'Workspace' (6/10 asked 'What's the difference between workspace and project?'), suggesting we should either eliminate the distinction (use only 'Project') or clearly explain the hierarchy in onboarding with examples."

## Insight Quality Checklist

Before calling something an insight, verify:

- [ ] **Specific:** Includes numbers, behaviors, and context?
- [ ] **Surprising:** Challenges assumptions or reveals something new?
- [ ] **Actionable:** Clear what to do with this information?
- [ ] **Evidence-based:** Grounded in data with quotes/numbers?
- [ ] **Prioritized:** Ranked by importance, effort indicated?

If you can't check all five boxes, it's not a strong insight yet - keep refining.

## From Weak to Strong: Transformation Examples

### Example 1

**Weak:** "Navigation needs work"

- Not specific, not actionable, no evidence

**Stronger:** "Users struggled with navigation"

- Still vague, what kind of struggle?

**Even Stronger:** "8/10 users couldn't find Settings"

- Specific, but no context or action

**Strong:** "8/10 users couldn't find Settings because it's in the hamburger menu that most users ignore (only 2/10 opened it). Moving Settings to top navigation would make it discoverable to all users."

- Specific, evidence-based, explains why, actionable

### Example 2

**Weak:** "Onboarding could be better"

- Too generic to act on

**Stronger:** "Users drop off during onboarding"

- Okay, where exactly?

**Even Stronger:** "60% of users abandon at step 3 of onboarding"

- Specific, but why? What do we do?

**Strong:** "60% of users abandon at step 3 ('Invite Team') because they don't have teammate emails ready and can't skip. Making this step optional with a 'Skip for now' button and Day 3 email reminder would reduce abandonment (target: 30%) while maintaining team invitation rate through follow-up."

- Specific, explains why, actionable, expected outcome

## Teaching Your Team Insight Quality

**Create a shared standard:**

- Use the 5 characteristics as evaluation criteria
- Review insights together as a team
- Practice rewriting weak insights to be stronger

**Insight review sessions:**

- Share draft insights before finalizing
- Have team score insights on the 5 characteristics
- Iterate to strengthen weak areas

**Make it safe to push back:**

- Encourage team to challenge vague insights
- "That's interesting, but what does it mean we should do?"
- Build culture of high insight standards
