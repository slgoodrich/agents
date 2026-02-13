# Use Case Template

Detailed template for documenting system interactions and behavior scenarios.

---

## Use Case Format

**Use Case:** [Action-oriented name, typically verb + noun]

**ID:** [Unique identifier, e.g., UC-001]

**Priority:** [Critical / High / Medium / Low]

**Status:** [Draft / In Review / Approved / Implemented]

---

## Primary Information

### Primary Actor

[The user or system initiating this use case]

**Examples:**

- New user
- Authenticated user
- System administrator
- External API
- Scheduled job

---

### Goal

[What the actor is trying to accomplish]

**Format:** [Verb + outcome]

**Examples:**

- Create account to access platform
- Complete purchase to own product
- Export data for external analysis

---

### Scope

[System or component this use case covers]

**Examples:**

- User Authentication System
- E-commerce Checkout Flow
- Reporting Module

---

### Level

[Abstraction level of this use case]

- **Summary:** High-level business process (spanning multiple systems)
- **User Goal:** Complete task that delivers value (most common)
- **Subfunction:** Detailed step within a user goal

---

## Preconditions

**What must be true before this use case can start:**

- [Precondition 1]
- [Precondition 2]
- [Precondition 3]

**Examples:**

- User has valid email address
- User is on registration page
- Database connection is available
- User has sufficient privileges

---

## Postconditions

### Success Postconditions

**What is true after successful completion:**

- [Postcondition 1]
- [Postcondition 2]
- [Postcondition 3]

**Examples:**

- Account created and activated
- User logged in
- Welcome email sent
- User redirected to dashboard

---

### Failure Postconditions

**What is true after failure:**

- [State after failure]
- [What's been rolled back]
- [What's been logged]

---

## Main Success Scenario (Happy Path)

**Step-by-step flow when everything goes right:**

1. [Actor] [action]
2. [System] [response/validation]
3. [Actor] [action]
4. [System] [response/processing]
5. [System] [final action/state change]

**Example:**

1. User navigates to registration page
2. System displays registration form
3. User enters email, password, and name
4. System validates inputs
5. System creates user account
6. System sends verification email
7. User clicks verification link in email
8. System activates account
9. System redirects user to dashboard

---

## Alternative Flows

### Alternative Flow 1: [Scenario Name]

**Trigger:** [What causes this alternative path]

**Steps:**

1. [Action at the branching point]
2. [Alternative handling]
3. [Resolution]

**Outcome:** [Where flow returns to main scenario or ends]

---

### Alternative Flow 2: [Scenario Name]

**Trigger:** [What causes this alternative path]

**Steps:**

1. [Action at the branching point]
2. [Alternative handling]
3. [Resolution]

**Outcome:** [Where flow returns to main scenario or ends]

---

## Exception Flows (Error Handling)

### Exception 1: [Error Scenario]

**Trigger:** [What causes this error]

**Steps:**

1. [System detects error]
2. [System handles error]
3. [System notifies user]

**Resolution:** [Use case ends / returns to step X / retries]

---

### Exception 2: [Error Scenario]

**Trigger:** [What causes this error]

**Steps:**

1. [System detects error]
2. [System handles error]
3. [System notifies user]

**Resolution:** [Use case ends / returns to step X / retries]

---

## Special Requirements

### Non-Functional Requirements

**Performance:**

- [Requirement with metric]

**Security:**

- [Security requirement]

**Usability:**

- [Usability requirement]

**Reliability:**

- [Reliability requirement]

---

## Frequency of Use

[How often is this use case executed?]

- Continuously
- Multiple times per day
- Daily
- Weekly
- Monthly
- Rare

**Business Context:** [Why frequency matters]

---

## Assumptions

**Assumptions made for this use case:**

- [Assumption 1]
- [Assumption 2]
- [Assumption 3]

---

## Open Issues

**Unresolved questions:**

1. [Issue 1]
   - **Status:** [Open / Resolved]
   - **Owner:** [Who's resolving this]

2. [Issue 2]
   - **Status:** [Open / Resolved]
   - **Owner:** [Who's resolving this]

---

## Example Use Case 1: User Registration

### Use Case: User Registers for Account

**ID:** UC-001

**Priority:** Critical

**Status:** Approved

---

**Primary Actor:** New user

**Goal:** Create account to access platform features

**Scope:** User Authentication System

**Level:** User Goal

---

**Preconditions:**

- User has valid email address
- User is on registration page
- Email service is operational

---

**Postconditions (Success):**

- Account created in database
- Account is active (after email verification)
- User is logged in
- Welcome email sent
- User profile initialized

**Postconditions (Failure):**

- No account created
- User remains on registration page
- Error logged for debugging

---

**Main Success Scenario:**

1. User navigates to registration page
2. System displays registration form (email, password, name fields)
3. User enters email, password, and full name
4. User clicks "Create Account" button
5. System validates inputs:
   - Email format is valid
   - Email is not already registered
   - Password meets strength requirements (12+ chars, alphanumeric + special)
   - Name is provided
6. System creates user account in database (inactive status)
7. System generates verification token (expires in 24 hours)
8. System sends verification email with link
9. System displays message: "Check your email to verify your account"
10. User opens email and clicks verification link
11. System validates token (not expired, matches user)
12. System activates account
13. System logs user in automatically
14. System redirects user to dashboard
15. System sends welcome email

---

**Alternative Flows:**

**3a. User Chooses Social Login**

- **Trigger:** User clicks "Sign up with Google" instead of form
- **Steps:**
  1. System redirects to Google OAuth
  2. User authorizes application
  3. System receives user data from Google
  4. System creates account with Google email
  5. Account is immediately active (email pre-verified)
  6. Continue from step 13 (redirect to dashboard)

**10a. User Didn't Receive Email**

- **Trigger:** User clicks "Resend verification email"
- **Steps:**
  1. System checks if account exists and is unverified
  2. System generates new verification token
  3. System sends new verification email
  4. System displays: "Verification email resent"
  5. Resume from step 10 (user checks email)

---

**Exception Flows:**

**5a. Email Already Registered**

- **Trigger:** Email exists in database
- **Steps:**
  1. System detects duplicate email
  2. System displays error: "This email is already registered"
  3. System offers options: "Log in instead" or "Reset password"
  4. Use case ends (user redirected to login or reset)

**5b. Password Too Weak**

- **Trigger:** Password doesn't meet requirements
- **Steps:**
  1. System validates password strength
  2. System displays error: "Password must be at least 12 characters with letters, numbers, and symbols"
  3. System highlights password field
  4. User enters new password
  5. Resume from step 4 (click Create Account)

**5c. Invalid Email Format**

- **Trigger:** Email format validation fails
- **Steps:**
  1. System validates email format
  2. System displays error: "Please enter a valid email address"
  3. System highlights email field
  4. User corrects email
  5. Resume from step 4

**8a. Email Service Unavailable**

- **Trigger:** Email sending fails (service down, network issue)
- **Steps:**
  1. System attempts to send email
  2. System catches email failure
  3. System queues email for retry
  4. System displays: "Account created! Verification email will arrive shortly."
  5. System retries email send every 5 minutes (up to 1 hour)
  6. If all retries fail, system logs error and notifies ops team

**11a. Verification Token Expired**

- **Trigger:** User clicks link >24 hours after registration
- **Steps:**
  1. System validates token
  2. System detects token expired
  3. System displays error: "Verification link expired. We'll send you a new one."
  4. System automatically sends new verification email
  5. Resume from step 10 (user checks email for new link)

**11b. Token Invalid/Tampered**

- **Trigger:** Token doesn't match any user or has been altered
- **Steps:**
  1. System validates token
  2. System detects invalid token
  3. System displays error: "Invalid verification link. Please register again or contact support."
  4. System logs security event
  5. Use case ends

---

**Special Requirements:**

**Performance:**

- Registration form submission response <1 second
- Email sent within 30 seconds of registration
- Verification link activates account <1 second

**Security:**

- Password hashed with bcrypt (cost factor 12)
- Verification tokens cryptographically random (256 bits)
- HTTPS required for all registration pages
- Rate limiting: Max 5 registration attempts per IP per hour
- Email verification required before account activation

**Usability:**

- Password strength indicator shows requirements
- Form remembers email if validation fails
- Clear error messages for all validation failures
- Mobile-responsive registration form

**Accessibility:**

- WCAG 2.1 Level AA compliant
- Keyboard navigation supported
- Screen reader compatible
- Focus indicators visible

---

**Frequency of Use:** Multiple times per day

**Business Context:** New user acquisition is critical growth driver. Smooth registration flow directly impacts conversion rate.

---

**Assumptions:**

- Users have access to email
- Users can receive and click links in email
- Email providers don't block verification emails
- Users register from supported browsers

---

**Open Issues:**

1. Should we support phone number registration in addition to email?
   - **Status:** Open
   - **Owner:** Product team

2. Should verification links work across devices or be device-locked?
   - **Status:** Resolved - Works across devices
   - **Owner:** Security team

---

## Example Use Case 2: Complete Online Purchase

### Use Case: User Completes Purchase

**ID:** UC-012

**Priority:** Critical

**Status:** Approved

---

**Primary Actor:** Authenticated user

**Goal:** Purchase products from cart and receive order confirmation

**Scope:** E-commerce Checkout System

**Level:** User Goal

---

**Preconditions:**

- User is logged in
- User has items in shopping cart
- Payment service is operational
- Inventory system is available

---

**Postconditions (Success):**

- Order created in database
- Payment charged successfully
- Inventory decremented
- Order confirmation email sent
- User receives order number
- User redirected to order confirmation page

**Postconditions (Failure):**

- No order created
- No payment charged
- Inventory unchanged
- User returned to checkout with error message

---

**Main Success Scenario:**

1. User clicks "Proceed to Checkout" from cart
2. System displays checkout form with sections: shipping, payment, review
3. User enters/confirms shipping address
4. System validates address format
5. System calculates shipping cost based on address
6. User selects shipping method (standard, express, overnight)
7. System updates total with shipping cost
8. User enters payment information (credit card details)
9. System validates card format (Luhn algorithm)
10. User reviews order: items, shipping, payment, total
11. User clicks "Place Order"
12. System creates order record (pending status)
13. System charges payment via payment processor
14. Payment processor returns success
15. System updates order status to confirmed
16. System decrements inventory for all items
17. System sends order confirmation email
18. System displays order confirmation page with order number
19. Use case ends successfully

---

**Alternative Flows:**

**8a. User Selects Saved Payment Method**

- **Trigger:** User clicks "Use saved card"
- **Steps:**
  1. System displays saved payment methods
  2. User selects card ending in [last 4 digits]
  3. User enters CVV for security
  4. Continue from step 10 (review order)

**3a. User Has Saved Addresses**

- **Trigger:** User has previously used addresses
- **Steps:**
  1. System displays saved addresses
  2. User selects address or enters new address
  3. Continue from step 4 (validate address)

**11a. User Applies Promo Code**

- **Trigger:** User clicks "Have a promo code?"
- **Steps:**
  1. System displays promo code input field
  2. User enters code
  3. System validates code (not expired, applicable to cart)
  4. System applies discount to total
  5. System displays updated total
  6. Continue from step 10 (review order)

---

**Exception Flows:**

**13a. Payment Declined - Insufficient Funds**

- **Trigger:** Payment processor returns "insufficient funds"
- **Steps:**
  1. System receives payment failure
  2. System deletes pending order
  3. System displays error: "Payment declined due to insufficient funds. Please use a different payment method."
  4. System returns user to payment step
  5. Resume from step 8 (enter payment info)

**13b. Payment Declined - Invalid Card**

- **Trigger:** Payment processor returns "invalid card"
- **Steps:**
  1. System receives payment failure
  2. System deletes pending order
  3. System displays error: "Card information is invalid. Please check your details."
  4. System highlights card number field
  5. Resume from step 8

**13c. Payment Service Timeout**

- **Trigger:** Payment processor doesn't respond within 30 seconds
- **Steps:**
  1. System times out waiting for payment response
  2. System marks order as "payment pending"
  3. System displays: "We're still processing your payment. You'll receive email confirmation shortly."
  4. System queues payment status check every 2 minutes
  5. If payment eventually succeeds: continue from step 15 (confirm order)
  6. If payment eventually fails: send cancellation email, return items to inventory

**16a. Item Out of Stock During Checkout**

- **Trigger:** Inventory check shows insufficient stock
- **Steps:**
  1. System checks inventory before decrementing
  2. System detects insufficient stock for [Item]
  3. System cancels order
  4. System refunds payment immediately
  5. System displays error: "[Item] is no longer in stock. Your payment was refunded."
  6. System removes out-of-stock item from cart
  7. User can continue shopping or checkout with remaining items
  8. Use case ends (order not completed)

**4a. Invalid Shipping Address**

- **Trigger:** Address validation fails (invalid format or undeliverable)
- **Steps:**
  1. System validates address against postal service API
  2. System detects invalid address
  3. System displays error: "We couldn't verify this address. Please check the details."
  4. System highlights address fields with issues
  5. Resume from step 3 (enter address)

---

**Special Requirements:**

**Performance:**

- Checkout page load <2 seconds
- Payment processing <5 seconds
- Order confirmation displayed <10 seconds total
- Handles 100 concurrent checkouts

**Security:**

- PCI DSS compliant payment handling
- No credit card numbers stored (use tokenization)
- SSL/TLS encryption for all checkout pages
- 3D Secure authentication for high-value orders (>$500)

**Reliability:**

- 99.9% checkout availability
- Payment failures handled gracefully with clear messaging
- Automatic retry for transient failures
- Transaction idempotency (prevent double-charging)

---

**Frequency of Use:** 500-1000 times per day

**Business Context:** Checkout conversion is critical revenue driver. Each 1% improvement in checkout completion = significant revenue increase.

---

## Use Case Template Checklist

Before finalizing a use case:

- [ ] Title is action-oriented (verb + noun)
- [ ] Primary actor identified
- [ ] Goal clearly stated
- [ ] Preconditions documented
- [ ] Postconditions for success and failure documented
- [ ] Main success scenario written step-by-step
- [ ] All major alternative flows documented
- [ ] All exception flows documented
- [ ] Special requirements specified
- [ ] Frequency of use estimated
- [ ] Assumptions listed
- [ ] Open issues tracked

---

## Related Templates

- `assets/prd-structure-template.md` - Full PRD structure for larger features
- `assets/user-story-template.md` - Agile-friendly story format
- `assets/job-story-template.md` - Context-based alternative format
- `references/specification-anti-patterns.md` - Common mistakes to avoid
