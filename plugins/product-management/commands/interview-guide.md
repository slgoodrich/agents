# Interview Guide Generator

Create structured user interview guides for discovery and validation research.

## Usage

```
/pm:interview-guide [research objective]
```

## What This Command Does

Generates comprehensive interview protocols with objectives, screening criteria, and question flow.

## Instructions

Create interview guide with:
1. Research objectives
2. Participant criteria
3. Interview structure (intro, warm-up, main questions, wrap-up)
4. Open-ended questions
5. Follow-up probes
6. Time allocation

## Template

```markdown
# Interview Guide: [Topic]

**Duration**: 45-60 minutes
**Research Objective**: [What you're trying to learn]

## Participant Criteria
- [Requirement 1]
- [Requirement 2]

## Interview Structure

### Introduction (5 min)
- Thank participant
- Explain purpose and confidentiality
- Get recording consent
- Set expectations

### Warm-up (5 min)
1. Tell me about your role
2. How long have you been [doing X]?

### Main Questions (35 min)

**Current Behavior**
3. Walk me through the last time you [relevant task]
4. What triggers you to [action]?
5. What tools do you currently use?

**Pain Points**
6. What's most frustrating about [current process]?
7. Tell me about a time when [problem occurred]
8. What workarounds have you developed?

**Goals & Needs**
9. What are you trying to achieve when you [task]?
10. How do you measure success?
11. What would make this dramatically better?

**Validation** (if testing solution)
12. [Show prototype/concept]
13. What's your initial reaction?
14. How would you use this?
15. What concerns do you have?

### Wrap-up (10 min)
16. Is there anything we haven't covered?
17. Who else should I talk to?
18. Thank you + next steps
```

## Model
claude-sonnet-4-5

## Related
- `/pm:persona` - Use personas to guide
- `/pm:research-synthesize` - Analyze interviews
