# Stakeholder Mapper

Map and analyze stakeholders with power/interest matrix and engagement strategy.

## Usage

```
/pm:stakeholder-map [project or initiative]
```

## What This Command Does

Creates stakeholder analysis with mapping, influence assessment, and communication plan.

## Instructions

1. Identify all stakeholders
2. Map on power/interest matrix
3. For each stakeholder:
   - Position (champion, supporter, neutral, skeptic, blocker)
   - Interests and concerns
   - Engagement strategy
   - Communication preferences

4. Create RACI matrix
5. Build communication plan

## Template

```markdown
# Stakeholder Map: [Initiative]

## Power/Interest Matrix

```
     High Power
         │
    ┌────┼────┐
    │ MANAGE  │  KEY
    │ CLOSELY │PLAYERS
    ┼─────────┼────────┤
    │ MONITOR │  KEEP
    │         │INFORMED
    └────┼────┘
      Low Interest → High
```

---

## Key Players (High Power, High Interest)

### [Name/Role - CEO]
**Position**:  Strong supporter
**Power**: 🔴 High
**Interest**: 🔴 High

**Interests**:
- [What they care about]

**Concerns**:
- [Their worries]

**Engagement Strategy**:
- Monthly 1:1 updates
- Include in key decisions
- Early wins visibility

**Communication**:
- Format: Executive summary
- Frequency: Monthly
- Channel: Email + presentations

---

## RACI Matrix

| Activity | PM | Eng | Design | Sales | Support |
|----------|----|----|---------|-------|---------|
| Strategy | A | C | C | I | I |
| PRD | R/A | C | C | I | I |
| Development | I | R/A | C | I | I |
| Launch | R/A | C | C | R | C |

**Legend**:
- R=Responsible, A=Accountable, C=Consulted, I=Informed

---

## Communication Plan

**Weekly**: Engineering team via Slack
**Monthly**: All stakeholders via roadmap review
**Quarterly**: Executives via business review
```

## Model
claude-sonnet-4-5

## Related
- `/pm:decision-log` - Document decisions
- `/pm:stakeholder-update` - Send updates
