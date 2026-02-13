# Agent Reference

## Overview

The Product Management Toolkit provides **9 AI agents** covering the complete PM lifecycle: 1 orchestrator, 7 PM specialists, and 1 utility agent. Most PM specialists use Claude Opus for deep strategic reasoning, with Sonnet for routing and structured output tasks, and Haiku for efficient utility operations.

**Agent-First Architecture:** Conversational PM through specialized agents instead of command memorization. The `product-manager` agent acts as an intelligent router, directing requests to appropriate specialists.

---

## Quick Reference

| Agent                     | Specialty                            | Primary Use Cases                                                  |
| ------------------------- | ------------------------------------ | ------------------------------------------------------------------ |
| **product-manager**       | Routing & orchestration              | General PM guidance, multi-faceted problems, workflow coordination |
| **market-analyst**        | Competitive intelligence             | Market research, positioning, TAM/SAM/SOM, competitive analysis    |
| **research-ops**          | User research                        | Interviews, usability testing, validation, feedback synthesis      |
| **product-strategist**    | Strategy & vision                    | Goals, product vision, strategic roadmaps, North Star metrics      |
| **roadmap-builder**       | Roadmap planning                     | Now-Next-Later roadmaps, quarterly planning, feature sequencing    |
| **feature-prioritizer**   | Prioritization                       | RICE/ICE scoring, Kano analysis, trade-off decisions               |
| **requirements-engineer** | Specifications                       | PRDs, technical specs, user stories, acceptance criteria           |
| **launch-planner**        | Go-to-market                         | Launch planning, GTM strategy, beta programs, launch execution     |
| **context-scanner**       | Codebase context discovery (utility) | Auto-discover features, tech stack, integrations during setup      |

---

## Agent Routing Pattern

### The product-manager Agent

The **product-manager** agent is your primary entry point - an intelligent router that:

1. **Analyzes requests** to identify PM discipline(s) needed
2. **Routes to specialists** automatically (research-ops, feature-prioritizer, etc.)
3. **Coordinates workflows** when multiple specialists are needed
4. **Synthesizes outputs** into cohesive recommendations

**When to use product-manager:**

- Unsure which specialist to consult
- Multi-faceted problems (e.g., "validate and prioritize feature X")
- General PM guidance and questions
- Complex workflows requiring multiple specialists

**When to bypass:**

- You know exactly which specialist you need
- Simple, focused requests
- Direct conversation with a specialist

**Routing examples:**

```
Tell product-manager: "Help me prioritize features"
→ Routes to feature-prioritizer

Tell product-manager: "Validate this feature idea and create a launch plan"
→ Routes to research-ops, then launch-planner
→ Synthesizes complete validation + GTM plan

Tell product-manager: "I need to plan Q2"
→ Routes to product-strategist for goals
→ Routes to roadmap-builder for roadmap
→ Routes to feature-prioritizer for backlog
→ Synthesizes complete quarterly plan
```

**Direct invocation (bypasses routing):**

```
Tell feature-prioritizer: "Score these 10 features with RICE"
Tell research-ops: "Design a churn study"
Tell roadmap-builder: "Create now-next-later roadmap"
```

---

## PM Specialist Agents

### 1. product-manager (Orchestrator)

**Specialty:** Intelligent routing and workflow orchestration
**Model:** Sonnet

**Core Purpose:**
Central coordination point that routes requests to appropriate specialist agents and orchestrates complex multi-agent workflows.

**Use for:**

- General PM questions ("What should I focus on for Q1?")
- Multi-faceted problems requiring multiple specialists
- When unsure which specialist to consult
- Complex workflows (validate → prioritize → plan → launch)
- Synthesis of multiple specialist perspectives

**Routing Capabilities:**

- Identifies PM disciplines needed from request
- Routes to appropriate specialist(s)
- Coordinates sequential workflows
- Synthesizes outputs from multiple agents
- Provides unified recommendations

**Example Interactions:**

**Simple routing:**

```
User: "Tell product-manager: I need to prioritize 10 features for Q2"
→ Routes to feature-prioritizer
→ Returns prioritized backlog with RICE scores
```

**Complex workflow:**

```
User: "Tell product-manager: Validate this feature idea, prioritize it, and plan delivery"
→ Routes to research-ops for validation study
→ Routes to feature-prioritizer for RICE scoring
→ Routes to requirements-engineer for PRD
→ Routes to roadmap-builder for timeline
→ Synthesizes complete feature plan
```

**Strategic guidance:**

```
User: "Tell product-manager: Help me figure out what to build for our SaaS product"
→ Routes to market-analyst for competitive landscape
→ Routes to research-ops for user needs
→ Routes to product-strategist for strategic direction
→ Synthesizes recommendations with priorities
```

---

### 2. market-analyst

**Specialty:** Market research, competitive analysis, and positioning
**Model:** Opus

**Use for:**

- Competitive landscape analysis
- Market sizing (TAM/SAM/SOM)
- Product positioning and differentiation
- Win/loss analysis
- Competitor feature comparison
- Market opportunity assessment
- Industry trend analysis

**Knowledge areas:**

- Competitive analysis frameworks (Porter's Five Forces, SWOT)
- April Dunford positioning methodology
- Market sizing techniques
- Industry research methods
- Competitive intelligence
- Market segmentation

**Example use:**

```
Tell market-analyst: "Analyze how we should position against Asana, Monday, and Linear"
Tell market-analyst: "Calculate TAM/SAM/SOM for project management software in North America"
Tell market-analyst: "Research competitive pricing strategies in the analytics space"
```

**Activates skills:**

- product-positioning
- competitive-analysis-templates
- market-sizing-frameworks

---

### 3. research-ops

**Specialty:** User research, interviews, usability testing, and validation
**Model:** Opus

**Use for:**

- User interview planning and execution
- Usability testing design
- Problem/solution validation
- Customer feedback synthesis
- Research study design
- Interview guide creation
- Research program management

**Knowledge areas:**

- User research methodologies (interviews, surveys, usability tests)
- Teresa Torres continuous discovery
- Jobs-to-be-Done framework
- Research synthesis techniques
- Usability testing (Nielsen heuristics)
- Validation frameworks (Lean Startup)

**Example use:**

```
Tell research-ops: "Design a study to understand why 30% of users churn after 30 days"
Tell research-ops: "Create an interview guide for validating this feature hypothesis"
Tell research-ops: "Synthesize these 20 interview transcripts and identify top insights"
```

**Activates skills:**

- user-research-techniques
- interview-frameworks
- synthesis-frameworks
- usability-frameworks
- validation-frameworks

---

### 4. product-strategist

**Specialty:** Product vision, strategy, and goals
**Model:** Opus

**Use for:**

- Product vision and strategy development
- Quarterly and annual goal creation
- Strategic roadmaps
- North Star metric definition
- Strategic trade-off decisions
- Product positioning
- Board and executive presentations

**Knowledge areas:**

- Goal-setting methodology (Google, Doerr)
- Strategic frameworks (DHM model, Playing to Win)
- North Star framework
- Product-led growth strategy
- Jobs-to-be-Done for strategy
- Vision/mission crafting

**Example use:**

```
Tell product-strategist: "Create Q2 2025 goals focused on achieving product-market fit"
Tell product-strategist: "Develop a 3-year product vision for our B2B SaaS platform"
Tell product-strategist: "Help me decide: should we expand to enterprise or improve SMB product?"
```

**Activates skills:**

- product-positioning
- roadmap-frameworks

---

### 5. roadmap-builder

**Specialty:** Roadmap planning and feature sequencing
**Model:** Opus

**Use for:**

- Now-Next-Later roadmaps
- Theme-based roadmaps
- Quarterly planning
- Feature sequencing and dependencies
- Roadmap communication
- Backlog organization
- Release planning

**Knowledge areas:**

- Now-Next-Later framework
- Outcome-based roadmaps
- Theme-based planning
- Release planning
- Roadmap communication
- Dependency management

**Example use:**

```
Tell roadmap-builder: "Create a 6-month now-next-later roadmap for our mobile app"
Tell roadmap-builder: "Plan Q1 2025 with focus on retention and enterprise features"
Tell roadmap-builder: "Build a theme-based roadmap around our North Star metric"
```

**Activates skills:**

- roadmap-frameworks

---

### 6. feature-prioritizer

**Specialty:** RICE/ICE scoring and prioritization frameworks
**Model:** Opus

**Use for:**

- RICE scoring (Reach, Impact, Confidence, Effort)
- ICE scoring (Impact, Confidence, Ease)
- Kano model analysis
- Value vs Effort matrices
- Trade-off decisions
- Backlog ranking
- Opportunity scoring

**Knowledge areas:**

- RICE framework (Intercom)
- ICE framework (Sean Ellis)
- Kano model
- Value vs Effort
- MoSCoW prioritization
- Cost of delay
- Opportunity scoring

**Example use:**

```
Tell feature-prioritizer: "Score these 10 features using RICE framework"
Tell feature-prioritizer: "Help me decide between feature A and feature B"
Tell feature-prioritizer: "Use Kano model to categorize these 20 feature requests"
```

**Activates skills:**

- prioritization-methods

---

### 7. requirements-engineer

**Specialty:** PRDs, technical specs, and user stories
**Model:** Sonnet

**Use for:**

- Product requirements documents (PRDs)
- Technical specifications
- User story writing
- Acceptance criteria
- Edge case documentation
- Feature specifications
- Requirements traceability

**Knowledge areas:**

- PRD structure and best practices
- User story mapping (Jeff Patton)
- Acceptance criteria (Given/When/Then)
- BDD (Behavior-Driven Development)
- INVEST criteria
- Specification techniques
- Edge case analysis

**Example use:**

```
Tell requirements-engineer: "Write a comprehensive PRD for dark mode feature"
Tell requirements-engineer: "Break this PRD into user stories with acceptance criteria"
Tell requirements-engineer: "Document all edge cases for SSO integration"
```

**Activates skills:**

- specification-techniques
- prd-templates
- user-story-templates

---

### 8. launch-planner

**Specialty:** Go-to-market planning and launch execution
**Model:** Opus

**Use for:**

- Product launch planning
- GTM strategy development
- Beta program design
- Launch messaging and positioning
- Launch timeline and milestones
- Success metrics
- Launch coordination

**Knowledge areas:**

- GTM frameworks
- Launch tiers (soft, limited, full)
- Beta program management
- Product marketing
- Launch checklists
- Launch metrics
- Positioning (April Dunford)

**Example use:**

```
Tell launch-planner: "Create a beta launch plan for our API product"
Tell launch-planner: "Design a 12-week launch plan for enterprise tier"
Tell launch-planner: "Help me position this feature for maximum impact"
```

**Activates skills:**

- launch-planning-frameworks

---

## Multi-Agent Workflows

### Sequential Pattern

Agents work one after another, passing context forward.

**Example: Feature Development**

```
1. research-ops → Validate user need
2. product-strategist → Align with strategy
3. requirements-engineer → Write comprehensive PRD
4. feature-prioritizer → Score against backlog
5. roadmap-builder → Plan timeline
6. launch-planner → Prepare GTM
```

### Parallel Pattern

Multiple agents work simultaneously on different aspects.

**Example: Quarterly Planning**

```
In parallel:
- market-analyst → Competitive landscape
- research-ops → User needs research
- product-strategist → Draft goals

Then synthesize:
- roadmap-builder → Create quarterly roadmap with all inputs
```

### Iterative Pattern

Agents refine each other's work through multiple passes.

**Example: PRD Refinement**

```
Round 1: requirements-engineer → Draft PRD
Round 2: research-ops → Validate with customers
Round 3: requirements-engineer → Incorporate feedback
Round 4: feature-prioritizer → Confirm priority
Round 5: roadmap-builder → Finalize timeline
```

---

## Model Configuration

Agents use a tiered model strategy based on task complexity:

**Claude Opus** (6 agents) - Deep strategic reasoning, nuanced judgment, creative synthesis:
- market-analyst, research-ops, product-strategist, roadmap-builder, feature-prioritizer, launch-planner

**Claude Sonnet** (2 agents) - Routing, pattern matching, structured output:
- product-manager (orchestrator), requirements-engineer

**Claude Haiku** (1 agent) - Fast file operations, data extraction:
- context-scanner (utility)

---

## Choosing the Right Agent

### By PM Activity

**Strategic Planning** → product-strategist, market-analyst
**Research & Discovery** → research-ops, market-analyst
**Planning & Prioritization** → roadmap-builder, feature-prioritizer
**Requirements & Specs** → requirements-engineer
**Launch & GTM** → launch-planner, market-analyst
**General Guidance** → product-manager (routes to specialists)

### By Question Type

**"Should we build this?"** → research-ops, feature-prioritizer, product-strategist
**"What should we build?"** → market-analyst, research-ops, product-strategist
**"When should we build it?"** → roadmap-builder, feature-prioritizer
**"How should we build it?"** → requirements-engineer
**"How do we launch it?"** → launch-planner

### By Output Type

**PRD / Specs** → requirements-engineer
**Goals** → product-strategist
**Roadmap** → roadmap-builder
**Prioritized Backlog** → feature-prioritizer
**Research Plan** → research-ops
**Launch Plan** → launch-planner
**Market Analysis** → market-analyst

---

## Utility Agents

Utility agents perform specialized operational tasks to support PM agents. They are not domain experts but provide essential capabilities that enable faster, more accurate PM work.

### 9. context-scanner

**Specialty:** Strategic context discovery from codebase
**Model:** Haiku (optimized for file operations)

**Core Purpose:**
Automatically discovers strategic product context from existing codebases to populate `.claude/product-context/` files during setup. Enables fast, accurate onboarding on existing projects.

**What it discovers:**

- **Features:** User-facing functionality from routes, pages, API endpoints
- **Tech Stack:** Frontend/backend frameworks, databases, languages from package manifests
- **Integrations:** 3rd party services from package dependencies (Stripe, SendGrid, etc.)
- **Scale:** Project size (files, LOC), complexity, maturity level

**What it doesn't do:**

- Code quality or architecture analysis (engineering territory)
- Performance or security assessment
- Technical recommendations or best practices
- Business logic analysis

**Key principle:** Facts not interpretation - reports WHAT exists, not HOW it's built or WHETHER it's good.

**Invoked by:**

- pm-setup command (during initial setup or refresh)
- market-analyst (when needing current feature inventory for competitive analysis)
- feature-prioritizer (when identifying gaps for prioritization)
- Any PM agent needing current product state

**Example flow (automatic invocation):**

```
User runs: /product-management:pm-setup

pm-setup detects codebase:
"I've detected an existing codebase. Scan to auto-discover context? (yes/no)"

User: yes

pm-setup invokes context-scanner via Task tool:
→ context-scanner scans file structure, package.json, routes, etc. using Read/Glob/Grep
→ context-scanner presents findings as structured markdown to user
→ All findings include evidence and confidence scores

context-scanner presents findings to user:
"Discovered from Codebase:
✓ Authentication (login, signup) [High confidence]
✓ Projects (CRUD operations) [High confidence]
✓ Analytics [Medium confidence - please verify]

Tech Stack:
Frontend: React 18.2, TypeScript 5.0
Backend: Node.js 20, Express 4.18
Database: PostgreSQL

Integrations:
- Stripe (payments)
- SendGrid (email)

Is this accurate?"

User validates (confirms, corrects, adds missing items)

context-scanner saves validated data to context files using Write tool:
- current-features.md (NEW FILE)
- tech-stack.md (UPDATED)
- product-info.md (UPDATED)

Control returns to pm-setup to continue setup workflow

Time saved: 10-15 minutes vs manual entry
```

**Example flow (invoked by PM agent):**

```
User: "Tell market-analyst: How do we compare to competitors?"

market-analyst checks if current-features.md exists and is recent:
→ If missing/stale: Invokes context-scanner via Task tool
→ context-scanner scans, user validates, saves current-features.md
→ Control returns to market-analyst
→ market-analyst reads current-features.md
→ Uses for competitive comparison
→ Returns: "You have core PM features (auth, projects, tasks) but lack timeline view, resource management, and portfolio features that Asana and Monday.com offer..."
```

**How it works:**

1. Scans codebase using Read/Glob/Grep tools
2. Organizes findings internally (features, tech stack, integrations, scale)
3. Presents findings as **structured markdown** to user
4. Requests user validation (confirm/add/remove/correct)
5. Saves validated data to context files using Write tool

**What it discovers:**

- Features (from routes, pages, API endpoints)
- Tech stack (from package.json, requirements.txt, etc.)
- Integrations (from 3rd party packages)
- Project scale (files, approximate LOC, complexity)
- All findings include evidence (file paths) and confidence scores (high/medium/low)

**Validation required:**
All discoveries must be confirmed by user before saving to context files. This prevents hallucination and ensures accuracy.

**Differences from PM specialists:**

- **Model:** Haiku (fast, efficient file operations) vs Opus/Sonnet (strategic reasoning)
- **Purpose:** Operational (gather facts) vs Strategic (provide guidance)
- **Workflow:** Conversational with user (scan → present → validate → save) vs Direct agent-to-user PM advice
- **Invocation:** By pm-setup command or PM agents via Task tool vs Direct user requests
- **Scope:** Context discovery only vs Full PM discipline expertise

---

## Agent Invocation Patterns

### Natural Language (Recommended)

```
Tell product-manager: "I need help planning Q2"
Tell research-ops: "Design a churn study"
Tell roadmap-builder: "Create a 6-month roadmap"
```

### Conversational

```
"I need to prioritize 10 features"           → Routes to feature-prioritizer
"Help me validate this feature idea"         → Routes to research-ops
"Create Q2 goals"                            → Routes to product-strategist
```

### Multi-Agent Request

```
Tell product-manager: "Validate this feature, prioritize it, and plan delivery"
→ Coordinates research-ops, feature-prioritizer, requirements-engineer, roadmap-builder
```

---

## Context Architecture

All agents reference `.claude/product-context/` files (created by `/product-management:pm-setup`):

**8 context files:**

- product-info.md
- business-metrics.md
- strategic-goals.md
- current-roadmap.md
- tech-stack.md
- customer-segments.md
- team-info.md
- competitive-landscape.md

**Benefits:**

- Agents ask 80% fewer questions
- Outputs are product-specific
- Context reused across all agents
- Consistent understanding across workflows

**Pattern:**

1. Agent checks for relevant context files
2. Extracts applicable information
3. Only asks for missing information
4. Produces context-aware output

---

## Best Practices

### 1. Start with product-manager for Complex Requests

Let the router determine which specialists are needed.

### 2. Go Direct for Focused Work

When you know exactly what you need, invoke the specialist directly.

### 3. Provide Context

Rich context produces better outputs. Use pm-setup or provide inline context.

### 4. Chain Agents Intentionally

Design logical sequences: research → strategy → prioritization → specs → launch

### 5. Iterate and Refine

Don't expect perfection on first output. Ask follow-up questions and refine.

---

## Summary

**Plugin:** ai-pm-copilot
**Total Agents:** 9 (1 orchestrator + 7 PM specialists + 1 utility)
**Models:** Claude Opus (6 agents), Claude Sonnet (2 agents), Claude Haiku (1 utility agent)
**Last Updated:** February 2026

---

## Questions & Support

- **Documentation:** See [usage.md](usage.md) for workflows
- **Issues:** [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions:** [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)
