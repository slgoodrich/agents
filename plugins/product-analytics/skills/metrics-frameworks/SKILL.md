---
name: metrics-frameworks
description: Apply AARRR (Pirate Metrics), HEART, North Star Metric, and OKR frameworks. Use when defining KPIs, measuring product success, or setting goals.
---

# Metrics Frameworks

## Overview

Comprehensive guide to product metrics frameworks for measuring success, tracking growth, and aligning teams around key outcomes.

## When to Use This Skill

- Defining product KPIs
- Setting up analytics
- Measuring feature success
- Growth optimization
- Board/executive reporting

## Core Frameworks

### 1. AARRR (Pirate Metrics) - Dave McClure

**Stages**:
```
Acquisition → Activation → Retention → Revenue → Referral
```

#### Acquisition
**Definition**: How users find you

**Metrics**:
- Signups / Visitors (conversion rate)
- CAC (Customer Acquisition Cost)
- Channel mix (organic, paid, referral)
- Cost per signup by channel

**Example**:
- 10,000 visitors → 500 signups = 5% conversion
- $2,500 ad spend / 500 signups = $5 CAC

#### Activation
**Definition**: First great experience ("aha moment")

**Metrics**:
- % users completing setup
- Time to value
- % reaching activation milestone

**Example**:
- Activation = "Created first project with 3+ tasks"
- 500 signups → 250 activated = 50% activation rate

#### Retention
**Definition**: Users coming back

**Metrics**:
- D1, D7, D30 retention
- Churn rate
- Cohort retention curves

**Example**:
- D1: 60%, D7: 35%, D30: 25%
- Monthly churn: 5%

#### Revenue
**Definition**: Monetization

**Metrics**:
- MRR (Monthly Recurring Revenue)
- ARPU (Average Revenue Per User)
- LTV (Lifetime Value)
- Conversion rate (free → paid)

**Example**:
- 100 paying users × $20/month = $2,000 MRR
- ARPU: $2,000 / 2,000 total users = $1

#### Referral
**Definition**: Viral growth

**Metrics**:
- k-factor (viral coefficient)
- NPS (Net Promoter Score)
- % users who invite others

**Example**:
- 15% of users invite (avg 2 people each)
- 30% of invites convert
- k-factor = 0.15 × 2 × 0.30 = 0.09

**When to Use AARRR**:
- Consumer products
- Growth-focused
- Funnel optimization

---

### 2. HEART Framework (Google)

**Dimensions**:
```
Happiness → Engagement → Adoption → Retention → Task Success
```

#### Happiness
**Definition**: User satisfaction and perception

**Metrics**:
- NPS (Net Promoter Score)
- CSAT (Customer Satisfaction)
- App store ratings
- Sentiment analysis

**Example**: NPS score of 45

#### Engagement
**Definition**: Frequency and depth of interaction

**Metrics**:
- DAU, WAU, MAU
- Session duration
- Pages/features per session
- DAU/MAU ratio (stickiness)

**Example**:
- DAU: 5,000, MAU: 20,000
- Stickiness: 5,000/20,000 = 25%

#### Adoption
**Definition**: New users of features

**Metrics**:
- % users trying new feature (first 30 days)
- Time to first use
- Feature penetration

**Example**:
- New feature: 40% of users tried in first month

#### Retention
**Definition**: Rate of return

**Metrics**:
- % users active after N days
- Cohort retention curves
- Churn rate

**Example**: 70% of users active after 7 days

#### Task Success
**Definition**: Efficiency, effectiveness, error rate

**Metrics**:
- Task completion rate
- Time on task
- Error rate
- Search success rate

**Example**: 85% task completion rate

**When to Use HEART**:
- Feature-level measurement
- UX improvement
- Holistic product health

---

### 3. North Star Metric

**Definition**: Single metric that best captures core value delivered to customers

**Characteristics**:
- Reflects customer value
- Leads to revenue
- Actionable by team
- Measurable
- Leading indicator

**Examples by Product Type**:
```
Slack: Messages sent
Airbnb: Nights booked
Spotify: Time listening
Medium: Total time reading
WhatsApp: Messages sent
Netflix: Hours watched
```

**How to Choose**:
1. What value does product deliver?
2. What user action indicates value received?
3. What correlates with retention and revenue?

**Supporting Metrics** (Inputs):
```
North Star: Weekly Active Users

Inputs:
├─ Acquisition: Signups
├─ Activation: Setup completion
├─ Engagement: Feature usage
└─ Retention: 7-day retention
```

**When to Use**:
- Company-wide alignment
- Focus entire organization
- Single success measure

---

### 4. OKRs (Objectives & Key Results)

(See okr-framework skill for full details)

**Structure**:
```
Objective: Qualitative, inspirational goal

Key Results:
1. [Metric] from [X] to [Y] by [Date]
2. [Milestone] achieved by [Date]
3. [Metric] reaches [Target]
```

**Example**:
```
Objective: Make product indispensable for daily workflows

Key Results:
1. DAU/MAU from 25% to 40% by June 30
2. Average session duration reaches 8+ minutes
3. 60% of users return within 24 hours
```

**When to Use**:
- Quarterly/annual planning
- Cross-functional alignment
- Ambitious goal-setting

---

### 5. Input vs Output vs Outcome Metrics

**Output Metrics** (What we ship):
- Features launched
- Story points completed
- Deploys per week

**Outcome Metrics** (Impact on users/business):
- User engagement increase
- Revenue growth
- Churn reduction

**Input Metrics** (Leading indicators):
- Activation rate
- Feature adoption
- Support tickets

**Hierarchy**:
```
Outcome (Goal)
   ↑
Output (What we ship)
   ↑
Input (Early signals)
```

**Example**:
- Input: Onboarding completion rate
- Output: New dashboard feature
- Outcome: User retention improves 10%

**Focus on Outcomes**, track outputs and inputs

---

## Product-Specific Metrics

### SaaS Metrics

**MRR (Monthly Recurring Revenue)**:
```
Total monthly revenue from subscriptions
```

**ARR (Annual Recurring Revenue)**:
```
MRR × 12
```

**Churn Rate**:
```
Churned customers / Total customers at start
```

**Revenue Churn**:
```
Lost MRR / Total MRR at start
```

**LTV (Lifetime Value)**:
```
ARPU / Churn Rate

Example:
ARPU: $50/month
Churn: 5%/month
LTV = $50 / 0.05 = $1,000
```

**CAC Payback**:
```
CAC / (ARPU × Gross Margin)

Example:
CAC: $200
ARPU: $50/month
Margin: 80%
Payback = $200 / ($50 × 0.80) = 5 months
```

**Rule**: LTV / CAC > 3

---

### E-commerce Metrics

**Conversion Rate**:
```
Purchases / Visitors
```

**AOV (Average Order Value)**:
```
Total Revenue / Number of Orders
```

**Cart Abandonment Rate**:
```
Abandoned carts / Carts created
```

**Customer Repeat Rate**:
```
Repeat customers / Total customers
```

---

### Marketplace Metrics

**GMV (Gross Merchandise Value)**:
```
Total transaction volume
```

**Take Rate**:
```
Platform revenue / GMV
```

**Liquidity**:
```
% of listings resulting in transaction
```

**Network Effects**:
- Suppliers added per demand-side user
- Cross-side network density

---

### Mobile App Metrics

**App Store Metrics**:
- Downloads
- Install rate (impressions → installs)
- App store rating

**Engagement**:
- Screen views per session
- Session interval (time between sessions)
- Push notification opt-in rate

---

## Metric Design

### Good Metrics are SMART

**S**pecific: Clearly defined
**M**easurable: Can track
**A**chievable: Stretch but possible
**R**elevant: Ties to goals
**T**ime-bound: Has deadline

**Example**:
- Bad: "Increase engagement"
- Good: "Increase DAU/MAU from 25% to 35% by June 30"

---

### Leading vs Lagging

**Leading** (Predictive):
- Activation rate
- Feature adoption
- Onboarding completion

**Lagging** (Historical):
- Revenue
- Retention
- NPS

Use leading to inform, lagging to validate

---

### Vanity vs Actionable

**Vanity Metrics**:
- Total users (without context)
- Page views
- App downloads

**Actionable Metrics**:
- DAU/MAU ratio
- Conversion rate by cohort
- Revenue per user

Focus on actionable, cohorted, comparative

---

## Metric Pitfalls

###  Avoid

**Goodhart's Law**: "When a measure becomes a target, it ceases to be a good measure"

**Gaming**:
- Optimizing metric at expense of user value
- Example: Engagement up, but from spam notifications

**Too Many Metrics**:
- Focus dilution
- Stick to 3-5 key metrics

**Ignoring Counter Metrics**:
- Track potential negative impacts
- Example: Speed up (good) but error rate up (bad)

###  Do

**Balance Metrics**:
- Pair growth with quality
- Example: New users + retention

**Segment**:
- By cohort, channel, persona
- Averages hide insights

**Set Guardrails**:
- Define acceptable ranges
- Monitor for unintended consequences

---

## Dashboard Design

### Hierarchy

**Level 1: Executive Dashboard**
- North Star Metric
- 3-5 key business metrics
- Weekly/monthly view

**Level 2: Product Dashboard**
- AARRR funnel
- Feature adoption
- Cohort retention

**Level 3: Feature Dashboard**
- Feature-specific metrics
- A/B test results
- User feedback

---

### Frequency

**Real-time**: Critical alerts
**Daily**: Ops metrics, bugs
**Weekly**: Product team sync
**Monthly**: Exec reviews
**Quarterly**: Board meetings

---

## Tools

**Analytics**:
- Mixpanel, Amplitude (product analytics)
- Google Analytics (web)
- Segment (data pipeline)

**Dashboards**:
- Tableau, Looker, Mode
- Metabase (open-source)

**Experimentation**:
- Optimizely, LaunchDarkly
- Google Optimize

---

## Templates

### Metric Definition

```markdown
## Metric: [Name]

**Definition**: [How calculated]
**Why it matters**: [Business impact]
**Target**: [Goal]
**Current**: [Baseline]
**Tracking**: [Tool, frequency]
**Owner**: [Person responsible]

**Related Metrics**:
- Leading: [Input metric]
- Counter: [Watch for negative impact]
```

---

## Resources

**Books**:
- "Lean Analytics" - Alistair Croll & Benjamin Yoskovitz
- "Measure What Matters" - John Doerr (OKRs)
- "The Lean Startup" - Eric Ries

**Frameworks**:
- AARRR: 500startups.com
- HEART: research.google/pubs/pub36299
- North Star: amplitude.com/north-star

---

## Quick Reference

```
Need a framework?

Growth-focused → AARRR
UX-focused → HEART
Company alignment → North Star
Goal-setting → OKRs

Track:
- One North Star
- 3-5 supporting metrics
- Counter metrics
- Input + Outcome

Avoid vanity, enable action
```
