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
many task nodes. In fact, task nodes are scaled up and down depending upon workload in the
cluster.

### Core + Task Scaling


### Minimum 5 min frequency


### Scaling in terms of number of instances


### Static Scale up


### Opaque scaling policy


## References

* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-scale-on-demand.html
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html
* https://aws.amazon.com/blogs/big-data/best-practices-for-resizing-and-automatic-scaling-in-amazon-emr/
