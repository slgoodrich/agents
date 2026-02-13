# Spike / Research Story Template

Template for time-boxed research, investigation, and proof-of-concept work.

---

## Template

```
Title: [Investigation topic]

As a [developer/PM/team]
I want to [research/investigate/prototype]
So that [decision/knowledge gained]

Research Questions:
1. [Question 1]
2. [Question 2]
3. [Question 3]

Acceptance Criteria:
- [ ] All research questions answered with evidence
- [ ] Recommendation documented with pros/cons
- [ ] Estimated effort for implementation (if applicable)
- [ ] POC code or diagrams created (if applicable)
- [ ] Findings shared with team
- [ ] Next steps or follow-up stories identified

Time Box: [X hours or Y days]
Deliverable: [Document, presentation, POC, technical spike]
Due Date: [When decision needed]
```

---

## Example: Technology Evaluation

```
Title: Evaluate real-time notification solutions

As a development team
I want to evaluate WebSocket vs Server-Sent Events vs polling for notifications
So that we can choose the best approach for our real-time notifications feature

Research Questions:
1. What are the pros/cons of WebSocket, SSE, and long polling for our use case?
2. What's the scalability profile of each approach (concurrent connections, server resources)?
3. What's browser support for each technology?
4. What libraries/services exist and what are their costs?
5. What's the implementation complexity for each approach?
6. How does each handle reconnection and offline scenarios?

Acceptance Criteria:
- [ ] Comparison matrix created for all 3 approaches
- [ ] POC implemented for top 2 approaches
- [ ] Load testing results documented (simulate 10K concurrent users)
- [ ] Browser compatibility verified (Chrome, Safari, Firefox, mobile)
- [ ] Cost analysis completed (infrastructure + services)
- [ ] Recommendation documented with pros/cons
- [ ] Estimated development effort for chosen approach
- [ ] Findings presented to team in 30-min session

Time Box: 3 days
Deliverable: Technical comparison doc + working POC + team presentation
Due Date: End of sprint (need to decide before next sprint planning)
```

---

## Example: Architecture Investigation

```
Title: Research microservices migration strategy

As a tech lead
I want to research how to migrate our monolith to microservices
So that we can improve scalability and team autonomy

Research Questions:
1. What are the main patterns for migrating monolith to microservices? (Strangler Fig, etc.)
2. What are the risks and common pitfalls?
3. How should we identify service boundaries?
4. What's the right first service to extract?
5. What infrastructure changes are needed (service mesh, API gateway, monitoring)?
6. What's the estimated timeline and effort?

Acceptance Criteria:
- [ ] Migration patterns researched and documented
- [ ] Service boundary analysis completed (using DDD or similar)
- [ ] First candidate service identified with justification
- [ ] Architecture diagram created for target state
- [ ] Risk assessment completed with mitigation strategies
- [ ] Phased migration plan proposed (6-12 month roadmap)
- [ ] Infrastructure requirements documented
- [ ] Team training needs identified
- [ ] Recommendation presented to engineering leadership

Time Box: 5 days
Deliverable: Migration strategy document + architecture diagrams + roadmap
Due Date: Before Q2 planning
```

---

## Example: User Research Spike

```
Title: Investigate user needs for collaborative features

As a product manager
I want to conduct user interviews about collaboration workflows
So that we can validate feature ideas before building

Research Questions:
1. How do users currently collaborate on projects?
2. What pain points exist in current collaboration workflows?
3. Would users value real-time collaborative editing?
4. What other collaboration features are most requested?
5. How much would users pay for collaboration features?

Acceptance Criteria:
- [ ] 10-15 user interviews completed
- [ ] Interview notes synthesized into themes
- [ ] Key pain points identified and prioritized
- [ ] Feature requests categorized by frequency
- [ ] Willingness-to-pay data collected
- [ ] User personas updated based on findings
- [ ] Recommendations for MVP scope documented
- [ ] Findings shared with product team

Time Box: 2 weeks
Deliverable: Research summary + user insights + MVP recommendations
Due Date: Before Q2 feature planning
```

---

## Guidance

### Time Boxing

Spikes must be time-boxed to prevent endless research:

**Too loose**: "Research caching solutions"
**Time-boxed**: "Research caching solutions (2 days max)"

Common time boxes:

- **1-2 hours**: Quick feasibility check
- **Half day**: Library comparison
- **1-2 days**: Technical spike with POC
- **3-5 days**: Complex architecture research
- **1-2 weeks**: User research or market analysis

### Research Questions

Good research questions are:

- **Specific**: Not "Is this a good idea?" but "What's the performance impact at 10K users?"
- **Actionable**: Answers lead to decisions
- **Scoped**: Can be answered in time box
- **Measurable**: Quantifiable where possible

### Acceptance Criteria for Spikes

Unlike feature stories, spike AC focuses on knowledge gained:

- Questions answered (with evidence)
- Decision recommendation
- Effort estimation
- POC or documentation
- Team communication

### Deliverables

Common spike deliverables:

- **Technical comparison**: Pros/cons matrix, recommendation
- **POC code**: Working prototype to validate approach
- **Architecture diagram**: Visual representation of proposed solution
- **Research summary**: User insights, competitive analysis
- **Effort estimate**: T-shirt size or story points for follow-up work

---

## After the Spike

Once spike is complete:

1. **Document findings** in team wiki or docs
2. **Present to team** (15-30 min)
3. **Create follow-up stories** based on recommendation
4. **Archive spike** (it's done, not ongoing)

**Example follow-up**:
After spike "Evaluate notification solutions", create:

- Feature story: "Implement WebSocket notifications"
- Technical story: "Set up Socket.io infrastructure"
- Research story: "Load test WebSocket at scale" (if needed)

---

## Common Spike Types

### Technical Spike

- Evaluate libraries/frameworks
- Prototype architecture
- Performance testing
- Feasibility investigation

### User Research Spike

- User interviews
- Usability testing
- Surveys
- Competitive analysis

### Business Spike

- Market research
- Pricing analysis
- Partnership exploration
- Compliance investigation

---

## When to Use This Template

Use for:

- Investigating technical approaches before committing
- Validating assumptions with research
- Exploring new technologies
- Architecture decisions
- User research
- Proof-of-concept development

**Not for**:

- Building production features (use feature-story-template.md)
- Fixing bugs (use bug-fix-story-template.md)
- Ongoing work (spikes are time-boxed and disposable)

**Remember**: Spikes don't ship to production. They inform decisions about what to build.
