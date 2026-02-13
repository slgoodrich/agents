# Google PRD Template

Google's approach emphasizes objectives, user benefits, and clear success criteria. This template is structured for clarity and clarity.

**Use for**: New products, major features, cross-team initiatives
**Length**: 5-10 pages
**Audience**: Cross-functional teams, leadership

**Note on Sections**: Not all sections are required. Include only sections where you have real data.

- **Required**: Objectives, User Benefits, Requirements, Technical Approach
- **Optional**: Success Metrics (include only if you have baselines/targets - omit if not available)

---

# [Product/Feature Name]

**Author**: [PM Name] | **Tech Lead**: [Eng Name] | **Designer**: [Design Name]
**Created**: [Date] | **Last Updated**: [Date]
**Status**: Draft / In Review / Approved
**Target Launch**: [Quarter Year]

---

## Objectives

### Goals

What are we trying to achieve? List 2-4 high-level goals.

1. [Goal 1]
2. [Goal 2]
3. [Goal 3]

**Example**:

1. Increase user engagement with photos by 30%
2. Reduce friction in photo sharing workflow
3. Enable new use case: collaborative photo albums

---

### Non-Goals

What are we explicitly NOT trying to do? Helps prevent scope creep.

- [Non-goal 1]
- [Non-goal 2]

**Example**:

- Building a full photo editing suite (use existing editor)
- Competing with professional photography tools
- Supporting video albums (photos only for v1)
- Third-party integrations (Google ecosystem only)

---

### Success Metrics _(Include only if you have actual metrics)_

⚠️ **IMPORTANT**: The examples below show FORMAT only. Do NOT fabricate numbers.

- **If you have baselines and targets**: Include this section with real data
- **If you don't have metrics defined**: Omit this section or work with user to define them

How will we measure success? Define metrics with targets when available.

**Primary Metrics**:

- [Metric 1]: [Baseline → Target within timeframe]
- [Metric 2]: [Baseline → Target within timeframe]

**Secondary Metrics**:

- [Metric 3]: [Baseline → Target]
- [Metric 4]: [Baseline → Target]

**Example**:
**Primary**:

- Weekly Active Users (WAU) engaging with photos: 10M → 13M within 3 months
- Photos shared per active user per week: 2.5 → 4.0

**Secondary**:

- Time spent in photo view: 3min → 5min per session
- Photo upload rate: +20%
- NPS for photo features: 35 → 50

---

## Background

### Problem

What problem are we solving? Describe from user perspective.

**Example**:
"Users have thousands of photos on their devices but rarely revisit them after initial upload. Current photo apps focus on storage and search, but don't facilitate meaningful engagement with photo memories. Users want to relive experiences and share them with others, but existing workflows are too cumbersome."

"Data shows that 80% of uploaded photos are never viewed again after initial upload. Users who do engage with photos cite 'rediscovering old memories' as the #1 value driver, yet we don't proactively surface these moments."

---

### Background & Strategic Fit

Why does this matter strategically? How does it fit company priorities?

**Example**:
"Photos are a high-engagement category with strong retention signals. Users who regularly engage with photos have 3x higher retention rates. This aligns with our Q2 goal to 'Increase user retention through regular engagement touchpoints.'"

"Competitive landscape: Apple Photos has Memories feature (automated photo collections) that drives significant engagement. We're losing ground to Apple in the photo space, particularly among iOS users. This feature helps us compete and differentiate."

---

### User Research Summary

What do we know from user research? Include key findings.

**Example**:
"Conducted 30 user interviews with active photo uploaders:

- 82% feel nostalgic when they stumble upon old photos
- 67% wish they could easily see photos from a year ago
- 54% want to share photo collections with specific people (e.g., family)
- Current pain: 'I have 10,000 photos but they're just sitting there. I never look at them unless I'm searching for something specific.'"

"Survey of 5,000 users: 72% said they'd use a feature that automatically creates collections from trips or events. 45% would share these collections with others."

---

## User Experience

### User Scenarios

Describe key user scenarios in story format.

**Scenario 1: [Name]**
[Who, what, when, where, why - tell a story]

**Example Scenario 1: Rediscovering Memories**
"Sarah is commuting to work on Monday morning. She opens the app and sees a notification: 'Memories from 1 year ago.' Curious, she taps it and sees photos from her vacation to Hawaii last year. She smiles, remembering the trip, and shares the collection with her husband via chat. He responds with heart emoji. Sarah feels connected to her memories and loved ones."

**Scenario 2: Collaborative Album**
"Mike is planning his parents' 40th anniversary. He creates a collaborative album in the app and invites his siblings to add their favorite photos of their parents. Over two weeks, the album grows to 150 photos from various family members. At the anniversary party, Mike presents the album as a digital slideshow. Everyone tears up."

---

### Key User Flows

Map out the primary user flows step-by-step.

**Flow 1: Viewing Auto-Generated Memory**

1. User opens app
2. System shows notification: "Memories from 1 year ago"
3. User taps notification
4. App displays curated collection of photos from that time period
5. User can scroll through, heart favorites, or share collection
6. User taps "Share" → selects recipients → collection link sent

**Flow 2: Creating Collaborative Album**

1. User taps "Create Album"
2. Selects "Collaborative Album"
3. Names album (e.g., "Mom & Dad's Anniversary")
4. Selects initial photos to include
5. Taps "Invite People"
6. Selects contacts or enters emails
7. Invitees receive notification and can add photos
8. Album updates in real-time as people add photos

---

### Mockups & Design

[Link to design files or embed key screens]

**Example**:

- Figma: [link]
- Key screens:
  - Memory notification
  - Memory collection view
  - Collaborative album creation
  - Album sharing interface

---

## Product Requirements

### Functional Requirements

What must the product do? Organize by priority.

**P0 (Must Have for Launch)**

**F1: Automatic Memory Generation**

- System analyzes photos to identify temporal clusters (same day/weekend)
- Surfaces memories from 1, 2, 3, 5 years ago (key anniversaries)
- User receives push notification: "Memories from X year(s) ago"
- Collection shows 10-30 photos from that time period
- User can view, heart, share, or dismiss

**F2: Manual Collection Creation**

- User can create custom photo collection
- Can select photos from library (multi-select)
- Can add title and description
- Can set privacy: private, shared, or public

**F3: Collaborative Albums**

- User can invite others to contribute to album
- Invitees can add/remove their own photos
- All contributors see real-time updates
- Push notifications when new photos added
- Can set permissions: view-only or can-edit

**F4: Sharing**

- User can share collection via link
- Link can be set to: specific people (via email/contact), anyone with link, or public
- Recipients can view but not edit (unless invited as collaborator)
- Share link expires after 30 days (configurable)

---

**P1 (Should Have, can defer if needed)**

**F5: Memory Customization**

- User can adjust frequency of memory notifications (daily/weekly/off)
- User can hide specific photos from appearing in memories
- User can manually trigger memory generation for custom date range

**F6: Reactions & Comments**

- Users can react to photos in shared collections (heart, laugh, etc.)
- Users can comment on individual photos
- Notifications for new reactions/comments

---

**P2 (Nice to Have, defer to v2)**

**F7: Themes & Templates**

- Pre-designed album themes (vacation, wedding, baby, etc.)
- Auto-layout suggestions based on photo content

**F8: Slideshow Mode**

- Auto-play collection as slideshow
- Background music options
- Chromecast/AirPlay support

---

### Non-Functional Requirements

**Performance**:

- Memory generation completes within 2 seconds
- Photo collections load within 1 second (first 20 photos)
- Collaborative album updates propagate to all users within 5 seconds

**Scale**:

- Support collections up to 1,000 photos
- Support up to 50 collaborators per album
- Handle 10M+ memory notifications per day

**Privacy & Security**:

- All shared links require authentication (no public anonymous access for v1)
- User can revoke shared links at any time
- GDPR-compliant data handling for EU users
- No AI scanning of photos without explicit user consent

**Accessibility**:

- VoiceOver support for iOS
- TalkBack support for Android
- Keyboard navigation for web
- High contrast mode support

---

## Technical Considerations

### Architecture

High-level technical approach.

**Example**:

- Memory generation: batch job runs nightly, analyzes photo metadata (timestamps, location)
- Uses ML model to identify quality photos (well-exposed, in-focus, faces detected)
- Ranking algorithm prioritizes photos with faces, variety, and composition
- Results cached per user for fast retrieval

---

### APIs & Integrations

What systems does this depend on?

**Example**:

- Photo Library API (read access to user photos)
- Notification Service (push notifications)
- Sharing Service (link generation, access control)
- ML Platform (photo quality scoring)
- Real-time Sync Service (collaborative albums)

---

### Data & Privacy

How do we handle user data?

**Example**:

- Photo analysis happens on-device where possible (privacy-preserving)
- Cloud analysis requires explicit user opt-in
- Shared album data stored with end-to-end encryption (planned, not v1)
- Users can delete collections (soft delete, 30-day recovery window)
- Comply with GDPR right-to-delete

---

### Performance & Scalability

How do we ensure this scales?

**Example**:

- Memory generation uses batch processing (not real-time) to manage load
- Photo thumbnails cached on CDN for fast loading
- Collaborative albums use WebSocket for real-time sync (fallback to polling)
- Horizontal scaling for sharing service
- Rate limiting: max 100 photos uploaded per day per user

---

### Risks & Mitigation

| Risk                                   | Impact                    | Likelihood | Mitigation                                                                     |
| -------------------------------------- | ------------------------- | ---------- | ------------------------------------------------------------------------------ |
| ML model picks bad photos for memories | High (poor UX)            | Medium     | Manual curation option, ML model validation with human reviewers               |
| Privacy concerns about photo analysis  | High (trust issues)       | Medium     | Clear user communication, opt-in approach, on-device processing where possible |
| Real-time sync doesn't scale           | Medium (degraded UX)      | Low        | Graceful degradation to polling, horizontal scaling ready                      |
| Users overwhelmed by notifications     | Medium (turn off feature) | High       | Default to weekly not daily, easy opt-out, smart notification throttling       |

---

## Dependencies

### Internal Dependencies

What do we need from other teams?

**Example**:

- **ML Team**: Photo quality scoring model (due: Q1 Week 6)
- **Infra Team**: WebSocket service capacity planning (due: Q1 Week 8)
- **Privacy Team**: Legal review of photo scanning disclosure (due: Q1 Week 4)
- **Design System Team**: New components for collection UI (due: Q1 Week 3)

---

### External Dependencies

What external factors could affect this?

**Example**:

- Platform changes (iOS/Android permission models)
- Third-party library updates (image processing SDK)
- Compliance requirements (GDPR, CCPA updates)

---

## Launch Plan

### Rollout Strategy

How will we launch this?

**Example**:

1. **Alpha** (Q1 W10): Internal dogfood with Google employees (500 users)
2. **Beta** (Q1 W12-14): Invite-only external beta (10,000 users)
3. **Staged Rollout** (Q2 W1-2): 1% → 5% → 25% → 100% of users
4. **Targeting**: Start with users who have 500+ photos (higher engagement likelihood)

---

### Success Criteria (Go/No-Go)

What must be true before full launch?

- [ ] Memory generation accuracy > 80% (user survey)
- [ ] < 0.5% crash rate in beta
- [ ] Notification click-through rate > 15%
- [ ] Sharing feature used by > 30% of beta users
- [ ] Privacy review completed and signed off
- [ ] Performance targets met (p95 < 2s for memory gen)

---

### Monitoring & Metrics

How will we track success post-launch?

**Week 1**:

- Monitor crash rates, error rates, load times
- Track feature adoption (% of users who view memories)
- Quick survey of early users (n=100)

**Month 1**:

- Measure primary metrics (WAU, photos shared)
- A/B test notification frequency (daily vs weekly vs monthly)
- User interviews with heavy users (n=20)

**Month 3**:

- Evaluate success metrics against targets
- Assess retention impact (cohort analysis)
- Decide on v2 features based on learnings

---

## Open Issues

Questions that need resolution before/during development.

| Issue                                                               | Owner   | Due Date | Status                  |
| ------------------------------------------------------------------- | ------- | -------- | ----------------------- |
| Should memory notifications be daily, weekly, or user-configurable? | PM      | Q1 W3    | Open                    |
| What's max photos per collaborative album?                          | Eng     | Q1 W4    | Blocked on perf testing |
| Do we need content moderation for shared albums?                    | Legal   | Q1 W2    | In Review               |
| Which ML model for photo quality?                                   | ML Team | Q1 W5    | Options identified      |

---

## Appendix

### Research Links

- User interview notes: [link]
- Survey results: [link]
- Competitive analysis: [link]

### Design Links

- Figma designs: [link]
- User flow diagrams: [link]
- Prototype: [link]

### Technical Docs

- Tech design doc: [link]
- API specs: [link]
- Data models: [link]

---

## Review & Approval

### Reviewers

- [ ] Engineering: [Name]
- [ ] Design: [Name]
- [ ] Product Marketing: [Name]
- [ ] Legal/Privacy: [Name]
- [ ] Data Science: [Name]

### Approval

- [ ] VP Product: [Name] | Date: **\_\_\_**
- [ ] Engineering Director: [Name] | Date: **\_\_\_**

---

## Tips for Google-Style PRDs

### Do's:

- Start with objectives (goals and non-goals)
- Define success metrics with specific targets
- Tell user stories to illustrate the experience
- Be specific about requirements and priorities
- Document open issues and dependencies
- Get cross-functional review early

### Don'ts:

- Don't conflate goals with features
- Don't write vague success criteria
- Don't skip non-functional requirements
- Don't hide risks or open questions
- Don't launch without clear go/no-go criteria

### Google's Product Philosophy

Google emphasizes:

1. **User benefit first**: What's the user value?
2. **Data-driven decisions**: How will we measure success?
3. **Scale from day one**: Will this work at Google scale?
4. **Launch and iterate**: Ship, measure, improve
5. **10x thinking**: Are we making things 10x better or 10% better?

---

**When to Use Google PRD vs Other Templates**:

- Google PRD: Cross-functional initiatives, data-driven products, scale considerations
- Amazon PR/FAQ: Customer-centric products, working backwards from launch
- Lean PRD: Small, focused features with low complexity
