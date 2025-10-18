---
name: Portfolio Optimization Workflow
description: Strategic review and optimization of product portfolio
category: Strategic Planning
duration: 4-6 weeks
model: sonnet
---

# Portfolio Optimization Workflow

Systematic process for evaluating, prioritizing, and optimizing a multi-product or multi-feature portfolio for maximum strategic impact.

## Usage
```
/portfolio-optimization
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Portfolio scope (multiple products, product lines, or feature areas)
- Number of items in portfolio
- Current portfolio performance (which are winning/losing)
- Strategic goals (growth, profitability, market share, innovation)
- Resource constraints (budget, team capacity)
- Timeline and urgency for optimization

## Timeline: 4-6 Weeks

## Phase 1: Portfolio Assessment (Week 1-2)

### Week 1: Inventory & Analysis
```
Task: product-ops agent
Create comprehensive product portfolio inventory:
- List all products, features, and initiatives
- Current status (active, maintenance, sunset planned)
- Resources allocated (team, budget)
- Strategic rationale for each
- Interdependencies
Create portfolio inventory matrix
```

```
Task: data-scientist agent
Analyze performance of each portfolio item:
- Usage and engagement metrics
- Revenue contribution
- Customer adoption rates
- Growth trends (up, flat, declining)
- Customer satisfaction (NPS per product)
- Development and maintenance costs
Create portfolio performance scorecard
```

```
Task: customer-insights agent
Analyze customer feedback by product:
- Support ticket volume and severity
- Feature requests and gaps
- Customer sentiment
- Churn reasons
- Competitive pressures
Create customer feedback analysis
```

### Week 2: Strategic Evaluation
```
Task: product-strategist agent
Evaluate portfolio against strategy:
- Strategic alignment with vision
- Market opportunity for each
- Competitive positioning
- Cannibalization analysis
- Portfolio coherence
- Resource efficiency
Use product-strategy-frameworks skill
```

```
Command: /pm:swot-analysis
Context: Overall product portfolio
Identify portfolio-level strengths, weaknesses, opportunities, threats
```

```
Task: competitive-analyst agent
Assess competitive landscape by product:
- Market share and positioning
- Competitive threats
- Market trends and dynamics
- White space opportunities
- Portfolio gaps vs. competitors
```

## Phase 2: Portfolio Prioritization (Week 3)

### Scoring & Ranking
```
Task: feature-prioritizer agent
Score each portfolio item using multiple frameworks:
- RICE scoring (Reach, Impact, Confidence, Effort)
- Strategic importance (1-5 scale)
- Revenue contribution (current and potential)
- Resource requirements
- Risk assessment
Create comprehensive portfolio scoring
```

```
Task: monetization-expert agent
Analyze portfolio economics:
- Revenue by product/feature
- Profit margins
- Customer acquisition cost by product
- Lifetime value by product
- Unit economics
- Cross-sell and upsell patterns
Create portfolio economics analysis
```

### Portfolio Matrix
```
Task: product-strategist agent
Plot portfolio on strategic matrix:

Axis 1: Strategic Importance (Low → High)
Axis 2: Performance/Success (Low → High)

Quadrants:
- **Stars** (High importance, High performance): Invest
- **Question Marks** (High importance, Low performance): Fix or kill
- **Cash Cows** (Low importance, High performance): Harvest
- **Dogs** (Low importance, Low performance): Sunset

Create visual portfolio matrix with recommendations
```

## Phase 3: Optimization Strategy (Week 4)

### Investment Decisions
```
Task: product-strategist agent
Develop investment strategy for each quadrant:

**Stars (Invest & Grow)**
- Increase resources
- Accelerate roadmap
- Expand market
- Add capabilities

**Question Marks (Fix or Kill)**
- Diagnose root issues
- Give 1-2 quarters to improve
- Clear success criteria
- Sunset if can't improve

**Cash Cows (Harvest & Maintain)**
- Reduce investment
- Maximize revenue extraction
- Minimal feature work
- Eventual sunset planning

**Dogs (Sunset)**
- Create sunset plan
- Minimize new investment
- Customer migration strategy
- Resource reallocation

Create portfolio investment strategy
```

```
Task: technical-pm agent
Assess technical debt across portfolio:
- Technical health by product
- Debt accumulation trends
- Platform consolidation opportunities
- Architecture simplification potential
- Shared services opportunities
Create technical portfolio optimization plan
```

### Resource Reallocation
```
Task: product-ops agent
Plan resource reallocation:
- Teams to reduce or reallocate
- Teams to expand
- Skills gaps and hiring needs
- Budget redistribution
- Timeline for changes
Create resource reallocation plan
```

```
Command: /pm:capacity-planner
Context: Optimized portfolio allocation
Plan capacity across products and initiatives
```

## Phase 4: Sunset & Migration Planning (Week 5)

### Products to Sunset
```
Task: product-ops agent
For each product/feature to sunset, create plan:
- Deprecation timeline (typically 6-12 months)
- Customer notification strategy
- Migration path to alternative
- Data export and portability
- Support wind-down
- Legal and compliance considerations
Create sunset playbook for each item
```

```
Command: /pm:sunset-product (use workflow when available)
For each product being sunset
Create detailed sunset plan
```

```
Task: customer-success agent
Customer migration strategy:
- Segment impacted customers
- Identify alternative solutions (internal or external)
- Migration assistance plan
- Retention offers if applicable
- Communication timeline and templates
- Success team support plan
```

### Communication Planning
```
Task: stakeholder-manager agent
Develop comprehensive communication plan:
- Internal announcements (teams, executives, company)
- Customer communications (timeline, alternatives, support)
- Partner notifications
- Public statements if applicable
- FAQ and talking points
Create portfolio change communication plan
```

```
Command: /pm:communication-plan
Initiative: Portfolio optimization changes
Create detailed stakeholder communication plan
```

## Phase 5: Roadmap Realignment (Week 6)

### Updated Portfolio Roadmap
```
Command: /pm:roadmap-builder
Timeframe: 12 months
Create optimized portfolio roadmap:
- Invest products: Accelerated roadmaps
- Fix products: Improvement initiatives
- Harvest products: Maintenance mode
- Sunset products: Wind-down timeline
Show resource allocation and priorities
```

```
Task: product-strategist agent
Align portfolio roadmap to strategy:
- Ensure stars get resources needed
- Question marks have clear improvement path
- Cash cows in maintenance mode
- Dogs being sunset efficiently
- Overall portfolio coherence
- Strategic balance (growth, retention, efficiency)
```

### OKR Alignment
```
Command: /pm:okr-framework
Create portfolio-level OKRs for next quarter:
- Growth objectives for star products
- Fix objectives for question marks
- Efficiency objectives for optimization
- Sunset objectives with clear timelines
```

```
Task: agile-coach agent
Cascade portfolio strategy to teams:
- Team-level OKRs aligned to portfolio strategy
- Sprint planning aligned to new priorities
- Sunset of deprecated work
- Excitement for new focus areas
Facilitate portfolio planning workshops
```

## Phase 6: Execution & Monitoring (Ongoing)

### Implementation
```
Task: product-ops agent
Track portfolio optimization execution:
- Resource reallocation progress
- Sunset plans on track
- Investment in stars delivering results
- Question marks showing improvement
- Communication milestones met
Create weekly/monthly progress reports
```

### Performance Monitoring
```
Task: data-scientist agent
Monitor portfolio optimization impact:
- Overall portfolio metrics improving
- Resource efficiency gains
- Revenue concentration or diversification
- Customer satisfaction trends
- Team velocity and morale
Create portfolio health dashboard
```

```
Task: product-strategist agent
Quarterly portfolio reviews:
- Review performance vs. expectations
- Reassess priorities
- Adjust investment levels
- New opportunities to add
- Continued optimization
Make portfolio a living, evolving strategy
```

## Deliverables

1. **Portfolio Inventory** - Complete list with status and metrics
2. **Performance Scorecard** - Metrics and analysis by product
3. **Portfolio Matrix** - Strategic quadrant mapping
4. **Investment Strategy** - Resource allocation plan
5. **Sunset Plans** - For products being discontinued
6. **Migration Strategy** - Customer transition plans
7. **Optimized Roadmap** - Realigned portfolio roadmap
8. **Communication Plan** - Internal and external messaging

## Success Metrics (6-12 months)
- Resource concentration on strategic products (>70% on stars)
- Improved overall portfolio performance
- Increased revenue per product team member
- Reduced technical debt
- Higher customer satisfaction (NPS improvement)
- Clearer strategic focus
- Team clarity and morale improvement

## Portfolio Optimization Triggers
Run this workflow when:
- Annual or semi-annual strategic planning
- Too many products/features to maintain
- Resource constraints
- Strategic shift or market change
- Performance plateaus
- Team fragmentation or confusion
- Excessive technical debt
- Customer feedback about product sprawl

## Common Portfolio Problems
- **Peanut butter spread**: Resources too thin
- **Zombie products**: Dead products consuming resources
- **Shiny object syndrome**: Chasing too many opportunities
- **Legacy burden**: Old products holding back innovation
- **Unclear strategy**: No coherent portfolio vision
- **Analysis paralysis**: Never sunsetting anything
