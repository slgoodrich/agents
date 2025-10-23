# Journey Mapper

Create customer journey maps showing user touchpoints, emotions, pain points, and opportunities across the full user experience.

## Usage

```
/customer-insights:journey-map [user persona or scenario] [optional: journey stage focus, research data]
```

## What This Command Does

1. Maps the end-to-end customer journey from awareness to advocacy
2. Identifies user actions, thoughts, emotions, and touchpoints at each stage
3. Highlights pain points and moments of delight throughout the experience
4. Reveals gaps, friction, and opportunities for improvement
5. Aligns teams around the user perspective and experience
6. Takes 1 hour vs 3-4 hours of manual journey mapping

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Journey Context**:
- What journey are we mapping? (specific user flow or full lifecycle)
- Which persona is this journey for? (link to persona if exists)
- What's the start and end point? (first touchpoint to final outcome)
- Why are you creating this journey map? (identify friction, improve onboarding, etc.)

**Journey Scope**:
- What stages should we map? (awareness, consideration, purchase, usage, advocacy)
- Focus on specific stage? (e.g., just onboarding, or full end-to-end)
- Channels included? (web, mobile, email, support, physical, etc.)
- Timeframe? (hours, days, weeks, months)

**Research Data Available**:
- User research conducted? (interviews, surveys, usability tests)
- Analytics data? (conversion funnels, drop-off points, usage patterns)
- Customer feedback? (support tickets, reviews, NPS comments)
- Existing journey maps to update?

**Touchpoints Known**:
- What channels/platforms do users interact with? (website, app, email, support)
- What teams/departments are involved? (sales, CS, support, product)
- What systems/tools are involved? (CRM, email platform, product)

**Example Input**:
```
Journey: SaaS trial signup to paid conversion
Persona: Mid-market sales manager (link to persona doc)
Stages: Awareness → Trial Signup → Onboarding → First Value → Purchase Decision
Timeframe: 14-day trial period
Research: 15 user interviews, analytics on 500 trial users, 200 survey responses
Goal: Identify why 60% of trials don't convert, improve conversion rate
Touchpoints: Website, product (web + mobile), email, sales calls, support chat
```

### 2. Define Journey Stages

**Common Journey Frameworks**:

**A. AIDA (Awareness, Interest, Desire, Action)**:
- Simple, marketing-focused
- Good for acquisition journeys

**B. AARRR (Awareness, Acquisition, Activation, Retention, Referral)**:
- Pirate Metrics framework
- Good for SaaS and growth products

**C. Full Lifecycle** (Most common for journey maps):
1. **Awareness**: User becomes aware of problem and solution
2. **Consideration**: User evaluates options
3. **Purchase/Signup**: User commits (buy or trial)
4. **Onboarding**: User gets started, first usage
5. **Usage/Engagement**: User becomes regular active user
6. **Loyalty/Retention**: User renews, stays long-term
7. **Advocacy**: User recommends, refers others

**D. Custom Stages**: Adapt to your specific journey (e.g., B2B enterprise sales has different stages)

### 3. Map Each Journey Stage

**For Each Stage, Capture**:
1. **Actions**: What user physically does (clicks, searches, calls, etc.)
2. **Thoughts**: What they're thinking (questions, concerns, expectations)
3. **Emotions**: How they feel (frustrated, excited, confused, delighted)
4. **Touchpoints**: Where they interact (website, app, email, phone, in-person)
5. **Channels**: Medium of interaction (digital, physical, human)
6. **Pain Points**: Frustrations, blockers, friction
7. **Delighters**: Moments of delight, pleasant surprises
8. **Opportunities**: How to improve this stage

### 4. Identify Emotion Curve

**Emotion Tracking**:
- Plot emotional highs and lows across journey
- Identify "moments of truth" (critical emotional turning points)
- Find "pain points" (negative emotions, frustration)
- Find "delighters" (positive emotions, delight)

**Emotional States**:
- 😞 Frustrated / Angry
- 😰 Anxious / Worried
- 😐 Neutral / Indifferent
- 🙂 Satisfied / Content
- 😃 Happy / Delighted
- 🎉 Ecstatic / Advocating

### 5. Prioritize Opportunities

**Opportunity Prioritization**:
- **High Impact + Low Effort**: Quick wins (do first)
- **High Impact + High Effort**: Strategic bets (plan carefully)
- **Low Impact + Low Effort**: Nice-to-haves (fill-ins)
- **Low Impact + High Effort**: Avoid

## Template

```markdown
# Customer Journey Map: [Persona/Scenario Name]

**Created**: [YYYY-MM-DD]
**Persona**: [Link to persona or brief description]
**Journey**: [Start point → End point]
**Timeframe**: [How long this journey typically takes]
**Last Updated**: [Date]

---

## Executive Summary

**Journey Overview**: [One sentence describing this journey]

**Key Insight**: [Main finding from mapping this journey]

**Critical Pain Points** (Top 3):
1. [Pain point 1 - which stage]
2. [Pain point 2 - which stage]
3. [Pain point 3 - which stage]

**Top Opportunities** (Top 3):
1. [Opportunity 1 - impact & effort]
2. [Opportunity 2 - impact & effort]
3. [Opportunity 3 - impact & effort]

---

## Journey Stages Overview

```
Awareness → Consideration → Purchase → Onboarding → Usage → Retention → Advocacy
   😐           😰            😃           😞          🙂          😃          🎉
[Timeline: Day 0 → Day 1 → Day 3 → Day 7 → Day 30 → Day 90 → Day 180]
```

**Emotional Curve**:
```
  High  😃🎉  ▲                      ▲              ▲
             │  \                  /  \          /   \
  Neutral 😐 │    \     ▲       /      \      /       \
             │      \ /   \   /          \  /
  Low   😞😰 │        ▼     ▼              ▼
             └─────────────────────────────────────────→
             Aware  Consider  Buy  Onboard  Use  Retain  Advocate
```

**Key Moments**:
- 🔴 **Critical Pain Points**: [Stage 1], [Stage 4]
- 🟢 **Moments of Delight**: [Stage 3], [Stage 7]
- 🟡 **Moments of Truth**: [Stage 2], [Stage 5] (make-or-break decisions)

---

## Stage-by-Stage Journey Map

### Stage 1: Awareness

**Timeline**: [Duration - e.g., "Day 0, 10-30 minutes"]

**Scenario**: [Brief narrative - e.g., "Sarah searches Google for 'CRM for sales teams' after hearing about the product from a colleague"]

---

#### User Actions

**What [Persona] Does**:
1. [Action 1 - e.g., "Searches Google for 'best CRM for sales teams'"]
2. [Action 2 - e.g., "Clicks on blog post comparing top CRMs"]
3. [Action 3 - e.g., "Visits product homepage from blog"]
4. [Action 4 - e.g., "Watches 2-minute demo video"]

**Goal at This Stage**: [What user wants to accomplish - e.g., "Understand if this product can solve my pipeline visibility problem"]

---

#### User Thoughts & Questions

**Thinking**:
> "I need a better way to track my team's pipeline. Excel is killing me."

**Questions**:
- [Question 1 - e.g., "Is this easy enough for my team to actually use?"]
- [Question 2 - e.g., "Does it integrate with Salesforce?"]
- [Question 3 - e.g., "What's the pricing?"]
- [Question 4 - e.g., "Is this overkill for a team of 10?"]

**Mental State**: [e.g., "Curious but skeptical - has tried tools before that didn't work"]

---

#### Emotions

**Emotional State**: 😐 **Neutral / Curious**

**Emotional Drivers**:
- **Positive**: Hope that this might solve problem
- **Negative**: Skepticism from past bad experiences, time pressure

**Emotion Level**: 3/5 (neutral to slightly positive)

---

#### Touchpoints

**Where [Persona] Interacts**:
- **Google Search** (organic search)
- **Blog post** (comparison content)
- **Homepage** (website)
- **Demo video** (embedded on homepage)

**Channels**:
- Digital (web, desktop)
- Self-service (no human interaction yet)

**Devices**: Laptop (at work)

---

#### Pain Points

**Frustrations at This Stage**:

1. **[Pain Point 1]**: [e.g., "Homepage is too generic, doesn't speak to sales managers specifically"]
   - **Impact**: Doesn't feel like product is "for me"
   - **Evidence**: [From research - e.g., "8/15 interviewees said homepage was too vague"]

2. **[Pain Point 2]**: [e.g., "Demo video is 5 minutes long, too long to watch during busy workday"]
   - **Impact**: Doesn't watch full video, misses key features
   - **Evidence**: [Analytics: 70% drop off after 90 seconds]

3. **[Pain Point 3]**: [e.g., "Pricing is hidden, requires 'Contact Sales' form"]
   - **Impact**: Creates friction, user hesitates to engage
   - **Evidence**: [Heat maps show lots of clicks on "Pricing" nav, then bounce]

---

#### Delighters

**Positive Moments**:
- [Delight 1 - e.g., "Blog post is extremely helpful, answers exact question"]
- [Delight 2 - e.g., "Homepage loads fast, looks professional"]

---

#### Opportunities for Improvement

**How to Improve This Stage**:

1. **[Opportunity 1]**: [e.g., "Add persona-specific homepage variants (sales manager view)"]
   - **Impact**: High (speaks directly to user's needs)
   - **Effort**: Medium (requires design + dev work)
   - **Priority**: 🔴 High

2. **[Opportunity 2]**: [e.g., "Shorten demo video to 90 seconds, create longer 'deep dive' option"]
   - **Impact**: Medium (reduces drop-off)
   - **Effort**: Low (video editing)
   - **Priority**: 🟢 Quick Win

3. **[Opportunity 3]**: [e.g., "Show transparent pricing on website"]
   - **Impact**: High (removes major friction)
   - **Effort**: Low (add pricing page)
   - **Priority**: 🔴 High

---

### Stage 2: Consideration

**Timeline**: [e.g., "Day 0-2, several short sessions (15-30 min each)"]

**Scenario**: [Narrative - e.g., "Sarah compares our product to 2 competitors, reads reviews, checks integration capabilities"]

---

#### User Actions

1. [Action 1 - e.g., "Reads G2 reviews (checks for Salesforce integration)"]
2. [Action 2 - e.g., "Compares features on competitor websites"]
3. [Action 3 - e.g., "Asks peers in Slack sales community for feedback"]
4. [Action 4 - e.g., "Revisits our website, explores integrations page"]

---

#### User Thoughts & Questions

**Thinking**:
> "Looks promising, but will it actually integrate with our existing tools? And will my team actually use it?"

**Questions**:
- [e.g., "How does this compare to Competitor X?"]
- [e.g., "What do other sales managers think?"]
- [e.g., "How hard is it to set up?"]

---

#### Emotions

**Emotional State**: 😰 **Anxious / Analyzing**

**Why Anxious**:
- Risk of choosing wrong tool (has happened before)
- Pressure to fix pipeline visibility problem
- Concerned about team adoption

**Emotion Level**: 2/5 (slightly negative - decision stress)

---

#### Touchpoints

- **G2 / Capterra** (reviews)
- **Competitor websites** (comparison)
- **Slack community** (peer recommendations)
- **Integrations page** (website)
- **Help docs** (technical specs)

---

#### Pain Points

1. **[Pain Point 1]**: [e.g., "Hard to compare features across competitors - no clear comparison table"]
2. **[Pain Point 2]**: [e.g., "Integration docs are technical, unclear if Salesforce sync is bidirectional"]
3. **[Pain Point 3]**: [e.g., "No clear onboarding information - how much effort to get started?"]

---

#### Delighters

- [Delight 1 - e.g., "G2 reviews mention 'easy Salesforce setup' repeatedly"]
- [Delight 2 - e.g., "Peer in Slack community recommends product enthusiastically"]

---

#### Opportunities

1. **[Opportunity]**: [e.g., "Create feature comparison page (us vs competitors)"]
   - **Priority**: 🟡 Medium

2. **[Opportunity]**: [e.g., "Add 'Setup time: <15 minutes' badges to product pages"]
   - **Priority**: 🟢 Quick Win

---

### Stage 3: Purchase / Trial Signup

**Timeline**: [e.g., "Day 2-3, 5-10 minutes"]

**Scenario**: [e.g., "Sarah decides to start free trial, fills out signup form"]

---

#### User Actions

1. [e.g., "Clicks 'Start Free Trial' on homepage"]
2. [e.g., "Fills out signup form (name, email, company, team size)"]
3. [e.g., "Verifies email"]
4. [e.g., "Logs into product for first time"]

---

#### User Thoughts & Questions

> "Okay, let's see if this is as good as it looks. I hope setup is actually quick."

**Questions**:
- [e.g., "Will I get spammed by sales?"]
- [e.g., "Can I cancel easily if it doesn't work out?"]

---

#### Emotions

**Emotional State**: 😃 **Excited / Hopeful**

**Why Excited**: About to solve problem, optimistic

**Emotion Level**: 4/5 (positive - highest point so far)

---

#### Touchpoints

- **Signup form** (website)
- **Email verification** (email)
- **Welcome email** (email)
- **Product login screen** (app)

---

#### Pain Points

1. **[Pain Point]**: [e.g., "Signup form asks for credit card (trial should be free, no CC)"]
   - **Impact**: High (creates abandonment)
   - **Evidence**: [40% drop-off at CC field]

2. **[Pain Point]**: [e.g., "Email verification delay (5 min wait), user loses momentum"]

---

#### Delighters

- [Delight]: [e.g., "Welcome email is personal, includes quick setup video"]

---

#### Opportunities

1. **[Opportunity]**: [e.g., "Remove credit card requirement from trial signup"]
   - **Priority**: 🔴 High (major friction reducer)

---

### Stage 4: Onboarding / First Usage

[Continue with same structure for each stage...]

---

### Stage 5: Regular Usage

[Continue...]

---

### Stage 6: Retention / Renewal

[Continue...]

---

### Stage 7: Advocacy

[Continue...]

---

## Journey Insights

### Critical Moments of Truth

**Moment 1: [Stage Name]** - [Description]
- **Why Critical**: [Make-or-break point in journey]
- **Current State**: [What happens now]
- **Desired State**: [What should happen]
- **Gap**: [What needs to change]

**Moment 2: [Stage Name]** - [Description]
[Repeat]

---

### Emotion Curve Analysis

**Emotional Highs** (Peak positive moments):
1. **[Stage]**: [e.g., "Trial signup - excited to solve problem"]
2. **[Stage]**: [e.g., "First successful report - got value quickly"]

**Emotional Lows** (Pain points):
1. **[Stage]**: [e.g., "Onboarding - confused by complex setup"]
2. **[Stage]**: [e.g., "First invoice - sticker shock from pricing"]

**Emotional Trajectory**: [Overall trend - e.g., "Starts positive (excited), dips during onboarding (frustrated), recovers after first value (satisfied), dips at renewal (price concern), ends high (advocate)"]

---

### Cross-Stage Patterns

**Themes Across Journey**:
1. **[Theme 1]**: [e.g., "Lack of clarity - user is confused at multiple stages (consideration, onboarding, renewal)"]
2. **[Theme 2]**: [e.g., "Friction from integrations - Salesforce sync issues appear in onboarding and usage"]
3. **[Theme 3]**: [e.g., "Delight from speed - fast performance is mentioned positively at every stage"]

**Handoff Issues** (Between stages):
- **[Handoff 1]**: [e.g., "Marketing → Product: Trial users don't understand value prop from marketing site"]
- **[Handoff 2]**: [e.g., "Sales → CS: No context passed from sales to CS team, user has to repeat info"]

---

## Opportunity Map

### Prioritized Improvements

**Quick Wins** (High Impact, Low Effort - Do Now):
1. **[Opportunity]**: [e.g., "Shorten demo video from 5min → 90sec"]
   - **Stage**: Awareness
   - **Impact**: Reduce 70% drop-off
   - **Effort**: 1 day (video editing)
   - **Owner**: Marketing

2. **[Opportunity]**: [e.g., "Add transparent pricing page"]
   - **Stage**: Awareness
   - **Impact**: Remove major friction point
   - **Effort**: 2 days
   - **Owner**: Product + Marketing

---

**Strategic Bets** (High Impact, High Effort - Plan):
1. **[Opportunity]**: [e.g., "Remove credit card from trial signup"]
   - **Stage**: Purchase
   - **Impact**: Reduce 40% abandonment
   - **Effort**: 2 weeks (eng work, legal approval, ops process change)
   - **Owner**: Product + Eng

2. **[Opportunity]**: [e.g., "Rebuild onboarding flow with progressive disclosure"]
   - **Stage**: Onboarding
   - **Impact**: Reduce 60% drop-off after signup
   - **Effort**: 6 weeks
   - **Owner**: Product + Design + Eng

---

**Nice-to-Haves** (Low Impact, Low Effort - Fill-ins):
1. **[Opportunity]**: [e.g., "Add success stories to consideration stage pages"]
   - **Effort**: 1 week
   - **Impact**: Small (marginal improvement)

---

**Avoid** (Low Impact, High Effort):
1. **[Opportunity to Skip]**: [e.g., "Build in-app gamification for usage stage"]
   - **Why Avoid**: High effort, unclear impact, not a top pain point

---

## Metrics & Measurement

**Journey Health Metrics**:

| Stage | Current | Target | Metric |
|-------|---------|--------|--------|
| Awareness → Consideration | 35% | 50% | % who return to site after first visit |
| Consideration → Trial | 8% | 15% | Conversion rate from visitor to trial |
| Trial → Onboarding | 60% | 85% | % who complete onboarding |
| Onboarding → First Value | 40% | 70% | % who create first report in 7 days |
| First Value → Active User | 65% | 80% | % who use product 2+ times/week |
| Active → Renewal | 75% | 85% | Retention rate |
| Renewal → Advocacy | 20% | 35% | % who refer or leave review |

**Leading Indicators**:
- Time to first value (currently 3 days, target 1 day)
- Onboarding completion rate (currently 40%, target 70%)
- Support tickets per user (currently 1.2, target 0.5)

---

## Action Plan

**Immediate (Next Sprint)**:
- [ ] [Action 1] - [Owner] - [Due date]
- [ ] [Action 2] - [Owner] - [Due date]

**Short-term (Next Quarter)**:
- [ ] [Action 3] - [Owner] - [Due date]
- [ ] [Action 4] - [Owner] - [Due date]

**Long-term (6-12 months)**:
- [ ] [Action 5] - [Owner] - [Due date]

---

## Related Journey Maps

**Primary Journey**: [This map - e.g., "Sales Manager Trial-to-Paid Journey"]

**Related Journeys**:
- **[Persona 2] Journey**: [e.g., "Individual Sales Rep Usage Journey"]
- **[Alternative Journey]**: [e.g., "Enterprise Sales Journey (different from self-serve trial)"]

```

---

## Best Practices

### DO ✅

- **Base on real research** - Use interviews, analytics, and observation (not assumptions)
- **Focus on emotions** - Emotional curve is most valuable insight
- **Include all touchpoints** - Digital, physical, human interactions
- **Show cross-functional view** - Journey crosses marketing, sales, product, support
- **Identify moments of truth** - Critical make-or-break points
- **Prioritize opportunities** - Not all pain points are equal
- **Update regularly** - Journey maps go stale, refresh quarterly
- **Make it visual** - Use diagrams, emotion curves, icons

### DON'T ❌

- **Don't rely on assumptions** - Must be grounded in research
- **Don't skip emotions** - Actions alone miss the human experience
- **Don't make it too detailed** - Focus on key stages (5-7 max)
- **Don't create and forget** - Journey maps must drive action
- **Don't map in isolation** - Involve cross-functional team
- **Don't ignore low-frequency touchpoints** - Support calls may be rare but critical
- **Don't make it about you** - It's the customer's journey, not your process
- **Don't skip the "why"** - Explain why user behaves this way

---

## Model

Use: Sonnet

---

## Related

- `/customer-insights:persona` - Create user personas before mapping journey
- `/user-research:research-synthesize` - Synthesize research into journey insights
- `/user-research:interview-guide` - Create interview guide to research journey
- `/user-research:usability-test` - Test specific journey stages
- `/requirements-engineering:user-stories` - Convert journey opportunities into user stories
- `/customer-insights:research-to-product` - Journey mapping in full research workflow
- `user-researcher` agent - Research methodology for journey mapping
- `ui-ux-designer` agent - Visual journey map design
