# Retention Curve Analysis Template

How to analyze retention curves to diagnose product-market fit and identify improvement opportunities.

## Why Retention is the Ultimate PMF Test

**Core Principle:** Retention curves reveal if users genuinely need your product or just tried it once.

**Marc Andreessen:** "Retention is the single most important thing for growth."

**Key Insight:** A flattening retention curve = PMF. A continuously declining curve = no PMF.

---

## The Three Retention Patterns

### Pattern 1: Leaky Bucket (No PMF)

```
Retention
100%│●
 80%│ ●
 60%│  ●
 40%│   ●
 20%│    ●
  0%│     ●─────  ← Approaches zero
    └────────────────────
     D1  W1  W2  W4  M2  M3
```

**Characteristics:**

- Continuous decline
- Never flattens
- Approaches 0% retention
- Losing users every period

**Diagnosis:** Product is NOT a must-have

- Users try it once, then leave
- No habit formation
- No core value experienced
- Wrong product or wrong market

**Action:**

- ✗ DON'T scale (throwing money into leaky bucket)
- ✓ DO find product-market fit first
- ✓ DO deep customer interviews
- ✓ DO rapid iteration on core value

**Timeline:** 6-18 months to find PMF before considering scale

---

### Pattern 2: Flattening Curve (PMF Achieved!)

```
Retention
100%│●
 80%│ ●
 60%│  ●
 40%│   ●────────  ← Flattens at 30-50%
 20%│
  0%│
    └────────────────────
     D1  W1  W2  W4  M2  M3
```

**Characteristics:**

- Initial drop-off (normal)
- Curve flattens at 30-50%
- Core users retain long-term
- Stable base of engaged users

**Diagnosis:** PMF achieved with core segment

- Some users churn (not target segment)
- Core users love it (become habits)
- Clear product-market fit with specific audience
- Ready to scale

**Action:**

- ✓ DO scale acquisition
- ✓ DO optimize for target segment
- ✓ DO improve onboarding (reduce early drop-off)
- ✓ DO expand addressable market

**Timeline:** Ready to scale now

---

### Pattern 3: Smiling Curve (Strong PMF)

```
Retention
100%│●
 90%│ ●
 80%│  ●───────
 70%│   ●─────●──  ← Usage increases!
 60%│
  0%│
    └────────────────────
     D1  W1  W2  W4  M2  M3
```

**Characteristics:**

- Minimal early drop-off
- Retention stable or increasing
- Users engage more over time
- Product becomes more valuable with use

**Diagnosis:** Very strong PMF with network effects/habit

- Network effects (more users = more value)
- Habit-forming (daily use patterns)
- Switching costs (data, content, connections)
- Examples: Social networks, collaboration tools, marketplaces

**Action:**

- ✓ DO scale aggressively
- ✓ DO focus on activation (get users to network/habit)
- ✓ DO invest in virality
- ✓ DO protect core engagement

**Timeline:** Scale as fast as you can hire/fund

---

## How to Build Retention Curves

### Step 1: Define Your Cohorts

**Cohort = Group of users who signed up in same period**

**Time periods:**

- Daily cohorts (high-frequency products)
- Weekly cohorts (most common)
- Monthly cohorts (low-frequency products)

**Example:**

- Week 1 cohort: Users who signed up Jan 1-7
- Week 2 cohort: Users who signed up Jan 8-14
- Etc.

---

### Step 2: Define "Retention"

**Critical decision:** What action constitutes "retained"?

**Options:**

- **Login retention:** User logged in (weak signal)
- **Usage retention:** User performed core action (better)
- **Value retention:** User got core value (best)

**Examples:**

- **Slack:** Sent a message
- **Spotify:** Listened to music
- **Notion:** Edited a page
- **Superhuman:** Read/sent email

**Choose action that indicates core value delivered**

---

### Step 3: Calculate Retention by Period

**Formula:**

```
Retention Rate = (Users active in period / Cohort size) × 100
```

**Example (Week 1 Cohort, 1000 users):**

```
Day 1:  1000/1000 = 100%
Day 7:   800/1000 = 80%
Day 14:  600/1000 = 60%
Day 30:  450/1000 = 45%
Day 60:  400/1000 = 40%
Day 90:  400/1000 = 40%  ← Flattened!
```

---

### Step 4: Plot the Curve

**X-axis:** Time periods (days, weeks, months)
**Y-axis:** Retention % (0-100%)

**Plot multiple cohorts to compare:**

```
100%│●●●
 80%│ ●●●
 60%│  ●●●
 40%│   ●●●────  ← All cohorts flatten around 40%
 20%│
  0%│
    └────────────────────
     D1  W1  W2  W4  M2  M3

    — Week 1 cohort
    — Week 2 cohort
    — Week 3 cohort
```

---

## Analyzing Your Curves

### Question 1: Is it flattening?

**Look for:**

- Does curve level off?
- At what period does it flatten?
- What % of users retained at plateau?

**If NO (continuously declining):**

- No PMF yet
- Don't scale
- Fix product first

**If YES (flattens):**

- PMF achieved!
- Note plateau level (30%? 50%? 70%?)
- Ready to scale

---

### Question 2: Where is the plateau?

**Benchmark plateau levels:**

**B2C Products:**

- 20-30%: Decent, depends on frequency
- 30-40%: Good PMF
- 40%+: Strong PMF

**B2B SaaS:**

- 40-50%: Minimum viable
- 50-70%: Good PMF
- 70%+: Excellent PMF

**High-frequency products** (daily use):

- Should retain 60%+ at plateau
- Examples: Communication, productivity tools

**Low-frequency products** (weekly/monthly):

- 30-40% plateau acceptable
- Examples: Tax software, travel booking

---

### Question 3: When does it flatten?

**Early flattening (Week 2-4):**

- Good sign
- Users quickly realize value
- Habit forms fast

**Late flattening (Month 2-3+):**

- Concerning if >3 months
- Takes long to realize value
- May indicate onboarding issues

**Never flattens:**

- Red flag
- No PMF
- Product not sticky

---

### Question 4: Are cohorts improving over time?

**Compare recent cohorts to older cohorts:**

```
Cohort          | D30 Retention | M3 Retention | Plateau
----------------|---------------|--------------|--------
Jan (oldest)    |     35%       |     30%      |  30%
Feb             |     40%       |     35%      |  35%
Mar             |     45%       |     40%      |  40%
Apr (newest)    |     50%       |     45%      |  45%

Trend: ✓ Improving (each cohort better than last)
```

**Improving cohorts = Good signs:**

- Product improvements working
- Better onboarding
- Better targeting
- PMF strengthening

**Declining cohorts = Warning signs:**

- Product degrading
- Wrong users signing up
- Market saturation
- PMF weakening

---

## Diagnosing Problems

### Problem: Steep drop-off in first week

```
100%│●
 50%│ ●────  ← 50% gone by Day 7
 40%│
  0%│
    └────────
     D1  D7
```

**Possible causes:**

- Poor onboarding
- Didn't reach "aha moment"
- Wrong expectations set
- Complex setup process

**Investigation questions:**

- What % complete onboarding?
- What % reach core action?
- Where in funnel do they drop?
- What do drop-offs have in common?

**Fixes:**

- Improve onboarding flow
- Reduce time-to-value
- Set correct expectations
- Simplify activation

---

### Problem: Never flattens, constant decline

```
100%│●
 80%│ ●
 60%│  ●
 40%│   ●
 20%│    ●
  0%│     ●→  ← Keeps declining
    └────────────
```

**Possible causes:**

- Not solving real problem
- Competition better
- Poor product quality
- Wrong target market

**Investigation questions:**

- Why do users leave?
- What alternative do they switch to?
- What were they expecting vs reality?
- Who stays vs who leaves?

**Fixes:**

- Deep customer interviews
- Consider pivot
- Fix core value prop
- Find right market segment

---

### Problem: Plateau too low (<20%)

```
100%│●
 80%│ ●
 60%│  ●
 20%│   ●────  ← Only 20% retained
  0%│
    └────────────
```

**Possible causes:**

- Narrow use case
- Solved one-time need
- Better alternatives exist
- Not habit-forming

**Investigation questions:**

- Who are the 20% that stay?
- What makes them different?
- Can we find more like them?
- Is TAM big enough at 20%?

**Fixes:**

- Double down on the 20% segment
- Build for them exclusively
- Accept niche if profitable
- Or pivot to broader use case

---

### Problem: Cohorts declining over time

```
         Jan  Feb  Mar  Apr
Month 3:  40%  35%  30%  25%  ← Getting worse

Trend: ✗ Declining
```

**Possible causes:**

- Product degrading (bugs, bloat)
- Acquiring wrong users
- Market saturation (early adopters only)
- Competition improving

**Investigation questions:**

- What changed between cohorts?
- User composition changing?
- Product changes impact?
- Competitive landscape shifts?

**Fixes:**

- Analyze cohort demographics
- Improve targeting
- Fix product quality
- Protect core value

---

## Retention Benchmarks by Industry

### B2B SaaS

**Day 1 → Day 30:**

- Great: >60%
- Good: 50-60%
- Concerning: <50%

**Month 1 → Month 3:**

- Great: >80%
- Good: 70-80%
- Concerning: <70%

**Month 3 plateau:**

- Great: >70%
- Good: 50-70%
- Concerning: <50%

**Monthly churn at steady state:**

- Great: <2% (logo), <5% (revenue)
- Acceptable: 2-5% (logo)
- Concerning: >5%

---

### B2C Social/Content

**Day 1 → Day 30:**

- Great: >40%
- Good: 30-40%
- Concerning: <30%

**DAU/MAU (stickiness):**

- Great: >60%
- Good: 40-60%
- Concerning: <40%

**Month 1 → Month 6:**

- Great: >50%
- Good: 30-50%
- Concerning: <30%

---

### E-commerce/Marketplaces

**First purchase → Second purchase:**

- Great: >40%
- Good: 30-40%
- Concerning: <30%

**Annual repurchase rate:**

- Great: >60%
- Good: 40-60%
- Concerning: <40%

---

## Improving Retention

### Phase 1: Activation (Day 1-7)

**Goal:** Get users to "aha moment" quickly

**Tactics:**

- Streamline onboarding
- Reduce time-to-value
- Guided first experience
- Quick wins early

**Measure:**

- D1 → D7 retention
- % reaching core action
- Time to first value

---

### Phase 2: Habit Formation (Week 2-4)

**Goal:** Make product part of routine

**Tactics:**

- Trigger regular usage
- Build streaks/engagement
- Email/push notifications
- Social features

**Measure:**

- W1 → W4 retention
- Usage frequency
- Engagement depth

---

### Phase 3: Long-term Value (Month 2+)

**Goal:** Make product indispensable

**Tactics:**

- Deepen feature usage
- Lock-in mechanisms (data, content, network)
- Expand use cases
- Build community

**Measure:**

- M1 → M3 → M6 retention
- Feature adoption
- Switching costs

---

## Retention Curve Worksheet

**Your Product:**

**Core action defining retention:**

---

**Current curves:**

```
Cohort: _____  (Signup dates: _____ to _____)

Day 1:    ____%
Day 7:    ____%
Day 30:   ____%
Month 2:  ____%
Month 3:  ____%
Month 6:  ____%

Pattern:
[ ] Leaky bucket (no PMF)
[ ] Flattening (PMF!)
[ ] Smiling (strong PMF)

Plateau level: ____%
Flattens at: Week ___ / Month ___
```

**Cohort comparison:**

```
Cohort       | D30  | M3   | Plateau | Trend
-------------|------|------|---------|-------
_____ (old)  | ___% | ___% | ___%    |
_____        | ___% | ___% | ___%    | [ ] ↗ [ ] → [ ] ↘
_____        | ___% | ___% | ___%    | [ ] ↗ [ ] → [ ] ↘
_____ (new)  | ___% | ___% | ___%    |
```

**Diagnosis:**

- [ ] PMF achieved (curve flattens at acceptable level)
- [ ] Close to PMF (flattening but low plateau)
- [ ] No PMF yet (not flattening)

**Action plan:**

1. ***
2. ***
3. ***

---

## Advanced Analysis

### Retention by Segment

Compare retention across user segments:

```
Segment          | D30  | M3   | Plateau
-----------------|------|------|--------
Power users      | 80%  | 75%  | 75%
Regular users    | 50%  | 45%  | 45%
Casual users     | 30%  | 20%  | 20%
```

**Insight:** Power users retain at 3x rate of casual users

**Action:** Activate more users into power user behaviors

---

### Retention by Cohort Behavior

First-week behaviors that predict retention:

```
Behavior             | Users | M3 Retention
---------------------|-------|-------------
Completed onboarding |  800  |    65%
Invited teammate     |  400  |    75%
Used core feature 3+ |  600  |    70%
None of above        |  200  |    15%
```

**Insight:** Inviting teammate = highest retention

**Action:** Emphasize team invitations in onboarding

---

### Resurrection Analysis

Users who churned but came back:

```
Churned at: Week 4
Resurrected at: Week 8
Resurrection rate: 15%
```

**Questions:**

- What brought them back?
- What's different second time?
- How to prevent initial churn?

**Tactics:**

- Win-back campaigns
- New feature announcements
- Address churn reasons
