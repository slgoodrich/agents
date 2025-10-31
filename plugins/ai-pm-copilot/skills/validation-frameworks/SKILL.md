---
name: validation-frameworks
description: Problem and solution validation methodologies, assumption testing, and MVP validation experiments
---

# Validation Frameworks

Frameworks for validating problems, solutions, and product assumptions before committing to full development.

## When to Use This Skill

**Auto-loaded by agents**:
- `research-ops` - For problem/solution validation and assumption testing

**Use when you need**:
- Validating product ideas before building
- Testing assumptions and hypotheses
- De-risking product decisions
- Running MVP experiments
- Validating problem-solution fit
- Testing willingness to pay
- Evaluating technical feasibility

## Core Principle: Reduce Risk Through Learning

Building the wrong thing is expensive. Validation reduces risk by answering critical questions before major investment:

- **Problem validation**: Is this a real problem worth solving?
- **Solution validation**: Does our solution actually solve the problem?
- **Market validation**: Will people pay for this?
- **Usability validation**: Can people use it?
- **Technical validation**: Can we build it?

## The Validation Spectrum

Validation isn't binary (validated vs. not validated). It's a spectrum of confidence:

```
Wild Guess → Hypothesis → Validated Hypothesis → High Confidence → Proven
```

Early stage: Cheap, fast tests (low confidence gain)
Later stage: More expensive tests (high confidence gain)

**Example progression**:
1. **Assumption**: "Busy parents struggle to plan healthy meals"
2. **Interview 5 parents** → Some validation (small sample)
3. **Survey 100 parents** → More validation (larger sample)
4. **Prototype test with 20 parents** → Strong validation (behavior observed)
5. **Launch MVP, track engagement** → Very strong validation (real usage)
6. **Measure retention after 3 months** → Proven (sustained behavior)

## Problem Validation vs. Solution Validation

### Problem Validation

**Question**: "Is this a problem worth solving?"

**Goal**: Confirm that:
- The problem exists
- It's painful enough that people want it solved
- It's common enough to matter
- Current solutions are inadequate

**Methods**:
- Customer interviews (discovery-focused)
- Ethnographic observation
- Surveys about pain points
- Data analysis (support tickets, analytics)
- Jobs-to-be-Done interviews

**Red flags that stop here**:
- No one cares about this problem
- Existing solutions work fine
- Problem only affects tiny niche
- Pain point is mild annoyance, not real pain

**Output**: Problem statement + evidence it's worth solving

See `assets/problem-validation-canvas.md` for a ready-to-use framework.

---

### Solution Validation

**Question**: "Does our solution solve the problem?"

**Goal**: Confirm that:
- Our solution addresses the problem
- Users understand it
- Users would use it
- It's better than alternatives
- Value proposition resonates

**Methods**:
- Prototype testing
- Landing page tests
- Concierge MVP (manual solution)
- Wizard of Oz (fake backend)
- Pre-sales or waitlist signups

**Red flags**:
- Users don't understand the solution
- They prefer their current workaround
- Would use it but not pay for it
- Solves wrong part of the problem

**Output**: Validated solution concept + evidence of demand

See `assets/solution-validation-checklist.md` for validation steps.

---

## The Assumption-Validation Cycle

### 1. Identify Assumptions

Every product idea rests on assumptions. Make them explicit.

**Types of assumptions**:

**Desirability**: Will people want this?
- "Users want to track their habits"
- "They'll pay $10/month for this"
- "They'll invite their friends"

**Feasibility**: Can we build this?
- "We can process data in under 1 second"
- "We can integrate with their existing tools"
- "Our team can build this in 3 months"

**Viability**: Should we build this?
- "Customer acquisition cost will be under $50"
- "Retention will be above 40% after 30 days"
- "We can reach 10k users in 12 months"

**Best practice**: Write assumptions as testable hypotheses
- Not: "Users need this feature"
- Yes: "At least 60% of users will use this feature weekly"

---

### 2. Prioritize Assumptions to Test

Not all assumptions are equally important. Prioritize by:

**Risk**: How uncertain are we? (Higher risk = higher priority)
**Impact**: What happens if we're wrong? (Higher impact = higher priority)

**Prioritization matrix**:

| Risk/Impact | High Impact | Low Impact |
|------------|-------------|------------|
| **High Risk** | **Test first** | Test second |
| **Low Risk** | Test second | Maybe skip |

**Riskiest assumptions** (test these first):
- Leap-of-faith assumptions the entire business depends on
- Things you've never done before
- Assumptions about user behavior with no data
- Technical feasibility of core functionality

**Lower-risk assumptions** (test later or assume):
- Based on prior experience
- Easy to change if wrong
- Industry best practices
- Minor features

---

### 3. Design Validation Experiments

For each assumption, design the cheapest test that could prove it wrong.

**Experiment design principles**:

**1. Falsifiable**: Can produce evidence that assumption is wrong
**2. Specific**: Clear success/failure criteria defined upfront
**3. Minimal**: Smallest effort needed to learn
**4. Fast**: Results in days/weeks, not months
**5. Ethical**: Don't mislead or harm users

**The Experiment Canvas**: See `assets/validation-experiment-template.md`

---

### 4. Run the Experiment

**Before starting**:
- [ ] Define success criteria ("At least 40% will click")
- [ ] Set sample size ("Test with 50 users")
- [ ] Decide timeframe ("Run for 1 week")
- [ ] Identify what success/failure would mean for product

**During**:
- Track metrics rigorously
- Document unexpected learnings
- Don't change experiment mid-flight

**After**:
- Analyze results honestly (avoid confirmation bias)
- Document what you learned
- Decide: Pivot, persevere, or iterate

---

## Validation Methods by Fidelity

### Low-Fidelity (Hours to Days)

**1. Customer Interviews**
- **Cost**: Very low (just time)
- **Validates**: Problem existence, pain level, current solutions
- **Limitations**: What people say ≠ what they do
- **Best for**: Early problem validation

**2. Surveys**
- **Cost**: Low
- **Validates**: Problem prevalence, feature preferences
- **Limitations**: Response bias, can't probe deeply
- **Best for**: Quantifying what you learned qualitatively

**3. Landing Page Test**
- **Cost**: Low (1-2 days to build)
- **Validates**: Interest in solution, value proposition clarity
- **Measure**: Email signups, clicks to "Get Started"
- **Best for**: Demand validation before building

**4. Paper Prototypes**
- **Cost**: Very low (sketch on paper/whiteboard)
- **Validates**: Concept understanding, workflow feasibility
- **Limitations**: Low realism
- **Best for**: Very early solution concepts

---

### Medium-Fidelity (Days to Weeks)

**5. Clickable Prototypes**
- **Cost**: Medium (design tool, 2-5 days)
- **Validates**: User flow, interaction patterns, comprehension
- **Tools**: Figma, Sketch, Adobe XD
- **Best for**: Usability validation pre-development

**6. Concierge MVP**
- **Cost**: Medium (your time delivering manually)
- **Validates**: Value of outcome, willingness to use/pay
- **Example**: Manually curate recommendations before building algorithm
- **Best for**: Validating value before automation

**7. Wizard of Oz MVP**
- **Cost**: Medium (build facade, manual backend)
- **Validates**: User behavior, feature usage, workflows
- **Example**: "AI" feature that's actually humans behind the scenes
- **Best for**: Testing expensive-to-build features

---

### High-Fidelity (Weeks to Months)

**8. Functional Prototype**
- **Cost**: High (weeks of development)
- **Validates**: Technical feasibility, actual usage patterns
- **Limitations**: Expensive if you're wrong
- **Best for**: After other validation, final pre-launch check

**9. Private Beta**
- **Cost**: High (full build + support)
- **Validates**: Real-world usage, retention, bugs
- **Best for**: Pre-launch final validation with early adopters

**10. Public MVP**
- **Cost**: Very high (full product)
- **Validates**: Product-market fit, business model viability
- **Best for**: After all other validation passed

---

## Validation Metrics and Success Criteria

### Quantitative Validation Metrics

**Interest/Demand**:
- Landing page conversion rate
- Waitlist signup rate
- Pre-order conversion
- Prototype test completion rate

**Usage**:
- Feature adoption rate
- Task completion rate
- Time on task
- Frequency of use

**Engagement**:
- DAU/MAU (daily/monthly active users)
- Session length
- Return rate
- Feature usage depth

**Value Realization**:
- Aha moment rate (reached key action)
- Time to value
- Retention curves
- Referral rate

**Business**:
- Conversion to paid
- Lifetime value (LTV)
- Customer acquisition cost (CAC)
- Churn rate

---

### Qualitative Validation Signals

**Strong positive signals**:
- Users ask when they can buy it
- Users describe it to others excitedly
- Users find use cases you didn't imagine
- Users return without prompting
- Users complain when you take it away

**Weak positive signals**:
- "That's interesting"
- "I might use that"
- Polite feedback with no follow-up
- Theoretical interest but no commitment

**Negative signals**:
- Confusion about value proposition
- Preference for existing solution
- Feature requests that miss the point
- Can't articulate who would use it
- Ghosting after initial interest

---

## Setting Success Criteria

**Before running experiment**, define what success looks like.

**Framework**: Set three thresholds

1. **Strong success**: Clear green light, proceed confidently
2. **Moderate success**: Promising but needs iteration
3. **Failure**: Pivot or abandon

**Example: Landing page test**
- Strong success: > 30% email signup rate
- Moderate success: 15-30% signup rate
- Failure: < 15% signup rate

**Example: Prototype test**
- Strong success: 8/10 users complete task, would use weekly
- Moderate success: 5-7/10 complete, would use monthly
- Failure: < 5/10 complete or no usage intent

**Important**: Decide criteria before seeing results to avoid bias.

---

## Teresa Torres Continuous Discovery Validation

### Opportunity Solution Trees

Map opportunities (user needs) to solutions to validate:

```
Outcome
└── Opportunity 1
    ├── Solution A
    ├── Solution B
    └── Solution C
└── Opportunity 2
    └── Solution D
```

**Validate each level**:
1. Outcome: Is this the right goal?
2. Opportunities: Are these real user needs?
3. Solutions: Will this solution address the opportunity?

### Assumption Testing

For each solution, map assumptions:

**Desirability assumptions**: Will users want this?
**Usability assumptions**: Can users use this?
**Feasibility assumptions**: Can we build this?
**Viability assumptions**: Should we build this?

Then test riskiest assumptions first with smallest possible experiments.

### Weekly Touchpoints

Continuous discovery = continuous validation:
- Weekly customer interviews (problem + solution validation)
- Weekly prototype tests with 2-3 users
- Weekly assumption tests (small experiments)

**Goal**: Continuous evidence flow, not one-time validation.

See `references/lean-startup-validation.md` and `references/assumption-testing-methods.md` for detailed methodologies.

---

## Common Validation Anti-Patterns

### 1. Fake Validation

**What it looks like**:
- Asking friends and family (they'll lie to be nice)
- Leading questions ("Wouldn't you love...?")
- Testing with employees
- Cherry-picking positive feedback

**Fix**: Talk to real users, ask open-ended questions, seek disconfirming evidence.

---

### 2. Analysis Paralysis

**What it looks like**:
- Endless research without decisions
- Testing everything before building anything
- Demanding statistical significance with 3 data points

**Fix**: Accept uncertainty, set decision deadlines, bias toward action.

---

### 3. Confirmation Bias

**What it looks like**:
- Only hearing what confirms existing beliefs
- Dismissing negative feedback as "they don't get it"
- Stopping research when you hear what you wanted

**Fix**: Actively seek disconfirming evidence, set falsifiable criteria upfront.

---

### 4. Vanity Validation

**What it looks like**:
- "I got 500 email signups!" (but 0 conversions)
- "People loved the demo!" (but won't use it)
- "We got great feedback!" (but all feature requests, no usage)

**Fix**: Focus on behavior over opinions, retention over acquisition.

---

### 5. Building Instead of Validating

**What it looks like**:
- "Let's build it and see if anyone uses it"
- "It'll only take 2 weeks" (takes 2 months)
- Full build before any user contact

**Fix**: Always do cheapest possible test first, build only after validation.

---

## Validation Workflow: End-to-End Example

**Idea**: Mobile app for tracking baby sleep patterns

### Phase 1: Problem Validation

**Assumption**: "New parents struggle to understand their baby's sleep patterns"

**Experiment 1: Customer Interviews**
- Interview 10 new parents
- Ask about sleep tracking current methods, pain points
- Success criteria: 7/10 express frustration with current methods

**Result**: 9/10 keep notes on paper, all frustrated by inconsistency

**Conclusion**: Problem validated, proceed.

---

### Phase 2: Solution Validation (Concept)

**Assumption**: "Parents would use an app that auto-tracks sleep from smart monitor"

**Experiment 2: Landing Page**
- Create page describing solution
- Run ads targeting new parents
- Success criteria: 20% email signup rate

**Result**: 8% signup rate

**Conclusion**: Interest is lower than hoped. Talk to non-signups to understand why.

**Learning**: They don't have smart monitors, manual entry would be fine.

---

### Phase 3: Solution Validation (Refined)

**Assumption**: "Parents will manually log sleep times if it's fast"

**Experiment 3: Concierge MVP**
- Ask 5 parents to text sleep times
- Manually create charts/insights
- Send back daily summaries
- Success criteria: 4/5 use it for 2 weeks

**Result**: All 5 use it for 2 weeks, ask to keep using

**Conclusion**: Strong validation, build simple MVP.

---

### Phase 4: Build & Validate MVP

**Build**: Simple app with manual time entry + basic charts

**Experiment 4: Private Beta**
- 30 parents use MVP for 4 weeks
- Success criteria: 60% retention after 2 weeks, 40% after 4 weeks

**Result**: 70% 2-week retention, 50% 4-week retention

**Conclusion**: Exceeded criteria, prepare for launch.

---

This workflow: problem → concept → refined solution → MVP took 8 weeks and cost minimal development before validation.

---

## Validation Checklist by Stage

### Idea Stage
- [ ] Problem validated through customer interviews
- [ ] Current solutions identified and evaluated
- [ ] Target user segment defined and accessible
- [ ] Pain level assessed (nice-to-have vs. must-have)

### Concept Stage
- [ ] Solution concept tested with users
- [ ] Value proposition resonates
- [ ] Demand signal measured (signups, interest)
- [ ] Key assumptions identified and prioritized

### Pre-Build Stage
- [ ] Prototype tested with target users
- [ ] Core workflow validated
- [ ] Pricing validated (willingness to pay)
- [ ] Technical feasibility confirmed

### MVP Stage
- [ ] Beta users recruited
- [ ] Usage patterns observed
- [ ] Retention measured
- [ ] Unit economics validated

---

## Ready-to-Use Resources

### In `assets/`:
- **problem-validation-canvas.md**: Framework for validating problems before solutions
- **solution-validation-checklist.md**: Step-by-step checklist for solution validation
- **validation-experiment-template.md**: Design experiments to test assumptions

### In `references/`:
- **lean-startup-validation.md**: Build-Measure-Learn cycle, MVP types, pivot decisions
- **assumption-testing-methods.md**: Comprehensive assumption testing techniques

---

## Further Reading

**Books**:
- "The Lean Startup" by Eric Ries
- "The Mom Test" by Rob Fitzpatrick
- "Continuous Discovery Habits" by Teresa Torres
- "Testing Business Ideas" by Bland & Osterwalder

**Key Concepts**:
- Minimum Viable Product (MVP)
- Build-Measure-Learn
- Validated learning
- Pivot or persevere
- Assumption mapping
- Evidence-based product development

---

**Remember**: Validation isn't about proving you're right. It's about learning what's true. Seek evidence that you're wrong - that's the fastest path to building something valuable.
