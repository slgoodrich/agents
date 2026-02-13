# Kano Model Template

## Kano Feature Categories

### Basic Needs (Must-Be Quality)

**Expected features** - Customers assume they exist, dissatisfied if absent

Examples:

- Login/authentication (any SaaS)
- Save functionality (any editor)
- Basic security (any app)

**Strategy**: Build all basic needs in V1 (table stakes)

### Performance Needs (One-Dimensional Quality)

**Linear satisfaction** - More is better, competitive differentiator

Examples:

- Speed/performance
- Number of integrations
- Storage capacity

**Strategy**: Competitive parity, then selective advantage

### Excitement Needs (Delighters)

**Unexpected joy** - Customers don't expect, thrilled when present

Examples:

- Dark mode (when first introduced)
- AI-powered features
- Delightful animations

**Strategy**: Strategic differentiation, create wow moments

### Indifferent

**Users don't care** - No impact whether present or absent

Examples:

- Features users don't need
- Over-engineering

**Strategy**: Don't build, focus elsewhere

### Reverse

**Users prefer without it** - Presence causes dissatisfaction

Examples:

- Forced tutorials
- Excessive notifications
- Clutter

**Strategy**: Remove or make optional

## Kano Survey Template

For each feature, ask two questions:

### Functional Question

"How would you feel if **[feature]** was **present**?"

Responses:

- [ ] I like it
- [ ] I expect it
- [ ] I'm neutral
- [ ] I can tolerate it
- [ ] I dislike it

### Dysfunctional Question

"How would you feel if **[feature]** was **absent**?"

Responses:

- [ ] I like it
- [ ] I expect it
- [ ] I'm neutral
- [ ] I can tolerate it
- [ ] I dislike it

## Kano Classification Matrix

```
              Functional (Feature Present)
              Like | Expect | Neutral | Tolerate | Dislike
Dysfunctional ────┼────────┼─────────┼──────────┼────────
(Absent)
Like          Q   │   E    │    E    │    E     │   P
Expect        R   │   I    │    I    │    I     │   M
Neutral       R   │   I    │    I    │    I     │   M
Tolerate      R   │   I    │    I    │    I     │   M
Dislike       R   │   R    │    R    │    R     │   Q

Legend:
E = Excitement (Delighter)
P = Performance (One-dimensional)
M = Must-be (Basic need)
I = Indifferent
R = Reverse
Q = Questionable (recheck responses)
```

## Feature Analysis Template

| Feature   | Functional Response | Dysfunctional Response | Category        | Priority |
| --------- | ------------------- | ---------------------- | --------------- | -------- |
| Feature A | Like                | Dislike                | Must-be (M)     | P0       |
| Feature B | Like                | Neutral                | Excitement (E)  | P1       |
| Feature C | Like                | Tolerate               | Performance (P) | P1       |
| Feature D | Neutral             | Neutral                | Indifferent (I) | Reject   |
| Feature E |                     |                        |                 |          |

## Example: Project Management Tool

### Survey Results

**Feature: Drag-and-Drop Task Prioritization**

Functional: "How would you feel if drag-and-drop was present?"

- 60% "I expect it"
- 30% "I like it"
- 10% "I'm neutral"

Dysfunctional: "How would you feel if drag-and-drop was absent?"

- 70% "I dislike it"
- 20% "I can tolerate it"
- 10% "I'm neutral"

**Classification**: Must-be (M) - Expected feature, users very dissatisfied without it

**Strategy**: Must build in V1 (table stakes)

---

**Feature: AI-Powered Task Suggestions**

Functional: "How would you feel if AI suggestions were present?"

- 80% "I like it"
- 15% "I'm neutral"
- 5% "I expect it"

Dysfunctional: "How would you feel if AI suggestions were absent?"

- 50% "I'm neutral"
- 30% "I can tolerate it"
- 20% "I like it" (prefer manual control)

**Classification**: Excitement (E) - Users love it when present, okay without

**Strategy**: Strategic differentiator for V1 (wow factor)

## Roadmap Strategy Using Kano

### Phase 1: Foundation (Must-Be Features)

Build all basic needs users expect

- User authentication
- Task creation/editing
- Project organization
- Drag-and-drop prioritization

**Goal**: Meet baseline expectations, no dissatisfaction

### Phase 2: Competitive (Performance Features)

Match or exceed competitors on key dimensions

- Faster load times (<1s)
- More integrations (top 10)
- Better mobile experience
- Advanced filtering

**Goal**: Competitive parity, selective advantage

### Phase 3: Differentiation (Excitement Features)

Create unexpected delight, stand out from competition

- AI-powered task suggestions
- Intelligent deadline predictions
- Proactive risk alerts
- Delightful animations

**Goal**: Wow users, word-of-mouth, differentiation

## Kano Lifecycle

Features move through categories over time:

```
Excitement → Performance → Basic Need

Example:
Dark mode was Excitement (2018) → Performance (2020) → Basic Need (2023)
```

**Implication**: Today's delighters become tomorrow's table stakes. Continuously innovate.

## Tips

- **Survey 20-30 users minimum** for reliable patterns
- **Segment by persona** - needs vary by user type
- **Consider lifecycle** - early adopters ≠ mainstream
- **Prioritize Must-Be first** - eliminate dissatisfaction
- **Differentiate with Excitement** - create wow moments
- **Don't over-build Indifferent** - users don't care, save effort
- **Remove Reverse features** - causing dissatisfaction

## When to Use Kano

- **Understanding user expectations** - What's table stakes vs delight?
- **Competitive analysis** - How to differentiate?
- **Roadmap sequencing** - Build Must-Be → Performance → Excitement
- **Feature validation** - Worth building?
- **Multi-release planning** - V1 vs V2 vs V3

## Next Steps

1. Identify 10-15 potential features
2. Create survey with functional + dysfunctional questions
3. Survey 20-30 target users
4. Classify each feature using Kano matrix
5. Prioritize: Must-Be (P0) → Performance (P1) → Excitement (P1-P2)
6. Build roadmap: V1 = Must-Be + key Excitement differentiator
7. Monitor feature lifecycle (Excitement → Performance → Must-Be over time)
