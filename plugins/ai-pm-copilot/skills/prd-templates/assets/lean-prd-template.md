# Lean PRD Template

**Use for**: Small features, enhancements, bug fixes
**Length**: 1-2 pages
**Audience**: Engineering team

**Note on Sections**: Lean PRDs focus on essentials. Include only sections where you have real data.

- **Required**: Problem, Solution, Requirements
- **Optional**: Success Criteria (include only if you have metrics - omit if not available)

---

# [Feature Name]

**Owner**: [PM Name] | **Status**: Draft / Review / Approved
**Target Release**: [Version/Date]

---

## Problem

[2-3 sentences describing the problem and who experiences it]

**Example**:
"Users frequently abandon the checkout process when they need to create an account. 35% of users who add items to cart never complete purchase. This costs us approximately $50K/month in lost revenue."

---

## Solution

[2-3 sentences describing the proposed solution]

**Example**:
"Add a 'Guest Checkout' option that allows users to complete purchase with just email and payment info. Account creation becomes optional after purchase is complete."

---

## Success Criteria

Define what success looks like with specific, measurable metrics.

- [Metric 1]: [Target]
- [Metric 2]: [Target]

**Example**:

- Cart-to-purchase conversion rate: 45% → 60%
- Guest checkout usage: >40% of new customer purchases
- Time to complete checkout: <3 minutes

---

## Requirements

List functional requirements in priority order.

1. [Requirement 1]
2. [Requirement 2]
3. [Requirement 3]

**Example**:

1. Add "Continue as Guest" button on checkout login screen
2. Collect minimal info for guest checkout: email, shipping address, payment
3. After purchase, offer account creation with pre-filled info
4. Send order confirmation email with guest access link
5. Store guest orders for 90 days with email-based retrieval

---

## Out of Scope

Explicitly list what you're NOT building in this version.

- [What we're NOT building]

**Example**:

- Passwordless login for returning guests (future consideration)
- Guest checkout on mobile app (web only for v1)
- Ability to merge guest orders into account retroactively
- Guest wishlist or saved items

---

## Open Questions

Track unresolved questions with owners and deadlines.

- [Question 1]
- [Question 2]

**Example**:

- How long should we store guest order data? (Owner: Legal, Due: Oct 15)
- Do we need PCI compliance review for guest payment? (Owner: Security, Due: Oct 20)
- Should guests receive marketing emails by default? (Owner: Marketing, Due: Oct 12)

---

## Notes

**When to use Lean PRD**:

- Feature is straightforward and well-understood
- Low cross-functional complexity
- Development effort < 1 week
- Primarily for engineering team consumption

**Keep it lean**:

- Focus on problem and solution, not process
- Skip sections that don't add value
- Use bullet points, not paragraphs
- Link to external docs instead of embedding
