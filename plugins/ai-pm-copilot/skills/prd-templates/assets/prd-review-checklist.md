# PRD Review Checklist

Use this checklist before submitting your PRD for review. A complete PRD saves time in reviews and ensures alignment.

---

## Content Completeness

### Problem & Context

- [ ] **Problem is clearly defined** with specific user pain points
- [ ] **Evidence is provided** (user research, data, support tickets, competitive analysis)
- [ ] **Problem is quantified** (how many users affected, business impact)
- [ ] **Users are identified** (who experiences this problem)
- [ ] **Strategic fit is explained** (why this aligns with company goals)

**Red flags**:

- Problem statement starts with "We need to..." instead of user pain
- No evidence provided (just assumptions)
- Can't articulate who the user is

---

### Goals & Success Criteria

- [ ] **Goals are specific and measurable** (not vague aspirations)
- [ ] **Success metrics are defined** with baselines and targets
- [ ] **Timeline for measurement** is specified (30/60/90 days)
- [ ] **Leading and lagging metrics** are both included
- [ ] **Non-goals are explicitly stated** (what we're NOT doing)

**Red flags**:

- Goals like "improve user experience" (too vague)
- Success metrics without targets ("increase engagement")
- No baseline data (don't know current state)

---

### Solution

- [ ] **Solution is clearly described** (what we're building)
- [ ] **User experience is explained** (how users will interact)
- [ ] **Key capabilities are listed** (what it can do)
- [ ] **User flows are documented** or linked
- [ ] **Mockups/designs are included** or linked

**Red flags**:

- Solution is vague or high-level only
- No mockups or user flow documentation
- Describes technology instead of user benefit

---

### Requirements

- [ ] **Functional requirements are listed** with clear descriptions
- [ ] **Requirements are prioritized** (P0/Must, P1/Should, P2/Nice-to-have)
- [ ] **Acceptance criteria are defined** for key requirements
- [ ] **Non-functional requirements are specified** (performance, security, scale)
- [ ] **Requirements are numbered** for traceability (REQ-001, REQ-002)

**Red flags**:

- Everything is marked P0 (no real prioritization)
- Vague requirements ("should be fast")
- No acceptance criteria (unclear when "done")

---

### Scope

- [ ] **Out of scope is explicitly listed** (what we're NOT building)
- [ ] **Rationale for exclusions** is provided
- [ ] **Future considerations noted** (what might come later)
- [ ] **Dependencies are identified** (what we need from other teams)

**Red flags**:

- No out-of-scope section (scope will creep)
- Everything is "future consideration" (unclear what's actually in scope)
- Hidden dependencies discovered mid-development

---

## Quality & Clarity

### Writing Quality

- [ ] **Document is well-structured** with clear sections and headings
- [ ] **Language is clear and concise** (no unnecessary jargon)
- [ ] **Consistent terminology** used throughout
- [ ] **Spelling and grammar are correct**
- [ ] **Appropriate level of detail** for audience

**Red flags**:

- Wall of text with no structure
- Technical jargon that team members won't understand
- Inconsistent naming (same thing called different names)

---

### Team Alignment

- [ ] **All relevant team members identified** as reviewers
- [ ] **Cross-functional input incorporated** (eng, design, marketing, legal)
- [ ] **Key decisions are documented** with rationale
- [ ] **Open questions are tracked** with owners and deadlines
- [ ] **Conflicting feedback is addressed**

**Red flags**:

- Only PM's perspective included
- Key team member not listed as reviewer
- Open questions with no owner or deadline

---

### Technical Feasibility

- [ ] **Technical approach is documented** or linked
- [ ] **Architecture implications** are addressed
- [ ] **Performance requirements** are specified
- [ ] **Security considerations** are included
- [ ] **Scalability is addressed** (will this work at scale?)
- [ ] **Engineering team has reviewed** and confirmed feasibility

**Red flags**:

- No technical review yet
- Performance/scale not mentioned
- Security as an afterthought

---

## Launch Readiness

### Go-to-Market

- [ ] **Launch plan is defined** (phased rollout, beta, full launch)
- [ ] **Target audience** is specified (who gets it first)
- [ ] **Marketing/comms plan** is addressed or linked
- [ ] **Customer support** is prepared (docs, training, FAQs)
- [ ] **Go/No-Go criteria** are defined

**Red flags**:

- No launch plan (just "ship it")
- Support team unaware
- No criteria for deciding whether to launch

---

### Risk Management

- [ ] **Risks are identified** (technical, market, operational)
- [ ] **Mitigation strategies** are defined for key risks
- [ ] **Fallback plans** exist for high-impact risks
- [ ] **Privacy/legal implications** are addressed
- [ ] **Compliance requirements** are identified

**Red flags**:

- No risks listed (overly optimistic)
- High-impact risks with no mitigation
- Legal/privacy issues unaddressed

---

### Monitoring & Learning

- [ ] **Metrics tracking is planned** (dashboards, alerts)
- [ ] **Post-launch evaluation** is scheduled
- [ ] **User feedback collection** is planned
- [ ] **Iteration approach** is defined (how we'll improve based on learnings)

**Red flags**:

- "Ship and forget" mentality
- No plan to measure success
- No process for gathering feedback

---

## Common Mistakes to Avoid

### Content Mistakes

❌ **Solutionizing in problem statement**

- Bad: "We need to build a dashboard"
- Good: "Users can't see their metrics at a glance"

❌ **Vague success criteria**

- Bad: "Increase engagement"
- Good: "Increase daily active users from 10K to 13K in 3 months"

❌ **Missing acceptance criteria**

- Bad: "REQ-001: Users can export data"
- Good: "REQ-001: Users can export data to CSV format, < 5 sec for 10K rows, all fields included"

❌ **Everything is P0**

- Prioritize ruthlessly - not everything can be critical

❌ **No out of scope section**

- Leads to scope creep and misaligned expectations

---

### Process Mistakes

❌ **Writing PRD in isolation**

- Get cross-functional input early, not after it's "done"

❌ **Too long or too short**

- Lean PRD: 1-2 pages
- Standard PRD: 3-5 pages
- Comprehensive PRD: 8-15 pages

❌ **No self-review**

- Don't skip eng, design, marketing, legal reviews

❌ **Ignoring feedback**

- Address all feedback or explicitly defer with rationale

❌ **No version control**

- Track changes, especially after major feedback rounds

---

## Review Process

### Self-Review

Before sending to others:

1. **Read aloud** - catches awkward phrasing
2. **Check links** - ensure all links work
3. **Run spell check** - obvious but often skipped
4. **Verify numbers** - double-check all metrics and targets
5. **Test mockups** - ensure design files are accessible to reviewers

---

### Peer Review

Get feedback from fellow PMs:

- **Content review**: Is it clear? Complete? Logical?
- **Blind spots**: What did I miss?
- **Devil's advocate**: Poke holes in assumptions

---

### Team Review

Organize reviews by function:

**Engineering** reviews for:

- Technical feasibility
- Requirement clarity
- Performance/scale implications
- Dependencies on other systems

**Design** reviews for:

- UX clarity and completeness
- Design feasibility
- Accessibility considerations
- Design system consistency

**Marketing** reviews for:

- Market positioning
- Customer messaging
- Launch readiness
- Competitive differentiation

**Legal/Compliance** reviews for:

- Privacy implications
- Data handling
- Regulatory compliance
- Terms of service updates

**Data Science** reviews for:

- Metric definitions
- Measurement feasibility
- Baseline data accuracy
- Statistical rigor

---

### Approval Checklist

Before marking as "Approved":

- [ ] All required reviewers have signed off
- [ ] Critical feedback has been addressed
- [ ] Open questions have owners and deadlines
- [ ] Team is aligned on scope and timeline
- [ ] Resources are confirmed (people, budget, time)
- [ ] Risks and mitigation are understood
- [ ] Success criteria are agreed upon

---

## Template-Specific Checklists

### Lean PRD Additional Checks

- [ ] Truly lean (1-2 pages max)
- [ ] Focused on small, well-understood feature
- [ ] No unnecessary sections
- [ ] Quick to read and understand

---

### Comprehensive PRD Additional Checks

- [ ] Executive summary at the top
- [ ] Table of contents for navigation
- [ ] All sections from template included
- [ ] Appendix with supporting materials
- [ ] Document version history

---

### Amazon PR/FAQ Additional Checks

- [ ] Press release is customer-focused (not technical)
- [ ] Press release is exciting and clear
- [ ] FAQ answers hard questions honestly
- [ ] Internal FAQ addresses business concerns
- [ ] Business model is explained
- [ ] Risks are acknowledged

---

### Google PRD Additional Checks

- [ ] Goals and non-goals clearly stated
- [ ] Success metrics with baselines and targets
- [ ] User scenarios tell compelling stories
- [ ] Launch plan with staged rollout
- [ ] Open issues tracked with owners

---

## Quick Health Check

Answer these 5 questions. If any answer is "no" or "unsure", revisit your PRD.

1. **Could an engineer start building from this PRD?**
   - [ ] Yes [ ] No [ ] Unsure

2. **Is success clearly measurable?**
   - [ ] Yes [ ] No [ ] Unsure

3. **Would a skeptical reviewer be convinced this is the right thing to build?**
   - [ ] Yes [ ] No [ ] Unsure

4. **If you were on vacation and someone read this PRD, could they answer questions about it?**
   - [ ] Yes [ ] No [ ] Unsure

5. **Have you addressed technical, legal, and market risks?**
   - [ ] Yes [ ] No [ ] Unsure

If all answers are "Yes", your PRD is ready for review.

---

## Before Final Submission

- [ ] Run through entire checklist
- [ ] Get peer review from another PM
- [ ] Share draft with team members informally first
- [ ] Set clear deadline for feedback
- [ ] Schedule review meeting if needed
- [ ] Be prepared to iterate based on feedback

---

## After Approval

- [ ] Update status to "Approved"
- [ ] Add approval dates and names
- [ ] Share with broader team
- [ ] Create tracking tickets/user stories
- [ ] Schedule kickoff meeting
- [ ] Plan for ongoing updates as development progresses

---

**Remember**: A great PRD is clear, complete, and compelling. It answers "what" and "why" so well that "how" becomes obvious. Take the time to get it right - it saves weeks of misalignment later.
