# Product Growth Plugin

Growth experiments, scaling playbooks, launches, and ROI analysis for accelerating product growth.

## Overview

This plugin provides comprehensive growth capabilities from launch planning to scaling playbooks, growth experiments to ROI analysis. Use it to accelerate growth, optimize launches, and scale from PMF to market leadership.

**What's Included:**
- **3 Growth Agents** - Growth PM, GTM planner, data scientist
- **5 Growth Commands** - Experiments, KPIs, impact estimates, releases, communications
- **3 Analysis Tools** - ROI, cost-benefit, and roadmapping (all Haiku-optimized)
- **4 Growth Workflows** - Launches, beta programs, growth sprints, scaling (all Sonnet)
- **6 Growth Skills** - Growth frameworks, metrics, analytics, experiments, GTM, PMF
- **Hybrid Model Strategy** - Fast analysis tools + strategic workflow coordination

## Quick Start

### Calculate Feature ROI
```bash
/tools:roi-calculator "Building enterprise SSO: $200K dev + $30K/yr maintenance. Returns: 50 customers @ $20K ACV, churn 8%→5%"
```

### Launch Product
```bash
/workflows:product-launch "Enterprise tier launch: SSO, white-labeling, dedicated support. $999/mo, target 20 deals in 6 months"
```

### Run Growth Sprint
```bash
/workflows:growth-sprint "Currently $5M ARR, 15% MoQ growth. Target: 25% growth through activation improvements"
```

---

## 👥 Agents

### Growth & Analytics Agents (3 agents - All Sonnet)

#### `/pm:growth-pm`
**Model**: Claude Sonnet 4.5

Expert in growth strategy, acquisition, activation, retention, and product-led growth.

**Use for**: Growth loops, experiments, scalable user growth, activation optimization, retention strategies

**Example**: `/pm:growth-pm "Activation rate is 35%, want to get to 50%. Help design growth experiments"`

#### `/pm:gtm-planner`
**Model**: Claude Sonnet 4.5

Expert in go-to-market strategy, product launches, positioning, and messaging.

**Use for**: Launch planning, GTM execution, market positioning, launch coordination

**Example**: `/pm:gtm-planner "Planning enterprise tier launch in 8 weeks, need full GTM strategy"`

#### `/pm:data-scientist`
**Model**: Claude Sonnet 4.5

Expert in analytics, experiments, statistical analysis, and data-driven decision making.

**Use for**: A/B testing, metrics analysis, cohort retention, quantitative insights, experiment design

**Example**: `/pm:data-scientist "Design A/B test for new onboarding flow, need sample size and metrics"`

---

## ⚡ Commands

### Growth & Launch Commands (5 commands)

#### `/pm:experiment-designer`
Design growth experiments with hypotheses, metrics, and test plans.

**Example**: `/pm:experiment-designer "Test if personalized emails increase activation from 30% to 40%"`

#### `/pm:kpi-dashboard`
Create KPI dashboards and metrics frameworks.

**Example**: `/pm:kpi-dashboard "Growth metrics dashboard: AARRR + North Star metric"`

#### `/pm:impact-estimator`
Estimate business impact of features and initiatives.

**Example**: `/pm:impact-estimator "New mobile app: impact on engagement, revenue, retention"`

#### `/pm:release-planner`
Plan product releases with rollout strategies.

**Example**: `/pm:release-planner "v3.0 release: 20 features, phased rollout to 10K users"`

#### `/pm:communication-plan`
Create launch and release communication plans.

**Example**: `/pm:communication-plan "Enterprise tier launch comms: customers, prospects, internal"`

---

## 🛠️ Tools

### Analysis Tools (3 tools - All Haiku optimized)

#### `/tools:roi-calculator`
**Model**: Claude Haiku 4 (fast, 141 lines)

Calculate return on investment for product features and initiatives with detailed modeling.

**Use for**: Feature prioritization, business cases, investment decisions, stakeholder alignment

**Output**:
- Simple ROI, NPV, IRR, payback period
- 3-year financial projection
- Scenario modeling (best/expected/worst)
- Sensitivity analysis
- Go/no-go recommendation

**Example**:
```bash
/tools:roi-calculator "Building mobile app: $200K dev, $30K/yr. Returns: 20% users mobile, 2x engagement, 15% conversion lift"
```

#### `/tools:cost-benefit-analysis`
**Model**: Claude Haiku 4 (fast, 146 lines)

Systematic evaluation of costs versus benefits for product decisions and investments.

**Use for**: Major feature decisions, platform investments, build vs buy, resource allocation

**Output**:
- Quantitative benefits (revenue, savings, productivity)
- Qualitative benefits (strategic value)
- Complete cost analysis (dev, infrastructure, GTM, opportunity)
- Timeline and break-even analysis
- Strategic considerations
- Go/no-go/pilot recommendation

**Example**:
```bash
/tools:cost-benefit-analysis "Native mobile app (iOS + Android). Web-only SaaS, competitors have apps, 20% mobile traffic"
```

#### `/tools:now-next-later-roadmap`
**Model**: Claude Haiku 4 (fast, 110 lines)

Build flexible, outcome-oriented roadmaps without rigid timelines.

**Use for**: Public roadmaps, stakeholder communication, agile planning, reducing commitment pressure

**Output**:
- NOW (0-3 months): In progress, high confidence
- NEXT (3-6 months): Planned, medium confidence
- LATER (6+ months): Being explored, lower confidence
- Outcome-focused framing
- Clear success criteria

**Example**:
```bash
/tools:now-next-later-roadmap "B2B SaaS, planning next 6-12 months. Focus: enterprise features, integrations, mobile"
```

---

## 🔄 Workflows

### Launch & Beta Workflows (2 workflows - Sonnet)

#### `/workflows:product-launch`
**Duration**: 6-8 weeks | **Model**: Sonnet

Full go-to-market orchestration for major product launches.

**Use for**: Major releases, new products, tier launches, market expansion

**Process**:
1. Launch Planning & Timeline
2. GTM Strategy & Positioning
3. Launch Materials & Enablement
4. Launch Execution
5. Post-Launch Optimization

**Example**:
```bash
/workflows:product-launch "Enterprise tier: SSO, white-labeling, dedicated support. $999/mo + setup. Target 20 deals in 6 months"
```

#### `/workflows:beta-program`
**Duration**: 4-8 weeks | **Model**: Sonnet

Comprehensive framework for launching and managing product beta programs.

**Use for**: Pre-launch validation, early adopter programs, feature testing, feedback loops

**Process**:
1. Beta Program Design
2. Participant Recruitment
3. Onboarding & Support
4. Feedback Collection
5. Learning & Iteration

**Example**:
```bash
/workflows:beta-program "New AI analytics feature. 6-week beta, target 20-30 customers, focus on enterprise segment"
```

### Growth & Scaling Workflows (2 workflows - Sonnet)

#### `/workflows:growth-sprint`
**Duration**: 4 weeks | **Model**: Sonnet

Intensive 4-week sprint to accelerate product growth through rapid experimentation.

**Use for**: Growth plateaus, activation improvements, conversion optimization, retention improvements

**Process**:
1. Growth Diagnosis & Baseline
2. Opportunity Identification (AARRR)
3. Experiment Design (20+ ideas → 5-7 tests)
4. Rapid Execution (1-week cycles)
5. Learning & Scaling

**Frameworks**:
- AARRR (Pirate Metrics): Acquisition, Activation, Retention, Revenue, Referral
- North Star Metric identification
- Growth loops
- ICE scoring (Impact, Confidence, Ease)

**Example**:
```bash
/workflows:growth-sprint "$5M ARR, 15% MoQ growth, want 25%. Focus: Activation (current 35% → target 50%)"
```

#### `/workflows:scale-playbook`
**Duration**: Ongoing framework | **Model**: Sonnet

Framework for scaling product and operations from PMF to growth stage ($5M → $20M ARR).

**Use for**: Scaling challenges, hiring planning, process scaling, platform investment decisions

**Covers**:
- Product scaling (tech debt, architecture, platform)
- Team scaling (hiring, onboarding, culture)
- Process scaling (agile, ceremonies, communication)
- GTM scaling (sales, marketing, customer success)
- Metrics & systems (analytics, monitoring, tools)

**Example**:
```bash
/workflows:scale-playbook "Achieved PMF at $5M ARR, 120 customers, 45 employees. Goal: $20M ARR in 12-18 months"
```

---

## 📚 Skills

### Growth & Launch Skills (6 skills)

#### `/pm:growth-frameworks`
Growth models including AARRR (Pirate Metrics), growth loops, and viral mechanics for accelerating product growth.

**When to use**: Growth strategy, growth loops, viral features, acquisition/activation/retention

#### `/pm:metrics-frameworks`
Apply AARRR (Pirate Metrics), HEART, North Star Metric, and OKR frameworks for measuring product success.

**When to use**: Defining KPIs, measuring success, setting goals, metrics strategy

#### `/pm:product-analytics`
Product analytics frameworks, metrics, and measurement best practices for data-driven decisions.

**When to use**: Analytics setup, metrics tracking, funnel analysis, cohort analysis

#### `/pm:experiment-design`
A/B testing, multivariate testing, and experiment frameworks for product optimization.

**When to use**: A/B tests, experiment design, hypothesis testing, statistical analysis

#### `/pm:go-to-market-playbooks`
Master product launches, positioning, messaging, and GTM strategies for successful market entry.

**When to use**: Launch planning, market entry, positioning, GTM execution

#### `/pm:product-market-fit`
Frameworks for measuring, achieving, and maintaining product-market fit.

**When to use**: PMF measurement, PMF improvement, retention optimization, market validation

---

## 💡 Model Strategy

### Cost Optimization

**Haiku Tools (3)**: Formula-based calculations, 64% smaller, 20x cheaper
- ROI Calculator, Cost-Benefit Analysis, Now-Next-Later Roadmap

**Sonnet Workflows (4)**: Complex coordination, strategic decisions
- Product Launch, Beta Program, Growth Sprint, Scale Playbook

### Model Override

```bash
/tools:roi-calculator "complex scenario" --model sonnet  # Higher quality
/workflows:growth-sprint "simple test" --model haiku  # Faster (not recommended)
```

**Expected Performance**:
- Haiku tools: 2-5 seconds, $0.25/$1.25 per M tokens
- Sonnet workflows: 10-30 seconds, $3/$15 per M tokens

---

## 📚 Common Use Cases

### Product Launch Planning
1. `/tools:cost-benefit-analysis` - Validate business case
2. `/tools:roi-calculator` - Project returns
3. `/workflows:beta-program` - Run private beta
4. `/workflows:product-launch` - Execute launch
5. `/tools:now-next-later-roadmap` - Communicate roadmap

### Growth Acceleration
1. `/workflows:growth-sprint` - 4-week intensive sprint
2. `/tools:roi-calculator` - Prioritize growth experiments
3. Run experiments
4. Measure and iterate

### Scaling from PMF to Growth
1. `/workflows:scale-playbook` - Systematic scaling framework
2. `/tools:cost-benefit-analysis` - Platform investment decisions
3. `/tools:now-next-later-roadmap` - Balance tech debt vs features
4. Execute scaling plan

### Feature Investment Decisions
1. `/tools:roi-calculator` - Quick ROI estimate
2. `/tools:cost-benefit-analysis` - Detailed analysis
3. Decision: Build / Defer / Buy
4. Track actual vs projected

---

## 🎯 Growth Frameworks

### AARRR (Pirate Metrics)
- **Acquisition**: How users find you
- **Activation**: First happy experience
- **Retention**: Users come back
- **Revenue**: Monetization
- **Referral**: Viral growth

### Growth Loops
- User-generated content loops
- Viral/referral loops
- Paid acquisition loops
- Sales-led loops

### North Star Metric
- Single metric that best captures core value
- Leading indicator of sustainable growth
- Aligns team around what matters

---

## 🔗 Related Plugins

- **product-strategy** - Annual planning, market sizing, competitive analysis
- **product-discovery** - Discovery sprints, PMF assessment, validation
- **product-execution** - Feature lifecycle, backlog optimization, shipping

---

## 📊 Plugin Stats

- **3 Agents**: All Sonnet (growth strategy and analytics)
- **5 Commands**: Experiments, KPIs, impact estimates, releases, communications
- **3 Tools**: All Haiku (optimized for speed)
- **4 Workflows**: All Sonnet (complex multi-step)
- **6 Skills**: Growth frameworks, metrics, analytics, experiments, GTM, PMF
- **Total**: 21 items focused on growth and launches
- **Token Savings**: 64% reduction on tools
- **Cost Efficiency**: ~30x for calculation tools
- **Focus**: Growth, scaling, launches, ROI

**Last Updated**: 2025-10-18
