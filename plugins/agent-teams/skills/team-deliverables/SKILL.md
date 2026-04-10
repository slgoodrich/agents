---
name: team-deliverables
description: "Output templates and scoring rubrics for multi-agent team workflows. Use when generating final deliverables from agent team debates, formatting validation verdicts, or scoring PRD reviews. Trigger on: 'format the team output', 'validation verdict template', 'PRD review report format', 'competitive synthesis template', 'scoring rubric'."
---

# Team Deliverables

Templates and scoring rubrics for the final outputs of multi-agent team workflows.

## When to Use This Skill

**Auto-loaded by all six agents**:

- `idea-researcher`, `market-researcher`, `idea-skeptic` - For validation verdict and competitive synthesis scoring rubrics
- `market-fit-reviewer`, `feasibility-reviewer`, `scope-reviewer` - For PRD review report scoring rubrics

**Use when you need**:

- Generating the final output of a team workflow
- Scoring ideas, PRDs, or competitive positions
- Structuring multi-perspective findings into a single deliverable
- Ensuring consistent output format across team workflows

## Template Selection Guide

| Command                             | Template              | When                                          |
| ----------------------------------- | --------------------- | --------------------------------------------- |
| `/agent-teams:validation-sprint`    | Validation Verdict    | After cross-examination of idea investigation |
| `/agent-teams:prd-stress-test`      | PRD Review Report     | After cross-referencing PRD review dimensions |
| `/agent-teams:competitive-war-room` | Competitive Synthesis | After parallel competitor deep-dives          |

---

## Scoring Rubrics

### Validation Sprint Scores (1-10)

**User Problem Score**

| Score | Meaning                                                                                    |
| ----- | ------------------------------------------------------------------------------------------ |
| 1-2   | No evidence of real user pain. Problem is theoretical.                                     |
| 3-4   | Some users mention this, but it's a mild annoyance. Existing solutions work "well enough." |
| 5-6   | Real problem, but unclear severity or frequency. Some workarounds exist.                   |
| 7-8   | Clear, validated pain point. Users actively seeking solutions. Workarounds are inadequate. |
| 9-10  | Hair-on-fire problem. Users spending significant time/money on bad workarounds.            |

**Market Opportunity Score**

| Score | Meaning                                                                                    |
| ----- | ------------------------------------------------------------------------------------------ |
| 1-2   | Tiny niche. No evidence of willingness to pay. Market too small to sustain a business.     |
| 3-4   | Small market or crowded space with no clear differentiation angle.                         |
| 5-6   | Viable market but competitive. Differentiation possible but unproven.                      |
| 7-8   | Attractive market with clear gaps. Evidence of willingness to pay. Timing is right.        |
| 9-10  | Large, growing market with underserved segments. Strong demand signals. Clear entry point. |

**Defensibility Score**

| Score | Meaning                                                                                 |
| ----- | --------------------------------------------------------------------------------------- |
| 1-2   | No moat. Any competitor could copy this in weeks. Pure feature play.                    |
| 3-4   | Weak differentiation. First-mover advantage only, which isn't a moat.                   |
| 5-6   | Some defensibility through domain expertise, data, or network effects. Not bulletproof. |
| 7-8   | Strong differentiation with compounding advantages. Switching costs for users.          |
| 9-10  | Deep moat. Proprietary data, strong network effects, or structural advantage.           |

### PRD Review Scores (1-5)

**Market Fit Score**

| Score | Meaning                                                                                                |
| ----- | ------------------------------------------------------------------------------------------------------ |
| 1     | No clear target user or problem. Fundamental market questions unanswered.                              |
| 2     | Target user defined but problem validation missing. "If you build it, will they come?" is unaddressed. |
| 3     | Problem and user are clear, but differentiation is weak. Could be any competitor's PRD.                |
| 4     | Strong problem-solution fit. Clear differentiation. Minor positioning gaps.                            |
| 5     | Excellent. Clear user, validated problem, sharp differentiation, compelling value prop.                |

**Feasibility Score**

| Score | Meaning                                                                                                        |
| ----- | -------------------------------------------------------------------------------------------------------------- |
| 1     | Major technical unknowns. Requirements are vague or contradictory. Can't estimate effort.                      |
| 2     | Core approach is clear but many requirements are ambiguous. Multiple "TBD" sections.                           |
| 3     | Mostly clear. Some edge cases missing, some acceptance criteria need tightening. Buildable with clarification. |
| 4     | Clear requirements, well-defined acceptance criteria. Minor gaps. Ready for engineering review.                |
| 5     | Precise, testable requirements. Edge cases covered. Acceptance criteria are specific and measurable.           |

**Scope Score**

| Score | Meaning                                                                                      |
| ----- | -------------------------------------------------------------------------------------------- |
| 1     | Massive scope. Years of work presented as an MVP. No prioritization visible.                 |
| 2     | Too much for V1. Some nice-to-haves mixed in with must-haves. Needs significant cutting.     |
| 3     | Reasonable but could be tighter. A few features could be deferred without losing core value. |
| 4     | Well-scoped. Clear must-haves, reasonable timeline. Only minor fat to trim.                  |
| 5     | Ruthlessly scoped. 3-5 core features. Clear what's in V1 vs. later. Ships fast.              |

---

## Template Standards

### Required Elements in Every Deliverable

1. **Header**: Command name, date, subject (idea/PRD/competitors)
2. **Scores**: Numerical scores with brief justification
3. **Verdict**: Clear recommendation (BUILD / DON'T BUILD / READY / NEEDS REVISION / etc.)
4. **Evidence**: Key findings from each agent's investigation
5. **Conflicts**: Where agents disagreed and why
6. **Next Steps**: Specific, actionable recommendations

### Formatting Rules

- Use tables for scores (scannable)
- Use bullet points for findings (not paragraphs)
- Bold the verdict and any blocking issues
- Keep the executive summary under 5 lines
- Put detailed evidence in expandable sections when the report is long

---

## Ready-to-Use Resources

### In `assets/`:

- **validation-verdict-template.md**: Go/No-Go format with three perspectives for validation sprints
- **prd-review-report-template.md**: Multi-dimensional review with conflicts section for PRD stress tests
- **competitive-synthesis-template.md**: Positioning map and battle cards format for competitive war rooms

---

## Troubleshooting

**"The template doesn't fit our findings"**: Adapt it. Drop sections that add nothing, expand sections where you have depth. A template that forces empty placeholder text is worse than no template. The structure is a starting point, not a constraint.

**"Scores across reviewers aren't comparable"**: Check that all reviewers used the same rubric anchors. A 4/5 from one reviewer should mean the same thing as a 4/5 from another. If they're using different mental scales, re-calibrate by sharing the rubric definitions before the next run.

**"The verdict is ambiguous (BUILD IF with too many conditions)"**: That usually means the idea needs more validation, not a conditional pass. If there are more than 3 conditions, downgrade to NEEDS MORE EVIDENCE and list what to validate next.

---

## Related

- `/agent-teams:validation-sprint` - Produces validation verdicts using these templates
- `/agent-teams:prd-stress-test` - Produces PRD review reports using these templates
- `/agent-teams:competitive-war-room` - Produces competitive syntheses using these templates
- `team-coordination` - Debate and synthesis protocols that feed into these deliverables

---

**Remember**: Templates create consistency, not rigidity. Adapt sections when the findings demand it. A template that forces you to fill in blanks with nothing useful is worse than no template.
