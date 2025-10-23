# Plugins Guide

## Overview

The Product Management Toolkit is organized as a **plugin-based system** that allows you to install and use only the PM capabilities you need. This guide explains the plugin structure, installation, and how to work with plugins.

---

## What is a Plugin?

A **plugin** is a self-contained collection of related product management capabilities:
- **Agents**: Expert AI assistants for specific PM disciplines
- **Commands**: Fast, focused utilities for common PM tasks
- **Skills**: Knowledge frameworks and best practices (coming soon)
- **Documentation**: Usage guides and examples

Plugins follow the principle of **single responsibility**: each plugin focuses on one PM domain or workflow area.

---

## Quick Start

### For Different PM Roles

**Individual Contributor PM:**
Start with the essentials for daily execution and feature delivery.
```bash
# Minimum viable toolkit
/plugin install product-execution    # Daily work, sprints, PRDs

# Add as needed
/plugin install product-discovery    # User research, validation
/plugin install product-growth       # Launches, experiments
```

**Lead PM / Senior PM:**
Full toolkit for end-to-end product leadership.
```bash
# Complete PM toolkit (recommended)
/plugin install product-strategy product-discovery product-growth product-execution

# All 4 plugins give you complete PM lifecycle coverage
```

**Director / VP of Product:**
Strategic focus with execution oversight.
```bash
# Strategy and planning focused
/plugin install product-strategy     # OKRs, roadmaps, portfolio

# Add execution for team oversight
/plugin install product-execution    # Process optimization, capacity planning
```

**CPO / Head of Product:**
Strategic direction and organizational design.
```bash
# Strategic and organizational
/plugin install product-strategy     # Annual planning, portfolio, strategy

# Add discovery for customer insights
/plugin install product-discovery    # Research synthesis, PMF assessment
```

### By Use Case

**Building MVP / Early Stage:**
```bash
/plugin install product-discovery    # Problem validation, MVP scoping
/plugin install product-execution    # Lean delivery, user stories
```

**Scaling Product / Growth Stage:**
```bash
/plugin install product-growth       # Growth experiments, launches
/plugin install product-strategy     # Roadmaps, prioritization
```

**Enterprise / Mature Product:**
```bash
/plugin install product-strategy     # Portfolio, annual planning
/plugin install product-execution    # Process optimization, governance
```

### Recommended Starting Point

**Just getting started?** Install all 4 plugins for complete coverage:
```bash
/plugin install product-strategy product-discovery product-growth product-execution
```

**Benefits of complete install:**
- ✅ Ready for any PM scenario
- ✅ No gaps in your toolkit
- ✅ Agents work together seamlessly
- ✅ Complete command library
- ✅ All workflows available

**Disk space:** ~50MB total for all 4 plugins
**Memory:** Plugins load on-demand (minimal overhead)

---

## Available Plugins

### 📋 product-strategy (26 items)

**Strategic planning, competitive analysis, business modeling, and roadmapping**

**What's Included:**
- 4 strategy agents (product-strategist, competitive-analyst, platform-architect, monetization-expert)
- 6 planning commands (OKRs, roadmaps, scenarios, executive summaries, risk assessments)
- 5 framework tools (SWOT, Business Model Canvas, competitive positioning, market sizing)
- 5 strategic workflows (annual/quarterly planning, portfolio optimization, market entry, pivots)
- 6 strategy skills (frameworks, vision/mission, positioning, pricing)

**Use this plugin for:**
- Annual and quarterly planning
- Competitive strategy and market analysis
- Business model design and validation
- Strategic decision making

**Installation:**
```bash
/plugin install product-strategy
```

---

### 🔍 product-discovery (20 items)

**Discovery, validation, research synthesis, and PMF assessment**

**What's Included:**
- 3 research agents (user-researcher, discovery-facilitator, customer-insights)
- 7 research commands (interview guides, personas, journey maps, surveys, MVP scoping)
- 2 discovery tools (assumption mapping, impact mapping)
- 4 discovery workflows (discovery sprints, solution validation, PMF assessment, research-to-product)
- 4 discovery skills (user research, continuous discovery, design thinking, JTBD)

**Use this plugin for:**
- Customer research and interviews
- Problem and solution validation
- Product-market fit measurement
- Continuous discovery practices

**Installation:**
```bash
/plugin install product-discovery
```

---

### 📈 product-growth (21 items)

**Growth experiments, scaling, launches, and ROI analysis**

**What's Included:**
- 3 growth agents (growth-pm, gtm-planner, data-scientist)
- 5 growth commands (experiment design, KPIs, impact estimation, release planning, communications)
- 3 analysis tools (ROI calculator, cost-benefit analysis, Now-Next-Later roadmaps)
- 4 growth workflows (growth sprints, scaling playbooks, beta programs, product launches)
- 6 growth skills (growth frameworks, metrics, analytics, experiments, GTM, PMF)

**Use this plugin for:**
- Product launches and GTM planning
- Growth experiments and optimization
- Scaling from PMF to market leadership
- ROI analysis and business cases

**Installation:**
```bash
/plugin install product-growth
```

---

### ⚙️ product-execution (40 items)

**Daily execution, shipping features, and tactical PM work**

**What's Included:**
- 8 execution agents (agile-coach, product-ops, feature-prioritizer, requirements-engineer, technical-pm, stakeholder-manager, customer-success, api-product-manager)
- 16 tactical commands (sprint planning, user stories, PRDs, quick answers, status updates, backlog grooming)
- 2 decision tools (technical debt assessment, trade-off analysis)
- 5 operational workflows (backlog optimization, feature lifecycle, process audit, crisis management, product sunset)
- 9 practice skills (agile, prioritization, specifications, story mapping, technical debt, OKRs)

**Use this plugin for:**
- Daily PM work and sprint planning
- Feature delivery and execution
- Stakeholder management
- Process optimization

**Installation:**
```bash
/plugin install product-execution
```

---

## Plugin Structure

### Standard Plugin Layout

```
plugins/
├── product-strategy/                # Strategic planning plugin
│   ├── agents/                      # 4 strategy agents
│   ├── commands/                    # 6 planning commands
│   ├── tools/                       # 5 framework tools
│   ├── workflows/                   # 5 strategic workflows
│   ├── skills/                      # 6 strategy skills
│   └── README.md
├── product-discovery/               # Discovery & validation plugin
│   ├── agents/                      # 3 research agents
│   ├── commands/                    # 7 research commands
│   ├── tools/                       # 2 discovery tools
│   ├── workflows/                   # 4 discovery workflows
│   ├── skills/                      # 4 discovery skills
│   └── README.md
├── product-growth/                  # Growth & launches plugin
│   ├── agents/                      # 3 growth agents
│   ├── commands/                    # 5 growth commands
│   ├── tools/                       # 3 analysis tools
│   ├── workflows/                   # 4 growth workflows
│   ├── skills/                      # 6 growth skills
│   └── README.md
└── product-execution/               # Daily execution plugin
    ├── agents/                      # 8 execution agents
    ├── commands/                    # 16 tactical commands
    ├── tools/                       # 2 decision tools
    ├── workflows/                   # 5 operational workflows
    ├── skills/                      # 9 practice skills
    └── README.md
```

### Plugin Components

#### Agents (agents/)
Expert AI assistants for specific PM disciplines.

**File format**: Markdown with YAML frontmatter
**Structure**:
```yaml
---
name: agent-name
description: One-line specialty description
model: sonnet
---

# Agent Name
[Comprehensive agent documentation]
```

**Example**: `agents/product-strategist.md`

#### Commands (commands/)
Fast utilities for specific PM tasks.

**File format**: Markdown with command specification
**Structure**:
```yaml
---
name: command-name
description: What this command does
usage: /pm:command-name [arguments]
---

# Command Documentation
[Usage examples and details]
```

**Example**: `commands/capacity-planner.md`

#### Skills (skills/)
Knowledge frameworks that agents reference.

**File format**: Markdown reference guides
**Structure**:
```yaml
---
name: skill-name
description: Framework or methodology
category: prioritization|agile|research|metrics|gtm
---

# Skill Documentation
[Comprehensive framework reference]
```

**Example**: `skills/prioritization-frameworks.md` (coming soon)

---

## Installation

### Method 1: Marketplace Installation (Recommended)

```bash
# Add the marketplace
/plugin marketplace add slgoodrich/agents

# Browse available plugins
/plugin

# Install all 4 plugins (recommended)
/plugin install product-strategy product-discovery product-growth product-execution

# Or install individual plugins as needed
/plugin install product-strategy    # Strategic planning only
/plugin install product-discovery   # Discovery and research only
/plugin install product-growth      # Growth and launches only
/plugin install product-execution   # Daily execution only
```

### Method 2: Direct Installation

```bash
# Clone the repository
git clone https://github.com/slgoodrich/agents.git

# Link all plugin directories
ln -s /path/to/agents/plugins/product-strategy ~/.claude/plugins/
ln -s /path/to/agents/plugins/product-discovery ~/.claude/plugins/
ln -s /path/to/agents/plugins/product-growth ~/.claude/plugins/
ln -s /path/to/agents/plugins/product-execution ~/.claude/plugins/

# Or link individual plugins as needed
ln -s /path/to/agents/plugins/product-strategy ~/.claude/plugins/
```

### Method 3: Manual Copy

```bash
# Copy all plugin directories to Claude Code plugins folder
cp -r plugins/product-strategy ~/.claude/plugins/
cp -r plugins/product-discovery ~/.claude/plugins/
cp -r plugins/product-growth ~/.claude/plugins/
cp -r plugins/product-execution ~/.claude/plugins/

# Or copy individual plugins as needed
cp -r plugins/product-execution ~/.claude/plugins/
```

---

## Using Plugins

### Discovering What's Available

```bash
# List installed plugins
/plugin

# View plugin details
/plugin info product-strategy
/plugin info product-discovery
/plugin info product-growth
/plugin info product-execution

# List agents in a plugin
/plugin agents product-strategy    # 4 strategy agents
/plugin agents product-execution   # 8 execution agents
```

### Using Agents

Agents activate automatically when you describe what you need:

```
Tell product-strategist: "Create Q2 OKRs"
Ask user-researcher: "Design a churn study"
Get requirements-engineer: "Write PRD for dark mode"
```

Or let Claude Code route automatically:

```
"I need to create quarterly OKRs"           → product-strategist
"Help me understand user churn"             → user-researcher
"Write specs for multi-factor auth"         → requirements-engineer
"Prioritize my backlog with RICE"           → feature-prioritizer
```

### Using Commands

Commands are invoked with slash syntax:

```bash
/pm:prd "Feature description"
/pm:okr "Q2 2025"
/pm:roadmap "Product Vision 2025"
/pm:sprint-plan "Sprint 47"
```

### Using Skills (Coming Soon)

Skills are referenced automatically by agents:

```
User: "Prioritize these features"
↓
feature-prioritizer agent activates
↓
Loads prioritization-frameworks skill (RICE, ICE, Kano)
↓
Applies framework to features
↓
Returns scored backlog
```

---

## Plugin Design Principles

### 1. Single Responsibility
Each plugin focuses on one PM domain or workflow.

**Good examples:**
- `product-strategy`: Strategic planning and competitive analysis
- `product-discovery`: User research and validation
- `product-growth`: Growth experiments and launches
- `product-execution`: Daily tactical execution
- `b2b-saas-pm`: B2B SaaS-specific practices (future)

**Avoid:**
- Mixing unrelated domains (e.g., PM + engineering)
- Feature creep within a plugin
- Overlap with other plugins

### 2. Composability
Plugins work independently or together.

**Design for:**
- Standalone usage
- Clear handoffs between plugins
- No hidden dependencies
- Explicit integration points

**Example workflow:**
```
product-discovery agents → Research and validation
product-strategy agents → Feature definition and roadmap
product-execution agents → Sprint planning and delivery
product-growth agents → Launch and optimization
```

### 3. Minimal Token Usage
Load only what's needed.

**Techniques:**
- Agent activation on request
- Progressive skill loading
- Focused commands
- Lazy context loading

**Avoid:**
- Loading entire plugin into context
- Preloading all agents
- Verbose documentation in prompts

### 4. Clear Boundaries
Each plugin has distinct responsibilities.

**Questions to ask:**
- Is this capability unique to this plugin?
- Would users expect to find this here?
- Does it overlap with another plugin?
- Is the scope clear?

---

## Plugin Customization

### Forking a Plugin

To create a custom version:

```bash
# Fork the repository
git clone https://github.com/slgoodrich/agents.git

# Create custom branch
cd agents
git checkout -b custom-pm-toolkit

# Modify agents, commands, or skills in any plugin
nano plugins/product-strategy/agents/product-strategist.md
nano plugins/product-execution/commands/sprint-planner.md

# Use your custom versions
ln -s /path/to/agents/plugins/product-strategy ~/.claude/plugins/
ln -s /path/to/agents/plugins/product-execution ~/.claude/plugins/
```

### Company-Specific Plugins

Create plugins tailored to your organization:

```
plugins/
├── product-strategy-acme/       # Acme Corp strategy toolkit
│   ├── agents/
│   │   ├── product-strategist.md       # Customized for Acme
│   │   └── competitive-analyst.md      # Acme market focus
│   ├── commands/
│   │   └── acme-roadmap-template.md    # Company template
│   ├── skills/
│   │   └── acme-strategy-process.md    # Company process
│   └── README.md
└── product-execution-acme/      # Acme Corp execution toolkit
    ├── agents/
    │   └── agile-coach.md              # Acme's Scrum process
    └── README.md
```

**Benefits:**
- Company-specific terminology
- Internal tool integrations
- Custom frameworks and processes
- Proprietary methodologies

### Industry-Specific Plugins

Vertical-specific PM practices:

```
plugins/
├── product-strategy/           # Core strategy (universal)
├── product-discovery/          # Core discovery (universal)
├── product-growth/             # Core growth (universal)
├── product-execution/          # Core execution (universal)
├── b2b-saas-pm/               # B2B SaaS specialization
├── consumer-apps-pm/          # Consumer mobile/web
├── marketplace-pm/            # Two-sided marketplaces
├── fintech-pm/                # Financial products
└── healthcare-pm/             # Healthcare compliance
```

---

## Creating New Plugins

### When to Create a Plugin

Create a new plugin when:
-  You have 3+ related agents for a specific domain
-  The domain is distinct from existing plugins
-  There's a clear user need or workflow
-  The plugin can stand alone

Don't create a plugin when:
-  It's just 1-2 agents (add to existing plugin)
-  It overlaps heavily with existing plugins
-  It's too niche (create as a custom fork)
-  It mixes unrelated domains

### Plugin Creation Checklist

**1. Define Scope**
- [ ] Clear plugin purpose
- [ ] Distinct from existing plugins
- [ ] 3+ agents or substantial commands
- [ ] Specific user workflow or domain

**2. Design Structure**
- [ ] Follow standard plugin layout
- [ ] Create agents directory
- [ ] Create commands directory
- [ ] Create skills directory (if applicable)
- [ ] Write plugin README

**3. Create Components**
- [ ] Design agents with clear specialties
- [ ] Create focused commands
- [ ] Document skills and frameworks
- [ ] Write comprehensive examples

**4. Document**
- [ ] Plugin README with overview
- [ ] Installation instructions
- [ ] Usage examples
- [ ] Integration guidance
- [ ] Contribution guidelines

**5. Test**
- [ ] Verify agents activate correctly
- [ ] Test commands work as expected
- [ ] Check for conflicts with other plugins
- [ ] Validate documentation accuracy

**6. Publish**
- [ ] Add to marketplace manifest
- [ ] Tag release version
- [ ] Update main repository docs
- [ ] Announce in discussions

---

## Plugin Manifest

Plugins are registered in the marketplace manifest (`.claude-plugin/marketplace.json`):

```json
{
  "name": "product-management-toolkit",
  "plugins": [
    {
      "name": "product-strategy",
      "description": "Strategic planning, competitive analysis, business modeling",
      "version": "1.0.0",
      "author": {
        "name": "Steve Goodrich",
        "url": "https://github.com/slgoodrich"
      },
      "keywords": [
        "product-management",
        "strategy",
        "competitive-analysis",
        "roadmapping"
      ],
      "agents": [
        "./agents/product-strategist.md",
        "./agents/competitive-analyst.md",
        "./agents/platform-architect.md",
        "./agents/monetization-expert.md"
      ],
      "commands": [
        "./commands/okr-framework.md",
        "./commands/roadmap-builder.md",
        "./tools/swot-analysis.md",
        "./tools/business-model-canvas.md",
        "./workflows/quarterly-planning.md",
        "./workflows/annual-planning.md"
      ],
      "skills": [
        "./skills/product-strategy-frameworks/SKILL.md",
        "./skills/vision-mission-strategy/SKILL.md"
      ]
    },
    {
      "name": "product-discovery",
      "description": "Discovery, validation, research, PMF assessment",
      "version": "1.0.0",
      "author": {
        "name": "Steve Goodrich",
        "url": "https://github.com/slgoodrich"
      },
      "keywords": [
        "product-management",
        "discovery",
        "user-research",
        "validation"
      ],
      "agents": [
        "./agents/user-researcher.md",
        "./agents/discovery-facilitator.md",
        "./agents/customer-insights.md"
      ],
      "commands": [
        "./commands/interview-guide.md",
        "./commands/persona-creator.md",
        "./tools/assumption-mapping.md",
        "./workflows/discovery-sprint.md",
        "./workflows/pmf-assessment.md"
      ],
      "skills": [
        "./skills/continuous-discovery/SKILL.md",
        "./skills/user-research-techniques/SKILL.md"
      ]
    }
  ]
}
```

**Important**: While the codebase organizes files into `tools/` and `workflows/` directories, they are **registered as commands** in the manifest. The Claude Code plugin schema only recognizes:
- `agents` - AI expert subagents
- `commands` - Slash commands (includes tools and workflows)
- `skills` - Knowledge frameworks
- `hooks` - Event handlers
- `mcpServers` - MCP server configs

The directory structure (`tools/`, `workflows/`, `commands/`) is organizational only.

---

## Plugin Versioning

### Semantic Versioning

Plugins follow semver: `MAJOR.MINOR.PATCH`

**MAJOR** (1.0.0 → 2.0.0): Breaking changes
- Agent interface changes
- Command argument changes
- Removed agents or commands

**MINOR** (1.0.0 → 1.1.0): New features
- New agents added
- New commands added
- New skills added
- Enhanced capabilities

**PATCH** (1.0.0 → 1.0.1): Bug fixes
- Agent documentation improvements
- Bug fixes
- Minor tweaks

### Version Management

```bash
# Install specific version
/plugin install product-strategy@1.0.0
/plugin install product-execution@1.0.0

# Update to latest
/plugin update product-strategy
/plugin update product-discovery product-growth product-execution

# List versions
/plugin versions product-strategy
```

---

## Plugin Dependencies

### Standalone vs. Dependent

**Standalone plugins** (recommended):
- No dependencies on other plugins
- Work independently
- Self-contained capabilities

**Dependent plugins**:
- Require other plugins
- Extend or specialize another plugin
- Clearly document dependencies

**Example dependency:**
```yaml
# Plugin manifest
name: b2b-saas-pm
dependencies:
  - product-strategy: ^1.0.0
  - product-growth: ^1.0.0
description: Extends core plugins with B2B SaaS-specific practices
```

---

## Plugin Performance

### Token Usage

**Small plugin** (<5 agents): ~2,000-5,000 tokens per invocation
**Medium plugin** (5-15 agents): ~5,000-10,000 tokens
**Large plugin** (15+ agents): ~10,000-20,000 tokens

**Optimization techniques:**
- Lazy agent loading
- Progressive skill disclosure
- Focused command scopes
- Efficient agent instructions

### Response Time

Factors affecting speed:
- Number of agents in plugin
- Agent complexity
- Skill loading
- Model selection (Sonnet vs Haiku)

**Best practices:**
- Use commands for speed
- Invoke specific agents when known
- Minimize skill loading
- Keep agent instructions concise

---

## Plugin Marketplace

### Publishing to Marketplace

```bash
# 1. Create plugin following standards
# 2. Add to marketplace manifest
# 3. Submit PR to slgoodrich/agents
# 4. Review and approval
# 5. Published!
```

### Discovery

Users find plugins via:
- `/plugin` command (browse installed)
- `/plugin marketplace` (browse available)
- GitHub repository README
- Documentation website

---

## Plugin Roadmap

### Current Plugins (v1.0 - Production Ready)

**product-strategy** (26 items)
- 4 strategy agents
- 6 planning commands
- 5 framework tools
- 5 strategic workflows
- 6 strategy skills

**product-discovery** (20 items)
- 3 research agents
- 7 research commands
- 2 discovery tools
- 4 discovery workflows
- 4 discovery skills

**product-growth** (21 items)
- 3 growth agents
- 5 growth commands
- 3 analysis tools
- 4 growth workflows
- 6 growth skills

**product-execution** (40 items)
- 8 execution agents
- 16 tactical commands
- 2 decision tools
- 5 operational workflows
- 9 practice skills

### Planned Industry Plugins (v1.1+)

**b2b-saas-pm** (Q2 2025)
- Enterprise sales motion
- B2B metrics and KPIs
- Multi-tenant considerations
- Contract negotiation

**consumer-apps-pm** (Q2 2025)
- App store optimization
- Virality and growth loops
- Consumer engagement metrics
- Mobile-first design

**marketplace-pm** (Q3 2025)
- Two-sided marketplace strategy
- Supply and demand balance
- Marketplace metrics
- Network effects

**data-products-pm** (Q3 2025)
- Data product strategy
- Analytics products
- ML/AI products
- Data monetization

### Planned Extension Plugins (v1.1+)

**pm-integrations** (Q3 2025)
- Jira, Linear, Asana sync
- Productboard integration
- Amplitude, Mixpanel analytics
- Slack, Teams notifications

**pm-templates** (Q2 2025)
- PRD templates
- OKR templates
- Roadmap templates
- Launch checklist templates

---

## Plugin Best Practices

### For Plugin Users

1. **Start with All 4**: Install all core plugins (strategy, discovery, growth, execution) for complete toolkit
2. **Or Install Selectively**: Install only the plugins you need for your current work
3. **Keep Updated**: Update plugins regularly for latest features and fixes
4. **Provide Feedback**: Report issues and suggest improvements
5. **Contribute Examples**: Share successful workflows and use cases

### For Plugin Creators

1. **Single Responsibility**: One plugin, one domain
2. **Clear Documentation**: Comprehensive README and examples
3. **Consistent Structure**: Follow standard plugin layout
4. **Test Thoroughly**: Verify all agents and commands
5. **Version Properly**: Use semantic versioning
6. **Support Users**: Respond to issues and questions

---

## Troubleshooting

### Plugin Not Loading

```bash
# Verify plugins are installed
/plugin

# Check plugin directories exist
ls ~/.claude/plugins/product-strategy
ls ~/.claude/plugins/product-execution

# Reinstall if needed
/plugin uninstall product-strategy
/plugin install product-strategy

# Or reinstall all
/plugin uninstall product-strategy product-discovery product-growth product-execution
/plugin install product-strategy product-discovery product-growth product-execution
```

### Agent Not Activating

```
# Be specific in your request
 "Help with strategy"
 "Tell product-strategist: Create Q2 OKRs"
 "Ask user-researcher: Design churn study"

# Or describe the task clearly
 "I need to create quarterly OKRs for my product team"      → product-strategist
 "Help me understand why users are churning"                → user-researcher
 "Plan my next sprint"                                      → agile-coach
```

### Command Not Found

```bash
# Verify command exists in the right plugin
/plugin info product-strategy      # OKRs, roadmaps
/plugin info product-execution     # Sprint planning, PRDs

# Check command syntax
/pm:prd --help
/pm:sprint-planner --help

# Update plugins to latest version
/plugin update product-strategy product-discovery product-growth product-execution
```

---

## Contributing Plugins

We welcome plugin contributions! See [CONTRIBUTING.md](../CONTRIBUTING.md) for:
- Plugin proposal process
- Quality standards
- Review criteria
- Publication workflow

**Ways to contribute:**
- Create industry-specific plugins
- Add agents to existing plugins
- Improve documentation
- Share usage examples

---

## Questions & Support

- **Documentation**: See plugin README files
- **Examples**: Check `usage.md` for workflows
- **Issues**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)

---

**Current Plugins**: 4 (product-strategy, product-discovery, product-growth, product-execution)
**Total Items**: 103 (18 agents, 31 commands, 12 tools, 18 workflows, 24 skills)
**Planned Plugins**: 6+ (B2B SaaS, consumer, marketplace, data, integrations, templates)
**Version**: 1.0.0
**Last Updated**: October 2025
