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
- **product-strategy**: Strategic planning, competitive analysis (26 items)
- **product-discovery**: User research, validation, PMF assessment (20 items)
- **product-growth**: Growth experiments, launches, scaling (21 items)
- **product-execution**: Daily execution, shipping, tactical work (40 items)
- Future: industry-specific plugins (B2B SaaS, consumer apps, marketplace)
- Organized by PM discipline and workflow

---

## Repository Structure

```
/Library/Developer/src/Projects/Claude Code Plugins/Agents/
├── plugins/
│   ├── product-strategy/            # Strategic planning (26 items)
│   │   ├── agents/                  # 4 strategy agents
│   │   │   ├── product-strategist.md
│   │   │   ├── competitive-analyst.md
│   │   │   ├── platform-architect.md
│   │   │   └── monetization-expert.md
│   │   ├── commands/                # 6 planning commands
│   │   ├── tools/                   # 5 framework tools
│   │   ├── workflows/               # 5 strategic workflows
│   │   ├── skills/                  # 6 strategy skills
│   │   └── README.md
│   ├── product-discovery/           # Discovery & validation (20 items)
│   │   ├── agents/                  # 3 research agents
│   │   │   ├── user-researcher.md
│   │   │   ├── discovery-facilitator.md
│   │   │   └── customer-insights.md
│   │   ├── commands/                # 7 research commands
│   │   ├── tools/                   # 2 discovery tools
│   │   ├── workflows/               # 4 discovery workflows
│   │   ├── skills/                  # 4 discovery skills
│   │   └── README.md
│   ├── product-growth/              # Growth & launches (21 items)
│   │   ├── agents/                  # 3 growth agents
│   │   │   ├── growth-pm.md
│   │   │   ├── gtm-planner.md
│   │   │   └── data-scientist.md
│   │   ├── commands/                # 5 growth commands
│   │   ├── tools/                   # 3 analysis tools
│   │   ├── workflows/               # 4 growth workflows
│   │   ├── skills/                  # 6 growth skills
│   │   └── README.md
│   └── product-execution/           # Daily execution (40 items)
│       ├── agents/                  # 8 execution agents
│       │   ├── agile-coach.md
│       │   ├── product-ops.md
│       │   ├── feature-prioritizer.md
│       │   ├── requirements-engineer.md
│       │   ├── technical-pm.md
│       │   ├── stakeholder-manager.md
│       │   ├── customer-success.md
│       │   └── api-product-manager.md
│       ├── commands/                # 16 tactical commands
│       ├── tools/                   # 2 decision tools
│       ├── workflows/               # 5 operational workflows
│       ├── skills/                  # 9 practice skills
│       └── README.md
├── docs/                            # System documentation
│   ├── architecture.md              # This file
│   ├── agents.md                    # Agent catalog
│   ├── plugins.md                   # Plugin guide
│   ├── usage.md                     # Usage patterns
│   └── skills.md                    # Skills reference
├── README.md                        # Project overview
├── CHANGELOG.md                     # Version history
└── CONTRIBUTING.md                  # Contribution guide
```

---

## Core Components

### 4 Specialized Plugins (103 Total Items)

**📋 product-strategy** (26 items)
- **4 Agents**: product-strategist, competitive-analyst, platform-architect, monetization-expert
- **6 Commands**: OKR framework, roadmap builder, scenario planner, executive summary, stakeholder mapper, risk assessment
- **5 Tools**: SWOT analysis, Business Model Canvas, Value Proposition Canvas, competitive positioning, market sizing
- **5 Workflows**: Annual planning, quarterly planning, portfolio optimization, market entry, product pivot
- **6 Skills**: Strategy frameworks, vision/mission, business models, platform strategy, positioning, pricing

**🔍 product-discovery** (20 items)
- **3 Agents**: user-researcher, discovery-facilitator, customer-insights
- **7 Commands**: Interview guide, research synthesizer, survey builder, usability test planner, persona creator, journey mapper, MVP scoper
- **2 Tools**: Assumption mapping, impact mapping
- **4 Workflows**: Discovery sprint, solution validation, PMF assessment, research-to-product
- **4 Skills**: User research techniques, continuous discovery, design thinking, jobs-to-be-done

**📈 product-growth** (21 items)
- **3 Agents**: growth-pm, gtm-planner, data-scientist
- **5 Commands**: Experiment designer, KPI dashboard, impact estimator, release planner, communication plan
- **3 Tools**: ROI calculator, cost-benefit analysis, Now-Next-Later roadmap
- **4 Workflows**: Growth sprint, scale playbook, beta program, product launch
- **6 Skills**: Growth frameworks, metrics (AARRR/HEART), product analytics, experiment design, GTM playbooks, product-market fit

**⚙️ product-execution** (40 items)
- **8 Agents**: agile-coach, product-ops, feature-prioritizer, requirements-engineer, technical-pm, stakeholder-manager, customer-success, api-product-manager
- **16 Commands**: Backlog groomer, capacity planner, sprint planner, sprint goal, user story writer, PRD generator, technical spec, ticket review, quick answer, quick prioritize, status update, meeting agenda, decision logger, doc update, release notes, alignment session
- **2 Tools**: Technical debt assessment, trade-off analysis
- **5 Workflows**: Backlog optimization, feature lifecycle, PM process audit, crisis management, sunset product
- **9 Skills**: Agile methodologies, dual-track agile, prioritization methods, specifications, story mapping, technical debt, OKRs, API products, lean development

### Total Coverage
- **18 Expert AI Agents** across all PM disciplines
- **34 Commands** for fast, focused tasks
- **12 Framework Tools** for analysis and decision-making
- **18 Multi-Step Workflows** for complex processes
- **25 Knowledge Skills** spanning all major PM methodologies

---

## Model Configuration

### Strategic Model Selection

**All agents use the Sonnet model** (currently Claude Sonnet 4.5) for:
- Complex strategic reasoning
- Nuanced stakeholder communication
- Deep contextual understanding
- Comprehensive framework application

**Tools and workflows use appropriate models:**
- **Haiku** for fast framework analysis (SWOT, Business Model Canvas, ROI calculators)
- **Sonnet** for complex multi-step workflows and strategic agents

This ensures consistent high-quality outputs across all PM disciplines while optimizing for performance and cost.

---

## Design Patterns

### Pattern 1: Single-Purpose Agent
Each agent focuses on one PM discipline.

**Example: product-strategist**
```yaml
name: product-strategist
description: Expert in product strategy, vision, roadmaps, and OKRs
model: sonnet
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
model: sonnet
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
├── product-strategy/           # Core (current)
├── product-discovery/          # Core (current)
├── product-growth/             # Core (current)
├── product-execution/          # Core (current)
├── b2b-saas-pm/               # B2B SaaS specialization (planned)
├── consumer-apps-pm/          # Consumer product focus (planned)
└── marketplace-pm/            # Two-sided marketplace (planned)
```

### 2. Company-Specific Customization
```
plugins/
├── product-strategy-acme/      # Acme Corp strategy toolkit
│   └── agents/
│       ├── product-strategist.md       # Acme-customized
│       └── competitive-analyst.md      # Acme market focus
└── product-execution-acme/     # Acme Corp execution toolkit
    └── agents/
        └── agile-coach.md              # Acme Scrum process
```

### 3. Tool Integrations (Future)
```
plugins/
└── pm-integrations/
    ├── jira/              # Jira sync for all 4 plugins
    ├── linear/            # Linear integration
    ├── productboard/      # ProductBoard connection
    └── amplitude/         # Analytics integration
```

---

## Comparison with Reference Architecture

This toolkit is inspired by [wshobson/agents](https://github.com/wshobson/agents) but specialized for product management:

**Similarities:**
- Single-purpose agents
- Modular plugin structure
- Model-per-complexity strategy (Haiku tools + Sonnet workflows)
- Skills as knowledge base

**Differences:**
- **Domain**: PM-specific vs. software development
- **Scale**: 103 PM items (18 agents, 31 commands, 12 tools, 18 workflows, 24 skills) vs. 85 multi-domain agents
- **Organization**: 4 plugins by PM discipline vs. multi-domain coverage
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
- **Sonnet model**: High-quality strategic outputs, nuanced stakeholder communication
- **Haiku model**: Fast, efficient framework analysis with consistent quality
- **Automatic updates**: Using aliases ensures agents benefit from latest model improvements
- **Consistent expertise**: All agents benefit from latest model capabilities

### Scalability
- **Agents**: Can add unlimited agents (each is independent)
- **Plugins**: Can create domain-specific plugin collections
- **Skills**: Centralized knowledge base grows without agent changes

---

## Version Management & Updates

### Semantic Versioning

All plugins follow [Semantic Versioning](https://semver.org/) (semver): `MAJOR.MINOR.PATCH`

**MAJOR version** (1.0.0 → 2.0.0): Breaking changes
- Agent interface or behavior changes
- Command argument changes
- Removed agents, commands, or workflows
- Breaking changes to skill specifications
- **Example**: Removing an agent, changing command syntax

**MINOR version** (1.0.0 → 1.1.0): New features (backward compatible)
- New agents added
- New commands added
- New tools or workflows
- New skills added
- Enhanced capabilities
- **Example**: Adding a new agent to product-strategy plugin

**PATCH version** (1.0.0 → 1.0.1): Bug fixes (backward compatible)
- Agent documentation improvements
- Bug fixes in existing agents
- Minor tweaks and clarifications
- Performance improvements
- **Example**: Fixing typos, improving agent instructions

### Version Management Commands

```bash
# Install specific version of a plugin
/plugin install product-strategy@1.0.0
/plugin install product-execution@1.2.1

# Install latest version (default)
/plugin install product-strategy

# Update to latest version
/plugin update product-strategy
/plugin update product-discovery product-growth product-execution

# Update all plugins
/plugin update --all

# List installed versions
/plugin list

# View available versions
/plugin versions product-strategy
```

### Update Strategy

**Automatic Updates** (Recommended):
- Set plugins to auto-update for MINOR and PATCH versions
- Review MAJOR version updates manually before upgrading
- Subscribe to release notifications on GitHub

**Manual Updates** (Conservative):
- Test updates in development environment first
- Review CHANGELOG.md for breaking changes
- Update one plugin at a time
- Verify workflows after updating

### Backward Compatibility

**Our Commitment:**
- MINOR and PATCH updates are backward compatible
- Existing workflows continue to work
- Deprecated features have 1 MAJOR version warning period
- Migration guides provided for MAJOR version updates

**Example deprecation path:**
```
v1.5.0: Feature X marked deprecated (still works)
v1.6.0: Feature X still works, warning shown
v2.0.0: Feature X removed, migration guide provided
```

### Plugin Dependencies

**Independent Plugins:**
All 4 core plugins (strategy, discovery, growth, execution) are independent:
- No dependencies between plugins
- Can update each plugin separately
- Backwards compatible within same MAJOR version

**Version Compatibility:**
```yaml
# Example: Industry-specific plugin with dependencies
name: b2b-saas-pm
version: 1.0.0
dependencies:
  product-strategy: ^1.0.0    # Compatible with 1.x.x
  product-growth: ^1.0.0       # Compatible with 1.x.x
```

### Marketplace Updates

**Publishing Updates:**
1. Update version in plugin manifest
2. Update CHANGELOG.md with changes
3. Tag release: `git tag v1.2.0`
4. Push tags: `git push --tags`
5. Marketplace auto-updates within 24 hours

**Update Notifications:**
Users receive notifications when updates are available:
- MAJOR: "Breaking changes available - review before updating"
- MINOR: "New features available - update recommended"
- PATCH: "Bug fixes available - update when convenient"

### Rolling Back

If an update causes issues:

```bash
# Uninstall current version
/plugin uninstall product-strategy

# Install previous version
/plugin install product-strategy@1.0.0

# Report issue
# Open GitHub Issue with version numbers and error details
```

### Plugin Lifecycle

**Active Development** (Current):
- Regular updates (monthly MINOR/PATCH releases)
- Bug fixes within 1-2 weeks
- New features based on community feedback
- Full support and documentation

**Maintenance Mode** (Future, if needed):
- Critical bug fixes only
- No new features
- Security updates
- 6-month notice before deprecation

**Deprecated** (Future, if needed):
- 12-month notice period
- Migration path to successor
- Documentation remains available
- Security updates for 6 months

### Release Schedule

**Regular Releases:**
- **Patch releases**: As needed (bug fixes)
- **Minor releases**: Monthly (new features)
- **Major releases**: Annually (breaking changes, if needed)

**Emergency Releases:**
- Critical security fixes: Within 24-48 hours
- Critical bugs: Within 1 week
- Tagged with `hotfix` in release notes

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
**Last Updated**: October 2025
**Total**: 103 items across 4 specialized plugins (product-strategy, product-discovery, product-growth, product-execution)
