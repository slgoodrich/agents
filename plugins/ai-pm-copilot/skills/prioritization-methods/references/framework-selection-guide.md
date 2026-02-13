# Framework Selection Guide

## Table of Contents

- [Quick Decision Tree](#quick-decision-tree)
- [Framework Comparison](#framework-comparison)
- [Detailed Framework Selection](#detailed-framework-selection)
- [Combining Frameworks](#combining-frameworks)
- [Decision Factors](#decision-factors)
- [Common Mistakes](#common-mistakes)
- [Framework Evolution](#framework-evolution)
- [Getting Started](#getting-started)
- [Resources](#resources)

## Quick Decision Tree

```
START: What type of prioritization do you need?

├─ MVP Scoping (what's in/out)?
│  └─ MoSCoW Method

├─ Large Backlog Ranking (20+ items)?
│  ├─ Have user reach data? → RICE Scoring
│  └─ Limited data? → ICE Scoring

├─ Visual Presentation?
│  └─ Value vs Effort Matrix

├─ Understanding User Expectations?
│  └─ Kano Model

├─ Multiple Competing Priorities?
│  └─ Weighted Scoring

└─ Outcome-Driven Innovation (Jobs-to-be-Done)?
   └─ Opportunity Scoring
```

## Framework Comparison

| Framework        | Time to Setup | Data Required | Best For                   | Output               |
| ---------------- | ------------- | ------------- | -------------------------- | -------------------- |
| **RICE**         | Medium        | High          | Large backlog ranking      | Numerical scores     |
| **ICE**          | Low           | Low           | Quick experiments          | Numerical scores     |
| **Value/Effort** | Low           | Low           | Visual presentations       | 2×2 matrix           |
| **MoSCoW**       | Low           | Low           | MVP scoping                | Categories (M/S/C/W) |
| **Kano**         | High          | Medium        | Understanding expectations | Categories           |
| **Weighted**     | Medium        | Medium        | Custom criteria            | Weighted scores      |
| **Opportunity**  | High          | High          | Jobs-to-be-done            | Opportunity scores   |

## Detailed Framework Selection

### Use RICE When...

**Best For**:

- Large backlog (20+ features) needs ranking
- Post-PMF with user metrics
- Need defendable, data-driven priorities
- Data-driven team culture

**You Have**:

- User reach data (MAU, traffic, conversion rates)
- Confidence in impact estimates
- Effort estimation capability
- Quantitative mindset

**Strengths**:

- Objective, defensible
- Forces explicit estimation
- Scales well to large backlogs
- Prevents HiPPO prioritization

**Weaknesses**:

- Requires quantitative data
- Effort estimation can be inaccurate
- Doesn't capture strategic nuance

**Time Investment**: 1-2 hours for 20 features

---

### Use ICE When...

**Best For**:

- Growth experiments (A/B tests, optimizations)
- Early-stage products with limited data
- Quick prioritization (need decision fast)
- Startup/fast-moving environments

**You Have**:

- Limited quantitative data
- Need to move quickly
- Appetite for gut + logic scoring
- Iteration culture (test and learn)

**Strengths**:

- Simple, fast, intuitive
- Low overhead
- Good for experiments
- Easy to explain

**Weaknesses**:

- Subjective (harder to defend)
- No explicit reach component
- Can be gamed more easily

**Time Investment**: 30 minutes for 20 features

---

### Use Value/Effort Matrix When...

**Best For**:

- Visual presentations
- Portfolio planning (high-level view)
- Quick assessments
- Executive communication

**You Have**:

- Need to visualize tradeoffs
- Diverse audience
- Limited time for analysis
- Strategic planning sessions

**Strengths**:

- Visual, intuitive
- Fast to create
- Easy to explain
- Great for presentations

**Weaknesses**:

- Binary thinking (high/low only)
- Doesn't capture nuance
- Subjective value/effort
- No quantitative rigor

**Time Investment**: 30-45 minutes for 15 features

---

### Use MoSCoW When...

**Best For**:

- MVP scoping (ruthless cutting)
- Release planning (what's in this release?)
- Clarity (go/no-go decisions)
- Timeline pressure (fixed time, flex scope)

**You Have**:

- Clear definition of "done"
- Fixed timeline or budget
- Need to cut aggressively
- Priority negotiation needed

**Strengths**:

- Clear, binary decisions
- Forces hard choices
- Collaborative
- Simple categories

**Weaknesses**:

- No ranking within categories
- Requires facilitation
- Can be contentious
- Doesn't handle dependencies well

**Time Investment**: 1-2 hours (with the team)

---

### Use Kano Model When...

**Best For**:

- Understanding user expectations (table stakes vs delighters)
- Competitive analysis (how to differentiate?)
- Roadmap sequencing (V1 → V2 → V3)
- Multi-release planning

**You Have**:

- 20-30 users available for survey
- 2-3 weeks for research
- Strategic planning horizon
- Need to understand satisfaction drivers

**Strengths**:

- User-centric
- Reveals expectations
- Strategic insights
- Competitive positioning

**Weaknesses**:

- Time-intensive (surveys + analysis)
- Requires research skills
- Complex to explain
- Features move categories over time

**Time Investment**: 1-2 weeks (survey + analysis)

---

### Use Weighted Scoring When...

**Best For**:

- Multiple priorities to balance
- Complex decisions with many factors
- Executive alignment needed
- Custom criteria that standard frameworks don't capture

**You Have**:

- Multiple criteria to balance
- Complex evaluation criteria
- Need transparent decision-making
- Time to define and agree on weights

**Strengths**:

- Flexible, customizable
- Transparent criteria
- Balances multiple priorities
- Defensible with executives

**Weaknesses**:

- Setup overhead (define criteria, weights)
- Can be gamed
- Requires facilitation
- Weights can be contentious

**Time Investment**: 2-3 hours (setup + scoring)

---

### Use Opportunity Scoring When...

**Best For**:

- Jobs-to-be-done methodology
- Outcome-focused prioritization
- Innovation opportunities (underserved needs)
- Feature gap analysis

**You Have**:

- Customer jobs identified (outcomes, not features)
- 15-30 customers available for survey
- 2-3 weeks for research
- JTBD mindset and practice

**Strengths**:

- User outcome focus
- Reveals underserved needs
- Data-driven
- Differentiates importance from satisfaction

**Weaknesses**:

- Requires research (surveys)
- Learning curve (JTBD methodology)
- Time-intensive
- May miss emergent innovations

**Time Investment**: 1-2 weeks (survey + analysis)

---

## Combining Frameworks

### RICE + Value/Effort

- **Use RICE** for numerical ranking
- **Use Value/Effort** for visual presentation to the team
- Best of both: Rigor + Communication

### MoSCoW + RICE

- **Use MoSCoW** for release planning (what's in?)
- **Use RICE** within each category to rank
- Example: Rank all "Must Haves" by RICE to sequence

### Kano + ICE

- **Use Kano** for strategy (Must-Be vs Excitement)
- **Use ICE** for tactical execution within each category
- Strategic + Tactical prioritization

### Weighted + RICE

- **Use Weighted** to determine RICE component weights
- Example: Strategic Fit 40%, User Value 30%, etc.
- Custom RICE for your context

---

## Decision Factors

### By Product Stage

**Pre-PMF (Validation)**:

- Primary: ICE (fast iteration)
- Secondary: Opportunity Scoring (validate jobs)

**Early PMF (Growth)**:

- Primary: RICE (data emerging)
- Secondary: Value/Effort (clarity)

**Scale (Optimization)**:

- Primary: RICE (data-rich)
- Secondary: Kano (competitive positioning)

### By Team Size

**Solo / 1-3 people**:

- ICE or Value/Effort (speed over rigor)
- MoSCoW for MVP

**Small team (4-10)**:

- RICE or ICE
- MoSCoW for releases

**Medium+ team (10+)**:

- RICE (defensibility)
- Weighted Scoring (clarity)
- Kano (strategic planning)

### By Data Availability

**Rich data** (MAU, metrics, research):

- RICE
- Opportunity Scoring
- Kano

**Limited data** (early, pre-launch):

- ICE
- Value/Effort
- MoSCoW

### By Decision Type

**MVP Scoping**: MoSCoW
**Backlog Ranking**: RICE or ICE
**Visual Presentation**: Value/Effort
**Strategic Planning**: Kano
**Growth Experiments**: ICE
**Complex Tradeoffs**: Weighted Scoring

---

## Common Mistakes

### ❌ Using Wrong Framework for Context

- Using RICE without user data
- Using Kano for fast tactical decisions
- Using ICE for long-term strategic planning

### ✓ Match Framework to Need

- Data available? → RICE
- Need speed? → ICE
- Strategic? → Kano

---

### ❌ Combining Too Many Frameworks

- Using 3+ frameworks creates confusion
- Analysis paralysis

### ✓ Use 1-2 Frameworks Max

- Primary for ranking
- Secondary for visualization or validation

---

### ❌ Set and Forget

- Priorities static for quarters/years
- Ignoring new data

### ✓ Regular Re-Prioritization

- Monthly for tactical (ICE)
- Quarterly for strategic (RICE, Kano)
- Re-score as you learn

---

## Framework Evolution

Your prioritization needs change as your product matures:

**Stage 1: Idea → MVP**

- Use: MoSCoW, ICE
- Why: Speed, ruthless cutting

**Stage 2: MVP → PMF**

- Use: ICE, Opportunity Scoring
- Why: Fast learning, validate jobs

**Stage 3: PMF → Growth**

- Use: RICE, Value/Effort
- Why: Data emerging, scale backlog

**Stage 4: Scale → Maturity**

- Use: RICE, Kano, Weighted
- Why: Competitive, complex tradeoffs, strategic

---

## Getting Started

### First Time Prioritizing?

**Start with**: Value vs Effort Matrix

- Fastest to learn
- Visual and intuitive
- Good enough for most decisions

### Have 20+ Features to Rank?

**Upgrade to**: ICE or RICE

- ICE if limited data
- RICE if have user metrics

### Planning MVP?

**Use**: MoSCoW

- Forces ruthless cutting
- Clear go/no-go criteria

### Strategic Planning?

**Use**: Kano or Opportunity Scoring

- Understand expectations
- Find underserved needs

---

## Resources

**RICE**:

- "RICE: Simple prioritization for product managers" - Intercom
- Tool: Airtable, Notion, Productboard

**ICE**:

- "How to use ICE Scoring" - Sean Ellis
- Tool: Spreadsheet, Notion

**Kano**:

- "The Kano Model" - UX Magazine
- Tool: Typeform/Google Forms for surveys

**Opportunity Scoring**:

- "Jobs to be Done" - Anthony Ulwick
- Tool: Survey tool + spreadsheet

**Weighted Scoring**:

- "Prioritization Frameworks" - ProductPlan
- Tool: Spreadsheet, Aha!

---

**Key Principle**: Choose the framework that matches your context (stage, data, team, decision type). Don't over-analyze - pick one, use it consistently, iterate.
