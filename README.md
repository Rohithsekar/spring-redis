# Spring Data Redis Demo Project

## This springboot project is aimed to demonstrate the use cases of Redis - an in-memory data structure keystore.
## Redis Overview
> Redis (Remote Dictionary Server) is an in-memory data structure store that can be used as a 
> database, cache, message broker, and streaming engine. It's known for its blazing speed (sub-millisecond latency) 
> since all data resides in RAM.

## **Abstraction Philosophy:** <br>
  Redis follows a  **data structure-centric approach** rather than a traditional **table-based database model**. Instead of organizing data in tables and rows, Redis provides native data structures:

+ Strings - simple key-value pairs
+ Hashes - field-value pairs (like objects/maps)
+ Lists - ordered collections
+ Sets - unordered unique collections
+ Sorted Sets - sets with scores for ordering
+ Bitmaps, HyperLogLogs, Streams, Geospatial indexes

This philosophy means you model your data around these structures rather than normalizing into tables.
You think in terms of "what operations do I need?" rather than "what queries will I write?". Redis provides 
atomic operations on these structures, making it powerful for concurrent scenarios.

## **Spring Boot Support:** <br>
Spring Boot integrates Redis through Spring Data Redis, which provides:

* RedisTemplate - low-level operations with full control
* StringRedisTemplate - specialized for string operations
* Repository abstraction - JPA-like interface for Redis entities
* Caching abstraction - declarative caching with @Cacheable, @CacheEvict, etc.
* Session management - distributed sessions via Spring Session
* Pub/Sub messaging - message listener containers

###  Redis primary use cases include:
* Session Storage - distributed sessions across microservices
* Real-time Analytics - counters, metrics, leaderboards using sorted sets
* Rate Limiting - API throttling with expiring keys
* Message Queue/Pub-Sub - lightweight message broker for event-driven systems
* Geospatial Applications - location-based queries (nearby places)
* Real-time Leaderboards - gaming scores with sorted sets
* Distributed Locks - coordination across distributed systems
* Full-text Search - with RediSearch module
* Time-series Data - metrics and monitoring with Redis Streams
* Job Queues - background job processing
* Autocomplete/Typeahead - search suggestions
* Unique Visitor Tracking - HyperLogLog for cardinality estimation
* Shopping Cart - e-commerce temporary cart storage
  