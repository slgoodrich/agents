# Integration Mapping

Identify 3rd party services from package dependencies.

## Common Integrations by Category

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

## Mobile Backend/Database

Firebase (Firestore, Realtime DB, Storage), Supabase, Realm, Core Data (iOS), Room (Android), Hive (Flutter).

## Mobile Networking

Alamofire (iOS), Retrofit (Android), Dio (Flutter), Axios (React Native).

## Mobile Media

Kingfisher (iOS), Coil (Android), cached_network_image (Flutter), react-native-fast-image.

## Cross-Platform Dependency Mapping

| Universal Name | iOS (CocoaPods/SPM) | Android (Gradle) | Flutter (pub) | React Native (npm) |
|---|---|---|---|---|
| Firebase Auth | Firebase/Auth | firebase-auth | firebase_auth | @react-native-firebase/auth |
| Stripe | Stripe | stripe-android | stripe_flutter | @stripe/stripe-react-native |
| Image Loading | Kingfisher | coil | cached_network_image | react-native-fast-image |
| Networking | Alamofire | retrofit | dio | axios |

## Confidence Note

Package installed does not mean actively used. Assign medium confidence to integrations.
