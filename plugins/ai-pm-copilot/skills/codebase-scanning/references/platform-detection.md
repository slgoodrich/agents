# Mobile Platform Detection

## Detection Order

Check in this order:

1. **Flutter**: pubspec.yaml exists AND lib/main.dart exists
2. **React Native**: package.json exists AND (ios/ + android/ directories OR "react-native" in dependencies)
3. **iOS Native**: (Podfile OR Package.swift OR *.xcodeproj) AND NO android/ directory
4. **Android Native**: (build.gradle OR build.gradle.kts) AND NO ios/ directory
5. **Hybrid/Monorepo**: Multiple platform indicators present

## Edge Cases

- **Expo**: Detect from app.json or "expo" in package.json dependencies
- **Flutter with custom native code**: Both pubspec.yaml and platform directories with custom code
- **Monorepo**: Multiple apps/ subdirectories with different platforms - scan each separately

## Feature Discovery by Platform

**iOS Native**: Search for *ViewController.swift (UIKit), *View.swift (SwiftUI). Count distinct ViewControllers/Views = feature count. Exclude Tests/, Pods/.

**Android Native**: Search for classes extending Activity, Fragment, @Composable functions. Parse navigation.xml. Count Activities + Fragment groups + Composable screens. Look in app/src/main/.

**Flutter**: Search lib/screens/, lib/pages/, route definitions. Parse MaterialApp.routes or GoRouter. Count screen files + routes.

**React Native**: Search src/screens/, src/pages/, Stack.Screen definitions. Parse React Navigation navigators. Count screen components.
