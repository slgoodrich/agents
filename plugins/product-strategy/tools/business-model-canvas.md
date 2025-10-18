---
name: Business Model Canvas
description: Design and analyze business models using the Osterwalder Business Model Canvas
category: Strategy
model: haiku
---

# Business Model Canvas

Create or analyze a business model using the Business Model Canvas framework by Alexander Osterwalder.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Product/Company**: What business model are you designing?
- **Context**: Stage (idea, startup, scaling, pivot), industry, market
- **Existing information**: What you know about each block (optional)

## Output

Business Model Canvas with 9 building blocks:

### Right Side (Customer-Facing)

**1. Customer Segments** - Who are we creating value for?
- Target customer groups, segment characteristics, prioritization, niche vs mass market, multi-sided platform considerations

**2. Value Propositions** - What value do we deliver?
- Solutions to problems, benefits provided, product/service bundle, quantitative value (price, speed), qualitative value (design, experience), jobs-to-be-done fulfilled

**3. Channels** - How do we reach customers?
- Awareness (how they learn), evaluation (how they assess), purchase (how they buy), delivery (how you deliver), after-sales (post-purchase support), own vs partner channels, integration

**4. Customer Relationships** - What relationship does each segment expect?
- Personal assistance, self-service, automated services, communities, co-creation, acquisition/retention/expansion strategies

**5. Revenue Streams** - For what value are customers willing to pay?
- Pricing models (subscription, usage, freemium, etc.), revenue sources, pricing mechanisms, payment methods, recurring vs one-time

### Left Side (Business Infrastructure)

**6. Key Resources** - What assets are required?
- Physical resources, intellectual property, human resources, financial resources, own vs lease vs partner

**7. Key Activities** - What do we need to do?
- Production and delivery, problem-solving activities, platform/network activities, core competencies, activities to create/deliver value

**8. Key Partnerships** - Who are our partners and suppliers?
- Strategic alliances, joint ventures, supplier relationships, motivations (optimization, risk reduction, resource acquisition)

**9. Cost Structure** - What are the most important costs?
- Cost-driven vs value-driven, fixed vs variable costs, economies of scale and scope, key cost drivers, cost allocation by block

### Analysis

**Coherence Check**:
- Do all blocks work together logically?
- Alignment: value props ↔ customer segments, channels ↔ segments, resources ↔ activities
- Sustainable: cost structure vs revenues

**Strengths & Risks**:
- Business model strengths, competitive advantages, key risks/dependencies, assumptions to validate

**Innovation Opportunities**:
- Untapped segments, new revenue streams, channel innovations, partnership opportunities, cost optimization

## Example

```
/business-model-canvas B2B SaaS project management tool. Context: Early-stage startup, targeting SMBs, competing with Asana/Monday.com. Freemium model, self-service onboarding, 5-person team.
```

## Variants

- **Lean Canvas** (Ash Maurya): Substitutes Problem, Solution, Key Metrics, Unfair Advantage - better for startups
- **Mission Model Canvas**: For non-profits and social enterprises

## Tips

✅ **DO**: Start with customer segments + value props, iterate (never "done"), validate assumptions with customers, use for team workshops, compare to competitors, update as business evolves

❌ **DON'T**: Try to be perfect on first pass, work in isolation, ignore interdependencies (each change affects other blocks), treat as static document

**Related**: `/tools/value-proposition-canvas`, `/tools/swot-analysis`
