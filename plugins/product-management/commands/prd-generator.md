# PRD Generator

Generate a comprehensive Product Requirements Document (PRD) from a feature idea or problem statement.

## Usage

```
/pm:prd [feature description or problem statement]
```

## What This Command Does

1. Analyzes your feature idea or problem
2. Generates a structured, comprehensive PRD including:
   - Problem statement and opportunity
   - User personas and use cases
   - Functional and non-functional requirements
   - Success metrics and KPIs
   - Technical specifications
   - Launch plan and rollout strategy
   - Risks and open questions
3. Provides a ready-to-review document for stakeholders

## Instructions

When the user provides a feature idea or problem statement:

1. **Gather Context** (ask if not provided):
   - Target users and personas
   - Core problem being solved
   - Business goals and success metrics
   - Technical constraints
   - Timeline and dependencies

2. **Generate PRD** using the requirements-engineer agent's comprehensive template:
   - TL;DR (2-3 sentence summary)
   - Problem statement with evidence
   - Goals and success metrics table
   - User personas and use cases
   - Solution overview and key features
   - Detailed functional requirements with acceptance criteria
   - Non-functional requirements (performance, security, accessibility)
   - User experience and wireframes section
   - Technical specifications
   - Dependencies and constraints
   - Rollout plan
   - Risks and mitigations
   - Open questions
   - Alternatives considered

3. **Ensure Quality**:
   - Specific, measurable success metrics
   - Clear acceptance criteria (Given-When-Then format)
   - Defined scope (what's in, what's out)
   - Evidence-based problem statement
   - Testable requirements

4. **Provide Next Steps**:
   - Review process (who needs to approve)
   - Questions to answer before build
   - Recommended followup actions

## Example

**Input**: "We need a dark mode for our app"

**Output**: Complete PRD including:
- Problem: User eye strain, modern UX expectation
- Success Metrics: 40% adoption, +15% session duration
- Requirements: Theme toggle, system preference detection, WCAG AA contrast
- Technical Spec: CSS custom properties approach
- Rollout: Beta → 10% → 100% over 2 weeks
- Risks: Third-party widgets may break

## Model

Use: claude-sonnet-4-5

## Related

- `/pm:user-stories` - Convert PRD to user stories
- `/pm:technical-spec` - Generate technical specification
- `/pm:one-pager` - Create executive summary
