# Tech Stack

**Last Updated:** 2025-10-30

## Stack

- **Languages:** Markdown, YAML, JSON (configuration-as-code)
- **Frontend:** N/A (Documentation and knowledge management)
- **Backend:** N/A (Claude Code plugin system)
- **Database:** None (Filesystem-based context storage)
- **Infrastructure:**
  - GitHub (version control, issue tracking, collaboration)
  - Claude Code Plugin System (runtime environment)

## Architecture

**Plugin Type:** Claude Code Agent Plugin with Knowledge Skills

**Core Components:**
- **9 Agent Files** (.md with YAML frontmatter)
  - 1 orchestration agent (product-manager)
  - 7 PM specialist agents (model: sonnet)
  - 1 utility agent (context-scanner, model: haiku)
- **16 Knowledge Skills** (progressive disclosure framework)
  - Each skill: SKILL.md + assets/ + references/
  - Categories: research, strategy, execution, launch
- **1 Command** (pm-setup wizard for context initialization)
- **Context System** (.claude/product-context/ - 8+ reusable files)

**Architecture Pattern:**
```
Orchestrator Pattern:
  User Request → product-manager (routing logic) → Specialist Agent → Skill (on-demand)

Progressive Context System:
  pm-setup command → Context files → All agents read before processing

Skill Progressive Disclosure:
  Agent invocation → Load only needed skills → Token-efficient operation
```

**File Structure:**
```
.claude-plugin/
├── plugin.json           # Core plugin metadata (name, version, category)
└── marketplace.json      # Marketplace registration (agents, skills, commands arrays)

plugins/ai-pm-copilot/
├── agents/               # 9 .md files with YAML frontmatter
│   ├── product-manager.md       (orchestrator)
│   ├── market-analyst.md        (specialist, sonnet)
│   ├── research-ops.md          (specialist, sonnet)
│   ├── product-strategist.md   (specialist, sonnet)
│   ├── roadmap-builder.md      (specialist, sonnet)
│   ├── feature-prioritizer.md  (specialist, sonnet)
│   ├── requirements-engineer.md (specialist, sonnet)
│   ├── launch-planner.md       (specialist, sonnet)
│   └── context-scanner.md      (utility, haiku)
├── commands/             # 1 .md command file
│   └── pm-setup.md
└── skills/               # 16 skill directories
    └── [skill-name]/
        ├── SKILL.md       # Main skill content
        ├── assets/        # Templates, frameworks
        └── references/    # Guides, best practices

.claude/product-context/  # Context storage (created by pm-setup)
├── product-info.md
├── business-metrics.md
├── strategic-goals.md
├── current-roadmap.md
├── tech-stack.md
├── customer-segments.md
├── team-info.md
├── competitive-landscape.md
└── current-features.md   # (created by context-scanner)

prds/                     # PRD storage (created by requirements-engineer)
└── [feature-name].md     # Kebab-case naming, no PRD- prefix
```

## Development Tools

**Configuration Management:**
- JSON configuration files (plugin.json, marketplace.json)
- YAML frontmatter for agent/skill metadata
- Git for version control

**Quality Assurance:**
- TEST_PLAN.md: Comprehensive test suite (8 categories, 60+ tests)
- Manual verification checklist for Claude Code integration
- Bash-based validation scripts (JSON validation, component counting, content quality checks)

**Testing Infrastructure:**
- Configuration validation (jq for JSON parsing)
- Component count verification (9 agents, 16 skills, 1 command)
- Content quality tests (no stakeholder references, solo dev focus)
- Frontmatter validation (required fields, model specifications)
- Cross-reference validation (skills referenced by agents, no orphaned files)

**Development Workflow:**
- GitHub Issues with templates (bug reports, feature requests, agent proposals)
- CODE_OF_CONDUCT.md and CONTRIBUTING.md for community standards
- Pre-commit checklist in CLAUDE.md

## Technical Constraints

**Hardcoded Component Counts** (verified before commits):
- Agents: 9 (1 orchestrator + 7 specialists + 1 utility)
- Skills: 16 (each must have SKILL.md + assets/ + references/)
- Commands: 1 (pm-setup only)
- All counts hardcoded in tests and documentation

**Required Frontmatter:**
- **PM Specialist Agents:** `model: sonnet` (expert-level reasoning)
- **Utility Agents:** `model: haiku` (efficient operations)
- **Agent frontmatter:** name, description, model
- **Skill frontmatter:** name, description, category

**Configuration Requirements:**
- plugin.json and marketplace.json versions must match (currently 1.0.0)
- All config files must be valid JSON
- All relative paths use `./` notation from plugin root
- Paths in marketplace.json must reference existing files

**Content Requirements:**
- Target: solo developers and small teams (1-10 people)
- No "stakeholder" references or enterprise jargon
- All skills must be referenced by at least one agent (no orphaned skills)
- All files in assets/ and references/ must be listed in parent SKILL.md (no dead files)

**Context System:**
- All 9 agents read `.claude/product-context/` files before processing
- Context gathered once via `/pm-setup` command (5-20 min: 5-10 min with codebase scanning, 15-20 min manual)
- context-scanner utility agent auto-discovers features, tech stack, integrations from existing codebases
- Reduces questions by ~80%, enables product-specific outputs
- Annual time savings: 50-70 hours for active users

**Plugin System Constraints:**
- No runtime code execution (pure configuration/documentation)
- No external dependencies (self-contained plugin)
- Markdown-only content delivery
- Filesystem-based context persistence

## Performance Characteristics

**Context-Aware Efficiency:**
- Progressive context loading (read only what's needed)
- One-time context gathering, infinite reuse
- 80% reduction in agent questions when context exists

**Parallel Execution Capabilities:**
- market-analyst: Spawns parallel sub-agents for 3+ competitors (60-70% time savings)
- research-ops: Spawns parallel sub-agents for 5+ interviews (60-70% time savings)
- Graceful degradation to sequential mode when needed

**Token Efficiency:**
- Skills load on-demand only (progressive disclosure)
- Context files external to prompts (reusable, not embedded)
- Utility agent uses haiku model for scanning operations

## Discovered Information

**Evidence:**
- Configuration analysis: .claude-plugin/plugin.json, .claude-plugin/marketplace.json
- Component counting: 9 agents, 16 skills, 1 command
- Directory structure scan: plugins/ai-pm-copilot/
- Test infrastructure: TEST_PLAN.md with 60+ automated tests
- GitHub integration: Issue templates, CODE_OF_CONDUCT.md, CONTRIBUTING.md

**Auto-discovered:** 2025-10-30
**Last validated:** 2025-10-30
