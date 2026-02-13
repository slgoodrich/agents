# Context Architecture for PM Toolkit

**Date**: 2025-10-28
**Status**: Specification

---

## Overview

This document defines the **context architecture** for the Product Management Toolkit - a standardized approach to gathering, storing, and reusing product/business context across all agents and skills.

### Benefits

The `.claude/product-context/` architecture provides:

- **One-time setup**: 15-20 minutes via `/pm-setup` creates reusable context
- **Fewer questions**: Agents read context files first, ask only for gaps
- **Better outputs**: Product-specific results instead of generic outputs
- **Workflow efficiency**: Context gathered once in Phase 0, reused across all phases
- **Universal reuse**: Same context files power all PM tools

---

## Context Directory Structure

### Core Files (Created by /pm-setup)

The `/ai-pm-copilot:pm-setup` command creates these 8 required context files:

```
project-root/
  .claude/
    product-context/
      product-info.md             # Product description, value prop, users
      business-metrics.md         # ARR, users, growth, key metrics
      strategic-goals.md          # Goals, priorities, strategic themes
      current-roadmap.md          # Now-Next-Later roadmap
      tech-stack.md               # Architecture, tech stack, constraints
      customer-segments.md        # Personas, ICP, segments
      team-info.md                # Team size, roles, constraints
      competitive-landscape.md    # Competitors, market position
```

### Suggested Optional Structure

You can add additional context files and directories as needed. These are examples, not required:

```
project-root/
  .claude/
    product-context/
      # Optional supplementary files (examples)
      gtm-strategy.md             # GTM approach, positioning, messaging
      stakeholder-map.md          # Key stakeholders, decision-makers
      org-chart.md                # Organizational structure
      platform-strategy.md        # Platform vision, ecosystem
      pricing-model.md            # Pricing tiers, monetization

  # Suggested directories for project artifacts
  prds/                           # Product Requirements Documents
    [feature-name].md             # Kebab-case, no PRD- prefix

  research/                       # User research artifacts
    interviews/
      YYYY-MM-DD-participant-description.md
    surveys/
      YYYY-MM-DD-survey-name.md
    feedback/
      customer-feedback.md
    previous-studies.md

  analytics/                      # Metrics and data
    current-metrics.md
    growth-metrics.md
    experiments/
      history.md
      active-experiments.md

  launches/                       # Launch history
    previous-launches.md

  backlog.md                      # Current backlog

  tech-debt/                      # Technical debt
    inventory.md

  incidents/                      # Incident history
    history.md

  processes/                      # Team processes
    current-processes.md

  docs/                           # Technical documentation
    architecture.md
    api-specs/
```

---

## Core Context Files (8 Required)

### 1. product-info.md

**Used By**: All agents
**Purpose**: Foundational product description and context

**Key Sections**:

- Product name and description
- Value proposition
- Target users and market
- Product stage (idea/MVP/PMF/growth/mature)
- Key features and capabilities
- Technology overview

---

### 2. business-metrics.md

**Used By**: All agents
**Purpose**: Current business performance and key metrics

**Key Sections**:

- Revenue metrics (ARR, MRR, growth rate)
- User metrics (total users, active users, growth)
- Engagement metrics (DAU/MAU, retention, churn)
- Product metrics (activation rate, time to value)
- Financial metrics (CAC, LTV, unit economics)
- Baseline dates for all metrics

---

### 3. strategic-goals.md

**Used By**: All agents
**Purpose**: Company and product strategic direction

**Key Sections**:

- Company goals (current quarter/year)
- Product goals (current quarter/year)
- Strategic themes and priorities
- Key initiatives
- Success criteria and targets

---

### 4. current-roadmap.md

**Used By**: All agents
**Purpose**: Product roadmap and planned work

**Key Sections**:

- NOW (0-3 months) - Active work
- NEXT (3-6 months) - Planned work
- LATER (6+ months) - Exploration
- Strategic themes mapping
- Not on roadmap (explicitly deprioritized)

---

### 5. tech-stack.md

**Used By**: All agents
**Purpose**: Technical architecture and constraints

**Key Sections**:

- Architecture overview (frontend, backend, infrastructure)
- Tech stack (languages, frameworks, services)
- Key integrations and dependencies
- Technical constraints
- Technical debt overview

---

### 6. customer-segments.md

**Used By**: All agents
**Purpose**: Customer understanding and segmentation

**Key Sections**:

- Customer personas (3-5 key personas)
- Ideal Customer Profile (ICP)
- Segment definitions (by size, industry, use case)
- User needs and pain points by segment
- Buying process and decision-makers

---

### 7. team-info.md

**Used By**: All agents
**Purpose**: Team composition and context

**Key Sections**:

- Team size and composition (roles, seniority)
- Team constraints and dependencies
- Key skills and expertise
- Working patterns and availability

---

### 8. competitive-landscape.md

**Used By**: All agents
**Purpose**: Market and competitive intelligence

**Key Sections**:

- Top 3-5 competitors
- Competitive positioning
- Our differentiation
- Competitive threats and opportunities
- Market trends and dynamics

---

## How Agents Use Context

### Pattern 1: Direct File Reading (Agents)

Agents should first **attempt to read context files**, then ask for missing information:

```markdown
## Context Gathering

**Step 1: Read Context Files**

Attempt to read:

- `.claude/product-context/product-info.md`
- `.claude/product-context/business-metrics.md`
- `.claude/product-context/strategic-goals.md`
- [agent-specific files]

**Step 2: Extract Relevant Information**

From context files, extract:

- [Field 1]
- [Field 2]
- [Field 3]

**Step 3: Identify Gaps**

Check if required information is present. If missing:

- [Question 1 if Field 1 missing]
- [Question 2 if Field 2 missing]
- [Question 3 if Field 3 missing]

**Step 4: Proceed with Task**

Use gathered context + user input to complete task.
```

**Example** (requirements-engineer agent):

```
Step 1: Read `.claude/product-context/product-info.md`, `tech-stack.md`, `customer-segments.md`
Step 2: Extract: product description, target users, tech stack, architecture
Step 3: Missing: Specific feature requirements → Ask user "What specific feature are you building?"
Step 4: Generate PRD with full product context + specific feature details
```

---

### Pattern 2: Context Parameter (Commands)

Commands should accept context files as input, fall back to questions:

```markdown
## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Context

**Attempt to read context files**:

- `.claude/product-context/product-info.md`
- `.claude/product-context/business-metrics.md`
- [command-specific files]

**If files exist**: Use data from files
**If files missing**: Ask user these questions:

- [Question 1]
- [Question 2]
- [Question 3]

### 2. Execute Command

[Command logic using context]
```

---

### Pattern 3: Phase 0 Context Gathering (Workflows)

All workflows should start with Phase 0 for comprehensive context gathering:

```markdown
## Phase 0: Context Gathering (5-10 minutes)

Before starting the workflow, gather all essential context.

### Step 1: Check for Context Files

Attempt to read required context files:

- `.claude/product-context/product-info.md` ✅/❌
- `.claude/product-context/business-metrics.md` ✅/❌
- `.claude/product-context/strategic-goals.md` ✅/❌
- `.claude/product-context/current-roadmap.md` ✅/❌
- [workflow-specific files]

### Step 2: Validate Completeness

For each file found, check if it contains required fields:

- product-info.md: product_name, stage, target_users, value_proposition
- business-metrics.md: arr, total_users, growth_rate
- strategic-goals.md: current_goals, priorities

### Step 3: Gather Missing Context

**If files missing or incomplete**, gather from user:

#### Essential Context (always required):

1. Product: [If product-info.md missing] "What product is this for? Describe in 2-3 sentences."
2. Stage: [If stage missing] "What stage? (idea/MVP/PMF/growth/mature)"
3. Goals: [If strategic-goals.md missing] "What are your top 3 strategic priorities this quarter?"
4. Metrics: [If business-metrics.md missing] "What are your key metrics? (ARR, users, growth rate)"

#### Workflow-Specific Context:

[Questions specific to this workflow]

### Step 4: Save Context for Reuse

For any information gathered from user:
```

Create/update context files:

- If product info gathered → update .claude/product-context/product-info.md
- If metrics gathered → update .claude/product-context/business-metrics.md
- If goals gathered → update .claude/product-context/strategic-goals.md

```

**Benefit**: Future workflows won't need to ask these questions again.

### Step 5: Package Context for Phases

Create comprehensive context object with all gathered information:
```

CONTEXT = {
product: [from product-info.md or user],
metrics: [from business-metrics.md or user],
goals: [from strategic-goals.md or user],
roadmap: [from current-roadmap.md or user],
team: [from team-info.md or user],
[workflow-specific context]
}

```

### Step 6: Checkpoint

Display context summary:
```

# Context Gathered:

Product: [product_name] - [stage]
Users: [total_users], ARR: [arr]
Strategic Focus: [top_priority]
[Workflow-specific context]

✅ Context saved to .claude/product-context/ for future reuse

Proceed to Phase 1? (yes/no)

````

---

## Phase 1+ Agent Invocations

All agent invocations in workflows should receive FULL context:

```markdown
## Phase [N]: [Phase Name]

**Agent**: `agent-name`

**Task**: Use Task tool to invoke agent:

````

subagent_type: "plugin-name::agent-name"
description: "[5-word description]"
prompt: "[Agent-specific instruction]

**CONTEXT** (from Phase 0):

**Product**:
[Insert product info from Phase 0]

**Business Metrics**:
[Insert metrics from Phase 0]

**Strategic Goals**:
[Insert goals from Phase 0]

**Current Roadmap**:
[Insert roadmap from Phase 0]

**Team Info**:
[Insert team info from Phase 0]

**Previous Phase Output**:
[Insert output from Phase N-1]

**Your Task**:
[Specific instruction for this phase]"

```

**Key**: Agent gets BOTH broad context (product, metrics, goals) AND specific input (previous phase output).
```

---

## Context File Maintenance

### When to Update

Context files should be updated:

- **Quarterly**: Strategic goals, roadmap, metrics baselines
- **Monthly**: Business metrics, team info
- **As needed**: Tech stack, competitive landscape, customer segments

### How to Update

**Option 1**: Edit files directly

```bash
# Open in editor
vi .claude/product-context/business-metrics.md

# Update metrics section
# Save and close
```

**Option 2**: Use `/pm-setup --update` command

```bash
# Interactive update of context files
/pm-setup --update

# Will prompt for updates to each file
```

**Option 3**: Inline during workflows
When workflows detect stale context, they can prompt:

```
⚠️  business-metrics.md last updated 3 months ago
Update metrics now? (yes/no)
```

---

## Best Practices

### 1. Start with `/pm-setup`

Before using PM tools extensively, run:

```bash
/pm-setup
```

This creates all 8 core context files with guided prompts (15-20 minutes one-time setup).

### 2. Keep Context Current

Set calendar reminders:

- Weekly: Update business metrics
- Monthly: Update roadmap and team info
- Quarterly: Update strategic goals

### 3. Don't Duplicate Context

If context exists in docs/ or elsewhere, reference it:

```markdown
# In .claude/product-context/tech-stack.md

## Architecture

See detailed architecture in `docs/architecture.md`

**Summary**: Microservices architecture with React frontend, Node.js backend, PostgreSQL database
```

### 4. Version Control Context Files

Add to `.gitignore` if context contains sensitive data:

```gitignore
# In .gitignore
.claude/product-context/business-metrics.md  # Contains revenue data
.claude/product-context/competitive-landscape.md  # Contains competitive intel
```

Or commit if sharable within team:

```bash
git add .claude/product-context/
git commit -m "Update Q4 strategic goals and roadmap"
```

---

## Implementation Guide

### For Existing Projects

**Step 1**: Run context setup

```bash
/pm-setup
```

**Step 2**: Test with an agent

```bash
Tell requirements-engineer: "Write a PRD for dark mode feature"
# Should read product-info.md and ask fewer questions
```

**Step 3**: Iterate and refine
Update context files based on what questions still get asked frequently.

---

### For New Projects

**Step 1**: Initialize project with Claude Code

```bash
cd my-new-product
claude-code init
```

**Step 2**: Set up PM context

```bash
/pm-setup
```

**Step 3**: Start using PM tools
All agents and skills will have rich context immediately.

---

## Value Delivered

### Performance with Context Architecture

- **Questions per agent request**: 0-3 (only for missing details)
- **Questions per workflow**: 5-10 (phase-specific only)
- **Setup time**: 15-20 min (one-time investment)
- **Output quality**: Product-specific, immediately actionable
- **User experience**: Streamlined, focused conversations

### Time Efficiency

- **Per agent interaction**: 5-10 min saved vs. answering repeated questions
- **Per multi-agent workflow**: 15-20 min saved
- **Weekly usage** (4 workflows): 60-80 min saved
- **Annual impact**: 50-70 hours available for product work

---

## Related Documentation

- [README](../README.md) - Toolkit overview
- [Architecture](./architecture.md) - System design and patterns
- [Agents Guide](./agents.md) - Complete agent reference
- [Skills Reference](./agent-skills.md) - Framework knowledge catalog

---

## Version History

- **Initial Release** (2025-10-28): Context architecture specification
