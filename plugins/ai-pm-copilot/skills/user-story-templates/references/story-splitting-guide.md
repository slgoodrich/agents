# Story Splitting Guide

Comprehensive guide to splitting large user stories into smaller, manageable pieces.

## Table of Contents

- [Why Split Stories?](#why-split-stories)
- [Splitting Patterns](#splitting-patterns)
- [Vertical vs Horizontal Slicing](#vertical-vs-horizontal-slicing)
- [Story Splitting Anti-Patterns](#story-splitting-anti-patterns)
- [INVEST Check for Split Stories](#invest-check-for-split-stories)
- [Practical Splitting Exercise](#practical-splitting-exercise)
- [When NOT to Split](#when-not-to-split)
- [Summary: Quick Decision Tree](#summary-quick-decision-tree)

---

## Why Split Stories?

**Large stories are problematic**:

- Hard to estimate accurately
- Take too long (miss sprint commitment)
- Difficult to test thoroughly
- Block other work
- Delay feedback
- Increase risk

**Small stories are better**:

- Easier to estimate
- Fit in sprint
- Deliver value faster
- Enable parallel work
- Reduce risk
- Facilitate learning

**Rule of thumb**: If a story is > 5 days of work (or >8 story points), split it.

---

## Splitting Patterns

### 1. Workflow Steps

Split by sequential steps in a process.

**Example: Checkout Process**

❌ **Too large**:

```
As a user
I want to complete the entire checkout process
So that I can purchase products
```

**Split into workflow steps**:

```
Story 1: As a user, I want to review my cart before checkout
Story 2: As a user, I want to enter my shipping address
Story 3: As a user, I want to select a shipping method
Story 4: As a user, I want to enter my payment information
Story 5: As a user, I want to review my complete order before submitting
Story 6: As a user, I want to receive an order confirmation
```

**When to use**: Multi-step workflows, wizards, processes

---

### 2. CRUD Operations

Split by Create, Read, Update, Delete.

**Example: Contact Management**

❌ **Too large**:

```
As a user
I want to manage my contacts
```

**Split by CRUD**:

```
Story 1: As a user, I want to CREATE new contacts
Story 2: As a user, I want to VIEW my contacts list
Story 3: As a user, I want to SEARCH for specific contacts
Story 4: As a user, I want to UPDATE contact details
Story 5: As a user, I want to DELETE contacts
```

**Order matters**: Usually build in this sequence:

1. Create (can't do anything without data)
2. Read/View (verify create works)
3. Update (modify existing data)
4. Delete (cleanup)

**When to use**: CRUD-heavy features, data management

---

### 3. User Roles

Split by different user types or personas.

**Example: Dashboard Access**

❌ **Too large**:

```
As a user
I want to access the analytics dashboard
```

**Split by user role**:

```
Story 1: As an admin, I want to view company-wide metrics
Story 2: As a manager, I want to view my team's performance
Story 3: As an employee, I want to view my personal stats
Story 4: As a guest, I want to view public metrics (read-only)
```

**Benefits**:

- Different roles = different value = easier prioritization
- Can develop in parallel (different permissions, different views)
- Can release to different roles at different times

**When to use**: Features with role-based access, multi-tenant apps

---

### 4. Business Rules

Split by different business logic variations.

**Example: Discount System**

❌ **Too large**:

```
As a user
I want to apply discounts at checkout
```

**Split by business rules**:

```
Story 1: As a user, I want to apply percentage-off coupons (e.g., 20% off)
Story 2: As a user, I want to apply fixed-amount coupons (e.g., $10 off)
Story 3: As a user, I want to apply BOGO offers (buy one get one)
Story 4: As a user, I want to apply free shipping codes
Story 5: As a user, I want to see error messages for invalid/expired coupons
Story 6: As a user, I want to apply multiple coupons (if allowed)
```

**When to use**: Features with complex business logic, multiple rule variations

---

### 5. Simple to Complex (Vertical Slicing)

Build simple version first, then add complexity.

**Example: Product Search**

❌ **Too large**:

```
As a user
I want to search for products with advanced filters
```

**Split by complexity**:

```
Story 1: As a user, I want to search by keyword (basic search)
Story 2: As a user, I want to filter results by category
Story 3: As a user, I want to filter results by price range
Story 4: As a user, I want to sort results (price, rating, newest)
Story 5: As a user, I want to save my search filters
Story 6: As a user, I want to combine multiple filters
```

**Benefits**:

- Deliver core value quickly (basic search)
- Learn from users before building complex features
- Can stop after early stories if simple version is enough

**When to use**: Features where complexity can be added incrementally

---

### 6. Happy Path vs Edge Cases

Split by success scenarios first, then error handling.

**Example: File Upload**

❌ **Too large**:

```
As a user
I want to upload profile photos with full error handling
```

**Split by scenarios**:

```
Story 1: As a user, I want to upload valid JPG/PNG photos (happy path)
Story 2: As a user, I see an error for unsupported file types
Story 3: As a user, I see an error when file exceeds size limit
Story 4: As a user, I see an error when upload fails due to network issues
Story 5: As a user, photos are auto-resized if they're too large
Story 6: As a user, I can retry failed uploads
```

**Order**: Always build happy path first, then add edge cases and error handling.

**When to use**: Any feature where error states add complexity

---

### 7. Data Variations

Split by different data types or sizes.

**Example: Data Export**

❌ **Too large**:

```
As a user
I want to export my data in various formats
```

**Split by data type/format**:

```
Story 1: As a user, I want to export small datasets (<1K rows) as CSV
Story 2: As a user, I want to export small datasets as Excel
Story 3: As a user, I want to export small datasets as PDF
Story 4: As a user, I want to export large datasets (>10K rows) with async processing
Story 5: As a user, I want to receive email notification when large export completes
```

**When to use**: Features handling multiple formats, scales, or data types

---

### 8. Platform/Device

Split by platform or device type.

**Example: Responsive Design**

❌ **Too large**:

```
As a user
I want the app to work on all devices
```

**Split by platform**:

```
Story 1: As a desktop user, I want a full-featured dashboard
Story 2: As a tablet user, I want a touch-optimized dashboard
Story 3: As a mobile user, I want a simplified dashboard
Story 4: As a user, I want the dashboard to adapt as I resize my browser
```

**When to use**: Cross-platform features, responsive design

---

### 9. Performance Tiers

Split by performance/scale requirements.

**Example: Real-Time Collaboration**

❌ **Too large**:

```
As a user
I want real-time collaboration at any scale
```

**Split by performance tier**:

```
Story 1: As a user, I want to collaborate with 1-5 people (MVP)
Story 2: As a user, I want to collaborate with 6-20 people
Story 3: As a user, I want to collaborate with 21-100 people
Story 4: As a user, I want collaboration to work smoothly even with slow internet
```

**When to use**: Features where scale/performance adds significant complexity

---

### 10. Interface vs API

Split by interface layer.

**Example: Payment Processing**

❌ **Too large**:

```
As a developer
I want a complete payment system
```

**Split by layer**:

```
Story 1: As a developer, I want a payment API endpoint (backend only)
Story 2: As a user, I want a payment form UI (frontend)
Story 3: As a user, I want to see payment confirmation (UI + integration)
Story 4: As an admin, I want to view payment history (admin UI)
```

**When to use**: Full-stack features, API-first development

---

## Vertical vs Horizontal Slicing

### Vertical Slice (Preferred)

**Definition**: Complete feature through all layers (UI → API → DB)

**Example**: "User can create a basic contact"

- Frontend: Create contact form
- API: POST /contacts endpoint
- Database: Insert contact record
- Result: Working end-to-end feature

**Benefits**:

- Delivers real value
- Can demo to users
- Tests integration
- Reveals issues early

### Horizontal Slice (Avoid)

**Definition**: Complete one layer across many features

**Example**: "Build all database tables"

- Story 1: Create all DB schemas
- Story 2: Build all API endpoints
- Story 3: Build all UI forms

**Problems**:

- No working feature until all layers done
- Can't get user feedback
- Integration issues discovered late
- No value delivered until final story

**When horizontal is OK**: Pure technical work (infrastructure, refactoring)

---

## Story Splitting Anti-Patterns

### Anti-Pattern 1: Splitting by Developer

❌ **Bad**:

```
Story 1: Bob builds the backend
Story 2: Alice builds the frontend
```

**Why bad**: Not valuable independently, creates dependencies

**Better**: Split by feature, allow pairing if needed

---

### Anti-Pattern 2: Splitting by Technical Layer

❌ **Bad**:

```
Story 1: Create database schema
Story 2: Build API
Story 3: Build UI
```

**Why bad**: No working feature until all done (horizontal slicing)

**Better**: Vertical slices through all layers

---

### Anti-Pattern 3: Splitting Tasks, Not Stories

❌ **Bad**:

```
Story 1: Design the UI
Story 2: Write the code
Story 3: Write tests
```

**Why bad**: These are tasks within a story, not separate stories

**Better**: One story includes design, code, tests

---

### Anti-Pattern 4: Making Stories Too Small

❌ **Too small**:

```
Story 1: Add "Submit" button
Story 2: Make "Submit" button blue
Story 3: Add click handler to "Submit" button
```

**Why bad**: Overhead of story management exceeds value

**Better**: Combine into one story with acceptance criteria

---

## INVEST Check for Split Stories

After splitting, verify each story meets INVEST:

**Independent**:

- [ ] Can be developed without waiting for other stories?
- [ ] If dependencies exist, are they minimal and clear?

**Negotiable**:

- [ ] Is the solution approach flexible?
- [ ] Can implementation details be discussed?

**Valuable**:

- [ ] Does it deliver value to user or business?
- [ ] Would anyone care if we shipped just this story?

**Estimable**:

- [ ] Can the team estimate effort confidently?
- [ ] Are there enough details to assess complexity?

**Small**:

- [ ] Can be completed in 1-3 days?
- [ ] Fits comfortably in a sprint?

**Testable**:

- [ ] Are acceptance criteria clear and testable?
- [ ] Can we verify it works without ambiguity?

---

## Practical Splitting Exercise

**Original Large Story**:

```
As a user
I want a notifications system
So that I stay informed about important events
```

**Questions to ask**:

1. What types of notifications? (Email, push, in-app, SMS)
2. What events trigger notifications? (Mentions, messages, updates)
3. What user controls exist? (Preferences, frequency, mute)
4. What platforms? (Web, mobile)
5. What complexity? (Real-time, batched, scheduled)

**Possible splitting**:

```
Story 1: As a user, I want in-app notifications for @mentions (real-time)
Story 2: As a user, I want email notifications for @mentions (batched hourly)
Story 3: As a user, I want to configure which events trigger notifications
Story 4: As a user, I want to mute notifications temporarily
Story 5: As a user, I want push notifications on mobile (requires Story 1)
Story 6: As a user, I want notification history (see past 30 days)
```

**Priority**:

- Must Have: Stories 1, 2 (core value)
- Should Have: Stories 3, 4 (user control)
- Nice to Have: Stories 5, 6 (enhancements)

---

## When NOT to Split

**Don't split if**:

- Story is already small (1-3 days)
- Splitting creates artificial dependencies
- Split stories don't deliver value independently
- Overhead of managing multiple stories exceeds benefit

**Example where splitting is overkill**:

```
As a user
I want to change my password
So that I can keep my account secure
```

This is already small. Don't split into "Show password form" + "Validate password" + "Save password". Just build it as one story.

---

## Summary: Quick Decision Tree

```
Is story > 5 days or >8 points?
├─ No → Don't split, it's already right-sized
└─ Yes → Can you split by...
    ├─ Workflow steps? (checkout steps, wizard pages)
    ├─ CRUD operations? (create → read → update → delete)
    ├─ User roles? (admin, manager, employee)
    ├─ Business rules? (different discount types)
    ├─ Complexity? (simple → advanced features)
    ├─ Scenarios? (happy path → edge cases)
    └─ If none fit → Consider combining patterns
```

**Golden rule**: Each split story should be valuable independently and fit in 1-5 days of work.
