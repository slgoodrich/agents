# Specification Anti-Patterns

Comprehensive guide to common specification mistakes and how to avoid them.

---

## Table of Contents

1. [Solution Masquerading as Problem](#solution-masquerading-as-problem)
2. [Vague Requirements](#vague-requirements)
3. [Over-Specification](#over-specification)
4. [Missing Acceptance Criteria](#missing-acceptance-criteria)
5. [Assuming Context](#assuming-context)
6. [Technical Debt Disguised as User Stories](#technical-debt-disguised-as-user-stories)
7. [Conflating Features with Value](#conflating-features-with-value)
8. [Ignoring Edge Cases](#ignoring-edge-cases)
9. [Prescribing UI/UX Details](#prescribing-ui-ux-details)
10. [Large, Monolithic Requirements](#large-monolithic-requirements)

---

## Solution Masquerading as Problem

### The Anti-Pattern

**Definition:** Specification describes a solution instead of the underlying problem.

**Why It's Bad:**

- Prevents exploration of better solutions
- Team doesn't understand the "why"
- May build wrong thing efficiently
- Reduces innovation and creativity

### Examples

**Anti-Pattern Example 1:**

```
"We need a chatbot on the homepage"
```

**Why Bad:** This is a solution (chatbot), not a problem statement.

**What's Missing:**

- What problem are users experiencing?
- What are they trying to accomplish?
- Why is a chatbot the assumed solution?

**Fix - Problem Statement:**

```
Problem: 60% of support tickets are basic questions already answered in documentation. Users can't find answers quickly, leading to:
- High support load (200+ tickets/week)
- User frustration (3.2/5 satisfaction)
- Delayed responses (4-8 hour wait times)

User Needs:
- Instant answers to common questions
- Self-service before contacting support
- 24/7 availability

Potential Solutions to Explore:
1. Chatbot with knowledge base
2. Improved search functionality
3. Interactive FAQ with categories
4. Contextual help tooltips
5. Video tutorials

Evaluation Criteria:
- Reduces support tickets by 30%
- Users find answers in <2 minutes
- Implementation cost <$50K
- Maintainable by non-technical team

Let's explore which solution best addresses the problem.
```

---

**Anti-Pattern Example 2:**

```
"Add a notification bell icon in the header"
```

**Why Bad:** Specifies UI solution without explaining problem.

**Fix:**

```
Problem: Users miss critical time-sensitive events when away from the app:
- 40% of trial users miss activation deadline
- 25% miss payment failures leading to service interruption
- Users check app sporadically (average 1x per day)

Impact:
- Trial conversion rate: 12% (target: 20%)
- Payment update requests: 150/week
- User frustration: "I didn't know my service was interrupted"

User Need:
- Awareness of important events in real-time
- Ability to take action quickly
- Control over notification preferences

Requirements:
- Real-time alerts for critical events (payment issues, expiring trials)
- In-app notification center (accessible from any page)
- Email notifications as backup
- User can configure which events trigger notifications

Implementation can include: bell icon, slide-out panel, toast messages, or other patterns. Team decides best approach.
```

---

### How to Identify

**Warning Signs:**

- Spec starts with "Add...", "Build...", "Create..." without context
- Describes features, not problems
- No "why" or user need explained
- Jumps to solution immediately

**Questions to Ask:**

1. What problem does this solve?
2. How do we know users have this problem?
3. What have users tried already?
4. Are there alternative solutions?
5. How will we measure success?

---

### Prevention Strategy

**Always Start With:**

**1. Problem Statement:**

```
What: [Clear description of problem]
Who: [Who experiences this problem]
Impact: [Business/user impact with data]
Current Situation: [What users do today]
```

**2. User Research:**

```
Evidence:
- User interviews: [Findings]
- Support tickets: [Frequency, themes]
- Analytics: [Behavior data]
- User quotes: [Direct feedback]
```

**3. Exploration:**

```
Potential Solutions:
1. [Solution A with pros/cons]
2. [Solution B with pros/cons]
3. [Solution C with pros/cons]

Recommended: [Solution] because [rationale]
```

---

## Vague Requirements

### The Anti-Pattern

**Definition:** Requirements use ambiguous language that can be interpreted multiple ways.

**Why It's Bad:**

- Different team members have different understanding
- Can't be tested objectively
- Leads to rework when expectations don't match
- Delays and conflicts during implementation

### Examples of Vague Language

**Vague Words to Avoid:**

| Vague Term      | Why Bad                | Better Alternative                        |
| --------------- | ---------------------- | ----------------------------------------- |
| "Fast"          | Fast to whom?          | "< 2 seconds (p95)"                       |
| "Good"          | Good by what standard? | Specific criteria                         |
| "User-friendly" | Subjective             | "Task completion <3 clicks"               |
| "Secure"        | How secure?            | "OWASP Top 10 compliant"                  |
| "Scalable"      | To what extent?        | "Handles 10K concurrent users"            |
| "Intuitive"     | For whom?              | "First-time users complete task in 5 min" |
| "Reliable"      | What reliability?      | "99.9% uptime"                            |
| "Soon"          | When exactly?          | Specific date or sprint                   |
| "Simple"        | Simple how?            | "Max 3 steps to complete"                 |
| "Better"        | Better than what?      | Specific improvement metric               |

---

**Anti-Pattern Example 1:**

```
"System should have good performance"
```

**Why Bad:**

- What is "good"?
- Performance of what? (pages, APIs, search, reports?)
- Under what load?
- How measured?

**Fix:**

```
Performance Requirements:

Page Load Times (Measured via Lighthouse):
- Homepage: <1.5 seconds (p95)
- Dashboard: <2 seconds (p95)
- Search results: <1 second (p95)
- Report generation: <5 seconds (p95)

API Response Times (Measured from application server):
- GET requests: <200ms (p95)
- POST requests: <500ms (p95)
- Complex queries: <1 second (p95)

Load Capacity:
- Supports 1,000 concurrent users
- Handles 5,000 requests/second peak
- No degradation up to 80% capacity

Test Conditions:
- Database with 1M records
- US East Coast data center
- Desktop Chrome, good 4G connection
```

---

**Anti-Pattern Example 2:**

```
"The interface should be intuitive and easy to use"
```

**Why Bad:**

- "Intuitive" is subjective
- "Easy" by what measure?
- No way to verify objectively

**Fix:**

```
Usability Requirements:

Learnability:
- New users complete primary task within 5 minutes (verified via user testing with 10 participants)
- Onboarding flow completion rate >80%
- First-time users can navigate to any main section without help

Efficiency:
- Primary workflows require ≤3 clicks
- Experienced users complete common tasks in <30 seconds
- Keyboard shortcuts available for all frequent actions

Error Prevention:
- Inline validation with real-time feedback
- Confirmation dialogs for destructive actions
- Undo available for all state-changing operations

Accessibility:
- WCAG 2.1 Level AA compliant (verified via automated and manual testing)
- Screen reader compatible
- Keyboard navigable

Verification Methods:
- Task completion time studies (5 users)
- Success rate measurement
- Time-to-first-value tracking
- User satisfaction surveys (>4.0/5.0 target)
```

---

**Anti-Pattern Example 3:**

```
"Handle large files"
```

**Why Bad:**

- How large is "large"?
- What does "handle" mean?
- Any constraints?

**Fix:**

```
File Upload Requirements:

Supported File Sizes:
- Images (JPG, PNG, GIF): Up to 10MB each
- Documents (PDF): Up to 25MB each
- Videos (MP4): Up to 100MB each

Upload Behavior:
- Files >5MB: Show progress bar with percentage
- Files <5MB: Simple loading indicator
- If upload fails: Automatic retry (3 attempts with exponential backoff)

Performance:
- 10MB file uploads in <30 seconds on 10 Mbps connection
- Upload does not block UI (background processing)
- User can continue working during upload

Error Handling:
- File too large: "File exceeds [format] limit of [X]MB"
- Unsupported format: "Only [formats] supported"
- Network failure: "Upload failed. Retry?"

Constraints:
- Maximum 5 simultaneous uploads
- Total storage quota: 100GB per user
```

---

### How to Make Requirements Specific

**Template:**

```
[Feature/Requirement]

What: [Specific capability]
When: [Trigger/context]
Where: [Location in system]
Who: [User type]
How Measured: [Specific metric]
Success Criteria: [Objective test]
```

**Example:**

```
Search Performance

What: Product search returns results quickly
When: User enters search query and presses Enter
Where: Main search bar in header (all pages)
Who: All logged-in users
How Measured: Time from Enter key to results displayed (Lighthouse, real user monitoring)
Success Criteria:
- <1 second (p95) for database with 100K products
- <2 seconds (p99)
- Works with 100 concurrent searches without degradation
```

---

### Specificity Checklist

For every requirement, ask:

- [ ] **Can we measure it?** (numbers, percentages, timeframes)
- [ ] **Can we test it?** (objective pass/fail)
- [ ] **Is it clear to all team members?** (no ambiguity)
- [ ] **Does it include constraints?** (limits, boundaries)
- [ ] **Does it define "done"?** (when is it satisfied)
- [ ] **Have we included examples?** (concrete cases)

---

## Over-Specification

### The Anti-Pattern

**Definition:** Specification prescribes implementation details, removing team autonomy and flexibility.

**Why It's Bad:**

- Removes engineering creativity
- May prescribe suboptimal solution
- Rigid, can't adapt to technical constraints
- Micromanages team
- Wastes time documenting implementation

### What to Specify vs. What to Leave Open

**✓ Specify (What/Why):**

- User-facing behavior
- Business rules
- Security/compliance requirements
- Performance targets
- Data to display
- User workflows

**✗ Don't Specify (How):**

- Technology choices (unless constrained)
- UI component libraries
- Database schema details
- Code architecture
- API design details
- Specific algorithms

---

**Anti-Pattern Example 1:**

```
"Use a React dropdown component with Material-UI styling, 300ms fade-in animation, store selection in Redux global state using the useSelector hook, and trigger onChange callback that dispatches UPDATE_SELECTION action"
```

**Why Bad:**

- Prescribes technology (React, Material-UI, Redux)
- Specifies implementation (hooks, actions)
- Removes flexibility
- May not be optimal
- Too much detail for spec

**Fix:**

```
User Selection Behavior:

What:
- User can select an option from a list of choices
- Selected option persists across page refreshes
- Selected option is displayed in subsequent screens

Requirements:
- All options visible without scrolling (if <10 options)
- Selected option highlighted visually
- Keyboard accessible (arrow keys, Enter to select)
- Screen reader announces selected option

Performance:
- Selection updates UI in <100ms
- No page flicker or layout shift

Let engineering decide: component library, state management, animation details.
```

---

**Anti-Pattern Example 2:**

```
"Create a PostgreSQL table named 'users' with columns: id (UUID primary key), email (VARCHAR(255) unique not null), password_hash (CHAR(60) bcrypt), created_at (TIMESTAMP), last_login (TIMESTAMP nullable), with indexes on email and created_at"
```

**Why Bad:**

- Specifies database technology
- Prescribes schema details
- Dictates implementation
- Engineering should own this

**Fix:**

```
User Data Requirements:

Data to Persist:
- Unique identifier for each user
- Email address (must be unique, required)
- Secure password storage (industry-standard hashing)
- Account creation timestamp
- Last login timestamp (optional)

Performance:
- User lookup by email <10ms
- Supports 100K users initially, scalable to 1M+

Security:
- Passwords never stored in plain text
- Password hashing meets OWASP recommendations
- Compliance with GDPR (data retention, deletion)

Let engineering decide: database choice, schema design, indexing strategy, password hashing algorithm (as long as meets security requirements).
```

---

**Anti-Pattern Example 3:**

```
"On button click, make HTTP POST request to /api/v1/submit endpoint with JSON payload containing {userId: number, formData: object}, include Authorization: Bearer ${token} header, handle 200 OK success by showing success toast using react-toastify library positioned top-right with 3-second auto-dismiss"
```

**Why Bad:**

- API design details
- Library choices
- UI implementation
- Too prescriptive

**Fix:**

```
Form Submission:

Behavior:
- User clicks submit button
- Form data is saved
- User receives confirmation
- Form is cleared/reset after successful save

Requirements:
- Submit button disabled during submission (prevent double-submit)
- User sees loading state while submitting
- Success confirmation is clear and noticeable
- Submission completes in <2 seconds (p95)

Error Handling:
- Network failure: User can retry
- Validation error: Specific field errors shown
- Server error: Generic error with support contact

Let engineering decide: API design, HTTP methods, payload format, success notification approach, libraries.
```

---

### How Much Detail is Right?

**Rule of Thumb:** Specify constraints and outcomes, not implementation.

**Questions to Ask:**

1. Does user care about this detail? (If no, probably over-specified)
2. Is there only one right way to do this? (If no, leave flexible)
3. Am I telling team _how_ to build it? (If yes, probably too detailed)
4. Does this remove technical flexibility? (If yes, reconsider)

**Good Level of Detail:**

```
Password Security

Requirements:
- Passwords hashed with industry-standard algorithm
- Minimum cost factor appropriate for current hardware (delays login by ~200-500ms)
- Plaintext passwords never logged or stored
- Meets OWASP password storage guidelines

Let engineering choose specific algorithm (bcrypt, Argon2, scrypt) and cost factor.
```

**Too Little Detail:**

```
"Passwords should be secure"
```

**Too Much Detail:**

```
"Use bcrypt with cost factor 12, salt generated using crypto.randomBytes(16), hash stored as 60-character string in CHAR(60) column, comparison done using constant-time comparison function to prevent timing attacks"
```

---

### When to Be Prescriptive

**Do Specify Implementation When:**

1. **Regulatory/Compliance Requirement:**

   ```
   "Use TLS 1.3 or TLS 1.2 for all HTTPS connections (HIPAA requirement)"
   ```

2. **Existing System Constraint:**

   ```
   "Must integrate with existing Stripe API for payment processing (company standard)"
   ```

3. **Proven Critical Path:**

   ```
   "Use lazy loading for images below fold (proven to reduce page load by 40%)"
   ```

4. **Known Performance Issue:**
   ```
   "Avoid N+1 queries on order history page (caused production outage last month)"
   ```

---

## Missing Acceptance Criteria

### The Anti-Pattern

**Definition:** User story or requirement has no clear "done" criteria.

**Why It's Bad:**

- No shared understanding of "done"
- Endless iteration and scope creep
- QA doesn't know what to test
- Product can't verify value delivered
- Team doesn't know when to stop

### Examples

**Anti-Pattern Example 1:**

```
User Story:
As a user
I want notifications
So that I'm aware of updates
```

**Why Bad:**

- What type of notifications?
- When are they sent?
- How are they displayed?
- What can user control?
- When is this "done"?

**Fix:**

```
User Story:
As a user
I want to receive email notifications for important events
So that I'm aware even when not in the app

Acceptance Criteria:

Scenario 1: Receive payment failure notification
Given my payment fails
When the payment processor returns error
Then I receive email within 5 minutes
And email includes:
  - Clear subject: "Payment Failed - Action Required"
  - What failed and why
  - How to update payment method
  - Link to billing settings

Scenario 2: Configure notification preferences
Given I'm in account settings
When I navigate to "Notifications"
Then I see toggles for each notification type:
  - Payment issues (always on, cannot disable)
  - Account security (always on, cannot disable)
  - Product updates (optional)
  - Marketing emails (optional)
And I can toggle optional notifications on/off
And changes save immediately

Scenario 3: Unsubscribe from marketing
Given I receive marketing email
When I click "Unsubscribe" in footer
Then I'm taken to preferences page
And marketing emails toggle is turned off
And I see confirmation "You've unsubscribed from marketing emails"

Scenario 4: Email delivery
Given notification is triggered
When system sends email
Then email delivers within 5 minutes (p95)
And delivery is tracked (sent, delivered, opened)
And failed deliveries are retried (3 attempts)
```

---

**Anti-Pattern Example 2:**

```
Requirement:
"System should handle errors gracefully"
```

**Why Bad:**

- What errors?
- What does "gracefully" mean?
- No examples
- Not testable

**Fix:**

```
Error Handling Requirements:

User-Facing Errors:

Error Category 1: Network Failures
- Scenario: API request times out after 30 seconds
- User sees: "Connection timeout. Please check your internet and try again."
- UI: Error message with "Retry" button, original form data preserved
- System: Error logged with request details, no sensitive data

Error Category 2: Validation Errors
- Scenario: User enters invalid email format
- User sees: "Please enter a valid email address (e.g., name@example.com)"
- UI: Inline error below field, field highlighted, no form submission
- System: No error logged (expected user input)

Error Category 3: Server Errors (500)
- Scenario: Database connection fails
- User sees: "Something went wrong on our end. We've been notified and are working on it."
- UI: Error message with support email, option to report issue
- System: Error logged with full stack trace, alert sent to ops team

Acceptance Criteria:
- All errors have user-friendly messages (no technical jargon)
- Users can always recover or get help
- Sensitive data never shown in errors
- Error rates tracked (alert if >1% of requests)
- Each error type tested with specific test case
```

---

### How to Write Good Acceptance Criteria

**Template:**

```
Given [precondition/context]
When [action/trigger]
Then [expected result]
And [additional result]
```

**Include:**

1. Happy path (successful scenario)
2. Unhappy paths (errors, edge cases)
3. Specific examples
4. Expected UI states
5. Data validation rules
6. Error messages

**Example:**

```
Feature: Product Search

Acceptance Criteria:

Happy Path:
Given I'm on the products page
When I enter "laptop" in the search box
And I press Enter
Then I see products matching "laptop"
And results show count: "42 results for 'laptop'"
And "laptop" is highlighted in product names
And results are sorted by relevance

Error Case: No Results
Given I search for "xyzabc123"
When I press Enter
Then I see "No products found for 'xyzabc123'"
And I see suggestions: "Try different keywords or browse categories"
And I can clear search and see all products

Edge Case: Special Characters
Given I search for "laptop & desktop"
When I press Enter
Then search treats "&" as "AND" operator
And results include products with both "laptop" and "desktop"

Edge Case: Very Long Query
Given I enter search query >200 characters
When I press Enter
Then query is truncated to 200 characters
And I see notice: "Search limited to 200 characters"
```

---

## Assuming Context

### The Anti-Pattern

**Definition:** Specification assumes reader has context or domain knowledge.

**Why It's Bad:**

- New team members can't understand
- Engineers don't know business context
- Designers don't understand technical constraints
- Cross-functional teams misaligned

### Examples

**Anti-Pattern Example:**

```
"Update the churn calculation to match the new retention methodology"
```

**Why Bad:**

- What is "churn"? (Definition may vary)
- What was old calculation?
- What is new retention methodology?
- Why are we changing?

**Fix:**

```
Background:
Churn = % of customers who stopped using product in a time period
Current calculation: Monthly churn = Customers lost in month / Customers at start of month
Problem: Doesn't account for new customers acquired during month

New Methodology:
Monthly churn = Customers lost in month / Average customers in month
Where: Average = (Start of month + End of month) / 2

Why Changing:
- Current method inflates churn during growth periods
- New method is industry standard (matches Stripe, ChartMogul)
- Enables better comparison with competitors

Example:
Month start: 1000 customers
Month end: 950 customers
Lost: 100 customers
New: 50 customers

Old calculation: 100 / 1000 = 10% churn
New calculation: 100 / ((1000 + 950) / 2) = 100 / 975 = 10.3% churn

Requirements:
- Update dashboard churn chart to use new formula
- Add tooltip explaining calculation
- Historical data recalculated retroactively
- Export includes calculation methodology note
```

---

**Anti-Pattern Example:**

```
"Implement the Stripe webhook handler for subscription updates"
```

**Why Bad:**

- Assumes team knows Stripe webhooks
- Assumes team knows which events matter
- No context on business impact

**Fix:**

```
Context:
When customer subscription changes in Stripe (upgrade, downgrade, cancel), we need to update our database to stay in sync.

Business Impact:
- Out-of-sync data causes support issues (customers see wrong plan)
- Billing errors when features don't match subscription
- Analytics/metrics incorrect

How Stripe Webhooks Work:
- Stripe sends HTTP POST to our webhook endpoint when events occur
- We receive JSON payload with event details
- We must respond with 200 OK within 30 seconds
- Stripe retries failed webhooks (exponential backoff, up to 3 days)

Events to Handle:
1. customer.subscription.updated
   - Customer upgrades/downgrades plan
   - Update user's plan_id and features in our database
   - Send confirmation email

2. customer.subscription.deleted
   - Customer cancels subscription
   - Downgrade to free plan
   - Send cancellation email

3. invoice.payment_failed
   - Payment failed for renewal
   - Send payment failure email
   - Give 7-day grace period before downgrade

Requirements:
- Webhook endpoint at /api/webhooks/stripe
- Verify webhook signature (prevent spoofing)
- Handle events idempotently (same event can arrive multiple times)
- Log all webhook events for debugging
- Alert if webhook processing fails
- Respond within 10 seconds (Stripe timeout is 30s)

Security:
- Verify webhook signature using Stripe signature header
- Use environment variable for webhook secret
- Reject unsigned requests

Error Handling:
- Transient errors: Throw error, let Stripe retry
- Permanent errors: Log, alert, return 200 (don't retry)
```

---

### Providing Context Checklist

For every spec, include:

- [ ] **Background:** Why this exists, history
- [ ] **Business Context:** Impact on users/business
- [ ] **Domain Definitions:** Explain jargon
- [ ] **Current State:** How it works today
- [ ] **Desired State:** How it should work
- [ ] **Why Changing:** Rationale for change
- [ ] **Examples:** Concrete scenarios
- [ ] **Constraints:** Limitations to be aware of
- [ ] **Success Metrics:** How we'll measure success

---

## Summary

**Key Takeaways:**

1. **Start with Problems, Not Solutions**
   - Understand user needs first
   - Explore multiple solutions
   - Justify solution choice

2. **Be Specific and Measurable**
   - No vague terms ("fast", "good", "intuitive")
   - Use numbers, examples, timeframes
   - Make requirements testable

3. **Specify What, Not How**
   - Define behavior and constraints
   - Let engineering own implementation
   - Prescribe only when necessary (compliance, constraints)

4. **Always Include Acceptance Criteria**
   - Happy path + unhappy paths
   - Specific, testable conditions
   - Clear definition of "done"

5. **Provide Context**
   - Don't assume knowledge
   - Explain background and rationale
   - Define domain terms
   - Show examples

**Remember:** Good specifications enable teams to build the right thing efficiently, while bad specifications constrain teams and lead to rework.
