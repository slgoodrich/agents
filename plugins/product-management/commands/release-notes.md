# Release Notes Generator

Generate customer-facing release notes from shipped features and changes.

## Usage

```
/pm:release-notes [version or sprint] [optional: changelog or commit history]
```

## What This Command Does

1. Converts technical changes into user-friendly language
2. Organizes updates by category (new, improvements, fixes)
3. Highlights user value and benefits
4. Creates engaging, scannable format
5. Generates multiple versions (in-app, email, blog)

## Instructions

1. **Gather Information**:
   - Version/release number
   - Features shipped
   - Bug fixes
   - Improvements
   - Breaking changes (if any)
   - Screenshots or demos

2. **Structure Release Notes**:
   - **Headline**: Most exciting new feature
   - **New Features**: What's brand new
   - **Improvements**: Enhancements to existing
   - **Bug Fixes**: Issues resolved
   - **What's Coming**: Sneak peek

3. **Write for Users**:
   - Focus on benefits, not technical details
   - Use active, friendly language
   - Include visuals when possible
   - Link to help docs
   - Celebrate user requests

4. **Tailor for Channel**:
   - **In-App**: Brief, scannable, visual
   - **Email**: Detailed, links, CTAs
   - **Blog**: Story-driven, comprehensive

## Template

```markdown
# Release Notes: [Version] - [Name]

**Released**: [Date]
**Highlights**: [One-sentence summary]

---

## 🎉 What's New

### [Feature Name]
[User-friendly description of what it does and why it matters]

**Who it's for**: [Target users]
**Why we built it**: [User request, problem solved]

[Screenshot or demo link]

**Try it now**: [How to access]

---

### [Another Feature]
[Same structure]

---

##  Improvements

- **[Feature/Area]**: [What improved and benefit] - *Thanks to [user who requested]*
- **[Feature/Area]**: [What's faster/better/easier]
- **[Feature/Area]**: [Enhancement description]

---

## 🐛 Bug Fixes

- Fixed [issue] that caused [user impact]
- Resolved [problem] when [scenario]
- Addressed [bug] affecting [users]

---

##  Learn More

- **Help Docs**: [Link to documentation]
- **Video Tutorial**: [Link to demo]
- **Feedback**: [How to share thoughts]

---

## 🔮 Coming Soon

We're working on:
- [Preview of next feature]
- [Upcoming improvement]

Stay tuned!

---

## Questions?

Reach us at [support email] or in [community/chat]
```

## Example

**Input**: "Generate release notes for v2.5 with dark mode, bulk actions, and performance improvements"

**Output**:

### Version 1: In-App Modal

```markdown
# ✨ What's New in v2.5

## Dark Mode is Here!
Your eyes will thank you. Switch between light and dark themes in Settings.

## Bulk Actions
Select multiple items and act on them all at once. Edit, delete, or move in one click.

## 2× Faster
Everything loads faster. Pages load in under 1 second now.

[See What's New] [Dismiss]
```

### Version 2: Email to Users

```markdown
Subject: Dark Mode + Bulk Actions 🎉

Hey there!

We've been listening to your feedback, and we're excited to share what's new:

## 🌙 Dark Mode (Finally!)

Our #1 requested feature is here. Toggle between light and dark themes in Settings > Appearance.

Perfect for late-night work sessions. Your retinas will appreciate it.

[Enable Dark Mode →]

##  Bulk Actions Save Time

Tired of editing items one by one? Now you can:
- Select multiple items
- Edit, delete, or move them all at once
- Save hours of repetitive work

This was requested by 500+ users. Thank you for the feedback!

[Watch Demo (30 sec) →]

## 🚀 Performance Boost

We rebuilt the engine. Everything is now 2× faster:
- Page loads: 3s → 1s
- Search results: Instant
- Smoother animations

## What's Next?

- Keyboard shortcuts (in QA now)
- Mobile app refresh
- Advanced filters

Got feedback? Hit reply - we read every message.

Cheers,
[Product Team]
```

### Version 3: Blog Post

```markdown
# Introducing Dark Mode, Bulk Actions, and Major Performance Improvements

*January 15, 2025*

Since our last release, we've shipped 47 improvements based on your feedback. Here's what's new:

## The Dark Side (It's Better Here)

After months of requests, dark mode is finally here...

[Full blog content with story, screenshots, technical details]
```

## Model

Use: claude-sonnet-4-5

## Related

- `/pm:prd` - Original requirements
- `/pm:changelog` - Technical changelog
- `/pm:stakeholder-update` - Internal update
