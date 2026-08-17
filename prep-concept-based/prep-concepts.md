# Backend/Laravel Interview Prep Concept Hierarchy

## Foundational Concepts

1. PHP 8.x Enums — basic — mga named constants na may associated values
2. PHP 8.x Readonly Properties — basic — properties na hindi pwedeng i-change after init
3. PHP 8.x Named Arguments — basic — pag-pass ng arguments gamit ang parameter name
4. PHP 8.x Match Expression — basic — stricter version ng switch na may loose comparison
5. PHP 8.x Attributes — basic — metadata syntax para sa classes, methods, properties
6. Composer Autoloading — basic — auto-loading ng classes gamit ang PSR-4
7. Type Declarations — basic — pag-specify ng data type sa function parameters at return
8. Exception Handling Basics — basic — try-catch-finally block for error handling

## Core Concepts

1. SOLID: Single Responsibility — basic — isang class, isang responsibility lang
2. SOLID: Open/Closed — intermediate — open for extension, closed for modification
3. SOLID: Liskov Substitution — intermediate — subtypes dapat mag-substitute ng parent nila
4. SOLID: Interface Segregation — intermediate — maliit na interfaces kaysa isang malaki
5. SOLID: Dependency Inversion — intermediate — depend sa abstraction, hindi sa concrete class
6. Repository Pattern — intermediate — abstraction layer para sa data access
7. Factory Pattern — intermediate — pag-create ng objects without specifying exact class
8. Strategy Pattern — intermediate — pag-swappable ng algorithms at runtime
9. Observer Pattern — intermediate — one-to-many dependency na nagno-notify ng changes
10. Adapter Pattern — intermediate — interface conversion para mag-work ang incompatible classes
11. Facade Pattern — intermediate — simple interface para sa complex subsystem

## Implementation Concepts

1. Service Container — intermediate — Laravel's IoC container for dependency injection
2. Service Providers — intermediate — bootstrap at register services sa application
3. Facades — basic — static-like access sa services sa container
4. Middleware — intermediate — layers na nagpo-process ng HTTP requests
5. Pipeline Pattern — intermediate — pag-chain ng handlers sa sequential manner
6. Request Lifecycle — intermediate — kung paano gumagana ang request from entry to response
7. Eloquent Relationships — intermediate — hasOne, hasMany, belongsTo, belongsToMany
8. Eloquent Eager Loading — intermediate — pag-load ng related models to avoid N+1
9. N+1 Problem — intermediate — inefficient queries na naglo-load ng related data
10. Model Events — intermediate — boot, creating, created, updating, updated hooks
11. Model Casts — intermediate — auto-casting ng attributes sa specified types
12. Query Scopes — intermediate — reusable query logic na naka-attach sa model

## Integration Concepts

1. Query Builder — intermediate — fluent interface para sa database queries
2. Database Transactions — intermediate — pag-wrap ng operations na dapat sabay mag-fail
3. Query Locking — advanced — pessimistic at optimistic locking strategies
4. EXPLAIN Analysis — advanced — pag-analyze ng query execution plan
5. Queues & Jobs — intermediate — pag-async ng tasks para sa background processing
6. Task Scheduling — intermediate — pag-run ng commands gamit ang scheduler
7. Events & Listeners — intermediate — loose coupling sa communication ng components
8. Notifications — basic — pag-send ng alerts via mail, database, broadcast
9. Mailables — intermediate — pag-configure ng email templates at sending
10. File Storage — intermediate — local, S3, at other disk drivers

## Architectural Concepts

1. Service Container Binding — intermediate — singleton, bind, instance registration
2. Service Provider Boot vs Register — intermediate — tamang phase ng registration
3. Facade Mechanics — intermediate — kung paano nag-resolve ang static calls
4. Pipeline Middleware Chaining — advanced — pag-order at pag-compose ng middleware
5. Eloquent Model Inheritance — advanced — STI vs class-based model design
6. Database Normalization — intermediate — 1NF, 2NF, 3NF at Boyce-Codd
7. Database Denormalization — intermediate — deliberate duplication para sa performance
8. Indexing Strategy — advanced — composite, partial, at covering indexes
9. Window Functions — advanced — ROW_NUMBER, RANK, LEAD, LAG sa SQL
10. Common Table Expressions — advanced — WITH clause para sa recursive queries
11. JSON Columns — intermediate — pag-store ng structured data sa database

## Design Concepts

1. Migrations — intermediate — version-controlled database schema changes
2. Seeders — basic — pag-populate ng test data sa database
3. Factories — intermediate — pag-generate ng fake model instances
4. Data Integrity — intermediate — constraints, foreign keys, at validation rules
5. Cache-Aside Pattern — intermediate — application manages cache reads at writes
6. Write-Through Cache — intermediate — cache updated kasabay ng database write
7. Cache Invalidation — advanced — tamang timing ng pag-clear ng cached data
8. Cache Tags — intermediate — granular cache management gamit ang tags
9. Distributed Locks — advanced — cross-instance cache locking strategies
10. Rate Limiting — intermediate — pag-limit ng requests per time window
11. HTTP Caching — intermediate — ETag, Cache-Control, at Last-Modified headers
12. OPcache — intermediate — bytecode caching para sa PHP performance

## Advanced Concepts

1. RESTful Conventions — intermediate — proper HTTP methods, status codes, at URIs
2. API Versioning — intermediate — strategies para sa backward compatibility
3. Pagination — basic — offset, cursor-based, at infinite scroll
4. Filtering & Sorting — intermediate — query parameter patterns para sa data retrieval
5. Sanctum — intermediate — token-based auth para sa SPAs at mobile apps
6. Passport — advanced — OAuth2 server implementation para sa Laravel
7. JWT — intermediate — stateless auth tokens na may expiry
8. OAuth2 Flows — advanced — authorization code, client credentials, at PKCE
9. Idempotency Keys — advanced — pag-prevent ng duplicate operations
10. Webhooks — intermediate — event-driven HTTP callbacks sa external systems
11. OWASP Top 10: XSS — intermediate — cross-site scripting prevention techniques
12. OWASP Top 10: SQLi — intermediate — SQL injection prevention at parameter binding
13. OWASP Top 10: CSRF — intermediate — cross-site request forgery tokens
14. OWASP Top 10: SSRF — advanced — server-side request forgery prevention
15. OWASP Top 10: IDOR — intermediate — insecure direct object reference prevention
16. Mass Assignment — intermediate — guarded vs fillable attribute protection

## Production Concepts

1. AuthN vs AuthZ — intermediate — authentication vs authorization distinction
2. Roles & Permissions — intermediate — Spatie, policies, at gates implementation
3. Policies — intermediate — authorization logic per model or action
4. Gates — intermediate — closure-based authorization checks
5. Secrets Management — intermediate — env files, vault, at key rotation
6. Encryption — intermediate — encrypt at decrypt ng sensitive data
7. Logging — basic — structured logging at log levels
8. Auditing — intermediate — pag-track ng model changes at user actions
9. Validation — intermediate — Form Requests at inline validation rules
10. Unit Testing — intermediate — testing individual methods at isolation
11. Feature Testing — intermediate — testing complete user workflows
12. Integration Testing — intermediate — testing component interactions
13. PHPUnit/Pest — intermediate — testing frameworks para sa PHP
14. TestCase & RefreshDatabase — intermediate — test isolation at clean state
15. Mocking & Fakes — advanced — replacing dependencies sa tests
16. HTTP Testing — intermediate — simulating API requests at assertions

## Optimization Concepts

1. TDD — intermediate — test-driven development workflow
2. Coverage Reports — intermediate — pag-measure ng test coverage percentage
3. CI Integration — intermediate — automated tests sa pipeline
4. Retries & Circuit Breakers — advanced — pag-handle ng transient failures
5. Graceful Degradation — advanced — fallback behavior kapag bumagsak ang service
6. Observability — intermediate — logging, monitoring, at alerting strategies
7. Sentry Integration — intermediate — error tracking at performance monitoring
8. Profiling Tools — intermediate — Blackfire, Telescope, at debug bar
9. Query Optimization — advanced — indexing, eager loading, at query rewriting
10. Cache Warming — advanced — preloading ng cache before first request
11. Connection Pooling — advanced — pag-manage ng database connections efficiently

## Expert/Strategic Concepts

1. Layered Architecture — advanced — separation ng concerns sa presentation, business, data
2. Service Layer Pattern — advanced — centralized business logic sa services
3. Clean Architecture — advanced — dependency rule at concentric circles
4. Refactoring Patterns — intermediate — code smell identification at improvement
5. Tech Debt Management — intermediate — prioritization ng code improvements
6. Code Review Best Practices — intermediate — effective feedback at knowledge sharing
7. Multi-Tenant Architecture — advanced — shared database vs database-per-tenant
8. Modular Architecture — advanced — package-based code organization
9. Git Workflow — intermediate — branching strategies at merge conflict resolution
10. CI/CD Pipelines — intermediate — automated build, test, at deployment
11. Docker & docker-compose — intermediate — containerization ng applications
12. Nginx & PHP-FPM — advanced — web server at process manager configuration
13. Supervisor — intermediate — process management para sa queue workers
14. Deployment Strategies — advanced — blue-green, rolling, at canary deployments
15. Cloud Basics — intermediate — AWS/GCP fundamentals para sa Laravel apps
