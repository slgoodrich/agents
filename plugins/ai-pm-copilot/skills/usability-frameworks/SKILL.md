---
name: usability-frameworks
description: Usability testing methodology, Nielsen's heuristics, and usability metrics for evaluating user interfaces
---

# Usability Frameworks

Comprehensive frameworks and methodologies for planning, conducting, and analyzing usability tests to improve user experience.

## When to Use This Skill

**Auto-loaded by agents**:
- `research-ops` - For usability testing and heuristic evaluation

**Use when you need**:
- Planning usability tests
- Conducting user testing sessions
- Evaluating interface designs
- Identifying usability problems
- Testing prototypes or live products
- Applying Nielsen's heuristics
- Measuring usability metrics

## Core Concepts

### What is Usability Testing?

Usability testing is a method for evaluating a product by testing it with representative users. Users attempt to complete typical tasks while observers watch, listen, and take notes.

**Purpose**: Identify usability problems, discover opportunities for improvement, and learn about user behavior and preferences.

**When to use**:
- Before development (testing prototypes)
- During development (iterative testing)
- After launch (validation and optimization)
- Before major redesigns

### The Five Usability Quality Components (Jakob Nielsen)

1. **Learnability**: How easy is it for users to accomplish basic tasks the first time?
2. **Efficiency**: How quickly can users perform tasks once they've learned the design?
3. **Memorability**: Can users remember how to use it after time away?
4. **Errors**: How many errors do users make, how severe, and how easily can they recover?
5. **Satisfaction**: How pleasant is it to use the design?

## Usability Testing Methodologies

### 1. Moderated Testing

**Setup**: Researcher guides participants through tasks in real-time
**Location**: In-person or remote (video call)

**Best for**:
- Early-stage prototypes needing clarification
- Complex products requiring guidance
- Exploring "why" behind user behavior
- Uncovering emotional reactions

**Process**:
1. Welcome and set expectations
2. Pre-task questions (background, experience)
3. Task scenarios with think-aloud protocol
4. Post-task questions and discussion
5. Wrap-up and thank you

**Advantages**:
- Rich qualitative insights
- Can probe deeper into issues
- Observe non-verbal cues
- Clarify misunderstandings immediately

**Limitations**:
- More time-intensive (30-60 min per session)
- Researcher bias possible
- Smaller sample sizes
- Scheduling logistics

### 2. Unmoderated Testing

**Setup**: Participants complete tasks independently, recorded for later review
**Location**: Remote, on participant's own schedule

**Best for**:
- Mature products with clear tasks
- Large sample sizes needed
- Quick turnaround required
- Benchmarking and metrics

**Process**:
1. Automated instructions and consent
2. Participants record screen/audio while completing tasks
3. Automated post-task surveys
4. Researcher reviews recordings later

**Advantages**:
- Faster data collection
- Larger sample sizes
- More natural environment
- Lower cost per participant

**Limitations**:
- Can't probe or clarify
- May miss nuanced insights
- Technical issues harder to resolve
- Participants may skip think-aloud

### 3. Hybrid Approaches

**Combination methods**:
- Moderated first impressions + unmoderated task completion
- Unmoderated testing + follow-up interviews with interesting cases
- Moderated pilot + unmoderated scale testing

## Nielsen's 10 Usability Heuristics

Quick reference for evaluating interfaces. See `references/nielsens-10-heuristics.md` for detailed explanations and examples.

1. **Visibility of system status** - Keep users informed
2. **Match between system and real world** - Speak users' language
3. **User control and freedom** - Provide escape hatches
4. **Consistency and standards** - Follow platform conventions
5. **Error prevention** - Prevent problems before they occur
6. **Recognition rather than recall** - Minimize memory load
7. **Flexibility and efficiency of use** - Accelerators for experts
8. **Aesthetic and minimalist design** - Remove irrelevant information
9. **Help users recognize, diagnose, and recover from errors** - Plain language error messages
10. **Help and documentation** - Provide when needed

## Think-Aloud Protocol

### What It Is

Participants verbalize their thoughts while completing tasks, providing real-time insight into their mental model.

### Types

**Concurrent think-aloud**: Speak while performing tasks
- More natural thought flow
- May affect task performance slightly

**Retrospective think-aloud**: Review recording and explain thinking after
- Doesn't disrupt natural behavior
- May forget or rationalize thoughts

### Facilitating Think-Aloud

**Prompts to use**:
- "What are you thinking right now?"
- "What are you looking for?"
- "What would you expect to happen?"
- "Is this what you expected?"

**Don't**:
- Ask leading questions
- Provide hints or solutions
- Interrupt natural flow too often
- Make participants feel tested

See `references/think-aloud-protocol-guide.md` for detailed facilitation techniques.

## Task Scenario Design

Good task scenarios are critical to meaningful usability test results.

### Characteristics of Good Task Scenarios

**Realistic**: Based on actual user goals
**Specific**: Clear endpoint/success criteria
**Self-contained**: Provide all necessary context
**Actionable**: Clear starting point
**Not prescriptive**: Don't tell them how to do it

### Example Transformation

**Poor**: "Click on the 'My Account' link and change your password"
- Too prescriptive, tells them exactly where to click

**Good**: "You've heard about recent security breaches and want to make your account more secure. Update your account to use a stronger password."
- Realistic motivation, clear goal, doesn't prescribe path

### Task Complexity Levels

**Simple tasks** (1-2 steps): Establish baseline usability
**Medium tasks** (3-5 steps): Test core workflows
**Complex tasks** (6+ steps): Evaluate overall experience and error recovery

See `assets/task-scenario-template.md` for ready-to-use templates.

## Severity Rating Framework

Not all usability issues are equal. Prioritize fixes based on severity.

### Three-Factor Severity Rating

**Frequency**: How often does this issue occur?
- High: > 50% of users encounter
- Medium: 10-50% encounter
- Low: < 10% encounter

**Impact**: When it occurs, how badly does it affect users?
- High: Prevents task completion / causes data loss
- Medium: Causes frustration or delays
- Low: Minor annoyance

**Persistence**: Do users overcome it with experience?
- High: Problem doesn't go away
- Medium: Users learn to avoid/work around
- Low: One-time problem only

### Combined Severity Ratings

**Critical** (P0): High frequency + High impact
**Serious** (P1): High frequency + Medium impact, OR Medium frequency + High impact
**Moderate** (P2): High frequency + Low impact, OR Medium frequency + Medium impact, OR Low frequency + High impact
**Minor** (P3): Everything else

See `assets/severity-rating-guide.md` for detailed rating criteria and examples.

## Usability Metrics

### Quantitative Metrics

**Task Success Rate**: % of participants who complete task successfully
- Binary: Did they complete it? (yes/no)
- Partial credit: Did they complete most of it?

**Time on Task**: How long to complete (for successful completions)
- Compare to baseline or competitor benchmarks

**Error Rate**: Number of errors per task
- Define what counts as an error for each task

**Clicks/Taps to Task Completion**: Efficiency measure
- More relevant for well-defined tasks

### Standardized Questionnaires

**SUS (System Usability Scale)**:
- 10 questions, 5-point Likert scale
- Score 0-100 (industry avg ~68)
- Quick, reliable, easy to administer
- Good for comparing versions or benchmarking

**UMUX (Usability Metric for User Experience)**:
- 4 questions, lighter than SUS
- Similar reliability
- Faster for participants

**SEQ (Single Ease Question)**:
- "Overall, how difficult or easy was the task to complete?" (1-7)
- One question per task
- Immediate subjective difficulty rating

**Other scales**:
- SUPR-Q (for websites)
- PSSUQ (post-study)
- NASA-TLX (cognitive load)

### Qualitative Insights

**Observed behaviors**:
- Hesitations and confusion
- Error patterns
- Unexpected paths
- Verbal frustrations

**Verbalized thoughts** (think-aloud):
- Mental model mismatches
- Expectation violations
- Pleasantly surprising discoveries

## Sample Size Guidelines

### For Qualitative Insights

**Nielsen's recommendation**: 5 users finds ~85% of usability problems
- Diminishing returns after 5
- Run 3+ small rounds instead of 1 large round
- Iterate between rounds

**Reality check**:
- 5 is a minimum, not ideal
- Complex products may need 8-10
- Multiple user types need 5 each

### For Quantitative Metrics

**Benchmarking**: 20+ users per user group
**A/B testing**: Depends on effect size and desired confidence
**Statistical significance**: Use power analysis calculators

## Planning Your Usability Test

### 1. Define Objectives

What decisions will this research inform?
- Redesign priorities?
- Feature cut decisions?
- Success of recent changes?

### 2. Identify User Segments

Who needs to be tested?
- New vs. experienced users?
- Different roles or use cases?
- Different devices or contexts?

### 3. Select Tasks

What tasks represent success?
- Most critical user goals
- Most frequent tasks
- Recently changed features
- Known problem areas

### 4. Choose Methodology

Moderated, unmoderated, or hybrid?
- Consider timeline, budget, research questions

### 5. Create Test Script

See `assets/usability-test-script-template.md` for a ready-to-use structure including:
- Welcome and consent
- Background questions
- Task instructions
- Probing questions
- Wrap-up

### 6. Recruit Participants

- Define screening criteria
- Aim for 5-10 per user segment
- Plan for no-shows (recruit 20% extra)
- Offer appropriate incentives

### 7. Conduct Pilot Test

- Test with colleague or friend
- Validate timing
- Check recording setup
- Refine unclear tasks

### 8. Run Sessions

- Stay neutral and encouraging
- Observe without interfering
- Take detailed notes
- Record if permitted

### 9. Analyze and Synthesize

- Code issues by severity
- Identify patterns across participants
- Link issues to heuristics violated
- Quantify task success and time

### 10. Report and Recommend

- Prioritized issue list
- Video clips of critical issues
- Recommendations with rationale
- Quick wins vs. strategic fixes

## Integration with Product Development

### When to Test

**Discovery phase**: Test competitors or analogous products
**Concept phase**: Test paper prototypes or wireframes
**Design phase**: Test high-fidelity mockups
**Development phase**: Test working builds iteratively
**Pre-launch**: Validate before release
**Post-launch**: Identify optimization opportunities

### Continuous Usability Testing

**Build it into your process**:
- Weekly or bi-weekly test sessions
- Rotating focus (new features, established flows, mobile vs. desktop)
- Standing recruiting panel
- Lightweight reporting to team

## Ready-to-Use Templates

We provide templates to accelerate your usability testing:

### In `assets/`:
- **usability-test-script-template.md**: Complete moderator script structure
- **task-scenario-template.md**: Framework for creating effective task scenarios
- **severity-rating-guide.md**: Detailed criteria for rating usability issues

### In `references/`:
- **nielsens-10-heuristics.md**: Deep dive into each heuristic with examples
- **think-aloud-protocol-guide.md**: Advanced facilitation techniques and troubleshooting

## Common Pitfalls to Avoid

1. **Leading participants**: "Was that easy?" → "How would you describe that experience?"
2. **Testing the wrong tasks**: Tasks that aren't real user goals
3. **Over-explaining**: Let users struggle and discover issues naturally
4. **Ignoring severity**: Fixing cosmetic issues while critical issues remain
5. **Testing too late**: After it's expensive to change
6. **Not iterating**: One-and-done testing instead of continuous improvement
7. **Confusing usability with preference**: "I like green" ≠ usability issue
8. **Sample bias**: Testing only power users or only complete novices

## Further Learning

**Books**:
- "Rocket Surgery Made Easy" by Steve Krug
- "Handbook of Usability Testing" by Jeffrey Rubin
- "Moderating Usability Tests" by Joseph Dumas

**Online resources**:
- Nielsen Norman Group articles
- Usability.gov
- Baymard Institute research

---

This skill provides the foundation for conducting effective usability testing. Use the templates in `assets/` for quick starts and `references/` for deeper dives into specific techniques.
