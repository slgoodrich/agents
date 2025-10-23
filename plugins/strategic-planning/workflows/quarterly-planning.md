---
description: Comprehensive quarterly OKR and roadmap planning
category: Strategic Planning
duration: 4 weeks
model: sonnet
---

# Quarterly Planning Workflow

Comprehensive quarterly OKR and roadmap planning workflow.

## Usage
```
/quarterly-planning [quarter, e.g., "Q2 2025"]
```

**Context from command**: $ARGUMENTS

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- Which quarter (Q1 2025, Q2 2025, etc.)
- Current company/product state (ARR, users, team size)
- Previous quarter results (OKRs achieved, velocity, key learnings)
- Strategic priorities or themes for the quarter
- Team capacity and any known constraints
- Key stakeholders and decision-makers

## Timeline: 4 Weeks

## Workflow Phases

### Week 1: Strategic Context & OKR Draft

**Agents**: `product-strategist`, `user-researcher`, `growth-pm`

**Activities**:
1. **Review Last Quarter**
   - OKR achievement (scoring)
   - Wins and misses
   - Key learnings

2. **Strategic Assessment**
   - Market trends and competitive moves
   - User feedback themes
   - Business priorities

3. **Draft OKRs**
   - 3-5 Objectives (qualitative goals)
   - 3-5 Key Results per Objective (measurable)
   - Align to company OKRs
   - Ambitious but achievable (60-70% confidence)

**Deliverables**:
- Previous quarter retro
- Strategic context doc
- Draft OKRs

**Commands**:
```
Tell product-strategist: "Review Q1 performance and draft Q2 OKRs"
/strategic-planning:okr "Q2 2025"
```

---

### Week 2: Initiative Planning & Prioritization

**Agents**: `feature-prioritizer`, `requirements-engineer`

**Activities**:
1. **Identify Initiatives**
   - What must we build to hit OKRs?
   - Carryover from last quarter
   - New opportunities
   - Technical debt priorities

2. **RICE Scoring**
   - Score all initiatives
   - Rank by RICE
   - Map to OKRs

3. **Capacity Planning**
   - Team availability (PTO, hiring)
   - Velocity estimates
   - Buffer for unknowns (20%)

4. **Draft Roadmap**
   - Now (Month 1)
   - Next (Month 2)
   - Later (Month 3)

**Deliverables**:
- Initiative inventory (with RICE)
- Capacity model
- Draft roadmap

**Commands**:
```
Tell feature-prioritizer: "Score these 20 initiatives with RICE"
/strategic-planning:roadmap "Q2 2025"
```

---

### Week 3: Stakeholder Alignment & Refinement

**Agents**: `stakeholder-manager`, `gtm-planner`

**Activities**:
1. **Stakeholder Review**
   - Present OKRs and roadmap
   - Gather feedback
   - Address concerns
   - Negotiate trade-offs

2. **Cross-Functional Alignment**
   - Engineering: Capacity and feasibility
   - Design: Bandwidth and priorities
   - Marketing/GTM: Launch timing
   - Sales: Customer commitments
   - Data: Metrics and tracking

3. **Dependencies**
   - Map cross-team dependencies
   - Identify risks
   - Mitigation plans

4. **GTM Calendar**
   - Major launches
   - Beta programs
   - Events and deadlines

**Deliverables**:
- Stakeholder feedback incorporated
- Dependency map
- GTM calendar

**Commands**:
```
/stakeholder-management:stakeholder-map "Q2 Planning"
Tell gtm-planner: "Create Q2 launch calendar"
```

---

### Week 4: Finalization & Communication

**Agents**: `agile-coach`, `stakeholder-manager`

**Activities**:
1. **Finalize OKRs**
   - Incorporate feedback
   - Final scoring/targets
   - Ownership assignment

2. **Lock Roadmap**
   - Commit to Now items
   - Tentative Next/Later
   - Clear "Not This Quarter"

3. **Sprint 1 Planning**
   - Break Month 1 work into sprints
   - Story creation
   - Sprint goals

4. **Communication**
   - All-hands presentation
   - Team kickoff
   - Written plan (wiki/doc)
   - Individual goal-setting

**Deliverables**:
- Final OKRs
- Committed roadmap
- Sprint 1 plan
- Communication deck

**Commands**:
```
/agile-coaching:sprint-plan "Sprint 1 - Q2"
/strategic-planning:okr "Q2 2025" --final
Tell stakeholder-manager: "Create Q2 kickoff presentation"
```

---

## OKR Template

```markdown
# Q2 2025 OKRs: [Product/Team]

## Objective 1: [Inspiring Goal]
**Why**: [Strategic importance]

**Key Results**:
1. [Metric] from [X] to [Y] by June 30
2. [Achievement] completed by May 15
3. [Metric] reaches [Target]%

**Initiatives**:
- [Initiative 1]
- [Initiative 2]

**Owner**: [Name]
**Confidence**: Medium (65%)

---

## Objective 2: [Another Goal]
[Same structure]

---

## Alignment
- **Company OKR**: [How this connects]
- **Dependencies**: [Cross-team needs]
- **Resources**: [Team, budget]

## Success Metrics Dashboard
[Link to tracking]
```

---

## Roadmap Template

```markdown
# Q2 2025 Roadmap

## Vision
[Where we're headed long-term]

## Themes
1. **[Theme 1]**: [Focus area]
2. **[Theme 2]**: [Focus area]

## Now (April)
| Initiative | OKR | Owner | Status |
|------------|-----|-------|--------|
| [Init 1] | Obj 1, KR 2 | [Name] | Planning |
| [Init 2] | Obj 2, KR 1 | [Name] | In Progress |

## Next (May-June)
| Initiative | OKR | Owner | Confidence |
|------------|-----|-------|------------|
| [Init 3] | Obj 1, KR 3 | [Name] | High |

## Later (Exploration)
- [Future idea 1]
- [Future idea 2]

## Not This Quarter
- [Deprioritized item] - Why: [Reason]
```

---

## Success Criteria

✅ OKRs are ambitious (60-70% confidence)
✅ OKRs align to company goals
✅ Roadmap is achievable with current capacity
✅ Stakeholders aligned
✅ Dependencies mapped
✅ Metrics tracking ready
✅ Team understands plan

---

## Common Pitfalls

❌ **Too many OKRs**: Stick to 3-5 objectives max
❌ **Sandbagging**: Make them ambitious (70% = success)
❌ **No alignment**: Must tie to company OKRs
❌ **Vague key results**: Must be measurable
❌ **Over-committing**: Leave 20% buffer
❌ **Skipping stakeholders**: Alignment is critical

---

## Timeline

**Week 1**: Draft OKRs and assess context
**Week 2**: Prioritize initiatives and build roadmap
**Week 3**: Stakeholder alignment and refinement
**Week 4**: Finalize and communicate

**Total**: 4 weeks before quarter starts (ideally last month of previous quarter)

---

## Related Workflows

- `feature-lifecycle` - Execute roadmap items
- `product-launch` - Major launches this quarter
- `discovery-sprint` - Validate new ideas

---

**Model**: Sonnet
