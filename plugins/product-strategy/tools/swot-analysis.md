---
name: SWOT Analysis
description: Strategic planning tool analyzing Strengths, Weaknesses, Opportunities, and Threats
category: Strategy
model: haiku
---

# SWOT Analysis

Comprehensive SWOT (Strengths, Weaknesses, Opportunities, Threats) analysis for strategic planning and decision-making.

## Usage

**Context from command**: $ARGUMENTS

**Model Override**: Use `--model sonnet` for higher quality analysis (default: varies by tool).

If $ARGUMENTS is provided, use it as starting context. Otherwise, gather:
- **Subject**: What are you analyzing? (product, company, feature, initiative, market entry)
- **Context**: Current situation, goals, market position
- **Timeframe**: Current state, or looking ahead X months/years
- **Scope**: Specific focus areas (optional)

## Output

SWOT analysis with four quadrants and strategic actions:

### Internal Factors

**Strengths** (Positive, Internal):
- Unique capabilities, strong assets/resources, competitive advantages, what you do better, positive brand attributes, IP, team expertise, technology/infrastructure, customer relationships, financial position

**Weaknesses** (Negative, Internal):
- Limitations/gaps, resource constraints, competitive disadvantages, what others do better, skills/capability gaps, weak brand elements, technical debt, process inefficiencies, geographic limitations, financial constraints

### External Factors

**Opportunities** (Positive, External):
- Market growth/trends, emerging customer needs, technology advances, favorable regulatory changes, competitive gaps, partnership possibilities, market expansion (geographic/segment), customer segment growth, favorable economic conditions, social/cultural trends

**Threats** (Negative, External):
- Market decline/saturation, emerging competitors, disruptive technologies, unfavorable regulatory changes, economic downturn, changing customer preferences, supply chain vulnerabilities, dependency risks, price pressure, talent competition

### SWOT Strategy Matrix

| Strategy Type | How to Execute |
|---------------|----------------|
| **SO** (Strengths + Opportunities) | Use strengths to capitalize on opportunities: growth strategies, market expansion, product development, competitive positioning |
| **WO** (Weaknesses + Opportunities) | Overcome weaknesses to pursue opportunities: improvement initiatives, capability building, partnerships/acquisitions, resource investments |
| **ST** (Strengths + Threats) | Use strengths to mitigate threats: defensive strategies, differentiation, customer retention, market protection |
| **WT** (Weaknesses + Threats) | Minimize weaknesses and avoid threats: damage control, risk mitigation, contingency plans, strategic pivots/exits |

### Prioritization

**Critical Items** (Top 3 each):
- Most important strengths to leverage: [1, 2, 3]
- Most critical weaknesses to address: [1, 2, 3]
- Highest potential opportunities: [1, 2, 3]
- Most dangerous threats: [1, 2, 3]

**Action Plan**:
- Immediate (0-3mo): [Actions]
- Short-term (3-6mo): [Initiatives]
- Long-term (6-12+mo): [Strategies]

## Example

```
/swot-analysis Launching our PM SaaS in enterprise market. Context: Currently successful SMB market, looking to move upmarket. Timeframe: Next 12 months.
```

## Tips

✅ **DO**: Be specific (use data, quantify), be honest (acknowledge weaknesses, don't downplay threats), be actionable (inform decisions), get diverse input (cross-functional perspectives), prioritize (top items), link to actions

❌ **DON'T**: Make lists too long, confuse internal/external factors, be vague/general, use wishful thinking vs realistic assessment, list without actions, treat as one-time exercise, ignore interdependencies

**Variations**: TOWS Matrix (reverse order), SOAR (Strengths, Opportunities, Aspirations, Results), PEST/PESTLE (Political, Economic, Social, Technological, Legal, Environmental)

**Related**: `/tools/competitive-positioning`, `/tools/assumption-mapping`

**Next Steps**: Prioritize → Strategize (use SWOT matrix) → Plan (create actions) → Execute → Monitor → Update (quarterly or when major changes)
