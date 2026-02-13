# User Story Template

Complete template for writing effective user stories using INVEST criteria and the 3Cs framework.

---

## Basic User Story Format

```
As a [user type/persona]
I want [capability/action]
So that [benefit/value]
```

---

## User Story Template

### Title: [Short, descriptive title]

```
As a [specific user type]
I want [specific capability]
So that [specific benefit or goal]
```

---

### Story Details

**Epic/Theme:** [Parent epic this story belongs to]

**Priority:** [P0 - Must Have / P1 - Should Have / P2 - Nice to Have]

**Size Estimate:** [Story points or t-shirt size: XS/S/M/L/XL]

---

### Acceptance Criteria (Given-When-Then)

**Scenario 1: [Happy Path]**

```
Given [precondition/context]
When [action/trigger]
Then [expected outcome]
And [additional outcome if applicable]
```

**Scenario 2: [Alternative Path]**

```
Given [different precondition]
When [action/trigger]
Then [expected outcome]
```

**Scenario 3: [Error/Edge Case]**

```
Given [error condition]
When [action/trigger]
Then [error handling outcome]
```

---

### INVEST Checklist

Verify your story meets INVEST criteria:

- [ ] **Independent** - Can be developed in any order without dependencies on other stories
- [ ] **Negotiable** - Details are flexible, not a contract; room for conversation during implementation
- [ ] **Valuable** - Delivers clear value to users or business (not just technical tasks)
- [ ] **Estimable** - Team can reasonably estimate size/effort
- [ ] **Small** - Fits within one sprint (typically 1-5 days of work)
- [ ] **Testable** - Has clear acceptance criteria and can be verified as "done"

---

### The 3 Cs (Card, Conversation, Confirmation)

**Card:**

- This user story document is the "card" - a placeholder for conversation

**Conversation:**

- **Questions to Discuss:**
  - [Question 1 to clarify during planning]
  - [Question 2 about edge cases]
  - [Question 3 about implementation approach]

**Confirmation:**

- The acceptance criteria above are the "confirmation" - how we'll verify it's done

---

## Example User Stories

### Example 1: E-commerce Product Filter

**Title:** Filter products by price range

```
As a shopper
I want to filter products by price range
So that I can find items within my budget
```

**Priority:** P0 - Must Have

**Size Estimate:** 3 points

**Acceptance Criteria:**

**Scenario 1: Apply price filter**

```
Given I'm viewing the product listing page
When I set minimum price to $50 and maximum price to $100
Then only products priced between $50-$100 are displayed
And the product count updates to show the filtered total
And the filter values persist when I navigate back to the page
```

**Scenario 2: Clear price filter**

```
Given I have applied a price filter
When I click "Clear filters" button
Then all products are shown again
And the price range inputs are reset
```

**Scenario 3: Invalid price range**

```
Given I'm setting a price filter
When I set minimum price higher than maximum price
Then I see an error message "Minimum price must be less than maximum"
And the filter is not applied
```

**INVEST Checklist:**

- [x] Independent - No dependencies on other stories
- [x] Negotiable - UI design details can be discussed
- [x] Valuable - Helps users find affordable products
- [x] Estimable - Clear scope, team can estimate
- [x] Small - Can complete in 1-2 days
- [x] Testable - Clear acceptance criteria

---

### Example 2: Team Management Access Control

**Title:** Remove users from workspace

```
As a team admin
I want to remove users from my workspace
So that former employees lose access to company data
```

**Priority:** P0 - Must Have

**Size Estimate:** 5 points

**Acceptance Criteria:**

**Scenario 1: Remove active user**

```
Given I'm on the team management page
And I have admin privileges
When I click "Remove" next to a user
And I confirm the removal in the modal
Then the user is immediately removed from the workspace
And the user receives an email notification of removal
And the user can no longer access any workspace resources
And the user's name appears in the audit log with "Removed by [Admin Name]"
```

**Scenario 2: Attempt to remove myself**

```
Given I'm viewing my own user entry
When I click "Remove" next to my name
Then I see a warning "You cannot remove yourself. Transfer admin to another user first."
And the removal does not proceed
```

**Scenario 3: Remove last admin**

```
Given there is only one admin in the workspace
When I attempt to remove that admin
Then I see an error "Cannot remove the only admin. Promote another user to admin first."
And the removal does not proceed
```

**Scenario 4: Remove user with active sessions**

```
Given a user is currently logged in and using the workspace
When I remove that user
Then all their active sessions are immediately terminated
And they are logged out with message "Your access has been revoked. Contact your admin."
```

**INVEST Checklist:**

- [x] Independent - Self-contained feature
- [x] Negotiable - Email template and UI wording can be refined
- [x] Valuable - Critical security feature
- [x] Estimable - Clear scope with known patterns
- [x] Small - Fits in one sprint (5 days)
- [x] Testable - Comprehensive acceptance criteria

**Conversation Topics:**

- Should removed users be able to re-join via invite, or are they permanently banned?
- What happens to content created by removed users?
- Should we have a "soft delete" with grace period before permanent removal?

---

## User Story Patterns

### Feature Story Pattern

```
As a [user type]
I want [feature]
So that [business value]

Acceptance Criteria:
- Given [setup]
- When [action]
- Then [outcome]
```

**Use for:** New features, enhancements

---

### Bug Fix Story Pattern

```
As a [user type]
I want [system to behave correctly]
So that [I can accomplish task without error]

Current Behavior:
[What's happening now]

Expected Behavior:
[What should happen]

Steps to Reproduce:
1. [Step 1]
2. [Step 2]
3. [Bug occurs]
```

**Use for:** Defects, incorrect behavior

---

### Technical Debt Story Pattern

```
As a developer
I want [technical improvement]
So that [system benefit: maintainability, performance, scalability]

Why This Matters:
[Impact on velocity, reliability, or future features]

Definition of Done:
- [Measurable improvement metric]
```

**Use for:** Refactoring, tech debt, technical improvements

**Note:** Frame in terms of user/system benefit, not just "clean code"

---

### Spike Story Pattern (Research/Investigation)

```
As a [developer/PM]
I want to [investigate/research question]
So that [we can make informed decision]

Questions to Answer:
1. [Question 1]
2. [Question 2]

Definition of Done:
- Document findings in [location]
- Present recommendation to team
- Follow-up stories created if needed

Timebox: [X days - spikes should be timeboxed]
```

**Use for:** Unknowns, research, proof of concepts

---

## Tips for Writing Great User Stories

### 1. Start with the User

**Bad:** "Add export button"

**Good:**

```
As a project manager
I want to export my project data as CSV
So that I can share reports with the team who don't use our tool
```

---

### 2. Focus on Why, Not How

**Bad:** "Implement Redis caching for user sessions"

**Good:**

```
As a user
I want the app to respond quickly when I navigate between pages
So that I can work efficiently without frustrating delays
```

---

### 3. Keep It Small

**Too Large:**

```
As a user
I want a complete analytics dashboard
So that I can track all my metrics
```

**Better (Split into Smaller Stories):**

```
Story 1: As a user, I want to see my top 5 metrics on a dashboard, so that I can quickly check performance

Story 2: As a user, I want to filter metrics by date range, so that I can analyze trends over time

Story 3: As a user, I want to export dashboard data as PDF, so that I can share reports with my team
```

---

### 4. Make It Testable

**Vague:** "Improve search performance"

**Testable:**

```
As a user
I want search results to appear in less than 2 seconds
So that I can quickly find what I'm looking for

Acceptance Criteria:
- Given I enter a search query
- When I press Enter
- Then results appear within 2 seconds at p95
- And the page remains responsive during search
```

---

### 5. Include Edge Cases

Don't just test the happy path:

**Happy Path:** User successfully logs in

**Edge Cases to Cover:**

- Wrong password (error message)
- Account locked after 3 failed attempts
- Expired session (redirect to login)
- Network timeout during login
- Password reset during login attempt

---

### 6. Use Examples

Include concrete examples in acceptance criteria:

**Vague:** "System validates email addresses"

**Clear with Examples:**

```
System validates email addresses:
✓ Valid: user@example.com, name+tag@domain.co.uk, user.name@company.com
✗ Invalid: user@, @domain.com, user@domain, user domain@example.com
```

---

## Common Mistakes to Avoid

### ❌ Mistake 1: Technical Task Disguised as User Story

**Bad:**

```
As a developer
I want to refactor the authentication module
So that the code is cleaner
```

**Why Bad:** No user value, just technical improvement

**Fix:** Either frame as user benefit OR use a technical debt story pattern with system benefit

**Good:**

```
As a developer
I want to refactor the authentication module
So that we can add social login features in half the time (reducing 2 weeks to 1 week)
```

---

### ❌ Mistake 2: Too Vague

**Bad:**

```
As a user
I want better performance
So that I have a good experience
```

**Why Bad:** Not measurable, not testable, not negotiable

**Fix:** Be specific

**Good:**

```
As a user
I want pages to load in under 2 seconds
So that I can navigate the app without frustrating delays

Acceptance Criteria:
- Landing page: <1.5s
- Dashboard: <2s
- Search results: <2s
- Measured at p95, desktop, good network conditions
```

---

### ❌ Mistake 3: No Acceptance Criteria

**Bad:**

```
As a user
I want notifications
So that I know about updates
```

**Why Bad:** What counts as "done" is unclear

**Fix:** Add specific, testable acceptance criteria

---

### ❌ Mistake 4: Over-Specified

**Bad:**

```
As a user
I want a notification bell icon in the top-right header using Material-UI component with red badge showing count, animated with a 300ms bounce effect when clicked, opening a dropdown 320px wide...
```

**Why Bad:** Removes team autonomy, prescribes implementation

**Fix:** Specify behavior and constraints, not implementation

**Good:**

```
As a user
I want to see unread notifications
So that I'm aware of important updates

Acceptance Criteria:
- Indicator shows I have unread notifications
- Clicking shows list of recent notifications
- I can mark notifications as read
- I can see notification count at a glance

(Let team decide: bell icon, badge style, animation details)
```

---

### ❌ Mistake 5: Multiple Stories in One

**Bad:**

```
As a user
I want to register for an account, verify my email, set up my profile, invite team members, and configure workspace settings
```

**Why Bad:** Too large, multiple features bundled

**Fix:** Split into separate stories, create an epic

---

## Story Splitting Techniques

When a story is too large, use these splitting patterns:

**1. By Workflow Steps**

- Story 1: Register account
- Story 2: Verify email
- Story 3: Complete profile

**2. By Business Rules**

- Story 1: Basic discount (flat percentage)
- Story 2: Tiered discount (by quantity)
- Story 3: Time-based discount (seasonal)

**3. By Variations**

- Story 1: Export as CSV
- Story 2: Export as PDF
- Story 3: Export as Excel

**4. By Priority**

- Story 1: Must-have fields (email, password)
- Story 2: Nice-to-have fields (avatar, bio)

**5. By Happy/Unhappy Path**

- Story 1: Successful login
- Story 2: Failed login (error handling)
- Story 3: Account locked (security)

---

## Template Checklist

Before marking story as "Ready for Development":

- [ ] Follows "As a... I want... So that..." format
- [ ] Specifies user type (not just "user")
- [ ] Includes clear benefit/value
- [ ] Has 2-5 acceptance criteria scenarios
- [ ] Acceptance criteria use Given-When-Then format
- [ ] Covers happy path
- [ ] Covers at least one error/edge case
- [ ] Passes all INVEST criteria
- [ ] Is estimable by the team
- [ ] Has conversation topics identified
- [ ] Includes examples where helpful
- [ ] No implementation details prescribed
- [ ] Clear definition of "done"
- [ ] Size estimate provided
- [ ] Priority assigned

---

## Related Templates

- `assets/prd-structure-template.md` - Full PRD structure for larger features
- `assets/job-story-template.md` - Alternative format focusing on context
- `assets/use-case-template.md` - Detailed interaction scenarios
- `references/user-story-writing-guide.md` - Comprehensive guide to writing user stories
- `references/acceptance-criteria-guide.md` - Deep dive on acceptance criteria formats
