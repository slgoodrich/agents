# MVP Scoper

Define minimum viable product scope with laser focus on core value and launch readiness.

## Usage

```
/continuous-discovery:mvp [product idea or feature] [optional: target users, timeline]
```

## What This Command Does

1. Defines crisp MVP scope using value-first principles
2. Separates must-haves from nice-to-haves with clear rationale
3. Creates launch-ready feature set that proves core value proposition
4. Identifies success metrics and validation criteria
5. Prevents scope creep with disciplined "out of scope" documentation
6. Takes 30 minutes vs 3 hours of manual MVP scoping

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Product/Feature Context**:
- Product or feature idea (what are we building?)
- Target users (who is this for?)
- Core problem being solved (why does this matter?)
- Business goals (what do we need to prove?)
- Timeline constraints (when does this need to launch?)

**Competitive Context**:
- Existing solutions (what exists today?)
- Your differentiation (why build this?)

**Resource Context**:
- Team size and composition
- Available timeline (weeks/months)
- Technical constraints or dependencies

**Example Input**:
```
Product Idea: AI-powered meeting notes app
Target Users: Remote teams, 5-50 people
Problem: Teams forget action items, spend time note-taking
Business Goal: Prove willingness to pay $10/user/month
Timeline: Launch MVP in 6 weeks
Team: 2 engineers, 1 designer, 1 PM
```

### 2. Define Core Value Proposition

Identify the **one thing** this MVP must deliver:

**Framework**: [User] can [action] without [pain point] so they can [outcome]

**Example**:
```
Remote teams can capture and share meeting action items
without manual note-taking
so they can stay aligned and accountable
```

### 3. Apply MVP Scoping Principles

**Must-Have Criteria** (all must be true):
- ✅ Delivers on core value proposition
- ✅ Required for product to be usable
- ✅ Must exist for success metrics to be measurable
- ✅ Can't be easily worked around
- ✅ Differentiates from existing solutions

**Nice-to-Have (Out of Scope)** if:
- ⚠️ Enhances experience but not required for core value
- ⚠️ Can be added after initial validation
- ⚠️ Users can work around it
- ⚠️ Significantly extends timeline

### 4. Scope the MVP

**Must-Haves**:
- Features absolutely required for core value
- Minimum quality bar (not "perfect", but "good enough")
- Success metrics infrastructure

**Out of Scope** (for V1):
- Features that enhance but don't deliver core value
- Optimizations and polish
- Edge cases (document, handle in V2)

**Launch Criteria**:
- What must be true to launch?
- How do we measure success?
- When do we decide to iterate or pivot?

### 5. Create MVP Roadmap

**Week-by-week plan**:
- Milestones and deliverables
- Validation checkpoints
- Launch readiness gates

## Templates

### MVP Scope Document

```markdown
# MVP Scope: [Product/Feature Name]

**Date**: [YYYY-MM-DD]
**PM**: [Your Name]
**Timeline**: [X] weeks to launch
**Team**: [Team composition]

---

## Core Value Proposition

**One Sentence**:
[User] can [action] without [pain point] so they can [outcome]

**Problem We're Solving**:
[Description of user pain point, validated by research or data]

**Why Now**:
- Market opportunity: [Why is this timely?]
- Competitive gap: [What differentiation?]
- Business need: [What do we need to prove?]

---

## Target Users (MVP)

**Primary User Segment**:
- **Who**: [Specific user description]
- **Size**: [How many users in this segment?]
- **Why Start Here**: [Why this segment first?]

**User Needs** (prioritized):
1. [Need 1] - CRITICAL - Must be addressed in MVP
2. [Need 2] - CRITICAL - Must be addressed in MVP
3. [Need 3] - Important - V2 consideration
4. [Need 4] - Nice to have - Future

---

## Must-Have Features (In Scope)

### Feature 1: [Feature Name]

**Why Must-Have**: [How does this deliver core value?]

**User Story**:
As a [user type]
I want to [action]
So that [outcome]

**Acceptance Criteria**:
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

**Success Metric**: [How we measure if this works]

**Quality Bar**: [Good enough definition - not perfect, but usable]

---

### Feature 2: [Feature Name]

[Repeat structure for each must-have feature]

---

## Out of Scope (V1)

### Explicitly NOT Included:

| Feature | Why Out of Scope | Workaround | When to Revisit |
|---------|------------------|------------|-----------------|
| [Feature 1] | Enhances but doesn't deliver core value | [Manual process or alternative] | V2 after validation |
| [Feature 2] | Optimization, not required for launch | [Users can tolerate slower performance] | V2 if usage grows |
| [Feature 3] | Edge case, affects <5% of users | [Document limitation] | V3 if users request |
| [Feature 4] | Nice-to-have polish | [Basic version sufficient] | V2 after feedback |

**Deferred Improvements**:
- [Polish item 1] - Not required for core value
- [Optimization 1] - Can be slower for MVP
- [Edge case handling] - Document known limitations

---

## Success Metrics

**North Star Metric** (validates core value):
[Primary metric that proves users get value]

**Goal**: From [current] to [target] in [timeline]

**Leading Indicators**:
- [Metric 1]: [Target] - Measures [what]
- [Metric 2]: [Target] - Measures [what]
- [Metric 3]: [Target] - Measures [what]

**Validation Criteria**:
- ✅ **Success**: [Metric] reaches [X], proceed to scale
- ⚠️ **Partial Success**: [Metric] reaches [Y], iterate
- ❌ **Failure**: [Metric] below [Z], pivot or cut

---

## Launch Criteria (Definition of Done)

**Product Readiness**:
- [ ] All must-have features complete and tested
- [ ] Core user journey works end-to-end
- [ ] Success metrics instrumented and validated
- [ ] Known bugs: 0 critical, <5 high
- [ ] Performance: Acceptable for MVP scale

**Go-to-Market Readiness**:
- [ ] Target users identified and recruited
- [ ] Positioning and messaging defined
- [ ] Support plan in place (FAQs, docs)
- [ ] Pricing decided (if applicable)

**Team Readiness**:
- [ ] Monitoring and alerts configured
- [ ] Rollback plan tested
- [ ] Team trained on how to support
- [ ] Launch communication prepared

**We Launch When**: All critical items above are ✅

---

## MVP Roadmap

### Week 1-2: Foundation
**Deliverables**:
- [Core infrastructure]
- [Basic feature 1]
- [Authentication/setup]

**Milestone**: Core foundation in place

---

### Week 3-4: Core Features
**Deliverables**:
- [Must-have feature 1] complete
- [Must-have feature 2] complete
- [Integration 1]

**Milestone**: Core value deliverable

---

### Week 5: Polish & Testing
**Deliverables**:
- Bug fixes (P0, P1)
- User testing with 5-10 beta users
- Metrics validation

**Milestone**: Beta-ready

---

### Week 6: Launch Prep & Launch
**Deliverables**:
- Final bug fixes
- Docs and support materials
- Soft launch to limited users
- Monitor and iterate

**Milestone**: MVP launched

---

## Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [Risk 1: e.g., Technical complexity underestimated] | High | High | [Buffer week built in, scope cut if needed] |
| [Risk 2: e.g., User adoption lower than expected] | Medium | High | [Beta test with real users week 5] |
| [Risk 3: e.g., Competitor launches similar] | Low | Medium | [Monitor competitive landscape] |

---

## Open Questions

- [ ] [Question 1 that needs answering before launch]
- [ ] [Question 2 that needs answering before launch]

**Owner**: [Who's responsible for answering]
**Deadline**: [When we need the answer]

---

## Stakeholder Alignment

**Decision Makers**:
- [Name/Role]: ✅ Approved | ⚠️ Has concerns | ❌ Blocks

**Concerns to Address**:
- [Stakeholder 1 concern]: [How we're addressing it]

---

## Post-Launch Plan

**Week 1 After Launch**:
- Monitor metrics daily
- User interviews with 10 users
- Bug triage and hot fixes

**Week 2-4 After Launch**:
- Assess vs success criteria
- Decide: Scale, Iterate, or Pivot
- Plan V2 based on learnings

**Success = Proceed to V2**:
If metrics hit targets, V2 adds:
- [Feature from out-of-scope list]
- [Optimization based on user feedback]
- [Next user segment expansion]
```

---

## Best Practices

### DO ✅

- **Start with value, not features** - Define what users can do, then work backward
- **Be ruthlessly minimal** - When in doubt, cut it from V1
- **Focus on one user segment** - Don't try to serve everyone in MVP
- **Set clear success metrics** - Define what "validated" means upfront
- **Plan for validation, not perfection** - MVP is learning tool, not final product
- **Document out-of-scope explicitly** - Prevents scope creep later
- **Include launch criteria** - Know when you're actually done

### DON'T ❌

- **Include "nice-to-haves"** - If you can't explain why it's must-have, cut it
- **Aim for perfect quality** - MVP quality bar is "good enough", not "perfect"
- **Try to serve all users** - Pick one segment, nail it, then expand
- **Build without success metrics** - Instrument metrics from day 1
- **Scope creep mid-build** - Lock scope, add to V2 backlog instead
- **Launch without validation plan** - Know how you'll measure success
- **Forget about post-launch** - Plan for learning and iteration

---

## Examples

### Example 1: Meeting Notes App

**Input**: "AI-powered meeting notes app for remote teams, launch in 6 weeks"

**Output**:

```markdown
# MVP Scope: AI Meeting Notes App

**Timeline**: 6 weeks to launch
**Team**: 2 engineers, 1 designer, 1 PM

---

## Core Value Proposition

Remote teams can capture and share meeting action items automatically
without manual note-taking
so they can stay aligned and accountable

---

## Must-Have Features (V1)

### 1. Meeting Recording Integration
- **Why**: Can't capture notes without recording
- **Quality Bar**: Works with Zoom and Google Meet
- **Out of Scope**: Teams, Webex (add in V2)

### 2. AI Action Item Extraction
- **Why**: Core value - automates note-taking
- **Quality Bar**: 80% accuracy on action items
- **Out of Scope**: Full transcript, sentiment analysis

### 3. Shared Action Item Dashboard
- **Why**: Team needs to see and track action items
- **Quality Bar**: Simple list view, assign to people
- **Out of Scope**: Calendar integration, reminders (V2)

### 4. Email Summary
- **Why**: Distribution mechanism
- **Quality Bar**: Plain text email after meeting
- **Out of Scope**: Slack integration, in-app notifications (V2)

---

## Out of Scope (V1)

| Feature | Why Out of Scope | When to Add |
|---------|------------------|-------------|
| Slack integration | Nice-to-have, email works for V1 | V2 if users request |
| Calendar sync | Optimization, manual works | V2 after validation |
| Meeting analytics | Enhancement, not core value | V3 |
| Custom AI training | Edge case, generic AI works | V3 if needed |
| Mobile app | Desktop web sufficient for V1 | V2 if mobile users |

---

## Success Metrics

**North Star**: Teams completing action items from meetings

**Goal**: 30 teams using weekly, 60% of action items completed within 1 week

**Validation Criteria**:
- ✅ Success: 30+ teams, 60%+ completion → Scale to V2
- ⚠️ Partial: 15-30 teams, 40-60% completion → Iterate
- ❌ Failure: <15 teams, <40% completion → Pivot

---

## MVP Roadmap

**Week 1-2**: Recording integration + AI extraction
**Week 3-4**: Dashboard + email summary
**Week 5**: Beta testing with 10 teams
**Week 6**: Launch to 30 target teams

**Launch Criteria**: All 4 must-haves working, metrics instrumented, 10 beta teams validated
```

---

### Example 2: Analytics Dashboard Feature

**Input**: "Custom analytics dashboard for B2B SaaS product"

**Output**:

```markdown
# MVP Scope: Custom Analytics Dashboard

**Timeline**: 4 weeks to launch
**Team**: 2 engineers, 1 designer

---

## Core Value Proposition

Power users can see their key metrics at a glance
without digging through multiple reports
so they can make faster data-driven decisions

---

## Must-Have Features (V1)

### 1. Dashboard Builder UI
- Drag-and-drop widget placement
- 3 widget types: Number, Chart, Table
- Save custom layouts

### 2. 5 Pre-built Widgets
- Active Users (number)
- Revenue (chart over time)
- Top Features (table)
- Growth Rate (number)
- User Engagement (chart)

### 3. Dashboard Sharing
- Share read-only link with team
- Public/private toggle

---

## Out of Scope (V1)

- Custom widget creation (V2)
- Scheduled email reports (V2)
- Real-time data (<5 min is fine for V1)
- Dashboard templates (V2)
- Export to PDF (V2)

---

## Success Metrics

**Goal**: 20% of active users create a dashboard in first 2 weeks

**Validation**: If 100+ dashboards created, expand to more widget types in V2
```

---

## Model

Use: Sonnet

---

## Related

- `/requirements-engineering:prd` - Full PRD for MVP features
- `/strategic-planning:roadmap` - Place MVP on roadmap timeline
- `/product-analytics:impact` - Estimate impact of MVP features
- `/requirements-engineering:user-stories` - Break MVP features into user stories
- `/product-analytics:experiment` - Design validation experiments for MVP
- `/continuous-discovery:discovery-sprint` - Validate MVP assumptions before building
- `product-strategist` agent - Strategic MVP decisions and scope trade-offs
- `requirements-engineer` agent - Detailed requirements for MVP features
- `feature-prioritizer` agent - Prioritize must-haves using frameworks
