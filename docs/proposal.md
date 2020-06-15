## Problem

AWS provides [Elastic Map Reduce (EMR)](https://aws.amazon.com/emr/) service to run
[Spark](https://spark.apache.org/) workloads. Spark is one of the most popular framework
used to run Big Data workloads across many enterprises and startups.

AWS EMR is a great fit for running spark jobs. It runs 1 master node, many core and task
nodes as part of an EMR cluster. Master node runs all the controller services such as
yarn, HDFS master; core nodes run node manager as well as HDFS worker whereas task nodes
only run node managers. This means that core nodes can run jobs as well as provide storage
for HDFS where task nodes only provide compute for the jobs running in the cluster.

A common configuration for EMR cluster is to run 1 master node, a few core nodes (2-4) and
many task nodes. Task nodes are often scaled up and down depending upon workload in the
cluster. AWS EMR provides
[managed scaling](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html)
to ease the task of scaling the nodes in the cluster. Combined with
[Instance Fleet](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html),
EMR provides flexibility to choose types of nodes, policy for scaling up and down etc.


### Core + Task Scaling

You cannot specify scaling policies separately for Core nodes and task nodes. Often, task
nodes are scaled whereas core nodes are kept constant in number givent that core nodes
manage the data that reside on HDFS and takes longer to scale up or down.

### Minimum 5 min frequency

The managed 

### Scaling in terms of number of instances


### Static Scale up


### Opaque scaling policy


## References

* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-scale-on-demand.html
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html
* https://aws.amazon.com/blogs/big-data/best-practices-for-resizing-and-automatic-scaling-in-amazon-emr/
