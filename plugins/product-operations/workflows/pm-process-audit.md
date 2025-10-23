---
description: Comprehensive audit of PM processes, practices, and effectiveness
category: Operations
duration: 2-3 weeks
model: sonnet
---

# Product Management Process Audit

Systematic assessment of product management processes, tools, and practices to identify inefficiencies and opportunities for improvement.

## Usage
```
/pm-process-audit
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Team size and structure (number of PMs, designers, eng, reporting structure)
- Current PM practices and tools (what's working, what's not)
- Pain points or specific areas of concern
- Recent changes or growth (team scaling, new products, org changes)
- Goals for audit (improve velocity, better alignment, reduce friction)

## Timeline: 2-3 Weeks

## Phase 1: Current State Assessment (Week 1)

### Process Inventory
```
Task: product-ops agent
Document all current PM processes:

**Strategy & Planning**:
- Vision and strategy development
- OKR setting and tracking
- Roadmap planning and updates
- Quarterly planning process
- Annual planning process

**Discovery & Research**:
- Customer research cadence
- User interview process
- Feedback collection and synthesis
- Market analysis
- Competitive intelligence

**Delivery & Execution**:
- Specification and PRD process
- Sprint planning and ceremonies
- Backlog management
- Prioritization framework
- Release process

**Communication & Collaboration**:
- Stakeholder updates
- Team meetings and rituals
- Decision-making process
- Documentation practices
- Cross-functional collaboration

Create process inventory map
```

### Tools & Systems Audit
```
Task: product-ops agent
Inventory all PM tools and systems:
- Product management tools (roadmap, backlog)
- Analytics and data tools
- Customer feedback tools
- Collaboration tools
- Documentation tools
- Design tools
- Development/project tools

Assess for each:
- Adoption level (% of team using)
- Effectiveness (solving intended problem?)
- Integration (works with other tools?)
- Cost (worth the investment?)
- Redundancy (overlapping with others?)

Create tools assessment matrix
```

### Team Survey
```
Task: product-ops agent
Survey product team members:

**Process effectiveness** (1-5 scale):
- How clear is our product vision?
- How effective is our prioritization?
- How efficient is our delivery process?
- How well do we collaborate cross-functionally?
- How customer-informed are our decisions?
- How data-driven are we?

**Pain points** (open-ended):
- What slows you down most?
- What processes feel like busywork?
- Where do you get blocked?
- What information do you wish you had?
- What tools frustrate you?

**Improvement ideas**:
- What should we start doing?
- What should we stop doing?
- What should we do differently?

Create team survey analysis
```

### Stakeholder Feedback
```
Task: stakeholder-manager agent
Interview key stakeholders (5-10):
- Engineering leaders
- Design leaders
- Sales/GTM leaders
- Customer success leaders
- Executive team

Questions:
- How effective is product management?
- Where does PM add most value?
- Where does PM create friction?
- What would make PM more effective?
- What are we missing?

Create stakeholder feedback synthesis
```

## Phase 2: Metrics & Outcomes Analysis (Week 1-2)

### Delivery Metrics
```
Task: data-scientist agent
Analyze delivery effectiveness:
- **Velocity trends** - Improving or declining?
- **Cycle time** - Idea to production time
- **Predictability** - Hit commitments?
- **Scope creep** - How often?
- **Release frequency** - Increasing or decreasing?
- **Feature adoption** - % of shipped features actually used
- **Time to value** - How long for customers to get value

Create delivery metrics dashboard
```

### Customer Impact Metrics
```
Task: data-scientist agent
Analyze customer outcome metrics:
- **NPS and CSAT trends**
- **Feature request backlog** - Growing or shrinking?
- **Support ticket trends** - Increasing or decreasing?
- **Customer retention** - Improving or declining?
- **Time from feedback to fix** - How responsive?

Correlate with PM processes
```

### Business Outcomes
```
Task: data-scientist agent
Analyze business impact:
- **Revenue growth** - Accelerating or slowing?
- **Customer acquisition** - Improving or declining?
- **Market share** - Growing or shrinking?
- **Product-market fit** indicators
- **Competitive position**

Link to PM effectiveness
```

### Team Productivity
```
Task: product-ops agent
Assess team productivity:
- **PM time allocation** - Where does time go?
- **Meeting load** - Too many meetings?
- **Documentation overhead** - Too much or too little?
- **Context switching** - How often?
- **Blocked time** - How much?
- **Strategic vs. tactical** - Balance?

Create time audit analysis
```

## Phase 3: Best Practice Comparison (Week 2)

### Industry Benchmarking
```
Task: product-ops agent
Compare to industry best practices:

**Discovery practices**:
- Continuous discovery (weekly customer contact)
- Research cadence and rigor
- Data-driven decision making

**Planning practices**:
- OKR maturity
- Roadmapping approach
- Prioritization frameworks
- Resource allocation

**Delivery practices**:
- Agile maturity
- Specification quality
- Release processes
- Post-launch measurement

**Collaboration practices**:
- Cross-functional integration
- Stakeholder management
- Communication effectiveness

Create gap analysis vs. best practices
```

### PMM Maturity Assessment
```
Task: product-ops agent
Assess PM maturity across dimensions:

**Level 1 - Ad hoc**: Reactive, inconsistent, hero-driven
**Level 2 - Repeatable**: Some processes, inconsistently followed
**Level 3 - Defined**: Documented processes, consistently followed
**Level 4 - Managed**: Measured processes, continuous improvement
**Level 5 - Optimized**: Data-driven, continuously optimizing

Assess maturity in:
- Strategy and planning
- Discovery and research
- Delivery and execution
- Measurement and learning
- Collaboration and communication

Create maturity assessment scorecard
```

## Phase 4: Problem Identification (Week 2)

### Synthesize Findings
```
Task: product-ops agent
Synthesize all findings:
- **Strengths** - What's working well?
- **Weaknesses** - What's not working?
- **Inefficiencies** - What creates waste?
- **Gaps** - What's missing?
- **Redundancies** - What's duplicated?
- **Pain points** - What frustrates people?
- **Quick wins** - Easy improvements?
- **Systemic issues** - Root causes?

Create comprehensive findings report
```

### Prioritize Problems
```
Task: product-ops agent
Prioritize issues to address:
- **Impact** - How much does it matter? (1-5)
- **Urgency** - How soon to fix? (1-5)
- **Effort** - How hard to fix? (1-5)
- **Priority Score** - (Impact × Urgency) / Effort

Focus on high-impact, high-urgency, low-effort first

Create prioritized problem list
```

## Phase 5: Improvement Roadmap (Week 3)

### Process Improvements
```
Task: product-ops agent
Design process improvements:

**For each major issue, define**:
- Current state (what happens now)
- Desired state (what should happen)
- Changes needed (what to change)
- Success metrics (how to measure)
- Timeline (when to implement)
- Owner (who drives it)

Create process improvement plans
```

### Tools & Systems Recommendations
```
Task: product-ops agent
Tool stack optimization:

**Keep**:
- Effective, well-adopted tools
- Good integrations

**Sunset**:
- Redundant tools
- Low-adoption tools
- Poor ROI tools

**Add**:
- Gaps in tooling
- Integration opportunities
- Automation potential

**Optimize**:
- Better utilization of existing tools
- Improved integrations
- Training and enablement

Create tool stack roadmap
```

### Team Practices & Rituals
```
Task: agile-coach agent
Redesign team practices:

**Meetings to optimize**:
- **Add**: Missing collaboration/sync
- **Remove**: Low-value meetings
- **Improve**: Make existing meetings better
- **Cadence**: Right frequency

**Rituals to establish**:
- Weekly customer contact
- Sprint retrospectives
- Product reviews
- Strategy offsites
- Demo days

**Documentation standards**:
- What to document
- Where to document
- Templates and formats
- Review and maintenance

Create team practices playbook
```

### Capability Building
```
Task: product-ops agent
Identify skill and capability gaps:

**Skills needed**:
- Customer research
- Data analysis
- Technical depth
- Domain expertise
- Strategic thinking
- Stakeholder management

**Development plans**:
- Training programs
- Mentoring and coaching
- Hiring needs
- Knowledge sharing
- External resources

Create capability development plan
```

## Phase 6: Implementation Plan (Week 3)

### Phased Rollout
```
Task: product-ops agent
Create phased implementation plan:

**Phase 1 (Month 1): Quick Wins**
- High-impact, low-effort improvements
- Build momentum and credibility
- Demonstrate value of changes

**Phase 2 (Month 2-3): Process Changes**
- Implement new processes
- Tool changes and optimization
- Team training and enablement

**Phase 3 (Month 4-6): Culture & Capability**
- Skill development
- Advanced practices
- Continuous improvement culture

Create detailed implementation roadmap
```

### Change Management
```
Task: stakeholder-manager agent
Design change management approach:
- **Communication plan** - What, when, who
- **Training and enablement** - How to adopt new ways
- **Pilot programs** - Test before full rollout
- **Feedback loops** - Capture concerns and iterate
- **Champions** - Early adopters to evangelize
- **Resistance management** - Address concerns

Create change management plan
```

### Success Metrics
```
Task: product-ops agent
Define success metrics for improvements:

**Leading indicators** (can see quickly):
- Process adoption rates
- Meeting time reduced
- Documentation completeness
- Team satisfaction scores

**Lagging indicators** (take time):
- Delivery velocity improvement
- Customer satisfaction improvement
- Business outcomes improvement
- Team retention and morale

Create measurement framework
```

## Deliverables

1. **Process Inventory** - All current PM processes mapped
2. **Tools Assessment** - Evaluation of all tools and systems
3. **Team & Stakeholder Feedback** - Survey and interview synthesis
4. **Metrics Analysis** - Delivery, customer, business metrics
5. **Maturity Assessment** - PM maturity scorecard
6. **Problem Prioritization** - Issues ranked by impact
7. **Improvement Roadmap** - Phased plan for improvements
8. **Implementation Plan** - How to roll out changes
9. **Success Metrics** - How to measure improvement

## Success Metrics (6 months post-audit)
- Team satisfaction with PM processes improves by 30%+
- Delivery velocity improves by 20%+
- Meeting time reduced by 25%+
- Documentation quality and completeness improves
- Stakeholder satisfaction with PM increases
- Customer impact metrics improve
- Time spent on strategic work increases

## Audit Triggers
Run this audit when:
- New PM leader joins
- Team feedback indicates process problems
- Delivery velocity declining
- Stakeholder frustration with PM
- Significant team growth
- Every 1-2 years for mature teams
- After major organizational changes

## Common PM Process Problems
- **Too many meetings** - Calendar stuffed, no focus time
- **Analysis paralysis** - Too much process, too slow
- **Feature factory** - All delivery, no discovery
- **Ivory tower** - Strategy disconnected from execution
- **Tool sprawl** - Too many tools, poor integration
- **Inconsistent practices** - Everyone does it differently
- **Documentation debt** - Knowledge in people's heads
- **Stakeholder ping-pong** - Conflicting priorities
- **Data blindness** - Decisions not informed by data
- **Customer disconnect** - Not talking to users enough
