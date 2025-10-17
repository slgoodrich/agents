# Architecture

## Design Philosophy

The Product Management Toolkit for Claude Code follows a modular, composable architecture inspired by modern product management practices and the Unix philosophy: **do one thing well**.

### Core Principles

#### 1. Single Responsibility Principle
Each agent specializes in one PM discipline:
- **product-strategist**: Vision, strategy, roadmaps, OKRs
- **user-researcher**: Discovery, interviews, synthesis
- **requirements-engineer**: PRDs, specs, user stories
- **agile-coach**: Sprint planning, ceremonies, backlog
- **feature-prioritizer**: RICE, ICE, prioritization frameworks
- Each agent has deep expertise in its domain

#### 2. Composability
Agents work independently or together:
- Mix and match agents based on your workflow
- No forced feature bundling
- Clear boundaries between agents
- Agents can reference each other for handoffs

Example: `product-strategist` → `requirements-engineer` → `agile-coach` (vision → specs → sprint)

#### 3. Progressive Disclosure
Information when you need it:
- Agents activate based on request patterns
- Skills load on-demand
- No bloated context windows
- Token-efficient design

#### 4. Plugin Distribution
Focused plugins for specific PM domains:
- **product-management**: Core PM capabilities (18 agents)
- Future: domain-specific plugins (B2B SaaS, consumer apps, marketplace)
- Organized by PM lifecycle stage

---

## Repository Structure

```
/Library/Developer/src/Projects/Agents/
├── plugins/
│   └── product-management/          # Core PM toolkit
│       ├── agents/                  # 18 specialized PM agents
│       │   ├── product-strategist.md
│       │   ├── user-researcher.md
│       │   ├── requirements-engineer.md
│       │   ├── agile-coach.md
│       │   ├── feature-prioritizer.md
│       │   ├── gtm-planner.md
│       │   ├── growth-pm.md
│       │   ├── stakeholder-manager.md
│       │   ├── technical-pm.md
│       │   ├── data-scientist.md
│       │   ├── competitive-analyst.md
│       │   ├── customer-insights.md
│       │   ├── customer-success.md
│       │   ├── monetization-expert.md
│       │   ├── api-product-manager.md
│       │   ├── platform-architect.md
│       │   ├── discovery-facilitator.md
│       │   └── product-ops.md
│       ├── commands/                # Focused command tools
│       │   └── capacity-planner.md
│       ├── skills/                  # PM knowledge frameworks (future)
│       └── README.md                # Plugin documentation
├── docs/                            # System documentation
│   ├── architecture.md              # This file
│   ├── agents.md                    # Agent catalog
│   ├── plugins.md                   # Plugin guide
│   ├── usage.md                     # Usage patterns
│   └── agent-skills.md              # Skills reference
├── README.md                        # Project overview
└── PLAN.md                          # Development plan
```

---

## Core Components

### 18 Specialized PM Agents

**Strategy & Planning** (3 agents)
- product-strategist
- platform-architect
- product-ops

**Discovery & Research** (4 agents)
- user-researcher
- discovery-facilitator
- customer-insights
- competitive-analyst

**Delivery & Execution** (4 agents)
- requirements-engineer
- technical-pm
- agile-coach
- feature-prioritizer

**Growth & Optimization** (3 agents)
- growth-pm
- data-scientist
- monetization-expert

**Go-to-Market & Collaboration** (4 agents)
- gtm-planner
- stakeholder-manager
- api-product-manager
- customer-success

### Command Tools
Focused utilities for specific tasks:
- capacity-planner
- (More coming: PRD generator, OKR builder, roadmap creator, etc.)

### Skills (25 Available)
Knowledge frameworks that extend agent capabilities:
- **Prioritization**: prioritization-methods (RICE, ICE, Kano, MoSCoW, Value vs Effort)
- **Agile**: agile-methodologies, dual-track-agile, story-mapping
- **Strategy**: product-strategy-frameworks, vision-mission-strategy, platform-strategy
- **Research**: user-research-techniques, continuous-discovery, jobs-to-be-done
- **Metrics**: metrics-frameworks, product-analytics, okr-methodology
- **Growth**: growth-frameworks, experiment-design, product-market-fit
- **GTM**: go-to-market-playbooks, product-positioning, pricing-packaging
- **Technical**: api-product-management, technical-debt-management, specification-techniques
- **Innovation**: lean-product-development, design-thinking, business-model-canvas

---

## Model Configuration

### Strategic Model Selection

**All agents use Claude Sonnet 4.5** for:
- Complex strategic reasoning
- Nuanced stakeholder communication
- Deep contextual understanding
- Comprehensive framework application

This ensures consistent high-quality outputs across all PM disciplines.

---

## Design Patterns

### Pattern 1: Single-Purpose Agent
Each agent focuses on one PM discipline.

**Example: product-strategist**
```yaml
name: product-strategist
description: Expert in product strategy, vision, roadmaps, and OKRs
model: claude-sonnet-4-5
capabilities:
  - Strategic planning
  - OKR frameworks
  - Roadmap development
  - Competitive strategy
```

**Benefits:**
- Deep expertise in domain
- Predictable behavior
- Easy to understand and use
- Token efficient (only loads relevant context)

### Pattern 2: Multi-Agent Composition
Combine agents for complex workflows.

**Example: Feature Development Workflow**
```
1. product-strategist    → Define strategic rationale
2. user-researcher       → Validate with customers
3. requirements-engineer → Write detailed specs
4. technical-pm          → Define technical approach
5. agile-coach           → Plan sprint execution
6. gtm-planner           → Prepare launch
```

**Benefits:**
- Each expert contributes their specialty
- Clear handoffs between stages
- Comprehensive coverage of lifecycle
- Flexible orchestration

### Pattern 3: Agent + Skill Integration (Planned)
Agents reference skills for framework expertise.

**Example: feature-prioritizer using RICE skill**
```
User: "Prioritize these 10 features"
↓
feature-prioritizer agent activates
↓
Loads RICE skill (Reach, Impact, Confidence, Effort)
↓
Applies framework systematically
↓
Returns scored backlog with rationale
```

**Benefits:**
- Progressive disclosure (skill loads only when needed)
- Consistent framework application
- Updated frameworks don't require agent changes
- Reusable knowledge across agents

### Pattern 4: Command + Agent Hybrid
Quick commands for speed, agents for depth.

**Example:**
```bash
# Fast: Generate PRD skeleton with command
/pm:prd "Dark mode feature"

# Deep: Refine with agent conversation
Tell requirements-engineer: "Add edge cases for system theme detection"
```

**Benefits:**
- Commands: Fast, deterministic, repeatable
- Agents: Adaptive, nuanced, exploratory
- User chooses interaction style

---

## Architecture Goals

### 1. Token Efficiency
**Problem**: Loading all PM knowledge bloats context
**Solution**:
- Modular agents (load one at a time)
- On-demand skills (progressive disclosure)
- Focused commands (minimal context)

**Result**: Faster responses, lower costs, more room for user context

### 2. Granularity
**Problem**: Monolithic "do everything" PM assistant is overwhelming
**Solution**:
- 18 specialized agents instead of 1 generalist
- Each agent is an expert in their domain
- Clear when to use which agent

**Result**: Better outputs, easier to learn, predictable behavior

### 3. Composability
**Problem**: Real PM work spans multiple disciplines
**Solution**:
- Agents designed to work together
- Clear handoff patterns
- Suggested agent combinations in docs

**Result**: Users can orchestrate complex workflows

### 4. Maintainability
**Problem**: Updating one capability shouldn't break others
**Solution**:
- Isolated agent files
- Skills separate from agents
- No inter-agent dependencies

**Result**: Easy to update, extend, and contribute

### 5. Clarity of Purpose
**Problem**: Users don't know which tool to use
**Solution**:
- Agent descriptions make specialty clear
- "When to use" sections in each agent
- Usage patterns documented

**Result**: Users pick the right tool quickly

---

## Agent Design Specification

Each agent follows a consistent structure:

```yaml
---
name: agent-name
description: One-line specialty and use case
model: claude-sonnet-4-5
---

# Agent Name

## Purpose
High-level mission and value proposition

## Core Philosophy
Foundational principles and beliefs

## Capabilities
Detailed breakdown of what this agent can do

## Knowledge Base
Frameworks, methodologies, tools, thought leaders

## Behavioral Traits
How this agent approaches problems

## Response Approach
Step-by-step process for handling requests

## Example Interactions
Realistic use cases with full conversations

## Integration with Other Agents
How this agent works with others

## When to Use This Agent
 Use for...
 Don't use for...
```

This structure ensures:
- Consistency across agents
- Clear capabilities
- Realistic expectations
- Easy onboarding

---

## Workflow Orchestration

### Sequential Workflows
Agents pass work to the next expert.

**Example: Idea to Launch**
```
1. discovery-facilitator  → Validate problem
2. product-strategist     → Define strategy
3. requirements-engineer  → Write specs
4. technical-pm           → Assess feasibility
5. agile-coach            → Plan sprints
6. gtm-planner            → Launch planning
```

### Parallel Workflows
Multiple agents work simultaneously.

**Example: Quarterly Planning**
```
In parallel:
- product-strategist    → Draft OKRs
- competitive-analyst   → Market research
- data-scientist        → Analyze Q4 metrics
- stakeholder-manager   → Gather input

Then:
- product-strategist    → Synthesize into final plan
```

### Iterative Workflows
Agents refine each other's work.

**Example: PRD Refinement**
```
1. requirements-engineer  → Draft PRD
2. user-researcher        → Validate with customers
3. technical-pm           → Add technical specs
4. stakeholder-manager    → Review with execs
5. requirements-engineer  → Final polish
```

---

## Extension Points

The architecture supports future expansion:

### 1. Industry-Specific Plugins
```
plugins/
├── product-management/          # Core (current)
├── b2b-saas-pm/                # B2B SaaS specialization
├── consumer-apps-pm/           # Consumer product focus
└── marketplace-pm/             # Two-sided marketplace
```

### 2. Company-Specific Customization
```
plugins/
└── product-management/
    └── agents/
        ├── product-strategist.md       # Default
        └── product-strategist-acme.md  # Acme Corp version
```

### 3. Tool Integrations (Future)
```
plugins/
└── product-management/
    └── integrations/
        ├── jira/           # Jira sync
        ├── linear/         # Linear integration
        └── productboard/   # ProductBoard connection
```

---

## Comparison with Reference Architecture

This toolkit is inspired by [wshobson/agents](https://github.com/wshobson/agents) but specialized for product management:

**Similarities:**
- Single-purpose agents
- Modular plugin structure
- Model-per-complexity strategy
- Skills as knowledge base

**Differences:**
- **Domain**: PM-specific vs. software development
- **Scale**: 18 PM agents vs. 85 multi-domain agents
- **Depth**: Deep PM expertise vs. broad engineering coverage
- **Audience**: Product managers vs. developers

**Complementary:** These toolkits work together! PMs use this for product work; developers use wshobson/agents for engineering.

---

## Performance Characteristics

### Token Usage
- **Single agent invocation**: 2,000-5,000 tokens (agent instructions + user prompt)
- **Multi-agent workflow**: 8,000-20,000 tokens (sequential calls)
- **With skills loaded**: +1,000-3,000 tokens per skill

### Response Quality
- **Sonnet 4.5**: High-quality strategic outputs, nuanced stakeholder communication
- **Consistent expertise**: All agents benefit from latest model capabilities

### Scalability
- **Agents**: Can add unlimited agents (each is independent)
- **Plugins**: Can create domain-specific plugin collections
- **Skills**: Centralized knowledge base grows without agent changes

---

## Contributing to Architecture

When contributing new agents or components:

**1. Follow Single Responsibility Principle**
- One agent = one PM discipline
- Clear, focused purpose
- No feature creep

**2. Use Standard Agent Structure**
- Follow agent template in existing files
- Include all required sections
- Provide realistic examples

**3. Document Integration Points**
- How does this work with other agents?
- What's the handoff pattern?
- When to use vs. other agents?

**4. Consider Token Efficiency**
- Can this be a skill instead of an agent?
- Can this be a command instead of a skill?
- Is there duplication to remove?

**5. Test Composability**
- Does this work standalone?
- Does it work in multi-agent workflows?
- Are handoffs clear?

---

## Questions & Feedback

Architecture decisions are documented in the repository. For questions or suggestions:
- Open a GitHub Issue
- Start a Discussion
- Contribute improvements via PR

---

**Version**: 1.0.0
**Last Updated**: January 2025
