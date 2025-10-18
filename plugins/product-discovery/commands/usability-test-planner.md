# Usability Test Planner

Plan and execute usability testing sessions to validate designs and identify user experience issues.

## Usage

```
/pm:usability-test [feature or flow] [optional: fidelity level, participant criteria]
```

## What This Command Does

1. Designs usability test plans for features, flows, or entire products
2. Creates task scenarios that simulate real user goals
3. Defines success criteria and metrics to measure usability
4. Provides participant recruitment criteria and screeners
5. Generates test scripts, facilitation guides, and observation templates
6. Takes 30 minutes vs 2 hours of manual usability test planning

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**What to Test**:
- Feature, flow, or product to test
- Fidelity level (wireframes, prototype, staging, production)
- Specific usability concerns or hypotheses
- What decisions will this test inform?

**Test Context**:
- Stage of development (discovery, design validation, pre-launch, post-launch)
- Previous research or known issues
- Competitive benchmark (optional - test yours vs competitor)

**Participants**:
- Who are your target users?
- How many participants do you need? (5-8 typical for qualitative)
- How will you recruit them?
- Any specific segment requirements?

**Constraints**:
- Timeline (when do you need results?)
- Moderated or unmoderated?
- Remote or in-person?
- Budget (for recruitment, incentives, tools)

**Example Input**:
```
Feature: New checkout flow (Figma prototype)
Goal: Validate redesigned checkout reduces friction
Concerns: Multi-step flow may be confusing, payment options unclear
Participants: 6-8 current users who've purchased before
Timeline: Need results in 1 week to inform dev sprint
Format: Remote moderated via Zoom
Budget: $50/participant incentive
```

### 2. Define Test Objectives

**What Questions Are We Answering?**:
- Can users complete [task] successfully?
- Where do users get stuck or confused?
- What's the task success rate and time on task?
- How does this compare to current design or competitors?

### 3. Design Task Scenarios

**Task Characteristics**:
- Realistic (matches real user goals)
- Specific (clear endpoint)
- Not leading (don't tell them how to do it)
- Representative (covers critical flows)

**Example**:
- ❌ Bad: "Click the checkout button and enter payment info"
- ✅ Good: "You've decided to purchase this item. Complete the purchase."

### 4. Plan Sessions

**Session Structure** (60 min typical):
- Intro (5 min)
- Background questions (5 min)
- Tasks (40 min - 4-5 tasks)
- Debrief (10 min)

**Facilitation Approach**:
- Think-aloud protocol
- Non-leading questions
- Observe without interfering

## Template

```markdown
# Usability Test Plan: [Feature/Flow Name]

**Date**: [YYYY-MM-DD]
**Test Owner**: [Your Name]
**Feature**: [What we're testing]
**Fidelity**: [Wireframes | Prototype | Staging | Production]
**Test Dates**: [Start] - [End]

---

## Test Objectives

**What We're Testing**:
[Brief description of feature/flow being tested]

**Key Questions**:
1. [Question 1 - e.g., "Can users complete checkout without assistance?"]
2. [Question 2 - e.g., "Do users understand the payment options?"]
3. [Question 3 - e.g., "Where do users encounter friction?"]

**Hypotheses**:
- **H1**: [What we think will happen - e.g., "New flow will reduce checkout time by 30%"]
- **H2**: [What we're unsure about - e.g., "Users may be confused by multi-step process"]

**Decisions This Will Inform**:
- [Decision 1 - e.g., "Ship new checkout in current form or iterate"]
- [Decision 2 - e.g., "Which payment options to prioritize"]

---

## Participants

**Target Users**:
[Description of ideal participant - role, behavior, experience level]

**Recruitment Criteria**:

**Include**:
- [Requirement 1 - e.g., "Has made at least 1 purchase in last 6 months"]
- [Requirement 2 - e.g., "Currently active user (logged in within 30 days)"]
- [Requirement 3 - e.g., "Age 25-55"]

**Exclude**:
- [Exclusion 1 - e.g., "Works in UX/design field (too expert)"]
- [Exclusion 2 - e.g., "Employee or family of employee"]
- [Exclusion 3 - e.g., "Participated in research in last 6 months"]

**Sample Size**: [X] participants
- **Rationale**: 5-8 participants typically uncover 85% of usability issues
- **Segments**: [If testing multiple user types, how many per segment]

**Incentive**: [$X gift card | Product credit | Donation to charity]

---

## Participant Screener

**Screening Survey** (5 min, send to recruitment pool):

**Q1: Product Usage**
"How often do you use [Product]?"
- [ ] Daily (CONTINUE)
- [ ] Weekly (CONTINUE)
- [ ] Monthly (CONTINUE)
- [ ] Rarely (TERMINATE)
- [ ] Never (TERMINATE)

**Q2: Purchase History**
"Have you made a purchase through [Product] in the last 6 months?"
- [ ] Yes (CONTINUE)
- [ ] No (TERMINATE - looking for users with purchase experience)

**Q3: Device Usage**
"Which devices do you use to access [Product]?"
- [ ] Desktop/Laptop
- [ ] Mobile phone
- [ ] Tablet
- [ ] Multiple devices
[NOTE: Ensure mix of device users if testing responsive design]

**Q4: Professional Background**
"Do you work in any of these fields?"
- [ ] User experience or design (TERMINATE - too expert)
- [ ] Software development (TERMINATE)
- [ ] None of the above (CONTINUE)

**Q5: Availability**
"Are you available for a 60-minute video call during [Date Range]?"
- [ ] Yes - Available times: __________
- [ ] No (TERMINATE)

**Q6: Contact Info**
- Name: __________
- Email: __________
- Phone: __________

---

## Test Tasks

**Task Design Principles**:
- Realistic scenarios (not "click here")
- Clear goal but don't prescribe solution
- Representative of real user journeys
- Prioritize critical paths

---

### Task 1: [Task Name - e.g., "Complete a Purchase"]

**Scenario**:
[Realistic context - e.g., "You've been browsing [Product Category] and found an item you want to buy. Complete the purchase."]

**Success Criteria**:
- **Task Success**: User completes checkout and reaches confirmation page
- **No Errors**: User doesn't encounter error messages or dead ends
- **Self-Recovery**: If stuck, user finds solution without help

**Metrics**:
- **Success Rate**: % who complete task
- **Time on Task**: Target <[X] seconds, Current baseline [Y] seconds
- **Errors**: Count of mistakes/wrong turns
- **Assists**: Times moderator had to help

**What to Observe**:
- Where do users hesitate?
- What do they say while completing task?
- What do they click/try that doesn't work?
- Emotional reactions (confusion, frustration, delight)

**Follow-Up Questions** (after task):
- "How easy or difficult was that?" (1-5 scale)
- "Was anything confusing or unclear?"
- "What would you change about that experience?"

---

### Task 2: [Task Name - e.g., "Find and Apply a Discount Code"]

**Scenario**:
[Context - e.g., "You have a discount code 'SAVE20'. Apply it to your purchase."]

**Success Criteria**:
- Finds discount code field
- Enters code correctly
- Sees discount applied to total

**Metrics**:
- Success Rate: [Target: >90%]
- Time on Task: [Target: <30 seconds]
- Findability: % who locate field without help

**What to Observe**:
- Do users notice the discount field?
- Is it where they expect it?
- Is the feedback clear when code is applied?

---

[Repeat for 3-5 total tasks covering critical flows]

---

## Test Script

### Introduction (5 minutes)

**Welcome**:
```
Hi [Name], thank you for joining! I'm [Your Name] and I'll be guiding you through today's session.

We're testing a new [feature/design] to see how it works for people like you. I want to emphasize: we're testing the design, not you. There are no right or wrong answers, and you can't do anything wrong.

The session will last about 60 minutes. I'll ask you to try a few tasks while thinking out loud - just tell me what you're thinking, what you're trying to do, and what you're seeing.

Do you have any questions before we start?

[Pause for questions]

Great! I'm going to start recording now so I can review this later. Is that okay?
[START RECORDING]
```

**Consent**:
- "This session is being recorded for research purposes only"
- "Your responses are confidential"
- "You can stop at any time"
- "Do you consent to participate?"

---

### Background Questions (5 minutes)

**Warm-Up Questions**:

**Q1**: "Tell me a bit about how you currently use [Product]."
- [Listen for: Frequency, use cases, context]

**Q2**: "When was the last time you [did task similar to what you're testing]?"
- [Listen for: Recency, frequency, context]

**Q3**: "What do you like most about [Product]?"
- [Listen for: What's working well - don't break it]

**Q4**: "What's most frustrating or challenging about [Product]?"
- [Listen for: Pain points your test should address]

---

### Task Instructions (40 minutes)

**Transition to Tasks**:
```
Great, thank you for that context. Now I'm going to ask you to try a few tasks using [this prototype / staging environment].

As you work, please think out loud - tell me what you're seeing, what you're thinking, what you're trying to do. If something is confusing or you're not sure what to do, that's really valuable feedback.

I'll mostly stay quiet while you work, but I may ask questions to understand your thinking.

Ready? Here's your first task...
```

**For Each Task**:

1. **Read scenario** (don't lead, don't explain UI)
2. **Observe silently** (let them struggle a bit)
3. **Probe when stuck**: "What are you thinking?" not "Click the button"
4. **Follow-up questions** after task completion

**Facilitation Reminders**:
- ✅ **DO**: "What are you looking for?", "What did you expect to happen?"
- ❌ **DON'T**: "Click the checkout button", "You're doing it wrong"

**If Participant Gets Stuck** (>2 minutes no progress):
- "If this were real, what would you do?"
- "What are you trying to accomplish right now?"
- Last resort: "Would you like a hint?" [Give minimal hint to unstick]

---

### Debrief (10 minutes)

**Overall Impressions**:

**Q1**: "Overall, how would you rate this experience?" (1-5 scale)
- 1 = Very difficult
- 5 = Very easy

**Q2**: "What worked well?"
- [Listen for: Positive surprises, moments of delight]

**Q3**: "What would you change or improve?"
- [Listen for: Top pain points, must-fix issues]

**Q4**: "How does this compare to [competitor / current version]?"
- [If applicable - competitive benchmark]

**Q5**: "Anything else you want to share?"
- [Open-ended catch-all]

**Thank You & Next Steps**:
```
That's all the questions I have. Thank you so much for your time and feedback - this is incredibly helpful.

Your [$X gift card] will be sent to [email] within [timeframe].

Do you have any questions for me?

Thanks again!
[END RECORDING]
```

---

## Observation Template

**Observer Note-Taking Guide** (if you have observers):

**For Each Task**, record:

| Participant | Task | Success (Y/N) | Time | Errors | Path Taken | Quotes | Issues |
|-------------|------|---------------|------|--------|------------|--------|--------|
| P1 | Task 1 | Y | 45s | 0 | [Steps] | "That was easy" | None |
| P1 | Task 2 | N | 120s | 2 | [Steps] | "Where is...?" | Couldn't find button |

**Issue Severity** (rate each issue observed):
- **Critical** (P0): Blocker - user cannot complete task
- **High** (P1): Major friction - user completes with significant difficulty
- **Medium** (P2): Minor friction - user notices but recovers
- **Low** (P3): Polish - cosmetic or edge case

**Patterns** (note across participants):
- "3/6 participants confused by [X]" = HIGH priority
- "1/6 mentioned [Y]" = Lower priority

---

## Test Logistics

### Schedule

| Session | Participant | Date | Time | Moderator | Observer |
|---------|-------------|------|------|-----------|----------|
| 1 | [P1 Name] | [Date] | [Time] | [Name] | [Name] |
| 2 | [P2 Name] | [Date] | [Time] | [Name] | [Name] |
| 3 | [P3 Name] | [Date] | [Time] | [Name] | [Name] |
| 4 | [P4 Name] | [Date] | [Time] | [Name] | [Name] |
| 5 | [P5 Name] | [Date] | [Time] | [Name] | [Name] |
| 6 | [P6 Name] | [Date] | [Time] | [Name] | [Name] |

**Buffer**: 30 min between sessions for notes and setup

---

### Tools & Setup

**Prototype/Environment**:
- **URL**: [Link to prototype or staging environment]
- **Access**: [Credentials if needed, or "public link"]
- **Test Data**: [Pre-populated accounts, test credit cards, etc.]

**Video Conferencing** (if remote):
- **Platform**: Zoom / Google Meet / Teams
- **Recording**: Enabled (cloud recording to [location])
- **Screen Sharing**: Participant shares their screen

**Note-Taking**:
- **Tool**: [Notion, Google Docs, Dovetail, etc.]
- **Template**: [Link to observation template]
- **Real-Time Collaboration**: Observer takes notes while moderator facilitates

**Participant Preparation** (send 1 day before):
```
Subject: Usability Test Tomorrow - What to Expect

Hi [Name],

Thank you for signing up for our usability testing session tomorrow at [Time].

Here's what to expect:
- Duration: 60 minutes
- Format: Video call (link below)
- You'll be testing a new [feature] and giving feedback
- No preparation needed - we'll guide you through everything

[VIDEO CALL LINK]

Technical requirements:
- Computer with webcam and microphone
- Stable internet connection
- Ability to share your screen

Questions? Reply to this email or call [Phone].

See you tomorrow!
[Your Name]
```

---

## Analysis Plan

### Immediate Analysis (After Each Session)

**Debrief** (15 min after session):
- What were the top 3 issues observed?
- Any surprising findings?
- What needs to be tested differently in next session?

**Update Research Tracker**:
- Log issues in severity order
- Note quotes/video timestamps for highlights
- Track patterns across participants

---

### Full Analysis (After All Sessions)

**Quantitative Summary**:

| Task | Success Rate | Avg Time | Errors | Difficulty (1-5) |
|------|--------------|----------|--------|------------------|
| Task 1 | 6/6 (100%) | 42s | 0.2 | 4.5 |
| Task 2 | 4/6 (67%) | 86s | 1.5 | 3.2 |
| Task 3 | 5/6 (83%) | 65s | 0.8 | 4.0 |

**Issue Tracking**:

| Issue | Severity | Frequency | Quote/Evidence | Recommendation |
|-------|----------|-----------|----------------|----------------|
| [Issue 1] | P0 Critical | 5/6 | "[Quote]" | [Fix before launch] |
| [Issue 2] | P1 High | 3/6 | "[Quote]" | [Must fix] |
| [Issue 3] | P2 Medium | 2/6 | "[Quote]" | [Fix if time allows] |

**Qualitative Themes**:
- [Theme 1]: [Description, frequency, evidence]
- [Theme 2]: [Description, frequency, evidence]

**Positive Findings** (What worked well):
- [Success 1]: All users loved [X]
- [Success 2]: Improved from previous design

---

### Reporting

**Executive Summary** (1 page):
- Test overview (what, who, when)
- Top 3 findings
- Recommended actions (must-fix, should-fix, nice-to-have)

**Detailed Report** (5-10 pages):
- Methodology
- Participant demographics
- Task-by-task results
- Issue severity breakdown
- Video highlight reel (3-5 min)
- Recommendations with rationale

**Presentation** (15-20 min for stakeholders):
- Research question
- Key findings (show video clips)
- Recommended design changes
- Next steps (re-test, ship, iterate)

---

## Success Metrics

**Test Execution**:
- [ ] Recruited [X] qualified participants
- [ ] Completed [X] sessions without technical issues
- [ ] Captured notes/recordings for all sessions
- [ ] Analyzed within [X] days of last session

**Research Quality**:
- [ ] Uncovered [X]+ usability issues
- [ ] Identified clear pattern (3+ participants experiencing same issue)
- [ ] Gathered actionable insights for design iteration
- [ ] Stakeholders attended live sessions or watched clips

**Impact**:
- [ ] Findings inform design decisions
- [ ] Critical issues fixed before launch
- [ ] Baseline metrics established for future comparison

```

---

## Best Practices

### DO ✅

- **Test early and often** - Test low-fidelity prototypes, not just finished products
- **Recruit real users** - Friends/family are not representative
- **Facilitate neutrally** - Don't lead, don't defend the design
- **Encourage thinking aloud** - "Tell me what you're thinking"
- **Let users struggle** - Don't jump in immediately when they're stuck
- **Record sessions** - You can't remember everything, video is invaluable
- **Test 5-8 participants** - Enough to find patterns, not so many you're overwhelmed
- **Fix critical issues immediately** - Don't wait to test again with broken design

### DON'T ❌

- **Don't explain the UI** - If you have to explain it, it's not intuitive
- **Don't ask leading questions** - "Don't you think this is easy?" biases response
- **Don't defend the design** - "Actually, that button is there because..." shuts down feedback
- **Don't test too much** - 4-5 tasks max, or fatigue sets in
- **Don't ignore patterns** - If 3+ people struggle with same thing, it's a real issue
- **Don't only test happy path** - Test error cases, edge cases too
- **Don't skip analysis** - Recording sessions but not analyzing is wasted effort

---

## Examples

### Example 1: Checkout Flow Test

**Input**: "Test new checkout flow prototype with 6 users"

**Output**:

```markdown
# Usability Test: New Checkout Flow

**Participants**: 6 current users who've purchased before
**Format**: Remote moderated, 60 min sessions
**Fidelity**: Figma prototype

## Tasks:
1. **Complete a purchase** (Success target: 100%, Time: <90s)
2. **Apply a discount code** (Success target: >90%, Time: <30s)
3. **Update payment method** (Success target: >80%)
4. **Review order before confirming** (Success target: 100%)

## Key Findings:
- **Critical (P0)**: 4/6 users couldn't find "Apply Code" button (hidden in collapsed section)
- **High (P1)**: 3/6 confused by multi-step progress indicator
- **Positive**: All users loved one-click address autofill

## Recommendations:
1. **Must Fix**: Make discount code field visible by default (launches with fix)
2. **Should Fix**: Simplify progress indicator to 2 steps instead of 4
3. **Nice-to-Have**: Add estimated delivery date earlier in flow
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:survey` - Quantitative research to complement usability testing
- `/pm:interview-guide` - User interviews for discovery research
- `/pm:research-synthesis` - Synthesize usability findings with other research
- `/workflows:discovery-sprint` - Use usability testing in solution validation
- `user-researcher` agent - Research methodology and test design
- `ui-ux-designer` agent - Design iteration based on usability findings
