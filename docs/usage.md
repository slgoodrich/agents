# Usage Guide

## Overview

This guide shows you how to use the Product Management Toolkit effectively. You'll learn conversational patterns, agent routing, context management, and best practices for solo developers and small teams.

---

## Getting Started

### Installation

```bash
# Install the complete toolkit
/plugin install ai-pm-copilot
```

That's it! You now have access to 9 agents, 16 skills, and 1 command.

### Initial Setup

Set up product context (recommended):

```bash
/ai-pm-copilot:pm-setup
```

This creates 8 context files in `.claude/product-context/` that all agents will reference, saving you from answering repetitive questions.

### Quick Test

Try a simple request to verify installation:

```
User: "Help me prioritize these 3 features: dark mode, API rate limiting, and mobile app"
```

The product-manager agent will route to feature-prioritizer and return scored results using RICE framework.

---

## Interaction Patterns

### Pattern 1: Conversational Requests (Primary)

**The main way to interact.** Just describe what you need naturally:

```
"Help me prioritize these features"
"Create a PRD for dark mode"
"Design user interviews for onboarding"
"Build a Q1 roadmap"
"Analyze our competitive position"
```

**How it works:**

1. product-manager agent receives your request
2. Analyzes intent and domain
3. Routes to appropriate specialist agent
4. Specialist loads relevant skills
5. Returns expert response

**Benefits:**

- Natural, conversational interface
- No need to memorize agent names
- Automatic expert selection
- Context-aware responses

**Best for:**

- Exploration and discovery
- Complex multi-faceted problems
- When unsure which agent to use
- Quick ad-hoc requests

### Pattern 2: Direct Agent Invocation

**For when you know exactly which specialist you need:**

**Syntax:**

```
Tell [agent-name]: "[your request]"
```

**Examples:**

```
Tell feature-prioritizer: "Score these 5 features using RICE"
Tell requirements-engineer: "Write a PRD for SSO integration"
Tell research-ops: "Design a usability test for checkout flow"
Tell roadmap-builder: "Create a Now-Next-Later roadmap"
Tell launch-planner: "Plan a beta program for Q2"
Tell market-analyst: "Analyze competitors in SaaS CRM space"
```

**Benefits:**

- Guaranteed routing to specific expert
- Bypass routing layer for speed
- Predictable behavior
- Good for repeated workflows

**Best for:**

- Known agent for the task
- Repeated workflows
- Specific expertise needed
- Complex multi-turn conversations with one specialist

### Pattern 3: Command Usage

**The toolkit has only ONE command:** pm-setup

**Usage:**

```bash
/ai-pm-copilot:pm-setup
```

**What it does:**

- Creates `.claude/product-context/` directory
- Generates 8 context files through interactive questions
- Sets up reusable product context for all agents

**When to use:**

- First-time setup after installation
- Major product changes (pivot, rebrand)
- Quarterly context refresh
- New team member onboarding

---

## Agent Routing

### How Routing Works

```
Your Request
↓
product-manager (routing agent)
↓
Analyzes keywords and intent:
- "prioritize" → feature-prioritizer
- "PRD" or "spec" → requirements-engineer
- "interview" or "research" → research-ops
- "roadmap" → roadmap-builder
- "launch" → launch-planner
- "competitive" or "market" → market-analyst
- "strategy" or "vision" → product-strategist
↓
Specialist Agent
↓
Loads relevant skills (if needed)
↓
Returns response
```

### Routing Keywords

**feature-prioritizer:**

- prioritize, score, rank, RICE, ICE, Kano
- value vs effort, cost of delay
- trade-off, backlog

**requirements-engineer:**

- PRD, spec, requirements, user story
- acceptance criteria, technical spec

**research-ops:**

- interview, survey, usability, research
- user testing, validation, discovery

**roadmap-builder:**

- roadmap, timeline, planning
- now-next-later, theme-based

**launch-planner:**

- launch, GTM, go-to-market
- beta, release, rollout

**market-analyst:**

- competitive, market, competitor
- positioning, SWOT, TAM/SAM/SOM

**product-strategist:**

- strategy, vision, positioning
- strategic, direction

### Bypass Routing

If routing isn't working as expected, invoke agents directly:

```
# Instead of relying on routing:
"Help me with feature prioritization"

# Invoke directly:
Tell feature-prioritizer: "Score these features"
```

---

## Context Management

### The Context System

The toolkit includes a context system that enables focused, streamlined conversations with agents.

**Context Files** (in `.claude/product-context/`):

1. **product-info.md** - Product name, description, target users, value prop
2. **metrics.md** - KPIs, current metrics, targets
3. **goals.md** - Business goals, product goals, success criteria
4. **roadmap.md** - Current roadmap, priorities, timeline
5. **tech-stack.md** - Technologies, architecture, integrations
6. **customers.md** - Customer segments, personas, use cases
7. **team.md** - Team structure, roles, constraints
8. **competitors.md** - Competitive landscape, differentiation

### Setting Up Context

**Initial setup:**

```bash
/ai-pm-copilot:pm-setup
```

Runs interactive wizard (15-20 minutes) to gather context.

**Update specific files:**

```bash
# Edit context files directly
vim .claude/product-context/metrics.md
vim .claude/product-context/roadmap.md
```

**Refresh context:**
Run pm-setup again quarterly or after major changes.

### How Agents Use Context

Every agent automatically:

1. Checks for context files first
2. Reads relevant information
3. Only asks for missing details
4. Generates product-specific outputs

**Without context:**

```
Tell requirements-engineer: "Write a PRD for API rate limiting"
→ Asks 10-15 questions about product, users, tech stack, goals, metrics...
```

**With context:**

```
Tell requirements-engineer: "Write a PRD for API rate limiting"
→ Reads product-info.md, metrics.md, tech-stack.md, customers.md
→ Generates PRD with 0-3 clarifying questions
→ Output is product-specific and high-quality
```

**Time savings:** 35-50 hours annually for active users

---

## Common Workflows

### Workflow 1: Feature Prioritization

```
1. Tell feature-prioritizer: "I have 8 features to prioritize:
   [list features]"

2. Agent asks for scoring inputs (reach, impact, confidence, effort)

3. Returns scored features with RICE scores and rationale

4. Optional: "Now compare using Kano model"
```

**Skills used:** prioritization-methods

### Workflow 2: PRD Creation

```
1. Tell requirements-engineer: "Write a PRD for [feature name]"

2. Agent reads product context

3. Asks 2-3 clarifying questions about feature specifics

4. Generates structured PRD using prd-templates skill

5. Optional: "Add technical implementation section"
```

**Skills used:** prd-templates, specification-techniques

### Workflow 3: User Research Planning

```
1. Tell research-ops: "Plan user interviews for [topic]"

2. Agent designs interview guide using interview-frameworks skill

3. Returns: research goals, screening criteria, questions, synthesis plan

4. Optional: "Add a usability test plan too"
```

**Skills used:** interview-frameworks, user-research-techniques

### Workflow 4: Roadmap Planning

```
1. Tell roadmap-builder: "Create a Now-Next-Later roadmap"

2. Agent reads context (goals.md, roadmap.md if exists)

3. Asks about priorities and timeline

4. Returns structured roadmap with themes and initiatives

5. Optional: "Convert to quarter-based timeline"
```

**Skills used:** roadmap-frameworks

### Workflow 5: Launch Planning

```
1. Tell launch-planner: "Plan a Q2 product launch"

2. Agent asks about launch tier, audience, goals

3. Returns comprehensive launch plan:
   - Timeline and milestones
   - GTM strategy
   - Cross-functional coordination
   - Success metrics

4. Optional: "Add a beta program plan"
```

**Skills used:** launch-planning-frameworks, go-to-market-playbooks

### Workflow 6: Competitive Analysis

```
1. Tell market-analyst: "Analyze our competitive position"

2. Agent reads competitors.md context

3. Asks for specific competitors to analyze

4. Returns SWOT analysis, positioning recommendations

5. Optional: "Calculate TAM/SAM/SOM for our market"
```

**Skills used:** competitive-analysis-templates, product-positioning, market-sizing-frameworks

### Workflow 7: Multi-Agent Collaboration

For complex scenarios, chain multiple agents:

```
1. Tell market-analyst: "Research competitive positioning"
   → Returns market analysis

2. Tell product-strategist: "Based on that analysis, suggest strategy"
   → Returns strategic recommendations

3. Tell roadmap-builder: "Create roadmap for that strategy"
   → Returns roadmap aligned with strategy

4. Tell requirements-engineer: "Write PRD for first roadmap item"
   → Returns detailed PRD
```

---

## Best Practices

### 1. Set Up Context First

Run `/ai-pm-copilot:pm-setup` before heavy usage:

- Saves time on every interaction
- Improves output quality
- Reduces repetitive questions

### 2. Be Specific in Requests

**Better:**

```
Tell feature-prioritizer: "Score these 5 features using RICE:
1. Dark mode - estimated 10K users affected
2. API rate limiting - prevents abuse
3. SSO integration - enterprise requirement
4. Mobile app - 30% of users request it
5. Advanced reporting - requested by top 5 customers"
```

**Worse:**

```
"prioritize features"
```

### 3. Use Direct Invocation for Complex Work

For multi-turn conversations with one specialist:

```
Tell requirements-engineer: "Write a PRD for SSO integration"
→ Agent returns PRD

"Add edge cases for failed authentication"
→ Agent updates PRD

"Include integration testing requirements"
→ Agent adds testing section
```

### 4. Reference Context Files

Remind agents of context when needed:

```
Tell roadmap-builder: "Create Q2 roadmap based on goals in goals.md"
Tell launch-planner: "Plan launch targeting customers in customers.md"
```

### 5. Iterate with Follow-ups

Agents maintain conversation context:

```
"Create a roadmap"
→ Agent returns roadmap

"Make it more aggressive"
→ Agent adjusts timeline

"Add dependencies between initiatives"
→ Agent enhances roadmap with sequencing details
```

### 6. Leverage Skills Explicitly

Request specific frameworks:

```
Tell feature-prioritizer: "Use Kano model instead of RICE"
Tell research-ops: "Design interviews using Jobs-to-be-Done framework"
Tell launch-planner: "Use product-led growth strategy"
```

### 7. Update Context Regularly

Keep context files current:

- Update metrics.md monthly
- Update roadmap.md quarterly
- Update goals.md when goals change
- Update competitors.md when market shifts

---

## Getting the Most from Agents

### Maximize Context Quality

Run pm-setup to provide agents with product context for more specific, actionable outputs.

### Get More Specific Outputs

Tips for better results:

- Add rich context files in `.claude/product-context/`
- Be specific in your requests
- Reference actual data and examples in prompts

### Control Agent Selection

Direct agent invocation when you know exactly what you need:

```
Tell feature-prioritizer: "Score these 5 features with RICE"
Tell roadmap-builder: "Create now-next-later roadmap"
```

### Provide Context in Requests

Include relevant information directly:

```
"Based on [feature description], create PRD"
"Given our roadmap focus on retention, prioritize these features"
```

### Choose Your Framework

Request specific methodologies:

```
Tell feature-prioritizer: "Use ICE instead of RICE"
Tell roadmap-builder: "Use theme-based instead of timeline-based"
```

---

## Tips & Tricks

### Tip 1: Chain Agents

```
"Research competitive positioning, then suggest strategy, then create roadmap"
```

product-manager will orchestrate across market-analyst, product-strategist, and roadmap-builder.

### Tip 2: Export for Sharing

```
Tell requirements-engineer: "Write PRD and format as markdown for Notion"
```

### Tip 3: Compare Approaches

```
Tell feature-prioritizer: "Score with RICE, then compare with Kano"
```

### Tip 4: Iterate Quickly

```
"Create PRD" → "Make it shorter" → "Add API section" → "Export as table"
```

### Tip 5: Use Context for Consistency

All agents read same context = consistent outputs across workflows

---

## Related Documentation

- [Agents Guide](agents.md) - Detailed agent documentation
- [Skills Reference](agent-skills.md) - Complete skills catalog
- [Architecture](architecture.md) - System design and patterns
- [Plugin Guide](plugins.md) - Installation and management

---

**Components**: 9 agents, 1 command, 16 skills
**Target Audience**: Solo developers and small teams
**Last Updated**: October 2025
