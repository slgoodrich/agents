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

## Available Skills (16 Total)

The ai-pm-copilot plugin includes 16 specialized skills organized into four core PM domains. Each skill contains frameworks, templates, and best practices that agents load on-demand.

### User Research & Discovery (5 skills)

**Used by**: research-ops agent

1. **user-research-techniques** - Comprehensive research methods: interviews, surveys, usability testing, Jobs-to-be-Done
   - 63+ assets including interview scripts, research plans, synthesis templates
   - 37+ reference guides covering best practices and methodologies

2. **interview-frameworks** - Interview design, questioning techniques, and synthesis
   - Assets: Interview scripts, discussion guides, synthesis templates, question banks

3. **synthesis-frameworks** - Affinity mapping, insight generation, research analysis
   - Assets: Synthesis templates, insight frameworks, theme identification guides

4. **usability-frameworks** - Usability testing, task analysis, Nielsen principles
   - Assets: Test plans, observation guides, findings templates

5. **validation-frameworks** - Problem/solution validation, MVP testing, hypothesis testing
   - Assets: Validation templates, testing protocols, success criteria frameworks

### Strategy & Positioning (4 skills)

**Used by**: product-strategist, market-analyst agents

6. **product-positioning** - April Dunford's positioning framework, market category definition
   - Assets: Positioning canvas, messaging frameworks, differentiation templates
   - Used by 6 different agent workflows (most referenced skill)

7. **competitive-analysis-templates** - SWOT, Porter's Five Forces, competitive matrices
   - Assets: Analysis templates, comparison frameworks, market assessment tools

8. **market-sizing-frameworks** - TAM/SAM/SOM calculation, market opportunity assessment
   - Assets: Sizing templates, calculation frameworks, opportunity maps

9. **product-market-fit** - Sean Ellis test, PMF indicators, validation approaches
   - Assets: PMF scorecards, validation frameworks, measurement templates

### Product Execution (5 skills)

**Used by**: requirements-engineer, roadmap-builder, feature-prioritizer agents

10. **roadmap-frameworks** - Now-Next-Later, theme-based, outcome-based roadmaps
    - Assets: Roadmap templates, visualization formats, communication frameworks

11. **prioritization-methods** - RICE, ICE, MoSCoW, Kano, Value vs Effort, Cost of Delay
    - Assets: Scoring templates, decision matrices, comparison frameworks

12. **specification-techniques** - Requirements writing, clarity, completeness
    - Assets: Specification templates, quality checklists, review frameworks

13. **prd-templates** - Product Requirements Document templates and best practices
    - Assets: PRD templates, section guides, review checklists

14. **user-story-templates** - User story formats, acceptance criteria, INVEST principles
    - Assets: Story templates, refinement guides, estimation frameworks

### Launch & GTM (2 skills)

**Used by**: launch-planner agent

15. **go-to-market-playbooks** - Product-led growth, sales-led growth, launch strategies
    - Assets: GTM templates, channel frameworks, launch checklists

16. **launch-planning-frameworks** - Launch tiers, messaging, coordination frameworks
    - Assets: Launch plans, timeline templates, readiness checklists

---

## Skill Composability

### Multi-Skill Scenarios

Agents can load multiple skills for complex tasks:

**Example: Complete Feature Prioritization**

```
User: "Prioritize these features considering effort,
business value, and strategic fit"

feature-prioritizer agent:
1. Loads prioritization-methods skill (RICE/ICE/Kano)
2. Loads roadmap-frameworks skill (strategic alignment)
3. Applies multiple frameworks for comprehensive scoring

Result: Comprehensive prioritization using multiple lenses
```

### Cross-Agent Skill Usage

Multiple agents can reference the same skill:

**Example: Product Positioning**

```
product-strategist + market-analyst
→ Both reference product-positioning skill
→ Consistent positioning framework across strategy
→ Unified market approach
```

---

## Creating New Skills

### When to Create a Skill

Create a skill when:

- 2+ agents need the same knowledge
- It's a well-defined framework or methodology
- It's reusable across scenarios
- It's substantial enough to warrant separation

Don't create a skill when:

- Only one agent uses it (include in agent directly)
- It's too specific to one scenario
- It's simple enough to be inline instructions

### Skill Structure Template

```yaml
---
name: skill-name
description: Brief description of when to use this skill
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

## Skill File Structure & Specification

### File Organization

Skills are organized in the ai-pm-copilot plugin's `skills/` directory. Each skill includes a SKILL.md file plus optional assets and references:

```
plugins/ai-pm-copilot/skills/
├── user-research-techniques/
│   ├── SKILL.md
│   ├── assets/           (templates, frameworks, checklists)
│   └── references/       (guides, best practices)
├── interview-frameworks/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── synthesis-frameworks/
│   ├── SKILL.md
│   └── assets/
├── usability-frameworks/
│   ├── SKILL.md
│   └── assets/
├── validation-frameworks/
│   ├── SKILL.md
│   └── assets/
├── product-positioning/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── competitive-analysis-templates/
│   ├── SKILL.md
│   └── assets/
├── market-sizing-frameworks/
│   ├── SKILL.md
│   └── assets/
├── product-market-fit/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── roadmap-frameworks/
│   ├── SKILL.md
│   └── assets/
├── prioritization-methods/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── specification-techniques/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── prd-templates/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
├── user-story-templates/
│   ├── SKILL.md
│   └── assets/
├── go-to-market-playbooks/
│   ├── SKILL.md
│   ├── assets/
│   └── references/
└── launch-planning-frameworks/
    ├── SKILL.md
    ├── assets/
    └── references/
```

**Total**: 16 skills, 63 asset files, 37 reference files

### Skill File Format

Each skill follows this standardized structure:

```markdown
---
name: skill-name
description: One-line description of when to use this skill
---

# Skill Name

## Overview

Brief introduction to the framework/methodology (2-3 paragraphs).

## When to Use This Skill

Clear guidance on scenarios where this skill applies.

## Core Frameworks

Detailed explanations of included frameworks, methodologies, or techniques.

### Framework 1: Name

**Purpose**: What this framework achieves
**When to use**: Specific scenarios
**How it works**: Step-by-step explanation

**Example:**
[Concrete example with real data]

### Framework 2: Name

[Similar structure...]

## Practical Application

How to apply this skill in real PM work.

## Integration with Other Skills

How this combines with other skills.

## Resources & References

- Thought leaders and practitioners
- Key books and articles
- Tools and templates

## Examples

### Example 1: [Scenario Name]

**Context**: [Realistic PM scenario]
**Application**: [How skill is applied]
**Outcome**: [Result achieved]
```

### YAML Frontmatter Specification

Skills use minimal frontmatter with just two required fields:

```yaml
---
name: skill-identifier # Lowercase, hyphen-separated
description: Brief one-line description of the skill and when to use it
---
```

Skills are activated by agents based on the request context. The skill's description and content body help agents determine when to load it.

### Progressive Disclosure Levels

**Level 1: Metadata** (Always loaded - ~200-500 tokens)

- Name, description, category
- Activation triggers
- Associated agents
- Basic "when to use" guidance

**Level 2: Instructions** (Loaded on activation - ~1,000-2,000 tokens)

- Framework overviews
- Step-by-step processes
- Core methodologies
- Decision criteria

**Level 3: Resources** (Referenced as needed - ~2,000-5,000 tokens)

- Detailed examples
- Case studies
- Templates
- Extended references

### Creating a New Skill

**Step 1: Define Scope**

```markdown
# What framework/methodology does this cover?

# What problem does it solve?

# Which agents will use it?

# What are the activation triggers?
```

**Step 2: Create Directory and File**

```bash
# Create skill directory in ai-pm-copilot plugin
mkdir -p plugins/ai-pm-copilot/skills/feature-flagging-strategy/
```

**Step 3: Add Frontmatter**

```yaml
---
name: feature-flagging-strategy
description: Progressive rollout, targeting, and feature management strategies
---
```

**Step 4: Write Content**
Follow the skill file format structure above.

**Step 5: Test Activation**

```
# Test with agent
Tell launch-planner: "How should we roll out this feature using feature flags?"

# Verify skill loads
→ Should reference feature-flagging-strategy skill
→ Should apply progressive rollout frameworks
```

### Skill Versioning

Skills are versioned with the plugin. Update the plugin version in `plugin.json` when making skill changes.

### Skill Quality Checklist

Before submitting a new skill:

- [ ] Frontmatter has name and description
- [ ] "When to use" guidance provided
- [ ] At least 2 detailed frameworks/methodologies
- [ ] 2+ practical examples with real data
- [ ] Integration guidance for agents
- [ ] Resources and references included
- [ ] Tested with relevant agents
- [ ] Follows progressive disclosure pattern
- [ ] Token-efficient (metadata < 500 tokens)

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

**Available Skills**: 16 in ai-pm-copilot plugin
**Categories**: User Research (5), Strategy (4), Execution (5), Launch (2)
**Assets**: 63 templates, frameworks, and checklists
**References**: 37 guides and best practices
**Last Updated**: February 2026
