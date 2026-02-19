---
name: codebase-scanning
description: Platform detection patterns, manifest parsing rules, feature discovery methods, integration mapping, and edge case handling for codebase scanning
---

# Codebase Scanning

Detection patterns and scanning rules for discovering strategic product context from existing codebases. Covers web and mobile platforms.

## When to Use This Skill

**Auto-loaded by agents**:

- `context-scanner` - For all codebase scanning operations

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

---

## Tech Stack Detection

Parse package manifests and project files to identify technologies.

### Supported Manifests

**Web Platforms**:

| Platform | Manifest |
|---|---|
| Node.js | package.json |
| Python | requirements.txt, pyproject.toml, Pipfile |
| Go | go.mod |
| Ruby | Gemfile |
| PHP | composer.json |
| Rust | Cargo.toml |
| Java | pom.xml, build.gradle |

**Mobile Platforms**:

| Platform | Manifests |
|---|---|
| iOS | Podfile, Package.swift, *.xcodeproj/project.pbxproj |
| Android | build.gradle, build.gradle.kts, AndroidManifest.xml |
| Flutter | pubspec.yaml, pubspec.lock |
| React Native | package.json, ios/Podfile, android/build.gradle |

### What to Detect

**Web**: Frontend frameworks (React, Vue, Angular, Svelte, Next.js), backend frameworks (Express, FastAPI, Rails, Django, Laravel, Gin), databases (PostgreSQL, MySQL, MongoDB, Redis via client packages), languages/versions, build tools (Vite, Webpack, esbuild).

**iOS**: Swift version, Objective-C, UIKit vs SwiftUI, iOS deployment target, Xcode version.

**Android**: Kotlin version, Java, Jetpack Compose vs XML layouts, minSdk, targetSdk, Gradle version.

**Flutter**: Flutter SDK version, Dart version, platform targets (iOS, Android, Web, Desktop).

**React Native**: RN version, TypeScript usage, Expo detection, native module detection.

---

## Integration Discovery

Identify 3rd party services from package dependencies.

**Common integrations by category**:

| Category | Services |
|---|---|
| Payments | Stripe, PayPal, Square, Braintree, In-App Purchases |
| Email | SendGrid, Mailgun, AWS SES |
| SMS | Twilio, Plivo |
| Auth | Auth0, Firebase Auth, Okta, Sign in with Apple, Google Sign-In |
| Cloud | AWS SDK, GCP SDK, Azure SDK |
| Analytics | Segment, Mixpanel, Amplitude, Firebase Analytics, Facebook SDK |
| Monitoring | Sentry, Datadog, New Relic, Crashlytics, Bugsnag |
| Push | Firebase Cloud Messaging, OneSignal, APNs |
| Maps/Location | Google Maps SDK, Mapbox, Apple Maps, Core Location |
| State Mgmt | Redux, MobX, Provider, Riverpod, GetX |

**Mobile backend/database**: Firebase (Firestore, Realtime DB, Storage), Supabase, Realm, Core Data (iOS), Room (Android), Hive (Flutter).

**Mobile networking**: Alamofire (iOS), Retrofit (Android), Dio (Flutter), Axios (React Native).

**Mobile media**: Kingfisher (iOS), Coil (Android), cached_network_image (Flutter), react-native-fast-image.

**Confidence note**: Package installed does not mean actively used. Assign medium confidence to integrations.

---

## Mobile Platform Detection

Check in this order:

1. **Flutter**: pubspec.yaml exists AND lib/main.dart exists
2. **React Native**: package.json exists AND (ios/ + android/ directories OR "react-native" in dependencies)
3. **iOS Native**: (Podfile OR Package.swift OR *.xcodeproj) AND NO android/ directory
4. **Android Native**: (build.gradle OR build.gradle.kts) AND NO ios/ directory
5. **Hybrid/Monorepo**: Multiple platform indicators present

**Edge cases**:

- **Expo**: Detect from app.json or "expo" in package.json dependencies
- **Flutter with custom native code**: Both pubspec.yaml and platform directories with custom code
- **Monorepo**: Multiple apps/ subdirectories with different platforms - scan each separately

### Mobile Feature Discovery

**iOS Native**: Search for *ViewController.swift (UIKit), *View.swift (SwiftUI). Count distinct ViewControllers/Views = feature count. Exclude Tests/, Pods/.

**Android Native**: Search for classes extending Activity, Fragment, @Composable functions. Parse navigation.xml. Count Activities + Fragment groups + Composable screens. Look in app/src/main/.

**Flutter**: Search lib/screens/, lib/pages/, route definitions. Parse MaterialApp.routes or GoRouter. Count screen files + routes.

**React Native**: Search src/screens/, src/pages/, Stack.Screen definitions. Parse React Navigation navigators. Count screen components.

### Mobile Integration Mapping

Map platform-specific dependencies to universal names:

| Universal Name | iOS (CocoaPods/SPM) | Android (Gradle) | Flutter (pub) | React Native (npm) |
|---|---|---|---|---|
| Firebase Auth | Firebase/Auth | firebase-auth | firebase_auth | @react-native-firebase/auth |
| Stripe | Stripe | stripe-android | stripe_flutter | @stripe/stripe-react-native |
| Image Loading | Kingfisher | coil | cached_network_image | react-native-fast-image |
| Networking | Alamofire | retrofit | dio | axios |

**Integration categories**: Authentication, Payments, Analytics, Database, Networking, Media, Location, Push Notifications, Crash Reporting, State Management.

---

## Scale Estimation

**Metrics to collect**:

- Total source files (excluding node_modules, dist, build, .git)
- Lines of code (approximated from file sizes, not precise line counts)

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

---

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

**Types**:

- React Native with custom native modules (RN + Swift + Kotlin)
- Flutter with platform channels (Flutter + native iOS/Android code)
- Capacitor/Ionic (web app in native container)

**Detection**:

- React Native: ios/ and android/ with custom .swift or .kt files beyond standard RN setup
- Flutter: ios/Runner/ or android/app/ with custom native code
- Capacitor: capacitor.config.json present

### Permission Issues

- Attempt to read file/directory
- If permission denied: log warning, continue with accessible files
- Report in scan_limitations

### Ambiguous Patterns

- If uncertain, assign lower confidence
- Provide evidence, let user decide
- Better to under-report than hallucinate

### Deprecated Code

- Report what exists (facts)
- Flag as medium/low confidence if evidence is weak
- User validation catches deprecated features

### Multi-Language Projects

- Scan all tech stacks present
- Report separately in tech_stack
- Note in confidence_notes

### Empty Projects

- No src/, pages/, routes/, api/ directories and no manifests
- Return empty findings
- Note: "Project appears empty or very early stage"
- pm-setup falls back to manual questions
