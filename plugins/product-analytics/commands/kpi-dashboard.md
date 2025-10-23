# KPI Dashboard Builder

Define and structure product KPIs and metrics dashboards with data sources and tracking plans.

## Usage

```
/product-analytics:kpi-dashboard [product or feature name] [optional: dashboard type]
```

## What This Command Does

1. Creates comprehensive KPI framework with North Star metric hierarchy
2. Defines primary, secondary, and counter metrics with explicit data sources
3. Structures metrics using AARRR, HEART, or custom frameworks
4. Provides tracking implementation plan with tools and methods
5. Generates dashboard templates for different audiences
6. Takes 30-60 minutes vs 2-4 hours of manual dashboard design

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Product Context**:
- Product name and type (B2B SaaS, B2C app, marketplace, etc.)
- Stage (early, growth, mature)
- Target users and use cases
- Business model (subscription, freemium, transaction, etc.)
- Current performance baseline (users, revenue, engagement)

**Data Availability**:
- **CRITICAL**: Ask user for current values of key metrics (don't assume)
- Analytics tools available (Google Analytics, Mixpanel, Amplitude, etc.)
- Database access for custom queries
- CRM/billing system (Stripe, Salesforce, etc.)
- Support/feedback tools (Zendesk, Intercom, etc.)

**Goals & Targets**:
- Business objectives for this period
- OKRs or goals this dashboard supports
- Timeline (monthly, quarterly, annual targets)
- Stakeholder audience (team, leadership, board)

### 2. Identify Dashboard Type

**Product Dashboard** - Overall product health
- Audience: Product team, leadership
- Metrics: Engagement, retention, activation
- Update: Daily/weekly

**Growth Dashboard** - Acquisition and activation
- Audience: Growth team, marketing
- Metrics: Signups, activation rate, CAC
- Update: Daily/weekly

**Business Dashboard** - Revenue and business metrics
- Audience: Leadership, sales, finance
- Metrics: MRR, churn, LTV, unit economics
- Update: Weekly/monthly

**Engineering Dashboard** - Technical and reliability
- Audience: Engineering team
- Metrics: Uptime, performance, incidents
- Update: Real-time/daily

**Executive Dashboard** - High-level business health
- Audience: C-suite, board
- Metrics: Revenue, growth rate, key business drivers
- Update: Weekly/monthly

### 3. Define Metric Hierarchy

**North Star Metric** (1 metric):
- Single most important indicator of value delivery
- Reflects core product value
- Correlates with long-term success

**Primary Metrics** (3-5 metrics):
- Key drivers of North Star
- Actionable by product/eng team
- Leading indicators

**Secondary Metrics** (5-10 metrics):
- Supporting metrics that add context
- Diagnostic metrics for deep dives
- Lagging indicators

**Counter Metrics** (2-4 metrics):
- Guardrails against optimization
- Quality/sustainability checks
- Prevent gaming

### 4. Follow Ground Rules

**Explicit Data Sourcing**:
- **CRITICAL**: Specify exact data source for each metric
- Document calculation method
- Note data quality/reliability
- Identify gaps in current tracking

**Upfront Data Gathering**:
- Ask user for current baseline values (don't make up numbers)
- Ask about analytics infrastructure
- Ask about metric calculation definitions
- Get clarity on targets and timeframes

**No Tracking Assumptions**:
- Don't assume what's being tracked
- Ask what analytics tools exist
- Ask about data pipeline maturity
- Verify metric definitions match user's definitions

## Templates

### Product Dashboard Template

```markdown
# KPI Dashboard: [Product Name]

**Dashboard Type**: Product Health
**Audience**: Product Team, Leadership
**Update Frequency**: Weekly
**Last Updated**: [Date]

---

## North Star Metric

**Metric**: Weekly Active Users (WAU)

**Definition**: Unique users who performed a core action (e.g., created a project, sent a message) in the last 7 days

**Why This Matters**:
- Represents actual product value delivery (not just signups)
- Leading indicator of retention and revenue
- Actionable by product/eng team

**Current**: 12,500 WAU

**Target**: 20,000 WAU by Q2 2025 (+60%)

**Data Source**:
- Tool: Mixpanel
- Event: `core_action_completed`
- Filter: Unique users, last 7 days
- Query: `SELECT COUNT(DISTINCT user_id) FROM events WHERE event_name = 'core_action_completed' AND timestamp > NOW() - INTERVAL '7 days'`

**Tracking Status**: ✅ Instrumented and validated

---

## Primary Metrics

### 1. Weekly Activation Rate

**Definition**: % of new signups who reach activated state within 7 days

**Formula**: (Activated users / Total signups) × 100

**Current**: 35%

**Target**: 50% by Q2 2025

**Why It Matters**:
- Strong predictor of retention
- Directly impacts North Star (more activated = more active)
- Influenced by onboarding improvements

**Data Source**:
- Signups: Google Analytics `sign_up` event
- Activation: Mixpanel `activation_milestone_reached` event
- Calculation: Daily batch job, 7-day cohort analysis

**Tracking Status**: ✅ Instrumented and validated

**Benchmarks**: Industry average 40-45% for B2B SaaS

---

### 2. 7-Day Retention

**Definition**: % of new users who return on Day 7

**Formula**: (Users active on Day 7 / Users signed up on Day 0) × 100

**Current**: 28%

**Target**: 35% by Q2 2025

**Why It Matters**:
- Early retention signal
- Product-market fit indicator
- Predicts long-term retention

**Data Source**:
- Tool: Amplitude
- Event: Any `session_start` event on Day 7
- Cohort: Daily cohorts tracked
- Dashboard: [Link to Amplitude cohort analysis]

**Tracking Status**: ✅ Instrumented and validated

**Benchmarks**: Industry average 25-30% for consumer apps

---

### 3. Feature Adoption Rate

**Definition**: % of active users using new feature X

**Formula**: (Users who used feature X / WAU) × 100

**Current**: 12% (launched 30 days ago)

**Target**: 25% by end of quarter

**Why It Matters**:
- Validates product investment
- Identifies product-led growth opportunities
- Informs roadmap priorities

**Data Source**:
- Tool: Mixpanel
- Event: `feature_x_used`
- Filter: Active users (WAU cohort)
- Dashboard: [Link to feature adoption dashboard]

**Tracking Status**: ✅ Instrumented and validated

---

### 4. Net Revenue Retention (NRR)

**Definition**: % of revenue retained from existing customers including expansions

**Formula**: ((Starting MRR + Expansion - Churn) / Starting MRR) × 100

**Current**: 115%

**Target**: 120% by Q2 2025

**Why It Matters**:
- Measures product value growth over time
- Indicator of customer satisfaction and expansion potential
- Key SaaS metric for growth

**Data Source**:
- Tool: ChartMogul / Stripe
- Data: Subscription events (upgrades, downgrades, cancellations)
- Calculation: Monthly cohort analysis
- Dashboard: [Link to ChartMogul NRR dashboard]

**Tracking Status**: ✅ Instrumented and validated

**Benchmarks**: Best-in-class B2B SaaS >110%

---

### 5. Time to Value (TTV)

**Definition**: Median time from signup to first core value moment

**Current**: 8 days (median)

**Target**: 3 days by Q2 2025

**Why It Matters**:
- Faster TTV = higher activation and retention
- Identifies onboarding friction
- Correlates with product-led growth

**Data Source**:
- Signup: Google Analytics `sign_up` event with timestamp
- Value moment: Mixpanel `first_value_event` with timestamp
- Calculation: `MEDIAN(first_value_timestamp - signup_timestamp)` per cohort
- Dashboard: Custom SQL query, visualized in Metabase

**Tracking Status**: ⚠️ Partially instrumented (need to add timestamps to value event)

**Action Needed**: Add timestamp tracking to `first_value_event` - [Owner] - [Due Date]

---

## AARRR Framework Metrics

### Acquisition

**Signups**:
- Current: 1,200/week
- Target: 2,000/week (+67%)
- Data Source: Google Analytics `sign_up` event
- Trend: ↗️ +15% WoW

**Cost Per Acquisition (CAC)**:
- Current: $125
- Target: <$100
- Data Source: Marketing spend (Google Sheets) / Signups (GA)
- Trend: ↘️ -5% (improving)

**Organic vs Paid**:
- Organic: 45% of signups
- Paid: 55% of signups
- Target: 60% organic by Q2
- Data Source: GA UTM parameters

---

### Activation

**Activation Rate (7-day)**:
- Current: 35%
- Target: 50%
- Data Source: Mixpanel cohort analysis
- Trend: → Flat (need improvement)

**Time to Activation**:
- Current: 4 days (median)
- Target: 2 days
- Data Source: Mixpanel funnel + timestamp diff
- Trend: → Flat

---

### Retention

**D1 Retention**:
- Current: 55%
- Target: 60%
- Data Source: Amplitude retention analysis

**D7 Retention**:
- Current: 28%
- Target: 35%
- Data Source: Amplitude retention analysis

**D30 Retention**:
- Current: 18%
- Target: 25%
- Data Source: Amplitude retention analysis

**Monthly Churn Rate**:
- Current: 7%
- Target: <5%
- Data Source: ChartMogul churn metrics

---

### Revenue

**Monthly Recurring Revenue (MRR)**:
- Current: $180K
- Target: $300K by Q2 (+67%)
- Data Source: Stripe MRR report
- Trend: ↗️ +12% MoM

**Average Revenue Per User (ARPU)**:
- Current: $45/month
- Target: $50/month
- Data Source: Stripe revenue / Active subscriptions
- Trend: → Flat

**Conversion Rate (Trial → Paid)**:
- Current: 18%
- Target: 25%
- Data Source: Stripe subscriptions / Mixpanel trial starts
- Trend: ↗️ +2% MoM

---

### Referral

**k-factor (Viral Coefficient)**:
- Current: 0.3 (each user invites 0.3 others)
- Target: 0.5
- Data Source: Mixpanel `invite_sent` and `invite_accepted` events
- Trend: → Flat

**Net Promoter Score (NPS)**:
- Current: 42
- Target: 50 (Excellent)
- Data Source: Delighted NPS survey (quarterly)
- Trend: ↗️ +3 pts from last quarter

---

## Counter Metrics (Guardrails)

### Performance Degradation

**Metric**: p95 Page Load Time

**Threshold**: Should not exceed 2 seconds

**Current**: 1.2 seconds

**Data Source**: Google Analytics Site Speed, New Relic

**Alert**: If p95 > 2s for > 24 hours

**Why**: Fast growth shouldn't come at cost of poor UX

---

### Support Burden

**Metric**: Support Tickets per 100 Active Users

**Threshold**: Should not exceed 5 tickets/100 users

**Current**: 3.2 tickets/100 users

**Data Source**: Zendesk tickets / Mixpanel WAU

**Alert**: If ratio > 5 for 2 consecutive weeks

**Why**: Feature velocity shouldn't create support overwhelm

---

### Engineering Stability

**Metric**: Incident Count (Severity 1-2)

**Threshold**: Should not exceed 2 incidents/month

**Current**: 1 incident/month

**Data Source**: PagerDuty incident log

**Alert**: If >2 incidents in rolling 30 days

**Why**: Growth shouldn't sacrifice reliability

---

### User Experience Quality

**Metric**: 1-Star App Store Reviews %

**Threshold**: Should not exceed 5%

**Current**: 2%

**Data Source**: App Store API

**Alert**: If >5% in rolling 30 days

**Why**: Quality bar must be maintained

---

## Weekly Dashboard View

| Metric | This Week | Last Week | WoW Change | Status | Notes |
|--------|-----------|-----------|------------|--------|-------|
| **North Star: WAU** | 12,500 | 11,800 | ↗️ +5.9% | 🟢 | On track to target |
| Weekly Activation | 35% | 34% | ↗️ +1% | 🟡 | Below target (50%) |
| 7-Day Retention | 28% | 27% | ↗️ +1% | 🟡 | Slow improvement |
| Feature Adoption | 12% | 10% | ↗️ +2% | 🟢 | Trending well |
| NRR | 115% | 115% | → 0% | 🟢 | Stable, need push to 120% |
| Time to Value | 8 days | 9 days | ↗️ -1 day | 🟡 | Still far from 3-day target |
| **Counter: Support** | 3.2/100 | 3.0/100 | ↘️ +0.2 | 🟢 | Within threshold |
| **Counter: Incidents** | 1 | 0 | ↘️ +1 | 🟢 | Within threshold |

**Overall Health**: 🟢 Growing steadily, activation needs focus

---

## Metric Tracking Implementation

### Currently Tracked ✅

| Metric | Tool | Event/Query | Validated | Dashboard Link |
|--------|------|-------------|-----------|----------------|
| WAU | Mixpanel | `core_action_completed` | ✅ | [Link] |
| Activation | Mixpanel | `activation_milestone_reached` | ✅ | [Link] |
| Retention | Amplitude | Cohort analysis | ✅ | [Link] |
| NRR | ChartMogul | Subscription data | ✅ | [Link] |

### Needs Implementation ⚠️

| Metric | Action Required | Owner | Due Date | Effort |
|--------|-----------------|-------|----------|--------|
| Time to Value | Add timestamp to value event | Engineering | Week 3 | 2 hours |
| Feature Adoption | Create cohort dashboard | Analytics | Week 2 | 4 hours |

### Data Quality Issues 🔴

| Metric | Issue | Impact | Resolution Plan |
|--------|-------|--------|-----------------|
| Signups | GA undercounts by ~5% | Targets may be off | Implement server-side tracking - Week 4 |

---

## Dashboard Maintenance

**Review Frequency**: Weekly on Mondays

**Owner**: Product Manager

**Distribution**:
- Email: Leadership team (weekly summary)
- Slack: #product-metrics (automated bot)
- Dashboard: [Link to live dashboard]

**Update Process**:
1. Pull data from all sources (automated)
2. Review anomalies and trends
3. Add commentary to key changes
4. Share with team

**Quarterly Review**:
- Reassess metric relevance
- Update targets based on progress
- Add/remove metrics as needed

```

---

### Growth Dashboard Template

```markdown
# Growth Dashboard: [Product Name]

**Focus**: User Acquisition & Activation
**Audience**: Growth Team, Marketing
**Update Frequency**: Daily
**Last Updated**: [Date]

---

## North Star: Weekly Active Users (WAU)

[Same structure as product dashboard]

---

## Primary Growth Metrics

### 1. Signup Conversion Rate

**Definition**: % of website visitors who sign up

**Current**: 3.2%

**Target**: 5.0% by Q2

**Funnel**:
- Homepage visits: 40,000/week → Signup page: 8,000 (20%) → Signups: 1,280 (3.2% overall)

**Data Source**: Google Analytics funnel, GA4 events

**Optimization Focus**: Improve signup page (currently 16% conversion)

---

### 2. Paid CAC by Channel

**Definition**: Customer acquisition cost per channel

**Channels**:
- Google Ads: $150 CAC, 400 signups/week
- Facebook: $110 CAC, 300 signups/week
- LinkedIn: $200 CAC, 100 signups/week
- Organic: $0 CAC, 400 signups/week

**Target**: Reduce paid CAC to $100 average

**Data Source**: Marketing spend tracker + GA attribution

---

### 3. Activation Funnel

**Definition**: % completion at each onboarding step

**Steps**:
1. Sign up → 100%
2. Complete profile → 75% (-25% drop)
3. Connect integration → 45% (-30% drop) ⚠️ **High friction**
4. First core action → 35% (-10% drop)
5. Activated → 35%

**Target**: 50% activation (need to reduce integration drop to 15%)

**Data Source**: Mixpanel funnel analysis

**Optimization**: A/B test optional integration step

---

[Additional growth-specific metrics...]
```

---

### Business/Executive Dashboard Template

```markdown
# Business Dashboard: [Product Name]

**Focus**: Revenue, Growth, Unit Economics
**Audience**: Leadership, Finance
**Update Frequency**: Weekly (Monday morning)
**Last Updated**: [Date]

---

## Executive Summary

**MRR**: $180K (+12% MoM)
**ARR**: $2.16M (annualized)
**Growth Rate**: 12% MoM, 189% YoY
**Runway**: 18 months at current burn

**Status**: 🟢 Healthy growth, on track to $3M ARR by EOY

---

## Revenue Metrics

### Monthly Recurring Revenue (MRR)

**Current**: $180,000

**Target**: $300,000 by Q2 2025

**Breakdown**:
- New MRR: +$25K
- Expansion MRR: +$8K
- Churned MRR: -$11K
- Net New MRR: +$22K (+12% MoM)

**Data Source**: ChartMogul, Stripe

---

### Net Revenue Retention (NRR)

**Current**: 115%

**Target**: 120%

**Calculation**: (($180K starting + $8K expansion - $11K churn) / $180K) = 98% retention + 17% expansion = 115% NRR

**Benchmark**: Top quartile B2B SaaS >110%

**Data Source**: ChartMogul cohort analysis

---

### Customer Metrics

**Active Customers**: 4,000

**ARPU**: $45/month

**Customer LTV**: $1,350 (30-month avg lifetime)

**LTV:CAC Ratio**: 10.8:1 (LTV $1,350 / CAC $125)

**Target LTV:CAC**: Maintain >3:1 (we're healthy at 10.8:1)

**Data Source**: Stripe + ChartMogul

---

### Churn & Retention

**Monthly Churn Rate**: 7.0%

**Target**: <5%

**Churn Cohorts**:
- 0-3 months: 15% (early churn - activation issue)
- 4-12 months: 8%
- 12+ months: 3% (low churn once established)

**Focus**: Reduce early churn through better activation

**Data Source**: ChartMogul churn analysis

---

## Growth Metrics

**New Customers**: 1,200/week signups → 216/week paid (18% conversion)

**Conversion Funnel**:
- Trial starts: 1,200/week
- Activated: 420 (35%)
- Converted to paid: 216 (18% overall, 51% of activated)

**Growth Levers**:
1. Increase activation 35% → 50% = +180 conversions/week
2. Improve trial→paid conversion 51% → 60% = +38 conversions/week

**Projected Impact**: +218 customers/week → +$10K MRR/week → +43K MRR/month

---

## Unit Economics

| Metric | Current | Target | Status |
|--------|---------|--------|--------|
| CAC | $125 | <$100 | 🟡 Needs improvement |
| CAC Payback | 2.8 months | <3 months | 🟢 Good |
| LTV | $1,350 | $1,500 | 🟢 Healthy |
| LTV:CAC | 10.8:1 | >3:1 | 🟢 Excellent |
| Gross Margin | 82% | >80% | 🟢 Strong |

**Status**: Unit economics are strong, focus on scaling customer acquisition

---

[Additional executive metrics: Team size, burn rate, runway, hiring plan, etc.]
```

---

## Best Practices

### DO ✅

- **One North Star** - Single most important metric everyone rallies around
- **Explicit sources** - Always document where data comes from
- **Current baselines** - Get actual numbers, don't make assumptions
- **Realistic targets** - Based on historical growth + strategic goals
- **Counter metrics** - Prevent gaming and maintain quality
- **Regular reviews** - Weekly for action metrics, monthly for trends
- **Ownership** - Clear owner for each metric
- **Actionability** - Choose metrics the team can influence

### DON'T ❌

- **Vanity metrics** - Avoid metrics that look good but don't drive value (e.g., total signups without activation)
- **Too many metrics** - Overwhelming, dilutes focus (stick to 3-5 primary)
- **Undefined metrics** - Vague definitions cause confusion and misalignment
- **Missing baselines** - Can't measure progress without starting point
- **Static dashboards** - Must evolve as product and business mature
- **Data without context** - Provide benchmarks, trends, and "why it matters"
- **Assume tracking works** - Validate instrumentation and data quality

---

## Metric Definition Framework

### For Each Metric, Specify:

1. **Name**: Clear, unambiguous name
2. **Definition**: Exact calculation method
3. **Why It Matters**: Business/user impact
4. **Current Value**: Baseline (with date)
5. **Target**: Goal and timeline
6. **Data Source**: Tool, event, query
7. **Tracking Status**: Instrumented? Validated?
8. **Owner**: Who monitors and acts
9. **Update Frequency**: How often reviewed
10. **Benchmarks**: Industry standards (if available)

---

## Example

**Input**: "KPI dashboard for B2B project management SaaS"

**Output**:

[Full dashboard following product dashboard template with:
- North Star: Teams completing projects (value metric)
- Primary: Activation rate, retention, collaboration features usage, team size growth, NRR
- AARRR breakdown with specific B2B SaaS metrics
- Counter metrics: Support load, performance, data loss incidents
- Explicit data sources: Mixpanel, Segment, Stripe, Intercom
- Actual values gathered from user (not made up)
- Tracking implementation plan with gaps identified]

---

## Model

Use: Sonnet

## Related

- `/strategic-planning:okr` - OKRs aligned to KPIs
- `/product-analytics:experiment` - Test metric improvements
- `/strategic-planning:roadmap` - Prioritize based on metric impact
- `/product-analytics:monthly-business-review` - Monthly metrics review workflow
- `data-scientist` agent - For metric analysis and forecasting
- `product-strategist` agent - For metric selection and strategy alignment
