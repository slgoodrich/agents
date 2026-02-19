---
name: validation-sprint
description: "Run a multi-agent validation sprint to answer: Should I build this?"
user-invocable: true
disable-model-invocation: true
argument-hint: '"<idea description>"'
allowed-tools: Read, Glob, Grep, Task
---

# Validation Sprint

Run a multi-agent validation sprint to answer: **"Should I build this?"** Three agents investigate in parallel, cross-examine each other's findings, and deliver a go/no-go verdict.

## Usage

```bash
/agent-teams:validation-sprint "AI-powered code review tool for solo developers"
```

---

## Overview

This command spawns three teammates with competing perspectives to stress-test a product idea:

- **idea-researcher**: Investigates the user problem (pain severity, frequency, workarounds)
- **market-researcher**: Investigates the market opportunity (size, competition, timing)
- **idea-skeptic**: Tries to kill the idea (finds structural reasons it should fail)

After parallel investigation, agents cross-examine each other's findings. The lead synthesizes everything into a **Validation Verdict** with scores and a BUILD / DON'T BUILD / NEEDS MORE EVIDENCE recommendation.

**What you get:**

- Three independent perspectives on your idea
- Cross-examination that surfaces blind spots
- Scored verdict (User Problem, Market Opportunity, Defensibility)
- Key risks with mitigations
- Specific next steps

---

## Idea Under Investigation

$ARGUMENTS

---

## Instructions

### Pre-Flight Check

Before starting, verify Agent Teams is available in your Claude Code version.
If teammates cannot be spawned, display:

```
This command requires Claude Code's Agent Teams feature.
Check https://docs.anthropic.com/en/docs/claude-code for setup instructions.
```

If not available, stop.

---

### Phase 1: Briefing

1. Check for existing product context:
   - Read `.claude/product-context/product-info.md` if it exists
   - Read `.claude/product-context/competitive-landscape.md` if it exists
   - Read `.claude/product-context/customer-segments.md` if it exists

2. Display briefing:

```
╔═══════════════════════════════════════════════════════════╗
║   Validation Sprint                                        ║
╔═══════════════════════════════════════════════════════════╝

Idea: [parsed idea description]

Assembling your validation team:
  1. idea-researcher  - Investigating the user problem
  2. market-researcher - Researching the market opportunity
  3. idea-skeptic      - Trying to kill this idea

Phase 1: Parallel Investigation (3 agents working simultaneously)
Phase 2: Cross-Examination (agents challenge each other)
Phase 3: Synthesis (final verdict with scores)

Starting investigation...
╚═══════════════════════════════════════════════════════════╝
```

---

### Phase 2: Parallel Investigation

Spawn 3 teammates simultaneously using Agent Teams:

**Teammate 1: idea-researcher**

```
Prompt: "Investigate the user problem behind this idea: [idea description].

[Include any product context found in Phase 1]

Your job: Determine if this is a real, painful problem for real people.
Assess pain severity, frequency, existing workarounds, and who feels this most.
Use your research-ops expertise. Search for evidence in forums, review sites,
and community discussions.

Deliver your findings in the standard idea-researcher output format.
Include confidence levels and evidence gaps."
```

**Teammate 2: market-researcher**

```
Prompt: "Research the market opportunity for this idea: [idea description].

[Include any product context found in Phase 1]

Your job: Assess market size, competitive landscape, and timing.
Use WebSearch to find real data on competitors, pricing, and market indicators.
Estimate TAM/SAM/SOM with transparent methodology.

Deliver your findings in the standard market-researcher validation sprint format.
Include source URLs and data gaps."
```

**Teammate 3: idea-skeptic**

```
Prompt: "Try to kill this idea: [idea description].

[Include any product context found in Phase 1]

Your job: Find every structural reason this idea should NOT be built.
Use your attack patterns: vitamin vs painkiller, feature vs product,
temporary differentiation, vague target market, incumbent response,
TAM inflation, switching costs.

Deliver at least 3 specific attacks in the standard idea-skeptic output format.
Rate each attack's severity. Be honest about which attacks are strong vs weak."
```

Wait for all three teammates to complete their investigations.

---

### Phase 3: Cross-Examination

Send each agent the other two agents' findings for one round of structured challenges.

**To idea-researcher:**

```
"Here are your teammates' findings. Review them and provide your challenges.

MARKET RESEARCHER'S FINDINGS:
[market-researcher output]

SKEPTIC'S CASE:
[idea-skeptic output]

Challenge their findings from the user problem perspective. Cite specific
claims from their reports. Use the cross-examination patterns from the
team-coordination skill. Focus your 2-3 strongest challenges."
```

**To market-researcher:**

```
"Here are your teammates' findings. Review them and provide your challenges.

IDEA RESEARCHER'S FINDINGS:
[idea-researcher output]

SKEPTIC'S CASE:
[idea-skeptic output]

Challenge their findings from the market perspective. Cite specific claims
from their reports. Use the cross-examination patterns from the team-coordination
skill. Focus your 2-3 strongest challenges."
```

**To idea-skeptic:**

```
"Here are your teammates' findings. Review them and provide your challenges.

IDEA RESEARCHER'S FINDINGS:
[idea-researcher output]

MARKET RESEARCHER'S FINDINGS:
[market-researcher output]

Update your case based on their evidence. Which of your attacks still stand?
Which are weakened? Do their findings reveal new vulnerabilities? Cite specific
evidence from their reports."
```

Wait for all three cross-examination responses.

---

### Phase 4: Synthesis

As the lead agent, compile all findings into the Validation Verdict.

1. Read all investigation reports and cross-examination responses.

2. Invoke the `team-deliverables` skill for the validation verdict template.

3. Score each dimension (1-10) using the rubrics from `team-deliverables`:
   - **User Problem**: Based primarily on idea-researcher's findings
   - **Market Opportunity**: Based primarily on market-researcher's findings
   - **Defensibility**: Based on all three perspectives, weighted by skeptic's attacks

4. Determine verdict:
   - **BUILD**: All scores 6+, no fatal skeptic attacks standing, convergence across agents
   - **DON'T BUILD**: Any score below 4, or fatal skeptic attacks unanswered
   - **NEEDS MORE EVIDENCE**: Scores 4-6 range with significant evidence gaps

5. Fill in the validation verdict template with:
   - Executive summary
   - Scores with justifications
   - Evidence from each agent
   - Cross-examination highlights (where they agreed, where they disagreed)
   - Key risks with mitigations
   - Specific next steps based on verdict
   - Dissenting views if any agent strongly disagreed with the verdict

6. Present the completed verdict to the user.

---

### Phase 5: Cleanup

1. Shut down all three teammates.

2. Offer to save the verdict:

```
Validation sprint complete.

Would you like me to save this verdict to:
  .claude/product-context/validation-[idea-slug].md

This will be available to other PM agents for future reference.
```

3. If user accepts, save the verdict file. If not, done.

---

## Error Handling

- If a teammate fails to produce output, note the gap in the synthesis and proceed with available findings. Don't fail the entire sprint.
- If WebSearch is unavailable, market-researcher should note data limitations and work with available information.
- If the idea description is too vague, ask the user for clarification before spawning teammates.

## Related

- `/agent-teams:prd-stress-test` - After validation, stress-test the PRD
- `/agent-teams:competitive-war-room` - Deep-dive specific competitors
- `product-strategist` agent - For strategy refinement after validation
