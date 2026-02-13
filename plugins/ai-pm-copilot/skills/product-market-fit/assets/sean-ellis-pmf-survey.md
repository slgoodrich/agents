# Sean Ellis PMF Survey Template

The definitive survey for measuring product-market fit using the 40% rule.

## The Core Question

**Primary Question:**

> "How would you feel if you could no longer use [Your Product Name]?"

**Response Options:**

- a) Very disappointed
- b) Somewhat disappointed
- c) Not disappointed (it isn't really that useful)

## PMF Scoring

**PMF Score** = % of respondents who answer "Very disappointed"

**Interpretation:**

- **40%+ "Very disappointed"** = PMF achieved (permission to scale)
- **25-40%** = Close, keep iterating on product
- **<25%** = No PMF yet, need significant changes

**Why 40%?**
Sean Ellis analyzed 100+ startups and found 40% is the threshold where companies transition from struggling to scaling successfully.

## Complete Survey Template

### Section 1: The PMF Question (Required)

**Q1: How would you feel if you could no longer use [Product]?**

- [ ] Very disappointed
- [ ] Somewhat disappointed
- [ ] Not disappointed (it isn't really that useful)

### Section 2: Segmentation (Required)

**Q2: Which of the following best describes your role?**

- [ ] [Role option 1]
- [ ] [Role option 2]
- [ ] [Role option 3]
- [ ] Other: **\_\_\_**

**Q3: How often do you use [Product]?**

- [ ] Multiple times per day
- [ ] Daily
- [ ] 2-3 times per week
- [ ] Weekly
- [ ] Less than weekly

**Q4: How long have you been using [Product]?**

- [ ] Less than 1 week
- [ ] 1-2 weeks
- [ ] 2-4 weeks
- [ ] 1-3 months
- [ ] 3+ months

### Section 3: Qualitative Insights (Required)

**Q5: What is the main benefit you receive from [Product]?**
[Open text field]

**Q6: What type of people do you think would most benefit from [Product]?**
[Open text field]

**Q7: How can we improve [Product] for you?**
[Open text field]

### Section 4: Optional Demographics

**Q8: What is your company size?**

- [ ] Just me
- [ ] 2-10 employees
- [ ] 11-50 employees
- [ ] 51-200 employees
- [ ] 200+ employees

**Q9: What industry are you in?**
[Open text field or dropdown]

## Survey Administration

### When to Survey

**Timing:**

- Survey after users have experienced core value
- Typically 2-4 weeks after activation (varies by product)
- For B2B: After first meaningful use in production
- For B2C: After achieving "aha moment"

**Frequency:**

- Quarterly for tracking progress
- After major releases to measure impact
- Continuously (always-on survey) for real-time tracking

### Sample Size

**Minimum viable:**

- 30-40 responses for initial directional signal
- 100+ responses for statistical confidence
- 200+ responses for segment analysis

**Target audience:**

- Active users (used in last 30 days)
- Users who experienced core value
- Not too early (need time to form opinion)
- Not too late (recency bias)

### Distribution Methods

**Email:**

```
Subject: Quick question about [Product]

Hi [Name],

I have a quick question that will take less than 2 minutes to answer.

Your feedback helps us improve [Product] and build features that matter most to users like you.

[Survey Link]

Thanks!
[Your name]
```

**In-app:**

- Trigger after key action
- Non-intrusive placement
- Easy to dismiss
- Incentive: "Help shape the product"

**Tips:**

- Keep survey short (under 5 minutes)
- Make all questions optional except PMF question
- No incentives (can skew results)
- Anonymous or identified (your choice)

## Analysis Framework

### Step 1: Calculate PMF Score

```
PMF Score = (# "Very disappointed" / Total responses) × 100
```

**Example:**

- 50 "Very disappointed"
- 30 "Somewhat disappointed"
- 20 "Not disappointed"
- Total: 100 responses
- **PMF Score: 50%** ✓ PMF achieved

### Step 2: Segment Analysis

Break down PMF score by:

- Role/persona
- Usage frequency
- Company size
- Time using product

**Look for:**

- Which segments have 40%+ PMF?
- Which segments are close (30-40%)?
- Which segments are far (<25%)?

**Example:**

```
Segment A (Product Managers): 65% very disappointed ✓
Segment B (Engineers): 35% very disappointed (close)
Segment C (Executives): 15% very disappointed (no PMF)

Strategy: Double down on PMs, improve for Engineers, ignore Execs
```

### Step 3: Analyze "Very Disappointed" Users

**Q5: Main benefit analysis**

- What do champions value most?
- What's the common thread?
- What makes it a "must-have"?

**Q6: Target persona analysis**

- Who do they think should use this?
- Does it match your ICP?
- Are you targeting right segment?

**Q7: Improvement requests**

- What features do they want?
- What would make it even better?
- What's missing from their workflow?

**Action:** Prioritize features requested by "very disappointed" users

### Step 4: Analyze "Somewhat Disappointed" Users

**Key question:** Are they target segment?

**If YES (match ICP):**

- What's missing for them?
- Why aren't they "very disappointed"?
- What would convert them?
- **Action:** Address gaps to convert

**If NO (don't match ICP):**

- Different use case?
- Different persona?
- Wrong segment entirely?
- **Action:** Don't build for them

### Step 5: Analyze "Not Disappointed" Users

**Typical reasons:**

- Wrong segment (not target user)
- Didn't reach core value
- Trying to use wrong way
- Expecting something different

**Action:**

- Don't build for them
- Focus on champions instead
- May need better onboarding (if targeting is right)

## Tracking Progress Over Time

### Quarterly Tracking

Run survey every quarter to measure progress:

```
Q1 2024: 22% very disappointed (Pre-PMF)
Q2 2024: 28% (Improving)
Q3 2024: 35% (Getting close)
Q4 2024: 42% (PMF achieved!)
Q1 2025: 48% (Strengthening)
```

**What to track:**

- Overall PMF score trend
- PMF score by segment
- Sample size (is it growing?)
- Qualitative themes changing

### Dashboard Metrics

**Create simple dashboard:**

- Current PMF score (big number)
- Trend over time (line chart)
- Score by segment (bar chart)
- Top requested features (word cloud from Q7)

**Share with:**

- Entire company
- Board
- Investors
- Key team members

## Common Mistakes

**Surveying too early:**

- Users haven't experienced value yet
- Score will be artificially low
- Wait until they've used core features

**Surveying wrong users:**

- Inactive users (churned, trial not converted)
- Users who never activated
- Wrong segment entirely
- **Fix:** Survey active, engaged users

**Leading questions:**

- Don't bias the question
- Keep it neutral
- Use exact wording from Sean Ellis
- Don't add explanations or context

**Ignoring qualitative answers:**

- The "why" is as important as the score
- Q5-Q7 tell you what to build
- Read every response
- Look for patterns

**Not segmenting:**

- Overall score can mask segment differences
- You might have PMF with one segment, not others
- Always analyze by segment

**Survey fatigue:**

- Don't over-survey same users
- Quarterly is enough for most
- Rotate sample if needed

## Advanced Techniques

### Predictive PMF (Before Survey)

Proxy metrics that correlate with PMF:

- Retention (flattening curves)
- Engagement (DAU/MAU, session length)
- Organic growth (word-of-mouth, virality)
- Willingness to pay (conversion, renewals)

### Real-time PMF Tracking

Instead of quarterly batches:

- Always-on survey (small % of users)
- Continuous scoring
- Real-time dashboard
- Alert if score drops

### PMF by Cohort

Track PMF score for each signup cohort:

- Jan 2024 cohort: 45%
- Feb 2024 cohort: 48%
- Mar 2024 cohort: 52%

**Insight:** Are newer cohorts experiencing better PMF? (Good onboarding, better targeting)

## Taking Action Based on Results

### Score <25%: No PMF Yet

**Actions:**

1. Deep customer interviews (10+ per week)
2. Rapid iteration on core value prop
3. Consider pivot
4. Don't scale yet
5. Small cohorts, fast learning

**Timeline:** 6-18 months to reach PMF

### Score 25-40%: Close to PMF

**Actions:**

1. Double down on what champions love (Q5)
2. Address top improvement requests (Q7)
3. Strengthen core value
4. Refine ICP based on "very disappointed" segment
5. Continue iterating

**Timeline:** 3-6 months to reach 40%

### Score 40%+: PMF Achieved

**Actions:**

1. Prove one scalable acquisition channel
2. Optimize unit economics
3. Start scaling gradually
4. Hire for growth
5. Maintain PMF (continuous surveys)

**Timeline:** Ready to scale

### Score Declining

**Red flag:** Score dropping over time

**Possible causes:**

- Feature bloat
- Serving wrong customers
- Market evolution
- Competitor pressure

**Actions:**

1. Emergency customer interviews
2. Analyze by cohort (old vs new users)
3. Return to core value
4. May need refresh/pivot

## Resources

**Original Sean Ellis Post:**
"The Startup Pyramid" (2010)

**Superhuman's PMF Journey:**
Rahul Vohra's "How Superhuman Built an Engine to Find Product-Market Fit" (First Round Review, 2018)

**Academic Research:**
Steve Blank & Bob Dorf: "The Startup Owner's Manual" - Customer Development

**Tools:**

- Typeform, SurveyMonkey: Survey platforms
- Airtable, Notion: Response tracking
- Amplitude, Mixpanel: Usage data correlation
