# Changelog

All notable changes to the Product Management Toolkit for Claude Code will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-10-23

### BREAKING CHANGES

This is a major architectural restructure that introduces breaking changes to command namespaces. All functionality has been preserved, but commands now use full descriptive namespaces instead of abbreviated prefixes.

**Migration Required**: Update all command references from old namespaces (e.g., `/ps:swot-analysis`) to new namespaces (e.g., `/strategic-planning:swot-analysis`). See [MIGRATION-GUIDE.md](./docs/MIGRATION-GUIDE.md) for complete mapping of all 157 namespace changes.

**Transition Period**: Old plugins (ps, pd, pg, pe) remain available during the transition period but are deprecated.

### Added

#### New Plugin Architecture (18 Focused Plugins - 103 Components)

**Perfect 1:1 Plugin-to-Agent Architecture**:
- Each plugin now contains exactly 1 unique agent (no duplication across plugins)
- 18 focused plugins vs 4 large plugins in v1.0.0
- Industry-standard architecture matching gold standard patterns
- Better discoverability with focused, single-responsibility plugins

**New Plugin Structure**:
1. **strategic-planning** (8 components) - Vision, mission, business models, strategic frameworks
2. **competitive-analysis** (6 components) - Market positioning, competitive intelligence, differentiation
3. **platform-strategy** (6 components) - Platform business models, ecosystems, multi-sided markets
4. **product-pricing** (6 components) - Pricing strategy, packaging, monetization frameworks
5. **user-research** (7 components) - User interviews, usability testing, research synthesis
6. **problem-discovery** (6 components) - Continuous discovery, opportunity solution trees
7. **design-thinking** (6 components) - Human-centered problem solving, design sprints
8. **jobs-framework** (5 components) - Jobs-to-be-Done framework and analysis
9. **growth-strategy** (8 components) - Growth frameworks, loops, viral mechanics
10. **metrics-analytics** (7 components) - AARRR, HEART, North Star metrics, OKR frameworks
11. **experimentation** (5 components) - A/B testing, experiment design, hypothesis validation
12. **go-to-market** (9 components) - Product launches, positioning, messaging, GTM strategies
13. **agile-execution** (11 components) - Scrum, Kanban, SAFe, Shape Up methodologies
14. **feature-management** (10 components) - Feature lifecycle, prioritization, delivery
15. **technical-pm** (6 components) - Technical debt, API products, technical specifications
16. **stakeholder-management** (7 components) - Alignment, communication, decision-making
17. **customer-success** (5 components) - User onboarding, support, customer feedback
18. **product-operations** (8 components) - Process optimization, capacity planning, operations

**Full Descriptive Namespaces**:
- All commands now use autocomplete-friendly, descriptive namespaces
- Examples: `/user-research:`, `/strategic-planning:`, `/growth-strategy:`, `/agile-execution:`
- Improved discoverability and self-documentation
- Better IDE/CLI autocomplete support

**Documentation Updates**:
- [NAMESPACE-UPDATE-REPORT.md](./docs/NAMESPACE-UPDATE-REPORT.md) - Complete mapping of 157 namespace changes
- [VALIDATION-REPORT.md](./docs/VALIDATION-REPORT.md) - Architecture integrity verification (zero old namespace references)
- [RESTRUCTURE-COMPLETE.md](./docs/RESTRUCTURE-COMPLETE.md) - Full metrics and analysis
- Updated plugin READMEs for all 18 plugins
- [MIGRATION-GUIDE.md](./docs/MIGRATION-GUIDE.md) - Detailed migration instructions

### Changed

#### Architecture Improvements

**Plugin Consolidation**:
- 8 initial plugins consolidated into 18 final focused plugins
- Logical groupings based on PM disciplines and workflows
- Each plugin maintains single responsibility principle
- Perfect 1:1 plugin-to-agent ratio (zero agent duplication)

**Token Efficiency Gains**:
- 66% overall token reduction (58,092 → 19,650 lines across all plugins)
- 95% reduction in average per-plugin load
- 84% reduction in total agent size (18,000 → 2,800 lines across all agents)
- Individual agents optimized from 500-2,700 lines to 150-300 lines each
- Progressive disclosure: Templates moved to skills (loaded on-demand vs always loaded)

**Component Distribution**:
- Average of 5.7 components per plugin
- Balanced distribution across 18 plugins
- All 103 original components preserved and reorganized
- Zero functionality lost in restructure

#### Namespace Changes (Breaking)

**Old Format** (v1.0.0):
```
/ps:swot-analysis
/pd:interview-guide
/pg:growth-sprint
/pe:backlog-groomer
```

**New Format** (v2.0.0):
```
/strategic-planning:swot-analysis
/user-research:interview-guide
/growth-strategy:growth-sprint
/agile-execution:backlog-groomer
```

**Total Changes**: 157 command namespace references updated across all plugins

### Deprecated

**Old Plugins** (v1.0.0 architecture):
- `ps` (product-strategy) - Split into strategic-planning, competitive-analysis, platform-strategy, product-pricing
- `pd` (product-discovery) - Split into user-research, problem-discovery, design-thinking, jobs-framework
- `pg` (product-growth) - Split into growth-strategy, metrics-analytics, experimentation, go-to-market
- `pe` (product-execution) - Split into agile-execution, feature-management, technical-pm, stakeholder-management, customer-success, product-operations

These plugins remain available during the transition period but are deprecated and will be removed in a future release.

**Old Namespace Prefixes**:
- `/ps:*` commands - Use new plugin-specific namespaces instead
- `/pd:*` commands - Use new plugin-specific namespaces instead
- `/pg:*` commands - Use new plugin-specific namespaces instead
- `/pe:*` commands - Use new plugin-specific namespaces instead

### Removed

**Agent Duplication**:
- Removed 14+ duplicate agent definitions across plugins
- Each agent now appears in exactly one plugin
- Agent ownership clearly defined by plugin boundaries

**Redundant Context**:
- Templates moved from agent files to skills (progressive disclosure)
- Removed always-loaded heavy templates (500+ lines each in some agents)
- Context now loaded on-demand when frameworks mentioned

### Fixed

**Architecture Issues**:
- Plugin overlap and unclear boundaries resolved
- Agent ownership ambiguity eliminated (1:1 plugin-to-agent)
- Token waste from duplicate agents fixed
- Namespace conflicts and abbreviation confusion resolved

**Performance Issues**:
- High token consumption per plugin load (95% reduction achieved)
- Slow plugin loading times improved through token reduction
- Context bloat from always-loaded templates eliminated

### Security

No security-related changes in this release.

### Migration

**Required Actions**:
1. Update all command references to use new namespaces (see [MIGRATION-GUIDE.md](./docs/MIGRATION-GUIDE.md))
2. Review plugin install list (you may want fewer focused plugins vs all 4 large plugins)
3. Update any automation/scripts referencing old namespaces
4. Update documentation referencing old command paths

**Backward Compatibility**:
- Old plugins (ps, pd, pg, pe) remain available during transition
- All 103 components preserved with identical functionality
- No changes to component behavior or outputs
- Only namespace paths changed

**Benefits After Migration**:
- 66% less token usage overall
- 95% less context loaded per plugin
- Faster command execution
- Better autocomplete/discoverability
- Clearer plugin ownership and boundaries
- Industry-standard architecture

### Technical Details

**Metrics**:
- Total plugins: 4 → 18 (450% increase in modularity)
- Total components: 103 (unchanged, all preserved)
- Total lines of code: 58,092 → 19,650 (66% reduction)
- Average plugin size: 14,523 → 1,092 lines (95% reduction)
- Average agent size: 1,125 → 156 lines (84% reduction)
- Namespace updates: 157 command references updated
- Agent consolidation: 32 agent definitions → 18 unique agents

**Architecture Validation**:
- Zero old namespace references in new plugins (validated via grep)
- 1:1 plugin-to-agent ratio verified across all 18 plugins
- All 103 components accounted for and tested
- Plugin independence maintained (zero cross-plugin dependencies)

**Component Breakdown by Type**:
- 18 agents (1 per plugin, optimized 84%)
- 31 commands (preserved, namespace updates only)
- 12 tools (preserved, namespace updates only)
- 18 workflows (preserved, namespace updates only)
- 24 skills (preserved, now loaded progressively)

### References

- [MIGRATION-GUIDE.md](./docs/MIGRATION-GUIDE.md) - Complete migration instructions
- [NAMESPACE-UPDATE-REPORT.md](./docs/NAMESPACE-UPDATE-REPORT.md) - All 157 namespace changes
- [VALIDATION-REPORT.md](./docs/VALIDATION-REPORT.md) - Architecture integrity verification
- [RESTRUCTURE-COMPLETE.md](./docs/RESTRUCTURE-COMPLETE.md) - Full restructure metrics and analysis

## [1.0.0] - 2025-10-18

### Added

#### Plugin Architecture (4 Specialized Plugins - 103 Items Total)

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
- **Total Items**: 103 (18 agents, 31 commands, 12 tools, 18 workflows, 24 skills)
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

[2.0.0]: https://github.com/slgoodrich/agents/releases/tag/v2.0.0
[1.0.0]: https://github.com/slgoodrich/agents/releases/tag/v1.0.0
