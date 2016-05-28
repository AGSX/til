# Setting the log-level of the HDFS Filesystem Shell

**Date: May 27, 2016**

You can set the log level of the HDFS Command Line Client through this argument:

```
hdfs --loglevel TRACE dfs -ls /
```

The options would be default Log4J log levels: INFO, DEBUG, WARN, ERROR, TRACE
