# Plugin Guide

## Overview

The Product Management Toolkit is distributed as a **single comprehensive plugin** that includes all PM capabilities. This simplified architecture makes installation and updates easier while providing access to 1 orchestration agent, 7 specialist agents, 16 skills, and context-aware workflows.

---

## Architecture

**Single unified plugin** provides:

- Complete PM toolkit in one install: `/plugin install ai-pm-copilot`
- 1 orchestration agent + 7 specialist agents with intelligent routing
- 16 skills with 100+ assets and references
- Unified versioning and updates
- No plugin dependencies

---

## Installation

### Quick Start

Install the complete toolkit with one command:

```bash
/plugin install ai-pm-copilot
```

That's it! You now have access to:

- **1 orchestration agent + 7 specialist agents** (product-manager routes to market-analyst, research-ops, product-strategist, roadmap-builder, feature-prioritizer, requirements-engineer, launch-planner)
- **16 skills** with 63 assets and 37 reference guides
- **1 command** (pm-setup for context initialization)

### Initial Setup

After installation, initialize your product context:

```bash
/ai-pm-copilot:pm-setup
```

This creates `.claude/product-context/` directory with 8 context files that all agents will reference:

- product-info.md
- metrics.md
- goals.md
- roadmap.md
- tech-stack.md
- customers.md
- team.md
- competitors.md

---

## Plugin Structure

```
ai-pm-copilot/
├── agents/          # 1 orchestration + 7 specialist agents
├── commands/        # 1 command (pm-setup)
└── skills/          # 16 skills with assets and references
```

### Agents

The plugin includes 1 orchestration agent and 7 specialist agents covering the complete PM lifecycle:

1. **product-manager** - Main routing agent, coordinates specialists
2. **market-analyst** - Market research, competitive analysis, positioning
3. **research-ops** - User research, interviews, usability testing
4. **product-strategist** - Strategy, vision, positioning
5. **roadmap-builder** - Roadmap creation and planning
6. **feature-prioritizer** - RICE/ICE/Kano scoring, prioritization
7. **requirements-engineer** - PRDs, specs, user stories
8. **launch-planner** - GTM strategy, launch planning

See [Agents Guide](agents.md) for detailed documentation.

### Skills

16 specialized skills provide framework knowledge:

**User Research** (5): user-research-techniques, interview-frameworks, synthesis-frameworks, usability-frameworks, validation-frameworks

**Strategy** (4): product-positioning, competitive-analysis-templates, market-sizing-frameworks, product-market-fit

**Execution** (5): roadmap-frameworks, prioritization-methods, specification-techniques, prd-templates, user-story-templates

**Launch** (2): go-to-market-playbooks, launch-planning-frameworks

See [Skills Reference](agent-skills.md) for detailed documentation.

### Command

**pm-setup** - Initialize .claude/product-context/ directory structure

---

## Usage Patterns

### Conversational Interface (Primary)

Talk directly to agents through the product-manager routing agent:

```
User: "Help me prioritize these 5 features"
→ product-manager routes to feature-prioritizer
→ Returns scored features with RICE framework

User: "Create a PRD for dark mode feature"
→ product-manager routes to requirements-engineer
→ Returns structured PRD using prd-templates skill

User: "Plan Q1 product launch"
→ product-manager routes to launch-planner
→ Returns launch plan using go-to-market-playbooks skill
```

### Direct Agent Invocation

For complex scenarios, invoke specialist agents directly:

```
Tell research-ops: "Design a user interview for payment flow"
Tell market-analyst: "Analyze our competitive position in SaaS CRM"
Tell roadmap-builder: "Create a Now-Next-Later roadmap"
```

### Command Usage

Use pm-setup command for initial context setup:

```bash
/ai-pm-copilot:pm-setup
```

---

## Version Management

### Current Status

- **Status**: 13/13 tests passing, production-ready
- **Components**: 9 agents, 1 command, 16 skills (63 assets + 37 references)

### Checking Version

```bash
/plugin list
```

### Updating

```bash
/plugin update ai-pm-copilot
```

### Rollback

If you need to rollback to a previous version:

```bash
/plugin uninstall ai-pm-copilot
/plugin install ai-pm-copilot@<version>
```

---

## Target Audience

The toolkit is optimized for **solo developers and small teams**:

- No stakeholder management jargon
- No corporate PM processes (RACI matrices, executive alignment)
- Practical, action-oriented guidance
- Templates scaled for lean teams
- Direct, efficient communication

---

## Performance & Testing

### Quality Standards

- All 9 agents have valid frontmatter and documentation
- All 16 skills have SKILL.md files
- 63/63 assets referenced in parent SKILL.md
- 37/37 references documented
- 0 orphaned skills (all actively used by agents)
- 0 stakeholder references (solo dev focused)

---

## Contributing

Want to contribute to the ai-pm-copilot plugin?

### Areas for Contribution

- **New Skills**: Add framework knowledge (e.g., "lean-startup-frameworks")
- **Agent Improvements**: Enhance agent instructions and examples
- **Assets**: Add templates, checklists, frameworks to skills
- **Documentation**: Improve usage examples and guides
- **Testing**: Expand test coverage

### Contribution Process

1. Fork the repository
2. Create feature branch
3. Follow existing patterns (see [Architecture](architecture.md))
4. Test your changes
5. Submit pull request

See CONTRIBUTING.md (coming soon) for detailed guidelines.

---

## Questions & Support

- **Installation Issues**: Check Claude Code plugin documentation
- **Usage Questions**: See [Usage Guide](usage.md) for patterns and examples
- **Feature Requests**: Open GitHub Issue
- **Bug Reports**: Open GitHub Issue with test results

---

## Related Documentation

- [Agents Guide](agents.md) - Detailed agent documentation
- [Skills Reference](agent-skills.md) - Complete skills catalog
- [Architecture](architecture.md) - System design and patterns
- [Usage Guide](usage.md) - Usage patterns and examples

---

**Plugin**: ai-pm-copilot
**Components**: 9 agents, 1 command, 16 skills
**Status**: Production-ready (13/13 tests passing)
**Last Updated**: October 2025
