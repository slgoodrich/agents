# Usage Guide

## Overview

This guide shows you how to use the Product Management Toolkit effectively. You'll learn interaction patterns, common workflows, and best practices for getting the most out of your PM agents and commands.

---

## Getting Started

### Installation

```bash
# Add the marketplace
/plugin marketplace add slgoodrich/agents

# Install the PM toolkit
/plugin install product-management

# Verify installation
/plugin
```

### First Steps

Try these quick wins to get familiar:

```bash
# 1. Get strategic guidance
Tell product-strategist: "What should I focus on for Q1 planning?"

# 2. Generate a PRD
/pm:prd "Add export functionality for reports"

# 3. Prioritize features
Tell feature-prioritizer: "Score these 5 features using RICE:
1. Dark mode
2. API rate limiting
3. SSO integration
4. Mobile app
5. Advanced reporting"

# 4. Plan a sprint
Tell agile-coach: "Help me plan Sprint 23 with 4 developers and velocity of 28 points"
```

---

## Interaction Patterns

### Pattern 1: Natural Language (Recommended)

Describe what you need in plain English. Claude Code automatically routes to the right agent.

**Examples:**
```
"I need to create quarterly OKRs"
→ Routes to product-strategist

"Help me understand why users are churning"
→ Routes to user-researcher or customer-insights

"Write a PRD for multi-factor authentication"
→ Routes to requirements-engineer

"Should we prioritize feature A or B?"
→ Routes to feature-prioritizer
```

**Benefits:**
-  No need to remember agent names
-  Claude Code picks the best expert
-  Conversational and flexible
-  Great for exploratory work

**Best for:**
- Exploration and discovery
- Complex, multi-faceted problems
- When unsure which agent to use
- Iterative conversations

### Pattern 2: Direct Agent Invocation

Explicitly tell Claude Code which agent you want.

**Syntax:**
```
Tell [agent-name]: "[your request]"
Ask [agent-name]: "[your question]"
Get [agent-name] to [do something]
```

**Examples:**
```
Tell product-strategist: "Create Q2 2025 OKRs"
Ask user-researcher: "Design a churn research study"
Get requirements-engineer to write a PRD for dark mode
Have technical-pm assess feasibility of real-time collaboration
```

**Benefits:**
-  Guaranteed routing to specific expert
-  Predictable behavior
-  Direct and efficient
-  Good for familiar workflows

**Best for:**
- Known agent for the task
- Repeated workflows
- Specific expertise needed
- Direct, focused requests

### Pattern 3: Slash Commands

Fast utilities for common, structured tasks.

**Syntax:**
```
/pm:command-name [arguments]
```

**Examples:**
```bash
/pm:prd "Feature description"
/pm:okr "Q2 2025"
/pm:roadmap "2025 Product Vision"
/pm:sprint-plan "Sprint 47"
/pm:capacity "Q1 planning"
```

**Benefits:**
-  Fastest interaction method
-  Deterministic outputs
-  Repeatable results
-  Great for templates

**Best for:**
- Quick document generation
- Template-based outputs
- Repetitive tasks
- Structured deliverables

---

## Common Workflows

### Workflow 1: Strategic Planning

**Goal**: Create quarterly strategy and OKRs

```
Step 1: Analyze performance
Tell data-scientist: "Analyze Q4 2024 metrics:
- 50K MAU (up from 35K)
- 35% activation rate (down from 40%)
- $2M ARR (up from $1.5M)
What should we focus on for Q1?"

Step 2: Research market
Tell competitive-analyst: "What are Asana, Monday, and Linear
focusing on in 2025? Any threats or opportunities?"

Step 3: Draft strategy
Tell product-strategist: "Create Q1 2025 strategy and OKRs.
Focus areas: Improve activation, expand enterprise features"

Step 4: Align stakeholders
Tell stakeholder-manager: "Help me present Q1 OKRs to exec team.
Potential concerns: Engineering wants tech debt time,
Sales wants more features"

Step 5: Prioritize backlog
Tell feature-prioritizer: "Score these 10 features against
our Q1 OKRs using RICE"

Step 6: Plan execution
Tell agile-coach: "Plan first sprint of Q1. Team of 5,
velocity 35. Must include: API v2 foundations"
```

### Workflow 2: Feature Development

**Goal**: Take feature from idea to launch

```
Step 1: Validate need
Tell user-researcher: "Design research to validate:
'Users need better export options for reports'"

Step 2: Define strategy
Tell product-strategist: "How does export functionality
fit our 2025 roadmap? Worth prioritizing?"

Step 3: Write specs
Tell requirements-engineer: "Write comprehensive PRD
for report export feature (CSV, PDF, JSON formats)"

Step 4: Technical feasibility
Tell technical-pm: "Assess technical approach for export.
Current stack: Node.js, PostgreSQL, React.
Should we do sync or async export?"

Step 5: Prioritize
Tell feature-prioritizer: "Score export feature vs.
these 5 other backlog items using RICE"

Step 6: Plan sprint
Tell agile-coach: "Break export feature into user stories
and estimate. Velocity: 32 points"

Step 7: Plan launch
Tell gtm-planner: "Create GTM plan for export feature.
Target: existing customers, secondary: prospects"

Step 8: Design onboarding
Tell customer-success: "How do we onboard customers to
export feature and drive adoption?"
```

### Workflow 3: Discovery & Research

**Goal**: Understand user churn problem

```
Step 1: Analyze data
Tell data-scientist: "Analyze churn cohorts:
- 30% of users churn after 30 days
- Higher churn in SMB segment
- Lower churn for users who complete onboarding
Build cohort analysis and identify patterns"

Step 2: Review feedback
Tell customer-insights: "Synthesize these 200 support tickets
and 50 customer interviews. What themes emerge?"

Step 3: Design research
Tell user-researcher: "Design research study to understand
30-day churn. Include interview guide, screener, and timeline"

Step 4: Facilitate discovery
Tell discovery-facilitator: "Create opportunity solution tree
for reducing churn. Key outcome: Improve 30-day retention from 70% to 85%"

Step 5: Competitive analysis
Tell competitive-analyst: "How do competitors solve onboarding
and activation? Any best practices we should adopt?"

Step 6: Define opportunities
Tell product-strategist: "Based on research, what are top 3
opportunities to reduce churn? Recommend prioritization"
```

### Workflow 4: Growth Optimization

**Goal**: Improve activation funnel

```
Step 1: Analyze funnel
Tell data-scientist: "Analyze signup → activation funnel:
- 100% signup
- 70% verify email
- 50% complete onboarding
- 30% reach aha moment
Where should we focus?"

Step 2: Design experiments
Tell growth-pm: "Design 5 experiments to improve onboarding
completion from 50% to 65%"

Step 3: Validate with users
Tell user-researcher: "Interview 10 users who dropped off
during onboarding. Why didn't they complete?"

Step 4: Create growth roadmap
Tell product-strategist: "Build Q1 growth roadmap focused
on activation. Include success metrics"

Step 5: Define technical approach
Tell technical-pm: "What's the technical approach for
experiment framework? Need to A/B test 5 onboarding variations"

Step 6: Track metrics
Tell data-scientist: "Design experiment tracking for
onboarding A/B tests. What's statistical significance threshold?"

Step 7: Optimize monetization
Tell monetization-expert: "Should we adjust pricing to
improve activation? Or focus on free-to-paid conversion?"
```

### Workflow 5: Product Launch

**Goal**: Launch new feature successfully

```
Step 1: Define positioning
Tell gtm-planner: "Create positioning for our new API product
targeting developers. Competitors: Stripe, Twilio, SendGrid"

Step 2: Build launch plan
Tell gtm-planner: "Create comprehensive launch plan:
- Internal preview: Feb 1
- Beta launch: Feb 15
- GA: March 1
Include timeline, channels, assets needed"

Step 3: Stakeholder alignment
Tell stakeholder-manager: "Present launch plan to exec team
and get buy-in. Concerns: Marketing capacity, sales readiness"

Step 4: Plan rollout
Tell agile-coach: "Plan 3-sprint execution for launch.
Include: Beta onboarding, GA release, bug fixes"

Step 5: Customer success prep
Tell customer-success: "Design customer onboarding for new API.
Include docs, tutorials, support resources"

Step 6: Track success
Tell data-scientist: "Define launch success metrics:
- Beta: 50 developers onboarded
- GA: 200 signups in first month
- 30-day retention: >70%"
```

---

## Multi-Agent Orchestration

### Sequential Pattern

Agents work one after another, passing outputs forward.

**Example: Idea → Launch**
```
1. discovery-facilitator
   Input: User problem
   Output: Opportunity solution tree

2. product-strategist
   Input: Opportunities
   Output: Strategic recommendation

3. requirements-engineer
   Input: Strategy
   Output: Detailed PRD

4. technical-pm
   Input: PRD
   Output: Technical specifications

5. agile-coach
   Input: Specs
   Output: Sprint plan

6. gtm-planner
   Input: Feature
   Output: Launch plan
```

### Parallel Pattern

Multiple agents work simultaneously on different aspects.

**Example: Quarterly Planning**
```
In parallel:

Agent A (data-scientist)
→ Analyze Q4 metrics

Agent B (competitive-analyst)
→ Market research

Agent C (customer-insights)
→ Feedback synthesis

Agent D (stakeholder-manager)
→ Gather stakeholder input

Then synthesize:
product-strategist
→ Create Q1 strategy from all inputs
```

### Iterative Pattern

Agents refine each other's work through multiple passes.

**Example: PRD Refinement**
```
Round 1:
requirements-engineer → Draft PRD

Round 2:
user-researcher → Validate with 5 customers
requirements-engineer → Update PRD based on feedback

Round 3:
technical-pm → Review technical feasibility
requirements-engineer → Adjust specs for feasibility

Round 4:
stakeholder-manager → Review with execs
requirements-engineer → Final polish
```

---

## Best Practices

### 1. Start Specific, Then Explore

**Good:**
```
"Tell product-strategist: Create Q2 2025 OKRs for a B2B SaaS
analytics platform. Current focus: product-market fit.
Team: 5 engineers, 2 designers, 1 PM"
```

**Better:**
Start specific, then ask follow-ups:
```
"Tell product-strategist: Create Q2 2025 OKRs"
→ Get draft OKRs
"How do these align with growth goals?"
→ Refine
"Can you adjust for enterprise focus?"
→ Final version
```

### 2. Provide Context

Agents work better with context. Include:
- Company stage (startup, scale-up, enterprise)
- Product type (B2B SaaS, consumer app, marketplace)
- Team size and structure
- Current metrics and goals
- Constraints and challenges

**Example:**
```
Tell growth-pm: "Optimize our activation funnel.

Context:
- B2B SaaS analytics platform
- 50K MAU, 30% activation
- Onboarding: 5 steps, 10 minutes
- Competitor benchmark: 45% activation
- Goal: Reach 40% activation by Q2

What should we focus on?"
```

### 3. Chain Agents Intentionally

Design agent sequences that make sense:

**Good chains:**
```
Strategy → Research → Specs → Execution
user-researcher → requirements-engineer → agile-coach

Analysis → Recommendation → Execution
data-scientist → product-strategist → gtm-planner
```

**Avoid:**
```
Random jumping between agents
Asking one agent for another's specialty
```

### 4. Use Commands for Speed

When you know exactly what you need:

**Fast:**
```bash
/pm:prd "Dark mode feature"
/pm:okr "Q2 2025"
/pm:roadmap "2025 Vision"
```

**Comprehensive:**
```
Tell requirements-engineer: "Write PRD for dark mode with:
- User stories for all personas
- Edge cases for system theme detection
- Accessibility considerations
- Analytics requirements"
```

Choose based on time vs. depth trade-off.

### 5. Iterate and Refine

Don't expect perfection on first output:

```
1. Get quick draft
   "Tell product-strategist: Quick Q1 OKRs"

2. Add constraints
   "Adjust for: Limited engineering capacity,
   focus on retention over acquisition"

3. Refine specifics
   "Make KR2 more measurable with specific target"

4. Final polish
   "Format for exec presentation"
```

### 6. Reference Previous Work

Agents remember conversation context:

```
"Tell requirements-engineer: Write PRD for export feature"
→ Get PRD

"Now break that into user stories for agile-coach"
→ User stories from same PRD

"technical-pm, assess feasibility of the PRD above"
→ Technical review of same feature
```

### 7. Ask for Frameworks

Agents know PM frameworks. Use them:

```
"Tell feature-prioritizer: Use RICE framework"
"Tell growth-pm: Apply AARRR framework"
"Tell user-researcher: Use Jobs-to-be-Done approach"
"Tell product-strategist: Apply DHM model (Delight, Hard-to-copy, Margin)"
```

---

## Tips & Tricks

### Getting Unstuck

**When unsure which agent to use:**
```
"I need to understand user churn and decide what to build"
→ Let Claude Code route automatically
```

**When output isn't quite right:**
```
"Can you make this more concise?"
"Can you add more technical detail?"
"Focus more on enterprise customers"
"Make this suitable for executive audience"
```

**When you need different perspective:**
```
After product-strategist:
"Now show me what data-scientist would say about this"

After user-researcher:
"What would competitive-analyst add to this?"
```

### Advanced Techniques

**1. Comparative Analysis**
```
"Tell feature-prioritizer: Compare these 3 features using
both RICE and Kano. Show me where they differ in ranking"
```

**2. Devil's Advocate**
```
"Tell product-strategist: Argue why we SHOULDN'T pursue
this strategy. What are the risks?"
```

**3. Multi-Format Output**
```
"Tell gtm-planner: Create launch plan in 3 formats:
1. Executive summary (1 page)
2. Detailed timeline (Gantt-style)
3. Checklist for execution"
```

**4. Scenario Planning**
```
"Tell product-strategist: Create OKRs for 3 scenarios:
1. We get Series B funding
2. We don't get funding
3. Competitor launches similar product"
```

**5. Template Creation**
```
"Tell requirements-engineer: Create a PRD template
for our team. Include: sections, questions to answer,
acceptance criteria format"
```

---

## Common Use Cases

### Daily PM Work

**Morning planning:**
```
Tell agile-coach: "What should I focus on today?
Sprint 23, day 3 of 10. Yesterday: shipped auth feature,
blocked on API design review"
```

**Quick decisions:**
```
Tell feature-prioritizer: "Should we fix bug affecting 100 users
or ship feature requested by 50 enterprise prospects?"
```

**Stakeholder updates:**
```
Tell stakeholder-manager: "Draft weekly update for exec team.
Wins: Shipped feature X. Challenges: Delayed feature Y.
Next: Planning Q2"
```

### Weekly PM Work

**Sprint planning:**
```
Tell agile-coach: "Plan Sprint 24. Velocity 30, team of 5.
Must include: API v2 foundation, bug fixes from last sprint"
```

**Backlog grooming:**
```
Tell requirements-engineer: "Review these 10 backlog items
and identify which need more detail before sprint planning"
```

**Metrics review:**
```
Tell data-scientist: "Analyze this week's metrics. Flag any
concerning trends and recommend if we should investigate"
```

### Monthly PM Work

**Roadmap reviews:**
```
Tell product-strategist: "Review our roadmap. Are we on track
for Q1 goals? Should we adjust priorities?"
```

**Research synthesis:**
```
Tell customer-insights: "Synthesize this month's feedback
from support, sales calls, and user interviews.
What are the top themes?"
```

**Competitive updates:**
```
Tell competitive-analyst: "What did our competitors ship
this month? Any threats or opportunities?"
```

### Quarterly PM Work

**Strategic planning:**
```
Tell product-strategist: "Create Q2 2025 strategy and OKRs"
```

**Quarterly reviews:**
```
Tell data-scientist: "Analyze Q1 performance against OKRs.
What worked? What didn't? What should change for Q2?"
```

**Team retrospectives:**
```
Tell agile-coach: "Facilitate Q1 team retrospective.
Topics: Process improvements, velocity trends,
collaboration challenges"
```

---

## Troubleshooting

### Agent Not Activating

**Problem**: Agent doesn't activate when expected

**Solutions:**
```
# Be more explicit
 "Help with strategy"
 "Tell product-strategist: Create Q2 OKRs"

# Describe the task clearly
 "I need to create quarterly objectives and key results
for my product team"

# Verify agent exists
/plugin agents product-management
```

### Wrong Agent Activated

**Problem**: Claude Code routed to wrong agent

**Solutions:**
```
# Be more specific about need
"I need user-researcher (not data-scientist) to design
a qualitative research study"

# Use direct invocation
"Tell user-researcher: [request]"
```

### Output Not Helpful

**Problem**: Agent output doesn't meet needs

**Solutions:**
```
# Provide more context
"Give me more context about your company and goals"

# Ask for refinement
"Can you make this more actionable?"
"Can you add specific examples?"
"Can you tailor this for B2B SaaS?"

# Try different agent
"Let me ask technical-pm for the technical perspective"
```

### Need Multiple Perspectives

**Problem**: Want input from multiple agents

**Solutions:**
```
# Sequential approach
1. "Tell product-strategist: Should we build feature X?"
2. "Tell user-researcher: Validate this with customers"
3. "Tell feature-prioritizer: Score against backlog"

# Synthesis request
"Get input from product-strategist, user-researcher,
and feature-prioritizer on whether to build feature X"
```

---

## Learning Resources

### Understanding PM Frameworks

Ask agents to explain frameworks:

```
"Tell feature-prioritizer: Explain RICE framework and
when to use it vs ICE"

"Tell product-strategist: Teach me about OKRs.
What makes good vs bad OKRs?"

"Tell growth-pm: Explain AARRR framework and how to apply it"
```

### Example-Based Learning

Ask for realistic examples:

```
"Tell requirements-engineer: Show me a well-written PRD
for a similar feature to what I'm building"

"Tell gtm-planner: Show example GTM plan for a SaaS product"

"Tell agile-coach: Example sprint retrospective facilitation"
```

### Framework Application

Practice applying frameworks:

```
"Tell feature-prioritizer: Walk me through scoring this
feature with RICE step-by-step"

"Tell product-strategist: Let's create OKRs together.
Ask me questions and guide me through the process"
```

---

## Next Steps

### Explore the Toolkit

```bash
# View all agents
/plugin agents product-management

# Read documentation
See docs/agents.md for agent catalog
See docs/architecture.md for design principles
```

### Join the Community

- **Issues**: [GitHub Issues](https://github.com/slgoodrich/agents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/slgoodrich/agents/discussions)
- **Contribute**: See CONTRIBUTING.md

### Share Your Workflows

Found a great multi-agent workflow? Share it!
- Open a discussion
- Submit a PR with example
- Help others learn from your experience

---

**Happy PM-ing!** 🚀

**Version**: 1.0.0
**Last Updated**: January 2025
