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

## Available Plugins

### product-management (Core Plugin)

**The foundational PM toolkit** covering the entire product lifecycle.

**What's Included:**
- 18 specialized PM agents
- Commands for common PM tasks
- Comprehensive documentation
- Framework and methodology references

**Size**: 18 agents, 1+ commands
**Focus**: End-to-end product management

**Use this plugin for:**
- Strategy and planning
- Discovery and research
- Requirements and delivery
- Growth and optimization
- GTM and stakeholder management

**Installation:**
```bash
/plugin install product-management
```

---

## Plugin Structure

### Standard Plugin Layout

```
plugins/
└── product-management/              # Plugin name
    ├── agents/                      # AI agents directory
    │   ├── product-strategist.md    # Individual agent
    │   ├── user-researcher.md
    │   ├── requirements-engineer.md
    │   └── ...                      # 18 total agents
    ├── commands/                    # Command tools directory
    │   ├── capacity-planner.md      # Individual command
    │   └── ...                      # More commands coming
    ├── skills/                      # Knowledge frameworks (planned)
    │   ├── prioritization-frameworks.md
    │   ├── agile-methodologies.md
    │   └── ...
    └── README.md                    # Plugin documentation
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
model: claude-sonnet-4-5
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

# Install the PM toolkit
/plugin install product-management
```

### Method 2: Direct Installation

```bash
# Clone the repository
git clone https://github.com/slgoodrich/agents.git

# Link the plugin directory
ln -s /path/to/agents/plugins/product-management ~/.claude/plugins/
```

### Method 3: Manual Copy

```bash
# Copy plugin directory to Claude Code plugins folder
cp -r plugins/product-management ~/.claude/plugins/
```

---

## Using Plugins

### Discovering What's Available

```bash
# List installed plugins
/plugin

# View plugin details
/plugin info product-management

# List agents in a plugin
/plugin agents product-management
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
- `product-management`: Core end-to-end PM toolkit
- `b2b-saas-pm`: B2B SaaS-specific practices (future)
- `growth-toolkit`: Deep growth specialization (future)

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
product-management agents → Feature definition
engineering-toolkit → Implementation
product-management agents → Launch
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

# Modify agents, commands, or skills
nano plugins/product-management/agents/product-strategist.md

# Use your custom version
ln -s /path/to/agents/plugins/product-management ~/.claude/plugins/
```

### Company-Specific Plugins

Create plugins tailored to your organization:

```
plugins/
└── product-management-acme/     # Acme Corp PM toolkit
    ├── agents/
    │   ├── product-strategist.md       # Customized for Acme
    │   └── ...
    ├── commands/
    │   └── acme-roadmap-template.md    # Company template
    ├── skills/
    │   └── acme-pm-process.md          # Company process
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
├── product-management/          # Core (universal)
├── b2b-saas-pm/                # B2B SaaS specialization
├── consumer-apps-pm/           # Consumer mobile/web
├── marketplace-pm/             # Two-sided marketplaces
├── fintech-pm/                 # Financial products
└── healthcare-pm/              # Healthcare compliance
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

Plugins are registered in the marketplace manifest:

```yaml
# .claude/marketplace.yaml
plugins:
  - name: product-management
    description: Complete product management toolkit
    version: 1.0.0
    author: slgoodrich
    agents: 18
    commands: 1+
    status: production
    tags:
      - product-management
      - strategy
      - discovery
      - agile
      - growth
```

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
/plugin install product-management@1.0.0

# Update to latest
/plugin update product-management

# List versions
/plugin versions product-management
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
  - product-management: ^1.0.0
description: Extends product-management with B2B SaaS specifics
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

## Future Plugin Roadmap

### Planned Core Plugins

**product-management** (current)
- 18 PM agents
- Command expansion
- Skills system

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

### Planned Extension Plugins

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

1. **Start with Core**: Install `product-management` first
2. **Add as Needed**: Install specialized plugins when needed
3. **Keep Updated**: Update plugins regularly
4. **Provide Feedback**: Report issues and suggest improvements
5. **Contribute Examples**: Share successful workflows

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
# Verify plugin is installed
/plugin

# Check plugin directory exists
ls ~/.claude/plugins/product-management

# Reinstall if needed
/plugin uninstall product-management
/plugin install product-management
```

### Agent Not Activating

```
# Be specific in your request
 "Help with strategy"
 "Tell product-strategist: Create Q2 OKRs"

# Or describe the task clearly
 "I need to create quarterly OKRs for my product team"
```

### Command Not Found

```bash
# Verify command exists in plugin
/plugin info product-management

# Check command syntax
/pm:prd --help

# Update plugin to latest version
/plugin update product-management
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

**Current Plugins**: 1 (product-management)
**Planned Plugins**: 5+ (B2B SaaS, consumer, marketplace, data, integrations)
**Version**: 1.0.0
**Last Updated**: January 2025
