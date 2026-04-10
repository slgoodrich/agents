---
name: codebase-scanning
description: "Detect platform, tech stack, features, integrations, and project scale from codebases. Use when scanning a codebase, analyzing project structure, discovering tech stack, or identifying integrations. Trigger on: 'scan my codebase', 'what tech stack am I using', 'analyze my project', 'discover integrations', 'what does this project do'."
---

# Codebase Scanning

Discover strategic product context from existing codebases. Covers web and mobile platforms.

Auto-loaded by the `context-scanner` agent for all codebase scanning operations. Also loaded when `pm-setup` bootstraps project context from code.

## Scanning Process

1. **Detect platform** - Identify web, mobile, or hybrid. For mobile, follow the detection order in `references/platform-detection.md`
2. **Parse tech stack** - Read manifests to identify frameworks, languages, databases. See `references/manifest-detection.md` for supported manifests per platform
3. **Discover features** - Scan routes, pages, and components for user-facing functionality
4. **Map integrations** - Match dependencies against known 3rd party services. See `references/integration-mapping.md` for lookup tables
5. **Estimate scale** - Count files, estimate LOC, assign complexity and maturity tiers
6. **Present results** - Use `assets/presentation-template.md` format, structured per `assets/output-schema.md`

## Feature Discovery

Scan routes, pages, and components to identify user-facing functionality.

**Methods**:

- Parse route files (Express routes, Next.js pages/, API routes)
- Analyze page/component names
- Identify API endpoints from route definitions
- Map features to evidence (file paths)

**Return format per feature**:

- name: Feature name (lowercase, descriptive)
- confidence: high/medium/low
- evidence: File paths, routes, or patterns

**Common features detected**: Authentication, project/task management, team collaboration, analytics/reporting, settings/configuration.

## Tech Stack Detection

Parse package manifests and project files to identify technologies. Supports 7 web platforms (Node.js, Python, Go, Ruby, PHP, Rust, Java) and 4 mobile platforms (iOS, Android, Flutter, React Native).

Full manifest tables and per-platform detection rules: `references/manifest-detection.md`

## Integration Discovery

Match package dependencies against known 3rd party services across 9 categories: Payments, Email, SMS, Auth, Cloud, Analytics, Monitoring, Push, Maps/Location.

Full lookup tables and cross-platform dependency mapping: `references/integration-mapping.md`

## Platform Detection

For mobile projects, detect platform type using ordered priority checks (Flutter > React Native > iOS Native > Android Native > Hybrid). Includes feature discovery rules per platform.

Detection order and feature discovery methods: `references/platform-detection.md`

## Scale Estimation

**Metrics to collect**:

- Total source files (excluding node_modules, dist, build, .git)
- Lines of code (estimate: average 25 LOC per KB of source file size, excluding binary and generated files)

**Complexity tiers**:

| Tier | Files | LOC | Characteristics |
|---|---|---|---|
| Simple | <50 | ~10k | Single service |
| Medium | 50-500 | 10k-100k | Few services |
| Complex | >500 | 100k+ | Many services/repos |

**Maturity signals**:

| Stage | LOC | Indicators |
|---|---|---|
| Prototype | ~5k | Rapid changes |
| MVP | 5k-25k | Core features present |
| Established | 25k-100k | Feature-complete |
| Mature | 100k+ | Extensive feature set |

## Confidence Assignment

- **High**: Direct evidence from routes, manifest versions, clear file patterns
- **Medium**: Package present but usage not verified; ambiguous naming patterns
- **Low**: Indirect evidence, weak signals, potentially deprecated

Package installed does not mean actively used. Assign medium confidence to integrations by default.

## Edge Cases & Limitations

### Large Codebases (>100k LOC, >1000 files)

- Limit scanning to primary directories: src/, pages/, routes/, api/, lib/
- Skip: node_modules/, dist/, build/, .git/, vendor/, test/ (unless small)
- Sample large directories (first 100 files, warn about remaining)
- Maximum 60 seconds total scan time
- Graceful degradation: return partial results with limitation note

### Monorepos

**Detection**: Check for lerna.json, nx.json, turbo.json, pnpm-workspace.yaml. Identify workspace structure (packages/, apps/).

**Handling**: Scan each workspace individually. Detect mobile + web combinations. Report tech stack per app with shared packages noted.

### Hybrid Mobile Apps

- React Native with custom native modules: ios/ and android/ with custom .swift or .kt files beyond standard RN setup
- Flutter with platform channels: ios/Runner/ or android/app/ with custom native code
- Capacitor/Ionic: capacitor.config.json present

### Conflicting Manifests

- If multiple manifests disagree (e.g., package.json has both react-native and expo), report both with evidence and let the user resolve
- Prefer the more specific indicator (expo in app.json overrides generic react-native in package.json)
- For monorepos with mixed platforms, report per-app rather than trying to unify

### Other Edge Cases

- **Permission issues**: Log warning, continue with accessible files, report in scan_limitations
- **Ambiguous patterns**: Assign lower confidence, provide evidence, let user decide. Better to under-report than hallucinate
- **Deprecated code**: Report what exists (facts), flag as medium/low confidence if evidence is weak
- **Multi-language projects**: Scan all tech stacks present, report separately
- **Empty projects**: Return empty findings, note "Project appears empty or very early stage". pm-setup falls back to manual questions
