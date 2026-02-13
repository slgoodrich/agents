# Specification Best Practices

Comprehensive guide to writing clear, effective product specifications that enable teams to build the right thing.

---

## Table of Contents

1. [Core Principles](#core-principles)
2. [Structure and Organization](#structure-and-organization)
3. [Writing Style and Clarity](#writing-style-and-clarity)
4. [Collaboration and Communication](#collaboration-and-communication)
5. [Progressive Elaboration](#progressive-elaboration)
6. [Visual Aids and Examples](#visual-aids-and-examples)
7. [Testing and Validation](#testing-and-validation)
8. [Maintenance and Updates](#maintenance-and-updates)
9. [Tools and Templates](#tools-and-templates)
10. [Quality Checklist](#quality-checklist)

---

## Core Principles

### Principle 1: Start with Why

**The Problem:** Specifications that jump to "what" without explaining "why" lead to misaligned solutions.

**Best Practice:** Always begin with problem statement and user needs.

**Template:**

```
Problem: [What problem exists today?]
Impact: [Who is affected and how?]
Evidence: [Data, research, user quotes]
Goal: [What would success look like?]
Non-Goals: [What are we explicitly not doing?]
```

**Example - Good:**

```
Problem: New users abandon signup flow before completing profile

Impact:
- 60% of users who start signup don't complete it
- We lose ~300 potential users/month
- Can't personalize experience without profile data
- Reduces trial-to-paid conversion by 40%

Evidence:
- Funnel analytics show 60% drop-off at profile step
- User interviews (15 participants): "Too many questions upfront"
- Competitor analysis: Top 3 competitors ask 2-3 questions max
- User quote: "I just wanted to try the app, not fill out a form"

Goal:
- Increase signup completion from 40% to 70%
- Collect essential data while reducing friction
- Get users to "aha moment" faster (within 2 minutes)

Non-Goals:
- Collecting detailed demographic data (move to post-signup)
- Integration with social media (future consideration)
- Email verification during signup (async after signup)
```

**Example - Bad:**

```
"Add a simplified signup form"
```

---

### Principle 2: Focus on Outcomes, Not Outputs

**The Problem:** Teams build requested features (outputs) that don't achieve desired results (outcomes).

**Best Practice:** Define success metrics and outcomes, not just deliverables.

**Output-Focused (Bad):**

```
Deliverable: Build email notification system
```

**Outcome-Focused (Good):**

```
Desired Outcome:
- Reduce missed critical alerts from 40% to <15%
- Increase trial activation rate from 12% to 20%
- Decrease support tickets about "didn't know" issues by 30%

Success Metrics:
- 60% of users opt into email notifications
- Email open rate >30%
- Time-to-action on critical alerts <2 hours (down from 8 hours)
- User satisfaction with notifications >4/5

Deliverable: Email notification system that achieves these outcomes

We'll iterate on the feature until outcomes are met, not just when feature ships.
```

---

### Principle 3: Make It Testable

**The Problem:** Ambiguous specifications can't be verified, leading to disagreements about "done."

**Best Practice:** Every requirement should have objective pass/fail criteria.

**Not Testable:**

```
- System should be fast
- UI should look good
- Code should be maintainable
```

**Testable:**

```
- Page load time <2 seconds (p95), measured via Lighthouse
- Lighthouse accessibility score >90, verified in CI
- Code coverage >80%, cyclomatic complexity <10 per function
```

**Testability Checklist:**

- [ ] Can write automated test for this
- [ ] Has measurable criteria (time, percentage, count)
- [ ] Pass/fail is objective, not subjective
- [ ] QA can create test case from this
- [ ] No ambiguous terms ("good", "fast", "intuitive")

---

### Principle 4: Specify Behavior, Not Implementation

**The Problem:** Over-specifying implementation removes team autonomy and may prescribe suboptimal solutions.

**Best Practice:** Define what system should do (behavior) and constraints, let team decide how.

**Too Prescriptive (Bad):**

```
"Use Material-UI Autocomplete component with custom renderOption function that displays user avatars fetched from /api/users endpoint, store selected users in Redux store using UPDATE_SELECTION action"
```

**Behavioral (Good):**

```
User Selection:

Behavior:
- User can search for other users by name or email
- As user types, matching suggestions appear (typeahead)
- Each suggestion shows user's name, email, and avatar
- User can select one or multiple users (depending on context)
- Selected users are visually distinct
- Selection persists across page refreshes

Performance:
- Suggestions appear within 300ms of typing
- Supports searching across 10,000+ users without performance degradation

Accessibility:
- Keyboard navigable (arrow keys, Enter to select, Esc to close)
- Screen reader announces suggestions and selections

Let engineering decide: component library, API design, state management, caching strategy
```

---

### Principle 5: Cover Happy and Unhappy Paths

**The Problem:** Specs that only cover happy paths leave edge cases undefined, leading to inconsistent behavior.

**Best Practice:** Document expected behavior for success cases, error cases, and edge cases.

**Only Happy Path (Incomplete):**

```
User can upload a file
```

**Complete (Happy + Unhappy Paths):**

```
File Upload:

Happy Path:
- User selects file <10MB, supported format (JPG, PNG, PDF)
- Upload progress bar shows percentage
- On completion: File appears in list, success message shown

Unhappy Path 1: File Too Large
- User selects file >10MB
- Before upload starts: Error "File exceeds 10MB limit"
- User can select different file

Unhappy Path 2: Unsupported Format
- User selects .exe file
- Before upload starts: Error "Only JPG, PNG, PDF files allowed"
- User can select different file

Unhappy Path 3: Network Failure Mid-Upload
- Upload starts, then network drops
- System retries 3 times (exponential backoff)
- If still fails: "Upload failed. Check your connection and try again."
- User can retry without re-selecting file
- Partial upload is cleaned up

Unhappy Path 4: Server Error
- Upload completes, but server fails to process
- User sees: "Upload failed. We've been notified. Please try again later."
- Error logged with file metadata for debugging

Edge Cases:
- Duplicate filename: Append " (2)" to avoid overwrite
- Zero-byte file: Error "File is empty"
- Corrupted file: Error "File appears to be corrupted"
- Simultaneous uploads: Queue, process sequentially
```

---

## Structure and Organization

### Best Practice 1: Hierarchical Organization

**Structure specs from high-level to detailed:**

```
1. Executive Summary (2-3 sentences)
   └─ Problem, solution, impact

2. Context (1 paragraph)
   └─ Background, why now, business value

3. Goals and Success Metrics (bullet list)
   └─ What we're trying to achieve

4. User Stories/Requirements (grouped by theme)
   └─ Detailed functional requirements

5. Non-Functional Requirements
   └─ Performance, security, accessibility

6. Technical Considerations
   └─ Dependencies, constraints, risks

7. Open Questions
   └─ What needs resolution
```

**Example:**

```markdown
# Feature: Email Notifications

## Executive Summary

Enable email notifications for critical events (payment failures, expiring trials) to reduce missed alerts from 40% to <15% and increase trial activation from 12% to 20%.

## Context

Users currently miss important events when not actively using the app. Analytics show 60% of trial users miss activation deadline, and 25% miss payment failures. This leads to service interruptions and lost trial conversions. Competitors all offer email notifications as standard feature.

## Goals and Success Metrics

- Reduce missed critical alerts from 40% to <15%
- Increase trial activation rate from 12% to 20%
- 60% opt-in rate for email notifications
- <2% unsubscribe rate
- Email open rate >30%

## User Stories

### US-1: Receive Critical Event Notifications

[Details...]

### US-2: Configure Notification Preferences

[Details...]

## Non-Functional Requirements

### Performance

- Emails sent within 5 minutes of event
  [...]

## Technical Considerations

### Dependencies

- SendGrid API for email delivery
  [...]

## Open Questions

1. Should we support SMS notifications? → Defer to v2
   [...]
```

---

### Best Practice 2: Progressive Disclosure

**Start broad, provide detail on demand:**

```
Level 1: One-liner (anyone can understand)
"Enable email notifications to reduce missed critical alerts"

Level 2: Summary (product/business folks)
- Problem: 60% miss critical alerts
- Solution: Email notifications
- Impact: 40% → 15% missed alerts

Level 3: Detailed Requirements (engineering/QA)
- Complete user stories with acceptance criteria
- Technical specifications
- Edge cases and error handling

Level 4: Implementation Details (engineering only)
- API endpoints
- Database schema
- Integration specifics
```

**In Practice:**

```markdown
# Email Notifications

Quick Summary: Enable email notifications for critical events to keep users informed.

<details>
<summary>Full Context (click to expand)</summary>

## Problem

Users miss critical events when not in app:

- 60% miss trial expiration
- 25% miss payment failures
[Full problem statement...]
</details>

<details>
<summary>Technical Details (click to expand)</summary>

## API Integration

[Technical implementation details...]

</details>
```

---

### Best Practice 3: Group Related Requirements

**Group by:**

- User persona
- User journey stage
- Feature theme
- Priority tier

**Example by Persona:**

```markdown
## Admin User Stories

### Story 1: Manage Team Members

As an admin, I want to add/remove team members...

### Story 2: View Audit Logs

As an admin, I want to see who did what...

## End User Stories

### Story 3: Complete Profile

As an end user, I want to fill out my profile...

### Story 4: Customize Settings

As an end user, I want to customize my preferences...
```

**Example by Priority:**

```markdown
## Must Have (P0) - Blocking Launch

### User can log in with email/password

[Requirements...]

### User can reset forgotten password

[Requirements...]

## Should Have (P1) - High Priority Post-Launch

### User can log in with Google OAuth

[Requirements...]

## Nice to Have (P2) - Future Consideration

### User can log in with fingerprint

[Requirements...]
```

---

## Writing Style and Clarity

### Best Practice 1: Use Clear, Concise Language

**Avoid:**

- Technical jargon (unless necessary)
- Overly complex sentences
- Passive voice
- Ambiguous terms

**Good Examples:**

**Before (Unclear):**

```
"The system shall facilitate the ability for users to effectuate modifications to their account credentials through the utilization of the profile management interface"
```

**After (Clear):**

```
"Users can update their email and password in account settings"
```

---

**Before (Ambiguous):**

```
"The page should load quickly and provide a good user experience"
```

**After (Specific):**

```
"The page loads in <2 seconds (p95) and Lighthouse performance score is >90"
```

---

### Best Practice 2: Use Active Voice

**Passive (Bad):**

```
"An email notification will be sent to the user when the payment fails"
```

**Active (Good):**

```
"System sends email notification to user when payment fails"
```

---

**Passive (Bad):**

```
"The form can be submitted by the user after validation is completed"
```

**Active (Good):**

```
"User submits form after validation succeeds"
```

---

### Best Practice 3: Define Domain Terms

**Create glossary for specialized terms:**

```markdown
## Glossary

**Churn**: Percentage of customers who stop using product in a time period

- Monthly churn = Customers lost / Average customers in month

**MAU (Monthly Active Users)**: Unique users who performed any action in last 30 days

**Conversion Rate**: Percentage of trial users who become paid customers

- Calculation: Paid subscriptions / Trial signups

**P95 (95th Percentile)**: 95% of requests complete faster than this time

- Example: P95 < 2s means 95% of page loads take under 2 seconds
```

---

### Best Practice 4: Use Consistent Terminology

**Bad (Inconsistent):**

```
- User logs in (Story 1)
- Customer authenticates (Story 2)
- Person signs in (Story 3)
```

**Good (Consistent):**

```
- User logs in (everywhere)
```

**Create terminology guide:**

```markdown
## Terminology Standards

| Use       | Don't Use                 | Rationale                |
| --------- | ------------------------- | ------------------------ |
| User      | Customer, Person, Account | Consistent with codebase |
| Log in    | Sign in, Authenticate     | Matches UI labels        |
| Dashboard | Home, Main Page           | Established product term |
```

---

## Collaboration and Communication

### Best Practice 1: Involve Team Early

**When to Involve Team members:**

**Discovery Phase (Before Writing Specs):**

- **Product + Engineering:** Technical feasibility
- **Product + Design:** User experience approach
- **Product + Business:** Business value, constraints

**Specification Phase (While Writing):**

- **Engineering Lead:** Review for technical clarity, missing details
- **Design:** UI/UX alignment
- **QA:** Testability, edge cases

**Review Phase (Before Development):**

- **Full Team:** Final walkthrough
- **Team members:** Sign-off on scope and success criteria

---

### Best Practice 2: Use Spike Stories for Unknowns

**When specs have unknowns, create timeboxed research:**

```markdown
# Spike: Search Performance Investigation

## Goal

Determine best approach to reduce search time from 8 seconds to <2 seconds

## Questions to Answer

1. Where is the bottleneck? (Database query? Network? Rendering?)
2. Would Elasticsearch provide significant improvement?
3. Can we optimize current PostgreSQL queries?
4. What's the cost/effort trade-off for each approach?

## Activities

- Profile current search implementation
- Benchmark database queries
- Prototype Elasticsearch integration
- Compare performance of each approach

## Timebox

3 days maximum

## Output

- Performance analysis document
- Recommendation with pros/cons
- Effort estimates for each option
- Follow-up stories for chosen approach
```

---

### Best Practice 3: Document Decisions

**Use Architecture Decision Records (ADRs) for significant choices:**

```markdown
# ADR-015: Use SendGrid for Email Notifications

## Status

Accepted

## Context

Need to send transactional emails (notifications, password resets).
Evaluated 3 options: SendGrid, AWS SES, Mailgun.

## Decision

Use SendGrid

## Rationale

- Best deliverability rates (99.7% vs 97% for SES)
- Excellent email analytics dashboard
- Better webhook support for tracking bounces/opens
- Team has prior experience with SendGrid
- Cost: $15/month for our volume (others similar)

## Consequences

### Positive

- Higher deliverability = more users receive notifications
- Good analytics for monitoring email performance
- Known quantity, faster implementation

### Negative

- Vendor lock-in (but email providers are interchangeable)
- Slightly more expensive than AWS SES ($15/mo vs $10/mo)

## Alternatives Considered

- AWS SES: Lower cost but worse deliverability
- Mailgun: Similar features but no team experience
```

---

## Progressive Elaboration

### Best Practice: Just-in-Time Details

**Don't write everything upfront. Elaborate details when needed:**

**Phase 1: Epic (High-Level)**

```
Epic: Email Notifications
Enable email notifications for critical events

Business Value: Reduce missed alerts, increase activation
Target: Q2 2024
Estimated Size: 3-4 sprints
```

**Phase 2: User Stories (Before Sprint Planning)**

```
Story 1: Send payment failure notifications
Story 2: Send trial expiration notifications
Story 3: User can configure preferences
Story 4: User can unsubscribe
[Each story is 1-liner at this point]
```

**Phase 3: Detailed Stories (During Backlog Refinement, 1-2 weeks before sprint)**

```
Story 1: Send payment failure notifications

Full user story format with:
- Detailed "as a, I want, so that"
- Acceptance criteria (happy + unhappy paths)
- Open questions resolved
- Designs attached
- Estimated at 5 points
```

**Phase 4: Implementation Details (During Development)**

```
Technical questions arise:
- Which email template library?
- How to handle rate limiting?

These are answered during development, not upfront.
```

---

## Visual Aids and Examples

### Best Practice 1: Use Diagrams

**Types of Diagrams to Include:**

**1. User Flow Diagrams**

```
[Login Page] → [Enter Credentials] → [Valid?]
                                        ├─ Yes → [Dashboard]
                                        └─ No → [Error Message] → [Retry or Reset Password]
```

**2. State Diagrams**

```
Order States:
[Draft] → [Submitted] → [Processing] → [Shipped] → [Delivered]
           ↓                              ↓
        [Cancelled]                   [Returned]
```

**3. Data Flow Diagrams**

```
[User] → [Web App] → [API Server] → [Database]
                  ↓
              [Email Service]
```

**4. Wireframes/Mockups**

- Attach Figma links or screenshots
- Annotate key interactions
- Show different states (empty, loading, error, success)

---

### Best Practice 2: Use Concrete Examples

**Instead of:**

```
"System validates input"
```

**Write:**

```
Input Validation Examples:

Valid Inputs:
- Email: user@example.com, name+tag@domain.co.uk
- Phone: (555) 123-4567, 555-123-4567, +1-555-123-4567
- Date: 2024-01-15, 01/15/2024, Jan 15, 2024

Invalid Inputs:
- Email: user@ → "Please include domain"
- Email: user space@example.com → "Email cannot contain spaces"
- Phone: 123 → "Phone must be 10 digits"
- Date: 2024-13-45 → "Invalid date"
```

---

### Best Practice 3: Show Before/After States

**For UI changes, show current and proposed:**

```markdown
## Current State (Before)

User profile page has:

- 12 separate sections
- All expanded by default
- Loads in 8 seconds
- Difficult to find specific info

[Screenshot of current page]

## Proposed State (After)

User profile page will have:

- 5 key sections
- Sections collapsed by default
- Loads in <2 seconds
- Search bar to find info quickly

[Wireframe of proposed page]

## What's Changing

- Consolidate 12 sections → 5 main sections
- Add expand/collapse to each section
- Add search/filter capability
- Lazy-load non-critical data
```

---

## Testing and Validation

### Best Practice 1: Write Testable Acceptance Criteria

**Every criterion should be verifiable:**

```markdown
## Acceptance Criteria

Testable:
✓ Page loads in <2 seconds (p95)
Test: Run Lighthouse 10 times, verify p95 <2s

✓ Form validation shows errors inline
Test: Submit form with invalid email, verify error appears below email field

✓ User receives email within 5 minutes
Test: Trigger notification event, check email delivery time

Not Testable:
✗ Page loads quickly
(How quickly? How to measure?)

✗ UI looks good
(Good by what standard? Subjective)

✗ System is secure
(Too vague, many interpretations)
```

---

### Best Practice 2: Include Test Scenarios

**Provide specific test cases for QA:**

```markdown
## Test Scenarios

### Test Case 1: Successful Login

**Setup:**

- User account exists: user@example.com / Password123!
- User is not currently logged in

**Steps:**

1. Navigate to /login
2. Enter email: user@example.com
3. Enter password: Password123!
4. Click "Login" button

**Expected Result:**

- Redirected to /dashboard within 2 seconds
- Welcome message shows: "Welcome back, [User Name]"
- Navigation shows user avatar
- Can access protected pages

**Pass Criteria:** All steps succeed without errors

---

### Test Case 2: Login with Wrong Password

**Setup:**

- User account exists: user@example.com / Password123!

**Steps:**

1. Navigate to /login
2. Enter email: user@example.com
3. Enter password: WrongPassword123!
4. Click "Login" button

**Expected Result:**

- Stay on /login page
- Error message shows: "Invalid email or password"
- Password field is cleared
- Email field retains "user@example.com"
- No session created
- Attempt logged for security monitoring

**Pass Criteria:** All expected results occur
```

---

### Best Practice 3: Define Edge Cases Explicitly

**Document behavior for edge cases:**

```markdown
## Edge Case Handling

### Edge Case 1: Duplicate Email Registration

**Scenario:** User tries to register with email that already exists

**Behavior:**

- Show error: "This email is already registered"
- Provide link: "Log in instead" or "Reset password"
- Do NOT reveal that email exists (security)
- Log attempt for monitoring

**Test:** Try to register with existing email, verify error shown

---

### Edge Case 2: Session Expires During Form Entry

**Scenario:** User fills out long form, session expires (30 min), then submits

**Behavior:**

- Show message: "Your session expired. Please log in again."
- Preserve form data (don't lose work)
- After re-login, return to form with data intact
- User can complete submission

**Test:** Fill form, wait 31 minutes, submit, verify data preserved after re-login

---

### Edge Case 3: Network Interruption Mid-Upload

**Scenario:** User uploads file, network drops during upload

**Behavior:**

- Detect network failure
- Pause upload progress bar
- Show message: "Connection lost. Retrying..."
- Retry 3 times (exponential backoff: 1s, 2s, 4s)
- If still fails: "Upload failed. Check connection and try again."
- User can click "Retry" without re-selecting file
- Cleanup partial upload on server

**Test:** Upload file, kill network mid-upload, verify retry behavior
```

---

## Maintenance and Updates

### Best Practice 1: Version Control Specs

**Track changes to specifications:**

```markdown
## Version History

| Version | Date       | Author     | Changes                                  |
| ------- | ---------- | ---------- | ---------------------------------------- |
| 1.0     | 2024-01-15 | Jane Smith | Initial specification                    |
| 1.1     | 2024-01-22 | Jane Smith | Added OAuth login (Story 4)              |
| 1.2     | 2024-02-01 | John Doe   | Updated success metrics based on Q1 data |
| 2.0     | 2024-03-15 | Jane Smith | Major revision: Added multi-factor auth  |
```

---

### Best Practice 2: Keep Specs Updated

**Don't let specs drift from reality:**

**During Development:**

- Update specs when requirements change
- Document decisions made during implementation
- Note deviations from original plan

**After Launch:**

- Update with actual metrics
- Add lessons learned
- Document what worked/didn't work

**Example:**

```markdown
## Post-Launch Updates

**Actual Results (3 months post-launch):**

- Missed alerts: Reduced from 40% → 12% (✓ exceeded goal of 15%)
- Trial activation: Increased from 12% → 18% (✗ missed goal of 20%)
- Opt-in rate: 55% (✗ missed goal of 60%)
- Unsubscribe rate: 1.2% (✓ better than goal of 2%)
- Open rate: 34% (✓ exceeded goal of 30%)

**Learnings:**

- Email notifications very effective for reducing missed alerts
- Trial activation improved but need additional interventions
- Opt-in rate lower than expected; consider default opt-in for critical notifications
- Users love the notification control (positive feedback in surveys)

**Follow-Up Items:**

- Experiment with default opt-in for critical notifications
- Add in-app reminders in addition to email (to hit 20% activation goal)
- Add SMS backup for critical alerts (requested by enterprise customers)
```

---

### Best Practice 3: Archive Completed Specs

**Organize specs by status:**

```
/specs/active/          (Currently being built)
  - email-notifications.md
  - user-roles.md

/specs/shipped/         (Completed features)
  - 2024-Q1/
    - onboarding-v2.md
    - search-improvements.md
  - 2024-Q2/
    - email-notifications.md

/specs/archived/        (Cancelled or obsolete)
  - abandoned-social-feed.md
  - deprecated-old-dashboard.md
```

---

## Tools and Templates

### Recommended Tools

**Documentation:**

- **Notion:** Great for collaborative specs with comments
- **Confluence:** Enterprise knowledge base
- **Google Docs:** Simple, widely accessible
- **Markdown + GitHub:** Version control, great for technical teams

**Diagramming:**

- **Miro / FigJam:** User flows, brainstorming
- **Lucidchart:** Technical diagrams
- **Mermaid:** Diagrams as code (in markdown)
- **Draw.io:** Free, powerful diagramming

**Design:**

- **Figma:** Industry standard for mockups/prototypes
- **Balsamiq:** Quick wireframes
- **Whimsical:** Fast flowcharts and wireframes

**Project Management:**

- **Jira:** Issue tracking, story management
- **Linear:** Modern, fast issue tracking
- **Asana / Monday:** Project management

---

### Template Library

**Available Templates:**

- `assets/prd-structure-template.md` - Full PRD structure
- `assets/user-story-template.md` - User story format with INVEST
- `assets/job-story-template.md` - Jobs-to-be-Done format
- `assets/use-case-template.md` - Detailed use case structure
- `assets/edge-case-checklist.md` - Comprehensive edge case coverage
- `assets/non-functional-requirements-template.md` - NFR documentation

---

## Quality Checklist

### Before Finalizing Specification

**Completeness:**

- [ ] Problem statement clearly defined
- [ ] User needs and goals documented
- [ ] Success metrics specified
- [ ] All user stories have acceptance criteria
- [ ] Non-functional requirements included
- [ ] Edge cases covered
- [ ] Dependencies identified
- [ ] Risks documented

**Clarity:**

- [ ] No ambiguous terms ("fast", "good", "intuitive")
- [ ] Domain terms defined
- [ ] Examples provided for complex requirements
- [ ] Visual aids included where helpful
- [ ] Consistent terminology throughout

**Testability:**

- [ ] Every requirement is verifiable
- [ ] Acceptance criteria are specific
- [ ] Test scenarios provided for QA
- [ ] Success metrics are measurable

**Collaboration:**

- [ ] Reviewed by engineering lead
- [ ] Reviewed by design (if UI changes)
- [ ] Reviewed by QA
- [ ] Open questions resolved
- [ ] Decision checkpoint obtained

**Scope Management:**

- [ ] Clear boundaries (in-scope / out-of-scope)
- [ ] Non-goals explicitly stated
- [ ] Priority levels assigned (P0, P1, P2)
- [ ] MVP clearly defined

**Flexibility:**

- [ ] Specifies "what", not "how" (where appropriate)
- [ ] Constraints documented but implementation flexible
- [ ] Room for team creativity and technical decisions

---

## Summary

**Great Specifications:**

1. **Start with Why**
   - Clear problem statement
   - User needs and business goals
   - Success metrics defined

2. **Be Specific and Testable**
   - No ambiguous terms
   - Measurable criteria
   - Concrete examples

3. **Cover All Scenarios**
   - Happy paths
   - Unhappy paths (errors)
   - Edge cases

4. **Balance Detail and Flexibility**
   - Specify behavior and constraints
   - Leave implementation to team
   - Progressive elaboration

5. **Use Visual Aids**
   - Diagrams and flows
   - Wireframes/mockups
   - Before/after comparisons

6. **Collaborate Early**
   - Involve team in discovery
   - Review with the team
   - Document decisions

7. **Keep Updated**
   - Track changes
   - Update with learnings
   - Archive when complete

**Remember:** The best specification creates shared understanding. The document is less important than the conversations it enables.
