# Aggressiveness of NameNode in block replication

**Date: Feb 23, 2016**

When you want your NameNode to increase the speed of replicating under-replicated blocks you can tweak these options

- `dfs.datanode.balance.bandwidthPerSec`
- `dfs.namenode.replication.max-streams`
- Datanode Java HeapSize

*Note: The NameNode and DataNodes will consume more RAM/CPU when you set this*