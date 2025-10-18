# Risk Assessment

Identify, analyze, and mitigate risks for features, projects, and strategic initiatives.

## Usage

```
/pm:risks [feature or project name] [optional: context, timeline]
```

## What This Command Does

1. Identifies risks across product, technical, market, and execution dimensions
2. Assesses probability and impact for each risk
3. Prioritizes risks using risk matrix (high/medium/low)
4. Develops mitigation strategies and contingency plans
5. Creates monitoring plan to track risks over time
6. Takes 30 minutes vs 2 hours of manual risk assessment

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Project/Feature Context**:
- What are we building/launching?
- Timeline and key milestones
- Team and resources involved
- Dependencies on other teams/systems

**Strategic Context**:
- Business goals and success metrics
- Competitive landscape
- Market conditions
- Regulatory/compliance requirements

**Historical Context**:
- Similar projects we've done
- Past failures or challenges
- Known organizational risks

**Example Input**:
```
Project: Enterprise tier launch
Timeline: 8 weeks to launch
Team: 10 engineers, 2 designers, 1 PM
Dependencies: Legal (compliance), Sales (enablement)
Business Goal: $500K ARR in first 6 months
Known Risks: Team has never built enterprise features before
```

### 2. Identify Risks by Category

**Product Risks**:
- Market fit uncertainty
- User adoption challenges
- Feature complexity
- Competitive threats

**Technical Risks**:
- Technical feasibility
- Scalability/performance
- Security vulnerabilities
- Integration complexity

**Execution Risks**:
- Resource constraints
- Timeline pressure
- Dependency delays
- Team capability gaps

**Business Risks**:
- Revenue impact
- Cost overruns
- Regulatory/compliance
- Reputation damage

### 3. Assess Each Risk

**Probability**: How likely is this to happen?
- High (>50% chance)
- Medium (20-50% chance)
- Low (<20% chance)

**Impact**: If it happens, how bad is it?
- High (Critical - blocks launch or major damage)
- Medium (Significant - delays or partial impact)
- Low (Minor - manageable impact)

**Risk Score** = Probability × Impact

### 4. Develop Mitigation Strategies

**For High Risks**:
- Proactive mitigation (prevent it happening)
- Contingency plan (if it happens, what do we do?)
- Monitoring triggers (how will we know it's happening?)

**For Medium Risks**:
- Mitigation plan
- Monitoring approach

**For Low Risks**:
- Accept and monitor
- No active mitigation unless it escalates

## Template

```markdown
# Risk Assessment: [Project/Feature Name]

**Date**: [YYYY-MM-DD]
**Assessed By**: [Your Name]
**Project**: [Brief description]
**Timeline**: [Start] - [Launch Date]

---

## Executive Summary

**Overall Risk Level**: 🔴 High | 🟡 Medium | 🟢 Low

**Critical Risks** (High Probability × High Impact): [X]
**High Risks** (Either High Prob or High Impact): [X]
**Medium Risks**: [X]
**Low Risks**: [X]

**Top 3 Risks to Watch**:
1. [Risk 1] - [Why critical]
2. [Risk 2] - [Why critical]
3. [Risk 3] - [Why critical]

**Recommendation**: [Proceed | Proceed with Mitigations | Delay | Don't Proceed]

---

## Risk Matrix

**Risk Prioritization**:

| Impact →<br>Probability ↓ | Low Impact | Medium Impact | High Impact |
|---------------------------|------------|---------------|-------------|
| **High Probability** | 🟡 Medium | 🔴 High | 🔴 **CRITICAL** |
| **Medium Probability** | 🟢 Low | 🟡 Medium | 🔴 High |
| **Low Probability** | 🟢 Low | 🟢 Low | 🟡 Medium |

**Our Risks Mapped**:
- 🔴 **Critical**: [List critical risks]
- 🔴 **High**: [List high risks]
- 🟡 **Medium**: [List medium risks]
- 🟢 **Low**: [List low risks]

---

## Critical Risks (Immediate Attention Required)

### Risk #1: [Risk Name]

**Category**: Product | Technical | Execution | Business

**Description**: [What could go wrong]

**Probability**: 🔴 High ([X]% chance)
**Impact**: 🔴 High (Critical)
**Risk Score**: 🔴 **CRITICAL**

**Triggers/Warning Signs**:
- [Sign 1 that this risk is materializing]
- [Sign 2]
- [Sign 3]

**Consequences if Risk Occurs**:
- [Impact 1]
- [Impact 2]
- [Impact 3]

**Mitigation Strategy** (Prevent):
1. [Action 1 to reduce probability]
2. [Action 2]
3. [Action 3]
- **Owner**: [Name]
- **Timeline**: [When to complete]
- **Cost**: [Resource investment]

**Contingency Plan** (If Occurs):
1. [Action 1 if risk materializes]
2. [Action 2]
3. [Action 3]
- **Trigger**: [When to activate contingency]
- **Owner**: [Name]

**Monitoring**:
- **Metric**: [What to track]
- **Frequency**: [How often to check]
- **Responsible**: [Who monitors]

**Status**: 🔴 Active | 🟡 Mitigating | 🟢 Resolved | ⚪ Accepted

---

[Repeat for each critical/high risk]

---

## Medium/Low Risks

| Risk | Category | Prob | Impact | Mitigation | Owner |
|------|----------|------|--------|------------|-------|
| [Risk 1] | [Cat] | Med | Med | [Brief mitigation] | [Name] |
| [Risk 2] | [Cat] | Low | High | [Brief mitigation] | [Name] |
```

---

## Best Practices

### DO ✅

- **Be pessimistic** - Better to over-identify risks than miss critical ones
- **Quantify probability and impact** - Use data when possible
- **Assign owners** - Every risk needs someone monitoring it
- **Plan contingencies** - Know what you'll do if it happens
- **Update regularly** - Reassess weekly for active projects
- **Focus on high risks** - Don't waste time on low risks
- **Learn from past** - What risks materialized in similar projects?

### DON'T ❌

- **Ignore black swans** - Low-probability/high-impact risks matter
- **Assess once and forget** - Risks evolve, reassess regularly
- **Over-mitigate low risks** - Focus resources on high risks
- **Hide risks** - Transparency builds trust
- **Skip contingency planning** - Hope is not a strategy

---

## Examples

### Example 1: Enterprise Launch

**Input**: "Assess risks for enterprise tier launch in 8 weeks"

**Output**:

```markdown
# Risk Assessment: Enterprise Tier Launch

---

## Critical Risks

### R1: Security Compliance Failure

**Probability**: Medium (40%)
**Impact**: High (Critical - can't launch)
**Risk Score**: 🔴 **HIGH**

**Mitigation**:
- Hire security consultant Week 1
- Security review every 2 weeks
- Penetration test Week 6

**Contingency**: Delay launch 2-4 weeks if audit fails

---

### R2: Timeline Slip

**Probability**: High (70%)
**Impact**: Medium (delay revenue)
**Risk Score**: 🔴 **HIGH**

**Mitigation**:
- Add experienced engineer consultant
- 2-week buffer in timeline
- Scope flex: audit logs can be v1.1

---

## Recommendation

**PROCEED WITH CONDITIONS**:
✅ Security consultant engaged
✅ 2-week buffer added
✅ Weekly risk reviews
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:mvp` - Scope MVP considering risks
- `/pm:scenario-planner` - Scenario planning for risk outcomes
- `/pm:decision-log` - Document risk decisions
- `product-strategist` agent - Strategic risk assessment
