# Edge Case and Error Handling Checklist

Comprehensive checklist for systematic edge case coverage and error handling in specifications.

---

## How to Use This Checklist

For every feature or user story, go through each category and identify which edge cases apply. Document how the system should handle each case.

**Format for each edge case:**

```
Scenario: [What happens]
Expected Behavior: [How system should respond]
User Experience: [What user sees/experiences]
System Behavior: [What happens behind the scenes]
```

---

## Category 1: Input Validation

### Empty/Null Inputs

- [ ] **Empty text fields**
  - Forms with no input
  - Required vs optional fields
  - Whitespace-only input

- [ ] **Null values**
  - Missing data in API requests
  - Null in database queries
  - Undefined variables

- [ ] **Zero values**
  - Numeric fields set to 0
  - When 0 is valid vs invalid

---

### Invalid Format Inputs

- [ ] **Email validation**
  - Missing @ symbol
  - Invalid domain
  - Special characters
  - Multiple @ symbols
  - Examples to handle:
    - ✓ Valid: user@example.com, name+tag@domain.co.uk
    - ✗ Invalid: user@, @domain.com, user@domain, user domain@example.com

- [ ] **Phone number validation**
  - Missing digits
  - Too many digits
  - Letters in phone number
  - International formats
  - Extensions

- [ ] **Date/time inputs**
  - Invalid dates (Feb 30, Month 13)
  - Date format mismatches
  - Time zones
  - Daylight saving time transitions
  - Past dates when future required
  - Future dates when past required

- [ ] **URL validation**
  - Missing protocol (http:// or https://)
  - Invalid characters
  - Localhost/internal URLs when public required
  - Relative vs absolute URLs

---

### Malicious Inputs

- [ ] **SQL injection attempts**
  - Input containing SQL keywords (DROP, SELECT, etc.)
  - Single quotes, double quotes
  - Semicolons
  - Comment indicators (--,

/_, _/)

- [ ] **XSS (Cross-site scripting) attempts**
  - <script> tags in input
  - JavaScript in URLs (javascript:)
  - Event handlers (onerror, onload)
  - Data URLs with scripts

- [ ] **Path traversal attempts**
  - ../../../etc/passwd
  - Absolute paths when relative expected
  - Special characters in filenames

- [ ] **Command injection**
  - Pipe characters |
  - Semicolons;
  - Backticks `
  - Shell variables $

- [ ] **Buffer overflow attempts**
  - Extremely long inputs
  - Repeated characters
  - Binary data

---

### Boundary Conditions

- [ ] **Maximum length exceeded**
  - Text inputs at max length
  - Text inputs exceeding max length
  - Database field limits

- [ ] **Numeric bounds**
  - Negative numbers when positive required
  - Decimals when integers required
  - Very large numbers (overflow)
  - Very small numbers (underflow)
  - Infinity, NaN

- [ ] **Collection limits**
  - Empty arrays/lists
  - Single-item arrays
  - Maximum capacity arrays
  - Just over maximum

---

## Category 2: Authentication & Authorization

### Authentication Issues

- [ ] **Not logged in**
  - Accessing protected resources
  - Session expired
  - Never logged in

- [ ] **Invalid credentials**
  - Wrong password
  - Wrong username
  - Account doesn't exist
  - Case sensitivity issues

- [ ] **Session management**
  - Expired sessions
  - Concurrent sessions
  - Session hijacking attempts
  - Logout while operations in progress

- [ ] **Token handling**
  - Expired tokens
  - Invalid tokens
  - Missing tokens
  - Tampered tokens

---

### Authorization Issues

- [ ] **Insufficient permissions**
  - User role doesn't have access
  - Trying to access others' data
  - Trying to perform admin actions

- [ ] **Resource ownership**
  - Editing someone else's content
  - Deleting someone else's content
  - Viewing private content

- [ ] **Permission edge cases**
  - User loses permission while editing
  - Shared resource with conflicting permissions
  - Group membership changes during operation

---

## Category 3: State Management

### Empty States

- [ ] **No data exists**
  - Empty search results
  - No saved items
  - New user with no history
  - Deleted all items

- [ ] **First-time experience**
  - Never configured settings
  - No preferences set
  - Empty dashboard/homepage

---

### Loading States

- [ ] **Data loading**
  - Show loading indicators
  - Handle slow loads (>5 seconds)
  - Handle very slow loads (>30 seconds)
  - Timeout handling

- [ ] **Progressive loading**
  - Partial data loaded
  - Images still loading
  - Lazy-loaded content

---

### Error States

- [ ] **Failed operations**
  - Save failed
  - Delete failed
  - Update failed
  - Clear error messaging

- [ ] **Recovery from errors**
  - Retry mechanisms
  - Rollback capabilities
  - Undo options

---

### Full/Capacity States

- [ ] **Storage full**
  - Disk space exhausted
  - Quota exceeded
  - Database full

- [ ] **Rate limits reached**
  - API rate limit
  - Upload limit
  - Request throttling

- [ ] **Maximum items**
  - Maximum users in team
  - Maximum files uploaded
  - Maximum connections

---

## Category 4: Concurrency & Race Conditions

### Simultaneous Operations

- [ ] **Concurrent edits**
  - Two users editing same document
  - Conflict resolution strategy
  - Last-write-wins vs merge vs conflict

- [ ] **Race conditions**
  - Read-modify-write conflicts
  - Duplicate submissions (double-click)
  - Simultaneous deletes

- [ ] **Lock handling**
  - Pessimistic locks (can't edit while locked)
  - Optimistic locks (edit conflict on save)
  - Deadlocks

---

### Stale Data

- [ ] **Outdated information**
  - Viewing old version after update elsewhere
  - Cache staleness
  - Refresh strategies

- [ ] **Version conflicts**
  - Saving over newer version
  - Merging divergent versions

---

## Category 5: Network & Infrastructure

### Network Issues

- [ ] **Connection lost**
  - Mid-operation disconnect
  - Offline mode
  - Reconnection handling

- [ ] **Slow connections**
  - Timeouts
  - Partial data received
  - Progress indicators

- [ ] **Request failures**
  - 400 Bad Request
  - 401 Unauthorized
  - 403 Forbidden
  - 404 Not Found
  - 429 Too Many Requests
  - 500 Internal Server Error
  - 502 Bad Gateway
  - 503 Service Unavailable
  - 504 Gateway Timeout

---

### Service Dependencies

- [ ] **External service down**
  - Payment processor unavailable
  - Email service down
  - Third-party API offline
  - Fallback strategies

- [ ] **Degraded performance**
  - Slow database queries
  - High load
  - Resource constraints

---

## Category 6: Data Integrity

### Missing Data

- [ ] **Required data missing**
  - Required fields not provided
  - Partial data submission
  - Corrupted data

- [ ] **Orphaned records**
  - Parent deleted but child remains
  - Foreign key violations
  - Dangling references

---

### Data Consistency

- [ ] **Inconsistent state**
  - Balance doesn't match transactions
  - Count doesn't match actual items
  - Derived data out of sync

- [ ] **Data format mismatch**
  - Expected JSON got XML
  - Expected string got number
  - Expected array got object

---

### Data Loss Prevention

- [ ] **Unsaved changes**
  - User navigates away with edits
  - Browser/app crashes
  - Accidental deletions

- [ ] **Backup and recovery**
  - Restore from backup
  - Point-in-time recovery
  - Data export

---

## Category 7: Time-Based Edge Cases

### Timing Issues

- [ ] **Expired items**
  - Expired coupons
  - Expired trials
  - Expired subscriptions
  - Expired sessions

- [ ] **Scheduled events**
  - Past scheduled time
  - Future scheduled time
  - Recurring events

- [ ] **Time zones**
  - Different user time zones
  - Daylight saving time transitions
  - Date line crossing

---

### Sequencing Issues

- [ ] **Out of order**
  - Messages arriving out of sequence
  - Events processed in wrong order
  - Timestamps not monotonic

---

## Category 8: User Behavior

### Unexpected Actions

- [ ] **Rapid clicking**
  - Double-click submit button
  - Spam clicking
  - Duplicate requests

- [ ] **Back button usage**
  - Browser back after form submission
  - Forward button
  - History navigation

- [ ] **Bookmark/direct URL**
  - Bookmarking middle of flow
  - Sharing URLs with session state
  - Direct URL access to protected pages

---

### Abandonment

- [ ] **Incomplete flows**
  - Start checkout, never finish
  - Multi-step form abandonment
  - Registration not completed

- [ ] **Idle timeout**
  - User inactive for extended period
  - Session expiration during work
  - Auto-save vs manual save

---

## Category 9: Cross-Browser & Cross-Device

### Browser Compatibility

- [ ] **Older browsers**
  - IE11 support (if required)
  - Feature detection vs user-agent sniffing
  - Polyfills for missing features

- [ ] **JavaScript disabled**
  - Graceful degradation
  - Server-side rendering fallbacks

- [ ] **Cookies/storage disabled**
  - LocalStorage unavailable
  - Cookies blocked
  - Private/incognito mode

---

### Device-Specific

- [ ] **Mobile constraints**
  - Small screen sizes
  - Touch vs mouse
  - Orientation changes (portrait/landscape)
  - Slow connections

- [ ] **Accessibility devices**
  - Screen readers
  - Keyboard-only navigation
  - Voice control

---

## Category 10: Business Logic Edge Cases

### Financial Operations

- [ ] **Currency handling**
  - Rounding errors
  - Currency conversion
  - Negative amounts
  - Refunds exceeding original amount

- [ ] **Payments**
  - Partial payments
  - Refunds
  - Chargebacks
  - Split payments

---

### Inventory/Availability

- [ ] **Stock levels**
  - Out of stock
  - Overselling (stock becomes negative)
  - Reserved/held inventory
  - Stock becomes available during checkout

---

### Discounts/Promotions

- [ ] **Promo code edge cases**
  - Invalid code
  - Expired code
  - Already used (single-use)
  - Doesn't apply to cart items
  - Minimum purchase not met
  - Multiple codes (allowed or not?)

---

## Error Handling Template

For each edge case identified, document using this format:

```markdown
### Edge Case: [Name]

**Scenario:**
[Describe what happens]

**Frequency:** [How often this occurs: Common / Occasional / Rare]

**Impact:** [Critical / High / Medium / Low]

**Expected System Behavior:**

1. [What system does internally]
2. [How it logs/monitors]
3. [Whether it retries]

**User Experience:**

- **Error Message:** "[Exact error message shown]"
- **UI State:** [What happens to UI - disable buttons, show error, etc.]
- **Recovery Action:** [What user can do to fix/retry]

**Example:**

Scenario: User submits form with invalid email format
Expected System Behavior:

1. System validates email format client-side before submission
2. System displays inline error on email field
3. System prevents form submission until corrected

User Experience:

- **Error Message:** "Please enter a valid email address (e.g., name@example.com)"
- **UI State:** Email field highlighted in red, error message below field, submit button remains enabled
- **Recovery Action:** User corrects email and resubmits
```

---

## Prioritization Framework

Not all edge cases are equal. Prioritize coverage using this framework:

### Must Handle (P0)

- Security vulnerabilities
- Data loss scenarios
- Payment failures
- Authentication/authorization issues
- Scenarios causing crashes/errors

### Should Handle (P1)

- Common user mistakes
- Network issues
- Browser compatibility
- Mobile-specific issues
- Accessibility concerns

### Nice to Handle (P2)

- Rare edge cases with low impact
- Cosmetic issues
- Advanced browser features
- Obscure device configurations

---

## Testing Checklist

For each edge case documented:

- [ ] Unit test exists
- [ ] Integration test exists
- [ ] Manual test case documented
- [ ] Error message is user-friendly
- [ ] Error is logged for debugging
- [ ] Metrics track frequency
- [ ] User can recover without data loss

---

## Review Questions

Before considering edge case coverage complete, answer:

1. What happens if this field is empty?
2. What happens if this value is negative?
3. What happens if the user loses internet connection right now?
4. What happens if two users do this at the same time?
5. What happens if this external service is down?
6. What happens if the user hits back button?
7. What happens if the user's permission changes mid-operation?
8. What happens at midnight/month boundary/year boundary?
9. What happens if someone intentionally tries to break this?
10. What happens if this takes 10x longer than expected?

---

## Related Templates

- `assets/prd-structure-template.md` - Document edge cases in PRD
- `assets/user-story-template.md` - Include edge cases in acceptance criteria
- `assets/use-case-template.md` - Document as exception flows
- `references/specification-anti-patterns.md` - Avoid common mistakes
