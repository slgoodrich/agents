---
name: Product-Market Fit Assessment Workflow
description: Systematic process to measure and improve product-market fit
category: Discovery
duration: 3-4 weeks
model: sonnet
---

# Product-Market Fit Assessment Workflow

Comprehensive framework for measuring product-market fit, identifying gaps, and creating an action plan to achieve or strengthen PMF.

## Usage
```
/pmf-assessment
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Product stage (pre-launch, early, growth, mature)
- Current metrics (users, revenue, growth rate, retention, NPS)
- Time since launch or pivot
- Symptoms observed (good or concerning signs)
- Market and competitive context
- Why assessing PMF now (fundraising, strategic planning, concerns)

## Timeline: 3-4 Weeks

## Phase 1: PMF Measurement (Week 1-2)

### Week 1: Quantitative Assessment

**Sean Ellis PMF Survey**
```
Task: user-researcher agent
Deploy Sean Ellis PMF survey to active users:

Survey questions:
1. "How would you feel if you could no longer use [product]?"
   - Very disappointed
   - Somewhat disappointed
   - Not disappointed

2. "What type of people do you think would most benefit from [product]?"

3. "What is the main benefit you receive from [product]?"

4. "How can we improve [product] for you?"

Target: 40%+ "very disappointed" = PMF achieved
Sample: 100+ active users for statistical significance
Reference product-market-fit skill
```

```
Task: data-scientist agent
Analyze retention and engagement metrics:
- **Retention curves** by cohort (Day 1, 7, 30, 90)
- **DAU/MAU ratio** (>20% is healthy)
- **L7/L28 ratio** (weekly active / monthly active)
- **Activation rate** (% reaching aha moment)
- **Time to value** (how long to first value)
- **Feature adoption** (core features usage)
- **Session frequency** and duration
- **Churn rate** (<5% monthly for B2C, <2% for B2B)

Create PMF metrics dashboard
```

```
Task: data-scientist agent
Analyze growth metrics:
- **Organic vs. paid** customer acquisition
- **Viral coefficient** (users referred per user)
- **Word-of-mouth** and referral rates
- **CAC trends** (increasing or decreasing)
- **LTV:CAC ratio** (>3:1 is healthy)
- **Payback period** (<12 months)
- **Revenue growth** rate

Organic growth signals strong PMF
```

```
Task: monetization-expert agent
Analyze revenue and unit economics:
- **Conversion rate** (free to paid)
- **ARPU/ARPA** trends
- **MRR/ARR growth** rate
- **Net revenue retention** (>100% ideal)
- **Expansion revenue** rate
- **Logo vs. revenue retention**
- **Customer payback period**

Create unit economics analysis
```

### Week 2: Qualitative Assessment

**Customer Interviews**
```
Task: user-researcher agent
Conduct 20-30 customer interviews across segments:

**High-expectation customers** (very disappointed group):
- Why would you be very disappointed?
- What would you use instead?
- What's the main value you get?
- What should we build next?
- Who else should use this?

**Medium-expectation customers** (somewhat disappointed):
- What's preventing you from loving this?
- What's missing?
- What would make you very disappointed to lose it?

**Low-expectation customers** (not disappointed):
- Why isn't this valuable to you?
- What would you use instead?
- Are you the right target customer?

Create interview synthesis report
Reference continuous-discovery skill
```

```
Task: customer-insights agent
Analyze customer feedback sources:
- **Support tickets**: What are common issues?
- **Feature requests**: What do they want?
- **NPS comments**: Why promoters promote, detractors detract
- **Churn surveys**: Why did they leave?
- **Sales calls**: Why won't prospects buy?
- **Reviews**: What do they love/hate?

Create customer feedback synthesis
```

```
Task: competitive-analyst agent
Analyze competitive win/loss:
- **Why do we win?** (unique value)
- **Why do we lose?** (gaps)
- **Competitor migrations**: Who are they going to?
- **Market positioning**: Where do we fit?
- **Differentiation**: What makes us unique?

Create competitive analysis report
```

## Phase 2: Segment Analysis (Week 2)

### Identify Best-Fit Customers
```
Task: customer-insights agent
Segment customers by PMF signals:

**Superhuman PMF Engine approach**:
1. Segment by "very disappointed" response
2. Analyze high-expectation customers (your best fit)
3. Identify their common characteristics:
   - Demographics
   - Firmographics
   - Use cases
   - Behaviors
   - Needs

Create best-fit customer profile
Reference product-market-fit skill
```

```
Task: data-scientist agent
Quantitative segment analysis:
- Cohort users by acquisition channel, date, attributes
- Analyze retention by segment
- Revenue and LTV by segment
- Engagement patterns by segment
- Conversion rates by segment

Identify: Which segments have strongest PMF?
```

```
Command: /pm:persona-creator
Context: Best-fit customers (PMF segment)
Create detailed persona for strongest PMF segment
```

## Phase 3: Gap Analysis (Week 3)

### Identify PMF Gaps
```
Task: product-strategist agent
Analyze PMF gaps across framework:

**Product gaps**:
- Missing must-have features
- Usability friction
- Performance issues
- Integration needs
- Technical debt impact

**Market gaps**:
- Wrong target customer
- Positioning unclear
- Messaging not resonating
- Competition better positioned

**Go-to-market gaps**:
- Wrong channels
- Poor onboarding
- Activation issues
- Pricing/packaging misaligned

**Value delivery gaps**:
- Time to value too long
- Aha moment not clear
- Core use case not solved well
- Alternative solutions better

Create comprehensive gap analysis
```

```
Task: discovery-facilitator agent
Map current state to desired PMF state:

**Current state**:
- PMF score: X%
- Best-fit segment size
- Key friction points
- Competitive positioning

**Desired state**:
- PMF score: >40%
- Expanded best-fit segment
- Friction removed
- Clear differentiation

**Gap**: What needs to change?
Create PMF gap map
```

## Phase 4: Improvement Strategy (Week 3-4)

### Double Down on What's Working
```
Task: product-strategist agent
Identify what high-expectation customers love:
- Which features do they value most?
- What outcomes do they achieve?
- What makes us uniquely valuable?
- What keeps them engaged?

**Strategy**: Double down
- Make these features even better
- Expand related capabilities
- Emphasize in marketing
- Optimize for this workflow

Create "double down" roadmap
```

### Address High-Expectation Customer Gaps
```
Task: requirements-engineer agent
Based on high-expectation customer feedback:
- What do they say is missing?
- What friction do they experience?
- What features do they request?
- What would increase their usage?

**Strategy**: Address gaps for best-fit customers
- Prioritize their must-haves
- Fix their pain points
- Build what they need next
- Improve their workflow

Create gap-filling requirements
```

### Expand to Adjacent Segments
```
Task: product-strategist agent
Identify adjacent segments with PMF potential:
- Similar to high-expectation customers
- Similar jobs-to-be-done
- Reachable with small product changes
- Addressable market size

**Strategy**: Expand PMF segment
- What small changes unlock new segment?
- How to acquire them?
- Messaging for each segment

Create segment expansion strategy
```

### Ignore or Deprioritize Poor-Fit Segments
```
Task: product-strategist agent
Identify poor-fit segments:
- "Not disappointed" group
- Low retention segments
- High support cost, low value
- Confused by product
- Want different product

**Strategy**: Politely ignore
- Don't build for them
- Consider sunsetting features they want
- Stop marketing to them
- Focus resources on best-fit

Create "what not to build" list
```

## Phase 5: Action Plan (Week 4)

### PMF Improvement Roadmap
```
Command: /pm:roadmap-builder
Timeframe: 6 months
Create PMF improvement roadmap:
- **Now (0-3 months)**: Fix critical gaps for best-fit customers
- **Next (3-6 months)**: Double down on what's working
- **Later (6+ months)**: Expand to adjacent segments
Prioritize ruthlessly for PMF
```

```
Task: feature-prioritizer agent
Prioritize PMF improvements:
- Impact on "very disappointed" score
- Impact on best-fit customer satisfaction
- Impact on retention
- Effort and resources required
- Time to impact

Use RICE scoring focused on PMF impact
```

```
Task: gtm-planner agent
Adjust go-to-market for PMF:
- **Target**: Best-fit customer segment only
- **Messaging**: Emphasize what they love
- **Channels**: Where best-fit customers are
- **Onboarding**: Optimize for aha moment
- **Success**: Support workflows that drive retention

Create PMF-focused GTM strategy
Reference go-to-market-playbooks skill
```

### OKRs for PMF Improvement
```
Command: /pm:okr-framework
Create PMF improvement OKRs:

Example Objective: "Achieve strong product-market fit with [segment]"
Key Results:
- Increase "very disappointed" from X% to 40%+
- Improve Day 30 retention from X% to Y%
- Increase NPS from X to 50+
- Grow organic signups by X%
```

### Quick Wins
```
Task: product-ops agent
Identify quick wins (4-6 weeks):
- Onboarding improvements
- Feature discoverability
- Performance optimizations
- Top feature requests from best-fit customers
- Messaging clarity

Create quick wins sprint plan
```

## Phase 6: Execution & Monitoring (Ongoing)

### Monthly PMF Tracking
```
Task: data-scientist agent
Track PMF metrics monthly:
- Sean Ellis PMF score
- Retention curves
- NPS by segment
- Revenue and unit economics
- Organic growth rate

Create monthly PMF dashboard
```

```
Task: discovery-facilitator agent
Continuous customer discovery:
- Weekly interviews with best-fit customers
- Ongoing feedback collection
- Rapid iteration based on learnings
- Build conviction in PMF improvements

Reference continuous-discovery skill
```

### Quarterly PMF Reassessment
```
Task: product-strategist agent
Quarterly PMF review:
- Is PMF score improving?
- Are we building for right customers?
- Is retention strengthening?
- Is organic growth accelerating?
- Should we adjust strategy?

Make course corrections as needed
```

## Deliverables

1. **PMF Score Report** - Sean Ellis survey results and analysis
2. **Metrics Dashboard** - Retention, engagement, growth metrics
3. **Best-Fit Customer Profile** - Characteristics of strongest PMF segment
4. **Gap Analysis** - Product, market, GTM gaps
5. **Improvement Strategy** - What to double down on, fix, ignore
6. **PMF Roadmap** - 6-month plan to strengthen PMF
7. **OKRs** - Measurable PMF improvement goals
8. **Monitoring Plan** - Ongoing tracking and iteration

## PMF Maturity Levels

### Pre-PMF (<40% very disappointed)
**Symptoms**:
- Retention curves don't plateau
- High churn
- Mostly paid acquisition
- Long sales cycles
- Unclear value prop

**Focus**: Rapid experimentation, find right customer and problem

### Early PMF (40-60% very disappointed)
**Symptoms**:
- Some retention improvement
- Word-of-mouth starting
- Segment clarity emerging
- Some organic growth

**Focus**: Double down on best-fit customers, remove friction

### Strong PMF (60%+ very disappointed)
**Symptoms**:
- Strong retention
- Significant organic growth
- Clear differentiation
- Customers tell you what to build
- Revenue growing efficiently

**Focus**: Scale go-to-market, expand to adjacent segments

## Success Metrics (6 months)
- PMF score >40% (strong PMF: >60%)
- Day 30 retention >40%
- NPS >50
- Organic growth >30% of total
- LTV:CAC >3:1
- Clear best-fit customer segment identified
- Team conviction and clarity on who we serve

## Common PMF Mistakes
- Assuming you have PMF when you don't
- Building for everyone instead of best-fit segment
- Focusing on new features before fixing core experience
- Scaling marketing before achieving PMF
- Ignoring retention to chase acquisition
- Not talking to customers regularly
- Premature optimization
- Giving up too early (or persisting too long)
