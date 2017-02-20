Q.List the components of Hadoop 2.x and explain them in detail.
Ans:
The components of Hadoop 2.x are:
1)HDFS
2)MapReduce
3)Yarn

1)HDFS
-HDFS is a filesystem designed for storing very large files with streaming data access patterns, running on clusters of commodity hardware.
-Very large here means hundreds of megabytes,gigabytes and terabytes of data.
-Petabytes of data are being stored by many hadoop clusters nowadays.
-HDFS is built around the idea that the most efficient data processing pattern is a write-once, read-many-times pattern
-Hadoop doesn’t require expensive, highly reliable hardware to run on. It’s designed to run on clusters of commodity hardware for which the chance of node failure across the cluster is high, at least for large clusters.HDFS is designed to carry on working without a noticeable interruption to the user in the face of such failure.
-HDFS blocks are large compared to disk blocks, and the reason is to minimize the cost.
-By making a block large enough, the time to transfer the data from the disk can be made to be significantly larger than the time to seek to the start of the block.Thus the time to transfer a large file made of multiple blocks operates at the disk transfer
rate.
-An HDFS cluster has two types of node operating in a master-worker pattern: a namenode and a number of datanodes.
-The namenode manages the filesystem namespace. It maintains the filesystem tree and the metadata for all the files.This information is stored persistently on the local disk in the form of two files: the namespace image and the edit log.
-Datanodes are the workhorses of the filesystem. They store and retrieve blocks when they are told to (by clients or the namenode), and they report back to the namenode periodically with lists of blocks that they are storing.

2)MapReduce
-MapReduce is a core component of the Apache Hadoop software framework.
-Hadoop enables resilient, distributed processing of massive unstructured data sets across commodity computer clusters, in which each node of the cluster includes its own storage.
-MapReduce serves two essential functions: It parcels out work to various nodes within the cluster or map, and it organizes and reduces the results from each node into a cohesive answer to a query.
-MapReduce is composed of several components, including:
JobTracker -the master node that manages all jobs and resources in a cluster
TaskTrackers -agents deployed to each machine in the cluster to run the map and reduce tasks
JobHistoryServer -a component that tracks completed jobs, and is typically deployed as a separate function or with JobTracker

3)YARN
-Apache Hadoop YARN (Yet Another Resource Negotiator) is a cluster management technology.
-YARN is one of the key features in the second-generation Hadoop 2 version of the Apache Software Foundation's open source distributed processing framework.
-YARN is now characterized as a large-scale, distributed operating system for big data applications.
-, YARN is a software rewrite that decouples MapReduce's resource management and scheduling capabilities from the data processing component, enabling Hadoop to support more varied processing approaches and a broader array of applications.
-YARN combines a central resource manager that reconciles the way applications use Hadoop system resources with node manager agents that monitor the processing operations of individual cluster nodes.
 
