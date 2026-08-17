# Laravel Concept Hierarchy

## Foundational Concepts

1. Laravel Framework — basic — ang PHP framework na may elegant syntax
2. MVC Pattern — basic — ang paghihiwalay ng model, view, at controller
3. Routing — basic — ang pagtugma ng URL sa tamang handler
4. Controllers — basic — ang nagha-handle ng incoming requests
5. Views — basic — ang HTML templates na nagre-render ng UI
6. Models — basic — ang representation ng database table
7. Middleware — basic — ang filter ng requests bago umabot sa controller
8. Service Container — basic — ang central na registry ng dependencies

## Core Concepts

1. Eloquent ORM — intermediate — ang paghawak ng database bilang PHP objects
2. Migrations — intermediate — ang versioned na pagbabago ng database structure
3. Seeders — basic — ang paglagay ng test data sa database
4. Factories — intermediate — ang paggawa ng fake data para sa testing
5. Blade Templating — intermediate — ang templating engine ng Laravel
6. Configuration Files — basic — ang mga settings ng application
7. Environment Variables — basic — ang sensitive na data sa .env file
8. Artisan Console — basic — ang command-line tool ng Laravel

## Implementation Concepts

1. Eloquent Relationships — intermediate — ang hasOne, hasMany, belongsTo at iba pa
2. Eager Loading — advanced — ang pag-optimize ng queries para iwasan N+1
3. Query Builder — intermediate — ang paggawa ng SQL gamit ang PHP methods
4. Form Requests — intermediate — ang dedicated na validation ng incoming data
5. API Resources — intermediate — ang pag-transform ng models para sa API response
6. Route Model Binding — intermediate — ang awtomatikong pag-inject ng model sa route
7. Service Providers — intermediate — ang nagbo-boot ng lahat ng services ng app
8. Facades — intermediate — ang static-like access sa services sa container
9. Event Listeners — intermediate — ang pag-react sa events ng application
10. Notifications — basic — ang pagpapadala ng alerts sa users

## Integration Concepts

1. Authentication (Sanctum) — intermediate — ang pag-verify ng user identity
2. Authorization (Policies & Gates) — advanced — ang pag-check ng user permissions
3. API Authentication — advanced — ang token-based na authentication para sa APIs
4. Mail & Mailables — intermediate — ang pagpapadala ng emails
5. Queue System — intermediate — ang background processing ng heavy tasks
6. Job Batches — advanced — ang pag-group ng maraming jobs para sa tracking
7. Task Scheduling — intermediate — ang awtomatikong pagpapatakbo ng cron jobs
8. Broadcasting — intermediate — ang real-time na communication sa clients
9. WebSockets — advanced — ang persistent na connection sa server
10. Third-party Integrations — intermediate — ang pag-connect sa external services

## Architectural Concepts

1. Service Layer — intermediate — ang pag-centralize ng business logic
2. Repository Pattern — advanced — ang paghihiwalay ng data access sa business logic
3. Action Classes — intermediate — ang paghiwalay ng logic sa maliit na classes
4. DTOs — intermediate — ang pag-pass ng data sa structured na objects
5. Clean Architecture — advanced — ang paghihiwalay ng layers ng application
6. Modular Design — advanced — ang pagbubuo ng app bilang independent modules
7. Multi-tenancy — advanced — ang pag-manage ng maraming tenants sa iisang app
8. Microservices with Laravel — advanced — ang pag-split ng app sa smaller services

## Design Concepts

1. Database Design — intermediate — ang paggawa ng efficient na table structure
2. Normalization — intermediate — ang pagbawas ng data duplication
3. Indexing Strategy — advanced — ang pagpapabilis ng database queries
4. Caching — intermediate — ang pag-cache ng madalas na data
5. Cache Invalidation — advanced — ang pag-update ng cache kapag nagbago ang data
6. Rate Limiting — intermediate — ang pag-limit ng API requests
7. Pagination — intermediate — ang paghahati ng results sa pages
8. Search Implementation — intermediate — ang paggawa ng search functionality

## Advanced Concepts

1. Race Conditions — advanced — ang pagprotekta ng shared data mula sa concurrent access
2. Idempotency — advanced — ang pagtiyak na hindi magdoble ang effect ng repeated requests
3. Distributed Locking — advanced — ang locking sa multiple servers
4. Event Sourcing — advanced — ang pag-record ng lahat ng changes bilang events
5. CQRS — advanced — ang paghihiwalay ng read at write operations
6. Domain-Driven Design — advanced — ang pag-model ng business domain sa code
7. Hexagonal Architecture — advanced — ang paghihiwalay ng core logic sa infrastructure
8. Testing Strategies — intermediate — ang pag-test ng unit, feature, at integration

## Production Concepts

1. Error Handling — intermediate — ang paghawak ng exceptions nang maayos
2. Logging — intermediate — ang pagtala ng important events
3. Security Best Practices — intermediate — ang pag-secure ng application
4. CSRF Protection — basic — ang depensa laban sa forged requests
5. SQL Injection Prevention — basic — ang pag-iwas ng SQL injection attacks
6. XSS Prevention — basic — ang pag-iwas ng cross-site scripting
7. Authentication Guards — intermediate — ang pag-manage ng multiple auth systems
8. Password Hashing — basic — ang pag-encrypt ng passwords

## Optimization Concepts

1. Query Optimization — advanced — ang pagpapabilis ng mabagal na queries
2. N+1 Problem Detection — intermediate — ang paghahanap ng hindi optimized na queries
3. Database Profiling — intermediate — ang pag-analyze ng query performance
4. OPcache — intermediate — ang caching ng compiled PHP scripts
5. Queue Optimization — intermediate — ang pag-optimize ng background jobs
6. Memory Management — advanced — ang pagbawas ng memory usage
7. Asset Optimization — intermediate — ang pag-combine at minify ng CSS at JS
8. CDN Integration — intermediate — ang paggamit ng content delivery network

## Expert/Strategic Concepts

1. Laravel Internals — advanced — ang loob ng framework kung paano ito gumagana
2. Custom Service Providers — advanced — ang paggawa ng sariling service provider
3. Package Development — advanced — ang pagbubuo ng reusable na packages
4. Performance Engineering — advanced — ang pag-optimize ng buong application
5. Scalability Patterns — advanced — ang pagpapalaki ng application capacity
6. Infrastructure as Code — advanced — ang pag-manage ng infrastructure gamit ang code
7. CI/CD Pipelines — intermediate — ang awtomatikong test at deploy
8. Blue-Green Deployment — advanced — ang zero-downtime na deployment strategy
9. Load Balancing — advanced — ang pag-distribute ng traffic sa maraming servers
