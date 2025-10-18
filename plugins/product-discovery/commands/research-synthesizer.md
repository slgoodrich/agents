# Research Synthesizer

Analyze and synthesize user research from multiple sources into actionable insights, themes, and recommendations.

## Usage

```
/pm:research-synthesize [study name or research data] [optional: method, participants]
```

## What This Command Does

1. Transforms raw research data (interviews, surveys, usability tests) into structured insights
2. Identifies recurring themes, patterns, and user pain points across participants
3. Synthesizes findings with supporting evidence (quotes, observations, data)
4. Maps opportunities from research insights to product improvements
5. Prioritizes recommendations by impact and feasibility
6. Takes 1 hour vs 3-4 hours of manual research synthesis

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Research Context**:
- What research did you conduct? (interviews, surveys, usability tests, field studies)
- How many participants? (sample size)
- When was research conducted? (dates, duration)
- What were the research objectives? (what you wanted to learn)
- What product/feature was being researched?

**Participant Information**:
- Who participated? (demographics, roles, segments)
- How were they recruited? (screening criteria)
- Are they existing users or prospects?
- Any notable participant characteristics?

**Data Available**:
- What format is the research data? (transcripts, notes, recordings, survey responses)
- How much data? (number of interviews, survey responses, test sessions)
- Is it qualitative, quantitative, or mixed?
- Any existing analysis or preliminary findings?

**Synthesis Goals**:
- What decisions does this research need to inform?
- Who is the audience for this synthesis? (exec team, eng team, designers)
- What level of detail do you need? (executive summary vs deep dive)
- Any specific themes or questions to focus on?

**Example Input**:
```
Research: 15 user interviews about checkout flow
Dates: Jan 10-15, 2025
Participants: Current customers who abandoned cart in last 30 days
Method: 30-min remote interviews via Zoom
Objective: Understand why users abandon checkout
Data: Transcripts from 15 interviews (150 pages)
Audience: Product team, exec team
Goal: Identify top 3 issues to fix in Q1
```

### 2. Analyze Research Data

**Analysis Process**:
- Read/review all data at least once (get full picture)
- Tag/code themes as they emerge (don't force pre-defined categories)
- Count frequency of mentions (how many participants mentioned each theme)
- Assess severity (how much pain does this cause users)
- Look for contradictions or outliers (what doesn't fit the pattern)
- Identify surprising findings (what was unexpected)

**Theme Identification**:
- **Recurring Themes**: Mentioned by 30%+ of participants
- **Strong Themes**: Mentioned by 50%+ of participants
- **Universal Themes**: Mentioned by 80%+ of participants

### 3. Synthesize Findings

**Key Findings Structure** (3-5 findings):
1. **Insight**: What did we learn?
2. **Evidence**: Quotes, observations, data supporting the insight
3. **Impact**: What does this mean for the product?
4. **Opportunity**: What could we build or improve?

**Supporting Evidence**:
- Direct quotes from participants (anonymized)
- Behavioral observations (what users did, not just said)
- Quantitative data (percentages, counts, ratings)

### 4. Map Opportunities

**Opportunity Mapping**:
- Connect user needs to potential solutions
- Prioritize by impact (how many users affected) and feasibility (effort to implement)
- Categorize as immediate fixes, short-term features, long-term strategy

### 5. Create Recommendations

**Recommendation Tiers**:
- **Immediate** (This sprint): Quick fixes, low-hanging fruit
- **Short-term** (Next quarter): Features addressing main pain points
- **Long-term** (6-12 months): Strategic initiatives, platform changes

## Template

```markdown
# Research Synthesis: [Study Name]

**Study Date**: [YYYY-MM-DD to YYYY-MM-DD]
**Synthesized By**: [Your Name]
**Date**: [YYYY-MM-DD]

---

## Executive Summary

**Research Question**: [What we wanted to learn]

**Key Insight**: [One-sentence main finding - most important takeaway]

**Primary Recommendation**: [Top action to take based on research]

**Impact**: [Expected business/user impact if recommendations implemented]

---

## Study Overview

### Research Design

**Method**: [User Interviews | Surveys | Usability Testing | Field Study | Diary Study | Card Sorting | etc.]

**Objectives**:
1. [Research objective 1 - what we wanted to learn]
2. [Research objective 2]
3. [Research objective 3]

**Dates**: [Start Date] to [End Date] ([X] days)

**Moderators/Researchers**: [Names and roles]

---

### Participants

**Sample Size**: [N] participants

**Recruitment Criteria**:
- [Criterion 1 - e.g., "Active users in last 30 days"]
- [Criterion 2 - e.g., "Made at least 3 purchases"]
- [Criterion 3 - e.g., "Ages 25-45"]

**Demographics**:
- **Age**: [Distribution or range]
- **Gender**: [Distribution if relevant]
- **Location**: [Geographic distribution]
- **Role/Segment**: [User types represented]

**User Experience Level**:
- New users: [X]
- Intermediate: [Y]
- Power users: [Z]

---

### Methodology

**Session Structure**:
- Duration: [X] minutes per session
- Format: [Remote/In-person, 1:1/Group]
- Compensation: [Incentive provided, if any]

**Data Collection**:
- [Recordings/Transcripts/Notes]
- [Screen recordings if applicable]
- [Survey responses if quantitative]

**Analysis Method**:
- Thematic analysis (coded [X] themes)
- Affinity mapping
- [Other methods used]

---

## Key Findings

### Finding 1: [Descriptive Theme Title]

**Insight**: [What we learned - 1-2 sentences]

**Frequency**: [X/Y] participants ([Z]%) mentioned this theme

**Severity**: 🔴 High | 🟡 Medium | 🟢 Low

**Evidence**:

**Quotes**:
> "Direct quote from participant that illustrates this finding"
> — Participant 3, [Role/Segment]

> "Another supporting quote"
> — Participant 7, [Role/Segment]

> "Third quote if relevant"
> — Participant 12, [Role/Segment]

**Observations**:
- [Behavioral pattern observed - e.g., "All participants hesitated before clicking submit"]
- [Another observation - e.g., "Users repeatedly went back to previous screen"]

**Quantitative Data** (if available):
- [X]% of participants experienced [issue]
- Average time spent: [Y] minutes (vs expected [Z] minutes)
- [Metric]: [Value]

**Impact on User Experience**:
[How this finding affects users - frustration, confusion, abandonment, delight, etc.]

**Impact on Business**:
[How this finding affects business goals - conversion, retention, support costs, etc.]

**Opportunity**:
[What we could build or improve to address this finding]

**Priority**: 🔴 High | 🟡 Medium | 🟢 Low

**Recommendation**: [Specific action to take]

---

### Finding 2: [Theme Title]

**Insight**: [What we learned]

**Frequency**: [X/Y] participants ([Z]%)

**Severity**: 🔴 High | 🟡 Medium | 🟢 Low

[Repeat structure from Finding 1]

---

### Finding 3: [Theme Title]

[Repeat structure]

---

### Finding 4: [Theme Title]

[Repeat structure]

---

### Finding 5: [Theme Title]

[Repeat structure]

---

## Themes & Patterns

**All Themes Identified** (ranked by frequency and severity):

| Rank | Theme | Frequency | Severity | Impact | Representative Quote |
|------|-------|-----------|----------|--------|---------------------|
| 1 | [Theme 1] | 13/15 (87%) | 🔴 High | High | "[Quote]" |
| 2 | [Theme 2] | 11/15 (73%) | 🔴 High | Medium | "[Quote]" |
| 3 | [Theme 3] | 9/15 (60%) | 🟡 Medium | High | "[Quote]" |
| 4 | [Theme 4] | 7/15 (47%) | 🟡 Medium | Medium | "[Quote]" |
| 5 | [Theme 5] | 4/15 (27%) | 🟢 Low | Low | "[Quote]" |

---

## Pain Points

**Critical Pain Points** (Must address):
1. **[Pain Point 1]**: [Description - what users struggle with]
   - **Impact**: [How it affects users and business]
   - **Frequency**: [How often encountered]
   - **Current Workaround**: [How users cope today, if at all]

2. **[Pain Point 2]**: [Description]
   - **Impact**: [Impact]
   - **Frequency**: [Frequency]
   - **Current Workaround**: [Workaround]

**Moderate Pain Points** (Should address):
3. [Pain Point 3]
4. [Pain Point 4]

**Minor Pain Points** (Nice to address):
5. [Pain Point 5]
6. [Pain Point 6]

---

## User Needs & Jobs to Be Done

**Primary Jobs to Be Done**:
1. **[Job 1]**: [What users are trying to accomplish]
   - **Functional Need**: [What they need to do]
   - **Emotional Need**: [How they want to feel]
   - **Social Need**: [How they want to be perceived]
   - **Current Solution**: [How they do it today]
   - **Desired Outcome**: [What success looks like]

2. **[Job 2]**: [What users are trying to accomplish]
   [Repeat structure]

**Prioritized Needs**:

**Must-Have** (Dealbreakers if missing):
- **[Need 1]**: [Why critical - e.g., "Users cannot complete core task without this"]
- **[Need 2]**: [Why critical]

**Important** (Strongly desired):
- **[Need 3]**: [Value - e.g., "Saves significant time"]
- **[Need 4]**: [Value]

**Nice-to-Have** (Future enhancements):
- **[Need 5]**: [Why nice but not essential]
- **[Need 6]**: [Why nice but not essential]

---

## User Behaviors & Mental Models

**Behavioral Patterns Observed**:
1. **[Behavior 1]**: [Description of what users do]
   - **Why**: [Underlying motivation or need]
   - **Implication**: [What this means for product design]

2. **[Behavior 2]**: [Description]
   [Repeat]

**Mental Models**:
- **How users think about [concept]**: [Description of user mental model]
- **Gap between mental model and actual system**: [Where product doesn't match expectations]
- **Design implication**: [How we should design to match mental models]

**User Workflows**:
[Description of how users actually use the product, not how we designed it to be used]

---

## Surprising Findings

**Unexpected Insights**:
1. **[Surprise 1]**: [What we didn't expect to find]
   - **Why surprising**: [What we expected vs what we found]
   - **Evidence**: [Supporting data]
   - **Implication**: [What this changes about our assumptions]

2. **[Surprise 2]**: [Unexpected finding]
   [Repeat]

**Contradictions**:
- **[Contradiction]**: [What some users said vs what others said]
  - **Why**: [Possible explanation for difference]
  - **Implication**: [How to handle this in product]

**Hypotheses Validated**:
- ✅ [Hypothesis 1]: Confirmed - [Evidence]
- ✅ [Hypothesis 2]: Confirmed - [Evidence]

**Hypotheses Invalidated**:
- ❌ [Hypothesis 3]: Rejected - [Evidence showing opposite]
- ❌ [Hypothesis 4]: Rejected - [Evidence]

---

## Opportunity Map

**Core Problems Identified**:

### Problem 1: [Core user problem]

**Opportunities to Address**:
```
Problem: [User need or pain point]
├── Opportunity 1: [Immediate fix - low effort, medium impact]
│   └── Action: [What to build]
├── Opportunity 2: [Feature improvement - medium effort, high impact]
│   └── Action: [What to build]
└── Opportunity 3: [Strategic initiative - high effort, high impact]
    └── Action: [What to build]
```

**Priority**: 🔴 High | 🟡 Medium | 🟢 Low

---

### Problem 2: [Core user problem]

[Repeat structure]

---

## Impact-Feasibility Matrix

**Prioritization of Opportunities**:

```
        HIGH IMPACT
             │
        ┌────┼────────────┐
        │  🌟 QUICK WINS  │
    L   │  [Opp 1]        │
    O   ├─────────────────┤
    W   │   FILL-INS      │
        │  [Opp 5]        │
    E   ├─────────────────┤
    F   │   THANKLESS     │
    F   │   TASKS         │
    O   │  [Opp 7]        │
    R   ├─────────────────┤
    T   │  🎯 BIG BETS    │
        │  [Opp 2]        │
    H   │  [Opp 3]        │
    I   └────┼────────────┘
    G        │
    H     LOW IMPACT
```

**🌟 Quick Wins** (Low Effort, High Impact - DO FIRST):
1. [Opportunity 1]
2. [Opportunity 4]

**🎯 Big Bets** (High Effort, High Impact - STRATEGIC):
1. [Opportunity 2]
2. [Opportunity 3]

**Fill-Ins** (Low Effort, Low Impact - NICE TO HAVE):
1. [Opportunity 5]

**Thankless Tasks** (High Effort, Low Impact - AVOID):
1. [Opportunity 7] - Consider dropping

---

## Recommendations

### Immediate Actions (This Sprint)

**Quick Fixes Based on Research**:
1. **[Fix 1]**: [Specific action - e.g., "Change button label from 'Submit' to 'Complete Purchase'"]
   - **Why**: [Research insight supporting this]
   - **Effort**: [X] hours/days
   - **Expected Impact**: [Metric improvement expected]
   - **Owner**: [Team/Person]

2. **[Fix 2]**: [Specific action]
   [Repeat]

**Total Effort**: [X] days
**Expected Impact**: [Aggregate impact on key metrics]

---

### Short-Term (Next Quarter)

**Features to Address Main Pain Points**:
1. **[Feature 1]**: [Description of feature to build]
   - **Addresses**: [Which finding/pain point]
   - **User Story**: As a [user], I want to [action] so that [benefit]
   - **Success Metric**: [How to measure success]
   - **Effort Estimate**: [X] story points or weeks
   - **Priority**: P0 | P1 | P2

2. **[Feature 2]**: [Description]
   [Repeat]

**Process Improvements**:
1. **[Improvement 1]**: [Non-product change - e.g., "Update onboarding emails"]
   [Details]

---

### Long-Term (6-12 Months)

**Strategic Initiatives**:
1. **[Initiative 1]**: [Major product/platform change]
   - **Vision**: [What this enables]
   - **Rationale**: [Why this research supports this direction]
   - **Dependencies**: [What needs to happen first]
   - **Effort**: [Quarters or months]

2. **[Initiative 2]**: [Initiative]
   [Repeat]

---

## Segmentation Insights

**Differences by Segment**:

### Segment 1: [User Type/Persona]
- **Unique Needs**: [What this segment needs differently]
- **Pain Points**: [Specific to this segment]
- **Opportunities**: [Tailored solutions]

### Segment 2: [User Type/Persona]
- **Unique Needs**: [Different needs]
- **Pain Points**: [Different pains]
- **Opportunities**: [Segment-specific solutions]

**Implication**: [Whether we need different experiences for different segments]

---

## What We Still Don't Know

**Open Questions**:
1. [Question 1 - something research didn't answer]
   - **Why it matters**: [Impact on decisions]
   - **How to answer**: [Suggested follow-up research]

2. [Question 2]
   [Repeat]

**Assumptions to Validate**:
- [Assumption 1 - something we're assuming but haven't proven]
- [Assumption 2]

---

## Follow-Up Research Needed

**Recommended Next Steps**:
1. **[Research Type]**: [What to study next]
   - **Objective**: [What we'd learn]
   - **Method**: [How to research it]
   - **Timeline**: [When to conduct]
   - **Priority**: 🔴 High | 🟡 Medium | 🟢 Low

2. **[Research Type]**: [Study]
   [Repeat]

---

## Appendix

### Raw Data Summary
- **Interview Transcripts**: [Link or location]
- **Survey Responses**: [Link]
- **Recordings**: [Link]
- **Photos/Screenshots**: [Link]

### Participant Details
[Anonymized participant list with demographics if needed]

### Research Materials Used
- Interview guide: [Link]
- Survey questions: [Link]
- Prototype tested: [Link]

---

## Distribution & Next Steps

**Shared With**:
- [Executive team - Date shared]
- [Product team - Date shared]
- [Engineering team - Date shared]

**Decisions Made**:
- [Decision 1 based on this research]
- [Decision 2]

**Action Items**:
- [ ] [Person] to create PRD for [Feature] by [Date]
- [ ] [Person] to prototype [Solution] by [Date]
- [ ] [Person] to schedule follow-up research by [Date]

**Review Date**: [When to revisit these insights - e.g., after implementing recommendations]

```

---

## Best Practices

### DO ✅

- **Read all data before coding** - Get full picture before tagging themes
- **Use participant quotes** - Direct quotes are powerful evidence
- **Count frequency** - How many participants mentioned each theme matters
- **Assess severity** - Some themes are more painful than others
- **Look for patterns** - What do multiple participants have in common?
- **Include contradictions** - Don't ignore data that doesn't fit the pattern
- **Prioritize ruthlessly** - Focus on top 3-5 findings, not all 20 themes
- **Connect to product** - Every finding should have a "so what" implication
- **Make it actionable** - Insights without recommendations are useless

### DON'T ❌

- **Don't cherry-pick quotes** - Use representative quotes, not just ones that support your bias
- **Don't over-interpret small samples** - 2/15 participants mentioning something isn't a pattern
- **Don't ignore quantitative data** - Numbers add credibility to qualitative insights
- **Don't force pre-defined categories** - Let themes emerge from data
- **Don't synthesize alone** - Involve teammates to reduce individual bias
- **Don't skip the "why"** - Understanding root cause is more valuable than surface symptoms
- **Don't create 20 recommendations** - Too many actions = no action, prioritize top 3-5
- **Don't forget the user voice** - Synthesis should amplify users, not replace them

---

## Examples

### Example 1: E-commerce Checkout Research

**Input**: "Synthesize 15 user interviews about checkout abandonment"

**Output**:

```markdown
# Research Synthesis: Checkout Abandonment Study

**Study Date**: 2025-01-10 to 2025-01-15
**Synthesized By**: Sarah Chen, Senior PM
**Date**: 2025-01-18

---

## Executive Summary

**Research Question**: Why do users abandon checkout after adding items to cart?

**Key Insight**: 87% of participants abandoned checkout due to unexpected costs (shipping, taxes) revealed only at final step, violating expectation of "total transparency"

**Primary Recommendation**: Show total cost estimate (including shipping) on cart page before checkout starts

**Impact**: Expected 15-20% reduction in cart abandonment based on industry benchmarks

---

## Study Overview

### Research Design

**Method**: Remote user interviews via Zoom

**Objectives**:
1. Understand reasons for checkout abandonment
2. Identify friction points in checkout flow
3. Validate hypotheses about shipping costs and trust

**Dates**: Jan 10, 2025 to Jan 15, 2025 (5 days)

**Moderators**: Sarah Chen (PM), Mike Torres (UX Researcher)

---

### Participants

**Sample Size**: 15 participants

**Recruitment Criteria**:
- Added items to cart in last 30 days
- Abandoned checkout without completing purchase
- U.S. customers only

**Demographics**:
- **Age**: 28-52 (median 37)
- **Gender**: 9 female, 6 male
- **Location**: Mixed urban/suburban U.S.
- **Segment**: All existing customers (had purchased before)

**Purchase Frequency**:
- Frequent shoppers (5+ purchases): 8
- Occasional shoppers (2-4 purchases): 5
- Rare shoppers (1 purchase): 2

---

## Key Findings

### Finding 1: Unexpected Costs Cause Immediate Abandonment

**Insight**: Participants abandon checkout when final cost significantly exceeds expected price due to shipping and taxes added at last step

**Frequency**: 13/15 participants (87%) mentioned this as primary abandonment reason

**Severity**: 🔴 High

**Evidence**:

**Quotes**:
> "I had $65 worth of items, then at checkout it jumped to $89 with shipping and taxes. I felt tricked and just closed the tab."
> — Participant 3, Frequent Shopper

> "I don't mind paying for shipping, but I want to know upfront. Surprises at checkout make me feel like the company is hiding something."
> — Participant 7, Occasional Shopper

> "The $15 shipping fee on a $40 order was a dealbreaker. I would have known that earlier, I wouldn't have wasted my time."
> — Participant 12, Rare Shopper

**Observations**:
- All 13 participants who mentioned this described it as "surprising" or "unexpected"
- 9 participants explicitly used the word "tricked" or "hidden"
- 11 participants said they would complete purchase if shipping cost shown earlier

**Quantitative Data**:
- 87% cited unexpected costs as primary abandonment reason
- Average perceived price increase: 24% (actual cart: $65, final: $89)
- 0% of participants checked shipping policy before adding to cart

**Impact on User Experience**:
Frustration, loss of trust, feeling deceived

**Impact on Business**:
Cart abandonment rate 68% (industry avg 55%), estimated lost revenue $2.1M/year

**Opportunity**:
Show shipping estimate on cart page before checkout

**Priority**: 🔴 High

**Recommendation**: Display total cost estimate (item total + shipping + tax) on cart page with note "Final total shown before payment"

---

### Finding 2: Guest Checkout Preference for First-Time Buyers

**Insight**: New or infrequent shoppers prefer guest checkout to avoid account creation, perceiving it as friction

**Frequency**: 7/15 participants (47%)

**Severity**: 🟡 Medium

[Continue with similar detail...]

---

## Recommendations

### Immediate Actions (This Sprint)

1. **Add shipping cost estimator to cart page**
   - **Why**: Addresses #1 pain point (87% of users)
   - **Effort**: 3 days (eng) + 1 day (design)
   - **Expected Impact**: Reduce cart abandonment by 10-15%
   - **Owner**: Checkout team

2. **Update checkout button copy from "Checkout" to "Continue to Shipping"**
   - **Why**: Sets expectation of multi-step process
   - **Effort**: 2 hours
   - **Expected Impact**: Reduce surprise at shipping step
   - **Owner**: PM

**Total Effort**: 4 days
**Expected Impact**: 10-15% reduction in cart abandonment ($350K annual revenue)
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:interview-guide` - Plan user research interviews
- `/pm:persona` - Create personas from research insights
- `/pm:journey-map` - Map user journeys based on research
- `/pm:user-stories` - Convert insights into user stories
- `/workflows:research-to-product` - Full research-to-roadmap workflow
- `user-researcher` agent - Research methodology and synthesis
- `customer-insights` agent - Analyze customer feedback and research
