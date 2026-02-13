---
description: "Run a multi-agent PRD review to answer: Is this PRD ready to build?"
argument-hint: "<path-to-prd.md>"
---

# PRD Stress Test

Run a multi-agent PRD review to answer: **"Is this PRD ready to build?"** Three reviewers analyze different dimensions in parallel, cross-reference findings, and deliver a consolidated review report.

## Usage

```bash
/agent-teams:prd-stress-test path/to/prd.md
```

---

## Overview

This command spawns three specialist reviewers to stress-test a PRD from different angles:

- **market-fit-reviewer**: Does this solve a real problem for a real market?
- **feasibility-reviewer**: Are the requirements clear and buildable?
- **scope-reviewer**: Is this appropriately sized for V1?

After parallel review, reviewers cross-reference findings to catch conflicts (e.g., scope-reviewer wants to cut a feature that market-fit-reviewer considers critical). The lead compiles everything into a consolidated review report with per-dimension scores and an actionable revision checklist.

**What you get:**

- Three independent review dimensions scored 1-5
- Blocking issues (must fix before building)
- Suggestions (nice to fix)
- Conflicts between reviewers
- Overall verdict: READY TO BUILD / NEEDS REVISION / MAJOR REWORK
- Specific revision checklist

---

## Instructions

### Pre-Flight Check

1. Verify Agent Teams feature is available:

```
Check environment: CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1

If not set:
╔═══════════════════════════════════════════════════════════╗
║   Agent Teams Required                                     ║
╔═══════════════════════════════════════════════════════════╝

This command requires Claude Code's experimental Agent Teams feature.

To enable it, set the environment variable:
  export CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1

Then restart Claude Code and try again.
╚═══════════════════════════════════════════════════════════╝
```

If not enabled, display the message and stop.

2. Verify the PRD file exists:
   - Read the file at the provided path
   - If file not found, display error and stop:
     ```
     Error: PRD file not found at [path].
     Please provide a valid path to a PRD markdown file.
     ```

3. Read the full PRD content for distribution to reviewers.

---

### Phase 1: PRD Intake

1. Parse the PRD content and identify key sections (features, requirements, target users, etc.).

2. Check for existing product context:
   - Read `.claude/product-context/product-info.md` if it exists
   - Read `.claude/product-context/competitive-landscape.md` if it exists

3. Display briefing:

```
╔═══════════════════════════════════════════════════════════╗
║   PRD Stress Test                                          ║
╔═══════════════════════════════════════════════════════════╝

PRD: [file path]
Title: [extracted title or first heading]

Assembling your review team:
  1. market-fit-reviewer   - Market fit and differentiation
  2. feasibility-reviewer  - Technical feasibility and requirements clarity
  3. scope-reviewer        - Scope appropriateness and MVP sizing

Phase 1: Parallel Review (3 reviewers working simultaneously)
Phase 2: Cross-Reference (reviewers check each other's findings)
Phase 3: Consolidated Report (verdict with revision checklist)

Starting review...
╚═══════════════════════════════════════════════════════════╝
```

---

### Phase 2: Parallel Review

Spawn 3 teammates simultaneously using Agent Teams:

**Teammate 1: market-fit-reviewer**

```
Prompt: "Review this PRD for market fit. Score 1-5.

PRD CONTENT:
[full PRD content]

[Include any product context found in Phase 1]

Your job: Evaluate target user clarity, problem validation, value proposition,
differentiation, and market context. Use your market-fit-reviewer expertise.

Deliver your review in the standard market-fit-reviewer output format.
Score 1-5 using the team-deliverables rubric."
```

**Teammate 2: feasibility-reviewer**

```
Prompt: "Review this PRD for technical feasibility and requirements clarity. Score 1-5.

PRD CONTENT:
[full PRD content]

Your job: Evaluate requirements clarity, acceptance criteria, technical
feasibility, edge cases, and integration points. Flag every ambiguity.
Use your feasibility-reviewer expertise.

Deliver your review in the standard feasibility-reviewer output format.
Score 1-5 using the team-deliverables rubric."
```

**Teammate 3: scope-reviewer**

```
Prompt: "Review this PRD for scope appropriateness. Score 1-5.

PRD CONTENT:
[full PRD content]

Your job: Assess total scope, classify every feature as MUST-HAVE / CUT FROM V1 /
DEFER TO V2, identify scope creep, and estimate effort reduction from cuts.
Use your scope-reviewer expertise. Apply the 3-Feature MVP Rule.

Deliver your review in the standard scope-reviewer output format.
Score 1-5 using the team-deliverables rubric."
```

Wait for all three reviewers to complete their reviews.

---

### Phase 3: Cross-Reference

Send each reviewer the other two reviewers' findings to flag conflicts.

**To market-fit-reviewer:**

```
"Here are your fellow reviewers' findings. Flag any conflicts with your review.

FEASIBILITY REVIEW:
[feasibility-reviewer output]

SCOPE REVIEW:
[scope-reviewer output]

Specifically check:
- Are features you consider critical for differentiation marked 'CUT' by scope-reviewer?
- Do feasibility concerns affect market-critical features?
Flag conflicts and explain your position."
```

**To feasibility-reviewer:**

```
"Here are your fellow reviewers' findings. Flag any conflicts with your review.

MARKET FIT REVIEW:
[market-fit-reviewer output]

SCOPE REVIEW:
[scope-reviewer output]

Specifically check:
- Do features market-fit-reviewer considers critical have clear requirements?
- Do scope cuts remove technically risky components (positive) or create gaps?
Flag conflicts and explain your position."
```

**To scope-reviewer:**

```
"Here are your fellow reviewers' findings. Flag any conflicts with your review.

MARKET FIT REVIEW:
[market-fit-reviewer output]

FEASIBILITY REVIEW:
[feasibility-reviewer output]

Specifically check:
- Are features you marked 'CUT' considered critical by market-fit-reviewer?
- Do your cuts align with feasibility concerns?
Flag conflicts and explain your position. Be willing to reconsider cuts if
market-fit evidence is strong."
```

Wait for all three cross-reference responses.

---

### Phase 4: Consolidated Report

As the lead agent, compile all findings into the PRD Review Report.

1. Read all review reports and cross-reference responses.

2. Invoke the `team-deliverables` skill for the PRD review report template.

3. Score each dimension using the rubrics from `team-deliverables`:
   - **Market Fit** (1-5): From market-fit-reviewer
   - **Feasibility** (1-5): From feasibility-reviewer
   - **Scope** (1-5): From scope-reviewer

4. Compile blocking issues from all three reviewers.

5. Document reviewer conflicts:
   - Where scope-reviewer and market-fit-reviewer disagree on cuts
   - Where feasibility-reviewer flags risks in market-critical features
   - Provide resolution recommendation for each conflict

6. Determine verdict:
   - **READY TO BUILD**: All scores 4+, no blocking issues, conflicts resolved
   - **NEEDS REVISION**: Average score 3+, blocking issues are fixable, no fundamental problems
   - **MAJOR REWORK**: Any score below 2, or fundamental problems across dimensions

7. Generate revision checklist:
   - **Must Fix (Blocking)**: Issues from all reviewers marked as blocking
   - **Should Fix (Important)**: Non-blocking but significant improvements
   - **Nice to Fix (Polish)**: Minor improvements

8. Present the completed report to the user.

---

### Phase 5: Cleanup

1. Shut down all three teammates.

2. Display completion:

```
PRD stress test complete.

Verdict: [READY TO BUILD / NEEDS REVISION / MAJOR REWORK]
Scores: Market Fit [X]/5 | Feasibility [X]/5 | Scope [X]/5

[If NEEDS REVISION or MAJOR REWORK]:
Use the revision checklist above to address the findings,
then run the stress test again to verify.
```

---

## Error Handling

- If a reviewer fails to produce output, note the gap in the report and proceed with available reviews.
- If the PRD is very short or missing major sections, note this upfront but still run the review (the reviews will surface the gaps).
- If the PRD file is not markdown, attempt to read it anyway and note any parsing issues.

## Related

- `/agent-teams:validation-sprint` - Validate the idea before writing a PRD
- `/agent-teams:competitive-war-room` - Research competitors referenced in the PRD
- `requirements-engineer` agent - For help improving the PRD based on review findings
