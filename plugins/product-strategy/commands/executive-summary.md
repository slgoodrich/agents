# Executive Summary Generator

Generate concise executive briefings and updates optimized for leadership consumption.

## Usage

```
/pm:exec-summary [topic or project] [optional: audience level, format]
```

## What This Command Does

1. Creates executive-level summaries following best practices
2. Leads with TL;DR and key decision points
3. Uses data visualization and metrics formatting
4. Structures complex information in scannable format
5. Adapts tone and depth for different executive levels (VP, C-suite, Board)
6. Highlights risks, decisions, and action items

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Audience & Purpose**:
- Who is this for? (VP, C-level, Board, specific exec by name)
- What's their role and priorities? (CEO cares about revenue, CTO cares about technology)
- What type of summary? (status update, decision brief, incident report, business review, board update)
- What format do they prefer? (email, PDF, slides, memo, dashboard)
- How much time will they spend reading? (2 min scan, 5 min read, pre-read for meeting)

**Content Inputs**:
- What topic or project is this about? (specific initiative, product area, company performance)
- What time period does this cover? (this week, Q1, past month)
- What's the current status? (on track, at risk, blocked, completed, crisis)
- What decision or action do you need from them? (approval, guidance, resources, just FYI)

**Context & Data**:
- What metrics or KPIs should be included? (revenue, users, OKRs, project milestones)
- What are the key accomplishments or wins?
- What are the risks or blockers?
- What decisions were made this period?
- What help is needed? (resources, escalation, approval)

**Background**:
- How much context does the exec have? (deeply involved vs distant observer)
- When was their last update? (to show delta from last time)
- What concerns or questions have they raised before?
- Are there any sensitivities or hot topics? (customer escalations, competitor moves)

**Strategic Context**:
- How does this tie to company goals or OKRs?
- What's the business impact? (revenue, users, risk, competitive advantage)
- What trade-offs or difficult choices were made?

### 2. Identify Summary Type

- **Status Update** - Project/initiative progress
- **Decision Brief** - Requesting approval or decision
- **Incident Report** - Problem summary and resolution
- **Business Review** - Metrics and performance summary
- **Strategic Recommendation** - Proposal or new direction
- **Board Update** - High-level quarterly/annual summary

### 3. Gather and Synthesize Content

- Core message (what they need to know)
- Current status or situation
- Key metrics or data points
- Decisions needed
- Risks and mitigations
- Next steps and timeline
- Resource requirements

### 4. Structure for Skimming
   - **Pyramid structure**: Most important first
   - **Scannable formatting**: Headers, bullets, bold
   - **Data visualization**: Tables, simple charts
   - **Page limits**: 1 page for VP, 2 pages for C-suite, 3 slides for Board

4. **Executive Communication Principles**:
   - **Lead with the bottom line** - Answer "so what?" immediately
   - **Be concise** - Executives read diagonally
   - **Use data** - Quantify everything possible
   - **Show confidence** - Clear recommendations, not options overload
   - **Respect their time** - Assume 2-3 minutes reading time

## Template

### Status Update Format

```markdown
# Executive Summary: [Project/Initiative Name]

**Date**: [Date]
**Author**: [Name, Role]
**For**: [Exec name/role]

---

## TL;DR

[2-3 sentences max. Current status, key accomplishment or concern, what you need from them if anything.]

**Status**: 🟢 On Track | 🟡 At Risk | 🔴 Blocked

---

## Key Metrics

| Metric | Target | Current | Status | Trend |
|--------|--------|---------|--------|-------|
| [Metric 1] | [Goal] | [Actual] | 🟢 | ↗️ +12% |
| [Metric 2] | [Goal] | [Actual] | 🟡 | → Flat |
| [Metric 3] | [Goal] | [Actual] | 🔴 | ↘️ -8% |

**Overall Health**: [X]% to goal | [Y]% complete | On track for [Date]

---

## Progress Highlights

**Accomplished**:
- ✅ [Major milestone 1] - [Impact]
- ✅ [Major milestone 2] - [Impact]
- ✅ [Major milestone 3] - [Impact]

**In Flight**:
- 🚧 [Current priority 1] - [% complete, ETA]
- 🚧 [Current priority 2] - [% complete, ETA]

---

## Risks & Mitigations

**🔴 Critical**: [Risk requiring escalation]
- **Impact**: [Business impact if unresolved]
- **Mitigation**: [What we're doing]
- **Ask**: [What you need from exec]

**🟡 Moderate**: [Risk being managed]
- **Impact**: [Potential impact]
- **Mitigation**: [Current plan]
- **Status**: [Monitoring/In progress]

---

## Decisions Needed

**Decision**: [What needs to be decided]
- **Options**: [A] [Recommended] | [B] Alternative
- **Recommendation**: [Option A] because [key reason]
- **Timing**: Need decision by [Date] to [avoid/achieve what]
- **Impact**: [What happens with each option]

---

## Next Steps

**Immediate** (This week):
- [Action 1]
- [Action 2]

**Near term** (This month):
- [Milestone 1] - [Date]
- [Milestone 2] - [Date]

---

## Ask

[Specific request: approval, resource, unblock, guidance - be clear and direct]
```

### Decision Brief Format

```markdown
# Executive Decision Brief: [Topic]

**Date**: [Date]
**Decision Needed By**: [Date]
**Recommended By**: [Name, Role]

---

## Recommendation

[One sentence: We should do X because Y]

**Confidence Level**: High | Medium | Low
**Reversibility**: Easy to reverse | ⚠️ Difficult | 🔴 One-way door

---

## Context

**Current Situation**:
[2-3 sentences: What's happening now, why we need to decide]

**Why Now**:
[1-2 sentences: Time sensitivity, opportunity window, escalating cost of delay]

**Stakeholders Aligned**:
✅ Engineering | ✅ Design | ⚠️ Sales (concerns noted) | ❌ Finance (opposed)

---

## Options Analysis

### Option A: [Recommended Option]

**Description**: [What we do]

**Pros**:
- [Benefit 1 with data]
- [Benefit 2 with data]
- [Benefit 3 with data]

**Cons**:
- [Drawback 1 and mitigation]
- [Drawback 2 and mitigation]

**Cost/Effort**: [$X] / [Y person-weeks] / [Z months]
**Expected Outcome**: [Quantified benefit]

---

### Option B: [Alternative]

**Description**: [What we do]

**Pros**: [Key benefits]
**Cons**: [Key drawbacks]
**Cost/Effort**: [Resource requirements]

**Why not recommended**: [1-2 sentence rationale]

---

### Option C: Do Nothing

**Impact if we don't act**:
- [Consequence 1]
- [Consequence 2]
- [Opportunity cost]

---

## Trade-offs We're Accepting

- [What we're giving up or risking with recommendation]
- [What we're explicitly NOT doing]

---

## Success Metrics

**How we'll measure**:
- [Metric 1]: From [X] to [Y] by [Date]
- [Metric 2]: Achieve [Z] by [Date]

**Review checkpoint**: [Date to assess if working]

---

## Next Steps if Approved

1. [Immediate action 1] - [Timeline]
2. [Immediate action 2] - [Timeline]
3. [Key milestone] - [Date]

**First update**: [When you'll report back]
```

### Incident Report Format

```markdown
# Incident Executive Summary

**Incident**: [Brief title]
**Date/Time**: [When it occurred]
**Duration**: [How long]
**Impact**: [Who/what affected]
**Status**: 🔴 Ongoing | 🟡 Mitigating | ✅ Resolved

---

## TL;DR

[2-3 sentences: What happened, impact, current status, resolution if resolved]

---

## Impact

**Customers Affected**: [Number/percentage]
**Revenue Impact**: [$X] / [Y% of MRR]
**Reputation Impact**: [Social media, press, customer sentiment]
**SLA Breach**: Yes [X hours] | No

**Critical Customer Calls**:
- [Company 1] - [Status]
- [Company 2] - [Status]

---

## Timeline

| Time | Event |
|------|-------|
| [HH:MM] | Initial incident detected |
| [HH:MM] | Team mobilized, incident commander assigned |
| [HH:MM] | Root cause identified |
| [HH:MM] | Mitigation deployed |
| [HH:MM] | Service restored |
| [HH:MM] | Full resolution confirmed |

**Total Downtime**: [X hours Y minutes]

---

## Root Cause

**What happened**: [Non-technical explanation]

**Why it happened**: [Underlying cause]

**Why it wasn't caught**: [Prevention gap]

---

## Resolution & Prevention

**Immediate fixes applied**:
- ✅ [Fix 1]
- ✅ [Fix 2]

**Permanent fixes committed** (with timeline):
- [ ] [Prevention 1] - [Date]
- [ ] [Prevention 2] - [Date]
- [ ] [Prevention 3] - [Date]

**Process improvements**:
- [Change to prevent recurrence]

---

## Customer Communication

**Completed**:
- ✅ Status page updated
- ✅ Email to affected customers
- ✅ Individual outreach to top 10 customers

**Pending**:
- [ ] Post-mortem blog post - [Date]
- [ ] Credit/compensation process - [Date]

---

## Ask

[If any: executive customer calls, public statement approval, additional resources]
```

### Business Review Format

```markdown
# [Quarter/Month] Business Review

**Period**: [Q1 2025 / January 2025]
**Prepared by**: [Name, Role]
**Date**: [Date]

---

## TL;DR

**Performance**: [Above/Met/Below expectations]
**Key Win**: [Biggest success this period]
**Key Miss**: [Biggest challenge or miss]
**Focus for Next Period**: [Top priority]

---

## Scorecard

| OKR/Goal | Target | Actual | Score | Status |
|----------|--------|--------|-------|--------|
| [Objective 1] | [Target] | [Actual] | 0.8 | 🟢 |
| [Objective 2] | [Target] | [Actual] | 0.5 | 🟡 |
| [Objective 3] | [Target] | [Actual] | 0.3 | 🔴 |

**Overall Score**: [0.X] / 1.0

---

## Financial Performance

| Metric | Plan | Actual | Variance | YoY |
|--------|------|--------|----------|-----|
| Revenue | $[X]M | $[Y]M | [+/-]% | [+/-]% |
| ARR | $[X]M | $[Y]M | [+/-]% | [+/-]% |
| NRR | [X]% | [Y]% | [+/-] pts | [+/-] pts |
| CAC | $[X] | $[Y] | [+/-]% | [+/-]% |
| LTV:CAC | [X]:1 | [Y]:1 | [+/-] | [+/-] |

**Trend**: ↗️ Growing | → Stable | ↘️ Declining

---

## Key Accomplishments

1. **[Accomplishment 1]** - [Impact/metric]
2. **[Accomplishment 2]** - [Impact/metric]
3. **[Accomplishment 3]** - [Impact/metric]

---

## Challenges & Misses

1. **[Challenge 1]** - [What, why, impact, plan]
2. **[Challenge 2]** - [What, why, impact, plan]

---

## Customer Highlights

**Wins**:
- New logo: [Company] - $[X]
- Expansion: [Company] - +$[Y]
- Testimonial: "[Quote]" - [Customer]

**Churn/Risk**:
- Lost: [Company] - $[X] - Reason: [Why]
- At risk: [Company] - $[Y] - Mitigation: [Plan]

---

## Product Releases

**Shipped**:
- [Feature 1] - [Adoption: X%, Impact: Y]
- [Feature 2] - [Adoption: X%, Impact: Y]

**Coming Next**:
- [Upcoming 1] - [Date]
- [Upcoming 2] - [Date]

---

## Team & Operations

**Headcount**: [Current] ([+/-X] from last period)
**Open Roles**: [Number] ([Critical/Important/Future])
**Attrition**: [X]% ([vs Y% goal])

---

## Next Period Priorities

1. [Priority 1] - [Expected outcome]
2. [Priority 2] - [Expected outcome]
3. [Priority 3] - [Expected outcome]

**Resource needs**: [Any asks for budget, headcount, etc.]
```

## Best Practices

### DO ✅

- **Lead with TL;DR** - Put the most important information first, assume they won't read further
- **Be concise** - Executives scan, they don't read word-for-word
- **Use data** - Quantify everything you can, numbers beat adjectives
- **Show trend** - Not just current state but direction (↗️ improving, → flat, ↘️ declining)
- **Make a recommendation** - Don't present 5 options, recommend one and explain why
- **Be honest about risks** - Transparency builds trust, hiding problems destroys it
- **Respect their time** - Aim for 2-3 minute read time, link to details
- **Use visual status** - 🟢🟡🔴 indicators for instant understanding
- **Be specific with asks** - "Need decision on pricing by Friday" beats "Seeking guidance"
- **Format for skimming** - Bullets, bold, tables, headers, white space

### DON'T ❌

- **Don't bury the lede** - Answer "so what?" in the first sentence
- **Don't write paragraphs** - Use bullets, keep paragraphs to 2-3 sentences max
- **Don't use jargon** - Unless you're certain they know it (spell out acronyms first time)
- **Don't be vague** - "Making progress" → "80% complete, ships Friday"
- **Don't oversell** - Be confident but realistic, avoid superlatives
- **Don't present 5 options** - Maximum 2-3, with clear recommendation
- **Don't hide bad news** - Put it upfront with mitigation plan
- **Don't assume context** - Briefly restate what project is about
- **Don't use passive voice** - "We decided" beats "It was decided"
- **Don't send without proofreading** - Typos undermine credibility with execs

## Executive Communication Best Practices

### For VPs
- **Length**: 1 page max
- **Detail**: Tactical and strategic mix
- **Frequency**: Weekly or bi-weekly
- **Focus**: Progress, blockers, decisions
- **Tone**: Direct, detailed

### For C-Suite
- **Length**: 1-2 pages or 5-minute read
- **Detail**: Strategic focus, high-level
- **Frequency**: Monthly or quarterly
- **Focus**: Business impact, risks, major decisions
- **Tone**: Concise, confident, data-driven

### For Board
- **Length**: 3-5 slides or 2-page memo
- **Detail**: Very high-level
- **Frequency**: Quarterly
- **Focus**: Strategy, financial metrics, major risks/opportunities
- **Tone**: Polished, strategic, forward-looking

## Formatting Guidelines

**Use**:
- ✅ Bullet points over paragraphs
- ✅ Bold for key information
- ✅ Tables for data comparison
- ✅ Status emojis (🟢🟡🔴) for quick scanning
- ✅ Specific numbers over vague terms
- ✅ Headers and sections for structure

**Avoid**:
- ❌ Long paragraphs (>3 sentences)
- ❌ Jargon without context
- ❌ Qualifiers ("somewhat", "might", "possibly")
- ❌ Passive voice
- ❌ Burying the lede

## Example

**Input**: "Executive summary for Q1 product performance for CEO"

**Output**:

```markdown
# Q1 2025 Product Performance - Executive Summary

**For**: CEO
**From**: VP Product
**Date**: April 5, 2025

---

## TL;DR

Q1 exceeded product OKRs (0.8/1.0 overall) driven by strong new feature adoption (40% of users). Mobile app launch successful with 15K downloads. Main concern: enterprise feature gaps causing deal delays ($500K pipeline at risk).

**Status**: 🟢 Strong quarter, some enterprise headwinds

---

## Scorecard

| OKR | Target | Actual | Score | Status |
|-----|--------|--------|-------|--------|
| New feature adoption | 25% | 40% | 1.0 | 🟢 Exceeded |
| Mobile downloads | 10K | 15K | 1.0 | 🟢 Exceeded |
| Enterprise revenue | $400K | $280K | 0.7 | 🟡 Behind |
| NPS | 50 | 48 | 0.6 | 🟡 Close |

**Overall**: 0.8/1.0 (Above target)

---

## Key Wins

1. **New dashboard feature** - 40% adoption in 30 days, driving 15% increase in daily engagement
2. **Mobile app launch** - 15K downloads, 4.8 star rating, 25% of DAUs now mobile
3. **Product-led growth** - 35% of trials converting without sales touch (up from 28%)

---

## Challenges

**🔴 Enterprise gap causing deal delays**:
- $500K in pipeline delayed due to missing SSO/SAML
- Sales requesting 3-month acceleration of enterprise roadmap
- Recommendation: Pull forward enterprise features to Q2 (requires 2 additional engineers)

---

## Q2 Priorities

1. Enterprise tier features (SSO, SAML, audit logs)
2. Mobile parity with web (60% feature coverage)
3. API v2 launch for integration partners

**Resource ask**: 2 engineers for enterprise acceleration
```

## Model

Use: Sonnet

## Related

- `/pm:status` - Status updates (more tactical)
- `/pm:decision-log` - Document decisions mentioned
- `/pm:meeting-agenda` - Prepare for exec meetings
- `/pm:stakeholder-map` - Executive stakeholder management
- `/workflows:monthly-business-review` - Monthly executive summaries
