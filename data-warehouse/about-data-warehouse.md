# Data Warehouse Overview

**Date: June 29, 2016**

A data warehouse is a relational database designed for query and analysis. It basically helps in the analysis of data. It makes use of ETL (Extract-Transform-Load) process, OLAP (Online Analytical Processing) engines and other tools that help in the management of data.

#### Characteristics
- Subject-Oriented
    - The ability to define what the data warehouse contains
- Integrated
    - Data has a consistent format therefore there are no problems regarding data inconsistency
- Nonvolatile
    - Data entered into the warehouse cannot be changed
- Time Variant
    - The ability to store historical data

#### Requirements
- Workload
    - Designed to accommodate ad hoc queries
- Data modification
    - It is updated on a regular basis by the ETL process
- Schema Design
    - Uses denormalized or partially denormalized schema for optimized performance
- Typical Operations
    - A typical data warehouse query scans thousands or millions of rows
- Historical Data
    - Stores years worth of data for historical analysis

#### References:
- [Oracle Documentation](https://docs.oracle.com/cd/B10501_01/server.920/a96520/concept.htm#50413)
