# PRD Writing Guide: Deep Dive

A comprehensive guide to writing exceptional Product Requirements Documents that drive alignment and successful execution.

---

## The Purpose of a PRD

A PRD serves multiple purposes:

1. **Alignment tool**: Gets everyone on the same page
2. **Decision artifact**: Documents what and why
3. **Communication vehicle**: Shares vision across teams
4. **Execution blueprint**: Guides building and launch
5. **Historical record**: Captures rationale for future reference

**A great PRD answers**:

- What are we building?
- Why are we building it?
- Who is it for?
- How will we know it's successful?
- What are we explicitly NOT building?

---

## The Problem with Most PRDs

### Common Failures

**Too vague**:

- "Improve user experience"
- "Make the product faster"
- "Add social features"

**Too prescriptive**:

- Dictates implementation before understanding constraints
- Leaves no room for engineering creativity
- Confuses solution with requirements

**Too long**:

- 50-page documents nobody reads
- Buried insights in walls of text
- Process over substance

**Missing the "why"**:

- Lists features without rationale
- No connection to business goals
- Can't make tradeoff decisions

---

## Writing Principles

### 1. Start with Why

Simon Sinek's Golden Circle applies to PRDs:

- **Why**: The problem and its impact
- **How**: The approach and key capabilities
- **What**: The specific features and requirements

Most PRDs start with "what". Great PRDs start with "why".

**Example**:

- **Why**: Users abandon checkout because account creation adds friction. We lose $50K/month.
- **How**: Allow purchase without account, offer account creation post-purchase
- **What**: Guest checkout flow with email + payment only

---

### 2. Write for Your Audience

Different team members need different things:

**Executives** need:

- Executive summary (2-3 paragraphs)
- Business impact and ROI
- Strategic alignment
- Key risks

**Engineers** need:

- Clear requirements with acceptance criteria
- Non-functional requirements (performance, scale)
- Technical dependencies
- Integration points

**Designers** need:

- User scenarios and use cases
- User flows and journeys
- Edge cases and error states
- Accessibility requirements

**Marketing** needs:

- Target audience definition
- Value proposition
- Competitive differentiation
- Launch timeline

**Pro tip**: Write executive summary last (once you know what you're saying), but put it first (so busy people read it).

---

### 3. Be Specific and Measurable

Vague language kills PRDs.

**Vague → Specific transformations**:

"Fast" → "Page load < 2 seconds (p95)"

"Many users" → "35% of daily active users"

"Improve engagement" → "Increase session length from 3min to 5min"

"Recent" → "Within last 30 days"

"Easy to use" → "New users complete key task in < 5 minutes without help"

---

### 4. Prioritize Ruthlessly

Not everything can be P0. Use frameworks:

**MoSCoW**:

- **Must have**: Required for launch
- **Should have**: Important but can defer
- **Could have**: Nice to have if easy
- **Won't have**: Explicitly out of scope

**P0/P1/P2**:

- **P0**: Blocks launch
- **P1**: Needed soon after launch
- **P2**: Future consideration

**Ask**: "If we had to launch with 50% less scope, what would we cut?"

---

### 5. Document Decisions and Rationale

Future you (and future PMs) need to know why decisions were made.

**Document**:

- Why this approach vs alternatives considered
- Why feature X is out of scope
- Why metric Y was chosen as success criteria
- Why we prioritized A over B

**Example**:
"We're starting with web only (no mobile app) because:

1. 80% of current usage is web
2. Mobile app requires 3x development time
3. We can validate core value prop on web first
4. Mobile can launch in Q2 based on web learnings"

---

## Section-by-Section Guide

### Executive Summary

**Purpose**: Give busy team members everything they need in 2 minutes

**Structure**:

- 2-4 paragraphs
- Problem (what's broken)
- Solution (how we'll fix it)
- Impact (why it matters - metrics and business value)

**Example**:
"Users abandon our checkout process at a 45% rate, primarily because forced account creation adds friction. This costs us approximately $50K/month in lost revenue. We're building a guest checkout option that reduces friction while maintaining the ability to convert users to accounts post-purchase.

Based on competitor benchmarks, we expect guest checkout to reduce cart abandonment by 30%, translating to $15K/month in recovered revenue. This also addresses the #1 complaint in our NPS surveys. Launch is targeted for Q2 Week 8."

---

### Problem Statement

**Purpose**: Convince team members this is worth solving

**Include**:

1. User pain point (describe from their perspective)
2. Who experiences it (user segment, % of users)
3. Impact if not solved (business + customer)
4. Evidence (research, data, quotes)

**Frameworks**:

**5 Whys** (root cause):

- "Users abandon checkout" (symptom)
- Why? "Account creation is required"
- Why does that matter? "They don't want another password"
- Why? "They're making one-time purchase"
- Why is that a problem? "We force relationship before trust"
- Root cause: Misaligned signup timing

**Jobs-to-be-Done** format:
"When [situation], users want to [motivation], so they can [expected outcome], but currently [obstacle]."

---

### Goals & Success Criteria

**Purpose**: Define what winning looks like

**Structure**:

1. Business goals (revenue, efficiency, market position)
2. User goals (what users can newly accomplish)
3. Success metrics with baselines and targets

**Good metrics characteristics (SMART)**:

- **Specific**: "Increase DAU" not "grow users"
- **Measurable**: Quantifiable number
- **Achievable**: Stretch but realistic
- **Relevant**: Ties to business goals
- **Time-bound**: 30/60/90 day targets

**Leading vs Lagging**:

- **Leading**: Predict success (activation rate, engagement)
- **Lagging**: Measure outcome (revenue, retention)
- **Track both**: Leading tells you how, lagging tells you if it worked

---

### Solution Overview

**Purpose**: Paint picture of what we're building

**Include**:

1. High-level description (what and why)
2. Key capabilities (what it can do)
3. User experience (how users interact)
4. Value proposition (why users care)

**Show, don't just tell**:

- User scenarios (storytelling)
- User flows (step-by-step)
- Mockups (visual representation)
- Examples (concrete not abstract)

**Bad**: "We'll add guest checkout"
**Good**: "Users will see a 'Continue as Guest' button on checkout. They'll enter email, shipping, and payment - no password required. Post-purchase, we'll offer account creation with pre-filled info. This lets users buy now, commit later."

---

### Requirements

**Purpose**: Define what to build

**Best practices**:

**Functional requirements**:

- One requirement per line
- Number them (REQ-001, REQ-002)
- Use active voice ("System shall...")
- Be specific and testable

**Acceptance criteria**:

- Defines "done"
- Testable (can verify yes/no)
- Specific enough to prevent ambiguity

**Example**:
**REQ-001**: User can complete purchase as guest without account creation

- **Acceptance criteria**:
  - [ ] "Continue as Guest" button visible on checkout page
  - [ ] Guest flow requires only email, shipping address, payment
  - [ ] No password required during guest checkout
  - [ ] Order confirmation sent to provided email
  - [ ] Guest users can access order status via magic link in email

**Non-functional requirements**:

- Performance (speed, latency, throughput)
- Security (authentication, authorization, encryption)
- Scalability (load handling, growth capacity)
- Accessibility (WCAG compliance, screen readers)
- Reliability (uptime, error rates)

---

### Out of Scope

**Purpose**: Prevent scope creep and manage expectations

**Why it matters**:

- Explicitly stating what we're NOT doing is as important as what we ARE doing
- Prevents "but I thought we were also..." mid-development
- Helps prioritization discussions

**Format**:

- List features/capabilities explicitly excluded
- Brief rationale for each (optional but helpful)
- Note if it's "never" or "not now"

**Example**:
**Out of Scope for v1**:

- Social login (Google/Facebook) - adds complexity, defer to v2 based on demand
- Guest wishlist/saved items - focus on purchase flow first
- Passwordless login for returning guests - interesting but not core value
- Merging guest orders into account - edge case, address if customers request

**Never in scope**:

- Guest checkout on mobile app - different UX paradigm, separate project

---

### Open Questions

**Purpose**: Track unresolved issues

**Structure**:

- Question clearly stated
- Owner (who will resolve)
- Target date (when we need answer)
- Options considered (if applicable)

**Example**:

1. **How long should we store guest order data?**
   - **Owner**: Legal team
   - **Due**: Oct 15
   - **Options**: 30 days, 90 days, 1 year
   - **Impact**: Privacy compliance, customer support access

2. **Should guest users receive marketing emails by default?**
   - **Owner**: Marketing + Legal
   - **Due**: Oct 12
   - **Options**: Opt-in, opt-out, no marketing
   - **Impact**: GDPR compliance, email list growth

---

## Writing Techniques

### Use the Inverted Pyramid

**Journalism technique**: Most important information first

**Application to PRDs**:

1. Executive summary (30-second version)
2. Problem and goals (2-minute version)
3. Solution overview (5-minute version)
4. Detailed requirements (full deep dive)

This lets readers stop when they have enough information.

---

### Tell Stories

**User scenarios** make requirements tangible.

**Structure**:

- **Setup**: Who is the user, what's their context
- **Trigger**: What makes them need this
- **Action**: What they do
- **Resolution**: What happens (success or failure)

**Example**:
"Jamie is a busy professional ordering a birthday gift for her sister. She finds the perfect item on our site but only has 2 minutes before her next meeting. She clicks 'Continue as Guest,' enters her email and shipping address, uses Apple Pay for instant payment, and completes purchase in under 60 seconds. Order confirmation arrives immediately. She closes her laptop and goes to her meeting, knowing the gift is on its way."

This is more compelling than "REQ-001: Support guest checkout."

---

### Use Visuals

**Tables** for comparisons:
| Feature | Current | Proposed |
|---------|---------|----------|
| Account required | Yes | No (guest option) |
| Checkout time | 5 min avg | 2 min avg |

**Diagrams** for flows:

- User journey maps
- System architecture
- Decision trees

**Mockups** for UI:

- Wireframes for early concepts
- High-fidelity for detailed specs

**Charts** for data:

- Current metrics and trends
- Projected impact

---

### Active Voice

**Passive**: "The order confirmation is sent to the user"
**Active**: "System sends order confirmation to user"

Active voice is clearer and more direct.

---

### Consistent Terminology

Pick terms and stick with them:

- "User" or "Customer"? (choose one)
- "Guest checkout" or "anonymous purchase"? (choose one)
- "Shopping cart" or "basket"? (choose one)

Create a glossary if needed.

---

## Common Writing Mistakes

### Mistake 1: Solution Before Problem

**Wrong order**:
"We're going to build guest checkout. Users will be able to purchase without accounts..."

**Right order**:
"Users abandon checkout because account creation adds friction (45% abandonment rate). To solve this, we're building guest checkout..."

**Why it matters**: Starting with the problem makes the solution obvious and necessary.

---

### Mistake 2: Assuming Context

You know the background deeply. Your readers may not.

**Missing context**:
"This addresses the issue we discussed last quarter."

**Good context**:
"Our Q3 user research found that 35% of checkout abandonment is due to required account creation. This feature directly addresses that finding."

---

### Mistake 3: Jargon Overload

**Technical jargon**:
"We'll implement stateless authentication via JWT with refresh token rotation for guest sessions."

**Plain language**:
"Guest users will stay logged in securely without creating an account. Their session will expire after 30 days for security."

Save technical details for the engineering spec.

---

### Mistake 4: Burying the Lede

**Buried**: Put the important point on page 3

**Front-loaded**: Put it in the first paragraph

Busy executives won't read to page 3.

---

### Mistake 5: No Failure Cases

Happy path is easy. What about:

- Error conditions?
- Edge cases?
- System failures?
- User mistakes?

Document these too.

---

## PRD Maintenance

### PRDs Are Living Documents

**During development**:

- Update as decisions are made
- Document changes and rationale
- Keep open questions current
- Mark requirements as complete

**Version control**:

- Track major revisions
- Note what changed and why
- Keep approval history

**After launch**:

- Document actual results vs targets
- Capture lessons learned
- Link to post-launch analysis

---

### When to Update

**Update immediately when**:

- Major scope changes
- Key decisions made
- Requirements added/removed
- Timeline changes significantly

**Mark changes clearly**:

- Strikethrough removed items
- Bold new items
- Change log at top or bottom

---

## PRD Anti-Patterns

### The Novel

**Symptom**: 50+ pages that nobody reads
**Fix**: Use appendices and links; keep core document focused

---

### The Vague Manifesto

**Symptom**: High-level vision with no specifics
**Fix**: Add concrete requirements, metrics, and examples

---

### The Technical Spec

**Symptom**: API endpoints and database schemas in PRD
**Fix**: Link to technical design doc; keep PRD focused on "what" and "why"

---

### The Feature List

**Symptom**: Bulleted features with no context
**Fix**: Add problem statement, user scenarios, and success criteria

---

### The Unchanging Artifact

**Symptom**: PRD written once, never updated
**Fix**: Treat as living document; update as you learn

---

## Quality Checklist

Great PRDs are:

- [ ] **Clear**: Anyone can understand it
- [ ] **Complete**: All necessary information included
- [ ] **Concise**: No unnecessary content
- [ ] **Compelling**: Makes team members want to build it
- [ ] **Concrete**: Specific requirements and metrics
- [ ] **Current**: Reflects latest decisions

---

## Learning Resources

**Books**:

- "Inspired" by Marty Cagan (product discovery)
- "Escaping the Build Trap" by Melissa Perri (outcomes over outputs)
- "The Lean Product Playbook" by Dan Olsen (product-market fit)

**Articles**:

- "Good Product Manager/Bad Product Manager" by Ben Horowitz
- "How to Write a Painfully Good Product Requirements Document" by Rahul Jain
- Amazon's PR/FAQ approach

**Templates**:

- Aha!, ProductPlan, and other PM tools have template libraries
- Study PRDs from successful companies (often shared on blogs)

---

**Remember**: The best PRD is the one that gets your team aligned and building the right thing. Adapt these guidelines to your context - there's no one perfect format.
