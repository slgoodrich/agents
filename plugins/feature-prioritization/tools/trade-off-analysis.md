---
description: Structured framework for making difficult product decisions and trade-offs
category: Planning
model: sonnet
---

# Trade-Off Analysis

Systematic approach to evaluating trade-offs and making difficult product decisions when you can't have everything.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Decision to make**: What are you deciding?
- **Options**: What are the alternatives (2-5 options typically)
- **Context**: Constraints, goals, stakeholders
- **Criteria** (optional): What matters most in this decision

## Output

Comprehensive trade-off analysis with recommendation:

### 1. Decision Framework

**Decision statement**:
- Clear articulation of decision
- Why decision is needed now
- Impact of decision
- Who owns decision

**Success criteria**:
- What does "good decision" look like?
- Key outcomes to optimize for
- Acceptable trade-offs
- Unacceptable compromises

### 2. Options Analysis

For each option (typically 2-5 options):

**Option [Name]**:
- **Description**: What this option entails
- **Pros**: Advantages and benefits
- **Cons**: Disadvantages and drawbacks
- **Assumptions**: What must be true
- **Resources required**: Time, money, people
- **Reversibility**: Can we undo this? (Easy/Hard/Irreversible)
- **Risk level**: Low/Medium/High

**Special option: "Do Nothing"**:
- What happens if we make no decision?
- Status quo baseline for comparison

### 3. Evaluation Criteria

**Weighted scoring matrix**:

Define criteria and weights (total 100%):
- **Strategic alignment** (20%): Fits vision and strategy
- **Customer value** (25%): Impact on customers
- **Business impact** (20%): Revenue, growth, metrics
- **Feasibility** (15%): Technical and operational ability
- **Resource efficiency** (10%): ROI and effort
- **Risk** (10%): Risk level and mitigation

**Score each option** (1-10 scale):
| Criterion (Weight) | Option A | Option B | Option C |
| Strategic (20%) | 8 (1.6) | 6 (1.2) | 7 (1.4) |
| Customer (25%) | 9 (2.25)| 7 (1.75)| 8 (2.0) |
| Business (20%) | 7 (1.4) | 9 (1.8) | 6 (1.2) |
| ...

**Weighted totals** - Sum of (score × weight)

### 4. Trade-Off Analysis

**What you gain vs. lose** for each option:

**Option A**:
- ✅ **Gains**: What you get
- ❌ **Sacrifices**: What you give up
- ⚠️ **Risks**: What could go wrong
- ✓ **Mitigations**: How to reduce risks

*Repeat for each option*

**Key trade-offs** (pairwise):
- Speed vs. Quality
- Scope vs. Time
- User experience vs. Technical simplicity
- Short-term revenue vs. Long-term value
- Breadth vs. Depth
- Flexibility vs. Simplicity
- Innovation vs. Stability

Identify which trade-offs this decision forces.

### 5. Stakeholder Perspectives

**Different stakeholder views**:

**Engineering**:
- Preferences and concerns
- Technical debt implications
- Long-term maintainability

**Customers**:
- Which option they'd prefer
- Impact on different segments
- Adoption and satisfaction

**Business/Leadership**:
- Financial implications
- Strategic alignment
- Competitive positioning

**Support/Operations**:
- Operational impact
- Support burden
- Scalability

Acknowledge whose needs are prioritized and whose are compromised.

### 6. Decision Aids

**Second-order consequences**:
- What does each option enable or prevent in future?
- Long-term implications beyond immediate impact
- Path dependencies created

**Regret minimization**:
- Which decision will we regret least?
- 6 months from now, what will we wish we'd chosen?
- Which option keeps most options open?

**Reversibility assessment**:
- **One-way doors** (irreversible): Decide very carefully
- **Two-way doors** (reversible): Decide quickly, test, iterate

### 7. Recommendation

**Recommended option**: [Option X]

**Rationale**:
- Why this option best serves goals
- How it aligns to criteria
- Trade-offs we're accepting
- Why trade-offs are acceptable

**Confidence level**: High/Medium/Low
- Why this confidence level
- What would increase confidence
- What could validate decision

**Implementation considerations**:
- Next steps to execute
- How to mitigate risks
- Success metrics
- Review timeline

**Dissenting opinions** (if any):
- Alternative viewpoints
- Valid concerns to monitor
- Conditions that might change recommendation

## Example Prompt

```
Create trade-off analysis for:
- Decision: Should we build mobile app (iOS + Android) or progressive web app (PWA)?
- Context: B2B SaaS, 15-person team, limited mobile expertise, competitors have native apps
- Constraints: 6-month timeline, $500K budget, team capacity for one approach
- Goals: Expand mobile usage, maintain feature parity, manageable maintenance
```

## Use Cases

- **Feature prioritization** - Choose between competing features
- **Technical decisions** - Architecture and technology choices
- **Strategy decisions** - Market, positioning, business model
- **Resource allocation** - Where to invest limited resources
- **Scope decisions** - What's in/out for release
- **Build vs. buy** - Make or partner decisions

## Trade-Off Frameworks

**Kano Model**:
- Must-haves (basic expectations)
- Performance (more is better)
- Delighters (unexpected value)

Use to understand which features are table stakes vs. differentiation.

**Cost of Delay**:
- What's the cost of waiting?
- Urgency and impact over time
- Opportunity cost

**MoSCoW**:
- Must have
- Should have
- Could have
- Won't have (this time)

**Value vs. Complexity** (2x2):
- High value, low complexity: Do first
- High value, high complexity: Strategic bets
- Low value, low complexity: Easy wins
- Low value, high complexity: Don't do

## Decision-Making Principles

**Be explicit about trade-offs**:
- Every decision involves trade-offs
- Acknowledge what you're giving up
- No shame in making trade-offs

**Use data where possible**:
- Quantify impact when you can
- Customer research and validation
- A/B tests for reversible decisions
- Pilot programs for major changes

**Acknowledge uncertainty**:
- Be honest about what you don't know
- Identify assumptions
- Plan to validate quickly
- Adjust based on learnings

**Consider reversibility**:
- Reversible decisions: Decide fast, test, iterate
- Irreversible decisions: Decide carefully, gather data
- Most decisions are more reversible than we think

**Balance analysis and action**:
- Analysis paralysis is a risk
- Set decision deadlines
- "Good enough" often beats "perfect too late"
- Some things you learn by doing

## Common Trade-Off Decisions

**Speed vs. Quality**:
- Fast launch with rough edges
- Delayed launch with polish

**Horizontal vs. Vertical**:
- Broad platform for many use cases
- Deep solution for specific niche

**Enterprise vs. SMB**:
- High-touch, customizable, expensive
- Self-serve, opinionated, affordable

**Innovation vs. Stability**:
- New capabilities and features
- Reliability and performance

**Revenue now vs. later**:
- Monetize aggressively today
- Grow adoption, monetize later

## After the Decision

**Document decision**:
```
Command: /stakeholder-management:decision-logger
Record decision, rationale, trade-offs
```

**Communicate broadly**:
- Share decision and reasoning
- Acknowledge trade-offs made
- Explain who benefits and who compromises

**Define success metrics**:
- How will we know if decision was right?
- Leading and lagging indicators
- Review timeline (30/60/90 days)

**Stay open to new information**:
- Monitor results
- Be willing to change course if wrong
- Some decisions can be unwound

## Related Tools

- `/stakeholder-management:decision-logger` - Document decisions
- `/tools/assumption-mapping` - Validate decision assumptions
- `/strategic-planning:scenario-planner` - Model different scenarios
- `/tools/impact-mapping` - Connect decisions to outcomes
- `/strategic-planning:risk-assessment` - Assess decision risks

## Tips for Better Trade-Off Decisions

**Involve right people**:
- Decision owner is clear
- Input from stakeholders
- Diverse perspectives
- But don't decide by committee

**Frame clearly**:
- What exactly are we deciding?
- What are we NOT deciding?
- What's the deadline?

**Consider opportunity cost**:
- Choosing X means not choosing Y
- What else could we do with resources?

**Test when possible**:
- Prototype, MVP, experiment
- Learn before big commitment
- Progressive roll-out

**Trust your judgment**:
- Not all decisions need extensive analysis
- Experience and intuition matter
- Some decisions are judgment calls

**Review and learn**:
- Look back at past decisions
- What did we get right/wrong?
- Improve decision-making process

Good product management is making good trade-offs. Great product management is making the trade-offs that matter most to your strategy and customers.
