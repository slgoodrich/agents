# Ticket Review

Quick, structured review of PRs, tickets, designs, and specs with context recall and actionable feedback.

## Usage

```
/agile-coaching:ticket-review [ticket/PR URL or description] [optional: review type]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Provides fast, structured reviews of work items
2. Recalls relevant context (PRD, requirements, decisions)
3. Checks completeness against acceptance criteria
4. Gives actionable, specific feedback
5. Approves, requests changes, or asks questions
6. Takes 5-10 minutes vs 15-20 minutes of context switching

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**What's Being Reviewed**:
- What type of review? (PR/code review, design review, ticket/story review, technical spec, test plan, release checklist)
- What's the ticket/PR number or identifier? (JIRA-123, PR #456, Figma link)
- What's the title or summary of what's being reviewed?
- Who created it? (author name, team, stakeholder)

**Context & Background**:
- What feature or epic is this part of? (so you can check alignment)
- Is there a related PRD or spec? (link or name - to verify against requirements)
- What are the acceptance criteria? (from ticket, PRD, or definition of done)
- Are there related decisions or constraints? (decision log entries, technical decisions, business rules)

**Review Scope**:
- What specifically should be reviewed? (full review vs quick check for specific issue)
- Is there a particular concern or question? (performance, accessibility, completeness, etc.)
- What's the urgency? (blocking deploy, sprint planning, just feedback)
- Who needs the review? (developer waiting, designer needs approval, stakeholder requesting)

**Standards & Requirements**:
- What standards should this meet? (design system, coding standards, accessibility requirements)
- Are there specific checklists to use? (Definition of Ready, Definition of Done, brand guidelines)
- What's the approval criteria? (what makes this "approved" vs "changes requested")

**Previous Reviews** (if applicable):
- Has this been reviewed before? (is this a re-review after changes)
- What feedback was given previously? (to check if addressed)
- Are there outstanding questions from last review?

### 2. Identify Review Type
   - **PR (Code Review)** - Pull request for feature/fix
   - **Design Review** - Figma, mockups, prototypes
   - **Ticket Review** - Jira/Linear story before dev starts
   - **Spec Review** - Technical spec or PRD
   - **Test Plan Review** - QA test plan
   - **Release Review** - Pre-launch checklist

3. **Gather Context**:
   - What is being reviewed
   - Related PRD or spec
   - Acceptance criteria
   - Previous decisions
   - Similar past reviews

3. **Review Against Criteria**:
   - **Completeness** - All requirements met?
   - **Quality** - Meets standards?
   - **Alignment** - Matches intent?
   - **Edge cases** - Handled?
   - **Documentation** - Updated?

4. **Provide Structured Feedback**:
   - **Strengths** - What's done well
   - **Required Changes** - Must fix before approve
   - **Suggestions** - Nice-to-haves
   - **Questions** - Need clarification

## Template

```markdown
# Review: [Ticket ID] - [Title]

**Type**: PR|Ticket|Design|Spec|Test Plan | **Reviewer**: [Name] | **Date**: [Date]

---

## Summary

**What's Being Reviewed**: [Brief description]
**Status**: ✅ Approved | 🟡 Approved with Changes | 🔴 Changes Requested

---

## Checklist

### Completeness
- [ ] Acceptance criteria met
- [ ] Edge cases handled
- [ ] Error states covered
- [ ] Documentation updated

### Quality
- [ ] Code/design quality good
- [ ] Tests included and passing
- [ ] Performance acceptable
- [ ] Accessibility considered

### Requirements
- [ ] Matches spec/requirements
- [ ] User experience smooth
- [ ] No scope creep
- [ ] Breaking changes documented

---

## Feedback

### ✅ What's Good
- [Positive feedback 1]
- [Positive feedback 2]

### 🟡 Suggested Changes
- [Suggestion 1] - Priority: High|Medium|Low
- [Suggestion 2] - Priority: High|Medium|Low

### 🔴 Required Changes
- [Required change 1] - Blocker for approval
- [Required change 2] - Blocker for approval

---

## Next Steps

- [ ] [Owner] - [Action] - [By when]

**Re-review needed**: Yes|No
```

## Best Practices

✅ **DO**: Review promptly (<24hrs), be specific ("line 42: validate input" vs "needs validation"), balance positive with constructive, explain why for changes, check ACs first, test it yourself, consider edge cases, suggest alternatives

❌ **DON'T**: Nitpick (focus on substance), approve without testing, skip context check, be vague ("needs work"), personal criticism, approve with unresolved blockers, forget to re-review after changes

**Related**: `/requirements-engineering:user-stories`, `/requirements-engineering:prd`
