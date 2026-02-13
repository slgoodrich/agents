# Now-Next-Later Roadmap Template

The most flexible roadmap format - no date commitments, easy to adjust, clear focus.

---

## Template

```markdown
# Product Roadmap - [Quarter/Year]

## Now (Current Focus)

What we're actively working on right now.

### [Initiative 1 Name]

**Problem**: [What customer/business problem this solves]
**Approach**: [How we're solving it]
**Status**: In development | Design | Testing
**Expected**: [Rough timeframe, e.g., "Next 4-6 weeks"]

### [Initiative 2 Name]

**Problem**: [Problem]
**Approach**: [Approach]
**Status**: [Status]
**Expected**: [Timeframe]

---

## Next (Coming Soon)

What we'll likely work on next - validated problems, high confidence.

### Theme: [Theme Name]

**Why**: [Strategic rationale]
**Initiatives**:

- [Initiative A]: [Brief description]
- [Initiative B]: [Brief description]
  **Success Metrics**: [How we'll measure]

### Theme: [Theme Name]

[Same format]

---

## Later (Future Direction)

Areas we're exploring - directional bets, lower confidence.

### [Area 1]

**Exploration**: [What we're considering]
**Why it matters**: [Strategic value]

### [Area 2]

[Same format]

---

## Not Doing (Trade-offs)

What we've explicitly decided not to prioritize:

- **[Thing 1]**: [Why not - e.g., "Low customer demand, doesn't fit strategy"]
- **[Thing 2]**: [Why not]
```

---

## When to Use

**Best for**:

- Fast-moving environments
- High uncertainty
- Want flexibility
- Avoid date commitments

**Not good for**:

- Complex dependencies
- Need resource planning
- Require executive buy-in on timeline

---

## Confidence Levels

**Now** (80-100% confidence):

- Problem validated
- Solution defined
- In active development
- Will deliver soon

**Next** (50-80% confidence):

- Problem validated
- Solution hypothesis
- Will likely do next
- Might change based on learnings

**Later** (20-50% confidence):

- Interesting signal
- Early exploration
- Direction, not commitment
- Could change dramatically

---

## Example

```markdown
# Product Roadmap - Q2 2024

## Now

### SSO Integration (SAML/OAuth)

**Problem**: Enterprise customers can't buy without SSO ($2M pipeline blocked)
**Approach**: SAML 2.0 + OAuth 2.0 support, Google Workspace + Okta first
**Status**: In development (80% complete)
**Expected**: Next 2-3 weeks

### Export Performance Improvements

**Problem**: Large exports (>10K rows) time out, users frustrated
**Approach**: Background job processing + email when complete
**Status**: Testing
**Expected**: Next 3-4 weeks

---

## Next

### Theme: Mobile Experience

**Why**: 40% of users try mobile, 80% bounce (poor experience)
**Initiatives**:

- Mobile-optimized dashboard
- Offline sync for field workers
- Push notifications
  **Success Metrics**: Mobile MAU 2K → 5K, mobile NPS 30 → 50

### Theme: Analytics & Insights

**Why**: Users struggle to make data-driven decisions (top feature request)
**Initiatives**:

- Advanced filtering
- Custom dashboards
- Automated insights
  **Success Metrics**: 60% of users use weekly, NPS +10 points

---

## Later

### AI-Powered Features

**Exploration**: Smart recommendations, automated workflows, predictive analytics
**Why it matters**: Competitive differentiator, reduces manual work

### International Expansion

**Exploration**: Multi-currency, multi-language, regional compliance
**Why it matters**: Unlock $5M TAM in EU/APAC

---

## Not Doing

- **Native desktop apps**: Low demand (5% of requests), web works well
- **Social login (Facebook, Twitter)**: Security/privacy concerns, SSO is priority
- **Custom branding**: Nice-to-have, doesn't move core metrics
```

---

## Tips

**Keep "Now" specific**:

- Active work items
- Clear deliverables
- Near-term completion

**Keep "Next" flexible**:

- Themes, not features
- Validated problems
- Room to adjust approach

**Keep "Later" vague**:

- Directions, not commitments
- Low confidence
- Explore, don't promise

**Always show trade-offs**:

- What you're NOT doing
- Why (strategy, data, resources)
- Manages expectations

---

## Updating the Roadmap

**Move items forward**:

- Later → Next (when validated)
- Next → Now (when resourced)
- Now → Shipped (when complete)

**Add new items**:

- Start in Later (low confidence)
- Graduate to Next (when validated)
- Promote to Now (when prioritized)

**Remove items**:

- Explicitly call out in "Not Doing"
- Explain why (don't just disappear)

**Frequency**: Update monthly, communicate changes

---

**Key Principle**: Now-Next-Later is about focus and flexibility. "Now" is your commitment, "Next" is your direction, "Later" is your vision. Everything else is "Not Doing".
