# Scenario Planner

Plan for multiple future scenarios with structured what-if analysis and contingency planning.

## Usage

```
/pm:scenarios [decision or plan] [optional: time horizon, key variables]
```

## What This Command Does

1. Develops 3-5 plausible future scenarios (best, expected, worst, wildcards)
2. Analyzes implications and strategic responses for each scenario
3. Identifies trigger events and early warning signals
4. Creates contingency plans and decision trees
5. Helps teams prepare for uncertainty and make robust decisions
6. Takes 45 minutes vs 2-3 hours of manual scenario planning

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Decision/Plan Context**:
- What decision or plan are we scenario planning for?
- What's the time horizon? (3 months, 1 year, 3 years)
- What outcome are we trying to achieve?
- What keeps you up at night about this decision?

**Key Uncertainties**:
- What external factors could change? (market, competition, technology, regulation)
- What internal factors are uncertain? (resources, team, execution)
- What assumptions are we making?
- What could go unexpectedly right or wrong?

**Constraints**:
- What's fixed/certain? (commitments already made, resources locked)
- What can we control vs what's beyond our control?
- What decisions are reversible vs irreversible?

**Example Input**:
```
Decision: Launch enterprise tier in Q2 vs Q4
Time Horizon: Next 12 months
Key Uncertainties:
- Will competitor X launch enterprise features?
- Can we hire 3 enterprise engineers by Q1?
- Will recession impact enterprise budgets?
Constraints:
- Board expects enterprise revenue in 2025
- Current team can't support enterprise without hiring
```

### 2. Define Scenario Dimensions

**Identify Key Variables** (2-3 most critical):
- What are the biggest uncertainties?
- What has highest impact if it changes?
- What do we have least control over?

**Example Variables**:
- Market demand (high/low)
- Competitive intensity (aggressive/passive)
- Resource availability (abundant/constrained)
- Technology maturity (ready/not ready)

### 3. Build Scenarios

**Scenario Types**:

**Expected Case** (50% probability):
- Most likely future based on current trends
- Continuation of status quo with normal variation
- "If things go roughly as planned..."

**Best Case** (15-20% probability):
- Optimistic but plausible
- Multiple things break favorably
- "If the stars align..."

**Worst Case** (15-20% probability):
- Pessimistic but plausible
- Multiple challenges compound
- "If Murphy's Law strikes..."

**Wildcard Scenarios** (5-10% probability each):
- Low probability, high impact events
- Disruptive changes to assumptions
- "If the unexpected happens..."

### 4. Analyze Implications

**For Each Scenario**:
- What does this mean for our decision?
- What opportunities emerge?
- What risks materialize?
- How does our strategy need to adapt?

### 5. Create Contingency Plans

**Trigger Events**: Early warning signals that scenario is unfolding
**Response Plans**: What we'll do if scenario occurs
**Decision Points**: When to pivot or double down

## Template

```markdown
# Scenario Planning: [Decision/Plan]

**Date**: [YYYY-MM-DD]
**Planner**: [Your Name]
**Decision**: [What we're planning for]
**Time Horizon**: [3 months | 6 months | 1 year | 3 years]

---

## Context

**What We're Deciding**:
[Clear statement of decision or plan being evaluated]

**Why Scenario Planning**:
[What uncertainties make this necessary - what could change the decision?]

**Time Horizon**: [How far out are we planning]

**Key Stakeholders**: [Who needs to be ready for different scenarios]

---

## Key Uncertainties

**Critical Variables** (2-3 most impactful):

### Variable 1: [Name, e.g., "Market Demand"]
- **High Scenario**: [Description of favorable outcome]
- **Low Scenario**: [Description of unfavorable outcome]
- **Current Evidence**: [What we know today]
- **Controllability**: [High | Medium | Low - how much can we influence this?]

### Variable 2: [Name, e.g., "Competitive Intensity"]
- **High Scenario**: [Description]
- **Low Scenario**: [Description]
- **Current Evidence**: [What we know]
- **Controllability**: [High | Medium | Low]

### Variable 3: [Name, e.g., "Resource Availability"]
- **High Scenario**: [Description]
- **Low Scenario**: [Description]
- **Current Evidence**: [What we know]
- **Controllability**: [High | Medium | Low]

---

## Scenario 1: Expected Case (Base Case)

**Probability**: ~50%
**Name**: [Memorable name, e.g., "Steady Growth"]

**Scenario Description**:
[Narrative description of this future - what happens, why, and how it unfolds]

**Key Assumptions**:
- [Assumption 1 - what has to be true for this scenario]
- [Assumption 2]
- [Assumption 3]

**Variable States**:
- Variable 1: [Expected level]
- Variable 2: [Expected level]
- Variable 3: [Expected level]

**Implications for Our Decision**:
- **Impact**: [How this scenario affects our decision/plan]
- **Opportunities**: [What opens up in this scenario]
- **Risks**: [What challenges emerge]
- **Strategic Response**: [What we should do if this unfolds]

**Metrics to Watch** (Early Signals):
- [Leading indicator 1]: [Current: X, If this scenario: Y]
- [Leading indicator 2]: [Current: X, If this scenario: Y]
- [Leading indicator 3]: [Current: X, If this scenario: Y]

**Trigger Events** (Confirm we're in this scenario):
- [Event 1 that would signal this scenario is happening]
- [Event 2]

**Timeline**:
- **Month 1-3**: [What happens early]
- **Month 4-6**: [Mid-term developments]
- **Month 7-12**: [Long-term outcome]

---

## Scenario 2: Best Case

**Probability**: 15-20%
**Name**: [Memorable name, e.g., "Breakout Success"]

**Scenario Description**:
[Narrative of optimistic but plausible future]

**Key Assumptions**:
- [What has to break favorably]
- [...]

**Variable States**:
- Variable 1: [High/favorable]
- Variable 2: [High/favorable]
- Variable 3: [High/favorable]

**Implications**:
- **Impact**: [How this changes our decision]
- **Opportunities**: [What we can achieve]
- **Risks**: [New challenges from success - scaling, competition response]
- **Strategic Response**: [How we capitalize]

**Metrics to Watch**:
- [Leading indicator 1]: [If this scenario: better than expected]
- [Leading indicator 2]: [...]

**Trigger Events**:
- [Event signaling we're in best case]
- [...]

**How to Accelerate** (Increase probability of this scenario):
- [Action 1 we can take to push toward this outcome]
- [Action 2]

---

## Scenario 3: Worst Case

**Probability**: 15-20%
**Name**: [Memorable name, e.g., "Perfect Storm"]

**Scenario Description**:
[Narrative of pessimistic but plausible future]

**Key Assumptions**:
- [What has to go wrong]
- [...]

**Variable States**:
- Variable 1: [Low/unfavorable]
- Variable 2: [Low/unfavorable]
- Variable 3: [Low/unfavorable]

**Implications**:
- **Impact**: [How this affects our decision]
- **Risks**: [Compounding problems]
- **Damage Control**: [What we do to minimize harm]
- **Strategic Response**: [Defensive strategy]

**Metrics to Watch**:
- [Leading indicator 1]: [If this scenario: worse than expected]
- [Leading indicator 2]: [...]

**Trigger Events**:
- [Early warning sign 1]
- [Early warning sign 2]

**Mitigation Plan** (Reduce probability or impact):
- [Action 1 to prevent or prepare for worst case]
- [Action 2]

**Exit Strategy** (If this scenario unfolds):
- [How we cut losses]
- [What we salvage]

---

## Scenario 4: Wildcard - [Name]

**Probability**: 5-10%
**Name**: [Memorable name, e.g., "Disruptive Shift"]

**Scenario Description**:
[Low probability, high impact scenario - game changer]

**What Changes**:
- [Major disruption to assumptions]
- [Example: New technology, regulatory change, market transformation]

**Implications**:
- **Impact**: [How this reshapes everything]
- **Response**: [How we adapt to fundamentally different world]

---

[Repeat for additional wildcard scenarios if needed]

---

## Scenario Comparison Matrix

| Dimension | Expected Case | Best Case | Worst Case | Wildcard |
|-----------|---------------|-----------|------------|----------|
| **Probability** | 50% | 15-20% | 15-20% | 5-10% |
| **Market Demand** | [Level] | [Level] | [Level] | [Level] |
| **Competition** | [Level] | [Level] | [Level] | [Level] |
| **Resources** | [Level] | [Level] | [Level] | [Level] |
| **Revenue Impact** | [Baseline] | [+X%] | [-Y%] | [±Z%] |
| **Team Impact** | [Baseline] | [Description] | [Description] | [Description] |
| **Strategic Posture** | [Balanced] | [Aggressive] | [Defensive] | [Adaptive] |

---

## Robust Decision Framework

**Decision Analysis Across Scenarios**:

### Option A: [Decision Option 1]

**Performance by Scenario**:
- **Expected Case**: [Outcome - good/neutral/bad]
- **Best Case**: [Outcome]
- **Worst Case**: [Outcome]
- **Wildcard**: [Outcome]

**Weighted Expected Value**: [Calculation considering probabilities]

**Robustness**: 🟢 Performs well across scenarios | 🟡 Mixed performance | 🔴 High variance

**Regret Analysis**:
- **Maximum Regret**: [Worst case - if we choose this and worst scenario unfolds]
- **Regret Tolerance**: [Can we live with this downside?]

---

### Option B: [Decision Option 2]

**Performance by Scenario**:
- **Expected Case**: [Outcome]
- **Best Case**: [Outcome]
- **Worst Case**: [Outcome]
- **Wildcard**: [Outcome]

**Weighted Expected Value**: [Calculation]

**Robustness**: 🟢 🟡 🔴

**Regret Analysis**:
- **Maximum Regret**: [Worst outcome]
- **Regret Tolerance**: [Acceptable?]

---

## Recommendation

**Most Robust Decision**: [Option A or B]

**Rationale**:
[Why this option performs best across scenarios, considering:
- Expected value
- Downside protection
- Upside potential
- Flexibility/optionality
- Reversibility]

**If We Choose This, We Should**:
1. [Action to maximize upside]
2. [Action to protect downside]
3. [Monitoring system to detect scenario unfolding]

---

## Contingency Plans

### If Expected Case Unfolds

**Trigger Events**:
- [Event 1 signals expected case happening]
- [Event 2]
- [Timeline: When to confirm]

**Action Plan**:
1. [Action 1 - what we do]
2. [Action 2]
3. [Resources needed]

**Decision Point**: [When to commit fully vs stay flexible]

---

### If Best Case Unfolds

**Trigger Events**:
- [Early signal 1 that we're exceeding expectations]
- [Signal 2]

**Action Plan**:
1. [How we accelerate - pour gas on the fire]
2. [Resources to add]
3. [Expansion opportunities]

**Watch Out For**: [Risks of rapid success - don't get complacent]

---

### If Worst Case Unfolds

**Trigger Events**:
- [Warning sign 1]
- [Warning sign 2]
- [Timeline: How early can we detect?]

**Action Plan**:
1. [Damage control action 1]
2. [Action 2]
3. [When to pivot or exit]

**Circuit Breakers** (Auto-trigger responses):
- **If [metric] drops below [threshold]**: [Automatic response]
- **If [event] occurs**: [Automatic response]

---

### If Wildcard Unfolds

**How We'll Know**: [Unmistakable signal]

**Action Plan**:
1. [Rapid assessment protocol]
2. [Adaptive response]
3. [Who makes the call to pivot]

---

## Monitoring Dashboard

**Weekly Check** (Track scenario signals):

| Indicator | Current | Expected | Best | Worst | Trend | Status |
|-----------|---------|----------|------|-------|-------|--------|
| [Metric 1] | [Value] | [Range] | [Range] | [Range] | ↑↓→ | 🟢🟡🔴 |
| [Metric 2] | [Value] | [Range] | [Range] | [Range] | ↑↓→ | 🟢🟡🔴 |
| [Metric 3] | [Value] | [Range] | [Range] | [Range] | ↑↓→ | 🟢🟡🔴 |

**Scenario Probability Update** (Monthly reassessment):
- Expected: [Increasing | Stable | Decreasing]
- Best: [Increasing | Stable | Decreasing]
- Worst: [Increasing | Stable | Decreasing]

**Decision to Reassess By**: [Date - when we make go/no-go call]

---

## Learning & Adaptation

**As Scenario Unfolds**:
- [ ] Document which scenario actually materialized
- [ ] Analyze which signals were accurate predictors
- [ ] Identify which assumptions were wrong
- [ ] Update future scenario planning with lessons learned

**Scenario Post-Mortem** (After 6-12 months):
- What scenario actually happened?
- What did we miss?
- What surprised us?
- How well did our contingency plans work?
```

---

## Best Practices

### DO ✅

- **Make scenarios plausible** - Each should be realistic, not science fiction
- **Use narratives** - Stories are easier to think through than bullet points
- **Identify trigger events** - Know early warning signs for each scenario
- **Plan for all scenarios** - Have a response ready for each, including worst case
- **Focus on uncertainties** - Don't scenario-plan things you control
- **Update regularly** - Scenarios change as information emerges
- **Use probability** - Weight scenarios to calculate expected values
- **Test decisions** - Evaluate options against all scenarios, not just expected

### DON'T ❌

- **Create impossible scenarios** - "Aliens invade" isn't helpful planning
- **Ignore worst case** - Hoping it won't happen is not a strategy
- **Make too many scenarios** - 3-5 is optimal, more creates paralysis
- **Forget about probabilities** - A 5% scenario shouldn't drive the decision
- **Lock in too early** - Maintain optionality until scenario becomes clear
- **Scenario plan everything** - Only for high-stakes, high-uncertainty decisions
- **Skip monitoring** - Must track signals to know which scenario is unfolding

---

## Examples

### Example 1: Product Launch Timing

**Input**: "Should we launch enterprise tier in Q2 or Q4?"

**Output**:

```markdown
# Scenario Planning: Enterprise Tier Launch Timing

## Key Uncertainties

1. **Competitive Intensity**: Will Competitor X launch enterprise in Q2?
2. **Team Readiness**: Can we hire enterprise engineers by Q1?
3. **Market Conditions**: Will recession reduce enterprise budgets?

---

## Scenarios

### Expected Case: "Cautious Market" (50%)
- Competition launches Q3
- We hire 2/3 engineers
- Market flat but not declining

**Implication**: Q4 launch is safe bet
- We're ready, competition hasn't saturated market
- Missing Q2 doesn't matter because market isn't buying yet

---

### Best Case: "Hot Market" (20%)
- No competitive launch until Q4
- We hire all 3 engineers by Feb
- Enterprise budgets robust

**Implication**: Q2 launch could capture huge first-mover advantage
- 6-month head start on competition
- Strong demand, ready team

---

### Worst Case: "Crowded & Slow" (20%)
- Competitor launches strong Q2 product
- We only hire 1 engineer, struggle to build
- Recession cuts enterprise budgets

**Implication**: Even Q4 might be too early
- Competitor has entrenched, we're behind on product
- Market not buying anyway

---

## Recommendation: **Q4 Launch with Q2 Decision Point**

**Plan**:
- Target Q4, but monitor for best case
- **Decision Point: End of Q1**
  - If: All 3 engineers hired + no competitor launch → Move to Q2
  - Else: Stick with Q4

**Downside Protection**:
- Q4 gives us buffer against worst case
- If market/team not ready, we have flexibility to delay further
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:risks` - Risk assessment for scenario planning inputs
- `/pm:impact` - Impact estimation for scenario outcomes
- `/pm:decision-log` - Document scenario-based decisions
- `/workflows:quarterly-planning` - Use scenarios in quarterly planning
- `product-strategist` agent - Strategic scenario analysis
- `competitive-analyst` agent - Competitive scenario development
