# PRD Generator

Generate comprehensive Product Requirements Documents (PRDs) from feature ideas or problem statements.

## Usage

```
/pm:prd [feature description or problem statement] [optional: context, constraints]
```

## What This Command Does

1. Analyzes feature ideas or problems to understand core requirements
2. Generates complete, stakeholder-ready PRDs with all standard sections
3. Includes problem statement, user personas, requirements, success metrics, technical specs
4. Provides acceptance criteria, rollout plans, and risk assessments
5. Creates testable, measurable, actionable requirements
6. Takes 60 minutes vs 4-6 hours of manual PRD writing

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Feature/Problem Context**:
- What feature are we building? Or what problem are we solving?
- Why are we building this now? (urgency, opportunity)
- Who requested this? (customer demand, stakeholder initiative, team proposal)
- What's the current workaround or alternative?

**User Context**:
- Who are the target users? (personas, segments, roles)
- What are their goals and pain points?
- How many users affected? (TAM, current user base segment)
- What user research have we done? (interviews, surveys, data)

**Business Context**:
- What business goal does this support? (revenue, retention, acquisition, efficiency)
- How will we measure success? (metrics, targets, timeline)
- What's the expected impact? (revenue, NPS, churn reduction)
- What's the priority vs other work?

**Technical Context**:
- What are the technical constraints? (platform, architecture, integrations)
- What dependencies exist? (APIs, services, teams)
- What's the estimated complexity? (effort, timeline)
- What technical research is needed?

**Scope Boundaries**:
- What's explicitly in scope for v1?
- What's explicitly out of scope?
- What's the MVP vs full vision?
- What can we defer to v2/v3?

**Example Input**:
```
Feature: Dark mode for mobile app
Context: #1 feature request (500+ votes), 60% of users report eye strain at night
Users: All mobile users (100K), especially night-time users (40K)
Business Goal: Improve retention (targeting +5% improvement)
Technical: React Native, need to theme all screens + 3rd party components
Timeline: Ship in Q1 (12 weeks)
MVP: Basic dark theme, system preference detection
Out of Scope: Custom theme colors, scheduling dark mode
```

### 2. Structure the PRD

**Standard PRD Sections** (all required):

1. **TL;DR** - Executive summary (2-3 sentences)
2. **Problem Statement** - What problem are we solving?
3. **Goals & Success Metrics** - Measurable outcomes
4. **Target Users** - Personas and use cases
5. **Solution Overview** - High-level approach
6. **Detailed Requirements** - Functional & non-functional
7. **User Experience** - Flows, wireframes, states
8. **Technical Specifications** - Architecture, integrations, data model
9. **Rollout Plan** - Launch strategy and phasing
10. **Risks & Mitigations** - What could go wrong
11. **Open Questions** - Unknowns to resolve
12. **Alternatives Considered** - Why we chose this approach

### 3. Write Requirements

**Requirement Quality Criteria**:
- **Specific**: Clear, unambiguous, no interpretation needed
- **Measurable**: Testable with objective criteria
- **Actionable**: Engineering can build from it
- **Relevant**: Tied to user or business goal
- **Time-bound**: Clear priority and timeline

**Acceptance Criteria Format** (Given-When-Then):
```
Given [context/precondition]
When [action/trigger]
Then [expected outcome]
```

### 4. Define Success Metrics

**Types of Metrics**:
- **Adoption**: % of users who enable/use feature
- **Engagement**: Frequency, duration, depth of use
- **Business**: Revenue, conversion, retention impact
- **Quality**: Bug rate, performance, satisfaction

**Set Targets**:
- Baseline: Current state
- Target: Goal for success
- Timeline: When to measure

## Template

```markdown
# PRD: [Feature Name]

**Author**: [Your Name, Role]
**Date**: [YYYY-MM-DD]
**Status**: [Draft | In Review | Approved | Archived]
**Reviewers**: [Names and roles of required approvers]
**Related Docs**: [Links to research, designs, specs]

---

## TL;DR

[2-3 sentence executive summary covering:
- What we're building
- Why (problem it solves)
- Expected impact (key success metric)]

**Example**:
*We're adding dark mode to our mobile app to reduce eye strain and meet user expectations for modern apps. This addresses our #1 feature request (500+ votes) and is expected to improve retention by 5% among night-time users (40K users).*

---

## Problem Statement

**What Problem Are We Solving?**

[Clear, concise description of the user problem or business opportunity]

**Evidence**:
- [Data point 1 - quantitative evidence, e.g., "500+ feature requests"]
- [Data point 2 - qualitative evidence, e.g., "User interviews showed..."]
- [Data point 3 - competitive context, e.g., "80% of competitors offer this"]

**Current Experience** (What happens today):
[Description of current state and workarounds users employ]

**Desired Experience** (What we want):
[Description of ideal state after feature is built]

**Why Now?**
[Urgency or opportunity that makes this a priority]

---

## Goals & Success Metrics

**Business Goals**:
1. [Goal 1 - e.g., "Improve user retention"]
2. [Goal 2 - e.g., "Reduce support tickets about eye strain"]
3. [Goal 3 - e.g., "Maintain parity with competitors"]

**Success Metrics**:

| Metric | Baseline | Target | Timeframe | How to Measure |
|--------|----------|--------|-----------|----------------|
| [Metric 1] | [Current value] | [Goal value] | [When to measure] | [Data source] |
| [Metric 2] | [Current] | [Goal] | [When] | [Source] |
| [Metric 3] | [Current] | [Goal] | [When] | [Source] |

**Example**:
| Metric | Baseline | Target | Timeframe | How to Measure |
|--------|----------|--------|-----------|----------------|
| Dark mode adoption | 0% | 40% | 30 days post-launch | Analytics event |
| Night session duration | 8 min | 9.2 min (+15%) | 60 days post-launch | Session analytics |
| Eye strain complaints | 15/week | <5/week | 30 days post-launch | Support tickets |

**Success Criteria**:
- ✅ **Launch Success**: [Minimum bar for calling launch successful]
- 🎯 **Target Success**: [Aspirational goal]
- ❌ **Failure Signal**: [Red flag that indicates we should pause/pivot]

---

## Target Users

**Primary Persona(s)**:

### Persona 1: [Name and Role]

**Demographics**:
- [Role/job title]
- [Company size/industry if B2B]
- [Usage frequency]

**Goals**:
- [What they're trying to accomplish]
- [What success looks like for them]

**Pain Points**:
- [Current frustration 1]
- [Current frustration 2]

**How This Feature Helps**:
[What this persona can now do that they couldn't before]

---

### Persona 2: [Name and Role]

[Repeat persona template if multiple target users]

---

**User Segments**:

| Segment | Size | Priority | Key Need |
|---------|------|----------|----------|
| [Segment 1] | [X users / % of base] | P0 (Must have) | [Need] |
| [Segment 2] | [X users / % of base] | P1 (Important) | [Need] |
| [Segment 3] | [X users / % of base] | P2 (Nice to have) | [Need] |

---

## Use Cases

### Use Case 1: [Title]

**Actor**: [Who is doing this]

**Precondition**: [What must be true before this use case]

**Trigger**: [What initiates this flow]

**Main Flow**:
1. User [action 1]
2. System [response 1]
3. User [action 2]
4. System [response 2]
5. [Continue...]

**Postcondition**: [System state after completion]

**Alternative Flows**:
- **3a.** If [condition], then [alternative path]
- **4a.** If [error condition], then [error handling]

---

[Repeat for 2-4 key use cases]

---

## Solution Overview

**High-Level Approach**:
[1-2 paragraphs describing the solution approach at a conceptual level]

**Key Features** (In Scope for V1):
1. **[Feature 1 Name]**: [One sentence description]
2. **[Feature 2 Name]**: [One sentence description]
3. **[Feature 3 Name]**: [One sentence description]

**Out of Scope** (V1):
- [Feature or capability we're explicitly not building in v1]
- [Reason it's deferred - complexity, unclear value, can be added later]

**Future Versions** (V2/V3 Roadmap):
- **V2**: [What comes next after successful v1]
- **V3**: [Long-term vision]

---

## Detailed Requirements

### Functional Requirements

**FR1: [Requirement Title]**

**Description**:
[Detailed description of what the system must do]

**User Story**:
*As a [user type], I want to [action] so that [benefit].*

**Acceptance Criteria**:
```
Given [precondition]
When [action]
Then [expected result]

And [additional condition]
Then [additional result]
```

**Priority**: [P0 Must Have | P1 Should Have | P2 Nice to Have]

**Dependencies**: [Other requirements, features, or systems this depends on]

**Notes**: [Additional context, design considerations, edge cases]

---

**FR2: [Requirement Title]**

[Repeat functional requirement template for each requirement]

---

### Non-Functional Requirements

**NFR1: Performance**

| Metric | Requirement | How to Measure |
|--------|-------------|----------------|
| Page load time | <[X]ms (p95) | Lighthouse, RUM |
| API response time | <[Y]ms (p95) | APM |
| Time to interactive | <[Z]s | Web vitals |

---

**NFR2: Security**

- [Security requirement 1 - e.g., "All user data encrypted at rest"]
- [Security requirement 2 - e.g., "OAuth 2.0 for authentication"]
- [Security requirement 3 - e.g., "Pass security audit before launch"]

**Acceptance Criteria**:
- [ ] Security review completed
- [ ] Penetration test passed
- [ ] No critical/high vulnerabilities

---

**NFR3: Accessibility**

**Standard**: WCAG 2.1 Level AA compliance

**Requirements**:
- Keyboard navigation for all features
- Screen reader compatibility
- Minimum contrast ratios (4.5:1 for text)
- Focus indicators visible
- Alternative text for images

**Acceptance Criteria**:
- [ ] Passes axe DevTools audit (0 violations)
- [ ] Manual screen reader testing complete
- [ ] Keyboard-only testing complete

---

**NFR4: Scalability**

- Support [X] concurrent users (peak load)
- Handle [Y] requests per second
- Database can scale to [Z] records

---

**NFR5: Reliability**

- 99.9% uptime SLA
- Graceful degradation if dependencies fail
- Error recovery and retry logic

---

## User Experience

### User Flows

**Flow 1: [Primary Flow Name]**

[Diagram or step-by-step description]

```
Entry Point → Step 1 → Step 2 → Step 3 → Success State
                ↓
              Error State (if applicable)
```

**Screens Involved**:
1. [Screen name and purpose]
2. [Screen name and purpose]

---

### UI States

**State 1: Default/Empty State**
- [What user sees when feature is unused/empty]
- [CTA or guidance to get started]

**State 2: Loading State**
- [What user sees while data loads]
- [Skeleton screens, spinners, progressive loading]

**State 3: Success State**
- [What user sees when action succeeds]
- [Confirmation message, updated UI]

**State 4: Error State**
- [What user sees when something fails]
- [Error message, recovery actions]

---

### Wireframes / Mockups

**Design Files**: [Link to Figma, Sketch, etc.]

**Key Screens**:
- [Screen 1]: [Purpose and key interactions]
- [Screen 2]: [Purpose and key interactions]

**Design Notes**:
- [Design principle or constraint]
- [Accessibility consideration]
- [Responsive behavior]

---

## Technical Specifications

### Architecture Overview

**Components**:
- **Frontend**: [Technology, responsibilities]
- **Backend**: [Services, APIs]
- **Database**: [Data storage approach]
- **Integrations**: [Third-party services]

**Diagram**: [Link to architecture diagram or ASCII diagram]

```
User → Frontend → API Gateway → Service A → Database
                         ↓
                    Service B → External API
```

---

### Data Model

**New Tables/Collections**:

**Table: [name]**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| id | UUID | Yes | Primary key |
| user_id | UUID | Yes | Foreign key to users |
| [field] | [type] | [Y/N] | [Purpose] |
| created_at | Timestamp | Yes | Record creation |

**Indexes**: [Which fields need indexing for performance]

**Migrations**: [How to handle existing data]

---

### API Specifications

**Endpoint: POST /api/[resource]**

**Request**:
```json
{
  "field1": "value",
  "field2": 123
}
```

**Response** (200 OK):
```json
{
  "id": "uuid",
  "field1": "value",
  "created_at": "2025-01-15T10:30:00Z"
}
```

**Errors**:
- 400: Invalid input
- 401: Unauthorized
- 500: Server error

---

### Third-Party Integrations

| Service | Purpose | API Docs | Rate Limits |
|---------|---------|----------|-------------|
| [Service 1] | [Why we use it] | [Link] | [Limits] |
| [Service 2] | [Why we use it] | [Link] | [Limits] |

---

### Security Considerations

- [Authentication approach]
- [Authorization model]
- [Data encryption]
- [Input validation]
- [Rate limiting]

---

## Dependencies & Constraints

### Dependencies

**Internal Dependencies**:
- [Team or feature we depend on]
- [What we need from them and by when]

**External Dependencies**:
- [Third-party service or API]
- [What we need and contingency if unavailable]

**Blocking Dependencies**:
- [Critical dependency that blocks development]
- [Timeline and mitigation plan]

---

### Constraints

**Technical Constraints**:
- [Platform limitation - e.g., "React Native 0.72+ required"]
- [Performance constraint - e.g., "Must work offline"]

**Business Constraints**:
- [Budget limitation]
- [Timeline deadline - e.g., "Must launch before Q2"]

**Legal/Compliance Constraints**:
- [Regulatory requirement - e.g., "GDPR compliance required"]
- [Legal review needed]

---

## Rollout Plan

### Launch Strategy

**Launch Type**: [Big Bang | Phased Rollout | Beta Test | Dark Launch]

**Phases**:

**Phase 1: Internal Beta**
- **Audience**: Internal team (50 users)
- **Timeline**: Week 1-2
- **Goal**: Catch critical bugs, validate core functionality
- **Success Criteria**: <5 critical bugs, positive team feedback

**Phase 2: Limited Beta**
- **Audience**: Beta testers (500 users, opted-in)
- **Timeline**: Week 3-4
- **Goal**: Validate at scale, gather user feedback
- **Success Criteria**: >80% CSAT, <10 critical bugs

**Phase 3: Gradual Rollout**
- **Audience**: 10% → 25% → 50% → 100% of users
- **Timeline**: Week 5-8 (1 week per phase)
- **Goal**: Safe, monitored expansion
- **Success Criteria**: No regression in core metrics

---

### Launch Checklist

**Product**:
- [ ] All P0 requirements implemented and tested
- [ ] Acceptance criteria met for all features
- [ ] User documentation/help content published
- [ ] In-app onboarding/tooltips ready

**Engineering**:
- [ ] Code reviewed and merged
- [ ] Unit tests passing (>80% coverage)
- [ ] Integration tests passing
- [ ] Performance benchmarks met
- [ ] Security audit passed
- [ ] Staging environment validated

**Design**:
- [ ] Final designs approved
- [ ] Accessibility review complete
- [ ] Responsive design tested (mobile, tablet, desktop)
- [ ] Design QA passed

**Go-to-Market**:
- [ ] Launch blog post drafted
- [ ] Email announcement ready
- [ ] In-app announcement/banner ready
- [ ] Sales/CS teams trained
- [ ] Support documentation updated

**Analytics**:
- [ ] Event tracking implemented
- [ ] Dashboards created
- [ ] Alerts configured for key metrics
- [ ] Baseline metrics captured

**Launch Approval**:
- [ ] PM sign-off
- [ ] Engineering lead sign-off
- [ ] Design sign-off
- [ ] Stakeholder approval

---

### Go/No-Go Criteria

**Go Criteria** (All must be true):
- [ ] All P0 requirements complete
- [ ] <[X] critical bugs outstanding
- [ ] Performance targets met
- [ ] Security review passed
- [ ] Launch checklist 100% complete

**No-Go Triggers** (Any = delay launch):
- ❌ Critical bug discovered
- ❌ Security vulnerability unresolved
- ❌ Performance below target
- ❌ Stakeholder approval not obtained

**Rollback Plan**:
- Feature flag to disable feature
- Database rollback procedure (if needed)
- Communication plan if rollback needed

---

## Risks & Mitigations

| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| [Risk 1] | H/M/L | H/M/L | [How we reduce/handle] | [Name] |
| [Risk 2] | H/M/L | H/M/L | [Mitigation plan] | [Name] |

**Example**:
| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|
| Third-party theme library breaks dark mode | Medium | High | Test all components, build fallback CSS | Eng Lead |
| Adoption below target (20% vs 40%) | Low | Medium | In-app promotion, email campaign, default to dark at night | PM |
| Timeline slips 2+ weeks | Medium | Medium | Cut scope (defer advanced theme customization to v2) | PM |

---

## Open Questions

**Technical Questions**:
- [ ] Q1: [Open technical question to resolve before build]
  - **Owner**: [Who will answer]
  - **Deadline**: [When we need answer]

**Design Questions**:
- [ ] Q2: [Open UX question]
  - **Owner**: [Who decides]
  - **Deadline**: [When]

**Business Questions**:
- [ ] Q3: [Open business/strategy question]
  - **Owner**: [Who decides]
  - **Deadline**: [When]

---

## Alternatives Considered

### Alternative 1: [Approach Name]

**Description**: [What this alternative was]

**Pros**:
- [Advantage 1]
- [Advantage 2]

**Cons**:
- [Disadvantage 1]
- [Disadvantage 2]

**Why Not Chosen**: [Reason we went with primary approach instead]

---

### Alternative 2: [Approach Name]

[Repeat for each alternative considered]

---

### Alternative 3: Do Nothing

**What Happens**: [Impact of not building this feature]

**Why Build**: [Reason we're investing in this over doing nothing]

---

## Success Measurement Plan

**Pre-Launch**:
- Capture baseline metrics
- Set up dashboards and alerts
- Define monitoring approach

**Week 1 Post-Launch**:
- Monitor: Adoption rate, errors, performance
- Target: [X]% adoption, <[Y] critical bugs
- Action: Fix critical issues immediately

**Week 4 Post-Launch**:
- Monitor: Engagement, satisfaction, business metrics
- Target: [Success metric targets from Goals section]
- Action: Iterate based on feedback

**3 Months Post-Launch**:
- Review: Full analysis of success metrics
- Decision: Expand, iterate, or sunset
- Next Steps: Plan v2 enhancements if successful

---

## Appendix

**Research Links**:
- [User research document]
- [Competitive analysis]
- [Market data]

**Design Links**:
- [Figma files]
- [User flow diagrams]
- [Prototype]

**Technical Links**:
- [Architecture diagrams]
- [Technical spike results]
- [API documentation]

**Related PRDs**:
- [Related feature 1]
- [Related feature 2]

```

---

## Best Practices

### DO ✅

- **Start with problem, not solution** - Validate the "why" before the "what"
- **Use data and evidence** - Quantify the problem and expected impact
- **Write testable requirements** - Every requirement should have clear pass/fail criteria
- **Define success metrics upfront** - Know how you'll measure success before building
- **Involve stakeholders early** - Get input from eng, design, sales, CS before finalizing
- **Keep it updated** - PRD is living document, update as decisions are made
- **Be specific about scope** - Clear "in scope" and "out of scope" prevents scope creep
- **Plan for rollout** - Think through launch strategy, not just feature build

### DON'T ❌

- **Don't write the solution first** - Start with problem statement and user needs
- **Don't assume you know the requirements** - Talk to users, validate assumptions
- **Don't make it too long** - Comprehensive doesn't mean verbose; be concise
- **Don't use vague language** - "Fast", "easy", "good" are not measurable
- **Don't skip non-functional requirements** - Performance, security, accessibility matter
- **Don't forget edge cases** - Error states, empty states, loading states
- **Don't set impossible metrics** - Targets should be ambitious but achievable
- **Don't write alone** - PRD is collaborative, get input from cross-functional team

---

## Examples

### Example 1: Dark Mode Feature

**Input**: "We need dark mode for our app"

**Output** (excerpt):

```markdown
# PRD: Dark Mode

**TL;DR**: We're adding dark mode to reduce eye strain and meet modern app expectations. This addresses our #1 feature request (500+ votes) and is expected to improve retention by 5% among night-time users.

## Problem Statement

**What**: Users experience eye strain when using our app in low-light conditions (evening, nighttime). 60% of our users report using the app after 8pm.

**Evidence**:
- 500+ feature requests (UserVoice #1 request)
- 23% of support tickets mention "bright screen" or "eye strain"
- User interviews: 8/10 users use workarounds (screen dimming, switching to competitor)

**Why Now**: 80% of top 20 competitors launched dark mode in last 12 months. Risk losing users to competitors.

## Goals & Success Metrics

| Metric | Baseline | Target | Timeframe |
|--------|----------|--------|-----------|
| Dark mode adoption | 0% | 40% | 30 days post-launch |
| Night session duration | 8min | 9.2min (+15%) | 60 days |
| Eye strain complaints | 15/week | <5/week | 30 days |

## Detailed Requirements

**FR1: Dark Mode Toggle**

*As a user, I want to toggle between light and dark mode so that I can use the app comfortably in any lighting condition.*

**Acceptance Criteria**:
```
Given I am on any screen with the mode toggle
When I tap the toggle
Then the app immediately switches to dark/light mode
And my preference is saved for future sessions
```

**FR2: System Preference Detection**

*As a user, I want the app to respect my OS dark mode setting so that it matches my device theme automatically.*

**Acceptance Criteria**:
```
Given I have dark mode enabled in iOS/Android settings
When I open the app for the first time
Then the app defaults to dark mode
And I can override this with in-app toggle
```

## Rollout Plan

**Phase 1**: Internal beta (50 employees, Week 1-2)
**Phase 2**: Limited beta (500 opted-in users, Week 3-4)
**Phase 3**: Gradual rollout (10% → 25% → 50% → 100%, Week 5-8)

## Risks

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| 3rd party widgets break | Medium | High | Audit all widgets, build custom themes for critical ones |
| Adoption <20% | Low | Medium | In-app promotion, default to dark 8pm-6am |
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:user-stories` - Convert PRD requirements into user stories
- `/pm:mvp` - Scope MVP for v1 of PRD
- `/pm:impact` - Estimate impact of PRD features
- `/pm:risks` - Detailed risk assessment for PRD
- `/pm:align` - Get stakeholder alignment on PRD
- `/workflows:feature-lifecycle` - End-to-end feature development from PRD to launch
- `requirements-engineer` agent - Detailed requirements writing and refinement
- `technical-pm` agent - Technical specifications and architecture
