# Agent Skills Reference

## Overview

**Skills** are specialized knowledge frameworks that extend agent capabilities in specific product management domains. They provide deep expertise in methodologies, frameworks, and best practices without loading everything into context upfront.

Skills use **progressive disclosure**: they activate only when needed, keeping interactions token-efficient while providing comprehensive PM knowledge when required.

---

## How Skills Work

### Activation Mechanism

Skills activate automatically based on request patterns:

```
User: "Prioritize these features using RICE"
↓
feature-prioritizer agent activates
↓
Detects "RICE" keyword → Loads prioritization-frameworks skill
↓
Applies RICE methodology from skill knowledge
↓
Returns scored features with detailed rationale
```

### Three-Tier Architecture

**1. Metadata** (Always loaded)
- Skill name and category
- Activation triggers
- When to use guidance

**2. Instructions** (Loaded on activation)
- Step-by-step methodology
- Framework application
- Decision criteria

**3. Resources** (Referenced as needed)
- Detailed examples
- Case studies
- Templates and tools

### Benefits

**Token Efficiency**
- Load only what's needed when needed
- Agents stay lightweight
- More room for user context

**Specialized Expertise**
- Deep framework knowledge
- Consistent methodology application
- Updated best practices

**Composability**
- Multiple agents can use same skill
- Skills combine for complex scenarios
- Clear knowledge boundaries

**Maintainability**
- Update framework knowledge without changing agents
- Add new skills without modifying existing agents
- Version skill knowledge independently

---

## Available Skills (25 Total)

### Prioritization Methods  Available

**Category**: Prioritization
**Agents**: feature-prioritizer, product-strategist

**Included Frameworks:**
1. **RICE** (Reach, Impact, Confidence, Effort) - Intercom
2. **ICE** (Impact, Confidence, Ease) - Sean Ellis
3. **Kano Model** (Basic, Performance, Delight)
4. **Value vs Effort Matrix**
5. **MoSCoW** (Must, Should, Could, Won't)
6. **Cost of Delay / CD3** (Cost of Delay Divided by Duration)
7. **Opportunity Scoring** (Opportunity vs. Satisfaction)

**Activation Triggers:**
- "prioritize using RICE"
- "score with ICE"
- "apply Kano model"
- "value vs effort analysis"

**Example Usage:**
```
Tell feature-prioritizer: "Score these 10 features using RICE.
Explain each score and rank them."

→ Loads prioritization-frameworks skill
→ Applies RICE: Reach × Impact × Confidence / Effort
→ Returns scored backlog with detailed breakdown
```

---

### Agile Methodologies  Available

**Category**: Agile
**Agents**: agile-coach, product-ops

**Included Methodologies:**
1. **Scrum** (Sprints, ceremonies, artifacts)
2. **Kanban** (Flow, WIP limits, continuous delivery)
3. **SAFe** (Scaled Agile Framework)
4. **Shape Up** (Basecamp's 6-week cycles)
5. **Dual-Track Agile** (Discovery + Delivery)
6. **Scrumban** (Hybrid approach)

**Activation Triggers:**
- "plan sprint" / "sprint planning"
- "setup Kanban board"
- "Shape Up cycle"
- "dual-track agile"

**Example Usage:**
```
Tell agile-coach: "Set up Kanban board for our team.
What WIP limits should we use?"

→ Loads agile-methodologies skill
→ Applies Kanban principles
→ Recommends WIP limits based on team size
→ Provides board structure and workflow
```

---

### User Research Techniques  Available

**Category**: Research
**Agents**: user-researcher, discovery-facilitator, customer-insights

**Included Techniques:**
1. **User Interviews** (Structured, semi-structured, unstructured)
2. **Usability Testing** (Moderated, unmoderated, remote)
3. **Surveys** (Design, distribution, analysis)
4. **Jobs-to-be-Done** (Interview framework)
5. **Diary Studies** (Longitudinal research)
6. **Card Sorting** (Information architecture)
7. **A/B Testing** (Hypothesis, design, analysis)
8. **Research Synthesis** (Affinity mapping, theme extraction)

**Activation Triggers:**
- "design user interview"
- "usability test"
- "JTBD interview"
- "synthesize research"

**Example Usage:**
```
Tell user-researcher: "Design a Jobs-to-be-Done interview
guide to understand why customers switch from competitors"

→ Loads user-research-techniques skill
→ References JTBD methodology
→ Creates interview guide with:
  - Hiring moment questions
  - Forces of progress questions
  - Timeline reconstruction
  - Anxiety and habit probes
```

---

### Metrics Frameworks  Available

**Category**: Metrics & Analytics
**Agents**: data-scientist, growth-pm, product-strategist

**Included Frameworks:**
1. **AARRR** (Pirate Metrics: Acquisition, Activation, Retention, Revenue, Referral)
2. **HEART** (Happiness, Engagement, Adoption, Retention, Task Success)
3. **North Star Metric** (One metric that matters)
4. **OKRs** (Objectives and Key Results)
5. **Product-Market Fit Score** (Sean Ellis Test)
6. **Cohort Analysis** (Retention, LTV)
7. **Funnel Analysis** (Conversion optimization)

**Activation Triggers:**
- "AARRR metrics"
- "apply HEART framework"
- "define north star metric"
- "cohort analysis"

**Example Usage:**
```
Tell data-scientist: "Apply HEART framework to our product.
What metrics should we track for each dimension?"

→ Loads metrics-frameworks skill
→ Applies HEART:
  - Happiness: NPS, satisfaction
  - Engagement: DAU/MAU, session length
  - Adoption: Feature adoption rate
  - Retention: 7-day, 30-day retention
  - Task Success: Completion rate, error rate
→ Recommends specific metrics for your product
```

---

### Go-to-Market Playbooks  Available

**Category**: Go-to-Market
**Agents**: gtm-planner, product-strategist, stakeholder-manager

**Included Playbooks:**
1. **Product-Led Growth (PLG)** (Self-serve, freemium, viral loops)
2. **Sales-Led Growth** (Demos, pilots, enterprise sales)
3. **Positioning** (April Dunford framework)
4. **Product Launch** (Internal preview, beta, GA)
5. **Market Entry** (Beachhead strategy, crossing the chasm)
6. **Channel Strategy** (Direct, partner, marketplace)
7. **Sales Enablement** (Deck, battlecards, demo scripts)

**Activation Triggers:**
- "product-led growth"
- "positioning strategy"
- "launch plan"
- "sales enablement"

**Example Usage:**
```
Tell gtm-planner: "Create product-led growth strategy
for our B2B SaaS product"

→ Loads gtm-playbooks skill
→ References PLG best practices:
  - Freemium model design
  - In-product activation
  - Viral mechanics
  - Self-serve onboarding
  - Usage-based pricing
→ Provides tailored PLG roadmap
```

---

### Product Strategy Frameworks  Available

**Category**: Strategy
**Agents**: product-strategist, platform-architect, competitive-analyst

**Included Frameworks:**
1. **Jobs-to-be-Done** (Strategy)
2. **DHM Model** (Delight, Hard-to-copy, Margin-enhancing) - Gibson Biddle
3. **Blue Ocean Strategy** (Value innovation)
4. **Platform Strategy** (Network effects, multi-sided markets)
5. **Business Model Canvas**
6. **Wardley Mapping** (Strategic situational awareness)
7. **Porter's Five Forces**

**Activation Triggers:**
- "JTBD strategy"
- "DHM model"
- "blue ocean strategy"
- "platform strategy"

**Example Usage:**
```
Tell product-strategist: "Apply DHM model to our analytics platform.
How do we create hard-to-copy advantages?"

→ Loads product-strategy-frameworks skill
→ Applies DHM:
  - Delight: What creates customer delight?
  - Hard-to-copy: What's defensible?
  - Margin-enhancing: What improves unit economics?
→ Analyzes your product through DHM lens
→ Recommends strategic initiatives
```

---

### Growth Frameworks  Available

**Category**: Growth
**Agents**: growth-pm, data-scientist, monetization-expert

**Included Frameworks:**
1. **Growth Loops** (Viral, content, paid, sales)
2. **Activation Playbook** (Aha moment, time to value)
3. **Retention Strategies** (Engagement loops, habit formation)
4. **Referral Programs** (Incentive design, viral mechanics)
5. **Pricing Psychology** (Anchoring, framing, decoy pricing)
6. **Funnel Optimization** (Conversion rate optimization)
7. **Experiment Design** (Hypothesis, sample size, statistical significance)

**Activation Triggers:**
- "growth loop"
- "activation strategy"
- "referral program"
- "optimize funnel"

**Example Usage:**
```
Tell growth-pm: "Design a viral growth loop for our product"

→ Loads growth-frameworks skill
→ References growth loop patterns:
  1. User acquisition (source)
  2. User activation (value delivery)
  3. User engagement (retention)
  4. User referral (new users)
  5. Loop back to acquisition
→ Designs custom loop for your product
→ Identifies metrics and experiments
```

---

### Technical PM Frameworks  Available

**Category**: Technical
**Agents**: technical-pm, api-product-manager, platform-architect

**Included Frameworks:**
1. **API Design** (REST, GraphQL, gRPC)
2. **System Architecture Patterns** (Microservices, event-driven, serverless)
3. **Technical Debt Management**
4. **Performance Optimization** (Caching, CDN, database optimization)
5. **Security Best Practices** (OWASP, authentication, encryption)
6. **Scalability Patterns** (Horizontal scaling, sharding, replication)
7. **Infrastructure as Code** (Terraform, CloudFormation)

**Activation Triggers:**
- "API design"
- "system architecture"
- "technical debt"
- "scalability"

**Example Usage:**
```
Tell technical-pm: "Design REST API for our reporting feature"

→ Loads technical-pm-frameworks skill
→ Applies REST API design principles:
  - Resource modeling
  - HTTP method semantics
  - Status codes
  - Pagination
  - Versioning strategy
→ Creates comprehensive API specification
```

---

### Customer Success Frameworks (Coming Soon)

**Category**: Customer Success
**Agents**: customer-success, customer-insights, stakeholder-manager

**Included Frameworks:**
1. **Customer Onboarding** (First day, first week, first month)
2. **Health Scoring** (Engagement, adoption, support tickets)
3. **Churn Prediction** (Leading indicators, intervention playbooks)
4. **Expansion Strategy** (Upsell, cross-sell, expansion triggers)
5. **Customer Lifecycle Management** (Awareness → Advocacy)
6. **Success Playbooks** (Segmented customer plays)
7. **Voice of Customer Programs** (Feedback loops, NPS)

**Activation Triggers:**
- "customer onboarding"
- "health scoring"
- "churn prevention"
- "expansion strategy"

**Example Usage:**
```
Tell customer-success: "Design health scoring model for our SaaS product"

→ Loads customer-success-frameworks skill
→ Applies health scoring methodology:
  - Engagement metrics (login frequency, feature usage)
  - Adoption metrics (active users, feature adoption)
  - Support metrics (ticket volume, sentiment)
  - Business metrics (renewals, expansion)
→ Creates custom health score formula
→ Defines red/yellow/green thresholds
→ Suggests intervention playbooks
```

---

## Skill Composability

### Multi-Skill Scenarios

Agents can load multiple skills for complex tasks:

**Example: Complete Feature Prioritization**
```
User: "Prioritize these features considering effort,
business value, and strategic fit"

feature-prioritizer agent:
1. Loads prioritization-frameworks skill (RICE)
2. Loads product-strategy-frameworks skill (strategic alignment)
3. Loads metrics-frameworks skill (business value)

Result: Comprehensive prioritization using multiple lenses
```

### Cross-Agent Skill Usage

Multiple agents can reference the same skill:

**Example: Metrics Frameworks**
```
data-scientist + growth-pm + product-strategist
→ All reference metrics-frameworks skill
→ Consistent metric definitions across agents
→ Unified analytics approach
```

---

## Skill Development Roadmap

###  Phase 1: Foundation (Complete)
-  25 core PM skills deployed
-  Prioritization, Agile, Research, Metrics
-  GTM, Strategy, Growth, Technical
-  Innovation and Design frameworks

### Phase 2: Enhancement (Q1 2025)
- Interactive skill guides
- Visual templates and examples
- Skill combination patterns
- Advanced case studies

### Phase 3: Specialization (Q2 2025)
- Industry-specific skills (B2B SaaS, consumer, marketplace)
- Company-specific frameworks
- Advanced techniques
- Regional/market-specific playbooks

### Phase 4: Integration (Q3 2025)
- Tool-integrated skills (Jira, Amplitude, etc.)
- Data-driven skill recommendations
- Custom skill builder
- Collaborative skill development

---

## Creating New Skills

### When to Create a Skill

Create a skill when:
-  2+ agents need the same knowledge
-  It's a well-defined framework or methodology
-  It's reusable across scenarios
-  It's substantial enough to warrant separation

Don't create a skill when:
-  Only one agent uses it (include in agent directly)
-  It's too specific to one scenario
-  It's simple enough to be inline instructions

### Skill Structure Template

```yaml
---
name: skill-name
description: Brief description of framework/methodology
category: prioritization|agile|research|metrics|gtm|strategy|growth|technical|customer-success
activation_triggers:
  - keyword1
  - keyword2
version: 1.0.0
---

# Skill Name

## Overview
What this skill provides and when to use it

## Frameworks Included
List of methodologies covered

## Framework 1: [Name]

### What It Is
Brief description of framework

### When to Use
Scenarios where this is appropriate

### How to Apply
Step-by-step methodology

### Example
Realistic example of application

### Common Pitfalls
What to avoid

### Resources
- Books, articles, tools

## Framework 2: [Name]
[Same structure]

## Integration Notes
How this skill works with agents

## References
Thought leaders, canonical resources
```

---

## Skill Best Practices

### For PM Users

**1. Request Specific Frameworks**
```
 "Prioritize these features"
 "Prioritize these features using RICE framework"
```

**2. Ask for Framework Explanations**
```
"Explain RICE framework before applying it"
"Why is JTBD better than traditional interviews?"
```

**3. Compare Frameworks**
```
"Compare RICE vs ICE for prioritizing these features"
"When should I use Scrum vs Kanban?"
```

**4. Request Framework Combinations**
```
"Use RICE for effort/impact, then validate with Kano model"
```

### For Skill Developers

**1. Clear Activation Triggers**
Define keywords that should load the skill

**2. Progressive Depth**
- Level 1: Quick reference
- Level 2: Detailed methodology
- Level 3: Examples and case studies

**3. Practical Examples**
Real-world scenarios, not abstract theory

**4. Integration Guidance**
How skills work with agents and other skills

**5. Keep Current**
Update with latest best practices and industry changes

---

## Skill Performance

### Token Usage

**Skill metadata**: ~200-500 tokens (always loaded)
**Skill instructions**: ~1,000-2,000 tokens (loaded on activation)
**Skill resources**: ~2,000-5,000 tokens (referenced as needed)

**Total per skill activation**: ~3,000-7,000 tokens

### Loading Strategy

**Just-in-time loading:**
- Skill metadata always available
- Instructions load when triggered
- Resources load only when needed

**Benefits:**
- Agents stay lightweight
- Fast response times
- More room for user context

---

## Future Enhancements

### Interactive Skills (Q3 2025)
Skills that guide users through frameworks interactively:
```
"Guide me through RICE scoring step by step"
→ Skill asks questions
→ User provides answers
→ Skill calculates and explains
```

### Visual Skills (Q4 2025)
Skills with diagrams, templates, and visualizations:
```
"Show me a prioritization matrix for these features"
→ Skill generates visual output
```

### Custom Skills (Q4 2025)
Users create company-specific skills:
```
skills/
└── custom/
    └── acme-prioritization-framework.md
```

---

## Questions & Support

- **Skill Requests**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Contribute Skills**: See [CONTRIBUTING.md](../CONTRIBUTING.md)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)

---

**Available Skills**: 25 (Production Ready)
**Categories**: 9 (Prioritization, Agile, Research, Metrics, GTM, Strategy, Growth, Technical, Innovation)
**Version**: 1.0.0 (Production)
**Last Updated**: January 2025
