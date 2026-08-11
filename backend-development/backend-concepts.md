# Backend Concept Hierarchy

## Foundational Concepts

1. Client-Server Model — basic — ang naghahati ng app sa client side at server side
2. Request-Response Cycle — basic — ang daloy ng tawag mula browser papunta sa server
3. HTTP Methods — basic — ang mga paraan ng pag-request gaya ng GET, POST, PUT
4. HTTP Status Codes — basic — ang mga code na nagsasabi kung success o error ang response
5. URL Routing — basic — ang pagtugma ng URL sa tamang handler o controller
6. HTTP Headers — intermediate — ang karagdagang metadata ng request at response
7. Cookies & Sessions — intermediate — ang nagpapanatili ng state sa pagitan ng requests
8. Environment Variables & Config — basic — ang mga settings na naka-store sa labas ng code
9. Git & Version Control — basic — ang nagtatala ng history ng code changes

## Core Concepts

1. Variables & Data Types — basic — ang lalagyan ng data at ang mga uri nito
2. Control Flow — basic — ang pagpapasya ng daloy ng code gamit ang if at loops
3. Functions & Scope — basic — ang reusable block ng code na may sariling saklaw
4. Strings & Text Processing — basic — ang paghawak at pag-format ng text data
5. Arrays & Collections — intermediate — ang grupo ng data na may key o index
6. Classes & Objects — intermediate — ang blueprint at instance ng isang entity
7. Encapsulation & Visibility — basic — ang pagtatago ng internal state sa public interface
8. Inheritance & Polymorphism — intermediate — ang pagmana at pagpalit ng behavior ng class
9. Interfaces & Abstract Classes — intermediate — ang kontrata ng methods na ipinapatupad ng class
10. Error Handling & Exceptions — intermediate — ang paghuli at paghawak ng errors nang maayos

## Implementation Concepts

1. Composer & Autoloading (PSR-4) — intermediate — ang naglo-load ng PHP packages at classes nang awtomatiko
2. PHP 8.x Features (enums, readonly, attributes, named arguments) — intermediate — ang mga bagong syntax para sa malinis na PHP code
3. Object-Oriented Design — intermediate — ang pagbubuo ng code gamit ang objects at responsibilities
4. SOLID Principles — advanced — ang limang prinsipyo para sa maintainable na design
5. Dependency Injection — intermediate — ang pagpasa ng dependencies imbes na gumawa ng bago
6. Composition over Inheritance — advanced — ang pagbubuo ng behavior sa pamamagitan ng objects
7. Design Patterns (Repository, Factory, Strategy, Observer) — advanced — ang mga proven na solusyon sa paulit-ulit na problema
8. Eloquent ORM & Relationships — intermediate — ang paghawak ng database tables bilang PHP objects
9. Eager Loading & N+1 Prevention — advanced — ang pag-optimize ng queries para iwasan ang extra database calls
10. Model Events & Casts — intermediate — ang mga hooks at conversion ng data sa Eloquent models
11. Query Builder — intermediate — ang paggawa ng SQL queries gamit ang PHP methods
12. Migrations & Schema Building — intermediate — ang versioned na pagbabago ng database structure
13. Seeders & Factories — basic — ang paglagay ng test data sa database nang mabilis
14. Validation & Form Requests — intermediate — ang pag-check ng input bago iproseso
15. Static Analysis (PHPStan, PHPCS) — intermediate — ang paghahanap ng bugs sa code nang hindi ito pinapatakbo

## Integration Concepts

1. RESTful API Design — intermediate — ang paggawa ng API na gumagamit ng standard na conventions
2. API Versioning — intermediate — ang paghihiwalay ng luma at bagong API endpoints
3. Pagination & Filtering — intermediate — ang paglimit ng results sa API responses
4. Authentication Mechanisms (Sanctum, Passport, JWT) — advanced — ang pag-verify kung sino ang user
5. Authorization (Roles, Policies, Gates) — advanced — ang pag-check kung may pahintulot ang user
6. OAuth2 Flows — advanced — ang pag-access ng third-party apps sa protected data
7. Webhooks & Signature Validation — advanced — ang notification mula sa ibang system na may verified signature
8. WebSockets & Broadcasting — advanced — ang real-time na komunikasyon sa pagitan ng client at server
9. Third-party API Integrations — intermediate — ang pag-connect ng app sa external services
10. Queues & Job Dispatch — intermediate — ang pagpatakbo ng mabibigat na trabaho sa background
11. Event & Listener System — intermediate — ang pag-react ng code sa mga nangyayaring events
12. Notifications & Mailables — basic — ang pagpapadala ng email at notifications sa users

## Architectural Concepts

1. Layered Architecture — intermediate — ang paghahati ng app sa presentation, business, at data layers
2. Service Layer Pattern — intermediate — ang pagsentro ng business logic sa dedicated services
3. Middleware & Request Lifecycle — intermediate — ang pagsala ng requests bago umabot sa controller
4. Service Container, Service Providers & Facades — advanced — ang registry ng dependencies ng Laravel
5. Clean Architecture — advanced — ang paghihiwalay ng business rules sa frameworks at UI
6. Modular & Multi-tenant Design — advanced — ang pagbubuo ng app bilang independent na modules
7. Design for Failure — advanced — ang paghahanda ng system sa mga posibleng breakdowns
8. Observability (Structured Logging, Monitoring, Tracing) — advanced — ang pagtingin sa loob ng tumatakbong system
9. Monolith vs Microservices — advanced — ang pagpili ng tamang deployment style ng system
10. Architecture Decision Records — basic — ang dokumentado ng mga malalaking technical decisions

## Design Concepts

1. Database Design & ER Modeling — intermediate — ang paggawa ng database structure mula sa entities
2. Normalization vs Denormalization — advanced — ang pagbalanse ng data duplication at query speed
3. Indexing Strategy (Composite, Covering) — advanced — ang pagpapabilis ng queries gamit ang tamang indexes
4. Transactions & ACID — intermediate — ang paggarantiya ng consistency sa bawat database operation
5. Query Optimization with EXPLAIN — advanced — ang pag-analyze ng execution plan ng query
6. Data Integrity & Constraints — basic — ang pagpapatupad ng valid rules sa database level
7. Caching Strategies (Cache-aside, Write-through) — advanced — ang pagpili kung saan i-store ang madalas na data
8. Cache Invalidation — advanced — ang pag-update ng cache kapag nagbago ang source data

## Advanced Concepts

1. Race Conditions & Locking — advanced — ang pagprotekta ng shared data mula sa sabay na access
2. Idempotency & Safe Retries — advanced — ang pagtiyak na hindi magdoble ang effect ng repeated requests
3. Rate Limiting & Throttling — intermediate — ang paglimit ng requests ng isang client sa isang panahon
4. Distributed Caching with Redis — advanced — ang shared cache sa labas ng app servers
5. Cache Tags & Locks — advanced — ang grupo ng cache keys at atomic na pag-update
6. Window Functions & CTEs — advanced — ang advanced SQL queries para sa analytics
7. Streaming & Long-lived Connections — advanced — ang tuloy-tuloy na data sa pagitan ng client at server
8. Async Processing & Workers — intermediate — ang parallel na pagproseso ng mga tasks
9. Resumable Jobs & Failed Job Handling — intermediate — ang pag-recover ng jobs na nabigo sa pagtakbo

## Production Concepts

1. Input Validation & Sanitization — basic — ang paglinis at pag-check ng lahat ng user input
2. CSRF & Mass Assignment Protection — intermediate — ang depensa laban sa forged requests at bulk assignment
3. Security Logging & Auditing — intermediate — ang tala ng mga security-relevant na events
4. Encryption at Rest & in Transit — intermediate — ang proteksyon ng data sa storage at sa paglipat
5. Secrets Management — intermediate — ang ligtas na pag-iimbak ng API keys at credentials
6. Error Tracking (Sentry) — basic — ang awtomatikong ulat ng exceptions sa production
7. Docker & Containers — intermediate — ang pag-encapsulate ng app kasama ang dependencies nito
8. Docker Compose & Multi-stage Builds — intermediate — ang pag-define ng maraming services sa isang file
9. CI/CD Pipelines — intermediate — ang awtomatikong test at deploy ng code changes
10. Server Administration (Nginx, PHP-FPM, Supervisor) — intermediate — ang pag-manage ng server na nagpapatakbo ng app
11. Deployment Strategies (Zero-downtime, Blue-green) — advanced — ang pag-deploy nang walang downtime
12. Load Balancers & Auto-scaling — advanced — ang pamamahagi ng traffic sa maraming servers

## Optimization Concepts

1. Performance Profiling (Debugbar, Xdebug, Telescope, Blackfire) — intermediate — ang pagsukat kung saan mabagal ang app
2. OPcache & PHP Configuration Tuning — intermediate — ang pag-optimize ng PHP runtime settings
3. HTTP Caching & Asset Optimization — intermediate — ang pagbawas ng repeat requests sa server
4. Database Query Profiling — intermediate — ang paghahanap ng mabagal na queries
5. Connection Pooling & Server Tuning — advanced — ang pag-reuse ng database connections
6. Batch Processing & Chunking — intermediate — ang pagproseso ng malalaking data sa maliliit na batches
7. Caching at Multiple Layers — advanced — ang pag-cache sa bawat antas ng system
8. Index Maintenance — advanced — ang regular na paglilinis ng database indexes

## Expert/Strategic Concepts

1. CAP Theorem & Consistency Models — advanced — ang pagpili ng tradeoffs sa distributed systems
2. Scalability Patterns (Vertical vs Horizontal) — advanced — ang pagpapalaki ng capacity ng system
3. Distributed Systems Fundamentals — advanced — ang paghawak ng maraming machines na nagtutulungan
4. Event-Driven Architecture — advanced — ang komunikasyon ng parts sa pamamagitan ng events
5. Security Hardening (OWASP Top 10) — advanced — ang pag-secure ng app laban sa karaniwang attacks
6. Threat Modeling — advanced — ang pag-identify ng posibleng pag-atake bago sila mangyari
7. SLOs & Error Budgets — intermediate — ang pag-set ng reliability targets ng system
8. Incident Response & Post-mortems — intermediate — ang paghawak at pag-aral ng production incidents
9. Performance Engineering — advanced — ang pagdisenyo ng system na mabilis mula sa simula
10. Code Review & Architecture Reviews — advanced — ang pag-validate ng quality at design ng code
