# BASIC HIVE VS PIG TIL

**Date: May 31, 2016**

### Summary
- Pig and Hive are both components of Hadoop that take advantage of HDFS.
- Pig and Hive are both used to filter and "query" data from the HDFS, before it is processed by MapReduce.

### nitty-gritty
- Pig imposes a "schema" on the data on read.
- Hive imposes a "schema" when the data is being written on HDFS with something similar to DDL.
- Hive is aimed at SQL users, therefore its syntax is similar to SQL.
- Hive is used as a "coaguation" of different data sources, integrating different data types into its own (ex: varchar and char and varchar(40) are stored as a string with HQL)
- It is better to use Pig if you intend to have muliple processes when "selecting" your data.
- Pig is better if you want to "filter" data while Hive is better if you want to "join" data from different sources?? (gray area)


### Not so sure
- Pig Latin (language of pig) is like having a stored procedure that performs multiple operations on a database before returning the data, while Hive is like having a super complicated nested query for the database that also does the same thing, but is just in a different form.

### References:
[Hive vs PIG](https://www.dezyre.com/article/difference-between-pig-and-hive-the-two-key-components-of-hadoop-ecosystem/79)
[Quora](https://www.quora.com/What-is-main-differences-between-hive-vs-pig-vs-sql)
[Stack Overflow](http://stackoverflow.com/questions/3356259/difference-between-pig-and-hive-why-have-both)

```
title - HIVE VS PIG TIL
filename - hive-vs-pig.md
```

### Author:
[Joseph Matthew Marcos](https://github.com/matthewmarcos94)
