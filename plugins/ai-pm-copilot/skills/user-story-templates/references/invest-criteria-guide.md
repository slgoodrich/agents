# INVEST Criteria Guide

Deep dive into the INVEST principles for writing high-quality user stories.

## Table of Contents

- [What is INVEST?](#what-is-invest)
- [I - Independent](#i---independent)
- [N - Negotiable](#n---negotiable)
- [V - Valuable](#v---valuable)
- [E - Estimable](#e---estimable)
- [S - Small](#s---small)
- [T - Testable](#t---testable)
- [INVEST Checklist for Every Story](#invest-checklist-for-every-story)
- [When Stories Don't Meet INVEST](#when-stories-dont-meet-invest)
- [Summary: INVEST in Action](#summary-invest-in-action)

---

## What is INVEST?

**INVEST** is a mnemonic for six qualities of good user stories, coined by Bill Wake in 2003.

**I**ndependent
**N**egotiable
**V**aluable
**E**stimable
**S**mall
**T**estable

Good stories meet all six criteria. If a story fails INVEST, it should be rewritten or split.

---

## I - Independent

### Definition

Story can be developed and delivered without dependency on other stories.

### Why It Matters

- **Flexibility**: Reorder backlog based on priority
- **Parallel work**: Multiple developers work simultaneously
- **Reduced risk**: One story's delay doesn't block others
- **Easier planning**: Don't need to coordinate dependent stories in same sprint

### Anti-Pattern: Dependent Stories

❌ **Bad** (tightly coupled):

```
Story 1: Build user database schema
Story 2: Create user API endpoints
Story 3: Build user registration form
```

**Problems**:

- Must complete in exact order
- Can't parallelize work
- Later stories blocked if earlier ones are delayed
- Hard to estimate (unknowns cascade)

**Good** (independent):

```
Story 1: User can register with email/password (full vertical slice: DB + API + UI)
Story 2: User can log in with email/password
Story 3: User can reset password via email
```

Each story goes through all layers (UI → API → DB) and delivers standalone value.

---

### When Dependencies Are Unavoidable

Sometimes dependencies are necessary:

**Example**: OAuth Integration

```
Story 1: User can log in with Google OAuth
Story 2: User can link existing account to Google OAuth
```

Story 2 depends on Story 1 (can't link to Google if Google login doesn't exist).

**How to handle**:

1. **Acknowledge dependency** explicitly
2. **Schedule dependent story later** (different sprint)
3. **Minimize dependencies** where possible
4. **Document in story**: "Depends on: Story 1 (Google OAuth)"

---

### Independence Checklist

- [ ] Can this story be developed without waiting for other stories?
- [ ] If dependencies exist, are they minimal and clearly documented?
- [ ] Can stories be reordered without breaking dependencies?
- [ ] Can this story be demonstrated independently?

---

## N - Negotiable

### Definition

Details of the story are flexible and can be discussed, not fixed contracts.

### Why It Matters

- **Collaboration**: Developers can suggest better approaches
- **Creativity**: Team can find optimal solution
- **Adaptability**: Can adjust as we learn
- **Ownership**: Team feels empowered, not just following orders

### Anti-Pattern: Over-Specification

❌ **Bad** (too prescriptive):

```
As a user
I want a "Forgot Password" link in blue (#0066CC) below the login form using Helvetica 14pt font
So that I can reset my password

Requirements:
- Use React useState hook for form state
- Call POST /api/auth/reset-password endpoint
- Store token in localStorage
- Use bcrypt with 12 rounds for hashing
- Email template must use SendGrid API
```

**Problems**:

- Dictates implementation (removes developer autonomy)
- Prevents better solutions (what if hooks aren't best approach?)
- Brittle (what if design changes?)
- Misses the "why" (solving problem vs following instructions)

**Good** (negotiable):

```
As a user
I want to reset my password if I forget it
So that I can regain access to my account

Acceptance Criteria:
- [ ] User receives reset email within 2 minutes
- [ ] Reset link expires after 24 hours
- [ ] New password meets security requirements (8+ chars, 1 number, 1 special char)
- [ ] User is logged in after successful reset
- [ ] Old password is immediately invalidated

Notes:
- Consider: How should UI look? (collaborate with design)
- Consider: Which email service? (tech team to decide)
- Consider: Password hashing strategy (security best practices)
```

**What's negotiable**: UI design, technology choices, implementation details

**What's fixed**: User outcome, security requirements, acceptance criteria

---

### Balancing Negotiable with Clear Requirements

**Negotiable ≠ Vague**

Provide enough detail to guide, but leave room for creativity:

**Too vague**: "Make search better"
**Too prescriptive**: "Use Elasticsearch with these exact mappings..."
**Just right**: "Search should return results in <500ms for 10K records. Consider options."

---

### Negotiable Checklist

- [ ] Story defines outcome, not implementation?
- [ ] Team can suggest better approaches?
- [ ] Details can be refined during development?
- [ ] Acceptance criteria focus on "what", not "how"?

---

## V - Valuable

### Definition

Story delivers clear value to user or business.

### Why It Matters

- **Prioritization**: Easy to rank by value
- **Motivation**: Team understands why they're building it
- **Scope management**: Low-value features can be cut
- **ROI**: Ensures we're building things that matter

### Anti-Pattern: No Clear Value

❌ **Bad** (no clear value):

```
As a developer
I want to refactor the authentication module
So that the code is cleaner
```

**Problems**:

- Who benefits? (developer, not user)
- What's the business value? (unclear)
- Why prioritize this? (can't compare to user features)

**Better** (clear value):

```
As a developer
I want to refactor the authentication module
So that we can add OAuth support without rewriting everything

Business Value:
- Enables OAuth (top user request)
- Reduces future auth feature development time by ~40%
- Improves testability (reduces auth bug risk)
```

**Even better** (user-facing value):

```
As a user
I want to log in with Google
So that I don't need to remember another password

Technical enabler: Requires auth module refactoring (separate story)
```

---

### Types of Value

**1. Direct User Value**
Solves user problem, enables user capability

```
As a user, I want to export data as CSV
So that I can analyze it in Excel
```

**2. Business Value**
Increases revenue, reduces costs, improves efficiency

```
As a business, we want to reduce page load time from 5s to 2s
So that we reduce bounce rate and increase conversions
```

**3. Compliance/Risk Value**
Meets legal requirements, reduces risk

```
As a business, we want GDPR-compliant data deletion
So that we comply with EU regulations and avoid fines
```

**4. Enabler Value**
Doesn't directly deliver value but enables future value

```
As a team, we want CI/CD pipeline
So that we can deploy features 10x faster
```

**All are valid**, but should be explicit about type of value.

---

### Valuable Checklist

- [ ] Clear who benefits (user, business, team)?
- [ ] Clear what the benefit is?
- [ ] Benefit is meaningful (not trivial)?
- [ ] Can articulate ROI or impact?
- [ ] Story could be prioritized based on value?

---

## E - Estimable

### Definition

Team can estimate the effort required with reasonable confidence.

### Why It Matters

- **Planning**: Can commit to sprint goals
- **Prioritization**: Compare effort vs value
- **Risk management**: Identify high-uncertainty stories
- **Velocity tracking**: Consistent estimates enable predictability

### Anti-Pattern: Too Vague to Estimate

❌ **Bad** (not estimable):

```
As a user
I want better performance
So that the app is faster
```

**Problems**:

- What does "better" mean? (2x faster? 10x faster?)
- Where? (which page? which operation?)
- How much effort? (completely unknowable)

**Good** (estimable):

```
As a user
I want the dashboard to load in under 2 seconds
So that I can quickly see my metrics

Acceptance Criteria:
- [ ] Dashboard loads in <2s (p95) for datasets up to 10K records
- [ ] Current baseline: 5-7 seconds
- [ ] Proposed approach: Query optimization + caching

Notes:
- Spike completed: 2 days effort for optimization + 1 day for caching
- Risks: May need database indexes (requires DBA approval)
```

**Team can estimate** because:

- Clear scope (dashboard only)
- Measurable target (2 seconds)
- Proposed approach (optimization + caching)
- Risk identified (DBA dependency)

---

### Factors That Make Stories Hard to Estimate

**1. Unclear Scope**

- "Improve user experience" → Vague
- "Reduce checkout clicks from 5 to 3" → Clear

**2. Unknown Technologies**

- "Integrate with [never-used-before service]" → Hard
- "Add field to existing form" → Easy

**3. Missing Information**

- "User can upload files" → What types? Size limits? Validation?
- "User can upload JPG/PNG up to 10MB" → Clear

**4. Large Size**

- "Build entire notification system" → Too big
- "In-app notifications for @mentions" → Right-sized

**5. External Dependencies**

- "Integrate with third-party API" → What if API is down? Changes?
- "Use existing internal service" → More predictable

---

### Making Stories Estimable

**Strategy 1: Add Details**

```
Before: "User can search"
After: "User can search products by keyword, returning results in <500ms for 10K products"
```

**Strategy 2: Spike Unknown Complexity**

```
Story 1 (Spike): Research real-time notification solutions (2 days)
Story 2 (Implementation): Implement real-time notifications using [chosen approach]
```

**Strategy 3: Split Large Stories**

```
Before: "Build checkout system" (too big)
After:
- "User enters shipping address"
- "User selects shipping method"
- "User enters payment info"
```

**Strategy 4: Reference Examples**

```
"This is similar to the export feature we built last month (that was 5 points)"
```

---

### Estimable Checklist

- [ ] Team understands what needs to be built?
- [ ] Scope is clear (not vague)?
- [ ] No unknown technologies (or spike planned)?
- [ ] Story is small enough (<5 days)?
- [ ] External dependencies are identified?

---

## S - Small

### Definition

Story can be completed in one sprint (ideally 1-3 days).

### Why It Matters

- **Predictability**: Easier to estimate small things accurately
- **Faster feedback**: Ship and learn quickly
- **Reduced risk**: Less can go wrong
- **Better flow**: Don't block other work
- **Easier testing**: Less surface area to test

### Anti-Pattern: Epic-Sized Stories

❌ **Bad** (too large):

```
As a user
I want a complete project management system
So that I can manage all my projects
```

**Problems**:

- Too big for one sprint (maybe not even one quarter)
- Hard to estimate
- Blocks other work
- Delays feedback
- High risk

**Good** (small, incremental):

```
Story 1: As a user, I want to create a project with name and description
Story 2: As a user, I want to add tasks to my project
Story 3: As a user, I want to mark tasks as complete
Story 4: As a user, I want to assign tasks to team members
Story 5: As a user, I want to see project progress (% complete)
```

Each story is 1-3 days, delivers value, enables next story.

---

### How Small is Small Enough?

**Guidelines**:

**Ideal**: 1-3 days (2-5 story points)

- Fits comfortably in sprint
- Low risk
- Easy to estimate

**Acceptable**: 3-5 days (5-8 story points)

- Fits in sprint with buffer
- Moderate risk
- Consider splitting if possible

**Too large**: >5 days (>8 points)

- Won't fit in sprint
- High risk
- Must split

**Too small**: <4 hours (<1 point)

- Overhead of story management exceeds value
- Consider combining with other small stories
- Exception: Critical bug fixes can be very small

---

### Story Splitting Techniques

See `story-splitting-guide.md` for comprehensive patterns. Quick summary:

1. **Workflow steps**: Wizard pages, multi-step processes
2. **CRUD operations**: Create → Read → Update → Delete
3. **User roles**: Admin → Manager → User
4. **Simple → Complex**: MVP → Advanced features
5. **Happy path → Edge cases**: Success scenarios → Error handling

---

### Small Checklist

- [ ] Can be completed in 1-3 days?
- [ ] Fits in single sprint?
- [ ] Can be demonstrated at sprint review?
- [ ] If >5 days, have you tried splitting?

---

## T - Testable

### Definition

Clear acceptance criteria that can be verified objectively.

### Why It Matters

- **Quality**: Know when story is truly done
- **Validation**: Confirm it works as expected
- **Acceptance**: Product owner can verify
- **Automation**: Can write automated tests
- **Prevents bugs**: Catches issues before production

### Anti-Pattern: Untestable Criteria

❌ **Bad** (not testable):

```
As a user
I want an intuitive interface
So that it's easy to use

Acceptance Criteria:
- UI is clean and modern
- User experience is smooth
- Design looks professional
- Performance is good
```

**Problems**:

- Subjective (what's "clean"? "professional"?)
- Not measurable
- Can't verify objectively
- QA can't write tests

**Good** (testable):

```
As a user
I want a simplified checkout flow
So that I can complete purchase quickly

Acceptance Criteria:
- [ ] Checkout completes in maximum 3 clicks (cart → shipping → payment → done)
- [ ] All form fields have clear labels
- [ ] Error messages appear inline next to invalid fields
- [ ] Page loads in <2 seconds (p95)
- [ ] Mobile responsive (tested on iOS and Android)
- [ ] Passes WCAG AA accessibility standards
- [ ] 80% of test users complete checkout without help (usability test, n=10)
```

**Each criterion** has clear pass/fail test.

---

### Making Stories Testable

**Strategy 1: Use Numbers**

```
Vague: "Fast page load"
Testable: "Page loads in <2 seconds (p95 latency)"
```

**Strategy 2: Use Examples**

```
Vague: "Validation works"
Testable: "Email validation rejects 'notanemail' and accepts 'user@example.com'"
```

**Strategy 3: Define Success Clearly**

```
Vague: "Search is relevant"
Testable: "Exact matches appear before partial matches"
```

**Strategy 4: Reference Standards**

```
Vague: "Accessible"
Testable: "Meets WCAG 2.1 AA standards (verified with axe DevTools)"
```

**Strategy 5: Use Observable Outcomes**

```
Vague: "Data is saved"
Testable: "Closing and reopening shows previously entered data"
```

---

### Types of Testing Criteria Should Enable

Good acceptance criteria enable multiple test types:

**Manual Testing**:

```
- [ ] Clicking "Submit" with empty form shows "Name is required" error
```

**Automated Testing**:

```
- [ ] API returns 400 with error message for invalid email format
```

**Performance Testing**:

```
- [ ] Search completes in <500ms for 10K records (measured via k6 load test)
```

**Accessibility Testing**:

```
- [ ] All interactive elements accessible via keyboard only (no mouse)
- [ ] Screen reader announces form errors
```

**Usability Testing**:

```
- [ ] 80% of users complete task without help (n=10 usability tests)
```

---

### Testable Checklist

- [ ] Each acceptance criterion has clear pass/fail test?
- [ ] QA can write test cases from criteria?
- [ ] Product owner can verify completion?
- [ ] Criteria are objective (not subjective)?
- [ ] Can be tested without interpretation?

---

## INVEST Checklist for Every Story

Before finalizing a story, verify it meets INVEST:

### Independent

- [ ] Can be developed without waiting for other stories
- [ ] Dependencies are minimal and documented
- [ ] Can be reordered in backlog

### Negotiable

- [ ] Focuses on outcome, not implementation
- [ ] Team can suggest better approaches
- [ ] Details can be refined during development

### Valuable

- [ ] Clear benefit to user or business
- [ ] Can articulate ROI or impact
- [ ] Worth prioritizing

### Estimable

- [ ] Team can estimate effort confidently
- [ ] Scope is clear
- [ ] No major unknowns (or spike planned)

### Small

- [ ] Fits in one sprint (1-5 days)
- [ ] If >5 days, can it be split?
- [ ] Can be demonstrated at sprint review

### Testable

- [ ] Clear acceptance criteria
- [ ] Criteria are objective and verifiable
- [ ] QA can write tests
- [ ] Product owner can confirm completion

---

## When Stories Don't Meet INVEST

**If a story fails INVEST**, don't force it into the backlog. Fix it first:

**Not Independent?** → Combine with dependent story OR add dependency note and sequence carefully

**Not Negotiable?** → Remove implementation details, focus on outcome

**Not Valuable?** → Reconsider if story is needed OR articulate value clearly

**Not Estimable?** → Add details OR create spike to gather information

**Not Small?** → Split using patterns from `story-splitting-guide.md`

**Not Testable?** → Rewrite acceptance criteria with measurable outcomes

---

## Summary: INVEST in Action

```
Bad Story:
As a user I want better search.

INVEST Analysis:
❌ Independent: Maybe (not clear)
❌ Negotiable: Too vague to negotiate
❌ Valuable: Unclear what value this provides
❌ Estimable: Can't estimate "better"
❌ Small: Unknown scope, could be huge
❌ Testable: How do you test "better"?

Fixed Story:
As a user
I want search results to appear in under 500ms
So that I can find products quickly without waiting

Acceptance Criteria:
- [ ] Search returns results in <500ms for datasets up to 10K products
- [ ] Results update as user types (debounced 300ms)
- [ ] Search covers product name, description, SKU
- [ ] No results message appears when query returns 0 items
- [ ] Search tested with 100 simultaneous users (load test)

INVEST Analysis:
✓ Independent: Can build and test standalone
✓ Negotiable: Implementation approach flexible, outcome clear
✓ Valuable: Faster search = better UX = higher conversion
✓ Estimable: Clear scope, team estimates 3 days
✓ Small: 3 days = fits in sprint
✓ Testable: Performance targets measurable, criteria clear
```

**Remember**: INVEST is a quality filter. Stories that pass INVEST are easier to build, test, and deliver.
