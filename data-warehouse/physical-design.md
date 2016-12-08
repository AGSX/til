# Data Warehouse: Physical Design

**Date: June 29, 2016**

### Physical Design

Taking ways and effectivity of storage into consideration.

#### Structures

###### Tablespaces

Tablespaces are container of Physical Design structures.

###### Tables and partitioned tables

Tables and Partioned Tables are container of raw data. They are the basic unit of storage.

###### Data Segment Compression

Ensures that speed and time spent on execution queries must increase and decrease, respectively.

###### Views

Visualizes data using tables.

###### Integrity Constraints

Adds rules on data manipulation to avoid invalid information.

###### Dimensions

Schema object defining relationships between fields.

###### Materialized Views

Does advance calculations and creates summaries to avoid expensive aggregate operations.

###### Indexes and Partitioned Indexes

Use of indexes to further partition table. Usuaully uses binary digit to signify on what category (or if it is part of the table category).

### References
- [Oracle9i Data Warehousing Guide](https://docs.oracle.com/cd/B10501_01/server.920/a96520/toc.htm)
- [Intricity101 videos](https://www.youtube.com/user/Intricity101/videos)

### Author

Almer Mendoza
