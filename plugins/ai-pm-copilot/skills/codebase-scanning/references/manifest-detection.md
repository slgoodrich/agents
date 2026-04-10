# Manifest Detection Tables

Package manifests and project files used to identify technologies.

## Web Platforms

| Platform | Manifest |
|---|---|
| Node.js | package.json |
| Python | requirements.txt, pyproject.toml, Pipfile |
| Go | go.mod |
| Ruby | Gemfile |
| PHP | composer.json |
| Rust | Cargo.toml |
| Java | pom.xml, build.gradle |

## Mobile Platforms

| Platform | Manifests |
|---|---|
| iOS | Podfile, Package.swift, *.xcodeproj/project.pbxproj |
| Android | build.gradle, build.gradle.kts, AndroidManifest.xml |
| Flutter | pubspec.yaml, pubspec.lock |
| React Native | package.json, ios/Podfile, android/build.gradle |

## What to Detect Per Platform

**Web**: Frontend frameworks (React, Vue, Angular, Svelte, Next.js), backend frameworks (Express, FastAPI, Rails, Django, Laravel, Gin), databases (PostgreSQL, MySQL, MongoDB, Redis via client packages), languages/versions, build tools (Vite, Webpack, esbuild).

**iOS**: Swift version, Objective-C, UIKit vs SwiftUI, iOS deployment target, Xcode version.

**Android**: Kotlin version, Java, Jetpack Compose vs XML layouts, minSdk, targetSdk, Gradle version.

**Flutter**: Flutter SDK version, Dart version, platform targets (iOS, Android, Web, Desktop).

**React Native**: RN version, TypeScript usage, Expo detection, native module detection.
