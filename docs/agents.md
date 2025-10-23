# Agent Reference

## Overview

The Product Management Toolkit provides **18 specialized AI agents** that cover the entire product management lifecycle. Each agent is an expert in a specific PM discipline, using the Sonnet model (currently Claude Sonnet 4.5) for sophisticated strategic reasoning and comprehensive outputs.

---

## Quick Reference

| Agent | Specialty | Primary Use Cases |
|-------|-----------|-------------------|
| **product-strategist** | Strategy, vision, roadmaps, OKRs | Strategic planning, competitive positioning, long-term direction |
| **user-researcher** | User research, interviews, testing | Discovery, validation, understanding user needs |
| **requirements-engineer** | PRDs, specs, user stories | Translating vision into detailed requirements |
| **agile-coach** | Scrum, Kanban, agile methods | Sprint planning, backlog grooming, ceremonies |
| **feature-prioritizer** | RICE, ICE, Kano frameworks | Feature scoring, trade-off decisions, prioritization |
| **gtm-planner** | Go-to-market, launches, positioning | Launch planning, GTM strategy, messaging |
| **growth-pm** | Growth loops, acquisition, retention | Product-led growth, experiments, scaling |
| **stakeholder-manager** | Alignment, communication, collaboration | Managing expectations, building consensus |
| **technical-pm** | API specs, system design, architecture | Technical requirements, engineering collaboration |
| **data-scientist** | Analytics, experiments, statistics | A/B testing, metrics analysis, data-driven insights |
| **competitive-analyst** | Competitive intelligence, market research | Competitor tracking, market positioning |
| **customer-insights** | Feedback synthesis, sentiment analysis | Voice-of-customer, insight generation |
| **customer-success** | Onboarding, adoption, retention | Customer lifecycle, success strategies |
| **monetization-expert** | Pricing, packaging, revenue | Pricing decisions, monetization optimization |
| **api-product-manager** | API products, developer experience | API-first products, developer relations |
| **platform-architect** | Platform strategy, ecosystems | Multi-sided markets, platform planning |
| **discovery-facilitator** | Continuous discovery, opportunity mapping | Discovery practices, assumption testing |
| **product-ops** | Process optimization, tools, templates | PM efficiency, process improvement |

---

## Agents by Category

### Strategy & Planning (3 agents)

#### product-strategist
**Specialty**: Product strategy, vision, roadmaps, and OKRs
**Model**: Sonnet

**Use for:**
- Creating product vision and 3-5 year strategy
- Developing quarterly and annual OKRs
- Building strategic roadmaps (now/next/later)
- Competitive positioning and differentiation
- Market opportunity analysis
- Strategic decision-making (pivot, sunset, expand)
- Board and executive presentations

**Knowledge areas:**
- Strategic frameworks (Jobs-to-be-Done, North Star, Product-led growth)
- OKR methodology (Google, Doerr approach)
- Roadmap techniques (outcome-based, theme-based)
- Competitive intelligence
- Business model innovation

**Example use:**
```
Tell product-strategist:
"Help me create Q2 2025 OKRs for a B2B SaaS analytics platform
focused on product-market fit"
```

---

#### platform-architect
**Specialty**: Platform strategy, ecosystems, multi-sided markets, and API products
**Model**: Sonnet

**Use for:**
- Platform vs. product strategy decisions
- Ecosystem design and partner strategy
- Multi-sided marketplace strategy
- Developer platform strategy
- API-as-a-product positioning
- Network effects and platform economics
- Third-party integration strategy

**Knowledge areas:**
- Platform business models
- Aggregation theory
- Network effects
- Developer ecosystems
- API economics
- Marketplace dynamics

**Example use:**
```
Tell platform-architect:
"We want to open our platform to third-party developers.
Help design the ecosystem strategy and incentive model."
```

---

#### product-ops
**Specialty**: PM process optimization, tools, templates, and operations
**Model**: Sonnet

**Use for:**
- Optimizing PM processes and workflows
- PM team tooling and infrastructure
- Creating templates and playbooks
- Process documentation and standardization
- PM team onboarding
- Cross-team coordination
- PM metrics and productivity

**Knowledge areas:**
- PM tools (Jira, Linear, ProductBoard, Amplitude)
- Process frameworks
- Template libraries
- Knowledge management
- Team operations
- PM metrics

**Example use:**
```
Tell product-ops:
"Help me design an efficient PRD template and review process
for a 5-person PM team."
```

---

### Discovery & Research (4 agents)

#### user-researcher
**Specialty**: User research, interviews, usability testing, and research synthesis
**Model**: Sonnet

**Use for:**
- Planning user research studies
- Creating interview guides and screeners
- Conducting usability testing
- Synthesizing research findings
- Creating personas and journey maps
- Validating assumptions
- Identifying user needs and pain points

**Knowledge areas:**
- Research methodologies (interviews, surveys, usability testing)
- Teresa Torres continuous discovery
- Jobs-to-be-Done framework
- User journey mapping
- Persona development
- Research synthesis techniques

**Example use:**
```
Tell user-researcher:
"Design a research study to understand why 30% of users
churn after the first month."
```

---

#### discovery-facilitator
**Specialty**: Continuous discovery, opportunity mapping, and assumption testing
**Model**: Sonnet

**Use for:**
- Running continuous discovery practices
- Opportunity solution trees
- Assumption mapping and testing
- Experiment design for validation
- Outcome-driven development
- Building discovery habits
- Identifying riskiest assumptions

**Knowledge areas:**
- Teresa Torres continuous discovery framework
- Opportunity solution trees
- Assumption testing
- Experiment design
- Outcome mapping
- Discovery habits

**Example use:**
```
Tell discovery-facilitator:
"Help me build an opportunity solution tree for improving
user activation in the first week."
```

---

#### customer-insights
**Specialty**: Customer feedback synthesis, sentiment analysis, and voice-of-customer programs
**Model**: Sonnet

**Use for:**
- Analyzing customer feedback at scale
- Sentiment analysis and theme extraction
- Voice-of-customer program design
- NPS analysis and action planning
- Support ticket analysis
- Feature request consolidation
- Customer interview synthesis

**Knowledge areas:**
- Feedback analysis techniques
- Sentiment analysis
- Thematic synthesis
- NPS methodology
- Voice-of-customer programs
- Insight generation

**Example use:**
```
Tell customer-insights:
"Analyze these 500 support tickets and customer interviews
to identify top pain points and opportunities."
```

---

#### competitive-analyst
**Specialty**: Competitive intelligence, market research, and industry analysis
**Model**: Sonnet

**Use for:**
- Competitive landscape analysis
- Competitor feature comparison
- Market trend identification
- Positioning and differentiation
- Competitor strategy assessment
- Win/loss analysis
- Market opportunity sizing

**Knowledge areas:**
- Competitive analysis frameworks
- Porter's Five Forces
- SWOT analysis
- Market research techniques
- Industry analysis
- Positioning strategy

**Example use:**
```
Tell competitive-analyst:
"Analyze how we should position our project management tool
against Asana, Monday, and Linear."
```

---

### Delivery & Execution (4 agents)

#### requirements-engineer
**Specialty**: PRDs, technical specs, user stories, and acceptance criteria
**Model**: Sonnet

**Use for:**
- Writing comprehensive PRDs
- Creating detailed technical specifications
- Breaking features into user stories
- Defining acceptance criteria
- Documenting edge cases
- Requirements traceability
- Specification templates

**Knowledge areas:**
- PRD structure and best practices
- User story mapping (Jeff Patton)
- Acceptance criteria (Given/When/Then)
- BDD (Behavior-Driven Development)
- Requirements documentation
- Specification by example

**Example use:**
```
Tell requirements-engineer:
"Write a comprehensive PRD for a multi-factor authentication
feature, including edge cases and acceptance criteria."
```

---

#### technical-pm
**Specialty**: API specs, system design, architecture decisions, and technical feasibility
**Model**: Sonnet

**Use for:**
- API specification and design
- System architecture decisions
- Technical feasibility assessment
- Data model design
- Performance and scalability requirements
- Security and compliance specifications
- Integration architecture
- Technical debt management

**Knowledge areas:**
- REST, GraphQL, gRPC API design
- System architecture patterns
- Database design (SQL, NoSQL)
- Performance optimization
- Security best practices
- Infrastructure and DevOps
- Technical documentation

**Example use:**
```
Tell technical-pm:
"Design a REST API for our custom reports feature,
including endpoints, data model, and performance considerations."
```

---

#### agile-coach
**Specialty**: Scrum, Kanban, and agile methodologies
**Model**: Sonnet

**Use for:**
- Sprint planning and estimation
- Backlog grooming and refinement
- Agile ceremony facilitation
- Velocity tracking and capacity planning
- Story mapping workshops
- Agile process optimization
- Team retrospectives

**Knowledge areas:**
- Scrum framework
- Kanban principles
- SAFe (Scaled Agile)
- Shape Up (Basecamp)
- Dual-track agile
- Agile ceremonies
- Estimation techniques

**Example use:**
```
Tell agile-coach:
"Help me plan Sprint 47 for my 5-person team with velocity
of 32 points. Bob is out 2 days and we need to ship auth."
```

---

#### feature-prioritizer
**Specialty**: Prioritization frameworks (RICE, ICE, Kano, Value vs Effort)
**Model**: Sonnet

**Use for:**
- Scoring features with RICE/ICE/Kano
- Making trade-off decisions
- Roadmap prioritization
- Backlog ranking
- Opportunity cost analysis
- Resource allocation
- Priority scoring systems

**Knowledge areas:**
- RICE (Reach, Impact, Confidence, Effort) - Intercom
- ICE (Impact, Confidence, Ease) - Sean Ellis
- Kano model
- Value vs Effort matrix
- MoSCoW prioritization
- Cost of delay
- Opportunity scoring

**Example use:**
```
Tell feature-prioritizer:
"Score these 10 features using RICE and recommend
the top 3 for our Q2 roadmap."
```

---

### Growth & Optimization (3 agents)

#### growth-pm
**Specialty**: Growth strategy, acquisition, activation, retention, and product-led growth
**Model**: Sonnet

**Use for:**
- Growth loop design
- Acquisition funnel optimization
- Activation and onboarding improvement
- Retention and engagement strategies
- Viral mechanics and referral programs
- Product-led growth strategies
- Growth experiment design

**Knowledge areas:**
- AARRR framework (Acquisition, Activation, Retention, Revenue, Referral)
- Growth loops
- Product-led growth (PLG)
- Viral mechanics
- Retention strategies
- Onboarding optimization
- Growth experiments

**Example use:**
```
Tell growth-pm:
"We have 50% drop-off at onboarding. Help me design
experiments to improve activation."
```

---

#### data-scientist
**Specialty**: Analytics, experiments, statistical analysis, and data-driven decision making
**Model**: Sonnet

**Use for:**
- A/B test design and analysis
- Metrics definition and tracking
- Statistical significance testing
- Cohort analysis
- Funnel analysis
- Predictive modeling
- Data visualization

**Knowledge areas:**
- Statistical analysis
- A/B testing methodology
- Metrics frameworks (HEART, North Star)
- SQL and data analysis
- Cohort retention analysis
- Statistical significance
- Experiment design

**Example use:**
```
Tell data-scientist:
"Design an A/B test to measure the impact of social proof
on signup conversion. How should I calculate significance?"
```

---

#### monetization-expert
**Specialty**: Pricing, packaging, revenue optimization, and billing strategies
**Model**: Sonnet

**Use for:**
- Pricing strategy and optimization
- Packaging and tiering design
- Freemium model design
- Usage-based pricing
- Enterprise pricing
- Billing and payment flows
- Revenue model innovation

**Knowledge areas:**
- Pricing psychology
- Value-based pricing
- Freemium strategies
- SaaS pricing models
- Usage-based pricing
- Pricing experiments
- Willingness-to-pay analysis

**Example use:**
```
Tell monetization-expert:
"Help me design a pricing strategy for our analytics platform.
Should we go usage-based or tiered subscription?"
```

---

### Go-to-Market & Collaboration (4 agents)

#### gtm-planner
**Specialty**: Go-to-market strategy, product launches, positioning, and messaging
**Model**: Sonnet

**Use for:**
- GTM strategy development
- Product launch planning
- Market positioning
- Messaging and value propositions
- Launch timeline and execution
- Sales enablement
- Launch metrics and success criteria

**Knowledge areas:**
- GTM frameworks
- Positioning (April Dunford)
- Product marketing
- Launch strategies
- Sales enablement
- Channel strategy
- Launch checklists

**Example use:**
```
Tell gtm-planner:
"Plan a product launch for our new API product targeting
developers. Include positioning, channels, and timeline."
```

---

#### stakeholder-manager
**Specialty**: Stakeholder alignment, communication, and cross-functional collaboration
**Model**: Sonnet

**Use for:**
- Stakeholder mapping and analysis
- Building alignment and consensus
- Executive communication
- Cross-functional collaboration
- Managing conflicting priorities
- Decision-making frameworks
- Influence without authority

**Knowledge areas:**
- Stakeholder analysis
- Communication frameworks
- Influence strategies
- Conflict resolution
- Executive communication
- Decision-making processes
- Change management

**Example use:**
```
Tell stakeholder-manager:
"Help me build alignment between Engineering (wants technical
debt) and Sales (wants features) for Q2 planning."
```

---

#### api-product-manager
**Specialty**: API products, developer experience, API documentation, and API monetization
**Model**: Sonnet

**Use for:**
- API product strategy
- Developer experience optimization
- API documentation and portals
- SDK design and distribution
- API monetization
- Developer community building
- API versioning and deprecation

**Knowledge areas:**
- API product management
- Developer experience (DX)
- API documentation
- SDK design
- Developer portals
- API monetization
- Developer relations

**Example use:**
```
Tell api-product-manager:
"Design a developer experience strategy for our new public API,
including docs, SDKs, and onboarding."
```

---

#### customer-success
**Specialty**: Customer onboarding, adoption, retention, and expansion
**Model**: Sonnet

**Use for:**
- Customer onboarding design
- Adoption and engagement strategies
- Churn reduction
- Expansion and upsell
- Customer health scoring
- Success playbooks
- Customer lifecycle management

**Knowledge areas:**
- Customer success frameworks
- Onboarding best practices
- Customer health metrics
- Churn analysis
- Expansion strategies
- Success playbooks
- Lifecycle management

**Example use:**
```
Tell customer-success:
"Design an onboarding program to get new customers to
value in their first week and reduce 30-day churn."
```

---

## Model Configuration

All agents use **Claude Sonnet 4.5** for:
- Complex strategic reasoning
- Nuanced stakeholder communication
- Deep contextual understanding
- Comprehensive framework application

This ensures consistent high-quality outputs across all PM disciplines.

---

## Agent Invocation

### Natural Language
Tell agents directly what you need:

```
Tell product-strategist: "Create Q2 2025 OKRs"
Tell user-researcher: "Design a research study for churn"
Tell requirements-engineer: "Write a PRD for dark mode"
```

Claude Code will automatically route to the appropriate agent.

### Direct Agent Selection
When you know which agent you need:

```
I need product-strategist to help with quarterly planning
Can feature-prioritizer score these 10 features?
Get gtm-planner to create a launch plan
```

---

## Multi-Agent Workflows

Agents are designed to work together for complex tasks.

### Example 1: Feature Development
```
1. user-researcher       → Validate customer need
2. product-strategist    → Align with strategy
3. requirements-engineer → Write comprehensive PRD
4. technical-pm          → Define technical approach
5. feature-prioritizer   → Prioritize against backlog
6. agile-coach           → Plan sprint execution
7. gtm-planner           → Prepare launch
8. customer-success      → Design onboarding
```

### Example 2: Quarterly Planning
```
1. data-scientist        → Analyze Q4 metrics
2. competitive-analyst   → Market landscape review
3. product-strategist    → Draft Q1 strategy and OKRs
4. stakeholder-manager   → Align with stakeholders
5. agile-coach           → Plan sprint capacity
6. feature-prioritizer   → Score and rank backlog
```

### Example 3: Growth Initiative
```
1. data-scientist        → Analyze activation funnel
2. user-researcher       → Interview churned users
3. growth-pm             → Design growth experiments
4. requirements-engineer → Spec improvements
5. data-scientist        → Design A/B tests
6. growth-pm             → Monitor and iterate
```

---

## Agent Integration Patterns

### Sequential Workflows
Agents pass work to the next expert in the chain.

**Pattern**: A → B → C
**Example**: Strategy → Specs → Execution

### Parallel Workflows
Multiple agents work simultaneously on different aspects.

**Pattern**: A + B + C → Synthesis
**Example**: Research + Competitive + Analytics → Strategy

### Iterative Workflows
Agents refine each other's work through multiple passes.

**Pattern**: A → B → A → B
**Example**: Draft PRD → Technical Review → Refine PRD → Final Review

---

## Choosing the Right Agent

### By PM Activity

**Strategic Planning** → product-strategist, platform-architect
**User Research** → user-researcher, discovery-facilitator, customer-insights
**Requirements** → requirements-engineer, technical-pm
**Prioritization** → feature-prioritizer, product-strategist
**Execution** → agile-coach, requirements-engineer
**Growth** → growth-pm, data-scientist, monetization-expert
**Launch** → gtm-planner, stakeholder-manager
**Analysis** → data-scientist, competitive-analyst
**Customer Lifecycle** → customer-success, customer-insights

### By Output Type

**PRD / Specs** → requirements-engineer
**OKRs / Roadmap** → product-strategist
**Research Plan** → user-researcher
**Sprint Plan** → agile-coach
**Prioritized Backlog** → feature-prioritizer
**Launch Plan** → gtm-planner
**Experiment Design** → data-scientist, growth-pm
**API Specification** → technical-pm, api-product-manager
**Positioning** → gtm-planner, competitive-analyst

### By Question Type

**"Should we build this?"** → product-strategist, user-researcher, feature-prioritizer
**"How should we build this?"** → requirements-engineer, technical-pm
**"When should we build this?"** → feature-prioritizer, agile-coach
**"Who should build this?"** → agile-coach, stakeholder-manager
**"How do we launch this?"** → gtm-planner, product-ops
**"Is it working?"** → data-scientist, customer-insights

---

## Agent Capabilities Summary

### All Agents Provide:
- Expert knowledge in their domain
- Best practice frameworks and methodologies
- Template outputs and examples
- Integration guidance with other agents
- "When to use" recommendations

### Common Agent Skills:
- Strategic thinking and systems thinking
- Data-informed decision making
- Clear communication and documentation
- Stakeholder-appropriate outputs
- Real-world examples and case studies

---

## Future Agent Additions

### Planned Agents (v1.1+)
- **ux-designer**: UX patterns, wireframes, design systems
- **technical-writer**: User docs, help centers, release notes
- **product-marketing**: Marketing strategy, campaigns, positioning
- **business-analyst**: Financial modeling, business cases, ROI
- **compliance-manager**: GDPR, HIPAA, SOC 2 compliance
- **ai-product-manager**: AI/ML product strategy
- **data-product-manager**: Data products and analytics

---

## Contributing New Agents

When proposing a new agent:

1. **Clear Specialty**: What unique expertise does it provide?
2. **Distinct from Existing**: How is it different from current agents?
3. **Real PM Need**: What common PM task does it solve?
4. **Integration**: How does it work with other agents?
5. **Knowledge Base**: What frameworks/methodologies does it use?

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

## Questions & Support

- **Documentation**: Each agent has inline documentation
- **Examples**: See `usage.md` for workflow examples
- **Issues**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)

---

**Total Agents**: 18
**Model**: Claude Sonnet 4.5 (all agents)
**Version**: 1.0.0
**Last Updated**: January 2025
