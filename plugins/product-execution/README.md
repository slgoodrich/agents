# Product Execution Plugin

Day-to-day execution, shipping features, process optimization, and tactical product management work.

## Overview

This plugin provides execution excellence tools and workflows for shipping products efficiently. From backlog management to crisis response, feature delivery to process audits, it covers the tactical execution side of product management - the hands-on work of getting things done and shipped.

**What's Included:**
- **8 Execution Agents** - Agile coach, product ops, technical PM, and more
- **16 Daily Commands** - Sprint planning, user stories, PRDs, quick answers
- **2 Decision Tools** - Technical debt assessment and trade-off analysis
- **5 Execution Workflows** - Backlog optimization, feature lifecycle, crisis management
- **9 Practice Skills** - Agile, prioritization, specifications, story mapping
- **Hybrid Model Strategy** - Strategic tools + comprehensive workflows

## Quick Start

### Optimize Backlog
```bash
/workflows:backlog-optimization "500+ items, team of 12, lots of stale items, unclear priorities, need cleanup before Q4"
```

### Assess Technical Debt
```bash
/tools:technical-debt-assessment "Codebase: 3yo Rails app, 200K LOC, team velocity down 30%, customer complaints about bugs"
```

### Handle Crisis
```bash
/workflows:crisis-management "Database server failure, 5K users affected, complete outage, enterprise SLAs at risk"
```

---

## 👥 Agents

### Execution & Delivery Agents (8 agents - All Sonnet)

#### `/pm:agile-coach`
**Model**: Claude Sonnet 4.5

Expert in Scrum, Kanban, and agile methodologies for optimizing team workflows.

**Use for**: Sprint planning, backlog grooming, ceremonies, agile process optimization

**Example**: `/pm:agile-coach "Team struggling with sprint planning - sprints always overcommitted"`

#### `/pm:product-ops`
**Model**: Claude Sonnet 4.5

Expert in PM process optimization, tools, templates, and operations for team efficiency.

**Use for**: Process improvement, PM tooling, templates, operational excellence

**Example**: `/pm:product-ops "Set up PM operations for new 5-person product team"`

#### `/pm:feature-prioritizer`
**Model**: Claude Sonnet 4.5

Expert in prioritization frameworks (RICE, ICE, Kano, Value vs Effort) for making trade-off decisions.

**Use for**: Scoring features, making trade-offs, roadmap prioritization, stakeholder alignment

**Example**: `/pm:feature-prioritizer "20 features in backlog, need to prioritize top 5 for Q4"`

#### `/pm:requirements-engineer`
**Model**: Claude Sonnet 4.5

Expert in PRDs, technical specs, user stories, and translating vision into actionable requirements.

**Use for**: Writing PRDs, technical specs, user stories, acceptance criteria

**Example**: `/pm:requirements-engineer "Write PRD for enterprise SSO feature"`

#### `/pm:technical-pm`
**Model**: Claude Sonnet 4.5

Expert in API specs, system design, architecture decisions, and technical feasibility assessment.

**Use for**: Technical requirements, API design, architecture decisions, engineering collaboration

**Example**: `/pm:technical-pm "Design REST API for our mobile app backend"`

#### `/pm:stakeholder-manager`
**Model**: Claude Sonnet 4.5

Expert in stakeholder alignment, communication, and cross-functional collaboration.

**Use for**: Managing expectations, building consensus, driving decisions, stakeholder updates

**Example**: `/pm:stakeholder-manager "CEO wants feature X, engineering says 6 months. Need to align expectations"`

#### `/pm:customer-success`
**Model**: Claude Sonnet 4.5

Expert in customer onboarding, adoption, retention, and expansion strategies.

**Use for**: Customer lifecycle, onboarding optimization, churn reduction, expansion opportunities

**Example**: `/pm:customer-success "Churn up from 5% to 8%, need retention strategy"`

#### `/pm:api-product-manager`
**Model**: Claude Sonnet 4.5

Expert in API products, developer experience, API documentation, and API monetization.

**Use for**: API-first products, developer portals, API design, developer experience

**Example**: `/pm:api-product-manager "Building public API for partners, need DX and docs strategy"`

---

## ⚡ Commands

### Sprint & Planning Commands (6 commands)

#### `/pm:backlog-groomer`
Clean and organize backlog with RICE scoring and stale item identification.

**Example**: `/pm:backlog-groomer "500+ item backlog, many outdated"`

#### `/pm:capacity-planner`
Calculate team capacity and sprint commitments.

**Example**: `/pm:capacity-planner "Team of 8, 2-week sprints, holidays next sprint"`

#### `/pm:sprint-planner`
Plan sprint goals, capacity, and commitments.

**Example**: `/pm:sprint-planner "Q4 planning sprint, team of 12, 2-week sprint"`

#### `/pm:sprint-goal`
Define clear, focused sprint goals.

**Example**: `/pm:sprint-goal "Payment flow improvements sprint"`

#### `/pm:user-story-writer`
Create user stories with acceptance criteria.

**Example**: `/pm:user-story-writer "SSO login feature for enterprise users"`

#### `/pm:ticket-review`
Review and improve ticket quality.

**Example**: `/pm:ticket-review "Review backlog ticket: Add export to CSV"`

### Documentation Commands (5 commands)

#### `/pm:prd-generator`
Generate product requirements documents.

**Example**: `/pm:prd-generator "Mobile app v2.0 with offline sync"`

#### `/pm:technical-spec-generator`
Create technical specifications.

**Example**: `/pm:technical-spec-generator "Real-time collaboration feature using WebSockets"`

#### `/pm:release-notes`
Write release notes for product updates.

**Example**: `/pm:release-notes "v2.3 release: AI search, bulk actions, performance improvements"`

#### `/pm:doc-update`
Update product documentation.

**Example**: `/pm:doc-update "Update API docs for new v2 endpoints"`

#### `/pm:status-update`
Create stakeholder status updates.

**Example**: `/pm:status-update "Weekly update for executive team"`

### Quick Execution Commands (5 commands)

#### `/pm:quick-answer`
Fast Q&A with automatic decision logging (Haiku-optimized).

**Example**: `/pm:quick-answer "Should we support IE11?"`

#### `/pm:quick-prioritize`
Quick prioritization for 2-5 items.

**Example**: `/pm:quick-prioritize "Bug fixes vs new features for this sprint"`

#### `/pm:meeting-agenda`
Create focused meeting agendas.

**Example**: `/pm:meeting-agenda "Sprint planning for team of 8"`

#### `/pm:decision-logger`
Log and document decisions with context.

**Example**: `/pm:decision-logger "Decided to use PostgreSQL over MongoDB"`

#### `/pm:alignment-session`
Plan alignment workshops and offsites.

**Example**: `/pm:alignment-session "Q4 planning offsite with product and engineering"`

---

## 🛠️ Tools

### Decision & Assessment Tools (2 tools)

#### `/tools:technical-debt-assessment`
**Model**: Claude Haiku 4 (fast, 156 lines)

Comprehensive framework for identifying, measuring, and managing technical debt.

**Use for**: Sprint planning, refactoring decisions, velocity diagnosis, platform investment

**Output**:
- Debt inventory (code quality, architecture, infrastructure, data, design)
- Impact assessment (velocity, reliability, team morale)
- Prioritized remediation roadmap
- Cost-benefit analysis of paying down debt
- Executive summary for stakeholders

**Example**:
```bash
/tools:technical-debt-assessment "Rails monolith, 3yo, 200K LOC, 12 eng team. Velocity down 30%, bugs up, onboarding slow"
```

#### `/tools:trade-off-analysis`
**Model**: Claude Sonnet 4.5 (strategic, 329 lines)

Systematic approach to evaluating trade-offs and making difficult product decisions.

**Use for**: Feature scope decisions, build vs buy, technical architecture choices, resource allocation

**Output**:
- Decision framework with success criteria
- Multi-criteria option analysis
- Trade-off matrix (cost, time, quality, scope)
- Risk assessment for each option
- Recommendation with clear rationale

**Example**:
```bash
/tools:trade-off-analysis "Decision: Build analytics in-house vs integrate Mixpanel vs use Amplitude. $50K budget, 3-month timeline"
```

---

## 🔄 Workflows

### Execution & Delivery Workflows (5 workflows - All Sonnet)

#### `/workflows:backlog-optimization`
**Duration**: 1-2 weeks | **Model**: Sonnet

Systematic backlog refinement, prioritization, and technical debt management.

**Use for**: Backlog overwhelm, sprint planning prep, stakeholder alignment, velocity improvements

**Process**:
1. Backlog Audit (categorize, identify stale items)
2. Priority Scoring (RICE/ICE framework)
3. Technical Debt Assessment
4. Grooming & Refinement
5. Capacity Mapping

**Outputs**:
- Sprint-ready backlog (top 2 sprints worth)
- Tech debt roadmap (10-20% capacity allocation)
- Archived/deferred items (with rationale)
- Priority framework (team-aligned)

**Example**:
```bash
/workflows:backlog-optimization "500+ items, team of 12, many stale (2+ years), unclear priorities, tech debt not tracked"
```

#### `/workflows:feature-lifecycle`
**Duration**: Varies (1-3 months per feature) | **Model**: Sonnet

End-to-end feature development from idea to launch and learning.

**Use for**: Feature development, product execution, learning loops, continuous improvement

**Process**:
1. Idea Validation (assumption testing)
2. Specification (PRD, technical spec)
3. Development (iterative, with checkpoints)
4. Launch (rollout strategy, monitoring)
5. Learning (metrics, feedback, iteration)

**Example**:
```bash
/workflows:feature-lifecycle "AI-powered analytics dashboard. 50+ customer requests, competitive gap, 3-month timeline"
```

#### `/workflows:pm-process-audit`
**Duration**: 1-2 weeks | **Model**: Sonnet

Comprehensive audit of PM processes, practices, and effectiveness.

**Use for**: Process improvement, team scaling, onboarding new PMs, velocity diagnosis

**Audits**:
- Discovery practices
- Prioritization frameworks
- Roadmap communication
- Stakeholder management
- Metrics and measurement
- Team collaboration
- Documentation quality

**Outputs**:
- Process maturity assessment
- Gap analysis
- Improvement recommendations
- Implementation roadmap

**Example**:
```bash
/workflows:pm-process-audit "Team of 3 PMs, 25 engineers. Feeling chaotic, unclear priorities, stakeholders frustrated"
```

#### `/workflows:crisis-management`
**Duration**: Immediate response | **Model**: Sonnet

Framework for managing product crises, incidents, and emergencies.

**Use for**: Outages, security incidents, data breaches, critical bugs, PR crises

**Process**:
1. Immediate Response (triage, communication, containment)
2. Investigation (root cause, impact assessment)
3. Resolution Planning (fix, rollback, mitigation)
4. Communication (internal, customers, public)
5. Post-Mortem (learning, prevention)

**Example**:
```bash
/workflows:crisis-management "Database failure, 5K users affected, complete outage, enterprise SLAs (99.9%), 150+ support tickets"
```

#### `/workflows:sunset-product`
**Duration**: 2-6 months | **Model**: Sonnet

Graceful process for sunsetting products, features, or platforms.

**Use for**: Feature deprecation, product end-of-life, platform migrations, focus management

**Process**:
1. Decision & Planning (business case, timeline)
2. User Analysis (who's affected, migration path)
3. Communication Strategy (announcement, timeline, support)
4. Migration Support (alternatives, data export, assistance)
5. Shutdown Execution (gradual wind-down, monitoring)
6. Post-Sunset Review

**Example**:
```bash
/workflows:sunset-product "Legacy API v1, 200 customers, new v2 available. Plan 12-month sunset"
```

---

## 📚 Skills

### Execution Excellence Skills (9 skills)

#### `/pm:agile-methodologies`
Master Scrum, Kanban, SAFe, Shape Up, and Scrumban frameworks. Sprint planning, ceremonies, metrics, and agile best practices for implementing effective workflows.

**When to use**: Implementing agile, optimizing team workflows, choosing methodology

#### `/pm:dual-track-agile`
Dual-track development balancing discovery and delivery work. Run discovery and delivery in parallel while maintaining sustainable pace.

**When to use**: Balancing discovery with delivery, continuous discovery practices

#### `/pm:prioritization-methods`
Apply RICE, ICE, MoSCoW, Kano, and Value vs Effort frameworks for feature prioritization and trade-off decisions.

**When to use**: Prioritizing features, roadmap planning, making trade-offs

#### `/pm:specification-techniques`
Best practices for writing clear, complete product specifications and requirements. PRDs, user stories, acceptance criteria, technical specs.

**When to use**: Writing requirements, PRDs, user stories, specifications

#### `/pm:story-mapping`
User Story Mapping for planning releases and understanding user journeys. Visualize product backlog as user activities and tasks.

**When to use**: Release planning, understanding user flows, backlog organization

#### `/pm:technical-debt-management`
Frameworks for identifying, prioritizing, and managing technical debt. Balance feature work with platform investment.

**When to use**: Managing tech debt, platform decisions, velocity optimization

#### `/pm:okr-methodology`
OKR best practices, cascading, tracking, and Google's OKR framework for goal setting and alignment.

**When to use**: Goal setting, OKR creation, team alignment, progress tracking

#### `/pm:api-product-management`
API-as-a-product strategy, developer experience, and API program management. Building API products and developer platforms.

**When to use**: API products, developer experience, platform strategy

#### `/pm:lean-product-development`
Lean Startup methodology, Build-Measure-Learn, and validated learning for efficient product development.

**When to use**: Lean processes, validated learning, reducing waste, MVP approach

---

## 💡 Model Strategy

### Why This Mix?

**Haiku Tool (1)**: Technical debt assessment is structured inventory → Fast
**Sonnet Tool (1)**: Trade-off analysis requires strategic reasoning → Quality
**Sonnet Workflows (5)**: Execution workflows require coordination and judgment → Quality

### Performance

**Haiku tools**: 2-5 seconds, $0.25/$1.25 per M tokens
**Sonnet tools/workflows**: 5-30 seconds, $3/$15 per M tokens

### Model Override

```bash
/tools:technical-debt-assessment "complex legacy system" --model sonnet  # Deeper analysis
/tools:trade-off-analysis "simple 2-option choice" --model haiku  # Faster
```

---

## 📚 Common Use Cases

### Velocity Improvement
1. `/tools:technical-debt-assessment` - Diagnose debt
2. `/workflows:backlog-optimization` - Clean and prioritize
3. Allocate 10-20% capacity to debt
4. Track velocity improvement

### Incident Response
1. `/workflows:crisis-management` - Immediate response framework
2. Execute incident response
3. Post-mortem and prevention
4. Update runbooks

### Feature Execution
1. `/workflows:feature-lifecycle` - Idea to launch
2. `/tools:trade-off-analysis` - Key decisions
3. `/tools:technical-debt-assessment` - Debt impact
4. Ship and learn

### Process Improvement
1. `/workflows:pm-process-audit` - Assess current state
2. Identify top 3 improvements
3. Implement changes
4. Re-audit in 6 months

### Product Sunsetting
1. `/tools:trade-off-analysis` - Sunset vs maintain decision
2. `/workflows:sunset-product` - Graceful sunset plan
3. `/tools:technical-debt-assessment` - Cleanup debt
4. Execute sunset

---

## 🎯 Execution Excellence

### Backlog Health Indicators
- **Top 2 sprints**: Sprint-ready, estimated, prioritized
- **Tech debt**: 10-20% capacity allocation
- **Stale items**: <5% of backlog older than 6 months
- **Priority clarity**: Team can explain top 5

### Feature Lifecycle Metrics
- **Cycle time**: Idea to launch
- **Success rate**: % features hitting goals
- **Customer satisfaction**: NPS on new features
- **Learning velocity**: Iterations per feature

### Crisis Response Checklist
- ✅ Incident commander assigned
- ✅ Status page updated
- ✅ Customer communication sent
- ✅ Engineering actively investigating
- ✅ Escalation path clear
- ✅ Post-mortem scheduled

---

## 🔗 Related Plugins

- **product-strategy** - Annual planning, portfolio optimization
- **product-discovery** - Discovery sprints, validation, PMF
- **product-growth** - Growth experiments, launches, scaling

---

## 📊 Plugin Stats

- **8 Agents**: All Sonnet (execution and delivery agents)
- **16 Commands**: Sprint planning, docs, quick execution (most frequent-use commands)
- **2 Tools**: 1 Haiku (assessment), 1 Sonnet (strategic)
- **5 Workflows**: All Sonnet (execution and delivery workflows)
- **9 Skills**: Agile, prioritization, specifications, story mapping, and more
- **Total**: 40 items - largest plugin focused on daily execution and shipping
- **Token Savings**: 68% reduction on tech debt tool
- **Focus**: Execution, delivery, shipping, tactical PM work

**Last Updated**: 2025-10-18
