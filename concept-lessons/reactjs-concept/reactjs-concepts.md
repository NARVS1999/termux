# React.js Concept Hierarchy

## Foundational Concepts

1. JSX — basic — ang HTML-like syntax sa loob ng JavaScript
2. Components — basic — ang reusable na UI pieces na may sariling laman
3. Props — basic — ang data na pinapasa mula parent papunta sa child
4. State — basic — ang internal data ng component na nagbabago
5. Virtual DOM — basic — ang lightweight na representation ng real DOM
6. One-Way Data Flow — basic — ang data ay pababa lang mula parent sa child
7. Fragments — basic — ang pag-group ng elements nang walang extra wrapper
8. Keys — basic — ang unique na identifier para sa lists ng elements

## Core Concepts

1. Functional Components — basic — ang components na gawa sa functions
2. Class Components — intermediate — ang components na gawa sa classes (legacy)
3. useState Hook — basic — ang pag-manage ng state sa functional components
4. useEffect Hook — intermediate — ang pag-handle ng side effects
5. useRef Hook — intermediate — ang pag-access ng DOM elements at mutable values
6. useMemo Hook — intermediate — ang pag-cache ng expensive computations
7. useCallback Hook — intermediate — ang pag-cache ng functions para sa optimization
8. useContext Hook — intermediate — ang pag-access ng context values
9. Custom Hooks — intermediate — ang pagbubuo ng sariling reusable hooks
10. Conditional Rendering — basic — ang pagpapakita ng elements batay sa condition

## Implementation Concepts

1. Component Lifecycle — intermediate — ang mga stages ng component mula mount hanggang unmount
2. Event Handling — basic — ang pag-react sa user actions gaya ng click at input
3. Forms — intermediate — ang paghawak ng controlled at uncontrolled inputs
4. Lists & Keys — intermediate — ang pag-render ng maraming items nang tama
5. Composition — intermediate — ang pagbubuo ng components mula sa mas maliliit na components
6. Children Prop — intermediate — ang pag-pass ng elements bilang prop
7. Props Destructuring — basic — ang pag-extract ng props sa function parameters
8. Default Props — basic — ang fallback values ng props kapag walang passed value
9. Error Boundaries — intermediate — ang pag-catch ng errors sa component tree
10. Refs Forwarding — advanced — ang pag-pass ng refs sa child components

## Integration Concepts

1. State Lifting — intermediate — ang paglipat ng state sa common parent
2. Context API — intermediate — ang pag-share ng data nang hindi nag-pa-pass ng props
3. React Router — intermediate — ang pag-navigate ng pages nang walang reload
4. Client-Side Routing — intermediate — ang pag-manage ng URL sa browser
5. API Fetching — intermediate — ang pagkuha ng data mula sa external APIs
6. Loading & Error States — intermediate — ang pag-display habang naglo-load o may error
7. Pagination — intermediate — ang paghahati ng data sa pages
8. Search & Filtering — intermediate — ang paghanap at pag-filter ng data

## Architectural Concepts

1. Component Architecture — intermediate — ang pagbubuo ng app bilang component tree
2. Container/Presentational Pattern — intermediate — ang paghihiwalay ng logic at UI
3. Higher-Order Components — advanced — ang functions na nag-e-enhance ng components
4. Render Props — advanced — ang pag-share ng logic gamit ang function as prop
5. Compound Components — advanced — ang pattern na may implicit state sharing
6. Controlled vs Uncontrolled — intermediate — ang pagpili ng tamang form approach
7. State Management Options — intermediate — ang pagpili ng state management solution
8. Component Reusability — intermediate — ang paggawa ng components na pwedeng i-reuse

## Design Concepts

1. Design System — intermediate — ang set ng reusable na UI components
2. Component Styling — intermediate — ang mga paraan ng pag-style ng components
3. CSS-in-JS — intermediate — ang pag-style gamit ang JavaScript objects
4. Responsive Design — intermediate — ang paggawa ng UI na nag-a-adapt sa screen size
5. Accessibility — intermediate — ang paggawa ng UI na accessible sa lahat ng users
6. Animation — intermediate — ang pagdagdag ng movements para sa better UX
7. Theming — intermediate — ang pag-manage ng colors at styles across the app
8. Icons & Images — basic — ang pag-handle ng visual assets

## Advanced Concepts

1. React.memo — advanced — ang pag-memoize ng component para sa optimization
2. Lazy Loading — intermediate — ang pag-load ng components kapag kailangan lang
3. Suspense — intermediate — ang pag-handle ng loading states ng lazy components
4. Concurrent Features — advanced — ang mga bagong features para sa better UX
5. Server Components — advanced — ang components na tumatakbo sa server
6. Streaming SSR — advanced — ang server-side rendering na hindi nagwa-wait
7. Islands Architecture — advanced — ang paghihiwalay ng interactive at static parts
8. Micro-Frontends — advanced — ang pag-split ng frontend sa smaller pieces

## Production Concepts

1. Code Splitting — intermediate — ang paghahati ng code sa smaller bundles
2. Bundle Analysis — intermediate — ang pagtingin ng bundle size breakdown
3. Tree Shaking — advanced — ang pagtanggal ng unused code
4. Minification — basic — ang pagliit ng file size
5. Source Maps — intermediate — ang pag-trace ng minified code sa original
6. Error Tracking — intermediate — ang pag-monitor ng errors sa production
7. Performance Monitoring — intermediate — ang pag-sukat ng app performance
8. SEO Optimization — intermediate — ang pag-optimize para sa search engines

## Optimization Concepts

1. Memoization — intermediate — ang pag-cache ng computations para hindi mag-recompute
2. Virtualization — advanced — ang pag-render lang ng visible items sa lists
3. Debouncing — intermediate — ang pag-delay ng function execution
4. Throttling — intermediate — ang pag-limit ng function execution frequency
5. Image Optimization — intermediate — ang pag-combine at lazy load ng images
6. Prefetching — intermediate — ang pag-load ng resources ahead of time
7. Service Worker — intermediate — ang caching ng assets para sa offline support
8. Performance Profiling — intermediate — ang pag-analyze ng bottlenecks

## Expert/Strategic Concepts

1. React Fiber Architecture — advanced — ang loob ng reconciler ng React
2. Reconciliation Algorithm — advanced — ang pag-compare ng old at new virtual DOM
3. Batch Updates — advanced — ang pag-group ng state updates para sa efficiency
4. React Internals — advanced — ang deep understanding ng React source code
5. Custom Renderer — advanced — ang paggawa ng sariling React renderer
6. Compiler Optimizations — advanced — ang understanding ng React Compiler
7. Testing Strategies — intermediate — ang pag-test ng React components
8. State Machine Approach — advanced — ang pag-model ng state gamit ang state machines
9. Performance Engineering — advanced — ang pag-optimize ng React app hanggang sa limit
