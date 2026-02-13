# PMF Measurement Dashboard Template

Comprehensive dashboard for tracking product-market fit through leading and lagging indicators.

## Dashboard Overview

Track PMF through multiple lenses: survey scores, retention, engagement, growth, and unit economics.

**Update frequency:** Monthly review, Quarterly deep-dive

**Owner:** Product Lead / Head of Product

---

## Primary Metrics (The Big 3)

### 1. Sean Ellis PMF Score

**Current Score:**

```
█████████████████████████████████░░░░░░░  58%

Last Quarter:  48%
This Quarter:  58%
Change:        +10% ✓

Status: ✓ PMF Achieved (40%+ threshold)
```

**Segment Breakdown:**

```
Very disappointed:     58%  [===========================>]
Somewhat disappointed: 27%  [============>               ]
Not disappointed:      15%  [======>                     ]
```

**Trend (Last 6 Quarters):**

```
60%│                           ●
50%│                     ●  ●
40%│- - - - - - ●  ●- - - - - - - - (PMF threshold)
30%│        ●
20%│     ●
10%│
   └─────────────────────────────────
   Q1  Q2  Q3  Q4  Q1  Q2
```

**Action Item:**

- [ ] If <40%: Focus on improving score before scaling
- [ ] If 40%+: Maintain and protect, ready to scale
- [ ] If declining: Red alert, investigate immediately

---

### 2. Retention (The Ultimate PMF Test)

**Cohort Retention Curves:**

```
Month 1 Cohort (Jan 2024)
100%│●
 80%│ ●
 60%│  ●
 40%│   ●─────────────  ← Flattened at 40%
 20%│
   └───────────────────────
    D1  W1  M1  M2  M3  M4

Status: ✓ Curve flattening (PMF signal)
```

**Key Metrics:**

- Day 1 → Day 30: \_\_\_\_% retained
- Month 1 → Month 3: \_\_\_\_% retained
- Month 3 → Month 6: \_\_\_\_% retained (should be flat)

**Target Benchmarks:**

- **B2C:** <5% monthly churn once flattened
- **B2B:** <2% logo churn, <5% revenue churn

**Retention by Segment:**

```
Champions (Very disappointed):     85% retained at M6
Warm Users (Somewhat):            60% retained at M6
Others (Not disappointed):        25% retained at M6

Analysis: Champions retain at 3x rate of others
```

---

### 3. NPS (Net Promoter Score)

**Current NPS:**

```
NPS: +52  (World-class)

Promoters (9-10):  65%  [===============================>]
Passives (7-8):    25%  [============>                   ]
Detractors (0-6):  10%  [====>                           ]

Calculation: 65% - 10% = 55 NPS
```

**NPS Trend:**

```
60│                        ●
50│                  ●  ●
40│            ●
30│      ●
20│  ●
  └───────────────────────
  Q1  Q2  Q3  Q4  Q1  Q2
```

**Target:**

- NPS >50 = World-class, strong PMF
- NPS 30-50 = Good, PMF likely
- NPS <30 = Concerning, may not have PMF

**Why NPS matters:**
Correlates strongly with PMF - users who would recommend are experiencing value.

---

## Leading Indicators (Feel It Now)

Early signals of PMF before metrics confirm it.

### Organic Growth

**Word-of-Mouth Metrics:**

- Referral rate: \_\_\_\_% of users refer someone
- Viral coefficient: \_\_\_\_ (new users per existing user)
- Organic signups: \_\_\_\_% of total signups
- Branded search volume: \_\_\_\_% increase MoM

**Social Signals:**

- Unprompted mentions: \_\_\_\_ per month
- User-generated content: \_\_\_\_ pieces
- Community size: \_\_\_\_ members
- Community engagement rate: \_\_\_\_%

**Target:** Organic should be growing faster than paid channels

**Status:**

- [ ] Strong: Organic > 50% of growth
- [ ] Moderate: Organic 25-50%
- [ ] Weak: Organic <25% (may not have PMF)

---

### Engagement Depth

**Usage Metrics:**

- DAU/MAU ratio: \_\_\_\_% (stickiness)
- Average session length: \_\_\_\_ minutes
- Sessions per week: \_\_\_\_
- Feature adoption: \_\_\_\_% use core features
- Power user %: \_\_\_\_% use daily+

**Engagement Trends:**

```
DAU/MAU: 45%  [=======================>      ] Target: 40%+
```

**Benchmarks:**

- **B2C Social:** 60%+ DAU/MAU = strong PMF
- **B2B SaaS:** 30-40% = good, depends on frequency
- **Consumer:** 20-30% = decent, evaluate by product type

**Status:**

- [ ] Increasing engagement = PMF strengthening
- [ ] Flat engagement = PMF stable
- [ ] Declining engagement = PMF at risk

---

### Customer Passion

**Qualitative Signals:**

Count of passionate responses:

- "Don't take this away from me": \_\_\_\_ mentions
- Volunteering to help/beta test: \_\_\_\_ users
- Unsolicited recommendations: \_\_\_\_ per month
- Active in community: \_\_\_\_ engaged users

**Customer interview quotes:**

> "Quote showing must-have status" - [User name]
> "Quote showing passionate usage" - [User name]

**User-Generated Value:**

- Help articles created by users: \_\_\_\_
- Community answers to questions: \_\_\_\_
- Feature ideas submitted: \_\_\_\_
- Templates/content shared: \_\_\_\_

**Status:**

- [ ] Strong passion signals across multiple users
- [ ] Moderate passion from some users
- [ ] Little passion visible (concerning)

---

### Sales Velocity

**Deal Metrics:**

- Average sales cycle: \_\_\_\_ days
- Win rate: \_\_\_\_%
- Average discount given: \_\_\_\_%
- Price objections: \_\_\_\_% of deals

**Velocity Trend:**

```
Avg Sales Cycle:
90 days│ ●
60 days│    ●
30 days│       ●──────  ← Shortening = PMF signal
       └────────────────
       Q1  Q2  Q3  Q4
```

**Green Lights:**

- Deals closing faster over time
- Higher win rates
- Less discounting needed
- Fewer price objections

**Status:**

- [ ] Accelerating (PMF strengthening)
- [ ] Stable (PMF established)
- [ ] Slowing (PMF weakening)

---

## Lagging Indicators (Metrics Confirm It)

Hard metrics that validate PMF retrospectively.

### Unit Economics

**LTV:CAC Ratio:**

```
Current: 5.2:1

LTV: $_____ (lifetime value)
CAC: $_____ (customer acquisition cost)

Ratio: ___:1

Status:
- >5:1 = Excellent, scale aggressively
- 3-5:1 = Good, scale sustainably
- <3:1 = Needs improvement before scaling
```

**Payback Period:**

```
Current: 8 months

Target: <12 months (ideally <6)

Status: ✓ Within target
```

**Gross Margin:**

```
Current: 78%

Target: >70% for SaaS

Status: ✓ Healthy margin
```

---

### Growth Rate

**Month-over-Month Growth:**

```
Current: +15% MoM

Last 6 months:
+18% → +16% → +15% → +15% → +12% → +15%

Status: Steady growth, slight deceleration
```

**Growth Chart:**

```
Users
1000│                    ●
 800│                 ●
 600│              ●
 400│           ●
 200│        ●
 100│     ●
    └───────────────────
    J  F  M  A  M  J
```

**Type of Growth:**

- [ ] Exponential (compounding, strong PMF)
- [ ] Linear (steady but not compounding)
- [ ] Flat (no growth, no PMF)
- [ ] Declining (losing PMF)

---

### Market Pull

**Inbound vs Outbound:**

```
Inbound:  65%  [==============================>]
Outbound: 35%  [================>              ]

Target: Inbound >50% signals market pull
```

**Brand Strength:**

- PR mentions: \_\_\_\_ per quarter
- Industry recognition: \_\_\_\_ awards/lists
- Competitor mentions: \_\_\_\_ times in battlecards
- Analyst recognition: \_\_\_\_ reports/quadrants

**Competitive Response:**

- Competitors copying features: \_\_\_\_ instances
- Competitive pricing pressure: [ ] Yes [ ] No
- Market awareness: \_\_\_\_% of TAM aware

**Status:**

- [ ] Strong market pull (PMF confirmed)
- [ ] Moderate pull (PMF present)
- [ ] Push-only (no PMF yet)

---

## PMF Health Score

Combine metrics into overall PMF health score.

**Scoring Rubric:**

```
Metric                  | Weight | Score | Weighted
------------------------|--------|-------|----------
Sean Ellis (40%+)       |  25%   |  ___  |  ___
Retention (flat curve)  |  25%   |  ___  |  ___
NPS (>50)              |  15%   |  ___  |  ___
Organic Growth         |  10%   |  ___  |  ___
Engagement (DAU/MAU)   |  10%   |  ___  |  ___
LTV:CAC (>3:1)         |  10%   |  ___  |  ___
Growth Rate (>10% MoM) |   5%   |  ___  |  ___
------------------------|--------|-------|----------
TOTAL PMF SCORE        | 100%   |       |  ___/100
```

**Interpretation:**

- **80-100:** Strong PMF, scale aggressively
- **60-79:** Good PMF, scale cautiously
- **40-59:** Approaching PMF, keep iterating
- **<40:** No PMF yet, don't scale

---

## Alert System

Set up automatic alerts for PMF warning signs.

### Red Alerts (Act Immediately)

- [ ] PMF score declining >5% quarter over quarter
- [ ] Retention curves no longer flattening
- [ ] NPS dropping below 30
- [ ] Churn accelerating
- [ ] Growth rate negative

**Action:** Emergency team meeting, deep customer interviews, pause scaling plans

### Yellow Alerts (Monitor Closely)

- [ ] PMF score flat for 2+ quarters
- [ ] Engagement declining
- [ ] Sales cycles lengthening
- [ ] Win rate dropping
- [ ] CAC increasing faster than LTV

**Action:** Investigate, talk to customers, review roadmap priorities

### Green Signals (Keep Going)

- [ ] PMF score increasing
- [ ] All leading indicators positive
- [ ] Unit economics improving
- [ ] Growth accelerating
- [ ] Customer passion high

**Action:** Maintain course, consider accelerating growth investments

---

## Dashboard Usage

### Monthly Review (30 min)

**With:** Product + Growth + Data teams

**Agenda:**

1. Review primary metrics (PMF score, retention, NPS)
2. Check leading indicators (any warning signs?)
3. Update projections
4. Flag issues for investigation

**Output:** One-page summary, action items

---

### Quarterly Deep-Dive (2 hours)

**With:** Leadership team + Board

**Agenda:**

1. Full dashboard review
2. Segment analysis (who has PMF, who doesn't)
3. Cohort analysis (improving or degrading?)
4. Competitive landscape
5. Strategy adjustments

**Output:**

- PMF health report
- Roadmap priorities for next quarter
- Growth investment decisions

---

## Segment-Specific Dashboards

Break down metrics by user segment for deeper insights.

### By User Persona

```
Persona A (Target ICP):
- PMF Score: 65%
- Retention: 80% at M6
- NPS: +60
Status: ✓ Strong PMF

Persona B (Adjacent):
- PMF Score: 35%
- Retention: 45% at M6
- NPS: +20
Status: ⚠ Weak PMF, consider dropping or improving

Persona C (Non-target):
- PMF Score: 15%
- Retention: 20% at M6
- NPS: -10
Status: ✗ No PMF, stop acquiring
```

### By Acquisition Channel

```
Channel          | PMF Score | Retention | LTV:CAC
-----------------|-----------|-----------|--------
Organic          |    62%    |    75%    |  8:1
Referral         |    58%    |    72%    |  12:1
Content          |    45%    |    55%    |  4:1
Paid Search      |    32%    |    40%    |  2:1
Paid Social      |    25%    |    30%    |  1.5:1

Insight: Organic + Referral have strong PMF, Paid doesn't
Action: Double down on Organic/Referral, pause Paid
```

### By Company Size (B2B)

```
SMB (1-50):      PMF 48%,  NPS +40
Mid-Market:      PMF 55%,  NPS +55
Enterprise:      PMF 35%,  NPS +25

Insight: Strong PMF with SMB + Mid-Market, weak with Enterprise
```

---

## Visualization Tips

**Use traffic light colors:**

- 🟢 Green: Metric exceeding target
- 🟡 Yellow: Metric near target, monitor
- 🔴 Red: Metric below target, action needed

**Show trends, not just snapshots:**

- Always include historical data
- Show direction (↗ ↘ →)
- Highlight inflection points

**Make it scannable:**

- Big numbers at top
- Charts for trends
- Tables for details
- One-page summary possible

**Update regularly:**

- Real-time for critical metrics
- Daily for engagement
- Weekly for growth
- Monthly for summary
- Quarterly for deep-dive
