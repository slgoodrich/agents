# User Story Writing Guide

Comprehensive guide to writing effective user stories using INVEST criteria, 3Cs framework, and modern best practices.

---

## Table of Contents

1. [What Makes a Good User Story](#what-makes-a-good-user-story)
2. [The INVEST Criteria](#the-invest-criteria)
3. [The 3 Cs Framework](#the-3-cs-framework)
4. [Acceptance Criteria Formats](#acceptance-criteria-formats)
5. [Story Splitting Patterns](#story-splitting-patterns)
6. [User Story vs Job Story vs Use Case](#user-story-vs-job-story-vs-use-case)
7. [Common Patterns and Examples](#common-patterns-and-examples)
8. [Advanced Techniques](#advanced-techniques)
9. [Anti-Patterns to Avoid](#anti-patterns-to-avoid)

---

## What Makes a Good User Story?

A good user story is a **placeholder for a conversation**, not a comprehensive specification.

**Purpose:**

- Facilitate discussion between product and engineering
- Defer details until implementation (just-in-time elaboration)
- Maintain flexibility while ensuring shared understanding
- Focus on user value, not technical implementation

**Key Characteristics:**

- Written from user's perspective
- Focuses on value/benefit (the "why")
- Small enough to complete in one sprint
- Independent of other stories (as much as possible)
- Has clear acceptance criteria
- Is negotiable (details can be discussed)

---

## The INVEST Criteria

Mike Cohn's framework for evaluating user story quality.

### I - Independent

**Definition:** Story can be developed and delivered in any order without depending on other stories.

**Why It Matters:**

- Flexible sprint planning
- Parallel development possible
- Can adjust priorities mid-sprint
- Reduces complexity and coupling

**How to Achieve:**

- Avoid "Part 1, Part 2" stories
- Make stories vertically sliced (full stack)
- Extract shared dependencies into separate stories
- Use feature flags if order matters

**Example - Bad (Dependent):**

```
Story 1: Build user database schema
Story 2: Create user API endpoints
Story 3: Build user registration UI
```

Problem: Must be done in order

**Example - Good (Independent):**

```
Story 1: User can register with email/password
Story 2: User can log in with email/password
Story 3: User can reset forgotten password
```

Each delivers complete vertical slice of value

---

### N - Negotiable

**Definition:** Story is not a contract; details are flexible and can be discussed during implementation.

**Why It Matters:**

- Team can suggest better approaches
- Encourages collaboration
- Avoids over-specification
- Implementation flexibility

**What to Leave Negotiable:**

- UI/UX details (exact wording, colors, layout)
- Technical implementation (which library, architecture)
- Edge case handling (discuss during refinement)

**What NOT to Leave Negotiable:**

- Core value proposition
- Security/compliance requirements
- Critical business rules

**Example - Too Prescribed (Not Negotiable):**

```
As a user
I want a blue "Submit" button in the bottom-right corner using Arial font at 16px
that makes an HTTP POST request to /api/submit using axios library
So that I can save my form
```

**Example - Appropriately Negotiable:**

```
As a user
I want to save my form data
So that I don't lose my work

Acceptance Criteria:
- Form data persists after save
- User gets confirmation of successful save
- Can retrieve saved data later
```

Team decides: button placement, styling, API design, tech stack

---

### V - Valuable

**Definition:** Story delivers value to users or business, not just technical implementation.

**Why It Matters:**

- Prioritization based on value
- Team members can understand ROI
- Avoids "technical for technical's sake" work

**Tests for Value:**

- Would users notice if we didn't build this?
- Can we measure impact?
- Does this solve a user problem or enable business goal?

**Example - Not Valuable (Technical Task):**

```
As a developer
I want to refactor the authentication module to use TypeScript
So that the code is type-safe
```

No user or business value

**Example - Valuable (Frames Technical Work as User Benefit):**

```
As a developer
I want to refactor the authentication module to use TypeScript
So that we can add social login features in half the time

(Reduces 2 weeks to 1 week for upcoming Google/Apple login stories)
```

Clear value: Faster delivery of user-facing features

**Alternative - Technical Debt Stories:**
When technical work is necessary but has no direct user value, frame as enabling future capabilities:

```
As the development team
We want to migrate to the latest framework version
So that we can maintain security patches and add requested features faster

(Current framework version is end-of-life in 6 months)
```

---

### E - Estimable

**Definition:** Team can reasonably estimate the effort required.

**Why It Matters:**

- Sprint planning accuracy
- Capacity management
- Identifies unknowns early

**What Makes Stories Estimable:**

- Clear scope and boundaries
- Known technology and approach
- Accessible for Q&A with product
- Similar to past work

**What Makes Stories Not Estimable:**

- Too vague or ambiguous
- Dependent on unknowns (research needed)
- No one on team has relevant experience

**Example - Not Estimable:**

```
As a user
I want better performance
So that the app is faster
```

What does "better" mean? Which part of the app?

**Example - Estimable:**

```
As a user
I want search results to load in under 2 seconds
So that I can find products quickly

Context:
- Current: 5-8 seconds
- Database has 100K products
- Team has experience optimizing queries
```

Team can estimate this

**When Stories Aren't Estimable:**
Create a **Spike Story** (timeboxed research):

```
Spike: Investigate search performance options

Goal: Determine approach for reducing search time from 8s to 2s

Questions to Answer:
1. Is database query the bottleneck?
2. Would Elasticsearch help?
3. What's the estimated effort for each approach?

Timebox: 2 days
Output: Tech spec with recommendation and estimates
```

---

### S - Small

**Definition:** Story fits within one sprint (typically 1-5 days of work).

**Why It Matters:**

- Faster feedback
- Easier to estimate accurately
- Less risk
- Frequent value delivery

**Size Guidelines:**

- 1-5 story points (using Fibonacci: 1, 2, 3, 5)
- Completable in 1-5 days
- If estimated at 8+ points, split it

**Tests for "Too Large":**

- Takes more than one sprint
- Multiple acceptance criteria (>5)
- Team says "that's a lot"
- Hard to describe in one sentence

**Example - Too Large (Epic, not Story):**

```
As a user
I want a complete user profile system
So that I can manage my account
```

**Example - Right-Sized (Split into Multiple Stories):**

```
Story 1: As a user, I want to view my profile, so I can see my account details

Story 2: As a user, I want to edit my profile name and email, so I can keep info current

Story 3: As a user, I want to upload a profile picture, so I can personalize my account

Story 4: As a user, I want to change my password, so I can maintain account security
```

---

### T - Testable

**Definition:** Clear acceptance criteria that can be verified as "done."

**Why It Matters:**

- Shared understanding of "done"
- QA can create test cases
- Developers know when finished
- Product can verify value delivered

**What Makes Stories Testable:**

- Specific acceptance criteria
- Observable outcomes
- Measurable results
- No ambiguity

**Example - Not Testable:**

```
As a user
I want a better homepage
So that I have a good experience
```

What is "better"? What is "good experience"?

**Example - Testable:**

```
As a user
I want to see my 5 most recent orders on the homepage
So that I can quickly track my purchases

Acceptance Criteria:
- Given I'm logged in
- When I land on homepage
- Then I see a "Recent Orders" section
- And it displays my last 5 orders
- And each order shows: date, total, status
- And clicking an order takes me to order details
```

Every criterion can be verified

---

## The 3 Cs Framework

Ron Jeffries' framework for understanding user story structure.

### Card

**Definition:** Physical or digital card with story title/description.

**Purpose:**

- Placeholder for conversation
- Not a complete specification
- Reminder of what to discuss

**What Goes on the Card:**

- Title: Short, descriptive
- User story: As a... I want... So that...
- Priority: P0, P1, P2
- Estimate: Story points or t-shirt size
- Brief notes (not full details)

**Example Card:**

```
Title: Email Notification Settings

As a user
I want to control which emails I receive
So that I'm not overwhelmed by notifications

Priority: P1
Estimate: 3 points
Notes: Marketing emails opt-out required by law
```

---

### Conversation

**Definition:** Discussion between product, engineering, and design to clarify details.

**Purpose:**

- Most important part of user stories
- Happens during refinement and planning
- Clarifies scope, edge cases, approach

**When Conversations Happen:**

- Backlog refinement: Initial discussion, rough sizing
- Sprint planning: Detailed discussion, commitment
- During development: Ongoing clarification

**Topics to Discuss:**

- Exact behavior and edge cases
- UI/UX approach
- Technical approach
- Definition of "done"
- Dependencies and risks

**Example Conversation Topics:**

```
Story: User can filter products by price range

Questions for Conversation:
1. What happens if min price > max price?
2. Should filter persist when user navigates away?
3. Should URL update to reflect filters (for sharing)?
4. What's the price step ($1, $5, $10)?
5. Include out-of-stock products in filtered results?
```

---

### Confirmation

**Definition:** Acceptance criteria that confirm the story is done.

**Purpose:**

- Testable definition of "done"
- Verifies value was delivered
- Basis for QA test cases

**Formats:**

- Given-When-Then (Gherkin/BDD style)
- Checklist style
- Example-based
- Scenario-based

**Example Confirmation (Given-When-Then):**

```
Scenario 1: Apply valid price filter
Given I'm on the product listing page
When I set min price to $50 and max to $100
Then only products priced $50-$100 are shown
And the product count reflects filtered results
And the filter state is saved in URL

Scenario 2: Invalid price range
Given I'm on the filter section
When I set min price higher than max price
Then I see error "Min price must be less than max"
And the filter is not applied

Scenario 3: No products in range
Given I set filter to $10,000-$15,000
When I apply the filter
Then I see "No products found in this price range"
And I have option to clear filters
```

---

## Acceptance Criteria Formats

### Format 1: Given-When-Then (Gherkin/BDD)

**Structure:**

```
Given [precondition/context]
When [action/event]
Then [expected outcome]
And [additional outcome]
```

**Best For:**

- Behavior-driven development
- Automated testing (Cucumber, etc.)
- Sequential workflows
- State transitions

**Example:**

```
Given I'm logged in as admin
And I'm on the user management page
When I click "Delete" next to a user
And I confirm the deletion
Then the user is removed from the system
And I see success message "User deleted"
And the user list updates without that user
```

---

### Format 2: Checklist Style

**Structure:**

```
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
```

**Best For:**

- Simple stories
- Multiple independent criteria
- Non-sequential requirements

**Example:**

```
Acceptance Criteria:
- [ ] User can upload JPG, PNG, GIF files
- [ ] Maximum file size is 10MB
- [ ] Image preview shows before upload completes
- [ ] Upload progress bar displays percentage
- [ ] Error message shown if file too large
- [ ] Uploaded image appears in profile immediately
```

---

### Format 3: Example-Based

**Structure:**

```
Example 1: [Scenario description]
Input: [What user provides]
Output: [What system does]

Example 2: [Another scenario]
Input: [What user provides]
Output: [What system does]
```

**Best For:**

- Complex calculations
- Validation rules
- Data transformations

**Example:**

```
Acceptance Criteria:

Example 1: Valid email
Input: user@example.com
Output: Email accepted, form submits

Example 2: Missing @ symbol
Input: userexample.com
Output: Error "Please include @ in email address"

Example 3: Multiple @ symbols
Input: user@@example.com
Output: Error "Email cannot contain multiple @ symbols"

Example 4: Missing domain
Input: user@
Output: Error "Please include domain after @"
```

---

## Story Splitting Patterns

When stories are too large (>8 story points), use these patterns to split them.

### Pattern 1: Workflow Steps

Split by sequential steps in a process.

**Large Story:**

```
As a user, I want to complete checkout
```

**Split Stories:**

```
1. As a user, I want to enter shipping address
2. As a user, I want to select shipping method
3. As a user, I want to enter payment information
4. As a user, I want to review and confirm order
```

---

### Pattern 2: Business Rules / Variations

Split by different rules or variations.

**Large Story:**

```
As a user, I want to apply a discount code
```

**Split Stories:**

```
1. As a user, I want to apply a percentage discount code
2. As a user, I want to apply a fixed-amount discount code
3. As a user, I want to apply a free-shipping discount code
4. As a user, I want to see error if discount code is invalid/expired
```

---

### Pattern 3: Simple/Complex

Start with simple version, add complexity later.

**Large Story:**

```
As a user, I want advanced search
```

**Split Stories:**

```
1. As a user, I want to search by keyword (simple)
2. As a user, I want to filter by category (add filter)
3. As a user, I want to filter by price range (add filter)
4. As a user, I want to save my search preferences (add complexity)
```

---

### Pattern 4: Happy Path / Edge Cases

Start with happy path, handle edge cases later.

**Large Story:**

```
As a user, I want to register for an account
```

**Split Stories:**

```
1. As a user, I want to register with email/password (happy path)
2. As a user, I want to see error if email already exists (edge case)
3. As a user, I want to verify my email after registration (edge case)
4. As a user, I want to resend verification email if needed (edge case)
```

---

### Pattern 5: CRUD Operations

Split create, read, update, delete into separate stories.

**Large Story:**

```
As a user, I want to manage my addresses
```

**Split Stories:**

```
1. As a user, I want to add a new address
2. As a user, I want to view my saved addresses
3. As a user, I want to edit an existing address
4. As a user, I want to delete an address
5. As a user, I want to set a default address
```

---

### Pattern 6: Data Types / Input Methods

Split by different data types or input methods.

**Large Story:**

```
As a user, I want to upload files
```

**Split Stories:**

```
1. As a user, I want to upload images (JPG, PNG)
2. As a user, I want to upload documents (PDF)
3. As a user, I want to upload spreadsheets (CSV, Excel)
4. As a user, I want to drag-and-drop files
```

---

## User Story vs Job Story vs Use Case

### When to Use Each Format

**User Stories:**

- Best for: Known features, sprint planning
- Focus: Persona-based needs
- Granularity: Small, sprintable chunks
- Format: As a [user], I want [feature], So that [benefit]

**Job Stories:**

- Best for: Discovery, understanding needs
- Focus: Context and situation
- Granularity: Problem-focused
- Format: When [situation], I want [motivation], So I can [outcome]

**Use Cases:**

- Best for: Complex workflows, system documentation
- Focus: Detailed interactions
- Granularity: Complete processes
- Format: Structured scenario with steps, alternatives, exceptions

**Comparison Example:**

**User Story:**

```
As a project manager
I want to assign tasks to team members
So that everyone knows their responsibilities
```

**Job Story:**

```
When I'm planning work for the sprint
I want to assign specific tasks with deadlines
So I can ensure work is distributed and nothing is forgotten
```

**Use Case:**

```
Use Case: Assign Task to Team Member

1. PM navigates to task board
2. PM selects unassigned task
3. PM clicks "Assign"
4. System shows team member list
5. PM selects team member
6. PM sets due date
7. System assigns task and sends notification
8. Team member receives notification

Alternative: Team member not available
- System shows "unavailable" indicator
- PM can assign anyway or choose different member
```

---

## Common Patterns and Examples

[Content continues in next message due to length...]

## Anti-Patterns to Avoid

### Anti-Pattern 1: Technical Story Disguised as User Story

**Bad:**

```
As a developer
I want to upgrade React to v18
So that the codebase uses the latest version
```

**Why Bad:** No user value

**Fix:** Frame as enabling capability

```
As a developer
I want to upgrade React to v18
So that we can implement concurrent rendering for 50% faster page loads
```

### Anti-Pattern 2: Solution Instead of Problem

**Bad:**

```
As a user
I want a chatbot
So that I can get help
```

**Why Bad:** Prescribes solution, doesn't explain problem

**Fix:** Describe problem

```
As a user
I want to quickly find answers to common questions
So that I don't have to wait for support to respond

(Explored solutions: chatbot, improved FAQ, better search)
```

### Anti-Pattern 3: Multiple Stories in One

**Bad:**

```
As a user
I want to register, verify email, set preferences, invite teammates, and configure workspace
```

**Why Bad:** Too large, multiple features

**Fix:** Split into separate stories

### Anti-Pattern 4: No Acceptance Criteria

**Bad:**

```
As a user
I want notifications
```

**Why Bad:** What counts as "done" is unclear

**Fix:** Add specific, testable criteria

---

## Summary

**Good User Stories:**

- Follow INVEST criteria (Independent, Negotiable, Valuable, Estimable, Small, Testable)
- Use 3 Cs framework (Card, Conversation, Confirmation)
- Have clear, testable acceptance criteria
- Focus on user value, not technical implementation
- Are small enough for one sprint
- Include relevant examples and edge cases

**Remember:**
Stories are placeholders for conversations, not comprehensive specs. The discussion is more important than the written artifact.
