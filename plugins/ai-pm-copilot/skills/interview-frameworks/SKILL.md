---
name: interview-frameworks
description: Master user interviews including interview guide design, questioning techniques, active listening, probing, avoiding leading questions, and interview analysis. Use when conducting user interviews, designing interview guides, researching user needs, discovering problems, validating assumptions, or gathering qualitative insights. Covers interview best practices, question types, and interviewing techniques from Teresa Torres and Erika Hall.
---

# Interview Frameworks

## Overview

Frameworks for conducting effective user interviews including question design, interviewing techniques, and extracting actionable insights.

**Core Principle**: Good interviews come from great questions. Focus on past behavior and specific examples, not hypotheticals or opinions. Listen more than you talk.

**Origin**: Synthesized from Teresa Torres ("Continuous Discovery Habits"), Erika Hall ("Just Enough Research"), and Rob Fitzpatrick ("The Mom Test").

**Key Insight**: User interviews are the foundation of customer discovery. Good interviews uncover unmet needs, validate assumptions, and reveal the "why" behind user behavior that quantitative data cannot.

## When to Use This Skill

**Auto-loaded by agents**:
- `research-ops` - For user interview guides and JTBD interviews

**Use when you need**:
- Customer discovery research
- Problem validation
- Solution validation
- Usability testing
- Feature prioritization research
- Understanding user workflows
- Jobs-to-be-Done research

---

## Four Types of User Interviews

### Discovery Interviews (Problem Exploration)

**Purpose**: Understand problems, needs, contexts, pain points

**When**: Early product development, new market, problem validation

**Focus**:
- Current workflows
- Pain points and workarounds
- Unmet needs
- Context and constraints

**Example question**: "Walk me through how you currently manage projects for your team"

**Complete script**: `assets/interview-script-templates.md` (Discovery section)

---

### Validation Interviews (Solution Testing)

**Purpose**: Test solutions, get feedback on concepts

**When**: After problem validation, before building

**Focus**:
- Solution fit with workflow
- Feature prioritization
- Willingness to pay
- Alternatives considered

**Example question**: "If we built [solution], how would that fit into your workflow?"

**Complete script**: `assets/interview-script-templates.md` (Validation section)

---

### Usability Interviews (Product Testing)

**Purpose**: Test actual product, identify friction

**When**: During or after building

**Focus**:
- Task completion
- Confusion points
- Feature clarity
- Missing functionality

**Example question**: "Try creating a project. Think aloud as you go."

**Complete script**: `assets/interview-script-templates.md` (Usability section)

---

### Generative Interviews (Open Exploration)

**Purpose**: Broad exploration, no specific hypothesis

**When**: Exploring new markets or pivots

**Focus**:
- Day in the life
- Goals and motivations
- Decision-making process
- Context and constraints

**Example question**: "Tell me about a recent project that didn't go as planned"

**Complete script**: `assets/interview-script-templates.md` (Generative section)

---

## Core Interview Techniques

### The Mom Test (Rob Fitzpatrick)

**Principle**: Ask questions that even your mom couldn't lie to you about

**Bad questions** (invite lies):
- "Would you buy this?" (people lie about future)
- "Do you think this is a good idea?" (want to be nice)
- "Would you use this feature?" (hypothetical)

**Good questions** (reveal truth):
- "When's the last time [problem] came up?" (frequency)
- "How much time/money did that cost you?" (severity)
- "What are you currently doing to solve it?" (existing solutions)
- "Show me your [current solution]" (actual behavior)
- "Who else should I talk to?" (validates problem is real)

**Complete guide**: `assets/questioning-techniques-template.md` (Mom Test section)

---

### The 5 Whys

**Purpose**: Get to root cause by asking "why" repeatedly

**Process**:
1. Start with observation
2. Ask "why" or "what causes that?"
3. Repeat 4-5 times until reaching root cause
4. Stop when you have actionable insight

**Example**:
```
"I don't use feature X"
→ Why? "It's too complicated"
→ Why complicated? "Don't understand buttons"
→ Why? "Labels unclear"
→ Why? "Use jargon I don't know"
→ Why? "Never learned terminology"

Root cause: Onboarding gap + plain language needed
```

**Complete guide**: `assets/questioning-techniques-template.md` (5 Whys section)

---

### Jobs-to-be-Done (JTBD) Interview

**Framework**: Understand the "job" user is hiring product to do

**Question Structure**:
1. **Context**: "Tell me about the last time you [hired product/made decision]"
2. **Situation**: "What was happening? What triggered you?"
3. **Desired Outcome**: "What were you hoping to achieve?"
4. **Alternatives**: "What else did you consider? Why didn't those work?"
5. **Decision**: "What made you choose [solution]?"

**Key Insight**: Find the real job (not surface level)
- Surface: "Manage tasks"
- Actual job: "Maintain visibility and accountability as team scales"

**Complete guide**: `assets/questioning-techniques-template.md` (JTBD section)

---

### Laddering Technique

**Purpose**: Connect features to emotional benefits

**Structure**: Attributes → Consequences → Values

**Process**: Keep asking "Why does that matter?" until reaching emotional value

**Example**:
```
Feature: "Real-time collaboration"
→ "So team can work together" (Consequence)
→ "Faster to get things done" (Consequence)
→ "I can go home on time" (Consequence)
→ "Spend time with my family" (Value)

Marketing insight: Sell "time with family" not "real-time sync"
```

**Complete guide**: `assets/questioning-techniques-template.md` (Laddering section)

---

## Best Practices

### DO

**Ask open-ended questions**:
- ✓ "How do you currently solve [problem]?"
- ✗ "Do you solve [problem] with a spreadsheet?" (yes/no)

**Listen more than talk** (80/20 rule):
- ✓ Silent pauses (let them fill silence)
- ✗ Jump to next question immediately

**Ask for specific examples**:
- ✓ "Tell me about the last time you..."
- ✗ "Generally, do you...?" (hypothetical)

**Probe for details**:
- ✓ "How much time does that take?"
- ✗ Accept vague answers ("a lot")

**Ask about past behavior**:
- ✓ "When did you last...?"
- ✗ "Would you...?" (future hypothetical)

---

### DON'T

**Lead the witness**:
- ✗ "Wouldn't it be great if...?"
- ✓ "How would that fit your workflow?"

**Pitch your solution** (discovery phase):
- ✗ "Our tool solves this with [feature]!"
- ✓ "What would an ideal solution look like?"

**Ask hypothetical questions**:
- ✗ "If we built X, would you use it?"
- ✓ "How did you decide to try your current solution?"

**Multi-part questions**:
- ✗ "Do you use A and what about B, also C?"
- ✓ One question at a time

---

## Participant Recruitment

### Define Target

**Must-Have Criteria** (Disqualify if NO):
- Role: [Specific role]
- Company size: [Range]
- Uses [product category]
- [Decision authority level]

**Disqualify**:
- Works at competitor
- Friends/family (too biased)
- Professional interviewees (6+ studies/year)

**Complete guide**: `assets/participant-recruitment-guide.md`

Screener templates, sourcing channels, outreach templates, incentive guidance

---

### Sourcing Channels

**Your users** (30-50% response rate):
- Best for: Usability testing, current user feedback
- Incentive: $0-50

**Your leads** (20-40% response rate):
- Best for: Problem validation, why they didn't buy
- Incentive: $50-75

**LinkedIn** (5-15% response rate):
- Best for: Discovery, reaching specific roles
- Incentive: $50-75

**Research panels** (Respondent.io, User Interviews):
- Best for: Fast recruitment, hard-to-reach segments
- Cost: $100-300 per participant

**Communities** (Reddit, Slack, Discord):
- Best for: Niche audiences, passionate users
- Incentive: $0-75 (sometimes free)

---

## Note-Taking and Recording

### Recording

**Always ask permission**:
```
"Do you mind if I record for my notes? Only our team will see it."

Tools:
- Zoom/Google Meet (built-in)
- Otter.ai (transcription)
- Grain.co (AI highlights)
```

**Benefits**: Don't miss details, review later, share with team, focus on listening

---

### Two-Column Notes

**Left: Observations** (What they said/did)
**Right: Interpretations** (What you think it means)

Example:

| Observations | Interpretations |
|--------------|-----------------|
| "Use spreadsheets" | Pain: Manual, error-prone? |
| "Takes 2 hours every Monday" | Severity: HIGH (100hr/year) |
| [Frustrated sigh] | Emotion: Strong frustration |

**Complete guide**: `assets/note-taking-analysis-guide.md`

Recording best practices, note templates, immediate debrief, transcription review

---

## Analysis and Synthesis

### Affinity Mapping

**Process**:
1. Write observations on sticky notes (one per note)
2. Put all notes on wall (physical or digital)
3. Group similar notes together
4. Name each cluster (theme)
5. Look for patterns across clusters

**Example themes**:
- "Manual reporting overhead"
- "Management visibility needs"
- "Tool fragmentation"
- "Coordination failures"

**Meta-pattern**: Management needs visibility → Forces manual reporting → Causes coordination failures

---

### Extracting Insights

**Good Insight Formula**: Observation + Pattern + Implication

**Bad** (too vague):
- "Users don't like the UI"

**Good** (specific, surprising, actionable):
- "5/8 users abandoned task at 'Add Members' step because 'team member' label was ambiguous, suggesting we need clearer labeling and examples"

**Insight Template**:
```
INSIGHT: [One-sentence summary]
EVIDENCE: [X/Y participants, specific data]
PATTERN: [How many? What's common?]
IMPLICATIONS:
- Product: [What to build/change]
- Priority: [HIGH/MEDIUM/LOW]
- Risk if ignored: [What happens if we don't act]
QUOTES: [Compelling verbatim quotes]
```

**Complete guide**: `assets/note-taking-analysis-guide.md` (Analysis section)

Observation extraction, affinity mapping detailed process, insight templates, analysis tools

---

## Research Deliverables

### Report Types

**Email Summary** (30 min):
- Best for: Quick updates, busy team members
- Format: TL;DR + 3 findings + recommendations

**Slide Deck** (2-4 hours):
- Best for: Presentations, cross-functional teams
- Format: 15-25 slides with findings and quotes

**Research Report** (4-8 hours):
- Best for: Comprehensive documentation
- Structure:
  1. Executive Summary (1 page)
  2. Methodology (1 page)
  3. Key Findings (3-5 pages)
  4. Recommendations (1-2 pages)
  5. Appendix

**Highlight Reel** (1-2 hours):
- Best for: Emotional impact, building empathy
- Format: 2-4 min video with 3-5 user clips

**Complete guide**: `references/research-deliverables-guide.md`

Report structures, presentation formats, storytelling with research, video highlights, sharing across org

---

## Templates and References

### Assets (Ready-to-Use Templates)

Copy-paste these for immediate use:
- `assets/interview-script-templates.md` - 4 complete interview scripts (Discovery, Validation, Usability, Generative) with timing and questions
- `assets/questioning-techniques-template.md` - Mom Test, 5 Whys, JTBD, Laddering, probing techniques
- `assets/participant-recruitment-guide.md` - Screener surveys, sourcing channels, outreach templates, incentive guide
- `assets/note-taking-analysis-guide.md` - Recording setup, two-column notes, affinity mapping, insight extraction

### References (Deep Dives)

When you need comprehensive guidance:
- `references/interviewing-best-practices-guide.md` - Complete interviewing guide covering preparation, execution, common pitfalls, advanced techniques, ethical considerations
- `references/research-deliverables-guide.md` - Report structures, presentation formats, storytelling with research, sharing insights across organization

---

## Quick Reference

```
Problem: Need to understand user needs and validate product decisions
Solution: Conduct user interviews

Interview Type Selection:
├─ Problem unclear? → Discovery interviews
├─ Have solution idea? → Validation interviews
├─ Product built? → Usability interviews
└─ Exploring broadly? → Generative interviews

Core Techniques:
├─ Mom Test: Past behavior, not future intentions
├─ 5 Whys: Find root cause
├─ JTBD: Understand the job
└─ Laddering: Connect features to emotions

Key Rules:
- Listen 80%, talk 20%
- Ask about past (not future)
- Probe surface answers
- Use silence
- Record everything
- Debrief immediately
```

---

## Resources

**Books**:
- "The Mom Test" by Rob Fitzpatrick (2013) - Asking good questions
- "Just Enough Research" by Erika Hall (2013) - Practical user research
- "Continuous Discovery Habits" by Teresa Torres (2021) - Ongoing customer interviews

**Articles**:
- "How to Do User Interviews" - Teresa Torres
- "The Mom Test: Customer Development Done Right" - Rob Fitzpatrick

**Tools**:
- **Recording**: Zoom, Otter.ai, Grain
- **Analysis**: Dovetail, Miro, Notion, Airtable
- **Recruitment**: Respondent.io, User Interviews

---

## Related Skills

- `synthesis-frameworks` - Synthesizing qualitative research into actionable insights
- `validation-frameworks` - Solution validation techniques and testing
- `user-research-techniques` - Comprehensive user research methods beyond interviews

---

**Key Principle**: Great interviews reveal truth through specific past behavior, not opinions about hypothetical futures. Master questioning techniques (Mom Test, 5 Whys, JTBD, Laddering) to uncover what users really think, not what they think you want to hear. Listen more than you talk, probe surface-level answers, and use synthesis techniques to extract actionable insights.
