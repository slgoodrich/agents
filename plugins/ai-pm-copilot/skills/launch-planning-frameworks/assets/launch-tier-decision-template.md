# Launch Tier Decision Framework

Use this framework to determine the appropriate launch tier (T1, T2, or T3) for your product or feature.

---

## Launch Tier System

### Tier 1: Major Launch (Company-wide priority)

**Characteristics**:

- New product or major feature
- Strategic initiative
- Broad customer impact
- Significant revenue opportunity

**Timeline**: 8-12 weeks planning
**Resources**: Full cross-functional team (PM, Marketing, Sales, CS, Eng)
**Investment**: High (marketing budget, events, PR, analyst relations)

**Examples**:

- New product line
- Platform launch
- Major rebrand
- Enterprise features for upmarket expansion
- Geographic expansion

---

### Tier 2: Standard Launch (Team priority)

**Characteristics**:

- Significant feature
- Specific customer segment
- Moderate revenue impact
- Competitive parity

**Timeline**: 4-6 weeks planning
**Resources**: Core team (PM, Marketing, Sales enablement)
**Investment**: Medium (email campaigns, in-app announcements, blog post)

**Examples**:

- New feature category
- Integration with major partner
- Expansion to new market segment
- Pricing changes
- Major workflow improvements

---

### Tier 3: Minor Launch (Low-key release)

**Characteristics**:

- Enhancement or improvement
- Existing feature iteration
- Limited customer impact
- Maintenance/quality focused

**Timeline**: 1-2 weeks planning
**Resources**: PM + minimal support (maybe blog post writer)
**Investment**: Low (release notes, in-app notification)

**Examples**:

- Feature improvements
- Bug fixes
- Performance enhancements
- UI refinements
- Minor integrations

---

## Decision Framework

Answer these questions to determine tier:

### Question 1: Customer Impact

**How many customers does this affect?**

- All/most customers → T1
- Specific segment (20-50%) → T2
- Small subset (<20%) → T3

**How important is this to affected customers?**

- Critical/game-changing → T1
- Important/valuable → T2
- Nice-to-have/incremental → T3

---

### Question 2: Business Impact

**What's the revenue opportunity?**

- > $1M ARR potential → T1
- $100K-$1M ARR → T2
- <$100K ARR → T3

**Strategic importance?**

- Enables new market/major strategy → T1
- Supports growth goals → T2
- Incremental improvement → T3

---

### Question 3: Competitive Landscape

**Competitive positioning?**

- Major differentiation/must-have for market → T1
- Parity with competitors → T2
- Nice-to-have enhancement → T3

**Market timing?**

- First-to-market opportunity → T1
- Important but not urgent → T2
- No time pressure → T3

---

### Question 4: Complexity & Risk

**Development complexity?**

- Major platform changes → T1
- Moderate feature addition → T2
- Simple enhancement → T3

**Cross-functional coordination needed?**

- Multiple teams, external partners → T1
- Few teams, mostly internal → T2
- Minimal coordination → T3

---

## Tier Decision Matrix

Use this scorecard:

```
Score each factor 1-3:
- 3 points = T1 characteristics
- 2 points = T2 characteristics
- 1 point = T3 characteristics

Factors:
1. Customer reach (all/segment/small)
2. Customer importance (critical/important/nice)
3. Revenue opportunity (high/medium/low)
4. Strategic importance (critical/supportive/incremental)
5. Competitive impact (differentiation/parity/minor)
6. Complexity (high/medium/low)

Total Score:
- 15-18 points → Tier 1
- 10-14 points → Tier 2
- 6-9 points → Tier 3
```

---

## Example: Deciding Tier

**Feature**: Real-time collaboration editing

**Scoring**:

1. Customer reach: Most customers (3)
2. Customer importance: Game-changing for remote teams (3)
3. Revenue: $500K ARR potential (2)
4. Strategic: Enables team plan upsells (2)
5. Competitive: Major differentiator (3)
6. Complexity: High - real-time sync (3)

**Total**: 16 points → **Tier 1 Launch**

**Plan**:

- 12-week launch timeline
- Full marketing campaign
- Sales enablement program
- PR and analyst outreach
- Customer beta program
- Executive sponsorship

---

## Tier Planning Comparison

| Aspect                    | Tier 1                   | Tier 2             | Tier 3              |
| ------------------------- | ------------------------ | ------------------ | ------------------- |
| **Planning Time**         | 8-12 weeks               | 4-6 weeks          | 1-2 weeks           |
| **Marketing Budget**      | $50K-$500K+              | $10K-$50K          | $0-$5K              |
| **Team Size**             | 10-20 people             | 3-5 people         | 1-2 people          |
| **Blog Post**             | Multiple, guest posts    | One comprehensive  | Short announcement  |
| **Email Campaign**        | Multi-touch nurture      | 2-3 emails         | Single announcement |
| **PR/Press**              | Press release, briefings | Selective outreach | None                |
| **Sales Training**        | Full program, materials  | Deck + FAQ         | Email summary       |
| **Event/Webinar**         | Yes, multiple            | Maybe one webinar  | No                  |
| **Beta Program**          | Yes, formal              | Maybe informal     | No                  |
| **Executive Involvement** | High (CEO/VP)            | Medium (Directors) | Low (Manager)       |

---

## Tips for Tier Assignment

**Over-tiering (making T3 → T1)**:

- Wastes resources
- Delays launch
- Creates unrealistic expectations
- Diverts attention from true priorities

**Under-tiering (making T1 → T3)**:

- Misses market opportunity
- Poor adoption (nobody knows about it)
- Frustrated sales team (not prepared)
- Wasted development effort

**Getting it right**:

- Be honest about impact
- Consider resource constraints
- Align with company priorities
- Validate with the team
- Can always adjust tier mid-planning if scope changes

---

## Template: Tier Decision Document

```markdown
# Launch Tier Decision: [Feature Name]

## Feature Summary

[1-2 sentence description]

## Tier Analysis

### Customer Impact

- Reach: [All / Segment / Small subset]
- Importance: [Critical / Important / Nice-to-have]
- Score: [1-3]

### Business Impact

- Revenue: [$X ARR potential]
- Strategy: [How it fits company goals]
- Score: [1-3]

### Competitive Impact

- Positioning: [Differentiation / Parity / Minor]
- Timing: [Urgent / Important / Flexible]
- Score: [1-3]

### Complexity

- Development: [High / Medium / Low]
- Coordination: [Many teams / Few / Minimal]
- Score: [1-3]

## Total Score: [X/18]

## Recommended Tier: [T1 / T2 / T3]

## Rationale

[Why this tier makes sense given constraints and opportunities]

## Approval

- PM: [Name] | Date: **\_\_\_**
- Marketing: [Name] | Date: **\_\_\_**
- Exec Sponsor: [Name] | Date: **\_\_\_**
```

---

## Next Steps After Tier Decision

**Once tier is decided**:

**For Tier 1**:
→ Use `12-week-launch-plan-template.md`
→ Assemble cross-functional launch team
→ Secure budget and executive sponsorship

**For Tier 2**:
→ Use condensed 6-week plan
→ Coordinate with marketing + sales
→ Plan targeted communication

**For Tier 3**:
→ Use `launch-checklist-template.md` (simplified)
→ Write release notes
→ Notify customers via in-app/email

---

**Key Principle**: The tier determines the investment, not the feature quality. Even Tier 3 launches should ship high-quality, well-tested features. The difference is in the marketing investment and coordination, not the product excellence.
