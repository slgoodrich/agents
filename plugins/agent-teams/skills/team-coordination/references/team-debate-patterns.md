# Team Debate Patterns: Deep Dive

Frameworks for structuring productive multi-agent debate, drawn from organizational decision-making research.

---

## Table of Contents

- [Dialectical Inquiry](#dialectical-inquiry)
- [Devil's Advocacy](#devils-advocacy)
- [Constructive Controversy](#constructive-controversy)
- [Choosing the Right Pattern](#choosing-the-right-pattern)
- [Applying Patterns to Agent Teams](#applying-patterns-to-agent-teams)

---

## Dialectical Inquiry

### What It Is

Two opposing positions are developed from the same data, then debated to find a stronger synthesis. Neither position is assumed correct. The goal is to surface hidden assumptions by forcing the same evidence to support contradictory conclusions.

### How It Works

1. **Present the data**: All agents receive the same information
2. **Thesis**: Agent A builds the strongest case FOR the proposition
3. **Antithesis**: Agent B builds the strongest case AGAINST, using the same data
4. **Structured debate**: Each side challenges the other's interpretation
5. **Synthesis**: A third agent (or the lead) integrates the strongest arguments from both sides

### When to Use

- When you suspect confirmation bias in initial analysis
- When the same data could support multiple interpretations
- When the decision has high stakes and reversal cost is high
- When the team is converging too quickly on one answer

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

### Pitfalls

- Agents treating the exercise as roleplay rather than genuine analysis
- Thesis and antithesis becoming straw men instead of steel men
- Synthesis that's just "the truth is somewhere in the middle" without specificity

---

## Devil's Advocacy

### What It Is

One designated agent's job is to find every reason the proposal should fail. This isn't about being negative. It's about systematic stress-testing. The devil's advocate role is assigned, not organic, which gives the agent permission to be adversarial without social cost.

### How It Works

1. **Proposal presented**: The idea, PRD, or strategy is laid out
2. **Advocates analyze**: Agents investigate from supportive angles
3. **Devil's advocate attacks**: One agent systematically tries to kill the proposal
4. **Attack patterns** (use at least 3):
   - Market viability: "Who specifically would pay for this?"
   - Competitive moat: "What if [incumbent] adds this feature tomorrow?"
   - Execution risk: "Your timeline assumes everything goes right. What breaks first?"
   - User adoption: "This requires users to change behavior. What's the switching cost?"
   - Business model: "Your unit economics only work at scale. How do you survive until then?"
   - Category risk: "This is a vitamin, not a painkiller. Users won't prioritize it."
5. **Response round**: Other agents respond to the strongest attacks
6. **Verdict**: Attacks that weren't adequately answered become documented risks

### When to Use

- Idea validation (the `idea-skeptic` agent embodies this)
- PRD review (finding fatal flaws before building)
- Strategy review (challenging strategic assumptions)
- Any high-investment decision where confirmation bias is a risk

### Attack Quality Standards

**Strong attacks** (must be answered):

- "Your TAM calculation assumes 20% market penetration, but the average SaaS in this category captures 2-5%. At 5%, your market is $2M, which doesn't support a sustainable business."
- "Three of your five competitors launched this exact feature in the last 6 months. What's your evidence that your version will be meaningfully different?"

**Weak attacks** (don't waste a round):

- "What if nobody wants this?" (too vague, no evidence)
- "The market could change" (always true, not actionable)
- "This seems hard to build" (not specific about what's hard)

### The Skeptic's Obligation

The devil's advocate must:

- Be specific about what's wrong and why
- Provide evidence or reasoning for each attack
- Acknowledge when a response adequately addresses their concern
- Note which attacks they consider "fatal" vs. "concerning"
- Be willing to say "I tried to kill this idea and couldn't" when the evidence is strong

---

## Constructive Controversy

### What It Is

Agents with genuinely different expertise examine the same question from their domain. Unlike dialectical inquiry, they're not artificially assigned opposing positions. Their natural expertise creates productive tension because they value different things.

### How It Works

1. **Frame the question**: Define what needs to be decided
2. **Independent analysis**: Each agent analyzes from their expertise
3. **Share and compare**: Agents present findings, noting where they differ
4. **Explore differences**: Rather than debating who's "right," explore WHY perspectives differ
5. **Integrate**: Build a recommendation that accounts for all dimensions

### When to Use

- PRD stress testing (market fit vs. feasibility vs. scope are naturally different lenses)
- Competitive analysis (different agents emphasize different competitive dimensions)
- Any multi-dimensional decision where no single perspective is sufficient

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

### Why Differences Are Valuable

When agents disagree, it usually means:

- **Different priorities**: Market fit cares about demand, scope cares about effort. Both are valid.
- **Different risk tolerances**: Feasibility flags technical risk, scope flags time risk. Both matter.
- **Missing information**: One agent found something the others missed.

The synthesis should explain WHY agents differed, not just that they differed.

---

## Choosing the Right Pattern

| Pattern                  | Best For                        | Agent Teams Use                                   |
| ------------------------ | ------------------------------- | ------------------------------------------------- |
| Dialectical Inquiry      | Same data, opposite conclusions | Validation sprint (researcher vs. skeptic)        |
| Devil's Advocacy         | Stress-testing proposals        | Validation sprint (idea-skeptic role), PRD review |
| Constructive Controversy | Multi-dimensional analysis      | PRD stress test, competitive war room             |

### Pattern Combinations

Most team workflows use a combination:

**Validation Sprint**: Constructive Controversy (three perspectives) + Devil's Advocacy (idea-skeptic role)

**PRD Stress Test**: Constructive Controversy (three review dimensions) + Cross-referencing phase

**Competitive War Room**: Parallel investigation + Constructive Controversy synthesis

---

## Applying Patterns to Agent Teams

### Pre-Debate Setup

1. Each agent receives a clear brief: what to investigate and what to deliver
2. Agents work independently in parallel (no cross-contamination)
3. Time-box the investigation phase to prevent scope creep

### During Cross-Examination

1. Each agent reads the other agents' full reports
2. Each agent selects their 2-3 strongest challenges
3. Challenges must cite specific claims from the reports
4. One round only. Make it count.

### During Synthesis

1. Lead agent reads all reports AND all cross-examination challenges
2. Identify convergence points (where independent analysis agreed)
3. Identify divergence points (where analysis disagreed)
4. For each divergence: determine if it's resolvable or genuine uncertainty
5. Render a verdict with explicit reasoning
6. Document dissent and unresolved tensions

### Post-Debate

1. Deliver the synthesized report to the user
2. Highlight areas where the team was uncertain
3. Recommend specific next steps to resolve uncertainty
4. Offer to save findings to product context files

---

**Remember**: The best debates produce conclusions that no single agent would have reached alone. If the synthesis is identical to any one agent's initial position, the debate didn't add value.
