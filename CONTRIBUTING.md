# Contributing to Product Management Toolkit

Thank you for considering contributing to the Product Management Toolkit for Claude Code! This toolkit grows with the PM community.

## How to Contribute

### Ways to Contribute

1. **Report Bugs or Request Features**
   - Open an issue on GitHub
   - Use clear, descriptive titles
   - Include reproduction steps for bugs
   - Explain the use case for feature requests

2. **Submit New Agents**
   - Create agents for specialized PM domains
   - Follow the agent template structure (see below)
   - Include comprehensive capabilities and examples
   - Add frontmatter with name, description, and model

3. **Add New Commands**
   - Create focused, single-purpose utilities
   - Follow the command template structure
   - Include clear usage instructions
   - Provide examples and edge cases

4. **Contribute Skills**
   - Add new PM frameworks and methodologies
   - Organize as SKILL.md in subdirectory
   - Include when-to-use guidance
   - Provide concrete examples

5. **Improve Documentation**
   - Fix typos or unclear explanations
   - Add usage examples
   - Expand best practices
   - Create tutorials

## Contribution Guidelines

### Naming Conventions

- **Lowercase, hyphen-separated**: `user-researcher.md`, `feature-prioritizer.md`
- **Descriptive names**: Name should clearly indicate purpose
- **Consistent patterns**: Follow existing naming in the repository

### Agent Template Structure

```markdown
---
name: agent-name
description: One-line description of expertise and when to use
model: claude-sonnet-4-5
---

# Agent Name

## Purpose
Clear statement of the agent's role and expertise.

## Core Philosophy
Guiding principles and approaches (3-6 key tenets).

## Capabilities
Detailed breakdown of what the agent can do, organized by category.

## When to Use This Agent
Specific scenarios where this agent adds value.

## Example Interactions
Sample conversations showing the agent in action.
```

### Command Template Structure

```markdown
# Command Name

One-line description of what this command does.

## Usage

\`\`\`
/pm:command-name [parameters]
\`\`\`

## What This Command Does

Numbered list of outputs and behaviors.

## Instructions

Step-by-step guide for the command execution.

## Examples

Concrete usage examples with expected outputs.
```

### Skills Template Structure

```markdown
---
name: skill-name
description: When to use this skill and what it provides
---

# Skill Name

## Overview
Brief introduction to the framework/methodology.

## When to Use This Skill
Specific scenarios where this knowledge applies.

## Core Frameworks
Detailed explanations with examples.

## Practical Application
How to apply in real PM work.
```

## Quality Standards

### Content Requirements

1. **Comprehensive**: Cover the topic thoroughly
2. **Practical**: Include real-world examples
3. **Actionable**: Provide clear next steps
4. **Well-structured**: Use clear headings and organization
5. **Accurate**: Ensure technical accuracy and cite sources

### Writing Style

- **Clear and concise**: Avoid jargon unless necessary
- **Professional**: Maintain a helpful, expert tone
- **Scannable**: Use headings, lists, and formatting
- **Example-driven**: Show, don't just tell

### Token Efficiency

- Focus on essential information
- Avoid redundancy
- Use progressive disclosure patterns
- Keep activation criteria clear

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

- Add your agent, command, or skill
- Follow the templates above
- Update plugin README if needed
- Test your contribution

### Step 4: Commit Changes

```bash
git add .
git commit -m "Add [agent/command/skill]: descriptive name"
```

### Step 5: Push and Create PR

```bash
git push origin feature/your-contribution-name
```

Then open a Pull Request on GitHub with:
- Clear title describing the contribution
- Summary of what you're adding
- Why it's valuable for PMs
- Any testing or validation you've done

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

## Questions?

- **General questions**: Open a GitHub Discussion
- **Bugs or issues**: Create a GitHub Issue
- **Contribution ideas**: Start with an Issue to discuss

## Recognition

All contributors will be acknowledged in:
- CHANGELOG.md for each release
- GitHub contributors list
- Special mentions for significant contributions

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for helping make the Product Management Toolkit better for the entire PM community!
