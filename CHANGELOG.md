# Changelog

All notable changes to the Product Management Toolkit for Claude Code will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-10-18

### Added

#### Plugin Architecture (4 Specialized Plugins - 107 Items Total)

**📋 product-strategy** (26 items)
- **Purpose**: Strategic planning, competitive analysis, business modeling, roadmapping
- **4 Agents**: product-strategist, competitive-analyst, platform-architect, monetization-expert
- **6 Commands**: okr-framework, roadmap-builder, scenario-planner, executive-summary, stakeholder-mapper, risk-assessment
- **5 Tools**: swot-analysis, business-model-canvas, value-proposition-canvas, competitive-positioning, market-sizing
- **5 Workflows**: annual-planning, quarterly-planning, portfolio-optimization, market-entry, product-pivot
- **6 Skills**: product-strategy-frameworks, vision-mission-strategy, business-model-canvas, platform-strategy, product-positioning, pricing-packaging

**🔍 product-discovery** (20 items)
- **Purpose**: Discovery, validation, research synthesis, PMF assessment
- **3 Agents**: user-researcher, discovery-facilitator, customer-insights
- **7 Commands**: interview-guide, research-synthesizer, survey-builder, usability-test-planner, persona-creator, journey-mapper, mvp-scoper
- **2 Tools**: assumption-mapping, impact-mapping
- **4 Workflows**: discovery-sprint, solution-validation, pmf-assessment, research-to-product
- **4 Skills**: user-research-techniques, continuous-discovery, design-thinking, jobs-to-be-done

**📈 product-growth** (21 items)
- **Purpose**: Growth experiments, scaling, launches, ROI analysis
- **3 Agents**: growth-pm, gtm-planner, data-scientist
- **5 Commands**: experiment-designer, kpi-dashboard, impact-estimator, release-planner, communication-plan
- **3 Tools**: roi-calculator, cost-benefit-analysis, now-next-later-roadmap
- **4 Workflows**: growth-sprint, scale-playbook, beta-program, product-launch
- **6 Skills**: growth-frameworks, metrics-frameworks, product-analytics, experiment-design, go-to-market-playbooks, product-market-fit

**⚙️ product-execution** (40 items)
- **Purpose**: Daily execution, shipping features, tactical PM work
- **8 Agents**: agile-coach, product-ops, feature-prioritizer, requirements-engineer, technical-pm, stakeholder-manager, customer-success, api-product-manager
- **16 Commands**: backlog-groomer, capacity-planner, sprint-planner, sprint-goal, user-story-writer, prd-generator, technical-spec-generator, ticket-review, quick-answer, quick-prioritize, status-update, meeting-agenda, decision-logger, doc-update, release-notes, alignment-session
- **2 Tools**: technical-debt-assessment, trade-off-analysis
- **5 Workflows**: backlog-optimization, feature-lifecycle, pm-process-audit, crisis-management, sunset-product
- **9 Skills**: agile-methodologies, dual-track-agile, prioritization-methods, specification-techniques, story-mapping, technical-debt-management, okr-methodology, api-product-management, lean-product-development

#### Core Infrastructure
- MIT License, comprehensive README, CONTRIBUTING guide
- Complete documentation suite (architecture, agents, plugins, usage, skills)
- Migration documentation (PLUGINS-INDEX, MIGRATION-GUIDE, COMPLETE-MIGRATION-SUMMARY)
- 4 comprehensive plugin READMEs (~500 lines each)

#### Performance Optimizations
- **Hybrid Model Strategy**: 8 Haiku tools (fast, cheap) + 4 Sonnet tools + 18 Sonnet workflows + 18 Sonnet agents
- **Token Efficiency**: 64% reduction on Haiku-optimized tools (2,574 → 925 lines)
- **Cost Savings**: ~30-40x efficiency on framework-based tools (Haiku 20x cheaper + 64% fewer tokens)
- **Model Override**: All tools and workflows support `--model` flag for flexibility

#### Documentation
- Total: ~3,500 lines of comprehensive documentation
- Plugin-specific READMEs with quick starts and examples
- Complete migration guides and cross-reference tables
- Backward compatibility documentation

### Technical Details
- **Total Items**: 107 (18 agents, 34 commands, 12 tools, 18 workflows, 25 skills)
- **Organization**: Domain-based (strategy, discovery, growth, execution)
- **Model Distribution**: 8 Haiku tools (27%), 22 Sonnet tools/workflows (73%)
- **Backward Compatibility**: Zero breaking changes, all legacy paths work
- **Status**: Production ready

### Framework Coverage
- **Prioritization**: RICE, ICE, MoSCoW, Kano, Value vs Effort
- **Agile**: Scrum, Kanban, SAFe, Shape Up, Scrumban, Dual-Track
- **Metrics**: AARRR (Pirate Metrics), HEART, North Star, OKRs
- **Growth**: Growth loops, viral mechanics, PLG, experiment design
- **Research**: Continuous Discovery (Teresa Torres), Design Thinking, Jobs-to-be-Done
- **Strategy**: SWOT, Porter's Five Forces, Blue Ocean, Business Model Canvas, Value Proposition Canvas

### Inspired By
- Teresa Torres (Continuous Discovery Habits)
- Marty Cagan (Empowered, Inspired)
- April Dunford (Obviously Awesome)
- Sean Ellis (Hacking Growth, ICE framework)
- Jeff Patton (User Story Mapping)
- Google (HEART, OKRs)
- Intercom (RICE Prioritization)
- Basecamp (Shape Up)

[1.0.0]: https://github.com/slgoodrich/agents/releases/tag/v1.0.0
