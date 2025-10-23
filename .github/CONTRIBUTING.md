# Contributing to Product Management Toolkit

Thank you for considering contributing to the Product Management Toolkit for Claude Code! This toolkit has 18 specialized plugins with perfect 1:1 plugin-to-agent architecture, and it grows with the PM community.

## Plugin Architecture Overview

The toolkit is organized into **18 focused plugins** with a 1:1 plugin-to-agent architecture. Each plugin has exactly one expert agent plus supporting commands, tools, workflows, and skills.

### The 18 Focused Plugins

1. **competitive-intelligence**: Market analysis, positioning, SWOT, competitive strategy
2. **business-models**: Business model design, pricing, monetization
3. **strategic-planning**: Product strategy, vision, roadmaps, OKRs
4. **platform-strategy**: Platform ecosystems, multi-sided markets
5. **user-research**: User interviews, surveys, usability testing, JTBD
6. **continuous-discovery**: Opportunity mapping, assumption testing, design thinking
7. **customer-insights**: Customer feedback synthesis, personas, journey mapping
8. **growth-strategy**: Growth loops, scaling, PMF assessment
9. **product-analytics**: Metrics, experiments, A/B testing, data science
10. **gtm-strategy**: Go-to-market planning, product launches
11. **agile-coaching**: Scrum, Kanban, sprint planning, backlog management
12. **feature-prioritization**: RICE/ICE scoring, trade-off analysis
13. **requirements-engineering**: PRDs, technical specs, user stories
14. **stakeholder-management**: Alignment, communication, decision-making
15. **api-product-management**: API products, developer experience
16. **product-operations**: PM process optimization, tools, templates
17. **customer-success**: Onboarding, retention, expansion
18. **technical-pm**: Technical architecture, technical debt management

### Plugin Structure Standard

Each plugin follows this directory structure:

```
plugins/plugin-name/
├── agents/
│   └── agent-name.md           (exactly 1 agent per plugin)
├── commands/
│   └── command-name.md         (0+ commands)
├── tools/
│   └── tool-name.md            (0+ tools - registered as commands)
├── workflows/
│   └── workflow-name.md        (0+ workflows - registered as commands)
└── skills/
    └── skill-name/
        └── SKILL.md            (0+ skills)
```

**Key Principles:**
- **1:1 Architecture**: Each plugin has exactly ONE agent (no duplicates, no sharing)
- **Focused Purpose**: Each plugin addresses a specific PM discipline
- **Component Organization**: Supporting components (commands/tools/workflows/skills) organized by type
- **Zero Dependencies**: Plugins work completely standalone

When contributing, choose the plugin that best fits your contribution's purpose.

---

## How to Contribute

### Ways to Contribute

1. **Report Bugs or Request Features**
   - Open an issue on GitHub
   - Use clear, descriptive titles
   - Include reproduction steps for bugs
   - Explain the use case for feature requests

2. **Add Components to Existing Plugins**
   - Add commands, tools, workflows, or skills to one of the 18 plugins
   - Follow the appropriate template structure (see below)
   - Include clear usage instructions
   - Provide examples and edge cases

3. **Propose New Plugins**
   - Only if addressing a distinct PM discipline not covered by existing 18 plugins
   - Must include exactly 1 agent + supporting components
   - Open an issue first to discuss fit and architecture
   - See "When to Create a New Plugin" section below

4. **Improve Documentation**
   - Fix typos or unclear explanations
   - Add usage examples
   - Expand best practices
   - Create tutorials

5. **Optimize Existing Components**
   - Reduce token count while maintaining clarity
   - Improve template structures
   - Enhance examples and practical guidance

## Contribution Guidelines

### Naming Conventions

- **Lowercase, hyphen-separated**: `user-researcher.md`, `feature-prioritizer.md`
- **Descriptive names**: Name should clearly indicate purpose
- **Consistent patterns**: Follow existing naming in the repository
- **Plugin namespaces**: Use full plugin names (e.g., `/user-research:interview-guide`, not `/ur:interview-guide`)

### Component Templates

#### Agent Template Structure (150-300 lines)

```markdown
---
name: agent-name
description: One-line description of expertise and when to use
model: sonnet
---

# Agent Name

## Purpose
Clear statement of the agent's role and expertise (2-3 sentences).

## Core Philosophy
3-7 guiding principles as bold headers with 1-sentence explanations.

## Capabilities
Detailed breakdown organized by category, using bulleted lists.

## Response Approach
Instructions for context gathering before providing recommendations.

IMPORTANT: Always gather context BEFORE providing recommendations.

Ask the user for necessary context:
- Current product state
- Market context
- Strategic goals
- Constraints and challenges

## Activation
When to invoke related skills for detailed templates/frameworks.

## Integration with Other Agents
Cross-references to related agents in other plugins.

## When to Use This Agent

✅ **Use feature-prioritizer for:**
- Scoring features with RICE/ICE frameworks
- Building prioritized roadmaps
- Trade-off decisions between competing features
- Backlog ranking and cleanup
- Stakeholder alignment on priorities

❌ **Don't use for:**
- Creating PRDs (use requirements-engineer)
- Strategic vision setting (use product-strategist)
- Primary user research (use user-researcher)

## Example Interactions (Optional)
Brief examples showing the agent in action.
```

**Key Requirements:**
- Must have frontmatter with `name`, `description`, and `model: sonnet`
- Always include context-gathering instructions
- Keep concise (150-300 lines) - extract details to skills
- Reference skills for progressive disclosure
- One agent addresses one PM discipline

#### Command Template Structure (200-600 lines)

```markdown
# Command Name

One-line description of what this command does.

## Usage

```
/plugin-name:command-name [parameters]
```

**Arguments:** $ARGUMENTS

## What This Command Does

Numbered list of outputs and behaviors:
1. First key output
2. Second key output
3. Third key output

## Instructions

Step-by-step guide for command execution:
1. Gather context (ask specific questions)
2. Process information
3. Generate output using template
4. Provide actionable next steps

## Template

```markdown
[Structured template for output format]
```

## Best Practices

✅ **DO**:
- Ask for specific context upfront (product stage, target users, business goals)
- Include concrete example inputs showing expected detail level
- Specify time savings (e.g., "Takes 30 minutes vs 2 hours of manual work")
- Use structured templates for consistent outputs
- Make requirements testable and measurable
- Reference other components that work together

❌ **DON'T**:
- Accept vague inputs without gathering context
- Create generic templates without real-world examples
- Skip the "why" behind decisions
- Make assumptions about user's situation
- Duplicate content that exists in skills (progressive disclosure)

## Examples

### Example 1: Feature Request Command
**Input:** `/requirements-engineering:prd "Dark mode for mobile app"`

**Expected Context Gathering:**
- What's the business goal? (retention, user satisfaction)
- Who are target users? (all 100K mobile users)
- What research supports this? (500+ votes, 60% report eye strain)
- Technical constraints? (React Native, theming approach)
- MVP vs full vision? (basic dark theme vs custom colors)

**Output:** Full PRD with problem statement, success metrics, requirements, rollout plan

### Example 2: Research Planning Command
**Input:** `/user-research:interview-guide "Why sales managers abandon trial onboarding"`

**Expected Context Gathering:**
- Research phase? (discovery vs validation)
- Participants? (churned trial users)
- Sample size? (12-15 interviews)
- Duration? (45 minutes)
- Hypotheses? (too complex, unclear value, integration blocker)

**Output:** Structured interview guide with screening, question flows, follow-up probes

## Related Components
- Commands: /plugin-name:related-command
- Agents: agent-name (plugin-name)
- Skills: skill-name
```

**Key Requirements:**
- No frontmatter (commands are pure markdown)
- Start with H1 heading
- Include usage syntax with full namespace
- Provide structured template for output
- Include examples and best practices

#### Tool Template Structure (50-150 lines, lightweight)

```markdown
---
name: tool-name
description: One-line description of what this tool does
model: haiku
---

# Tool Name

## What This Tool Does

2-3 sentence overview of the tool's purpose and output.

## Instructions

1. Ask for required inputs (minimal context gathering)
2. Apply framework/methodology
3. Generate structured output
4. Provide interpretation guidance

## Output Format

```markdown
[Structured template - usually a table or framework canvas]
```

## Example

**Scenario:** Launching our PM SaaS in enterprise market. Currently successful in SMB market, looking to move upmarket. Timeframe: Next 12 months.

**Output:** Complete SWOT analysis with:
- **Strengths**: Product-market fit in SMB, $2M ARR, 95% retention
- **Weaknesses**: No enterprise features, small sales team, limited compliance
- **Opportunities**: $50M enterprise TAM, growing demand, weak competitors
- **Threats**: Microsoft/Salesforce entering space, compliance requirements
- **SO Strategy**: Leverage SMB success stories to win enterprise pilots
- **WO Strategy**: Build enterprise features, hire enterprise sales leader
- **Top Actions**: (1) SOC2 compliance in Q1, (2) Enterprise tier by Q2, (3) Hire VP Enterprise Sales

## Tips

✅ **DO**: Be specific (use data, quantify), be honest (acknowledge weaknesses), prioritize (top 3 items), link to actions

❌ **DON'T**: Make lists too long, confuse internal/external factors, use wishful thinking vs realistic assessment, ignore interdependencies

**Related Tools**: `/competitive-intelligence:competitive-positioning`, `/continuous-discovery:assumption-mapping`
```

**Key Requirements:**
- Must have frontmatter with `name`, `description`, and `model: haiku` (default)
- Lightweight and fast (framework applications)
- Users can override with `--model sonnet` if needed
- Registered in marketplace.json as a command (not separate "tools" array)

#### Workflow Template Structure (300-800 lines)

```markdown
---
name: workflow-name
description: One-line description of this multi-week process
model: sonnet
duration: 2-4 weeks
---

# Workflow Name

## Overview
2-3 paragraph explanation of the workflow's purpose and outcomes.

## Timeline
**Duration:** X weeks
**Commitment:** Y hours/week

## Prerequisites
- Required context
- Preparation steps
- Stakeholders needed

## Phases

### Week 1: Problem Framing & Research
**Goal:** Validate the problem exists and understand user pain points

**Activities:**
1. Define problem statement (invoke `user-researcher` agent)
2. Create interview guide: `/user-research:interview-guide "Problem discovery for [problem]"`
3. Conduct 5-8 user interviews
4. Synthesize findings: `/user-research:research-synthesize [interview notes]`

**Outputs:**
- Problem brief with validated hypotheses
- Research synthesis showing pain point patterns
- Target user personas

### Week 2: Solution Ideation & Validation
**Goal:** Explore solutions and validate with users

**Activities:**
1. Brainstorm solutions (invoke `product-strategist` agent)
2. Create solution concepts: `/requirements-engineering:prd [feature concept]`
3. Run solution validation interviews
4. Prioritize approaches: `/feature-prioritization:quick-prioritize`

**Outputs:**
- 3-5 solution concepts evaluated
- User validation findings
- Recommended approach with rationale

## Success Criteria
How to know the workflow succeeded:
- Problem validated with 8+ user interviews showing consistent pain points
- Solution concept tested with 5+ users showing 80%+ positive response
- Clear recommendation with confidence level and supporting evidence
- Stakeholder alignment on next steps (build/iterate/pivot)

## Risks and Mitigations

**Risk:** Can't recruit enough participants (need 10-15 users)
**Mitigation:** Start recruitment early, offer incentives, use multiple channels (email, support tickets, LinkedIn)

**Risk:** Research reveals problem isn't significant
**Mitigation:** Accept findings, pivot to different opportunity, document learnings

**Risk:** Timeline slips due to scheduling conflicts
**Mitigation:** Schedule interviews in advance, have backup participants, compress synthesis phase if needed

## Completion Checklist
- [ ] 8+ user interviews completed and recorded
- [ ] Research synthesis document finalized
- [ ] Solution concepts created and evaluated
- [ ] Validation interviews completed (5+ users)
- [ ] Final recommendation presented to stakeholders
- [ ] Decision made: build/iterate/pivot

## Related Components
- Agents: `user-researcher`, `product-strategist`, `requirements-engineer`, `feature-prioritizer`
- Commands: `/user-research:interview-guide`, `/user-research:research-synthesize`, `/requirements-engineering:prd`, `/feature-prioritization:quick-prioritize`
- Skills: `continuous-discovery`, `user-research-techniques`, `prioritization-methods`
```

**Key Requirements:**
- Must have frontmatter with `name`, `description`, `model: sonnet`, and `duration`
- Explicit phases with clear timeline
- Specify which agents/commands to invoke in each phase
- Include success criteria and completion checklist
- Registered in marketplace.json as a command (not separate "workflows" array)

#### Skill Template Structure (200-400 lines)

```markdown
---
name: skill-name
description: When to use this skill and what it provides
---

# Skill Name

## Overview
2-3 paragraph introduction to the framework/methodology.
Include origin (e.g., "Teresa Torres' Continuous Discovery Habits").

## When to Use This Skill
Specific scenarios where this knowledge applies:
- Choosing between competing features
- Building quarterly roadmaps
- Backlog prioritization
- Saying "no" with evidence
- Stakeholder alignment on priorities

## Core Frameworks

### Framework 1: RICE Scoring (Intercom)

**Formula**: (Reach × Impact × Confidence) / Effort

**Components**:
- **Reach**: How many users per time period (e.g., per quarter)
- **Impact**: 0.25 (minimal), 0.5 (low), 1 (medium), 2 (high), 3 (massive)
- **Confidence**: 100% (high data), 80% (medium), 50% (low data)
- **Effort**: Person-months to build

**When to Use**: Large backlog needs ranking, data-driven culture, quantifiable reach

**Pros**: Objective, forces estimation, scales well
**Cons**: Requires data, effort estimation can be inaccurate

### Framework 2: ICE Scoring (Sean Ellis)

**Formula**: (Impact + Confidence + Ease) / 3

**Components** (each scored 1-10):
- **Impact**: How much will this move the needle?
- **Confidence**: How sure are we it will work?
- **Ease**: How simple is it to implement?

**When to Use**: Early-stage products, growth experiments, quick prioritization

**Pros**: Simple, fast, intuitive
**Cons**: Subjective, harder to defend

## Practical Application

### Step-by-Step Process
1. **Gather features to prioritize**: Collect backlog items, ideas, requests
2. **Choose framework**: RICE for data-driven, ICE for speed, Value vs Effort for visual
3. **Score each feature**: Use consistent rubric across team
4. **Calculate scores**: Apply formula or plot on matrix
5. **Prioritize roadmap**: Rank by score, allocate capacity
6. **Communicate decisions**: Share rationale with stakeholders

### Template

```markdown
## Feature Prioritization: [Quarter/Initiative]

### Framework: RICE

| Feature | Reach | Impact | Confidence | Effort | RICE Score | Priority |
|---------|-------|--------|------------|--------|------------|----------|
| Dark Mode | 10,000 | 2 | 80% | 1.5 | 10,667 | High |
| Export CSV | 2,000 | 1 | 100% | 0.5 | 4,000 | Medium |

### Decisions
- **Build Now**: Dark Mode (score 10,667), Export CSV (4,000)
- **Defer**: Advanced analytics (low confidence)
- **Won't Build**: Custom themes (low reach)
```

## Key Metrics/Success Indicators
How to measure effectiveness:
- **Roadmap velocity**: Features shipped on time
- **Business impact**: Metrics improved by prioritized features
- **Team alignment**: Reduced debate on priority decisions
- **Stakeholder satisfaction**: Fewer escalations on priorities

## Examples

### Example 1: SaaS Product Backlog Prioritization

**Scenario**: 50 feature requests, 3-person eng team, need Q1 roadmap

**Process**:
1. Scored all 50 features using RICE
2. Top 10 scores: 15,000 to 5,000 range
3. Bottom 40 scores: <1,000
4. Capacity: 9 person-months in Q1
5. Selected top 6 features totaling 8.5 person-months

**Result**: Clear roadmap, stakeholder buy-in, 15% increase in retention from prioritized features

## Common Pitfalls

**Prioritization Mistakes**:
- **HIPPO prioritization**: Don't prioritize by Highest Paid Person's Opinion - use frameworks
- **Ignoring effort**: Value alone is insufficient - must consider implementation cost
- **Set-and-forget**: Re-prioritize regularly as context changes
- **Gaming the system**: Use honest scoring, don't inflate numbers to favor pet features

**Experiment Design Mistakes**:
- **Peeking**: Checking results too early invalidates statistical significance
- **Multiple comparisons**: Testing too many variants inflates false positives
- **Novelty effect**: Initial excitement creates bias in early results
- **Simpson's paradox**: Overall trends can reverse in specific segments

**Framework Application Mistakes**:
- **Wrong framework for context**: RICE needs data, don't use if you have none
- **Missing "why not"**: Document why features were rejected, not just selected
- **No stakeholder buy-in**: Show your work, explain trade-offs transparently

## Further Reading
- **Teresa Torres** - "Continuous Discovery Habits" (opportunity solution trees, assumption testing)
- **Marty Cagan** - "Empowered", "Inspired" (product teams, product leadership)
- **April Dunford** - "Obviously Awesome" (positioning and differentiation)
- **Sean Ellis** - "Hacking Growth" (ICE framework, growth strategies)
- **Jeff Patton** - "User Story Mapping" (story maps, outcome-driven planning)
- **Intercom** - RICE Prioritization framework
- **Google** - HEART Framework, OKR methodology
- **Basecamp** - Shape Up methodology
```

**Key Requirements:**
- Must have frontmatter with `name` and `description`
- Located in `skills/skill-name/SKILL.md` (subdirectory + SKILL.md file)
- Referenced by agents for progressive disclosure
- Include detailed templates and examples
- Credit framework creators (Teresa Torres, Marty Cagan, etc.)

### Frontmatter Requirements Summary

**Components WITH frontmatter (YAML):**
- **Agents**: `name`, `description`, `model: sonnet` (always)
- **Tools**: `name`, `description`, `model: haiku` (default, user-overridable)
- **Workflows**: `name`, `description`, `model: sonnet`, `duration: X weeks`
- **Skills**: `name`, `description`

**Components WITHOUT frontmatter:**
- **Commands**: Pure markdown starting with `# Command Name`

This distinction is critical for proper component registration and behavior.

## Quality Standards

### Content Requirements

1. **Comprehensive**: Cover the topic thoroughly within token budget
2. **Practical**: Include real-world PM examples
3. **Actionable**: Provide clear next steps and templates
4. **Well-structured**: Use clear headings and organization
5. **Accurate**: Ensure technical accuracy and cite framework sources
6. **Token-efficient**: Focus on essential information, avoid redundancy

### Writing Style

- **Clear and concise**: Avoid jargon unless standard PM terminology
- **Professional**: Maintain helpful, expert tone
- **Scannable**: Use headings, lists, and formatting
- **Example-driven**: Show, don't just tell
- **Context-aware**: Gather context before providing recommendations

### Token Efficiency Patterns

1. **Skills on demand**: Extract detailed templates/examples to skills (loaded when mentioned)
2. **Focused agents**: Single responsibility per agent (150-300 lines)
3. **Haiku for tools**: Framework tools default to Haiku (20x cheaper, faster)
4. **Workflow orchestration**: Break complex processes into phases
5. **Explicit context gathering**: Ask structured questions upfront

### Namespace Conventions

Use full plugin names in all references:

**Correct:**
```markdown
- /user-research:interview-guide
- /strategic-planning:okr-framework
- /competitive-intelligence:swot-analysis
```

**Incorrect (old style - do not use):**
```markdown
- /pd:interview-guide
- /ps:okr-framework
- /ps:swot-analysis
```

## When to Create a New Plugin vs Adding to Existing

### Add to Existing Plugin When:
- The component naturally belongs to one of the 18 existing PM disciplines
- It extends or enhances an existing agent's expertise
- It's a new tool, workflow, or skill for an established area
- Example: Adding a "prototype testing guide" to user-research plugin

### Create New Plugin When:
- Addressing a completely distinct PM discipline not covered by existing 18 plugins
- The new area requires its own dedicated agent with unique expertise
- Cannot reasonably fit within any existing plugin's scope
- Example: A hypothetical "product-compliance" plugin for regulatory/legal PM work

**Important:** Creating a new plugin requires:
1. Opening an issue first to discuss fit and necessity
2. Creating exactly 1 agent for the new discipline
3. Adding supporting components (commands/tools/workflows/skills)
4. Updating `.claude-plugin/marketplace-v2-final.json`
5. Following the standard plugin directory structure

**Note:** The current 18 plugins cover the comprehensive PM lifecycle. Most contributions should enhance existing plugins rather than create new ones.

## Submission Process

### Step 1: Fork and Clone

```bash
git clone https://github.com/slgoodrich/agents.git
cd agents
```

### Step 2: Create a Branch

```bash
git checkout -b feature/your-contribution-name
```

### Step 3: Make Changes

#### For Adding Components to Existing Plugins:

1. **Identify the right plugin** from the 18 focused plugins listed above
2. **Create the component file** in the appropriate directory:
   - Agent: `plugins/plugin-name/agents/`
   - Command: `plugins/plugin-name/commands/`
   - Tool: `plugins/plugin-name/tools/`
   - Workflow: `plugins/plugin-name/workflows/`
   - Skill: `plugins/plugin-name/skills/skill-name/SKILL.md`

3. **Follow the appropriate template** (see Component Templates section)

4. **Register in marketplace-v2-final.json**:
   ```json
   {
     "plugins": [
       {
         "name": "plugin-name",
         "agents": ["./agents/agent-name.md"],
         "commands": [
           "./commands/existing-command.md",
           "./commands/your-new-command.md",    // if command
           "./tools/your-new-tool.md",          // if tool
           "./workflows/your-new-workflow.md"   // if workflow
         ],
         "skills": [
           "./skills/existing-skill/SKILL.md",
           "./skills/your-new-skill/SKILL.md"   // if skill
         ]
       }
     ]
   }
   ```

   **Important:** Tools and workflows are registered in the `commands` array, NOT separate arrays.

5. **Test your contribution**:
   - Verify frontmatter syntax (if applicable)
   - Check file paths are correct
   - Ensure namespace references use full plugin names
   - Test with realistic PM scenarios

#### For Creating New Plugins (Rare):

1. **Open an issue first** to discuss the new plugin's necessity and scope
2. **Create plugin directory structure**:
   ```bash
   mkdir -p "plugins/new-plugin-name"/{agents,commands,tools,workflows,skills}
   ```
3. **Create the agent** (exactly 1 per plugin) in `agents/`
4. **Add supporting components** as needed
5. **Register in marketplace-v2-final.json** with all required fields
6. **Document the new plugin** in this CONTRIBUTING.md (update the 18 plugins list)

### Step 4: Commit Changes

```bash
git add .
git commit -m "Add [component-type] to [plugin-name]: descriptive-name"
```

Examples:
- `git commit -m "Add command to user-research: usability-test-planner"`
- `git commit -m "Add skill to strategic-planning: okr-methodology"`
- `git commit -m "Add workflow to gtm-strategy: product-launch"`

### Step 5: Push and Create PR

```bash
git push origin feature/your-contribution-name
```

Then open a Pull Request on GitHub with:
- **Clear title** describing the contribution
- **Summary** of what you're adding and to which plugin
- **Why it's valuable** for PMs
- **Testing** or validation you've done
- **Checklist**:
  - [ ] Followed appropriate template structure
  - [ ] Added correct frontmatter (if applicable)
  - [ ] Registered in marketplace-v2-final.json
  - [ ] Used full plugin namespace in references
  - [ ] Followed naming conventions (lowercase-hyphenated)
  - [ ] Included examples and best practices
  - [ ] Tested with realistic scenarios

## Validation Checklist

Before submitting, verify:

### File Structure
- [ ] Component placed in correct plugin directory
- [ ] File uses lowercase-hyphenated naming
- [ ] Skills follow `skill-name/SKILL.md` structure
- [ ] No duplicate agents (only 1 agent per plugin)

### Content Quality
- [ ] Follows appropriate template structure
- [ ] Includes practical examples
- [ ] Provides actionable guidance
- [ ] References PM frameworks/creators appropriately
- [ ] Token-efficient (no unnecessary verbosity)

### Technical Requirements
- [ ] Correct frontmatter (or none for commands)
- [ ] Registered in marketplace-v2-final.json
- [ ] Uses full plugin namespaces (not abbreviations)
- [ ] Valid JSON syntax in marketplace file
- [ ] File paths use correct directory structure

### Testing
- [ ] Read through the component as if you were Claude Code
- [ ] Verify instructions are clear and unambiguous
- [ ] Test with at least one realistic PM scenario
- [ ] Check cross-references to other components work

## Code of Conduct

### Our Standards

- **Be respectful**: Treat all contributors with respect
- **Be collaborative**: Work together constructively
- **Be inclusive**: Welcome diverse perspectives
- **Be patient**: Help newcomers learn
- **Be professional**: Keep discussions focused and productive

### Unacceptable Behavior

- Harassment or discriminatory comments
- Personal attacks or trolling
- Spam or off-topic contributions
- Plagiarism or uncredited work
- Violating the spirit of token efficiency (bloated contributions)

## Questions?

- **General questions**: Open a GitHub Discussion
- **Bugs or issues**: Create a GitHub Issue
- **Contribution ideas**: Start with an Issue to discuss
- **Architecture questions**: Reference CLAUDE.md and RESTRUCTURE-COMPLETE.md

## Recognition

All contributors will be acknowledged in:
- CHANGELOG.md for each release
- GitHub contributors list
- Special mentions for significant contributions

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

## Additional Resources

### Key Documentation Files

- **CLAUDE.md**: Complete architecture guidance and patterns
- **RESTRUCTURE-COMPLETE.md**: Details on the v2 architecture transformation
- **.claude-plugin/marketplace-v2-final.json**: Plugin registry configuration
- **MIGRATION-GUIDE.md**: Guide for users migrating from v1 to v2

### PM Frameworks Referenced

When creating agents/skills, reference these frameworks by name for credibility and skill activation:

- **Teresa Torres** - Continuous Discovery Habits, Opportunity Solution Trees
- **Marty Cagan** - Empowered, Inspired, Product Leadership
- **April Dunford** - Obviously Awesome (positioning)
- **Sean Ellis** - Hacking Growth, ICE prioritization
- **Jeff Patton** - User Story Mapping
- **Intercom** - RICE Prioritization
- **Google** - HEART Framework, OKRs
- **Basecamp** - Shape Up
- **Strategyzer** - Business Model Canvas, Value Proposition Canvas

Mentioning these names/frameworks in agent prompts triggers skill activation.

### Example Plugin Structures

**Small Plugin (2-3 components):**
```
plugins/customer-success/
├── agents/
│   └── customer-success.md
├── commands/
├── tools/
├── workflows/
│   └── crisis-management.md
└── skills/
```

**Medium Plugin (5-7 components):**
```
plugins/user-research/
├── agents/
│   └── user-researcher.md
├── commands/
│   ├── interview-guide.md
│   ├── research-synthesizer.md
│   ├── survey-builder.md
│   └── usability-test-planner.md
├── tools/
├── workflows/
│   └── solution-validation.md
└── skills/
    ├── jobs-to-be-done/
    │   └── SKILL.md
    └── user-research-techniques/
        └── SKILL.md
```

**Large Plugin (8+ components):**
```
plugins/strategic-planning/
├── agents/
│   └── product-strategist.md
├── commands/
│   ├── executive-summary.md
│   ├── okr-framework.md
│   ├── risk-assessment.md
│   ├── roadmap-builder.md
│   └── scenario-planner.md
├── tools/
│   └── now-next-later-roadmap.md
├── workflows/
│   ├── annual-planning.md
│   ├── product-pivot.md
│   └── quarterly-planning.md
└── skills/
    ├── okr-methodology/
    │   └── SKILL.md
    ├── product-strategy-frameworks/
    │   └── SKILL.md
    └── vision-mission-strategy/
        └── SKILL.md
```

---

Thank you for helping make the Product Management Toolkit better for the entire PM community! Your contributions help thousands of PMs work more effectively with Claude Code.
