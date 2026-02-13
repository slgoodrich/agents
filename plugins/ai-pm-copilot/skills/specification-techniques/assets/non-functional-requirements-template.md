# Non-Functional Requirements (NFR) Template

Comprehensive template for documenting quality attributes and system constraints.

---

## What Are Non-Functional Requirements?

**Functional Requirements:** Define WHAT the system does (features, capabilities)

**Non-Functional Requirements:** Define HOW WELL the system does it (quality attributes, constraints)

**Examples:**

- Functional: "Users can upload files"
- Non-Functional: "File upload completes in <5 seconds for files up to 10MB"

---

## NFR Template

**Feature/System:** [What this NFR applies to]

**Category:** [Performance / Security / Reliability / Scalability / Usability / etc.]

**Priority:** [Critical / High / Medium / Low]

**Status:** [Draft / In Review / Approved / Implemented]

---

## 1. Performance Requirements

### Response Time

**Definition:** How quickly the system responds to user actions

```
**Requirement ID:** PERF-001

**Description:** Page load time

**Metric:**
- Landing page: <1.5 seconds (p95)
- Dashboard: <2 seconds (p95)
- Search results: <1 second (p95)
- Report generation: <5 seconds (p95)

**Measurement Context:**
- Measured from: User's browser (real user monitoring)
- Network conditions: Good 4G connection (10 Mbps)
- Device: Desktop (Chrome, Firefox, Safari latest versions)
- Location: US East Coast data center proximity

**Test Conditions:**
- 100 concurrent users
- Typical data volumes (1000 products, 50 categories)
- Database with 1M records

**Verification:**
- Lighthouse performance score >90
- Real user monitoring (RUM) data
- Synthetic monitoring from multiple locations
```

---

### API Response Time

```
**Requirement ID:** PERF-002

**Description:** API endpoint response times

**Metrics:**
| Endpoint | p50 | p95 | p99 | Timeout |
|----------|-----|-----|-----|---------|
| GET /api/users | <100ms | <200ms | <500ms | 5s |
| POST /api/orders | <300ms | <500ms | <1s | 10s |
| GET /api/reports | <1s | <3s | <10s | 30s |

**Measurement Context:**
- Measured from: Application server
- Excludes network latency
- Includes database query time

**Verification:**
- APM tool (New Relic, Datadog)
- Load testing with JMeter/k6
```

---

### Throughput

```
**Requirement ID:** PERF-003

**Description:** Request handling capacity

**Metrics:**
- Requests per second (RPS): 1,000 sustained
- Concurrent users: 10,000
- Peak capacity: 5,000 RPS (burst for 5 minutes)

**Measurement Context:**
- Mix of read (70%) and write (30%) operations
- Typical request payload size <1MB
- Current infrastructure (6 application servers)

**Verification:**
- Load testing results
- Production metrics over 30-day period
```

---

### Resource Utilization

```
**Requirement ID:** PERF-004

**Description:** System resource usage

**Metrics:**
- CPU utilization: <70% average, <90% peak
- Memory utilization: <80% average, <95% peak
- Disk I/O: <70% capacity
- Network bandwidth: <60% capacity

**Rationale:** Headroom for traffic spikes and maintenance

**Verification:**
- Infrastructure monitoring (CloudWatch, Prometheus)
```

---

## 2. Security Requirements

### Authentication

```
**Requirement ID:** SEC-001

**Description:** User authentication requirements

**Requirements:**
- Multi-factor authentication (MFA) required for admin accounts
- Password complexity: minimum 12 characters, must include:
  - At least 1 uppercase letter
  - At least 1 lowercase letter
  - At least 1 number
  - At least 1 special character
- Password expiration: 90 days for standard users, 60 days for admins
- Account lockout: After 5 failed attempts, lock for 15 minutes
- Session timeout: 30 minutes inactivity, 8 hours absolute
- Password reuse: Cannot reuse last 5 passwords

**Verification:**
- Security audit
- Penetration testing
- Automated security scans (OWASP ZAP)
```

---

### Authorization

```
**Requirement ID:** SEC-002

**Description:** Access control requirements

**Requirements:**
- Role-Based Access Control (RBAC) with roles:
  - Super Admin (full system access)
  - Admin (manage users, view all data)
  - User (own data only)
  - Read-Only (view access only)
- Principle of least privilege enforced
- Audit log for all admin actions (who, what, when, IP)
- Cannot escalate own privileges
- Admin approval required for permission changes

**Verification:**
- Access control testing
- Audit log review
- Security compliance scan
```

---

### Data Protection

```
**Requirement ID:** SEC-003

**Description:** Data security requirements

**Requirements:**
- Encryption at rest: AES-256 for all PII
- Encryption in transit: TLS 1.3 minimum, TLS 1.2 fallback
- Database encryption: Transparent data encryption (TDE)
- Backup encryption: Encrypted with separate key
- Key management: AWS KMS or equivalent, keys rotated every 90 days
- PII handling: GDPR, CCPA, HIPAA compliant (as applicable)
- Right to deletion: 30-day retention after deletion request

**Data Classification:**
- Public: No restrictions
- Internal: Employees only
- Confidential: Specific roles only
- Restricted: Executive approval required

**Verification:**
- Encryption validation tests
- Compliance audit
- Vulnerability scanning
```

---

### Application Security

```
**Requirement ID:** SEC-004

**Description:** Application-level security

**Requirements:**
- Input validation: All user input sanitized
- Output encoding: Prevent XSS attacks
- SQL injection prevention: Parameterized queries only
- CSRF protection: Token-based
- Secure headers: CSP, HSTS, X-Frame-Options
- Dependency scanning: No high/critical vulnerabilities
- Secret management: No hardcoded secrets, use vault
- Security testing: SAST and DAST in CI/CD

**OWASP Top 10 Coverage:**
- A01: Broken Access Control - Addressed by SEC-002
- A02: Cryptographic Failures - Addressed by SEC-003
- A03: Injection - Addressed by input validation
- [Continue for all top 10]

**Verification:**
- SAST tools (SonarQube, Checkmarx)
- DAST tools (OWASP ZAP, Burp Suite)
- Dependency scanning (Snyk, Dependabot)
- Manual penetration testing (annual)
```

---

## 3. Reliability Requirements

### Availability

```
**Requirement ID:** REL-001

**Description:** System uptime requirements

**Metrics:**
- Uptime: 99.9% (8.7 hours downtime/year maximum)
- Planned maintenance: <4 hours/month, announced 7 days ahead
- Maintenance window: Saturday 2-6am EST
- Critical services: 99.95% (4.4 hours downtime/year)

**Downtime Categories:**
- Planned: Scheduled maintenance (not counted toward SLA)
- Unplanned: System failures (counted toward SLA)
- Emergency: Security patches (not counted if <2 hours)

**Measurement:**
- Calculated monthly
- Measured from external monitoring (Pingdom, UptimeRobot)
- Excludes client-side issues and network problems

**Penalties/Remediation:**
- 99.0-99.9%: Service credit 10%
- 95.0-99.0%: Service credit 25%
- <95.0%: Service credit 50%

**Verification:**
- Uptime monitoring reports
- Incident postmortems
```

---

### Data Integrity

```
**Requirement ID:** REL-002

**Description:** Data integrity and backup requirements

**Requirements:**
- Zero data loss: No user data lost under normal operations
- Automated backups: Every 6 hours
- Backup retention: 30 days daily, 12 months monthly
- Backup testing: Monthly restore drills
- Point-in-time recovery: Any point in last 30 days within 15 minutes
- Backup geo-replication: Secondary region for disaster recovery
- Database transactions: ACID compliant
- Checksums: All backups validated

**Verification:**
- Backup success logs
- Monthly restore tests
- Annual disaster recovery drill
```

---

### Fault Tolerance

```
**Requirement ID:** REL-003

**Description:** Resilience to failures

**Requirements:**
- No single point of failure: All components redundant
- Automatic failover: <5 seconds to backup systems
- Graceful degradation: Continue with reduced functionality vs hard failure
- Circuit breakers: Prevent cascade failures
- Retry logic: 3 retries with exponential backoff
- Health checks: Every 30 seconds, remove unhealthy instances
- Database replication: Multi-AZ with read replicas

**Failure Scenarios:**
| Scenario | Expected Behavior | RTO | RPO |
|----------|-------------------|-----|-----|
| Single server failure | Auto-failover | 30s | 0 |
| Database failure | Failover to standby | 2min | 5min |
| Data center outage | Switch to DR site | 15min | 15min |
| Complete region loss | Activate DR region | 1hr | 1hr |

**Verification:**
- Chaos engineering tests (Chaos Monkey)
- Disaster recovery drills
- Failover testing
```

---

### Error Handling

```
**Requirement ID:** REL-004

**Description:** Error handling requirements

**Requirements:**
- All errors logged with context (stack trace, user, time)
- User-friendly error messages (no technical details)
- Error recovery options presented to user
- Transient failures retried automatically (network, external services)
- Permanent failures reported clearly
- Error rate monitoring: Alert if >1% of requests fail
- Error budgets: 0.1% error rate acceptable

**Error Categories:**
| Type | Example | User Message | System Action |
|------|---------|--------------|---------------|
| Client Error (4xx) | Invalid input | "Email format invalid" | Return to form |
| Server Error (5xx) | Database down | "Something went wrong. We've been notified." | Log, alert, retry |
| Timeout | Slow external API | "This is taking longer than expected. Please wait..." | Retry, then fail gracefully |

**Verification:**
- Error logging review
- Error rate monitoring (last 30 days)
```

---

## 4. Scalability Requirements

### Horizontal Scaling

```
**Requirement ID:** SCALE-001

**Description:** Ability to scale by adding more servers

**Requirements:**
- Stateless application servers: Can add/remove without data loss
- Load balancing: Even distribution across instances
- Auto-scaling: Automatically add servers when CPU >70% for 5 minutes
- Auto-scaling down: Remove servers when CPU <30% for 15 minutes
- Maximum scale: 50 application servers
- Database read replicas: Scale to 10 read replicas

**Growth Targets:**
| Metric | Current | Year 1 | Year 2 | Year 3 |
|--------|---------|--------|--------|--------|
| Users | 10K | 50K | 200K | 500K |
| RPS | 100 | 500 | 2K | 5K |
| Data | 100GB | 500GB | 2TB | 10TB |

**Verification:**
- Load test at 2x current capacity
- Review auto-scaling logs
```

---

### Database Scalability

```
**Requirement ID:** SCALE-002

**Description:** Database scaling approach

**Requirements:**
- Vertical scaling: Scale to 64 CPU, 256GB RAM
- Horizontal scaling: Sharding by user_id when >10M users
- Read replicas: Add up to 10 replicas for read-heavy operations
- Caching layer: Redis for frequently accessed data
- Connection pooling: Max 1000 connections, reuse connections
- Query optimization: All queries <100ms (p95)

**Verification:**
- Database load testing
- Query performance analysis
```

---

## 5. Usability Requirements

### Learnability

```
**Requirement ID:** USE-001

**Description:** How easily new users can learn the system

**Requirements:**
- First-time user can complete primary task within 5 minutes
- Onboarding flow completion rate >80%
- In-app help and tooltips for all non-obvious features
- Contextual help: Right-click help option
- Video tutorials for advanced features
- User documentation: Up-to-date, searchable

**Verification:**
- New user testing sessions (5 participants)
- Onboarding analytics
- Time-to-first-value metric
```

---

### Efficiency

```
**Requirement ID:** USE-002

**Description:** Speed of task completion for experienced users

**Requirements:**
- Primary workflows require ≤3 clicks
- Keyboard shortcuts for all common actions
- Bulk operations available (select multiple, act on all)
- Recently used items easily accessible
- Search accessible from any page (Cmd/Ctrl+K)
- Form auto-fill with saved data

**Task Completion Times:**
| Task | Target Time (Experienced User) |
|------|-------------------------------|
| Create new item | <30 seconds |
| Search and find item | <15 seconds |
| Edit existing item | <45 seconds |
| Generate report | <60 seconds |

**Verification:**
- Task completion time studies
- User satisfaction surveys
```

---

### Error Prevention

```
**Requirement ID:** USE-003

**Description:** Prevent user errors before they happen

**Requirements:**
- Confirmation dialogs for destructive actions (delete, overwrite)
- Undo capability for all state-changing actions
- Auto-save drafts every 30 seconds
- Validation before submission (inline, real-time)
- Disabled buttons when action not allowed (with tooltip explanation)
- Clear constraints shown upfront ("Max file size: 10MB")

**Verification:**
- User error rate <5% of actions
- Undo feature usage tracking
```

---

## 6. Accessibility Requirements

### WCAG 2.1 Compliance

```
**Requirement ID:** ACCESS-001

**Description:** Web Content Accessibility Guidelines compliance

**Requirements:**
- WCAG 2.1 Level AA compliance minimum
- Level AAA for critical user flows (registration, checkout)

**Specific Requirements:**

**Perceivable:**
- All images have alt text
- Color contrast ratio ≥4.5:1 for normal text, ≥3:1 for large text
- Text resizable up to 200% without loss of content
- No content relies solely on color to convey meaning
- Captions for all video content
- Transcripts for audio content

**Operable:**
- All functionality accessible via keyboard
- No keyboard traps
- Skip links to main content
- Focus indicators visible (≥2px border)
- No time limits, or adjustable time limits
- No content flashes more than 3 times per second

**Understandable:**
- Page language declared in HTML
- Form labels associated with inputs
- Error messages clear and specific
- Consistent navigation across pages

**Robust:**
- Valid HTML5
- ARIA landmarks used appropriately
- Compatible with assistive technologies (JAWS, NVDA, VoiceOver)

**Verification:**
- Automated accessibility testing (axe, WAVE)
- Manual testing with screen readers
- Keyboard navigation testing
- Color contrast checks
- Annual accessibility audit
```

---

## 7. Compatibility Requirements

### Browser Support

```
**Requirement ID:** COMPAT-001

**Description:** Supported browsers and versions

**Requirements:**

**Tier 1 Support (Full features, actively tested):**
- Chrome: Last 2 versions
- Firefox: Last 2 versions
- Safari: Last 2 versions
- Edge: Last 2 versions

**Tier 2 Support (Core features, tested periodically):**
- Chrome: Last 5 versions
- Firefox: Last 5 versions
- Safari: Last 5 versions

**Not Supported:**
- Internet Explorer (any version)
- Browsers older than 3 years

**Mobile Browsers:**
- iOS Safari: iOS 14+
- Chrome Mobile: Android 10+

**Verification:**
- BrowserStack cross-browser testing
- Analytics on browser usage
- Automated E2E tests on supported browsers
```

---

### Device Support

```
**Requirement ID:** COMPAT-002

**Description:** Supported devices and screen sizes

**Requirements:**

**Desktop:**
- Minimum resolution: 1280×720
- Optimal resolution: 1920×1080
- Responsive up to: 4K (3840×2160)

**Tablet:**
- iPad (9.7" and larger)
- Android tablets (10" and larger)
- Portrait and landscape orientations

**Mobile:**
- iPhone 6 and newer (4.7" and larger)
- Android phones (5" and larger)
- Portrait orientation primary, landscape supported

**Responsive Breakpoints:**
- Mobile: <768px
- Tablet: 768px-1024px
- Desktop: >1024px

**Verification:**
- Responsive design testing
- Device lab testing
- Real device testing for critical flows
```

---

## 8. Maintainability Requirements

### Code Quality

```
**Requirement ID:** MAINT-001

**Description:** Code maintainability standards

**Requirements:**
- Code coverage: >80% for critical paths, >60% overall
- Code complexity: Cyclomatic complexity <10 per method
- Code duplication: <5%
- Documentation: All public APIs documented
- Code style: Enforced via linter (ESLint, Prettier)
- Technical debt: Max 1 day/sprint, tracked in backlog

**Verification:**
- SonarQube quality gates
- Code review process
- Static analysis in CI/CD
```

---

### Monitoring & Observability

```
**Requirement ID:** MAINT-002

**Description:** System monitoring requirements

**Requirements:**
- Logging: Structured logs (JSON) with trace IDs
- Log levels: ERROR, WARN, INFO, DEBUG
- Log retention: 30 days in hot storage, 1 year in cold storage
- Metrics: Application, infrastructure, business metrics
- Tracing: Distributed tracing with OpenTelemetry
- Alerting: PagerDuty for critical alerts, email for warnings
- Dashboards: Real-time dashboards for key metrics

**Key Metrics to Track:**
- Response times (p50, p95, p99)
- Error rates
- Request rates
- Active users
- Database query performance
- Cache hit rates
- Queue depths

**Verification:**
- Review monitoring dashboards
- Test alert configurations
```

---

## 9. Compliance Requirements

### Data Privacy

```
**Requirement ID:** COMP-001

**Description:** Data privacy compliance

**Requirements:**

**GDPR (EU customers):**
- Right to access: Provide all user data within 30 days
- Right to deletion: Delete all user data within 30 days
- Right to portability: Export data in machine-readable format (JSON)
- Consent management: Explicit opt-in for marketing
- Data processing agreements: With all third-party processors
- Privacy policy: Clear, accessible, up-to-date

**CCPA (California customers):**
- Right to know what data is collected
- Right to delete personal data
- Right to opt-out of data sales (we don't sell data)
- Non-discrimination for exercising rights

**HIPAA (if handling health data):**
- Encryption at rest and in transit
- Access controls and audit logs
- Business associate agreements (BAAs)
- Breach notification procedures

**Verification:**
- Privacy audit
- Legal review
- Data flow mapping
- Compliance training for team
```

---

## 10. Deployment & Operations Requirements

### Deployment

```
**Requirement ID:** OPS-001

**Description:** Deployment process requirements

**Requirements:**
- Zero-downtime deployments: Blue-green or rolling deployments
- Rollback capability: Can rollback within 5 minutes
- Database migrations: Backward compatible, run before code deployment
- Feature flags: All new features behind feature flags
- Deployment frequency: Multiple deploys per day supported
- Deployment window: Any time (24/7 deployments)
- Automated tests: 100% pass before deployment to production

**Verification:**
- Deployment success rate >99%
- Mean time to rollback <5 minutes
- Zero production incidents from deployments (last 3 months)
```

---

## NFR Checklist

When documenting NFRs, ensure:

- [ ] **Specific and Measurable** - No vague terms like "fast" or "secure"
- [ ] **Testable** - Can verify if requirement is met
- [ ] **Realistic** - Achievable with available resources
- [ ] **Prioritized** - Critical, High, Medium, Low
- [ ] **Includes Metrics** - Numbers, percentages, time periods
- [ ] **Context Provided** - Under what conditions measured
- [ ] **Verification Method** - How to test/validate
- [ ] **Rationale** - Why this requirement exists
- [ ] **Trade-offs Acknowledged** - What you're optimizing for

---

## Common NFR Mistakes

### ❌ Too Vague

**Bad:** "System should be fast"

**Good:** "Dashboard loads in <2 seconds (p95) for 10,000 concurrent users"

---

### ❌ Not Measurable

**Bad:** "System should be highly available"

**Good:** "System maintains 99.9% uptime (max 8.7 hours downtime/year)"

---

### ❌ Missing Context

**Bad:** "API response time <100ms"

**Good:** "API GET requests return in <100ms (p95) measured from application server, excluding network latency, with database containing 1M records"

---

### ❌ No Verification Method

**Bad:** "System must be secure"

**Good:** "System passes OWASP Top 10 security scan with zero high/critical findings, verified monthly via automated scanning"

---

## Related Templates

- `assets/prd-structure-template.md` - Document NFRs in PRD "Technical Considerations" section
- `assets/edge-case-checklist.md` - NFRs inform edge case handling (timeouts, errors, etc.)
- `references/specification-anti-patterns.md` - Common mistakes to avoid
