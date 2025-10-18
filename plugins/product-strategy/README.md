# Product Strategy Plugin

Strategic planning, competitive analysis, business modeling, and roadmapping tools for product leaders.

## Overview

This plugin provides comprehensive strategic planning capabilities, from annual vision-setting to competitive positioning and business model design. Use it for high-level strategy work that shapes product direction.

**What's Included:**
- **4 Strategy Agents** - Product strategist, competitive analyst, platform architect, monetization expert
- **6 Planning Commands** - OKRs, roadmaps, scenarios, executive summaries
- **5 Strategic Tools** - Frameworks for strategy, analysis, and positioning
- **5 Planning Workflows** - End-to-end strategic planning processes
- **6 Strategy Skills** - Frameworks, vision/mission, business models, positioning, pricing
- **Hybrid Model Strategy** - Optimized for cost and performance

## Quick Start

### Analyze Competitive Positioning
```bash
/tools:competitive-positioning "Our B2B SaaS vs. competitors in enterprise market"
```

### Create Annual Strategy
```bash
/workflows:annual-planning "FY2026 Planning - $15M ARR to $40M"
```

### Design Business Model
```bash
/tools:business-model-canvas "New AI-powered analytics feature as separate product"
```

---

## 👥 Agents

### Strategic Planning Agents (4 agents - All Sonnet)

#### `/pm:product-strategist`
**Model**: Claude Sonnet 4.5

Expert in product strategy, vision, roadmaps, and OKRs for long-term product direction.

**Use for**: Strategic planning, vision development, roadmap creation, OKR setting

**Example**: `/pm:product-strategist "Help create 3-year product vision for our B2B SaaS platform"`

#### `/pm:competitive-analyst`
**Model**: Claude Sonnet 4.5

Expert in competitive intelligence, market research, and industry analysis.

**Use for**: Competitor tracking, market positioning, strategic insights, competitive analysis

**Example**: `/pm:competitive-analyst "Analyze top 3 competitors in project management SaaS space"`

#### `/pm:platform-architect`
**Model**: Claude Sonnet 4.5

Expert in platform strategy, ecosystems, multi-sided markets, and API products.

**Use for**: Platform planning, ecosystem strategy, marketplace design, API strategy

**Example**: `/pm:platform-architect "Design platform strategy for turning our product into a marketplace"`

#### `/pm:monetization-expert`
**Model**: Claude Sonnet 4.5

Expert in pricing, packaging, revenue optimization, and billing strategies.

**Use for**: Pricing decisions, packaging strategy, monetization optimization, revenue models

**Example**: `/pm:monetization-expert "Should we switch from per-user to usage-based pricing?"`

---

## ⚡ Commands

### Strategic Planning Commands (6 commands)

#### `/pm:okr-framework`
Create OKRs (Objectives and Key Results) for team alignment.

**Example**: `/pm:okr-framework "Q4 OKRs for product team, focus on enterprise growth"`

#### `/pm:roadmap-builder`
Build strategic product roadmaps with themes and initiatives.

**Example**: `/pm:roadmap-builder "12-month roadmap for B2B SaaS, enterprise focus"`

#### `/pm:scenario-planner`
Plan multiple future scenarios and strategies.

**Example**: `/pm:scenario-planner "Best/expected/worst case for market expansion to EU"`

#### `/pm:executive-summary`
Create executive summaries for strategic decisions.

**Example**: `/pm:executive-summary "Q3 product performance and Q4 strategy"`

#### `/pm:stakeholder-mapper`
Map stakeholders and their interests for alignment.

**Example**: `/pm:stakeholder-mapper "Stakeholders for enterprise tier launch"`

#### `/pm:risk-assessment`
Assess and mitigate product and strategic risks.

**Example**: `/pm:risk-assessment "Risks for migrating 1000 customers to new platform"`

---

## 🛠️ Tools

### Strategic Analysis Tools (3 tools - Haiku optimized)

#### `/tools:swot-analysis`
**Model**: Claude Haiku 4 (fast, 80 lines)

Comprehensive SWOT (Strengths, Weaknesses, Opportunities, Threats) analysis.

**Use for**: Strategic planning, product launches, competitive positioning, investment decisions

**Example**:
```bash
/tools:swot-analysis "Launching our PM SaaS in enterprise market. Currently successful SMB, moving upmarket over next 12 months"
```

#### `/tools:business-model-canvas`
**Model**: Claude Haiku 4 (fast, 86 lines)

Design and analyze business models using Osterwalder's 9-block framework.

**Use for**: New business validation, pivot planning, competitive analysis, investor pitches

**Example**:
```bash
/tools:business-model-canvas "B2B SaaS project management tool. Early-stage startup targeting SMBs, freemium model"
```

#### `/tools:value-proposition-canvas`
**Model**: Claude Haiku 4 (fast, 85 lines)

Map customer jobs, pains, and gains to your product's value propositions.

**Use for**: Product development, feature prioritization, messaging, product-market fit validation

**Example**:
```bash
/tools:value-proposition-canvas "Target: Small business owners managing inventory. Product: Cloud inventory SaaS"
```

### Market & Competitive Tools (2 tools)

#### `/tools:competitive-positioning`
**Model**: Claude Sonnet 4.5 (strategic, 267 lines)

Comprehensive competitive positioning analysis and strategy development.

**Use for**: Market positioning, differentiation strategy, competitive intelligence

#### `/tools:market-sizing`
**Model**: Claude Haiku 4 (fast, 121 lines)

Calculate TAM, SAM, and SOM for market opportunity assessment.

**Use for**: Fundraising, market validation, strategic planning, prioritization

---

## 🔄 Workflows

### Strategic Planning Workflows (3 workflows - All Sonnet)

#### `/workflows:annual-planning`
**Duration**: 2-4 weeks | **Model**: Sonnet

Comprehensive annual strategic planning process.

**Use for**: Annual strategy sessions, vision-setting, long-term roadmapping

**Example**:
```bash
/workflows:annual-planning "FY2026: Series B funded, $15M ARR, target $40M ARR, 85 employees"
```

#### `/workflows:quarterly-planning`
**Duration**: 1 week | **Model**: Sonnet

Quarterly OKR and roadmap planning process.

**Use for**: Quarterly planning cycles, OKR setting, capacity allocation

**Example**:
```bash
/workflows:quarterly-planning "Q4 2025: $5M ARR, 12 eng, 3 designers. Goal: Path to $10M ARR by mid-2026"
```

#### `/workflows:portfolio-optimization`
**Duration**: 1-2 weeks | **Model**: Sonnet

Strategic review and optimization of product portfolio.

**Use for**: Portfolio management, resource allocation, sunset decisions

### Growth & Transformation Workflows (2 workflows)

#### `/workflows:market-entry`
**Duration**: 2-4 weeks | **Model**: Sonnet

Strategic workflow for entering new markets or segments.

**Use for**: Market expansion, new segment targeting, geographic expansion

#### `/workflows:product-pivot`
**Duration**: 2-3 weeks | **Model**: Sonnet

Strategic process for evaluating and executing product pivots.

**Use for**: Pivot decisions, strategic shifts, business model changes

---

## 📚 Skills

### Strategy Framework Skills (6 skills)

#### `/pm:product-strategy-frameworks`
SWOT, Porter's Five Forces, Blue Ocean Strategy, Ansoff Matrix for strategic analysis and planning.

**When to use**: Strategic analysis, market planning, competitive strategy

#### `/pm:vision-mission-strategy`
Crafting product vision, mission statements, and strategy documents that align teams and inspire action.

**When to use**: Vision development, mission statements, strategy documentation

#### `/pm:business-model-canvas`
Business Model Canvas, Lean Canvas, and business model design frameworks (Osterwalder/Pigneur).

**When to use**: Business model design, pivot planning, new product validation

#### `/pm:platform-strategy`
Platform business models, ecosystems, and multi-sided markets. Network effects and platform dynamics.

**When to use**: Platform planning, ecosystem design, marketplace strategy

#### `/pm:product-positioning`
Positioning statements, value propositions, and differentiation frameworks for market positioning.

**When to use**: Market positioning, messaging, differentiation, competitive positioning

#### `/pm:pricing-packaging`
Pricing strategy, packaging, and monetization frameworks for product growth and revenue optimization.

**When to use**: Pricing decisions, packaging strategy, monetization, pricing experiments

---

## 💡 Model Strategy

### Cost Optimization

**Haiku Tools (4)**: Template-based frameworks, 64% smaller, 20x cheaper
- SWOT, Business Model Canvas, Value Proposition Canvas, Market Sizing

**Sonnet Tools (1)**: Strategic analysis requiring nuanced reasoning
- Competitive Positioning

**All Workflows (5)**: Complex multi-step coordination, always Sonnet

### Model Override

Use `--model sonnet` or `--model haiku` to override:
```bash
/tools:swot-analysis "complex scenario" --model sonnet  # Higher quality
/tools:competitive-positioning "simple case" --model haiku  # Faster
```

**Expected Performance**:
- Haiku tools: 2-5 seconds, $0.25/$1.25 per M tokens
- Sonnet tools/workflows: 5-30 seconds, $3/$15 per M tokens

---

## 📚 Common Use Cases

### Annual Strategic Planning
1. `/tools:swot-analysis` - Assess current position
2. `/tools:competitive-positioning` - Analyze market
3. `/workflows:annual-planning` - Create comprehensive plan
4. `/tools:business-model-canvas` - Validate business model

### Quarterly Planning Cycle
1. `/workflows:quarterly-planning` - Set OKRs and roadmap
2. `/tools:market-sizing` - Size opportunities
3. `/tools:value-proposition-canvas` - Prioritize features

### New Market Entry
1. `/tools:market-sizing` - Assess TAM/SAM/SOM
2. `/tools:competitive-positioning` - Analyze competition
3. `/workflows:market-entry` - Plan entry strategy
4. `/tools:swot-analysis` - Risk assessment

### Product Pivot Evaluation
1. `/workflows:product-pivot` - Systematic pivot evaluation
2. `/tools:business-model-canvas` - New business model
3. `/tools:value-proposition-canvas` - New value prop

---

## 🔗 Related Plugins

- **product-discovery** - Discovery, validation, PMF assessment
- **product-growth** - Growth experiments, scaling, launches
- **product-execution** - Execution, backlog management, shipping features

---

## 📊 Plugin Stats

- **4 Agents**: All Sonnet (strategic planning and analysis)
- **6 Commands**: OKRs, roadmaps, scenarios, summaries, stakeholder mapping
- **5 Tools**: 4 Haiku (optimized), 1 Sonnet (strategic)
- **5 Workflows**: All Sonnet (complex multi-step)
- **6 Skills**: Strategy frameworks, vision/mission, business models, positioning
- **Total**: 26 items focused on strategic planning
- **Token Savings**: 64% reduction on Haiku tools
- **Cost Efficiency**: ~30x for framework-based tools

**Last Updated**: 2025-10-18
