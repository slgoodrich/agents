# Product Management Plugin

The complete product management toolkit for Claude Code - empowering PMs to work at the speed of thought across strategy, discovery, delivery, and growth.

## Overview

This plugin transforms Claude Code into your full-stack PM copilot, handling everything from quarterly planning to sprint execution, user research to product launches.

**What's Included:**
-  **8 Specialized AI Agents** - Expert partners for every PM discipline
-  **15 Command Tools** - Single-purpose utilities for common PM tasks
-  **5 Knowledge Skills** - Comprehensive frameworks and methodologies
-  **Battle-Tested Frameworks** - RICE, OKRs, AARRR, Kano, and more

## Installation

```bash
# Add the marketplace
/plugin marketplace add slgoodrich/agents

# Install the plugin
/plugin install product-management
```

## Quick Start

### Generate a PRD
```bash
/pm:prd "We need dark mode for our mobile app"
```

### Create Quarterly OKRs
```bash
/pm:okr "Q2 2025" --focus growth
```

### Build a Product Roadmap
```bash
/pm:roadmap "2025 Product Vision"
```

### Plan a Sprint
```bash
/pm:sprint-plan "Sprint 47" --velocity 32
```

---

##  AI Agents

Specialized agents with deep expertise in specific PM domains.

### Strategic Planning

#### `product-strategist`
Vision, strategy, roadmaps, and OKRs. Your strategic thinking partner.

**Use for:**
- Crafting product vision and strategy
- Building strategic roadmaps
- Creating OKRs (quarterly/annual)
- Competitive positioning
- Market analysis
- Portfolio management

**Example:**
```
Tell product-strategist: "Help me create a 3-year vision for our AI analytics platform"
```

---

### Discovery & Research

#### `user-researcher`
User research, interviews, usability testing, and insight synthesis.

**Use for:**
- Planning research studies
- Creating interview guides
- Usability test design
- Research synthesis
- Persona development
- Journey mapping

**Example:**
```
Tell user-researcher: "Design a study to understand why activation rate is only 40%"
```

---

### Requirements & Delivery

#### `requirements-engineer`
PRDs, technical specs, user stories, and acceptance criteria.

**Use for:**
- Writing comprehensive PRDs
- Creating user stories
- Defining acceptance criteria
- Technical specifications
- API documentation
- Breaking down epics

**Example:**
```
Tell requirements-engineer: "Convert this feature idea into a detailed PRD with acceptance criteria"
```

#### `agile-coach`
Sprint planning, ceremonies, backlog grooming, and process optimization.

**Use for:**
- Sprint planning
- Backlog refinement
- Facilitating retrospectives
- Agile process optimization
- Velocity tracking
- Ceremony facilitation

**Example:**
```
Tell agile-coach: "Plan Sprint 47 for a 5-person team with 32-point velocity"
```

---

### Prioritization & Planning

#### `feature-prioritizer`
RICE, ICE, Kano, and value/effort prioritization frameworks.

**Use for:**
- Scoring features with RICE/ICE
- Value vs effort analysis
- Building prioritized backlogs
- Trade-off decisions
- Roadmap ranking
- Stakeholder alignment

**Example:**
```
Tell feature-prioritizer: "Score these 10 features using RICE framework"
```

---

### Growth & Launch

#### `gtm-planner`
Go-to-market strategy, product launches, positioning, and messaging.

**Use for:**
- Planning product launches
- Positioning and messaging
- GTM strategy development
- Beta program design
- Launch asset creation
- Market entry planning

**Example:**
```
Tell gtm-planner: "Create a launch plan for our new AI features"
```

#### `growth-pm`
Growth loops, experiments, funnels, and product-led growth strategies.

**Use for:**
- Growth strategy development
- Funnel optimization
- A/B experiment design
- Viral loop creation
- Activation improvement
- Retention strategies

**Example:**
```
Tell growth-pm: "Our activation rate is 40%. Design experiments to improve it to 70%"
```

---

### Collaboration

#### `stakeholder-manager`
Cross-functional alignment, executive communication, and consensus building.

**Use for:**
- Stakeholder mapping
- Communication strategies
- Executive updates
- Decision facilitation
- Escalation handling
- RACI matrices

**Example:**
```
Tell stakeholder-manager: "Engineering wants to delay launch by 2 months. Help me navigate this"
```

---

##  Command Tools

Fast, focused commands for common PM tasks.

### Documentation

| Command | Purpose |
|---------|---------|
| `/pm:prd` | Generate comprehensive PRD |
| `/pm:user-stories` | Convert requirements to user stories |
| `/pm:release-notes` | Create customer-facing release notes |
| `/pm:decision-log` | Document key decisions |

### Planning

| Command | Purpose |
|---------|---------|
| `/pm:roadmap` | Build strategic roadmaps (Now/Next/Later) |
| `/pm:okr` | Create quarterly/annual OKRs |
| `/pm:sprint-plan` | Plan agile sprints |
| `/pm:backlog-groom` | Refine and organize backlog |

### Research

| Command | Purpose |
|---------|---------|
| `/pm:persona` | Generate user personas |
| `/pm:journey-map` | Create customer journey maps |
| `/pm:interview-guide` | Build research interview protocols |
| `/pm:research-synthesize` | Analyze and synthesize research findings |

### Analytics

| Command | Purpose |
|---------|---------|
| `/pm:kpi-dashboard` | Define KPI frameworks |
| `/pm:experiment` | Design A/B tests and experiments |

### Collaboration

| Command | Purpose |
|---------|---------|
| `/pm:stakeholder-map` | Map stakeholders with engagement strategy |
| `/pm:decision-log` | Document decisions with context and rationale |

---

##  Knowledge Skills

Comprehensive frameworks and methodologies that agents can reference.

### `prioritization-methods`
RICE, ICE, MoSCoW, Kano, Value vs Effort, Weighted Scoring, Opportunity Scoring

**When to use:**
- Choosing between features
- Building roadmaps
- Making trade-offs
- Stakeholder alignment

**Frameworks included:**
- RICE (Reach × Impact × Confidence / Effort)
- ICE (Impact + Confidence + Ease)
- Value vs Effort Matrix
- MoSCoW (Must/Should/Could/Won't)
- Kano Model
- Weighted Scoring
- Opportunity Scoring (JTBD)

---

### `agile-methodologies`
Scrum, Kanban, SAFe, Shape Up, Scrumban, Dual-Track Agile

**When to use:**
- Implementing agile processes
- Choosing methodology
- Optimizing team workflow
- Scaling agile

**Frameworks included:**
- Scrum (sprints, ceremonies, roles)
- Kanban (flow, WIP limits)
- Shape Up (6-week cycles, betting)
- SAFe (scaled agile)
- Dual-Track Agile (discovery + delivery)

---

### `user-research-techniques`
Interviews, usability testing, surveys, ethnography, synthesis

**When to use:**
- Planning research
- Conducting studies
- Analyzing findings
- Validating assumptions

**Methods included:**
- User interviews
- Usability testing
- Surveys (NPS, CSAT, CES)
- Field studies
- Card sorting
- Analytics
- A/B testing

---

### `metrics-frameworks`
AARRR, HEART, North Star Metric, OKRs

**When to use:**
- Defining KPIs
- Measuring success
- Setting goals
- Tracking growth

**Frameworks included:**
- AARRR (Pirate Metrics)
- HEART (Google framework)
- North Star Metric
- OKRs
- SaaS metrics (MRR, churn, LTV)

---

### `go-to-market-playbooks`
PLG, sales-led, positioning, launches, market entry

**When to use:**
- Planning launches
- Positioning products
- Entering markets
- GTM strategy

**Playbooks included:**
- Product-Led Growth (PLG)
- Sales-Led Growth
- Community-Led Growth
- Positioning framework (April Dunford)
- Launch strategies
- Market entry tactics

---

## Workflows

For complex, multi-step workflows, see the [Commands Repository](https://github.com/slgoodrich/commands) which includes:

- `/workflows:feature-lifecycle` - Idea → Discovery → Build → Launch
- `/workflows:quarterly-planning` - OKR and roadmap planning
- `/workflows:product-launch` - Full GTM orchestration
- `/workflows:discovery-sprint` - Problem and solution validation
- More...

---

## Usage Examples

### Example 1: Quarterly Planning

```bash
# Generate quarterly OKRs
/pm:okr "Q2 2025" --focus growth

# Build roadmap aligned to OKRs
/pm:roadmap "Q2 2025 Roadmap"

# Prioritize backlog
Tell feature-prioritizer: "Score these 15 features using RICE"

# Create stakeholder alignment plan
/pm:stakeholder-map "Q2 Planning"
```

### Example 2: Feature Development

```bash
# Write PRD
/pm:prd "Multi-factor authentication for enterprise users"

# Break into user stories
/pm:user-stories [paste PRD]

# Plan sprint
/pm:sprint-plan "Sprint 48"

# Create launch plan
Tell gtm-planner: "Plan beta launch for MFA feature"
```

### Example 3: Research & Discovery

```bash
# Create interview guide
/pm:interview-guide "Understanding why users churn after 30 days"

# [Conduct interviews]

# Synthesize findings
/pm:research-synthesize [paste interview notes]

# Generate personas
/pm:persona "Enterprise IT Admin"

# Map journey
/pm:journey-map "Enterprise IT Admin onboarding flow"
```

### Example 4: Growth Optimization

```bash
# Define metrics
/pm:kpi-dashboard "Growth Metrics"

# Design experiment
/pm:experiment "Add social proof to increase signup conversion"

# Analyze funnel
Tell growth-pm: "Our activation funnel shows 50% drop-off at onboarding. Help me optimize"

# Create growth roadmap
Tell product-strategist: "Build a growth-focused roadmap for next quarter"
```

---

## Best Practices

### 1. Start with Strategy
Use `product-strategist` to set vision and OKRs before diving into tactics.

### 2. Research Before Building
Leverage `user-researcher` to validate assumptions before committing resources.

### 3. Document Decisions
Use `/pm:decision-log` to maintain context and rationale for key choices.

### 4. Balance Frameworks
Combine multiple frameworks (e.g., RICE + Value/Effort) for comprehensive prioritization.

### 5. Continuous Discovery
Make research a habit, not a phase. Talk to users weekly.

### 6. Measure What Matters
Define success metrics (via `/pm:kpi-dashboard`) before building.

### 7. Align Stakeholders Early
Use `stakeholder-manager` to build consensus and manage expectations.

---

## Tips & Tricks

### Combining Agents

Agents work together seamlessly:

```bash
# Strategic planning → Requirements → Execution
1. Tell product-strategist: "Create Q2 strategy"
2. Tell requirements-engineer: "Convert strategy into PRDs"
3. Tell agile-coach: "Plan sprints from these PRDs"
```

### Iterative Refinement

Commands produce drafts you can refine:

```bash
/pm:prd "Dark mode feature"
# Review output, then:
Tell requirements-engineer: "Add accessibility requirements to the PRD"
```

### Context Sharing

Feed outputs between tools:

```bash
/pm:persona "Power User"
# Then:
/pm:journey-map [paste persona] "Onboarding experience"
```

---

## Folder Structure

```
product-management/
├── agents/                    # 8 specialized AI agents
│   ├── product-strategist.md
│   ├── user-researcher.md
│   ├── requirements-engineer.md
│   ├── agile-coach.md
│   ├── feature-prioritizer.md
│   ├── gtm-planner.md
│   ├── growth-pm.md
│   └── stakeholder-manager.md
├── commands/                  # 15 focused tools
│   ├── prd-generator.md
│   ├── user-story-writer.md
│   ├── roadmap-builder.md
│   ├── okr-framework.md
│   ├── release-notes.md
│   ├── sprint-planner.md
│   ├── persona-creator.md
│   ├── journey-mapper.md
│   ├── interview-guide.md
│   ├── research-synthesizer.md
│   ├── kpi-dashboard.md
│   ├── experiment-designer.md
│   ├── stakeholder-mapper.md
│   ├── decision-logger.md
│   └── backlog-groomer.md
├── skills/                    # 5 knowledge frameworks
│   ├── prioritization-methods/
│   ├── agile-methodologies/
│   ├── user-research-techniques/
│   ├── metrics-frameworks/
│   └── go-to-market-playbooks/
└── README.md                  # This file
```

---

## Contributing

This is an open toolkit that grows with the PM community. Contributions welcome!

**Ideas for expansion:**
- Additional agents (data-scientist, competitive-analyst, technical-pm)
- More commands (pricing-strategy, competitive-analysis, technical-spec)
- New skills (jobs-to-be-done, product-market-fit, platform-strategy)
- Industry-specific playbooks (B2B SaaS, consumer, marketplace)

---

## Support & Feedback

- **Issues**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)
- **Workflows**: [Commands Repo](https://github.com/slgoodrich/commands)

---

## License

MIT License - Use freely, contribute back

---

## Acknowledgments

Inspired by modern PM practices from:
- Teresa Torres (Continuous Discovery)
- Marty Cagan (Empowered Teams)
- April Dunford (Positioning)
- Sean Ellis (Growth)
- Jeff Patton (Story Mapping)
- And the broader product community

Built with Claude Code's agent and plugin framework.

---

**Version**: 1.0.0
**Last Updated**: January 2025
**Maintainer**: [@slgoodrich](https://github.com/slgoodrich)
