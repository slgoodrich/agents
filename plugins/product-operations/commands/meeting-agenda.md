# Meeting Agenda Generator

Create structured meeting agendas with time allocations, objectives, and action item tracking.

## Usage

```
/product-operations:agenda [meeting type, topic] [optional: duration, attendees]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Generates structured agendas for different meeting types
2. Allocates time for each agenda item
3. Defines clear meeting objectives and outcomes
4. Includes preparation materials and pre-reads
5. Provides templates for decision points and action items
6. Adapts format based on meeting type and duration

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Meeting Basics**:
- What type of meeting is this? (1:1, team sync, decision meeting, working session, stakeholder update, kickoff)
- What's the meeting about? (specific topic or objective)
- How long is the meeting? (15 min, 30 min, 60 min, 90 min, 2 hours)
- When is it scheduled? (today, tomorrow, next week - affects prep time available)

**Attendees**:
- Who's attending? (names, roles, decision authority)
- How many people? (2 people vs 10 people affects agenda structure)
- Who's facilitating? (owner of meeting outcomes)
- Are there any required attendees vs optional?

**Meeting Objectives**:
- What needs to be accomplished? (make decision, align on strategy, solve problem, share updates)
- What's the one thing that must happen for this meeting to be successful?
- Are there decisions to make? (what decisions and who decides)
- Are there specific deliverables needed? (document, plan, list of priorities)

**Context & Preparation**:
- What background do attendees need? (pre-read materials, data, proposals)
- How much prep time do attendees have? (affects pre-read feasibility)
- Has this topic been discussed before? (is this a first discussion or follow-up)
- Are there any disagreements or tensions to navigate?

**Previous Meetings** (if recurring):
- What was decided last time? (to avoid re-litigation)
- What action items are outstanding? (to follow up)
- What topics were parked for this meeting?

### 2. Identify Meeting Type

- **1:1** - Manager/report, peer, stakeholder check-in
- **Team Sync** - Sprint planning, standup, retrospective
- **Decision Meeting** - Product review, prioritization, go/no-go
- **Working Session** - Design review, brainstorming, problem-solving
- **Stakeholder Update** - Executive briefing, cross-functional sync
- **Kickoff** - Project launch, initiative start

### 3. Gather Meeting Details
   - Meeting objective (what needs to be accomplished)
   - Duration (15min, 30min, 60min, 90min)
   - Attendees and roles
   - Required prep or pre-reads
   - Decision points
   - Key topics or questions

3. **Structure Agenda**:
   - **Opening** (5-10%): Context, objectives, ground rules
   - **Main Content** (70-80%): Discussion, decisions, working time
   - **Closing** (10-15%): Action items, next steps, parking lot

4. **Time Management**:
   - Allocate time per agenda item
   - Build in buffer (10-15%)
   - Hard stop at meeting end
   - Flag high-priority items

## Templates

### 1:1 (30min)
```
**1:1: [Name]** | [Date] | [Location]

**Their Topics** (10min): [What they want to discuss]
**Your Topics** (10min): [Updates needed, questions, alignment]
**Discussion: [Key Topic]** (7min): [Context, question, desired outcome]
**Career & Growth** (3min): [Development goals, feedback, opportunities]

**Action Items**: [Action - Owner - Due]
**Next 1:1**: [Date] - [Topics to cover]
```

### Decision Meeting (60min)
```
**Decision: [Topic]** | [Date] | Decision Maker: [Who]

**Objective**: Decide [specific decision] by end of meeting
**Pre-Read** (send 24h before): [Background doc, options analysis, recommendation]

**Agenda**:
1. Context & Problem (5min): [What, why now, impact]
2. Options Review (20min): [Option A/B/C pros/cons/cost/risks]
3. Discussion (20min): [Questions, concerns, trade-offs]
4. Decision (10min): [Poll, decision + rationale, dissents, commitment]
5. Next Steps (5min): [Actions, communication, timeline, metrics]

**Decision**: [Option X] - [Rationale] - [Trade-offs accepted]
**Actions**: [Document, communicate, implement, review]
```

### Sprint Planning (90min)
```
**Sprint [N] Planning** | [Date] | [Team]

**Objectives**: Commit to goal & backlog, align on priorities

**Agenda**:
1. Sprint Review (10min): Last sprint velocity, learnings
2. Capacity (10min): Availability, velocity target, capacity points
3. Sprint Goal (15min): One thing we're achieving, ties to OKRs
4. Story Selection (40min): Walk backlog, commit/defer, running tally
5. Task Breakdown (10min): Top stories → tasks, dependencies, owners
6. Risk Review (5min): Dependencies, technical risks, mitigation

**Commitment**: Goal: [X] | Stories: [Y] ([Z] points) | Confidence: [H/M/L]
```

### Brainstorming (60min)
```
**Brainstorming: [Topic]** | [Date] | Facilitator: [Name]

**Ground Rules**: Defer judgment, encourage wild ideas, "yes and...", quantity over quality

**Agenda**:
1. Problem Framing (10min): [Problem statement, HMW, constraints]
2. Divergent - Ideation (25min):
   - Individual (5min): Silent brainstorm, 5+ ideas each
   - Share & Build (10min): Present, build on ideas
   - Wild Ideas (5min): No constraints
   - Rapid Fire (5min): Quick ideas, 10+ more
3. Convergent - Clustering (10min): Group similar, name clusters
4. Dot Voting (5min): 3 votes each → top 5
5. Discussion (10min): Top ideas - exciting, concerns, next steps

**Output**: Top 5 ideas, next steps (1-pagers, research, feasibility spike)
```

### Executive Briefing (30min)
```
**Executive Briefing: [Topic]** | [Date] | Decision Needed: [What]

**Pre-Read** (10min): [Doc link]

**Agenda**:
1. Context (5min): Situation, why it matters, what's at stake
2. Recommendation (10min): Proposal, rationale, cost, outcomes
3. Risks (5min): What could go wrong, mitigations, monitoring
4. Decision (8min): Questions, decision
5. Next Steps (2min): Actions, timeline, communication

**Decision Request**: [Specific approval] by [date] - [If approved/not approved]
```


## Time Allocations

| Duration | Opening | Content | Closing |
|----------|---------|---------|---------|
| 30min | 3min | 23min | 4min |
| 60min | 5min | 48min | 7min |
| 90min | 10min | 70min | 10min |

**Always buffer 10-15% for overruns**

## Best Practices

✅ **DO**: Send agenda 24hrs ahead, state clear objective, timebox items, build buffer, assign roles (facilitator, notes, decider), include pre-read, start/end on time, capture actions, use parking lot, end with recap

❌ **DON'T**: Overschedule (2 focused 30min > 1 unfocused 60min), invite too many (>8 people), bury the lede (top items first), skip prep ("figure it out in meeting"), let one person dominate, end without actions, have meetings that could be emails, forget follow-up, schedule back-to-back, use for status updates

**Related**: `/product-operations:status`, `/stakeholder-management:decision-log`, `/stakeholder-management:stakeholder-map`
