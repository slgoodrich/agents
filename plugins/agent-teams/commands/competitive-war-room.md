---
description: "Run parallel competitor deep-dives and synthesize into positioning strategy and battle cards"
argument-hint: '"<competitor1>, <competitor2>, <competitor3>"'
---

# Competitive War Room

Run parallel competitor deep-dives and synthesize into positioning strategy, battle cards, and competitive intelligence. One researcher per competitor, working simultaneously.

## Usage

```bash
/agent-teams:competitive-war-room "Notion, Coda, Slite"
```

```bash
/agent-teams:competitive-war-room "Vercel, Netlify, Cloudflare Pages, Railway"
```

---

## Overview

This command spawns one market-researcher teammate per competitor. Each researcher does a deep-dive on their assigned competitor using WebSearch. The lead synthesizes individual deep-dives into:

- Competitive positioning map
- Differentiation opportunities
- Competitive threats
- Battle cards (one per competitor)
- White space analysis

**What you get:**

- Deep-dive on each competitor (strategy, strengths, weaknesses, pricing, sentiment)
- Side-by-side comparison across competitive dimensions
- Battle cards ready for sales or product decisions
- Specific strategic recommendations

---

## Instructions

### Pre-Flight Check

1. Verify Agent Teams feature is available:

```
Check environment: CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1

If not set:
╔═══════════════════════════════════════════════════════════╗
║   Agent Teams Required                                     ║
╔═══════════════════════════════════════════════════════════╝

This command requires Claude Code's experimental Agent Teams feature.

To enable it, set the environment variable:
  export CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1

Then restart Claude Code and try again.
╚═══════════════════════════════════════════════════════════╝
```

If not enabled, display the message and stop.

2. Parse the comma-separated competitor list from the command argument.
   - Trim whitespace from each competitor name
   - Validate at least 2 competitors provided
   - If fewer than 2: "Please provide at least 2 competitors, separated by commas."

3. Load product context for positioning baseline:
   - Read `.claude/product-context/product-info.md` if it exists
   - Read `.claude/product-context/competitive-landscape.md` if it exists
   - If no product-info.md, ask the user: "What's your product and who's it for? I need this to position you against competitors."

---

### Phase 1: Mission Briefing

1. Define your product's positioning baseline from context files or user input.

2. Display briefing:

```
╔═══════════════════════════════════════════════════════════╗
║   Competitive War Room                                     ║
╔═══════════════════════════════════════════════════════════╝

Your Product: [product name and positioning from context]

Competitors to analyze:
  [1. Competitor 1]
  [2. Competitor 2]
  [3. Competitor 3]
  [... etc.]

Deploying [N] market researchers (one per competitor).
Each will deep-dive: strategy, strengths, weaknesses, pricing, sentiment.

Phase 1: Parallel Deep-Dives ([N] researchers working simultaneously)
Phase 2: Synthesis (positioning map, battle cards, recommendations)

Starting research...
╚═══════════════════════════════════════════════════════════╝
```

---

### Phase 2: Parallel Deep-Dives

Spawn N market-researcher teammates simultaneously, one per competitor.

**For each competitor, spawn a market-researcher with:**

```
Prompt: "Deep-dive competitor: [Competitor Name].

CONTEXT - YOUR PRODUCT:
[Product info from context or user input]

Your job: Become the expert on [Competitor Name]. Use WebSearch extensively
to research:

1. **Overview**: What they do, who they serve, how they position
2. **Strategy**: Their approach to the market, recent moves, direction
3. **Strengths**: What they do well (cite evidence from reviews, features)
4. **Weaknesses**: Where they fall short (cite evidence from reviews, complaints)
5. **Pricing**: Full pricing model with tiers (link to pricing page)
6. **Customer Sentiment**: What users love and hate (G2, Capterra, Reddit, etc.)
7. **Threat Level**: How much of a threat are they to [your product]?

Use the standard market-researcher competitive war room output format.
Cite every claim with a source URL and date.
Be thorough but focused. Quality over exhaustiveness."
```

Wait for all researchers to complete their deep-dives.

---

### Phase 3: Synthesis

As the lead agent, compile all deep-dives into a competitive synthesis.

1. Read all individual competitor deep-dives.

2. Invoke the `team-deliverables` skill for the competitive synthesis template.

3. Build the positioning map:
   - Map your product against each competitor across key dimensions
   - Identify where you're stronger, where you're weaker

4. Identify differentiation opportunities:
   - **Where you win**: Advantages to exploit
   - **Where you lose**: Weaknesses to mitigate or avoid
   - **White space**: Needs no competitor addresses well

5. Assess competitive threats:
   - Likelihood and impact of each threat
   - Recommended response for each

6. Generate battle cards:
   - One per competitor using the battle card section of the template
   - Include: their pitch, your counter, where you win, where they win, landmines, killer question

7. Develop strategic recommendations:
   - Positioning refinements based on competitive landscape
   - Feature priorities informed by competitive gaps
   - Messaging adjustments to highlight differentiation

8. Present the completed competitive synthesis to the user.

---

### Phase 4: Battle Cards

After presenting the synthesis, generate a standalone battle card for each competitor.

Each battle card should be concise (under 1 page) and actionable:

- When you encounter this competitor
- Their pitch vs. your counter
- Your advantages and their advantages (be honest)
- Topics to avoid (their strengths you can't match)
- One killer question that shifts the conversation in your favor

---

### Phase 5: Cleanup

1. Shut down all researcher teammates.

2. Offer to save:

```
Competitive war room complete.

Would you like me to save these findings?

  1. Full report → .claude/product-context/competitive-landscape.md
  2. Battle cards → .claude/product-context/battle-cards/[competitor].md

Saving makes this available to other PM agents (product-strategist,
launch-planner, feature-prioritizer) for future reference.
```

3. If user accepts:
   - Save competitive landscape to `.claude/product-context/competitive-landscape.md`
   - Save individual battle cards to `.claude/product-context/battle-cards/` directory
   - Include "Last Updated: [date]" header in each file

4. If declined, done.

---

## Error Handling

- If a researcher fails on a specific competitor, note the gap in the synthesis and proceed with available deep-dives.
- If WebSearch is unavailable, note that data will be limited and work with available information.
- If a competitor name is ambiguous (multiple companies with similar names), the researcher should clarify which one based on the product context.
- If more than 5 competitors provided, warn the user that quality may decrease with too many parallel researchers, but proceed.

## Related

- `/agent-teams:validation-sprint` - Validate your idea against the competitive landscape
- `/agent-teams:prd-stress-test` - Stress-test a PRD with competitive context
- `market-analyst` agent - For focused competitive research on a single competitor
- `product-strategist` agent - For positioning strategy based on competitive findings
