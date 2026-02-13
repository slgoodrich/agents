# Technical Debt Story Template

Template for documenting technical improvements, refactoring, and infrastructure work.

---

## Template

```
Title: [Technical improvement]

As a [developer/team/system]
I want to [technical change]
So that [technical benefit and business value]

Technical Context:
[Explanation of current technical debt or limitation]

Proposed Solution:
[How we'll improve it]

Acceptance Criteria:
- [ ] [Technical outcome 1]
- [ ] [Technical outcome 2]
- [ ] [Measurement of improvement]
- [ ] [Tests added or updated]
- [ ] [Documentation updated]

Impact:
- Performance: [Improvement metric or N/A]
- Maintainability: [How it helps developers]
- Scalability: [Future benefit]
- Security: [If applicable]

Risks:
[Potential issues or migration concerns]

Story Points: [Estimate]
Priority: [High / Medium / Low]
```

---

## Example: Database Query Optimization

```
Title: Optimize slow dashboard query

As a developer
I want to refactor the dashboard analytics query
So that users see their dashboard load in under 2 seconds

Technical Context:
The main dashboard query fetches user analytics by joining 4 tables with no indexes. As data has grown to 1M+ records, the query now takes 8-12 seconds, causing timeouts and poor UX. Current query scans full tables on every page load.

Proposed Solution:
1. Add composite indexes on frequently joined columns
2. Implement query result caching (Redis, 5-minute TTL)
3. Denormalize key metrics into summary table (updated nightly)
4. Add query monitoring and slow query alerts

Acceptance Criteria:
- [ ] Dashboard loads in <2 seconds (p95) for datasets up to 5M records
- [ ] Database indexes added on user_id, created_at, status columns
- [ ] Redis caching implemented with 5-minute TTL
- [ ] Summary table created with nightly batch job
- [ ] Query performance tests added to test suite
- [ ] Monitoring dashboard shows query performance metrics
- [ ] No regression in data accuracy
- [ ] Documentation updated with caching strategy

Impact:
- Performance: 8-12s → <2s (85% improvement)
- Maintainability: Clear caching strategy documented, easier to debug
- Scalability: Can handle 10x data growth without degradation
- Security: N/A

Risks:
- Cache invalidation complexity (mitigated by 5-min TTL)
- Migration requires database downtime (~5 min during low-traffic window)
- Summary table adds storage cost (~100MB)

Story Points: 5
Priority: High (user-facing performance issue)
```

---

## Example: Code Refactoring

```
Title: Refactor authentication module for testability

As a developer
I want to refactor the authentication module
So that we can write unit tests and catch auth bugs before production

Technical Context:
Authentication logic is currently tightly coupled to Express middleware with hard-coded dependencies. This makes it impossible to unit test without spinning up full server. Code has grown to 800 lines in single file, making it hard to understand and modify.

Proposed Solution:
1. Extract core auth logic into pure functions
2. Inject dependencies (database, session store) for testability
3. Split into smaller modules by responsibility (login, logout, session, tokens)
4. Add comprehensive unit test coverage

Acceptance Criteria:
- [ ] Auth logic extracted into pure, testable functions
- [ ] Dependencies injected via constructor/parameters
- [ ] Module split into 4 files: login.js, logout.js, session.js, tokens.js
- [ ] Unit test coverage >85% for auth module
- [ ] All existing integration tests still pass
- [ ] No change to external API (backward compatible)
- [ ] Code review approved by 2 senior developers

Impact:
- Performance: No change (refactor only)
- Maintainability: Much easier to understand, modify, and test
- Scalability: Easier to add new auth methods (OAuth, SSO) in future
- Security: Better test coverage reduces risk of auth bugs

Risks:
- Regression risk (mitigated by existing integration tests + new unit tests)
- Learning curve for team (mitigated by documentation + pairing)

Story Points: 8
Priority: Medium (important but not urgent)
```

---

## Guidance

### Framing Technical Work for Team members

Technical debt stories should connect to business value:

**Poor framing**: "Refactor authentication code"
**Good framing**: "Refactor authentication so we can test it thoroughly and prevent security bugs"

**Poor framing**: "Upgrade React version"
**Good framing**: "Upgrade React to get performance improvements and security patches"

Always answer: "Why does this matter to the business/users?"

---

## Impact Categories

### Performance

Measurable speed improvements:

- Page load time reduced
- Query execution faster
- API response time decreased
- Server costs reduced

### Maintainability

Developer productivity:

- Easier to understand code
- Faster to add new features
- Reduced debugging time
- Better onboarding for new developers

### Scalability

Future capacity:

- Handle more users/data
- Easier horizontal scaling
- Reduced infrastructure costs at scale

### Security

Risk reduction:

- Patches vulnerabilities
- Improves authentication/authorization
- Better data protection
- Compliance requirements met

---

## Prioritization Guidance

### High Priority

- Blocks new features
- Causes production issues
- Security vulnerabilities
- Significant performance impact
- High-interest debt (getting worse fast)

### Medium Priority

- Slows feature development
- Moderate performance impact
- Needed for upcoming features
- Team velocity impact

### Low Priority

- Nice to have
- Small improvements
- Future-proofing
- Code cleanliness

**Tip**: Allocate 15-20% of sprint capacity to technical debt to prevent accumulation.

---

## When to Use This Template

Use for:

- Refactoring existing code
- Performance optimizations
- Infrastructure improvements
- Library/dependency upgrades
- Test coverage improvements
- Code quality enhancements

**Not for**:

- New features (use feature-story-template.md)
- Bug fixes (use bug-fix-story-template.md)
- Research tasks (use spike-research-story-template.md)
