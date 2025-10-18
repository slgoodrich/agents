---
name: Product Crisis Management
description: Framework for managing product crises, incidents, and emergencies
category: Operations
duration: Hours to weeks (varies by severity)
model: sonnet
---

# Product Crisis Management Workflow

Structured approach for responding to product crises including outages, security breaches, data losses, PR incidents, and critical bugs.

## Usage
```
/crisis-management [crisis description]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- What is the crisis (outage, security breach, data loss, PR incident, critical bug)
- When did it start (timeline)
- Who/how many affected (users, customers, scale of impact)
- Current status (ongoing, contained, resolved)
- Severity level (if known: SEV1/2/3/4)
- Teams involved or needed

## Crisis Severity Levels

### SEV1: Critical Crisis
- **Impact**: Total outage, data breach, severe security issue, major PR crisis
- **Users affected**: All or majority
- **Response time**: Immediate (minutes)
- **Team**: All hands on deck
- **Duration**: Hours to days

### SEV2: Major Issue
- **Impact**: Partial outage, significant feature broken, moderate security issue
- **Users affected**: Significant portion
- **Response time**: Within 1 hour
- **Team**: Core response team
- **Duration**: Hours to days

### SEV3: Minor Issue
- **Impact**: Limited functionality issue, cosmetic bug, small user segment
- **Users affected**: Small portion
- **Response time**: Same day
- **Team**: Standard support
- **Duration**: Days to week

## Phase 1: Incident Detection & Declaration (Minutes)

### Detect Crisis
```
Task: product-ops agent
Crisis detection triggers:
- **Monitoring alerts** - System down, errors spiking
- **Customer reports** - Support tickets flooding in
- **Social media** - Public complaints trending
- **Security alerts** - Breach detected
- **Team discovery** - Internal testing finds critical issue
- **Press inquiry** - Media asking about incident

Assess severity immediately
```

### Declare Incident
```
Task: product-ops agent
Declare incident and severity:
- Assess scope and impact
- Declare severity level (SEV1/2/3)
- Notify incident response team
- Create incident channel (Slack, Teams)
- Start incident log and timeline
- Activate response protocol

Create incident declaration
```

### Assemble Response Team
```
Task: stakeholder-manager agent
Mobilize crisis response team:

**SEV1 Core Team**:
- **Incident Commander** - Overall coordination
- **Technical Lead** - Engineering response
- **Customer Lead** - Customer communication
- **PR/Comms Lead** - External communication
- **Legal** (if needed) - Compliance, liability
- **Executive Sponsor** - Decision authority

**SEV2/3**: Subset of above based on needs

Assign clear roles and responsibilities
```

## Phase 2: Immediate Response (Minutes to Hours)

### Assess Situation
```
Task: technical-pm agent
Rapid situation assessment:
- **What happened?** - Facts only, no speculation
- **When did it start?** - Timeline
- **Who's affected?** - User segments, scale
- **What's the impact?** - Severity of consequences
- **What's the cause?** (if known) - Root cause
- **What's our exposure?** - Worst case scenario

Update every 15-30 minutes as learn more
Create situation summary
```

### Immediate Containment
```
Task: technical-pm agent
Stop the bleeding:
- **Halt rollout** - Stop any ongoing deploys
- **Activate failover** - Switch to backup systems
- **Isolate issue** - Prevent spread
- **Emergency patch** - Quick fix if available
- **Rollback** - Revert to last known good state
- **Rate limiting** - Reduce load if needed

Prioritize stability over full function
```

### Internal Communication
```
Task: stakeholder-manager agent
Immediate internal updates:
- **Leadership** - Executive briefing
- **Company-wide** - Transparency about situation
- **Sales/CS** - Talking points for customers
- **Support team** - How to handle inquiries

Updates every 30-60 minutes during crisis
```

## Phase 3: Customer Communication (30-60 minutes)

### Initial Customer Notification
```
Task: stakeholder-manager agent
Notify affected customers ASAP:

**Status Page Update** (within 30 min):
- "We are investigating reports of [issue]"
- Impact and affected services
- Current status and what we're doing
- Next update time commitment

**Direct Communication** (within 60 min):
- Email to affected customers (if possible to identify)
- In-app notification
- Social media acknowledgment

**Tone**: Transparent, empathetic, action-oriented
```

```
Task: customer-success agent
Provide customer support:
- Dedicated crisis support channel
- FAQ with known information
- Workarounds if available
- Proactive outreach to key accounts
- Escalation path for critical issues

Staff up support immediately
```

### Ongoing Updates
```
Task: stakeholder-manager agent
Regular communication cadence:

**SEV1**: Updates every 30-60 minutes
**SEV2**: Updates every 2-4 hours
**SEV3**: Updates daily

Even if "no new information" - communicate that
- What we know
- What we're doing
- When next update
- Where to get help

Consistency builds trust
```

## Phase 4: Investigation & Resolution (Hours to Days)

### Root Cause Investigation
```
Task: technical-pm agent
Parallel investigation and resolution:

**Immediate team**:
- Fix the crisis (restore service)
- Implement workarounds
- Monitor stability

**Investigation team**:
- Determine root cause
- Identify contributing factors
- Check for other exposure
- Document timeline and actions

Create incident investigation log
```

### Coordinate Fix Development
```
Task: technical-pm agent
Develop and deploy fix:
- Design solution
- Test thoroughly (don't rush and break more)
- Deploy to test environment
- Gradual rollout with monitoring
- Verification of fix
- Continued monitoring

Balance speed with safety
```

### Monitor Resolution
```
Task: data-scientist agent
Validate resolution:
- Error rates returning to normal
- Customer reports declining
- System metrics healthy
- No new issues introduced
- Sustained stability (not transient)

Don't declare victory too early
```

## Phase 5: Resolution Communication (Hours to Days)

### Resolution Announcement
```
Task: stakeholder-manager agent
Announce resolution:

**Status page**:
- "Issue has been resolved"
- Summary of what happened
- What was done
- Ongoing monitoring
- Link to post-mortem (when available)

**Customer communication**:
- Direct notification to affected customers
- Apology for disruption
- Summary of resolution
- Steps to prevent recurrence
- How to contact support if still issues

**Internal**:
- Thank team for response
- Share resolution details
- Plan for post-mortem
```

### Post-Resolution Monitoring
```
Task: technical-pm agent
Extended monitoring period:
- Watch for regression
- Monitor for related issues
- Gradual rollback of emergency measures
- Return to normal operations slowly

Don't assume it's over too quickly
```

## Phase 6: Customer Recovery (Days to Weeks)

### Customer Impact Assessment
```
Task: customer-success agent
Assess customer impact:
- Who was affected and how severely?
- Lost data or transactions
- Business impact on customers
- Contractual SLA violations
- Revenue impact to customers

Create customer impact report
```

### Customer Remediation
```
Task: customer-success agent
Make customers whole:

**Possible remediation**:
- Service credits or refunds
- Extended trial or free period
- Priority support
- Account upgrades
- Custom solutions
- Personal apology calls

**High-touch customers**:
- Executive-level apology
- Dedicated recovery support
- Custom remediation plan
- Relationship repair

Create remediation program
```

```
Task: stakeholder-manager agent
Reputation repair:
- Public apology if appropriate
- Transparency about what happened
- Commitment to improvement
- Share lessons learned
- Demonstrate accountability

Rebuild trust through action
```

## Phase 7: Post-Mortem Analysis (Days to Weeks)

### Conduct Post-Mortem
```
Task: product-strategist agent
Blameless post-mortem:

**Timeline reconstruction**:
- What happened and when (minute by minute)
- Actions taken
- Decision points
- Contributing factors

**Root cause analysis**:
- Immediate cause
- Contributing causes
- Systemic issues
- Process failures

**What went well**:
- Effective actions
- Good decisions
- Successful practices

**What went poorly**:
- Ineffective actions
- Poor decisions
- Process gaps

**Action items**:
- Immediate fixes (completed)
- Short-term improvements (1-2 weeks)
- Long-term prevention (1-6 months)
- Process changes
- Tool/system improvements
- Training needs

Create comprehensive post-mortem document
Reference: Google SRE post-mortem template
```

```
Command: /pm:decision-logger
Decision: Learnings from [incident]
Document decisions and action items
```

### Share Learnings
```
Task: product-ops agent
Share post-mortem:

**Internal**:
- All-company presentation
- Technical deep-dive for engineering
- Customer-facing teams briefing
- Update runbooks and playbooks

**External** (if appropriate):
- Public post-mortem blog post
- Transparency builds trust
- Show commitment to improvement
- Technical credibility

Balance transparency with legal/competitive concerns
```

## Phase 8: Prevention & Improvement (Weeks to Months)

### Implement Preventive Measures
```
Task: technical-pm agent
Execute improvement plan:

**Technical improvements**:
- Fix root causes
- Improve monitoring and alerting
- Better testing and QA
- Circuit breakers and failsafes
- Redundancy and backup systems
- Graceful degradation

**Process improvements**:
- Update incident response process
- Improve communication templates
- Better escalation paths
- Training and drills
- Documentation improvements

Create improvement roadmap
```

```
Command: /pm:risk-assessment
Context: [Incident type] prevention
Assess remaining risks and mitigation
```

### Test Improvements
```
Task: technical-pm agent
Validate improvements:
- Chaos engineering / game days
- Load testing
- Failover drills
- Communication drills
- Incident simulations

Practice crisis response when not in crisis
```

### Crisis Preparedness
```
Task: product-ops agent
Build crisis readiness:

**Documentation**:
- Incident response playbook
- Communication templates
- Runbooks for common incidents
- Escalation contacts
- Customer remediation policies

**Training**:
- Team onboarding on crisis protocols
- Regular crisis simulation drills
- Customer communication training
- Leadership crisis training

**Tools**:
- Incident management system
- Status page
- Communication platforms
- Monitoring and alerting
- Backup and failover systems

Create crisis preparedness program
```

## Deliverables

1. **Incident Timeline** - Minute-by-minute event log
2. **Status Updates** - All customer communications
3. **Resolution Summary** - What happened and how resolved
4. **Customer Impact Report** - Who affected and how
5. **Remediation Plan** - How making customers whole
6. **Post-Mortem Document** - Comprehensive analysis
7. **Action Items** - Improvements and prevention measures
8. **Updated Playbooks** - Crisis response documentation

## Crisis Communication Principles

### DO:
- Communicate quickly (even if incomplete information)
- Be transparent and honest
- Take responsibility
- Show empathy
- Provide regular updates
- Explain what you're doing
- Give realistic timelines

### DON'T:
- Speculate or guess
- Blame others (customers, vendors, team)
- Minimize the issue
- Make promises you can't keep
- Go dark / hide
- Use jargon or technical excuses
- Declare victory prematurely

## Success Metrics
- Time to detect (<5 minutes)
- Time to customer notification (<30 min for SEV1)
- Time to resolution (varies by severity)
- Customer satisfaction post-crisis
- SLA compliance
- Learnings implemented
- Similar incidents prevented

## Crisis Scenarios to Plan For

### Technical Crises:
- Complete outage
- Data breach or security incident
- Data loss or corruption
- Performance degradation
- Third-party service failure

### Product Crises:
- Critical bug in production
- Harmful feature or content
- Privacy violation
- Accessibility failure
- Compliance violation

### Business Crises:
- PR incident
- Executive departure
- Acquisition or pivot
- Funding issues
- Legal action

## Crisis Prevention

Best crisis management is prevention:
- Robust testing and QA
- Gradual rollouts
- Feature flags
- Monitoring and alerting
- Incident simulations
- Regular disaster recovery tests
- Culture of reliability
- Blameless post-mortems
- Continuous improvement
