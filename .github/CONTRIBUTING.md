# Contributing to Product Management Toolkit

Thank you for your interest in contributing! This guide will help you contribute agents, skills, documentation, or improvements to the Product Management Toolkit.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Ways to Contribute](#ways-to-contribute)
- [Development Workflow](#development-workflow)
- [Agent Contributions](#agent-contributions)
- [Skill Contributions](#skill-contributions)
- [Documentation Standards](#documentation-standards)
- [Content Guidelines](#content-guidelines)
- [Pull Request Process](#pull-request-process)

---

## Code of Conduct

This project follows the Contributor Covenant Code of Conduct. By participating, you agree to uphold this code. Please report unacceptable behavior to the maintainers.

**Expected behavior:**

- Be respectful and inclusive
- Welcome newcomers
- Focus on constructive feedback
- Prioritize quality over speed

---

## Getting Started

### Prerequisites

- Claude Code installed and configured
- Git for version control
- Markdown editor (VS Code, Obsidian, etc.)
- Basic understanding of product management concepts

### Fork and Clone

```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR_USERNAME/agents.git
cd agents

# Add upstream remote
git remote add upstream https://github.com/slgoodrich/agents.git
```

### Install Plugin Locally

```bash
# In Claude Code, install from local directory
/plugin install /path/to/agents
```

---

## Ways to Contribute

### 1. Bug Reports

Found a bug? Please open an issue with:

- Clear description of the issue
- Steps to reproduce
- Expected vs actual behavior
- Claude Code version

### 2. Feature Requests

Have an idea? Open an issue describing:

- Problem you're trying to solve
- Proposed solution
- Why this would benefit solo developers/small teams
- Example use cases

### 3. Agent Improvements

Enhance existing agents:

- Improve instructions
- Add better examples
- Refine behavioral traits
- Update knowledge base

### 4. New Skills

Add framework knowledge:

- Research methodologies
- Strategic frameworks
- Execution playbooks
- Templates and assets

### 5. Documentation

Improve guides and references:

- Fix typos or unclear sections
- Add usage examples
- Create tutorials
- Expand references

---

## Development Workflow

### 1. Create Branch

```bash
# Sync with upstream
git fetch upstream
git checkout main
git merge upstream/main

# Create feature branch
git checkout -b feature/your-feature-name
# or
git checkout -b fix/bug-description
```

### 2. Make Changes

Follow the patterns and conventions in existing files.

### 3. Test Changes

```bash
# Manual testing in Claude Code
/plugin install /path/to/your/fork
# Test your changes
```

### 4. Commit

```bash
git add .
git commit -m "feat: Add new skill for lean startup frameworks"
# or
git commit -m "fix: Correct frontmatter in market-analyst agent"
```

**Commit message conventions:**

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation only
- `test:` Adding or fixing tests
- `refactor:` Code changes that neither fix bugs nor add features

### 5. Push and Create PR

```bash
git push origin feature/your-feature-name
```

Then create a Pull Request on GitHub.

---

## Agent Contributions

### Creating a New Agent

**When to create:**

- Covers a distinct PM discipline not handled by existing 8 agents
- Has clear, focused responsibilities
- Would be used by solo developers/small teams

**When NOT to create:**

- Overlaps significantly with existing agents
- Too specialized (create a skill instead)
- Corporate PM focused (stakeholder management, executive alignment)

### Agent Structure

Follow this template for new agents:

```markdown
---
name: agent-name
description: One-line description of specialty and use cases
model: sonnet
---

# Agent Name

## Purpose

High-level mission and value proposition.

## Core Philosophy

Foundational principles this agent follows.

## Capabilities

Detailed breakdown of what this agent can do:

- Capability 1
- Capability 2
- Capability 3

## Skills Activated

Skills this agent loads on-demand:

- skill-name-1
- skill-name-2

## Response Approach

Step-by-step process for handling requests:

1. Analyze request
2. Load relevant skills
3. Apply frameworks
4. Generate response

## Example Interactions

### Example 1: [Scenario]

**User:** "[realistic request]"

**Agent:** "[detailed response showing approach]"

### Example 2: [Scenario]

**User:** "[another realistic request]"

**Agent:** "[response demonstrating different capability]"

## When to Use This Agent

Use when:

- Scenario 1
- Scenario 2

Don't use when:

- Other agent is better suited
- Task is too simple

## Integration with Other Agents

How this agent collaborates:

- Works with X agent for Y workflow
- Hands off to Z agent when...
```

### Agent Checklist

Before submitting agent PR:

- [ ] Frontmatter includes name, description, model
- [ ] Purpose section clearly explains mission
- [ ] At least 2 detailed example interactions
- [ ] "When to use" guidance provided
- [ ] Integration with other agents documented
- [ ] No stakeholder management jargon
- [ ] Solo developer/small team focus
- [ ] Skills activated are listed
- [ ] Follows existing agent patterns
- [ ] Tested in Claude Code

---

## Skill Contributions

### Creating a New Skill

**When to create:**

- 2+ agents would use this knowledge
- Well-defined framework or methodology
- Reusable across scenarios
- Substantial enough to warrant separation

**When NOT to create:**

- Only one agent uses it (add to agent instead)
- Too specific to one scenario
- Simple enough for inline instructions

### Skill Structure

Each skill includes:

1. **SKILL.md** - Main skill file with frontmatter
2. **assets/** - Templates, frameworks, checklists
3. **references/** - Guides, best practices, methodologies

**Directory structure:**

```
skills/
└── your-skill-name/
    ├── SKILL.md
    ├── assets/
    │   ├── template-1.md
    │   ├── framework-2.md
    │   └── checklist-3.md
    └── references/
        ├── guide-1.md
        └── best-practices-2.md
```

**SKILL.md template:**

```markdown
---
name: skill-name
description: Brief description of framework/methodology
category: research|strategy|execution|launch
---

# Skill Name

## Overview

What this skill provides and when to use it.

## Frameworks Included

1. Framework 1
2. Framework 2
3. Framework 3

## Framework 1: Name

### What It Is

Brief description.

### When to Use

Scenarios where this is appropriate.

### How to Apply

Step-by-step methodology.

### Example

Realistic example with data.

### Assets

- Template: `assets/template-name.md`
- Checklist: `assets/checklist-name.md`

## Framework 2: Name

[Same structure...]

## Integration with Agents

Which agents use this skill and how:

- **agent-name**: Uses for [purpose]

## References

Guides and best practices:

- Guide: `references/guide-name.md`
- Best practices: `references/best-practices.md`
```

### Asset Files

Create focused, practical assets:

**Templates** (`assets/`):

- Structured formats for deliverables
- Fill-in-the-blank sections
- Examples showing usage
- Solo developer/small team scaled

**References** (`references/`):

- Best practices guides
- Methodology deep-dives
- Framework comparisons
- Industry standards

### Skill Checklist

Before submitting skill PR:

- [ ] SKILL.md has valid frontmatter (name, description, category)
- [ ] At least 2 frameworks documented
- [ ] Each framework has practical example
- [ ] Assets directory exists with templates/frameworks
- [ ] All assets referenced in SKILL.md
- [ ] References directory exists if applicable
- [ ] All references mentioned in SKILL.md
- [ ] Integration section lists which agents use this
- [ ] No stakeholder management jargon
- [ ] Solo developer focus
- [ ] Tested with relevant agents

---

## Documentation Standards

### Markdown Formatting

- Use GitHub-flavored markdown
- Include code fences with language tags
- Use tables for comparisons
- Add clear section headings

### Style Guide

**Tone:**

- Clear and concise
- Action-oriented
- Solo developer focused
- No jargon or buzzwords

**Language:**

- Use "you" (not "users" or "stakeholders")
- Active voice
- Present tense
- Direct instructions

**Examples:**

- Provide realistic scenarios
- Use actual product examples
- Include complete workflows
- Show before/after comparisons

### File Organization

- Keep related content together
- Use consistent naming conventions
- Link between related docs
- Maintain table of contents

---

## Content Guidelines

### Target Audience

**Solo developers and small teams:**

- 1-10 person teams
- Limited PM resources
- Need practical, actionable advice
- Focus on execution over process

### What to Include

- Practical frameworks and templates
- Real-world examples
- Step-by-step instructions
- Quick wins and best practices

### What to Avoid

- Stakeholder management jargon
- Corporate PM processes (RACI, executive alignment)
- Enterprise-scale solutions
- Academic or theoretical content
- Buzzwords and marketing speak

### Quality Standards

**All contributions must:**

- Be accurate and well-researched
- Provide practical value
- Scale to small teams
- Follow existing patterns
- Include examples
- Pass automated tests

---

## Pull Request Process

### 1. Create PR

- Clear, descriptive title
- Detailed description of changes
- Screenshots if applicable

**PR template:**

```markdown
## Description

Brief summary of changes.

## Motivation

Why is this change needed?

## Type of Change

- [ ] Bug fix
- [ ] New feature (agent, skill, command)
- [ ] Documentation
- [ ] Testing

## Testing

- [ ] Manual testing completed

## Checklist

- [ ] Follows contribution guidelines
- [ ] Documentation updated
- [ ] No stakeholder references
- [ ] Solo developer focused
```

### 2. Review Process

Maintainers will review for:

- Code quality and patterns
- Test coverage
- Documentation completeness
- Content guidelines adherence
- Solo developer focus

**Feedback may include:**

- Requested changes
- Questions for clarification
- Suggestions for improvement
- Alternative approaches

### 3. Address Feedback

- Make requested changes
- Push updates to same branch
- Respond to reviewer comments
- Request re-review when ready

### 4. Merge

Once approved:

- Maintainer will merge
- Your contribution becomes part of the toolkit
- You'll be credited in CHANGELOG.md

---

## Development Guidelines

### File Structure

Follow existing patterns:

```
plugins/ai-pm-copilot/
├── agents/           # 8 agent files
├── commands/         # 1 command file
└── skills/           # 16 skill directories
    └── skill-name/
        ├── SKILL.md
        ├── assets/
        └── references/
```

### Naming Conventions

**Agents:** `agent-name.md` (kebab-case)
**Skills:** `skill-name/` (kebab-case directory)
**Assets:** `descriptive-name.md` (kebab-case)
**References:** `topic-name.md` (kebab-case)

### Frontmatter

**Agents:**

```yaml
---
name: agent-name
description: One-line description
model: sonnet
---
```

**Skills:**

```yaml
---
name: skill-name
description: Brief description
category: research|strategy|execution|launch
---
```

### Versioning

Plugin uses semantic versioning:

- **MAJOR** (2.0.0): Breaking changes
- **MINOR** (2.1.0): New features (backward compatible)
- **PATCH** (2.0.1): Bug fixes

Your contribution determines version bump:

- New agent/skill: MINOR
- Breaking changes: MAJOR
- Bug fixes: PATCH
- Documentation: PATCH

---

## Questions & Support

### Getting Help

- **Questions:** Open a GitHub Discussion
- **Bugs:** Open an Issue with test results
- **Ideas:** Open an Issue with proposal
- **Chat:** Join community discussions

### Resources

- [Architecture Guide](docs/architecture.md) - System design
- [Agents Guide](docs/agents.md) - Agent documentation
- [Skills Reference](docs/agent-skills.md) - Skills catalog
- [Usage Guide](docs/usage.md) - Usage patterns

---

## Recognition

Contributors are recognized in:

- CHANGELOG.md for each release
- GitHub contributors list
- Project README.md

Thank you for contributing to the Product Management Toolkit!

---

**Last Updated**: October 2025
**Maintained by**: Steve Goodrich (@slgoodrich)
