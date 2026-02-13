# Pattern Identification Guide

Deep dive into identifying and analyzing patterns in qualitative research data.

## Table of Contents

- [Overview](#overview)
- [Types of Patterns to Look For](#types-of-patterns-to-look-for)
- [Pattern Analysis Techniques](#pattern-analysis-techniques)
- [From Patterns to Insights](#from-patterns-to-insights)
- [Pattern Validation Checklist](#pattern-validation-checklist)
- [Common Pattern Pitfalls](#common-pattern-pitfalls)
- [Advanced Pattern Recognition](#advanced-pattern-recognition)

## Overview

Pattern recognition is the core skill of research synthesis. Raw data becomes insight when you identify recurring themes, behavioral patterns, and meaningful variations across participants.

## Types of Patterns to Look For

### 1. Frequency Patterns

**Definition:** How often did something occur across participants?

**Questions to ask:**

- How many users mentioned this?
- What percentage experienced this issue?
- Is this common or an outlier?

**Examples:**

- 8/10 users mentioned pricing concerns
- 12/15 users struggled with onboarding step 3
- 5/8 users requested mobile app capability
- All 10 users clicked Help before starting task

**Interpreting frequency:**

- **>50% of users:** Likely important, widespread issue
- **25-50%:** Significant minority, worth investigating
- **<20%:** May be edge case, but could be vocal minority or early signal
- **100% (universal):** Critical finding, requires immediate attention

**Using frequency patterns:**

- Prioritize common issues over rare ones
- Identify "table stakes" features (everyone expects)
- Spot emerging patterns (mentioned by few, but strongly)
- Validate assumptions (is this really a problem for users?)

**Caution:**
Don't only focus on frequency. A rarely-mentioned but severe issue may be more important than a commonly-mentioned minor annoyance.

### 2. Behavioral Patterns

**Definition:** What did users actually do (not what they said they'd do)?

**Questions to ask:**

- What actions did users take?
- What paths did they follow?
- Where did they get stuck?
- What workarounds did they create?

**Examples:**

- 6/8 users clicked "Help" before starting task (seeking confidence)
- All users skipped onboarding tutorial (preferred exploration)
- 9/10 users searched before browsing menu (search-first behavior)
- 7/10 users opened multiple tabs simultaneously (comparison shopping)

**Why behavior > stated preference:**

- Users often don't know why they do things
- Social desirability bias (say what sounds good)
- Actions reveal true priorities
- Workarounds show unmet needs

**Common behavioral patterns:**

- **Avoidance:** Users consistently skip or bypass a feature
- **Repetition:** Users repeat same action multiple times (confusion)
- **Workaround:** Users find alternative path to goal
- **Abandonment:** Users give up before completing task
- **Exploration:** Users poke around before committing

**Using behavioral patterns:**

- Identify usability issues (where users struggle)
- Understand actual workflows (vs intended)
- Spot design improvements (make easy path the right path)
- Validate feature value (are they using it?)

### 3. Sentiment Patterns

**Definition:** How did users feel about their experience?

**Questions to ask:**

- What emotions did users express?
- What language did they use?
- What tone of voice?
- What non-verbal cues?

**Examples:**

- Frustration: "This drives me crazy" (said forcefully)
- Delight: "Oh wow, that's amazing!" (surprised, happy)
- Confusion: "I don't understand what this does" (uncertain)
- Disappointment: "I expected more" (deflated)
- Anxiety: "I'm worried I'll mess this up" (hesitant)

**Identifying sentiment:**

- Listen to tone and inflection
- Watch facial expressions and body language
- Note word choice (strong adjectives)
- Observe behavioral indicators (sighing, smiling, etc.)

**Sentiment levels:**

- **Strong positive:** Unprompted praise, excitement
- **Mild positive:** Satisfied, meeting expectations
- **Neutral:** Functional, neither good nor bad
- **Mild negative:** Slightly frustrated, minor annoyance
- **Strong negative:** Angry, ready to quit/switch

**Why sentiment matters:**

- Strong emotions indicate priorities
- Frustration = pain point to fix
- Delight = differentiator to amplify
- Confusion = communication/design issue
- Anxiety = trust/confidence problem

**Using sentiment patterns:**

- Identify pain points (fix what frustrates)
- Amplify delights (what makes users happy?)
- Address confusion (improve clarity)
- Build confidence (reduce anxiety)

### 4. Segment Patterns

**Definition:** Do patterns differ by user type, role, or context?

**Questions to ask:**

- Are there distinct user groups?
- Do different groups have different needs?
- What behaviors are unique to each segment?
- What's common across all segments?

**Examples:**

- New users: Struggled with industry terminology
- Power users: Requested keyboard shortcuts and automation
- Enterprise: Needed admin controls and SSO
- SMB: Wanted simpler pricing, self-service
- Mobile users: Different workflow than desktop

**Identifying segments:**

- Behavioral differences (how they use product)
- Goal differences (what they're trying to achieve)
- Context differences (when/where/why they use it)
- Not superficial demographics (age, gender don't matter unless they drive behavior)

**Common segmentation dimensions:**

- **Experience level:** Novice vs expert users
- **Use case:** Different jobs to be done
- **Company size:** SMB vs enterprise needs
- **Role:** End user vs admin vs buyer
- **Frequency:** Daily vs occasional users

**Why segment patterns matter:**

- Different segments have different needs
- One-size-fits-all solutions often fail
- Personalization opportunities
- Prioritization (which segment matters most?)

**Using segment patterns:**

- Prioritize features by target segment
- Tailor experiences (onboarding, UI, messaging)
- Identify underserved segments
- Validate ICP (ideal customer profile)

### 5. Journey Patterns

**Definition:** When in the user journey did something occur?

**Questions to ask:**

- At what point did users struggle?
- Where do they succeed or fail?
- What's the critical moment?
- How does behavior change over time?

**Examples:**

- Signup: No issues, smooth experience
- Onboarding: 70% dropped off at step 3
- First use: Confusion on core feature
- Day 7: Re-engagement needed
- Month 2: Power users emerge

**Journey stages:**

- **Awareness:** How they discover product
- **Evaluation:** How they decide to try
- **Onboarding:** First experience with product
- **First value:** When they get initial benefit
- **Habit formation:** Becoming regular user
- **Power use:** Advanced usage patterns
- **Advocacy:** Recommending to others

**Journey moments:**

- **Activation moments:** First aha, initial value delivered
- **Friction moments:** Where users struggle or quit
- **Delight moments:** Unexpected positive experiences
- **Decision moments:** Go/no-go evaluation points

**Why journey patterns matter:**

- Identify critical moments (make or break experiences)
- Focus improvements on highest-impact moments
- Understand drop-off points
- Optimize for faster time-to-value

**Using journey patterns:**

- Fix drop-off points (reduce abandonment)
- Optimize critical moments (onboarding, first use)
- Accelerate time to value
- Build retention through habit formation

## Pattern Analysis Techniques

### Cross-Participant Comparison

Look for patterns across multiple participants:

- "All 10 users struggled with X"
- "Power users did Y, but new users did Z"
- "8/10 mentioned pricing without prompting"

### Within-Participant Analysis

Track patterns within individual sessions:

- User started confident, became frustrated over time
- User ignored feature initially, later discovered and loved it
- User had different behavior on desktop vs mobile

### Temporal Patterns

Notice how patterns change over time:

- Early in session vs late in session
- First visit vs return visit
- Over days, weeks, months

### Contextual Patterns

Understand how context affects patterns:

- Patterns in quiet environment vs noisy
- Solo use vs collaborative
- Work context vs personal

## From Patterns to Insights

**Pattern:** Observation of what happened
**Insight:** Understanding why + what it means + what to do

**Example transformation:**

**Pattern:** "8/10 users clicked the wrong button first"

**Insight:** "Users expect 'Submit' button to be bottom-right (web convention), but ours is top-right, causing 80% to click wrong button first. Moving to bottom-right would align with user expectations and reduce errors."

## Pattern Validation Checklist

Before declaring something a pattern:

- [ ] Appears in multiple participants (not just one)
- [ ] Has sufficient evidence (quotes, observations, data)
- [ ] Makes sense given context
- [ ] Distinct from other patterns (not just restating same thing)
- [ ] Meaningful for product decisions (actionable)
- [ ] Validated with team (not just researcher's interpretation)

## Common Pattern Pitfalls

**Confirmation bias:**
Seeing only patterns that confirm existing beliefs. Actively look for disconfirming evidence.

**Overgeneralization:**
"One user did X, therefore all users..." Need multiple examples to claim pattern.

**Correlation ≠ causation:**
Two things occurring together doesn't mean one causes the other.

**Ignoring outliers:**
Sometimes the exception reveals something important.

**Pattern fatigue:**
Finding so many patterns you can't see the forest for the trees. Focus on the most important ones.

## Advanced Pattern Recognition

### Negative patterns (absence)

Sometimes the absence of something is the pattern:

- No one mentioned feature Y (low awareness? low value?)
- Users didn't complain about X (actually okay, or not important enough to mention?)

### Contradictory patterns

When patterns conflict, that's interesting:

- Users say they want X, but their behavior shows they prefer Y
- Half of users love feature, half hate it (segment difference?)

### Meta-patterns

Patterns about patterns:

- All the issues are in onboarding (focus area)
- Problems cluster around specific feature (deep issue)
- Positive feedback is generic, negative is specific (revealing)
