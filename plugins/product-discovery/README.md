# Product Discovery Plugin

Discovery, validation, research synthesis, and assumption testing for continuous product discovery.

## Overview

This plugin enables systematic discovery and validation workflows, helping teams find product-market fit, validate solutions before building, and transform research into actionable roadmaps. Based on Teresa Torres' Continuous Discovery framework and modern product discovery best practices.

**What's Included:**
- **3 Discovery Agents** - User researcher, discovery facilitator, customer insights
- **7 Research Commands** - Interview guides, surveys, personas, journey maps
- **2 Strategic Tools** - Frameworks for assumption testing and impact mapping
- **4 Discovery Workflows** - End-to-end discovery and validation processes
- **4 Framework Skills** - User research, continuous discovery, design thinking, JTBD
- **All Sonnet Models** - Strategic thinking for discovery decisions

## Quick Start

### Run Discovery Sprint
```bash
/workflows:discovery-sprint "B2B SaaS signup has 65% drop-off at onboarding. Need to validate problem and test solutions"
```

### Validate Solution
```bash
/workflows:solution-validation "AI-powered email categorization feature"
```

### Map Assumptions
```bash
/tools:assumption-mapping "New mobile app for existing web product. Assuming users want mobile-first experience"
```

---

## 👥 Agents

### Discovery & Research Agents (3 agents - All Sonnet)

#### `/pm:user-researcher`
**Model**: Claude Sonnet 4.5

Expert in user research, interviews, usability testing, and research synthesis.

**Use for**: Research planning, interview design, usability studies, insight synthesis

**Capabilities**:
- Design research studies and protocols
- Create interview guides and scripts
- Analyze research data and identify patterns
- Synthesize insights into actionable recommendations
- User persona development
- Journey mapping

**Example**:
```bash
/pm:user-researcher "Help me design a research study to understand why enterprise customers aren't adopting our mobile app"
```

#### `/pm:discovery-facilitator`
**Model**: Claude Sonnet 4.5

Expert in continuous discovery, opportunity mapping, and assumption testing (Teresa Torres framework).

**Use for**: Discovery planning, opportunity solution trees, assumption testing, continuous discovery practices

**Capabilities**:
- Facilitate discovery workshops
- Create opportunity solution trees
- Design assumption tests
- Build discovery habits and practices
- Opportunity mapping and prioritization
- Connect discovery to roadmap

**Example**:
```bash
/pm:discovery-facilitator "Help me set up a continuous discovery practice for our team of 3 PMs and 12 engineers"
```

#### `/pm:customer-insights`
**Model**: Claude Sonnet 4.5

Expert in customer feedback synthesis, sentiment analysis, and voice-of-customer programs.

**Use for**: Feedback analysis, insight generation, VoC programs, customer understanding

**Capabilities**:
- Analyze customer feedback at scale
- Identify patterns and themes
- Sentiment analysis
- Build VoC programs
- Close feedback loops
- Prioritize based on customer insights

**Example**:
```bash
/pm:customer-insights "Analyze 500+ customer support tickets and identify top pain points"
```

---

## ⚡ Commands

### Research & Planning Commands (7 commands)

#### `/pm:interview-guide`
Create structured interview guides for user research.

**Example**: `/pm:interview-guide "Enterprise customers, focus on onboarding experience"`

#### `/pm:research-synthesizer`
Synthesize research findings into insights and recommendations.

**Example**: `/pm:research-synthesizer "20 customer interviews about pricing concerns"`

#### `/pm:survey-builder`
Design user surveys with best practices.

**Example**: `/pm:survey-builder "NPS survey + feature satisfaction for Q4"`

#### `/pm:usability-test-planner`
Plan usability testing sessions with tasks and metrics.

**Example**: `/pm:usability-test-planner "New checkout flow, 5 participants, remote testing"`

#### `/pm:persona-creator`
Create detailed user personas based on research.

**Example**: `/pm:persona-creator "B2B SaaS buyer persona, IT managers at mid-market companies"`

#### `/pm:journey-mapper`
Map customer journeys with touchpoints and pain points.

**Example**: `/pm:journey-mapper "Enterprise sales journey from discovery to renewal"`

#### `/pm:mvp-scoper`
Define minimum viable product scope for new features.

**Example**: `/pm:mvp-scoper "AI-powered search feature, 8-week timeline, team of 3"`

---

## 🛠️ Tools

### Discovery & Validation Tools (2 tools - Both Sonnet)

#### `/tools:assumption-mapping`
**Model**: Claude Sonnet 4.5 (strategic, 410 lines)

Systematically identify, prioritize, and test assumptions underlying product decisions.

**Use for**: Risk reduction, validation planning, hypothesis testing, de-risking launches

**Output**:
- Assumption inventory with risk/importance scoring
- Prioritized assumptions to test first
- Test design for each critical assumption
- Validation roadmap

**Example**:
```bash
/tools:assumption-mapping "Launching enterprise SSO feature. Assuming: enterprises will pay premium, implementation is 2 weeks, customers can self-serve"
```

#### `/tools:impact-mapping`
**Model**: Claude Sonnet 4.5 (strategic, 289 lines)

Connect business goals to deliverables through behavioral changes using Gojko Adzic's framework.

**Use for**: Roadmap planning, feature prioritization, alignment, scope management

**Output**:
- Goal → Actor → Impact → Deliverable mapping
- Prioritized deliverables by goal impact
- Minimum viable feature set
- Metrics for measuring impact

**Example**:
```bash
/tools:impact-mapping "Goal: Increase trial-to-paid conversion from 15% to 25% in next quarter"
```

---

## 🔄 Workflows

### Discovery Workflows (4 workflows - All Sonnet)

#### `/workflows:discovery-sprint`
**Duration**: 1-2 weeks | **Model**: Sonnet

Rapid problem/solution validation inspired by Teresa Torres and Google Design Sprint.

**Use for**: Problem validation, solution exploration, customer discovery, de-risking before build

**Process**:
1. Problem Definition & Research
2. Opportunity Mapping
3. Solution Ideation
4. Prototype & Test
5. Learning Synthesis

**Example**:
```bash
/workflows:discovery-sprint "B2B signup 65% drop-off at onboarding (500 signups/mo, only 175 complete). Hypothesis: Process too complex"
```

#### `/workflows:solution-validation`
**Duration**: 1-2 weeks | **Model**: Sonnet

Validate solution ideas before full development commitment.

**Use for**: Feature validation, concept testing, prototype validation, build/no-build decisions

**Process**:
1. Solution Definition
2. Assumption Identification
3. Test Design
4. Validation Execution
5. Go/No-Go Decision

**Example**:
```bash
/workflows:solution-validation "AI-powered analytics dashboard. Customer request from 50+ customers, competitive gap"
```

#### `/workflows:pmf-assessment`
**Duration**: 1-2 weeks | **Model**: Sonnet

Systematic process to measure and improve product-market fit.

**Use for**: PMF measurement, identifying PMF gaps, roadmap prioritization, investor discussions

**Metrics Analyzed**:
- Sean Ellis PMF Survey (>40% "very disappointed")
- Cohort retention curves
- NPS trends
- Organic growth rate
- Customer feedback analysis

**Example**:
```bash
/workflows:pmf-assessment "B2B sales enablement, 18mo post-launch, $1.2M ARR, 85 customers. 40% trial conversion, 8% churn, NPS 35"
```

#### `/workflows:research-to-product`
**Duration**: 1 week | **Model**: Sonnet

Transform user research into actionable product roadmap items.

**Use for**: Research synthesis, roadmap planning, prioritization, stakeholder alignment

**Process**:
1. Research Synthesis
2. Insight Extraction
3. Opportunity Identification
4. Feature Ideation
5. Roadmap Integration

**Example**:
```bash
/workflows:research-to-product "Conducted 25 customer interviews about onboarding pain points. Need to synthesize and prioritize"
```

---

## 📚 Skills

### Discovery Framework Skills (4 skills)

#### `/pm:user-research-techniques`
Master user interviews, usability testing, surveys, and research synthesis. Covers qualitative and quantitative methods, best practices for different research types, and synthesis frameworks.

**When to use**: Planning research, designing studies, analyzing findings, learning research methods

#### `/pm:continuous-discovery`
Teresa Torres' Continuous Discovery framework for ongoing customer research and opportunity-driven development. Weekly customer touchpoints, opportunity solution trees, assumption testing.

**When to use**: Building discovery practices, opportunity mapping, assumption-driven development

#### `/pm:design-thinking`
Design Thinking methodology for human-centered problem solving. Empathize, Define, Ideate, Prototype, Test. Stanford d.school approach.

**When to use**: Creative problem solving, innovation workshops, human-centered design

#### `/pm:jobs-to-be-done`
Jobs-to-be-Done framework for understanding customer motivations and desired outcomes. Focuses on the job the customer hires your product to do.

**When to use**: Understanding customer needs, feature prioritization, positioning, competitive analysis

---

## 💡 Model Strategy

### Why All Sonnet?

Discovery and validation require strategic thinking, nuanced analysis, and complex decision-making:
- **Assumption mapping**: Risk assessment, prioritization frameworks
- **Impact mapping**: Goal-to-feature connectivity, behavioral analysis
- **Discovery workflows**: Multi-stakeholder coordination, synthesis
- **Validation workflows**: Test design, learning interpretation

**No Haiku tools in this plugin** - discovery is inherently strategic work.

### Performance

**All Tools & Workflows**: Claude Sonnet 4.5
- Response Time: 5-30 seconds
- Token Cost: $3/$15 per M tokens
- Quality: ⭐⭐⭐⭐⭐ (Excellent - strategic analysis)

---

## 📚 Common Use Cases

### Continuous Discovery Practice
1. `/workflows:discovery-sprint` - Weekly/bi-weekly customer research
2. `/tools:impact-mapping` - Connect research to roadmap
3. `/tools:assumption-mapping` - Identify what to test
4. `/workflows:solution-validation` - Test before building

### Pre-Build Validation
1. `/tools:assumption-mapping` - List all assumptions
2. `/workflows:solution-validation` - Test critical assumptions
3. `/tools:impact-mapping` - Define success metrics
4. Build with confidence

### Product-Market Fit Journey
1. `/workflows:pmf-assessment` - Measure current PMF
2. `/workflows:research-to-product` - Identify gaps
3. `/workflows:discovery-sprint` - Explore solutions
4. Iterate toward PMF

### Research Synthesis
1. Conduct customer interviews/surveys
2. `/workflows:research-to-product` - Synthesize insights
3. `/tools:impact-mapping` - Map to business goals
4. Prioritize roadmap

---

## 🎯 Discovery Best Practices

### Teresa Torres Principles

**Continuous**: Discovery every week, not just at kickoff
**Collaborative**: Cross-functional team involvement
**Outcome-focused**: Tie to business outcomes, not features
**Customer-centric**: Regular customer touchpoints

### This Plugin Supports:

- ✅ **Weekly discovery** - Quick sprint format (1-2 weeks)
- ✅ **Assumption-driven** - Systematic assumption mapping
- ✅ **Outcome mapping** - Impact mapping connects goals to features
- ✅ **Validation before build** - Solution validation workflow

---

## 🔗 Related Plugins

- **product-strategy** - Annual planning, competitive positioning, SWOT
- **product-growth** - Growth experiments, scaling, beta programs
- **product-execution** - Feature lifecycle, backlog management, shipping

---

## 📊 Plugin Stats

- **3 Agents**: All Sonnet (strategic research and insights)
- **7 Commands**: Research, personas, journey maps, MVPs
- **2 Tools**: Both Sonnet (strategic complexity)
- **4 Workflows**: All Sonnet (complex multi-step)
- **4 Skills**: User research, continuous discovery, design thinking, JTBD
- **Total**: 20 items focused on discovery and validation
- **Focus**: Discovery, validation, research, PMF
- **Methodology**: Teresa Torres, Lean Startup, Design Sprint

**Last Updated**: 2025-10-18
