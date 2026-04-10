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

## Field Notes

Field names in the schema are self-documenting. See `SKILL.md` for detection rules, confidence assignment, and platform-specific guidance. See `references/example-scans.md` for complete output examples across all supported platforms.
