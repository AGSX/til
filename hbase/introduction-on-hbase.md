# Introduction on HBase

**Date: May 31, 2016**

#### Gist on Hadoop

All the essentials for Hadoop were discussed. From the motivations for the creation of Hadoop to its components.

Hadoop, as emphasized during the day, is not a database that collects various inputs but rather a filesystem. Hence, the existence of HDFS or the Hadoop Distributed File System. Hadoop is a system that handles large data sets of different formats.

A few of the data formats to be handled are:
- script
- SQL
- NoSQL

To be able to support various formats, Hadoop consists of components for file access to handle data of different formats. Pig, Hive and HBase are just some of the tools used to handle various formats.

#### Emphasis on the importance of HBase

A data format that should be considered would be NoSQL formats. Motivation on why NoSQL formats be supported is because of the increasing use of NoSQL, especially for social media data. As an example, social media web sites like Twitter and facebook handles tweets and posts. Basically, posts and tweets contains the name of who posted it, date of post and number of likes / favorites to the tweet or post. But companies want to commoditize these posts in such a way that we can attach, for example, views on the post or how talked about these posts are. These are data that are considered especially because of the volume these data.

Thus, HBase runs on Hadoop to handle semi-structured data formats. HBase is a data access component of Hadoop and it runs on top of Hadoop as a NoSQL database. It is fault tolerant and can handle large data sets.

A thing to point out, during one of the discussions we had is that we should easily distinguish if a data is structured, unstructured or semi-structured as it informs us what component to use, whether Hive, HBase or the other components.

Some unstructured data that HBase will handle includes:
- pictures
- videos
- blog posts
- facebook posts
- tweets

#### References
- [Big Data, What is and Why it matters](http://www.sas.com/en_th/insights/big-data/what-is-big-data.html)
- [Hortonworks Data Platform](http://hortonworks.com/products/hdp/)
- [Apache HBase](http://hortonworks.com/apache/hbase/)
- [Learn Hadoop: The Essentials Series](https://www.youtube.com/playlist?list=PL2y_WpKCCNQeLC4reyP-RaBqfH5QML000)


#### Author

Almer Mendoza
