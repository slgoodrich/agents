# Context Scanner Presentation Template

Use this markdown template when presenting scan findings to users for validation.

## Template

```markdown
## Codebase Scan Results

### Platform

- **Type:** [Web application / iOS Native / Android Native / Flutter / React Native] ([framework details])

### Features Discovered (High Confidence)

- **[Feature Name]** - Evidence: [file paths, routes]
- **[Feature Name]** - Evidence: [file paths, routes]

### Features Discovered (Medium Confidence)

- **[Feature Name]** - Evidence: [file paths] (may be work-in-progress)

### Tech Stack

**Frontend:** [frameworks, languages, build tools]
**Backend:** [frameworks, languages, runtimes]
**Database:** [databases with package evidence]
**Infrastructure:** [deployment, CI/CD]

_(For mobile, replace with:)_
**Platform:** [iOS Native / Android Native / Flutter / React Native]
**Language:** [Swift X.X / Kotlin X.X / Dart X.X]
**UI Framework:** [SwiftUI / Jetpack Compose / Flutter Widgets / RN Components]
**Package Managers:** [CocoaPods, SPM, Gradle, pub, npm]

### Integrations Detected

- **[Service]** ([category]) - Evidence: [package@version in manifest] [Medium confidence - package present, usage not verified]

### Project Scale

- **Files:** [N] source files
- **Size:** ~[N]k LOC (approximate)
- **Complexity:** [Simple / Medium / Complex]
- **Maturity:** [Prototype / MVP / Established / Mature]

_(For mobile, add:)_
- **Screens:** [N] detected
- **Native Modules:** [N] custom
- **3rd Party SDKs:** [N] integrated

### Confidence Notes

[Explain confidence levels. Example: "High confidence on features (clear routes and pages). High confidence on tech stack (direct from package.json). Stripe integration detected but not verified in use (medium confidence on active usage)."]

### Scan Limitations

[Note any limitations. Example: "None. Full scan completed successfully." or "Large codebase detected (5000+ files). Scanned src/, api/, and pages/ directories only."]

---

**Please review and validate:**

- Are these features correct?
- Any features I missed?
- Any features listed that don't actually exist or are deprecated?
- Are tech stack and integrations accurate?
```

## After Validation

After the user confirms/corrects findings, create or update context files using the Write tool. Add metadata to all auto-discovered data:

```markdown
_Auto-discovered: [date]_
_Last validated: [date]_
_Evidence: [manifest files and directories scanned]_
```
