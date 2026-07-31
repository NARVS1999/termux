# ReactJS Developer Roadmap: Fundamentals → Intermediate

> General knowledge for frontend developers, with React-specific context.

## JavaScript Fundamentals (Prerequisites)

- [x] **Phase 1** — ES6+ features: destructuring, spread/rest, template literals, arrow functions, optional chaining
- [x] **Phase 2** — Array methods: map, filter, reduce, find, some, every, flat, flatMap
- [x] **Phase 3** — Promises, async/await, error handling, fetch API
- [x] **Phase 4** — Modules: import/export, default vs named exports, dynamic imports
- [x] **Phase 5** — Closures, hoisting, event loop, spread vs rest, destructuring patterns

## React Core Concepts

- [x] **Phase 6** — JSX syntax, expressions, fragments, attribute handling
- [x] **Phase 7** — Functional components, component composition, file structure
- [x] **Phase 8** — Props: passing data, defaultProps, prop drilling, children
- [x] **Phase 9** — State with useState, immutability, state batching
- [x] **Phase 10** — Event handling, synthetic events, event delegation
- [x] **Phase 11** — Conditional rendering: ternary, &&, early return, switch
- [x] **Phase 12** — Lists & keys: rendering arrays, key selection, stable keys

## React Hooks Deep-Dive

- [x] **Phase 13** — useEffect: side effects, cleanup, dependency array, common patterns
- [x] **Phase 14** — useRef: DOM refs, mutable values, avoiding re-renders
- [x] **Phase 15** — useContext + useReducer: complex state logic, reducer patterns
- [x] **Phase 16** — Custom hooks: extracting logic, naming conventions, composition
- [x] **Phase 17** — useMemo, useCallback, React.memo: preventing unnecessary re-renders

## Styling & UI

- [x] **Phase 18** — CSS Modules: scoped styles, composition, TypeScript support
- [x] **Phase 19** — CSS-in-JS: styled-components, dynamic styles, theming
- [x] **Phase 20** — Tailwind CSS: utility-first, responsive design, dark mode, custom config

## Routing

- [x] **Phase 21** — React Router v6: BrowserRouter, Routes, Route, Link, NavLink
- [x] **Phase 22** — Dynamic routes: useParams, useSearchParams, programmatic navigation
- [x] **Phase 23** — Nested routes: Outlet, layout routes, index routes
- [x] **Phase 24** — Protected routes: auth guards, redirect, role-based routing

## Forms & Validation

- [x] **Phase 25** — Controlled vs uncontrolled inputs, form state management
- [x] **Phase 26** — Form validation: manual, library (React Hook Form, Yup/Zod)
- [x] **Phase 27** — File uploads, multi-step forms, form wizards

## State Management

- [x] **Phase 28** — Local vs global state, when to lift state, prop drilling solutions
- [x] **Phase 29** — Context API: providers, consumers, performance implications
- [x] **Phase 30** — useReducer: action dispatching, middleware patterns, testing
- [x] **Phase 31** — External libraries: Zustand, Redux Toolkit, Jotai (when & why)

## Data Fetching & APIs

- [x] **Phase 32** — useEffect + fetch: loading states, error handling, abort controllers
- [x] **Phase 33** — TanStack Query (React Query): useQuery, useMutation, cache invalidation
- [x] **Phase 34** — REST API patterns: pagination, infinite scroll, optimistic updates
- [x] **Phase 35** — Error boundaries, error states, retry strategies

## Performance Optimization

- [x] **Phase 36** — React.memo, useMemo, useCallback: when to memoize vs skip
- [x] **Phase 37** — Code splitting: React.lazy, Suspense, route-based splitting
- [x] **Phase 38** — Virtualization: react-window, react-virtualized, lazy lists

## Testing

- [x] **Phase 39** — Jest: setup, configuration, mocking modules, snapshots
- [x] **Phase 40** — React Testing Library: render, screen, fireEvent, userEvent, waitFor
- [x] **Phase 41** — Testing patterns: unit vs integration, MSW for API mocking

## Advanced Patterns & Modern React

- [ ] **Phase 42** — Error boundaries: catching errors, fallback UI, recovery
- [ ] **Phase 43** — Compound components: shared context, flexible APIs
- [ ] **Phase 44** — Render props vs hooks: when each pattern shines
- [ ] **Phase 45** — Server Components: RSC, async components, streaming
- [ ] **Phase 46** — Suspense & concurrent features: transitions, deferred values
- [ ] **Phase 47** — Project structure: feature-based layout, barrel files, monorepo basics

## Recommended Learning Path (priority order)

1. **Phase 1** — ES6+ fundamentals
2. **Phase 6–9** — JSX, components, props, state
3. **Phase 13–14** — useEffect, useRef
4. **Phase 21–22** — React Router
5. **Phase 25–26** — Forms & validation
6. **Phase 28–29** — State management
7. **Phase 32–33** — Data fetching + TanStack Query

> Focus on building real projects — employers hire mid-level React devs for clean, performant, well-tested components plus ownership of features end-to-end.
