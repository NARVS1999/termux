# PHP Concept Hierarchy

## Foundational Concepts

1. PHP Syntax — basic — ang opening at closing tags, semicolons, at structure
2. Variables — basic — ang lalagyan ng data gamit ang $ symbol
3. Data Types — basic — ang mga uri ng data gaya ng string, int, float, boolean
4. Operators — basic — ang mga symbol para sa math, comparison, at logical
5. echo & print — basic — ang pag-output ng data sa browser
6. Comments — basic — ang mga notes na hindi pinapatakbo
7. Include & Require — basic — ang pag-import ng ibang PHP files
8. Superglobals — basic — ang built-in na variables gaya ng $_GET, $_POST

## Core Concepts

1. Control Structures — basic — ang if, else, elseif para sa pagpapasya
2. Loops — basic — ang for, while, foreach para sa paulit-ulit na code
3. Functions — basic — ang reusable block ng code na may parameter at return
4. Scope — intermediate — ang visibility ng variables sa iba't ibang parte
5. Arrays — basic — ang indexed at associative na list ng values
6. Array Functions — intermediate — ang map, filter, array_merge at iba pa
7. String Functions — intermediate — ang strlen, strpos, substr at iba pa
8. Math Functions — basic — ang abs, round, ceil, floor at iba pa

## Implementation Concepts

1. Classes & Objects — intermediate — ang blueprint at instance ng entity
2. Properties & Methods — intermediate — ang data at behavior ng class
3. Constructors — basic — ang special na method na tumatakbo kapag nag-create ng object
4. Inheritance — intermediate — ang pagmana ng properties at methods sa parent class
5. Interfaces — intermediate — ang kontrata ng methods na ipinapatupad ng class
6. Abstract Classes — intermediate — ang partial na implementation na hindi pwedeng i-instantiate
7. Traits — intermediate — ang reusable na code na hindi gumagamit ng inheritance
8. Namespaces — intermediate — ang pag-organize ng classes sa logical groups
9. Autoloading — intermediate — ang awtomatikong pag-load ng classes kapag kailangan
10. Error Handling — intermediate — ang paghuli at paghawak ng errors gamit ang try-catch

## Integration Concepts

1. File Handling — intermediate — ang pagbasa at pag-write ng files
2. Database Connection — intermediate — ang pag-connect sa MySQL gamit ang PDO
3. Prepared Statements — intermediate — ang ligtas na pag-query ng database
4. Sessions — intermediate — ang pag-iimbak ng data sa server para sa user
5. Cookies — basic — ang pag-iimbak ng data sa browser
6. HTTP Headers — intermediate — ang pag-set ng response headers
7. JSON Encoding/Decoding — basic — ang pag-convert ng data sa JSON format
8. Regular Expressions — intermediate — ang pattern matching sa strings
9. Date & Time — basic — ang paghawak ng timestamps at dates
10. Email Sending — intermediate — ang pagpapadala ng emails gamit ang PHPMailer

## Architectural Concepts

1. MVC Pattern — intermediate — ang paghihiwalay ng model, view, at controller
2. Singleton Pattern — intermediate — ang class na may isang instance lang
3. Factory Pattern — intermediate — ang class na nagre-create ng objects
4. Repository Pattern — advanced — ang paghihiwalay ng data access sa business logic
5. Dependency Injection — intermediate — ang pagpasa ng dependencies sa class
6. Service Layer — intermediate — ang pag-centralize ng business logic
7. Repository Pattern — advanced — ang abstraction ng data source
8. SOLID Principles — advanced — ang limang prinsipyo para sa maintainable na code

## Design Concepts

1. Database Design — intermediate — ang paggawa ng efficient na table structure
2. Normalization — intermediate — ang pagbawas ng data duplication
3. Indexing — intermediate — ang pagpapabilis ng database queries
4. Transactions — intermediate — ang pag-group ng related database operations
5. Query Optimization — advanced — ang pagpapabilis ng mabagal na queries
6. Caching — intermediate — ang pag-cache ng madalas na data
7. API Design — intermediate — ang paggawa ng RESTful API
8. Error Handling Strategy — intermediate — ang pag-setup ng error handling system

## Advanced Concepts

1. Generators — advanced — ang memory-efficient na iteration
2. Fibers — advanced — ang concurrent na execution sa PHP
3. Reflection API — advanced — ang pag-analyze ng classes at methods runtime
4. Composer — intermediate — ang package manager ng PHP
5. PSR Standards — intermediate — ang coding standards ng PHP community
6. Static Analysis — intermediate — ang paghahanap ng bugs nang hindi pinapatakbo
7. Code Quality Tools — intermediate — ang PHPStan, PHP-CS-Fixer at iba pa
8. Performance Profiling — intermediate — ang pag-analyze ng PHP performance

## Production Concepts

1. Security Best Practices — intermediate — ang pag-secure ng PHP applications
2. Input Validation — basic — ang pag-check ng lahat ng user input
3. SQL Injection Prevention — basic — ang pag-iwas ng SQL injection attacks
4. XSS Prevention — basic — ang pag-iwas ng cross-site scripting
5. CSRF Protection — basic — ang depensa laban sa forged requests
6. Password Hashing — basic — ang pag-encrypt ng passwords gamit ang password_hash
7. Encryption — intermediate — ang pag-encrypt ng sensitive data
8. Logging — intermediate — ang pagtala ng important events

## Optimization Concepts

1. OPcache — intermediate — ang caching ng compiled PHP scripts
2. Memory Management — intermediate — ang pagbawas ng memory usage
3. Profiling — intermediate — ang pag-analyze ng slow code
4. Database Optimization — intermediate — ang pag-optimize ng database queries
5. Caching Strategies — intermediate — ang pagpili ng tamang caching approach
6. Asset Optimization — intermediate — ang pag-combine at minify ng files
7. Load Testing — intermediate — ang pag-test ng application under load
8. Code Optimization — intermediate — ang pagbawas ng unnecessary operations

## Expert/Strategic Concepts

1. PHP Internals — advanced — ang loob ng PHP engine kung paano ito gumagana
2. Extension Development — advanced — ang paggawa ng sariling PHP extensions
3. Zephir & PHP Extensions — advanced — ang paggawa ng C-level na extensions
4. PHP 8.x Features — intermediate — ang enums, readonly, named arguments at iba pa
5. Modern PHP Patterns — intermediate — ang mga bagong patterns sa PHP development
6. Microservices with PHP — advanced — ang pag-split ng app sa smaller services
7. Event-Driven Architecture — advanced — ang communication gamit ang events
8. Domain-Driven Design — advanced — ang pag-model ng business domain sa code
9. Hexagonal Architecture — advanced — ang paghihiwalay ng core logic sa infrastructure
