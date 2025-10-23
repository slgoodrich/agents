# Stakeholder Mapper

Map and analyze stakeholders with power/interest matrices and engagement strategies for initiatives.

## Usage

```
/stakeholder-management:stakeholder-map [project or initiative] [optional: scope, organization context]
```

## What This Command Does

1. Identifies all stakeholders affected by or influencing an initiative
2. Maps stakeholders on power/interest and influence/impact matrices
3. Assesses each stakeholder's position (champion, supporter, neutral, skeptic, blocker)
4. Develops tailored engagement strategies for each stakeholder or group
5. Creates RACI matrix for roles and responsibilities
6. Builds communication plan aligned with stakeholder needs
7. Takes 30 minutes vs 2 hours of manual stakeholder analysis

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Initiative Context**:
- What initiative, project, or decision are we mapping stakeholders for?
- What's the scope and timeline?
- What's at stake? (revenue, strategy, resources, org change)
- What's controversial or politically sensitive?

**Stakeholder Landscape**:
- Who is affected by this initiative?
- Who has decision-making power?
- Who controls resources (budget, people, time)?
- Who are the influencers (may not have formal power)?
- Any known supporters or blockers?

**Organization Context**:
- Org structure (departments, reporting lines)
- Decision-making culture (top-down, consensus, data-driven)
- Past initiatives (what worked, what failed, why)
- Political dynamics to navigate

**Example Input**:
```
Initiative: Enterprise tier launch (new product tier)
Scope: 6-month project, $500K investment, affects sales, eng, CS teams
Stakes: Board expects $2M ARR Year 1, reputation risk if fails
Stakeholders: CEO (sponsor), VP Sales (champion), VP Eng (skeptical - resource concerns), CS team (neutral), Finance (approver)
Politics: Sales and Eng historically don't align well
```

### 2. Identify All Stakeholders

**Categories**:
- **Decision Makers**: Final approval authority
- **Influencers**: Sway decisions, trusted advisors
- **Implementers**: Execute the work
- **Users**: Use the product/feature
- **Affected Parties**: Impacted but not directly involved

**Don't Forget**:
- Indirect stakeholders (legal, compliance, finance)
- External stakeholders (customers, partners)
- Informal influencers (team leads without formal power)

### 3. Map Stakeholders

**Power/Interest Matrix** (Most common):
- **Power**: Ability to influence outcome (decision authority, resources, influence)
- **Interest**: How much they care about this initiative

**Influence/Impact Matrix** (Alternative):
- **Influence**: Their ability to affect the project
- **Impact**: How much the project affects them

### 4. Assess Stakeholder Position

**Positions**:
- **🟢 Champion**: Actively advocates for initiative
- **🔵 Supporter**: Positive but not actively promoting
- **⚪ Neutral**: No strong opinion yet
- **🟡 Skeptic**: Has concerns but can be convinced
- **🔴 Blocker**: Actively opposes, likely to obstruct

### 5. Develop Engagement Strategies

**Strategy by Quadrant** (Power/Interest):
- **High Power, High Interest (Key Players)**: Manage closely, regular updates
- **High Power, Low Interest (Keep Satisfied)**: Keep informed, don't overwhelm
- **Low Power, High Interest (Keep Informed)**: Regular communication, leverage enthusiasm
- **Low Power, Low Interest (Monitor)**: Light touch, monitor for changes

## Template

```markdown
# Stakeholder Map: [Initiative Name]

**Initiative**: [Brief description]
**PM Owner**: [Your Name]
**Date**: [YYYY-MM-DD]
**Status**: [Draft | Active | Complete]

---

## Executive Summary

**Total Stakeholders**: [X]
**Key Players** (High Power, High Interest): [Y]
**Champions**: [Z names]
**Blockers**: [W names]
**Biggest Risk**: [Top stakeholder risk]
**Mitigation**: [How we're addressing it]

---

## Power/Interest Matrix

**Visual Map**:

```
         HIGH POWER
             │
        ┌────┼────────────┐
        │  MANAGE CLOSELY │
    H   │  🔴 KEY PLAYERS │
    I   ├─────────────────┤
    G   │   KEEP INFORMED │
    H   │  🔵 KEEP ENGAGED│
        ├─────────────────┤
    I   │    MONITOR      │
    N   │  ⚪ LIGHT TOUCH │
    T   ├─────────────────┤
    E   │  KEEP SATISFIED │
    R   │  🟡 INFORM BUT  │
    E   │     DON'T BURDEN│
    S   └────┼────────────┘
    T        │
          LOW POWER
```

**Stakeholder Placement**:

**🔴 Manage Closely** (High Power, High Interest):
- [Stakeholder 1 - Title/Role]
- [Stakeholder 2 - Title/Role]

**🔵 Keep Informed** (Low Power, High Interest):
- [Stakeholder 3]
- [Stakeholder 4]

**🟡 Keep Satisfied** (High Power, Low Interest):
- [Stakeholder 5]
- [Stakeholder 6]

**⚪ Monitor** (Low Power, Low Interest):
- [Stakeholder 7]

---

## Stakeholder Profiles

### Key Players (High Power, High Interest)

#### Stakeholder 1: [Name, Title/Role]

**Power Level**: 🔴 High
**Interest Level**: 🔴 High
**Position**: 🟢 Champion | 🔵 Supporter | ⚪ Neutral | 🟡 Skeptic | 🔴 Blocker

**Why They Matter**:
[Their role, decision authority, or influence - why are they key to success?]

**Interests** (What they care about):
- [Interest 1 - e.g., "Revenue impact and ROI"]
- [Interest 2 - e.g., "Team morale and workload"]
- [Interest 3 - e.g., "Customer satisfaction"]

**Concerns** (What worries them):
- [Concern 1 - e.g., "Timeline too aggressive"]
- [Concern 2 - e.g., "Resource allocation from other priorities"]
- [Concern 3 - e.g., "Risk of customer churn if we fail"]

**Motivations** (What drives their position):
- [Personal: Career advancement, reputation]
- [Professional: Team success, department goals]
- [Strategic: Company objectives, market position]

**Influence on Initiative**:
- **Decision Authority**: [What they can approve/veto]
- **Resource Control**: [Budget, people, time they control]
- **Influence**: [Who listens to them, informal power]

**Current Position**: [Champion | Supporter | Neutral | Skeptic | Blocker]
**Desired Position**: [Where you need them to be]

**Engagement Strategy**:
- **Objective**: [What you need from them - approval, resources, advocacy]
- **Approach**: [How to engage - 1:1s, presentations, data-driven]
- **Tactics**:
  1. [Tactic 1 - e.g., "Weekly 1:1 progress updates"]
  2. [Tactic 2 - e.g., "Include in key milestone decisions"]
  3. [Tactic 3 - e.g., "Early access to results/wins"]
- **Messaging**: [What to emphasize - ROI, customer impact, competitive advantage]
- **Frequency**: [How often to engage - daily, weekly, monthly]

**Communication Plan**:
- **Format**: [Email, presentation, dashboard, 1:1]
- **Frequency**: [Weekly, bi-weekly, monthly]
- **Channel**: [Email, Slack, meetings, reports]
- **Content Focus**: [Executive summary, metrics, decisions needed]

**Risk Management**:
- **Risk if Unsupportive**: [What happens if they oppose or disengage]
- **Mitigation**: [How to prevent or address]

**Actions**:
- [ ] [Action 1 - e.g., "Schedule kickoff 1:1 by [date]"]
- [ ] [Action 2 - e.g., "Share PRD for feedback by [date]"]
- [ ] [Action 3 - e.g., "Include in go/no-go decision meeting"]

**Owner**: [Who manages this relationship - usually PM]

---

#### Stakeholder 2: [Name, Role]

[Repeat stakeholder profile template]

---

### Keep Informed (Low Power, High Interest)

#### Stakeholder 3: [Name, Role]

**Power**: 🔵 Low-Medium
**Interest**: 🔴 High

**Why They Care**: [Reason for high interest]

**Engagement Strategy**:
- Regular updates (weekly team meetings)
- Leverage their enthusiasm (beta testing, feedback)
- Recognize contributions publicly

---

[Repeat for other stakeholders in this quadrant]

---

### Keep Satisfied (High Power, Low Interest)

#### Stakeholder 5: [Name, Role]

**Power**: 🔴 High
**Interest**: 🟡 Low-Medium

**Engagement Strategy**:
- Don't overwhelm with details
- High-level monthly updates
- Ask for input only when needed
- Respect their time

---

### Monitor (Low Power, Low Interest)

#### Stakeholder 7: [Name, Role]

**Engagement**: Light touch, monitor for changes in interest or power

---

## RACI Matrix

**Roles & Responsibilities**:

| Activity | [Stakeholder 1] | [Stakeholder 2] | [Stakeholder 3] | [Team A] | [Team B] |
|----------|-----------------|-----------------|-----------------|----------|----------|
| **Strategy Definition** | A | C | I | C | I |
| **PRD Creation** | C | R/A | C | C | I |
| **Design Approval** | I | C | R/A | C | I |
| **Development** | I | C | I | R/A | C |
| **QA/Testing** | I | I | C | C | R/A |
| **Go/No-Go Decision** | A | C | I | C | C |
| **Launch** | A | R | C | C | C |
| **Post-Launch Support** | I | C | I | C | R/A |

**Legend**:
- **R = Responsible**: Does the work
- **A = Accountable**: Ultimately answerable, final decision
- **C = Consulted**: Provides input, two-way communication
- **I = Informed**: Kept in the loop, one-way communication

**Notes**:
- Each activity should have exactly ONE "A" (accountable)
- "R" can be shared across multiple people
- Avoid too many "C"s (consultation fatigue)

---

## Communication Plan

### By Stakeholder Group

**🔴 Key Players** (High Power, High Interest):
- **Channel**: 1:1 meetings, executive presentations
- **Frequency**: Weekly or bi-weekly
- **Format**: Executive summary (1 page), metrics dashboard
- **Content**: Progress, decisions needed, risks, asks
- **Tone**: Strategic, outcome-focused

**🔵 Keep Informed** (Low Power, High Interest):
- **Channel**: Team meetings, Slack updates, email
- **Frequency**: Weekly
- **Format**: Detailed updates, task-level visibility
- **Content**: What's shipping, blockers, how to help
- **Tone**: Tactical, collaborative

**🟡 Keep Satisfied** (High Power, Low Interest):
- **Channel**: Email summaries, monthly reviews
- **Frequency**: Monthly or as-needed
- **Format**: Brief executive summary
- **Content**: High-level status, major milestones, escalations only
- **Tone**: Concise, respectful of time

**⚪ Monitor** (Low Power, Low Interest):
- **Channel**: Passive (roadmap updates, all-hands)
- **Frequency**: Quarterly or as-needed
- **Format**: General announcements
- **Content**: Major milestones only

---

### Communication Schedule

**Weekly**:
- Monday: Slack update to eng team (progress, blockers)
- Wednesday: 1:1 with VP Eng (key player)
- Friday: Email summary to all stakeholders (wins, next week preview)

**Bi-Weekly**:
- Sprint demos (invite key players, keep informed group)
- Stakeholder roundtable (align on priorities)

**Monthly**:
- Executive summary to CEO, board
- All-hands update on initiative progress
- Roadmap review with sales/CS

**Quarterly**:
- Business review with executives
- Stakeholder survey (check engagement, concerns)

---

## Influence & Coalition Building

**Champions to Leverage**:
- [Stakeholder X]: Can influence [Stakeholder Y], use for [specific ask]
- [Stakeholder Z]: Trusted by CEO, get their buy-in early

**Coalition Strategy**:
- Build support with [Group A] first (easier win)
- Use [Group A] success to convince [Group B]
- Address [Blocker]'s concerns before broader rollout

**Alliances**:
- [Team/Person 1] + [Team/Person 2] = Natural allies (shared goals)
- Partner them for [specific initiative outcome]

---

## Risk & Mitigation

### Stakeholder Risks

**Risk 1: [Stakeholder] Becomes Blocker**
- **Probability**: [High | Medium | Low]
- **Impact**: [High | Medium | Low]
- **Trigger**: [What would cause this]
- **Mitigation**:
  1. [Action to prevent]
  2. [Contingency if it happens]

**Risk 2: Key Stakeholder Leaves**
- **Probability**: [Low, but high impact]
- **Impact**: High
- **Mitigation**: Build relationships with 2nd-tier, document decisions

**Risk 3: Stakeholder Fatigue (Too Much Communication)**
- **Mitigation**: Segment communication, respect preferences, be concise

---

## Conflict Resolution

**Potential Conflicts**:

**Conflict 1: [Team A] vs [Team B] (Resource Allocation)**
- **Stakeholders**: [Names]
- **Issue**: [Description of disagreement]
- **Resolution Strategy**:
  1. [Understand both perspectives]
  2. [Find common ground - shared goal]
  3. [Propose compromise or data-driven decision]
  4. [Escalate to [Accountable Person] if unresolved]

**Conflict 2: [Stakeholder] Opposes Initiative**
- **Root Cause**: [Why they oppose - fears, incentives, info gap]
- **Resolution**:
  1. Listen and validate concerns
  2. Address objections with data/examples
  3. Find win-win (what would make them supportive?)
  4. If unresolved, escalate to shared manager

---

## Success Metrics

**Stakeholder Engagement Health**:
- **Response Rate**: % of stakeholders responding to requests (target: >80%)
- **Meeting Attendance**: % attending stakeholder meetings (target: >75%)
- **Satisfaction**: Quarterly survey score (target: >4/5)
- **Alignment**: % agreeing on priorities and decisions (target: >90%)

**Tracking**:
- [ ] Quarterly stakeholder survey
- [ ] Track engagement in meetings/emails
- [ ] Monitor for conflict or disengagement

---

## Action Items

**Immediate (This Week)**:
- [ ] [Schedule 1:1 with [Key Player] by [date]]
- [ ] [Send PRD to [Stakeholder] for feedback by [date]]
- [ ] [Address [Skeptic]'s concern about [issue]]

**Ongoing**:
- [ ] Weekly updates to Key Players
- [ ] Monthly check-ins with Keep Satisfied group
- [ ] Monitor for power/interest shifts

**Next Review**: [Date to reassess stakeholder map]

```

---

## Best Practices

### DO ✅

- **Map early** - Do stakeholder analysis before initiative kicks off
- **Update regularly** - Power and interest shift, reassess quarterly
- **Tailor communication** - One size doesn't fit all, personalize approach
- **Build champions** - Cultivate advocates who can influence others
- **Address skeptics early** - Don't ignore concerns, engage proactively
- **Document everything** - Track positions, concerns, commitments
- **Respect preferences** - Learn how stakeholders want to be engaged
- **Follow through** - Do what you say, build trust

### DON'T ❌

- **Don't ignore low-power stakeholders** - Interest can grow, power can shift
- **Don't over-communicate to busy execs** - Respect time, be concise
- **Don't under-communicate to champions** - Keep them engaged and informed
- **Don't surprise stakeholders** - No one likes bad news via email
- **Don't play politics** - Be transparent, ethical, collaborative
- **Don't forget informal influencers** - Title ≠ influence
- **Don't assume positions are fixed** - Skeptics can become champions

---

## Model

Use: Sonnet

---

## Related

- `/stakeholder-management:align` - Facilitate stakeholder alignment sessions
- `/gtm-strategy:comm-plan` - Detailed communication planning
- `/stakeholder-management:decision-log` - Document stakeholder decisions
- `/strategic-planning:annual-planning` - Strategic stakeholder engagement
- `stakeholder-manager` agent - Stakeholder management strategies
