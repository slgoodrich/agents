# Survey Builder

Design effective user surveys and questionnaires for product research and feedback collection.

## Usage

```
/pm:survey [research objective] [optional: target audience, timeline]
```

## What This Command Does

1. Designs survey questionnaires aligned with research objectives
2. Creates multiple question types (multiple choice, Likert, open-ended, ranking)
3. Recommends sample size and screening criteria for target respondents
4. Provides distribution strategy and timeline
5. Includes analysis plan for interpreting results
6. Takes 30 minutes vs 2-3 hours of manual survey design

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Research Objective**:
- What are you trying to learn?
- What decisions will this inform?
- What hypotheses are you testing?
- What questions keep you up at night?

**Target Audience**:
- Who should respond? (current users, churned users, prospects, specific segments)
- How many responses do you need?
- How will you reach them?

**Constraints**:
- Timeline (how soon do you need results?)
- Survey length tolerance (5 min, 10 min, 15 min max?)
- Distribution channels available (email, in-app, paid panel)
- Budget (for incentives or paid panels)

**Example Input**:
```
Objective: Understand why users churn after onboarding
Target Audience: Users who signed up in last 3 months but churned
Sample Size Needed: 100+ responses
Timeline: Need results in 2 weeks
Max Length: 7-10 minutes
Distribution: Email to churned users
```

### 2. Define Research Questions

**Map Objectives to Questions**:
- What do we need to know to achieve objective?
- What metrics, behaviors, or attitudes matter?
- What segments or cohorts to analyze?

**Question Prioritization**:
- Must-know (critical for decision)
- Nice-to-know (adds context)
- Exploratory (may reveal insights)

### 3. Design Question Types

**Multiple Choice**: Clear options, mutually exclusive
**Likert Scale**: Attitudes, satisfaction, agreement (1-5 or 1-7)
**Rating**: Numeric ratings (0-10, 1-5 stars)
**Ranking**: Order of preference
**Open-Ended**: Qualitative insights, "why" questions
**Matrix/Grid**: Rate multiple items on same scale

### 4. Structure Survey Flow

**Introduction** → **Screening** → **Core Questions** → **Demographics** → **Thank You**

**Flow Principles**:
- Start easy, build to complex
- Group related questions
- Put sensitive questions late
- End with open-ended feedback

### 5. Plan Distribution & Analysis

**Distribution Strategy**:
- Channels (email, in-app, social, paid panel)
- Timing (day of week, time of day)
- Incentives (gift card, feature access, donation)
- Follow-up reminders

**Analysis Plan**:
- How to segment responses
- Statistical tests to run
- Qualitative coding approach
- Reporting format

## Template

```markdown
# Survey Design: [Research Objective]

**Date**: [YYYY-MM-DD]
**Owner**: [Your Name]
**Research Goal**: [What we're trying to learn]
**Target Audience**: [Who we're surveying]
**Timeline**: [Start Date] - [Results Date]

---

## Research Objectives

**Primary Question**:
[The main question this survey answers]

**Secondary Questions**:
1. [Question 2]
2. [Question 3]

**Hypotheses Being Tested**:
- **H1**: [Hypothesis 1 - what we think is true]
- **H2**: [Hypothesis 2]

**Decisions This Will Inform**:
- [Decision 1]
- [Decision 2]

---

## Target Respondents

**Who Should Respond**:
[Description of ideal respondent - role, behavior, segment]

**Sample Size**:
- **Target**: [X] responses
- **Minimum**: [Y] responses (for statistical significance)
- **Rationale**: [Why this number - confidence interval, segment size]

**Screening Criteria** (Include/Exclude):
- ✅ **Include**: [Who qualifies to take survey]
- ❌ **Exclude**: [Who doesn't qualify]

**Example Screening**:
- Include: Signed up in last 90 days, used product at least once
- Exclude: Current paying customers (separate survey), employees

---

## Survey Structure

**Estimated Length**: [X] minutes ([Y] questions)
**Completion Rate Estimate**: [Z]% (based on length and audience)

**Survey Sections**:
1. Introduction & Consent
2. Screening Questions
3. Core Topic Questions
4. Behavioral Questions
5. Demographic Questions
6. Open Feedback
7. Thank You & Next Steps

---

## Survey Questions

### Section 1: Introduction & Consent

**Introduction Text**:
```
[Survey title and purpose]

Thank you for taking our survey! We're trying to understand [objective] to improve [product/feature].

This survey takes about [X] minutes. Your responses are confidential and will be used only for research purposes.

[If incentive: Complete the survey to receive [incentive]]
```

**Consent**:
- [ ] I agree to participate in this research survey

---

### Section 2: Screening Questions

**Purpose**: Ensure respondent fits target audience

**Q1: [Screening Question 1]**
- **Type**: Multiple choice (single select)
- **Question**: [Example: "How often do you use [Product]?"]
- **Options**:
  - [ ] Daily
  - [ ] Weekly
  - [ ] Monthly
  - [ ] Rarely
  - [ ] Never
- **Logic**: If "Never" → Terminate survey (not qualified)

**Q2: [Screening Question 2]**
- **Type**: Multiple choice
- **Question**: [Example: "When did you sign up for [Product]?"]
- **Options**:
  - [ ] Less than 1 month ago
  - [ ] 1-3 months ago
  - [ ] 3-6 months ago
  - [ ] More than 6 months ago
- **Logic**: If "> 6 months" → Skip to different section or terminate

---

### Section 3: Core Research Questions

**Q3: [Primary Research Question]**
- **Type**: Likert Scale (1-5)
- **Question**: [Example: "How satisfied are you with [Feature]?"]
- **Scale**:
  - 1 = Very Dissatisfied
  - 2 = Dissatisfied
  - 3 = Neutral
  - 4 = Satisfied
  - 5 = Very Satisfied
- **Analysis**: Mean satisfaction score, % satisfied (4-5)

---

**Q4: [Secondary Question - Multiple Choice]**
- **Type**: Multiple choice (multi-select)
- **Question**: [Example: "Which features do you use most often? (Select all that apply)"]
- **Options**:
  - [ ] Feature A
  - [ ] Feature B
  - [ ] Feature C
  - [ ] Feature D
  - [ ] Other (please specify): __________
- **Analysis**: % selecting each feature, identify most/least used

---

**Q5: [Ranking Question]**
- **Type**: Ranking
- **Question**: [Example: "Rank these potential features by priority (1 = highest priority)"]
- **Items to Rank**:
  1. [Feature option 1]
  2. [Feature option 2]
  3. [Feature option 3]
  4. [Feature option 4]
- **Analysis**: Average rank for each feature, prioritization

---

**Q6: [NPS or Similar Metric]**
- **Type**: Rating scale (0-10)
- **Question**: "How likely are you to recommend [Product] to a friend or colleague?"
- **Scale**: 0 (Not at all likely) to 10 (Extremely likely)
- **Analysis**:
  - Promoters: 9-10
  - Passives: 7-8
  - Detractors: 0-6
  - **NPS Score** = % Promoters - % Detractors

---

**Q7: [Follow-up to Q6 - NPS Reasoning]**
- **Type**: Open-ended
- **Question**: "What is the primary reason for your score?"
- **Logic**: Show only if Q6 answered
- **Analysis**: Qualitative coding by theme, identify patterns in promoter/detractor feedback

---

**Q8: [Pain Point Identification]**
- **Type**: Multiple choice (single select)
- **Question**: [Example: "What is your biggest challenge with [Product]?"]
- **Options**:
  - [ ] Too complicated to use
  - [ ] Missing features I need
  - [ ] Too expensive
  - [ ] Poor performance/reliability
  - [ ] Lack of support/documentation
  - [ ] Other (please specify): __________
- **Analysis**: Top pain points by frequency

---

### Section 4: Behavioral Questions

**Q9: [Usage Frequency]**
- **Type**: Multiple choice (single select)
- **Question**: "How often do you currently use [Product/Feature]?"
- **Options**:
  - [ ] Multiple times per day
  - [ ] Daily
  - [ ] Weekly
  - [ ] Monthly
  - [ ] Less than monthly
- **Analysis**: Usage distribution, correlate with satisfaction

---

**Q10: [Feature Discovery]**
- **Type**: Multiple choice (single select)
- **Question**: "How did you first learn about [Feature/Product]?"
- **Options**:
  - [ ] In-app discovery
  - [ ] Email from us
  - [ ] Colleague recommendation
  - [ ] Social media
  - [ ] Search engine
  - [ ] Other: __________
- **Analysis**: Most effective discovery channels

---

### Section 5: Demographic Questions

**Note**: Demographics at end to avoid survey abandonment

**Q11: [Role/Job Function]**
- **Type**: Multiple choice
- **Question**: "What is your role?"
- **Options**:
  - [ ] [Role 1]
  - [ ] [Role 2]
  - [ ] [Role 3]
  - [ ] Other: __________
- **Analysis**: Segment responses by role

---

**Q12: [Company Size]** (if B2B)
- **Type**: Multiple choice
- **Question**: "How many employees does your company have?"
- **Options**:
  - [ ] 1-10
  - [ ] 11-50
  - [ ] 51-200
  - [ ] 201-1000
  - [ ] 1000+
- **Analysis**: Segment by company size

---

### Section 6: Open Feedback

**Q13: [Open-Ended Feedback]**
- **Type**: Long text
- **Question**: "Is there anything else you'd like to share about your experience with [Product]?"
- **Optional**: Yes
- **Analysis**: Qualitative themes, verbatims for case studies

---

**Q14: [Contact for Follow-Up]** (Optional)
- **Type**: Short text
- **Question**: "If you're willing to participate in a follow-up interview, please provide your email:"
- **Optional**: Yes
- **Analysis**: Build interview pipeline

---

### Section 7: Thank You

**Closing Text**:
```
Thank you for completing our survey!

Your feedback is invaluable and will help us improve [Product].

[If incentive: Your [gift card/reward] will be sent to [email] within [X] days.]

[If follow-up: We may reach out for a brief follow-up conversation.]

Questions? Contact us at [email]
```

---

## Distribution Plan

### Target Sample

**Goal**: [X] completed responses
**Expected Response Rate**: [Y]%
**Invitations Needed**: [X / (Y/100)] = [Z] invitations

**Example**:
- Goal: 200 responses
- Response Rate: 20%
- Invitations: 200 / 0.20 = 1,000 emails

---

### Distribution Channels

**Primary Channel**: [Email | In-app | Website popup | Social | Paid panel]

**Email Strategy** (if applicable):
- **List**: [Segment description, size]
- **Subject Line**: [Example: "Help us improve [Product] - 5 minutes"]
- **Send Time**: [Day of week, time] (optimize for opens)
- **Reminder 1**: [X] days after initial (to non-responders)
- **Reminder 2**: [Y] days after Reminder 1

**In-App Strategy** (if applicable):
- **Trigger**: [When to show - e.g., after 3rd session, on feature page]
- **Format**: [Modal, banner, slide-in]
- **Dismissible**: [Yes/No]
- **Frequency Cap**: [Once per user]

---

### Incentives

**Incentive Offered**: [Gift card, product credit, donation, entry to raffle]
**Value**: [$X per response or total pool]
**Rationale**: [Boost response rate from Y% to Z%]

**Delivery**:
- When: [Immediately | Within X days of completion]
- How: [Email, in-app credit, etc.]

**Budget**: [Total cost = Responses × Incentive Value]

---

### Timeline

| Phase | Activity | Duration | Date |
|-------|----------|----------|------|
| **Design** | Finalize questions | [X] days | [Date] |
| **Review** | Stakeholder review | [X] days | [Date] |
| **Setup** | Build in survey tool | [X] days | [Date] |
| **Pilot** | Test with 5-10 users | [X] days | [Date] |
| **Launch** | Send to full audience | [X] day | [Date] |
| **Reminder 1** | First reminder | [X] days after | [Date] |
| **Reminder 2** | Final reminder | [X] days after | [Date] |
| **Close** | Survey closes | [X] days open | [Date] |
| **Analysis** | Analyze results | [X] days | [Date] |
| **Report** | Share findings | [X] days | [Date] |

**Total Duration**: [X] weeks from design to report

---

## Analysis Plan

### Quantitative Analysis

**Descriptive Statistics**:
- Response rate
- Completion rate
- Mean scores for Likert/rating questions
- Distribution for multiple choice
- Top selections for ranking

**Segmentation**:
- Analyze by: [Role, Company Size, Usage Frequency, Cohort]
- Compare: [Promoters vs Detractors, Power Users vs Casual]

**Statistical Tests**:
- Chi-square test for categorical differences
- T-test for mean score comparisons
- Correlation analysis between variables

**Key Metrics**:
- **NPS**: [Net Promoter Score = % Promoters - % Detractors]
- **CSAT**: [% Satisfied (4-5 on 5-point scale)]
- **Top Pain Point**: [Most selected challenge]
- **Feature Priority**: [Ranked list of requested features]

---

### Qualitative Analysis

**Open-Ended Coding**:
- **Step 1**: Read all responses, note themes
- **Step 2**: Create codebook (5-10 themes)
- **Step 3**: Code each response (1-3 codes per response)
- **Step 4**: Count frequency of each theme

**Themes to Watch For**:
- Feature requests
- Pain points
- Use cases
- Competitive mentions
- Emotional language (love, frustrated, confused)

**Verbatim Selection**:
- Select 10-15 representative quotes
- Use in presentations, PRDs, roadmap docs

---

### Reporting Format

**Executive Summary** (1 page):
- Response rate and sample
- Top 3 findings
- Recommended actions

**Detailed Report** (5-10 pages):
- Methodology
- Full results (charts, tables)
- Segmented analysis
- Qualitative themes
- Recommendations

**Presentation** (10-15 slides):
- Research question
- Key findings (data visualizations)
- Implications for product
- Next steps

---

## Survey Quality Checklist

**Before Launch**:
- [ ] Questions aligned with research objectives
- [ ] All questions necessary (no "nice to have" bloat)
- [ ] Question wording clear and unbiased
- [ ] Response options exhaustive and mutually exclusive
- [ ] Logical flow (easy → complex, impersonal → personal)
- [ ] Screening logic correct
- [ ] Survey length < [X] minutes
- [ ] Tested with 5-10 people (pilot)
- [ ] Typos and formatting checked
- [ ] Incentive delivery process confirmed
- [ ] Data privacy / consent included

**After Launch**:
- [ ] Monitor response rate daily
- [ ] Check for drop-off points (fix if >20% abandon)
- [ ] Send reminders as planned
- [ ] Close survey at target response count or end date
- [ ] Deliver incentives promptly
- [ ] Analyze and report within [X] days

```

---

## Best Practices

### DO ✅

- **Start with clear objective** - Know what decision this informs
- **Keep it short** - Every question adds 5-10% abandonment risk
- **Use simple language** - Avoid jargon, write for 8th grade reading level
- **Offer "Other" option** - Catch responses you didn't anticipate
- **Pilot test** - Find confusing questions before full launch
- **Incentivize thoughtfully** - Small incentive often doubles response rate
- **Send reminders** - 2 reminders can boost response 30-50%
- **Close the loop** - Share what you learned and what you'll do

### DON'T ❌

- **Ask leading questions** - "How much do you love [feature]?" is biased
- **Make surveys too long** - >10 min = high abandonment
- **Ask what you already know** - Check analytics first
- **Use jargon or acronyms** - Not everyone knows your product terms
- **Forget mobile users** - 40-60% will respond on mobile
- **Skip pilot testing** - Always test with 5-10 people first
- **Let survey sit forever** - Close it and analyze, don't leave open indefinitely

---

## Examples

### Example 1: Churn Survey

**Input**: "Why do users churn after onboarding?"

**Output**:

```markdown
# Survey: Understanding Early Churn

**Target**: Users who signed up 30-90 days ago but haven't used product in 30+ days
**Sample Size**: 150 responses
**Length**: 7 minutes (12 questions)

## Key Questions:

**Q1: Onboarding Satisfaction** (Likert 1-5)
"How satisfied were you with the onboarding experience?"

**Q2: Feature Discovery** (Multiple choice)
"Were you able to find the features you needed?"
- Yes, easily
- Yes, but it took time
- Some features, but not all
- No, I couldn't find what I needed

**Q3: Primary Barrier** (Multiple choice)
"What is the main reason you stopped using [Product]?"
- Too complicated to use
- Missing features I need
- Found a better alternative
- No longer need this type of product
- Price
- Other: __________

**Q4: Re-engagement** (Open-ended)
"What would it take for you to start using [Product] again?"

## Distribution:
- Email to 750 churned users (20% response rate = 150)
- $10 gift card incentive
- 2-week survey window with 2 reminders
```

---

## Model

Use: Sonnet

---

## Related

- `/pm:interview-guide` - Qualitative research for deeper insights
- `/pm:usability-test` - Test specific flows before surveying
- `/pm:research-synthesis` - Synthesize survey results with other research
- `/workflows:discovery-sprint` - Use surveys in discovery validation
- `user-researcher` agent - Survey design and research methodology
- `customer-insights` agent - Survey analysis and insight extraction
