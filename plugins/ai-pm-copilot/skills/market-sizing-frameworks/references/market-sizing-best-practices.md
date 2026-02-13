# Market Sizing Best Practices

Comprehensive guide to avoiding common mistakes, validating assumptions, and applying market sizing frameworks effectively.

---

## Table of Contents

1. [Common Mistakes and How to Avoid Them](#common-mistakes-and-how-to-avoid-them)
2. [Validation Frameworks](#validation-frameworks)
3. [Industry-Specific Considerations](#industry-specific-considerations)
4. [Competitive Landscape Analysis](#competitive-landscape-analysis)
5. [Assumption Management](#assumption-management)
6. [Sensitivity Analysis and Scenario Planning](#sensitivity-analysis-and-scenario-planning)
7. [Case Studies: Good vs Bad Market Sizing](#case-studies-good-vs-bad-market-sizing)
8. [Advanced Considerations](#advanced-considerations)

---

## Common Mistakes and How to Avoid Them

### Mistake 1: Confusing TAM with SAM

**The Problem:**
Teams often present TAM as their addressable market when pitching, leading to unrealistic expectations.

**Example - Wrong:**

```
"We're targeting the $50B project management software market"
(This is TAM for ALL project management software globally)
```

**Example - Right:**

```
"Our TAM is $50B (all PM software), but our SAM is $10M
(PM tools specifically for solo developers in English-speaking markets)"
```

**Why This Matters:**

- Investors spot inflated numbers immediately
- Planning with TAM leads to wrong resource allocation
- You'll miss actual market constraints

**How to Avoid:**

1. Always calculate TAM, SAM, and SOM separately
2. Be explicit about which number you're discussing
3. Show the filters you applied to get from TAM → SAM → SOM
4. Use SAM for strategic planning, not TAM

---

### Mistake 2: Top-Down Only Sizing

**The Problem:**
Top-down sizing typically produces inflated numbers because it starts with large markets and applies percentages.

**Example - Flawed Logic:**

```
Global SaaS market: $200B
PM tools are 5% of SaaS: $10B
We'll capture 1%: $100M TAM

Problem: You haven't validated that 1% is achievable
```

**Why This Fails:**

- Percentages feel scientific but are often guesses
- No connection to actual customer count
- Can't validate assumptions easily
- Investors see through this immediately

**How to Avoid:**

1. **Always start with bottom-up** (count customers, estimate pricing)
2. Use top-down only for validation
3. If numbers differ by >2x, investigate why
4. Trust bottom-up over top-down when in doubt

**Proper Approach:**

```
Bottom-Up (Primary):
- Product managers globally: 500,000
- % who are solo/small team: 30% = 150,000
- % who would pay for specialized tool: 20% = 30,000
- Average spend: $120/year
- TAM = 30,000 × $120 = $3.6M

Top-Down (Validation):
- PM tools market: $5B
- Solo/small team segment: 15% = $750M
- New entrant realistic share: 0.5% = $3.75M

Analysis: Numbers are similar ($3.6M vs $3.75M) → Good confidence
```

---

### Mistake 3: Ignoring Competitive Reality

**The Problem:**
Calculating market size without considering existing competitors leads to overestimation of SOM.

**Example - Naive Sizing:**

```
SAM: $100M
Year 1 target: 1% = $1M

Problem: Market already has 10 established competitors
Your realistic share is much smaller
```

**Competitive Reality Check:**

```
SAM: $100M
Known competitors: 10
Estimated competitor revenue: ~$50M total (half the market)

Available market: $50M
As new entrant: Realistically 0.5-2% in Year 1
Year 1 SOM: $250K-$1M (not just 1% of SAM)
```

**How to Account for Competition:**

**Step 1: Map competitive landscape**

```
Direct competitors: [List with estimated revenue]
Competitor A: $10M/year
Competitor B: $8M/year
Competitor C: $5M/year
Total: $23M

Indirect competitors: [List]
Alternative D (different category): $15M
Alternative E (DIY solutions): ~$10M estimated value
```

**Step 2: Calculate available market**

```
SAM: $100M
Occupied by competitors: $23M (direct) + $25M (indirect) = $48M
Truly available: $52M

BUT: Most customers are "sticky" with current solutions
Realistic churn/switching: 10-20% per year
Actually available Year 1: $5-10M

Your realistic capture: 5-10% of available
Year 1 SOM: $250K-$1M
```

**Step 3: Identify your wedge**

- What will make customers switch to you?
- Can you serve an underserved segment?
- Do you have differentiated value prop?
- What's your unfair advantage?

---

### Mistake 4: Assuming Linear Adoption

**The Problem:**
Projecting early growth rates linearly leads to hockey-stick projections that never materialize.

**Example - Unrealistic Projection:**

```
Year 1: $100K (100 customers)
Year 2: $400K (4x growth)
Year 3: $1.6M (4x growth)
Year 4: $6.4M (4x growth)

Problem: This assumes same growth rate continues indefinitely
```

**Reality of Growth:**

```
Year 1: Slow (early adopters only)
- $100K
- 100 customers
- High touch, lots of learning

Year 2: Acceleration (if PMF achieved)
- $300K (3x, not 4x)
- 300 customers
- Product-market fit starting

Year 3: Strong growth (scaling)
- $750K (2.5x)
- 750 customers
- Repeatable acquisition

Year 4: Sustainable growth
- $1.5M (2x)
- 1,500 customers
- Approaching segment saturation

Year 5: Market share growth
- $2.5M (1.67x)
- Market position established
```

**Realistic Growth Patterns:**

**B2B SaaS (typical):**

- Year 1: Base building (slow)
- Year 2-3: 50-100% YoY growth (if successful)
- Year 4-5: 30-50% YoY growth (sustainable)
- Year 6+: 20-30% YoY (mature)

**Consumer/PLG (typical):**

- Year 1: Slow organic growth
- Year 2: 100-200% if viral mechanics work
- Year 3: 50-100% YoY
- Year 4+: 30-50% YoY

**How to Model Realistically:**

1. Conservative Year 1 (early adopters only)
2. Accelerate Year 2-3 only if PMF validated
3. Decelerate growth rate as market saturates
4. Factor in competitive response
5. Use S-curve thinking, not linear

---

### Mistake 5: No Customer Names

**The "10 Customer Test":**
If you can't name 10 specific potential customers right now, your market might be too narrow or unclear.

**Red Flag:**

```
Interviewer: "Who are your first 10 customers?"
You: "Well, any product manager who needs better roadmapping..."
```

**Green Flag:**

```
Interviewer: "Who are your first 10 customers?"
You: "I've talked to 30 PMs. Here are 10 who said they'd buy:
1. Sarah at Stripe (PM for payments)
2. Mike at Figma (PM for platform)
3. Chen at Notion (PM for integrations)
..."
```

**How to Avoid:**

1. Interview 20-50 potential customers before sizing
2. Keep a spreadsheet of interested prospects
3. Validate they'd actually pay (not just "interested")
4. Use their titles/companies in your bottom-up calculation
5. If you can't name 10, your market may not exist yet

---

### Mistake 6: Forgetting to Update Assumptions

**The Problem:**
Market sizing done once and never revisited, even as you learn.

**Example:**

```
Month 1: Estimated 100,000 potential customers
Month 6: Learned actual number is 30,000
Month 12: Still using 100,000 in all projections
```

**How to Avoid:**

**Set Review Cadence:**

- **Monthly (First 6 months):** Quick review of key assumptions
- **Quarterly (First 2 years):** Full market sizing update
- **Annually (Mature):** Complete re-validation

**Track Actual vs. Projected:**

```markdown
## Market Sizing Tracker

### Original Estimates (Jan 2024)

- SAM: $10M
- Year 1 SOM: $100K
- Assumption: 30,000 potential customers

### Updated Estimates (Jul 2024)

- SAM: $6M (revised down)
- Year 1 SOM: $80K (on track)
- Actual learning: Only 18,000 potential customers, but higher willingness to pay

### What Changed:

- Customer count was overestimated (LinkedIn data was inflated)
- BUT: Pricing power is stronger than assumed
- Net effect: Market smaller but more profitable
```

---

## Validation Frameworks

### The Three-Method Validation

Always calculate market size using all three methods for robust validation.

**Framework:**

```
Method 1: Bottom-Up
Calculate: Count customers × pricing
Confidence: High (most grounded)

Method 2: Top-Down
Calculate: Total market × your segment %
Confidence: Medium (validates direction)

Method 3: Value Theory
Calculate: Value created × capture rate
Confidence: Medium (tests pricing)

If all three agree (within 2-3x): High confidence
If they differ >5x: Deep dive needed
```

**Example - Strong Validation:**

```
Bottom-Up: $5M TAM
(50,000 customers × $100/year)

Top-Down: $6M TAM
($100M PM tools × 6% solo segment)

Value Theory: $4M TAM
(50,000 × 5 hrs saved × $80/hr × 2% capture)

Analysis: All within 2x range → Strong confidence
Use conservative estimate: $4-5M TAM
```

**Example - Weak Validation:**

```
Bottom-Up: $2M TAM
(10,000 customers × $200/year)

Top-Down: $20M TAM
($500M market × 4% segment)

Value Theory: $500K TAM
(10,000 × 2 hrs saved × $50/hr × 5% capture)

Analysis: 40x difference between top-down and value theory
Action Required: Figure out which assumptions are wrong
```

---

### The Sanity Check Framework

Seven questions to reality-check your market sizing.

**1. The Customer Name Test**

```
Can you name 10 specific potential customers?
[ ] Yes → Proceed
[ ] No → Market might not exist or is too narrow
```

**2. The Competitor Validation Test**

```
Are there existing competitors making money in this space?
[ ] Yes → Market exists (good)
[ ] No → Either no market OR huge opportunity (risky)

If yes:
- Estimated competitor revenue: $_________
- Is this < your SAM? (sanity check)
- Can you compete? Why would customers switch?
```

**3. The Current Spending Test**

```
Do customers currently spend money trying to solve this problem?
[ ] Yes → Proven willingness to pay
[ ] No → You'll need to create the market (harder)

If yes:
- What do they spend on: _________
- How much: $_________
- Your pricing relative to current spending: _________%
```

**4. The Size Threshold Test**

```
Is the market large enough for your goals?

Bootstrapped side project: $1M+ TAM
Full-time sustainable business: $10M+ TAM
Venture-backed startup: $100M+ TAM

Your TAM: $_________
Your goal: _________
Match: [ ] Yes [ ] No
```

**5. The Year 1 Feasibility Test**

```
Is your Year 1 SOM achievable with your resources?

Year 1 SOM: $_________
Customers needed: _________
Per month: _________ customers/month

Current capacity:
- Team size: _________
- Budget: $_________
- Sales capacity: _________ deals/month

Can you acquire this many customers?
[ ] Yes, realistic
[ ] Stretch but possible
[ ] No, not feasible
```

**6. The Progression Test**

```
Does TAM > SAM > SOM progression make sense?

TAM: $_________
SAM: $_________ (______% of TAM)
SOM Year 1: $_________ (______% of SAM)

Typical ranges:
- SAM: 10-40% of TAM
- SOM Year 1: 0.1-1% of SAM

Your percentages: [ ] In range [ ] Outside range
```

**7. The Competition Math Test**

```
Market share math validation:

Number of competitors: _________
Average revenue per competitor: $_________
Total competitive revenue: $_________

Your SAM: $_________

Sanity check: Competitive revenue should be < SAM
Check: [ ] Pass [ ] Fail

If fail: Your SAM might be underestimated
```

---

### The Customer Economics Validation

Validate market size by checking unit economics feasibility.

**Framework:**

```
1. Estimate Customer Acquisition Cost (CAC)
   - Marketing cost: $_________
   - Sales cost: $_________
   - Total CAC: $_________

2. Calculate Customer Lifetime Value (LTV)
   - Average revenue per customer: $_________/year
   - Expected lifetime: _________ years
   - Gross margin: _________%
   - LTV = Revenue × Lifetime × Margin = $_________

3. Check LTV:CAC Ratio
   - LTV:CAC = _________:1
   - Healthy: >3:1
   - Great: >5:1
   - Your ratio: [ ] Healthy [ ] Needs work

4. Validate Market Size Against Economics
   - If CAC is too high relative to market size
   - Market might not be economically viable
   - Need: Larger market OR lower CAC OR higher pricing
```

**Example - Economically Viable:**

```
SAM: $10M
Target Year 3: $1M revenue (10% of SAM)
Customers needed: 1,000 (at $1,000/year each)

CAC: $500
LTV: $2,500 (over 3 years)
LTV:CAC: 5:1

Budget to acquire 1,000 customers: $500K
This is feasible with $1M+ funding

Verdict: Market is economically viable
```

**Example - Not Viable:**

```
SAM: $2M
Target Year 3: $200K (10% of SAM)
Customers needed: 400 (at $500/year each)

CAC: $1,200 (enterprise sales required)
LTV: $1,000 (only 2 years average)
LTV:CAC: 0.8:1 (losing money!)

Budget to acquire 400 customers: $480K
Would spend $480K to get $200K revenue

Verdict: Market is NOT economically viable
Need: Lower CAC OR higher pricing OR longer retention
```

---

## Industry-Specific Considerations

Different industries have different market sizing dynamics.

### B2B SaaS

**Characteristics:**

- Long sales cycles (3-12 months)
- High LTV relative to pricing
- Account-based approach
- Expansion revenue important

**Sizing Approach:**

```
Bottom-Up Prioritized:
1. Count companies in target segment (be specific)
2. Estimate % that have the problem
3. Estimate % that would buy (not just "interested")
4. Factor in multi-year contracts
5. Include expansion revenue in LTV

Example:
- US companies with 50-500 employees: 200,000
- % with dedicated PM function: 20% = 40,000
- % that would buy PM tool: 30% = 12,000
- Average contract: $10K/year
- TAM = 12,000 × $10K = $120M

SAM Filters:
- English-speaking only: 70% = 8,400 companies
- Can reach via direct sales: 50% = 4,200
- SAM = 4,200 × $10K = $42M
```

**Special Considerations:**

- Account for expansion revenue (multi-seat, upsells)
- Consider land-and-expand strategy
- Factor in longer sales cycles in Year 1 projections
- Enterprise deals can be lumpy

---

### B2C Consumer

**Characteristics:**

- Fast decision cycles (minutes to days)
- Low LTV, high volume
- Viral/organic growth important
- Paid acquisition at scale

**Sizing Approach:**

```
Focus on Addressable Users:
1. Total users in category (broad)
2. Narrow to your niche
3. Estimate % that would pay (most won't)
4. Calculate at scale (millions of users)

Example:
- Global smartphone users: 6B
- English-speaking: 30% = 1.8B
- Ages 18-45: 40% = 720M
- Interested in productivity: 10% = 72M
- Would pay for app: 1% = 720K
- Average: $5/month × 12 = $60/year
- TAM = 720K × $60 = $43M

Reality check:
- This assumes 1% conversion (typical for consumer)
- Organic + paid acquisition mix
- High churn (20-30% annual is normal)
```

**Special Considerations:**

- Freemium conversion rates (1-5% typical)
- High churn requires constant acquisition
- App store fees (30% cut)
- Global opportunity larger but localization needed

---

### Enterprise B2B

**Characteristics:**

- Very long sales cycles (6-24 months)
- Large contract values ($100K-$1M+)
- Complex buying process
- High implementation effort

**Sizing Approach:**

```
Account-Based Math:
1. List target accounts explicitly (Fortune 500, etc.)
2. Estimate deal size per account
3. Estimate conversion rate (low, 5-15%)
4. Calculate multi-year value

Example:
- Fortune 500 companies: 500
- Companies with need: 200
- Realistic to close Year 1-3: 20 (10%)
- Average contract value: $250K/year
- Average contract length: 3 years
- TAM = 200 × $250K = $50M
- Year 3 SOM = 20 × $250K = $5M
```

**Special Considerations:**

- Land with pilot, expand to enterprise-wide
- Implementation services can be larger than software
- Renewal rates are critical (85%+ needed)
- References and case studies gate next sales

---

### Marketplace / Platform

**Characteristics:**

- Two-sided market (buyers and sellers)
- Network effects (value grows with users)
- Take rate on transactions
- Chicken-and-egg cold start

**Sizing Approach:**

```
Transaction-Based Math:
1. Estimate GMV (Gross Merchandise Value) in category
2. Determine realistic platform share
3. Apply take rate

Example (Freelance Platform):
- Total freelance spending: $1T globally
- Online-friendly segments: $200B
- Addressable (US, English): $50B
- Platform could capture: 2% = $1B GMV
- Take rate: 15%
- TAM = $1B × 15% = $150M

Alternative (User-Based):
- Freelancers in category: 2M
- Subscription model: $20/month
- TAM = 2M × $240/year = $480M
```

**Special Considerations:**

- GMV vs revenue (take rate) distinction
- Need both sides to reach liquidity
- Winner-take-most dynamics
- Supply side often harder to activate

---

### Developer Tools

**Characteristics:**

- Bottom-up adoption (developers choose)
- Freemium/open-source common
- Usage-based pricing
- Strong word-of-mouth

**Sizing Approach:**

```
Developer Count × Adoption:
1. Count developers in target category
2. Estimate % that would use tool
3. Estimate % that would pay (freemium conversion)
4. Calculate based on usage or seats

Example (API Service):
- Backend developers globally: 10M
- Building API products: 20% = 2M
- Would try tool: 10% = 200K
- Convert to paid: 5% = 10K
- Average spend: $500/month = $6K/year
- TAM = 10K × $6K = $60M
```

**Special Considerations:**

- Open-source can expand TAM but complicate pricing
- Usage-based means revenue grows with customer success
- PLG motion (product-led growth) changes acquisition
- Infrastructure spend can scale dramatically

---

## Competitive Landscape Analysis

How to factor competition into realistic market sizing.

### Competitive Intensity Framework

**Assess Market Concentration:**

**1. Fragmented Market (No Clear Leader)**

```
Characteristics:
- No player has >15% share
- 20+ meaningful competitors
- Low switching costs
- Commoditized offerings

Market Opportunity: Medium to High
- Easier to enter
- Can differentiate
- Customer acquisition feasible

SOM Adjustment: 0.5-2% of SAM realistic in Year 1
```

**2. Concentrated Market (2-3 Leaders)**

```
Characteristics:
- Top 3 players have 60%+ combined share
- Clear market leaders
- Moderate switching costs
- Some differentiation

Market Opportunity: Medium
- Need strong differentiation
- Can target underserved segments
- Harder but possible

SOM Adjustment: 0.2-0.8% of SAM realistic in Year 1
```

**3. Monopolistic Market (One Dominant Player)**

```
Characteristics:
- One player has >50% share
- High switching costs
- Network effects or lock-in
- Industry standard

Market Opportunity: Low to Medium
- Very hard to compete directly
- Need wedge strategy
- Target different segment or use case

SOM Adjustment: 0.1-0.3% of SAM realistic in Year 1
```

---

### Competitive Positioning Impact

**Where you fit affects realistic market capture:**

**Head-to-Head Competition:**

```
Competing directly with established player

Challenges:
- Must be 10x better, not 10% better
- High customer acquisition cost
- Trust and brand disadvantage

Realistic SOM:
- Year 1: 0.1-0.5% of SAM
- Need strong differentiation or much lower price
```

**Wedge Strategy:**

```
Serving underserved segment first

Advantages:
- Less competition
- Can build momentum
- Expand later

Realistic SOM:
- Year 1: 1-5% of your niche SAM
- Example: Figma started with design tools for web (not Adobe's core)
```

**New Category Creation:**

```
Creating entirely new category

Challenges:
- Market education required
- No existing budget
- Must prove value

Advantages:
- No competition (yet)
- Can own category

Realistic SOM:
- Year 1: Very low (early adopters only)
- Year 2-3: Can accelerate if category proven
```

---

### The Switching Cost Analysis

**Impact of Switching Costs on Market Capture:**

**Low Switching Costs (<1 hour, <$100)**

```
Examples: Productivity apps, simple tools
Customer behavior: Willing to try alternatives

Market Capture:
- 15-25% of SAM is "in-market" annually
- You can realistically compete for 5-10% of in-market
- Year 1 SOM: 0.75-2.5% of SAM
```

**Medium Switching Costs (1-5 days, $100-$5K)**

```
Examples: CRM, marketing automation
Customer behavior: Will switch if significantly better

Market Capture:
- 8-12% of SAM is "in-market" annually
- You can compete for 3-5% of in-market (with strong value prop)
- Year 1 SOM: 0.25-0.6% of SAM
```

**High Switching Costs (>1 month, >$10K)**

```
Examples: ERP, core infrastructure
Customer behavior: Very reluctant to switch

Market Capture:
- 3-5% of SAM is "in-market" annually
- You can compete for 1-2% of in-market (must be exceptional)
- Year 1 SOM: 0.03-0.1% of SAM
```

---

## Assumption Management

Market sizing is fundamentally about assumptions. Manage them rigorously.

### The Assumption Ladder

**Classify assumptions by impact and confidence:**

```markdown
## Critical Assumptions (High Impact, Must Validate)

### Assumption 1: Customer Count

- Assumption: 500,000 product managers globally
- Source: LinkedIn job title count + BLS data
- Confidence: Medium (data sources may overcount)
- Impact if wrong: ±50% on TAM
- Validation plan: Survey PM communities, validate with industry reports

### Assumption 2: Willingness to Pay

- Assumption: 20% would pay for specialized PM tool
- Source: Customer interviews (15 of 50 expressed interest)
- Confidence: Low (interest ≠ willingness to pay)
- Impact if wrong: ±75% on TAM
- Validation plan: Test pricing with landing page, collect credit cards

### Assumption 3: Pricing

- Assumption: $120/year average
- Source: Competitive analysis, value-based pricing estimate
- Confidence: Medium
- Impact if wrong: Direct 1:1 impact on TAM
- Validation plan: A/B test pricing tiers

## Secondary Assumptions (Medium Impact, Should Validate)

### Assumption 4: Market Growth Rate

- Assumption: 10% annual growth in PM role
- Source: Industry reports
- Confidence: Medium
- Impact if wrong: Affects multi-year projections
- Validation plan: Track job posting trends quarterly

### Assumption 5: Geographic Distribution

- Assumption: 40% of PMs are in English-speaking markets
- Source: LinkedIn data
- Confidence: High
- Impact if wrong: ±20% on SAM
- Validation plan: Industry demographics data

## Tertiary Assumptions (Lower Impact, Monitor)

### Assumption 6: Competitive Response

- Assumption: Incumbents won't directly compete in our niche
- Source: Strategic analysis
- Confidence: Low
- Impact if wrong: Could reduce SOM by 50%
- Validation plan: Monitor product releases, track market moves
```

---

### The Assumption Testing Plan

**Systematic approach to validating assumptions:**

**Before Building (Discovery Phase):**

```
1. Customer Interviews (30-50 people)
   Goal: Validate problem, willingness to pay
   Success: 40%+ say "I would pay for this"

2. Pricing Surveys
   Goal: Validate price points
   Success: 50%+ would pay at target price

3. Competitive Analysis
   Goal: Understand market size, pricing
   Success: Find 3-5 comparable companies with revenue data
```

**During Early Building (MVP Phase):**

```
4. Landing Page Test
   Goal: Validate demand signal
   Success: 5-10% conversion to waitlist

5. Pilot Customers (10-20)
   Goal: Validate usage, retention, expansion
   Success: 60%+ actively using after 30 days

6. Pricing Tests
   Goal: Optimize price point
   Success: Find tier with best LTV:CAC
```

**After Launch (Validation Phase):**

```
7. Customer Acquisition
   Goal: Validate CAC assumptions
   Success: CAC < 1/3 of LTV

8. Retention Analysis
   Goal: Validate customer lifetime assumptions
   Success: <5% monthly churn

9. Market Penetration
   Goal: Validate addressable market
   Success: Hitting projected customer counts
```

---

### The "What If" Tracker

**Track how wrong assumptions affect projections:**

```markdown
## Sensitivity Analysis

### Base Case (Current Assumptions)

- TAM: $10M
- SAM: $3M
- Year 1 SOM: $100K

### Scenario 1: Customer Count is 50% Lower

- Impact: TAM becomes $5M, SAM becomes $1.5M
- Decision: Still viable, but need higher pricing
- Action: Revisit pricing strategy

### Scenario 2: Pricing Must Be 30% Lower

- Impact: TAM becomes $7M, Year 1 SOM becomes $70K
- Decision: Borderline viable for bootstrapping
- Action: Need to reduce CAC or find higher-value segment

### Scenario 3: Adoption Rate is Half

- Impact: SAM becomes $1.5M, Year 1 SOM becomes $50K
- Decision: Too small for full-time, good for side project
- Action: Either pivot or keep as nights/weekends project

### Scenario 4: Competition Fiercer Than Expected

- Impact: Year 1 SOM becomes $50K (takes longer to gain traction)
- Decision: Need more runway
- Action: Reduce burn rate or raise more funding

### Worst Case (All Negative Scenarios)

- Customer count: -50%
- Pricing: -30%
- Adoption: -50%
- Result: TAM = $2.5M, Year 1 SOM = $25K
- Decision: Not viable, would pivot
```

---

## Sensitivity Analysis and Scenario Planning

### The Three-Scenario Framework

**Always model three scenarios to bound your estimates:**

**1. Pessimistic Scenario (30% Probability)**

```
Assumptions:
- Customer count: Lower estimate
- Pricing: 30% below target
- Adoption: Half of expected
- Competition: Fiercer
- Sales cycle: 2x longer

Example:
- TAM: $5M (vs $10M base case)
- SAM: $1.5M (vs $3M base case)
- Year 1 SOM: $50K (vs $100K base case)
- Year 3 SOM: $200K (vs $500K base case)

Decision Framework:
- Is worst case still worth pursuing?
- If not, too risky
- If yes, understand downside
```

**2. Base Case (50% Probability)**

```
Assumptions:
- Current best estimates
- Realistic adoption rates
- Normal competitive dynamics
- Expected sales cycle

Example:
- TAM: $10M
- SAM: $3M
- Year 1 SOM: $100K
- Year 3 SOM: $500K

Decision Framework:
- This is your working model
- Use for planning and resource allocation
- Update quarterly as you learn
```

**3. Optimistic Scenario (20% Probability)**

```
Assumptions:
- Customer count: Higher estimate
- Pricing: Can charge more
- Adoption: Faster than expected
- Weaker competition
- Viral growth

Example:
- TAM: $20M (vs $10M base case)
- SAM: $6M (vs $3M base case)
- Year 1 SOM: $200K (vs $100K base case)
- Year 3 SOM: $1.5M (vs $500K base case)

Decision Framework:
- Don't plan for this
- But understand upside potential
- Helps with fundraising narrative
```

---

### Monte Carlo Simulation Approach

**For advanced analysis, use probability distributions:**

```markdown
## Probabilistic Market Sizing

### Input Variables (with ranges)

Customer Count:

- Low: 300,000 (10th percentile)
- Base: 500,000 (50th percentile)
- High: 800,000 (90th percentile)
- Distribution: Normal

Adoption Rate:

- Low: 15% (10th percentile)
- Base: 25% (50th percentile)
- High: 40% (90th percentile)
- Distribution: Skewed (long tail of high adoption)

Pricing:

- Low: $80/year
- Base: $120/year
- High: $180/year
- Distribution: Normal

### Run Simulation (1000 iterations)

Result (TAM):

- 10th percentile: $3.6M
- Median: $15M
- 90th percentile: $57M
- Mean: $18M (skewed by high end)

Interpretation:

- 80% confidence: TAM is between $3.6M and $57M
- Use median ($15M) for planning, not mean
- Understand that huge uncertainty exists
```

---

## Case Studies: Good vs Bad Market Sizing

### Case Study 1: Superhuman (Good Market Sizing)

**Background:**
Email client for high-velocity professionals, launched 2017.

**Market Sizing Approach:**

```
Bottom-Up (Primary):
- "Very busy professionals" (VCs, founders, execs): ~500K globally
- % who need email help: 80% = 400K
- % willing to pay premium: 50% = 200K
- Pricing: $30/month = $360/year
- TAM = 200K × $360 = $72M

Validation:
- Started with waitlist of 100K+
- Very clear ICP (ideal customer profile)
- Knew exact target market

Result:
- Achieved ~$20M ARR by 2021
- 27% of TAM in 4 years (strong capture)
- Market sizing was realistic
```

**What They Did Right:**

- Narrow, well-defined segment
- Validated willingness to pay ($30/month was tested)
- Bottom-up approach with actual customer names
- Conservative estimates
- Premium positioning matched market sizing

---

### Case Study 2: Quibi (Bad Market Sizing)

**Background:**
Short-form video platform for mobile, raised $1.75B, shut down after 6 months.

**Market Sizing Approach (Flawed):**

```
Top-Down (Only):
- Mobile video market: $50B
- "Quick bites" segment: 10% = $5B
- Quibi could capture: 5% = $250M/year
- Therefore: Massive opportunity

Problems:
- No bottom-up validation
- Didn't validate customer willingness to pay
- Assumed market wanted this (they didn't)
- Never asked: "Who are our first 10,000 customers?"
```

**What Went Wrong:**

- Pure top-down sizing (no customer validation)
- Built 18 months before launching
- Ignored competitive threats (TikTok, YouTube)
- Didn't validate that problem existed
- $1.75B spent without market validation

**Result:**

- 500K subscribers at peak (vs millions expected)
- <6 months to shutdown
- Market sizing was fantasy

---

### Case Study 3: Figma (Patient Market Building)

**Background:**
Design tool, founded 2012, launched 2015, IPO territory by 2021.

**Market Sizing Evolution:**

```
Phase 1 (2012-2015): Building Technology
- Didn't size market initially
- Focused on technical feasibility
- Knew design tools was multi-billion market

Phase 2 (2015-2018): Wedge Strategy
- Initial TAM: "Designers who design for web" = $100M
- Much smaller than Adobe's TAM
- But less competition, could win

Phase 3 (2018-2020): Market Expansion
- COVID accelerated remote collaboration need
- TAM expanded: "All designers who collaborate" = $5B+
- Market came to them

Phase 4 (2020+): Platform Play
- TAM: "All creative professionals" = $20B+
- Expansion into adjacent markets
```

**What They Did Right:**

- Started narrow (wedge)
- Patient technology building (3 years before launch)
- Expanded TAM as product proved itself
- Market timing met product readiness
- Bottom-up expansion (team by team adoption)

---

### Case Study 4: Slack (Market Creation)

**Background:**
Team communication, launched 2013, grew to $1B+ ARR by 2019.

**Market Sizing Approach:**

```
Initial (2013):
- "Team communication" market didn't really exist
- Email was incumbent
- Hard to size: Creating new category

Approach:
- Started with bottom-up in tech companies
- Sized: "Tech company teams" = 50K companies
- Average: $5K/year
- Initial TAM: $250M (conservative)

Reality (2019):
- Expanded to all industries
- Market was actually $10B+ (much larger)
- They created the market

Evolution:
2013: $250M TAM (tech companies only)
2015: $2B TAM (all companies)
2019: $10B+ TAM (market leadership)
2022: $28B valuation (mature market)
```

**Lessons:**

- When creating market, size conservatively
- Start with reachable segment
- Market can be larger than you think
- But don't plan for best case

---

## Advanced Considerations

### Market Timing Impact

**Markets are not static - timing matters:**

**Emerging Market (Growing >20% annually):**

```
Characteristics:
- New technology or behavior
- Increasing awareness
- Growing budget allocation

Sizing Approach:
- Project growth into future
- Model expanding TAM over time
- Example: AI tools market 2023-2025

Year 1 TAM: $500M
Year 2 TAM: $750M (+50%)
Year 3 TAM: $1.2B (+60%)

Your capture can grow faster than market
```

**Mature Market (Growing <5% annually):**

```
Characteristics:
- Established category
- Fixed budget pool
- Market share game

Sizing Approach:
- TAM is relatively fixed
- Growth comes from share gain
- Harder to win

TAM: $5B (relatively stable)
Your growth must come from:
- Taking share from competitors
- Expanding usage within accounts
- Adjacent product expansion
```

**Declining Market (Negative growth):**

```
Characteristics:
- Technology shift
- Behavior change
- Budget migration

Sizing Approach:
- Don't just project current market forward
- Model decline rate
- May not be worth entering

Example: DVD rental market 2010-2015
Year 1 TAM: $5B
Year 2 TAM: $3.5B (-30%)
Year 3 TAM: $2B (-40%)

Warning: Even if you win share, market shrinks
```

---

### Geographic Expansion Dynamics

**How to model geographic market expansion:**

**Phase 1: Home Market (Year 1)**

```
Start narrow:
- US only: 40% of global market
- English-speaking: 70% of global market
- Your geography: X% of global TAM

SAM = Global TAM × Geographic %
```

**Phase 2: Similar Markets (Year 2-3)**

```
Expand to similar:
- Cultural similarity
- Same language
- Similar GDP per capita

Example: US → UK, Canada, Australia
Combined: 50% of global market
```

**Phase 3: International (Year 3-5)**

```
Full international:
- Localization required
- Different pricing
- Different go-to-market

Reach: 80-100% of global TAM
But: Different economics per region
```

**Modeling Approach:**

```markdown
## Geographic TAM Expansion

### Year 1: US Only

- Global TAM: $10M
- US: 40% = $4M
- SAM (Year 1): $4M

### Year 2: English-Speaking

- Add: UK, Canada, Australia, NZ
- Coverage: 50% of global = $5M
- SAM (Year 2): $5M

### Year 3: Europe

- Add: Germany, France, Spain (localized)
- Coverage: 70% of global = $7M
- SAM (Year 3): $7M

### Year 4-5: Global

- Add: Asia-Pacific, Latin America
- Coverage: 90% of global = $9M
- SAM (Year 4-5): $9M

Note: SAM grows even if TAM stays constant
```

---

### Platform Effects and Network Dynamics

**For platforms and networks, market sizing is different:**

**Network Effects Impact:**

```
Traditional Product:
- Value is linear with adoption
- Market size is fixed pool

Network Product:
- Value grows with adoption (n² or n×log(n))
- Market can expand as value increases
- Winner-take-most dynamics

Implication:
- Early market size estimates may be too low
- If network effects kick in, TAM expands
- But: Market also consolidates (fewer winners)
```

**Example: Social Network**

```
Initial TAM (before network effects):
- Potential users: 100M
- Willingness to pay: $5/year
- TAM: $500M

After Network Effects:
- Users: 1B (10x larger - network drew more users)
- Willingness to pay: $0 (ad-supported)
- Advertiser TAM: $20B (much larger than original)

Lesson: Network products can expand TAM dramatically
But: Business model may change
```

---

### Adjacent Market Opportunities

**How to model expansion beyond core market:**

**Framework:**

```
Core Market (Year 1-2):
- Your initial target
- Example: "PM tools for solo PMs"
- TAM: $10M

Adjacent Market 1 (Year 3-4):
- Natural expansion
- Example: "PM tools for small teams"
- Additional TAM: $30M

Adjacent Market 2 (Year 4-5):
- Further expansion
- Example: "PM tools for enterprise"
- Additional TAM: $100M

Total Addressable (Long-term):
- Sum of all adjacent markets
- Example: $140M total
```

**Modeling Caution:**

- Don't include adjacent markets in initial TAM
- Validate core before expanding
- Adjacent markets may require different products
- Show progression: Core → Adjacent 1 → Adjacent 2

---

## Summary: Market Sizing Best Practices

**DO:**

1. **Use all three methods** (bottom-up, top-down, value theory) for validation
2. **Start with bottom-up** (most grounded in reality)
3. **Name actual customers** (the "10 customer test")
4. **Document all assumptions** (and track confidence)
5. **Reality-check with competition** (how much market is available?)
6. **Model three scenarios** (pessimistic, base, optimistic)
7. **Update regularly** (quarterly in early stages)
8. **Check unit economics** (CAC, LTV, margins)
9. **Be conservative** (under-promise, over-deliver)
10. **Validate with actual customers** (not just data)

**DON'T:**

1. **Don't use only top-down** (inflates numbers)
2. **Don't confuse TAM with SAM** (be explicit)
3. **Don't ignore competition** (market is not empty)
4. **Don't assume linear growth** (use S-curves)
5. **Don't forget to update** (assumptions will be wrong)
6. **Don't size once and forget** (revisit quarterly)
7. **Don't let large TAM seduce you** (SAM and SOM matter more)
8. **Don't plan for optimistic case** (plan for base case)
9. **Don't skip customer validation** (talk to 30-50 people minimum)
10. **Don't trust your own estimates** (validate externally)

**Key Principle:**
Market sizing is educated guessing. The goal is reasonable estimates with documented assumptions, not precision. Focus on getting the order of magnitude right (is it $1M, $10M, or $100M?) rather than exact numbers.

**Remember:**

- If you can't name 10 customers, your market might not exist
- If competitors exist and are profitable, market is validated
- If Year 1 SOM < $50K, question whether market is worth it
- Market sizing should inform decisions, not justify them

---

## Further Reading

**Books:**

- **"Disciplined Entrepreneurship"** - Bill Aulet (MIT methodology)
- **"The Four Steps to the Epiphany"** - Steve Blank (customer development)
- **"Crossing the Chasm"** - Geoffrey Moore (market adoption curves)

**Articles:**

- **"How to Calculate TAM, SAM, and SOM"** - Bain & Company
- **"Market Sizing: A Complete Guide"** - First Round Review
- **"The Startup Founder's Guide to Market Sizing"** - NFX

**Frameworks:**

- **Jobs-to-be-Done** - Clayton Christensen (understanding market size through jobs)
- **TAM/SAM/SOM** - Bill Aulet (MIT three-tier framework)
- **Validated Learning** - Eric Ries (test assumptions systematically)

**Data Sources:**

- **Gartner, IDC, Forrester** - Industry market sizing reports
- **Bureau of Labor Statistics** - Employment and wage data
- **Census Bureau** - Demographic and economic data
- **LinkedIn** - Job titles and company data
- **Crunchbase, PitchBook** - Competitor funding and revenue estimates
