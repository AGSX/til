# Reading and Using JStat to Read Java Heap Usage and Java GC

**Date: (March 30, 2016)**

Most Hadoop Components are made out of Java. Sometimes they won't have a straightforward way of telling you how much heap they're using, or if they don't have GC logs, they might already be experiencing Full GC's. This is useful if, for example, a high impacting component such as Kafka is behaving weirdly.

First off, to understand how GC's work, read up on [understanding how java garbage collection works](http://www.cubrid.org/blog/dev-platform/understanding-java-garbage-collection/).

Next is to actually get GC data. You can do this by running `jstat -gc <pid>`. To get the java pid, you can run `jps` on the command line to list all the pid's of the java processes.

A caveat though, you must use the user that was used to launch the java process. For example, you can see which user through the `ps` command, ex. `ps aux | grep kafka`.

Example: I want to read the jstat values of the Kafka Broker running on my machine

    user  $ ps aux | grep kafka
    kafka   1002   0.0  0.2  2568016  17232   ??  S     7:58AM   0:00.33 java /kafka/path

    # I see that the user "kafka" was used to launch this java process
    user  $ sudo su kafka
    
    kafka $ jps
    1002 kafka
    1001 jps
    
    kafka $ jstat -gc 1002
     S0C    S1C    S0U    S1U      EC       EU        OC         OU       PC     PU    YGC     YGCT    FGC    FGCT     GCT
    500.0 500.0 500.0  0.0   5000.0 5000.0  100000.0  100000.0  50000.0 2500.0  5000 500.0 500   100.500 100.500
    
The meaning of these values are taken from [this article](http://karunsubramanian.com/java/5-not-so-easy-ways-to-monitor-the-heap-usage-of-your-java-application/), 

- S0C  Current survivor space 0 capacity (KB)
- S1C  Current survivor space 1 capacity (KB)
- S0U  Survivor space 0 utilization (KB)
- S1U  Survivor space 1 utilization (KB)
- EC  Current eden space capacity (KB)
- EU  Eden space utilization (KB)
- OC  Current old space capacity (KB)
- OU  Old space utilization (KB)
- PC  Current permanent space capacity (KB)
- PU  Permanent space utilization (KB)
- YGC  Number of young generation GC Events
- YGCT  Young generation garbage collection time
- FGC  Number of full GC events
- FGCT  Full garbage collection time
- GCT  Total garbage collection time
    
### Java Usage

Just add the following values:

OU + PU + EU + S0U  + S1U = Total Utilization

### Java GC

Watch out for the FGC, FGCT and GCT values. If they grow too quickly, somethings wrong with the Garbage Collection.