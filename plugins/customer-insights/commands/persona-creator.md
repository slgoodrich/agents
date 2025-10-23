# Persona Creator

Generate detailed user personas from research, data, and customer insights to guide product decisions.

## Usage

```
/customer-insights:persona [target user segment or role] [optional: research data, demographics]
```

## What This Command Does

1. Creates research-based user personas with demographics, goals, behaviors, and pain points
2. Synthesizes data from interviews, surveys, analytics, and customer insights
3. Develops realistic scenarios showing how personas use the product
4. Identifies persona-specific needs, motivations, and decision criteria
5. Provides actionable insights for product, design, and marketing teams
6. Takes 45 minutes vs 2-3 hours of manual persona creation

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Persona Context**:
- Who is this persona representing? (user segment, role, job title)
- Why are you creating this persona? (product planning, marketing, feature prioritization)
- How will this persona be used? (roadmap decisions, design validation, messaging)
- Are there multiple personas needed? (primary vs secondary)

**Research Data Available**:
- User research conducted? (interviews, surveys, usability tests)
- How many participants? (sample size for each method)
- Analytics data? (behavioral data, usage patterns)
- Customer feedback? (support tickets, reviews, sales calls)
- Competitive analysis? (how competitors segment users)

**Demographic Information**:
- Age range of this user segment
- Job titles/roles (if B2B)
- Company size/industry (if B2B)
- Geographic location (if relevant)
- Technical sophistication level

**Behavioral Information**:
- What are their primary goals with your product?
- What pain points do they experience?
- What tools do they currently use?
- How do they make purchasing decisions?
- What's their typical workflow?

**Example Input**:
```
Persona: Mid-market sales manager
Purpose: Inform CRM feature prioritization
Research: 12 user interviews, 200 survey responses, 6 months analytics
Demographics: 30-45 years old, manages teams of 5-15 reps
Industry: B2B SaaS companies, 50-200 employees
Goals: Hit quota, retain top performers, reduce manual reporting
Pain points: Data entry burden, lack of pipeline visibility, manual forecasting
Tools: Salesforce, Excel, Slack, Zoom
```

### 2. Synthesize Research into Persona

**Data Sources to Synthesize**:
- **Qualitative**: Interview transcripts, open survey responses, customer quotes
- **Quantitative**: Survey data, analytics, demographic information
- **Behavioral**: Usage patterns, feature adoption, workflow observations
- **Attitudinal**: Motivations, frustrations, decision criteria

**Persona Components**:
1. **Demographic Profile**: Age, role, background (grounded in real data)
2. **Psychographic Profile**: Attitudes, values, motivations
3. **Goals & Motivations**: What drives them (personal and professional)
4. **Pain Points & Frustrations**: Current problems and barriers
5. **Behaviors & Preferences**: How they work, decide, learn
6. **Technology Usage**: Tools, platforms, comfort level
7. **Product Needs**: What they need from your product

### 3. Make Personas Realistic

**Persona Realism**:
- Use real quotes from research participants
- Base demographics on actual data (not stereotypes)
- Include contradictions (people are complex)
- Show tradeoffs they make (e.g., "prefers feature X but willing to sacrifice for ease of use")

**Avoid Persona Pitfalls**:
- Don't create generic personas (too broad to be useful)
- Don't rely on assumptions without data
- Don't over-segment (3-5 personas max)
- Don't make personas too aspirational (who they are, not who they want to be)

### 4. Create Actionable Scenarios

**Day-in-the-Life Scenarios**:
- Show realistic workflow using your product
- Include triggers (what prompts them to use product)
- Demonstrate value delivered (how product helps them)
- Highlight friction points (where they struggle)

### 5. Validate and Update

**Persona Validation**:
- Share with stakeholders who interact with these users (sales, CS, support)
- Test against new research findings
- Update quarterly or when significant new data emerges
- Deprecate personas that no longer match user base

## Template

```markdown
# User Persona: [Name]

**Created**: [YYYY-MM-DD]
**Last Updated**: [YYYY-MM-DD]
**Based on**: [Research sources - e.g., "12 interviews, 200 survey responses, 6mo analytics"]

---

## At a Glance

**Photo/Image**: [Description - e.g., "Professional woman, 30s, at desk with dual monitors"]

**Tagline**: "[One sentence capturing essence - e.g., 'Data-driven sales leader balancing team growth with hitting quota']"

**Archetype**: [Type - e.g., "Power User" | "Beginner" | "Reluctant User" | "Champion"]

---

## Demographic Profile

**Name**: [First name - make it memorable]
**Age**: [Specific age or narrow range - e.g., "35-40"]
**Location**: [City/region if relevant - e.g., "San Francisco Bay Area"]
**Education**: [Highest degree - e.g., "Bachelor's in Business"]

### Professional

**Job Title**: [Specific title - e.g., "Sales Manager, Mid-Market"]
**Company**: [Type/size - e.g., "B2B SaaS startup, 150 employees, Series B"]
**Industry**: [Sector - e.g., "Marketing Technology"]
**Tenure**: [Years in role - e.g., "3 years as manager, 8 years in sales"]
**Team Size**: [If manages people - e.g., "Manages 8 SDRs and 4 AEs"]
**Reports to**: [Manager's role - e.g., "VP of Sales"]

### Personal

**Household**: [If relevant - e.g., "Married, 2 kids (ages 5, 8)"]
**Technical Proficiency**: 🟢 High | 🟡 Medium | 🔴 Low
**Preferred Devices**: [e.g., "MacBook Pro (work), iPhone"]

---

## Quote

> "[Representative quote from research that captures their mindset, frustration, or goal]"
>
> — [Source: Interview participant #7, Sales Manager at 120-person company]

**Alternative Quotes**:
> "[Another quote showing different facet]"

> "[Third quote if helpful]"

---

## Goals & Motivations

### Primary Goals (What they MUST achieve)

1. **[Goal 1]**: [Specific, measurable goal - e.g., "Hit 110% of quarterly quota"]
   - **Why it matters**: [Personal/professional reason]
   - **Current approach**: [How they try to achieve this today]
   - **Success metric**: [How they measure progress]

2. **[Goal 2]**: [Goal - e.g., "Develop team into top performers"]
   - **Why it matters**: [Reason]
   - **Current approach**: [Method]
   - **Success metric**: [Metric]

### Secondary Goals (Important but not critical)

3. **[Goal 3]**: [e.g., "Reduce time on reporting and admin tasks"]
4. **[Goal 4]**: [e.g., "Improve forecast accuracy"]

### Aspirational Goals (Long-term ambitions)

- [Long-term goal - e.g., "Become VP of Sales within 3 years"]
- [Career aspiration - e.g., "Build reputation as sales leader in industry"]

---

## Frustrations & Pain Points

### Critical Frustrations (Daily blockers)

1. **[Frustration 1]**: [Specific pain - e.g., "Salesforce data entry takes 2+ hours/day"]
   - **Impact**: [How this affects them - e.g., "Takes time away from coaching team"]
   - **Frequency**: [How often - e.g., "Daily, after every customer call"]
   - **Current workaround**: [What they do now - e.g., "Batch updates at end of day"]

2. **[Frustration 2]**: [Pain - e.g., "No visibility into pipeline health until weekly reports"]
   - **Impact**: [Effect]
   - **Frequency**: [How often]
   - **Current workaround**: [Workaround]

### Moderate Frustrations (Annoying but not dealbreakers)

3. **[Frustration 3]**: [e.g., "Manual forecast updates in Excel"]
4. **[Frustration 4]**: [e.g., "Inconsistent data quality from team"]

### Minor Frustrations (Nice to fix)

5. **[Frustration 5]**: [e.g., "Mobile app is slow"]

---

## Behaviors & Habits

### Daily Workflow

**Typical Day**:
```
7:00 AM  - Check email, review overnight activity
8:00 AM  - Team standup (15 min)
8:30 AM  - 1:1s with reps (rotating schedule)
10:00 AM - Customer calls (shadowing reps)
12:00 PM - Lunch, catch up on Slack
1:00 PM  - Deal reviews, pipeline analysis
3:00 PM  - Forecast updates in Salesforce + Excel
5:00 PM  - Leadership meeting (sales + marketing alignment)
6:00 PM  - Email, planning for next day
```

**Key Activities**:
- Spends 40% time coaching team
- Spends 30% time in meetings (leadership, customer calls)
- Spends 20% time on reporting/admin
- Spends 10% time on strategic planning

---

### Technology & Tools

**Current Tech Stack** (Daily use):
- **CRM**: Salesforce (mandatory, uses 60% of features)
- **Communication**: Slack, Zoom, Email
- **Productivity**: Google Calendar, Notion (for personal notes)
- **Analytics**: Looker dashboards (set up by ops team)
- **Other**: LinkedIn Sales Navigator, Gong (call recording)

**Technology Adoption Style**:
- 🟢 **Early adopter** for tools that save time
- Willing to pay for quality tools from personal budget
- Prefers integrations over standalone apps
- Values mobile access (reviews pipeline on commute)

**Learning Preferences**:
- Learns by doing (hates long tutorials)
- Asks colleagues before reading documentation
- Watches YouTube videos for complex features
- Expects tools to be intuitive

---

### Decision-Making Process

**How [Name] Evaluates Products**:

1. **Awareness**: Learns about new tools from peers, LinkedIn, sales outreach
2. **Research**:
   - Checks G2/Capterra reviews
   - Asks sales leader peers in Slack community
   - Watches demo video (won't sit through >5 min)
3. **Evaluation**:
   - **Must-haves**: Salesforce integration, mobile app, easy onboarding
   - **Deal-breakers**: Steep learning curve, poor mobile UX, no trial
   - **Budget**: Will pay $50-100/month personally, $500+/month needs VP approval
4. **Trial**: Expects free trial (14-30 days), will abandon if too complex
5. **Purchase**: Prefers annual billing (discount), needs approval for $5K+
6. **Adoption**: Needs quick wins in first week or will churn

**Influencers**:
- Peers in sales leader community (highest trust)
- VP of Sales (approval authority)
- Sales Ops team (technical vetting)

---

## Product Needs & Expectations

### Must-Have Features (Non-negotiable)

1. **[Feature 1]**: [e.g., "Real-time pipeline visibility dashboard"]
   - **Why critical**: [e.g., "Can't wait until weekly reports to course-correct"]
   - **Acceptable alternatives**: [If any]

2. **[Feature 2]**: [e.g., "Salesforce bi-directional sync"]
   - **Why critical**: [e.g., "Salesforce is mandated by company, can't maintain two systems"]

### Important Features (Strongly desired)

3. **[Feature 3]**: [e.g., "Automated activity tracking (calls, emails)"]
   - **Why important**: [e.g., "Eliminates data entry burden"]

4. **[Feature 4]**: [e.g., "Team coaching insights"]
   - **Why important**: [e.g., "Shows where reps need help"]

### Nice-to-Have Features (Differentiators)

5. **[Feature 5]**: [e.g., "AI-powered deal scoring"]
6. **[Feature 6]**: [e.g., "Customizable reports"]

---

## Non-Functional Requirements

**Performance Expectations**:
- Dashboards load in <2 seconds
- Mobile app works offline (airplane mode)
- Real-time sync (not 15-min delay)

**Usability Expectations**:
- Onboarding in <15 minutes
- No training required for basic features
- Clean, uncluttered interface

**Support Expectations**:
- Chat support (email too slow)
- Help docs with video tutorials
- Responsive support (<1 hour for urgent issues)

---

## Day-in-the-Life Scenario

### Scenario: Monday Morning Pipeline Review

**Context**: It's Monday 8:00 AM. [Name] arrives at office, needs to understand weekend activity and prepare for team standup.

**Step 1: Check Weekend Activity**
- Opens mobile app on commute
- Sees 3 new deals moved to "Closing" stage by reps
- Notices 1 large deal slipped to "On Hold" (uh oh)
- Gets alert: "2 deals at risk based on activity drop"

**Step 2: Deep Dive Before Standup**
- At desk, opens dashboard on laptop
- Filters pipeline by "This Quarter" + "At Risk"
- Sees that $250K deal (Acme Corp) had no activity for 5 days
- Pulls up activity timeline - last email was pricing discussion
- **Decision**: Will ask Sarah about Acme deal in standup

**Step 3: Team Standup**
- Shares screen showing pipeline view
- Highlights 3 deals closing this week (team motivation)
- Asks Sarah about Acme Corp
- Sarah explains: "Waiting on legal review, should close this week"
- **Action**: [Name] adds note to deal in CRM via mobile app

**Step 4: Forecast Update**
- After standup, updates forecast
- Product auto-suggests forecast based on deal stage + velocity
- [Name] adjusts 2 deals (insider knowledge from standup)
- Forecast updated in 5 minutes (vs 30 min manual Excel process)
- **Value**: Saves 25 minutes, forecast more accurate

**Outcome**:
- Started week with clear pipeline view
- Identified at-risk deal before it slipped further
- Updated forecast quickly
- **Time saved**: 45 minutes vs old process
- **Confidence**: High confidence going into week

---

## Metrics & Measurement

**How [Name] Measures Success** (with our product):

**Adoption Metrics**:
- Logs in daily (high engagement)
- Uses mobile app 3-4x/day
- Invites all 8 direct reports to platform

**Outcome Metrics**:
- Forecast accuracy improves from 70% → 85%
- Time on admin tasks reduces 40% (2hr/day → 1.2hr/day)
- Team quota attainment increases 15%

**Satisfaction Metrics**:
- NPS score: 9/10 (promoter)
- Renewal: Auto-renews annually
- Expansion: Upgrades to Team plan, adds CS module

---

## Jobs to Be Done

When [Name] uses our product, they're "hiring" it to:

### Functional Jobs
1. **[Job 1]**: "Help me understand pipeline health instantly"
   - **Desired outcome**: Know which deals need attention without manual analysis
2. **[Job 2]**: "Reduce time spent on manual reporting"
   - **Desired outcome**: Automated reports that VP trusts

### Emotional Jobs
3. **[Job 3]**: "Feel confident in my forecast"
   - **Desired outcome**: No surprises at end of quarter
4. **[Job 4]**: "Be seen as a data-driven leader"
   - **Desired outcome**: Impress VP with insights, get promoted

### Social Jobs
5. **[Job 5]**: "Help my team succeed"
   - **Desired outcome**: Reps hit quota, earn promotions

---

## Anti-Personas (What [Name] is NOT)

**Not**:
- Enterprise sales leader (500+ person sales org) - different needs at that scale
- Individual contributor / IC sales rep - less concerned with team management
- First-time manager - [Name] is experienced, needs advanced features

**Why this matters**: Helps us avoid building features for wrong audience

---

## Persona Segmentation

**How Common is [Name]?**:
- **% of user base**: 25% of users (2nd largest segment)
- **% of revenue**: 40% of ARR (high-value segment)
- **Growth**: Fastest-growing segment (+60% YoY)

**Prioritization**: 🔴 High Priority
- Large segment, high revenue, strong product-market fit

---

## Related Personas

**Primary Persona**: [Name] (Sales Manager) - You are here

**Secondary Personas**:
- **[Persona 2]**: [e.g., "Sarah" - Individual Sales Rep] - reports to [Name]
- **[Persona 3]**: [e.g., "Michael" - VP of Sales] - [Name]'s manager

**Persona Relationships**:
- [Name] influences [Persona 2] (team adoption)
- [Name] needs [Persona 3] approval for purchase
- [Name] collaborates with [Persona 4 - Sales Ops] on forecasting

---

## Competitive Positioning

**What [Name] Uses Today** (Competitors):
- **Current solution**: Salesforce + Excel + Looker (painful, manual)
- **Tried before**: HubSpot (too simple), Clari (too expensive, overkill)
- **Competitors considered**: Gong (call intelligence focus), People.ai (too complex)

**Why [Name] Chooses Us**:
- Right balance of power and simplicity
- Better Salesforce integration than competitors
- More affordable than enterprise solutions
- Mobile-first experience (competitors neglect mobile)

---

## Quote Library (from Research)

> "I spend 2 hours a day updating Salesforce. It's soul-crushing."
> — Interview Participant #3

> "I need to see pipeline health in real-time, not wait for weekly reports."
> — Survey Response #147

> "If a tool doesn't work on mobile, I won't use it. I'm always on the go."
> — Interview Participant #7

> "My VP doesn't trust my Excel forecasts. I need something more professional."
> — Interview Participant #11

---

## Updates & Version History

### v1.0 (2025-01-18)
- Initial persona creation based on 12 interviews, 200 survey responses

### [Future updates]
- Track changes as new research emerges
- Note when persona needs refresh (quarterly review)

```

---

## Best Practices

### DO ✅

- **Base on real research** - Use actual user interviews, surveys, and data
- **Use real quotes** - Direct quotes from research participants
- **Make it specific** - "Sarah, 37" beats "Sales Manager, 35-45"
- **Include contradictions** - People are complex (e.g., "values speed but wants thorough analysis")
- **Show behaviors, not just demographics** - How they work matters more than age
- **Create scenarios** - Day-in-the-life stories bring personas to life
- **Update regularly** - Personas go stale, refresh quarterly
- **Limit quantity** - 3-5 personas max (more = less useful)

### DON'T ❌

- **Don't rely on assumptions** - "I think users are like this" without data
- **Don't use stereotypes** - Avoid gender, age, or cultural stereotypes
- **Don't make them too generic** - "Tech-savvy millennial" is useless
- **Don't skip validation** - Share with sales, CS, support who know these users
- **Don't create aspirational personas** - Document who they ARE, not who they want to be
- **Don't over-segment** - Too many personas = no clear focus
- **Don't forget to use them** - Personas in a drawer help no one
- **Don't make them static** - Users evolve, personas must too

---

## Examples

### Example 1: B2B SaaS Sales Manager Persona

**Input**: "Create persona for mid-market sales manager using our CRM"

**Output**: [See full template above - "Sarah Chen, Sales Manager" example]

---

### Example 2: B2C Mobile App User Persona

**Input**: "Create persona for busy parent using grocery delivery app"

**Output**:

```markdown
# User Persona: Jessica Martinez

**Created**: 2025-01-18
**Based on**: 20 user interviews, 500 app reviews, 12mo analytics

---

## At a Glance

**Photo**: Working mom, mid-30s, kitchen background, smartphone in hand

**Tagline**: "Busy working parent juggling career, kids, and household management"

**Archetype**: Convenience Seeker

---

## Demographic Profile

**Name**: Jessica Martinez
**Age**: 36
**Location**: Suburban Austin, TX
**Education**: Master's in Marketing

### Professional

**Job Title**: Marketing Director, Tech Startup
**Company**: 80-person B2B SaaS company
**Work Schedule**: 8 AM - 5 PM, occasional evenings
**Commute**: 25 minutes (drives)

### Personal

**Household**: Married, 2 kids (ages 4, 7)
**Technical Proficiency**: 🟢 High (works in tech)
**Devices**: iPhone 15, MacBook (work), iPad (kids)

---

## Quote

> "I don't have time to go to the grocery store. If I can save 2 hours a week, that's 2 hours with my kids."

---

## Goals

1. **Balance work and family** without sacrificing either
2. **Minimize time on chores** (grocery shopping, meal prep)
3. **Feed family healthy meals** despite busy schedule

---

## Frustrations

1. **Grocery shopping takes 2+ hours** (drive, shop, checkout, unload)
   - **Impact**: Eats into weekend family time
   - **Current workaround**: Husband does shopping, but he forgets items

2. **Meal planning is mental load** (what to cook, do we have ingredients)
   - **Impact**: Stress, decision fatigue
   - **Current workaround**: Orders takeout 3x/week (expensive, unhealthy)

---

## Behaviors

**Daily Workflow**:
- 6:30 AM: Wake kids, breakfast, school drop-off
- 8 AM - 5 PM: Work (meetings, strategic planning)
- 5:30 PM: Pick up kids, dinner prep
- 8 PM: Kids bedtime
- 8:30 PM: Personal time (Netflix, plan next day)

**Technology**:
- Uses phone for everything (orders groceries during commute)
- Saves favorite items for easy reordering
- Uses Apple Pay (hates entering credit card)

---

## Product Needs

**Must-Have**:
1. **Fast checkout** (<2 min to complete order)
2. **Accurate delivery** (no substitutions without asking)
3. **Same-day delivery** (order at lunch, arrives by dinner)

**Important**:
4. **Meal planning integration** (suggest recipes based on items)
5. **Reorder favorites** (repeat last week's order in 1 tap)

**Nice-to-Have**:
6. **Family sharing** (husband can add items to cart)

---

## Scenario: Tuesday Evening Grocery Order

**6:45 PM**: Kids in car, driving home from soccer practice. Realizes fridge is empty.

**Action**: Opens app on iPhone
- Taps "Reorder Last Week"
- Adds milk (ran out), removes avocados (still have some)
- App suggests: "You usually buy strawberries on Tuesdays" → Adds to cart
- Checkout with Face ID (Apple Pay)
- Total time: 90 seconds

**Outcome**:
- Groceries arrive at 8 PM (before bedtime)
- Saved 2 hours vs in-store shopping
- **Value**: More time reading bedtime stories to kids
```

---

## Model

Use: Sonnet

---

## Related

- `/customer-insights:journey-map` - Map customer journey for this persona
- `/user-research:interview-guide` - Create interview guide to research persona
- `/user-research:research-synthesize` - Synthesize research into personas
- `/requirements-engineering:user-stories` - Write user stories for this persona
- `/customer-insights:research-to-product` - Research-to-persona-to-roadmap workflow
- `user-researcher` agent - Research methodology and persona development
- `customer-insights` agent - Analyze customer data for persona creation
