---
name: Scale Playbook Workflow
description: Framework for scaling product and operations from PMF to growth stage
category: Growth
duration: 6-12 months
model: sonnet
---

# Scale Playbook Workflow

Comprehensive framework for scaling a product that has achieved product-market fit through the growth stage while maintaining quality and culture.

## Usage
```
/scale-playbook [optional: current state and goals]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Current scale (ARR, users, team size, markets)
- PMF confidence level and evidence
- Target scale (12-18 month goals)
- Growth rate (current and target)
- Key scaling challenges anticipated (hiring, infrastructure, processes, culture)
- Resources available (funding, runway, team capacity)

## Overview

**When to use**: After achieving product-market fit (>40% "very disappointed" in Sean Ellis test, strong retention)

**Phases**: Foundation → Customer Acquisition → Team & Operations → Product Evolution → Sustainable Growth

## Phase 1: Validate Readiness to Scale (Month 1)

### PMF Validation
```
Task: product-strategist agent
Confirm readiness to scale:

**PMF Indicators** (must have):
- Sean Ellis score >40% "very disappointed"
- Retention curves plateau (not declining to zero)
- Organic growth and word-of-mouth
- Clear value proposition and messaging
- Defined customer segment
- Reasonable unit economics (LTV:CAC >2, improving)

**Warning signs to NOT scale**:
- Churn rate not stabilizing
- Only paid acquisition works
- Unclear who's the customer
- Product still changing dramatically
- Negative unit economics with no path to positive

Create PMF readiness scorecard
Reference product-market-fit skill
```

```
Command: /pm:pmf-assessment (use workflow)
Run comprehensive PMF assessment before scaling
```

### Unit Economics Validation
```
Task: monetization-expert agent
Validate unit economics can scale:

**Key metrics**:
- **CAC** (Customer Acquisition Cost): Stable or declining
- **LTV** (Lifetime Value): Stable or increasing
- **LTV:CAC ratio**: >3:1 (healthy), >2:1 (acceptable)
- **Payback period**: <12 months (B2B), <6 months (B2C)
- **Gross margin**: >70% (SaaS target)
- **Contribution margin**: Positive and improving

**Scaling projection**:
- Model economics at 2x, 5x, 10x scale
- Identify margin improvement opportunities
- Determine cash needs for growth

Create unit economics model
```

## Phase 2: Build Scaling Foundation (Month 1-3)

### Technical Infrastructure
```
Task: technical-pm agent
Prepare infrastructure to scale:

**Performance & Reliability**:
- Handle 10x current load
- <1% error rate
- <500ms response time (p95)
- 99.9%+ uptime
- Auto-scaling configured

**Instrumentation**:
- Comprehensive analytics
- Monitoring and alerting
- Error tracking
- Performance monitoring
- Customer data platform

**Technical debt**:
- Address critical tech debt
- Platform stability
- Code quality and testing
- Documentation
- Developer experience

Create technical scaling roadmap
```

### Data & Analytics Foundation
```
Task: data-scientist agent
Build data infrastructure for scale:

**Data collection**:
- Event tracking instrumented
- Product analytics (Amplitude, Mixpanel, etc.)
- Attribution and cohort tracking
- Customer data warehouse
- A/B testing platform

**Dashboards & Reporting**:
- Key metrics dashboards
- Funnel analysis
- Cohort retention
- Channel performance
- Business metrics

**Data governance**:
- Data quality processes
- Privacy compliance (GDPR, CCPA)
- Security and access control

Reference product-analytics skill
```

### Process & Operations
```
Task: product-ops agent
Establish scalable processes:

**Product processes**:
- Roadmap planning (quarterly)
- OKR setting and tracking
- Prioritization framework
- Launch processes
- Post-launch review

**Communication**:
- Weekly/monthly metrics reviews
- Stakeholder update cadence
- Cross-functional rituals
- Documentation standards
- Decision-making framework

**Tools & Systems**:
- Product management platform
- Documentation wiki
- Customer feedback tools
- Project management
- Communication tools

Create operations playbook
```

## Phase 3: Scale Customer Acquisition (Month 2-6)

### Channel Expansion
```
Task: gtm-planner agent
Scale and diversify acquisition channels:

**Optimize existing channels**:
- Double down on what's working
- Improve conversion funnels
- Increase spend efficiently
- Test and optimize continuously

**Expand to new channels**:
- Content marketing and SEO
- Paid advertising (search, social, display)
- Partnerships and integrations
- Sales (if B2B)
- Community and events
- PR and media

**Channel strategy**:
- Aim for 3-5 reliable channels
- Reduce reliance on single channel
- Understand CAC and payback by channel

Reference go-to-market-playbooks skill
```

```
Task: growth-pm agent
Build growth loops:
- **Viral loops** - User-driven growth
- **Content loops** - SEO and organic
- **Paid loops** - Efficient CAC
- **Sales loops** - Repeatable sales process

Create sustainable, compounding growth
Reference growth-frameworks skill
```

### Conversion Optimization
```
Task: growth-pm agent
Optimize conversion across funnel:

**Acquisition**:
- Landing page conversion
- Signup flow optimization
- Free trial/freemium flow

**Activation**:
- Onboarding conversion
- Time to value
- Aha moment clarity

**Revenue**:
- Free to paid conversion
- Pricing and packaging
- Upgrade flows

**Run continuous experiments**:
- 5-10 experiments per month
- Compound 1-2% improvements
- Build experimentation culture

Use experiment-design skill
```

### Sales Enablement (B2B)
```
Task: gtm-planner agent (if B2B)
Build scalable sales motion:

**Sales process**:
- Repeatable sales playbook
- Demo and POC process
- Qualification criteria (BANT/MEDDIC)
- Sales cycle optimization
- Forecasting and pipeline management

**Sales enablement**:
- Competitive battlecards
- Objection handling
- Case studies and proof points
- ROI calculators
- Sales training program

**Sales tools**:
- CRM (Salesforce, HubSpot)
- Sales engagement platform
- Demo environments
- Proposal automation

Create sales playbook
```

## Phase 4: Scale Team & Organization (Month 3-8)

### Team Structure
```
Task: product-ops agent
Design scaled team structure:

**Team organization** (at scale):
- **Product teams** - By customer segment, feature area, or journey
- **Platform team** - Shared services and infrastructure
- **Growth team** - Acquisition and activation
- **Data team** - Analytics and insights

**Roles to add**:
- Additional product managers
- Engineering managers
- Designers and researchers
- Data analysts
- Product operations
- Technical writers

**Span of control**:
- 1 PM per 5-8 engineers (typical)
- Cross-functional pods
- Clear ownership and autonomy

Create org chart and hiring plan
```

### Hiring & Onboarding
```
Task: product-ops agent
Build hiring and onboarding:

**Recruiting**:
- Define role requirements
- Sourcing strategies
- Interview process
- Assessment criteria
- Offer and closing process

**Onboarding**:
- 30/60/90 day plans
- Onboarding documentation
- Buddy/mentor program
- Learning resources
- Ramp-up projects

**Culture preservation**:
- Define values and ways of working
- Culture interview
- New hire culture immersion
- Regular culture reinforcement

Maintain quality bar while scaling
```

### Knowledge & Documentation
```
Task: product-ops agent
Scale knowledge and documentation:

**Product documentation**:
- Product strategy and vision
- Roadmap and priorities
- Feature specifications
- Architecture documentation
- API and integration docs

**Process documentation**:
- How we work
- Decision-making frameworks
- Templates and playbooks
- Meeting structures
- Communication norms

**Self-service resources**:
- Wiki or knowledge base
- Video walkthroughs
- FAQ and troubleshooting
- Best practices and patterns

Create documentation system
```

## Phase 5: Scale Product & Experience (Month 4-10)

### Feature Development at Scale
```
Task: product-strategist agent
Balance growth and product development:

**Resource allocation** (typical):
- 30-40% New features and capabilities
- 20-30% Growth and optimization
- 20-30% Technical debt and platform
- 10-20% Customer requests and bugs

**Prioritization at scale**:
- Clear prioritization framework
- Transparent roadmap
- Quarterly planning rhythm
- Cross-team dependencies managed
- Customer feedback loop

Use prioritization-methods skill
```

### Platform & Scalability
```
Task: platform-architect agent
Build platform capabilities:

**Platform services**:
- Authentication and authorization
- Notifications and messaging
- Integrations and API
- Data and reporting
- Admin and management tools

**Extensibility**:
- Plugin/extension architecture
- API for third-party integrations
- Customization capabilities
- White-label options (if relevant)

**Developer experience**:
- SDK and libraries
- Documentation and guides
- Sandbox environments

If platform business: Reference platform-strategy skill
```

### International Expansion
```
Task: gtm-planner agent (when ready)
Plan international scaling:

**Localization**:
- Language and translation
- Currency and payments
- Date/time and formatting
- Cultural adaptation

**Market entry**:
- Market selection and prioritization
- Local regulations and compliance
- Local partnerships
- Geo-specific features

**Infrastructure**:
- Data residency
- Performance and latency
- Payment processing
- Support coverage

Reference market-entry workflow
```

## Phase 6: Scale Customer Success (Month 4-10)

### Segmented Success Model
```
Task: customer-success agent
Design tiered success approach:

**Enterprise** (high touch):
- Dedicated customer success manager
- Quarterly business reviews
- Strategic planning support
- Executive relationship
- Custom onboarding and training

**Mid-market** (medium touch):
- Pooled CSM (1:20-40 ratio)
- Scaled onboarding
- Group training and webinars
- Health monitoring and intervention

**SMB/Self-serve** (low/no touch):
- Self-service onboarding
- In-app guidance and tutorials
- Automated emails and campaigns
- Community and peer support
- Usage-based health monitoring

Create customer success playbook
```

### Retention & Expansion
```
Task: customer-success agent
Build retention and expansion programs:

**Retention**:
- Churn prediction and prevention
- Health score monitoring
- At-risk customer intervention
- Onboarding completion tracking
- Feature adoption programs

**Expansion**:
- Upsell and cross-sell playbooks
- Usage-based expansion triggers
- Success milestones → upgrade prompts
- Multi-product strategy
- Land and expand motion

**Net revenue retention target**: >100% (ideal: >120%)
```

### Support at Scale
```
Task: customer-success agent
Scale support operations:

**Self-service support**:
- Help center and knowledge base
- In-app help and tutorials
- Community forum
- Chatbot for common questions

**Tiered support**:
- Email support (all customers)
- Chat support (paid tiers)
- Phone support (enterprise)
- Dedicated support (top tier)

**Support metrics**:
- First response time <2 hours
- Resolution time <24 hours
- CSAT >90%
- Deflection rate >50% (self-service)

Create support scaling plan
```

## Phase 7: Governance & Risk (Month 6-12)

### Compliance & Security
```
Task: technical-pm agent
Scale compliance and security:

**Security**:
- SOC 2 Type II certification
- Regular security audits
- Penetration testing
- Incident response plan
- Security training

**Compliance**:
- GDPR compliance (EU)
- CCPA compliance (California)
- Industry-specific (HIPAA, etc.)
- Data processing agreements
- Privacy policies and terms

**Risk management**:
- Business continuity plan
- Disaster recovery
- Data backup and retention
- Insurance coverage

Create compliance roadmap
```

### Financial Planning
```
Task: monetization-expert agent
Financial planning for scale:

**Budgeting**:
- Departmental budgets
- Headcount planning
- Marketing spend planning
- Infrastructure costs
- Tool and vendor management

**Forecasting**:
- Revenue projections
- Cash flow management
- Runway and burn rate
- Fundraising needs and timing
- Path to profitability

**Metrics tracking**:
- MRR/ARR and growth rate
- CAC and LTV
- Burn multiple
- Rule of 40
- Gross and net retention

Create financial model and dashboard
```

## Phase 8: Sustainable Growth Culture (Ongoing)

### Metrics & Accountability
```
Task: product-ops agent
Build metrics-driven culture:

**Key metrics**:
- North Star Metric
- Pirate metrics (AARRR)
- Team-level OKRs
- Individual KPIs
- Leading indicators

**Cadence**:
- Daily metric check-ins
- Weekly team reviews
- Monthly all-hands
- Quarterly business reviews
- Board reporting

**Transparency**:
- Metrics dashboards visible to all
- Regular all-hands updates
- Celebrating wins and learning from losses

Create metrics cadence and culture
```

### Continuous Improvement
```
Task: product-strategist agent
Build learning culture:

**Experimentation**:
- A/B testing continuously
- Innovation time (10-20%)
- Hackathons and demo days
- Fail fast, learn faster

**Feedback loops**:
- Customer feedback integration
- Team retrospectives
- Post-mortems (blameless)
- Competitive analysis
- Market monitoring

**Evolution**:
- Quarterly strategy reviews
- Annual planning cycles
- Product portfolio management
- Strategic pivots when needed

Stay agile even at scale
```

## Deliverables

1. **PMF Readiness Scorecard** - Validation to scale
2. **Unit Economics Model** - Financial viability at scale
3. **Technical Scaling Roadmap** - Infrastructure for 10x growth
4. **Growth Strategy** - Multi-channel acquisition plan
5. **Org Chart & Hiring Plan** - Team scaling roadmap
6. **Customer Success Playbook** - Segmented success model
7. **Operations Playbook** - Processes and systems
8. **Financial Model** - Revenue, costs, runway projections

## Success Metrics (12 months)
- Revenue growth >3x (triple)
- Customer growth >3-5x
- Net revenue retention >110%
- Customer acquisition cost stable or declining
- Team size scaled 2-3x
- Maintained or improved engagement metrics
- Maintained or improved NPS
- Sustainable unit economics (LTV:CAC >3)

## Scaling Challenges & Solutions

### Challenge: "Scaling breaks things"
**Solution**: Invest in infrastructure before it breaks, technical debt sprints

### Challenge: "Lost agility and speed"
**Solution**: Small autonomous teams, reduced dependencies, clear ownership

### Challenge: "Communication breakdown"
**Solution**: Structured communication, transparent metrics, regular rituals

### Challenge: "Culture dilution"
**Solution**: Intentional culture work, values-based hiring, onboarding immersion

### Challenge: "Quality decline"
**Solution**: Maintain quality bar in hiring, invest in QA and testing, slower controlled growth

### Challenge: "Founder/PM bottleneck"
**Solution**: Delegation, trust, empowerment, systems and processes

## Scale Stage Milestones

### Early Scale (ARR: $1-5M)
- PMF validated
- 10-30 person team
- Basic processes
- Single market/product

### Mid Scale (ARR: $5-20M)
- Multiple channels working
- 30-100 person team
- Defined processes
- Potential international/multi-product

### Late Scale (ARR: $20-100M)
- Repeatable growth motion
- 100-300 person team
- Mature operations
- Multi-market/multi-product

### At Scale (ARR: $100M+)
- Sustainable growth engines
- 300+ person team
- Enterprise-grade operations
- Platform ecosystem

Each stage requires evolution of systems, processes, and leadership.
