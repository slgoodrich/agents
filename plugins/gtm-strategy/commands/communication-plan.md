# Communication Plan

Create stakeholder communication strategy for initiatives, launches, and changes.

## Usage

```
/gtm-strategy:comm-plan [initiative or change] [stakeholders]
```

## What This Command Does

1. Maps stakeholders and their communication needs
2. Defines communication channels, cadence, and messaging
3. Creates message templates for different audiences
4. Establishes feedback loops and two-way communication
5. Plans timeline for rolling out communications
6. Takes 30 minutes vs 2 hours of manual communication planning

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Initiative Context**:
- What are you communicating? (product launch, feature update, pricing change, policy change, incident/outage, organizational change)
- Why is this communication needed now? (what's the trigger or urgency)
- What's the scope and impact? (how big is this change, who's affected)
- What are the business goals? (adoption, awareness, compliance, retention)

**Stakeholder Context**:
- Who needs to know? (customers, internal teams, partners, investors, press, public)
- How many people in each stakeholder group? (scale of communication)
- What do they care about? (what's in it for them, what concerns will they have)
- How do they prefer to receive information? (email, Slack, meeting, blog, etc.)
- Who has decision authority? (who needs to approve messaging)

**Timeline & Urgency**:
- When does this need to be communicated? (specific date or ASAP)
- How much lead time do stakeholders need? (to prepare, react, adopt)
- Are there dependencies? (must announce before/after something else)
- What's the rollout timeline? (all at once vs phased)

**Messaging Context**:
- What's the core message? (the one thing everyone should understand)
- Is this good news, bad news, or neutral? (affects tone and approach)
- What concerns or objections do you expect? (so we can address proactively)
- Are there legal/compliance requirements? (mandatory disclosures, opt-in language)

**Channels & Resources**:
- What communication channels are available? (email lists, Slack, blog, in-app, etc.)
- Who owns each channel? (who can send emails, publish blogs, etc.)
- What's the budget? (for paid channels, webinars, events)
- Who's involved in creating content? (PM, marketing, legal, etc.)

**Previous Communications** (if applicable):
- Have we communicated about this before? (is this an update or follow-up)
- What worked well or poorly in past communications? (learn from history)
- Are there templates or examples to reference?

**Example Input**:
```
Initiative: Pricing change (15% increase)
Stakeholders: Existing customers, sales team, CS team, internal
When: Announce in 2 weeks, effective in 8 weeks
Key Message: Increased value justifies price, grandfathered rates available
```

### 2. Map Stakeholders

**By Segment**:
- Customers (existing, prospects, churned)
- Internal teams (sales, CS, eng, marketing)
- Partners
- Press/Analysts
- Investors/Board

**By Impact Level**:
- High impact: Directly affected, needs detailed info
- Medium impact: Indirectly affected, needs awareness
- Low impact: FYI only

### 3. Define Messaging

**Core Message** (What everyone hears):
- What's changing
- Why it matters
- What to do

**Tailored Messages** (Per audience):
- Different benefits/implications per stakeholder
- Address specific concerns
- Relevant call to action

### 4. Choose Channels

**By Stakeholder Preference**:
- Email (formal updates)
- Slack/Teams (quick updates, Q&A)
- All-hands (major announcements)
- 1-on-1 (sensitive topics)
- Help center/Docs (reference)
- Blog/PR (public announcements)

### 5. Set Cadence

**Announcement Timeline**:
- Pre-announcement (select stakeholders)
- Main announcement (all stakeholders)
- Follow-up (Q&A, reinforcement)
- Ongoing updates (as needed)

## Template

```markdown
# Communication Plan: [Initiative Name]

**Date**: [YYYY-MM-DD]
**Owner**: [Your Name]
**Initiative**: [Brief description]
**Communication Timeline**: [Start] - [End]

---

## Executive Summary

**What we're communicating**:
[One sentence: what's changing/launching]

**Why it matters**:
[Business impact, user impact, strategic importance]

**Who needs to know**:
[X] customers, [Y] internal stakeholders, [Z] partners

**Communication Window**: [Start Date] - [End Date]

---

## Stakeholder Map

| Stakeholder Group | Size | Impact Level | Primary Concern | Channel |
|-------------------|------|--------------|-----------------|---------|
| Existing Customers | [X] | High | [What they care about] | Email, In-app |
| Sales Team | [X] | High | [How to sell it] | Slack, Training |
| CS Team | [X] | High | [How to support] | Slack, Training |
| Engineering | [X] | Medium | [Technical details] | All-hands |
| Marketing | [X] | Medium | [How to message] | Meeting |
| Partners | [X] | Low | [Awareness] | Email |

---

## Core Messaging

### Key Messages (Everyone Hears)

**What**:
[One sentence: what's changing]

**Why**:
[One sentence: why this change]

**When**:
[Timeline: when it happens]

**What to Do**:
[Call to action: what stakeholders should do]

---

### Message Framing

**Positive Framing**:
- [Benefit 1]
- [Benefit 2]
- [Value created]

**Addressing Concerns**:
- **Concern**: [Common objection]
  - **Response**: [How we address it]
- **Concern**: [Common objection]
  - **Response**: [How we address it]

---

## Tailored Messaging by Stakeholder

### For Customers

**What They Care About**: [Value, pricing, features]

**Message**:
[Tailored message emphasizing customer benefits]

**Key Points**:
- [Point 1 relevant to customers]
- [Point 2 relevant to customers]
- [Point 3 relevant to customers]

**Call to Action**: [What you want customers to do]

**Concerns to Address**:
- [Concern 1]: [Response]
- [Concern 2]: [Response]

---

### For Sales Team

**What They Care About**: [How to sell, objection handling]

**Message**:
[Tailored message for sales context]

**Key Points**:
- [How this helps close deals]
- [New value props to emphasize]
- [Updated pricing/positioning]

**Enablement Needed**:
- [ ] Updated sales deck
- [ ] Objection handling guide
- [ ] Demo talking points
- [ ] Competitive positioning

---

### For Internal Teams

**What They Care About**: [Impact on their work]

**Message**:
[Tailored message for internal context]

**Key Points**:
- [How this affects their day-to-day]
- [What they need to do differently]
- [Support available]

---

## Communication Timeline

### Week -2: Pre-Announcement (Confidential)

**Audience**: Leadership, key stakeholders
**Channel**: 1-on-1 meetings, confidential brief
**Purpose**: Early heads-up, gather feedback, align messaging

**Activities**:
- [ ] Brief CEO/leadership
- [ ] Align with sales/CS leads
- [ ] Finalize messaging based on feedback

---

### Week -1: Internal Announcement

**Audience**: All internal teams
**Channel**: All-hands meeting, Slack
**Purpose**: Inform before customers hear

**Activities**:
- [ ] All-hands announcement
- [ ] Q&A session
- [ ] Distribute internal FAQ
- [ ] Train customer-facing teams

**Message**: [Link to internal announcement]

---

### Week 0: Public Announcement

**Audience**: Customers, partners, public
**Channel**: Email, blog, in-app, social
**Purpose**: Main announcement

**Activities**:
- [ ] Email to all customers
- [ ] Blog post published
- [ ] In-app notification
- [ ] Social media posts
- [ ] Press release (if applicable)

**Message**: [Link to public announcement]

---

### Week 1-2: Follow-Up & Q&A

**Audience**: Responders, concerned stakeholders
**Channel**: Email, Slack, 1-on-1
**Purpose**: Address questions, reinforce messaging

**Activities**:
- [ ] Respond to customer questions
- [ ] Host customer webinar/Q&A
- [ ] Update FAQ based on questions
- [ ] 1-on-1 with at-risk accounts

---

### Ongoing: Reinforcement

**Frequency**: Weekly/Monthly
**Channel**: Newsletter, updates, reminders
**Purpose**: Keep stakeholders informed of progress

**Activities**:
- [ ] Progress updates
- [ ] Success stories
- [ ] Reminder of upcoming changes

---

## Message Templates

### Email Template: Customers

```
Subject: [Subject Line - Clear, Benefit-Focused]

Hi [Name],

[Personalized opening - acknowledge relationship]

**What's Changing**:
[One sentence: the change]

**Why This Matters to You**:
[Benefits relevant to this customer]

**What You Need to Do**:
[Clear call to action, deadline if applicable]

**Timeline**:
- [Date]: [Milestone]
- [Date]: [Milestone]

**Questions?**
[How to get help - link to FAQ, support email]

Thank you for being a valued customer.

[Your Name]
```

---

### Slack Template: Internal Teams

```
📢 **Announcement: [Initiative Name]**

**TL;DR**: [One sentence summary]

**What**: [Brief description]
**Why**: [Rationale]
**When**: [Timeline]

**What You Need to Do**:
1. [Action 1]
2. [Action 2]

**Questions?** Thread below or ping [Name] 👇
```

---

### Blog Post Template: Public

```
# [Title - SEO Optimized, Benefit-Focused]

**Summary**: [One sentence hook]

[Intro paragraph - why we're making this change]

## What's New

[Description of change/launch]

## Why We're Doing This

[Business rationale, customer benefit]

## What This Means for You

[Impact on users, specific benefits]

## How to Get Started

[Call to action, next steps]

## FAQs

**Q: [Common question]**
A: [Clear answer]

[Repeat for top 5 questions]

## Questions?

[How to reach us for more info]
```

---

## Channels & Tactics

### Email

**Use For**: Formal announcements, detailed info, legal notices
**Frequency**: One-time announcement + 1-2 follow-ups
**Best Practices**:
- Clear subject line
- TL;DR at top
- Scannable bullets
- Clear CTA

---

### Slack/Teams

**Use For**: Quick updates, Q&A, informal communication
**Frequency**: Real-time during announcement period
**Best Practices**:
- Pin important messages
- Use threads for Q&A
- React to show acknowledgment

---

### Blog Post

**Use For**: Public announcements, SEO, thought leadership
**Timing**: Day of announcement
**Distribution**: Email, social, in-app link

---

### In-App Notification

**Use For**: Reach active users where they are
**Timing**: Day of announcement, remind 1 week before deadline
**Best Practices**:
- Brief message with link to details
- Dismissible but persistent
- Clear CTA

---

### Webinar/Q&A

**Use For**: Complex changes, customer education
**Timing**: 1 week after announcement
**Format**: 30 min presentation + 30 min Q&A
**Recording**: Available for those who can't attend

---

## Feedback Loops

### How We'll Gather Feedback

**Surveys**:
- Send to [X]% of customers
- Ask: Clarity, sentiment, concerns
- Timeline: 1 week after announcement

**Support Tickets**:
- Monitor ticket volume and themes
- Flag common questions for FAQ update

**Sales/CS Feedback**:
- Weekly check-in with frontline teams
- What questions are they hearing?
- What concerns are customers raising?

**Metrics**:
- Email open/click rates
- Blog post traffic
- In-app notification dismiss rate
- Support ticket volume

---

### How We'll Respond

**Quick Response** (<24 hours):
- Critical concerns
- Widespread confusion
- Negative sentiment spike

**Updates to Messaging**:
- Add to FAQ if >5 people ask
- Clarify if confusion detected
- Add examples if needed

**Course Correction**:
- If [X]% negative feedback → Reconsider approach
- If [Y]% don't understand → Simplify messaging

---

## Success Criteria

**Communication Success** (measured 2 weeks post-announcement):

- [ ] [X]% of stakeholders aware (survey or confirm receipt)
- [ ] [Y]% understand change (comprehension check)
- [ ] <[Z]% negative sentiment (sentiment analysis)
- [ ] <[W] support tickets about change
- [ ] All customer-facing teams trained

**Outcome Success** (measured 4 weeks post-change):

- [ ] [Desired outcome metric 1]
- [ ] [Desired outcome metric 2]

---

## Risks & Mitigation

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| [Risk 1: e.g., Customer backlash] | [H/M/L] | [H/M/L] | [How we'll handle] |
| [Risk 2: e.g., Message misunderstood] | [H/M/L] | [H/M/L] | [Clarity improvements] |
| [Risk 3: e.g., Internal teams unprepared] | [H/M/L] | [H/M/L] | [Training plan] |

---

## Roles & Responsibilities

| Role | Responsible For | Owner |
|------|-----------------|-------|
| PM | Overall communication plan, messaging | [Name] |
| Marketing | Blog post, social, PR | [Name] |
| CS | Customer outreach, support | [Name] |
| Sales | Sales enablement, deals at risk | [Name] |
| Eng | Technical details, implementation | [Name] |

---

## Checklist

### Before Announcement

- [ ] Stakeholder map complete
- [ ] Messaging finalized and approved
- [ ] Templates created for all channels
- [ ] FAQ drafted
- [ ] Internal teams trained
- [ ] Customer-facing teams have talking points

### Announcement Day

- [ ] Email sent
- [ ] Blog post published
- [ ] In-app notification live
- [ ] Social media posted
- [ ] Internal announcement made
- [ ] Monitoring started (tickets, sentiment)

### Post-Announcement

- [ ] Q&A sessions scheduled
- [ ] Feedback being collected
- [ ] FAQ updated based on questions
- [ ] Success metrics tracked
```

---

## Best Practices

### DO ✅

- **Communicate early** - Give stakeholders time to prepare
- **Tailor messaging** - Different audiences, different messages
- **Two-way communication** - Listen and respond, don't just broadcast
- **Internal first** - Team hears it from you before customers
- **Clear CTAs** - Tell people what to do next
- **Track feedback** - Monitor and respond to concerns
- **Follow up** - Reinforce message, answer questions

### DON'T ❌

- **Surprise people** - Unexpected announcements breed distrust
- **One-size-fits-all** - Same message to customers and engineers fails
- **Ignore feedback** - If everyone's confused, messaging needs work
- **Communicate once** - Important messages need repetition
- **Forget internal teams** - Sales/CS need to be prepared
- **Wing it** - Plan communications carefully
- **Over-communicate trivial things** - Save bandwidth for what matters

---

## Model

Use: Sonnet

---

## Related

- `/stakeholder-management:stakeholder-map` - Map stakeholders for communication
- `/stakeholder-management:align` - Alignment meetings for stakeholder buy-in
- `/gtm-strategy:release-plan` - Release communication planning
- `stakeholder-manager` agent - Stakeholder communication strategies
- `gtm-planner` agent - Go-to-market communication
