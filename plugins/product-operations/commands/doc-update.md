# Doc Update

Smart, surgical updates to product documentation preserving context and tracking changes.

## Usage

```
/product-operations:doc-update [doc type, section to update] [optional: change description]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. Makes surgical updates to existing documentation without full rewrites
2. Preserves valuable existing content and context
3. Tracks changes with automatic changelog generation
4. Handles multiple doc types (PRD, spec, roadmap, wiki, decision log)
5. Generates change notifications for stakeholders
6. Takes 5-10 minutes vs 30-60 minutes of manual editing

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Document Context**:
- What document needs updating? (PRD, technical spec, roadmap, wiki page, decision log, meeting notes)
- Where is the document located? (Google Doc link, Notion URL, Confluence page, GitHub markdown file)
- What's the document title and current version? (to ensure working on correct doc)
- When was it last updated? (helps assess staleness and impact of changes)

**Change Context**:
- What needs to be updated? (specific section, requirement, timeline, metric, decision)
- Why is this update needed? (decision made, requirement changed, customer feedback, strategy shift, error correction)
- What changed? (be specific: from [old] to [new])
- When did this change? (date of decision/change, to correlate with decision log if applicable)

**Scope & Impact**:
- Which sections are affected? (list specific section names or numbers)
- Is this a quick fix, medium update, or major revision? (helps scope effort)
- Does this change affect other related documents? (cascade updates needed)
- Are there dependencies? (must update A before B)

**Stakeholder Context**:
- Who needs to know about this change? (team members, stakeholders, customers)
- How critical is this update? (blocking work, high priority, nice-to-have)
- Should notifications be sent? (who to notify and through what channel)
- Who should review the update? (before publishing)

**Content Preservation**:
- What existing content is still valid? (preserve what works, update what changed)
- Are there examples or diagrams that need updating? (keep visual aids current)
- Should old content be archived or deleted? (maintain history vs clean slate)

**Tracking & Versioning**:
- Should this be tracked in a changelog? (major changes yes, typo fixes maybe not)
- What version number or date should this be? (semantic versioning or date-based)
- How should changes be attributed? (who made the change, why)

### 2. **Identify Document Type**:
   - **PRD** - Product requirements document
   - **Technical Spec** - Engineering specification
   - **Roadmap** - Product roadmap
   - **Decision Log** - Decision documentation
   - **Wiki/Docs** - Team documentation
   - **Meeting Notes** - Meeting documentation

2. **Determine Update Scope**:
   - **Quick Update** - Single section change (5 min)
   - **Medium Update** - Multiple related sections (15 min)
   - **Major Update** - Significant revision (30+ min)

3. **Gather Context**:
   - What changed (decision, requirement, priority)
   - Why it changed (customer feedback, tech constraint, strategy shift)
   - What sections are affected
   - Who needs to know about the change

4. **Make Surgical Changes**:
   - Update only affected sections
   - Preserve existing content that's still valid
   - Maintain document structure and formatting
   - Cross-reference related changes
   - Update metadata (date, version, status)

5. **Document Changes**:
   - Add changelog entry
   - Note what changed and why
   - Tag affected stakeholders
   - Generate notification if needed

## Update Types

### Quick Section Update

**When**: Single section needs updating (scope change, requirement clarification, metric update)

**Time**: 5-10 minutes

**Process**:
1. Identify section to update
2. Read current content
3. Make surgical change
4. Add changelog entry
5. Notify affected stakeholders

### Requirements Change

**When**: User story, acceptance criteria, or feature requirements changed

**Time**: 10-15 minutes

**Process**:
1. Update requirements section
2. Update acceptance criteria if affected
3. Update user stories if needed
4. Note impact on timeline/scope
5. Update changelog with decision reference

### Priority/Roadmap Shift

**When**: Feature priority changed, roadmap updated, timeline adjusted

**Time**: 10-20 minutes

**Process**:
1. Update roadmap section
2. Update timeline/milestones
3. Update priority tiers
4. Note rationale for shift
5. Generate stakeholder notification

### Decision Integration

**When**: Decision made that affects multiple doc sections

**Time**: 15-30 minutes

**Process**:
1. Update all affected sections
2. Link to decision log entry
3. Update technical approach if needed
4. Update success metrics if affected
5. Comprehensive changelog

## Templates

### PRD Update
```markdown
## [Section] Updated - [Date]

**Changed by**: [Name] | **Reason**: [Why updated]

### What Changed
- [Change 1]: [Old → New]
- [Change 2]: [Old → New]

### Impact
- **Scope**: [Changed/Unchanged]
- **Timeline**: [Changed/Unchanged]
- **Dependencies**: [New dependencies or changes]

### Action Required
- [ ] [Team/Person] - [Action needed] - [By when]
```

### Technical Spec Update
```markdown
## API Change - [Date]

**Endpoint**: `[METHOD] /api/path`
**Breaking**: Yes ❗ | No
**Version**: [v1 → v2]

**Changes**:
- [Field X]: [Old type → New type]
- [Behavior Y]: [Old behavior → New behavior]

**Migration**:
1. [Step 1]
2. [Step 2]

**Deadline**: [When old version deprecated]
```

### Runbook/Docs Update
```markdown
## [Doc Name] Updated - [Date]

**Updated by**: [Name]

**Changes**:
- ✅ Added: [New section/info]
- ✏️ Updated: [What changed]
- ❌ Removed: [What's outdated]

**Why**: [Reason for changes]

**Review by**: [Person] by [Date]
```

### Changelog Entry
```markdown
## [Version] - [Date]

### Added
- [New feature 1]
- [New feature 2]

### Changed
- [Change 1]
- [Change 2]

### Fixed
- [Bug fix 1]
- [Bug fix 2]

### Deprecated
- [Item 1] - Use [Alternative] instead

### Removed
- [Item 1] - Removed in [version]
```

### Decision Log Update
```markdown
## Decision Updated: [Decision ID]

**Original**: [What was decided before]
**Updated**: [New decision]
**Date**: [Date of change]
**Reason**: [Why changed - new info, changed context, mistake]

**Impact**: [Who/what affected]
**Migration**: [If applicable]
```


## Best Practices

✅ **DO**: Update immediately (when decision made, not later), include date + author + reason, show what changed (old → new), highlight breaking changes, notify affected people, version control everything, link related docs, include migration path, mark deprecated items clearly, keep changelog consistent

❌ **DON'T**: Update without explaining why, forget to notify affected teams, make breaking changes without migration plan, leave outdated info (confuses people), update without version bump (for specs), use vague "updated docs" commit messages, skip review for critical docs, forget to update related docs, leave TODOs unfixed, change docs without updating code (or vice versa)

**Related**: `/stakeholder-management:decision-log`, `/requirements-engineering:prd`, `/requirements-engineering:technical-spec`, `/product-operations:changelog`
