# Architecture

## Design Philosophy

The Product Management Toolkit for Claude Code follows an **agent-first architecture** optimized for solo developers and small teams. The design prioritizes conversational workflows over command-line tools.

### Core Principles

#### 1. Agent-First Design
Conversational agents are the primary interface:
- **1 orchestration agent + 7 PM specialist agents + 1 utility agent** cover the complete PM lifecycle
- **product-manager agent** (orchestrator) routes requests to PM specialist agents
- **context-scanner utility agent** provides operational support (codebase scanning)
- Agents collaborate through intelligent routing
- Conversational interface instead of command memorization

**Example Routing:**
```
User: "Help me prioritize these features"
↓
product-manager analyzes request
↓
Routes to feature-prioritizer agent
↓
feature-prioritizer loads prioritization-methods skill
↓
Returns scored features with rationale
```

#### 2. Single Plugin Architecture
Single comprehensive plugin with all PM capabilities:
- **product-management**: All 9 agents, 16 skills, 1 command
- Simpler installation and updates
- Unified versioning and testing
- Easier maintenance and contribution

**Benefits:**
- One command to install everything: `/plugin install product-management`
- All agents work together seamlessly
- Consistent version management
- Reduced cognitive overhead

#### 3. Progressive Skill Loading
16 specialized skills provide deep framework knowledge:
- Skills activate only when needed
- Each skill includes assets (templates, frameworks) and references (guides)
- 63 assets + 37 references = 100 total documentation files
- Token-efficient: load frameworks on-demand

#### 4. Context-Aware Workflows
Reusable product context enables efficient, focused interactions:
- **`.claude/product-context/`** directory stores core context files
- One-time setup with `/product-management:pm-setup` command (5-10 min with codebase scanning)
- All 9 agents read context files first, then ask only for gaps
- context-scanner utility agent can auto-discover context from existing codebases
- More time for product work, less time providing background

**Context Files:**
- product-info.md, metrics.md, goals.md, roadmap.md
- tech-stack.md, customers.md, team.md, competitors.md

**Value:**
- Focused, streamlined conversations (agents ask 80% fewer questions)
- Product-specific, actionable outputs
- Consistent understanding across all agents

See [Context Architecture Guide](context-architecture.md) for detailed specification.

#### 5. Solo Developer Focus
Designed for individuals and small teams:
- No stakeholder management jargon
- No corporate PM processes (RACI matrices, executive alignment)
- Practical, actionable advice
- Templates scaled for lean teams
- Direct language focused on execution

---

## Repository Structure

```
/Library/Developer/src/Projects/Claude Code Plugins/Agents/
├── plugins/
│   └── product-management/              # Single comprehensive plugin
│       ├── agents/                      # 1 orchestration + 7 PM specialists + 1 utility
│       │   ├── product-manager.md       # Orchestration agent (routes requests)
│       │   ├── market-analyst.md        # Market research & competitive analysis
│       │   ├── research-ops.md          # User research & discovery
│       │   ├── product-strategist.md    # Strategy & positioning
│       │   ├── roadmap-builder.md       # Roadmap planning
│       │   ├── feature-prioritizer.md   # Feature scoring & prioritization
│       │   ├── requirements-engineer.md # PRDs, specs, user stories
│       │   ├── launch-planner.md        # Go-to-market & launches
│       │   └── context-scanner.md       # Utility: Codebase context discovery
│       ├── commands/
│       │   └── pm-setup.md              # Initialize .claude/product-context/
│       └── skills/                      # 16 specialized skills
│           ├── user-research-techniques/    # SKILL.md + assets/ + references/
│           ├── interview-frameworks/        # SKILL.md + assets/ + references/
│           ├── synthesis-frameworks/        # SKILL.md + assets/
│           ├── usability-frameworks/        # SKILL.md + assets/
│           ├── validation-frameworks/       # SKILL.md + assets/
│           ├── product-positioning/         # SKILL.md + assets/ + references/
│           ├── competitive-analysis-templates/  # SKILL.md + assets/
│           ├── market-sizing-frameworks/    # SKILL.md + assets/
│           ├── product-market-fit/          # SKILL.md + assets/ + references/
│           ├── roadmap-frameworks/          # SKILL.md + assets/
│           ├── prioritization-methods/      # SKILL.md + assets/ + references/
│           ├── specification-techniques/    # SKILL.md + assets/ + references/
│           ├── prd-templates/               # SKILL.md + assets/ + references/
│           ├── user-story-templates/        # SKILL.md + assets/
│           ├── go-to-market-playbooks/      # SKILL.md + assets/ + references/
│           └── launch-planning-frameworks/  # SKILL.md + assets/ + references/
├── .claude-plugin/
│   ├── plugin.json                  # Plugin manifest
│   └── marketplace.json             # Marketplace configuration
├── docs/                            # System documentation
│   ├── architecture.md              # This file
│   ├── agents.md                    # Agent catalog
│   ├── agent-skills.md              # Skills reference
│   ├── plugins.md                   # Plugin guide
│   ├── usage.md                     # Usage patterns
│   └── context-architecture.md      # Context system spec
├── README.md                        # Project overview
└── CONTRIBUTING.md                  # Contribution guide
```

**Component Totals:**
- **9 agents**: 1 orchestration agent + 7 PM specialists + 1 utility agent for complete PM lifecycle coverage
- **1 command**: Context initialization with optional codebase scanning (pm-setup)
- **16 skills**: Framework knowledge with 63 assets + 37 references
- **126 total files**: All tested and documented

---

## Core Components

### Agents (9 Total)

The product-management plugin includes 9 agents covering the complete PM lifecycle: 8 PM experts (1 orchestrator + 7 specialists) and 1 utility agent for operational support. The **product-manager** agent serves as the main entry point and intelligently routes requests to specialist agents.

#### Routing Agent

**product-manager** (Main entry point)
- Analyzes user requests and routes to appropriate specialist agents
- Handles general PM questions
- Coordinates multi-agent workflows
- Ensures consistent product context across specialists

#### Specialist Agents (7)

**market-analyst** (Market research & competitive intelligence)
- Competitive analysis (SWOT, Porter's Five Forces)
- Market sizing (TAM/SAM/SOM)
- Product positioning and differentiation
- **Skills**: product-positioning, competitive-analysis-templates, market-sizing-frameworks, product-market-fit

**research-ops** (User research & discovery)
- User interviews and surveys
- Usability testing
- Research synthesis and insight generation
- Problem/solution validation
- **Skills**: user-research-techniques, interview-frameworks, synthesis-frameworks, usability-frameworks, validation-frameworks

**product-strategist** (Strategy & vision)
- Product strategy and vision
- Market positioning
- Strategic planning and decision-making
- **Skills**: product-positioning, product-market-fit

**roadmap-builder** (Roadmap planning)
- Roadmap creation (Now-Next-Later, theme-based, outcome-based)
- Timeline planning
- Dependency mapping
- **Skills**: roadmap-frameworks

**feature-prioritizer** (Feature scoring & prioritization)
- RICE, ICE, MoSCoW, Kano scoring
- Value vs Effort analysis
- Cost of Delay calculations
- Trade-off analysis
- **Skills**: prioritization-methods

**requirements-engineer** (PRDs, specs, user stories)
- Product Requirements Documents (PRDs)
- Technical specifications
- User story writing
- Acceptance criteria definition
- **Skills**: specification-techniques, prd-templates, user-story-templates

**launch-planner** (Go-to-market & launches)
- Launch planning and execution
- GTM strategy (PLG, sales-led)
- Launch tier definition
- Cross-functional coordination
- **Skills**: go-to-market-playbooks, launch-planning-frameworks

#### Utility Agent (1)

**context-scanner** (Codebase context discovery)
- Auto-discovers features, tech stack, integrations, and scale from existing codebases
- Enables fast onboarding (5-10 min vs 15-20 min manual entry)
- Invoked by pm-setup command or PM agents needing current product state
- Returns structured JSON with evidence and confidence scores
- User validation required before saving context
- **Model**: Haiku (optimized for efficient file operations)
- **Focus**: Strategic context only (WHAT exists, not HOW it's built)

**Differences from PM Specialists:**
- **Purpose**: Operational (gather facts) vs Strategic (provide guidance)
- **Model**: Haiku (fast, efficient) vs Sonnet (expert reasoning)
- **Output**: Structured data (JSON) vs Conversational advice
- **Invocation**: Programmatic (by commands/agents) vs User-initiated
- **Scope**: Context discovery only vs Full PM discipline expertise

**When to create utility agents:**
- Task is operational, not strategic (file scanning vs analysis)
- Task is reusable across multiple PM agents
- Task benefits from different model (Haiku for speed/cost)
- Task is fact-gathering, not consultation

---

### Utility Agent Pattern

Not all agents are domain experts. Utility agents perform specialized tasks that support PM agents without requiring strategic thinking.

#### Domain Expert Agents (8)

**Characteristics:**
- Strategic thinking and PM consultation
- Apply PM frameworks and methodologies
- Use Sonnet model for expert-level reasoning
- Examples: market-analyst, product-strategist, feature-prioritizer

**Purpose:** Provide PM expertise and strategic guidance

#### Utility Agents (1)

**Characteristics:**
- Specialized task execution (file operations, data processing)
- Fact-gathering without interpretation
- Use Haiku model for efficiency
- Examples: context-scanner

**Purpose:** Support PM agents with operational tasks

#### When to Use Utility Agents

Create utility agents when:
- Task is operational, not strategic (file scanning, not analysis)
- Task is reusable across multiple PM agents
- Task benefits from different model (Haiku for speed/cost)
- Task is fact-gathering, not consultation

**Example: context-scanner**
- **Operational:** Scans files and manifests (no strategic analysis)
- **Reusable:** pm-setup, market-analyst, feature-prioritizer all use it
- **Haiku-appropriate:** File operations, no complex reasoning needed
- **Fact-gathering:** Reports WHAT exists, doesn't analyze or recommend

#### Agent Invocation Pattern

```
User → product-manager (orchestrator)
     → market-analyst (domain expert) needs current features
     → Invokes context-scanner (utility)
     → context-scanner returns facts (features, tech stack, scale)
     → market-analyst uses facts for strategic analysis
     → Returns competitive analysis to user
```

**Benefits:**
- PM experts focus on strategy, not operations
- Right model for the job (Sonnet for thinking, Haiku for doing)
- Clean separation of concerns
- Reusable utilities across agents

---

### Agent Routing Pattern

```
User Request
↓
product-manager (analyzes intent)
↓
Routes to specialist:
- Market questions → market-analyst
- Research questions → research-ops
- Strategy questions → product-strategist
- Roadmap questions → roadmap-builder
- Prioritization → feature-prioritizer
- Requirements → requirements-engineer
- Launch questions → launch-planner
↓
Specialist loads relevant skills
↓
Returns expert response
```

### Component Breakdown
- **9 agents**: 1 routing agent + 7 PM specialists + 1 utility agent covering complete PM lifecycle
- **1 command**: pm-setup (context initialization with optional codebase scanning)
- **16 skills**: Framework knowledge with progressive disclosure
- **63 assets**: Templates, frameworks, checklists
- **37 references**: Guides, best practices, methodologies
- **Total**: 126 tested files ready for production

---

## Model Configuration

### Right Model for the Job

**PM specialists use Claude Sonnet, utility agents use Claude Haiku** - optimizing for the task at hand:

**PM Specialist Agents** (8: 1 orchestrator + 7 specialists) → **Sonnet**
- Complex strategic reasoning and nuanced decision-making
- Deep contextual understanding and interactive conversations
- Comprehensive framework application across all PM disciplines
- Intelligent routing and multi-agent collaboration

**Utility Agents** (1: context-scanner) → **Haiku**
- Fast, efficient file operations and data processing
- Operational tasks without strategic analysis
- Cost-effective for repetitive scanning operations
- Optimized for structured data extraction

**Command** (1 setup tool) → **Uses both models**
- pm-setup orchestration uses Sonnet for intelligent workflow coordination
- Invokes context-scanner (Haiku) for codebase scanning when applicable
- Analyzes project needs and creates appropriate context structure

**Skills** (16 knowledge frameworks)
- Progressive disclosure of PM frameworks and methodologies
- Load on-demand to keep agents token-efficient
- Detailed knowledge from industry leaders (Teresa Torres, Marty Cagan, April Dunford, Sean Ellis)

**Benefits of mixed architecture:**
- **Quality where it matters:** Sonnet for strategic PM guidance
- **Efficiency for operations:** Haiku for file scanning and data extraction
- **Cost optimization:** Right model for each task reduces token costs
- **Performance:** Fast utility operations don't slow down strategic work

---

## Design Patterns

### Pattern 1: Single-Purpose Agent
Each agent focuses on one PM discipline.

**Example: product-strategist**
```yaml
name: product-strategist
description: Expert in product strategy, vision, roadmaps, and goals
model: sonnet
capabilities:
  - Strategic planning
  - Goal-setting frameworks
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
- product-strategist    → Draft goals
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
- **Scale**: Single comprehensive PM plugin vs. multi-domain agent collection
- **Organization**: Agent-first with intelligent routing vs. multi-domain coverage
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

**Last Updated**: October 2025
**Status**: 13/13 tests passing, production-ready
**Total**: 9 agents, 1 command, 16 skills (63 assets + 37 references) in single product-management plugin
