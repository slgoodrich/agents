---
name: Growth Sprint Workflow
description: Intensive 4-week sprint to accelerate product growth through rapid experimentation
category: Growth
duration: 4 weeks
model: sonnet
---

# Growth Sprint Workflow

Focused 4-week sprint methodology for rapidly testing and implementing growth initiatives across acquisition, activation, retention, or revenue.

## Usage
```
/growth-sprint [growth goal, e.g., "increase activation" or "reduce churn"]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Growth goal or metric to improve (acquisition, activation, retention, revenue, referral)
- Current baseline metrics and performance
- Target improvement (percentage or absolute numbers)
- Timeline and resources available
- Known constraints or challenges
- Previous growth experiments tried

## Timeline: 4 Weeks

## Pre-Sprint: Preparation (Week 0)

### Define Growth Goal
```
Task: growth-pm agent
Set sprint focus and goal:
- Choose ONE growth metric to move
- Set ambitious but achievable target
- Define time-bound goal (4 weeks)

**Examples**:
- Increase signup conversion by 25%
- Improve Day 7 retention from 40% to 50%
- Grow weekly active users by 30%
- Increase free-to-paid conversion by 15%

**North Star Focus**:
Align goal to North Star Metric
Reference growth-frameworks skill
```

### Assemble Growth Team
```
Task: product-ops agent
Create dedicated growth sprint team:
- **Growth PM** - Sprint leader and coordinator
- **Engineer** - Build and ship experiments
- **Designer** - UI/UX for experiments
- **Data Analyst** - Metrics and analysis
- **Marketer** (optional) - Acquisition experiments

Commit to 100% dedicated time for 4 weeks
```

### Baseline Metrics
```
Task: data-scientist agent
Establish current state:
- Current performance on target metric
- Historical trends
- Breakdown by segment and channel
- Funnel analysis
- Cohort analysis
- Benchmark against industry

Create baseline metrics dashboard
```

## Week 1: Ideation & Prioritization

### Day 1-2: Growth Ideation
```
Task: growth-pm agent
Rapid growth ideation session:

**Brainstorm experiments for**:
- **Acquisition**: New channels, viral loops, partnerships
- **Activation**: Onboarding, aha moments, time-to-value
- **Retention**: Engagement loops, notifications, habit formation
- **Revenue**: Pricing, packaging, upsells, expansion
- **Referral**: Viral mechanics, incentives, sharing

**Quantity over quality**: 50-100+ ideas
**No filtering yet**: All ideas welcome

Use growth-frameworks and AARRR funnel
```

```
Task: growth-pm agent
Idea categories:
- **Quick wins** - High impact, low effort (<1 week)
- **Big bets** - High impact, high effort (2-4 weeks)
- **Moonshots** - Uncertain impact, high effort
- **Optimizations** - Low impact, low effort (continuous)

Generate ideas across categories
```

### Day 3-4: Idea Prioritization
```
Task: feature-prioritizer agent
Score ideas using ICE framework:
- **Impact**: Expected impact on goal metric (1-10)
- **Confidence**: How sure are we it'll work? (1-10)
- **Ease**: How easy to implement? (1-10)
- **ICE Score**: (Impact × Confidence × Ease) / 3

Prioritize top 20 ideas by ICE score
```

```
Task: growth-pm agent
Additional prioritization factors:
- **Learning value** - Even if fails, what will we learn?
- **Reversibility** - Can we undo if bad?
- **Dependencies** - Does it unblock other ideas?
- **Compound effect** - Builds foundation for future?

Refine priority list
```

### Day 5: Sprint Planning
```
Task: growth-pm agent
Plan 4-week sprint:

**Week 1**: 3-4 quick wins (test rapidly)
**Week 2**: 1-2 big bets (medium complexity)
**Week 3**: Continue big bets, start winners from week 1/2
**Week 4**: Scale winners, implement learnings

**Goal**: Ship 10-15 experiments in 4 weeks
Balance quick wins with bigger bets

Create experiment backlog
```

```
Command: /pm:sprint-planner
Duration: 4 weeks (growth sprint)
Plan experiments and resource allocation
```

## Week 2-4: Rapid Experimentation

### Experiment Design (Ongoing)
```
Task: growth-pm agent
For each experiment, define:

**Hypothesis**:
"If [change], then [metric] will [improve by X%], because [reason]"

**Success metrics**:
- Primary: Main goal metric
- Secondary: Supporting metrics
- Guardrails: Metrics that shouldn't decline

**Experiment design**:
- A/B test, multivariate, or launch & measure
- Sample size needed
- Duration (typically 5-14 days for statistical significance)
- Segments to test

**Implementation**:
- What to build/change
- Tracking and instrumentation
- QA and testing

Use experiment-design skill
```

### Rapid Build & Ship (Daily)
```
Task: technical-pm agent
Fast implementation cycle:

**Daily standup**:
- What shipped yesterday
- What shipping today
- Any blockers

**Shipping cadence**:
- Design → Build → QA → Ship: 1-3 days per experiment
- Ship multiple experiments per week
- Feature flags for easy rollback

**Speed over perfection**:
- MVT (minimum viable test)
- Polish later if wins
- Learn fast, iterate faster

Monitor: Ship at least 2-3 experiments per week
```

### Metrics Monitoring (Daily)
```
Task: data-scientist agent
Real-time experiment tracking:

**Daily metrics review**:
- All active experiments
- Early signals (directional, not conclusive)
- Guardrail metrics
- Statistical significance progress
- Anomalies or issues

**Weekly deep dive**:
- Completed experiments analysis
- Statistical significance achieved
- Segment analysis
- Unexpected insights

Create live growth dashboard
```

### Weekly Sprint Reviews
```
Task: growth-pm agent
End-of-week review:

**Review completed experiments**:
- Winners (ship to 100%)
- Losers (learn and move on)
- Neutral (iterate or abandon)

**Learnings**:
- Why did it win/lose?
- What did we learn about users?
- What's our next test?
- Any insights for other areas?

**Plan next week**:
- Double down on winners
- New experiments based on learnings
- Adjust priorities

Document: Create experiment log with results
```

## Week 4: Scale & Iterate

### Scale Winners
```
Task: growth-pm agent
Implement winning experiments:
- Roll out to 100% of users
- Polish and optimize
- Instrument for ongoing monitoring
- Document for team learnings
- Build on success with iterations

Don't just run experiments - ship wins!
```

### Iterate on Learnings
```
Task: growth-pm agent
V2 experiments based on learnings:
- Winning experiments: How to make even better?
- Losing experiments: What else could we try?
- Surprising insights: What does this enable?

**Example**:
- Test 1: New signup CTA wins
- Test 2: Try different CTA copy variations
- Test 3: Try CTA in additional locations
- Test 4: Test CTA design variations

Compound wins through iteration
```

### Build Growth Loops
```
Task: growth-pm agent
Design sustainable growth loops:
- Identify self-reinforcing cycles
- Content loops
- Viral loops
- Paid loops
- Build systems, not one-off wins

Reference growth-frameworks and growth loops
```

## Sprint Retrospective

### Results Analysis
```
Task: data-scientist agent
Comprehensive sprint analysis:

**Quantitative**:
- Goal metric movement (vs. target)
- Experiments run (goal: 10-15)
- Win rate (typical: 10-30%)
- Impact of winners
- Overall velocity and learnings

**Statistical rigor**:
- Proper significance testing
- Segment analysis
- Long-term impact projection

Create sprint results report
```

### Qualitative Review
```
Task: growth-pm agent
Sprint retrospective:

**What worked well**:
- Successful experiments
- Good processes
- Team dynamics
- Velocity and speed

**What didn't work**:
- Failed experiments (learnings?)
- Process bottlenecks
- Communication gaps
- Resource constraints

**What to improve**:
- Next sprint improvements
- Process optimizations
- Tool or capability needs
- Team composition

**Key learnings**:
- User behavior insights
- Channel effectiveness
- Feature adoption patterns
- Growth levers discovered

Document for future sprints
```

### Roadmap Integration
```
Task: growth-pm agent
Integrate learnings into roadmap:
- Which wins to scale and build on
- Which ideas to continue testing
- New hypotheses to explore
- Platform capabilities to build

Growth sprint → ongoing growth practice
```

```
Command: /pm:roadmap-builder
Context: Growth sprint learnings
Update roadmap with growth initiatives
```

## Deliverables

1. **Growth Goal** - Specific, measurable, time-bound target
2. **Experiment Backlog** - Prioritized list of 50+ ideas
3. **Experiment Log** - All tests run with hypotheses and results
4. **Results Dashboard** - Real-time metrics tracking
5. **Sprint Results Report** - Comprehensive analysis of outcomes
6. **Learnings Document** - User insights and growth discoveries
7. **Roadmap Updates** - Integration of winning experiments

## Success Metrics
- Goal metric improvement (target: 10-30% lift)
- Experiments shipped (target: 10-15 in 4 weeks)
- Win rate (10-30% is normal, high-quality ideas)
- Learnings velocity (insights per experiment)
- Team engagement and momentum
- Sustainable practices implemented

## Growth Sprint Best Practices

### DO:
- Set ONE clear, measurable goal
- Ship quickly, learn faster
- Run many small experiments
- Focus on high-ICE ideas
- Celebrate wins and learnings
- Document everything
- Iterate on winners
- Build sustainable loops

### DON'T:
- Try to move all metrics at once
- Build perfect experiments (MVT)
- Wait for statistical significance before next test
- Give up on losing experiments (learn why!)
- Ship winners without tracking
- Ignore guardrail metrics
- Stop after sprint ends

## Experiment Types by Focus Area

### Acquisition:
- Landing page optimization
- Channel experiments (SEO, paid, content, social)
- Viral loops and referrals
- Partnership integrations
- Top-of-funnel messaging

### Activation:
- Onboarding flow optimization
- Time-to-value reduction
- Aha moment clarity
- Feature discovery
- Empty state experiences

### Retention:
- Engagement loops and triggers
- Email/notification optimization
- Habit formation mechanics
- Re-engagement campaigns
- Feature adoption nudges

### Revenue:
- Pricing and packaging tests
- Upgrade prompts and messaging
- Trial length and structure
- Payment flow optimization
- Expansion revenue opportunities

### Referral:
- Invitation mechanisms
- Incentive structures
- Sharing flows
- Social proof
- Network effects

## Common Growth Sprint Pitfalls

- **Analysis paralysis** - Waiting too long to ship
- **Scope creep** - Building too much per experiment
- **Stat sig obsession** - Not shipping directional winners
- **One and done** - Not iterating on winners
- **Ignoring losers** - Not learning from failures
- **No compound effect** - Random experiments vs. strategic themes
- **Process over pace** - Too much bureaucracy
- **Polish trap** - Making it perfect vs. testing quickly

## After the Sprint

**Continue growth practice**:
- Weekly experiment reviews
- Continuous testing culture
- Dedicated growth capacity (20% time)
- Quarterly growth sprints
- Compound learnings over time

**Build growth capability**:
- Experimentation platform and tools
- Analytics and attribution
- Cross-functional collaboration
- Data-driven decision culture
- Growth team or guild

Growth sprint is a start, not an end. Build continuous growth muscle.
