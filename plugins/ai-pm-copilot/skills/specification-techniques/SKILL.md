---
name: specification-techniques
description: Master techniques for writing clear, complete product specifications and requirements documents (PRDs). Use when defining feature requirements, writing user stories, creating acceptance criteria, documenting API specifications, aligning cross-functional teams, reducing ambiguity, covering edge cases, or translating product vision into actionable development tasks. Covers PRD structure, user story formats (INVEST, 3Cs, Given-When-Then), Jobs-to-be-Done, use cases, non-functional requirements, and specification best practices.
---

# Specification Techniques

Structured methods for translating product vision into clear, actionable requirements that align teams, reduce ambiguity, and enable successful execution.

## Overview

Specification techniques help you answer "what" and "why" clearly while leaving "how" flexible for the team to determine. They create shared understanding without being prescriptive about implementation.

**Core Principle:** The value of specifications isn't in comprehensive documentation—it's in the conversations and shared understanding they create. A 3-sentence user story that everyone understands is better than a 30-page spec no one reads.

**Origin:** Modern specification techniques evolved from software engineering (Karl Wiegers), agile methodologies (Mike Cohn), and design thinking (Alan Cooper).

**Key Insight:** Good specifications enable teams to build the right thing, while bad specifications constrain teams and lead to rework.

---

## When to Use This Skill

**Auto-loaded by agents**:
- `requirements-engineer` - For PRDs, user stories, acceptance criteria, and NFRs

**Use when you need to**:
- Write product requirements documents (PRDs)
- Create user stories with acceptance criteria
- Define feature requirements clearly
- Document edge cases and error handling
- Specify non-functional requirements (performance, security)
- Align cross-functional teams on scope
- Translate product vision into development tasks

---

## Product Requirements Documents (PRDs)

### Core Structure

A well-structured PRD contains:

1. **Overview** - Problem, goals, non-goals, success metrics
2. **Background** - Context, user research, competitive analysis
3. **User Personas** - Primary/secondary users, use cases
4. **Requirements** - Functional and non-functional requirements
5. **User Experience** - Flows, wireframes, interaction details
6. **Technical Considerations** - Architecture, APIs, performance
7. **Success Criteria** - Launch criteria, key metrics
8. **Timeline & Resources** - Milestones, team, risks

**Complete Template:** See `assets/prd-structure-template.md` for full PRD structure with examples and best practices.

---

### Essential PRD Components

**Problem Statement:**
```
What: Clear description of the problem
Who: Who experiences this problem
Impact: Business/user impact with data
Current: What users do today
```

**Goals and Non-Goals:**
- **Goals:** What you want to achieve (measurable)
- **Non-Goals:** What you're explicitly not doing (sets boundaries)

**Success Metrics:**
- Specific, measurable outcomes
- Baseline → Target values
- Timeline for achievement

**Example:**
```
Problem: Users miss critical alerts when not in app, leading to 40% missed events.

Goal: Reduce missed alerts from 40% to <15% via email notifications.

Non-Goals:
- SMS notifications (future scope)
- Customizable notification frequency (v1: fixed)

Success Metrics:
- 60% opt-in to email notifications
- 25% reduction in missed alerts
- <2% unsubscribe rate
```

---

## User Stories

### The Standard Format

```
As a [user type]
I want [capability]
So that [benefit]
```

**Purpose:** Placeholder for conversation, not complete specification.

**Example:**
```
As a project manager
I want to assign tasks to team members
So that everyone knows their responsibilities
```

---

### INVEST Criteria

Framework for evaluating user story quality (Mike Cohn):

- **I - Independent:** Can be developed in any order
- **N - Negotiable:** Details flexible, not a contract
- **V - Valuable:** Delivers user or business value
- **E - Estimable:** Team can estimate effort
- **S - Small:** Fits within one sprint (1-5 days)
- **T - Testable:** Clear acceptance criteria

**Complete Guide:** See `references/user-story-writing-guide.md` for detailed explanations, examples, and story splitting patterns.

**Template:** See `assets/user-story-template.md` for comprehensive user story template with INVEST checklist.

---

### The 3 Cs Framework (Ron Jeffries)

**Card:** Brief story description (placeholder)
**Conversation:** Discuss details during planning/refinement (most important)
**Confirmation:** Acceptance criteria (how to verify done)

**Key Insight:** The conversation is more valuable than the written artifact.

---

## Acceptance Criteria

### Three Formats

**Format 1: Given-When-Then (Gherkin/BDD)**
```
Given [precondition/context]
When [action/event]
Then [expected outcome]
And [additional outcome]
```

**Best for:** Behavior-driven development, sequential workflows, automated testing

**Example:**
```
Given I am on the login page
When I enter valid credentials and click "Login"
Then I am redirected to my dashboard
And I see a welcome message with my name
```

---

**Format 2: Checklist Style**
```
Acceptance Criteria:
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
```

**Best for:** Simple features, independent criteria, non-sequential requirements

**Example:**
```
- [ ] User can upload JPG, PNG, GIF files
- [ ] Maximum file size is 10MB
- [ ] Upload progress bar shows percentage
- [ ] Error shown if file too large
```

---

**Format 3: Example-Based**
```
Scenario: [Description]
Input: [What user provides]
Output: [What system produces]
```

**Best for:** Complex calculations, validation rules, data transformations

**Example:**
```
Scenario 1: Valid email
Input: user@example.com
Output: Email accepted

Scenario 2: Missing @ symbol
Input: userexample.com
Output: Error "Email must include @ symbol"
```

**Complete Guide:** See `references/acceptance-criteria-guide.md` for comprehensive guide to writing testable acceptance criteria with all three formats, examples, and best practices.

---

## Job Stories (Jobs-to-be-Done)

### Format

```
When [situation/context]
I want to [motivation]
So I can [expected outcome]
```

**Difference from User Stories:**
- Focuses on context/situation (not persona)
- Emphasizes motivation (not implementation)
- Better for discovering underlying needs

**Example:**
```
When I'm in a meeting and need to reference previous discussions
I want to quickly search message history by keyword
So I can find relevant context without disrupting the meeting flow
```

**Complete Template:** See `assets/job-story-template.md` for detailed job story structure, examples, and when to use vs. user stories.

---

## Use Cases

### Structure

Detailed interaction scenarios documenting step-by-step system behavior.

**Components:**
- Primary actor and goal
- Preconditions and postconditions
- Main success scenario (happy path)
- Alternative flows (variations)
- Exception flows (error handling)

**Example Structure:**
```
Use Case: User Registers for Account

Primary Actor: New user
Goal: Create account to access platform

Main Success Scenario:
1. User enters email, password, name
2. System validates inputs
3. System creates account
4. System sends verification email
5. User clicks verification link
6. System activates account
```

**Complete Template:** See `assets/use-case-template.md` for comprehensive use case template with examples of alternative flows, exception handling, and special requirements.

---

## Edge Cases and Error Handling

### Systematic Coverage

Document behavior for:

**1. Input Validation** - Empty inputs, special characters, invalid formats
**2. Permissions** - Unauthenticated, insufficient privileges, expired sessions
**3. State Handling** - Empty state, loading state, error state, full state
**4. Boundary Conditions** - Zero, one, maximum, just over maximum
**5. Time-Based** - Expired tokens, time zones, scheduling
**6. Network Issues** - Timeouts, server errors, rate limiting

**Example:**
```
Error Scenario: Payment fails due to insufficient funds

User Experience:
- Error message: "Payment declined - insufficient funds. Please use a different payment method."

System Behavior:
- Transaction rolled back
- User not charged
- Order not created
- Error logged

Recovery Action:
- User can update payment method and retry
```

**Complete Checklist:** See `assets/edge-case-checklist.md` for systematic 100+ point checklist covering all edge case categories with examples and error handling templates.

---

## Non-Functional Requirements

### Key Categories

**Performance Requirements:**
- Response time (page loads, API calls)
- Throughput (requests per second)
- Scalability (concurrent users, data volume)

**Security Requirements:**
- Authentication (MFA, password policies)
- Authorization (RBAC, least privilege)
- Data protection (encryption, GDPR compliance)

**Reliability Requirements:**
- Availability (uptime %)
- Data integrity (backups, recovery)
- Fault tolerance (failover, retries)

**Accessibility Requirements:**
- WCAG 2.1 compliance
- Keyboard navigation
- Screen reader compatibility

**Example:**
```
Performance: Page loads in <2 seconds (p95)
Security: All PII encrypted at rest (AES-256)
Reliability: 99.9% uptime (max 8.7 hours downtime/year)
Accessibility: WCAG 2.1 Level AA compliant
```

**Complete Template:** See `assets/non-functional-requirements-template.md` for comprehensive NFR documentation covering all categories with specific metrics and verification methods.

---

## Specification Best Practices

### Start with Why

Always begin with problem statement before jumping to solutions:

**Problem Statement Template:**
```
Problem: [What problem exists?]
Impact: [Who is affected and how?]
Evidence: [Data, research, user quotes]
Goal: [What would success look like?]
```

---

### Be Specific and Measurable

**Vague (Bad):** "System should be fast"

**Specific (Good):** "Page loads in <2 seconds (p95), measured via Lighthouse"

**Avoid Ambiguous Terms:**
- "Fast" → Specific time (< 2 seconds)
- "Good" → Specific criteria
- "User-friendly" → Task completion metrics
- "Secure" → OWASP Top 10 compliant

---

### Cover Happy and Unhappy Paths

**Happy Path:** Successful scenario

**Unhappy Paths:**
- Error cases (invalid input, permission denied)
- Edge cases (boundary conditions, rare scenarios)
- Network failures (timeouts, service down)

**Example:**
```
Happy: User logs in with valid credentials → Dashboard
Error: User enters wrong password → Error message, stay on login
Edge: Session expires during form entry → Preserve data, re-authenticate
```

---

### Specify Behavior, Not Implementation

**Too Prescriptive (Bad):**
```
"Use Material-UI Autocomplete component with Redux state management"
```

**Behavioral (Good):**
```
"User can search for other users by name, see suggestions as they type, select one or multiple users. Selection persists across page refreshes."

Let engineering decide: component library, state management
```

---

### Include Visual Aids

**Use diagrams for:**
- User flows
- State machines
- Data flows
- Wireframes/mockups

**Use examples for:**
- Input validation rules
- Calculations
- Data transformations

---

## Anti-Patterns to Avoid

### 1. Solution Masquerading as Problem

**Bad:** "We need a chatbot on the homepage"

**Good:**
```
Problem: 60% of support tickets are basic questions. Users can't find answers quickly.
Explored solutions: Chatbot, improved search, interactive FAQ
```

---

### 2. Vague Requirements

**Bad:** "System should have good performance"

**Good:** "Dashboard loads in <2 seconds (p95) for 10,000 concurrent users"

---

### 3. Over-Specification

**Bad:** "Use bcrypt with cost factor 12, store in CHAR(60) column"

**Good:** "Passwords hashed with industry-standard algorithm meeting OWASP guidelines"

---

### 4. Missing Acceptance Criteria

**Bad:**
```
As a user, I want notifications
```

**Good:**
```
As a user, I want email notifications
So that I'm aware of critical events

Acceptance Criteria:
- Given payment fails, when processor returns error, then email sent within 5 minutes
- Given I'm in settings, when I toggle notifications, then preference saves immediately
```

---

### 5. Ignoring Edge Cases

**Bad:** "User can upload a file"

**Good:**
```
User can upload file:
- Happy: File <10MB, supported format → Success
- Error: File >10MB → "File exceeds 10MB limit"
- Error: Unsupported format → "Only JPG, PNG, PDF allowed"
- Error: Network failure → Auto-retry 3x, then "Upload failed. Retry?"
```

**Complete Guide:** See `references/specification-anti-patterns.md` for detailed anti-patterns with examples and fixes.

---

## Reference Guides

### Comprehensive Guides

**User Story Writing:**
- `references/user-story-writing-guide.md`
- INVEST criteria in depth
- The 3 Cs framework
- Story splitting patterns
- User story vs job story vs use case

**Acceptance Criteria:**
- `references/acceptance-criteria-guide.md`
- All three formats explained
- Writing testable criteria
- Covering happy/unhappy paths
- Edge case documentation

**Anti-Patterns:**
- `references/specification-anti-patterns.md`
- Common mistakes and how to avoid them
- Solution masquerading as problem
- Vague requirements
- Over-specification

**Best Practices:**
- `references/specification-best-practices.md`
- Core principles
- Structure and organization
- Writing style and clarity
- Collaboration and communication
- Progressive elaboration

---

## Templates and Tools

### Ready-to-Use Templates

**Documentation:**
- `assets/prd-structure-template.md` - Complete PRD template
- `assets/user-story-template.md` - User story with INVEST
- `assets/job-story-template.md` - Jobs-to-be-Done format
- `assets/use-case-template.md` - Detailed use case structure

**Checklists:**
- `assets/edge-case-checklist.md` - 100+ point systematic coverage
- `assets/non-functional-requirements-template.md` - NFR documentation

---

## Summary

**Good Specifications:**
- Start with problem and user needs (the "why")
- Are specific, measurable, and testable
- Cover happy paths, unhappy paths, and edge cases
- Specify behavior and constraints (the "what")
- Leave implementation flexible (the "how")
- Use visual aids and concrete examples
- Create shared understanding through conversation

**Remember:** Specifications are conversation starters, not contracts. Focus on creating shared understanding between product, engineering, design, and QA.

---

## Related Skills

- `prd-templates` - PRD templates and examples
- `user-story-templates` - User story templates and patterns
- `user-research-techniques` - Understanding user needs and requirements
