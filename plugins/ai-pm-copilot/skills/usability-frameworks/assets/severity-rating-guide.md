# Usability Issue Severity Rating Guide

## Table of Contents

- [Why Rate Severity?](#why-rate-severity)
- [Three-Factor Severity Model](#three-factor-severity-model)
- [Combined Severity Ratings](#combined-severity-ratings)
- [Severity Rating Matrix](#severity-rating-matrix)
- [How to Rate an Issue: Step-by-Step](#how-to-rate-an-issue-step-by-step)
- [Special Considerations](#special-considerations)
- [Rating Worksheet](#rating-worksheet)
- [Example Rated Issues](#example-rated-issues)
- [Severity Rating Best Practices](#severity-rating-best-practices)
- [Communicating Severity to Team members](#communicating-severity-to-team-members)
- [Adjusting Severity Over Time](#adjusting-severity-over-time)

## Why Rate Severity?

Not all usability issues are created equal. Severity ratings help teams:

- Prioritize fixes effectively
- Allocate resources appropriately
- Communicate urgency to the team
- Track progress on critical issues

## Three-Factor Severity Model

Evaluate each usability issue using three dimensions:

### 1. Frequency

How often does this issue occur?

- **High**: More than 50% of users encounter this issue
- **Medium**: 10-50% of users encounter this issue
- **Low**: Less than 10% of users encounter this issue

**Examples**:

- High: Issue on the login page (100% of users log in)
- Medium: Issue in a secondary feature used by some users
- Low: Issue in an advanced admin setting

---

### 2. Impact

When the issue occurs, how severely does it affect the user?

- **High**: Prevents task completion, causes data loss, or creates serious errors
- **Medium**: Causes significant frustration, delays, or confusion but task can be completed
- **Low**: Minor annoyance or cosmetic issue

**Examples**:

- High: Can't save work, payment fails, can't log in
- Medium: Extra steps required, confusing labels, unclear error message
- Low: Minor visual glitch, typo, slightly awkward wording

---

### 3. Persistence

Do users overcome this issue once they learn about it?

- **High**: Problem persists even after users learn the system
- **Medium**: Users eventually learn workaround or adapt
- **Low**: One-time problem that users quickly overcome

**Examples**:

- High: Confusing error that keeps recurring
- Medium: Unusual pattern users learn after first encounter
- Low: Initial confusion that clears up immediately

---

## Combined Severity Ratings

Combine the three factors to determine overall severity:

### Critical (P0) - Fix Immediately

**Characteristics**:

- High frequency + High impact
- Affects majority of users
- Prevents core functionality
- May cause data loss or serious errors

**Examples**:

- Login doesn't work
- Payment processing fails
- Users lose unsaved work
- Critical feature is broken

**Action**: Drop everything, fix immediately, hotfix if needed

---

### Serious (P1) - Fix Before Next Release

**Characteristics**:

- High frequency + Medium impact
- Medium frequency + High impact
- Affects significant portion of users
- Causes major frustration or workflow disruption

**Examples**:

- Important filter doesn't work
- Confusing checkout flow causing cart abandonment
- Search returns irrelevant results
- Mobile navigation is broken

**Action**: Fix in next sprint, don't ship without addressing

---

### Moderate (P2) - Fix Soon

**Characteristics**:

- High frequency + Low impact
- Medium frequency + Medium impact
- Low frequency + High impact
- Noticeable but users can work around it

**Examples**:

- Missing keyboard shortcuts
- Unclear button labels in secondary features
- Inconsistent iconography
- Slow loading times on less-used pages

**Action**: Include in roadmap, fix within 1-2 release cycles

---

### Minor (P3) - Fix When Convenient

**Characteristics**:

- Low frequency + Low or Medium impact
- Medium frequency + Low impact + Low persistence
- Cosmetic or minor usability improvements

**Examples**:

- Typos in help text
- Minor visual inconsistencies
- Nice-to-have features
- Slightly awkward wording

**Action**: Track in backlog, fix during UI polish or when working on adjacent code

---

## Severity Rating Matrix

| Frequency/Impact     | High Impact     | Medium Impact  | Low Impact  |
| -------------------- | --------------- | -------------- | ----------- |
| **High Frequency**   | **P0 Critical** | **P1 Serious** | P2 Moderate |
| **Medium Frequency** | **P1 Serious**  | P2 Moderate    | P3 Minor    |
| **Low Frequency**    | P2 Moderate     | P3 Minor       | P3 Minor    |

**Note**: Persistence can elevate or lower a rating:

- High persistence: Consider moving up one level
- Low persistence: Consider moving down one level

---

## How to Rate an Issue: Step-by-Step

### Step 1: Describe the Issue Clearly

**Template**:

```
When [context/situation], users [observed behavior] instead of [expected behavior].
This causes [consequence].
```

**Example**:
"When checking out with a new payment method, users must re-enter their billing address even though it's already in their profile. This adds 2-3 minutes to checkout and causes frustration."

---

### Step 2: Assess Frequency

Ask:

- What % of users will encounter this?
- How often is this feature/page used?
- Is this in the critical path?

**Example**: "Checkout is used by 100% of purchasing users" → **High frequency**

---

### Step 3: Assess Impact

Ask:

- Can users complete their task?
- How much frustration does this cause?
- Are there workarounds?
- Does this cause errors or data loss?

**Example**: "Users can complete checkout, but it's annoying and takes longer" → **Medium impact**

---

### Step 4: Assess Persistence

Ask:

- Will users learn to avoid this?
- Does it get easier with experience?
- Is there a workaround they'll discover?

**Example**: "Users might learn to copy/paste, but it's annoying every time" → **High persistence**

---

### Step 5: Combine into Overall Rating

**Example**:

- Frequency: High
- Impact: Medium
- Persistence: High

**Result**: High frequency + Medium impact = **P1 Serious** (elevated by high persistence)

---

## Special Considerations

### Accessibility Issues

Accessibility issues that affect users with disabilities should generally be rated higher:

- **Blocker for screen reader users** → Treat as High impact
- **Missing keyboard navigation** → Treat as at least Medium impact

Many accessibility issues are infrequent (low % of users) but have high impact when they occur.

### New vs. Existing Issues

**New issues** (in features not yet released):

- Rate severity, then decide if it blocks launch
- P0/P1 typically block launch
- P2 might be acceptable depending on feature importance

**Existing issues** (in production):

- P0 requires immediate hotfix
- P1 fix in next planned release
- P2/P3 prioritize against other work

### Combination Issues

When multiple small issues compound:

- Several P3 issues in same flow might equal P2
- Document as both individual issues and systemic problem

---

## Rating Worksheet

Use this worksheet for each usability issue:

```markdown
## Issue #[Number]: [Short title]

**Description**:
When [context], users [behavior] instead of [expected].
This causes [consequence].

**Observed in**:

- [ ] Task: [Task name]
- [ ] Participants affected: [X out of Y]
- [ ] Video timestamps: [List]

**Frequency Assessment**:

- What % of users will encounter this? **\_**
- How often is this path used?
  - [ ] Always (critical path)
  - [ ] Frequently (common task)
  - [ ] Sometimes (secondary feature)
  - [ ] Rarely (edge case or advanced feature)
- **Frequency Rating**: [ ] High [ ] Medium [ ] Low

**Impact Assessment**:

- Can users complete the task?
  - [ ] No - task failure
  - [ ] Yes, but with significant effort/frustration
  - [ ] Yes, with minor annoyance
- Consequences:
  - [ ] Data loss or errors
  - [ ] Task abandonment
  - [ ] Extra time/steps required
  - [ ] Confusion or uncertainty
  - [ ] Cosmetic only
- **Impact Rating**: [ ] High [ ] Medium [ ] Low

**Persistence Assessment**:

- Will users learn workaround?
  - [ ] No, issue persists
  - [ ] Maybe, but still frustrating
  - [ ] Yes, one-time learning curve
- **Persistence Rating**: [ ] High [ ] Medium [ ] Low

**Overall Severity**: [ ] P0 Critical [ ] P1 Serious [ ] P2 Moderate [ ] P3 Minor

**Recommendation**:
[Suggested fix or improvement]

**Related Issues**:
[Link to similar issues or dependencies]
```

---

## Example Rated Issues

### Example 1: Cannot Save Form

**Description**: When users fill out a lengthy profile form and click "Save", nothing happens. The save button appears to work (button press animation) but data is not saved.

**Frequency**: High (affects all users updating profiles)
**Impact**: High (complete task failure, data loss)
**Persistence**: High (happens every time)

**Rating**: **P0 Critical**

**Reasoning**: This is a show-stopper. Users can't complete a core task, and they lose their work. Affects everyone who tries to update their profile.

---

### Example 2: Confusing Dashboard Labels

**Description**: Dashboard uses term "Workspaces" but users refer to them as "Projects." Users hesitate when looking for their projects and some click the wrong area initially.

**Frequency**: High (all users see dashboard)
**Impact**: Low (causes brief confusion but they find it)
**Persistence**: Low (users learn quickly that Workspace = Project)

**Rating**: **P2 Moderate**

**Reasoning**: High frequency keeps this from being P3, but low impact and persistence prevent it from being more severe. Fix during next terminology cleanup.

---

### Example 3: Missing Advanced Filter

**Description**: Power users want to filter by date range, but only preset filters (Today, This Week, This Month) are available. Users with custom needs can't filter precisely.

**Frequency**: Low (only power users, 10% of base)
**Impact**: Medium (workaround is exporting and filtering in Excel)
**Persistence**: High (they want this every time)

**Rating**: **P2 Moderate**

**Reasoning**: Low frequency suggests P3, but medium impact affecting a valuable user segment (power users) elevates to P2. Add to roadmap.

---

### Example 4: Button Color Inconsistency

**Description**: Primary action buttons are blue on most pages but green on the settings page. No user confusion observed, but visual inconsistency noted.

**Frequency**: Low (only seen if user visits settings)
**Impact**: Low (cosmetic, no usability impact)
**Persistence**: Not applicable (users don't notice)

**Rating**: **P3 Minor**

**Reasoning**: Pure cosmetic issue. Fix during next design system cleanup.

---

### Example 5: Mobile Keyboard Covers Input

**Description**: On mobile checkout, when users tap the credit card field, the keyboard covers the "Pay Now" button. Users must scroll to find the button after entering card details.

**Frequency**: Medium (40% of transactions on mobile)
**Impact**: Medium (confusing, causes hesitation, but users eventually scroll)
**Persistence**: High (happens every time on mobile)

**Rating**: **P1 Serious**

**Reasoning**: Medium frequency on high-value flow (checkout), causes friction in revenue-generating workflow. Medium persistence keeps this from being P0, but should be fixed soon.

---

## Severity Rating Best Practices

### Do's:

- Use data when available (analytics, testing notes)
- Consider frequency in context of entire user base
- Factor in business impact (revenue, retention, brand)
- Get team consensus on borderline issues
- Revisit ratings as you learn more

### Don'ts:

- Don't inflate severity to get attention
- Don't rate based on ease of fix (separate from severity)
- Don't ignore low-frequency/high-impact issues
- Don't forget accessibility impact
- Don't rate everything as Critical

---

## Communicating Severity to Team members

### For Executives:

"We found 3 critical issues (P0) that prevent users from checking out, 7 serious issues (P1) causing cart abandonment, and 15 moderate issues (P2) we should address in the next quarter."

### For Developers:

"Here are the P0/P1 issues we need to fix before launch, prioritized by user impact. P2/P3 issues are documented for future sprints."

### For Designers:

"The P1 issues cluster around the onboarding flow—we should redesign that entire experience. The P2/P3 issues are scattered and can be addressed individually."

---

## Adjusting Severity Over Time

Severity can change based on:

- **New data**: More users encounter issue than expected → increase severity
- **Product changes**: Feature becomes more critical → increase severity
- **Workarounds**: Users find alternative path → decrease severity
- **Business priorities**: Feature becomes strategic → increase severity

**Best practice**: Review issue severity quarterly or when priorities shift.

---

**Remember**: Severity ratings are a tool for decision-making, not rigid rules. Use judgment, consider context, and be willing to debate and adjust ratings as your understanding evolves.
