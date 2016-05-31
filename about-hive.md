# General Overview of Hive

**Date: 05/31/16**

Hive is non-relational database. It is a data warehouse layer built on top of Hadoop that simplifies analysis and queries. It takes polystructured data and outputs clean data that the client actually needs. Hive consists of metadata and hiveql.

Hive has SQL-ish language. It has support for most of the basic commands but lacks support for transactions and materialized view. It also has limited subquery support. Hive tables consists of data and schema. It also has support for multitable inserts. Data can be accessed with a simple query language and it supports overwriting of data. Data stored in Hbase can be accessed by Hive.

It has fast response time even when handling large data. It is scalable and extensive. Even as data grows, there is no apparant performance reduction. It is also compatible with traditional analytics tool.

It is mainly used by data analysts. It is also of great use to developers who are not well-verse in the MapReduce framework for writing queries. It operates on the server-side of any cluster and it explicitly defines its schema before data is even acquired.

####References:
- [Hortonworks](http://hortonworks.com/apache/hive/)
- [Wikipedia](https://en.wikipedia.org/wiki/Apache_Hive)
- [Difference between Pig and Hive-The Two Key Components of Hadoop Ecosystem](https://www.dezyre.com/article/difference-between-pig-and-hive-the-two-key-components-of-hadoop-ecosystem/79)
