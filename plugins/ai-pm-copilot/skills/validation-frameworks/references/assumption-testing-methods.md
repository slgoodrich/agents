# Assumption Testing Methods: Comprehensive Guide

How to systematically test product assumptions with the right methods for each type.

## Table of Contents

- [Assumption Testing Framework](#assumption-testing-framework)
- [Types of Assumptions](#types-of-assumptions)
- [Testing Methods by Assumption Type](#testing-methods-by-assumption-type)
- [Assumption Testing Roadmap](#assumption-testing-roadmap)
- [Choosing the Right Method](#choosing-the-right-method)
- [Key Principles](#key-principles)

---

## Assumption Testing Framework

```
1. Identify assumption
2. Classify assumption type
3. Assess risk and priority
4. Select testing method(s)
5. Design experiment
6. Run test
7. Analyze results
8. Update assumptions
```

---

## Types of Assumptions

### Desirability Assumptions

**Question**: Will people want this?

**Examples**:

- "Users want automated time tracking"
- "Customers will pay $99/month"
- "Freelancers check this app daily"
- "Parents care about screen time limits"

**Test with**:

- Customer interviews
- Landing page tests
- Pre-sales
- Prototype testing
- Surveys

---

### Usability Assumptions

**Question**: Can people use this?

**Examples**:

- "Users can complete checkout in under 2 minutes"
- "Non-technical users understand the dashboard"
- "Mobile interface is sufficient (no desktop needed)"
- "Users can set up integrations themselves"

**Test with**:

- Prototype testing
- Usability testing
- Think-aloud sessions
- Task completion tests
- Wizard of Oz MVP

---

### Feasibility Assumptions

**Question**: Can we build this?

**Examples**:

- "We can process 1M transactions per second"
- "Algorithm can achieve 95% accuracy"
- "Integration with API X is possible"
- "We can build this in 3 months"

**Test with**:

- Technical spikes
- Proof of concept
- API testing
- Prototype development
- Expert consultation

---

### Viability Assumptions

**Question**: Should we build this? Will it be sustainable?

**Examples**:

- "CAC will be under $50"
- "LTV will exceed $200"
- "We can acquire 10,000 users in 6 months"
- "Support costs will be under $10 per user"

**Test with**:

- Market research
- Channel tests
- Pricing experiments
- Financial modeling
- Competitor analysis

---

## Testing Methods by Assumption Type

---

## 1. Customer Interviews

### Best For

- **Desirability**: Problem validation, needs assessment
- Early-stage understanding
- Qualitative insights

### How It Works

1. Recruit target users (5-15 for qualitative)
2. Ask open-ended questions about problems, not solutions
3. Listen for pain points, workflows, current solutions
4. Probe for evidence of problem severity

### Sample Questions

**Problem discovery**:

- "Tell me about the last time you [relevant activity]"
- "What's frustrating about [current process]?"
- "How do you currently solve [problem]?"
- "How much time/money does this cost you?"

**Solution validation**:

- "I'm going to describe something—tell me what you think"
- "How would this fit into your workflow?"
- "What concerns would you have about this?"
- "What would you pay for something like this?"

### Validation Criteria

- **Strong**: 8/10 users express significant pain, current solutions inadequate
- **Moderate**: 5-7/10 have problem, workarounds acceptable
- **Weak**: < 5/10 have problem or don't care

### Pitfalls

- Leading questions: "Wouldn't you love...?"
- Asking about hypothetical future behavior
- Interviewing friends/family (they'll lie to be nice)
- Confusing enthusiasm with commitment

### Cost & Speed

- **Cost**: Low (just time)
- **Speed**: 1-2 weeks
- **Sample size**: 5-15 for qualitative insights

---

## 2. Surveys

### Best For

- **Desirability**: Quantifying problem prevalence
- **Viability**: Market sizing
- Scaling insights from interviews

### How It Works

1. Draft questions (mix of multiple choice and open-ended)
2. Distribute to target audience
3. Analyze quantitative and qualitative responses
4. Look for patterns and segmentation

### Survey Types

**Problem validation surveys**:

- How often do you experience [problem]?
- How much time/money does it cost?
- What have you tried to solve it?
- How important is solving this? (1-10)

**Solution interest surveys**:

- How interested are you in [solution]? (1-5)
- What would you pay for this?
- What concerns do you have?
- When would you start using this?

**Feature prioritization surveys**:

- Rank these features by importance
- Which features are must-have vs. nice-to-have?
- What's missing from this list?

### Validation Criteria

- **Problem prevalence**: > 40% experience problem regularly
- **Interest**: > 30% "very interested" (not just "interested")
- **Willingness to pay**: Price point alignment with value perceived

### Pitfalls

- Selection bias (who takes surveys?)
- Stated preferences ≠ actual behavior
- Leading questions
- Survey fatigue (too long)

### Cost & Speed

- **Cost**: Low to medium (tools, incentives)
- **Speed**: 1-2 weeks
- **Sample size**: 100+ for quantitative confidence

---

## 3. Landing Page Tests

### Best For

- **Desirability**: Demand validation
- **Viability**: Channel testing, CAC estimation
- Testing value proposition messaging

### How It Works

1. Create landing page describing product
2. Explain value proposition
3. Call-to-action (signup, pre-order, waitlist)
4. Drive traffic (ads, content, social)
5. Measure conversion rate

### Page Elements

- Clear headline (value proposition)
- Subheading (who it's for, key benefit)
- Visuals (mockup, explainer video)
- Feature list or benefits
- Social proof (if available)
- CTA (email signup, pre-order, "Request Demo")

### Traffic Sources

- Paid ads (Facebook, Google, LinkedIn)
- Content marketing (blog posts)
- Social media
- Communities (Reddit, forums)
- Email to existing list

### Validation Criteria

- **Strong**: > 30% email signup rate (warm traffic)
- **Moderate**: 10-30% signup rate
- **Weak**: < 10% signup rate

**Adjust for traffic source**:

- Warm traffic (existing audience): Higher baseline
- Cold traffic (ads): Lower baseline acceptable

### Pitfalls

- Wrong traffic source (not target audience)
- Unclear value proposition
- Asking too much (immediate purchase vs. email)
- No follow-up (measure signups but not activation)

### Cost & Speed

- **Cost**: $500-$2000 for ads + landing page
- **Speed**: 1-2 weeks
- **Sample size**: 500-1000 visitors minimum

---

## 4. Prototype Testing

### Best For

- **Desirability**: Solution validation
- **Usability**: Interaction validation
- Testing user flows before development

### How It Works

1. Create clickable prototype (Figma, Sketch, InVision)
2. Recruit target users (5-10)
3. Give realistic tasks
4. Observe completion, confusion, errors
5. Ask follow-up questions

### Prototype Fidelity

**Low-fidelity** (paper, wireframes):

- Test concepts and flows
- Fast to create and iterate
- Good for early validation

**Medium-fidelity** (clickable mockups):

- Test interactions and workflows
- More realistic feedback
- Balance of speed and realism

**High-fidelity** (near-final design):

- Test usability and polish
- Expensive to create
- Use after concept validated

### Tasks to Test

- Most critical user goal (must work)
- Most frequent task (will be used most)
- Most complex task (likely to break)
- Recently changed features (regression testing)

### Validation Criteria

- **Strong**: 8/10 complete core tasks without help
- **Moderate**: 5-7/10 complete, some confusion
- **Weak**: < 5/10 complete or major usability issues

### Pitfalls

- Over-explaining before letting them try
- Helping too quickly when stuck
- Testing with designers or developers
- Not testing realistic tasks

### Cost & Speed

- **Cost**: Low (design time only)
- **Speed**: 1-2 weeks
- **Sample size**: 5-10 users per round

---

## 5. Concierge MVP

### Best For

- **Desirability**: Value validation
- **Viability**: Willingness to pay
- Understanding what "done right" looks like

### How It Works

1. Recruit small group of users (3-10)
2. Manually deliver the service/outcome
3. Charge money (if that's the model)
4. Learn what users value
5. Measure retention and satisfaction

### Example: Meal Planning Service

- **Not concierge**: Build app that generates meal plans
- **Concierge**: Personally create meal plans for 5 customers each week
- **Learn**: What makes a good plan? What do they customize? Do they follow it?

### When to Use

- Before building automation
- When outcome is clear but path is uncertain
- Testing willingness to pay for outcome

### Validation Criteria

- **Strong**: 7/10 users continue for 4+ weeks, would pay target price
- **Moderate**: 5-7/10 continue for 2-4 weeks, some price resistance
- **Weak**: < 5/10 continue past week 1

### Pitfalls

- Providing unrealistic quality (not sustainable at scale)
- Not charging money (can't validate willingness to pay)
- Helping too much (not replicable)

### Cost & Speed

- **Cost**: Low tech, high time
- **Speed**: 2-4 weeks to learn
- **Sample size**: 3-10 users

---

## 6. Wizard of Oz MVP

### Best For

- **Desirability**: Behavioral validation
- **Feasibility**: Testing expensive-to-build features
- **Usability**: Natural usage patterns

### How It Works

1. Build user-facing interface
2. Backend is manual (humans, not algorithms)
3. Users think it's automated
4. Observe natural behavior
5. Decide if automation is worth building

### Example: AI Feature

- **Not Wizard of Oz**: Build machine learning model first
- **Wizard of Oz**: Build UI, humans provide "AI" responses
- **Learn**: Do users find AI valuable? How do they use it?

### When to Use

- Expensive backend to build
- Want to test user behavior with "real" product
- Validating automation before building it

### Validation Criteria

- **Strong**: Users engage naturally, don't notice it's manual, willing to pay
- **Moderate**: Some usage, would use if improved
- **Weak**: Low usage or users detect it's not automated

### Pitfalls

- Manual process not sustainable at scale
- Users detect it's fake (ruins trust)
- Response times not realistic

### Cost & Speed

- **Cost**: Medium (build frontend)
- **Speed**: 2-4 weeks
- **Sample size**: 10-50 users

---

## 7. Fake Door Test

### Best For

- **Desirability**: Feature demand
- **Viability**: Prioritization
- Testing within existing product

### How It Works

1. Add UI element for non-existent feature
2. Track clicks/interest
3. Show "Coming soon" message when clicked
4. Measure demand before building

### Example

- Add "Export to Excel" button
- Track how many users click it
- Show "We're working on this! Want to be notified?"
- Decide if usage warrants building it

### When to Use

- Feature prioritization
- Inside existing product
- Before committing to roadmap

### Validation Criteria

- **Strong**: > 20% of active users click/request
- **Moderate**: 10-20% show interest
- **Weak**: < 10% interest

### Pitfalls

- Users think feature is broken (be transparent)
- Overusing creates "boy who cried wolf" effect
- Not following up (frustrated users)

### Cost & Speed

- **Cost**: Very low (UI change only)
- **Speed**: Days
- **Sample size**: Existing user base

---

## 8. Pre-Sales / Pre-Orders

### Best For

- **Desirability**: Commitment validation
- **Viability**: Revenue validation
- Strongest demand signal

### How It Works

1. Offer product for pre-order before building
2. Real payment (or deposit)
3. Clear delivery timeline
4. Measure conversion rate

### Variations

**Full pre-sale**:

- Charge full price
- Deliver later or refund
- Strongest signal

**Deposit**:

- Charge partial amount ($50 of $500)
- Refundable or applied to purchase
- Medium signal

**Refundable pre-order**:

- Charge full price, easy refund
- Less strong but still meaningful

### Validation Criteria

- **Strong**: > 20% conversion to pre-order
- **Moderate**: 5-20% conversion
- **Weak**: < 5% conversion

### Pitfalls

- Not delivering on promise (ruins reputation)
- Long delivery time (refunds pile up)
- Not building if pre-sales fail (sunk cost fallacy)

### Cost & Speed

- **Cost**: Low (landing page + payment)
- **Speed**: 1-2 weeks
- **Sample size**: 100+ potential customers

---

## 9. Smoke Test

### Best For

- **Desirability**: Very early demand validation
- **Viability**: Market testing
- Before any development

### How It Works

1. Create appearance of product (ads, landing page)
2. Measure how many people try to buy/sign up
3. Explain it's not ready yet, collect interest
4. No actual product exists

### Example

- Run ads for new product
- Landing page with pricing and "Buy Now"
- Click shows "Not available yet, join waitlist"
- Measure click-through rate and "purchase intent"

### When to Use

- Very early stage
- Validating demand before building anything
- Testing multiple concepts to pick one

### Validation Criteria

- **Strong**: > 5% click "buy" or "sign up"
- **Moderate**: 2-5% show purchase intent
- **Weak**: < 2% engagement

### Pitfalls

- Misleading users (ethical concerns)
- Burning early interest (announced too early)
- Not following up with waitlist

### Cost & Speed

- **Cost**: Very low
- **Speed**: Days
- **Sample size**: 500-1000 visitors

---

## 10. A/B Testing

### Best For

- **Usability**: Interaction optimization
- **Viability**: Conversion optimization
- Incremental improvements

### How It Works

1. Create two versions (A and B)
2. Split traffic 50/50
3. Measure conversion or key metric
4. Determine statistical significance
5. Implement winner

### What to Test

**Value proposition**:

- Headline variations
- Feature ordering
- Benefit framing

**Pricing**:

- Price points
- Packaging
- Discount strategies

**Usability**:

- Button placement
- Form length
- Navigation structure

### Validation Criteria

- **Statistically significant**: p < 0.05 typically
- **Practically significant**: > 10% improvement worth implementing
- **Sample size**: Depends on baseline and effect size (use calculator)

### Pitfalls

- Testing too many things at once
- Not enough traffic for significance
- Stopping test too early
- Testing the wrong thing (focus on high-impact changes)

### Cost & Speed

- **Cost**: Low to medium (tool costs)
- **Speed**: 1-4 weeks (depends on traffic)
- **Sample size**: 100+ conversions per variant minimum

---

## 11. Technical Spike / Proof of Concept

### Best For

- **Feasibility**: Technical validation
- **Viability**: Development time estimation
- De-risking technical unknowns

### How It Works

1. Identify technical uncertainty
2. Build minimal proof of concept
3. Test if approach works
4. Estimate effort for full build

### Examples

- "Can we integrate with Salesforce API?" → Build integration prototype
- "Can algorithm run fast enough?" → Build performance test
- "Will this scale?" → Load testing

### When to Use

- Technical unknowns blocking decision
- Before committing to architecture
- Estimating development effort

### Validation Criteria

- **Strong**: Proof of concept works, path forward clear
- **Moderate**: Possible but harder than expected
- **Weak**: Not feasible or too expensive

### Pitfalls

- Building too much (proof of concept becomes production)
- Not throwing away spike code (technical debt)
- Ignoring learnings (committing to infeasible approach)

### Cost & Speed

- **Cost**: Medium to high (engineering time)
- **Speed**: 1-2 weeks
- **Sample size**: N/A (technical test)

---

## 12. Channel Testing

### Best For

- **Viability**: Customer acquisition validation
- **Desirability**: Message/market fit
- Finding scalable growth channels

### How It Works

1. Identify potential channels (ads, content, SEO, sales, etc.)
2. Run small test in each channel
3. Measure CAC and conversion
4. Double down on winners

### Channels to Test

**Paid**:

- Google Ads
- Facebook/Instagram Ads
- LinkedIn Ads

**Organic**:

- SEO
- Content marketing
- Social media

**Direct**:

- Sales outreach
- Partnerships
- Referrals

### Validation Criteria

- **Strong**: CAC < 1/3 of LTV, channel is scalable
- **Moderate**: CAC < LTV but economics tight
- **Weak**: CAC > LTV or not scalable

### Pitfalls

- Giving up on channel too quickly (need time to optimize)
- Spreading budget too thin (test channels sequentially)
- Ignoring cohort retention (cheap users who churn don't matter)

### Cost & Speed

- **Cost**: $500-$2000 per channel test
- **Speed**: 2-4 weeks per channel
- **Sample size**: 50-100 conversions minimum

---

## Assumption Testing Roadmap

### Early Stage (Pre-Product)

1. **Customer interviews** - Validate problem
2. **Landing page test** - Validate interest
3. **Prototype test** - Validate usability
4. **Concierge MVP** - Validate value

### Build Stage (MVP Development)

1. **Technical spike** - Validate feasibility
2. **Wizard of Oz MVP** - Validate behavior
3. **Pre-sales** - Validate willingness to pay
4. **Fake door tests** - Prioritize features

### Growth Stage (Post-Launch)

1. **A/B testing** - Optimize conversion
2. **Channel testing** - Validate CAC
3. **Cohort analysis** - Validate retention
4. **Pricing experiments** - Optimize revenue

---

## Choosing the Right Method

### Decision Tree

**Question to answer** → **Best method**

"Do people have this problem?" → **Customer interviews**
"How common is the problem?" → **Survey**
"Will people pay for this?" → **Pre-sales**
"Can people use this?" → **Prototype test**
"Is this valuable enough?" → **Concierge MVP**
"Will this work technically?" → **Technical spike**
"Which channel works?" → **Channel testing**
"Which version is better?" → **A/B testing**

---

## Key Principles

1. **Start cheap**: Cheaper tests first, expensive tests later
2. **Be specific**: Clear success criteria before testing
3. **Seek disconfirmation**: Try to prove yourself wrong
4. **Behavior over opinions**: What people do > what they say
5. **Iterate quickly**: Many small tests > one big test
6. **Fail fast**: Negative results are valuable
7. **Follow the data**: Be willing to pivot

---

**Remember**: The goal isn't to validate that you're right. It's to learn what's true as quickly and cheaply as possible.
