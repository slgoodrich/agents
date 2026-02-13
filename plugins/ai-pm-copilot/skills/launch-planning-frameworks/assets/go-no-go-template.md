# Go/No-Go Decision Template

Framework for making launch readiness decisions one week before launch.

---

## Go/No-Go Meeting

**Date**: [T-1 week from launch]
**Time**: [Time]
**Duration**: 60 minutes
**Decision Maker**: [PM / Exec Sponsor]

**Attendees (Required)**:

- PM (Launch Owner)
- Engineering Lead
- Marketing Lead
- Sales Lead (if Tier 1/2)
- CS Lead
- Support Lead
- Exec Sponsor (if Tier 1)

---

## Decision Criteria

### Must-Have Criteria (Hard Blockers)

These must all be YES to launch:

#### 1. Product Stability

- [ ] **YES** | [ ] NO: No critical (P0) bugs
- [ ] **YES** | [ ] NO: No high (P1) bugs that impact core functionality
- [ ] **YES** | [ ] NO: Feature is stable (no crashes, no data loss)
- [ ] **YES** | [ ] NO: Performance meets SLAs (load time, API response)

**If NO**: What are the bugs? Can they be fixed in 1 week?

---

#### 2. Technical Readiness

- [ ] **YES** | [ ] NO: Deployed to staging successfully
- [ ] **YES** | [ ] NO: Load testing passed (handles 2x expected traffic)
- [ ] **YES** | [ ] NO: Monitoring and alerting configured
- [ ] **YES** | [ ] NO: Rollback plan tested and working
- [ ] **YES** | [ ] NO: Security review complete (no critical vulnerabilities)

**If NO**: What's missing? What's the timeline to complete?

---

#### 3. Team Readiness

- [ ] **YES** | [ ] NO: Sales team trained and confident
- [ ] **YES** | [ ] NO: Support team trained with runbook
- [ ] **YES** | [ ] NO: CS team ready with customer communications
- [ ] **YES** | [ ] NO: Marketing assets complete and scheduled

**If NO**: Which team needs more time? How much time?

---

#### 4. Messaging & Communication

- [ ] **YES** | [ ] NO: Positioning finalized and approved
- [ ] **YES** | [ ] NO: Key messaging validated with customers
- [ ] **YES** | [ ] NO: Customer communications written and approved
- [ ] **YES** | [ ] NO: Internal company communications ready

**If NO**: What needs to be finalized? Can it be done in 1 week?

---

### Nice-to-Have Criteria (Soft Preferences)

These are NOT blockers, but note concerns:

#### Product Polish

- [ ] All P2 (nice-to-have) features complete
- [ ] All UI/UX refinements done
- [ ] All edge cases handled gracefully

#### Marketing Readiness

- [ ] Press coverage secured (Tier 1 only)
- [ ] Influencer/partner amplification lined up
- [ ] Paid campaign creative approved

#### Business Readiness

- [ ] Early customer commitments secured
- [ ] Sales pipeline forecast updated
- [ ] Pricing/packaging finalized

**Assessment**: Are missing nice-to-haves acceptable for launch?

---

## Risk Assessment

### Identified Risks

For each risk, assess **likelihood** and **impact**:

**Risk 1**: [Describe risk]

- Likelihood: High / Medium / Low
- Impact: High / Medium / Low
- Mitigation: [How we'll handle it]

**Risk 2**: [Describe risk]

- Likelihood: High / Medium / Low
- Impact: High / Medium / Low
- Mitigation: [How we'll handle it]

**Risk 3**: [Describe risk]

- Likelihood: High / Medium / Low
- Impact: High / Medium / Low
- Mitigation: [How we'll handle it]

**Critical risks** (High likelihood + High impact):

- [ ] None
- [ ] [List critical risks and whether they're acceptable]

---

## Readiness Scores

Rate each function 1-5:

- 1 = Not ready at all
- 3 = Somewhat ready, have concerns
- 5 = Fully ready and confident

| Function            | Score (1-5) | Concerns        |
| ------------------- | ----------- | --------------- |
| Product/Engineering | [ ] / 5     | [Note concerns] |
| Marketing           | [ ] / 5     | [Note concerns] |
| Sales               | [ ] / 5     | [Note concerns] |
| Customer Success    | [ ] / 5     | [Note concerns] |
| Support             | [ ] / 5     | [Note concerns] |

**Average Score**: [ ] / 5

**Threshold for GO**:

- All teams ≥ 4 = GO
- Any team < 3 = NO-GO
- Any team = 3 = CONDITIONAL GO (watch closely)

---

## Launch Confidence Poll

Each attendee votes:

**Confidence in launch success** (1-5 scale):

- 5 = Very confident, will be great
- 4 = Confident, minor concerns
- 3 = Neutral, could go either way
- 2 = Not confident, significant concerns
- 1 = Not confident at all, shouldn't launch

| Name        | Confidence | Main Concern |
| ----------- | ---------- | ------------ |
| [PM]        | [ ] / 5    | [Note]       |
| [Eng Lead]  | [ ] / 5    | [Note]       |
| [Marketing] | [ ] / 5    | [Note]       |
| [Sales]     | [ ] / 5    | [Note]       |
| [CS]        | [ ] / 5    | [Note]       |
| [Support]   | [ ] / 5    | [Note]       |
| [Exec]      | [ ] / 5    | [Note]       |

**Average**: [ ] / 5

**Threshold**: Average ≥ 4 = GO | Average < 3 = NO-GO

---

## Decision Framework

```
IF (All Must-Have Criteria = YES)
  AND (No Critical Risks)
  AND (Average Readiness ≥ 4)
  AND (Average Confidence ≥ 4)
THEN → GO

ELSE → Evaluate delay
```

---

## GO Decision

**Decision**: **GO** ✅

**Launch Date Confirmed**: [Date]

**Conditions for GO** (if any):

- [Condition 1 that must be met before launch]
- [Condition 2 that must be met before launch]

**Risks We're Accepting**:

- [Risk 1 - why we're accepting it]
- [Risk 2 - why we're accepting it]

**Monitoring Plan**:

- [What we'll watch closely on launch day]
- [Thresholds for rolling back]

**Rollback Criteria**:

- If [metric] goes below [threshold] → rollback
- If [error rate] exceeds [percentage] → rollback
- If [critical bug] discovered → rollback

**Sign-Off**:

- PM: **********\_\_\_********** Date: **\_\_\_**
- Engineering: ******\_\_\_****** Date: **\_\_\_**
- Marketing: ********\_******** Date: **\_\_\_**
- Exec Sponsor: ******\_\_****** Date: **\_\_\_**

---

## NO-GO Decision

**Decision**: **NO-GO** ❌

**Reason for Delay**:

- [ ] Product not stable
- [ ] Teams not ready
- [ ] Missing critical deliverables
- [ ] High-risk concerns
- [ ] Other: [Specify]

**Specific Blockers**:

1. [Blocker 1 - what's missing/broken]
2. [Blocker 2 - what's missing/broken]
3. [Blocker 3 - what's missing/broken]

**New Launch Date**: [Date] (X weeks delay)

**Action Plan to Unblock**:

| Blocker     | Owner  | Due Date | Status   |
| ----------- | ------ | -------- | -------- |
| [Blocker 1] | [Name] | [Date]   | [Status] |
| [Blocker 2] | [Name] | [Date]   | [Status] |
| [Blocker 3] | [Name] | [Date]   | [Status] |

**Next Go/No-Go Review**: [Date]

**Communication Plan**:

- [ ] Internal teams notified
- [ ] Customers notified (if public launch date)
- [ ] Revised timeline communicated
- [ ] Team members updated

**Sign-Off**:

- PM: **********\_\_\_********** Date: **\_\_\_**
- Exec Sponsor: ******\_\_****** Date: **\_\_\_**

---

## Post-Decision Actions

### If GO:

- [ ] Confirm launch timeline with all teams
- [ ] Final prep week activities begin
- [ ] War room scheduled
- [ ] Launch day runbook distributed
- [ ] Press/analyst briefings confirmed (Tier 1)

### If NO-GO:

- [ ] Communicate delay to all team members
- [ ] Update launch plan with new date
- [ ] Address blockers immediately
- [ ] Schedule next go/no-go review
- [ ] Manage customer expectations (if needed)

---

## Historical Context

**Past Go/No-Go Decisions** (for learning):

| Launch      | Date   | Decision                | Outcome              | Learnings                         |
| ----------- | ------ | ----------------------- | -------------------- | --------------------------------- |
| [Feature X] | [Date] | GO                      | Success              | [What went well]                  |
| [Feature Y] | [Date] | NO-GO (delayed 2 weeks) | Success after delay  | [Why delay was right call]        |
| [Feature Z] | [Date] | GO (with risks)         | Issues on launch day | [What we should have delayed for] |

**Key Learnings**:

- When in doubt, delay
- Quality > timeline
- Team confidence matters
- Better to launch great 1 week late than launch broken on time

---

**Key Principle**: The go/no-go decision protects the team, the company, and customers. It's not about hitting a date at all costs - it's about launching successfully. A delayed launch that succeeds is better than an on-time launch that fails.
