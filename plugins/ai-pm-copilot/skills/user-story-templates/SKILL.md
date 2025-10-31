---
name: user-story-templates
description: Master user story templates including As-a/I-want/So-that format, acceptance criteria (Given-When-Then), story splitting, and INVEST criteria. Use when writing user stories, defining acceptance criteria, splitting stories, refining backlogs, or communicating requirements to development teams. Covers user story best practices, story templates, and agile requirements techniques.
---

# User Story Templates

Comprehensive templates and frameworks for writing effective user stories with clear acceptance criteria, enabling agile development teams to deliver value incrementally.

## What is a User Story?

A user story is a concise description of a feature from the end-user's perspective. It follows the format: "As a [user], I want [goal], so that [benefit]."

**Purpose**:
- Communicate requirements from user perspective
- Enable incremental delivery
- Facilitate conversation and collaboration
- Support estimation and planning
- Guide testing and acceptance

## When to Use This Skill

**Auto-loaded by agents**:
- `requirements-engineer` - For user story formats, epic breakdown, and spike stories

**Use when you need**:
- Breaking down features into user stories
- Writing acceptance criteria
- Planning sprints and iterations
- Communicating requirements to development teams
- Refining product backlogs
- Splitting large stories
- Validating story quality with INVEST criteria
- Estimating and prioritizing work

---

## User Story Format

### Basic Template

```
As a [user type/persona]
I want to [action/goal]
So that [benefit/value]
```

**Example**:
```
As a small business owner
I want to export my invoices as PDF
So that I can send professional-looking invoices to clients
```

### Three Key Components

**1. User Type/Persona** (Who)
- Specific user segment or role
- Good: "free trial user", "team administrator", "mobile app user"
- Bad: "user" (too vague), "the system" (not a user)

**2. Action/Goal** (What)
- What the user wants to accomplish
- Good: "filter search results by date range", "receive email notifications"
- Bad: "have a button" (describes UI), "use the API" (describes implementation)

**3. Benefit/Value** (Why)
- Why the user wants this, what value it provides
- Good: "so that I can quickly find relevant information"
- Bad: "so that it works" (not a benefit), omitting "so that" entirely

For detailed guidance on each component, see `assets/basic-user-story-template.md`.

---

## Ready-to-Use Templates

We provide copy-paste-ready templates for common story types:

### Feature Stories
**Use for**: New features, enhancements, user-facing work
**Template**: `assets/feature-story-template.md`

Includes:
- Full user story format
- Acceptance criteria checklist
- Definition of Done
- Story points and priority
- Dependencies tracking

---

### Bug Fix Stories
**Use for**: Defects, regressions, user-reported issues
**Template**: `assets/bug-fix-story-template.md`

Includes:
- Current vs expected behavior
- Steps to reproduce
- Environment details
- Severity levels
- Impact assessment

---

### Technical Debt Stories
**Use for**: Refactoring, code improvements, infrastructure work
**Template**: `assets/technical-debt-story-template.md`

Includes:
- Technical context
- Proposed solution
- Impact on performance/maintainability/scalability
- Risk assessment
- Business value justification

---

### Spike/Research Stories
**Use for**: Time-boxed investigation, POCs, research tasks
**Template**: `assets/spike-research-story-template.md`

Includes:
- Research questions
- Time box
- Deliverables
- Acceptance criteria for knowledge gained
- Next steps identification

---

### Epic Breakdown
**Use for**: Breaking large initiatives into manageable stories
**Template**: `assets/epic-breakdown-template.md`

Includes:
- Epic goal and value proposition
- Story sequencing
- Definition of Done (epic level)
- Timeline and dependencies
- Risk mitigation

---

## Acceptance Criteria

Acceptance criteria define when a story is "done." Use one of three formats:

### 1. GIVEN-WHEN-THEN (BDD Style)

Best for: Complex workflows, state-dependent behavior, testing focus

```
GIVEN [precondition/context]
WHEN [action/event]
THEN [expected outcome]
```

**Example**:
```
GIVEN I'm on the login page
WHEN I enter valid email and password
THEN I'm redirected to my dashboard
```

### 2. Checklist Format

Best for: Simple features, quick validation, straightforward requirements

```
Acceptance Criteria:
- [ ] [Observable outcome 1]
- [ ] [Observable outcome 2]
- [ ] [Observable outcome 3]
```

**Example**:
```
- [ ] Export button appears on data table
- [ ] Clicking export generates CSV file
- [ ] CSV includes all visible columns
- [ ] CSV filename includes current date
- [ ] Export completes within 5 seconds for up to 10K rows
```

### 3. Rule-Based Format (MoSCoW)

Best for: Variable scope, prioritization needed, time-constrained sprints

```
Must: [Critical requirements]
Should: [Important but not critical]
May: [Nice to have]
```

**Comprehensive guide**: See `references/acceptance-criteria-guide.md` for deep dive on writing testable, specific criteria including error states, edge cases, and performance requirements.

---

## Story Splitting

Large stories (>5 days or >8 points) should be split into smaller, deliverable pieces.

### Common Splitting Patterns

**1. Workflow Steps**: Sequential process steps (e.g., checkout: cart → shipping → payment → confirmation)

**2. CRUD Operations**: Create → Read → Update → Delete

**3. User Roles**: Admin → Manager → Employee → Guest

**4. Business Rules**: Different variations of logic (e.g., discount types: percentage, fixed amount, BOGO)

**5. Simple to Complex**: MVP → Advanced features (progressive enhancement)

**6. Happy Path vs Edge Cases**: Success scenarios → Error handling

**7. Data Variations**: Different formats, sizes, types

**8. Platform/Device**: Desktop → Tablet → Mobile

**9. Performance Tiers**: 1-5 users → 6-20 users → 21-100 users

**10. Interface vs API**: Backend → Frontend → Integration

**Best practice**: Use vertical slicing (complete feature through all layers) vs horizontal slicing (one layer across many features).

**Comprehensive guide**: See `references/story-splitting-guide.md` for detailed examples, anti-patterns, and decision trees.

---

## INVEST Criteria

Good user stories follow the INVEST principles:

**I - Independent**: Can be developed without dependency on other stories
**N - Negotiable**: Details flexible, focuses on outcome not implementation
**V - Valuable**: Delivers clear value to user or business
**E - Estimable**: Team can estimate effort with reasonable confidence
**S - Small**: Fits in one sprint (1-5 days)
**T - Testable**: Clear acceptance criteria that can be verified

### Quick INVEST Check

- [ ] **Independent**: Can this be built without waiting for other stories?
- [ ] **Negotiable**: Does it define outcome, not implementation?
- [ ] **Valuable**: Is the benefit clear and meaningful?
- [ ] **Estimable**: Can the team estimate this confidently?
- [ ] **Small**: Can it be completed in 1-5 days?
- [ ] **Testable**: Are acceptance criteria clear and verifiable?

If a story fails any INVEST criterion, it should be rewritten or split.

**Comprehensive guide**: See `references/invest-criteria-guide.md` for deep dive on each principle with examples, anti-patterns, and fixing strategies.

---

## User Story Best Practices

### Writing Clear Stories

**DO**:
- Focus on user value, not implementation
- Keep stories independent and testable
- Write from user's perspective
- Include clear acceptance criteria
- Size stories for 1-3 days of work

**DON'T**:
- Prescribe implementation ("use React hooks")
- Mix multiple features in one story
- Write from system's perspective
- Skip acceptance criteria
- Create epics disguised as stories

### Good Example

```
As a free trial user
I want to see how many days remain in my trial
So that I can decide when to upgrade

Acceptance Criteria:
- [ ] Days remaining appears in header
- [ ] Warning shows when <7 days remain
- [ ] "Upgrade" CTA appears with countdown
- [ ] Counter updates daily at midnight
```

### Bad Example

```
As the system
I want to implement a counter using React hooks
So that the trial days feature works

[No acceptance criteria]
```

---

## Acceptance Criteria Best Practices

**DO**:
- Make criteria testable and observable
- Include happy path AND error states
- Specify performance requirements
- Cover edge cases
- Use numbers for specificity

**Good Example**:
```
- [ ] Search completes within 2 seconds for datasets <10K records
- [ ] Loading spinner shows while search is processing
- [ ] Error message appears if search fails
- [ ] No results message shows when query returns 0 items
- [ ] Search results highlight matching keywords
```

**Bad Example**:
```
- Search feature works
- UI looks good
- Performance is acceptable
```

---

## Story Point Estimation

### Modified Fibonacci Scale

- **1 point**: Trivial change (1-2 hours)
- **2 points**: Small change (half day)
- **3 points**: Medium change (1 day)
- **5 points**: Larger change (2-3 days)
- **8 points**: Large change (3-5 days) - consider splitting
- **13 points**: Epic, must be split

### Estimation Guidelines

- Points represent complexity, not time
- Compare to reference stories ("this is like that export feature we built")
- Include testing and documentation in estimate
- Account for unknowns
- Split stories >8 points

---

## Common Mistakes to Avoid

**Too technical**:
- Bad: "Implement REST API endpoint"
- Good: "Retrieve my order history via mobile app"

**Too large**:
- Bad: "Build entire checkout system"
- Good: "Enter shipping address during checkout"

**Implementation-focused**:
- Bad: "Add a button to the navbar"
- Good: "Access my account settings quickly"

**Missing acceptance criteria**:
- Bad: Only the story statement
- Good: Story + clear, testable acceptance criteria

**Vague**:
- Bad: "Make the app faster"
- Good: "Load dashboard in under 2 seconds"

---

## Related Skills

- `prd-templates` - Product requirements documentation that feeds into user stories
- `specification-techniques` - General specification writing best practices
- `prioritization-methods` - Prioritizing stories for sprint planning

---

## Templates and References

### Assets (Ready-to-Use Templates)

Copy-paste these for immediate use:
- `assets/basic-user-story-template.md` - Simple story format with guidance
- `assets/feature-story-template.md` - Full-featured story with DoD
- `assets/bug-fix-story-template.md` - Bug tracking and resolution
- `assets/technical-debt-story-template.md` - Technical improvements
- `assets/spike-research-story-template.md` - Time-boxed research
- `assets/epic-breakdown-template.md` - Epic to stories breakdown

### References (Deep Dives)

When you need comprehensive guidance:
- `references/story-splitting-guide.md` - 10 splitting patterns with examples, anti-patterns, decision trees
- `references/acceptance-criteria-guide.md` - Writing testable criteria, all three formats, common mistakes
- `references/invest-criteria-guide.md` - Deep dive on each INVEST principle with examples and fixes

---

## Quick Start

**For new features**:
1. Start with `assets/feature-story-template.md`
2. Fill in user type, goal, and benefit
3. Add acceptance criteria (use `references/acceptance-criteria-guide.md` if needed)
4. Verify INVEST criteria
5. Estimate story points
6. If >8 points, split using patterns from `references/story-splitting-guide.md`

**For bugs**:
1. Use `assets/bug-fix-story-template.md`
2. Document current vs expected behavior
3. Add reproduction steps
4. Include severity and impact
5. Write fix verification criteria

**For research**:
1. Use `assets/spike-research-story-template.md`
2. Define research questions
3. Set time box (critical!)
4. Specify deliverable
5. Include next steps in acceptance criteria

---

**Key Principle**: Great user stories are conversations, not contracts. They enable collaboration while providing enough structure to guide development, testing, and acceptance.
