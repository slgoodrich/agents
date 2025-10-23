---
description: End-to-end feature development from idea to launch and learning
category: Feature Development
duration: 12-16 weeks
model: sonnet
---

# Feature Lifecycle Workflow

End-to-end feature development from idea to launch and learning.

## Usage

```
/feature-lifecycle [feature idea or problem statement]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Feature idea or problem being solved
- Who requested it (customer, internal team, competitive gap)
- Why now (urgency, strategic importance)
- Expected impact (users affected, business metrics)
- Current stage (ideation, validated, ready to build)

## Overview

This workflow orchestrates the complete feature lifecycle:
**Idea → Discovery → Spec → Prioritization → Build → Launch → Learn**

## Timeline: 12-16 Weeks

## Workflow Phases

### Phase 1: Discovery & Validation (Weeks 1-2)

**Objective**: Validate problem and explore solutions

**Agents**:
- `user-researcher`: Conduct discovery research
- `product-strategist`: Assess strategic fit

**Activities**:
1. **Problem Validation**
   - User interviews (5-8 users)
   - Analyze existing data/feedback
   - Quantify problem impact

2. **Solution Exploration**
   - Competitive analysis
   - Solution sketching
   - Prototype concepts

3. **Strategic Assessment**
   - Alignment to product vision
   - Market opportunity sizing
   - Business case draft

**Deliverables**:
- Research synthesis report
- Problem/solution validation
- Initial business case

**Go/No-Go Decision**: Is this worth building?

---

### Phase 2: Specification (Week 3)

**Objective**: Define detailed requirements

**Agents**:
- `requirements-engineer`: Write comprehensive PRD
- `technical-pm`: Define technical approach
- `gtm-planner`: Plan go-to-market

**Activities**:
1. **PRD Creation**
   - Problem statement with evidence
   - User stories and acceptance criteria
   - Success metrics (KPIs)
   - Technical requirements
   - Scope (in/out)

2. **Technical Spec**
   - Architecture approach
   - API contracts
   - Data models
   - Performance requirements
   - Security considerations

3. **GTM Planning**
   - Positioning and messaging
   - Target audience
   - Launch channels
   - Beta program design

**Deliverables**:
- Complete PRD
- Technical specification
- GTM strategy doc

---

### Phase 3: Prioritization (Week 4)

**Objective**: Confirm priority and sequencing

**Agents**:
- `feature-prioritizer`: Score with RICE/ICE
- `stakeholder-manager`: Align stakeholders

**Activities**:
1. **Prioritization Scoring**
   - RICE score calculation
   - Value vs effort analysis
   - Dependencies mapping
   - Risk assessment

2. **Stakeholder Alignment**
   - Present business case
   - Review trade-offs
   - Secure buy-in
   - Resource allocation

3. **Roadmap Integration**
   - Sequence with other initiatives
   - Timeline estimation
   - Milestone definition

**Deliverables**:
- RICE scorecard
- Stakeholder sign-off
- Updated roadmap

**Go/No-Go Decision**: Is this the right priority now?

---

### Phase 4: Planning & Design (Weeks 5-6)

**Objective**: Plan sprint execution

**Agents**:
- `agile-coach`: Sprint planning
- `requirements-engineer`: Story breakdown

**Activities**:
1. **Epic Breakdown**
   - Break PRD into epics
   - Epics into user stories
   - Stories into tasks
   - Estimation (story points)

2. **Sprint Planning**
   - Sequence stories by dependencies
   - Allocate to sprints
   - Identify risks
   - Set sprint goals

3. **Design Handoff**
   - Design mockups/prototypes
   - Design system integration
   - Accessibility review

**Deliverables**:
- Sprint-ready backlog
- Multi-sprint plan
- Design specifications

---

### Phase 5: Build (Weeks 7-10, typically 2-4 sprints)

**Objective**: Develop and test feature

**Agents**:
- `agile-coach`: Facilitate sprints
- `stakeholder-manager`: Progress updates

**Activities Per Sprint**:
1. **Sprint Execution**
   - Daily standups
   - Development
   - Code reviews
   - Testing (unit, integration)

2. **Sprint Review**
   - Demo to stakeholders
   - Gather feedback
   - Adjust next sprint

3. **Retrospective**
   - What went well
   - What to improve
   - Action items

4. **Stakeholder Updates**
   - Weekly progress reports
   - Blockers and risks
   - Timeline adjustments

**Deliverables** (per sprint):
- Working increment
- Updated backlog
- Sprint report

**Milestone Review**: Is quality sufficient for launch?

---

### Phase 6: Launch (Weeks 11-12)

**Objective**: Release to users

**Agents**:
- `gtm-planner`: Execute GTM plan
- `stakeholder-manager`: Coordinate teams

**Activities**:
1. **Pre-Launch (Week 11)**
   - Beta program (if applicable)
   - Final QA and bug fixes
   - Launch assets (blog, email, docs)
   - Sales/support training
   - Go/no-go decision

2. **Launch (Day 0)**
   - Feature flag rollout (10% → 50% → 100%)
   - Announcement (blog, email, social)
   - Monitor metrics
   - War room for issues

3. **Post-Launch (Week 12)**
   - Daily metrics monitoring
   - User feedback collection
   - Bug triage and fixes
   - Optimization iterations

**Deliverables**:
- Launched feature
- Launch announcement
- Monitoring dashboards

---

### Phase 7: Learn & Iterate (Weeks 13-16)

**Objective**: Measure, learn, improve

**Agents**:
- `growth-pm`: Analyze metrics and optimize
- `user-researcher`: Gather qualitative feedback
- `product-strategist`: Assess strategic impact

**Activities**:
1. **Metrics Analysis** (Week 13-14)
   - Compare to success criteria
   - Cohort analysis
   - Funnel analysis
   - Identify drop-offs

2. **User Feedback** (Week 14-15)
   - User interviews (5-8)
   - Survey (NPS, satisfaction)
   - Support ticket analysis
   - Usage patterns

3. **Iteration Planning** (Week 15-16)
   - Identify quick wins
   - Plan v1.1 improvements
   - Measure ROI
   - Document learnings

4. **Strategic Review**
   - Did we achieve OKRs?
   - Market reception
   - Competitive response
   - Next steps

**Deliverables**:
- Success metrics report
- User feedback synthesis
- Iteration backlog
- Lessons learned doc

---

## Success Criteria

### Discovery Phase
- ✅ Problem validated with 5+ users
- ✅ Potential impact quantified
- ✅ Strategic alignment confirmed

### Specification Phase
- ✅ PRD approved by stakeholders
- ✅ Technical approach validated
- ✅ GTM plan reviewed

### Prioritization Phase
- ✅ RICE score justifies build
- ✅ Resources allocated
- ✅ Stakeholders aligned

### Build Phase
- ✅ All acceptance criteria met
- ✅ Test coverage >80%
- ✅ Zero critical bugs
- ✅ Performance requirements met

### Launch Phase
- ✅ Rollout complete
- ✅ No major incidents
- ✅ Announcement published

### Learn Phase
- ✅ Success metrics tracked
- ✅ User feedback collected
- ✅ Learnings documented

---

## Decision Points

### After Discovery
**Go**: Problem is validated, strategic fit is strong
**Pivot**: Explore different solution
**Kill**: Problem not significant enough

### After Prioritization
**Go**: RICE score justifies immediate build
**Defer**: Good idea, but other priorities higher
**Kill**: Not worth the effort

### Before Launch
**Go**: Quality is sufficient, metrics in place
**Delay**: Critical bugs or missing requirements
**Kill**: Changed priorities or assumptions invalid

---

## Timeframe

**Typical Timeline**: 12-16 weeks from idea to learning

- Discovery: 2 weeks
- Specification: 1 week
- Prioritization: 1 week
- Planning: 2 weeks
- Build: 4 weeks (2-4 sprints)
- Launch: 2 weeks
- Learn: 4 weeks

**Fast Track**: 6-8 weeks (for simple features)
**Complex**: 20+ weeks (for major initiatives)

---

## Roles & Responsibilities

**Product Manager** (You):
- Drive overall process
- Make go/no-go decisions
- Stakeholder alignment
- Prioritization

**Engineering**:
- Technical design
- Development
- QA and deployment

**Design**:
- User research support
- Mockups and prototypes
- Design QA

**Marketing/GTM**:
- Launch planning
- Messaging
- Announcement execution

**Data/Analytics**:
- Metrics definition
- Tracking implementation
- Analysis and reporting

---

## Templates & Tools

Use these commands throughout the workflow:

**Discovery**:
- `/user-research:interview-guide` - Research planning
- `/user-research:research-synthesize` - Analysis

**Specification**:
- `/requirements-engineering:prd` - PRD generation
- `/requirements-engineering:user-stories` - Story creation

**Prioritization**:
- Tell `feature-prioritizer` - RICE scoring

**Planning**:
- `/agile-coaching:sprint-plan` - Sprint planning
- `/agile-coaching:backlog-groom` - Backlog prep

**Launch**:
- `/product-operations:release-notes` - Announcements
- Tell `gtm-planner` - GTM execution

**Learn**:
- `/product-analytics:kpi-dashboard` - Metrics
- `/product-analytics:experiment` - Optimization tests

---

## Example Execution

```
User: Let's build multi-factor authentication

Workflow:

Week 1-2: Discovery
→ Tell user-researcher: "Design study to validate MFA need"
→ [Conduct 8 enterprise customer interviews]
→ Tell user-researcher: "Synthesize findings"
→ Result: 90% of enterprise prospects require MFA

Week 3: Specification
→ /requirements-engineering:prd "Multi-factor authentication for enterprise users"
→ Tell requirements-engineer: "Add technical security requirements"
→ Tell gtm-planner: "Plan enterprise launch for MFA"

Week 4: Prioritization
→ Tell feature-prioritizer: "Score MFA with RICE"
→ Result: RICE = 3200 (high priority)
→ Tell stakeholder-manager: "Present MFA business case to exec team"
→ Result: Approved, resourced

Week 5-6: Planning
→ /requirements-engineering:user-stories [paste PRD]
→ /agile-coaching:sprint-plan "Sprint 47: MFA Phase 1"
→ Result: 4-sprint plan created

Week 7-10: Build
→ 4 sprints of development
→ Weekly stakeholder updates
→ Sprint demos

Week 11-12: Launch
→ Beta with 20 enterprise customers
→ General availability rollout
→ Blog post and sales enablement

Week 13-16: Learn
→ Track: 15% of users enable MFA
→ Interview 10 users: "Why/why not enable MFA?"
→ Plan v1.1: SMS fallback option
→ Result: Enterprise ARR +$50K
```

---

## Workflow Orchestration

This workflow uses the Task tool to delegate to specialized agents:

```
Phase 1: Task(user-researcher, "Discovery research")
Phase 2: Task(requirements-engineer, "Write PRD")
Phase 3: Task(feature-prioritizer, "RICE scoring")
Phase 4: Task(agile-coach, "Sprint planning")
Phase 5: [Manual: Engineering builds]
Phase 6: Task(gtm-planner, "Execute launch")
Phase 7: Task(growth-pm, "Analyze and optimize")
```

Each task runs autonomously and returns results.

---

## Adaptations

**For Small Features**: Skip or compress phases
**For Large Initiatives**: Add more discovery, multiple betas
**For Technical Debt**: Lighter discovery, heavier technical spec
**For UX Improvements**: More usability testing, faster iterations

---

**Model**: Sonnet (Complex multi-phase reasoning)
**Related Workflows**: quarterly-planning, product-launch, discovery-sprint
