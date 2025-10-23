---
description: Graceful process for sunsetting products, features, or platforms
category: Operations
duration: 6-12 months
model: sonnet
---

# Product Sunset Workflow

Comprehensive framework for responsibly and gracefully deprecating and sunsetting products, features, or platforms while minimizing customer disruption.

## Usage
```
/sunset-product [product, feature, or platform to sunset]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- What is being sunset (product, feature, platform, API)
- Why (strategic shift, low usage, technical debt, cost reduction)
- How many users/customers affected
- Revenue impact if applicable
- Migration path or alternative (if any)
- Timeline constraints (urgent vs planned)

## Timeline: 6-12 Months

## Phase 1: Sunset Decision & Planning (Month 1-2)

### Sunset Evaluation
```
Task: product-strategist agent
Validate sunset decision:
- **Strategic misalignment** - Doesn't fit vision
- **Low usage** - Few active users
- **High cost** - Expensive to maintain
- **Technical debt** - Holding back platform
- **Better alternatives** - Internal or external
- **Business model** - Not viable
- **Market shift** - Demand disappeared

Ensure sunset is the right decision vs. improve/pivot

Create sunset business case
```

```
Task: data-scientist agent
Analyze impact of sunset:
- **Users affected** - How many?
- **Revenue at risk** - Current and future
- **Usage patterns** - Who uses it how?
- **Alternative adoption** - Will they migrate?
- **Customer segments** - Who's most affected?
- **Dependencies** - What relies on this?

Create impact analysis report
```

```
Command: /strategic-planning:scenario-planner
Scenarios:
- Sunset with 6-month notice
- Sunset with 12-month notice
- Keep in maintenance mode
- Sell or transfer to third party
Compare outcomes and costs
```

### Sunset Timeline Planning
```
Task: product-ops agent
Define sunset timeline (typically 6-12 months):

**Standard Timeline**:
- **Month 1-2**: Internal planning and preparation
- **Month 3**: Announcement to customers
- **Month 3-9**: Migration period with support
- **Month 9-10**: Final warnings and deadline
- **Month 10-11**: Grace period (read-only access)
- **Month 12**: Complete shutdown

**Factors influencing timeline**:
- Complexity of migration
- Customer contract terms
- Size of user base
- Availability of alternatives
- Regulatory requirements

Create detailed sunset timeline
```

### Legal & Contractual Review
```
Task: stakeholder-manager agent
Review legal and contractual obligations:
- **Terms of service** - What did we promise?
- **SLAs and contracts** - Existing commitments
- **Data retention** - Legal requirements
- **Privacy regulations** - Data handling
- **Refund policies** - Financial obligations
- **Partner agreements** - Third-party impacts

Work with legal team to ensure compliance
Create legal compliance checklist
```

## Phase 2: Migration Strategy (Month 2-3)

### Identify Migration Paths
```
Task: customer-success agent
Define migration options for users:

**Option 1: Internal alternative**
- Similar product/feature you offer
- Migration path and tools
- Pricing for existing customers
- Training and support

**Option 2: External alternative**
- Recommended third-party solutions
- Partnership arrangements
- Data export assistance
- No endorsement liability

**Option 3: DIY/Self-hosted**
- Open source the code (if feasible)
- Documentation for self-hosting
- Community support

**Option 4: No replacement**
- Users discontinue usage
- Data export and preservation

Create migration guide for each segment
```

```
Task: technical-pm agent
Design migration tools and support:
- **Data export** - Comprehensive, useful formats
- **Migration automation** - Tools to ease transition
- **API access** - Extended access during migration
- **Documentation** - Migration guides and FAQs
- **Support resources** - Dedicated migration support

Create technical migration plan
```

### Customer Segmentation
```
Task: customer-insights agent
Segment affected customers:

**Enterprise/High-value**:
- Personal outreach
- Dedicated migration support
- Custom timelines if needed
- Retention offers

**Mid-market**:
- Webinars and group support
- Migration tooling
- Standard timeline
- Potential incentives

**Small/Self-serve**:
- Email and documentation
- Self-service migration
- Community support

Create customer segmentation and outreach plan
```

## Phase 3: Communication Planning (Month 2-3)

### Communication Strategy
```
Task: stakeholder-manager agent
Develop comprehensive communication plan:

**Internal communications**:
- Engineering and product teams
- Sales and customer success
- Support and operations
- Executive and board
- All company announcement

**Customer communications**:
- Initial announcement (Month 3)
- Migration resources available (Month 4)
- Milestone reminders (Month 6, 8)
- Final warnings (Month 9, 10)
- Thank you and farewell (Month 11-12)

**Public communications**:
- Blog post announcement
- Press release (if significant)
- Social media
- Partner notifications
- Community forums

Create detailed communication calendar
```

```
Command: /gtm-strategy:communication-plan
Initiative: [Product] sunset
Create stakeholder communication strategy
```

### Message Development
```
Task: gtm-planner agent
Craft sunset messaging:

**Key messages**:
- **Why**: Honest reason for sunset (strategic focus, better alternatives)
- **What**: What's happening and when
- **Who**: Who's affected
- **How**: Migration options and support
- **When**: Timeline and key dates
- **Empathy**: Acknowledge disruption and apologize

**Tone**:
- Transparent and honest
- Empathetic and apologetic
- Helpful and supportive
- Appreciative of customers

Create messaging framework and templates
```

```
Command: /product-operations:faq-generator
Topic: [Product] sunset
Create comprehensive FAQ document
```

## Phase 4: Announcement & Initial Support (Month 3-4)

### Month 3: Public Announcement
```
Task: stakeholder-manager agent
Execute announcement:

**Day 1: Internal**
- All-company announcement
- Sales/CS enablement
- Support team briefing
- FAQ and talking points

**Day 2-3: High-touch customers**
- Personal calls to enterprise customers
- Account manager outreach
- Executive involvement if needed

**Day 4: Public announcement**
- Blog post published
- Email to all users
- In-app notifications
- Social media posts
- Press release if applicable

Monitor and respond to reactions
```

```
Command: /strategic-planning:executive-summary
Audience: Affected customers
Summarize sunset decision, timeline, and support
```

### Month 4: Migration Resources Launch
```
Task: customer-success agent
Launch migration support program:
- **Migration documentation** - Published and accessible
- **Export tools** - Available and tested
- **Webinars** - Migration guidance sessions
- **Support** - Dedicated channel or team
- **Office hours** - Live Q&A sessions
- **Community** - Peer support forum

Track engagement and usage of resources
```

```
Task: technical-pm agent
Ensure migration tools working:
- Data export tested and validated
- Migration scripts functional
- API access maintained
- Performance at scale
- Error handling and support

Monitor and fix issues quickly
```

## Phase 5: Migration Period (Month 4-9)

### Ongoing Support & Communication
```
Task: customer-success agent
Provide continuous migration support:

**Month 4-6: Early migration**
- Proactive outreach to early movers
- Support migration issues
- Collect feedback to improve
- Celebrate successful migrations
- Case studies and testimonials

**Month 7-8: Mid-migration push**
- Reminder communications
- Office hours and webinars
- Address common issues
- Incentivize migration

**Month 9: Final push**
- Urgent communications
- Escalation support
- Last-chance messaging

Track migration progress weekly
```

```
Task: data-scientist agent
Monitor migration metrics:
- **Migration rate** - % of users migrated
- **Export usage** - Who's exporting data
- **Alternative adoption** - Taking your alternative?
- **Support volume** - Trends and issues
- **Sentiment** - Customer feedback
- **Revenue impact** - Churn and retention

Create migration dashboard
```

### Handle Escalations
```
Task: stakeholder-manager agent
Manage difficult situations:
- **Angry customers** - Empathy and support
- **Contract disputes** - Legal involvement
- **Extension requests** - Evaluate case-by-case
- **Public criticism** - Transparent response
- **Press inquiries** - Coordinated messaging

Create escalation playbook
```

## Phase 6: Final Warnings & Grace Period (Month 10-11)

### Month 10: Final Warnings
```
Task: customer-success agent
Final notification push:
- Email to all remaining users
- In-app warnings (prominent)
- Personal outreach to high-value accounts
- Clear deadline communication
- Last-chance support offers

Track final migration surge
```

### Month 11: Grace Period (Optional)
```
Task: technical-pm agent
Implement grace period:
- **Read-only access** - Can view, can't edit
- **Extended export** - Additional time to export
- **Reduced functionality** - Core features only
- **No support** - Self-service only

Communicate grace period terms clearly
```

## Phase 7: Shutdown (Month 12)

### Final Shutdown
```
Task: technical-pm agent
Execute shutdown:

**Week 1**:
- Final user communications
- Disable new actions (read-only)
- Export deadline passed

**Week 2-3**:
- Data archival for legal retention
- Service degradation notices
- Countdown to shutdown

**Week 4**:
- Complete service shutdown
- Data deleted per retention policy
- DNS and infrastructure removed
- Monitoring discontinued

Document shutdown execution
```

```
Task: product-ops agent
Post-shutdown checklist:
- **Infrastructure** - Decommissioned
- **Data** - Archived or deleted per policy
- **Support** - Channel closed
- **Documentation** - Archived
- **Billing** - Final invoices sent
- **Monitoring** - Alerts removed
- **Marketing** - Website/content removed
- **Legal** - Compliance verified

Create shutdown completion report
```

### Thank You & Farewell
```
Task: stakeholder-manager agent
Final communications:
- Thank you message to community
- Celebrate what was achieved
- Acknowledge loyal users
- Share learnings (if appropriate)
- Redirect to alternatives

End on positive, grateful note
```

## Phase 8: Post-Sunset (Month 12+)

### Post-Mortem
```
Task: product-strategist agent
Conduct sunset retrospective:
- **What went well?**
- **What was challenging?**
- **What would we do differently?**
- **Learnings for future sunsets**
- **Customer feedback themes**
- **Financial impact**
- **Team impact**

Create sunset retrospective document
```

```
Command: /stakeholder-management:decision-logger
Decision: Lessons from [product] sunset
Document learnings for future reference
```

### Ongoing Support
```
Task: customer-success agent
Limited post-sunset support:
- FAQ and archived documentation
- Redirect to archived content
- No active support
- Community resources if available

Manage residual inquiries
```

## Deliverables

1. **Sunset Business Case** - Why sunsetting and impact analysis
2. **Sunset Timeline** - Detailed 6-12 month plan
3. **Migration Guide** - Options and resources for users
4. **Communication Plan** - Internal, customer, public messaging
5. **Migration Tools** - Data export and transition support
6. **FAQ Document** - Comprehensive questions and answers
7. **Support Playbook** - How to support migration
8. **Shutdown Checklist** - Infrastructure and data cleanup
9. **Retrospective** - Learnings and improvements

## Success Metrics
- Migration rate >80%
- Customer sentiment neutral to positive
- Support volume manageable
- Revenue impact minimized
- No legal issues
- Smooth technical shutdown
- Team learnings captured

## Sunset Best Practices
- **Give adequate notice** (6-12 months typical)
- **Be transparent** about why
- **Provide alternatives** and migration paths
- **Make export easy** - comprehensive data export
- **Support generously** - dedicated resources
- **Communicate frequently** - regular updates
- **Show empathy** - acknowledge disruption
- **End gracefully** - thank users

## Common Sunset Mistakes
- Insufficient notice period
- Poor communication (surprise)
- No migration path or tools
- Inadequate export options
- Abrupt shutdown
- No customer support
- Defensive or blame-shifting messaging
- Ignoring contractual obligations
- No post-mortem or learnings captured
- Damaging brand and trust

## Sunset vs. Alternatives

Consider alternatives before sunsetting:
- **Maintenance mode** - Keep running, no new features
- **Open source** - Community takeover
- **Sell or transfer** - Find buyer or partner
- **Pivot** - Transform into something new
- **Merge** - Consolidate with another product

Only sunset when truly best option for customers and business.
