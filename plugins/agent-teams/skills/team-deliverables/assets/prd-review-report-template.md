# PRD Review Report Template

Template for the final deliverable of a `/agent-teams:prd-stress-test` workflow.

---

## Template

```markdown
# PRD Stress Test Report: [PRD Title]

**Date**: [Date]
**PRD**: [File path or title]
**Version Reviewed**: [Version number if available]

---

## Executive Summary

[2-3 sentences. Is this PRD ready to build? What's the biggest issue?]

---

## Scores

| Dimension   | Score           | Reviewer             | Justification  |
| ----------- | --------------- | -------------------- | -------------- |
| Market Fit  | [X]/5           | market-fit-reviewer  | [One sentence] |
| Feasibility | [X]/5           | feasibility-reviewer | [One sentence] |
| Scope       | [X]/5           | scope-reviewer       | [One sentence] |
| **Overall** | **[Average]/5** |                      |                |

---

## Verdict: [READY TO BUILD / NEEDS REVISION / MAJOR REWORK]

[1-2 sentences explaining the verdict.]

---

## Blocking Issues (Must Fix Before Building)

[These must be resolved. Building without addressing these will lead to failure or significant rework.]

1. **[Issue]** (flagged by [reviewer]): [Description and why it's blocking]
2. **[Issue]** (flagged by [reviewer]): [Description and why it's blocking]

---

## Market Fit Review

### What's Strong

- [Positive finding with reasoning]
- [Positive finding with reasoning]

### What's Missing or Weak

- [Gap 1]: [What's missing and why it matters]
- [Gap 2]: [What's missing and why it matters]

### Questions the PRD Doesn't Answer

- [Question about target user/market]
- [Question about differentiation/positioning]

### Score Justification

[2-3 sentences explaining the market fit score]

---

## Feasibility Review

### What's Clear

- [Well-specified requirement or section]
- [Well-specified requirement or section]

### Ambiguous Requirements

- **[Requirement]** (Section [X]): [What's ambiguous and suggested fix]
- **[Requirement]** (Section [X]): [What's ambiguous and suggested fix]

### Missing Edge Cases

- [Edge case not covered]
- [Edge case not covered]

### Technical Risks

- [Risk 1]: [Likelihood and impact]
- [Risk 2]: [Likelihood and impact]

### Score Justification

[2-3 sentences explaining the feasibility score]

---

## Scope Review

### Scope Assessment

- **Current scope estimate**: [Rough effort estimate - weeks/months]
- **Recommended V1 scope**: [What should ship first]

### Feature Classification

| Feature     | Classification | Reasoning                          |
| ----------- | -------------- | ---------------------------------- |
| [Feature 1] | MUST-HAVE      | [Why it's essential for V1]        |
| [Feature 2] | MUST-HAVE      | [Why it's essential for V1]        |
| [Feature 3] | CUT FROM V1    | [Why it can wait]                  |
| [Feature 4] | CUT FROM V1    | [Why it can wait]                  |
| [Feature 5] | DEFER TO V2    | [Why it's valuable but not urgent] |

### Estimated Impact of Cuts

- Cutting [features] reduces scope by approximately [X]%
- Core value proposition preserved: [YES/NO - explanation]

### Score Justification

[2-3 sentences explaining the scope score]

---

## Reviewer Conflicts

[Where reviewers disagreed with each other]

### [Conflict Topic]

- **[Reviewer A]** says: [Position]
- **[Reviewer B]** says: [Opposing position]
- **Resolution**: [How this should be handled]

---

## Revision Checklist

[Ordered by priority. Check these off before building.]

### Must Fix (Blocking)

- [ ] [Specific revision with section reference]
- [ ] [Specific revision with section reference]

### Should Fix (Important)

- [ ] [Specific revision with section reference]
- [ ] [Specific revision with section reference]

### Nice to Fix (Polish)

- [ ] [Specific revision with section reference]
- [ ] [Specific revision with section reference]

---

## Dissenting Views

[If a reviewer's concerns were overruled in the overall verdict, document them here.]
```

---

## When to Use

- After completing all phases of a PRD stress test
- When synthesizing three review dimensions into a consolidated assessment
- As the final deliverable with an actionable revision checklist

## Best Practices

- Blocking issues should be genuinely blocking. Don't inflate minor concerns.
- The feature classification table is the most actionable part for scope decisions.
- Conflicts between reviewers are features, not bugs. Document them clearly.
- The revision checklist should be specific enough to hand to the PRD author as a to-do list.

## Related Templates

- `validation-verdict-template.md` - For validation sprints
- `competitive-synthesis-template.md` - For competitive war rooms

---

**Key Principle**: A PRD review that says "looks good" is worthless. Specific, actionable feedback with clear priority levels is what makes PRDs better.
