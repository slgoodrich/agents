# Decision Logger

Document product decisions with context, rationale, trade-offs, and follow-up actions for transparency and future reference.

## Usage

```
/pm:decision-log [decision topic] [optional: context, participants]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Creates structured decision documentation capturing options, rationale, and trade-offs
2. Records dissenting opinions and how concerns were addressed
3. Documents impact on roadmap, resources, users, and technical architecture
4. Assesses reversibility and defines criteria for revisiting decisions
5. Maintains decision history to prevent rehashing settled questions
6. Takes 20 minutes vs 1 hour of manual decision documentation

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Decision Context**:
- What decision needs to be made? (specific question to answer)
- Why is this decision needed now? (trigger, urgency)
- What's at stake? (impact if we choose wrong)
- What constraints exist? (budget, timeline, technical, political)

**Decision Participants**:
- Who is the decision maker? (accountable person)
- Who was consulted? (provided input)
- Who will be informed? (needs to know)
- Were there dissenting opinions? (disagreements)

**Options Context**:
- What options were considered? (list all alternatives)
- What criteria were used to evaluate? (how options compared)
- What data informed the decision? (research, metrics, analysis)
- What's the recommended option? (if consensus exists)

**Impact Context**:
- How does this affect the roadmap? (timeline, priorities)
- What resources are required? (team, budget, tools)
- What's the user impact? (how customers are affected)
- What are the technical implications? (architecture, tech debt)

**Example Input**:
```
Decision: Choose authentication provider (Auth0 vs AWS Cognito vs build custom)
Context: Need SSO for Enterprise tier, launching in Q2
Trigger: Enterprise customers blocking on SSO feature
Stake: $2M ARR from 5 waiting enterprise deals
Participants: CTO (decision maker), VP Eng, Security Lead, PM (me)
Options: Auth0 ($$$, fast), Cognito ($$, AWS-native), Custom ($, slow, flexible)
Constraints: 8 weeks until launch, budget $50K for auth solution
Data: Eng team evaluated all 3, security audit completed
Dissent: Security Lead prefers custom for control, others prefer vendor
```

### 2. Document Decision Process

**Decision Framework** (Use one of these):
- **Pros/Cons**: Simple comparison of advantages/disadvantages
- **Weighted Scoring**: Score each option on criteria (cost, speed, quality, etc.)
- **RICE/ICE**: Prioritization framework (Reach, Impact, Confidence, Effort)
- **Trade-off Analysis**: Explicitly evaluate what you're giving up

**Criteria for Evaluation**:
- Cost (one-time and recurring)
- Time to implement
- Quality/performance
- Flexibility/future-proofing
- Risk level
- Team capability/learning curve

### 3. Record Decision Rationale

**Strong Rationale Includes**:
- **Data-driven reasoning**: What research/metrics support this?
- **Strategic alignment**: How does this fit our goals?
- **Trade-offs accepted**: What are we explicitly choosing NOT to have?
- **Assumptions made**: What are we assuming is true?

**Weak Rationale to Avoid**:
- "Because we've always done it this way"
- "Because [person] said so" (without reasoning)
- "It feels right" (without data)

### 4. Assess Reversibility

**Reversibility Levels**:
- **✅ Easy**: Can reverse with <1 week effort, minimal cost
- **⚠️ Moderate**: Can reverse with 1-4 weeks effort, some cost/disruption
- **🔴 Hard**: Reversal would take >1 month, significant cost, or impossible

**Why Reversibility Matters**:
- Easy-to-reverse decisions → Move fast, experiment
- Hard-to-reverse decisions → Take time, gather more data

### 5. Define Success Criteria

**Decision Success Metrics**:
- How will we know if this was the right choice?
- What metrics will we track?
- When will we review this decision?
- What would trigger reconsidering this decision?

## Template

```markdown
# Decision Log: [Decision Topic]

**Decision ID**: DEC-[XXX]
**Date**: [YYYY-MM-DD]
**Status**: 🟢 Decided | ⏸️ Paused | 🔄 Revisited | ❌ Reversed

---

## Decision Summary

**Decision**: [One sentence: what was decided]

**Decision Maker**: [Name, Title] (Accountable)

**Decision Type**:
- [ ] Strategic (Company direction, market positioning)
- [ ] Product (Feature, user experience, roadmap)
- [ ] Technical (Architecture, infrastructure, tooling)
- [ ] Operational (Process, team structure, workflow)

**Timeline**: Decision needed by [Date], Implementation by [Date]

---

## Context & Background

**Why This Decision Was Needed**:
[Explain the problem, opportunity, or situation requiring a decision]

**Trigger/Catalyst**:
[What prompted this decision now - e.g., customer request, competitive threat, technical debt]

**Stakes**:
- **High Stakes**: [What's at risk if we choose wrong - revenue, users, team morale]
- **Opportunity Cost**: [What we can't do if we commit to this]

**Constraints**:
- **Budget**: [Financial limits]
## Template

```markdown
# Decision: [Short Title]

**ID**: DEC-[YYYY]-[NNN] | **Date**: [Date] | **Status**: Proposed|Accepted|Superseded
**Decision Maker**: [Name/Role] | **Impact**: High|Medium|Low

---

## Decision

[One sentence: What was decided]

---

## Context

**Problem/Situation**:
[What prompted this decision? What problem are we solving?]

**Why Now**:
[Why is this decision needed now? What's the urgency/trigger?]

**Stakeholders**:
- [Name/Team]: [Their interest/concern]
- [Name/Team]: [Their interest/concern]

---

## Options Considered

### Option A: [Name] (✅ CHOSEN)
**Description**: [What is this option]
**Pros**: [Benefits]
**Cons**: [Drawbacks]
**Cost/Effort**: [Estimate]

### Option B: [Name]
**Description**: [What is this option]
**Pros**: [Benefits]
**Cons**: [Drawbacks]
**Cost/Effort**: [Estimate]

### Option C: Do Nothing
**Impact**: [What happens if we don't decide]

---

## Decision Rationale

**Why Option A**:
1. [Reason 1]
2. [Reason 2]
3. [Reason 3]

**Trade-offs Accepted**:
- [What we're giving up by choosing this]

**Assumptions**:
- [Key assumption 1]
- [Key assumption 2]

---

## Implementation

**Actions**:
- [ ] [Action 1] - [Owner] - [By when]
- [ ] [Action 2] - [Owner] - [By when]

**Timeline**: [When this takes effect]

**Success Criteria**: [How we'll know this was right decision]

---

## Consequences

**Teams Affected**: [List teams and how affected]
**Migration Needed**: [If applicable]
**Risks**: [Risks of this decision]
**Reversibility**: Easy|Hard|Irreversible - [Why]

---

## Related

- **Supersedes**: [Previous decision if applicable]
- **Related Decisions**: [Links]
- **Documentation**: [PRD/spec links]

---

## Review

**Review Date**: [When to revisit this]
**Owner**: [Who monitors this decision]
```

## Best Practices

✅ **DO**: Decide and document quickly, capture all options considered, explain why (rationale), include dissenting opinions, be specific about trade-offs, make decision maker clear, include review date, link to related decisions, update status when superseded

❌ **DON'T**: Decide without documenting, hide dissent, skip the "why", make decisions in vacuum (no stakeholder input), forget to communicate decision, leave status ambiguous, skip review dates, make irreversible decisions lightly

**Related**: `/pm:quick-answer`, `/pm:prd`, `/pm:technical-spec`
