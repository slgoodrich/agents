---
name: roadmap-frameworks
description: Master product roadmaps including roadmap types (timeline, outcome-based, Now-Next-Later), communication strategies, and prioritization. Use when creating roadmaps, communicating strategy, prioritizing initiatives, or evolving product direction. Covers roadmap formats, communication tactics, and roadmap best practices from product leaders.
---

# Roadmap Frameworks

Frameworks for building, communicating, and managing product roadmaps that align teams, guide execution, and drive strategic outcomes.

## What is a Roadmap?

A roadmap is a strategic communication tool that:
- Shows **WHERE** you're going (direction, themes)
- Explains **WHY** you're going there (strategy, rationale)
- Indicates **WHEN** (roughly) you'll get there (timeframes)
- Communicates **HOW** you'll get there (initiatives, bets)

**NOT**: A list of features with dates
**BUT**: A strategic narrative about the future

**Good roadmaps**: Outcome-oriented, flexible, strategic, audience-appropriate, actionable

**Bad roadmaps**: Feature lists, hard dates, everything for everyone, disconnected from strategy, stale

## When to Use This Skill

**Auto-loaded by agents**:
- `roadmap-builder` - For Now-Next-Later, theme-based, and outcome roadmaps

**Use when you need**:
- Quarterly/annual planning
- Strategic clarity
- Team coordination
- Clear communication
- Investment decisions
- Customer/user communication

---

## Roadmap Types

### 1. Now-Next-Later (Recommended for Most)

**Structure**: Three buckets without dates

**NOW**: What we're working on right now (high confidence, active)
**NEXT**: What we'll likely do next (medium confidence, validated)
**LATER**: What we're exploring (low confidence, directional)

**When to use**: Maximum flexibility, minimal commitment, high uncertainty

**Benefits**:
- No date commitments
- Easy to adjust
- Clear focus
- Simple communication

**Template**: `assets/now-next-later-template.md`

Complete template with examples, confidence levels, updating guidance

---

### 2. Theme-Based

**Structure**: Strategic themes with grouped initiatives

Organize by themes (e.g., "Enterprise Readiness", "Customer Experience") rather than features.

**When to use**: Communicate strategic focus areas

**Benefits**:
- Strategic clarity
- Outcome-focused
- Flexible within themes

---

### 3. Outcome-Based

**Structure**: Lead with results, not outputs

Focus on customer/business outcomes (e.g., "Reduce churn by 50%") with flexible approaches.

**When to use**: Results-driven teams, goal-driven culture

**Benefits**:
- Clear success criteria
- Measurable
- Team autonomy on "how"

**Template**: `assets/outcome-roadmap-template.md`

Includes outcome format, examples, comparison with feature roadmaps

---

### 4. Timeline

**Structure**: Initiatives plotted on calendar/quarters

Visual timeline showing sequencing and dependencies.

**When to use**: Internal planning only, complex dependencies

**NOT for**: External communication (creates date expectations)

---

**Choosing the right type**: See `references/roadmap-types-guide.md` for detailed comparison and selection criteria.

---

## Roadmap by Audience

Different audiences need different roadmaps:

### Executive Roadmap
**Focus**: Strategy, business outcomes, resource needs
**Format**: Themes + outcomes, annual + quarterly
**Detail**: Low (strategic)

### Customer Roadmap
**Focus**: Value delivery, transparency
**Format**: Now-Next-Later with problem framing
**Exclude**: Internal work, hard dates

### Sales Roadmap
**Focus**: Deal enablement, competitive positioning
**Guidance**: "Commit to Now, position Next as likely, describe Later as exploring"

### Engineering Roadmap
**Focus**: Execution, technical detail
**Format**: Timeline with dependencies
**Detail**: High (sprint-plannable)

### Internal All-Hands
**Focus**: Company alignment, transparency
**Frequency**: Quarterly updates

**Comprehensive guide**: `references/roadmap-communication-guide.md`

Includes communication tactics, update formats, anti-patterns

---

## Building Your Roadmap

### 7-Step Process

**Step 1**: Establish Strategy (company goals, product strategy, market position)

**Step 2**: Gather Inputs (customer feedback, business priorities, technical needs, competitive intel)

**Step 3**: Prioritize (RICE, Impact/Effort, Strategic Fit)

**Step 4**: Define Themes (3-5 customer-centric, strategic themes)

**Step 5**: Sequence (dependencies, resources, timing, value delivery)

**Step 6**: Validate & Align (exec, engineering, sales/CS, customers)

**Step 7**: Communicate (audience-specific views, all-hands, documentation)

**Detailed guide**: `references/roadmap-building-guide.md`

Includes detailed steps, outputs, prioritization frameworks, maintenance cadence

---

## Roadmap Narrative

Tell the story of your roadmap - where, why, how:

**Structure**:
1. Vision (where we're going)
2. Strategy (why this roadmap)
3. Prioritization approach (how we chose)
4. What we're building (Now, Next, Later)
5. Trade-offs (what we're NOT doing)
6. Feedback process (how to influence)

**Template**: `assets/roadmap-narrative-template.md`

---

## Roadmap Best Practices

**DO**:
- Start with strategy (not features)
- Use themes and outcomes (not feature lists)
- Tailor to audience (exec, team, customer)
- Show trade-offs (what you're NOT doing)
- Update regularly (quarterly planning, monthly review)
- Communicate changes (transparency)
- Link to metrics (measurable outcomes)
- Keep "Now" specific, "Later" vague

**DON'T**:
- Commit to dates (use timeframes)
- Promise everything (prioritize ruthlessly)
- Use internal jargon (customer language)
- Build in vacuum (validate with user feedback)
- Set and forget (iterate continuously)
- Hide trade-offs (be transparent)
- Lead with features (lead with problems)
- Make it static (living document)

---

## Roadmap Anti-Patterns

**Common mistakes**:

1. **Feature Laundry List**: Just features, no strategy → Use theme-based, outcome-oriented
2. **Date-Driven Commitments**: "Ship X on June 15" → Use timeframes, confidence levels
3. **One Size Fits All**: Same roadmap for all audiences → Tailor by audience
4. **Set and Forget**: Never updated, stale → Regular review cadence
5. **Everything for Everyone**: No priorities → Explicit prioritization, "not doing" list
6. **No Strategic Connection**: Disconnected from goals → Link every theme to objective
7. **Too Much Detail**: Over-specified → Appropriate detail for timeframe
8. **Internal Jargon**: Technical speak → Problem-focused, customer language

---

## Roadmap Maintenance

### Review Cadence

**Weekly** (30 min): Current work on track? Adjust "Now"

**Monthly** (60 min): Progress on quarter, validate "Next", refine "Later"

**Quarterly** (Half day): Build next quarter roadmap, review outcomes

### When to Update

**DO update**:
- Quarterly planning (always)
- Major strategic shift
- Significant customer feedback
- Competitive threat
- Resource changes

**DON'T update**:
- Every feature request
- Minor adjustments
- Random requests

### Communicating Changes

When roadmap changes materially:
```
Roadmap Update: [Date]

What Changed: [Change + Why]
What Stayed: [Core themes still priority]
Impact: [Who this affects]
```

**Frequency**: Only material changes

---

## For Solo Operators / Small Teams

**Simplify**:
- Use Now-Next-Later (simplest format)
- Focus on 2-3 themes max
- Skip elaborate tools (Google Slides works)
- Update monthly (not weekly)
- Share with customers for feedback

**Timeline**: 4-6 hours for quarterly roadmap

**Key**: Simple beats perfect. Better a clear 1-page roadmap than elaborate 20-page deck nobody reads.

---

## Roadmap Tools

**Lightweight** (Early stage):
- Google Slides/PowerPoint
- Notion/Coda
- Miro/Figma

**Purpose-Built** (Growth):
- Productboard
- Aha!
- ProductPlan
- Jira Product Discovery

**Custom** (Enterprise):
- Custom-built, integrated with data warehouse

**Recommendation for solo/small teams**: Start with slides, upgrade only when pain is real.

---

## Templates and References

### Assets (Ready-to-Use Templates)

Copy-paste these for immediate use:
- `assets/now-next-later-template.md` - Most flexible format, complete example
- `assets/outcome-roadmap-template.md` - Results-focused format
- `assets/roadmap-narrative-template.md` - Storytelling structure

### References (Deep Dives)

When you need comprehensive guidance:
- `references/roadmap-types-guide.md` - All types compared, selection criteria
- `references/roadmap-communication-guide.md` - Audience-specific roadmaps, communication tactics
- `references/roadmap-building-guide.md` - 7-step process, prioritization, maintenance

---

## Related Skills

- `prioritization-methods` - Prioritization frameworks (RICE, ICE, Impact/Effort)
- `product-positioning` - Strategic positioning
- `go-to-market-playbooks` - Launch planning and GTM strategy

---

## Quick Start

**For your first roadmap**:
1. Use Now-Next-Later format (simplest)
2. Start with `assets/now-next-later-template.md`
3. Define 2-3 strategic themes
4. Fill in Now (what you're working on)
5. Add Next (validated problems, likely next)
6. Add Later (exploring)
7. Include "Not Doing" (trade-offs)
8. Present to team, get feedback
9. Update quarterly

**For quarterly planning**:
1. Review last quarter: What shipped? What didn't? Why?
2. Gather inputs: Customer feedback, business priorities, tech needs
3. Prioritize: Impact, effort, strategic fit
4. Sequence: Now → Next → Later
5. Communicate: All-hands + written doc
6. Update monthly based on learnings

---

**Key Principle**: Roadmaps are strategic communication tools, not commitments. They show direction and rationale, enabling alignment while maintaining flexibility. Good roadmaps create clarity without over-committing. Update regularly, communicate changes, focus on outcomes.
