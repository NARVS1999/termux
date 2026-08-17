# React Native Concept Hierarchy

## Foundational Concepts

1. React Native — basic — ang cross-platform mobile framework na gamit ang JavaScript at React
2. JavaScript & TypeScript — basic — ang scripting languages para sa React Native logic at type safety
3. JSX — basic — ang HTML-like syntax para sa React Native component rendering
4. Components — basic — ang reusable UI building blocks ng React Native
5. Props — basic — ang data na ina-pass from parent to child component
6. State — basic — ang mutable data na nagko-control ng component behavior
7. Hooks — basic — ang functions na nag-a-extend ng capabilities ng functional components
8. Platform API — basic — ang iOS at Android specific APIs na accessible sa RN

## Core Concepts

1. View — basic — ang fundamental container component para sa layout
2. Text — basic — ang component para sa text rendering at nesting
3. Pressable — basic — ang touchable component para sa user interactions
4. ScrollView — basic — ang scrollable container para sa content overflow
5. StyleSheet — basic — ang API para sa declarative CSS-like styling
6. Flexbox — basic — ang layout system ng React Native components
7. useState — basic — ang hook para sa local component state management
8. useEffect — intermediate — ang hook para sa side effects at lifecycle management
9. useRef — basic — ang hook para sa persisting values across renders
10. Platform.select — basic — ang function para sa platform-specific code branching

## Implementation Concepts

1. Expo — basic — ang managed workflow platform para sa React Native development
2. React Native CLI — basic — ang bare workflow setup para sa full native control
3. Navigation Container — intermediate — ang root component para sa navigation tree
4. Stack Navigator — intermediate — ang push/pop navigation pattern
5. Tab Navigator — intermediate — ang bottom/top tab navigation setup
6. FlatList — intermediate — ang performant list component para sa large data sets
7. SectionList — intermediate — ang grouped list component para sa sectioned data
8. Image — basic — ang component para sa image display at loading
9. TextInput — basic — ang component para sa user text input
10. Dimensions — basic — ang API para sa screen width at height access

## Integration Concepts

1. React Navigation — intermediate — ang navigation library para sa screen management
2. Gesture Handler — intermediate — ang gesture recognition system para sa touch interactions
3. Safe Area Context — basic — ang provider para sa notch at status bar handling
4. Context API — intermediate — ang React context para sa state sharing across components
5. Async Storage — basic — ang key-value storage para sa local data persistence
6. Fetch API — basic — ang HTTP client para sa network requests
7. Error Boundaries — intermediate — ang error catching component para sa graceful failures
8. Linking — basic — ang API para sa deep linking at URL handling

## Architectural Concepts

1. Redux Toolkit — intermediate — ang state management library para sa global state
2. Zustand — intermediate — ang lightweight state management alternative
3. React Query — advanced — ang server state management para sa caching at mutations
4. MMKV — intermediate — ang fast key-value storage para sa mobile
5. SQLite — intermediate — ang relational database para sa structured local data
6. File System — basic — ang API para sa file read/write operations
7. Native Modules — advanced — ang bridge para sa custom native code integration
8. Turbo Modules — advanced — ang new architecture para sa faster native bridging

## Design Concepts

1. Theming — intermediate — ang system para sa consistent colors at design tokens
2. Dark Mode — intermediate — ang appearance switching para sa light at dark themes
3. Responsive Design — intermediate — ang adaptive layout para sa different screen sizes
4. Breakpoints — basic — ang screen size thresholds para sa responsive styling
5. Orientation — basic — ang portrait at landscape mode handling
6. Animations — intermediate — ang motion API para sa smooth transitions
7. Reanimated — advanced — ang animation library para sa worklet-based animations
8. SVG — intermediate — ang scalable vector graphics para sa custom shapes
9. WebView — intermediate — ang embedded browser para sa web content display

## Advanced Concepts

1. Memoization — intermediate — ang React.memo at useMemo para sa performance optimization
2. useCallback — intermediate — ang hook para sa function reference stability
3. Lazy Loading — intermediate — ang code splitting para sa smaller bundles
4. Image Caching — intermediate — ang image optimization para sa fast loading
5. List Virtualization — advanced — ang off-screen rendering optimization para sa large lists
6. Memory Leaks — advanced — ang detection at prevention ng unnecessary memory usage
7. Hermes Engine — basic — ang JavaScript engine optimized para sa React Native
8. New Architecture — advanced — ang Fabric at TurboModules para sa better performance

## Production Concepts

1. Code Signing — intermediate — ang certificate setup para sa app distribution
2. App Store Publishing — intermediate — ang submission process para sa iOS at Android stores
3. OTA Updates — advanced — ang over-the-air updates para sa bug fixes without app store
4. Crash Reporting — intermediate — ang error tracking para sa production monitoring
5. CI/CD — advanced — ang automated build at deployment pipelines
6. Version Management — intermediate — ang semantic versioning para sa app releases
7. Build Configuration — intermediate — ang environment setup para sa dev at production builds

## Optimization Concepts

1. Re-render Optimization — advanced — ang profiling at reducing unnecessary component updates
2. Bundle Size — advanced — ang analysis at reduction ng JavaScript bundle size
3. Startup Performance — advanced — ang cold start optimization para sa faster app launch
4. Network Optimization — advanced — ang request batching at caching strategies
5. Image Optimization — intermediate — ang compression at lazy loading para sa images
6. Memory Profiling — advanced — ang detection at fixing ng memory bottlenecks
7. Profiler Tool — basic — ang React DevTools profiler para sa performance analysis

## Expert/Strategic Concepts

1. Micro-frontends — advanced — ang modular architecture para sa large-scale apps
2. Code Push — advanced — ang deployment strategy para sa instant updates
3. A/B Testing — advanced — ang experimentation framework para sa feature validation
4. Analytics Integration — intermediate — ang tracking setup para sa user behavior insights
5. Accessibility — advanced — ang screen reader at inclusive design implementation
6. Internationalization — advanced — ang multi-language support para sa global apps
7. Security Hardening — advanced — ang encryption at secure storage para sa sensitive data
