# How to dump Spark SQL Outputs

**Date: May 27, 2016**

To dump Spark SQL outputs from command line interface, you can pipe the output from HDFS to the UNIX file system

- `spark-sql -f 'sql_command.sql' > sql_result.txt`

*Note: The command would be ran in Spark and based on Hive tables
