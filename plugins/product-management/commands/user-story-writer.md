# User Story Writer

Convert requirements or features into well-formed user stories with acceptance criteria.

## Usage

```
/pm:user-stories [feature or requirements description]
```

## What This Command Does

1. Takes a feature, PRD, or requirements document
2. Breaks it down into user stories following best practices
3. Generates acceptance criteria in Given-When-Then format
4. Provides story sizing and prioritization guidance
5. Creates a backlog-ready output

## Instructions

When provided with a feature or requirements:

1. **Analyze Input**:
   - Identify distinct user needs and workflows
   - Recognize different user types/personas
   - Break down into atomic, deliverable pieces
   - Identify dependencies and order

2. **Generate User Stories**:
   - Use "As a [persona], I want to [action], so that [benefit]" format
   - Ensure each story is INVEST compliant:
     - Independent
     - Negotiable
     - Valuable
     - Estimable
     - Small
     - Testable

3. **Create Acceptance Criteria**:
   - Use Given-When-Then (Gherkin) format
   - Cover happy path and edge cases
   - Include error scenarios
   - Define non-functional requirements
   - Specify success criteria

4. **Organize Stories**:
   - Group into epics if multiple related stories
   - Suggest priority (P0, P1, P2)
   - Estimate size (story points or t-shirt sizing)
   - Map dependencies

5. **Provide Implementation Notes**:
   - Technical considerations
   - Design requirements
   - Testing scenarios

## Template

```markdown
## Epic: [Epic Name]

### User Story 1: [Title]

**Story**:
As a [persona]
I want to [action]
So that [outcome/benefit]

**Acceptance Criteria**:
```gherkin
Scenario: [Happy path scenario name]
  Given [initial context]
  And [additional context]
  When [action taken]
  Then [expected result]
  And [additional result]

Scenario: [Edge case]
  Given [context]
  When [edge condition]
  Then [expected handling]
```

**Priority**: P0 (MVP) | P1 | P2
**Size**: [XS/S/M/L/XL or 1/2/3/5/8 points]
**Dependencies**: [Other stories or technical requirements]
```

## Example

**Input**: "Users should be able to filter search results by date range and category"

**Output**:

```markdown
## Epic: Search Filtering

### Story 1: Filter by Date Range
As a user
I want to filter search results by date range
So that I can find recent or historical content quickly

**Acceptance Criteria**:
```gherkin
Scenario: Filter by last 7 days
  Given I am on the search results page
  When I select "Last 7 days" from the date filter
  Then I see only results from the past 7 days
  And the result count updates
  And the filter is visually indicated as active

Scenario: Custom date range
  Given I am on the search results page
  When I click "Custom range"
  And I select start date "Jan 1, 2025"
  And I select end date "Jan 31, 2025"
  Then I see results from that date range
  And the date range displays in the filter indicator
```

**Priority**: P0 (Core feature)
**Size**: 5 points (Medium)
**Dependencies**: None

---

### Story 2: Filter by Category
[Similar structure...]
```

## Model

Use: claude-sonnet-4-5

## Related

- `/pm:prd` - Generate PRD first
- `/pm:acceptance-criteria` - Deep dive on ACs
- `/pm:sprint-planner` - Plan sprint with stories
