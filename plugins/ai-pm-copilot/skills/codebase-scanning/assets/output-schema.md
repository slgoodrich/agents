# Context Scanner Output Schema

Internal data structure used by context-scanner to organize findings before presenting to users as markdown.

## JSON Schema

```json
{
  "platform": "web" | "ios" | "android" | "flutter" | "react-native" | "hybrid",
  "platform_details": {
    "type": "native" | "cross-platform" | "hybrid",
    "primary_platform": "ios" | "android" | "flutter" | "react-native" | "web",
    "additional_platforms": ["web", "desktop"],
    "architecture": "standard" | "monorepo" | "custom"
  },
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "src/pages/login.tsx, src/api/auth/, /auth/* routes"
    }
  ],
  "tech_stack": {
    "frontend": ["React 18.2", "TypeScript 5.0", "Vite 4.3"],
    "backend": ["Node.js 20", "Express 4.18", "TypeScript 5.0"],
    "database": ["PostgreSQL 15 (via pg package)", "Redis (via ioredis)"],
    "infrastructure": ["Docker", "GitHub Actions (CI/CD)"],

    "mobile_platform": "iOS Native" | "Android Native" | "Flutter" | "React Native",
    "mobile_language": "Swift" | "Kotlin" | "Dart" | "JavaScript/TypeScript",
    "mobile_language_version": "Swift 5.9" | "Kotlin 1.9" | "Dart 3.1",
    "platform_version": {
      "ios_target": "15.0",
      "android_min_sdk": "21",
      "android_target_sdk": "34",
      "flutter_sdk": "3.13.0",
      "react_native": "0.72.0"
    },
    "ui_framework": "UIKit" | "SwiftUI" | "Jetpack Compose" | "XML" | "Flutter Widgets" | "React Native Components",
    "package_managers": ["CocoaPods", "SPM", "Gradle", "pub", "npm"],
    "native_modules": {
      "ios": ["CustomCameraModule.swift"],
      "android": ["CustomCameraModule.kt"]
    }
  },
  "integrations": [
    {
      "service": "Stripe",
      "type": "payments",
      "evidence": "stripe@12.0.0 in package.json",
      "platforms": ["ios", "android"]
    }
  ],
  "scale": {
    "total_files": 234,
    "lines_of_code": 45234,
    "complexity": "medium",
    "maturity": "established",
    "screens_detected": 18,
    "native_modules": 2,
    "third_party_sdks": 8
  },
  "mobile_metadata": {
    "supported_devices": ["iPhone", "iPad"],
    "app_capabilities": ["push_notifications", "location", "camera"],
    "build_system": "Xcode" | "Gradle" | "Flutter CLI",
    "feature_discovery_method": "view_controllers" | "activities_fragments" | "screen_files" | "route_definitions",
    "dependency_lock_files_present": true,
    "multi_module": false
  },
  "monorepo_structure": {
    "apps": [
      {
        "name": "mobile-ios",
        "path": "apps/ios",
        "platform": "ios"
      }
    ],
    "shared_packages": ["packages/ui-components", "packages/api-client"]
  },
  "confidence_notes": "Free-form explanation of confidence levels and uncertainties.",
  "scan_limitations": "Free-form explanation of what couldn't be scanned and why."
}
```

## Field Definitions

**platform**: Primary platform type (web, ios, android, flutter, react-native, hybrid).

**platform_details**: Platform-specific metadata.

- type: native (iOS/Android), cross-platform (Flutter/RN), hybrid (multiple)
- primary_platform: Main platform if multiple exist
- additional_platforms: Other platforms supported (web, desktop)
- architecture: standard, monorepo, custom

**features**: Array of user-facing functionality.

- name: Feature name (lowercase, descriptive)
- confidence: high/medium/low
- evidence: File paths, routes, or patterns that indicate this feature

**tech_stack**: Technology components.

- frontend: UI frameworks, languages, build tools
- backend: Server frameworks, languages, runtimes
- database: Databases and caching systems (via client packages)
- infrastructure: Deployment and DevOps tools
- mobile_platform: iOS Native, Android Native, Flutter, React Native
- mobile_language: Swift, Kotlin, Dart, JavaScript/TypeScript
- mobile_language_version: Version of primary language
- platform_version: iOS target, Android SDK versions, Flutter/RN versions
- ui_framework: UIKit, SwiftUI, Jetpack Compose, XML, Flutter Widgets
- package_managers: CocoaPods, SPM, Gradle, pub, npm
- native_modules: Custom native code in iOS/Android directories

**integrations**: 3rd party services.

- service: Service name (Stripe, Firebase Auth, etc.)
- type: Category (payments, email, cloud, auth)
- evidence: Package name and version
- platforms: Platforms where this integration is used (optional)

**scale**: Project size indicators.

- total_files: Count excluding node_modules, dist, build
- lines_of_code: Rough estimate
- complexity: simple/medium/complex
- maturity: prototype/mvp/established/mature
- screens_detected: Mobile screen count (mobile only)
- native_modules: Count of custom native modules (mobile only)
- third_party_sdks: Count of integrated SDKs (mobile only)

**mobile_metadata**: Mobile-specific metadata (mobile platforms only).

- supported_devices: iPhone, iPad, Android phone, tablet
- app_capabilities: push_notifications, location, camera, etc.
- build_system: Xcode, Gradle, Flutter CLI
- feature_discovery_method: How features were detected
- dependency_lock_files_present: Podfile.lock, pubspec.lock present
- multi_module: Android multi-module project detection

**monorepo_structure**: Monorepo details (if detected).

- apps: Array of apps in monorepo (name, path, platform)
- shared_packages: Shared code packages

**confidence_notes**: Free-form explanation of confidence levels and uncertainties.

**scan_limitations**: Free-form explanation of what couldn't be scanned and why.
