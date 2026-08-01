# Android Developer Roadmap: Fundamentals → Intermediate

> General knowledge for mobile developers, with Android-specific context.

## Kotlin & Language Fundamentals (Prerequisites)

- [x] **Phase 1** — Kotlin basics: variables, data types, control flow, null safety
- [x] **Phase 2** — OOP in Kotlin: classes, inheritance, interfaces, sealed classes
- [x] **Phase 3** — Functions & lambdas: higher-order functions, scope functions, extensions
- [x] **Phase 4** — Collections: lists, maps, sets, filtering, mapping, sorting
- [x] **Phase 5** — Coroutines basics: launch, async, suspend functions, scopes

## Android Fundamentals

- [x] **Phase 6** — Project structure: Gradle, manifest, SDK levels, build variants
- [x] **Phase 7** — Activities & lifecycle: states, config changes, saved state
- [x] **Phase 8** — Intents: explicit vs implicit, intent filters, deep links
- [x] **Phase 9** — Fragments & navigation: fragment lifecycle, back stack, NavController
- [x] **Phase 10** — RecyclerView: adapters, ViewHolders, diffing, list rendering
- [x] **Phase 11** — App resources: strings, drawables, themes, localization, configurations

## UI Development

- [x] **Phase 12** — Jetpack Compose basics: composables, layout, modifiers, state
- [x] **Phase 13** — Compose state: remember, mutableStateOf, state hoisting, ViewModel state
- [x] **Phase 14** — XML layouts: ConstraintLayout, LinearLayout, view binding
- [x] **Phase 15** — Material Design: Material 3, theming, color systems, typography
- [x] **Phase 16** — Forms & inputs: TextFields, validation, gestures, focus handling
- [x] **Phase 17** — Animation: Compose animations, transitions, Lottie, motion

## Data & Persistence

- [x] **Phase 18** — Preferences: SharedPreferences, DataStore, settings patterns
- [x] **Phase 19** — Room: entities, DAOs, database, flows, migrations
- [x] **Phase 20** — SQLite: queries, relations, indices, performance
- [x] **Phase 21** — WorkManager: background tasks, constraints, chaining, retries
- [x] **Phase 22** — File storage: internal vs external, scoped storage, caching

## Networking & APIs

- [x] **Phase 23** — Retrofit & OkHttp: endpoints, interceptors, error handling
- [x] **Phase 24** — Serialization: kotlinx.serialization, Gson/Moshi, model mapping
- [x] **Phase 25** — Image loading: Coil, Glide, caching, placeholder handling
- [x] **Phase 26** — Connectivity: network state, timeouts, offline handling, retries

## Architecture & Patterns

- [ ] **Phase 27** — MVVM: ViewModel, UI state, unidirectional data flow
- [ ] **Phase 28** — Repository pattern: data sources, abstractions, caching layers
- [ ] **Phase 29** — Dependency injection: Hilt, Koin, manual DI, modules
- [ ] **Phase 30** — Clean architecture: layers, use cases, domain models
- [ ] **Phase 31** — Flows & state: StateFlow, SharedFlow, collecting flows safely

## Testing & Quality

- [ ] **Phase 32** — Unit testing: JUnit, MockK, coroutine testing, coverage
- [ ] **Phase 33** — Compose UI tests: testing APIs, assertions, semantics
- [ ] **Phase 34** — Instrumentation tests: Espresso, emulator testing, test devices
- [ ] **Phase 35** — Code quality: lint, detekt, formatting, ktlint

## Performance & Optimization

- [ ] **Phase 36** — Profiling: CPU, memory, network profiling tools
- [ ] **Phase 37** — Memory: leaks, weak references, bitmap handling, ProGuard/R8
- [ ] **Phase 38** — App startup: cold start, lazy init, baseline profiles
- [ ] **Phase 39** — Battery & network: Doze, background limits, efficient requests

## Security & Best Practices

- [ ] **Phase 40** — Secure storage: Keystore, EncryptedSharedPreferences, biometrics
- [ ] **Phase 41** — Networking security: HTTPS, certificate pinning, cleartext policy
- [ ] **Phase 42** — Permissions: runtime permissions, scoped models, rationale flows

## Publishing & App Store

- [ ] **Phase 43** — Release builds: signing, minification, versioning, Play App Signing
- [ ] **Phase 44** — App Bundles: AAB vs APK, asset delivery, store size limits
- [ ] **Phase 45** — Play Console: releases, tracks, testing channels, store listing
- [ ] **Phase 46** — Updates & rollout: staged rollout, update monitoring, migrations
- [ ] **Phase 47** — Crash reporting & analytics: Crashlytics, Firebase Analytics, alerts

## Recommended Learning Path (priority order)

1. **Phase 1–5** — Kotlin fundamentals
2. **Phase 6–11** — Android fundamentals
3. **Phase 12–13** — Jetpack Compose
4. **Phase 23–26** — Networking & APIs
5. **Phase 27–31** — Architecture patterns
6. **Phase 19–22** — Data persistence
7. **Phase 43–47** — Publishing & release

> Focus on building real projects — employers hire mid-level Android devs for clean, performant, well-tested code plus ownership of features end-to-end.
