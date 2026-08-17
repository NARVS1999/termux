# Database Design Concept Hierarchy

## Foundational Concepts

1. Database — basic — ang lugar kung saan naka-store ang data nang maayos
2. Table — basic — ang hugis-grid na naglalaman ng rows at columns
3. Row — basic — ang isang record sa loob ng table
4. Column — basic — ang field na nagde-define ng uri ng data
5. Primary Key — basic — ang unique na identifier ng bawat row
6. Foreign Key — basic — ang field na nag-uugnay sa ibang table
7. Data Types — basic — ang mga uri ng data gaya ng INT, VARCHAR, DATE
8. Schema — basic — ang blueprint ng buong database structure

## Core Concepts

1. One-to-One Relationship — basic — ang isang record sa table ay may kapares sa isa lang
2. One-to-Many Relationship — basic — ang isang record ay may maraming kaugnay sa ibang table
3. Many-to-Many Relationship — intermediate — ang maraming records ay nagkakaugnay sa isa't isa
4. Junction Table — intermediate — ang junction table na nagco-connect sa many-to-many
5. Composite Key — intermediate — ang primary key na gawa sa dalawang o higit pang columns
6. Surrogate Key — basic — ang artificial na ID na hindi business data
7. Natural Key — basic — ang existing data na ginagamit bilang identifier
8. Candidate Key — intermediate — ang mga possible na pwedeng maging primary key

## Implementation Concepts

1. CREATE TABLE — basic — ang command para gumawa ng bagong table
2. ALTER TABLE — basic — ang command para mag-modify ng existing table
3. DROP TABLE — basic — ang command para tanggalin ang table
4. NOT NULL Constraint — basic — ang hindi pwedeng maging blankong field
5. UNIQUE Constraint — basic — ang hindi pwedeng mag-duplicate na value
6. DEFAULT Value — basic — ang fallback value kapag walang input
7. CHECK Constraint — intermediate — ang rule na nagva-validate ng data range
8. ENUM Type — intermediate — ang fixed na list ng allowed values
9. AUTO_INCREMENT — basic — ang awtomatikong pagtaas ng number ID
10. TIMESTAMP Fields — basic — ang auto-update na created_at at updated_at

## Integration Concepts

1. Normalization — intermediate — ang pagbawas ng data duplication sa tables
2. Denormalization — advanced — ang pagdagdag ng duplication para sa bilis ng query
3. Indexing — intermediate — ang pagpapabilis ng query gamit ang index
4. Composite Index — advanced — ang index na gumagamit ng maraming columns
5. Covering Index — advanced — ang index na nagco-cover ng buong query
6. Foreign Key Constraints — intermediate — ang integridad ng data sa pagitan ng tables
7. CASCADE Delete — intermediate — ang awtomatikong pagtanggal ng related records
8. RESTRICT Delete — intermediate — ang pagbabawal ng delete kapag may reference
9. Transactions — intermediate — ang grouping ng operations na dapat sabay-sabay
10. ACID Properties — advanced — ang garantiya ng consistency sa bawat transaction

## Architectural Concepts

1. Star Schema — intermediate — ang design na may central fact table at dimension tables
2. Snowflake Schema — advanced — ang normalized na version ng star schema
3. Data Warehouse — advanced — ang centralized na repository ng historical data
4. OLTP vs OLAP — advanced — ang pagkakaiba ng transactional at analytical processing
5. Sharding — advanced — ang paghahati ng database sa maraming servers
6. Replication — advanced — ang pag-copy ng data sa maraming instances
7. Master-Slave Architecture — advanced — ang primary at backup database setup
8. Connection Pooling — intermediate — ang pag-reuse ng database connections
9. Database Partitioning — advanced — ang paghahati ng large tables sa smaller pieces

## Design Concepts

1. Entity-Relationship Diagram — intermediate — ang visual na representation ng tables at relationships
2. Functional Dependency — intermediate — ang relasyon ng columns sa loob ng table
3. Transitive Dependency — advanced — ang indirect na dependency ng columns
4. Boyce-Codd Normal Form — advanced — ang strict na version ng 3NF
5. Denormalization Trade-offs — advanced — ang pagbalaanse ng speed at consistency
6. Slowly Changing Dimensions — advanced — ang paghawak ng nagbabago na historical data
7. Data Dictionary — basic — ang dokumentasyon ng lahat ng tables at columns
8. Naming Conventions — basic — ang consistent na pangalan ng tables at columns

## Advanced Concepts

1. Query Optimization — advanced — ang pagpapabilis ng mabagal na queries
2. EXPLAIN Plan — advanced — ang pag-analyze ng execution plan ng query
3. Index Tuning — advanced — ang pag-optimize ng index strategy
4. Partition Pruning — advanced — ang pagbawas ng scan sa tamang partitions
5. Materialized Views — intermediate — ang pre-computed na query results
6. Stored Procedures — intermediate — ang saved na logic sa database level
7. Triggers — intermediate — ang automatic na action kapag nagbago ang data
8. Cursors — advanced — ang pag-loop ng results row by row
9. Batch Processing — intermediate — ang pagproseso ng malaking data sa chunks

## Production Concepts

1. Backup Strategies — basic — ang pag-iimbak ng data copies para sa safety
2. Point-in-Time Recovery — advanced — ang pagbalik ng data sa specific na oras
3. Data Encryption — intermediate — ang pag-encrypt ng data sa storage
4. Access Control — intermediate — ang pag-limit ng user permissions sa database
5. Audit Logging — intermediate — ang pagtala ng lahat ng database changes
6. Connection Limits — intermediate — ang pag-set ng max na connections
7. Query Timeout — intermediate — ang pag-limit ng oras ng isang query
8. Deadlock Handling — advanced — ang pag-resolve ng sabay na nag-aagaw na transactions
9. Failover — advanced — ang automatic na pag-switch sa backup server

## Optimization Concepts

1. Query Caching — intermediate — ang pag-cache ng query results
2. Buffer Pool Tuning — advanced — ang pag-optimize ng memory allocation
3. Disk I/O Optimization — advanced — ang pagbawas ng disk operations
4. Compression — intermediate — ang pagliit ng data storage size
5. Archiving — intermediate — ang paglipat ng lumang data sa separate storage
6. Vacuum & Maintenance — intermediate — ang regular na paglilinis ng database
7. Statistics Update — intermediate — ang pag-update ng query optimizer data
8. Memory Configuration — advanced — ang pag-tune ng database memory settings

## Expert/Strategic Concepts

1. CAP Theorem — advanced — ang trade-offs sa distributed database systems
2. BASE Properties — advanced — ang alternative sa ACID para sa scalability
3. Eventual Consistency — advanced — ang pagtanggap ng temporary na inconsistency
4. Database Migration Strategies — advanced — ang paglipat ng database sa bagong system
5. Multi-tenancy Design — advanced — ang pag-share ng database sa maraming tenants
6. Data Governance — advanced — ang pag-manage ng data quality at compliance
7. Schema Evolution — advanced — ang pagbabago ng schema nang walang downtime
8. Database-as-a-Service — intermediate — ang paggamit ng cloud-managed databases
9. NewSQL & Distributed SQL — advanced — ang bagong approach sa scalable transactions
