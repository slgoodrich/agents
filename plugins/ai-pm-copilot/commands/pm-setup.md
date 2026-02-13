---
description: "Initialize .claude/product-context/ with essential product information for all PM agents"
argument-hint: "[--update]"
---

# PM Context Setup

Quick setup wizard to initialize `.claude/product-context/` with essential product information. Takes 5-10 minutes and enables all PM agents, commands, and workflows to work with your product context.

## Usage

```bash
/product-management:pm-setup
```

Or update existing context:

```bash
/product-management:pm-setup --update
```

---

## Overview

This command sets up the foundational context that powers the entire PM Toolkit. Instead of asking for everything upfront, **we create the essentials now and let the journey build additional context progressively**.

**What it does:**

- Creates `.claude/product-context/` directory
- Guides you through 2 required files (product basics, tech stack)
- Offers optional files if applicable (goals, metrics, team)
- Explains how agents will create additional context as you progress

**What you get:**

- Context reused across 1 orchestrator + 7 specialists
- Agents work with YOUR product specifics
- No repeated questions across tools
- Progressive context building through your journey

---

## Instructions

### Introduction

Display introduction message:

```
╔═══════════════════════════════════════════════════════════╗
║   Product Management Context Setup                        ║
╔═══════════════════════════════════════════════════════════╝

Quick setup to get your PM agents working with your product context.

**How it works:**
We'll create the essential INPUT files now (5-10 minutes). As you progress
through your product journey, agents will create additional context files:

- Stage 1 (Validation) → competitive-landscape.md
- Stage 2 (Understanding) → customer-segments.md
- Stage 5 (Planning) → current-roadmap.md

Your context grows as your product develops!

**What we'll create now:**

Required:
1. product-info.md - Product basics (name, description, stage, market, value prop)
2. tech-stack.md - Tech stack, architecture, constraints

Optional (if applicable):
3. strategic-goals.md - Vision, goals, priorities (we can help with product-strategist)
4. business-metrics.md - Current metrics (only if post-launch)
5. team-info.md - Team size, velocity (only if team > 1)

Ready to begin? (yes/no)
```

If user says "no", exit. If "yes", continue.

---

### Step 0: Check Existing Context

Check if `.claude/product-context/` directory exists:

```bash
ls .claude/product-context/ 2>/dev/null
```

**If directory exists** with files:

```
I found existing context files:
✓ product-info.md
✓ tech-stack.md
✓ competitive-landscape.md (created by market-analyst in Stage 1)
❌ strategic-goals.md (missing)
...

Would you like to:
1. Update existing files
2. Start fresh (overwrite all)
3. Cancel

Your choice (1/2/3):
```

**If directory doesn't exist:**

```bash
mkdir -p .claude/product-context
```

```
Creating .claude/product-context/ directory...
✓ Directory created
```

---

### Step 0.5: Detect Codebase (NEW)

Before asking manual questions, check if we can auto-discover context from an existing codebase.

**Check for codebase indicators:**

```bash
# Check for common source directories and manifests
ls src/ pages/ routes/ api/ app/ package.json requirements.txt go.mod Gemfile composer.json 2>/dev/null
```

**Codebase detected if any of these exist:**

- Source directories: `src/`, `pages/`, `routes/`, `api/`, `app/`, `lib/`
- Package manifests: `package.json`, `requirements.txt`, `pyproject.toml`, `go.mod`, `Gemfile`, `composer.json`, `Cargo.toml`

**If codebase detected:**

- Proceed to Step 0.6 (Optional Codebase Scanning)

**If NOT detected:**

- Skip scanning
- Proceed to Step 1 (Product Information - manual entry)
- Display: "No existing codebase detected. Let's set up your context manually."

---

### Step 0.6: Optional Codebase Scanning (NEW)

**If codebase was detected in Step 0.5:**

Display scanning offer:

```
═══════════════════════════════════════════════════════════
Codebase Detected!
═══════════════════════════════════════════════════════════

I've detected an existing codebase in this project.

I can scan your codebase to automatically discover:
- Features (from routes, pages, API endpoints)
- Tech stack (from package.json, requirements.txt, etc.)
- Integrations (from 3rd party packages)
- Project scale (files, lines of code, complexity)

This takes about 30-60 seconds and saves you 10-15 minutes of manual entry.

**What gets scanned:**
- File structure and routes
- Package manifests (package.json, requirements.txt, etc.)
- Tech dependencies
- Project size indicators

**What does NOT get scanned:**
- Code quality or architecture
- Performance or security issues
- Your code implementation details

All findings will be presented for your validation before saving.

Scan codebase now? (yes/no)
```

#### If User Says YES (Accept Scanning)

**Step 1: Invoke context-scanner**

Use Task tool to invoke context-scanner agent:

```
subagent_type: "product-management:context-scanner"
description: "Scan codebase for strategic context"
prompt: "Scan the current codebase and return structured discovery of features, tech stack, integrations, and scale. Include evidence and confidence scores for all findings."
```

**Step 2: Receive and Parse JSON**

context-scanner returns JSON with:

- features (array of discoveries with evidence)
- tech_stack (frontend, backend, database, infrastructure)
- integrations (3rd party services)
- scale (files, LOC, complexity, maturity)
- confidence_notes (explanations)
- scan_limitations (what couldn't be scanned)

**Step 3: Present Findings to User**

Display findings in readable format:

```
═══════════════════════════════════════════════════════════
Scan Complete! Here's what I discovered:
═══════════════════════════════════════════════════════════

## Features Found

[For each feature in features array:]
✓ [Feature name] ([details])
  Evidence: [evidence]
  Confidence: [High/Medium/Low]

[Example:]
✓ Authentication (login, signup, password reset)
  Evidence: src/pages/auth/login.tsx, /api/auth routes
  Confidence: High

✓ Project Management (create, list, edit, delete)
  Evidence: src/pages/projects/, /api/projects routes
  Confidence: High

✓ Analytics (reporting dashboard)
  Evidence: found /analytics route
  Confidence: Medium - please verify if this is complete

## Tech Stack

**Frontend:** [list frontend tech]
**Backend:** [list backend tech]
**Database:** [list databases]
**Infrastructure:** [list infrastructure]

Evidence: package.json, requirements.txt, Dockerfile

## Integrations

[For each integration:]
- [Service name] ([type])
  Evidence: [package info]
  Confidence: [level]

[Example:]
- Stripe (payments)
  Evidence: stripe@12.0.0 in package.json
  Confidence: Medium (package present, usage not verified)

- SendGrid (email)
  Evidence: @sendgrid/mail in package.json
  Confidence: Medium (package present, usage not verified)

## Project Scale

- Total files: [count]
- Lines of code: ~[estimate]
- Complexity: [simple/medium/complex]
- Maturity: [prototype/mvp/established/mature]

[If scan_limitations exist:]
## Scan Limitations

[Display limitations]
Example: "Large codebase detected (5000+ files). Scanned primary directories only. May have missed features in non-standard locations."

───────────────────────────────────────────────────────────
```

**Step 4: User Validation**

```
Is this information accurate? You can:
1. Confirm all (looks good)
2. Make corrections (add, remove, or fix items)
3. Start over with manual entry (ignore scan results)

Your choice (1/2/3):
```

**If choice = 1 (Confirm all):**

```
Great! I'll use this discovered context.

Any features or details I missed that you'd like to add? (describe or type "none"):
[User input]

[If user adds items, append to relevant sections]
✓ Added: [user's addition]
```

**If choice = 2 (Make corrections):**

```
Let's review each section:

═══════════════════════════════════════════════════════════
Features Review
═══════════════════════════════════════════════════════════

[For each feature with Medium/Low confidence:]
[Feature name]: [Confidence level]

Keep this feature? (yes/no/rename)
[User input for each]

[If rename:]
What should I call it instead?
[User input]

[After reviewing uncertain features:]
Any features I completely missed? (list them or type "none"):
[User input]

✓ Features validated

═══════════════════════════════════════════════════════════
Tech Stack Review
═══════════════════════════════════════════════════════════

[Display tech stack]

Is this tech stack accurate? (yes/no)
[If no:]
What needs correction?
[User input]

✓ Tech stack validated

═══════════════════════════════════════════════════════════
Integrations Review
═══════════════════════════════════════════════════════════

[For each integration:]
[Service]: [Type] - Confirm this is actively used? (yes/no/remove)
[User input for each]

Any integrations I missed?
[User input]

✓ Integrations validated
```

**If choice = 3 (Start over with manual entry):**

```
No problem! Let's set up your context manually instead.

Proceeding to manual entry...
```

Skip to Step 1: Product Information (manual flow)

**Step 5: Save Validated Data to Context Files**

Create/update context files with validated data:

**Create current-features.md:**

```markdown
# Current Features

_Auto-discovered: [current date]_
_Last validated: [current date]_

## Core Features

[For each validated feature:]

### [Feature Name]

- [Feature details]
- Evidence: [evidence from scan]
- Confidence: [confidence level]

## Integrations

[For each validated integration:]

### [Service Name] ([Type])

- Evidence: [evidence from scan]
- Confidence: [confidence level]
- Status: [Active/Detected but not verified]

## Not Included (Known Gaps)

[Any features user mentioned as "not yet built" or "planned"]

---

_This file was auto-discovered by context-scanner and validated by user._
_Refresh by running: /product-management:pm-setup_
```

**Update tech-stack.md:**

```markdown
# Tech Stack

**Last Updated:** [current date]
_Auto-discovered from codebase, validated by user_

## Stack

- **Frontend:** [discovered frontend tech]
- **Backend:** [discovered backend tech]
- **Database:** [discovered databases]
- **Infrastructure:** [discovered infrastructure]

_Evidence: [package.json / requirements.txt / etc.]_

## Architecture

[discovered architecture pattern or "Not specified"]

## Technical Constraints

[If user added constraints during validation, list them. Otherwise: "None specified"]

## Scale

- Lines of code: ~[discovered LOC]
- Source files: [discovered file count]
- Complexity: [discovered complexity]
- Maturity: [discovered maturity]

---

_Tech stack auto-discovered by context-scanner_
```

**Update product-info.md (add Features section):**

```markdown
# Product Information

[Existing sections...]

## Features

[For each validated feature:]

- [Feature name]

See `current-features.md` for detailed feature inventory.

---

_Features auto-discovered: [date]_
```

**Step 6: Display Success Message**

```
✓ Context auto-discovered and validated!
✓ Saved to .claude/product-context/

Files created/updated:
- current-features.md (feature inventory)
- tech-stack.md (stack and scale)
- product-info.md (features section added)

Time saved: ~10-15 minutes vs manual entry

───────────────────────────────────────────────────────────
```

Then proceed to Step 3: Optional Context Files (strategic-goals, business-metrics, team-info)

#### If User Says NO (Decline Scanning)

```
No problem! I'll guide you through manual setup instead.

Proceeding to manual entry...
```

Skip scanning, proceed to Step 1: Product Information (manual flow)

---

### Refresh Mode (When Existing Context Detected)

**If Step 0 detected existing `.claude/product-context/` with files:**

Display refresh options:

```
═══════════════════════════════════════════════════════════
Existing Product Context Detected
═══════════════════════════════════════════════════════════

I found existing product context from [date of last update].

Would you like to:

1. Refresh context (re-scan codebase, show what changed)
2. Add to existing (keep current, add new information)
3. Start fresh (archive current, create new)
4. Cancel

Your choice (1/2/3/4):
```

**If choice = 1 (Refresh):**

```
═══════════════════════════════════════════════════════════
Refreshing Product Context
═══════════════════════════════════════════════════════════

Re-scanning your codebase to detect changes...

[Invoke context-scanner again]
[Receive new scan results]

Comparing to existing context...

═══════════════════════════════════════════════════════════
Changes Detected:
═══════════════════════════════════════════════════════════

## Features

**Added:**
[List features in new scan but not in existing context]
- Analytics dashboard
- Export functionality

**Updated:**
[List features that changed]
- Project Management: Now includes Gantt chart view

**Removed:**
[List features in existing context but not in new scan]
- None

**Unchanged:**
- Authentication
- Task Management
- Team Collaboration

## Tech Stack

**Updated:**
- Node.js: 18.x → 20.x
- React: 18.0 → 18.2

**Added:**
- Vite 4.3 (build tool)

**Removed:**
- None

## Integrations

**Added:**
- Slack (notifications)

**Unchanged:**
- Stripe (payments)
- SendGrid (email)

═══════════════════════════════════════════════════════════

Apply these changes? (yes/no/review)
```

**If yes:** Update context files with changes, preserve metadata

**If review:** Let user validate each change individually

**If no:** Keep existing context unchanged

**If choice = 2 (Add to existing):**

```
What would you like to add or update?

1. Add new features
2. Update tech stack
3. Add/update integrations
4. Update strategic goals
5. Update metrics
6. Update team info

Select items to update (comma-separated, e.g., "1,2"):
[User input]
```

Then guide through only selected sections, append to existing files.

**If choice = 3 (Start fresh):**

```
This will archive your current context and create a new one from scratch.

Archive location: .claude/product-context-backup-[YYYY-MM-DD]/

Proceed? (yes/no)
```

If yes:

```bash
# Archive existing context
mv .claude/product-context .claude/product-context-backup-$(date +%Y-%m-%d)

# Create fresh directory
mkdir -p .claude/product-context
```

Then proceed with fresh setup (Step 0.5: Detect Codebase)

**If choice = 4 (Cancel):**

Exit setup without changes.

---

### Step 1: Product Information (Required)

```
═══════════════════════════════════════════════════════════
Step 1 of 2 (Required): Product Information
═══════════════════════════════════════════════════════════

Let's capture the basics about your product.

**Product Name:**
[User input]

**Product Description** (2-3 sentences - what does it do and for whom?):
[User input]

**Product Stage** (select one):
1. Idea - Validating concept, no code yet
2. MVP - First version built, testing with early users
3. PMF - Product-market fit achieved, growing user base
4. Growth - Scaling go-to-market, optimizing funnel
5. Mature - Established product, focus on retention/expansion

Your choice (1-5):
[User input]

**Primary Target Market** (e.g., "B2B SaaS for SMBs", "Consumer productivity app"):
[User input]

**Key Value Proposition** (one sentence - what unique value do you provide?):
[User input]

✓ Product information captured
```

Create `.claude/product-context/product-info.md`:

```markdown
# Product Information

**Product Name:** [name]
**Stage:** [stage]
**Last Updated:** [current date]

## Description

[description]

## Target Market

[target market]

## Value Proposition

[value proposition]

## Product Type

[Infer from description: Web app, Mobile app, API/Platform, Desktop app, etc.]
```

---

### Step 2: Tech Stack (Required)

```
═══════════════════════════════════════════════════════════
Step 2 of 2 (Required): Tech Stack
═══════════════════════════════════════════════════════════

What's your technology stack? This helps agents give specific technical guidance.

**Frontend** (e.g., React, Vue, SwiftUI, Flutter):
[User input]

**Backend** (e.g., Node.js, Python/Django, Go, Ruby/Rails):
[User input]

**Database** (e.g., PostgreSQL, MongoDB, MySQL):
[User input]

**Infrastructure** (e.g., AWS, Vercel, Railway, self-hosted):
[User input]

**Architecture Pattern** (select one):
1. Monolith
2. Microservices
3. Serverless
4. Hybrid

Your choice (1-4):
[User input]

**Key Technical Constraints** (optional, one per line, or type "none"):
[User input - allow multiple lines]
[User types "none" or "done" when finished]

✓ Tech stack captured
```

Create `.claude/product-context/tech-stack.md`:

```markdown
# Tech Stack

**Last Updated:** [current date]

## Stack

- **Frontend:** [frontend]
- **Backend:** [backend]
- **Database:** [database]
- **Infrastructure:** [infrastructure]

## Architecture

[architecture pattern]

## Technical Constraints

[list constraints, or "None specified"]
```

---

### Step 3: Optional Context Files

After completing the 2 required files:

```
═══════════════════════════════════════════════════════════
Optional Context Files
═══════════════════════════════════════════════════════════

Great! You've completed the required files. Would you like to add optional
context files now? These are helpful if applicable to your situation:

1. strategic-goals.md - Vision, goals, priorities (we can help with product-strategist)
2. business-metrics.md - Current metrics, growth rates (only if post-launch)
3. team-info.md - Team size, velocity, capacity (only if team > 1)
4. None - Skip optional files for now

Select files to create (comma-separated, e.g., "1,2" or "4" for none):
[User input]
```

#### Optional: Strategic Goals

If user selects option 1:

```
═══════════════════════════════════════════════════════════
Optional: Strategic Goals
═══════════════════════════════════════════════════════════

Do you have a product vision and strategic goals defined?

1. Yes - I have them ready to share
2. No - Help me develop them with product-strategist agent
3. Skip for now

Your choice (1/2/3):
```

**If choice = 1 (Has goals):**

```
Great! Let's capture your strategic direction.

**Product Vision** (one sentence - where are you headed in 3-5 years?):
[User input]

**Top 3 Strategic Priorities** (for current quarter/period):
1. [User input]
2. [User input]
3. [User input]

**Key Success Metrics** (what metrics define success? optional):
1. [User input or "Skip"]
2. [User input or "Skip"]
3. [User input or "Skip"]

✓ Strategic goals captured
```

Create `.claude/product-context/strategic-goals.md`:

```markdown
# Strategic Goals

**Period:** [Current quarter/year]
**Last Updated:** [current date]

## Product Vision

[vision statement]

## Strategic Priorities

1. [priority 1]
2. [priority 2]
3. [priority 3]

## Key Success Metrics

[list metrics, or "To be defined"]
```

**If choice = 2 (Needs help):**

```
Perfect! I'll invoke product-strategist to help you develop vision and strategic goals.

Routing to product-strategist agent...
```

**Invoke product-strategist agent:**

```
Use the Task tool to invoke:

Task(
  subagent_type: "product-strategist",
  description: "Develop product vision and goals",
  prompt: "Help develop product vision and strategic goals for this product.

Product context:
- Name: [product name]
- Description: [product description]
- Stage: [product stage]
- Target Market: [target market]
- Value Prop: [value proposition]

Please help the user:
1. Craft a compelling 3-5 year product vision (one sentence)
2. Define 3 strategic priorities for the current quarter/period
3. Suggest 2-3 key success metrics to track

Focus on outcomes and strategic direction, not feature lists. Keep it concise and actionable.

When complete, format the output as:

# Strategic Goals

**Period:** [Current quarter/year]
**Last Updated:** [date]

## Product Vision

[vision statement]

## Strategic Priorities

1. [priority 1]
2. [priority 2]
3. [priority 3]

## Key Success Metrics

1. [metric 1]
2. [metric 2]
3. [metric 3]

Then save this to .claude/product-context/strategic-goals.md"
)
```

After agent completes:

```
✓ Vision and strategic goals developed with product-strategist
✓ Saved to strategic-goals.md
```

**If choice = 3 (Skip):**

```
Skipping strategic goals for now. You can add this later with:
/pm-setup --update
```

#### Optional: Business Metrics

If user selects option 2:

```
═══════════════════════════════════════════════════════════
Optional: Business Metrics
═══════════════════════════════════════════════════════════

Let's capture your current metrics (provide what you track, skip what you don't).

**User Metrics:**
- Total active users (MAU): [User input or "Skip"]
- User growth rate (% per month): [User input or "Skip"]

**Revenue Metrics** (if applicable):
- MRR or ARR: [User input or "Skip"]
- Revenue growth rate: [User input or "Skip"]

**Engagement:**
- Retention Day 30: [User input or "Skip"]
- Key engagement metric: [User input or "Skip"]

✓ Business metrics captured
```

Create `.claude/product-context/business-metrics.md`:

```markdown
# Business Metrics

**Last Updated:** [current date]

## User Metrics

[list provided metrics or "Not tracking yet"]

## Revenue Metrics

[list provided metrics or "Pre-revenue"]

## Engagement Metrics

[list provided metrics or "To be measured"]
```

#### Optional: Team Information

If user selects option 3:

```
═══════════════════════════════════════════════════════════
Optional: Team Information
═══════════════════════════════════════════════════════════

**Team Size:**
- Product/PM: [User input]
- Engineering: [User input]
- Design: [User input]
- Other: [User input or "0"]

**Work Cadence** (select one):
1. Solo builder (just me)
2. Scrum (2-week sprints)
3. Kanban (continuous flow)
4. Other

Your choice (1-4):
[User input]

**Velocity** (if you track it):
- Story points per sprint: [User input or "Not tracked"]
OR
- Features per month: [User input or "Not tracked"]

✓ Team info captured
```

Create `.claude/product-context/team-info.md`:

```markdown
# Team Information

**Last Updated:** [current date]

## Team Size

- Product/PM: [count]
- Engineering: [count]
- Design: [count]
- Other: [count]

**Total:** [sum] people

## Work Cadence

[cadence type and details]

## Velocity

[velocity info or "Not tracked"]
```

---

### Final Summary

Display completion summary:

```
═══════════════════════════════════════════════════════════
✅ Setup Complete!
═══════════════════════════════════════════════════════════

Context files created in .claude/product-context/:

Required:
✓ product-info.md - [Product Name] ([Stage])
✓ tech-stack.md - [Frontend] + [Backend] stack

[If optional files were created]:
Optional:
✓ strategic-goals.md - Vision and priorities [+ product-strategist ✨ if invoked]
✓ business-metrics.md - [Key metrics]
✓ team-info.md - [Team size] team

───────────────────────────────────────────────────────────

**Next: Start Your Product Journey**

Your agents will now work with your product context! As you progress through
stages, agents will create additional context files:

**Stage 1: Validation** (market-analyst)
→ Tell market-analyst: "Validate my [product] idea"
→ Creates: competitive-landscape.md (competitors, positioning)

**Stage 2: Understanding** (research-ops)
→ Tell research-ops: "Help me understand my users"
→ Creates: customer-segments.md (personas, pain points)

**Stage 3: Scoping** (feature-prioritizer)
→ Tell feature-prioritizer: "Help me scope my MVP"
→ Uses: All prior context for RICE scoring

**Stage 4: Speccing** (requirements-engineer)
→ Tell requirements-engineer: "Write a PRD for [feature]"
→ Uses: Tech stack, personas for specific specs

**Stage 5: Planning** (roadmap-builder)
→ Tell roadmap-builder: "Create a Now-Next-Later roadmap"
→ Creates: current-roadmap.md (Now/Next/Later)

**Stage 6: Launch** (launch-planner)
→ Tell launch-planner: "Plan my Product Hunt launch"
→ Uses: All context for targeted launch strategy

───────────────────────────────────────────────────────────

**Or use the orchestrator:**
→ Tell product-manager: "Help me validate my idea" (routes to market-analyst)
→ Tell product-manager: "Create a PRD for auth" (routes to requirements-engineer)

**Quick commands also available:**
→ /prd-generator - Write PRDs
→ /quick-prioritize - RICE scoring
→ /mvp-scoper - Scope MVP
→ /roadmap-builder - Create roadmaps

**Update context anytime:**
→ /pm-setup --update (refresh any file)
→ Edit files directly in .claude/product-context/
→ Recommended: Update quarterly (goals, metrics)

───────────────────────────────────────────────────────────

Ready to start? Tell product-manager or a specialist agent what you need!
```

---

## Update Mode

If user runs `/pm-setup --update`:

```
╔═══════════════════════════════════════════════════════════╗
║   Update Product Management Context                       ║
╔═══════════════════════════════════════════════════════════╝

Which files would you like to update?

Essential:
1. ⬜ product-info.md (last updated: [date])
2. ⬜ tech-stack.md (last updated: [date])

Optional:
3. ⬜ strategic-goals.md (last updated: [date]) [⚠️ if >3 months old]
4. ⬜ business-metrics.md (last updated: [date]) [⚠️ if >1 month old]
5. ⬜ team-info.md (last updated: [date])

Created by journey (usually updated by agents):
6. ⬜ competitive-landscape.md (last updated: [date])
7. ⬜ customer-segments.md (last updated: [date])
8. ⬜ current-roadmap.md (last updated: [date])

9. All files

Select files to update (comma-separated, e.g., "1,3" or "9" for all):
[User input]
```

For each selected file:

- Re-run that file's questions
- Show current values: `Current: [value]. Press Enter to keep, or type new value:`
- For strategic-goals: Offer product-strategist help again if updating
- Update only changed values
- Update "Last Updated" timestamp

---

## Validation

After each step, validate that essential information is provided:

**Essential per required file:**

- product-info.md: name, description, stage, target market, value prop (all required)
- tech-stack.md: frontend, backend, database, infrastructure, architecture (all required)

**For optional files:**

- strategic-goals.md: at least vision OR 3 priorities
- business-metrics.md: at least 2 metrics
- team-info.md: team size and cadence

If essential fields missing:

```
⚠️  Missing required information:
- [Field name]: [Brief explanation of why it's needed]

Would you like to:
1. Provide this information now
2. Cancel this file

Your choice (1/2):
```

---

## Error Handling

**If .claude/ directory doesn't exist:**

```bash
mkdir -p .claude/product-context
```

**If file write fails:**

```
❌ Error writing to [file_path]

Possible issues:
- Directory permissions
- Disk space

Would you like to:
1. Retry
2. Skip this file
3. Cancel setup

Your choice (1/2/3):
```

**If agent invocation fails** (for strategic-goals):

```
❌ Error invoking product-strategist agent

Falling back to manual input. Let's capture your strategic direction:

[Proceed with manual questions for strategic-goals]
```

**If user quits mid-setup:**

```
Setup incomplete. Files created so far:
✓ product-info.md
❌ tech-stack.md (not created)

Required files are incomplete. Please run /pm-setup again to finish.
```

---

## Related

**Context Architecture:**

- See `docs/context-architecture.md` for detailed specification
- Context files follow progressive disclosure pattern

**How Agents Use Context:**

- All agents read context files before asking questions
- Agents that create strategic artifacts save back to context
- Context accumulates through your product journey

**Update Frequency:**

- Required files (product-info, tech-stack): Update when fundamentals change
- Strategic goals: Update quarterly or when priorities shift
- Metrics: Update monthly if actively tracking growth
- Journey-created files: Updated by agents as insights evolve

**Progressive Context Building:**

- Setup creates INPUT files (what agents need to start)
- Journey creates OUTPUT files (what agents generate)
- Your context grows richer as you progress through stages
