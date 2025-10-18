---
name: Value Proposition Canvas
description: Interactive value proposition design tool based on Strategyzer framework
category: Strategy
model: haiku
---

# Value Proposition Canvas

Map customer jobs, pains, and gains to your product's value propositions using the Strategyzer Value Proposition Canvas framework.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Target customer segment**: Who are you creating value for?
- **Product or feature**: What are you offering?
- **Context** (optional): Industry, stage, competitive landscape

## Output

Value Proposition Canvas with two sides:

### Customer Profile (Right Side)

**Customer Jobs** - What are they trying to get done?
- Functional jobs (tasks to complete)
- Social jobs (how they want to be perceived)
- Emotional jobs (how they want to feel)

**Pains** - What frustrates them?
- Obstacles and challenges
- Risks and potential bad outcomes
- Barriers to getting jobs done

**Gains** - What do they desire?
- Desired outcomes and benefits
- Aspirations and wants
- Measures of success

### Value Map (Left Side)

**Products & Services** - What you offer
- Features and capabilities

**Pain Relievers** - How you address pains
- How you eliminate or reduce each pain
- Explicit pain-to-solution mapping

**Gain Creators** - How you create gains
- Benefits and positive outcomes you enable
- Explicit gain-to-benefit mapping

### Fit Analysis

**Pain-Reliever Fit**:
- Mapping: customer pains → your pain relievers
- Strength of fit: Strong / Medium / Weak for each
- Gaps: Pains not addressed

**Gain-Creator Fit**:
- Mapping: customer gains → your gain creators
- Strength of fit: Strong / Medium / Weak for each
- Gaps: Gains not created

**Overall Value Proposition Fit**:
- How well your value map addresses customer profile
- Unique value propositions (differentiation)
- Must-haves vs nice-to-haves
- Feature prioritization by customer value

## Example

```
/value-proposition-canvas Target: Small business owners managing inventory. Product: Cloud-based inventory management SaaS. Context: Competing vs spreadsheets and legacy desktop software.
```

## Tips

✅ **DO**: Focus on ONE customer segment at a time, be specific (not generic), rank items by customer importance, validate with real customer interviews, update regularly as you learn

❌ **DON'T**: Try to serve all segments at once, use vague statements, assume you know without customer research, create and forget (iterate constantly)

**Related**: `/tools/business-model-canvas`, `/tools/competitive-positioning`
