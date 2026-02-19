# Example Scan Results

Reference examples showing expected output for different project types. All examples use the JSON internal schema (see `assets/output-schema.md`), which is then presented to users as markdown (see `assets/presentation-template.md`).

## Example 1: React + Node.js Project

```json
{
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "src/pages/auth/login.tsx, src/pages/auth/signup.tsx, /api/auth routes"
    },
    {
      "name": "projects",
      "confidence": "high",
      "evidence": "src/pages/projects/, /api/projects routes"
    },
    {
      "name": "tasks",
      "confidence": "high",
      "evidence": "src/pages/tasks/, /api/tasks routes"
    }
  ],
  "tech_stack": {
    "frontend": ["React 18.2", "TypeScript 5.0", "Vite 4.3"],
    "backend": ["Node.js 20", "Express 4.18", "TypeScript 5.0"],
    "database": ["PostgreSQL 15 (via pg@8.11)"],
    "infrastructure": ["Docker", "GitHub Actions"]
  },
  "integrations": [
    {
      "service": "Stripe",
      "type": "payments",
      "evidence": "stripe@12.0.0 in package.json"
    }
  ],
  "scale": {
    "total_files": 234,
    "lines_of_code": 45234,
    "complexity": "medium",
    "maturity": "established"
  },
  "confidence_notes": "High confidence on all findings. Clear routes and pages for features. Tech stack directly from package.json. Stripe integration detected but not verified in use (medium confidence on active usage).",
  "scan_limitations": "None. Full scan completed successfully."
}
```

---

## Example 2: Python FastAPI Project

```json
{
  "features": [
    {
      "name": "api-authentication",
      "confidence": "high",
      "evidence": "/api/v1/auth endpoints in app/routers/auth.py"
    },
    {
      "name": "user-management",
      "confidence": "high",
      "evidence": "/api/v1/users endpoints in app/routers/users.py"
    }
  ],
  "tech_stack": {
    "frontend": [],
    "backend": ["Python 3.11", "FastAPI 0.104", "Uvicorn 0.24"],
    "database": ["PostgreSQL (via psycopg2)", "Redis (via redis-py)"],
    "infrastructure": ["Docker", "Docker Compose"]
  },
  "integrations": [
    {
      "service": "SendGrid",
      "type": "email",
      "evidence": "sendgrid in requirements.txt"
    }
  ],
  "scale": {
    "total_files": 87,
    "lines_of_code": 12400,
    "complexity": "simple",
    "maturity": "mvp"
  },
  "confidence_notes": "High confidence on API endpoints (clear router files). Medium confidence on SendGrid (package present, not verified in use).",
  "scan_limitations": "API-only project, no frontend detected."
}
```

---

## Example 3: Empty Project

```json
{
  "features": [],
  "tech_stack": {
    "frontend": [],
    "backend": [],
    "database": [],
    "infrastructure": []
  },
  "integrations": [],
  "scale": {
    "total_files": 3,
    "lines_of_code": 145,
    "complexity": "simple",
    "maturity": "prototype"
  },
  "confidence_notes": "No meaningful features or tech stack detected.",
  "scan_limitations": "Project appears empty or very early stage. Only README.md, .gitignore, and LICENSE detected. Manual context entry recommended."
}
```

---

## Example 4: iOS Native App (Swift + SwiftUI)

```json
{
  "platform": "ios",
  "platform_details": {
    "type": "native",
    "primary_platform": "ios",
    "architecture": "standard"
  },
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "LoginView.swift, SignupView.swift, ForgotPasswordView.swift"
    },
    {
      "name": "dashboard",
      "confidence": "high",
      "evidence": "HomeViewController.swift, StatsView.swift"
    },
    {
      "name": "transactions",
      "confidence": "high",
      "evidence": "TransactionListView.swift, TransactionDetailView.swift, AddTransactionView.swift"
    },
    {
      "name": "budget",
      "confidence": "high",
      "evidence": "BudgetOverviewView.swift, EditBudgetView.swift"
    }
  ],
  "tech_stack": {
    "mobile_platform": "iOS Native",
    "mobile_language": "Swift",
    "mobile_language_version": "Swift 5.9",
    "platform_version": {
      "ios_target": "15.0"
    },
    "ui_framework": "SwiftUI",
    "package_managers": ["CocoaPods", "Swift Package Manager"],
    "database": ["Core Data", "UserDefaults", "Keychain"]
  },
  "integrations": [
    {
      "service": "Firebase Authentication",
      "type": "authentication",
      "evidence": "Firebase/Auth in Podfile",
      "platforms": ["ios"]
    },
    {
      "service": "Firebase Firestore",
      "type": "database",
      "evidence": "Firebase/Firestore in Podfile",
      "platforms": ["ios"]
    },
    {
      "service": "Stripe Payments",
      "type": "payments",
      "evidence": "Stripe pod in Podfile",
      "platforms": ["ios"]
    },
    {
      "service": "Kingfisher",
      "type": "media",
      "evidence": "Kingfisher pod (image loading)",
      "platforms": ["ios"]
    }
  ],
  "scale": {
    "total_files": 145,
    "lines_of_code": 18500,
    "complexity": "medium",
    "maturity": "mvp",
    "screens_detected": 18,
    "native_modules": 0,
    "third_party_sdks": 4
  },
  "mobile_metadata": {
    "supported_devices": ["iPhone", "iPad"],
    "app_capabilities": ["push_notifications", "biometric_auth"],
    "build_system": "Xcode",
    "feature_discovery_method": "view_controllers",
    "dependency_lock_files_present": true,
    "multi_module": false
  },
  "confidence_notes": "High confidence on features (18 SwiftUI views detected). High confidence on tech stack (Podfile + project.pbxproj). Medium confidence on active integration usage.",
  "scan_limitations": "None. Full scan completed successfully."
}
```

---

## Example 5: Android Native App (Kotlin + Jetpack Compose)

```json
{
  "platform": "android",
  "platform_details": {
    "type": "native",
    "primary_platform": "android",
    "architecture": "standard"
  },
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "LoginScreen.kt, SignupScreen.kt (Composables)"
    },
    {
      "name": "feed",
      "confidence": "high",
      "evidence": "FeedActivity.kt, PostListScreen.kt"
    },
    {
      "name": "profile",
      "confidence": "high",
      "evidence": "ProfileActivity.kt, EditProfileScreen.kt"
    },
    {
      "name": "messaging",
      "confidence": "high",
      "evidence": "MessagesActivity.kt, ChatScreen.kt"
    }
  ],
  "tech_stack": {
    "mobile_platform": "Android Native",
    "mobile_language": "Kotlin",
    "mobile_language_version": "Kotlin 1.9",
    "platform_version": {
      "android_min_sdk": "24",
      "android_target_sdk": "34"
    },
    "ui_framework": "Jetpack Compose",
    "package_managers": ["Gradle"],
    "database": ["Room", "DataStore"]
  },
  "integrations": [
    {
      "service": "Firebase Authentication",
      "type": "authentication",
      "evidence": "com.google.firebase:firebase-auth in build.gradle",
      "platforms": ["android"]
    },
    {
      "service": "Firebase Cloud Messaging",
      "type": "push_notifications",
      "evidence": "com.google.firebase:firebase-messaging in build.gradle",
      "platforms": ["android"]
    },
    {
      "service": "Retrofit",
      "type": "networking",
      "evidence": "com.squareup.retrofit2:retrofit in build.gradle",
      "platforms": ["android"]
    },
    {
      "service": "Coil",
      "type": "media",
      "evidence": "io.coil-kt:coil-compose in build.gradle (image loading)",
      "platforms": ["android"]
    }
  ],
  "scale": {
    "total_files": 198,
    "lines_of_code": 22400,
    "complexity": "medium",
    "maturity": "mvp",
    "screens_detected": 15,
    "native_modules": 0,
    "third_party_sdks": 5
  },
  "mobile_metadata": {
    "supported_devices": ["phone", "tablet"],
    "app_capabilities": ["push_notifications", "camera", "location"],
    "build_system": "Gradle",
    "feature_discovery_method": "activities_fragments",
    "dependency_lock_files_present": false,
    "multi_module": false
  },
  "confidence_notes": "High confidence on features (15 Activities + Composable screens detected). High confidence on tech stack (build.gradle). Medium confidence on active integration usage.",
  "scan_limitations": "None. Full scan completed successfully."
}
```

---

## Example 6: Flutter Cross-Platform App

```json
{
  "platform": "flutter",
  "platform_details": {
    "type": "cross-platform",
    "primary_platform": "flutter",
    "additional_platforms": ["ios", "android", "web"],
    "architecture": "standard"
  },
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "lib/screens/login_screen.dart, lib/screens/signup_screen.dart"
    },
    {
      "name": "tasks",
      "confidence": "high",
      "evidence": "lib/screens/task_list_screen.dart, lib/screens/task_detail_screen.dart"
    },
    {
      "name": "projects",
      "confidence": "high",
      "evidence": "lib/screens/projects_screen.dart"
    },
    {
      "name": "settings",
      "confidence": "high",
      "evidence": "lib/screens/settings_screen.dart"
    }
  ],
  "tech_stack": {
    "mobile_platform": "Flutter",
    "mobile_language": "Dart",
    "mobile_language_version": "Dart 3.1",
    "platform_version": {
      "flutter_sdk": "3.13.0"
    },
    "ui_framework": "Flutter Widgets",
    "package_managers": ["pub"],
    "database": ["Hive", "shared_preferences"]
  },
  "integrations": [
    {
      "service": "Firebase Authentication",
      "type": "authentication",
      "evidence": "firebase_auth in pubspec.yaml",
      "platforms": ["ios", "android", "web"]
    },
    {
      "service": "Firebase Cloud Firestore",
      "type": "database",
      "evidence": "cloud_firestore in pubspec.yaml",
      "platforms": ["ios", "android", "web"]
    },
    {
      "service": "Provider",
      "type": "state_management",
      "evidence": "provider package in pubspec.yaml",
      "platforms": ["ios", "android", "web"]
    },
    {
      "service": "Cached Network Image",
      "type": "media",
      "evidence": "cached_network_image in pubspec.yaml",
      "platforms": ["ios", "android", "web"]
    }
  ],
  "scale": {
    "total_files": 156,
    "lines_of_code": 15800,
    "complexity": "medium",
    "maturity": "mvp",
    "screens_detected": 12,
    "native_modules": 0,
    "third_party_sdks": 4
  },
  "mobile_metadata": {
    "supported_devices": ["iPhone", "iPad", "Android phone", "Android tablet"],
    "app_capabilities": ["push_notifications", "camera"],
    "build_system": "Flutter CLI",
    "feature_discovery_method": "screen_files",
    "dependency_lock_files_present": true,
    "multi_module": false
  },
  "confidence_notes": "High confidence on features (12 screen files detected in lib/screens/). High confidence on tech stack (pubspec.yaml). Cross-platform targets: iOS, Android, Web. Medium confidence on active integration usage.",
  "scan_limitations": "None. Full scan completed successfully."
}
```

---

## Example 7: React Native App with Custom Native Modules

```json
{
  "platform": "react-native",
  "platform_details": {
    "type": "hybrid",
    "primary_platform": "react-native",
    "architecture": "standard"
  },
  "features": [
    {
      "name": "authentication",
      "confidence": "high",
      "evidence": "src/screens/LoginScreen.tsx, src/screens/SignupScreen.tsx"
    },
    {
      "name": "marketplace",
      "confidence": "high",
      "evidence": "src/screens/MarketplaceScreen.tsx, src/screens/ProductDetailScreen.tsx"
    },
    {
      "name": "cart",
      "confidence": "high",
      "evidence": "src/screens/CartScreen.tsx, src/screens/CheckoutScreen.tsx"
    },
    {
      "name": "profile",
      "confidence": "high",
      "evidence": "src/screens/ProfileScreen.tsx, src/screens/OrderHistoryScreen.tsx"
    }
  ],
  "tech_stack": {
    "mobile_platform": "React Native",
    "mobile_language": "JavaScript/TypeScript",
    "platform_version": {
      "react_native": "0.72.0"
    },
    "ui_framework": "React Native Components",
    "package_managers": ["npm", "CocoaPods (iOS)", "Gradle (Android)"],
    "native_modules": {
      "ios": ["CustomCameraModule.swift", "PaymentModule.swift"],
      "android": ["CustomCameraModule.kt", "PaymentModule.kt"]
    }
  },
  "integrations": [
    {
      "service": "Firebase Authentication",
      "type": "authentication",
      "evidence": "@react-native-firebase/auth in package.json",
      "platforms": ["ios", "android"]
    },
    {
      "service": "Stripe Payments",
      "type": "payments",
      "evidence": "@stripe/stripe-react-native in package.json",
      "platforms": ["ios", "android"]
    },
    {
      "service": "React Navigation",
      "type": "navigation",
      "evidence": "@react-navigation/native in package.json",
      "platforms": ["ios", "android"]
    },
    {
      "service": "Fast Image",
      "type": "media",
      "evidence": "react-native-fast-image in package.json",
      "platforms": ["ios", "android"]
    }
  ],
  "scale": {
    "total_files": 212,
    "lines_of_code": 28400,
    "complexity": "medium",
    "maturity": "established",
    "screens_detected": 16,
    "native_modules": 4,
    "third_party_sdks": 6
  },
  "mobile_metadata": {
    "supported_devices": ["iPhone", "iPad", "Android phone", "Android tablet"],
    "app_capabilities": ["push_notifications", "camera", "payments"],
    "build_system": "Metro Bundler",
    "feature_discovery_method": "route_definitions",
    "dependency_lock_files_present": true,
    "multi_module": false
  },
  "confidence_notes": "High confidence on features (16 screen components detected in src/screens/). High confidence on tech stack (package.json + native dependencies). Hybrid architecture: React Native with 4 custom native modules (2 iOS Swift, 2 Android Kotlin). Medium confidence on active integration usage.",
  "scan_limitations": "None. Full scan completed successfully."
}
```

---

## Example 8: Monorepo (Web + iOS + Android)

```json
{
  "platform": "hybrid",
  "platform_details": {
    "type": "hybrid",
    "architecture": "monorepo"
  },
  "monorepo_structure": {
    "apps": [
      {
        "name": "web",
        "path": "apps/web",
        "platform": "web",
        "tech_stack": {
          "frontend": ["React 18.2", "TypeScript 5.0"]
        }
      },
      {
        "name": "mobile-ios",
        "path": "apps/ios",
        "platform": "ios",
        "tech_stack": {
          "mobile_platform": "iOS Native",
          "mobile_language": "Swift 5.9",
          "ui_framework": "SwiftUI"
        }
      },
      {
        "name": "mobile-android",
        "path": "apps/android",
        "platform": "android",
        "tech_stack": {
          "mobile_platform": "Android Native",
          "mobile_language": "Kotlin 1.9",
          "ui_framework": "Jetpack Compose"
        }
      }
    ],
    "shared_packages": [
      "packages/ui-components",
      "packages/api-client",
      "packages/utils"
    ]
  },
  "confidence_notes": "Monorepo detected with 3 apps: web (React + TS), iOS (Swift + SwiftUI), Android (Kotlin + Compose). Shared packages detected. Tech stack reported per app.",
  "scan_limitations": "None. Full scan completed successfully."
}
```
