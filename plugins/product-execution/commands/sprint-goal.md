# Sprint Goal Generator

Create inspiring, achievable sprint goals that align teams and tie to broader product strategy.

## Usage

```
/pm:sprint-goal [sprint number/name] [optional: theme or key stories]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Generates clear, inspiring sprint goals from planned work
2. Connects sprint goals to product strategy and OKRs
3. Ensures goals are achievable and measurable
4. Provides both team-facing and stakeholder-facing versions
5. Helps maintain focus throughout the sprint

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Sprint Basics**:
- What's the sprint number or name? (Sprint 42, Q1 Sprint 3, "Mobile Polish Sprint")
- What are the sprint dates? (start and end date, to calculate timeline)
- What team is this for? (team name, product area)
- What's the sprint length? (1 week, 2 weeks, 3 weeks)

**Planned Work**:
- What stories or features are planned for this sprint? (list of key items from backlog)
- What's the total capacity or story points? (to assess achievability)
- Are there any carry-over items from last sprint? (incomplete work)
- Is there dedicated time for bugs, tech debt, or support? (affects capacity for goal)

**Strategic Context**:
- What OKR or roadmap theme does this sprint support? (how it connects to bigger picture)
- What's the quarterly goal? (to align sprint goal)
- Is this part of a multi-sprint initiative? (phase 1 of 3, final sprint before launch)
- Are there any customer commitments or deadlines? (external pressure or promise)

**Team Context**:
- What did the team accomplish last sprint? (momentum, velocity, learnings)
- Are there any team capacity constraints? (PTO, holidays, new team members ramping)
- What's the team's current focus? (new features, stabilization, tech debt paydown)
- Is there a specific theme the team is excited about? (leverage motivation)

**User/Customer Impact**:
- Who benefits from this sprint's work? (which user segment or customer type)
- What capability or outcome does this enable? (the "so that" part of user story)
- How does this improve the product? (faster, more reliable, new capability, better UX)
- Is this a visible change or under-the-hood improvement? (affects goal framing)

**Success Criteria**:
- What must be done for the sprint to be considered successful? (definition of done)
- What can be demoed at sprint review? (tangible outcomes)
- What would make this sprint a failure? (to set realistic expectations)

**Previous Sprint Context** (if applicable):
- What was last sprint's goal? (for continuity)
- Was last sprint's goal achieved? (learn from success/failure)
- Are there any blockers or risks from last sprint? (to address)

### 2. **Identify Core Theme**:
   - What's the one thing this sprint accomplishes?
   - What capability does the team ship?
   - What outcome do we enable for users/business?
   - How does it move us closer to quarterly goals?

3. **Craft Goal Statement**:
   - **One sentence** - Easy to remember
   - **Outcome-focused** - What users can do, not what we build
   - **Inspiring** - Energizes the team
   - **Achievable** - Realistic given capacity
   - **Measurable** - Clear success criteria

4. **Add Success Criteria**:
   - 3-5 concrete criteria
   - Mix of shipped features and outcomes
   - Testable/demoable

## Sprint Goal Formula

**Structure**: [User/Customer] can [outcome/capability] [qualifier/benefit]

**Examples**:
- "Beta users can invite teammates and collaborate in real-time"
- "Enterprise customers can single sign-on with their company credentials"
- "Power users can create and share custom dashboards"
- "Mobile users can complete core workflows offline"

**Avoid vague goals**:
- ❌ "Make progress on authentication"
- ❌ "Work on dashboard improvements"
- ❌ "Fix bugs and tech debt"

## Template

```markdown
# Sprint [N] Goal

**Sprint**: [N] | **Dates**: [Start - End] | **Team**: [Name]

---

## Sprint Goal

**Goal**: [One sentence - what we're achieving]

Example: "Enable users to search and filter product catalog by category and price"

---

## Why This Matters

**Strategic Alignment**: [How this ties to OKRs/roadmap]
**User Impact**: [What users can do that they couldn't before]
**Business Value**: [Metric we're moving or problem we're solving]

---

## Success Criteria

Sprint is successful if:
- [ ] [Criterion 1 - measurable]
- [ ] [Criterion 2 - measurable]
- [ ] [Criterion 3 - measurable]

---

## What's In Scope

**Stories Contributing to Goal**:
- [Story 1] - [How it contributes]
- [Story 2] - [How it contributes]

**Total**: [X] points toward goal

**Other Work** (not goal-related):
- [Story Y] - [Z] points (tech debt/bug fixes/etc)

---

## What's NOT in Scope

Explicitly excluding:
- [Item 1] - Deferred to Sprint [N+1]
- [Item 2] - Out of scope for this goal

---

## Risks

- 🟡 [Risk 1]: [Description] - Mitigation: [Plan]
- 🟡 [Risk 2]: [Description] - Mitigation: [Plan]
```

## Best Practices

✅ **DO**: One goal per sprint, make it specific and measurable, tie to business value, get team buy-in, focus 70-80% of capacity on goal, allow some non-goal work (bugs/tech debt), communicate goal to stakeholders, review goal daily in standup

❌ **DON'T**: Multiple goals (dilutes focus), vague goals ("improve quality"), goal that's just a list of stories, 100% capacity on goal (no flexibility), change goal mid-sprint without team agreement, forget to celebrate when goal achieved

**Related**: `/pm:sprint-plan`, `/pm:okr`
