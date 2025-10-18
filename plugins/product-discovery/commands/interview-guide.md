# Interview Guide Generator

Create structured user interview guides for discovery, validation, and continuous research with research objectives and thoughtful question flows.

## Usage

```
/pm:interview-guide [research objective] [optional: participant type, research phase]
```

## What This Command Does

1. Generates comprehensive interview protocols with objectives, screening, and question flows
2. Structures questions using best practices (open-ended, behavioral, non-leading)
3. Creates follow-up probes to dig deeper into user responses
4. Balances discovery (understanding current state) and validation (testing solutions)
5. Includes logistics, consent, and ethics considerations
6. Takes 30 minutes vs 2 hours of manual interview guide creation

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Research Context**:
- What's the research objective? (what you want to learn)
- What phase of research? (discovery, validation, usability testing)
- What decisions will this research inform? (roadmap, design, feature prioritization)
- What hypotheses are you testing? (if validation research)

**Participant Context**:
- Who should you interview? (user segments, personas, roles)
- How will you recruit? (user list, screening survey, referrals)
- How many interviews? (typically 5-15 for qualitative insights)
- Any compensation? (incentive amount, delivery method)

**Interview Logistics**:
- How long should interviews be? (30 min, 45 min, 60 min)
- Where will interviews happen? (remote video, in-person, phone)
- Who conducts interviews? (PM, researcher, multiple people)
- Will you record? (audio, video, screen recording)

**Topic Context**:
- What product/feature are you researching?
- What do you already know? (existing research, analytics)
- What gaps exist? (what you don't know yet)
- Any constraints? (sensitive topics, competitive intelligence)

**Example Input**:
```
Objective: Understand why sales managers abandon trial onboarding before first value
Phase: Discovery (identifying pain points)
Participants: Sales managers who signed up for trial but didn't complete onboarding (churned users)
Recruitment: Email list of 200 churned trial users, offer $50 Amazon gift card
Sample size: 12-15 interviews
Duration: 45 minutes per interview
Format: Remote (Zoom), recorded with consent
Hypotheses: (1) Onboarding is too complex, (2) Value prop isn't clear, (3) Integration setup is blocker
```

### 2. Define Research Objectives

**Types of Research Objectives**:

**A. Discovery (Exploratory)**:
- Understand current behaviors and workflows
- Identify pain points and frustrations
- Learn about goals and motivations
- Map the customer journey

**B. Validation (Evaluative)**:
- Test solution concepts or prototypes
- Validate problem hypotheses
- Assess willingness to pay
- Evaluate competitive positioning

**C. Usability (Tactical)**:
- Test specific features or flows
- Identify usability issues
- Measure task success
- Gather feedback on design

**D. Continuous (Ongoing)**:
- Stay connected to users
- Track evolving needs
- Monitor competitive landscape
- Identify emerging opportunities

### 3. Structure Interview Flow

**Standard Interview Structure** (60 min example):

1. **Introduction** (5 min): Consent, context, expectations
2. **Warm-up** (5 min): Build rapport, ease into conversation
3. **Main Questions** (40 min): Core research questions
4. **Wrap-up** (10 min): Final thoughts, referrals, thanks

**Time Allocation Rules**:
- Never plan for 100% of time (always goes over)
- Plan for 80% of allocated time (45 min interview = 35 min questions)
- Build in buffer for tangents and follow-ups

### 4. Write Effective Questions

**Question Types**:

**A. Behavioral Questions** (Past behavior predicts future):
- "Tell me about the last time you..." (specific instance)
- "Walk me through how you..." (process)
- "Describe a recent situation where..." (context)

**B. Open-Ended Questions** (Not yes/no):
- "What..." (exploration)
- "How..." (process)
- "Why..." (rationale - use sparingly, can feel defensive)

**C. Probing Questions** (Dig deeper):
- "Tell me more about that"
- "What happened next?"
- "How did that make you feel?"
- "Can you give me an example?"

**Question Writing Principles**:
- ✅ **DO**: Use open-ended questions ("What challenges do you face with...")
- ❌ **DON'T**: Use leading questions ("Don't you think it would be better if...")
- ✅ **DO**: Ask about past behavior ("Last time you...")
- ❌ **DON'T**: Ask hypothetical ("Would you use...")
- ✅ **DO**: Stay neutral ("What do you think about...")
- ❌ **DON'T**: Show bias ("We think this is great, don't you?")

### 5. Create Follow-Up Probes

**Probing Techniques**:
- **Clarification**: "Can you explain what you mean by that?"
- **Elaboration**: "Tell me more about that"
- **Example**: "Can you give me a specific example?"
- **Emotion**: "How did that make you feel?"
- **Comparison**: "How does that compare to..."
- **Silence**: (Wait 3-5 seconds - participant often fills the gap with gold)

## Template

```markdown
# Interview Guide: [Research Topic]

**Created**: [YYYY-MM-DD]
**Researcher**: [Your Name]
**Research Phase**: [Discovery | Validation | Usability | Continuous]

---

## Research Overview

### Objectives

**Primary Research Question**: [One sentence - what you're trying to learn]

**Secondary Questions**:
1. [Supporting question 1]
2. [Supporting question 2]
3. [Supporting question 3]

**Hypotheses to Test** (if validation research):
- **H1**: [Hypothesis 1 - e.g., "Users abandon onboarding because it's too complex"]
- **H2**: [Hypothesis 2 - e.g., "Value proposition is unclear during trial"]

**Key Decisions This Research Informs**:
- [Decision 1 - e.g., "Whether to rebuild onboarding flow"]
- [Decision 2 - e.g., "Which features to prioritize in Q2"]

---

## Participant Profile

### Screening Criteria

**Must-Have Requirements**:
- [Requirement 1 - e.g., "Sales manager role (manages 5+ people)"]
- [Requirement 2 - e.g., "Signed up for trial in last 90 days"]
- [Requirement 3 - e.g., "Did NOT complete onboarding (churned before first value)"]

**Nice-to-Have**:
- [Preference 1 - e.g., "Uses Salesforce (our primary integration)"]
- [Preference 2 - e.g., "Team size 10-50 (mid-market segment)"]

**Exclusions**:
- [Exclude 1 - e.g., "Current paid customers (different mindset)"]
- [Exclude 2 - e.g., "Employees or family of employees"]

**Diversity Goals**:
- Mix of company sizes (small, mid-market, enterprise)
- Mix of industries (if relevant)
- Mix of experience levels (new managers vs seasoned)

### Recruitment

**Source**: [Where to find participants - e.g., "Email list of churned trial users"]

**Outreach Message**:
> Subject: Help improve [Product] - $50 Amazon gift card
>
> Hi [Name],
>
> I noticed you recently tried [Product]. We're conducting research to better understand the trial experience and would love to hear your honest feedback.
>
> **What**: 45-minute video call about your experience
> **When**: [Date/time options]
> **Compensation**: $50 Amazon gift card
>
> Your insights will directly shape product improvements. Interested?
>
> [Calendar link]

**Screening Survey** (if needed):
1. What's your job title?
2. How many people report to you?
3. When did you sign up for [Product] trial?
4. Why did you sign up?
5. Did you complete onboarding? (Yes/No - filter for "No")

**Sample Size**: [Target number - e.g., "12-15 interviews (saturation typically at 12)"]

---

## Interview Logistics

**Duration**: [Total time - e.g., "60 minutes (plan for 50 min of questions)"]

**Format**: [Remote video (Zoom) | In-person | Phone]

**Recording**:
- [ ] Audio recording (required for transcription)
- [ ] Video recording (if observing non-verbal cues)
- [ ] Screen recording (if showing prototype or asking to demo tool)

**Compensation**: [Amount and delivery - e.g., "$50 Amazon gift card, sent within 48 hours"]

**Tools Needed**:
- Video conferencing (Zoom, Google Meet)
- Note-taking app (Notion, Google Docs)
- Recording software (Zoom built-in, Grain.co, Otter.ai)
- Prototype or materials (if validation research)

**Team**:
- **Interviewer**: [Who asks questions - typically PM or researcher]
- **Note-taker**: [Who takes notes - optional but recommended]
- **Observers**: [Stakeholders who silently observe - optional]

---

## Interview Protocol

### Pre-Interview Checklist

**24 Hours Before**:
- [ ] Send calendar invite with Zoom link
- [ ] Send reminder email with what to expect
- [ ] Prepare prototype/materials (if needed)
- [ ] Review participant background
- [ ] Test recording setup

**5 Minutes Before**:
- [ ] Start Zoom, test audio/video
- [ ] Open note-taking doc
- [ ] Review research objectives
- [ ] Take deep breath (stay curious, not defensive)

---

### Interview Script

#### Introduction (5 minutes)

**[Join Zoom, greet warmly]**

> "Hi [Name]! Thanks so much for joining me today. Can you hear me okay? Great!
>
> Before we start, I want to give you some context and get your consent for a few things.
>
> **What we're doing today**: I'm a product manager at [Company], and we're trying to understand the trial experience better. I'm going to ask you about your experience signing up and trying [Product]. There are no right or wrong answers - I genuinely want to hear your honest thoughts, even if it's critical.
>
> **Recording**: I'd like to record our conversation so I can go back and listen carefully later. The recording is only for internal research purposes and won't be shared outside our team. Is that okay with you? [Wait for consent]
>
> **Confidentiality**: Nothing you say will be attributed to you by name in any reports or presentations. We'll anonymize all feedback.
>
> **How this works**: I'll ask you questions about your experience. Please feel free to be completely honest - I'm not here to sell you anything or convince you to use the product. Your candid feedback is incredibly valuable.
>
> **Questions before we start?** [Pause for questions]
>
> Great! Let's dive in."

**[Start recording if consented]**

---

#### Warm-Up (5 minutes)

**Goal**: Build rapport, ease into conversation, gather context

**Questions**:

1. **Tell me a bit about your role**
   - **Probe**: What does a typical day look like for you?
   - **Probe**: How long have you been in this role?

2. **What are your main responsibilities?**
   - **Probe**: What takes up most of your time?
   - **Probe**: What metrics are you measured on?

**[Transition]**: "Thanks for that context! Now I'd like to hear about your experience with [Product]..."

---

#### Main Questions (40 minutes)

---

##### Section 1: Background & Context (10 minutes)

**Goal**: Understand what led them to try your product

**Question 1**: **How did you first hear about [Product]?**
- **Probe**: What were you doing when you heard about it?
- **Probe**: What was your initial impression?

**Question 2**: **What prompted you to sign up for the trial?**
- **Probe**: What problem were you trying to solve?
- **Probe**: What were you hoping to achieve?
- **Note-taking focus**: Listen for "job to be done"

**Question 3**: **Were you evaluating other solutions at the same time?**
- **Probe**: Which other tools did you consider?
- **Probe**: How did you compare them?
- **Note-taking focus**: Competitive landscape

**Question 4**: **Walk me through the moment you decided to sign up**
- **Probe**: Where were you? (at desk, on phone, etc.)
- **Probe**: What happened right before?
- **Probe**: What happened right after?
- **Note-taking focus**: Trigger event, context

---

##### Section 2: Trial Experience (15 minutes)

**Goal**: Understand trial experience step-by-step

**Question 5**: **Walk me through what happened after you signed up**
- **Probe**: What was the first screen you saw?
- **Probe**: What did you try to do first?
- **Probe**: How did that go?
- **Note-taking focus**: First impressions, onboarding flow

**Question 6**: **What were you trying to accomplish during the trial?**
- **Probe**: Did you have a specific goal in mind?
- **Probe**: How far did you get toward that goal?
- **Note-taking focus**: Success criteria, expectations

**Question 7**: **Tell me about any moments where you got stuck or frustrated**
- **Probe**: What were you trying to do when that happened?
- **Probe**: How did you try to solve it?
- **Probe**: Did you reach out for help? (support, docs, etc.)
- **Note-taking focus**: Pain points, friction, abandonment triggers

**Question 8**: **What did you find confusing or unclear?**
- **Probe**: Can you give me a specific example?
- **Probe**: What did you expect vs what actually happened?
- **Note-taking focus**: Expectation mismatches

**Question 9**: **At what point did you stop using the trial?**
- **Probe**: Do you remember the specific moment?
- **Probe**: What was the trigger to stop?
- **Probe**: Did you plan to come back? (if yes, why didn't you?)
- **Note-taking focus**: Churn moment, abandonment reason

---

##### Section 3: Alternatives & Workarounds (10 minutes)

**Goal**: Understand what they did instead

**Question 10**: **What are you using now to solve [problem]?**
- **Probe**: How's that working out?
- **Probe**: What do you like about it?
- **Probe**: What do you dislike about it?
- **Note-taking focus**: Current solution, job to be done

**Question 11**: **If we could wave a magic wand and make [Product] perfect for you, what would change?**
- **Probe**: What's the most important thing?
- **Probe**: Why is that important to you?
- **Note-taking focus**: Unmet needs, feature requests

**Question 12**: **Would you ever consider trying [Product] again?**
- **Probe**: What would need to change for you to give it another shot?
- **Probe**: What would convince you it's worth your time?
- **Note-taking focus**: Re-engagement opportunities

---

##### Section 4: Validation (5 minutes) - **[Optional, skip if discovery-only]**

**Goal**: Test solution concepts if you have them

**[If you have prototype/concept to show]**:

> "Thanks for sharing all that. Based on feedback from you and others, we're considering some changes. I'd love to show you a quick concept and get your reaction. Remember, this is very rough - focus on the idea, not the polish."

**[Share screen with prototype]**

**Question 13**: **What's your initial reaction to this?**
- **Probe**: What stands out to you (positive or negative)?
- **Silence**: [Wait 5-10 seconds, let them process]

**Question 14**: **How would this fit into your workflow?**
- **Probe**: Walk me through how you'd use this
- **Probe**: What would make this more useful?

**Question 15**: **What concerns or questions do you have about this approach?**
- **Probe**: What would stop you from using this?
- **Note-taking focus**: Objections, gaps

---

#### Wrap-Up (10 minutes)

**Goal**: Final insights, referrals, gratitude

**Question 16**: **Is there anything we haven't talked about that you think I should know?**
- **Silence**: [Give them 10 seconds to think]
- **Probe**: Anything you expected me to ask but I didn't?

**Question 17**: **Who else do you think I should talk to?**
- **Probe**: Anyone on your team who tried the product?
- **Probe**: Anyone in your network who has similar needs?
- **Note-taking focus**: Referrals for recruitment

**[Closing]**:
> "This has been incredibly helpful - thank you for being so candid. Your feedback will directly influence what we build next.
>
> **Next steps**:
> - I'll send you a $50 Amazon gift card within 48 hours
> - If you're interested, I can follow up with you when we make improvements based on this research
> - Feel free to email me anytime with additional thoughts: [your email]
>
> Thanks again!"

**[Stop recording]**

---

## Post-Interview

### Immediately After (15 minutes)

**While fresh in memory**:
- [ ] Write down top 3 insights
- [ ] Flag any surprising quotes
- [ ] Note any follow-up questions for next interviews
- [ ] Jot down emotions/body language observed

**Debrief Questions** (if note-taker present):
- What stood out to you?
- What surprised you?
- Any patterns emerging across interviews?

---

### Follow-Up Actions

**Within 24 Hours**:
- [ ] Send thank you email with gift card
- [ ] Add notes to research synthesis doc
- [ ] Share key insights with team (if urgent)

**Within 48 Hours**:
- [ ] Transcribe interview (use Otter.ai, Rev, or manual)
- [ ] Tag/code themes
- [ ] Add to research repository

**After All Interviews Complete**:
- [ ] Synthesize findings across all interviews
- [ ] Create research report
- [ ] Present to stakeholders
- [ ] Convert insights into roadmap items

---

## Interview Facilitation Tips

### DO ✅

- **Listen more than you talk** (80/20 rule)
- **Ask "why" 3 times** (dig to root cause)
- **Embrace silence** (wait 5 seconds after they finish - often they'll add gold)
- **Follow tangents** (if interesting, explore it)
- **Stay curious, not defensive** (even if feedback hurts)
- **Take notes on emotions** (frustration, excitement, confusion)
- **Ask for examples** ("Can you give me a specific instance?")
- **Validate their experience** ("That sounds frustrating")

### DON'T ❌

- **Don't lead the witness** ("Don't you think X would be better?")
- **Don't defend the product** ("Well, actually, that feature exists...")
- **Don't interrupt** (let them finish, even if rambling)
- **Don't ask hypotheticals** ("Would you use this if...")
- **Don't ask yes/no questions** (turn into open-ended)
- **Don't pitch or sell** (you're here to learn, not convince)
- **Don't rush** (comfortable silence is okay)
- **Don't assume** (ask even if it seems obvious)

---

## Question Bank (Adapt to Your Needs)

### Discovery Questions

**Current Behavior**:
- "Walk me through the last time you [did task]"
- "How often do you [activity]?"
- "What triggers you to [action]?"
- "Describe a typical [workflow]"

**Pain Points**:
- "What's most frustrating about [current process]?"
- "Tell me about a time when [problem occurred]"
- "What workarounds have you developed?"
- "If you had a magic wand, what would you change?"

**Goals & Motivations**:
- "What are you trying to achieve when you [task]?"
- "How do you measure success?"
- "What does 'better' look like?"
- "Why is this important to you?"

**Tools & Alternatives**:
- "What tools do you currently use for this?"
- "How did you solve this before [tool]?"
- "What do you like/dislike about [current solution]?"

### Validation Questions

**Reaction**:
- "What's your initial reaction?"
- "What stands out to you?"
- "How does this compare to what you use now?"

**Usage**:
- "How would you use this?"
- "Walk me through how this would fit into your workflow"
- "What would you use this for first?"

**Value**:
- "How would this make your life better?"
- "How much time would this save you?"
- "What would you be willing to pay for this?"

**Concerns**:
- "What concerns do you have?"
- "What would stop you from using this?"
- "What's missing?"

---

## Ethics & Best Practices

### Informed Consent

**Always Get Consent For**:
- Recording (audio/video)
- Note-taking
- Observation by others
- Use of quotes in reports
- Sharing with external partners

**Participant Rights**:
- Can decline to answer any question
- Can stop interview at any time
- Can request recording be deleted
- Can withdraw consent after interview

### Compensation

**Fair Compensation**:
- Pay for participant's time (typical: $50-150 for 45-60 min)
- Send promptly (within 48 hours)
- Don't make compensation contingent on "right" answers

### Privacy

**Protect Participant Data**:
- Anonymize transcripts (remove names, companies)
- Store recordings securely
- Don't share recordings outside research team
- Delete recordings after transcription (or set retention policy)

---

```

---

## Best Practices

### DO ✅

- **Pilot test your guide** - Run 1-2 test interviews, refine questions
- **Stay flexible** - Don't be rigid to script, follow interesting threads
- **Record everything** - You can't remember it all, recordings are gold
- **Take breaks** - Don't schedule back-to-back interviews (mental drain)
- **Involve stakeholders** - Invite eng, design, CS to observe
- **Iterate** - Refine questions after first 3-5 interviews based on learnings
- **Show empathy** - Validate participant's frustrations
- **End on time** - Respect their schedule

### DON'T ❌

- **Don't ask leading questions** - "Don't you think X is better?" is biased
- **Don't defend your product** - You're here to learn, not sell
- **Don't skip warm-up** - Cold starts lead to shallow answers
- **Don't multi-task** - Give participant your full attention
- **Don't forget compensation** - Send gift card promptly
- **Don't ignore contradictions** - Probe when answers don't match behavior
- **Don't interview only fans** - Talk to churned users, skeptics, non-users
- **Don't forget to synthesize** - Interviews are useless if insights aren't shared

---

## Model

Use: Sonnet

---

## Related

- `/pm:persona` - Create personas from interview insights
- `/pm:research-synthesize` - Synthesize interview findings
- `/pm:journey-map` - Map customer journey from interviews
- `/pm:user-stories` - Convert insights into user stories
- `/pm:usability-test` - Create usability test plan
- `/workflows:research-to-product` - Full research-to-roadmap workflow
- `user-researcher` agent - Research methodology and best practices
- `customer-insights` agent - Analyze interview data
