# Status Update Generator

Create audience-tailored progress updates that communicate clearly, build trust through transparency, and drive action on blockers.

## Usage

```
/product-operations:status [project or initiative] [optional: audience, time period]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. **Generates concise status updates** customized for different audiences (saves 30-60 min per update)
2. **Summarizes progress clearly** with completed work, in-progress items, and blockers in scannable format
3. **Highlights key metrics and milestones** with actual vs target to show trajectory
4. **Formats for various channels** (Slack, email, standup, reports) with appropriate tone and detail level
5. **Tracks progress over time** by maintaining consistent structure for trend analysis
6. **Surfaces risks proactively** with impact assessment and mitigation plans to build credibility

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Update Context**:
- What project/initiative is this status for? (product launch, feature development, ongoing project)
- What time period does this cover? (this week, last sprint, this month, Q1)
- When was the last update? (to show progress delta)
- What's the overall status? (on track 🟢, at risk 🟡, blocked 🔴, completed ✅)

**Audience & Channel**:
- Who is the audience? (team, leadership, executives, cross-functional partners, board)
- What channel? (Slack message, email, written report, verbal standup, dashboard)
- What's the frequency? (daily, weekly, bi-weekly, monthly, on-demand)
- What tone is appropriate? (casual, professional, formal, collaborative)
- What level of detail? (tactical/task-level vs strategic/high-level)

**Progress Information**:
- What was completed this period? (features shipped, milestones hit, decisions made)
- What's in progress? (current work, % complete, ETAs)
- What's next? (priorities for upcoming period)
- What blockers exist? (technical, resource, dependency, decision-needed)

**Metrics & Milestones**:
- What metrics are tracked? (KPIs, OKRs, health metrics)
- What are the targets vs actuals? (to show on/off track)
- What milestones were planned? (and were they hit?)
- What milestones are upcoming? (to set expectations)

**Risks & Asks**:
- What risks exist? (and severity: high/medium/low)
- What mitigations are in place?
- What help is needed? (from whom, by when)
- What decisions are needed? (from whom, by when)

**Strategic Context** (for leadership/exec updates):
- How does this tie to company OKRs or strategy?
- What's the business impact? (revenue, users, efficiency)
- What trade-offs were made? (scope, timeline, quality)

### 2. Structure Status Update for Clarity

**Essential Components** (all updates):
1. **Header**: Project name, date, time period
2. **Overall Status**: Visual indicator (🟢🟡🔴✅)
3. **TL;DR**: One-sentence summary (especially for leadership/exec)
4. **Completed**: What shipped/finished
5. **In Progress**: Current work
6. **Blockers/Risks**: What's at risk or blocked
7. **Next Up**: Upcoming priorities
8. **Ask**: Help or decisions needed (if any)

**Additional Components** (based on audience):
- **Metrics**: For leadership/exec (actual vs target)
- **Milestones**: For project tracking
- **Decisions Made**: For transparency
- **Team Health**: For leadership (morale, capacity, burnout)
- **Budget**: For exec/board (spent vs allocated)

### 3. Customize for Audience

**Team Updates** (Daily/Weekly):
- **Detail Level**: Tactical - specific tasks, PRs, tickets
- **Tone**: Casual, conversational
- **Focus**: Blockers, coordination, immediate next steps
- **Format**: Slack, standup, brief bullets
- **Length**: 100-200 words
- **Frequency**: Daily standups, weekly summaries

**Leadership Updates** (Weekly/Bi-weekly):
- **Detail Level**: Strategic - outcomes, metrics, risks
- **Tone**: Professional, structured
- **Focus**: Progress vs goals, risks, decisions made
- **Format**: Email, written report
- **Length**: 300-500 words
- **Frequency**: Weekly or bi-weekly

**Executive Updates** (Monthly/Quarterly):
- **Detail Level**: Executive summary - key results, critical risks
- **Tone**: Formal, concise
- **Focus**: Business impact, decisions needed, escalations
- **Format**: Email, slides, dashboard
- **Length**: 150-300 words (execs are time-constrained)
- **Frequency**: Monthly or quarterly

**Cross-Functional Updates** (As Needed):
- **Detail Level**: Relevant dependencies and handoffs
- **Tone**: Collaborative, clear
- **Focus**: Impact on other teams, timeline changes, help needed
- **Format**: Email, shared doc
- **Length**: 200-400 words
- **Frequency**: When dependencies change or coordination needed

### 4. Format for Channel

**Slack** (Team Updates):
- Use emojis for visual scanning (✅ 🚧 🚨 📊)
- Bullet points, no paragraphs
- @mention specific people for asks
- Thread for details, keep top-level concise
- Update thread as status changes

**Email** (Leadership/Exec):
- Clear subject line: "[Project] - [Period] Status Update"
- TL;DR at top (execs may not read further)
- Structured sections with headers
- Table for metrics/milestones
- Professional formatting
- Call-out boxes for critical items

**Written Report** (Comprehensive):
- Full narrative with context
- Multiple sections with detailed breakdowns
- Charts/graphs for metrics
- Appendix for supporting data
- Change log from last report

**Verbal Standup** (Daily):
- Yesterday/Today/Blockers format
- 60-90 seconds per person
- Details in writing, not verbal
- Focus on coordination

### 5. Write for Impact

**Lead with Status** (use color coding):
- 🟢 **On Track**: Progressing as planned, no concerns
- 🟡 **At Risk**: Behind schedule or risks emerged, mitigation in place
- 🔴 **Blocked**: Cannot progress without help, escalation needed
- ✅ **Completed**: Done, shipped, closed

**Be Specific** (quantify everything):
- ❌ "Making good progress on the feature"
- ✅ "Feature 80% complete, backend done, frontend in code review, ships Friday"

- ❌ "Some bugs reported"
- ✅ "15 bugs reported, 8 fixed, 5 in progress, 2 deferred to next sprint"

**Show Trend** (progress over time):
- "NPS increased from 35 → 42 (target: 50) - on track"
- "Velocity 18 pts (last sprint: 20 pts) - down 10% due to holidays"

**Own Risks** (don't hide problems):
- ❌ "Everything is fine" (when it's not)
- ✅ "🟡 At Risk: Timeline slipping 1 week due to scope increase. Mitigation: Descoping feature X to stay on track."

**Make Asks Clear**:
- ❌ "Need help with backend"
- ✅ "Ask: @Alice review API design by Wed to unblock frontend work"

### 6. Maintain Consistency

**Use Same Structure** (every update):
- Makes it easy to scan and compare
- Shows progress trends
- Builds trust through transparency

**Update Regularly** (establish rhythm):
- Daily: Team standups
- Weekly: Leadership updates
- Monthly: Executive summaries
- Consistency > Perfection

**Track Changes** (what's different from last time):
- What status changed (🟢 → 🟡)
- What metrics moved
- What new risks emerged
- What blockers were cleared

## Templates

### Team Update (Slack)
```
**[Project] - Week of [Date]** | Status: 🟢/🟡/🔴/✅

✅ **Shipped**: [Item 1 - impact], [Item 2 - impact]
🚧 **In Progress**: [Item 1 - 80% done, ships Fri], [Item 2 - blocked on X]
🚨 **Blockers**: @[Person] need [X] by [date] | None
📊 **Metrics**: [Metric]: [Current] (↑/↓ vs target)
🎯 **Next Week**: [Priority 1], [Priority 2]
💬 **Asks**: @[Person]: [Specific ask + deadline]
```

### Leadership Update (Email)
```
Subject: [Project] - Week of [Date]

**TL;DR**: [One sentence: status, key achievement, critical item]
**Status**: 🟢 | **Period**: [Dates]

## Progress
[2-3 sentences connecting achievements to goals]
- [Achievement 1]: [Impact on OKRs]
- [Achievement 2]: [Business metric impact]

## Metrics & Milestones
| Metric/Milestone | Target | Actual | Status |
|---|---|---|---|
| [Metric 1] | [Goal] | [Current] | 🟢🟡🔴 |

**OKR Progress**: [X]% toward [OKR name]

## Risks
### 🟡 [Risk]: [Impact] | Mitigation: [Plan] | Owner: [Who]
### 🔴 [High Risk]: [Impact] | Escalation needed: [What] by [When]

## Next Week
1. [Priority 1]: [Expected outcome]
2. [Priority 2]: [Expected outcome]

## Asks
- [Specific ask] - [By when] - [Why needed]
```

### Executive Update (Monthly)
```
**[Project] - [Month] Summary** | Status: 🟢

**One-liner**: [Accomplishment + business impact]

## By the Numbers
| Metric | Target | Actual | Trend |
|---|---|---|---|
| [Key Metric 1] | [Goal] | [Current] | ↑↓→ |
| Timeline | [Plan] | [Forecast] | 🟢 |

**OKR**: [X]% toward [objective]

## Critical Updates
🔴 **Decision Needed**: [What] by [Date] - [Impact if delayed]

## Next Milestone
**[Date]**: [Milestone] - [Deliverable] - [Success criteria]
```

### Daily Standup
```
**[Name] - [Date]**
**Yesterday**: ✅ [Specific completed item 1], ✅ [Item 2]
**Today**: 🚧 [Deliverable 1], 🚧 [Deliverable 2]
**Blockers**: 🚨 [Blocker] - need help from @[Person] | None
```


## Best Practices

✅ **DO**: Consistent structure/frequency, lead with 🟢🟡🔴, quantify ("80% done" > "almost there"), own risks transparently, specific asks (@Person X by Date), update regularly (even "no change"), show trends vs target, tailor for audience, write TL;DR first, link to details

❌ **DON'T**: Be vague ("making progress"), hide bad news, write novels, use jargon, skip asks, over/under-report, assume context, send without proofreading

**Related**: `/stakeholder-management:decision-log`, `/strategic-planning:exec-summary`, `/stakeholder-management:stakeholder-map`, `/gtm-strategy:communication-plan`
