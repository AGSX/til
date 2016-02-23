# Container Spawn Problems with YARN

**Date: Feb 23, 2016**

This is a ever-updating exhaustive checklist revolving around container spawn problems with YARN

### Decommissioned Data Nodes

Most default installations co-located NodeManagers with DataNodes. When you have a Decommissioned DataNode and your ApplicationMaster is set to request containers on node-local/rack-local containers, it will not place any containers on NodeManagers with Decommissioned Datanodes.

To resolve this, recommission your datanode. 

Note: Namenode will slowly replicate the blocks there. Do not assume that YARN will spawn containers correctly on the get-go. It will spawn containers based on the amount of blocks that have already been replicated there.

### Data Locality

On HDP-2.3.4, if your NodeManagers are not co-located with DataNodes, Application Master will usually fire ResourceRequests for containers on nodemanagers with data-locality. We can disable this feature:

```
yarn.scheduler.capacity.node-locality-delay=-1
```

This relaxes the constraints of the ApplicationMaster on where it requests containers and will use all NodeManagers in the cluster regardless whether they have data-locality or not.