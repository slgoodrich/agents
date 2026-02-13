# Task Scenario Template

## Table of Contents

- [What Makes a Good Task Scenario?](#what-makes-a-good-task-scenario)
- [Task Scenario Formula](#task-scenario-formula)
- [Examples: Poor vs. Good](#examples-poor-vs-good)
- [Task Scenario Template](#task-scenario-template)
- [Template Examples by Task Type](#template-examples-by-task-type)
- [Task Complexity Guidelines](#task-complexity-guidelines)
- [Providing Task Information](#providing-task-information)
- [Common Mistakes to Avoid](#common-mistakes-to-avoid)
- [Adapting Task Scenarios for Different Test Types](#adapting-task-scenarios-for-different-test-types)
- [Task Prioritization](#task-prioritization)
- [Sample Task Set for a Project Management Tool](#sample-task-set-for-a-project-management-tool)

## What Makes a Good Task Scenario?

A good task scenario is:

- **Realistic**: Based on actual user goals and motivations
- **Specific**: Clear success criteria
- **Self-contained**: Provides all necessary context
- **Actionable**: Clear starting point
- **Not prescriptive**: Doesn't tell users where to click or what steps to take

## Task Scenario Formula

```
[Context/Situation] + [Motivation/Why] + [Goal/What to accomplish]
```

## Examples: Poor vs. Good

### Example 1: Password Change

**Poor**:
"Click on 'My Account' and change your password."

**Why it's poor**:

- Tells user exactly where to click
- No realistic motivation
- Prescriptive path

**Good**:
"You've been reading about recent security breaches and want to make your account more secure. Change your password to something stronger."

**Why it's good**:

- Realistic motivation (security concern)
- Clear goal (stronger password)
- Doesn't prescribe the path
- Self-contained context

---

### Example 2: Finding Information

**Poor**:
"Go to the Help section and find the article about refunds."

**Why it's poor**:

- Tells them where to go
- No real user motivation

**Good**:
"You accidentally bought the wrong subscription tier and want to know if you can get a refund. Find out what the refund policy is."

**Why it's good**:

- Realistic mistake scenario
- Clear information need
- Lets them discover the path

---

### Example 3: E-commerce

**Poor**:
"Add a laptop to your cart and check out."

**Why it's poor**:

- Unrealistic (no context about why)
- Too simple, not representative of real behavior

**Good**:
"Your current laptop is running slow, and you need something more powerful for video editing. Find a laptop that would work well for editing 4K video and is within a $1,500 budget. You don't need to actually purchase it—just add it to your cart."

**Why it's good**:

- Realistic need (specific use case)
- Decision criteria provided
- Clear stopping point
- Enables testing of product filtering/search

---

## Task Scenario Template

Use this template to create your own task scenarios:

```markdown
### Task [Number]: [Short task name for your reference]

**Scenario**:
"[Context: What's happening in their life/work?] [Motivation: Why do they need to do this?] [Goal: What do they want to accomplish?]"

**Success criteria** (internal, not shared with participant):

- [ ] User successfully [primary action]
- [ ] User reached [expected destination/state]
- [ ] [Optional: User discovered/used expected feature]

**Expected path** (for comparison to actual path):

1. [Step 1]
2. [Step 2]
3. [Step 3]

**Alternative valid paths**:

- Path B: [Alternative approach that also works]
```

---

## Template Examples by Task Type

### 1. Information Finding Task

```markdown
### Task 3: Finding Support Information

**Scenario**:
"You're having trouble connecting your account to [third-party service]. Find information about how to troubleshoot this connection issue."

**Success criteria**:

- [ ] Found the integration troubleshooting guide
- [ ] Located relevant section for [third-party service]

**Expected path**:

1. Navigate to Help or Support section
2. Search or browse for integrations
3. Find troubleshooting article
```

---

### 2. Account/Settings Management Task

```markdown
### Task 2: Privacy Settings

**Scenario**:
"You're concerned about your privacy and want to make sure your profile isn't visible to people outside your organization. Adjust your settings so only people in your company can see your profile."

**Success criteria**:

- [ ] Located privacy settings
- [ ] Changed profile visibility to organization-only
- [ ] Saved changes

**Expected path**:

1. Account or Settings menu
2. Privacy or Profile section
3. Visibility toggle/dropdown
4. Save
```

---

### 3. Creation/Setup Task

```markdown
### Task 1: Creating First Project

**Scenario**:
"You just joined a new team at work, and you need to set up a project to track your team's marketing campaign for the summer launch. Create a new project called 'Summer Launch 2024'."

**Success criteria**:

- [ ] Successfully created new project
- [ ] Named it correctly
- [ ] Reached project dashboard/view

**Expected path**:

1. Find "New Project" or similar CTA
2. Enter project details
3. Submit/Create
```

---

### 4. Comparison/Decision Task

```markdown
### Task 4: Plan Selection

**Scenario**:
"Your startup is growing, and you currently have 8 team members with plans to hire 5 more this quarter. You need a plan that supports at least 15 users and includes priority support. Find the right plan for your needs and see how much it would cost per month."

**Success criteria**:

- [ ] Viewed pricing/plans page
- [ ] Identified appropriate plan tier
- [ ] Determined monthly cost

**Expected path**:

1. Navigate to Pricing
2. Compare plans
3. Calculate or view 15-user pricing
```

---

### 5. Troubleshooting/Recovery Task

```markdown
### Task 5: Recovering Deleted Item

**Scenario**:
"You accidentally deleted an important report yesterday and just realized you need it. Try to recover the deleted report."

**Success criteria**:

- [ ] Found trash/deleted items area
- [ ] Located and restored the item

**Expected path**:

1. Find trash/deleted items
2. Browse or search for item
3. Restore action
```

---

## Task Complexity Guidelines

### Simple Tasks (1-3 clicks)

**Purpose**: Establish baseline usability, test navigation

**Example**: "Find your account settings"

**Use for**:

- Warm-up tasks
- Testing core navigation
- Quick usability checks

---

### Medium Tasks (3-7 clicks)

**Purpose**: Test realistic workflows, uncover common issues

**Example**: "Change your email notification preferences to only receive weekly summaries"

**Use for**:

- Primary task flows
- Most common user journeys
- Feature discovery

---

### Complex Tasks (7+ clicks, multiple steps)

**Purpose**: Test complete workflows, error handling, persistence

**Example**: "Set up a new campaign with three different audience segments, allocate budget across them, and schedule it to run next week"

**Use for**:

- Advanced features
- Multi-step processes
- Testing stamina and error recovery

---

## Providing Task Information

### Option 1: Verbal Instructions

**Facilitator reads scenario aloud**

**Pros**:

- More natural, conversational
- Can adjust wording on the fly

**Cons**:

- Participant may forget details
- Harder to stay consistent across participants

---

### Option 2: Written Cards/Sheets

**Participant reads scenario from paper or screen**

**Pros**:

- Can refer back as needed
- Consistent wording
- Participant sets their own pace

**Cons**:

- Slightly less natural
- Need to prepare materials

---

### Option 3: Combination

**Facilitator reads, participant has written version too**

**Best of both worlds**: Natural + referenceable

---

## Common Mistakes to Avoid

### 1. Too Prescriptive

**Bad**: "Click the menu in the top-right corner and select Settings"
**Good**: "Change your password"

### 2. Using Product Terminology

**Bad**: "Create a new workspace and invite collaborators"
**Good**: "Set up a shared space where your team can work together"
(Unless you're specifically testing if users understand "workspace")

### 3. Unrealistic Motivation

**Bad**: "Find the about page"
**Good**: "You want to know what year the company was founded for a presentation you're giving"

### 4. Multiple Goals in One Task

**Bad**: "Update your profile, change your notification settings, and add a payment method"
**Good**: Split into 3 separate tasks

### 5. Impossible Tasks

**Bad**: "Find the user guide" (if no user guide exists)
**Make sure**: All tasks are actually possible with current product

---

## Adapting Task Scenarios for Different Test Types

### For Moderated Tests

- Can be slightly more open-ended
- Facilitator can clarify if needed
- Include motivation and context

### For Unmoderated Tests

- Must be extremely clear and self-contained
- Include all details participant needs
- Specify exact endpoint (e.g., "Stop when you've found the answer")

### For Prototype Tests

- Acknowledge limited functionality
- Focus on concept and flow rather than completion
- "Imagine this button worked—what would you expect to happen?"

---

## Task Prioritization

When you have limited time, prioritize tasks that:

1. **Represent critical user goals** - What must work for product to be valuable?
2. **Are frequently performed** - High-volume tasks have high impact
3. **Have known issues** - Validate fixes or explore problems
4. **Are recent changes** - Test new features before launch
5. **Cross multiple features** - End-to-end workflows reveal integration issues

---

## Sample Task Set for a Project Management Tool

```markdown
### Task 1: Create a Project (Simple)

"You're starting a new initiative to redesign your company website. Create a project to track this work."

### Task 2: Invite Team Member (Simple-Medium)

"You need your designer, Jamie, to collaborate on this project. Add Jamie (jamie@example.com) to the website redesign project."

### Task 3: Organize Tasks (Medium)

"The website redesign has three main phases: Research, Design, and Development. Organize your project to reflect these phases."

### Task 4: Set a Deadline (Medium)

"Your CEO wants the website redesign completed by December 1st. Set up the project to track toward that deadline."

### Task 5: View Progress (Medium)

"You're preparing for your weekly status meeting. Get an overview of how the website redesign project is progressing."

### Task 6: Find Overdue Items (Medium-Complex)

"You think some tasks might be falling behind schedule. Find any overdue tasks across all your projects."
```

This set tests: creation, collaboration, organization, scheduling, reporting, and cross-project views.

---

**Remember**: Great task scenarios make participants forget they're in a test. They should feel like real problems they might actually need to solve.
