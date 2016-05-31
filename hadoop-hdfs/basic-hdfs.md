# Basic HDFS

**Date: May31, 2016**

### Summary
HDFS = *Hadoop Distributed File System*

HDFS is the filesystem used by hadoop and its subcomponents. It hides the complexity of having multiple disks, racks, partitions, and filesystems so that the user only thinks of the data as being stored in a single "drive".


### Nitty-gritty
We have the concept of a **cluster**, which is a network of connected computers. These computers have storage devices, processors and memory which hadoop uses to quickly process information. The HDFS is the filesystem that allows these computers to interact with the different data stored in each of these drives.

Upon storing a file, HDFS splits files into **blocks** with a **64MB** default size. These blocks are distributed with redunancy into different physical drives called **nodes**. The blocks that contigouously compose a single file does not necessarily have to be stored in the same node.

This redundancy is a feature that allows the data to be readily available even when some nodes fail. It also improves concurrency and allows the data to scale horizontally across different commodity hardware.

The **Namenode** is a node that keeps track of the locations of data blocks. Think of it as an address book for blocks. It contains a key-value pair that index the node (and rack) of the block.

Every so often (the time interval is configurable), the Namenode receives a *heartbeat* from each of the data nodes. If it does not receive a heartbeat from a data node, it assumes that the data node is dead and replaces it.

### References
1. [Hadoop Diagram](http://i.stack.imgur.com/JRM54.png)
1. [Hadoop Diagram2](https://s3.amazonaws.com/bradhedlund/2011/hadoop-network-intro/Data-Node-Read-from-HDFS.PNG)
1. Justin Abrantes

```
title - HDFS TIL
filename - basic-hdfs-til-matt.md
```
### Author:
[Joseph Matthew Marcos](https://github.com/matthewmarcos94)
