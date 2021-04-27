# Reading: Class 12

### [SQL vs NoSQL Database Differences Explained](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
*Most of you are already familiar with SQL database, and have a good knowledge on either MySQL, Oracle, or other SQL databases. In the last several years, NoSQL database is getting widely adopted to solve various business problems.*

- SQL vs NoSQL: High-Level Differences
  * SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database
  * SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores - This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to
  * SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data
  * SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable - SQL databases are scaled by increasing the horse-power of the hardware - NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load
  * SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents - *Sometimes it is also called as UnQL (Unstructured Query Language)*
  *SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb
  * For complex queries: SQL databases are good fit for the complex query intensive environment whereas NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
  * For the type of data to be stored: SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.
  * For scalability: In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.
  * For high transactional based application: SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data. While you can use NoSQL for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.
  * For support: Excellent support are available for all SQL database from their vendors. There are also lot of independent consultations who can help you with SQL database for a very large scale deployments. For some NoSQL database you still have to rely on community support, and only limited outside experts are available for you to setup and deploy your large scale NoSQL deployments.
  * For properties: SQL databases emphasizes on ACID properties ( Atomicity, Consistency, Isolation and Durability) whereas the NoSQL database follows the Brewers CAP theorem
  * For DB types: On a high-level, we can classify SQL databases as either open-source or close-sourced from commercial vendors. NoSQL databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.

- SQL Database Examples
  1. [MySQL Database](https://www.thegeekstuff.com/2008/07/howto-install-mysql-on-linux/)is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js.
    * Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application
    * Sharding: MySQL sharding os useful when there is large no of write operations in a high traffic website. By sharding MySQL servers, the application is partitioned into multiple servers dividing the database into small chunks. As low cost servers can be deployed for this purpose, this is cost effective.
    * Memcached as a NoSQL API to MySQL: Memcached can be used to increase the performance of the data retrieval operations giving an advantage of NoSQL api to MySQL server.
    * Maturity: This database has been around for a long time and tremendous community input and testing has gone into this database making it very stable.
    * Wide range of Platforms and Languages: MySql is available for all major platforms like Linux, Windows, Mac, BSD and Solaris. It also has connectors to languages like Node.js, Ruby, C#, C++, C, Java, Perl, PHP and Python.
    * Cost effectiveness: It is open source and free.

  2. MS-SQL Server Express Edition
  *It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft.*
    * Integrated Development Environment: Microsoft visual studio, Sql Server Management Studio and Visual Developer tools provide a very helpful way for development and increase the developers productivity.
    * Disaster Recovery: It has good disaster recovery mechanism including database mirroring, fail over clustering and RAID partitioning.
    * Cloud back-up: Microsoft also provides cloud storage when you perform a cloud-backup of your database
  
  3. Oracle Express Edition
  *It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment.*
    * Easy to Upgrade: Can be easily upgraded to newer version, or to an enterprise edition.
    * Wide platform support: It supports a wide range of platforms including Linux and Windows
    * Scalability: Although the scalability of this database is not cost effective as MySQL server, but the solution is very reliable, secure, easily manageable and productive.

- NoSQL Database Examples
  1. MongoDB
  Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks.
    * Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.
    * Scalability: It is horizontally scalable i.e. you can reduce the workload by increasing the number of servers in your resource pool instead of relying on a stand alone resource.
    * Manageable: It is easy to use for both developers and administrators. This also gives the ability to shard database
    * Dynamic Schema: Its gives you the flexibility to evolve your data schema without modifying the existing data

  2. CouchDB
  CouchDB is also a document based NoSQL database. It stores data in form of JSON documents. The following are some of CouchDB benefits and strengths:
    * Schema-less: As a member of NoSQL family, it also have dynamic schema which makes it more flexible, having a form of JSON documents for storing data.
    * HTTP query: You can access your database documents using your web browser.
    * Conflict Resolution: It has automatic conflict detection which is useful while in a distributed database.
    * Easy Replication: Implementing replication is fairly straight forward

  3. Redis
  Redis is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language.
  The following are some of Redis benefits and strengths:
  * Data structures: Redis provides efficient data structures to an extend that it is sometimes called as data structure server. The keys stored in database can be hashes, lists, strings, sorted or unsorted sets.
  * Redis as Cache: You can use Redis as a cache by implementing keys with limited time to live to improve the performance.
  * Very fast: It is consider as one of the fastest NoSQL server as it works with the in-memory dataset.

### [NOSQL DATA MODELING TECHNIQUES](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)
NoSQL databases are often compared by various non-functional criteria, such as scalability, performance, and consistency. This aspect of NoSQL is well-studied both in practice and theory because specific non-functional properties are often the main justification for NoSQL usage and fundamental results on distributed systems like the CAP theorem apply well to NoSQL systems.  At the same time, NoSQL data modeling is not so well studied and lacks the systematic theory found in relational databases.

First, we should note that SQL and relational model in general were designed long time ago to interact with the end user. This user-oriented nature had vast implications:
 * The end user is often interested in aggregated reporting information, not in separate data items, and SQL pays a lot of attention to this aspect.
 * No one can expect human users to explicitly control concurrency, integrity, consistency, or data type validity. That’s why SQL pays a lot of attention to transactional guaranties, schemas, and referential integrity.

On the other hand, it turned out that software applications are not so often interested in in-database aggregation and able to control, at least in many cases, integrity and validity themselves. Besides this, elimination of these features had an extremely important influence on the performance and scalability of the stores. And this was where a new evolution of data models began:
  * Key-Value storage is a very simplistic, but very powerful model. Many techniques that are described below are perfectly applicable to this model.
  * One of the most significant shortcomings of the Key-Value model is a poor applicability to cases that require processing of key ranges. Ordered Key-Value model overcomes this limitation and significantly improves aggregation capabilities.
  * Ordered Key-Value model is very powerful, but it does not provide any framework for value modeling. In general, value modeling can be done by an application, but BigTable-style databases go further and model values as a map-of-maps-of-maps, namely, column families, columns, and timestamped versions.
  * Document databases advance the BigTable model offering two significant improvements. The first one is values with schemes of arbitrary complexity, not just a map-of-maps. The second one is database-managed indexes, at least in some implementations. Full Text Search Engines can be considered a related species in the sense that they also offer flexible schema and automatic indexes. The main difference is that Document database group indexes by field names, as opposed to Search Engines that group indexes by field values. It is also worth noting that some Key-Value stores like Oracle Coherence gradually move towards Document databases via addition of indexes and in-database entry processors.
  * Graph data models can be considered as a side branch of evolution that origins from the Ordered Key-Value models. Graph databases allow one model business entities very transparently (this depends on that), but hierarchical modeling techniques make other data models very competitive in this area too. Graph databases are related to Document databases because many implementations allow one model a value as a map or document.

- General Notes on NoSQL Data Modeling
- Conceptual Techniques
- General Modeling Techniques
- Hierarchy Modeling Techniques

Bookmarked:
[Mongoose API](https://mongoosejs.com/docs/api.html#Model)
[YouTube Video - SQL vs NOSQL](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)