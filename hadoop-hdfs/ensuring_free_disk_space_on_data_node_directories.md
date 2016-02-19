# Ensuring Free Disk Space on Data Node Directories

**Date: Feb 19, 2016**

If you currently have data node directories which includes a disk that's about to get full, try setting these attributes for HDFS in Ambari:

- `dfs.datanode.available-space-volume-choosing-policy.balanced-space-preference-fraction` - 1.0. This absolutely chooses disks with more space versus ones without space.
- `dfs.datanode.du.reserved` - 1073741824 bytes (1GB) is the defaut. Increase this to desired value. This setting ensures that if the **free space** of a specific data node directory/volume is about to hit this value, HDFS will no longer assign blocks to this directory. It gives breathing space and provides Non-HDFS disk space for your disks. 
    - Tip: For an easier time setting the value, use Google's Bytes to GB converter. Go to Google, search for "unit converter", a dropdown will appear, and select "Digital Storage".

After doing this, restart your HDFS cluster and run `hdfs balancer -policy blockpool -threshold 100`. By default, balancer policy uses `datanode` as it's value, `blockpool` is a stricter balancer. It ensures the balance of blocks down to the blockpool level. Your disks should be able to breathe now.

This worked with `HDP-2.2` and above.
