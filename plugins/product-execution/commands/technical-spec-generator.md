# Technical Specification Generator

Generate detailed technical specifications for features and systems with architecture, APIs, data models, and implementation plans.

## Usage

```
/pm:technical-spec [feature or system name] [optional: spec type, complexity]
```

## What This Command Does

1. Creates comprehensive technical specifications from PRD requirements
2. Defines system architecture, APIs, and data models
3. Documents security, performance, and scalability requirements
4. Specifies integration points and dependencies
5. Provides implementation plan with milestones
6. Takes 1-2 hours vs 4-6 hours of manual spec writing

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**From PRD/Requirements**:
- Feature name and description
- User stories and acceptance criteria
- Success metrics and KPIs
- Target users and use cases
- Constraints and dependencies

**Technical Context**:
- Current system architecture
- Existing APIs and services
- Technology stack preferences
- Performance requirements
- Security requirements
- Scale requirements (users, data volume, requests)

**Resources**:
- Team size and skills
- Timeline expectations
- Budget constraints
- Third-party services available

### 2. Identify Spec Type

**Feature Spec** - New feature or capability
- When: Building new user-facing functionality
- Depth: Medium - focuses on user flows and API design
- Timeline: 2-4 weeks implementation

**API Spec** - New API or endpoints
- When: Building integrations or platform capabilities
- Depth: High - detailed endpoint specs, contracts
- Timeline: 1-3 weeks implementation

**System Design Spec** - Architecture or infrastructure
- When: Building foundational systems or scaling existing ones
- Depth: Very high - architecture diagrams, scalability analysis
- Timeline: 4-12 weeks implementation

**Integration Spec** - Third-party integration
- When: Connecting to external services
- Depth: Medium - focuses on integration patterns and error handling
- Timeline: 1-3 weeks implementation

**Data Migration Spec** - Data model changes
- When: Changing database schema or migrating data
- Depth: High - detailed migration plan and rollback strategy
- Timeline: 2-6 weeks implementation

### 3. Structure the Specification

**Every spec includes**:
1. **Overview** - What, why, success criteria
2. **Technical Approach** - How we'll build it
3. **Architecture** - System design and components
4. **Detailed Design** - APIs, data models, algorithms
5. **Security & Privacy** - Authentication, authorization, data protection
6. **Performance & Scale** - Load handling, optimization
7. **Testing** - Unit, integration, end-to-end testing strategy
8. **Implementation Plan** - Phases, milestones, timeline
9. **Risks & Mitigations** - Technical risks and how we'll handle them
10. **Appendix** - References, alternatives considered

### 4. Follow Ground Rules

**Explicit Data Sourcing**:
- Source all requirements from PRD or user input
- Document assumptions explicitly
- Reference existing system documentation

**Upfront Data Gathering**:
- Ask for all required information before generating spec
- Don't assume technical constraints
- Get clarity on performance/scale requirements

**No Infrastructure Assumptions**:
- Ask about deployment environment
- Ask about database preferences
- Ask about third-party service availability

## Templates

### Feature Specification

```markdown
# Technical Specification: [Feature Name]

**Author**: [Engineering Lead]
**Date**: [Date]
**Status**: Draft | Review | Approved | Implemented
**Related PRD**: [Link to PRD]

---

## 1. Overview

### 1.1 Summary

**What**: [2-3 sentences describing the feature]

**Why**: [Business/user value - from PRD]

**Success Criteria**:
- [Criterion 1 - from PRD]
- [Criterion 2 - from PRD]
- [Criterion 3 - from PRD]

**Target Users**: [User segment - from PRD]

### 1.2 Scope

**In Scope**:
- [Feature component 1]
- [Feature component 2]
- [Feature component 3]

**Out of Scope** (for this version):
- [Future enhancement 1]
- [Future enhancement 2]

**Dependencies**:
- [External dependency 1]
- [External dependency 2]

---

## 2. Technical Approach

### 2.1 High-Level Architecture

```
[Architecture diagram or text description]

User → Frontend → API Gateway → Feature Service → Database
                              → Cache
                              → External API
```

**Components**:
1. **Frontend** - [Technology, responsibility]
2. **Backend API** - [Technology, responsibility]
3. **Data Storage** - [Database type, schema]
4. **Cache Layer** - [If needed, technology]
5. **External Integrations** - [If any, which services]

### 2.2 Technology Stack

**Frontend**:
- Framework: [React / Vue / Angular / etc.]
- State Management: [Redux / Context / etc.]
- UI Library: [Component library]

**Backend**:
- Language: [Python / Node.js / Java / etc.]
- Framework: [Express / FastAPI / Spring / etc.]
- Runtime: [Node 20 / Python 3.11 / etc.]

**Data**:
- Primary DB: [PostgreSQL / MongoDB / etc.]
- Cache: [Redis / Memcached / none]
- Search: [Elasticsearch / Algolia / none]

**Infrastructure**:
- Hosting: [AWS / GCP / Azure / self-hosted]
- Container: [Docker / Kubernetes / none]
- CI/CD: [GitHub Actions / Jenkins / etc.]

### 2.3 Design Decisions

**Decision 1**: [Choice made]
- **Options Considered**: [A, B, C]
- **Chosen**: [Option A]
- **Rationale**: [Why chosen]
- **Trade-offs**: [What we're accepting]

**Decision 2**: [Choice made]
- [Same structure]

---

## 3. Detailed Design

### 3.1 User Flows

**Flow 1: [Primary User Flow]**
1. User [action]
2. System [response]
3. User [action]
4. System [response]
5. Outcome: [End state]

**Edge Cases**:
- If [condition]: [Handling]
- If [condition]: [Handling]

### 3.2 API Design

#### Endpoint: Create [Resource]

```
POST /api/v1/[resource]

Request:
{
  "field1": "string (required, max 255 chars)",
  "field2": "integer (optional, default: 0)",
  "field3": {
    "nested": "string"
  }
}

Response (200 OK):
{
  "id": "uuid",
  "field1": "string",
  "field2": "integer",
  "field3": { "nested": "string" },
  "created_at": "ISO 8601 timestamp",
  "updated_at": "ISO 8601 timestamp"
}

Response (400 Bad Request):
{
  "error": "validation_error",
  "message": "field1 is required",
  "details": [
    { "field": "field1", "issue": "required" }
  ]
}

Response (401 Unauthorized):
{
  "error": "unauthorized",
  "message": "Authentication required"
}
```

**Validation Rules**:
- `field1`: Required, 1-255 characters, alphanumeric
- `field2`: Optional, 0-999999, positive integer

**Rate Limiting**: 100 requests per minute per user

**Authentication**: Bearer token required

#### Endpoint: Get [Resource]

```
GET /api/v1/[resource]/{id}

Response (200 OK):
[Same as POST response]

Response (404 Not Found):
{
  "error": "not_found",
  "message": "Resource not found"
}
```

**[Additional endpoints...]**

### 3.3 Data Models

#### [Resource] Model

**Table/Collection**: `resources`

```sql
CREATE TABLE resources (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID NOT NULL REFERENCES users(id) ON DELETE CASCADE,
  field1 VARCHAR(255) NOT NULL,
  field2 INTEGER DEFAULT 0,
  field3 JSONB,
  status VARCHAR(50) DEFAULT 'active',
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),
  deleted_at TIMESTAMP NULL,

  INDEX idx_user_id (user_id),
  INDEX idx_status (status),
  INDEX idx_created_at (created_at)
);
```

**Indexes**:
- `idx_user_id`: Speed up user-based queries
- `idx_status`: Speed up status filtering
- `idx_created_at`: Support time-based queries

**Constraints**:
- Foreign key to users table (cascade delete)
- Status must be in ['active', 'archived', 'deleted']

**Soft Delete**: Uses `deleted_at` timestamp

### 3.4 Business Logic

**[Key Algorithm or Process]**

```
Function: calculate[Something](input)
  1. Validate input parameters
  2. Fetch related data from DB
  3. Apply business rules:
     - Rule 1: If [condition], then [action]
     - Rule 2: If [condition], then [action]
  4. Calculate result
  5. Update state if needed
  6. Return result

Edge cases:
  - If input is null: Return error
  - If user not found: Return 404
  - If quota exceeded: Return 429
```

### 3.5 State Management

**Feature States**:
- `pending`: Initial state after creation
- `processing`: System is working on it
- `completed`: Successfully finished
- `failed`: Error occurred
- `archived`: User archived it

**State Transitions**:
```
pending → processing → completed
        → processing → failed
completed → archived
failed → pending (retry)
```

---

## 4. Security & Privacy

### 4.1 Authentication

**Method**: [OAuth 2.0 / JWT / API Key / etc.]

**Implementation**:
- All endpoints require authentication (except health check)
- Bearer token in Authorization header
- Token expiry: 1 hour (refresh available)
- Invalid token → 401 response

### 4.2 Authorization

**Permission Model**: [RBAC / ABAC / etc.]

**Roles**:
- `admin`: Full access
- `user`: Can CRUD own resources
- `viewer`: Read-only access

**Resource Ownership**:
- Users can only access their own resources
- Admins can access all resources
- Checked at API layer before DB query

### 4.3 Data Protection

**PII Handling**:
- Fields containing PII: [field1, field2]
- Encryption: [At rest / In transit / Both]
- Retention: [30 days / 1 year / etc.]

**Sensitive Data**:
- [field3] is encrypted using AES-256
- Encryption keys stored in [AWS KMS / Vault / etc.]
- Never logged or cached

**GDPR Compliance**:
- User data export: [Endpoint/process]
- User data deletion: [Endpoint/process]
- Data minimization: Only collect [specific fields]

### 4.4 Input Validation

**All User Input**:
- Sanitize HTML/script tags
- Validate against schema
- Max lengths enforced
- SQL injection prevention (parameterized queries)
- XSS prevention (output encoding)

---

## 5. Performance & Scale

### 5.1 Performance Requirements

**Latency**:
- p50: < 200ms
- p95: < 500ms
- p99: < 1000ms

**Throughput**:
- Target: 1000 requests/second
- Peak: 2000 requests/second

**Availability**:
- Target: 99.9% uptime (43 minutes downtime/month)

### 5.2 Scalability

**Current Scale**:
- Users: [10K / 100K / 1M]
- Data: [1GB / 100GB / 1TB]
- Requests: [100/sec / 1K/sec / 10K/sec]

**Target Scale** (12 months):
- Users: [Growth expectation]
- Data: [Growth expectation]
- Requests: [Growth expectation]

**Scaling Strategy**:
- **Horizontal scaling**: Add API servers behind load balancer
- **Database**: Read replicas for queries, primary for writes
- **Caching**: Redis for frequently accessed data (1 hour TTL)
- **CDN**: Static assets served via CDN

### 5.3 Optimization

**Database**:
- Indexes on high-query columns
- Query optimization for N+1 problems
- Connection pooling (50 connections)

**Caching**:
- Cache user sessions (1 hour)
- Cache [resource] reads (15 minutes)
- Cache invalidation on writes

**API**:
- Pagination for list endpoints (default: 20, max: 100)
- Field filtering to reduce payload size
- Compression (gzip) enabled

---

## 6. Testing Strategy

### 6.1 Unit Tests

**Coverage Target**: 80%

**Critical Paths**:
- Business logic functions
- Data validation
- State transitions
- Error handling

**Mocking**: External APIs, database calls

### 6.2 Integration Tests

**Test Scenarios**:
- API endpoint flows (happy path)
- Error responses (4xx, 5xx)
- Authentication/authorization
- Database transactions

**Test Data**: Fixtures or factory functions

### 6.3 End-to-End Tests

**User Journeys**:
1. User creates [resource] → verifies it exists
2. User updates [resource] → verifies changes
3. User deletes [resource] → verifies deletion

**Tools**: [Cypress / Selenium / Playwright]

### 6.4 Load Testing

**Scenarios**:
- Baseline: 500 req/sec for 10 minutes
- Peak: 2000 req/sec for 2 minutes
- Soak: 1000 req/sec for 1 hour

**Success Criteria**:
- No errors under baseline load
- < 1% errors under peak load
- No memory leaks in soak test

---

## 7. Implementation Plan

### 7.1 Phases

**Phase 1: Foundation** (Week 1-2)
- [ ] Database schema and migrations
- [ ] Basic API scaffolding
- [ ] Authentication/authorization
- [ ] Unit test framework

**Phase 2: Core Features** (Week 3-4)
- [ ] CRUD endpoints
- [ ] Business logic implementation
- [ ] Error handling
- [ ] Integration tests

**Phase 3: Polish** (Week 5)
- [ ] Performance optimization
- [ ] Security hardening
- [ ] Documentation
- [ ] E2E tests

**Phase 4: Launch Prep** (Week 6)
- [ ] Load testing
- [ ] Security audit
- [ ] Monitoring/alerting
- [ ] Production deployment

### 7.2 Milestones

| Milestone | Date | Deliverable | Owner |
|-----------|------|-------------|-------|
| DB Schema Ready | Week 1 | Migrations tested in staging | [Backend Lead] |
| API Alpha | Week 2 | Basic CRUD working | [Backend Team] |
| Feature Complete | Week 4 | All endpoints implemented | [Backend Team] |
| QA Sign-off | Week 5 | All tests passing | [QA Lead] |
| Production Launch | Week 6 | Deployed to production | [DevOps] |

### 7.3 Team & Resources

**Engineering**:
- Backend: 2 engineers × 6 weeks
- Frontend: 1 engineer × 4 weeks (parallel)
- QA: 1 engineer × 2 weeks

**Dependencies**:
- Design mockups (Week 0)
- PRD finalized (Week 0)
- Infrastructure provisioned (Week 1)

---

## 8. Monitoring & Observability

### 8.1 Metrics

**Application Metrics**:
- Request rate (req/sec)
- Error rate (4xx, 5xx)
- Latency (p50, p95, p99)
- Active users
- Resources created/updated/deleted

**Infrastructure Metrics**:
- CPU utilization
- Memory usage
- Database connections
- Cache hit rate

### 8.2 Logging

**Log Levels**:
- ERROR: System failures, exceptions
- WARN: Degraded performance, retries
- INFO: Key events (user actions, state changes)
- DEBUG: Detailed execution flow (dev only)

**Structured Logging**:
```json
{
  "timestamp": "2025-10-17T10:30:00Z",
  "level": "INFO",
  "service": "feature-api",
  "event": "resource_created",
  "user_id": "uuid",
  "resource_id": "uuid",
  "duration_ms": 145
}
```

### 8.3 Alerts

**Critical Alerts** (page on-call):
- Error rate > 5%
- p99 latency > 2000ms
- Service down

**Warning Alerts** (Slack):
- Error rate > 2%
- p99 latency > 1000ms
- Database connection pool > 80% full

---

## 9. Risks & Mitigations

### 9.1 Technical Risks

**Risk 1: Database performance degrades at scale**
- **Likelihood**: Medium
- **Impact**: High (user-facing latency)
- **Mitigation**: Read replicas, caching strategy, query optimization
- **Contingency**: Add database sharding if needed

**Risk 2: Third-party API dependency fails**
- **Likelihood**: Low
- **Impact**: High (feature broken)
- **Mitigation**: Circuit breaker pattern, graceful degradation, retry logic
- **Contingency**: Fallback to manual process, queue for retry

**Risk 3: Security vulnerability discovered**
- **Likelihood**: Low
- **Impact**: Critical (data breach)
- **Mitigation**: Security audit before launch, penetration testing, dependency scanning
- **Contingency**: Incident response plan, rollback procedure

### 9.2 Timeline Risks

**Risk**: Engineering bandwidth reduced
- **Mitigation**: Buffer in timeline, prioritize MVP scope
- **Contingency**: Defer nice-to-haves to v1.1

---

## 10. Rollout & Deployment

### 10.1 Deployment Strategy

**Approach**: [Blue-green / Canary / Rolling / Feature flag]

**Steps**:
1. Deploy to staging environment
2. Run full test suite
3. Deploy to 5% of production traffic (canary)
4. Monitor metrics for 24 hours
5. If healthy, deploy to 50% of traffic
6. If healthy, deploy to 100%

**Rollback Plan**:
- If error rate > 5%, immediate rollback
- Rollback via [deployment tool]
- Estimated rollback time: < 5 minutes

### 10.2 Feature Flags

**Flag**: `enable_[feature_name]`
- **Default**: `false` (disabled)
- **Rollout**: Gradual (5% → 25% → 50% → 100%)
- **Kill Switch**: Can disable instantly if issues

### 10.3 Data Migration

**Migration Plan**:
1. Add new schema columns (backwards compatible)
2. Backfill existing data (background job)
3. Update application to use new columns
4. Verify data integrity
5. Drop old columns (after 30 days)

**Rollback**: Keep old columns for 30 days to allow rollback

---

## 11. Documentation

### 11.1 API Documentation

**Format**: OpenAPI 3.0 spec
**Published**: [URL to docs]
**Includes**:
- All endpoints with examples
- Authentication guide
- Error codes reference
- Rate limiting info

### 11.2 Internal Documentation

**Architecture Decision Records (ADRs)**:
- [ADR-001]: [Decision made]
- [ADR-002]: [Decision made]

**Runbooks**:
- Deployment procedure
- Incident response
- Common troubleshooting

**Developer Setup**:
- Local development guide
- Testing guide
- Contribution guidelines

---

## 12. Appendix

### 12.1 Alternatives Considered

**Alternative 1**: [Different approach]
- **Pros**: [Benefits]
- **Cons**: [Drawbacks]
- **Why not chosen**: [Reason]

**Alternative 2**: [Different approach]
- [Same structure]

### 12.2 References

- PRD: [Link]
- Design mockups: [Link]
- Related specs: [Links]
- External docs: [Links to third-party APIs, libraries]

### 12.3 Glossary

- **[Term]**: [Definition]
- **[Acronym]**: [What it stands for and means]

### 12.4 Open Questions

- [ ] [Question 1] - Owner: [Name] - Due: [Date]
- [ ] [Question 2] - Owner: [Name] - Due: [Date]

---

## Approval

**Technical Review**:
- [ ] Engineering Lead - [Name]
- [ ] Architect - [Name]
- [ ] Security - [Name]

**Product Review**:
- [ ] Product Manager - [Name]

**Approval Date**: [Date when approved]

**Next Review**: [Date for spec review/update]
```

---

### API Specification Template

```markdown
# API Specification: [API Name]

**Version**: v1
**Author**: [Engineering Lead]
**Date**: [Date]
**Status**: Draft | Review | Approved | Implemented

---

## 1. Overview

### 1.1 Purpose

**What**: [API description]

**Use Cases**:
- [Use case 1]
- [Use case 2]
- [Use case 3]

**Target Consumers**:
- Internal services: [Which services]
- Third-party integrations: [Which partners]
- Public developers: [If public API]

### 1.2 Design Principles

- **RESTful**: Standard HTTP methods and status codes
- **Consistent**: Predictable naming and structure
- **Versioned**: Support v1, v2 without breaking changes
- **Documented**: OpenAPI spec for all endpoints
- **Secure**: Authentication and rate limiting

---

## 2. Authentication

### 2.1 API Keys

**Obtaining Keys**:
1. User creates account
2. Generates API key in dashboard
3. Includes key in requests

**Usage**:
```
Authorization: Bearer sk_live_abc123...
```

**Key Types**:
- `sk_live_`: Production keys
- `sk_test_`: Test environment keys

**Rotation**: Recommended every 90 days

### 2.2 OAuth 2.0 (if applicable)

**Supported Flows**:
- Authorization Code (for web apps)
- Client Credentials (for server-to-server)

**Scopes**:
- `read:resources`: Read access
- `write:resources`: Write access
- `admin`: Full access

---

## 3. Endpoints

### 3.1 Base URL

**Production**: `https://api.example.com/v1`
**Staging**: `https://api-staging.example.com/v1`

### 3.2 Common Headers

**Request**:
```
Authorization: Bearer {token}
Content-Type: application/json
Accept: application/json
```

**Response**:
```
Content-Type: application/json
X-Request-ID: {uuid}
X-RateLimit-Remaining: {count}
X-RateLimit-Reset: {timestamp}
```

### 3.3 Endpoint Catalog

#### List Resources

```
GET /resources
```

**Query Parameters**:
- `page` (integer, default: 1): Page number
- `limit` (integer, default: 20, max: 100): Items per page
- `sort` (string, default: "created_at"): Sort field
- `order` (string, default: "desc"): Sort order (asc/desc)
- `filter[status]` (string): Filter by status
- `filter[created_after]` (ISO 8601): Filter by date

**Response (200 OK)**:
```json
{
  "data": [
    {
      "id": "res_123",
      "type": "resource",
      "attributes": {
        "name": "Example",
        "status": "active",
        "created_at": "2025-10-17T10:00:00Z"
      }
    }
  ],
  "meta": {
    "page": 1,
    "limit": 20,
    "total": 150,
    "pages": 8
  },
  "links": {
    "self": "/resources?page=1",
    "next": "/resources?page=2",
    "last": "/resources?page=8"
  }
}
```

#### Create Resource

[Full endpoint spec as in feature template]

#### Update Resource

[Full endpoint spec]

#### Delete Resource

[Full endpoint spec]

---

## 4. Error Handling

### 4.1 Error Response Format

```json
{
  "error": {
    "code": "validation_error",
    "message": "Request validation failed",
    "details": [
      {
        "field": "email",
        "issue": "invalid_format",
        "message": "Must be a valid email address"
      }
    ],
    "request_id": "req_abc123"
  }
}
```

### 4.2 HTTP Status Codes

**2xx Success**:
- `200 OK`: Success
- `201 Created`: Resource created
- `204 No Content`: Success, no response body

**4xx Client Errors**:
- `400 Bad Request`: Invalid request
- `401 Unauthorized`: Authentication required
- `403 Forbidden`: Insufficient permissions
- `404 Not Found`: Resource not found
- `422 Unprocessable Entity`: Validation error
- `429 Too Many Requests`: Rate limit exceeded

**5xx Server Errors**:
- `500 Internal Server Error`: Server error
- `503 Service Unavailable`: Temporary outage

### 4.3 Error Codes

- `validation_error`: Request failed validation
- `authentication_error`: Invalid or missing credentials
- `authorization_error`: Insufficient permissions
- `not_found`: Resource does not exist
- `rate_limit_exceeded`: Too many requests
- `server_error`: Internal server error

---

## 5. Rate Limiting

**Limits**:
- **Authenticated**: 1000 requests per hour
- **Public**: 100 requests per hour

**Headers**:
```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 950
X-RateLimit-Reset: 1634567890
```

**Exceeded Limit**:
```json
{
  "error": {
    "code": "rate_limit_exceeded",
    "message": "Rate limit exceeded. Try again in 45 minutes.",
    "retry_after": 2700
  }
}
```

---

## 6. Pagination

**Strategy**: Cursor-based pagination

**Parameters**:
- `limit`: Items per page (default: 20, max: 100)
- `cursor`: Pagination cursor from previous response

**Response**:
```json
{
  "data": [...],
  "pagination": {
    "has_more": true,
    "next_cursor": "eyJpZCI6MTIzfQ=="
  }
}
```

---

## 7. Webhooks (if applicable)

**Events**:
- `resource.created`
- `resource.updated`
- `resource.deleted`

**Payload**:
```json
{
  "id": "evt_123",
  "type": "resource.created",
  "created_at": "2025-10-17T10:00:00Z",
  "data": {
    "id": "res_123",
    "attributes": {...}
  }
}
```

**Verification**: HMAC signature in `X-Webhook-Signature` header

---

## 8. Versioning

**Strategy**: URL versioning (`/v1/`, `/v2/`)

**Breaking Changes**:
- Removing endpoints
- Changing response format
- Changing required fields

**Non-Breaking Changes**:
- Adding endpoints
- Adding optional fields
- Adding response fields

**Deprecation**:
- 6-month notice before sunset
- `Sunset` header in responses
- Migration guide provided

---

## 9. Testing

### 9.1 Test Environment

**Base URL**: `https://api-test.example.com/v1`

**Test API Keys**: `sk_test_...`

**Test Data**: Sandbox with realistic test data

### 9.2 Example Requests

```bash
# Create resource
curl -X POST https://api.example.com/v1/resources \
  -H "Authorization: Bearer sk_live_abc123" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Test Resource",
    "description": "Created via API"
  }'

# List resources
curl -X GET "https://api.example.com/v1/resources?limit=10" \
  -H "Authorization: Bearer sk_live_abc123"
```

---

## 10. OpenAPI Specification

**Link**: [URL to OpenAPI spec file]

**Tools**:
- Postman collection: [Link]
- Interactive docs: [Link to Swagger UI]
- SDK generators: [Links]

---

## Appendix

[Same as feature spec - alternatives, references, glossary, approvals]
```

---

## System Design Specification Template

```markdown
# System Design: [System Name]

**Architect**: [Name]
**Date**: [Date]
**Status**: Draft | Review | Approved | Implemented

---

## 1. System Overview

**Purpose**: [What problem this system solves]

**Scope**:
- [Component 1]
- [Component 2]
- [Component 3]

**Non-Functional Requirements**:
- **Availability**: 99.95% uptime
- **Latency**: p99 < 100ms
- **Throughput**: 10,000 requests/second
- **Data Retention**: 90 days
- **Disaster Recovery**: RPO < 1 hour, RTO < 4 hours

---

## 2. Architecture Diagram

```
                    ┌─────────────┐
                    │   CDN       │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │ Load Balancer│
                    └──────┬──────┘
                           │
          ┌────────────────┴────────────────┐
          │                                 │
    ┌─────▼─────┐                   ┌──────▼──────┐
    │ Web Servers│                   │ API Servers  │
    │ (Nginx)    │                   │ (Node.js)    │
    └─────┬─────┘                   └──────┬───────┘
          │                                 │
          │                    ┌────────────┴─────────┐
          │                    │                      │
          │              ┌─────▼────┐          ┌─────▼────┐
          │              │ PostgreSQL│          │  Redis   │
          │              │  Primary  │          │  Cache   │
          │              └─────┬────┘          └──────────┘
          │                    │
          │              ┌─────▼────┐
          │              │PostgreSQL │
          │              │ Replicas  │
          └──────────────┴───────────┘
```

---

## 3. Component Design

### 3.1 Frontend Layer

**Technology**: React 18 + TypeScript
**Hosting**: CloudFront CDN
**Bundling**: Vite

**Responsibilities**:
- User interface rendering
- Client-side routing
- State management
- API communication

### 3.2 API Layer

**Technology**: Node.js 20 + Express
**Instances**: 5 instances (auto-scaling 3-10)
**Load Balancing**: Round-robin with health checks

**Responsibilities**:
- Request routing
- Authentication/authorization
- Business logic
- Data validation
- Response formatting

### 3.3 Data Layer

**Primary Database**: PostgreSQL 15
- **Size**: 500GB SSD
- **Connections**: 100 max
- **Backup**: Daily snapshots, point-in-time recovery

**Read Replicas**: 2 replicas
- **Lag**: < 1 second
- **Use**: Read-heavy queries, analytics

**Cache**: Redis 7
- **Size**: 16GB memory
- **Eviction**: LRU
- **TTL**: 1 hour default

---

## 4. Data Flow

**Write Path**:
1. Client → API → Validate
2. API → Primary DB → Write
3. API → Cache → Invalidate
4. API → Client → Response

**Read Path**:
1. Client → API → Check cache
2. If cache hit → Return from cache
3. If cache miss → Query replica DB
4. Store in cache → Return to client

---

## 5. Scalability

**Horizontal Scaling**:
- API servers: Auto-scale based on CPU (target: 70%)
- Database: Add read replicas as needed

**Vertical Scaling**:
- Database: Can scale to 128GB RAM if needed

**Data Partitioning**:
- User data sharded by user_id mod 4
- Archive data > 90 days to cold storage

---

## 6. High Availability

**Redundancy**:
- Multiple API server instances
- Database failover to replica (automatic)
- Multi-AZ deployment

**Health Checks**:
- API: `/health` endpoint every 30 seconds
- Database: Connection pool monitoring

**Failover**:
- API instance failure: Load balancer reroutes (< 5 sec)
- Primary DB failure: Promote replica to primary (< 2 min)

---

## 7. Security

**Network**:
- VPC with private subnets for databases
- Security groups restrict access
- TLS 1.3 for all connections

**Data**:
- Encryption at rest (AES-256)
- Encryption in transit (TLS)
- PII fields encrypted in database

**Access Control**:
- API uses JWT tokens
- Database uses role-based access
- Secrets stored in AWS Secrets Manager

---

## 8. Monitoring

**Metrics**:
- Application: Request rate, error rate, latency
- Infrastructure: CPU, memory, disk, network
- Database: Query performance, connection pool

**Dashboards**: Grafana with key metrics

**Alerts**: PagerDuty for critical issues

---

## 9. Disaster Recovery

**Backup**:
- Database: Daily snapshots retained 30 days
- Point-in-time recovery: 7 days
- Configuration: Stored in version control

**Recovery Procedures**:
- Data corruption: Restore from snapshot (RTO: 2 hours)
- Region failure: Failover to secondary region (RTO: 4 hours)

---

## 10. Cost Estimation

**Monthly Costs**:
- API servers: $500 (5 × $100)
- Database: $1,200 (primary + replicas)
- Cache: $300
- CDN: $200
- Other: $300
- **Total**: ~$2,500/month

**Scaling Costs**:
- 2x traffic: +$800/month
- 10x traffic: +$5,000/month

---

[Remaining sections: Implementation plan, risks, approvals, etc.]
```

---

## Best Practices

### DO ✅

- **Start from PRD** - All requirements should trace back to product requirements
- **Be specific** - Exact technologies, versions, configurations
- **Include diagrams** - Architecture, flows, data models
- **Document decisions** - Explain why, not just what
- **Consider scale** - Think 12-24 months ahead
- **Security first** - Address security in design, not as afterthought
- **Plan for failure** - Error handling, retries, fallbacks
- **Make it testable** - Clear testing strategy and criteria

### DON'T ❌

- **Assume requirements** - Get clarity from PM/stakeholders
- **Skip edge cases** - Document error scenarios
- **Over-engineer** - Build for current needs + reasonable growth
- **Ignore constraints** - Work within budget, timeline, team skills
- **Forget monitoring** - Plan observability from start
- **Leave questions open** - Resolve unknowns before implementation

---

## Example

**Input**: "Technical spec for user authentication with OAuth"

**Output**:

```markdown
# Technical Specification: OAuth 2.0 Authentication

**Author**: Engineering Lead
**Date**: 2025-10-17
**Status**: Draft
**Related PRD**: User Authentication PRD v1.2

---

## 1. Overview

### 1.1 Summary

**What**: Implement OAuth 2.0 authentication allowing users to sign up and log in with Google, GitHub, and LinkedIn.

**Why**:
- Reduce signup friction (PRD Goal: Increase activation from 35% to 50%)
- Eliminate password management burden for users
- Industry standard authentication

**Success Criteria** (from PRD):
- Users can sign up with 3rd-party OAuth in < 30 seconds
- 40%+ of new signups use OAuth (vs email/password)
- Zero critical security vulnerabilities
- 99.9% authentication success rate

**Target Users**: All new and existing users

### 1.2 Scope

**In Scope**:
- OAuth 2.0 Authorization Code flow
- Google, GitHub, LinkedIn providers
- Account linking for existing users
- JWT-based session management
- Email fallback for auth failures

**Out of Scope** (future versions):
- Two-factor authentication (v1.1)
- Magic link authentication (v1.2)
- Enterprise SSO/SAML (v2.0)

**Dependencies**:
- OAuth app registrations with Google, GitHub, LinkedIn
- Email service for account verification
- User dashboard for connected accounts management

---

## 2. Technical Approach

### 2.1 High-Level Architecture

```
User Browser → Our App → OAuth Provider (Google/GitHub/LinkedIn)
                ↓
          Generate JWT Token
                ↓
          Store in Database
                ↓
          Return to User
```

**Flow**:
1. User clicks "Sign in with Google"
2. User redirected to Google OAuth consent screen
3. User grants permission
4. Google redirects back with authorization code
5. Our backend exchanges code for access token
6. We fetch user profile from Google
7. Create/update user in our database
8. Issue JWT token to user
9. User authenticated

### 2.2 Technology Stack

**Frontend**:
- Framework: React 18
- OAuth Library: `react-oauth2-code-flow` v1.0
- State Management: Context API

**Backend**:
- Language: Node.js 20
- Framework: Express 4.18
- OAuth Library: `passport` v0.6 + `passport-google-oauth20`, `passport-github2`, `passport-linkedin-oauth2`
- JWT Library: `jsonwebtoken` v9.0

**Data**:
- Primary DB: PostgreSQL 15
- Tables: `users`, `oauth_connections`, `sessions`

### 2.3 Design Decisions

**Decision 1**: Use Authorization Code flow (not Implicit flow)
- **Options**: Authorization Code, Implicit, Client Credentials
- **Chosen**: Authorization Code with PKCE
- **Rationale**: More secure (tokens never exposed in browser), supports refresh tokens, recommended by OAuth 2.0 best practices
- **Trade-offs**: Slightly more complex implementation (acceptable)

**Decision 2**: Issue JWT tokens (not opaque session tokens)
- **Options**: JWT, Opaque tokens in database, Cookie sessions
- **Chosen**: JWT stored in httpOnly cookies
- **Rationale**: Stateless authentication, scales horizontally, industry standard
- **Trade-offs**: Can't revoke tokens before expiry (mitigated with short TTL + refresh tokens)

**Decision 3**: Allow account linking
- **Options**: Force single auth method, Allow multiple methods per account
- **Chosen**: Allow linking multiple OAuth providers to one account
- **Rationale**: User flexibility, better UX if one provider is down
- **Trade-offs**: More complex account management (acceptable for better UX)

---

[Continue with full spec following the template...]

## 3. Detailed Design

### 3.1 User Flows

**Flow 1: New User OAuth Signup**
1. User clicks "Sign in with Google"
2. System redirects to Google OAuth consent page
3. User grants permissions
4. Google redirects to callback URL with authorization code
5. System exchanges code for access token
6. System fetches user email and name from Google
7. System creates new user account
8. System issues JWT token
9. User redirected to dashboard (authenticated)

**Edge Cases**:
- If email already exists: Prompt to link accounts or use existing auth method
- If OAuth provider is down: Show error, suggest email/password login
- If user denies permission: Return to login page with explanation

### 3.2 API Design

#### Endpoint: Initiate OAuth Flow

```
GET /auth/oauth/{provider}/initiate

Parameters:
- provider: "google" | "github" | "linkedin"

Response (302 Redirect):
Location: https://accounts.google.com/o/oauth2/v2/auth?
  client_id=...&
  redirect_uri=https://ourapp.com/auth/oauth/google/callback&
  response_type=code&
  scope=email profile&
  state=random_csrf_token
```

#### Endpoint: OAuth Callback

```
GET /auth/oauth/{provider}/callback

Parameters:
- code: Authorization code from provider
- state: CSRF token (must match session)

Response (200 OK):
{
  "user": {
    "id": "uuid",
    "email": "user@example.com",
    "name": "John Doe",
    "oauth_provider": "google",
    "created_at": "2025-10-17T10:00:00Z"
  },
  "token": "eyJhbGc...",  // JWT token
  "expires_in": 3600
}

Also sets cookie:
Set-Cookie: auth_token=eyJhbGc...; HttpOnly; Secure; SameSite=Strict; Max-Age=3600
```

### 3.3 Data Models

#### Users Table

```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email VARCHAR(255) UNIQUE NOT NULL,
  name VARCHAR(255),
  avatar_url VARCHAR(500),
  email_verified BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),

  INDEX idx_email (email)
);
```

#### OAuth Connections Table

```sql
CREATE TABLE oauth_connections (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID NOT NULL REFERENCES users(id) ON DELETE CASCADE,
  provider VARCHAR(50) NOT NULL, -- 'google', 'github', 'linkedin'
  provider_user_id VARCHAR(255) NOT NULL,
  access_token TEXT, -- Encrypted
  refresh_token TEXT, -- Encrypted
  token_expires_at TIMESTAMP,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW(),

  UNIQUE(provider, provider_user_id),
  INDEX idx_user_id (user_id)
);
```

---

[Continue with remaining sections: Security, Performance, Testing, Implementation Plan, etc.]
```

---

## Model

Use: Sonnet

## Related

- `/pm:prd` - Product requirements driving the spec
- `/pm:api-documentation` - For API-specific docs
- `/pm:decision-log` - Document technical decisions
- `technical-pm` agent - For complex technical questions
- `backend-architect` agent - For architecture review
