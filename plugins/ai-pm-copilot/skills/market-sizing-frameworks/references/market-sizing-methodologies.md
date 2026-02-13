# Market Sizing Methodologies Guide

Complete guide to all market sizing approaches with detailed examples, when to use each method, and how to combine them for accurate estimates.

## Table of Contents

- [Overview](#overview)
- [Method 1: Bottom-Up Approach](#method-1-bottom-up-approach)
- [Method 2: Top-Down Approach](#method-2-top-down-approach)
- [Method 3: Value Theory Approach](#method-3-value-theory-approach)
- [Combining All Three Methods](#combining-all-three-methods)
- [Industry-Specific Approaches](#industry-specific-approaches)
- [Summary: Method Selection Guide](#summary-method-selection-guide)

## Overview

Market sizing is part art, part science. The goal is not precision - it's reasonable estimates that help you make decisions about market opportunity.

**The Three Fundamental Approaches:**

1. **Bottom-Up**: Build from customer counts (most reliable)
2. **Top-Down**: Start with total market, narrow down (good validation)
3. **Value Theory**: Calculate from value created (tests pricing)

**Best practice:** Use all three methods, compare results, understand differences.

---

## Method 1: Bottom-Up Approach

**Philosophy:** Count specific customers, multiply by average revenue.

**When to use:**

- Primary method for most markets
- When you can identify and count customers
- For new products where no market data exists
- Most reliable and defensible

**Strengths:**

- Based on specific, verifiable data
- Forces you to think granularly
- Easy to explain and defend
- Can segment precisely

**Weaknesses:**

- Time-consuming
- Requires good customer data
- May miss edge cases
- Can be conservative

---

### Step-by-Step Bottom-Up Process

#### Step 1: Define Your Customer Universe

**Be extremely specific about who is a customer:**

**Bad (too broad):**

- "Businesses"
- "People who need X"
- "Companies with Y problem"

**Good (specific):**

- "B2B SaaS companies, 10-200 employees, in North America, using Salesforce, with dedicated product teams"
- "Solo software developers building their own products, making <$100K/year, focused on mobile apps"
- "Series A-B startup founders who raised $2M-$20M in last 18 months, building B2B products"

**How to define:**

```
Who they are:
- Job title/role: _____________
- Company size: _____________
- Industry: _____________
- Geography: _____________
- Stage: _____________

What they do:
- Specific activity: _____________
- Frequency: _____________
- Tools they use: _____________

Psychographics:
- Values: _____________
- Behaviors: _____________
- Pain points: _____________
```

**Test your definition:**

- Can you identify 10 people who fit this? (If no, too narrow)
- Can you exclude 10 people who don't fit? (If no, too broad)

---

#### Step 2: Count Total Customers

**Data Sources (in order of reliability):**

**Government/Official Data:**

```
Examples:
- Bureau of Labor Statistics (job counts)
- Census Bureau (business counts)
- Professional licensing boards
- Government registrations

Pros: Authoritative, free, comprehensive
Cons: Often outdated, broad categories

Example:
"BLS reports 50,000 product managers in US (2023)"
```

**Platform Data:**

```
Examples:
- LinkedIn (search by job title, company, location)
- GitHub (developer counts by language/activity)
- Crunchbase (startups by stage, funding, location)
- App stores (developers, downloads)

Pros: Current, filterable, specific
Cons: Incomplete, sampling bias

Example:
"LinkedIn shows 75,000 profiles with 'Product Manager' title in US"
```

**Market Research:**

```
Examples:
- Gartner, IDC, Forrester reports
- Industry associations
- Trade publications
- Academic research

Pros: Expert analysis, trend data
Cons: Expensive, paywalled, dated

Example:
"Gartner estimates 500,000 PMs globally (2024)"
```

**Your Own Research:**

```
Methods:
- Customer interviews
- Surveys
- Industry events
- Direct observation

Pros: Specific to your definition, current
Cons: Small sample, time-intensive

Example:
"Interviewed 50 solo developers, 40% building products (20/50)"
```

**Triangulation approach:**
Use multiple sources and average:

```
Source A (BLS): 50,000
Source B (LinkedIn): 75,000
Source C (Gartner): 60,000

Average: 62,000
Range: 50K-75K
Use: 60,000 (conservative)
```

---

#### Step 3: Filter to Addressable Market

**Apply sequential filters:**

**Filter 1: Have the Problem**

```
Total potential: 60,000 PMs

Who have this specific problem: 80%
(Example: Use PM tools actively)

After filter: 60,000 × 80% = 48,000
```

**Filter 2: Aware of Solutions**

```
Starting: 48,000

Who know solutions exist: 70%
(Many use default/free tools, unaware of specialized options)

After filter: 48,000 × 70% = 33,600
```

**Filter 3: Willing to Pay**

```
Starting: 33,600

Who would pay for solution: 50%
(Others use free alternatives, company won't pay, etc.)

After filter: 33,600 × 50% = 16,800
```

**Filter 4: Can Reach Them**

```
Starting: 16,800

Who you can reach through your channels: 60%
(Distribution, marketing, network limitations)

Final addressable: 16,800 × 60% = 10,080
```

**Adoption Curve Consideration:**

If creating new category:

- Innovators (2.5%): 10,080 × 2.5% = 252
- Early Adopters (13.5%): 10,080 × 13.5% = 1,361
- Total early market: 1,613

If existing category:

- Early + Early Majority (50%): 10,080 × 50% = 5,040

---

#### Step 4: Estimate Revenue Per Customer

**Approach A: Comparable Pricing**

```
Find 5 comparable products:
- Product A: $15/month = $180/year
- Product B: $25/month = $300/year
- Product C: $10/month = $120/year
- Product D: $20/month = $240/year
- Product E: $12/month = $144/year

Average: $197/year
Median: $180/year

Your pricing: $15/month = $180/year
(At median, defensible)
```

**Approach B: Value-Based Pricing**

```
Value created per customer:
- Time saved: 5 hours/week
- Value of time: $80/hour
- Weekly value: $400
- Annual value: $20,800

Standard capture: 10% of value
Price: $20,800 × 10% = $2,080/year

But market rate is $180/year (1% of value)
Use: $180/year (market-driven, not value-driven)
```

**Approach C: Tiered Pricing**

```
If you have tiers:
- Basic (60% of customers): $120/year
- Pro (30% of customers): $240/year
- Enterprise (10% of customers): $600/year

Weighted average:
$120 × 0.6 + $240 × 0.3 + $600 × 0.1
= $72 + $72 + $60 = $204/year
```

---

#### Step 5: Calculate TAM

```
Addressable customers: 10,080
Revenue per customer: $180/year

TAM = 10,080 × $180 = $1,814,400

Rounded: $1.8M TAM
```

---

### Bottom-Up Example: Solo Developer Tool

**Complete worked example:**

**Step 1: Define Universe**

```
"Solo software developers building their own products (not employed full-time),
based in English-speaking countries, working on web or mobile apps,
making <$100K/year from their products, actively developing (not just maintaining)"
```

**Step 2: Count Total**

```
Source A (GitHub): ~10M active developers
Filter (solo, product-building): ~500K (5%)

Source B (Indie Hackers): 100K members
Filter (active, building products): ~40K (40%)

Source C (Product Hunt): Makers ~50K
Filter (solo developers): ~30K (60%)

Triangulation:
Conservative estimate: 200,000 solo devs building products globally
```

**Step 3: Filter to Addressable**

```
Total: 200,000

English-speaking markets: 60% = 120,000
(US, UK, Canada, Australia, India, etc.)

Using PM tools (not just code): 40% = 48,000
(Many developers don't use formal PM processes)

Would pay for tools: 30% = 14,400
(Many use free alternatives: Notion, Trello)

Can reach through our channels: 50% = 7,200
(Product Hunt, Dev.to, HN, Reddit)

Addressable: 7,200 customers
```

**Step 4: Revenue**

```
Comparable pricing:
- Notion: $10/month (but multi-use)
- Linear: $8/user/month (but team-focused)
- Coda: $12/month

Target: $10/month = $120/year
(Affordable for solo devs, comparable to alternatives)
```

**Step 5: Calculate**

```
TAM = 7,200 × $120 = $864,000

Rounded: $860K TAM
```

**Validation:**

```
If we capture 10% of market in 3 years:
720 customers × $120 = $86,400/year

Is this worth it?
- Solo founder: Yes, enough to live on
- Small team: Maybe, tight but possible
- VC-backed: No, too small

Decision: Good for bootstrap, not for VC
```

---

## Method 2: Top-Down Approach

**Philosophy:** Start with large market, narrow to your segment.

**When to use:**

- Validation of bottom-up calculation
- When customer counts are unavailable
- For investor presentations (shows big picture)
- Quick market sense

**Strengths:**

- Fast
- Shows big picture context
- Easy to communicate
- Leverages existing research

**Weaknesses:**

- Can be wildly inflated
- Assumptions compound
- Hard to validate
- Easy to manipulate

---

### Step-by-Step Top-Down Process

#### Step 1: Find Total Market Size

**Where to find data:**

**Market Research Firms:**

```
Examples:
- Gartner ($2K-$10K per report)
- Forrester ($1K-$5K per report)
- IDC, Grand View Research, etc.

What they provide:
- Total market size ($X billion)
- Growth rates (X% CAGR)
- Segment breakdowns
- 5-year forecasts

Example:
"Project Management Software Market: $6.8B (2024),
growing 10.5% annually to $11.2B (2029)" - Gartner
```

**Free Sources:**

```
- Industry association reports
- Government industry reports
- Public company filings (TAM disclosure)
- Market summaries on Statista (free tier)
- Business news articles citing research

Example:
"Collaboration software market $12B" - Forbes citing IDC
```

**Proxy Markets:**

```
If your specific market isn't sized, find related:
- Broader category
- Adjacent market
- Sum of related submarkets

Example:
If "PM tools for solo devs" not sized, use:
- "Productivity software market" $X
- "Developer tools market" $Y
- "Project management market" $Z
```

---

#### Step 2: Estimate Your Segment

**Apply percentage filters sequentially:**

**Example: PM Tool for Solo Developers**

```
Starting market: "Project Management Software"
Total market size: $6.8B (Gartner 2024)

Filter 1: Solo/Small Team Segment
- Enterprise PM tools: 60% = $4.1B
- SMB PM tools: 30% = $2.0B
- Individual PM tools: 10% = $0.68B

Your segment: Individual tools = $680M

Filter 2: Developer-Specific
- General PM tools: 70% = $476M
- Developer-focused PM tools: 30% = $204M

Your segment: $204M

Filter 3: Solo Developers (vs small teams)
- Solo individual: 40% = $82M
- 2-5 person teams: 60% = $122M

Your segment: $82M

Filter 4: English-speaking markets
- Global: $82M
- English-speaking: 50% = $41M

Final TAM (top-down): $41M
```

**Validate filters:**

```
Total filters applied: 10% × 30% × 40% × 50% = 0.6%

From $6.8B to $41M = 0.6% of total market

Is 0.6% reasonable for "PM tools for solo developers"?
- Seems right: Very specific niche
- Could argue 1-2% if include adjacent segments
```

---

#### Step 3: Sanity Check

**Compare to bottom-up:**

```
Bottom-up TAM: $860K
Top-down TAM: $41M

Difference: 48x

Why such a big difference?
- Top-down may include tangential products
- Bottom-up may be too conservative on reach
- Truth likely in between

Revised estimate: ~$5-10M TAM
(Split the difference, lean toward conservative)
```

---

### Top-Down Example: Enterprise SaaS

**Complete worked example:**

**Step 1: Total Market**

```
"Enterprise Software Market"
Size: $500B (2024) - Gartner

Too broad, narrow to category:
"Enterprise Collaboration Software"
Size: $50B - IDC

Still broad, narrow further:
"Enterprise Team Communication"
Size: $8B - Forrester
```

**Step 2: Apply Filters**

```
Starting: $8B (Team Communication)

Geography (North America focus):
$8B × 40% = $3.2B

Company size (mid-market, 100-1000 employees):
$3.2B × 30% = $960M

Industry (Tech companies):
$960M × 40% = $384M

Use case (async communication, not real-time):
$384M × 25% = $96M

Final TAM: $96M
```

**Step 3: Validate**

```
Comparables:
- Slack revenue: ~$1.5B (but all segments)
- Teams bundled (hard to estimate)
- Asana revenue: ~$500M (PM + communication)

If Slack is $1.5B across all segments,
and we're targeting 5-10% of their TAM,
$96M seems reasonable

Validation: ✓ Passes sanity check
```

---

## Method 3: Value Theory Approach

**Philosophy:** Calculate market size based on value created.

**When to use:**

- Testing pricing assumptions
- New category (no comparables)
- Disruptive innovation
- Value proposition validation

**Strengths:**

- Grounded in customer value
- Tests if pricing makes sense
- Good for pitching
- Shows value capture opportunity

**Weaknesses:**

- Hard to quantify value
- Capture rate is guesswork
- Assumes rational buyers
- Can be overly optimistic

---

### Step-by-Step Value Theory Process

#### Step 1: Quantify Value Created

**Approach A: Time Savings**

```
Time saved per customer:
- Hours per week: 5 hours
- Value of time: $80/hour
- Weekly value: 5 × $80 = $400
- Annual value: $400 × 52 = $20,800 per customer

Value created for all customers:
- Potential customers: 10,000
- Total value: 10,000 × $20,800 = $208M value created annually
```

**How to estimate "value of time":**

```
For individuals:
- Hourly rate (freelancer): Direct
- Salary ÷ 2080 hours: For employees
- Opportunity cost: What else could they do?

For companies:
- Loaded labor cost (salary × 1.4-2.0)
- Revenue per employee ÷ hours
- Opportunity cost (lost revenue)

Example:
$100K salary employee
Loaded cost: $140K/year
Hourly: $140K ÷ 2080 = $67/hour
Round to: $70/hour for calculations
```

---

**Approach B: Cost Savings**

```
Current cost of alternatives:
- Tool A: $200/year
- Tool B: $300/year
- Manual process: $500/year (time cost)
Total current cost: $1,000/year

Your solution:
- Replaces all three
- More efficient
- Cost: $150/year

Net savings: $1,000 - $150 = $850/year per customer

Total value created:
- Potential customers: 10,000
- Total savings: 10,000 × $850 = $8.5M/year
```

---

**Approach C: Revenue Increase**

```
Revenue increase from using your tool:
- Better conversion rates: +5%
- Average customer revenue: $50K/year
- Increase: $50K × 5% = $2,500/year

Attribution to your tool: 50%
(Other factors also contribute)

Value created: $2,500 × 50% = $1,250/year per customer

Total value created:
- Potential customers: 10,000
- Total value: 10,000 × $1,250 = $12.5M/year
```

---

#### Step 2: Estimate Value Capture Rate

**How much of created value can you charge?**

**Industry standards:**

```
B2C Productivity: 10-20% of value created
B2B SaaS: 10-30% of value created
Enterprise Software: 30-50% of value created
Infrastructure/Platforms: 5-15% of value created
```

**Why not capture more?**

- Customer needs ROI (typically want 3-10x)
- Competition sets ceiling
- Buyer psychology (anchoring)
- Willingness to pay ≠ value created

**Example calculation:**

```
Value created: $20,800/year per customer
Capture rate: 10% (B2C standard)
Your pricing: $20,800 × 10% = $2,080/year

But market comparables: $180/year
Actual capture: $180 ÷ $20,800 = 0.9%

Insight: Market significantly underprices value
Opportunity: Either price higher or capture more customers
```

---

#### Step 3: Calculate TAM

```
Value-based TAM calculation:

Option A: Theoretical Max (full value capture at standard rate)
Customers: 10,000
Value created: $20,800/customer
Capture rate: 10%
TAM = 10,000 × $20,800 × 10% = $20.8M

Option B: Market-Rate (what market actually pays)
Customers: 10,000
Market rate: $180/customer
TAM = 10,000 × $180 = $1.8M

Insight: $1.8M is realistic TAM, but $20.8M shows value gap
Strategy: Could we capture more value through better positioning?
```

---

### Value Theory Example: Developer Productivity Tool

**Complete worked example:**

**Step 1: Quantify Value**

```
Tool: AI-powered code review assistant

Time saved per developer:
- Code review time: 5 hours/week currently
- Tool reduces to: 2 hours/week
- Savings: 3 hours/week

Value of developer time:
- Average developer salary: $120K/year
- Loaded cost: $170K/year
- Hourly: $170K ÷ 2080 = $82/hour

Weekly value: 3 hours × $82 = $246
Annual value: $246 × 52 = $12,792 per developer

Quality improvement value:
- Fewer bugs: ~$5K/year saved
- Faster shipping: ~$3K/year value
Total quality value: $8K/year

Total value created: $12,792 + $8,000 = $20,792/year per dev
```

**Step 2: Capture Rate**

```
Value created: $20,792/year
Standard B2B capture: 20%
Theoretical price: $20,792 × 20% = $4,158/year

But need ROI for customer:
Customer wants 3x ROI minimum
Max they'd pay: $20,792 ÷ 3 = $6,931/year

Competitive pricing (similar tools):
- Tool A: $500/year/dev
- Tool B: $800/year/dev
- Tool C: $600/year/dev
Average: $633/year

Your pricing (competitive): $600/year
Actual capture: $600 ÷ $20,792 = 2.9%

Much lower than theoretical, but market-driven
```

**Step 3: Calculate TAM**

```
Potential customers: 5M developers globally
Filter (would use this tool): 20% = 1M devs
Filter (English-speaking): 60% = 600K devs
Filter (companies would pay): 40% = 240K devs

TAM = 240,000 × $600 = $144M

Theoretical max (if captured 20% of value):
TAM = 240,000 × $4,158 = $998M

Insight: Market is $144M at current pricing, but
could be $998M if we could capture more value through
positioning, bundling, or enterprise pricing
```

---

## Combining All Three Methods

**Best practice approach:**

### Step 1: Calculate All Three

```
Bottom-Up TAM:    $860K
Top-Down TAM:     $41M
Value Theory TAM: $20.8M
```

### Step 2: Analyze Differences

```
Why such variation?

Bottom-Up ($860K) is most conservative:
- Based on specific customer counts
- Realistic reach assumptions
- May underestimate market

Top-Down ($41M) is highest:
- Includes adjacent segments we missed
- Market research includes tangential products
- May overestimate our specific segment

Value Theory ($20.8M) is middle:
- Based on value created
- Assumes higher value capture than market currently does
- Aspirational but grounded
```

### Step 3: Triangulate

```
Approach A: Simple Average
($860K + $41M + $20.8M) ÷ 3 = $20.9M
But gives equal weight to all methods

Approach B: Weighted Average
Bottom-Up (50%): $860K × 0.5 = $430K
Top-Down (25%): $41M × 0.25 = $10.25M
Value Theory (25%): $20.8M × 0.25 = $5.2M
Weighted: $15.9M

Approach C: Range
Conservative: $5M (lean toward bottom-up)
Aggressive: $40M (lean toward top-down)
Mid-point: $20M

Recommended TAM: $15-20M
(Weighted average, with range for sensitivity)
```

### Step 4: Document Rationale

```
TAM Estimate: $15-20M

Reasoning:
- Bottom-up gives $860K but likely undercounts reach
- Top-down gives $41M but includes adjacent segments
- Value theory shows $20.8M opportunity at higher pricing
- Triangulated to $15-20M range

Confidence: Medium
- Good data on customer counts
- Comparable market research exists
- Value creation is measurable

Assumptions to validate:
- Can we reach more than 7,200 customers? (expand bottom-up)
- Is top-down including non-competitive products? (refine)
- Could we capture more value through positioning? (test)
```

---

## Industry-Specific Approaches

### B2B SaaS

**Primary: Bottom-Up**

```
Count companies by:
- Employee size
- Revenue range
- Industry
- Technology stack

Data sources:
- ZoomInfo, Clearbit
- LinkedIn Sales Navigator
- Crunchbase (for startups)
- Public company databases
```

### Consumer Apps

**Primary: Top-Down + Value Theory**

```
Start with:
- Smartphone users: 6B globally
- App category downloads
- Time spent in category

Then bottom-up:
- Active users in category
- Conversion to paid
- ARPU
```

### Enterprise Software

**Primary: Bottom-Up (Company Count)**

```
Global 2000 companies
Fortune 500 subset
Industry-specific counts

Revenue per account: $100K-$1M+
Smaller customer count, higher revenue
```

### Developer Tools

**Primary: Bottom-Up (Developer Count)**

```
GitHub users: 100M
Active developers: Filter down
Paying developers: 5-10%
ARPU: $100-$500
```

---

## Summary: Method Selection Guide

```
Use Bottom-Up when:
✓ You can count customers
✓ You need defensible numbers
✓ You're presenting to investors
✓ Market is new/undefined

Use Top-Down when:
✓ Quick sense-check needed
✓ Validating bottom-up
✓ Showing big picture
✓ Market research exists

Use Value Theory when:
✓ Testing pricing
✓ No comparables exist
✓ Disruptive innovation
✓ Need to justify premium pricing

Always:
✓ Use multiple methods
✓ Understand why they differ
✓ Document assumptions
✓ Validate with customers
```
