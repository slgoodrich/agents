---
description: Comprehensive annual strategic planning process
category: Strategic Planning
duration: 6-8 weeks
model: sonnet
---

# Annual Planning Workflow

Complete annual strategic planning including vision refresh, annual OKRs, roadmap, and resource allocation.

## Usage
```
/annual-planning [year, e.g., "FY2026" or "2026"]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Which year/fiscal year (FY2026, 2026, etc.)
- Current company state (ARR, team size, market position)
- Previous year performance (goals achieved, growth rate, key challenges)
- Strategic priorities or focus areas for the year
- Board expectations or investor commitments
- Major initiatives or bets being considered

## Timeline: 6-8 Weeks

## Phase 1: Strategic Review (Week 1-2)
**Reflect on past year and market landscape**

### Week 1: Performance Analysis
```
Task: data-scientist agent
Analyze previous year's performance:
- Review all key metrics vs. targets
- Cohort analysis and trends
- Revenue and growth analysis
- User retention and engagement
- Feature adoption rates
Create comprehensive annual performance report
```

```
Task: competitive-analyst agent
Conduct market and competitive review:
- Market trends and shifts
- Competitive landscape changes
- New entrants and threats
- Technology evolution
- Customer segment changes
Prepare competitive landscape report
```

### Week 2: Strategic Assessment
```
Task: product-strategist agent
Using SWOT and strategic frameworks:
- Analyze Strengths, Weaknesses, Opportunities, Threats
- Assess competitive positioning
- Identify strategic opportunities
- Review product-market fit
- Evaluate portfolio performance
Create strategic assessment document
```

```
Command: /stakeholder-management:stakeholder-mapper
Map key stakeholders for annual planning:
- Executive team
- Board members
- Department heads
- Key customers
- Partners
```

## Phase 2: Vision & Strategy (Week 3-4)

### Week 3: Vision Refresh
```
Task: product-strategist agent
Refresh or evolve product vision:
- Review current vision (3-5 year)
- Assess if vision needs evolution
- Articulate aspirational future state
- Define customer-focused direction
- Create compelling vision statement
Reference vision-mission-strategy skill
```

```
Task: platform-architect agent (if applicable)
Assess platform and ecosystem strategy:
- Platform maturity evaluation
- Ecosystem opportunities
- Technology evolution roadmap
- Build vs. buy decisions
Create platform strategy document
```

### Week 4: Strategic Priorities
```
Task: product-strategist agent
Define annual strategic priorities:
- Top 3-5 strategic themes
- Market positioning strategy
- Competitive differentiation
- Key initiatives alignment
- Success criteria for each theme
Use product-strategy-frameworks skill
```

```
Command: /competitive-intelligence:swot-analysis
Context: [annual planning, strategic priorities]
Create comprehensive SWOT analysis
```

## Phase 3: OKR Development (Week 5)

### Annual OKRs
```
Task: product-strategist agent with okr-methodology skill
Develop annual company/product OKRs:
- 3-5 Objectives (inspirational, qualitative)
- 3-5 Key Results per Objective (measurable)
- Ensure alignment with vision
- Set ambitious but achievable targets
- Define quarterly breakdown
Create annual OKR document
```

```
Task: agile-coach agent
Facilitate OKR cascading workshop:
- Company OKRs → Product OKRs
- Product OKRs → Team OKRs
- Ensure vertical alignment
- Check horizontal dependencies
- Validate feasibility with teams
```

```
Command: /stakeholder-management:alignment-session
Topic: Annual OKRs and strategic priorities
Stakeholders: Leadership team, department heads
```

## Phase 4: Roadmap Planning (Week 6-7)

### Week 6: Opportunity Identification
```
Task: discovery-facilitator agent
Synthesize opportunities from multiple sources:
- Customer research insights
- Market opportunities
- Technical opportunities
- Strategic initiatives
- Innovation ideas
Create opportunity map with sizing and prioritization
```

```
Task: feature-prioritizer agent
Prioritize major initiatives for the year:
- Use RICE scoring for annual themes
- Consider strategic alignment
- Resource requirements assessment
- Dependencies and sequencing
- Risk evaluation
Create prioritized initiative list
```

### Week 7: Annual Roadmap
```
Command: /strategic-planning:roadmap-builder
Timeframe: Annual (4 quarters)
Create comprehensive annual roadmap:
- Q1-Q4 major themes and initiatives
- Now/Next/Later structure
- Dependencies and milestones
- Resource allocation by quarter
- Confidence levels
```

```
Task: technical-pm agent
Technical roadmap and architecture alignment:
- Technical debt priorities
- Infrastructure investments
- Platform capabilities
- Security and compliance
- Technology upgrades
Ensure tech roadmap supports product roadmap
```

## Phase 5: Resource Planning (Week 7-8)

### Resource Allocation
```
Task: product-ops agent
Annual resource and capacity planning:
- Team sizing and headcount
- Skills and hiring needs
- Budget allocation by initiative
- Tools and infrastructure costs
- Vendor and partner requirements
Create annual resource plan
```

```
Command: /agile-coaching:capacity-planner
Context: Annual roadmap, team composition
Plan capacity across 4 quarters
```

### Financial Planning
```
Task: monetization-expert agent (if applicable)
Annual revenue and monetization planning:
- Revenue targets by quarter
- Pricing and packaging evolution
- New monetization opportunities
- Customer lifetime value goals
- Unit economics improvement
Create annual revenue plan
```

## Phase 6: Communication & Alignment (Week 8)

### Executive Alignment
```
Command: /strategic-planning:executive-summary
Summarize annual plan for leadership:
- Vision and strategic priorities
- Annual OKRs
- Roadmap highlights
- Resource requirements
- Success metrics and milestones
```

```
Task: stakeholder-manager agent
Create comprehensive communication plan:
- Internal announcements (all-hands, department meetings)
- External communications (customers, partners)
- Ongoing progress updates
- Quarterly review cadence
- Stakeholder-specific messaging
```

### Team Kickoff
```
Command: /product-operations:meeting-agenda
Purpose: Annual planning kickoff
Participants: Full product and engineering teams
Content: Vision, strategy, OKRs, roadmap, expectations
```

```
Task: agile-coach agent
Facilitate annual planning kickoff:
- Share vision and strategy
- Present annual OKRs
- Walk through roadmap
- Clarify roles and responsibilities
- Q&A and team input
- Generate excitement and alignment
```

## Deliverables

1. **Annual Performance Report** - Previous year analysis
2. **Strategic Assessment** - SWOT and market analysis
3. **Vision Statement** - Refreshed 3-5 year vision
4. **Strategic Priorities** - Top 3-5 themes for the year
5. **Annual OKRs** - Company and product objectives
6. **Annual Roadmap** - Quarterly initiative plan
7. **Resource Plan** - Budget, headcount, capacity
8. **Communication Plan** - Stakeholder engagement strategy

## Success Metrics
- Leadership alignment on vision and strategy
- OKRs cascaded to all teams
- Roadmap buy-in from stakeholders
- Resource allocation approved
- Team understanding and engagement
- Clear quarterly execution plan

## Quarterly Checkpoints
- Q1 Review: Progress on annual OKRs, roadmap adjustments
- Q2 Review: Mid-year assessment, pivot if needed
- Q3 Review: Momentum check, Q4 planning
- Q4 Review: Annual results, next year preparation
