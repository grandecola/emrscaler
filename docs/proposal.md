## Problem

AWS provides [Elastic Map Reduce (EMR)](https://aws.amazon.com/emr/) service to run
[Spark](https://spark.apache.org/) workloads. Spark is one of the most popular framework
used to run Big Data workloads across many enterprises and startups. While AWS EMR is
a great fit for running spark jobs, there are many challenges that one would face.

### Slow Startup
EMR is supposed to be an ephemeral compute. It is recommended that an EMR cluster is
started before jobs are started, and stopped once jobs complete. 

### Core + Task Scaling

### Minimum 5 min frequency

### Scaling in terms of number of instances

### Static Scale up

### Opaque scaling policy


https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-scale-on-demand.html
https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html
https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-fleet.html
https://aws.amazon.com/blogs/big-data/best-practices-for-resizing-and-automatic-scaling-in-amazon-emr/
