# Basic Pig

**Date: May 31, 2016**

#### Introduction on Pig

Pig is a scripting framework that runs on top of Hadoop and is able to replicate functionalities similar from SQL and Hive. It separates itself from SQL and HiveQL since its approach is procedural compared to the typical declarative.

#### Pig Components

Pig has the following components
- Pig Latin
- Grunt
- Piggybank

#### Pig Latin

Pig Latin is a high level scripting language that provides functionalities similar to the SQL functionalities such as SELECT (LOAD in Pig Latin), ORDER, UNION, etc. It allows programmers to create query statements similar to the syntaxes to the typical high level procedural languages.

Below are two examples on how we use Pig Latin, specifically on getting data and combining two data sets.

###### Getting data

```

data1 = LOAD `somefile.txt`;
DUMP data1;

```

###### Data Union

```

data1 = LOAD `somefile1.txt`;
data2 = LOAD `somefile2.txt`;
out1  = UNION data1, data2;
DUMP out1;

```

#### Grunt

Grunt is a shell for Pig. Basically, what Grunt does is that it allows Pig Latin commands to be executed in the shell.

#### Piggybank

Piggybank is a collection of user-defined functions for Pig Latin.

#### References

- [Pig Latin Reference Manual](https://pig.apache.org/docs/r0.7.0/piglatin_ref2.html#LOAD)
- [Pig Latin Basics](https://pig.apache.org/docs/r0.11.1/basic.html)
- [Apache Pig](http://hortonworks.com/apache/pig/)
- [Piggybank](https://cwiki.apache.org/confluence/display/PIG/PiggyBank)
- [Exploring Data with Apache Pig from the Grunt Shell](http://hortonworks.com/hadoop-tutorial/exploring-data-apache-pig-grunt-shell/)

#### Author

Almer Mendoza
