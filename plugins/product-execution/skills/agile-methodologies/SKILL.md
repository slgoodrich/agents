---
name: agile-methodologies
description: Master Scrum, Kanban, SAFe, Shape Up, and Scrumban frameworks. Use when implementing agile processes, optimizing team workflows, or choosing methodology.
---

# Agile Methodologies

## Overview

Comprehensive guide to modern agile frameworks including Scrum, Kanban, SAFe, Shape Up, Scrumban, and Dual-Track Agile.

## When to Use This Skill

- Choosing agile framework for team
- Implementing or improving agile practices
- Facilitating ceremonies
- Scaling agile across organization
- Adapting methodology to context

## Core Frameworks

### 1. Scrum

**Core Principles**:
- Fixed-length sprints (1-4 weeks, typically 2)
- Cross-functional teams (5-9 people)
- Iterative and incremental
- Empirical process (inspect & adapt)

**Roles**:
- **Product Owner**: Maximizes value, manages backlog
- **Scrum Master**: Facilitates, removes impediments
- **Development Team**: Self-organizing, cross-functional

**Artifacts**:
- **Product Backlog**: Ordered list of work
- **Sprint Backlog**: Sprint commitment
- **Increment**: Potentially shippable product

**Events**:
1. **Sprint Planning** (4-8 hours for 2-week sprint)
   - What: Select backlog items
   - How: Break into tasks
   - Output: Sprint goal and commitment

2. **Daily Scrum** (15 min)
   - What did I do yesterday?
   - What will I do today?
   - Any blockers?

3. **Sprint Review** (2-4 hours)
   - Demo increment
   - Gather feedback
   - Update product backlog

4. **Sprint Retrospective** (1.5-3 hours)
   - What went well?
   - What could improve?
   - Action items (max 3)

5. **Backlog Refinement** (ongoing, ~10% of sprint)
   - Groom upcoming stories
   - Estimate and clarify
   - Ensure readiness

**When to Use Scrum**:
- Predictable cadence needed
- Cross-functional team
- Regular stakeholder feedback
- Complex, evolving requirements

**Pros**: Structured, well-documented, scalable
**Cons**: Rigid, overhead for small teams

---

### 2. Kanban

**Core Principles**:
1. Visualize workflow
2. Limit work in progress (WIP)
3. Manage flow
4. Make policies explicit
5. Implement feedback loops
6. Improve collaboratively

**Key Practices**:
- **Kanban Board**: To Do → In Progress → Done
- **WIP Limits**: Max items in each column
- **Pull System**: Pull work when capacity available
- **Flow Metrics**: Cycle time, lead time, throughput

**Metrics**:
- **Lead Time**: Total time from request to delivery
- **Cycle Time**: Time in "In Progress"
- **Throughput**: Items completed per period
- **WIP**: Current work in progress

**Board Example**:
```
Backlog | Ready | In Progress | Review | Done
  (∞)   |  (8)  |     (3)     |  (2)   | (∞)
```

**When to Use Kanban**:
- Continuous flow preferred over sprints
- Varying work item sizes
- Support/ops work
- Mature team with stable process

**Pros**: Flexible, visual, minimal overhead
**Cons**: Less structure, requires discipline

---

### 3. Scrumban (Hybrid)

**Combines**:
- Scrum's ceremonies and roles
- Kanban's flow and visualization

**Typical Setup**:
- 2-week sprints (Scrum)
- Kanban board with WIP limits
- Sprint planning and retros
- Continuous flow within sprint

**When to Use**:
- Transitioning from Scrum to Kanban
- Want structure + flexibility
- Mix of project and BAU work

---

### 4. Shape Up (Basecamp)

**Cycle Structure**:
- **6-week cycles**: Longer than sprints
- **2-week cooldown**: Bug fixes, exploration
- **Betting table**: Leadership chooses pitches

**Process**:
1. **Shaping** (pre-work):
   - Problem definition
   - Solution sketching
   - Risk assessment
   - Appetite (time budget)

2. **Betting**:
   - Leadership reviews pitches
   - Small bets (1-2 people, 1-2 weeks)
   - Big bets (team, 6 weeks)
   - Circuit breaker (no extensions)

3. **Building**:
   - Team has full 6 weeks
   - Scope hammering (cut smartly)
   - Hill charts (track progress)

4. **Cooldown**:
   - Fix bugs
   - Explore new ideas
   - Technical debt

**Key Concepts**:
- **Appetite**: How much time willing to spend (not estimate)
- **Circuit Breaker**: No sprint extensions, ship or kill
- **Scope Hammering**: Cut scope to fit time
- **Hill Charts**: Show uncertainty → certainty

**When to Use Shape Up**:
- Experienced team
- OK with longer cycles
- Want to reduce micromanagement
- Leadership involved in prioritization

**Pros**: Reduces estimation waste, empowers teams
**Cons**: Requires maturity, 6 weeks risky for critical work

---

### 5. SAFe (Scaled Agile Framework)

**Levels**:
1. **Team**: Scrum/Kanban teams
2. **Program**: Agile Release Train (ART)
3. **Large Solution**: Multi-ART coordination
4. **Portfolio**: Strategy to execution

**Key Ceremonies**:
- **PI Planning** (Program Increment Planning):
  - Quarterly planning event (2 days)
  - All teams plan together
  - Dependency mapping
  - Objectives and commitments

- **Scrum of Scrums**: Cross-team sync
- **ART Sync**: Program-level sync
- **Inspect & Adapt**: PI retrospective

**When to Use SAFe**:
- Large organization (50+ people)
- Multiple teams, complex dependencies
- Need structure at scale

**Pros**: Scales agile, comprehensive
**Cons**: Heavy, bureaucratic, learning curve

---

### 6. Dual-Track Agile

**Two Parallel Tracks**:

**Discovery Track**:
- Validate problems and solutions
- User research and testing
- Prototyping
- Risk reduction

**Delivery Track**:
- Build validated features
- Ship to production
- Measure and iterate

**Process**:
```
Discovery → Validation → Delivery → Measurement
   ↓                          ↓
Research                   Build
Prototype                  Ship
Test                       Learn
   ↓                          ↓
   ← ← ← ← Feedback ← ← ← ←
```

**When to Use**:
- Product discovery important
- Reduce build waste
- Continuous learning culture

**Pros**: De-risks features, user-centric
**Cons**: Requires PM/design capacity

---

## Choosing Methodology

### Team Size

**Small (2-5)**: Kanban or Shape Up
**Medium (5-9)**: Scrum or Scrumban
**Large (10+)**: Scrum with scaling
**Enterprise (50+)**: SAFe or LeSS

### Work Type

**New Product**: Dual-Track + Scrum
**Established Product**: Kanban or Scrumban
**Support/Ops**: Kanban
**R&D/Innovation**: Shape Up

### Team Maturity

**New to Agile**: Scrum (structure helps)
**Experienced**: Kanban, Shape Up
**Scaling**: SAFe, LeSS, Nexus

### Organizational Culture

**Hierarchical**: SAFe
**Flat**: Kanban, Shape Up
**Startup**: Scrum, Dual-Track

---

## Best Practices

### 1. Start Simple
- Don't over-engineer process
- Add practices as needed
- Retrospect and adapt

### 2. Definition of Done (DoD)
```
Feature is Done when:
- [ ] Code written
- [ ] Peer reviewed
- [ ] Tests pass (unit, integration)
- [ ] Deployed to staging
- [ ] PM/Designer approved
- [ ] Documentation updated
- [ ] No critical bugs
```

### 3. Definition of Ready (DoR)
```
Story is Ready when:
- [ ] Clear acceptance criteria
- [ ] Sized (< 13 points)
- [ ] Dependencies identified
- [ ] Team understands it
- [ ] Mockups available (if UI)
- [ ] No blockers
```

### 4. Estimation Techniques

**Planning Poker**:
- Cards: 1, 2, 3, 5, 8, 13, 20, ?, ∞
- Everyone estimates simultaneously
- Discuss outliers
- Converge on estimate

**T-Shirt Sizing**: XS, S, M, L, XL
- Faster, less precise
- Good for high-level roadmap

**Story Points** (Fibonacci):
- Relative sizing
- 1 = trivial, 13 = max, >13 = break down

### 5. Velocity Tracking

**Calculate**:
- Sum points completed per sprint
- Average last 3-5 sprints
- Use for forecasting

**Forecast**:
```
Backlog: 100 points
Velocity: 20 points/sprint
Estimate: 5 sprints = 10 weeks
```

### 6. Burndown Charts

**Sprint Burndown**:
```
Points
  ↑
40│╲
30│ ╲___
20│     ╲___
10│         ╲___
 0│_______________╲_→
  0  2  4  6  8  10 Days
```

**Release Burndown**: Track progress to launch

---

## Common Pitfalls

###  Avoid

**Agile Theater**:
- Ceremonies without purpose
- Process over outcomes
- Cargo culting

**Micromanagement**:
- Trust the team
- Empower decisions
- Focus on outcomes

**No Retrospectives**:
- Continuous improvement essential
- Action items must be actioned
- Psychological safety required

**Ignoring Metrics**:
- Velocity trends
- Cycle time
- Quality metrics (bugs, tech debt)

###  Do

**Adapt to Context**:
- No one-size-fits-all
- Modify for your team
- Experiment and learn

**Focus on Value**:
- User outcomes > story points
- Business impact > velocity
- Learning > rigid process

**Build Psychological Safety**:
- Blameless retrospectives
- Celebrate failures as learning
- Encourage experimentation

---

## Resources

**Books**:
- "Scrum: The Art of Doing Twice the Work in Half the Time" - Jeff Sutherland
- "Kanban" - David J. Anderson
- "Shape Up" - Ryan Singer (free online)
- "User Story Mapping" - Jeff Patton

**Certifications**:
- Certified Scrum Product Owner (CSPO)
- Professional Scrum Master (PSM)
- SAFe certification

**Tools**:
- Jira, Linear, Azure DevOps
- Trello, Asana for Kanban
- Miro, FigJam for planning

---

## Quick Decision Guide

```
Need structure? → Scrum
Want flexibility? → Kanban
Hybrid approach? → Scrumban
Long cycles? → Shape Up
Scaling? → SAFe
Discovery-focused? → Dual-Track

Always: Retrospect, adapt, improve
```
