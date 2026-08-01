# Design Patterns Roadmap: Fundamentals → Intermediate

> General knowledge for software developers, with design patterns-specific context.

## Foundations

- [x] **Phase 1** — SOLID principles: single responsibility, open-closed, Liskov, interface segregation, dependency inversion
- [x] **Phase 2** — DRY, KISS, YAGNI: code simplicity principles and when to apply
- [x] **Phase 3** — Composition vs inheritance: favoring object composition over class inheritance
- [x] **Phase 4** — Abstraction, encapsulation, polymorphism: OOP pillars in practice

## Creational Patterns

- [x] **Phase 5** — Singleton: lazy vs eager initialization, thread safety, anti-patterns
- [x] **Phase 6** — Factory Method: creating objects without specifying exact class
- [x] **Phase 7** — Abstract Factory: families of related objects, product families
- [x] **Phase 8** — Builder: step-by-step construction, fluent interfaces, director
- [x] **Phase 9** — Prototype: cloning objects, copy constructor, shallow vs deep copy
- [x] **Phase 10** — Object Pool: reusing expensive objects, connection pools

## Structural Patterns

- [x] **Phase 11** — Adapter: converting interfaces, legacy integration, third-party wrapping
- [x] **Phase 12** — Bridge: separating abstraction from implementation, platform independence
- [x] **Phase 13** — Composite: tree structures, part-whole hierarchy, recursive composition
- [x] **Phase 14** — Decorator: adding responsibilities dynamically, wrapping objects
- [x] **Phase 15** — Facade: simplified interface, subsystem abstraction
- [x] **Phase 16** — Flyweight: sharing common state, memory optimization
- [x] **Phase 17** — Proxy: controlling access, virtual proxy, protection proxy, remote proxy

## Behavioral Patterns

- [x] **Phase 18** — Observer: publish-subscribe, event systems, decoupled notifications
- [x] **Phase 19** — Strategy: interchangeable algorithms, runtime behavior selection
- [x] **Phase 20** — Command: encapsulating requests, undo/redo, queue operations
- [x] **Phase 21** — Template Method: defining algorithm skeleton, hook methods
- [x] **Phase 22** — Iterator: traversing collections, external vs internal iteration
- [x] **Phase 23** — State: state machines, transitions, context objects
- [x] **Phase 24** — Chain of Responsibility: passing requests, middleware pipelines
- [x] **Phase 25** — Mediator: centralizing complex communications, chat rooms
- [x] **Phase 26** — Visitor: adding operations to object structures, double dispatch

## Architectural Patterns

- [x] **Phase 27** — MVC: model-view-controller, separation of concerns
- [x] **Phase 28** — MVP: model-view-presenter, testability, passive view
- [x] **Phase 29** — MVVM: model-view-viewmodel, data binding, reactive patterns
- [x] **Phase 30** — Clean Architecture: layers, dependency rule, use cases
- [x] **Phase 31** — Hexagonal Architecture: ports and adapters, pluggable infrastructure

## Concurrency Patterns

- [x] **Phase 32** — Thread Pool: resource management, worker threads, task queue
- [x] **Phase 33** — Producer-Consumer: bounded buffer, blocking queue
- [x] **Phase 34** — Read-Write Lock: concurrent reads, exclusive writes
- [x] **Phase 35** — Monitor: synchronization, condition variables, mutex

## Enterprise Patterns

- [x] **Phase 36** — Repository: data access abstraction, separation from business logic
- [x] **Phase 37** — Unit of Work: transaction management, change tracking
- [x] **Phase 38** — Specification: business rules composition, query building
- [x] **Phase 39** — Identity Map: object caching, avoiding duplicate instances
- [x] **Phase 40** — Data Transfer Object: data transport, serialization boundaries

## Anti-Patterns & Refactoring

- [x] **Phase 41** — God Object: excessive responsibilities, refactoring to single responsibility
- [x] **Phase 42** — Spaghetti Code: tangled dependencies, extracting clean layers
- [x] **Phase 43** — Golden Hammer: overusing familiar tools, recognizing when to refactor

## Pattern Selection & Trade-offs

- [x] **Phase 44** — Pattern selection: choosing the right pattern for the problem
- [x] **Phase 45** — Pattern combinations: using multiple patterns together
- [x] **Phase 46** — Performance implications: pattern overhead, profiling before optimizing
- [x] **Phase 47** — Real-world applications: patterns in Laravel, React, and production codebases

## Recommended Learning Path (priority order)

1. **Phase 1** — SOLID principles (foundation for everything)
2. **Phase 6** — Factory Method (most commonly used)
3. **Phase 15** — Facade (simplifies complex systems)
4. **Phase 18** — Observer (event-driven is everywhere)
5. **Phase 19** — Strategy (runtime flexibility)
6. **Phase 27** — MVC (architectural foundation)
7. **Phase 36** — Repository (data access pattern)

> Focus on recognizing patterns in existing code — employers hire mid-level developers who can identify, apply, and explain design patterns in real codebases.
