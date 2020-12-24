# Redis（基于内存的缓存数据库）

### NoSQL概述

NoSQL(NoSQL=Not Only SQL)，意即“不仅仅是SQL”，泛指非关系型的数据库。

-   NoSQL不依赖业务逻辑方式存储，而以简单的key-value模式存储。因此大大的增加了数据库的扩展能力。

-   不遵循SQL标准。

-   不支持ACID。

-   远超于SQL的性能。

### NoSQL适用场景

-   对数据高并发的读写

-   海量数据的读写

-   对数据高可扩展性的

### NoSQL不适用场景

-   需要事务支持

-   基于sql的结构化查询存储，处理复杂的关系，需要即席查询。

# Redis简介

Redis是一个开源的key-value存储系统。和Memcached类似，它支持存储的value类型相对更多，包括string(字符串）、list(链表）、set(集合）、zset(sorted set--有序集合）和hash(哈希类型）。这些数据类型都支持push/pop、add/remove及取交集并集和差集及更丰富的操作，而且这些操作都是原子性的。在此基础上，Redis支持各种不同方式的排序。与memcached一样，为了保证效率，数据都是缓存在内存中。区别的是Redis会周期性的把更新的数据写入磁盘或者把修改操作写入追加的记录文件，并且在此基础上实现了master-slave(主从）同步。

配合关系型数据库做高速缓存
高频次，热门访问的数据（热点数据），降低数据库IO
分布式架构，做session共享


