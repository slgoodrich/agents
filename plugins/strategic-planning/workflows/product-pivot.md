---
description: Strategic process for evaluating and executing a product pivot
category: Strategic Transformation
duration: 6-10 weeks
model: sonnet
---

# Product Pivot Workflow

Comprehensive framework for recognizing when to pivot, choosing the right pivot type, and executing the transition successfully.

## Usage
```
/product-pivot [optional: pivot context or concerns]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Current product and market position
- Why considering pivot (lack of traction, market feedback, competitive pressure, strategic shift)
- Metrics showing need for change (growth stalling, churn high, low engagement)
- Type of pivot being considered (customer segment, value proposition, technology, business model)
- Resources and runway available
- Team and stakeholder alignment on need for change

## Timeline: 6-10 Weeks

## Phase 1: Pivot Recognition & Decision (Week 1-2)

### Week 1: Situation Assessment
```
Task: product-strategist agent
Assess current product situation:
- Review key metrics and trends
- Customer retention and churn analysis
- Revenue growth or decline
- Market feedback and signals
- Competitive dynamics
- Team morale and efficiency
Create honest situation assessment
```

```
Task: data-scientist agent
Analyze product-market fit signals:
- Sean Ellis PMF survey (if >40% very disappointed)
- Retention curves by cohort
- NPS and customer satisfaction
- Activation and engagement trends
- Revenue metrics and unit economics
Reference product-market-fit skill
```

```
Task: customer-insights agent
Synthesize customer feedback:
- Support tickets and complaints
- Sales loss reasons
- Feature requests and gaps
- Competitor migrations
- User interviews (recent 20)
Identify patterns and root causes
```

### Week 2: Pivot Evaluation
```
Task: product-strategist agent
Evaluate need for pivot:
- Is current strategy working?
- Are metrics improving or declining?
- Is market responding?
- Are we solving the right problem?
- Do we have enough runway?
- What are alternatives to pivot?
Make pivot recommendation (yes/no/continue monitoring)
```

```
Task: product-strategist agent
If pivot recommended, identify pivot type:
1. Zoom-in pivot (feature becomes product)
2. Zoom-out pivot (product becomes feature)
3. Customer segment pivot (different target)
4. Customer need pivot (different problem)
5. Platform pivot (app to platform or reverse)
6. Value capture pivot (different monetization)
7. Engine of growth pivot (different acquisition)
Reference lean-product-development skill for pivot types
```

```
Command: /strategic-planning:scenario-planner
Create scenarios for:
- Continue current path
- Each potential pivot option
- Shut down option
Compare outcomes and risks
```

## Phase 2: Pivot Strategy Development (Week 3-4)

### Week 3: Opportunity Validation
```
Task: user-researcher agent
Validate new direction with customers:
- 20-30 customer interviews
- Test new value proposition
- Understand target segment needs
- Assess willingness to pay
- Gauge market interest
Use jobs-to-be-done and continuous-discovery skills
```

```
Task: competitive-analyst agent
Assess new competitive landscape:
- Who are competitors in new direction?
- What's their positioning?
- Where are gaps and opportunities?
- What's our differentiation?
- Market size and growth
Use Porter's Five Forces and competitive frameworks
```

```
Command: /competitive-intelligence:market-sizing
Target: [new pivot direction]
Calculate opportunity size
```

### Week 4: Pivot Strategy
```
Task: product-strategist agent
Define comprehensive pivot strategy:
- New vision and mission
- Target customer segment
- Value proposition
- Product positioning
- Competitive differentiation
- Go-to-market approach
Reference vision-mission-strategy and product-positioning skills
```

```
Command: /competitive-intelligence:value-proposition-canvas
Target: New customer segment/need
Map new value proposition
```

```
Task: product-strategist agent
Create pivot roadmap:
- What changes to product?
- What stays the same?
- Build, keep, sunset decisions
- Timeline for transition
- Resource requirements
- Risks and mitigations
```

## Phase 3: Product Redefinition (Week 5-6)

### Week 5: Product Strategy
```
Task: requirements-engineer agent
Define new product requirements:
- Core features for new direction
- Features to sunset or deprecate
- New features to build
- Technical debt to address
- MVP for pivot direction
Create pivot product requirements document
```

```
Command: /continuous-discovery:mvp-scoper
Context: Pivot to [new direction]
Define minimum viable product for pivot
```

```
Task: technical-pm agent
Technical assessment and planning:
- Architecture changes needed
- Technical debt implications
- Migration requirements
- Data model changes
- Infrastructure needs
Create technical pivot plan
```

### Week 6: Experience Design
```
Task: discovery-facilitator agent
Design new user experience:
- User flows for new use cases
- Onboarding for pivot direction
- Feature prioritization
- UI/UX changes needed
- Customer migration path
```

```
Command: /customer-insights:journey-mapper
Customer: [new target segment]
Map new customer journey
```

## Phase 4: Transition Planning (Week 7-8)

### Week 7: Customer Transition
```
Task: customer-success agent
Plan customer transition strategy:
- Segment existing customers (pivot with us vs. won't)
- Migration communication plan
- Support and hand-holding
- Deprecation timeline for old features
- Grandfathering decisions
- Refund/credit policies if applicable
```

```
Task: stakeholder-manager agent
Stakeholder communication strategy:
- Internal team communication
- Investor update
- Board presentation
- Customer announcements
- Partner notifications
- Public messaging (if applicable)
Create comprehensive communication plan
```

```
Command: /gtm-strategy:communication-plan
Initiative: Product pivot
Create detailed communication strategy
```

### Week 8: Go-to-Market Reset
```
Task: gtm-planner agent
Redesign go-to-market strategy:
- New positioning and messaging
- Pricing and packaging for pivot
- Sales and marketing approach
- Channel strategy
- Customer acquisition plan
- Brand evolution if needed
Reference go-to-market-playbooks skill
```

```
Command: /gtm-strategy:gtm-plan
Product: [pivoted product]
Target: [new segment]
Create new GTM strategy
```

```
Task: monetization-expert agent
Redesign monetization:
- New pricing strategy
- Packaging for new use cases
- Migration pricing for existing customers
- Revenue model changes
- Unit economics validation
Use pricing-packaging skill
```

## Phase 5: Execution & Launch (Week 9-10)

### Week 9: Internal Preparation
```
Task: product-ops agent
Prepare organization for pivot:
- Team reorganization if needed
- Training and enablement
- Process changes
- Tools and systems updates
- Success metrics redefinition
```

```
Task: agile-coach agent
Realign team around new direction:
- Vision and strategy workshop
- New OKRs aligned to pivot
- Sprint planning for pivot work
- Remove old commitments
- Celebrate new direction
```

```
Command: /product-operations:meeting-agenda
Purpose: Pivot kickoff all-hands
Create inspiring, clarifying agenda
```

### Week 10: Pivot Launch
```
Task: gtm-planner agent
Execute pivot launch:
- Customer communications sent
- New website/messaging live
- Press and media outreach
- Sales team activated
- Existing customer support
- Monitor feedback intensively
```

```
Command: /product-operations:release-notes
Context: Pivot changes
Create clear, benefit-focused release communication
```

```
Task: customer-success agent
Intensive customer support during transition:
- Proactive outreach to key customers
- Migration assistance
- Quick response to issues
- Gather feedback
- Address concerns rapidly
```

## Phase 6: Post-Pivot Validation (Ongoing)

### Monitor & Iterate
```
Task: data-scientist agent
Track pivot success metrics:
- New customer acquisition
- Existing customer retention
- Activation in new direction
- Engagement with new features
- Revenue impact
- NPS and satisfaction
Create weekly pivot dashboard
```

```
Task: discovery-facilitator agent
Continuous discovery in new direction:
- Weekly customer interviews
- Validate assumptions
- Test new features
- Rapid iteration
- Build conviction in pivot
Reference continuous-discovery skill
```

```
Task: product-strategist agent
Monthly pivot retrospective:
- What's working?
- What's not working?
- Do we need to pivot the pivot?
- Are metrics improving?
- Course corrections needed
Document learnings and adjustments
```

## Deliverables

1. **Situation Assessment** - Current state analysis
2. **Pivot Decision** - Why pivot and which type
3. **Pivot Strategy** - New vision, positioning, roadmap
4. **Product Requirements** - What to build/keep/sunset
5. **Customer Transition Plan** - Migration strategy
6. **Communication Plan** - Internal and external messaging
7. **GTM Strategy** - Repositioned go-to-market
8. **Success Metrics** - How to measure pivot success

## Success Metrics (3-6 months post-pivot)
- Customer acquisition improving
- Retention curves strengthening
- Revenue growth accelerating
- NPS increasing
- Team morale and conviction high
- Product-market fit signals positive
- Clear path to sustainable growth

## Risk Mitigation
- Validate new direction with customers before committing
- Maintain existing revenue during transition
- Communicate transparently with stakeholders
- Move quickly but not recklessly
- Plan for customer attrition
- Have contingency plans
- Set clear success criteria and checkpoints
- Be willing to pivot the pivot if needed

## Common Pivot Mistakes to Avoid
- Pivoting too early (not giving strategy enough time)
- Pivoting too late (out of runway)
- Not validating with customers first
- Changing too many things at once
- Poor communication creating confusion
- Abandoning existing customers too quickly
- Not committing fully to new direction
- Pivoting based on one customer's request
