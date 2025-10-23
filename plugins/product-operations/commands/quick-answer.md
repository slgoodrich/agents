# Quick Answer

Rapidly answer team questions about priorities, decisions, or requirements with automatic decision logging.

## Usage

```
/product-operations:quick-answer [question or topic] [optional: asker, context]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Provides fast, clear answers to common team questions
2. Automatically logs decisions to prevent repeated questions
3. Formats answers for different channels (Slack, email, doc comment)
4. References related decisions, docs, or context
5. Ensures consistency in responses
6. Takes 2-5 minutes vs 10-15 minutes of back-and-forth

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Question Context**:
- What is the exact question being asked? (be precise, avoid assumptions)
- Who is asking? (team member, stakeholder, customer, leadership)
- Why do they need to know? (unblock work, planning, decision-making, curiosity)
- When do they need the answer? (urgent/today, this week, no rush)

**Background**:
- Has this been asked or answered before? (check decision log, docs)
- What context do they already have? (are they new to the project or deeply involved)
- Are there related questions or decisions? (is this part of a bigger topic)
- What will they do with the answer? (implement something, plan, communicate to others)

**Decision Impact** (if applicable):
- Does this answer represent a new decision? (vs referencing existing decision)
- Who should know about this decision? (just asker or broader team)
- Should this be logged for future reference? (to prevent re-asking)

### 2. Categorize Question Type
   - **Priority** - "Should we build X or Y first?"
   - **Scope** - "Is Z in scope for this sprint/feature?"
   - **Requirements** - "How should X work in scenario Y?"
   - **Decision** - "Have we decided on approach A or B?"
   - **Context** - "Why are we doing X?"
   - **Process** - "What's the process for Y?"

2. **Gather Minimal Context**:
   - Who's asking
   - What they need the answer for (unblock work, planning, curiosity)
   - Urgency (today, this week, just wondering)
   - Previous related decisions

3. **Formulate Answer**:
   - **Direct** - Start with yes/no or clear answer
   - **Concise** - 2-3 sentences max
   - **Actionable** - Next steps if any
   - **Referenced** - Link to source of truth

4. **Auto-Log Decision**:
   - If answer represents a decision, log it
   - Prevents same question being asked again
   - Creates searchable decision history

## Template

```markdown
## Quick Answer: [Question]

**Asked by**: [Name/Team] | **Date**: [Date] | **Category**: Priority|Scope|Requirements|Decision|Context|Process

---

## Question
[Restate clearly]

## Answer

**TL;DR**: [One sentence direct answer]

**Details**: [2-3 sentences explaining]

**Reasoning**:
- [Why this answer]
- [Key factors]
- [Trade-offs if any]

**Source**: [OKR/roadmap/previous decision/strategy doc]

---

## Action Items
- [ ] [Asker] - [What to do now]
- [ ] [PM] - [Follow-up if needed]

**If you need more**: [When/how to escalate]

---

## Related
- Decision: [Link to decision log]
- Doc: [Link to PRD/spec]

---

## Decision Log
**Decision**: [If this represents a decision]
**Logged**: Yes ✓ | No (just clarification)
```

## Response Patterns

### Priority ("Should we X or Y first?")
**TL;DR**: Build [X] in [Q], [Y] in [Q+1]
**Details**: [X] prioritized because: [N] customer requests, competitive gap, faster to ship, unlocks $[X]
**Source**: [OKR/Roadmap]

### Scope ("Is Z in scope?")
**TL;DR**: No, [Z] out of scope for v1
**Details**: v1 is [limited scope]. [Z] explicitly out to ship faster. Can iterate in v1.1.
**Source**: [PRD Section X]

### Requirements ("How should X work?")
**TL;DR**: [Specific behavior]
**Details**: [How it works], [Why this way]
**Source**: [Spec Section X]

### Decision Recall ("Did we decide X or Y?")
**TL;DR**: [X] chosen
**Details**: Decision made [date], reasons: [list]
**Source**: [Decision Log ID]

### Context ("Why are we doing X?")
**TL;DR**: [Goal/outcome]
**Details**: [User/business impact], [Strategic alignment]
**Source**: [Strategy/OKR]

### Process ("What's the process for X?")
**TL;DR**: [Step-by-step]
**Details**: [Timeline/SLAs]
**Source**: [Team wiki]

## Quick Formats

### Slack
```
**Q**: [Question]
**A**: [Direct answer in 1 sentence]
**Why**: [Key reason]
**Source**: [Where from]
**Action**: [What asker should do]
**Logged**: ✓
```

### Email
```
Hi [Name],
Quick answer: **[Question]**

**Answer**: [Direct answer]

**Reasoning**: [Bullet points]

**Source**: [Link]

**Your Next Steps**: [Actions]

Logged [here: link].
```

## Decision Logging Rules

**Always log**: Scope decisions, Priority decisions, Approach decisions, Policy creation
**Don't log**: Clarifications, Process explanations, Context, "How to"

## Best Practices

✅ **DO**: Be direct (yes/no first), be concise (2-3 sentences), reference source, check precedent, log decisions, provide context, give next steps, respond quickly, ask clarifying questions, escalate if unsure

❌ **DON'T**: Be vague ("it depends" without specifics), assume context, create new decisions solo, bury the answer, forget to log, give conflicting answers, over-explain, say "I think", leave them hanging, answer outside your area

**Related**: `/stakeholder-management:decision-log`, `/requirements-engineering:prd`, `/product-operations:status`
