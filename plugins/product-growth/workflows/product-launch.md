---
name: Product Launch Workflow
description: Full go-to-market orchestration for major product launches
category: Go-to-Market
duration: 8 weeks
model: sonnet
---

# Product Launch Workflow

Full go-to-market orchestration for major product launches.

## Usage
```
/product-launch [product or feature name]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Product or feature being launched
- Launch date or target timeline
- Target audience (all users, specific segment, beta, enterprise)
- Launch type (major release, feature update, new product)
- Key stakeholders and teams involved
- Success criteria for launch

## Timeline: 8 Weeks

## Workflow Phases

### T-8 Weeks: Strategy & Planning

**Agents**: `product-strategist`, `gtm-planner`

**Activities**:
1. Positioning (April Dunford framework)
2. Messaging hierarchy
3. Target audience definition
4. Launch tier (T1/T2/T3)
5. Success metrics
6. Launch team assembly

**Deliverables**: Launch strategy doc, positioning statement

**Commands**:
```
Tell gtm-planner: "Create launch strategy for [product]"
```

---

### T-6 Weeks: Asset Creation

**Agents**: `gtm-planner`, `requirements-engineer`

**Activities**:
1. **Marketing Assets**
   - Landing page
   - Product video (60-90 sec)
   - Demo video
   - Case studies (2-3)
   - Social graphics

2. **Sales Enablement**
   - One-pager
   - Pitch deck
   - Demo script
   - FAQ
   - Battle cards

3. **Product Readiness**
   - Help docs
   - Onboarding flows
   - In-app announcements

**Deliverables**: All launch assets

**Commands**:
```
/pm:release-notes [version]
Tell gtm-planner: "Create sales enablement package"
```

---

### T-4 Weeks: Beta Program

**Agents**: `user-researcher`, `growth-pm`

**Activities**:
1. Recruit beta users (50-100)
2. Onboard and educate
3. Gather feedback
4. Capture testimonials
5. Identify bugs/issues
6. Iterate product

**Success Criteria**:
- 80%+ task completion
- NPS > 40
- 3+ quotable testimonials
- <5 critical bugs

**Commands**:
```
/pm:interview-guide "Beta feedback sessions"
Tell user-researcher: "Synthesize beta feedback"
```

---

### T-2 Weeks: Enablement & Prep

**Agents**: `stakeholder-manager`

**Activities**:
1. **Internal Training**
   - Sales team
   - Support team
   - Success team

2. **Press & Media**
   - Press kit
   - Embargo briefings
   - Influencer outreach

3. **Final QA**
   - Bug bash
   - Performance testing
   - Security review

4. **Go/No-Go Decision**

**Commands**:
```
Tell stakeholder-manager: "Coordinate launch readiness review"
```

---

### Launch Week: Execution

**Day -1: Final Prep**
- Assets staged
- Monitoring dashboards
- Rollback plan tested
- War room scheduled

**Day 0: Launch**
- Feature flag: 10% → 50% → 100%
- Blog post published
- Email campaigns sent
- Social media blitz
- Press release distributed
- Monitor metrics (real-time)

**Day +1-7: Amplification**
- Product Hunt launch
- Webinar series
- Customer success outreach
- Bug triage
- Feedback collection

**Commands**:
```
/pm:release-notes --channel all
Tell gtm-planner: "Execute launch day plan"
```

---

### Post-Launch (Weeks 1-4)

**Agents**: `growth-pm`, `user-researcher`, `stakeholder-manager`

**Week 1**: Daily monitoring
- Adoption metrics
- Bug triage
- User feedback
- Quick fixes

**Week 2**: Analysis
- Success metrics vs targets
- User interviews (10)
- NPS survey
- Channel performance

**Week 3**: Optimization
- A/B tests for improvements
- Feature refinements
- Documentation updates

**Week 4**: Retrospective
- What worked
- What didn't
- Lessons learned
- Case study creation

**Commands**:
```
/pm:kpi-dashboard "Launch Metrics"
Tell growth-pm: "Analyze launch performance and recommend optimizations"
```

---

## Launch Tiers

### Tier 1: Major Launch
- New product
- Major rebrand
- Strategic bet
- Full PR, events, paid ads
- 8-week timeline

### Tier 2: Feature Launch
- Significant capability
- Blog, email, social
- Targeted outreach
- 4-week timeline

### Tier 3: Improvement
- Minor features, fixes
- Release notes, changelog
- 1-week timeline

---

## Success Metrics

**Awareness**:
- Press mentions
- Website traffic
- Social impressions

**Adoption**:
- Signups/trials
- Activation rate
- Feature usage

**Satisfaction**:
- NPS score
- App store ratings
- Customer feedback

**Business**:
- Revenue impact
- Customer acquisition
- Expansion revenue

---

## Launch Channels

**Owned**:
- Website/landing page
- Blog
- Email
- In-app
- Social media

**Earned**:
- Press (TechCrunch, etc.)
- Product Hunt
- Hacker News
- Influencers

**Paid**:
- Google Ads
- Social ads
- Retargeting

**Partners**:
- Co-marketing
- Integrations

---

## Rollback Plan

**Triggers**:
- Critical bugs
- Performance degradation
- Negative user sentiment
- Security issues

**Process**:
1. Feature flag to 0%
2. Notify stakeholders
3. User communication
4. Root cause analysis
5. Fix and relaunch

---

**Model**: Sonnet
