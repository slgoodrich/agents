# AI PM Copilot for Claude Code

> Answer product management's hardest questions in minutes, not days

**Expert product management guidance powered by frameworks from Teresa Torres, Marty Cagan, April Dunford, and more - without hiring a product manager.**

Right feature. Right users. Right time. Right reasons.

Not a project management tool. Not a generic AI assistant. A specialized copilot that combines:

- **Speed of AI** (answers in minutes)
- **Depth of product management frameworks** (Teresa Torres, Marty Cagan, April Dunford)
- **Context-aware reasoning** (remembers your product, personalizes outputs)

Built for solo developers and small teams who need enterprise product management capabilities without the complexity.

## Why AI PM Copilot?

**You're a solo founder building your first product.** You can code, but product management decisions feel like guesswork:

- "Should I build feature X or Y first?"
- "How do I validate this idea without wasting weeks?"
- "Which users should I target?"
- "When is the right time to launch?"

**Generic AI** (ChatGPT, Claude): Fast answers, but no product management frameworks or strategic depth
**Enterprise PM tools** (Jira, Aha!): Deep features, but slow, complex, and expensive
**Manual PM work** (Notion, templates): Flexible, but requires expertise you don't have

**AI PM Copilot:** Expert product management frameworks + AI speed = rigorous answers delivered in minutes.

Built on 16 proven methodologies from product management thought leaders. Context-aware intelligence that remembers your product. Developer-native experience inside Claude Code.

## Built on Proven Product Management Frameworks

AI PM Copilot isn't generic AI advice - it's built on expert frameworks from product management thought leaders:

**Research & Discovery:** Teresa Torres (Continuous Discovery), Erika Hall (Just Enough Research)  
**Strategy & Goals:** Marty Cagan (Empowered), Sean Ellis (Product-Market Fit), April Dunford (Positioning)  
**Execution & Planning:** Jeff Patton (Story Mapping), Basecamp (Shape Up), Google (HEART/Goals)  
**Prioritization:** Intercom (RICE), Dan Olsen (Lean Product Playbook)

16 proven methodologies. 100+ templates and frameworks. Expert rigor at AI speed.

## How It Works

**Just talk to Claude Code like you would a consultant:**

```
You: "I'm building a SaaS analytics tool. Should I prioritize dashboards or API access first?"

→ product-manager routes to feature-prioritizer
→ Reads your product context from setup
→ Returns scored recommendations with rationale

Result: Expert RICE scoring in 2 minutes with explanation of why each feature ranks where it does.
```

**Try it yourself:**

1. Install: `/plugin install ai-pm-copilot`
2. Setup (optional, 5-10 min): `/ai-pm-copilot:pm-setup`
3. Ask: "Should I prioritize feature X or Y?"

## What's Included

**8 Expert Product Management Agents** - Available 24/7 for research, strategy, execution, and launch (1 orchestrator + 7 specialists)

**1 Utility Agent** - Automated codebase context discovery (context-scanner)

**3 Multi-Agent Team Presets** - Validation sprints, PRD stress tests, competitive war rooms

**16 Proven Frameworks** - RICE, JTBD, Lean Startup, Story Mapping, and more

**100+ Templates & Assets** - PRD templates, roadmap frameworks, interview guides

**Context-Aware Intelligence** - One-time setup, personalized outputs across all agents

Built on frameworks from Teresa Torres, Marty Cagan, April Dunford, Sean Ellis, Jeff Patton, and more.

## Get Started (5 Minutes to Your First Expert Answer)

### 1. Install the Plugin

```bash
/plugin marketplace add https://github.com/slgoodrich/agents
/plugin install ai-pm-copilot
```

### 2. (Optional) Set Up Product Context

Spend 5-10 minutes setting up context once, save 80% of questions across all future interactions:

```bash
/ai-pm-copilot:pm-setup
```

### 3. Ask Your First Product Management Question

```
"Should I prioritize feature X or Y?"
"Design a user interview study for churn"
"Score these 5 features with RICE"
```

**Get expert product management guidance in minutes, not days.** No signup. No API keys. Just install and ask.

## Use Cases

### Daily Product Management Work

**Feature validation:**

```
"I want to add real-time collaboration. Is this worth building?"
→ Coordinates research-ops for validation, feature-prioritizer for scoring
```

**Planning:**

```
"Plan next quarter focused on retention"
```

**Documentation:**

```
"Write a PRD for SSO integration"
```

### Strategic Planning

**Quarterly Goals:**

```
"Create Q2 goals for a pre-PMF SaaS product"
```

**Market analysis:**

```
"Research the competitive landscape for project management tools"
```

**Roadmap:**

```
"Build a now-next-later roadmap for next 6 months"
```

### Research & Discovery

**User research:**

```
"Design a study to understand user onboarding pain points"
```

**Validation:**

```
"Help me validate this feature hypothesis with 10 user interviews"
```

**Synthesis:**

```
"Analyze these interview transcripts and identify top 3 insights"
```

### Launch Planning

**Go-to-market:**

```
"Create a beta launch plan for our API product"
```

**Positioning:**

```
"Develop positioning for a new pricing tier"
```

## Agent Teams (Experimental)

Multi-agent team presets for high-stakes product decisions. Multiple agents work in parallel, challenge each other's conclusions, and synthesize competing perspectives.

Requires Claude Code's experimental Agent Teams feature: `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`

### Validation Sprint

```
/agent-teams:validation-sprint "AI-powered code review tool for solo developers"
```

Three agents investigate in parallel (idea-researcher, market-researcher, idea-skeptic), cross-examine each other's findings, and deliver a BUILD / DON'T BUILD / NEEDS MORE EVIDENCE verdict.

### PRD Stress Test

```
/agent-teams:prd-stress-test path/to/prd.md
```

Three reviewers (market-fit, feasibility, scope) score your PRD independently, flag conflicts between their reviews, and deliver a READY TO BUILD / NEEDS REVISION / MAJOR REWORK verdict.

### Competitive War Room

```
/agent-teams:competitive-war-room "Notion, Coda, Slite"
```

One researcher per competitor runs a deep-dive in parallel. Results are synthesized into a positioning map, battle cards, and strategic recommendations.

## Agents

The toolkit provides 1 orchestration agent, 7 specialist agents, and 1 utility agent that work together to cover the complete product lifecycle:

### 1. product-manager (Main Router)

**Your primary entry point** - Intelligent agent that routes requests to specialized experts

**Use for:**

- General product management questions and guidance
- Multi-faceted problems requiring multiple perspectives
- When unsure which specialist to consult

**Example:**

```
"I need to validate a feature idea, prioritize it, and plan delivery"
→ Routes to research-ops, feature-prioritizer, and requirements-engineer
```

### 2. market-analyst

**Market research, competitive analysis, and positioning**

**Use for:**

- Competitive landscape analysis
- Market sizing and opportunity assessment
- Product positioning and differentiation
- TAM/SAM/SOM calculations
- Win/loss analysis

**Example:**

```
"Analyze our position against competitors in the project management space"
"Research competitive landscape for project management tools"
```

### 3. research-ops

**User research, interviews, and validation**

**Use for:**

- User interview planning and synthesis
- Usability testing
- Problem/solution validation
- Customer feedback analysis
- Research program design

**Example:**

```
"Design a study to understand why 30% of users churn after first month"
"Synthesize these interview transcripts into themes and insights"
```

### 4. product-strategist

**Vision, strategy, and goals**

**Use for:**

- Product vision and strategy
- Quarterly and annual goals
- Strategic roadmaps
- North Star metric definition
- Strategic trade-offs

**Example:**

```
"Create Q2 goals focused on reaching product-market fit"
```

### 5. roadmap-builder

**Roadmap planning and sequencing**

**Use for:**

- Now-Next-Later roadmaps
- Theme-based roadmaps
- Quarterly planning
- Feature sequencing and phasing
- Milestone planning

**Example:**

```
"Build a 6-month roadmap for our mobile app launch"
```

### 6. feature-prioritizer

**RICE, ICE, and prioritization frameworks**

**Use for:**

- RICE/ICE scoring
- Kano model analysis
- Value vs Effort matrices
- Trade-off decisions
- Backlog ranking

**Example:**

```
"Score these 10 features using RICE framework"
```

### 7. requirements-engineer

**PRDs, specs, and user stories**

**Use for:**

- Product requirements documents (PRDs)
- Technical specifications
- User story writing
- Acceptance criteria
- Feature documentation

**Example:**

```
"Write a comprehensive PRD for dark mode feature"
```

### 8. launch-planner

**Go-to-market and launch execution**

**Use for:**

- Launch planning and execution
- GTM strategy and distribution channel selection
- Beta programs
- Launch messaging and positioning
- Community launches (Product Hunt, Hacker News, Reddit)

**Example:**

```
"Create a launch plan for our new API product"
```

### 9. context-scanner (Utility Agent)

**Automated strategic context discovery from codebase**

**Use for:**

- Auto-discovering features, tech stack, and integrations during setup
- Refreshing stale context when product changes
- Getting accurate baseline for competitive analysis
- Fast onboarding on existing projects

**What it discovers:**

- Features (from routes, pages, API endpoints)
- Tech stack (from package.json, requirements.txt, etc.)
- Integrations (from 3rd party packages)
- Project scale (files, LOC, complexity)

**What it doesn't do:**

- Code quality or architecture analysis
- Performance or security assessment
- Engineering recommendations

**Note:** This is a utility agent (not a PM specialist) that uses Haiku model for efficient file operations. It's automatically invoked by pm-setup when you have an existing codebase, or can be invoked by PM agents when they need current product state.

**Example (automatic invocation):**

```
/ai-pm-copilot:pm-setup
→ Detects codebase
→ "Scan codebase to auto-discover context? (yes/no)"
→ If yes: context-scanner runs, presents findings for validation
→ Time saved: 10-15 minutes vs manual entry
```

## Agent Routing Pattern

The **product-manager** agent acts as an intelligent router that:

1. Analyzes your request to understand the product management discipline(s) needed
2. Routes to the appropriate specialist agent(s)
3. Coordinates multi-agent workflows when needed
4. Synthesizes outputs from multiple specialists

**Simple routing:**

```
"Help me prioritize features"
→ product-manager routes to feature-prioritizer
```

**Multi-agent workflow:**

```
"Validate this feature idea and create a launch plan"
→ product-manager routes to research-ops (validation)
→ Then to launch-planner (GTM strategy)
→ Synthesizes complete plan
```

**Direct to specialist:** If your question clearly fits one domain, Claude Code may route directly to the specialist without going through product-manager first.

## Skills

Skills are knowledge frameworks that agents load progressively when needed, organized by the product development journey:

### Stage 1: Validation (Before writing code)

Is this idea worth my time? Who are my competitors?

- **competitive-analysis-templates** - SWOT, Porter's Five Forces, competitive positioning
- **market-sizing-frameworks** - TAM/SAM/SOM, market validation
- **product-positioning** - April Dunford framework, differentiation strategy

### Stage 2: Understanding (Who am I building for?)

Who are my users? What problems am I solving?

- **user-research-techniques** - Interviews, surveys, usability testing, JTBD
- **interview-frameworks** - Interview design, questioning, synthesis
- **synthesis-frameworks** - Affinity mapping, insight generation
- **usability-frameworks** - Usability testing, Nielsen principles
- **validation-frameworks** - Problem/solution validation, MVP testing

### Stage 3: Scoping (What's the MVP?)

What features do I build? How do I avoid scope creep?

- **prioritization-methods** - RICE, ICE, Kano, Value vs Effort
- **product-market-fit** - PMF indicators, Sean Ellis test, MVP scoping

### Stage 4: Speccing (Make Claude Code build it well)

Clear requirements, user stories, acceptance criteria

- **specification-techniques** - Requirements writing, clarity
- **prd-templates** - PRD formats and best practices
- **user-story-templates** - User story formats, INVEST criteria

### Stage 5: Planning (What's my roadmap?)

Phase 1, 2, 3 and milestone planning

- **roadmap-frameworks** - Now-Next-Later, outcome-based roadmaps

### Stage 6: Launch (How do I get users?)

Where do I launch? What's my messaging?

- **go-to-market-playbooks** - GTM strategies, distribution channels
- **launch-planning-frameworks** - Launch tiers, timelines, execution

## Setup Command

### /ai-pm-copilot:pm-setup

**One-time context setup that makes everything better.**

Creates 8 core context files that all agents reference:

```
.claude/product-context/
  ├── product-info.md          # Product description, users, value prop
  ├── business-metrics.md      # ARR, users, growth, retention
  ├── strategic-goals.md       # Goals, priorities, themes
  ├── current-roadmap.md       # Now-Next-Later roadmap
  ├── tech-stack.md           # Architecture, tech, constraints
  ├── customer-segments.md     # Personas, segments, ICP
  ├── team-info.md            # Team size, roles, constraints
  └── competitive-landscape.md # Competitors, positioning
```

**Benefits:**

- Agents ask 80% fewer questions
- Outputs are product-specific, not generic
- Context reused across all agents and skills

**Usage:**

```bash
# First-time setup
/ai-pm-copilot:pm-setup

# Update context later
/ai-pm-copilot:pm-setup --update
```

## Architecture

### Agent-First Design

- **Two plugins** - core PM toolkit (ai-pm-copilot) + multi-agent team presets (agent-teams)
- **Main orchestration agent + 7 specialist agents + 6 team agents** with clear responsibilities
- **Intelligent routing** through main product-manager agent
- **Progressive skills** that load on-demand
- **Solo developer focus** - no enterprise complexity

### Agent-First Benefits

- Natural conversation instead of memorizing commands
- Agents collaborate automatically
- Context flows between specialists
- Simpler mental model
- Install what you need: core plugin or full suite

### Model Strategy

- Expert-level strategic reasoning
- Nuanced decision-making
- Context-aware responses
- High-quality outputs

## Creating PRDs

Use **requirements-engineer** to create Product Requirements Documents with automatic template selection:

```
"Write a PRD for [your feature]"
```

**Intelligent Template Selection:**
requirements-engineer uses complexity assessment to automatically select the right template:

**How it works:**

1. Assesses 3 dimensions: Technical Complexity, Risk/Impact, Scope Breadth (0-10 each)
2. Reads repository context (`.claude/product-context/tech-stack.md`, etc.) for informed scoring
3. Applies decision thresholds based on average complexity score
4. Communicates reasoning transparently with complexity breakdown

**Templates:**

- **Lean PRD** (1-2 pages): Low complexity (avg < 4), < 1 week, simple features
- **Comprehensive PRD** (3-5 pages): Moderate complexity (avg 4-7), standard features [DEFAULT]
- **Amazon PR/FAQ** (3-6 pages): New products (detected by keywords)
- **Google PRD** (5-10 pages): High risk (security/payments) or scale-critical (high complexity)

**Example reasoning:** "OAuth authentication" → Google PRD (Risk: 9/10 security-critical, triggers high-detail template)

You can always request a different template if the automatic selection doesn't fit your needs.

**Storage:**
PRDs are automatically saved to `prds/[feature-name].md` using kebab-case naming:

- `prds/dark-mode.md`
- `prds/csv-export.md`
- `prds/user-notifications.md`

## Target Audience

Built for **solo developers and small teams** who need:

- Enterprise product management capabilities without complexity
- Conversational interface, not command memorization
- Intelligent routing to the right expertise
- Progressive learning and guidance

**Perfect for:**

- Solo founders building their first product
- Small teams without a dedicated product manager
- Developers transitioning to product roles
- Side projects and indie hackers

**Not designed for:**

- Enterprise organizations with product management teams
- Complex stakeholder management scenarios
- Large-scale portfolio management
- Multiple product lines with dependencies

## Documentation

- **[Architecture](docs/architecture.md)** - Agent-first design and system overview
- **[Agents](docs/agents.md)** - Complete agent reference and capabilities
- **[Skills](docs/agent-skills.md)** - Framework knowledge and progressive disclosure
- **[Usage](docs/usage.md)** - Patterns, workflows, and best practices
- **[Plugins](docs/plugins.md)** - Plugin structure and organization

## Inspired By

This plugin was inspired by [wshobson/agents](https://github.com/wshobson/agents). If, like me, you're not a software developer by trade, I highly recommend checking out that repository to get better results from Claude Code.

## Contributing

Contributions welcome! This toolkit grows with the community.

**Ways to contribute:**

- Report bugs or issues
- Suggest new features or improvements
- Share usage examples and workflows
- Improve documentation
- Add new skills or assets

See [CONTRIBUTING.md](.github/CONTRIBUTING.md) for detailed guidelines.

## Requirements

- Claude Code
- Basic familiarity with product management concepts

## Support

- **Documentation** - See [docs/](docs/) directory
- **Issues** - [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions** - [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)

## License

This project is licensed under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/). See [LICENSE](LICENSE) for details.

---

_Empowering solo developers and small teams with enterprise product management capabilities through conversational AI agents._
