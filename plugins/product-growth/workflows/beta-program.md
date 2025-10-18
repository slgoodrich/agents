---
name: Beta Program Workflow
description: Comprehensive framework for launching and managing product beta programs
category: Growth
duration: 8-12 weeks
model: sonnet
---

# Beta Program Workflow

Structured process for launching beta programs to validate features, gather feedback, and build momentum before general availability.

## Usage
```
/beta-program [feature or product name]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Feature or product for beta program
- Beta goals (validation, feedback, early adoption, buzz generation)
- Target beta audience (customers, prospects, power users, specific segments)
- Timeline and GA launch target date
- Team capacity and resources
- Key success metrics

## Timeline: 8-12 Weeks

## Phase 1: Beta Strategy & Planning (Week 1-2)

### Define Beta Objectives
```
Task: product-strategist agent
Set clear beta program goals:

**Primary objectives** (choose 1-2):
- **Validation**: Test product-market fit
- **Feedback**: Gather user input for improvements
- **Technical**: Stress test infrastructure and scalability
- **Marketing**: Generate buzz and early adopters
- **Learning**: Understand usage patterns and behaviors
- **Revenue**: Early revenue and case studies

**Success criteria**:
- Define what "successful beta" means
- Quantitative metrics (adoption, engagement, NPS)
- Qualitative goals (insights, testimonials, case studies)

Create beta program charter
```

### Beta Type Selection
```
Task: product-strategist agent
Choose beta model:

**Closed Beta** (invitation-only):
- Controlled group (50-500 users)
- High-touch feedback
- NDA and privacy
- Intense support
- Good for: Early validation, B2B, sensitive features

**Open Beta** (anyone can join):
- Large group (1,000+ users)
- Scalability testing
- Public feedback
- Self-service
- Good for: Consumer products, infrastructure testing, buzz generation

**Private Beta** (internal + select customers):
- Very limited group (10-50 users)
- Dogfooding + friendly customers
- Highest quality feedback
- Good for: Very early stage, high-risk features

**Hybrid**: Start private, expand to closed, open to public
```

### Timeline Planning
```
Task: product-ops agent
Create beta timeline:

**Typical Beta Timeline**:
- **Week 1-2**: Planning and setup
- **Week 3**: Recruit participants
- **Week 4**: Onboard first cohort
- **Week 5-8**: Active beta with feedback loops
- **Week 9**: Stabilization and final improvements
- **Week 10**: Beta wrap-up and analysis
- **Week 11**: GA preparation
- **Week 12**: General availability launch

**Duration factors**:
- Product complexity
- Feedback cycles needed
- Technical stability goals
- Market timing

Create detailed beta timeline
```

## Phase 2: Beta Design & Preparation (Week 2-3)

### Participant Criteria
```
Task: user-researcher agent
Define ideal beta participants:

**Selection criteria**:
- **Fit**: Matches target customer profile
- **Motivation**: Willing to provide feedback
- **Technical ability**: Can handle rough edges
- **Availability**: Has time to engage
- **Influence**: Can become advocates

**Diversity considerations**:
- Mix of user types and segments
- Range of use cases
- Geographic and demographic diversity
- Technical sophistication levels
- New and existing customers

**Target numbers**:
- Closed beta: 50-500 participants
- Open beta: 1,000-10,000+ participants
- Cohorts: 2-4 waves if possible

Create participant criteria and recruiting plan
```

### Beta Application & Selection
```
Task: user-researcher agent
Design application process:

**Application form**:
- Basic demographics
- Use case description
- Why want to participate
- Feedback commitment
- Technical environment
- Agreement to terms

**Selection process**:
- Review applications
- Prioritize by fit and diversity
- Rolling acceptance (cohorts)
- Waitlist management

Create application form and selection rubric
```

### Beta Feature Scope
```
Task: requirements-engineer agent
Define beta scope and limitations:

**What's included**:
- Core feature set
- Key user flows
- Essential functionality
- Documentation and support

**What's NOT included** (yet):
- Edge cases
- Advanced features
- Polish and refinement
- Full integrations
- Enterprise features

**Known limitations**:
- Performance constraints
- Feature gaps
- Browser/platform support
- Scalability limits

Create beta scope document and known issues list
```

### Support & Resources
```
Task: customer-success agent
Plan beta support model:

**Support channels**:
- Dedicated Slack/Discord channel
- Email support (priority queue)
- Office hours (weekly)
- Documentation and FAQs
- Video tutorials
- Community forum

**Support team**:
- Product manager (primary)
- Engineer (technical issues)
- Designer (UX feedback)
- Community manager (engagement)

**Resources**:
- Beta portal or website
- Onboarding guide
- Feature documentation
- Feedback mechanisms
- Bug reporting process

Create beta support plan
```

## Phase 3: Recruitment & Onboarding (Week 3-4)

### Beta Recruitment
```
Task: gtm-planner agent
Recruit beta participants:

**Recruitment channels**:
- **Email list**: Existing users who opted in
- **Waitlist**: From landing page or signup
- **Customer outreach**: Account teams nominate
- **Social media**: Twitter, LinkedIn announcements
- **Community**: Forums, Slack groups
- **Partnerships**: Partner companies
- **Press**: TechCrunch, Product Hunt

**Messaging**:
- Exclusive early access
- Shape the product
- Free or discounted access
- Direct line to product team
- Recognition and credits

Create recruitment campaign
```

```
Command: /pm:beta-program
Design beta program structure and recruitment materials
```

### Acceptance & Onboarding
```
Task: customer-success agent
Onboard beta participants:

**Acceptance communication**:
- Congratulations email
- Program expectations
- Timeline and milestones
- How to get started
- Support resources

**Onboarding flow**:
1. Welcome email and program overview
2. Account setup and access
3. Onboarding video or webinar
4. First-use guidance
5. Feedback mechanism introduction

**Onboarding goals**:
- Get to aha moment quickly
- Understand how to give feedback
- Know where to get help
- Feel excited and special

Create onboarding sequence
```

### Cohort Management
```
Task: product-ops agent
Manage beta cohorts:

**Why cohorts**:
- Controlled rollout
- Isolated feedback
- Iterative improvements
- Manageable support load

**Cohort strategy**:
- **Cohort 1** (Week 4): 20-50 power users
- **Cohort 2** (Week 5): 50-100 diverse users
- **Cohort 3** (Week 6): 100-200 expansion
- **Cohort 4** (Week 7): Full beta group

Learn and improve between cohorts
```

## Phase 4: Active Beta & Feedback (Week 4-8)

### Ongoing Engagement
```
Task: customer-success agent
Keep beta participants engaged:

**Engagement activities**:
- **Weekly updates**: Progress, improvements, gratitude
- **Office hours**: Weekly or bi-weekly live Q&A
- **Feature drops**: New capabilities regularly
- **Challenges/missions**: Encourage specific usage
- **Recognition**: Shoutout top contributors
- **Swag**: T-shirts, stickers for engaged users

**Communication channels**:
- Email newsletter (weekly)
- Beta community Slack/Discord (daily)
- Video updates (bi-weekly)
- 1:1 calls with select users (weekly)

Maintain momentum and enthusiasm
```

### Feedback Collection
```
Task: user-researcher agent
Systematically gather feedback:

**Quantitative feedback**:
- In-app surveys (NPS, feature ratings)
- Usage analytics and funnel tracking
- Bug and error tracking
- Performance metrics
- A/B tests on variations

**Qualitative feedback**:
- In-app feedback widget
- Community discussions
- User interviews (5-10 weekly)
- Support tickets and requests
- Session recordings and heatmaps

**Feedback themes to explore**:
- What do you love?
- What's confusing or frustrating?
- What's missing?
- How does it compare to alternatives?
- Would you recommend? Why/why not?

Create feedback collection system
```

```
Command: /pm:survey-builder
Context: Beta program feedback
Design feedback surveys for beta participants
```

```
Task: customer-insights agent
Synthesize feedback weekly:
- Common themes and patterns
- Critical issues to fix
- Feature requests by priority
- Usability problems
- Delightful moments
- Unexpected use cases

Create weekly beta insights report
```

### Rapid Iteration
```
Task: product-ops agent
Fast iteration cycle:

**Weekly rhythm**:
- Monday: Review previous week feedback
- Tue-Thu: Build and ship improvements
- Friday: Deploy updates and communicate changes
- Weekend: Monitor and support

**What to prioritize**:
- **P0 bugs**: Blocking issues
- **Quick wins**: High-impact, easy fixes
- **Common feedback**: Mentioned by 20%+ of users
- **Aha moment**: Improve activation
- **Confusion**: Remove friction

**Ship velocity**: 1-2 updates per week minimum

Show beta users you're listening and acting
```

### Metrics Monitoring
```
Task: data-scientist agent
Track beta health metrics:

**Participation metrics**:
- Active users (DAU/WAU/MAU)
- Feature adoption rates
- Session frequency and duration
- Funnel conversion rates

**Feedback metrics**:
- Feedback volume and quality
- Bug reports submitted
- Support ticket volume
- Community engagement

**Satisfaction metrics**:
- NPS or satisfaction scores
- Would-recommend percentage
- Retention (% coming back)
- Churn from beta

**Technical metrics**:
- Error rates and crashes
- Performance (load times)
- API usage and rate limits
- Infrastructure utilization

Create beta metrics dashboard
```

## Phase 5: Beta Optimization (Week 6-9)

### Address Critical Gaps
```
Task: requirements-engineer agent
Fix major issues before GA:

**Categories to address**:
- **Showstoppers**: Must fix for GA
- **Major gaps**: Important for GA
- **Nice-to-haves**: Can wait for post-GA

**Prioritization**:
- Impact on adoption
- Frequency of mention
- Complexity to fix
- Strategic importance

Create GA readiness backlog
```

### Beta Milestones & Challenges
```
Task: growth-pm agent
Drive specific behaviors:

**Example challenges**:
- "Complete your first [action]"
- "Invite a teammate"
- "Try all 5 core features"
- "Share feedback on 3 topics"
- "Achieve [outcome]"

**Incentives**:
- Leaderboard and recognition
- Extended free access
- Exclusive features
- Swag and rewards
- Credits or discounts

Gamify to increase engagement and learning
```

### Case Study Development
```
Task: gtm-planner agent
Capture success stories:

**Identify success stories**:
- Users achieving great results
- Interesting use cases
- Quantifiable outcomes
- Enthusiastic advocates

**Case study process**:
- Interview successful users
- Capture metrics and quotes
- Draft case study
- Review and approval
- Publish at GA launch

**Assets to create**:
- Written case studies
- Video testimonials
- Metrics and ROI stories
- User quotes for marketing

Create case study pipeline
```

## Phase 6: Beta Wind-Down & GA Prep (Week 9-11)

### Stabilization Period
```
Task: technical-pm agent
Focus on stability and polish:

**Week 9-10 goals**:
- **Feature freeze**: No new features
- **Bug fixing**: Address all critical bugs
- **Performance**: Optimize slow operations
- **Polish**: UI/UX refinement
- **Documentation**: Complete and accurate
- **Testing**: Comprehensive QA

**GA readiness checklist**:
- <1% error rate
- Performance targets met
- Critical bugs fixed
- Documentation complete
- Support team trained
- Infrastructure scaled
- Monitoring in place

Create GA readiness scorecard
```

### Beta Graduation Plan
```
Task: customer-success agent
Plan transition for beta users:

**Beta user options**:
1. **Convert to paid**: If freemium/trial beta
2. **Grandfather pricing**: Special beta pricing
3. **Early access extended**: Extra time before billing
4. **VIP status**: Ongoing special treatment
5. **Beta alumni**: Community recognition

**Communication**:
- Thank beta participants
- Share impact they had
- Transition plan and timeline
- Special offers
- Continued relationship

Reward early believers
```

### Final Beta Survey
```
Task: user-researcher agent
Comprehensive exit survey:

**Survey questions**:
- Overall satisfaction (1-10)
- Would you recommend? (NPS)
- What did you love?
- What should we improve?
- How does it compare to alternatives?
- Will you continue using?
- What's your use case?
- Can we use you as reference?

**In-depth interviews**:
- 10-20 interviews
- Diverse perspectives
- Deep dive on experience
- Testimonials and quotes
- Improvement ideas

Create final beta feedback report
```

## Phase 7: GA Launch & Transition (Week 11-12)

### General Availability Launch
```
Command: /pm:product-launch (use workflow)
Execute full product launch:
- Public announcement
- Marketing campaign
- Press and media
- Sales enablement
- Customer onboarding at scale

Leverage beta learnings and testimonials
```

### Beta to GA Communication
```
Task: stakeholder-manager agent
Communicate GA launch:

**Beta participants**:
- Early heads up
- Thank you and recognition
- Transition details
- How to stay involved

**Broader market**:
- Beta success stories
- Proof points and metrics
- Case studies and testimonials
- Product benefits

**Internal**:
- Beta learnings
- GA readiness confirmation
- Support and sales prep
- Celebration of launch

Create GA launch communication plan
```

### Post-Beta Monitoring
```
Task: data-scientist agent
Compare beta vs. GA metrics:
- Activation and engagement rates
- Feature adoption patterns
- Support volume and types
- Performance and reliability
- User satisfaction

Identify any regression or GA-specific issues
```

## Phase 8: Beta Program Retrospective (Week 12)

### Program Review
```
Task: product-strategist agent
Comprehensive beta retrospective:

**Quantitative results**:
- Participation and engagement metrics
- Feedback volume and quality
- Bugs identified and fixed
- Features improved based on feedback
- Conversion and adoption rates

**Qualitative results**:
- Key insights learned
- Product improvements made
- Use cases discovered
- Market validation
- Advocacy and testimonials

**Process evaluation**:
- What worked well
- What didn't work
- Surprises and learnings
- Improvements for next beta

**ROI assessment**:
- Time and resource investment
- Value of feedback
- Quality improvement
- Market readiness
- Momentum generated

Create beta program retrospective document
```

```
Command: /pm:decision-logger
Decision: Learnings from beta program
Document for future beta programs
```

## Deliverables

1. **Beta Program Charter** - Goals, strategy, success criteria
2. **Participant Criteria** - Ideal beta user profile
3. **Beta Timeline** - Detailed schedule and milestones
4. **Recruitment Plan** - How to find and onboard participants
5. **Support Resources** - Documentation, guides, support channels
6. **Feedback System** - Collection and synthesis process
7. **Beta Insights Reports** - Weekly synthesis of learnings
8. **Case Studies** - Success stories and testimonials
9. **GA Readiness Scorecard** - Launch readiness assessment
10. **Program Retrospective** - Learnings and improvements

## Success Metrics
- Participation target achieved (e.g., 200 beta users)
- Engagement rate >60% (weekly active)
- NPS >40 (beta participants)
- Feedback volume (>10 items per user)
- Bugs identified and fixed (>50)
- Case studies created (3-5)
- Beta to paid conversion (>30%)
- Ready for GA launch on schedule

## Beta Program Best Practices

### DO:
- Set clear expectations upfront
- Treat beta users as VIPs
- Act on feedback visibly
- Communicate frequently
- Make users feel special
- Iterate rapidly
- Celebrate and recognize participants
- Capture success stories

### DON'T:
- Over-promise and under-deliver
- Ignore feedback
- Let beta drag on forever
- Neglect support
- Treat users as free QA
- Be defensive about criticism
- Launch GA before ready
- Forget to thank participants

## Common Beta Challenges

### Challenge: Low engagement
**Solution**: Regular communication, challenges, recognition, direct outreach

### Challenge: Poor feedback quality
**Solution**: Specific prompts, structured surveys, 1:1 interviews, incentives

### Challenge: Technical issues overwhelming users
**Solution**: Better onboarding, clear known issues, responsive support, cohorted rollout

### Challenge: Scope creep during beta
**Solution**: Clear feature freeze date, prioritization discipline, focus on stability

### Challenge: Beta never ending
**Solution**: Time-bound program, clear GA criteria, commitment to timeline

## Beta vs. Other Validation Methods

**Beta** (8-12 weeks, 50-500 users):
- Validates at scale
- Real usage in production
- Builds momentum
- Marketing value

**Prototype Testing** (1-2 weeks, 8-15 users):
- Quick validation
- Lower fidelity
- Usability focus
- Before full build

**Pilot** (3-6 months, 5-20 companies):
- Deep partnership
- B2B focused
- Revenue validation
- Higher touch

Choose based on product stage, goals, and resources.
