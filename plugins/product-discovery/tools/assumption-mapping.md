---
name: Assumption Mapping
description: Identify, prioritize, and validate assumptions to reduce risk in product development
category: Planning
model: sonnet
---

# Assumption Mapping

Systematic approach to identifying, prioritizing, and testing assumptions that underlie product decisions and strategies.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Initiative/Feature/Strategy**: What are you building or planning?
- **Context**: Stage (idea, design, build, launch), known information
- **Goal**: What you're trying to achieve
- **Risks** (optional): Known concerns or uncertainties

## Output

Comprehensive assumption map with testing strategy:

### 1. Assumption Inventory

**Assumption categories** to explore:

**Customer/Problem Assumptions**:
- Customers have this problem
- Problem is painful enough to solve
- Current solutions are inadequate
- Customers will change behavior
- Target segment is correct

**Solution Assumptions**:
- Our solution solves the problem
- Customers can/will use our solution
- Solution is better than alternatives
- Value proposition is compelling

**Usability Assumptions**:
- Customers understand how to use it
- Workflow fits their process
- Learning curve is acceptable
- No major friction points

**Technical Assumptions**:
- We can build this
- Performance will be adequate
- Integration with X will work
- Scalability is achievable
- Security/compliance requirements met

**Business Assumptions**:
- Customers will pay $X
- We can acquire customers for <$Y
- Market size is sufficient
- Unit economics work
- Can reach profitability

**Go-to-Market Assumptions**:
- We can reach target customers
- Message will resonate
- Channel X will work
- Sales cycle is N months
- Conversion rate will be Z%

**Competitive Assumptions**:
- Competitors won't respond
- Our differentiation matters
- Barriers to entry exist
- We can defend position

For each assumption:
- **Assumption statement**: What we believe is true
- **Why we believe it**: Current evidence or rationale
- **If wrong, what happens**: Impact if assumption proves false

**Identify 15-30 key assumptions**

### 2. Assumption Prioritization Matrix

**Two dimensions**:

**Importance** (if assumption is wrong):
- **Critical** (10): Product fails completely
- **High** (7-9): Major pivot needed
- **Medium** (4-6): Adjustments required
- **Low** (1-3): Minor impact

**Evidence/Certainty** (how sure we are):
- **Known** (10): Strong evidence, validated
- **Confident** (7-9): Good evidence, likely true
- **Uncertain** (4-6): Some evidence, unclear
- **Unknown** (1-3): No evidence, pure assumption

**Risk Score** = Importance × (10 - Evidence)
- High risk = Important assumption with low evidence

**2x2 Matrix**:
```
          High Importance
                |
Unknown   TEST  |  VALIDATE
Evidence  FIRST |  SOON
          ------|--------
          WATCH |  MONITOR
                |  LATER
           Low Importance
```

**Quadrants**:
- **Test First** (High importance, low evidence): Highest priority to validate
- **Validate Soon** (High importance, high evidence): Confirm beliefs
- **Watch** (Low importance, low evidence): Keep eye on
- **Monitor Later** (Low importance, high evidence): Low priority

### 3. Prioritized Assumption List

**Top 10 riskiest assumptions** to test:
1. [Assumption] - Risk score: [X]
2. [Assumption] - Risk score: [X]
...

Focus validation efforts on highest-risk items.

### 4. Testing Strategy

For each high-priority assumption, define:

**Assumption**: [Statement]

**What we need to learn**:
- Specific question to answer
- Success criteria
- What "validated" looks like

**Test method**:
- **Customer interviews** - Exploratory, open-ended
- **Surveys** - Quantitative validation, scale
- **Landing page test** - Interest and demand
- **Prototype test** - Usability and workflow
- **Wizard of Oz MVP** - Value proposition test
- **Concierge MVP** - Service delivery test
- **A/B test** - Conversion and engagement
- **Data analysis** - Existing behavior patterns
- **Competitive analysis** - Market validation
- **Technical spike** - Feasibility proof

**Design experiment**:
- What exactly to do
- With how many people/samples
- Success metrics
- Timeline (days/weeks)
- Resources needed

**Decision criteria**:
- If results show X, we will Y
- Proceed, pivot, or kill thresholds
- What we'll do with learnings

### 5. Learning Plan

**Validation roadmap**:

**Week 1-2**:
- Assumption 1: [Test method]
- Assumption 2: [Test method]
- Assumption 3: [Test method]

**Week 3-4**:
- Based on Week 1-2 learnings
- Next highest priority assumptions
- Deeper validation of partially validated assumptions

**Week 5-6**:
- Final critical assumptions
- Refine based on accumulated knowledge

**Learning checkpoints**:
- After each test: Update assumption map
- Weekly: Review progress, adjust plan
- Bi-weekly: Major go/no-go decisions

**Budget**:
- Time investment
- Money for tools, incentives, ads
- People involved

### 6. Assumption Tracking

**Status for each assumption**:
- 🔴 **Invalidated**: Assumption proven false
- 🟡 **Uncertain**: Test results inconclusive
- 🟢 **Validated**: Strong evidence assumption is true
- ⚪ **Not tested**: Haven't validated yet

**Test results log**:
- What we tested
- Method used
- Results (quantitative and qualitative)
- What we learned
- Impact on assumption status
- Next steps

**Decision log**:
- Changes made based on learnings
- Pivots or adjustments
- Features added/removed
- Strategy shifts

### 7. Risk Mitigation

**For invalidated assumptions**:
- What does this mean for product?
- Pivot options
- Alternative approaches
- Go/no-go decision

**For uncertain assumptions**:
- Additional tests needed
- How to proceed with uncertainty
- Contingency plans

**Remaining risks**:
- Assumptions we can't test easily
- Acceptable risks to take
- Monitoring plan post-launch
- Rollback strategies

## Example Prompt

```
Create assumption map for:
- Initiative: Launching AI-powered code review feature for developers
- Context: Early design stage, targeting enterprise dev teams
- Goal: Drive expansion revenue from existing customers
- Known risks: Uncertain if developers trust AI for code quality, integration complexity
```

## Use Cases

- **New product development** - De-risk ideas before building
- **Feature validation** - Test before committing resources
- **Market entry** - Validate new market or segment
- **Strategy planning** - Test strategic assumptions
- **Pivot decisions** - Understand what needs validation
- **Risk management** - Identify and mitigate risks

## When to Use Assumption Mapping

**Pre-development**:
- Before writing specs or code
- Validate riskiest assumptions first
- Avoid building wrong thing

**During discovery**:
- Part of continuous discovery practice
- Regular assumption testing
- Update as you learn

**Strategic decisions**:
- Market entry
- Business model changes
- Positioning shifts

**High-uncertainty initiatives**:
- New markets
- Unvalidated ideas
- Innovative features

## Benefits

**Reduces risk**:
- Test before building
- Fail fast and cheap
- Evidence-based decisions

**Focuses effort**:
- Prioritize what matters
- Don't test everything
- Highest-risk assumptions first

**Shared understanding**:
- Team alignment on unknowns
- Explicit about what we don't know
- Honest about uncertainty

**Learning culture**:
- Embrace experimentation
- Celebrate validated learning
- Okay to be wrong early

## Assumption Testing Methods

**Qualitative (understanding)**:
- **Customer interviews** (5-10): Deep understanding
- **Prototype testing** (8-15): Usability and workflow
- **Observation** (3-5): Contextual inquiry
- **Expert interviews** (3-5): Domain knowledge

**Quantitative (measuring)**:
- **Surveys** (50-100+): Scale and patterns
- **Landing page tests** (100-1000s): Interest/demand
- **A/B tests** (1000s+): Conversion and behavior
- **Analytics analysis**: Existing behavior

**Mixed methods**:
- **Wizard of Oz MVP**: Fake automation, manual backend
- **Concierge MVP**: Manual service delivery
- **Smoke tests**: Gauge interest before building
- **Fake door tests**: Track clicks on non-existent features

**Speed vs. Confidence**:
- Interview 5 people: Fast (days), directional
- Survey 100 people: Medium (week), more confident
- A/B test 10K users: Slower (2-4 weeks), statistical significance

Choose based on risk level and time available.

## Common Assumption Categories by Product Stage

**Idea stage**:
- Problem exists and is painful
- Customers will pay
- Market is big enough
- We can reach customers

**Design stage**:
- Solution solves problem
- Customers can use it
- Better than alternatives
- Value prop resonates

**Build stage**:
- Technical feasibility
- Performance acceptable
- Integration works
- Security/compliance met

**Launch stage**:
- Pricing is right
- Channels work
- Messaging resonates
- Conversion rates sufficient

**Growth stage**:
- Can scale operations
- Unit economics work
- Retention is strong
- Expansion opportunities exist

## Common Pitfalls

**Not testing at all**:
- "We already know" syndrome
- Assuming instead of validating
- Confirmation bias

**Testing everything**:
- Analysis paralysis
- Testing low-risk assumptions
- Never shipping

**Testing wrong way**:
- Asking what people would do (unreliable)
- Observing what they actually do (reliable)
- Small sample, big conclusions

**Ignoring results**:
- Testing but not acting on learnings
- Confirmation bias
- Sunk cost fallacy

**Not updating regularly**:
- Test once, never revisit
- Market changes, assumptions change

## Related Tools

- `/workflows/solution-validation` - Comprehensive validation process
- `/tools/impact-mapping` - Connect assumptions to goals
- `/tools/trade-off-analysis` - Make decisions under uncertainty
- `/workflows/pmf-assessment` - Product-market fit validation
- `/pm:experiment-designer` - Design tests

## After Assumption Mapping

**Create**:
- Discovery plan and schedule
- Experiment backlog
- Test scripts and materials
- Decision criteria

**Execute**:
- Run tests systematically
- Document learnings
- Update assumption map
- Make go/no-go decisions

**Iterate**:
- Test, learn, adjust
- Build conviction
- Reduce risk progressively

Assumption mapping makes the invisible visible. By explicitly stating and testing what we believe to be true, we reduce risk and build conviction in our product decisions.

Remember: It's okay to have assumptions. It's not okay to not test them.
