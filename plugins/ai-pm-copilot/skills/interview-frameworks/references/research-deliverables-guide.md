# Research Deliverables and Reporting Guide

## Table of Contents

- [Overview](#overview)
- [Part 1: Types of Research Deliverables](#part-1-types-of-research-deliverables)
- [Part 2: Research Report](#part-2-research-report)
- [Part 3: Presentation Deck](#part-3-presentation-deck)
- [Part 4: Highlight Reel (Video)](#part-4-highlight-reel-video)
- [Part 5: One-Pager (Email Summary)](#part-5-one-pager-email-summary)
- [Part 6: Storytelling with Research](#part-6-storytelling-with-research)
- [Part 7: Research Repository](#part-7-research-repository)
- [Part 8: Communicating Research Across Organization](#part-8-communicating-research-across-organization)
- [Deliverable Checklist](#deliverable-checklist)

## Overview

How to transform interview data into compelling deliverables that drive decisions. Covers report structures, presentation formats, storytelling with research, and sharing insights across the organization.

---

## Part 1: Types of Research Deliverables

### Quick Reference Guide

Choose based on audience and goal:

| Deliverable             | Time to Create | Best For               | Audience                      |
| ----------------------- | -------------- | ---------------------- | ----------------------------- |
| **Email Summary**       | 30 min         | Quick updates          | PM team                       |
| **Slide Deck**          | 2-4 hours      | Presentations          | Execs, cross-functional teams |
| **Research Report**     | 4-8 hours      | Comprehensive findings | Product, design, eng teams    |
| **Highlight Reel**      | 1-2 hours      | Emotional impact       | All company                   |
| **Insight Cards**       | 1-2 hours      | Ongoing reference      | Product team, design          |
| **Research Repository** | Ongoing        | Long-term knowledge    | Entire company                |

---

## Part 2: Research Report

### Purpose

Comprehensive documentation of research with findings, evidence, and recommendations.

### When to Use

- Completed research cycle (10+ interviews)
- Need to document thoroughly
- Multiple team members need access
- Will reference findings over months

---

### Report Structure

**1. Executive Summary** (1 page)

**Goal**: Busy execs read this only - give them everything they need

```
## Executive Summary

**Research Goal**
[1-2 sentences: What we wanted to learn]

**Methodology**
- [X] interviews with [participant description]
- Conducted [dates]
- [Recruitment method]

**Key Findings** (3-5 bullets, most important)
1. [Finding 1 with impact]
   - Evidence: [X/Y participants mentioned]
   - Impact: [What this means for product]

2. [Finding 2 with impact]
   - Evidence: [Specific data point]
   - Impact: [Business implication]

3. [Finding 3 with impact]

**Recommendations** (3-5 actions, prioritized)
1. [HIGH] [Action 1]: [Why and expected impact]
2. [HIGH] [Action 2]: [Why and expected impact]
3. [MEDIUM] [Action 3]: [Why and expected impact]

**Next Steps**
- [What happens next]
- [Timeline]
- [Who owns what]
```

**Example**:

```
## Executive Summary

**Research Goal**
Understand why enterprise customers (500+ employees) aren't adopting our project management tool despite initial interest.

**Methodology**
- 12 interviews with PMs at enterprise companies (500-2000 employees)
- Conducted Feb 1-15, 2024
- Recruited via LinkedIn + existing leads

**Key Findings**
1. SSO (Single Sign-On) is a hard blocker, not a nice-to-have
   - Evidence: 11/12 participants cited SSO as requirement before even piloting
   - Impact: We can't win enterprise deals without SSO

2. Enterprise customers need audit logs and activity tracking for compliance
   - Evidence: 8/12 mentioned SOC2/compliance requirements
   - Impact: Compliance features are table-stakes, not differentiators

3. Pricing is secondary to security and compliance
   - Evidence: 10/12 said they'd pay 2-3x more if security features were included
   - Impact: Price isn't the barrier - missing features are

**Recommendations**
1. [HIGH] Build SSO integration (SAML) - Required to enter enterprise market
2. [HIGH] Add audit logs and activity tracking - Required for compliance
3. [MEDIUM] Create enterprise security page on website - Helps sales conversations

**Next Steps**
- Product to scope SSO work (Feb 20)
- Design to mockup audit logs (Feb 25)
- Marketing to create security content (March 1)
```

---

**2. Methodology** (1 page)

**Goal**: Establish credibility, help others replicate

```
## Methodology

**Research Approach**
[Type of research: Discovery, Validation, Usability]

**Participants**
- **Number**: [X] participants
- **Recruitment**: [How recruited]
- **Criteria**:
  - Must-have: [List]
  - Nice-to-have: [List]
  - Disqualify: [List]

**Demographics**
| Segment | Count |
|---------|-------|
| Company size 50-200 | 4 |
| Company size 200-500 | 5 |
| Company size 500+ | 3 |

**Interview Format**
- **Duration**: [X] minutes per interview
- **Method**: Video call (Zoom)
- **Recording**: Yes, with permission (11/12 consented)
- **Date range**: [Start - End dates]

**Interview Topics**
- Current project management process
- Pain points with existing tools
- Decision-making process for tools
- Requirements for new tools

**Limitations**
- Sample skewed toward tech industry (10/12 from SaaS companies)
- US-only participants (may not apply internationally)
- All participants had tried competitors (not "fresh" users)
- 1 participant worked at competitor (excluded from analysis)
```

---

**3. Key Findings** (3-5 pages)

**Goal**: Document insights with evidence

**Structure for Each Finding**:

```
### Finding 1: [Headline Summary]

**Insight**
[1-2 sentences describing the pattern/insight]

**Evidence**
- [X/Y] participants mentioned [behavior]
- [Specific data point]
- [Pattern observed]

**Quotes**
> "[Powerful quote 1]" - Participant 3, PM at 500-person company
>
> "[Powerful quote 2]" - Participant 7, PM at 1000-person company

**Impact**
- **Product Implications**: [What this means for product]
- **Priority**: [HIGH/MEDIUM/LOW based on frequency and impact]
- **Risk if Ignored**: [What happens if we don't act]

**Recommendation**
[Specific action to take based on this finding]
```

**Example**:

```
### Finding 1: SSO is Hard Requirement, Not Nice-to-Have

**Insight**
Enterprise customers (500+ employees) cannot even pilot our tool without SSO due to security policies. This is a binary gate, not a feature preference.

**Evidence**
- 11/12 participants mentioned SSO as requirement before any evaluation
- 4 participants said IT/security team would block any tool without SSO
- 3 participants said they couldn't even show mockups to decision makers without SSO roadmap
- Average company policy: "No new tools without SSO" (8 participants had written policies)

**Quotes**
> "SSO isn't a nice-to-have for us. It's the entry ticket to even have the conversation. Without it, IT won't let us pilot anything." - P4, Director of Product at 750-person SaaS company
>
> "I can't even fill out your signup form because it'll get flagged by our security team. We have a hard rule: SSO or nothing." - P8, Senior PM at 1200-person fintech

**Impact**
- **Product Implications**: SSO is table-stakes for enterprise (500+ employees), not a differentiator
- **Priority**: HIGH - Blocks entire market segment (>$10M ARR opportunity)
- **Risk if Ignored**: Cannot win any enterprise deals, limited to SMB market

**Recommendation**
Build SAML-based SSO integration as P0 for enterprise product line (target: Q2 2024)
```

---

**4. Recommendations** (1-2 pages)

**Goal**: Actionable next steps, prioritized

**Structure**:

```
## Recommendations

**Summary**
Based on research findings, we recommend [high-level strategy]

**Prioritized Actions**

### Priority 1 (HIGH) - [Must do]

**1. [Action 1]**
- **Why**: [Finding it addresses]
- **Expected Impact**: [What we gain]
- **Effort**: [Time/resources estimate]
- **Owner**: [Team/person]
- **Timeline**: [When]

**2. [Action 2]**
[Same structure]

### Priority 2 (MEDIUM) - [Should do]

**3. [Action 3]**
[Same structure]

### Priority 3 (LOW) - [Nice to have]

**4. [Action 4]**
[Same structure]

**Not Recommended**
- [Action X]: [Why we're NOT doing this despite it being mentioned]
```

**Example**:

```
## Recommendations

**Summary**
To successfully enter the enterprise market, we must build security and compliance features (SSO, audit logs, RBAC) before focusing on feature differentiation. Price is not the barrier - missing security features are.

**Prioritized Actions**

### Priority 1 (HIGH) - Must Build to Enter Enterprise

**1. Build SAML-based SSO Integration**
- **Why**: Hard blocker for 11/12 enterprise participants
- **Expected Impact**: Unlocks $10M+ ARR enterprise market
- **Effort**: 4-6 engineer weeks
- **Owner**: Eng team + Product
- **Timeline**: Q2 2024 (complete by end April)

**2. Add Audit Logs and Activity Tracking**
- **Why**: Required for SOC2 compliance (8/12 participants)
- **Expected Impact**: Meets compliance requirements for regulated industries
- **Effort**: 2-3 engineer weeks
- **Owner**: Eng team
- **Timeline**: Q2 2024 (after SSO)

### Priority 2 (MEDIUM) - Improves Conversion

**3. Create Enterprise Security Page on Website**
- **Why**: Sales needs to reference security features in conversations
- **Expected Impact**: Reduces security objections, shortens sales cycle
- **Effort**: 1 designer week + 0.5 eng week
- **Owner**: Marketing + Design
- **Timeline**: March 2024

### Priority 3 (LOW) - Nice to Have

**4. Custom Onboarding for Enterprise**
- **Why**: 3 participants mentioned complex onboarding for large teams
- **Expected Impact**: Faster time-to-value, better retention
- **Effort**: TBD
- **Owner**: CS team
- **Timeline**: Q3 2024

**Not Recommended**
- Lower pricing for enterprise: 10/12 said they'd pay 2-3x more for security features, so price isn't the barrier
```

---

**5. Appendix** (Optional)

**Include**:

- Full participant list (anonymized: P1, P2, etc.)
- Interview guide used
- Screener survey
- Additional quotes
- Raw data (if relevant)
- Affinity map photos

**Don't include**:

- Full transcripts (too long)
- Identifying information
- Irrelevant tangents

---

### Report Template (Complete)

```
[Cover Page]
Research Report
[Title of Research]
[Your Name, Date]

---

Table of Contents
1. Executive Summary
2. Methodology
3. Key Findings
4. Recommendations
5. Appendix

---

[Full sections as outlined above]
```

---

## Part 3: Presentation Deck

### Purpose

Present findings to the team in meeting format.

### When to Use

- All-hands presentation
- Product planning meetings
- Design reviews
- Documentation and reference

### Deck Structure (15-25 slides)

**Slide 1: Title**

```
Research Findings:
[Research Topic]

[Your Name]
[Date]
```

**Slide 2: Agenda**

```
Today's Agenda
1. Research Goals
2. Who We Talked To
3. Key Findings (3-5)
4. Recommendations
5. Next Steps
6. Q&A
```

**Slide 3-4: Context**

```
Slide 3: Why This Research?
- [Problem we were investigating]
- [Questions we needed to answer]
- [How this informs product decisions]

Slide 4: Who We Talked To
- [X] interviews
- [Participant criteria]
- [Demographics visual/table]
- [Date range]
```

**Slides 5-15: Key Findings** (One finding per 2-3 slides)

```
Slide 5: Finding 1 - [Headline]
- [1-sentence insight]
- Evidence: [X/Y participants]
- Impact: [What this means]

Slide 6: Finding 1 - Quote
[Large pull quote with attribution]
[Image of participant context if available]

Slide 7: Finding 1 - So What?
- Product implication: [What we should build/change]
- Priority: [HIGH/MEDIUM/LOW]
- Recommendation: [Action to take]

[Repeat structure for Findings 2, 3, etc.]
```

**Slides 16-20: Recommendations**

```
Slide 16: Summary of Recommendations
1. [Action 1 - P0]
2. [Action 2 - P0]
3. [Action 3 - P1]
4. [Action 4 - P1]

Slide 17: Recommendation 1 - [Action]
- Why: [Finding it addresses]
- Expected Impact: [What we gain]
- Effort: [Estimate]
- Timeline: [When]

[One slide per major recommendation]
```

**Slide 21: Next Steps**

```
What Happens Next?
1. [Immediate next step - by when]
2. [Second step - by when]
3. [Third step - by when]

Owners: [Who's responsible]
```

**Slide 22: Questions**

```
Questions?

[Your contact info]
[Link to full report if available]
```

---

### Presentation Tips

**Visuals**:

- Use large quotes (24pt+ font)
- Photos of participants (with permission, or stock photos representing context)
- Simple charts (bar charts for frequency data)
- Minimal text (bullet points, not paragraphs)
- Consistent theme/colors

**Storytelling**:

- Start with context (why this matters)
- One insight per slide (don't cram)
- Use quotes for emotional impact
- Connect findings to business goals
- End with clear actions

**Delivery**:

- Practice beforehand
- Time yourself (aim for 20-30 min + Q&A)
- Pause after key quotes
- Ask for questions throughout (if appropriate)
- Have backup slides for deep dives

---

## Part 4: Highlight Reel (Video)

### Purpose

Emotional impact through seeing/hearing real users. More compelling than text.

### When to Use

- All-hands to build empathy
- Presentations to decision makers
- Onboarding new team members
- Building case for prioritization

### How to Create

**1. Select Clips** (20-30 seconds each)

```
Choose moments that:
- Show strong emotion
- Have powerful quotes
- Demonstrate problem severity
- Represent patterns (not outliers)

Total: 3-5 clips, 2-4 minutes total
```

**2. Edit** (Tools: iMovie, Premiere, Descript, Grain)

```
Format:
- Intro slide (2 sec): Context
- Clip 1 (30 sec): [Topic]
- Transition slide (2 sec): Next topic
- Clip 2 (30 sec): [Topic]
- [...]
- Outro slide (5 sec): Summary + call to action
```

**3. Add Context**

```
Before each clip:
- Participant role/company size
- Question being answered
- Why this matters

Example:
"Sarah, PM at 500-person SaaS company, describing frustration with manual reporting:"
[Clip plays]
```

**4. Share**

```
- Upload to internal drive/Loom
- Share link in Slack/email
- Present in meetings
- Add to research repository
```

**Example Structure**:

```
00:00 - Intro: "We interviewed 10 PMs about project management pain"
00:05 - Clip 1: Participant frustrated by manual reporting (30 sec)
00:35 - Text overlay: "8/10 participants mentioned this problem"
00:40 - Clip 2: Participant describing lost data due to spreadsheet (25 sec)
01:05 - Clip 3: Participant excited about proposed solution (20 sec)
01:25 - Outro: "Key insight: Automated reporting is highest-value feature. Next steps: [Action]"
```

---

## Part 5: One-Pager (Email Summary)

### Purpose

Quick, scannable update for busy team members.

### When to Use

- Weekly research updates
- Quick findings after 2-3 interviews
- Sharing with people who won't read full report
- Getting feedback fast

### Structure

**Subject**: [Research Update] [Topic] - [Key Finding]

**Email Body**:

```
Hi team,

Quick update on [research topic]. Here's what we learned:

**TL;DR**
[1-sentence most important finding]

**What We Did**
- [X] interviews with [participants]
- Dates: [range]

**Key Findings** (top 3)
1. [Finding 1]: [Evidence + impact]
2. [Finding 2]: [Evidence + impact]
3. [Finding 3]: [Evidence + impact]

**Best Quote**
"[Powerful verbatim quote]" - [Participant description]

**Recommendations** (prioritized)
1. [Action 1 - HIGH]
2. [Action 2 - MEDIUM]
3. [Action 3 - LOW]

**Next Steps**
- [What happens next]
- [When]

Full report: [Link]
Questions? Reply or ping me on Slack.

[Your name]
```

**Example**:

```
Subject: [Research Update] Enterprise PM Tool Research - SSO is Hard Blocker

Hi team,

Quick update on enterprise research. Here's what we learned:

**TL;DR**
SSO is a hard requirement (not nice-to-have) for all enterprise customers. We can't win deals without it.

**What We Did**
- 12 interviews with PMs at 500-2000 person companies
- Dates: Feb 1-15

**Key Findings**
1. SSO blocks 100% of enterprise deals: 11/12 participants said IT policy requires SSO before pilot
2. Compliance features (audit logs) required: 8/12 need for SOC2
3. Price is NOT the barrier: 10/12 would pay 2-3x more for security features

**Best Quote**
"SSO isn't a nice-to-have. It's the entry ticket. Without it, IT won't let us pilot anything." - Director of Product, 750-person SaaS company

**Recommendations**
1. [HIGH] Build SAML SSO - Q2 2024 target
2. [HIGH] Add audit logs - After SSO
3. [MEDIUM] Create enterprise security page - March

**Next Steps**
- Product to scope SSO work by Feb 20
- Design to mockup audit logs by Feb 25

Full report: [Link to doc]
Questions? Reply or ping me.

Jordan
```

---

## Part 6: Storytelling with Research

### The Story Arc

Research findings are more compelling when told as a story.

**Structure**:

```
1. Setup (Context)
   "We noticed [problem]. We wanted to understand why."

2. Journey (Research)
   "We talked to [X] users who [criteria]"

3. Discovery (Insights)
   "Here's what we learned that surprised us..."

4. Climax (Key Insight)
   "The real problem isn't [what we thought], it's [actual insight]"

5. Resolution (Recommendation)
   "So here's what we should do..."
```

**Example**:

```
SETUP:
"Enterprise customers were signing up but not converting to paid. We assumed it was price."

JOURNEY:
"We interviewed 12 enterprise PMs to understand why they weren't buying."

DISCOVERY:
"Turns out, price wasn't even a concern. Every single person mentioned security features."

CLIMAX:
"The real blocker? We're missing table-stakes security features like SSO. They can't even pilot our tool without it due to IT policies."

RESOLUTION:
"So we're building SSO in Q2. This unlocks a $10M+ market we currently can't access."
```

---

### Using Quotes Effectively

**Bad Quote Usage**:

```
Finding: Users find the UI confusing
Quote: "It's confusing." - P3
```

[Too short, no context, not impactful]

**Good Quote Usage**:

```
Finding: Users find the UI confusing

Quote:
"I spent 10 minutes trying to figure out how to archive a project. I clicked 'Delete' thinking it would give me more options, and it just... deleted everything. No confirmation, no undo. I almost quit right there." - P3, PM at 200-person startup

[Specific, emotional, shows severity]
```

**Pull Quote Format** (For slides/reports):

```
[Large, prominent display]

"I'd pay anything to get those 2 hours back every week.
Seriously, 3x the price? Done."

— Sarah Chen, Director of Product
   750-person SaaS company
```

---

## Part 7: Research Repository

### Purpose

Long-term knowledge base of all research. Prevents re-learning same things.

### Structure

**Repository Sections**:

```
1. Research Studies
   - Folders by date or theme
   - Each study has:
     - Report
     - Raw notes
     - Recordings
     - Presentations

2. Insights Database
   - Searchable insights across all research
   - Tagged by theme, product area, user segment

3. Participant Database
   - Who we've talked to
   - When, about what topics
   - Contact info (if they agreed to follow-up)

4. Quote Library
   - Best quotes across all research
   - Organized by theme
   - Easy to grab for presentations

5. Research Methods
   - Interview guides
   - Screeners
   - Templates
   - Best practices
```

---

### Tools for Repository

**Notion**:

- Flexible structure
- Easy to search
- Good for databases (participants, insights)
- Free for small teams

**Dovetail**:

- Purpose-built for research
- Transcription + tagging
- Insight repository
- More expensive

**Airtable**:

- Database-first
- Good for structured data
- Custom views
- Linking between tables

**Confluence/Wiki**:

- If company already uses it
- Good search
- Version control
- Integration with Jira

---

### Best Practices

**1. Consistent Naming**

```
Format: [Date]-[Type]-[Topic]

Examples:
- 2024-02-01_Discovery_Enterprise-Adoption
- 2024-03-15_Usability_Onboarding-Flow
- 2024-04-10_Validation_Reporting-Feature
```

**2. Tagging System**

```
Tags by:
- User segment (Enterprise, SMB, Individual)
- Product area (Reporting, Collaboration, Admin)
- Theme (Pain point, Feature request, Workflow)
- Priority (High, Medium, Low)
- Status (Active, Addressed, Archived)
```

**3. Regular Maintenance**

```
Quarterly review:
- Archive old research
- Update insights that were addressed
- Tag new themes that emerged
- Share top insights with company
```

---

## Part 8: Communicating Research Across Organization

### To Different Audiences

**Executives**:

- Focus: Business impact (revenue, risk, opportunity)
- Format: 1-page summary or 10-slide deck
- Emphasize: Numbers, ROI, competitive position
- Time: 15 minutes max

**Product Team**:

- Focus: Feature implications, user needs
- Format: Full report + presentation
- Emphasize: Detailed insights, quotes, patterns
- Time: 45-60 minutes

**Engineering**:

- Focus: Technical requirements, user workflows
- Format: Written doc with user stories
- Emphasize: "Why" behind features, context
- Time: 30 minutes + Q&A

**Design**:

- Focus: User experience, pain points, delighters
- Format: Highlight reel + full report
- Emphasize: Emotional responses, workflows, quotes
- Time: 30-45 minutes

**Sales/CS**:

- Focus: Objections, competitive positioning, use cases
- Format: One-pager + quote library
- Emphasize: Customer language, competitor comparisons
- Time: 15-20 minutes

---

### Sharing Cadence

**Immediate** (Within 24 hours of interview):

- Quick Slack update: "Just talked to [type of user]. Key takeaway: [insight]"

**Weekly** (If running multi-week research):

- Email summary of last week's interviews
- Top 2-3 findings so far
- Interesting quotes

**End of Research** (When complete):

- Full report (write within 1 week)
- Presentation (schedule within 2 weeks)
- Research repository update

**Quarterly**:

- "Research Highlights" all-hands presentation
- Top insights from last quarter
- How research shaped product

---

## Deliverable Checklist

**Before Sharing**:

- [ ] Anonymize participant data
- [ ] Check for typos and formatting
- [ ] Verify quotes are verbatim
- [ ] Confirm evidence supports claims
- [ ] Get feedback from teammate
- [ ] Add clear next steps
- [ ] Include your contact info

**When Sharing**:

- [ ] Right format for audience
- [ ] Right level of detail
- [ ] Clear recommendations
- [ ] Links to related research
- [ ] Easy to skim/scan
- [ ] Visually clean

**After Sharing**:

- [ ] Add to research repository
- [ ] Follow up on action items
- [ ] Track what got built
- [ ] Measure impact
- [ ] Share learnings with team

---

**Key Principle**: Great research isn't valuable until it drives decisions. Choose the right format for your audience, tell a compelling story with evidence, make recommendations actionable, and make findings easily accessible for future reference.
