---
description: Visual planning technique connecting goals to features through actors and impacts
category: Planning
model: sonnet
---

# Impact Mapping

Create impact maps that connect business goals to deliverables through behavioral changes using Gojko Adzic's impact mapping framework.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Goal**: Business or product goal to achieve
- **Timeframe**: When to achieve goal
- **Context**: Current situation, constraints, stakeholders
- **Known information** (optional): Actors, impacts, or deliverables you're considering

## Output

Four-level hierarchical impact map:

### Level 1: GOAL (Why?)
**Central business objective**

Format: [Metric] by [Amount] by [Date]

Examples:
- "Increase trial-to-paid conversion by 25% in Q3"
- "Reduce customer churn from 5% to 3% monthly by end of year"
- "Grow monthly active users from 10K to 20K in 6 months"

**Goal characteristics**:
- Specific and measurable
- Time-bound
- Aligned to business strategy
- Measurable with existing data
- Achievable but ambitious

### Level 2: ACTORS (Who?)
**People and systems who can help or hinder goal achievement**

For each actor:
- **Actor name**: Who they are
- **Role/Segment**: Their relationship to product
- **Current behavior**: What they do now
- **Potential influence**: How they can impact goal

**Actor categories**:
- **Primary actors**: Direct users who perform actions
- **Secondary actors**: Influence primary actors
- **System actors**: APIs, integrations, platforms

**Identify 5-10 key actors**

### Level 3: IMPACTS (How?)
**Behavioral changes for each actor that support goal**

For each actor, list impacts (desired behavior changes):
- **Impact description**: What behavior should change
- **How it supports goal**: Connection to overall objective
- **Current vs. desired state**: What changes
- **Measurability**: How to track this change

**Impact format**:
- "Start doing X" (new behavior)
- "Stop doing Y" (eliminate behavior)
- "Do more of Z" (increase behavior)
- "Do less of W" (decrease behavior)

**Identify 2-5 impacts per actor**

### Level 4: DELIVERABLES (What?)
**Features, initiatives, or solutions that enable impacts**

For each impact, potential deliverables:
- **Deliverable description**: What to build/do
- **How it enables impact**: Mechanism of change
- **Effort estimate**: T-shirt size (S/M/L/XL)
- **Assumptions**: What must be true
- **Priority**: Must-have, should-have, could-have

**List 1-4 deliverables per impact**

### Impact Map Visualization

```
                    GOAL
                     |
        +------------+------------+
        |            |            |
     ACTOR 1      ACTOR 2      ACTOR 3
        |            |            |
    +---+---+    +---+---+    +---+---+
    |       |    |       |    |       |
 IMPACT  IMPACT IMPACT IMPACT IMPACT IMPACT
    |       |    |       |    |       |
  DELIV  DELIV DELIV  DELIV DELIV  DELIV
```

### Impact Prioritization

**Prioritize paths** (Actor → Impact → Deliverable):
- **Impact on goal**: How much will this help?
- **Confidence**: How sure are we?
- **Effort**: How hard to implement?
- **Dependencies**: What else is needed?

**Priority Quadrants**:
- **High impact, Low effort**: Do first (quick wins)
- **High impact, High effort**: Strategic initiatives
- **Low impact, Low effort**: Maybe do later
- **Low impact, High effort**: Don't do (distractions)

### Minimum Viable Impact

**Minimum set of deliverables** to achieve goal:
- Which actors must change behavior?
- Which impacts are essential?
- Which deliverables are must-haves?
- What can wait for later?

Create focused delivery plan with highest-leverage items.

### Assumptions to Validate

For each path, identify assumptions:
- **Actor assumptions**: Will this actor actually do this?
- **Impact assumptions**: Will this behavior change achieve results?
- **Deliverable assumptions**: Will this feature drive the behavior change?
- **Measurability assumptions**: Can we track this?

**Validation plan**:
- How to test assumptions before building
- Customer interviews, prototypes, experiments
- Prioritize riskiest assumptions to validate first

## Example Prompt

```
Create an impact map for:
- Goal: Increase free-to-paid conversion by 30% in next quarter
- Context: SaaS project management tool, current conversion is 10%, freemium model
- Timeframe: 3 months
- Known info: Users cite "not enough team features" and "pricing confusion" in surveys
```

## Use Cases

- **Feature prioritization** - Connect features to goals
- **Product planning** - Strategic roadmap development
- **Assumption mapping** - Identify what to validate
- **Stakeholder alignment** - Visual shared understanding
- **Scope management** - What's in/out for MVP
- **Team collaboration** - Collaborative planning exercise

## Benefits of Impact Mapping

**Goal-oriented**:
- Everything traces back to measurable goal
- Prevents feature bloat
- Focus on outcomes

**Visual and collaborative**:
- Easy to understand hierarchy
- Great for workshops
- Shared mental model

**Assumption surfacing**:
- Makes beliefs explicit
- Identifies what to validate
- Risk mitigation

**Scope flexibility**:
- Easy to add/remove deliverables
- Find minimum viable path
- Adapt to learnings

## How to Create Impact Map (Workshop Format)

**Step 1: Define Goal** (15 min)
- Agree on specific, measurable goal
- Write in center of map

**Step 2: Identify Actors** (30 min)
- Brainstorm all possible actors
- Group and prioritize
- Add to map as branches

**Step 3: Map Impacts** (45 min)
- For each actor, brainstorm behavior changes
- How each impact supports goal
- Prioritize by leverage

**Step 4: Generate Deliverables** (45 min)
- For each impact, possible solutions
- Multiple options per impact
- Estimate effort

**Step 5: Prioritize** (30 min)
- Score paths by impact and effort
- Identify minimum viable scope
- Create delivery sequence

**Step 6: Identify Assumptions** (30 min)
- What must be true for each path
- Rank assumptions by risk
- Plan validation approach

**Total: 3-4 hour workshop with cross-functional team**

## Impact Mapping vs. Other Techniques

**User Story Mapping**:
- Similar: Hierarchical, outcome-focused
- Different: Impact mapping more goal-oriented, user story mapping more journey-oriented
- Use together: Impact map for "what to build", story map for "how to build it"

**OKRs**:
- Similar: Goal and key results
- Different: Impact mapping shows how to achieve results
- Use together: OKR sets goal, impact map plans execution

**Feature Roadmap**:
- Similar: Plans what to build
- Different: Impact mapping shows why and prioritizes by goal impact
- Use together: Impact map informs roadmap priorities

## Maintaining Impact Maps

**Update frequency**:
- Review quarterly or when goal changes
- Update based on learnings
- Add new actors/impacts discovered
- Remove deprioritized paths

**Use as living document**:
- Reference during sprint planning
- Validate assumptions continuously
- Measure impacts achieved
- Adjust based on results

## Common Pitfalls

**Starting with deliverables**:
- Don't jump to solutions
- Start with goal, identify actors and impacts first
- Deliverables should emerge from impacts

**Too many actors**:
- Focus on 5-10 most important actors
- Not every user type needs to be separate actor

**Vague impacts**:
- Be specific about behavior change
- Measurable if possible
- "Use feature more" is vague, "Log in 3x/week instead of 1x/week" is specific

**One deliverable per impact**:
- Explore multiple options
- Create optionality
- Choose based on effort and confidence

**Creating and forgetting**:
- Use map actively in planning
- Reference in prioritization discussions
- Update based on learnings

## Related Tools

- `/strategic-planning:okr-framework` - Goal setting
- `/tools/assumption-mapping` - Validate assumptions
- `/requirements-engineering:user-story-writer` - Create user stories from deliverables
- `/strategic-planning:roadmap-builder` - Turn impact map into roadmap
- `/tools/trade-off-analysis` - Choose between deliverables

## Deliverables from Impact Map

Use impact map to create:
- **Roadmap**: Deliverables sequenced over time
- **Backlog**: User stories and epics
- **Experiment plan**: Validate assumptions
- **Success metrics**: Measure impacts and goal
- **Minimum viable scope**: Smallest set to test hypothesis

Impact mapping bridges strategy (goals) and execution (features) by focusing on the behavioral changes that matter.
