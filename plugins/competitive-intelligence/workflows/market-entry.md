---
description: Strategic workflow for entering new markets or segments
category: Strategic Growth
duration: 8-12 weeks
model: sonnet
---

# Market Entry Workflow

Comprehensive process for evaluating, planning, and executing entry into new markets, geographies, or customer segments.

## Usage
```
/market-entry [market, geography, or segment description]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Target market, geography, or segment (e.g., "enterprise market", "European market", "healthcare vertical")
- Current market position and presence
- Why now (opportunity, competitive pressure, strategic imperative)
- Expected market size and potential
- Resources available for entry
- Timeline and milestones

## Timeline: 8-12 Weeks

## Phase 1: Market Assessment (Week 1-3)

### Week 1: Market Research
```
Task: competitive-analyst agent
Conduct comprehensive market analysis:
- Market size and growth (TAM, SAM, SOM)
- Market trends and drivers
- Regulatory environment
- Economic and cultural factors
- Technology adoption patterns
Create market opportunity assessment
```

```
Command: /competitive-intelligence:market-sizing
Target: [new market/segment/geography]
Calculate TAM, SAM, SOM with methodology
```

```
Task: competitive-analyst agent
Analyze competitive landscape:
- Existing competitors in market
- Market leaders and share
- Competitive positioning
- Barriers to entry
- White space opportunities
Use Porter's Five Forces framework
```

### Week 2: Customer Discovery
```
Task: user-researcher agent
Conduct customer research in new market:
- 15-20 customer interviews
- Understand jobs-to-be-done
- Identify pain points and needs
- Current solutions and alternatives
- Willingness to pay
- Decision-making process
Use jobs-to-be-done skill
```

```
Command: /customer-insights:persona-creator
Context: New market segment
Create 2-3 personas for target market
```

```
Task: customer-insights agent
Analyze market-specific customer needs:
- Synthesize interview findings
- Identify unique needs vs. existing markets
- Cultural or regional considerations
- Buying behaviors and preferences
Create customer insights report
```

### Week 3: Strategic Analysis
```
Task: product-strategist agent
Evaluate strategic fit and opportunity:
- Alignment with company vision
- Competitive advantage potential
- Resource requirements
- Risk assessment
- Expected returns and timeline
Use SWOT and strategic frameworks
```

```
Command: /competitive-intelligence:swot-analysis
Context: Market entry for [target market]
```

```
Task: product-strategist agent
Make go/no-go recommendation:
- Business case summary
- Investment required
- Expected outcomes
- Key risks and mitigations
- Success criteria
- Timeline to profitability
Create market entry business case
```

## Phase 2: Product-Market Fit Strategy (Week 4-6)

### Week 4: Product Adaptation
```
Task: requirements-engineer agent
Assess product requirements for new market:
- Core features needed (table stakes)
- Market-specific features required
- Features to remove or modify
- Localization requirements
- Compliance and regulatory needs
Create market-specific product requirements
```

```
Task: technical-pm agent
Evaluate technical considerations:
- Architecture changes needed
- Data residency and privacy
- Integration requirements
- Performance and scale
- Infrastructure and hosting
Create technical feasibility assessment
```

### Week 5: Positioning & Messaging
```
Task: gtm-planner agent
Develop market-specific positioning:
- Value proposition for new market
- Competitive differentiation
- Messaging and narrative
- Use cases and proof points
- Brand adaptation if needed
Use product-positioning skill
```

```
Command: /competitive-intelligence:value-proposition-canvas
Target: [new market segment]
Map customer jobs, pains, gains and product fit
```

### Week 6: Pricing & Packaging
```
Task: monetization-expert agent
Design pricing and packaging strategy:
- Competitive pricing analysis
- Willingness to pay research
- Pricing model selection
- Package differentiation
- Discounting strategy
- Currency and payment considerations
Use pricing-packaging skill
```

```
Command: /competitive-intelligence:competitive-positioning
Compare pricing and positioning vs. local competitors
```

## Phase 3: Go-to-Market Planning (Week 7-9)

### Week 7: GTM Strategy
```
Task: gtm-planner agent
Develop comprehensive go-to-market plan:
- Market entry strategy (land & expand, full launch, pilot)
- Customer acquisition strategy
- Channel strategy (direct, partners, resellers)
- Sales and marketing approach
- Customer success model
Create GTM strategy document
```

```
Command: /gtm-strategy:gtm-plan
Product: [existing product]
Target: [new market]
Create detailed go-to-market plan
```

### Week 8: Marketing & Sales Enablement
```
Task: gtm-planner agent
Create marketing and sales assets:
- Market-specific website content
- Sales decks and demos
- Case studies and proof points
- Marketing collateral
- Sales playbooks
- Objection handling
```

```
Command: /product-operations:one-pager
Audience: [new market prospects]
Create compelling one-page overview
```

```
Task: customer-success agent
Design onboarding for new market:
- Market-specific onboarding flow
- Educational content
- Support resources
- Success milestones
- Expansion strategy
```

### Week 9: Partnership & Channel Strategy
```
Task: stakeholder-manager agent
Identify and evaluate potential partners:
- Local partners and resellers
- Technology integration partners
- Distribution channel partners
- Strategic alliances
- Community and ecosystem players
Create partnership strategy
```

## Phase 4: Pilot & Validation (Week 10-11)

### Week 10: Pilot Program
```
Task: discovery-facilitator agent
Launch pilot program in new market:
- Recruit 5-10 pilot customers
- Limited feature set or beta
- Intensive support and feedback
- Rapid iteration based on learnings
- Document product-market fit signals
Reference product-market-fit skill
```

```
Command: /gtm-strategy:beta-program
Design beta program structure for market entry
```

### Week 11: Validation & Iteration
```
Task: data-scientist agent
Analyze pilot program results:
- Usage and engagement metrics
- Conversion and activation rates
- Customer feedback and NPS
- Revenue and unit economics
- Retention signals
Create pilot results analysis
```

```
Task: user-researcher agent
Conduct pilot customer interviews:
- Satisfaction and value delivered
- Feature gaps and needs
- Pricing perception
- Competitive comparison
- Willingness to recommend
Synthesize feedback for product improvements
```

## Phase 5: Launch Preparation (Week 12)

### Launch Readiness
```
Task: product-ops agent
Validate launch readiness:
- Product completeness checklist
- Technical infrastructure ready
- Support and success team trained
- Marketing materials complete
- Sales team enabled
- Legal and compliance approved
- Partnerships activated
Create launch readiness scorecard
```

```
Command: /gtm-strategy:release-planner
Target: Market entry launch
Coordinate all launch activities
```

### Communication & Launch
```
Task: gtm-planner agent
Execute launch communications:
- Press and media outreach
- Customer announcements
- Partner communications
- Internal launch celebration
- Social media and content
- Analyst briefings (if applicable)
```

```
Command: /gtm-strategy:communication-plan
Initiative: [Market] entry launch
Create comprehensive communication plan
```

## Post-Launch (Ongoing)

### Monitor & Optimize
```
Task: growth-pm agent
Track market entry performance:
- Customer acquisition metrics
- Activation and onboarding success
- Revenue and pipeline growth
- Market penetration rate
- Competitive win rates
Create weekly/monthly dashboards
```

```
Task: customer-insights agent
Continuous customer feedback:
- Regular customer interviews
- NPS and satisfaction tracking
- Feature request analysis
- Churn analysis and prevention
Create monthly insights reports
```

## Deliverables

1. **Market Assessment Report** - Size, opportunity, competition
2. **Customer Research Insights** - Personas, needs, JTBD
3. **Business Case** - Investment, returns, risks
4. **Product Requirements** - Market-specific features
5. **GTM Strategy** - Positioning, pricing, channels
6. **Launch Plan** - Timeline, activities, success metrics
7. **Pilot Results** - Validation and learnings
8. **Performance Dashboard** - Ongoing tracking

## Success Metrics
- Market opportunity validated (TAM/SAM)
- Pilot program success (NPS >40, retention >60%)
- Initial customer acquisition (10-50 customers)
- Product-market fit signals (qualitative and quantitative)
- Revenue targets hit (quarters 2-4)
- Unit economics validated (LTV:CAC >3)

## Risk Mitigation
- Start with pilot to validate assumptions
- Limit initial investment until validation
- Build market-specific expertise on team
- Establish local partnerships
- Plan for cultural and regulatory differences
- Set clear success criteria and exit conditions
