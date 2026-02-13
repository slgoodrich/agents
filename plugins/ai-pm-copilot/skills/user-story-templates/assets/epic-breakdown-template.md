# Epic to Stories Breakdown Template

Template for breaking down large epics into manageable user stories.

---

## Template

```markdown
# Epic: [Epic Name]

## Epic Goal

[One-sentence description of what this epic achieves]

## User Value

[Why this matters to users - the problem it solves or opportunity it enables]

## Business Value

[Why this matters to business - metrics, revenue, strategy]

## Success Criteria

- [Metric 1]: [Baseline → Target]
- [Metric 2]: [Baseline → Target]

---

## User Stories

### Story 1: [Title]

**Priority**: Must Have / Should Have / Nice to Have

As a [user]
I want [goal]
So that [benefit]

**Acceptance Criteria**:

- [ ] [Criterion]
- [ ] [Criterion]

**Story Points**: [X]
**Dependencies**: [List any blocking stories]

---

### Story 2: [Title]

[Same format]

---

[Continue for all stories...]

---

## Definition of Done (Epic Level)

- [ ] All Must Have stories completed
- [ ] Integration tested across all stories
- [ ] Documentation complete (user docs + technical docs)
- [ ] Launched to production
- [ ] Success metrics tracked and initial results reviewed

## Out of Scope

- [Feature explicitly excluded]
- [Future iteration item]

## Timeline

- **Start**: [Date]
- **Target Launch**: [Date]
- **Duration**: [X weeks/sprints]
```

---

## Example: Collaborative Album Epic

```markdown
# Epic: Collaborative Photo Albums

## Epic Goal

Enable users to create and share photo albums where multiple people can contribute photos.

## User Value

Users want to collect memories from events (weddings, trips, parties) where multiple people took photos. Currently they have to manually collect photos from everyone. Collaborative albums let everyone contribute directly, creating richer, more complete memory collections.

## Business Value

- **Engagement**: Increase weekly active users by 15% (collaborative features drive retention)
- **Viral growth**: Each shared album brings 2-3 new users on average
- **Premium upgrade**: 30% of collaborative album creators expected to upgrade to premium (unlimited albums)

## Success Criteria

- **Adoption**: 20% of active users create or contribute to collaborative album in first 3 months
- **Engagement**: Users with collaborative albums have 2x session length vs baseline
- **Viral coefficient**: 0.3 (each user invites 0.3 new users on average)
- **Premium conversion**: 10% of album creators upgrade within 30 days

---

## User Stories

### Story 1: Create Collaborative Album

**Priority**: Must Have

As a user
I want to create a new album and mark it as "collaborative"
So that I can invite others to add photos

**Acceptance Criteria**:

- [ ] "Create Album" button visible on Albums page
- [ ] User can name the album
- [ ] Toggle for "Allow others to contribute" (defaults to off)
- [ ] Album appears in user's album list
- [ ] Album creator is owner with full permissions

**Story Points**: 3
**Dependencies**: None

---

### Story 2: Invite Contributors

**Priority**: Must Have

As an album owner
I want to invite people to contribute to my album
So that they can add their photos

**Acceptance Criteria**:

- [ ] "Invite Contributors" button on album page
- [ ] Can invite via email address or app username
- [ ] Can select permission level: View Only or Can Add Photos
- [ ] Invitees receive email notification with album link
- [ ] Invitation includes album name and owner name
- [ ] Can invite up to 50 people per album

**Story Points**: 5
**Dependencies**: Story 1

---

### Story 3: Accept Invitation & Add Photos

**Priority**: Must Have

As an invitee
I want to accept the invitation and add my photos
So that I can contribute to the shared album

**Acceptance Criteria**:

- [ ] Clicking invitation link opens album (if logged in) or signup page
- [ ] Album appears in "Shared with Me" section
- [ ] "Add Photos" button visible if contributor has add permission
- [ ] Can select and upload multiple photos at once
- [ ] Photos appear in album immediately after upload
- [ ] Other contributors see new photos within 30 seconds (real-time or near real-time)

**Story Points**: 5
**Dependencies**: Story 2

---

### Story 4: Real-Time Updates

**Priority**: Should Have

As a contributor
I want to see when others add photos to the shared album
So that I can see the album growing without refreshing

**Acceptance Criteria**:

- [ ] New photos appear automatically without page refresh
- [ ] Updates propagate within 30 seconds
- [ ] Visual indication when new photos added ("3 new photos")
- [ ] Works on web and mobile app
- [ ] Graceful fallback if real-time connection lost (poll every 60s)

**Story Points**: 8
**Dependencies**: Story 3

---

### Story 5: Manage Permissions

**Priority**: Should Have

As an album owner
I want to manage who has access to my album
So that I can control contributions and viewing

**Acceptance Criteria**:

- [ ] "Manage Contributors" page lists all invited people
- [ ] Can change permission level (View Only ↔ Can Add)
- [ ] Can remove contributors
- [ ] Removed contributors lose access immediately
- [ ] Can change album from collaborative to private (freezes contributions)
- [ ] Confirmation dialog before removing contributor

**Story Points**: 3
**Dependencies**: Story 2

---

### Story 6: Notifications

**Priority**: Nice to Have

As a contributor
I want to receive notifications when photos are added
So that I stay engaged with the album

**Acceptance Criteria**:

- [ ] Push notification when new photos added (batched: max 1/hour)
- [ ] Email digest option (daily or weekly summary)
- [ ] In-app notification badge
- [ ] Notification settings per album
- [ ] Notification includes photo preview and contributor name

**Story Points**: 5
**Dependencies**: Story 3

---

### Story 7: Album Activity Feed

**Priority**: Nice to Have

As a user
I want to see activity history for the album
So that I know who contributed what

**Acceptance Criteria**:

- [ ] "Activity" tab shows chronological feed
- [ ] Feed shows: photos added, contributors joined, permissions changed
- [ ] Each activity shows timestamp and person
- [ ] Can filter by contributor
- [ ] Activity feed loads fast (<2s) even for albums with 100+ activities

**Story Points**: 5
**Dependencies**: Story 3

---

## Definition of Done (Epic Level)

- [ ] All Must Have stories completed (Stories 1-3)
- [ ] All Should Have stories completed (Stories 4-5)
- [ ] Integration tested: Full flow from create → invite → contribute → manage
- [ ] Load tested: 50 contributors per album, 1000 photos per album
- [ ] Documentation complete:
  - [ ] User guide: "Creating Collaborative Albums"
  - [ ] FAQ updated
  - [ ] API docs (if applicable)
- [ ] Launched to production via staged rollout (1% → 10% → 100%)
- [ ] Success metrics dashboard created
- [ ] Week 1 metrics reviewed

## Out of Scope for v1

- Album templates or themes (future: make albums prettier)
- Comments on individual photos (future: enable discussion)
- Album moderation/reporting (future: handle abuse)
- Collaborative albums in mobile app (v1 is web-only)
- Merge/split albums (edge case, defer unless requested)
- Album analytics (who viewed, engagement stats)

## Timeline

- **Start**: Sprint 12 (June 1)
- **Must Have Stories**: Sprints 12-13 (3 weeks)
- **Should Have Stories**: Sprints 14-15 (3 weeks)
- **Testing & Polish**: Sprint 16 (1 week)
- **Target Launch**: End of Sprint 16 (July 15)
- **Total Duration**: 7 weeks

## Risks & Mitigation

| Risk                            | Mitigation                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Real-time sync doesn't scale    | Build with graceful degradation (fallback to polling)        |
| Users spam invites (abuse)      | Rate limit: max 50 invites/album, max 10 albums/day          |
| Storage costs for shared albums | Monitor closely, consider premium-only for >500 photos/album |
```

---

## Guidance

### Epic vs Story

**Epic**: Large body of work that can be broken down (weeks/months)
**Story**: Small, deliverable increment of value (days)

**Signs you have an epic**:

- Takes more than 1 sprint
- Involves multiple team members
- Has multiple user workflows
- Requires multiple stories to deliver value

**Signs you have a story**:

- Can be completed in 1-5 days
- One developer can implement it
- Clear acceptance criteria
- Testable outcome

---

### Breaking Down Epics

**Common splitting strategies**:

1. **By workflow steps**: Create → Invite → Contribute → Manage
2. **By priority**: Must Have → Should Have → Nice to Have
3. **By user role**: Admin → Contributor → Viewer
4. **By CRUD**: Create → Read → Update → Delete
5. **By complexity**: Simple version → Advanced features

**Good breakdown**:

- Each story delivers some value independently
- Early stories enable later stories (dependencies clear)
- Stories can be developed in parallel where possible
- Critical path identified (what must be done first)

---

### Story Sequencing

Order matters. Consider:

1. **Dependencies**: What blocks what?
2. **Risk**: De-risk technical unknowns early
3. **Value**: Deliver highest value first
4. **Learning**: Get user feedback early
5. **Parallelization**: What can different devs work on simultaneously?

**Example sequence for Collaborative Albums**:

- Week 1: Story 1 (Create Album) - foundation
- Week 2: Stories 2 & 3 in parallel (Invite + Contribute) - core value
- Week 3: Story 4 (Real-time) - technical risk, start early
- Week 4: Story 5 (Permissions) - builds on invite
- Week 5-6: Stories 6 & 7 (Notifications, Activity) - polish

---

### Estimating Epics

**Bottom-up estimation**:

1. Break epic into stories
2. Estimate each story (story points or days)
3. Sum estimates
4. Add buffer (20-30% for unknowns)

**Top-down estimation** (before detailed breakdown):

- T-shirt sizes: S (2-3 weeks), M (1-2 months), L (2-3 months), XL (split it!)
- Fibonacci: 13, 21, 34, 55+ story points

**Example**: Collaborative Albums

- Story 1: 3 points
- Story 2: 5 points
- Story 3: 5 points
- Story 4: 8 points
- Story 5: 3 points
- Story 6: 5 points
- Story 7: 5 points
- **Total**: 34 points (~7 weeks at 5 points/week velocity)

---

### Epic Success Criteria

Define SMART metrics:

- **Specific**: "Increase engagement" → "Increase weekly active users by 15%"
- **Measurable**: Use numbers, percentages, concrete targets
- **Achievable**: Stretch but realistic based on data
- **Relevant**: Ties to business goals and user value
- **Time-bound**: "within 3 months of launch"

Track both:

- **Leading indicators**: Adoption rate, feature usage
- **Lagging indicators**: Retention, revenue impact

---

## When to Use This Template

Use when you have:

- Large feature that takes multiple sprints
- Complex workflow requiring many stories
- Major initiative requiring team alignment
- Need for executive-level visibility
- Multi-team coordination needed

For single-sprint work, skip epic and just create stories.
