# Team Debate Patterns

Practical patterns for structuring multi-agent debate. Each pattern shapes how agents interact differently.

---

## Dialectical Inquiry

Two opposing positions built from the same data, debated to find a stronger synthesis. Neither position is assumed correct. Forces hidden assumptions to surface.

**Use when**: You suspect confirmation bias, the same data supports multiple interpretations, or the team is converging too quickly.

### Example: Validation Sprint

```
Data: Market research shows 15 competitors in the space, all with 3-4 star reviews.

Thesis (market-researcher): "Market validation. Lots of competitors means
real demand. Mediocre reviews mean opportunity to build something better."

Antithesis (idea-skeptic): "Crowded market. 15 competitors with loyal-enough
users means brutal customer acquisition. Mediocre reviews might mean the
problem isn't painful enough for anyone to get right."

Synthesis: "Demand exists, but differentiation is critical. Success depends
on identifying a specific underserved segment rather than competing broadly.
Mediocre reviews need investigation: is it a solvable UX problem or an
inherent limitation of the approach?"
```

**Pitfall**: Synthesis that's just "the truth is somewhere in the middle" without specificity. The synthesis must take a position.

---

## Devil's Advocacy

One designated agent systematically tries to kill the proposal. The role is assigned, not organic, which gives the agent permission to be adversarial.

**Use when**: Idea validation, PRD review, strategy review, any high-investment decision.

### Strong vs Weak Attacks

**Strong** (must be answered):
- "Your TAM calculation assumes 20% market penetration, but the average SaaS in this category captures 2-5%. At 5%, your market is $2M, which doesn't support a sustainable business."
- "Three of your five competitors launched this exact feature in the last 6 months. What's your evidence that your version will be meaningfully different?"

**Weak** (don't waste a round):
- "What if nobody wants this?" (too vague)
- "The market could change" (always true, not actionable)
- "This seems hard to build" (not specific about what's hard)

**The skeptic's obligation**: Be specific, provide evidence, acknowledge when a response adequately addresses your concern, and be willing to say "I tried to kill this and couldn't."

---

## Constructive Controversy

Agents with genuinely different expertise examine the same question from their domain. Their natural expertise creates productive tension because they value different things.

**Use when**: Multi-dimensional decisions where no single perspective is sufficient.

### Example: PRD Stress Test

```
Question: Is this PRD ready to build?

market-fit-reviewer: "The market need is clear but the positioning is
vague. Who exactly is this for? The PRD says 'developers' but that's
not a segment."

feasibility-reviewer: "Requirements are mostly clear but Section 3
has ambiguous acceptance criteria. 'Fast' isn't a requirement. 'Under
200ms p95' is a requirement."

scope-reviewer: "This is a 6-month build disguised as a 6-week MVP.
Cut features 4-7 entirely. Ship features 1-3, learn, then decide."

Integration: "NEEDS REVISION. Narrowing the target segment will
clarify both market fit AND scope. Tightening acceptance criteria
fixes feasibility concerns. Cutting scope to features 1-3 makes
the timeline realistic."
```

**Why differences are valuable**: When agents disagree, it usually means different priorities (market fit vs effort), different risk tolerances (technical risk vs time risk), or missing information one agent found that others missed. The synthesis should explain WHY agents differed.

---

## Choosing the Right Pattern

| Pattern                  | Best For                        | Agent Teams Use                                   |
| ------------------------ | ------------------------------- | ------------------------------------------------- |
| Dialectical Inquiry      | Same data, opposite conclusions | Validation sprint (researcher vs. skeptic)        |
| Devil's Advocacy         | Stress-testing proposals        | Validation sprint (idea-skeptic role), PRD review |
| Constructive Controversy | Multi-dimensional analysis      | PRD stress test, competitive war room             |

Most workflows combine patterns:
- **Validation Sprint**: Constructive Controversy (three perspectives) + Devil's Advocacy (idea-skeptic role)
- **PRD Stress Test**: Constructive Controversy (three review dimensions) + cross-referencing phase
- **Competitive War Room**: Parallel investigation + Constructive Controversy synthesis
