---
description: Validate solution ideas before full development commitment
category: Discovery
duration: 2-3 weeks
model: sonnet
---

# Solution Validation Workflow

Rapid process for validating that a proposed solution actually solves the customer problem before investing in full development.

## Usage
```
/solution-validation [solution or feature idea]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Proposed solution or feature idea
- Problem it's meant to solve
- Who has this problem (target users)
- Why we think this solution will work (hypothesis)
- Alternative solutions considered
- Risk/effort if we build wrong thing

## Timeline: 2-3 Weeks

## Phase 1: Assumption Mapping (Week 1)

### Day 1-2: Identify Assumptions
```
Task: discovery-facilitator agent
Map all assumptions about the solution:
- **Customer assumptions**: Who will use this?
- **Problem assumptions**: What problem does it solve?
- **Solution assumptions**: How will our solution work?
- **Value assumptions**: Why will customers use it?
- **Usability assumptions**: Can customers use it?
- **Feasibility assumptions**: Can we build it?
- **Viability assumptions**: Will it drive business results?
Reference continuous-discovery skill
```

```
Task: product-strategist agent
Score assumptions by risk:
- **Certainty**: How sure are we? (1-5 scale)
- **Impact**: If wrong, what happens? (1-5 scale)
- **Risk Score**: (5 - Certainty) × Impact

Prioritize: High risk (low certainty, high impact) test first
Create assumption risk matrix
```

### Day 3-5: Design Validation Tests
```
Task: discovery-facilitator agent
Design experiments for top 5-10 riskiest assumptions:
- What's the cheapest/fastest test?
- What evidence do we need?
- What's our success criteria?
- How long will it take?

Test types:
- Customer interviews
- Landing page tests
- Prototype testing
- Wizard of Oz MVP
- Concierge MVP
- Feature fake (button that doesn't work yet)

Create validation test plan
Reference lean-product-development skill
```

## Phase 2: Prototype Development (Week 1-2)

### Build Validation Prototype
```
Task: requirements-engineer agent
Define prototype requirements:
- Minimum fidelity needed to test assumptions
- Key user flows to prototype
- What must be real vs. fake
- Data needed for realistic testing
- Edge cases to include or exclude
Create prototype specification
```

**Prototype Options** (choose based on what you're testing):

**High-Fidelity Interactive Prototype**
```
If testing: Usability, user flows, interaction design
Tool: Figma, Sketch, Adobe XD
Includes: Realistic UI, clickable interactions, key flows
```

**Wizard of Oz MVP**
```
If testing: Value proposition, willingness to use
Approach: Manual backend, automated frontend
Build: Simple interface that appears to work, humans do the work behind scenes
```

**Concierge MVP**
```
If testing: Value delivered, customer workflow
Approach: Fully manual service delivery
Build: Onboarding flow, deliver service manually
```

**Landing Page MVP**
```
If testing: Demand, value proposition, willingness to pay
Build: Marketing page explaining product
Measure: Signups, email capture, pre-orders
```

**Feature Stub**
```
If testing: Feature discovery, click-through interest
Build: Button/menu item in existing product
Measure: Clicks, track interest
```

### Technical Feasibility Spike
```
Task: technical-pm agent
If technical feasibility is a key assumption:
- Build technical prototype/proof of concept
- Test performance at scale
- Validate integrations
- Assess complexity
- Estimate effort
Create technical feasibility report
```

## Phase 3: Customer Testing (Week 2-3)

### Recruit Test Participants
```
Task: user-researcher agent
Recruit 8-15 test participants:
- Target customer segment
- Mix of existing and potential customers
- Represent use cases and personas
- Screen for appropriate fit
- Schedule sessions
```

### Conduct Validation Tests

**Usability Testing** (if testing solution usability)
```
Task: user-researcher agent
Run 8-12 usability test sessions:
- Give realistic tasks
- Think-aloud protocol
- Observe where they struggle
- Note confusion and delight
- Time on task
- Completion rates
- Post-task questions
Use user-research-techniques skill
```

**Solution Interview** (if testing value and workflow)
```
Task: user-researcher agent
Conduct solution interviews:
- Show prototype
- Explain value proposition
- Walk through use case
- Ask: Would you use this?
- Ask: How much would you pay?
- Ask: What's missing?
- Compare to current solution
Reference jobs-to-be-done skill
```

**A/B Test** (if testing messaging or conversion)
```
Task: growth-pm agent
Run landing page A/B test:
- Version A: Current or control
- Version B: New value prop/solution
- Measure: Conversion, signups, interest
- Statistical significance
- Segment analysis
```

**Fake Door Test** (if testing feature interest)
```
Task: data-scientist agent
Add feature stub to product:
- Track clicks/attempts to use
- Show "coming soon" message
- Capture interest signal
- Optional: Collect email for early access
Measure interest level
```

### Daily Synthesis
```
Task: customer-insights agent
Synthesize learnings daily during testing:
- Patterns across sessions
- Surprising insights
- Assumption validation status
- Unexpected findings
- Necessary pivots
Create daily insights log
```

## Phase 4: Analysis & Decision (Week 3)

### Comprehensive Analysis
```
Task: user-researcher agent
Analyze all validation data:
- Qualitative: Themes from interviews/tests
- Quantitative: Metrics and conversion rates
- Assumption scorecard: Validated, invalidated, unclear
- Customer quotes and evidence
- Video highlights if recorded
Create validation research report
```

```
Task: data-scientist agent
Analyze quantitative signals:
- Usage metrics from tests
- Conversion rates
- Time to value
- Feature interaction data
- Funnel analysis
- Cohort behavior
Create quantitative validation analysis
```

### Decision Framework
```
Task: product-strategist agent
Make go/no-go/pivot decision:

**Strong GO signals**:
- Key assumptions validated
- Customers expressed strong interest
- Usability successful (>80% completion)
- Willingness to pay at target price
- Clear differentiation from alternatives
- Technical feasibility confirmed

**PIVOT signals**:
- Some assumptions validated, others not
- Interest exists but solution not quite right
- Different segment showed more interest
- Different use case more compelling
- Pricing needs adjustment

**NO-GO signals**:
- Weak customer interest
- Can't articulate value clearly
- Customers prefer current solution
- Too complex to use
- Won't pay enough for unit economics
- Technical challenges too great

Create decision recommendation with rationale
```

```
Command: /stakeholder-management:decision-logger
Decision: [Go/No-go/Pivot on solution]
Log decision with evidence and rationale
```

## Phase 5: Plan Next Steps (Week 3)

### If GO: Plan Development

```
Task: requirements-engineer agent
Create development specification:
- Incorporate learnings from validation
- Prioritize features based on testing
- Edge cases to handle
- Success metrics
- Technical requirements
Create PRD for validated solution
```

```
Command: /requirements-engineering:prd-generator
Feature: [validated solution]
Create comprehensive PRD with validation insights
```

```
Task: agile-coach agent
Plan development sprints:
- MVP scope based on validation
- Sprint plan for first release
- Success metrics to track
- Timeline and milestones
```

### If PIVOT: Plan Next Validation

```
Task: discovery-facilitator agent
Plan pivot validation:
- What did we learn?
- What should we test next?
- New assumptions to validate
- Modified solution to test
- Timeline for next validation cycle
Create pivot plan and schedule
```

### If NO-GO: Document Learnings

```
Task: product-ops agent
Document for organizational learning:
- What we tested
- What we learned
- Why we're not proceeding
- Implications for strategy
- Ideas for future consideration
Create solution validation post-mortem
```

## Deliverables

1. **Assumption Risk Matrix** - Prioritized assumptions to test
2. **Validation Test Plan** - Experiments to run
3. **Prototype** - Minimum fidelity to test assumptions
4. **Research Report** - Qualitative and quantitative findings
5. **Validation Scorecard** - Assumptions validated/invalidated
6. **Decision Recommendation** - Go/no-go/pivot with rationale
7. **Next Steps Plan** - Development plan or next validation

## Success Metrics
- High-risk assumptions validated (>80%)
- Clear evidence-based decision made
- Customer interest demonstrated (>60% would use)
- Usability validated (>80% task completion)
- Time and cost to validate minimized
- Learnings documented for team

## Validation Best Practices
- Test riskiest assumptions first
- Use lowest fidelity prototype that works
- Talk to real target customers
- Observe behavior, don't just ask questions
- Quantify when possible (metrics > opinions)
- Be willing to pivot or kill based on evidence
- Document learnings even if no-go
- Move fast but be thorough

## Common Validation Mistakes
- Testing with wrong customers (friends, not targets)
- Building too high fidelity too early
- Asking what people would do vs. observing
- Confirmation bias (seeing what you want)
- Testing too many things at once
- Not having clear success criteria
- Ignoring negative signals
- Taking too long to validate
