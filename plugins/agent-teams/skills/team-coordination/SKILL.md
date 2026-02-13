---
name: team-coordination
description: Structured debate protocols, cross-examination patterns, and synthesis techniques for multi-agent team workflows. Use when coordinating agent teams for idea validation, PRD review, or competitive analysis. Covers dialectical inquiry, devil's advocacy, constructive controversy, and consensus-building frameworks.
---

# Team Coordination

Protocols for structuring productive debate, cross-examination, and synthesis across multi-agent teams.

## Table of Contents

- [When to Use This Skill](#when-to-use-this-skill)
- [Core Principle: Structured Disagreement Produces Better Decisions](#core-principle)
- [Debate Protocol](#debate-protocol)
- [Cross-Examination Patterns](#cross-examination-patterns)
- [Consensus vs. Dissent Handling](#consensus-vs-dissent-handling)
- [Synthesis Patterns](#synthesis-patterns)
- [Team Communication Standards](#team-communication-standards)
- [Common Anti-Patterns](#common-anti-patterns)
- [Ready-to-Use Resources](#ready-to-use-resources)

## When to Use This Skill

**Auto-loaded by agents**:

- `idea-researcher` - For structured debate in validation sprints
- `market-researcher` - For cross-examination in validation sprints and war rooms
- `idea-skeptic` - For devil's advocacy protocols
- `market-fit-reviewer` - For cross-referencing in PRD stress tests
- `feasibility-reviewer` - For cross-referencing in PRD stress tests
- `scope-reviewer` - For cross-referencing in PRD stress tests

**Use when you need**:

- Running multi-agent team workflows
- Structuring productive debate between agents
- Cross-examining findings from parallel investigations
- Synthesizing multiple perspectives into a verdict
- Handling disagreements between team members
- Building consensus or documenting dissent

## Core Principle: Structured Disagreement Produces Better Decisions

Solo decision-making has blind spots. But unstructured debate is just noise. The sweet spot is structured disagreement: agents with different perspectives challenge each other using evidence, following clear protocols that force productive conflict.

**Not this**: Three agents agreeing with each other to be polite.
**This**: Three agents stress-testing each other's conclusions with pointed questions and evidence.

The goal isn't agreement. It's a well-examined conclusion where every weakness has been probed.

---

## Debate Protocol

### Phase Structure

Every team debate follows three phases:

**1. Independent Investigation**
Each agent works in parallel on their assigned dimension. No cross-talk. This prevents groupthink and ensures genuinely independent perspectives.

- Each agent produces a structured finding report
- Reports include evidence, confidence levels, and key claims
- No agent sees another's work until investigation completes

**2. Cross-Examination**
Agents receive each other's findings and challenge them. One round of structured challenges. Each agent must:

- Cite specific claims from other agents' reports
- Challenge with evidence, not opinion
- Ask pointed questions that could change the conclusion
- Acknowledge when another agent's evidence is strong

**3. Synthesis**
The lead agent compiles all perspectives into a final deliverable. Must:

- Represent all perspectives accurately
- Note where agents agreed (convergence)
- Note where agents disagreed (divergence) and why
- Make a final recommendation with explicit reasoning
- Flag unresolved tensions rather than papering over them

### Debate Rules

1. **Evidence over assertion**. "I think this won't work" is weak. "Users in similar markets showed 3% conversion rates [source], suggesting this won't work" is strong.

2. **Steel-man before attacking**. Before challenging a claim, restate it in its strongest form. This proves you understood it.

3. **One round, make it count**. Cross-examination is a single round. Agents can't go back and forth endlessly. This forces precision.

4. **Disagree and commit**. After synthesis, the verdict stands even if an agent disagrees. But dissent gets documented, not silenced.

5. **No false consensus**. If agents genuinely disagree, the synthesis says so. "Researchers disagreed on X. Here's why." is better than pretending everyone agreed.

---

## Cross-Examination Patterns

### Challenge Formats

When examining another agent's findings, use these question structures:

**Evidence Challenge**

> "You claim [X]. What evidence supports this beyond [the single source you cited]? If that source is wrong, does your conclusion still hold?"

**Assumption Challenge**

> "Your analysis assumes [Y]. What happens to your conclusion if [Y] is false? Is there evidence that [Y] might not hold?"

**Magnitude Challenge**

> "You identified [risk/opportunity]. How significant is this really? Is this a deal-breaker or a minor concern? What's the actual impact?"

**Alternative Explanation**

> "You attribute [outcome] to [cause]. Could [alternative cause] explain this equally well? Have you considered [different framing]?"

**So-What Challenge**

> "You found [data point]. What does this actually mean for the decision we're making? How should this change our recommendation?"

### Challenge Quality Standards

**Strong challenge** (changes the conversation):

- Cites specific evidence that contradicts the claim
- Identifies an assumption the agent didn't examine
- Presents an alternative explanation with supporting data
- Asks a question the agent should have answered but didn't

**Weak challenge** (wastes a round):

- "I'm not sure about that" (no evidence)
- Repeating your own findings without engaging the other agent's
- Nitpicking minor points while ignoring major claims
- Asking rhetorical questions that don't demand real answers

---

## Consensus vs. Dissent Handling

### When Agents Agree

Document the convergence explicitly:

```
## Convergence Points
All three perspectives agree on:
1. [Finding] - Supported by [evidence from each agent]
2. [Finding] - Supported by [evidence from each agent]

Confidence: HIGH (independent analyses converged)
```

Agreement from independent investigation is a strong signal. It means the conclusion is robust across different analytical lenses.

### When Agents Disagree

Not all disagreements need resolution. Some reflect genuine uncertainty.

**Resolvable disagreements** (one agent has stronger evidence):

```
## Resolved Disagreement: [Topic]
- Agent A claimed [X] based on [evidence]
- Agent B claimed [Y] based on [evidence]
- Resolution: Agent A's position is stronger because [reasoning]
- Agent B's concern remains valid as a risk to monitor
```

**Unresolvable disagreements** (genuine uncertainty):

```
## Unresolved: [Topic]
- Agent A: [Position] based on [evidence]
- Agent B: [Opposing position] based on [evidence]
- Why it's unresolved: [Explanation - insufficient data, different frameworks, etc.]
- Implication: This uncertainty should factor into risk assessment
- Recommended action: [How to resolve - more research, user testing, etc.]
```

### Dissent Documentation

When the synthesis verdict goes against one agent's recommendation:

```
## Dissenting View: [Agent Name]
[Agent] recommends [alternative] because [reasoning].
This dissent is noted because [why it matters].
The majority verdict differs because [reasoning].
If [condition], revisit this dissent.
```

---

## Synthesis Patterns

### Weighted Synthesis

When combining perspectives with different relevance:

1. Assign weight to each perspective based on the decision being made
2. For idea validation: User Problem (40%), Market Opportunity (30%), Defensibility (30%)
3. For PRD review: Market Fit (35%), Feasibility (35%), Scope (30%)
4. Weights are guidelines, not formulas. Override when evidence demands it.

### Narrative Synthesis

Don't just list findings. Tell the story:

1. **What we investigated** (the question)
2. **What we found** (key findings from each perspective)
3. **Where we agree** (convergence points)
4. **Where we disagree** (divergence points)
5. **What it means** (interpretation and verdict)
6. **What to do next** (recommended actions)

### Verdict Framework

Every synthesis must end with a clear verdict:

- **Strong conviction**: "BUILD / DON'T BUILD / READY TO BUILD" with high confidence
- **Conditional**: "BUILD IF [specific conditions are met]" with conditions list
- **Insufficient evidence**: "NEEDS MORE EVIDENCE on [specific gaps]" with research plan

Never end with "it depends" without specifying what it depends on and how to resolve it.

---

## Team Communication Standards

### Message Structure

When agents send findings to teammates:

```
## [Agent Name] Findings: [Topic]

### Key Claims
1. [Claim] - Confidence: [HIGH/MEDIUM/LOW] - Evidence: [summary]
2. [Claim] - Confidence: [HIGH/MEDIUM/LOW] - Evidence: [summary]

### Evidence Base
- [Source 1]: [What it shows]
- [Source 2]: [What it shows]

### Gaps and Limitations
- [What I couldn't find or verify]
- [Assumptions I'm making]

### Preliminary Recommendation
[What I think this means for the decision]
```

### Confidence Levels

- **HIGH**: Multiple independent sources confirm. Would bet on this.
- **MEDIUM**: Some evidence supports, but gaps exist. Directionally correct.
- **LOW**: Limited evidence, significant assumptions. Treat as hypothesis.

---

## Common Anti-Patterns

### 1. Consensus Theater

Agents agree too quickly to avoid conflict. Every team debate should have at least one genuine challenge. If nobody disagrees, someone isn't doing their job.

### 2. Authority Bias

Deferring to the "lead" agent's view without genuine examination. The lead synthesizes; they don't dictate.

### 3. Evidence Arms Race

Agents competing to find the most evidence rather than the most relevant evidence. Five weak sources don't beat one strong one.

### 4. Scope Creep in Debate

Cross-examination expanding into entirely new investigations. Stick to challenging existing findings, not opening new lines of inquiry.

### 5. False Precision

Scoring with decimal precision (7.3/10) when the underlying evidence only supports rough buckets (high/medium/low). Don't manufacture certainty.

---

## Ready-to-Use Resources

### In `references/`:

- **team-debate-patterns.md**: Dialectical Inquiry, Devil's Advocacy, and Constructive Controversy frameworks with implementation details

---

**Remember**: The point of multi-agent debate isn't to be adversarial. It's to be thorough. Every blind spot found in debate is a blind spot that won't surprise you in the market.
