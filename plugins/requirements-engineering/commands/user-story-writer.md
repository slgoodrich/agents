# User Story Writer

Convert requirements, features, or PRDs into well-formed user stories with acceptance criteria.

## Usage

```
/requirements-engineering:user-stories [feature or requirements description] [optional: context, personas]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Breaks down features or requirements into atomic, deliverable user stories
2. Writes stories in proper "As a... I want... So that..." format
3. Generates Given-When-Then acceptance criteria for each story
4. Provides INVEST-compliant stories (Independent, Negotiable, Valuable, Estimable, Small, Testable)
5. Suggests story sizing, priority, and dependencies
6. Takes 30 minutes vs 2 hours of manual story writing

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Feature Context**:
- What feature or capability are we breaking down?
- What's the source? (PRD, feature request, requirements doc)
- What problem does this solve for users?
- What's the business goal?

**User Context**:
- Who are the target users? (personas, roles)
- What are their goals and workflows?
- What's their technical sophistication?
- Are there multiple user types with different needs?

**Scope Context**:
- What's in scope for this set of stories?
- What's explicitly out of scope?
- What's the MVP vs future enhancements?
- Any technical constraints or dependencies?

**Development Context**:
- What's the team's velocity/capacity?
- What story point scale do you use? (Fibonacci, t-shirt sizes)
- Are there existing stories these build on?
- Any sprint/timeline constraints?

**Example Input**:
```
Feature: Search filtering (from PRD)
Users: All platform users (100K), especially power users who search frequently
Goal: Help users find relevant content faster
Scope: Date range and category filters only (v1), location/tags deferred to v2
Context: Current search has no filtering, users complain content is hard to find
Team: Fibonacci point scale, 32 point velocity, 2-week sprints
```

### 2. Break Down Into Stories

**Decomposition Principles**:
- **User-Centric**: Each story delivers value to a user
- **Atomic**: Story is smallest shippable unit
- **Testable**: Can be demoed and validated
- **Independent**: Minimal dependencies on other stories

**Story Granularity**:
- Too big: "Build entire checkout flow" (should be epic with multiple stories)
- Too small: "Add button" (should be part of larger story)
- Just right: "Allow user to apply discount code during checkout"

### 3. Write User Stories

**User Story Format**:
```
As a [persona/user type]
I want to [action/capability]
So that [outcome/benefit]
```

**Components**:
- **As a**: Who is this for? Use specific persona or role
- **I want**: What does the user want to do? Be specific
- **So that**: Why does the user want this? What's the benefit?

### 4. Create Acceptance Criteria

**Given-When-Then Format**:
```
Scenario: [Descriptive scenario name]
  Given [precondition/context]
  And [additional context if needed]
  When [action or trigger]
  Then [expected result]
  And [additional expected result]
```

**Coverage**:
- Happy path (primary use case)
- Edge cases (boundary conditions)
- Error scenarios (validation, failures)
- Non-functional requirements (performance, security, accessibility)

### 5. Size and Prioritize Stories

**Story Points** (Fibonacci: 1, 2, 3, 5, 8, 13):
- 1 pt: Trivial change, < 1 day
- 2 pts: Simple story, 1-2 days
- 3 pts: Moderate complexity, 2-3 days
- 5 pts: Complex story, 3-5 days
- 8 pts: Very complex, consider breaking down
- 13+ pts: Epic, must break down

**Priority**:
- P0: Must have (MVP blocker)
- P1: Should have (important, not blocker)
- P2: Nice to have (defer if needed)

## Template

```markdown
# User Stories: [Feature Name]

**Source**: [PRD/Request] | **Epic**: [Parent epic] | **Target**: [Sprint/Backlog]

## Epic Overview
**Goal**: [Business and user value]
**Personas**: [Who needs this]
**Estimated Size**: [X] points ([Y] sprints)

---

## Story 1: [Descriptive Title]

**Story**:
As a [specific persona]
I want to [specific action]
So that [clear benefit/outcome]

**Context**: [1-2 sentences: why valuable, what problem solved]

**Acceptance Criteria**:
```gherkin
Scenario: [Happy path]
  Given [context]
  When [action]
  Then [result]

Scenario: [Edge case]
  Given [different context]
  When [action]
  Then [outcome]

Scenario: [Error case]
  Given [context]
  When [invalid action]
  Then [error shown]
  And [user can recover]
```

**Non-Functional**:
- Performance: [e.g., "<500ms response"]
- Accessibility: [e.g., "Keyboard navigable"]
- Security: [If applicable]

**Definition of Done**:
- [ ] Code implemented & reviewed
- [ ] Unit tests passing
- [ ] ACs validated in staging
- [ ] Accessibility reviewed
- [ ] Documentation updated

**Priority**: P0 (Must) | P1 (Should) | P2 (Nice)
**Size**: [X] points
**Sizing Rationale**: [Why this estimate - complexity factors]
**Dependencies**: [What must be complete first]

**Technical Notes**: [Implementation considerations, libs, DB changes]
**Design Notes**: [Mockup link, UI/UX considerations, states]
**Testing Notes**: [Key scenarios, edge cases, performance benchmarks]

---

[Repeat for additional stories]

---

## Story Dependencies

```
Story 1 (Foundation)
  ↓
Story 2 (Builds on 1)
  ↓
Story 3

Story 4 (Independent, parallel)
Story 5 (Independent, parallel)
```

**Sprint Plan**: Sprint 1: [Stories 1,4,5], Sprint 2: [Stories 2,3]

---

## Out of Scope (Future)
- [Enhancement 1]: Deferred because [reason], revisit [when]
- [Enhancement 2]: Deferred because [reason], revisit [when]
```


## Story Sizing (Fibonacci)

| Points | Complexity | Duration |
|--------|-----------|----------|
| 1 | Trivial | <1 day |
| 2 | Simple | 1-2 days |
| 3 | Moderate | 2-3 days |
| 5 | Complex | 3-5 days |
| 8 | Very complex | Break down |
| 13+ | Epic | Must break down |

## INVEST Criteria

✅ **Independent**: Can be developed independently
✅ **Negotiable**: Details can be refined
✅ **Valuable**: Delivers value to user/business
✅ **Estimable**: Team can estimate effort
✅ **Small**: Fits in one sprint
✅ **Testable**: Clear success criteria, demo-able

## Best Practices

✅ **DO**: Write from user perspective, keep small (<8pts), make valuable, include "why" (so that...), use specific personas, write testable ACs, cover edge cases, include non-functional requirements

❌ **DON'T**: Write technical tasks ("refactor DB" isn't user story), skip ACs, make stories dependent, use vague language ("fast", "easy"), forget persona, skip benefit, write novels, estimate >13pts

**Related**: `/requirements-engineering:prd`, `/continuous-discovery:mvp`, `/agile-coaching:sprint-plan`, `/agile-coaching:backlog-groom`, `/requirements-engineering:feature-lifecycle`
