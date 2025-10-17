# Decision Logger

Document product decisions with context, rationale, and trade-offs.

## Usage

```
/pm:decision-log [decision topic]
```

## What This Command Does

Creates structured decision documentation capturing options, rationale, trade-offs, and follow-up actions.

## Instructions

1. Document decision context
2. List options considered
3. Record chosen option with rationale
4. Note trade-offs accepted
5. Capture dissenting opinions
6. Define follow-up actions

## Template

```markdown
# Decision Log: [Topic]

**Date**: [Date]
**Decision Maker**: [Name/role]
**Participants**: [Who involved]
**Decision Type**: Strategic | Tactical | Technical

---

## Context
[Why this decision was needed]

---

## Options Considered

### Option A: [Description]
**Pros**:
- [Benefit 1]
- [Benefit 2]

**Cons**:
- [Drawback 1]
- [Drawback 2]

**Cost/Effort**: [Estimate]

### Option B: [Description]
[Same structure]

### Option C: [Description]
[Same structure]

---

## Decision
**Chosen**: [Option X]

**Rationale**:
- [Reason 1]
- [Reason 2]
- [Reason 3]

**Trade-offs Accepted**:
- [What we're giving up]
- [Risks we're accepting]

---

## Impact

**On Roadmap**: [Timeline effects]
**On Resources**: [Team/budget]
**On Users**: [Customer impact]
**On Tech**: [Technical implications]

---

## Dissenting Opinions
- [Name] preferred Option B because [reason]
- [How concerns were addressed]

---

## Reversibility
**Level**:  Easy | ⚠️ Moderate | 🔴 Hard

[Explanation of reversal difficulty]

---

## Follow-up Actions
- [ ] [Action 1] - [Owner] - [Due date]
- [ ] [Action 2] - [Owner] - [Due date]

**Review Date**: [When to revisit]

---

## Related Decisions
- Links to related decision docs
- Dependencies
```

## Model
claude-sonnet-4-5

## Related
- `/pm:stakeholder-map` - Stakeholder involvement
- `/pm:trade-off` - Analyze trade-offs
