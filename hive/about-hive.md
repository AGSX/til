# General Overview of Hive

**Date: 05/31/16
  
YARN in a nutshell is basically just the processing component of Hadoop. 

It handles operations, security, and data governance. It extends the power of Hadoop to all other technologies within the system.

It is the JobTracker of the entire system that performs two functionalities: resource management and job scheduling/monitoring.

YARN is often called the Operating System of Hadoop because it enhances the Hadoop cluster by providing multi-tenancy, cluster utilization, scalability and compatibility. It allows multiple engines to use Hadoop to simultaneously access the same data. It improves the MapReduce model by providing multiple processing. This is actually its most significant benefit because we are no longer limited to the I/O intensive and high latency MapReduce framework. It expands scalability to manage more and more data and is also developed as to not interfere with any running applications.

YARN generally works hand-in-hand with HDFS as seen in the image:
![YARN and HDFS](http://d287f0h5fel5hu.cloudfront.net/blog/wp-content/uploads/2013/10/Hadoop-2.0-Intro-Blog2.jpg)

####Resources:
1. http://www.tomsitpro.com/articles/hadoop-2-vs-1,2-718.html
2. http://hortonworks.com/apache/yarn/
