# Bug Fix Story Template

Template for documenting and tracking bug fixes in user story format.

---

## Template

```
Title: [Bug description]

As a [affected user]
I want [expected behavior]
So that [benefit/impact of fixing]

Current Behavior:
[What currently happens - the bug]

Expected Behavior:
[What should happen]

Steps to Reproduce:
1. [Step 1]
2. [Step 2]
3. [Step 3]
4. [Observe bug]

Acceptance Criteria:
- [ ] Bug no longer occurs following reproduction steps
- [ ] Regression tests added to prevent recurrence
- [ ] Related edge cases tested
- [ ] Root cause documented
- [ ] Fix verified in all affected environments

Environment:
- Browser/OS: [Details]
- Version: [Version]
- Device: [If applicable]

Severity: [Critical / High / Medium / Low]
Impact: [Number of users affected, business impact]
```

---

## Example: Payment Processing Bug

```
Title: Payment fails when using American Express cards

As a customer
I want to complete purchases using my American Express card
So that I can buy products without switching payment methods

Current Behavior:
When users enter American Express card details and click "Pay", the payment fails with error "Invalid card number" even though the card is valid.

Expected Behavior:
American Express cards should process successfully just like Visa/Mastercard.

Steps to Reproduce:
1. Add item to cart and proceed to checkout
2. Enter American Express card number: 378282246310005 (test card)
3. Enter valid expiry and CVV
4. Click "Pay Now"
5. Observe error: "Invalid card number"

Acceptance Criteria:
- [ ] American Express cards process successfully
- [ ] Test with multiple AmEx test cards (personal, corporate, international)
- [ ] Error no longer appears for valid AmEx cards
- [ ] Regression tests added for all card types (Visa, MC, AmEx, Discover)
- [ ] Fix verified in staging and production
- [ ] Root cause documented in tech spec

Environment:
- Browser: All browsers (Chrome, Safari, Firefox tested)
- Version: Production v2.3.1
- Payment gateway: Stripe

Severity: High
Impact: 15% of attempted transactions (AmEx market share), ~$5K/day in lost revenue
```

---

## Severity Levels

### Critical

- System down or major function broken
- Data loss or security vulnerability
- Affects all or majority of users
- No workaround available
- **Response time**: Immediate

### High

- Important feature broken
- Affects significant number of users
- Workaround is difficult or inconvenient
- Revenue impact
- **Response time**: Same day

### Medium

- Feature partially broken
- Affects some users
- Workaround exists
- Minor revenue impact
- **Response time**: 2-3 days

### Low

- Minor issue or cosmetic problem
- Affects few users
- Easy workaround
- No revenue impact
- **Response time**: Next sprint

---

## Guidance

### Current vs Expected Behavior

Be specific and concrete:

- **Vague**: "Payment doesn't work"
- **Specific**: "Payment fails with error 'Invalid card number' for AmEx cards"

### Steps to Reproduce

Make it easy for developers and QA to verify:

1. Use numbered steps
2. Be specific about actions
3. Include test data if applicable
4. Note the exact error or unexpected behavior

### Acceptance Criteria

For bugs, include:

- Bug fix verification
- Regression test coverage
- Related scenarios tested
- Root cause analysis
- Cross-environment verification

### Impact Assessment

Help prioritize by documenting:

- Number of users affected
- Revenue impact
- User experience degradation
- Workarounds available
- Competitive implications

---

## When to Use This Template

Use for:

- Defects in existing features
- Regression bugs after releases
- User-reported issues
- QA-identified problems

**Not for**:

- Feature requests (use feature-story-template.md)
- Technical improvements (use technical-debt-story-template.md)
- Design changes (use feature-story-template.md)
