---
name: prd-templates
description: Master PRD templates including problem statements, success metrics, requirements, user stories, and technical considerations. Use when writing PRDs, documenting features, defining requirements, communicating product decisions, or creating feature specifications. Covers PRD structure, writing best practices, and templates from Amazon, Google, and high-performing PM teams.
---

# PRD Templates

Comprehensive PRD (Product Requirements Document) templates and frameworks for documenting product requirements and driving successful execution.

## When to Use This Skill

**Auto-loaded by agents**:
- `requirements-engineer` - For Amazon PR/FAQ, comprehensive PRD, and lean PRD templates

**Use when you need**:
- Writing product requirements documents
- Documenting feature specifications
- Aligning cross-functional teams
- Communicating product decisions
- Creating feature briefs
- Defining project scope
- Establishing success metrics

## What is a PRD?

A PRD is the primary document for defining what to build and why. It serves as:
- **Alignment tool**: Gets everyone on the same page
- **Decision artifact**: Documents what and why
- **Communication vehicle**: Shares vision across teams
- **Execution blueprint**: Guides building and launch
- **Historical record**: Captures rationale for future decisions

**A great PRD answers**:
- What are we building?
- Why are we building it?
- Who is it for?
- How will we know it's successful?
- What are we explicitly NOT building?

---

## When to Use Which Template

We provide 4 ready-to-use PRD templates for different contexts:

### Lean PRD
**Use for**: Small features, enhancements, bug fixes
**Effort**: 1-2 hours to write
**Length**: 1-2 pages
**Audience**: Engineering team

**Best for**:
- Features requiring < 1 week of development
- Well-understood problems with clear solutions
- Internal tools or quick experiments
- Low cross-functional complexity

**Template**: `assets/lean-prd-template.md`

---

### Comprehensive PRD (Standard)
**Use for**: Most features, new capabilities, significant enhancements
**Effort**: 4-8 hours to write
**Length**: 3-5 pages
**Audience**: Cross-functional team

**Best for**:
- Standard features (1-4 weeks of development)
- Customer-facing changes
- Features requiring cross-functional coordination
- New capabilities or platform features

**Template**: `assets/comprehensive-prd-template.md`

---

### Amazon PR/FAQ
**Use for**: New products, major bets, working backwards from customer
**Effort**: 8-16 hours to write
**Length**: 3-6 pages (1-2 page PR + 2-4 pages FAQ)
**Audience**: Solo dev or small team (customer-first thinking)

**Best for**:
- New products or product lines
- Major strategic initiatives
- Customer-facing launches
- Working backwards from customer experience
- Pitching to executives or board

**Unique approach**: Start with the press release announcing the finished product, then answer hard questions. Forces customer-first thinking and addresses risks early.

**Template**: `assets/amazon-pr-faq-template.md`

---

### Google PRD
**Use for**: Data-driven products, cross-team initiatives, scale-focused
**Effort**: 8-12 hours to write
**Length**: 5-10 pages
**Audience**: Cross-functional teams, leadership

**Best for**:
- Products where metrics and scale matter from day one
- Cross-team initiatives requiring tight coordination
- Features with significant technical complexity
- Initiatives requiring executive approval

**Unique approach**: Emphasizes objectives (goals and non-goals), user benefits, and clear success criteria with measurable targets.

**Template**: `assets/google-prd-template.md`

---

## Core PRD Components

Regardless of template, great PRDs include these key elements:

### 1. Problem Statement

**Purpose**: Validate this is worth solving

**Include**:
- User pain point (describe from their perspective)
- Who experiences it (user segment, % affected)
- Impact if not solved (business + customer cost)
- Evidence (research, data, quotes)

**Good example**:
"Small business owners spend 5+ hours per week manually creating invoices, leading to delayed payments and cash flow issues. 68% of survey respondents cited invoicing as their #1 time sink. Current tools require accounting expertise most small business owners lack."

**Bad example**:
"We need an invoicing feature because competitors have one."

---

### 2. Goals & Success Criteria

**Purpose**: Define what winning looks like

**Include**:
- Business goals (revenue, efficiency, market position)
- User goals (what users can newly accomplish)
- Success metrics with baselines and targets
- Timeline for measurement (30/60/90 days)

**Make metrics SMART**:
- **Specific**: "Increase DAU" not "grow users"
- **Measurable**: Quantifiable number
- **Achievable**: Stretch but realistic
- **Relevant**: Ties to business goals
- **Time-bound**: Clear deadline

**Track both**:
- **Leading metrics**: Predict success (activation, engagement)
- **Lagging metrics**: Measure outcome (revenue, retention)

---

### 2.5. Evidence (Optional Section)

**Purpose**: Validate the problem with data

**CRITICAL - Never Fabricate Evidence**:

PRDs are specifications Claude Code uses to build features. Fabricated evidence leads to wrong implementations. All included evidence MUST be from real sources.

**Include Evidence section ONLY when you have**:
- Real user research (synthesized by research-ops or user-provided)
- Competitive analysis (from competitive-landscape.md or market-analyst)
- Support data (ticket volumes, customer quotes from user)
- Analytics data (user-provided metrics and usage patterns)

**If no evidence exists**: Omit the Evidence section entirely. Do not use placeholders or template examples as if they were real data.

**Valid evidence sources**:
- Context files: `competitive-landscape.md` (Stage 1), `customer-segments.md` (Stage 2)
- Specialist agents: research-ops synthesis, market-analyst competitive research
- User-provided: Support tickets, analytics, surveys, interview transcripts
- WebSearch: Current market data, competitor information

**Attribution required** - All evidence must cite source:
- "Synthesized from 6 interviews (research-ops, Oct 2025)"
- "From competitive-landscape.md (created Stage 1, validated Oct 2025)"
- "User-provided: 12 support tickets over 3 months"
- "WebSearch: Current competitor analysis (Oct 2025)"

**Template examples show FORMAT only**:
- Examples in templates demonstrate structure, not content to copy
- Never copy example numbers, quotes, or data as if they were real
- Replace with actual data or omit section

**Check context first**:
- Before asking user, check if `competitive-landscape.md` or `customer-segments.md` contain feature-relevant data
- If context files exist but don't cover this feature, ask user if new research is needed
- Route to specialist agents (market-analyst, research-ops) when beneficial

---

### 3. Proposed Solution

**Purpose**: Paint picture of what we're building

**Include**:
- High-level description (what and why)
- Key capabilities (what it can do)
- User experience (how users interact)
- Value proposition (why users care)

**Show, don't just tell**:
- User scenarios (storytelling)
- User flows (step-by-step)
- Mockups (visual representation)
- Concrete examples

---

### 4. Requirements

**Purpose**: Define what to build

**Functional requirements**:
- Number them (REQ-001, REQ-002)
- Use active voice ("System shall...")
- Be specific and testable
- Include acceptance criteria

**Non-functional requirements**:
- Performance (speed, latency, throughput)
- Security (authentication, authorization, encryption)
- Scalability (load handling, growth capacity)
- Accessibility (WCAG compliance)
- Reliability (uptime, error rates)

**Prioritize ruthlessly**:
- **P0/Must**: Required for launch
- **P1/Should**: Important, can defer if needed
- **P2/Nice-to-have**: Future consideration

---

### 5. Out of Scope

**Purpose**: Prevent scope creep and maintain focus

**Why it matters**:
- Explicitly stating what we're NOT doing prevents scope creep mid-development
- Helps prioritization discussions
- Maintains focus on core value

**Include**:
- Features/capabilities explicitly excluded
- Brief rationale for each
- Note if it's "never" or "not now"

---

### 6. Launch Plan

**Purpose**: Define rollout strategy

**Include**:
- Rollout approach (phased, beta, full launch)
- Target segments or cohorts
- Success validation approach
- Go/No-Go criteria

---

## PRD Writing Best Practices

### Start with Why

Most PRDs start with "what". Great PRDs start with "why".

**Poor order**: "We're building guest checkout. Users will be able to..."
**Good order**: "Users abandon checkout because account creation adds friction (45% rate). To solve this, we're building..."

---

### Be Specific and Measurable

Vague language kills PRDs.

**Vague → Specific**:
- "Fast" → "Page load < 2 seconds (p95)"
- "Many users" → "35% of daily active users"
- "Improve engagement" → "Increase session length from 3min to 5min"
- "Easy to use" → "New users complete key task in < 5 minutes without help"

---

### Write for Clarity

Clear documentation serves multiple purposes:

**For implementation**: Clear requirements, acceptance criteria, non-functional requirements
**For yourself**: User scenarios, flows, edge cases, decisions and rationale
**For users**: Target audience, value proposition, differentiation

---

### Document Decisions and Rationale

Future you needs to know why decisions were made.

**Example**:
"We're starting with web only (no mobile app) because:
1. 80% of current usage is web
2. Mobile requires 3x development time
3. We can validate core value on web first
4. Mobile can launch in Q2 based on learnings"

---

### Use Visuals

**Tables** for comparisons, **diagrams** for flows, **mockups** for UI, **charts** for data.

A picture is worth a thousand words of requirements.

---

## Common PRD Mistakes to Avoid

❌ **Solutionizing too early**: Start with problem, not "we need to build..."
❌ **Vague requirements**: "Fast" instead of "< 2 seconds"
❌ **Missing acceptance criteria**: No clear definition of "done"
❌ **No prioritization**: Everything is P0
❌ **Scope creep**: Adding "just one more thing" repeatedly
❌ **Missing success metrics**: No way to measure if it worked
❌ **No evidence**: "I think users want..." instead of data
❌ **Too long**: 20-page PRDs nobody reads

---

## Writing Clear PRDs for Solo Builders

For solo developers and small teams, PRDs serve as thinking documents and future reference.

### Start with a Brief

**Before writing full PRD**:
1. Draft 1-page overview (problem, solution, metrics, scope)
2. Validate direction with quick user feedback or research
3. Refine based on insights
4. Then write full PRD

**Why this works**:
- Low time investment if direction is wrong
- Easier to course-correct early
- Validates problem before deep specification
- Prevents over-planning before validation

---

### Self-Review Process

**Before finalizing**:
1. Step away for 24 hours
2. Re-read with fresh eyes
3. Ask: Would Claude Code understand this?
4. Ask: Would a new teammate understand this?
5. Update for clarity

**Review checklist**:
- Problem clearly stated with evidence
- Success metrics specific and measurable
- Requirements testable and complete
- Out of scope explicitly documented
- Decisions and rationale captured

---

## PRD Review Checklist

Before submitting your PRD, verify:

**Content Completeness**:
- [ ] Problem clearly defined with evidence
- [ ] Goals and success metrics specified
- [ ] Solution described with user flows
- [ ] Requirements listed with acceptance criteria
- [ ] Out of scope explicitly stated
- [ ] Launch plan defined

**Quality**:
- [ ] Well-structured and easy to navigate
- [ ] Clear, concise language
- [ ] Specific and measurable requirements
- [ ] Technical feasibility considered
- [ ] Risks identified with mitigation

**For full checklist**: See `assets/prd-review-checklist.md`

---

## Ready-to-Use Templates

We provide complete, copy-paste-ready templates:

### In `assets/`:
- **lean-prd-template.md**: Quick 1-2 page format for small features
- **comprehensive-prd-template.md**: Standard 3-5 page format for most features
- **amazon-pr-faq-template.md**: Working backwards from customer experience
- **google-prd-template.md**: Data-driven, objectives-focused format
- **prd-review-checklist.md**: Quality checklist before submission

### In `references/`:
- **prd-writing-guide.md**: Deep dive on writing techniques, section-by-section guidance, common mistakes

---

## PRD Workflow

### 1. Research & Discovery
- Customer interviews
- Data analysis
- Competitive research
- Problem validation

### 2. Pre-PRD Validation (1-2 days)
- Draft 1-pager
- Validate with user feedback or research
- Iterate on direction

### 3. Write PRD (1-3 days)
- Choose appropriate template
- Document problem, solution, requirements
- Add mockups and user flows
- Define success metrics

### 4. Review & Iterate (1-2 days)
- Self-review after 24 hours
- Peer review if available
- Refine for clarity
- Finalize

### 5. Development
- Update PRD as decisions made
- Regular demos and check-ins
- Scope change management

### 6. Launch & Learn
- Execute launch plan
- Track success metrics
- Document results
- Share learnings

---

## When NOT to Write a PRD

PRDs aren't always needed:

**Skip for**:
- Trivial changes (copy tweaks, simple bug fixes)
- Well-understood maintenance work
- One-person side projects
- Throwaway prototypes

**Use instead**:
- Quick Slack/email for trivial changes
- GitHub issue for bug fixes
- Lightweight spec for small projects

**PRDs make sense when**:
- Significant time investment (>1 week)
- Complex feature requiring clear specification
- Need documentation for future reference
- Building with AI coding tools like Claude Code

---

## Adapting Templates

Templates are starting points, not rigid structures.

**Adapt based on**:
- Company culture (startup vs enterprise)
- Product maturity (new product vs established)
- Team size (2 people vs 20)
- Audience (internal tool vs customer-facing)

**Good adaptation**:
- Removing sections that don't apply
- Adding sections for specific context
- Adjusting level of detail
- Changing format/structure

**Bad adaptation**:
- Removing problem statement (always needed)
- Skipping success metrics (always needed)
- No out-of-scope (always needed)
- Ignoring audience needs

---

## Related Skills

- **user-story-templates**: For user story format and acceptance criteria
- **specification-techniques**: General spec writing best practices
- **go-to-market-playbooks**: For launch planning

---

## Learning More

**In this skill**:
- See templates in `assets/` for ready-to-use formats
- See `references/prd-writing-guide.md` for writing techniques

**Books**:
- "Inspired" by Marty Cagan
- "Escaping the Build Trap" by Melissa Perri
- "The Lean Product Playbook" by Dan Olsen

**Key Principle**: The best PRD is the one that gets your team aligned and building the right thing. Use these templates as starting points and adapt to your context.
