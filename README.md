# Product Management Toolkit for Claude Code

**The ultimate product management plugin suite** - Transform Claude Code into your full-stack PM copilot for strategy, discovery, delivery, and growth.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-purple)](https://claude.com/claude-code)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/slgoodrich/agents/releases)
[![GitHub Issues](https://img.shields.io/github/issues/slgoodrich/agents.svg)](https://github.com/slgoodrich/agents/issues)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## Overview

This plugin marketplace provides comprehensive product management capabilities for Claude Code, enabling PMs to work at the speed of thought across the entire product lifecycle.

**What You Get:**
-  8 specialized AI agents (strategy, research, requirements, agile, prioritization, GTM, growth, stakeholder management)
-  15 command tools (PRD generation, roadmaps, OKRs, sprint planning, research synthesis)
-  5 knowledge skills (prioritization frameworks, agile methods, research techniques, metrics, GTM playbooks)
-  Battle-tested PM frameworks (RICE, Kano, AARRR, HEART, Shape Up, and more)

---

## Quick Start

### Installation

```bash
# Add this marketplace
/plugin marketplace add slgoodrich/agents

# Install the product management plugin
/plugin install product-management
```

### First Commands

```bash
# Generate a PRD
/pm:prd "Dark mode for mobile app"

# Create quarterly OKRs
/pm:okr "Q2 2025"

# Build a roadmap
/pm:roadmap "Product Vision 2025"

# Plan a sprint
/pm:sprint-plan "Sprint 47"
```

---

## What's Included

###  AI Agents

Expert partners for every PM discipline:

| Agent | Specialty | Use For |
|-------|-----------|---------|
| **product-strategist** | Vision, strategy, roadmaps | Strategy, OKRs, competitive positioning |
| **user-researcher** | Research, interviews, testing | Discovery, validation, user insights |
| **requirements-engineer** | PRDs, specs, user stories | Documentation, acceptance criteria |
| **agile-coach** | Sprint planning, ceremonies | Scrum, Kanban, backlog grooming |
| **feature-prioritizer** | RICE, ICE, trade-offs | Prioritization, roadmap ranking |
| **gtm-planner** | Launches, positioning | GTM strategy, product launches |
| **growth-pm** | Growth loops, experiments | Funnel optimization, A/B testing |
| **stakeholder-manager** | Alignment, communication | Stakeholder mapping, exec updates |

###  Command Tools

Fast, focused utilities:

**Documentation**: PRD, user stories, release notes, decision logs
**Planning**: Roadmaps, OKRs, sprint planning, backlog grooming
**Research**: Personas, journey maps, interview guides, synthesis
**Analytics**: KPI dashboards, experiment design
**Collaboration**: Stakeholder mapping, decision logging

###  Knowledge Skills

Comprehensive frameworks:

- **Prioritization Methods**: RICE, ICE, MoSCoW, Kano, Value vs Effort
- **Agile Methodologies**: Scrum, Kanban, SAFe, Shape Up, Dual-Track
- **User Research**: Interviews, usability testing, surveys, synthesis
- **Metrics Frameworks**: AARRR, HEART, North Star, OKRs
- **GTM Playbooks**: PLG, sales-led, positioning, launches

---

## Use Cases

### Scenario 1: Quarterly Planning

```bash
# 1. Set strategic direction
Tell product-strategist: "Create Q2 2025 vision and themes"

# 2. Generate OKRs
/pm:okr "Q2 2025" --focus growth

# 3. Build roadmap
/pm:roadmap "Q2 2025"

# 4. Prioritize backlog
Tell feature-prioritizer: "Score backlog with RICE"

# 5. Align stakeholders
/pm:stakeholder-map "Q2 Planning"
```

### Scenario 2: Feature Development

```bash
# 1. Write comprehensive PRD
/pm:prd "Multi-factor authentication"

# 2. Break into user stories
/pm:user-stories [paste PRD]

# 3. Create sprint plan
/pm:sprint-plan "Sprint 48"

# 4. Plan GTM
Tell gtm-planner: "Beta launch for MFA"

# 5. Set success metrics
/pm:kpi-dashboard "MFA Success Metrics"
```

### Scenario 3: Discovery & Research

```bash
# 1. Plan research
/pm:interview-guide "Why users churn after 30 days"

# 2. Conduct interviews (manual)

# 3. Synthesize findings
/pm:research-synthesize [interview notes]

# 4. Create personas
/pm:persona "Power User"

# 5. Map journey
/pm:journey-map "Power User onboarding"

# 6. Identify opportunities
Tell user-researcher: "What features should we build based on this research?"
```

### Scenario 4: Growth Optimization

```bash
# 1. Analyze current metrics
/pm:kpi-dashboard "Activation Metrics"

# 2. Design experiment
/pm:experiment "Social proof to increase signups"

# 3. Optimize funnel
Tell growth-pm: "50% drop-off at onboarding, help optimize"

# 4. Build growth roadmap
Tell product-strategist: "Growth-focused Q2 roadmap"
```

---

## Plugin Structure

```
plugins/
└── product-management/          # The complete PM toolkit
    ├── agents/                  # 8 specialized agents
    ├── commands/                # 15 focused tools
    ├── skills/                  # 5 knowledge frameworks
    └── README.md                # Plugin documentation
```

---

## Companion Repository

For complex multi-agent workflows, check out [Commands Repository](https://github.com/slgoodrich/commands):

- Feature lifecycle workflows (Idea → Launch)
- Quarterly planning orchestration
- Product launch automation
- Discovery sprint facilitation
- And more...

---

## Philosophy

### Built for Modern PMs

This toolkit embodies modern product management best practices:

- **User-Centric**: Research and discovery built-in
- **Data-Driven**: Metrics and frameworks at your fingertips
- **Collaborative**: Stakeholder alignment tools
- **Agile**: Sprint planning and execution support
- **Strategic**: Vision and roadmap capabilities
- **Growth-Focused**: Optimization and experimentation

### Inspired By

- **Teresa Torres** - Continuous Discovery Habits
- **Marty Cagan** - Empowered Teams, Product Leadership
- **April Dunford** - Obviously Awesome (Positioning)
- **Sean Ellis** - Hacking Growth (ICE, Growth Frameworks)
- **Jeff Patton** - User Story Mapping
- **Gibson Biddle** - Ask Gib (DHM Model)
- **Intercom** - RICE Prioritization
- **Google** - HEART Framework, OKRs
- **Basecamp** - Shape Up

---

## Requirements

- Claude Code (latest version)
- Basic familiarity with product management concepts

---

## Getting Help

### Documentation
- Plugin README: `plugins/product-management/README.md`
- Agent documentation: Each agent has comprehensive inline docs
- Skills: Each skill is a full reference guide

### Support
- **Issues**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)
- **Questions**: Open a discussion with the `question` label

### Contributing

Contributions are welcome! This toolkit grows with the PM community.

**Ways to contribute:**
- Report bugs or request features
- Submit new agents or commands
- Improve documentation
- Share use cases and examples
- Add industry-specific playbooks

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Roadmap

### Current (v1.0)
-  8 core agents
-  15 essential commands
-  5 comprehensive skills

### Planned (v1.1)
-  10 additional agents (data-scientist, competitive-analyst, technical-pm, etc.)
-  30 more commands
-  Multi-agent workflows
-  Industry-specific playbooks (B2B SaaS, consumer, marketplace)

### Future
- Templates library (PRD templates, OKR templates, etc.)
- Integration with PM tools (Jira, Linear, ProductBoard)
- Metrics dashboards and tracking
- Collaborative PM workflows

---

## Examples & Templates

### Example Agents Usage

**Strategy Session:**
```
Tell product-strategist:
"I'm a PM at a Series A startup building analytics software.
Help me craft a 3-year product vision and Q1 2025 OKRs."
```

**Research Planning:**
```
Tell user-researcher:
"We have 30% churn after the first month. Design a research study
to understand why users aren't finding value."
```

**Sprint Planning:**
```
Tell agile-coach:
"Plan Sprint 47 for my 5-person team. We have velocity of 32 points,
Bob is out for 2 days, and we need to ship auth by end of sprint."
```

### Example Commands

**Generate PRD:**
```
/pm:prd "Users need to be able to export their data in CSV, JSON, and PDF formats"
```

**Create OKRs:**
```
/pm:okr "Q2 2025" --theme "Product-Market Fit"
```

**Build Roadmap:**
```
/pm:roadmap "2025 Platform Strategy"
```

---

## Performance & Best Practices

### Efficiency Tips

1. **Use Commands for Speed**: Commands are faster for straightforward tasks
2. **Use Agents for Complexity**: Agents provide deep expertise and nuance
3. **Combine Tools**: Feed command outputs to agents for refinement
4. **Reference Skills**: Agents automatically reference relevant skills
5. **Iterate**: Generate drafts quickly, then refine

### Model Selection

- **Agents**: Use Sonnet 4.5 (complex reasoning, strategic thinking)
- **Commands**: Use Sonnet 4.5 (comprehensive outputs)
- **Skills**: Knowledge bases (no model needed)

---

## FAQ

**Q: Can I use this without product management experience?**
A: Yes! The agents teach PM concepts while helping you. Start with `product-strategist` for guidance.

**Q: Does this replace PM tools like Jira or Linear?**
A: No, this complements them. Use this for thinking and planning, then implement in your PM tools.

**Q: Can I customize agents or commands?**
A: Yes! Fork the repo and modify to your needs. Contributions back are welcome.

**Q: What's the difference between agents and commands?**
A: Agents are interactive experts you converse with. Commands are quick utilities for specific tasks.

**Q: Do I need all agents?**
A: No, use what you need. But having the full toolkit means you're ready for any PM scenario.

**Q: Can I use this for non-software products?**
A: The frameworks are universal, but examples are software-focused. Adapt as needed.

---

## License

MIT License - See [LICENSE](LICENSE) for details

---

## Acknowledgments

**Built with:**
- Claude Code's plugin framework
- Modern PM methodologies
- Community feedback and contributions

**Special thanks to:**
- The Claude Code team at Anthropic
- Product management thought leaders
- Early adopters and contributors

---

## Stay Connected

- **Repository**: https://github.com/slgoodrich/agents
- **Commands Repo**: https://github.com/slgoodrich/commands
- **Issues**: Report bugs or request features
- **Discussions**: Share use cases and ask questions

---

**Version**: 1.0.0
**Status**: Production Ready
**Last Updated**: January 2025
**Maintainer**: [@slgoodrich](https://github.com/slgoodrich)

---

*Empowering product managers to work at the speed of thought.*
