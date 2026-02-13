# Launch Metrics Guide

Comprehensive guide to measuring product launch success with leading and lagging indicators.

## Table of Contents

- [Metrics Framework](#metrics-framework)
- [Metrics by Launch Tier](#metrics-by-launch-tier)
- [Success Criteria Example](#success-criteria-example)
- [Measurement Setup](#measurement-setup)
- [Metrics Dashboard](#metrics-dashboard)
- [Common Metrics Mistakes](#common-metrics-mistakes)
- [When to Pivot](#when-to-pivot)
- [Reporting Cadence](#reporting-cadence)

---

## Metrics Framework

### Leading Indicators (Week 1)

**Definition**: Early signals that predict future success

**Measure**: Days 1-7 after launch

**Purpose**: Quick feedback, course correction

---

#### Awareness Metrics

**What they measure**: Did people hear about the launch?

**Key Metrics**:

- Website visits to launch page
- Blog post views
- Social media impressions
- Social media engagement (likes, shares, comments)
- Email open rates
- Email click-through rates
- Press coverage mentions

**Targets** (example for Tier 1):

- 10K+ landing page visits
- 5K+ blog post views
- 100K+ social impressions
- 40%+ email open rate
- 10%+ email click-through rate

---

#### Early Adoption Metrics

**What they measure**: Are people trying it?

**Key Metrics**:

- Signups/trials started
- Feature activation rate (% who use it at least once)
- Time to first use (how quickly after signup)
- D1 retention (% who return day 1)
- Early user feedback (NPS, surveys)

**Targets** (example):

- 500+ signups in Week 1
- 60%+ activation rate
- <24 hours time to first use
- 40%+ D1 retention
- NPS >40 from early users

---

#### Technical Health Metrics

**What they measure**: Is it working properly?

**Key Metrics**:

- Uptime percentage
- Error rate
- Page load time (p50, p95)
- API response time
- Support ticket volume
- Critical bug count

**Targets**:

- 99.9%+ uptime
- <1% error rate
- Page load <2s (p95)
- API response <500ms (p95)
- Support tickets <10/day (Tier 1)
- Zero critical bugs

---

### Lagging Indicators (Months 1-3)

**Definition**: Longer-term measures of success

**Measure**: 30, 60, 90 days post-launch

**Purpose**: Validate product-market fit, business impact

---

#### Adoption Metrics

**What they measure**: Sustained usage over time

**Key Metrics**:

- % of target customers using feature
- DAU (Daily Active Users) for feature
- MAU (Monthly Active Users) for feature
- WAU / MAU ratio (engagement frequency)
- D7, D30 retention rates
- Feature usage frequency (times per week)
- Cohort retention curves

**Targets** (example for Tier 1):

- 40% of target segment using monthly
- 10K DAU
- 50K MAU
- 50% WAU/MAU (weekly actives)
- 60% D7 retention
- 40% D30 retention
- 3x per week average usage

---

#### Business Impact Metrics

**What they measure**: Does it drive business results?

**Key Metrics**:

- Revenue from feature (if monetized directly)
- Conversion lift (free → paid, trial → customer)
- Expansion revenue (upsells enabled by feature)
- Customer acquisition cost (CAC) impact
- Churn reduction (if retention-focused)
- Customer Lifetime Value (LTV) impact

**Targets** (example):

- $500K ARR from feature
- 15% increase in free→paid conversion
- $200K expansion revenue
- 10% reduction in churn
- 20% increase in LTV

---

#### Product Quality Metrics

**What they measure**: Quality and user satisfaction

**Key Metrics**:

- Bug rate (bugs per 1K users)
- Support ticket volume
- Time to resolution (support)
- Feature requests (what's missing)
- NPS (Net Promoter Score)
- CSAT (Customer Satisfaction)
- App store ratings (if mobile)

**Targets**:

- <5 bugs per 1K users
- <20 support tickets per week
- <24hr time to resolution
- NPS >50
- CSAT >4.5/5
- 4.5+ star rating (mobile)

---

## Metrics by Launch Tier

### Tier 1 (Major Launch)

**Focus**: All metrics, high targets

**Key Metrics**:

- Awareness: 100K+ impressions
- Adoption: 40%+ of segment in 3 months
- Business: $500K+ revenue impact
- NPS: 50+

**Measurement**: Daily Week 1, Weekly Month 1, Monthly after

---

### Tier 2 (Standard Launch)

**Focus**: Adoption and business impact

**Key Metrics**:

- Adoption: 20%+ of segment in 3 months
- Business: $100K+ revenue impact
- NPS: 40+

**Measurement**: Weekly Month 1, Monthly after

---

### Tier 3 (Minor Launch)

**Focus**: Technical health and basic adoption

**Key Metrics**:

- Adoption: 10%+ of users try it
- Technical: No critical bugs
- Support: <5 tickets

**Measurement**: Monthly check-ins

---

## Success Criteria Example

### Feature: Advanced Analytics Dashboard

**Launch Tier**: Tier 1

**Success Metrics (3 months)**:

**Leading Indicators (Week 1)**:

- ✅ 15K landing page visits (target: 10K)
- ✅ 500 signups (target: 500)
- ✅ 70% activation rate (target: 60%)
- ✅ NPS 55 from early users (target: 40)

**Lagging Indicators (3 months)**:

- **Adoption**: 40% of paying customers use weekly
  - Baseline: 0%
  - Target: 40%
  - Actual: 45% ✅

- **Engagement**: 15 min average session time
  - Baseline: N/A (new feature)
  - Target: 15 min
  - Actual: 18 min ✅

- **Business**: $500K ARR from dashboard upsells
  - Baseline: $0
  - Target: $500K
  - Actual: $620K ✅

- **Satisfaction**: NPS 50+ from users
  - Baseline: N/A
  - Target: 50
  - Actual: 58 ✅

**Result**: Success - exceeded all targets

---

## Measurement Setup

### Pre-Launch

- [ ] Analytics instrumentation complete
- [ ] Baseline data captured (for comparison)
- [ ] Dashboard created (real-time monitoring)
- [ ] Targets defined for each metric
- [ ] Data sources integrated (GA, Mixpanel, Salesforce, etc.)

### Week 1 Post-Launch

- [ ] Daily metrics review (30 min meeting)
- [ ] Early issue triage
- [ ] Quick wins identified
- [ ] Data quality verified

### Month 1 Post-Launch

- [ ] Weekly metrics review
- [ ] Cohort analysis (how is Week 1 cohort performing?)
- [ ] Trend analysis (are metrics improving?)
- [ ] Iterate based on data

### Month 3 Post-Launch

- [ ] Success criteria review
- [ ] Declare success/failure vs targets
- [ ] Document learnings
- [ ] Plan v2 based on data

---

## Metrics Dashboard

### Real-Time Dashboard (Launch Day)

**Purpose**: Monitor for issues

**Metrics**:

- Uptime (% green)
- Error rate (per hour)
- Active users (real-time count)
- Support tickets (count + severity)

**Alerts**:

- Uptime <99.5% → Page on-call
- Error rate >2% → Page on-call
- Support tickets >10/hour → Alert PM

---

### Week 1 Dashboard

**Purpose**: Track early traction

**Metrics**:

- Signups per day
- Activation rate (%)
- D1 retention (%)
- NPS (rolling average)
- Top issues (bugs, feedback)

**Cadence**: Check 3x/day

---

### Monthly Dashboard

**Purpose**: Track sustained adoption

**Metrics**:

- MAU (total and by cohort)
- Retention curves (D7, D30)
- Revenue impact ($)
- NPS trend
- Feature requests (top 10)

**Cadence**: Weekly review, monthly deep-dive

---

## Common Metrics Mistakes

❌ **Mistake 1: Vanity Metrics**

- Bad: "10K page views!"
- Good: "10K page views, 500 signups (5% conversion), 300 activated (60% activation)"

❌ **Mistake 2: No Baseline**

- Bad: "We have 1K DAU!"
- Good: "DAU increased from 800 to 1K (+25%) since launch"

❌ **Mistake 3: Measuring Too Late**

- Bad: Check metrics 3 months post-launch
- Good: Daily Week 1, Weekly Month 1, Monthly after

❌ **Mistake 4: No Targets**

- Bad: "Let's see what happens"
- Good: "Target: 40% adoption in 3 months"

❌ **Mistake 5: Ignoring Negative Signals**

- Bad: Focus only on positive metrics
- Good: Actively monitor churn, bugs, negative NPS

---

## When to Pivot

**Red flags** (consider pivoting or iterating):

- Activation rate <30% (people try but don't use)
- D7 retention <20% (people don't come back)
- NPS <20 (users actively dislike it)
- Support tickets >50/day sustained (too many issues)
- <10% adoption after 3 months (nobody cares)

**What to do**:

1. Gather qualitative feedback (why aren't people using it?)
2. Identify the blocker (confusing, buggy, not valuable?)
3. Pivot quickly (fix UX, fix bugs, or kill feature)

---

## Reporting Cadence

**Week 1**: Daily email to team (5 bullets)
**Month 1**: Weekly presentation to leadership (15 min)
**Month 3**: Written post-mortem + metrics review
**Ongoing**: Monthly metrics review (as long as feature exists)

---

**Key Principle**: Metrics without action are just numbers. Use metrics to drive decisions - what to fix, what to double down on, what to kill.
