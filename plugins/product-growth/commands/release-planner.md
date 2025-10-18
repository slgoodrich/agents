# Release Planner

Plan multi-sprint releases with coordinated feature rollouts, testing, and launch readiness.

## Usage

```
/pm:release-plan [release version or name] [timeline]
```

## What This Command Does

1. Plans multi-sprint releases with feature dependencies and staging
2. Creates sprint-by-sprint breakdown of work and milestones
3. Coordinates testing, QA, and launch readiness activities
4. Identifies critical path and risks to release timeline
5. Generates launch checklist and go/no-go criteria
6. Takes 45 minutes vs 3 hours of manual release planning

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Release Basics**:
- What's the release name or version? (v2.0, Q1 2025 Release, Enterprise Launch, "Project Phoenix")
- What's the target launch date? (specific date or quarter)
- How much time until launch? (weeks or months available)
- What type of release is this? (major feature release, minor update, patch, rebranding)

**Scope & Features**:
- What features or epics are included? (list of major features/capabilities)
- What's the primary goal of this release? (the one thing this release achieves)
- Which features are must-haves? (non-negotiable for launch)
- Which features are nice-to-haves? (could be cut or delayed if needed)
- Are there dependencies between features? (feature B requires feature A)

**Team & Capacity**:
- Who's on the team? (number of engineers, designers, QA, PM)
- What's the team's velocity? (story points per sprint, if known)
- Are there any planned PTO or holidays? (affects capacity)
- Are there other commitments? (support work, other projects taking capacity)

**Timeline & Constraints**:
- Is the date fixed or flexible? (hard deadline vs target date)
- Why this date? (customer commitment, event, competitive pressure, end of quarter)
- What happens if we miss the date? (severity of delay)
- Are there intermediate milestones? (beta launch, dogfooding start, customer preview)

**Launch Context**:
- How are we launching? (big bang, phased rollout, beta first, feature flags)
- Who's the target audience? (all users, specific segment, enterprise customers)
- What's the communication plan? (blog post, email, in-app, event)
- Are there dependencies outside the team? (marketing, sales enablement, legal, compliance)

**Quality & Risk**:
- What's the quality bar? (MVP acceptable vs production-grade polish)
- What are the risks? (technical unknowns, new tech, complex integration)
- What testing is required? (security audit, performance testing, accessibility, beta testing)
- What's the go/no-go criteria? (what must be true to ship)

**Previous Releases** (if applicable):
- How did the last release go? (learn from what worked or didn't)
- Are there lessons learned to apply? (process improvements)
- What's the release cadence? (monthly, quarterly, continuous)

**Example Input**:
```
Release: v2.0 (Analytics Dashboard)
Launch Date: March 15 (10 weeks from now)
Features: Custom dashboards, widget library, sharing, mobile view
Team: 8 engineers, 2 designers, 1 QA
Must-Have: Custom dashboards, widget library
Nice-to-Have: Mobile view
```

### 2. Break Into Sprints

**Sprint Structure** (typical 2-week sprints):
- Sprint 1-2: Foundation work
- Sprint 3-4: Core features
- Sprint 5: Polish & testing
- Sprint 6: Launch prep

**Feature Staging**:
- Which features ship together?
- What's the minimum launchable product?
- What can be phased after initial launch?

### 3. Plan Testing & Quality Gates

**Quality Gates** (must pass to proceed):
- Sprint 3: Internal dogfooding begins
- Sprint 4: Beta testing with customers
- Sprint 5: Security audit, performance testing
- Sprint 6: Go/no-go decision

### 4. Identify Critical Path

**Critical Path**: Longest dependency chain determines timeline
- What blocks what?
- What can be parallelized?
- Where are the bottlenecks?

### 5. Create Launch Checklist

**Product Readiness**:
- Features complete and tested
- Performance benchmarks met
- Security audit passed

**GTM Readiness**:
- Marketing materials ready
- Sales enablement complete
- Support documentation published

## Template

```markdown
# Release Plan: [Release Name/Version]

**Target Launch**: [Date]
**Duration**: [X] weeks ([Y] sprints)
**Team**: [Team composition]
**PM**: [Your name]
**Date Created**: [YYYY-MM-DD]

---

## Release Goals

**What we're shipping**:
[One sentence description of release]

**Why this matters**:
[Business value, user impact, strategic importance]

**Success Metrics**:
- [Metric 1]: [Target]
- [Metric 2]: [Target]
- [Metric 3]: [Target]

---

## Release Scope

### Must-Have Features (Launch Blockers)

| Feature | Description | Epic/Stories | Estimate | Owner |
|---------|-------------|--------------|----------|-------|
| [Feature 1] | [Description] | [Link] | [X] pts | [Team/Name] |
| [Feature 2] | [Description] | [Link] | [X] pts | [Team/Name] |
| [Feature 3] | [Description] | [Link] | [X] pts | [Team/Name] |

**Total Must-Haves**: [X] story points

---

### Nice-to-Have Features (Can Slip to v2.1)

| Feature | Description | Estimate | Why Nice-to-Have |
|---------|-------------|----------|------------------|
| [Feature A] | [Description] | [X] pts | [Enhances but not required] |
| [Feature B] | [Description] | [X] pts | [Can launch without] |

---

### Explicitly Out of Scope

| Feature | Why Out of Scope | When to Revisit |
|---------|------------------|-----------------|
| [Feature X] | [Reason] | [v2.1 or later] |
| [Feature Y] | [Reason] | [After validation] |

---

## Sprint Breakdown

### Sprint 1: [Dates] - Foundation

**Goals**:
- [Goal 1]
- [Goal 2]

**Features**:
- [Feature/Component 1]: [What's being built]
- [Feature/Component 2]: [What's being built]

**Deliverables**:
- [ ] [Deliverable 1]
- [ ] [Deliverable 2]

**Dependencies**: [Any external dependencies]
**Risks**: [Sprint-specific risks]

---

### Sprint 2: [Dates] - Core Feature Build

**Goals**:
- [Goal 1]
- [Goal 2]

**Features**:
- [Feature 1]: [Progress expected]
- [Feature 2]: [Progress expected]

**Deliverables**:
- [ ] [Deliverable 1]
- [ ] [Deliverable 2]

**Quality Gate**: [Milestone that must be hit]

---

[Repeat for each sprint]

---

### Sprint N (Final): [Dates] - Launch Prep

**Goals**:
- Final bug fixes
- Launch readiness
- Go/no-go decision

**Activities**:
- Bug bash
- Performance testing
- Security audit
- Launch checklist completion

**Go/No-Go Meeting**: [Date/Time]

---

## Feature Dependencies

**Dependency Map**:

```
[Feature A] (Sprint 1-2)
    ↓
[Feature B] (Sprint 3) - depends on A
    ↓
[Feature C] (Sprint 4) - depends on B
```

**Critical Path**: [Feature A] → [Feature B] → [Feature C] (4 sprints)

**Bottlenecks**:
- [Feature X]: Longest dependency chain, determines timeline
- [Team Y]: Most work allocated, capacity risk

---

## Testing & Quality Plan

### Internal Dogfooding

**Start**: Sprint [X]
**Participants**: Internal team ([Y] people)
**Focus**: Usability, major bugs, workflow validation
**Success Criteria**: [X]% of team using daily

---

### Beta Testing

**Start**: Sprint [X]
**Participants**: [Y] customers (mix of power users and new users)
**Duration**: [Z] weeks
**Focus**: Real-world usage, edge cases, feedback
**Success Criteria**:
- [X]% of beta users active weekly
- <[Y] critical bugs reported
- NPS >[Z]

---

### Performance Testing

**Timeline**: Sprint [X]
**Scenarios**:
- [Scenario 1]: [X] concurrent users, <[Y]s response time
- [Scenario 2]: [X] requests/sec sustained load

**Benchmarks**:
- Page load: <[X]s (95th percentile)
- API latency: <[Y]ms (95th percentile)
- Uptime: >[Z]%

---

### Security Audit

**Timeline**: Sprint [X]
**Scope**: [What's being audited]
**Auditor**: [Internal/External]
**Must Pass**: [Critical security requirements]

---

## Launch Readiness Checklist

### Product Readiness

**Features**:
- [ ] All must-have features complete and tested
- [ ] <[X] critical bugs, <[Y] high bugs
- [ ] Performance benchmarks met
- [ ] Security audit passed
- [ ] Internal dogfooding successful

**Technical**:
- [ ] Monitoring and alerts configured
- [ ] Rollback plan tested
- [ ] Database migrations validated
- [ ] Feature flags in place
- [ ] Load testing passed

---

### GTM Readiness

**Marketing**:
- [ ] Launch blog post written
- [ ] Product video/demo created
- [ ] Email campaign ready
- [ ] Social media scheduled
- [ ] Press outreach (if applicable)

**Sales**:
- [ ] Sales deck updated
- [ ] Competitive battlecards ready
- [ ] Demo environment set up
- [ ] Pricing/packaging finalized

**Customer Success**:
- [ ] Support documentation published
- [ ] Training materials created
- [ ] FAQ updated
- [ ] CS team trained

---

### Launch Logistics

**Communications**:
- [ ] Internal announcement ready
- [ ] Customer announcement ready
- [ ] Changelog updated
- [ ] Release notes published

**Operations**:
- [ ] Launch timeline communicated
- [ ] War room scheduled (for launch day)
- [ ] On-call rotation assigned
- [ ] Escalation path defined

---

## Go / No-Go Decision

**Go/No-Go Meeting**: [Date, Time]
**Decision Maker**: [Name/Role]
**Attendees**: [PM, Eng Lead, Design, QA, CS]

**Go Criteria** (all must be YES):
- [ ] All must-have features complete
- [ ] <[X] critical bugs
- [ ] Performance benchmarks met
- [ ] Security audit passed
- [ ] Beta feedback addressed
- [ ] Launch checklist 100% complete

**No-Go Triggers** (any = delay):
- ❌ Critical bug blocking launch
- ❌ Performance below benchmarks
- ❌ Security vulnerability unresolved
- ❌ Launch checklist <90% complete

**Delay Scenario**:
- **If No-Go**: Delay [X] weeks, address blockers
- **Next Review**: [Date]

---

## Risks to Release

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| [Risk 1] | High | High | [Strategy] | [Name] |
| [Risk 2] | Med | High | [Strategy] | [Name] |
| [Risk 3] | Med | Med | [Strategy] | [Name] |

**Contingency Plans**:
- **If [X] delayed**: [Backup plan]
- **If [Y] blocked**: [Alternative approach]

---

## Success Metrics (Post-Launch)

**Week 1**:
- [Metric 1]: [Target]
- [Metric 2]: [Target]

**Month 1**:
- [Metric 1]: [Target]
- [Metric 2]: [Target]

**Review**: [Date for post-launch review]

---

## Communication Plan

**Internal Updates**: Weekly sprint reviews
**Stakeholder Updates**: Bi-weekly release status
**Launch Announcement**: [Date, channel]
```

---

## Best Practices

### DO ✅

- **Build in buffer** - Add 1-2 week buffer for unknowns
- **Lock scope early** - Changes after Sprint 2 risky
- **Test continuously** - Don't wait until end
- **Communicate often** - Weekly updates to stakeholders
- **Define go/no-go criteria** - Objective decision framework
- **Plan for rollback** - Know how to undo if needed
- **Celebrate milestones** - Keep team motivated

### DON'T ❌

- **Add features mid-release** - Scope creep kills timelines
- **Skip testing sprints** - Quality can't be rushed
- **Ignore critical path** - Focus on longest dependency chain
- **Over-commit team** - Leaves no room for bugs/unknowns
- **Launch without checklist** - Ensures nothing forgotten
- **Forget post-launch plan** - Monitoring, support, iteration

---

## Model

Use: Sonnet

---

## Related

- `/pm:sprint-plan` - Individual sprint planning
- `/pm:roadmap` - Place release on roadmap
- `/pm:mvp` - Define MVP for release
- `/pm:risks` - Risk assessment for release
- `/workflows:product-launch` - Full product launch workflow
- `gtm-planner` agent - Go-to-market planning
- `agile-coach` agent - Agile release management
