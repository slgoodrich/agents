# Release Notes Generator

Generate customer-facing release notes that transform technical changes into engaging, user-friendly updates that drive adoption and celebrate shipped value.

## Usage

```
/pm:release-notes [version or sprint] [optional: changelog or commit history]
```

**Model Override**: Add `--model sonnet` for higher quality analysis (default: Haiku).

## What This Command Does

1. **Converts technical jargon** into user-friendly language (saves 1-2 hours per release)
2. **Organizes updates** by category (new features, improvements, fixes) for scannability
3. **Highlights user value** and benefits rather than implementation details
4. **Creates multiple versions** optimized for different channels (in-app, email, blog, changelog)
5. **Celebrates customer requests** to show you're listening and building what users need
6. **Drives feature adoption** through clear explanations and calls-to-action

## Instructions

**Context from command**: $ARGUMENTS

### 1. Gather Required Information

**IMPORTANT**: If $ARGUMENTS is empty or insufficient, gather this information from the user:

**Release Details**:
- What version/release number? (v2.5.0, Sprint 42, Q1 Release)
- When will this ship? (today, next Tuesday, Jan 15)
- Is this a major release, minor update, or patch?
- What's the target audience? (all users, specific segment, beta users)

**Changes to Announce**:
- What features/capabilities shipped? (provide list or link to changelog)
- What improvements were made? (performance, UX, existing features)
- What bugs were fixed? (especially user-reported ones)
- Are there breaking changes? (deprecations, migrations required)
- Are there visual changes? (screenshots, mockups, demos available?)

**Context**:
- What were the most requested features? (check support tickets, feedback)
- Which changes solve specific user pain points?
- Are there any customers to thank by name? (for feedback, beta testing)
- What's the story behind the biggest feature? (why built, problem solved)

**Distribution**:
- Which channels will you use? (in-app notification, email, blog, social)
- Do you need multiple versions? (short for in-app, detailed for email)
- Are there help docs or tutorials to link to?
- Is there a demo video or walkthrough available?

**Tone & Brand**:
- What's your product's voice? (formal, casual, playful, technical)
- Are there brand guidelines for release notes?
- Do you use emojis in communications?

### 2. Categorize and Prioritize Changes

**Categorization Framework**:
- **🎉 New Features**: Brand new capabilities that didn't exist before
- **✨ Improvements**: Enhancements to existing features (faster, easier, more powerful)
- **🐛 Bug Fixes**: Issues resolved (focus on user-reported or high-impact)
- **🔧 Under the Hood**: Performance, security, infrastructure (optional)
- **⚠️ Breaking Changes**: Deprecations, migrations, removed features (if applicable)

**Prioritization**:
1. Lead with the most exciting or most-requested feature
2. Group related changes together
3. Move technical/minor fixes to the bottom
4. Consider hiding very minor fixes ("and 15 other small improvements")

### 3. Write User-Focused Content

**Focus on Benefits, Not Features**:
- ❌ "Added OAuth2 integration with SAML support"
- ✅ "Sign in faster with your company account (Google, Microsoft, Okta)"

**Use Active, Friendly Language**:
- ❌ "The application has been optimized to reduce latency"
- ✅ "Pages now load 3× faster"

**Show, Don't Just Tell**:
- Include screenshots for visual changes
- Add GIFs for interactions or workflows
- Link to demo videos for complex features
- Use before/after comparisons

**Celebrate User Requests**:
- "Our #1 most-requested feature is here!"
- "Thanks to @Sarah from Acme Corp for suggesting this"
- "500+ users asked for this - thank you for the feedback!"

**Make It Actionable**:
- Tell users how to access the new feature
- Link to help docs or tutorials
- Include a clear call-to-action
- Highlight if it's opt-in or automatic

### 4. Tailor Content for Each Channel

**In-App Notification/Modal**:
- **Length**: 50-150 words max
- **Format**: Scannable bullets, large headlines
- **Visuals**: Screenshot or illustration required
- **CTA**: "Try it now" or "Learn more"
- **Tone**: Enthusiastic, concise
- **Goal**: Drive immediate adoption

**Email to Users**:
- **Length**: 200-400 words
- **Format**: Sections with headers, bullets, visuals
- **Visuals**: Multiple screenshots or GIFs
- **CTAs**: Multiple ("Enable now", "Watch demo", "Read docs")
- **Tone**: Conversational, detailed
- **Goal**: Explain value, drive clicks

**Blog Post**:
- **Length**: 500-1500 words
## Template

```markdown
# Release Notes: [Version] - [Product Name]

**Release Date**: [Date] | **Version**: [X.Y.Z]

---

## TL;DR

[2-3 sentences: What's in this release and why it matters to users]

---

## What's New

### 🚀 [Feature Name]
**What**: [What this feature does]
**Why**: [Benefit to users]
**How to use**: [Quick steps or link]

### ✨ [Feature Name]
[Same structure]

---

## Improvements

- **[Area]**: [What improved and benefit]
- **[Area]**: [What improved and benefit]

---

## Bug Fixes

- Fixed: [Issue description] - [Impact on users]
- Fixed: [Issue description] - [Impact on users]

---

## Breaking Changes ⚠️

### [Change Name]
**What changed**: [Old → New]
**Action required**: [What users must do]
**By when**: [Deadline if applicable]
**Migration guide**: [Link or steps]

---

## Deprecated

- **[Feature/API]**: Use [Alternative] instead. Removal: [Version/Date]

---

## Coming Soon

[Quick preview of next release to build excitement]

---

## Need Help?

- **Docs**: [Link]
- **Support**: [Contact/link]
- **Feedback**: [How to provide feedback]
```

## Best Practices

✅ **DO**: Write for users (not devs), lead with benefits ("you can now" vs "we added"), be specific, include screenshots/GIFs, highlight breaking changes clearly, provide migration guides, use consistent formatting, version properly (semver), publish on time, link to docs

❌ **DON'T**: Use jargon, list commits ("fixed bug #123"), skip the "why" (users don't care about implementation), hide breaking changes, write novels (be concise), forget visuals, publish late, skip user testing of notes

**Related**: `/pm:changelog`, `/pm:communication-plan`
