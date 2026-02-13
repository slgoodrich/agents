# MoSCoW Prioritization Template

## Categories

- **M** = Must Have (critical for launch, non-negotiable)
- **S** = Should Have (important but not critical)
- **C** = Could Have (nice-to-have, if time permits)
- **W** = Won't Have (out of scope this release)

## Target Distribution

- **60%** Must Have (M)
- **20%** Should Have (S)
- **20%** Could Have (C)
- **0%** Won't Have (explicit de-prioritization)

## Prioritization Template

### Must Have (60% of capacity)

Critical requirements without which the product cannot launch:

1. [ ] **User Authentication**
   - Why: Can't have product without secure login
   - Impact: Blocks all user-specific features

2. [ ] **Core Workflow (Feature Name)**
   - Why: The primary job-to-be-done
   - Impact: No core value without this

3. [ ] **Data Persistence**
   - Why: Users must save their work
   - Impact: Unusable without data storage

4. [ ]

5. [ ]

### Should Have (20% of capacity)

Important features that significantly enhance value but aren't deal-breakers:

1. [ ] **Email Notifications**
   - Why: Drives re-engagement
   - Impact: Lower retention without it, but product still usable

2. [ ] **Export Functionality**
   - Why: Users want data portability
   - Impact: Frustrating without, but workarounds exist

3. [ ]

4. [ ]

### Could Have (20% of capacity)

Nice-to-have features that improve experience but can wait:

1. [ ] **Dark Mode**
   - Why: User preference feature
   - Impact: Delight factor, not necessity

2. [ ] **Keyboard Shortcuts**
   - Why: Power user efficiency
   - Impact: Nice polish, not required

3. [ ]

4. [ ]

### Won't Have (This Release)

Explicitly out of scope for this release (but may be future releases):

1. **Mobile App**
   - Why: Desktop-first strategy
   - Future: Consider for V2 after PMF

2. **Advanced Analytics**
   - Why: Users need core product first
   - Future: Add based on user demand

3. **Team Collaboration**
   - Why: Focusing on solo use case
   - Future: Expansion opportunity

4.

5.

## MoSCoW Decision Criteria

### Must Have Test

Ask: "Can we launch without this?"

- If **NO** → Must Have
- If **YES** → Not a Must Have

### Should Have Test

Ask: "Would absence significantly damage value?"

- If **YES** → Should Have
- If **NO** → Could Have or Won't Have

### Could Have Test

Ask: "Would this be nice to have but not necessary?"

- If **YES** → Could Have
- If **NO** → Won't Have

### Won't Have

Ask: "Is this out of scope or should we defer?"

- If **YES** → Won't Have (document why)

## Example: MVP Feature Set

**Product: AI-Powered PM Tool for Solo Developers**

### Must Have (60%)

- [ ] User account and authentication
- [ ] AI-powered PRD generation from ideas
- [ ] User story breakdown with acceptance criteria
- [ ] MVP scope recommendation (3-5 features)
- [ ] Basic export (Markdown)

### Should Have (20%)

- [ ] GitHub issue sync
- [ ] Notion export integration
- [ ] Interview guide generation
- [ ] Research synthesis

### Could Have (20%)

- [ ] Roadmap builder (Now-Next-Later)
- [ ] Goal tracking
- [ ] Dark mode
- [ ] Keyboard shortcuts

### Won't Have (V1)

- Mobile app (desktop-first)
- Team collaboration (solo-first)
- Advanced analytics
- AI model selection
- White-label options

## Tips

- **Negotiate aggressively** - If everything is "Must Have", nothing is prioritized
- **Use 60/20/20 rule** - Forces hard choices, prevents scope creep
- **Document rationale** - Explain "why" for each category
- **Clarity** - Get agreement on Must Haves before building
- **Timebox releases** - Lock Must Haves, flex Could Haves based on time
- **Re-evaluate** - MoSCoW can change between releases as strategy evolves

## When to Use MoSCoW

- **MVP scoping** - Ruthlessly cut to minimum viable
- **Release planning** - What's in this release vs next?
- **Clarity** - Get agreement on priorities
- **Timeline pressure** - When time is fixed, scope flexes
- **Go/no-go decisions** - Clear launch criteria

## Common Mistakes

❌ **Everything is Must Have** - Defeats the purpose, causes scope creep
✓ **Force 60/20/20 distribution** - Hard choices = real prioritization

❌ **Vague criteria** - "Important" isn't a Must Have
✓ **Clear rationale** - Why can't we launch without it?

❌ **No Won't Have list** - Implicit scope creep
✓ **Explicit Won't Haves** - Clear boundaries, documented

## Next Steps

1. List all proposed features/requirements
2. Apply Must Have test to each
3. Categorize into M/S/C/W
4. Check distribution (target 60/20/20)
5. Negotiate until distribution achieved
6. Get decision checkpoint on Must Haves
7. Build Must Haves first, then Shoulds, then Coulds
8. Document Won't Haves to prevent feature creep
