# Validation Verdict Template

Template for the final deliverable of a `/agent-teams:validation-sprint` workflow.

---

## Template

```markdown
# Validation Verdict: [Idea Name / One-Line Description]

**Date**: [Date]
**Idea**: [Brief description of the idea being validated]

---

## Executive Summary

[2-3 sentences. What did the team find? What's the verdict? What's the single most important thing to know?]

---

## Scores

| Dimension          | Score            | Justification                  |
| ------------------ | ---------------- | ------------------------------ |
| User Problem       | [X]/10           | [One sentence: why this score] |
| Market Opportunity | [X]/10           | [One sentence: why this score] |
| Defensibility      | [X]/10           | [One sentence: why this score] |
| **Overall**        | **[Average]/10** |                                |

---

## Verdict: [BUILD / DON'T BUILD / NEEDS MORE EVIDENCE]

[1-2 sentences explaining the verdict. If conditional, state the conditions.]

---

## User Problem Analysis (idea-researcher)

### Key Findings

- [Finding 1 with evidence]
- [Finding 2 with evidence]
- [Finding 3 with evidence]

### Evidence Strength

- **Strong evidence**: [What we're confident about]
- **Gaps**: [What we don't know yet]

### Confidence: [HIGH / MEDIUM / LOW]

---

## Market Opportunity Analysis (market-researcher)

### Key Findings

- [Market size estimate with methodology]
- [Competitive landscape summary]
- [Timing assessment]

### Evidence Strength

- **Strong evidence**: [What WebSearch confirmed]
- **Gaps**: [Data not publicly available]

### Confidence: [HIGH / MEDIUM / LOW]

---

## Skeptic's Case (idea-skeptic)

### Top Attacks

1. **[Attack name]**: [Specific argument against the idea with evidence]
2. **[Attack name]**: [Specific argument against the idea with evidence]
3. **[Attack name]**: [Specific argument against the idea with evidence]

### Attacks That Were Answered

- [Attack]: Addressed by [which agent] because [evidence]

### Attacks That Stand

- [Attack]: Remains a risk because [reasoning]

### Skeptic's Final Assessment

[Did the idea survive scrutiny? What's the skeptic's honest take?]

---

## Cross-Examination Highlights

### Where the Team Agreed

- [Convergence point 1]
- [Convergence point 2]

### Where the Team Disagreed

- **[Topic]**: [Agent A] said [X], [Agent B] said [Y]. Resolution: [resolved/unresolved]

### Strongest Challenge

[The single most impactful challenge raised during cross-examination and how it was handled]

---

## Key Risks

| Risk     | Severity       | Mitigation       |
| -------- | -------------- | ---------------- |
| [Risk 1] | [HIGH/MED/LOW] | [How to address] |
| [Risk 2] | [HIGH/MED/LOW] | [How to address] |
| [Risk 3] | [HIGH/MED/LOW] | [How to address] |

---

## Recommended Next Steps

### If BUILD:

1. [Specific next step - e.g., "Run 5 problem discovery interviews with [target segment]"]
2. [Specific next step - e.g., "Build landing page to test conversion"]
3. [Specific next step - e.g., "Scope MVP to [core features]"]

### If DON'T BUILD:

1. [What to do instead - pivot direction, alternative ideas, or park it]

### If NEEDS MORE EVIDENCE:

1. [Specific research to conduct]
2. [What would change the verdict to BUILD]
3. [What would change the verdict to DON'T BUILD]

---

## Dissenting Views

[If any agent strongly disagreed with the verdict, document their position here. If all agents aligned, note that convergence.]
```

---

## When to Use

- After completing all phases of a validation sprint
- When synthesizing parallel investigation findings into a go/no-go recommendation
- As the final deliverable presented to the user

## Best Practices

- Fill in scores BEFORE writing the verdict to avoid anchoring
- Be specific in justifications. "Market is big" is useless. "TAM estimated at $X based on [method]" is useful.
- The skeptic's section is the most valuable part. Don't soft-pedal it.
- Next steps should be specific enough that someone could act on them today

## Related Templates

- `prd-review-report-template.md` - For PRD stress tests
- `competitive-synthesis-template.md` - For competitive war rooms

---

**Key Principle**: A verdict without reasoning is just an opinion. Every score and recommendation must trace back to evidence from the investigation.
