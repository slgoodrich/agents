# Acceptance Criteria Writing Guide

Comprehensive guide to writing clear, testable acceptance criteria for user stories.

## Table of Contents

- [What Are Acceptance Criteria?](#what-are-acceptance-criteria)
- [Three Main Formats](#three-main-formats)
- [Writing Great Acceptance Criteria](#writing-great-acceptance-criteria)
- [Acceptance Criteria for Different Story Types](#acceptance-criteria-for-different-story-types)
- [Common Mistakes to Avoid](#common-mistakes-to-avoid)
- [Acceptance Criteria Checklist](#acceptance-criteria-checklist)
- [Examples: Before & After](#examples-before--after)
- [Summary: The Acceptance Criteria Formula](#summary-the-acceptance-criteria-formula)

---

## What Are Acceptance Criteria?

**Definition**: Conditions that a story must satisfy to be considered complete.

**Purpose**:

- Define "done" clearly
- Prevent misunderstanding
- Enable testing
- Guide development
- Facilitate acceptance

**A good acceptance criterion**:

- Is testable (can verify yes/no)
- Is specific (no ambiguity)
- Is complete (covers all scenarios)
- Focuses on "what", not "how"

---

## Three Main Formats

### 1. GIVEN-WHEN-THEN (BDD Style)

**Template**:

```
GIVEN [precondition/context]
WHEN [action/event]
THEN [expected outcome]
```

**When to use**:

- Complex workflows
- State-dependent behavior
- Testing focus

**Example: Login**:

```
User Story: Secure login

Acceptance Criteria:

1. GIVEN I'm on the login page
   WHEN I enter valid email and password
   THEN I'm redirected to my dashboard

2. GIVEN I'm on the login page
   WHEN I enter invalid password
   THEN I see error "Invalid email or password"
   AND password field is cleared
   AND I remain on login page

3. GIVEN I've failed login 5 times
   WHEN I attempt 6th login
   THEN my account is locked for 15 minutes
   AND I receive email about suspicious activity
```

**Benefits**:

- Clear context setup
- Explicit trigger
- Specific outcome
- Great for automated testing (Cucumber, etc.)

---

### 2. Checklist Format

**Template**:

```
Acceptance Criteria:
- [ ] [Observable outcome 1]
- [ ] [Observable outcome 2]
- [ ] [Observable outcome 3]
```

**When to use**:

- Simple, straightforward features
- Quick validation
- Less state-dependent

**Example: Export Feature**:

```
User Story: Export data as CSV

Acceptance Criteria:
- [ ] "Export" button appears on data table
- [ ] Clicking export generates CSV file
- [ ] CSV includes all visible columns
- [ ] CSV filename includes current date (data_export_2024-01-15.csv)
- [ ] Export completes within 5 seconds for up to 10K rows
- [ ] Loading indicator shows while export is processing
- [ ] Error message appears if export fails
- [ ] CSV opens correctly in Excel and Google Sheets
```

**Benefits**:

- Easy to read and write
- Clear progress tracking
- Simple pass/fail checking

---

### 3. Rule-Based Format (MoSCoW)

**Template**:

```
Acceptance Criteria:

Must:
- [Critical requirements]

Should:
- [Important but not critical]

May:
- [Nice to have]
```

**When to use**:

- Features with variable scope
- Time-constrained sprints
- Prioritization needed

**Example: Search Feature**:

```
User Story: Product search

Acceptance Criteria:

Must:
- Search accepts text input (min 2 characters)
- Results update as user types (debounced 300ms)
- Results show product name, price, image
- "No results" message when query returns 0 items
- Search works across product name and description

Should:
- Results highlight matching keywords
- Results sorted by relevance (not just alphabetical)
- Recent searches saved (last 5 searches)
- Search suggestions appear (autocomplete)

May:
- Filter search results by category
- Voice search support
- Search history shared across devices
```

**Benefits**:

- Clear prioritization
- Enables scope negotiation
- Supports MVP thinking

---

## Writing Great Acceptance Criteria

### Principle 1: Be Specific and Measurable

❌ **Vague**:

- "Page loads fast"
- "UI looks good"
- "Search works well"
- "Many users can access simultaneously"

**Specific**:

- "Page loads in < 2 seconds (p95 latency)"
- "UI matches Figma design (link) with 100% accuracy"
- "Search returns results in < 500ms for datasets up to 10K items"
- "System supports 1000 concurrent users without degradation"

**Transformation formula**: Replace vague adjectives with numbers, benchmarks, or clear definitions.

---

### Principle 2: Cover Happy Path AND Edge Cases

Every story needs both:

**Happy Path**: Normal, expected usage
**Edge Cases**: Boundaries, errors, unusual scenarios

**Example: Age Input Field**:

Happy Path:

- User enters age 25 → accepted

Edge Cases:

- User enters age 0 → error "Age must be at least 1"
- User enters age 150 → error "Please enter a valid age"
- User enters negative number → error
- User enters non-numeric value → error
- User leaves field blank → error "Age is required"

**Rule**: If you only have happy path criteria, you're not done.

---

### Principle 3: Include Error States

**Every feature can fail**. Document what happens.

**Example: Payment Processing**:

```
Acceptance Criteria:

Happy Path:
- [ ] Payment processes successfully with valid card
- [ ] User receives confirmation email within 2 minutes

Error States:
- [ ] Declined card shows error "Payment declined. Please try another card."
- [ ] Network timeout shows "Payment is processing. You'll receive confirmation shortly."
- [ ] Invalid CVV shows "Invalid security code"
- [ ] Expired card shows "This card has expired"
- [ ] Insufficient funds shows "Payment declined (insufficient funds)"
- [ ] Generic errors show "Payment failed. Please try again or contact support."
```

**Think about**:

- Network failures
- Invalid input
- System errors
- Timeout scenarios
- Permission issues

---

### Principle 4: Make Criteria Testable

**Test**: Can someone verify this criterion without interpretation?

❌ **Not testable**:

- "UI is intuitive"
- "Performance is good"
- "Feature works properly"
- "Design looks professional"

**Testable**:

- "New users complete task in < 5 minutes without help (usability test: n=10)"
- "Page load time < 2s (p95) measured via Lighthouse"
- "All acceptance criteria pass without bugs"
- "Design matches approved Figma mockup (pixel-perfect)"

**Key**: Use observable outcomes, measurable benchmarks, or clear definitions.

---

### Principle 5: Avoid Implementation Details

Focus on **what** (outcome), not **how** (implementation).

❌ **Too prescriptive** (describes HOW):

- "Use React hooks to implement"
- "Store data in PostgreSQL"
- "Call GET /api/users endpoint"
- "Implement using Observer pattern"

**Outcome-focused** (describes WHAT):

- "User sees updated data without page refresh"
- "User data persists across sessions"
- "User list loads on page visit"
- "UI updates automatically when data changes"

**Why**: Gives developers flexibility to choose best implementation.

**Exception**: Non-functional requirements (security, performance, architecture constraints).

---

## Acceptance Criteria for Different Story Types

### Feature Stories

```
User Story: Dark mode toggle

Acceptance Criteria:
- [ ] Toggle switch appears in Settings
- [ ] Toggle defaults to system preference (light/dark)
- [ ] Clicking toggle switches between light and dark mode
- [ ] Mode change applies immediately (no page refresh)
- [ ] Mode preference persists across sessions (stored in localStorage)
- [ ] All pages respect mode setting (light text on dark background)
- [ ] Images/icons have dark mode variants where needed
- [ ] Accessibility: Sufficient contrast in both modes (WCAG AA)
```

**Include**:

- UI elements
- User interactions
- Data persistence
- Visual changes
- Accessibility

---

### Bug Fix Stories

```
User Story: Fix date picker showing wrong month

Acceptance Criteria:
- [ ] Bug no longer occurs (date picker shows correct month)
- [ ] Tested with all browsers (Chrome, Safari, Firefox, Edge)
- [ ] Tested with various date formats (US, EU, ISO)
- [ ] Regression test added to test suite
- [ ] Root cause documented in ticket
- [ ] Related edge cases tested (leap years, month boundaries, timezones)
```

**Include**:

- Bug fix verification
- Regression prevention
- Cross-environment testing
- Root cause analysis

---

### Technical Debt Stories

```
User Story: Refactor authentication module

Acceptance Criteria:
- [ ] Auth module split into 4 testable files (login, logout, session, tokens)
- [ ] Unit test coverage >85%
- [ ] All existing integration tests still pass
- [ ] No change to external API (backward compatible)
- [ ] Performance unchanged or improved (measured via benchmarks)
- [ ] Code review approved by 2 senior developers
- [ ] Documentation updated with new module structure
```

**Include**:

- Technical outcomes
- Test coverage
- Backward compatibility
- Performance impact
- Documentation

---

### Spike/Research Stories

```
User Story: Research caching solutions

Acceptance Criteria:
- [ ] All research questions answered with evidence
- [ ] Pros/cons comparison matrix created for top 3 options
- [ ] POC implemented for recommended approach
- [ ] Load testing results documented (10K concurrent users)
- [ ] Cost analysis completed
- [ ] Recommendation presented to team
- [ ] Estimated effort for implementation provided
```

**Include**:

- Questions answered
- Evidence gathered
- Decision documented
- Team communicated

---

## Common Mistakes to Avoid

### Mistake 1: Too Vague

❌ **Bad**:

```
- Feature works
- UI looks good
- Performance is acceptable
```

**Good**:

```
- User can complete checkout in < 3 clicks
- UI matches approved design (Figma link)
- Page loads in < 2 seconds (p95)
```

---

### Mistake 2: Too Prescriptive

❌ **Bad**:

```
- Use React useState hook
- Store in Redux
- Call API with axios
```

**Good**:

```
- Form state persists when user navigates away
- Data available across all components
- API errors are handled gracefully
```

---

### Mistake 3: Missing Error States

❌ **Incomplete**:

```
- User can upload file
```

**Complete**:

```
- User can upload valid JPG/PNG files
- Error shown for invalid file types
- Error shown for files >10MB
- Error shown if upload fails
- User can retry failed upload
```

---

### Mistake 4: Not Testable

❌ **Not testable**:

```
- Users find it easy to use
- Design is beautiful
- Code is clean
```

**Testable**:

```
- 80% of test users complete task without help (n=10)
- Design matches approved mockup with 0 deviations
- Code passes linter with 0 warnings
```

---

### Mistake 5: No Acceptance Criteria at All

❌ **Just a story, no criteria**:

```
As a user
I want to reset my password
So that I can regain access if I forget it

[No acceptance criteria]
```

This leaves "done" undefined. Developers guess. Tests are inconsistent. Bugs slip through.

**Always include acceptance criteria.**

---

## Acceptance Criteria Checklist

Before finalizing, verify:

**Completeness**:

- [ ] Happy path covered
- [ ] Edge cases covered
- [ ] Error states covered
- [ ] Performance requirements specified
- [ ] Accessibility requirements included

**Quality**:

- [ ] Each criterion is testable
- [ ] Each criterion is specific (not vague)
- [ ] Criteria focus on "what", not "how"
- [ ] Success is clearly defined
- [ ] Failure scenarios are clear

**Collaboration**:

- [ ] Team reviewed criteria
- [ ] QA can write tests from criteria
- [ ] Developers understand what to build
- [ ] Product owner can verify completion

---

## Examples: Before & After

### Example 1: Password Reset

❌ **Before**:

```
User Story: Password reset

Acceptance Criteria:
- User can reset password
- Email sent
- Secure
```

**After**:

```
User Story: Password reset

Acceptance Criteria:
1. GIVEN I click "Forgot Password"
   WHEN I enter my email
   THEN I receive reset email within 2 minutes

2. GIVEN I click reset link in email
   WHEN I enter new password
   THEN password is updated
   AND I'm logged in automatically

3. GIVEN reset link is >24 hours old
   WHEN I click it
   THEN I see "Link expired" message
   AND I can request new link

4. Password requirements:
   - [ ] Minimum 8 characters
   - [ ] At least 1 number
   - [ ] At least 1 special character
   - [ ] Error shown if requirements not met

5. Security:
   - [ ] Reset link expires after 24 hours
   - [ ] Reset link is single-use (can't reuse after password changed)
   - [ ] Old password invalidated immediately
```

---

### Example 2: Search Feature

❌ **Before**:

```
Acceptance Criteria:
- Search works
- Results are relevant
- Fast enough
```

**After**:

```
Acceptance Criteria:

Performance:
- [ ] Results return in < 500ms for datasets up to 10K items
- [ ] Results return in < 2s for datasets up to 100K items
- [ ] Loading indicator shows if search takes >200ms

Functionality:
- [ ] Accepts minimum 2 characters
- [ ] Results update as user types (debounced 300ms)
- [ ] Search covers product name, description, SKU
- [ ] Results show: product name, price, thumbnail, stock status
- [ ] Results are paginated (20 per page)

Relevance:
- [ ] Exact matches appear first
- [ ] Partial matches appear second
- [ ] Results sorted by: exact → partial → recent

Edge Cases:
- [ ] "No results" message when query returns 0 items
- [ ] Special characters handled (quotes, slashes, unicode)
- [ ] Very long queries (>100 chars) are truncated with indicator
- [ ] Duplicate results are deduplicated

Accessibility:
- [ ] Keyboard navigation (arrow keys, enter)
- [ ] Screen reader announces result count
- [ ] Focus management (stays in search box while typing)
```

---

## Summary: The Acceptance Criteria Formula

```
For every story:

1. Happy Path (what success looks like)
2. Edge Cases (boundaries, unusual inputs)
3. Error States (what happens when things fail)
4. Performance (speed, scale requirements)
5. Accessibility (keyboard, screen reader, WCAG)

Each criterion must be:
- Testable (can verify yes/no)
- Specific (no ambiguity)
- Outcome-focused (what, not how)
```

**Remember**: If you can't test it, it's not good acceptance criteria.
