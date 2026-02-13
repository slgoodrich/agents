# Acceptance Criteria Guide

Comprehensive guide to writing clear, testable acceptance criteria for user stories and requirements.

---

## What Are Acceptance Criteria?

**Definition:** Specific conditions that must be met for a user story to be considered "done."

**Purpose:**

- Create shared understanding between product, engineering, and QA
- Define testable "done" criteria
- Prevent scope creep during development
- Form basis for QA test cases
- Enable automated testing

**Key Principle:** Acceptance criteria define **what** to build, not **how** to build it.

---

## The Three Formats

### Format 1: Given-When-Then (Gherkin/BDD)

**Best For:**

- Behavior-driven development
- Sequential workflows
- State transitions
- Automated testing (Cucumber, Behave)

**Structure:**

```
Given [precondition/context]
When [action/event]
Then [expected outcome]
And [additional outcome]
But [exception/variation]
```

**Example - Login Flow:**

```
Scenario: Successful login with valid credentials

Given I am on the login page
And I am not currently logged in
When I enter valid email "user@example.com"
And I enter valid password
And I click the "Login" button
Then I am redirected to my dashboard
And I see a welcome message with my name
And my session is active
And I can access protected features
```

**Example - Error Handling:**

```
Scenario: Login fails with invalid credentials

Given I am on the login page
When I enter email "user@example.com"
And I enter incorrect password
And I click the "Login" button
Then I remain on the login page
And I see error message "Invalid email or password"
And the password field is cleared
And the email field retains my input
But I am not logged in
And no session is created
```

**When to Use:**

- Stories with clear trigger events
- Multi-step workflows
- State-based behavior
- When using BDD tools

---

### Format 2: Checklist Style

**Best For:**

- Simple features
- Independent criteria
- Non-sequential requirements
- Quick validation

**Structure:**

```
Acceptance Criteria:
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
```

**Example - File Upload:**

```
Acceptance Criteria:
- [ ] User can select files via file picker dialog
- [ ] User can drag and drop files onto upload zone
- [ ] Supported formats: JPG, PNG, GIF, PDF
- [ ] Maximum file size: 10MB per file
- [ ] Maximum 5 files per upload
- [ ] Upload progress bar shows percentage complete
- [ ] Preview shows for image files before upload completes
- [ ] Success message appears after successful upload
- [ ] Error message shows if file too large: "File exceeds 10MB limit"
- [ ] Error message shows if format unsupported: "Only JPG, PNG, GIF, PDF allowed"
- [ ] Uploaded files appear in file list immediately
- [ ] Clicking uploaded file opens preview/download
```

**When to Use:**

- Stories with multiple independent conditions
- Feature checklists
- Configuration requirements
- When Given-When-Then feels forced

---

### Format 3: Example-Based

**Best For:**

- Complex calculations
- Validation rules
- Data transformations
- Edge case documentation

**Structure:**

```
Scenario: [Description]
Input: [What user provides]
Output: [What system produces]
```

**Example - Email Validation:**

```
Acceptance Criteria:

Scenario 1: Valid standard email
Input: user@example.com
Output: Email accepted, form submits successfully

Scenario 2: Valid email with subdomain
Input: user@mail.example.com
Output: Email accepted

Scenario 3: Valid email with plus addressing
Input: user+tag@example.com
Output: Email accepted

Scenario 4: Valid email with dots in local part
Input: user.name@example.com
Output: Email accepted

Scenario 5: Missing @ symbol
Input: userexample.com
Output: Error "Email must include @ symbol"

Scenario 6: Multiple @ symbols
Input: user@@example.com
Output: Error "Email cannot contain multiple @ symbols"

Scenario 7: Missing domain
Input: user@
Output: Error "Email must include domain after @"

Scenario 8: Invalid characters
Input: user name@example.com (space)
Output: Error "Email cannot contain spaces"

Scenario 9: Too long
Input: [string > 254 characters]@example.com
Output: Error "Email cannot exceed 254 characters"
```

**Example - Price Calculation:**

```
Acceptance Criteria:

Scenario 1: Standard pricing
Input:
- Quantity: 1
- Unit price: $100
- Tax rate: 10%
Output:
- Subtotal: $100.00
- Tax: $10.00
- Total: $110.00

Scenario 2: Quantity discount
Input:
- Quantity: 10
- Unit price: $100
- Discount: 15% (orders 10+)
- Tax rate: 10%
Output:
- Subtotal: $850.00 ($100 × 10 × 0.85)
- Tax: $85.00
- Total: $935.00

Scenario 3: Free shipping threshold
Input:
- Subtotal: $150
- Shipping: $10
- Free shipping threshold: $100
Output:
- Shipping: $0.00 (free)
- Message: "You qualify for free shipping!"
```

**When to Use:**

- Complex logic with multiple variations
- Calculation-heavy features
- Validation rules
- Need to document specific examples

---

## Writing Effective Acceptance Criteria

### Principle 1: Be Specific and Measurable

**Vague (Bad):**

```
- System should be fast
- UI should be user-friendly
- Error messages should be helpful
```

**Specific (Good):**

```
- Page loads in <2 seconds (p95)
- All buttons have clear labels and are keyboard accessible
- Error messages tell user exactly what went wrong and how to fix it
```

---

### Principle 2: Cover Happy and Unhappy Paths

**Only Happy Path (Incomplete):**

```
Given user enters valid credentials
When user clicks login
Then user is logged in
```

**Happy + Unhappy Paths (Complete):**

```
Happy Path:
Given user enters valid credentials
When user clicks login
Then user is logged in and redirected to dashboard

Unhappy Path 1: Invalid credentials
Given user enters wrong password
When user clicks login
Then error shown: "Invalid email or password"
And user remains on login page

Unhappy Path 2: Account locked
Given user failed login 5 times
When user tries to login again
Then error shown: "Account locked. Reset your password or wait 15 minutes"

Unhappy Path 3: Network timeout
Given user clicks login
When network request times out after 30s
Then error shown: "Connection timeout. Please try again"
And retry button is available
```

---

### Principle 3: Use Examples

**Without Examples (Ambiguous):**

```
- System validates phone numbers
```

**With Examples (Clear):**

```
- System validates phone numbers:
  ✓ Valid: (555) 123-4567, 555-123-4567, 5551234567, +1-555-123-4567
  ✗ Invalid: 123, 555-12-3456 (wrong format), abc-def-ghij (letters)
```

---

### Principle 4: State Expected UI Changes

**Vague:**

```
- User can submit form
```

**Specific with UI State:**

```
- User can submit form:
  - Before submit: Button shows "Submit", enabled
  - During submit: Button shows "Submitting...", disabled, spinner visible
  - After success: Button shows "Submitted", disabled, success checkmark visible
  - After error: Button shows "Submit", enabled, error message below form
```

---

### Principle 5: Include Edge Cases

**Missing Edge Cases:**

```
- User can create a new project
```

**With Edge Cases:**

```
- User can create a new project:
  - Happy path: Valid name, user has <10 projects
  - Edge case 1: Empty name → Error "Project name required"
  - Edge case 2: Duplicate name → Error "Project with this name already exists"
  - Edge case 3: Name too long (>100 chars) → Error "Name must be 100 characters or less"
  - Edge case 4: User at max projects (10) → Error "Maximum 10 projects. Delete a project first."
  - Edge case 5: Special characters in name → Allowed except <>?/\|*
```

---

## Common Patterns

### Pattern 1: Form Validation

**Template:**

```
Field: [Field name]

Valid input:
- [Criterion 1]
- [Criterion 2]

Invalid input:
- [Case 1] → Error message: "[Message]"
- [Case 2] → Error message: "[Message]"
```

**Example - Password Field:**

```
Field: Password

Valid input:
- 12-128 characters
- Contains at least 1 uppercase letter
- Contains at least 1 lowercase letter
- Contains at least 1 number
- Contains at least 1 special character (!@#$%^&*)

Invalid input:
- <12 characters → "Password must be at least 12 characters"
- No uppercase → "Password must contain at least one uppercase letter"
- No lowercase → "Password must contain at least one lowercase letter"
- No number → "Password must contain at least one number"
- No special char → "Password must contain at least one special character (!@#$%^&*)"
- Common password (e.g., "Password123!") → "This password is too common. Choose a more unique password."

UI Behavior:
- Password strength indicator updates in real-time
- Each requirement shows checkmark when met
- Submit button disabled until all requirements met
```

---

### Pattern 2: CRUD Operations

**Template for Create:**

```
Given [user state]
When user creates [entity]
Then:
- [Entity] is saved to database
- User sees confirmation: "[Message]"
- User is [redirected/shown entity]
- [Entity] appears in listing immediately
- Audit log records creation (who, when)
```

**Example - Create User:**

```
Scenario: Admin creates new user

Given I am logged in as admin
And I am on the "Add User" page
When I enter:
  - Email: newuser@example.com
  - Name: John Smith
  - Role: Editor
And I click "Create User"
Then:
- User account is created in database
- Welcome email is sent to newuser@example.com
- I see success message: "User John Smith created successfully"
- I am redirected to user listing page
- John Smith appears in user listing
- Audit log shows "Admin [my name] created user John Smith at [timestamp]"
```

---

### Pattern 3: Search/Filter

**Template:**

```
Given [data state]
When user searches for "[query]"
Then:
- Results matching [criteria] are shown
- Results count displays: "X results"
- Results are sorted by [field]
- If no results: "[Empty state message]"
- Search query persists in URL (for sharing/bookmarking)
```

**Example - Product Search:**

```
Scenario 1: Search with results

Given product catalog has 1000 products
When I enter "laptop" in search box
And I press Enter or click search icon
Then:
- Products with "laptop" in name or description are shown
- Results count shows "42 results for 'laptop'"
- Products are sorted by relevance (best match first)
- Search term "laptop" is highlighted in results
- URL updates to /search?q=laptop
- Search term persists if I navigate back

Scenario 2: Search with no results

Given I search for "xyzabc123"
When I press Enter
Then:
- Empty state shows: "No products found for 'xyzabc123'"
- Suggestion shown: "Try different keywords or browse categories"
- Search filters are visible to refine search
- Recent searches dropdown available

Scenario 3: Search with filters

Given I search for "laptop"
When I apply filter "Price: $500-$1000"
And I apply filter "Brand: Dell"
Then:
- Only Dell laptops priced $500-$1000 are shown
- Results count updates
- Applied filters show as removable chips/tags
- URL includes filters: /search?q=laptop&price=500-1000&brand=dell
```

---

## Acceptance Criteria for Different Story Types

### Feature Stories

**Focus:** New capability, user value, happy + unhappy paths

**Example:**

```
Story: User can reset forgotten password

Acceptance Criteria:

Scenario 1: Request password reset
Given I'm on login page
When I click "Forgot password?"
And I enter my email
And I click "Send reset link"
Then I see message "Reset link sent to your email"
And I receive email with reset link within 5 minutes
And reset link is valid for 24 hours

Scenario 2: Reset password with valid link
Given I click valid reset link from email
When I enter new password (meets requirements)
And I confirm new password (matches)
And I click "Reset Password"
Then password is updated
And I see "Password reset successful"
And I'm redirected to login page
And I can log in with new password
And old password no longer works

Scenario 3: Invalid/expired link
Given I click reset link older than 24 hours
When page loads
Then I see "Reset link expired. Request a new one."
And I can request new reset link
```

---

### Bug Fix Stories

**Focus:** Current behavior, expected behavior, how to verify fixed

**Example:**

```
Story: Fix incorrect tax calculation for Canadian orders

Current Behavior:
- Orders to Canada calculate only federal GST (5%)
- Provincial tax (e.g., ON HST 13%) is not included
- Total is incorrect

Expected Behavior:
- Orders to Canada calculate correct tax based on province
- ON, NB, NL, NS, PE: HST (13-15%)
- BC, MB, SK: GST (5%) + PST (6-8%)
- AB: GST only (5%)

Acceptance Criteria:

Test Case 1: Ontario order
Given cart total is $100
And shipping address is Ontario
When checkout calculates tax
Then tax is $13.00 (13% HST)
And total is $113.00

Test Case 2: Alberta order
Given cart total is $100
And shipping address is Alberta
When checkout calculates tax
Then tax is $5.00 (5% GST)
And total is $105.00

Test Case 3: Order summary
Given I proceed to payment
Then order summary shows:
- Subtotal: $100.00
- Tax (HST 13%): $13.00
- Total: $113.00

Test Case 4: Invoice
Given order is completed
Then invoice shows correct tax label (HST/GST+PST)
And tax rate matches province
```

---

### Technical Debt/Refactoring Stories

**Focus:** Performance improvements, measurable outcomes

**Example:**

```
Story: Optimize product search query performance

Current State:
- Search query takes 5-8 seconds
- Database query scans all 100K products
- No indexes on search fields
- Blocks UI during search

Target State:
- Search returns results in <1 second (p95)
- Database query uses indexes
- UI remains responsive during search

Acceptance Criteria:

Performance:
- Search query execution time <500ms (p95)
- Database query uses indexes (verify with EXPLAIN)
- No full table scans
- Search handles 100 concurrent requests without degradation

Functional:
- Search results are same as before (no behavior change)
- All existing search features work (filters, sorting, pagination)
- Search relevance scoring unchanged

Verification:
- Load test shows <1s response time at 100 concurrent users
- Monitoring dashboard shows <500ms query time (p95)
- EXPLAIN shows index usage, no table scans
- Manual testing confirms all features work
```

---

## Anti-Patterns to Avoid

### Anti-Pattern 1: Implementation Details in Criteria

**Bad:**

```
- Use React hooks for state management
- Implement using REST API with JSON payload
- Store data in PostgreSQL users table
```

**Good:**

```
- User data persists across sessions
- API calls complete in <500ms
- Data remains consistent across page refreshes
```

---

### Anti-Pattern 2: Too Vague

**Bad:**

```
- System works well
- Good user experience
- Performs acceptably
```

**Good:**

```
- Page loads in <2 seconds (p95)
- All buttons labeled clearly with action (e.g., "Save", "Cancel", not just icons)
- Forms validate in real-time with helpful error messages
```

---

### Anti-Pattern 3: No Error Cases

**Bad:**

```
- User can upload file
```

**Good:**

```
- User can upload file:
  - Happy: File <10MB, supported format → uploads successfully
  - Error 1: File >10MB → "File too large. Maximum 10MB."
  - Error 2: Unsupported format → "Only JPG, PNG, PDF allowed."
  - Error 3: Network failure → "Upload failed. Retry?"
```

---

### Anti-Pattern 4: Untestable Criteria

**Bad:**

```
- UI looks good
- Code is clean
- Performance is acceptable
```

**Good:**

```
- Lighthouse accessibility score >90
- Code coverage >80% for new code
- Page load time <2 seconds (p95)
```

---

## Acceptance Criteria Checklist

Before marking story as "Ready for Development":

- [ ] Written in clear, unambiguous language
- [ ] Covers happy path (successful scenario)
- [ ] Covers at least 2-3 unhappy paths (errors, edge cases)
- [ ] Includes specific examples where helpful
- [ ] Defines expected UI states and messages
- [ ] Is testable (can verify pass/fail)
- [ ] Does not prescribe implementation (focuses on "what", not "how")
- [ ] Measurable where applicable (time, size, count)
- [ ] Reviewed with engineering and QA
- [ ] Each criterion is independent and clear
- [ ] No ambiguous terms ("fast", "good", "acceptable")
- [ ] Documented in consistent format (Given-When-Then, checklist, or examples)

---

## Writing Criteria for QA

**Purpose:** Acceptance criteria should be directly usable by QA for test case creation.

**Best Practice:** For each acceptance criterion, QA should be able to:

1. Understand exactly what to test
2. Know how to set up the test
3. Know what the expected result is
4. Verify pass/fail unambiguously

**Example - Good for QA:**

```
Criterion: Password field validation

Test Case 1: Password too short
1. Enter password "Pass123!"  (11 chars)
2. Click out of field
3. Expected: Error shown "Password must be at least 12 characters"
4. Submit button remains disabled

Test Case 2: Password meets all requirements
1. Enter password "MySecureP@ss123" (15 chars, all requirements met)
2. Click out of field
3. Expected: All requirement checkmarks turn green
4. No error message
5. Submit button enabled
```

---

## Acceptance Criteria for Non-Functional Requirements

**Performance:**

```
- Page load time <2 seconds (p95) measured via Lighthouse
- API response time <500ms (p95) measured via APM tool
- Handles 1000 concurrent users without degradation
```

**Security:**

```
- All passwords hashed with bcrypt (cost factor 12)
- No SQL injection vulnerabilities (verified via SAST scan)
- All endpoints require authentication (verified via security test)
- PII encrypted at rest (AES-256)
```

**Accessibility:**

```
- Lighthouse accessibility score >90
- All images have alt text
- Color contrast ratio ≥4.5:1 (verified via Wave tool)
- All functionality accessible via keyboard only
- Screen reader compatible (tested with NVDA)
```

---

## Summary

**Good Acceptance Criteria:**

- Are specific, measurable, and testable
- Cover happy paths and unhappy paths (errors, edge cases)
- Include concrete examples
- Define expected UI states and messages
- Focus on "what" (behavior) not "how" (implementation)
- Can be used directly by QA for test cases
- Create shared understanding across product, engineering, QA

**Remember:** Acceptance criteria are the "confirmation" part of the 3Cs (Card, Conversation, Confirmation). They verify that the conversation led to the right implementation.
