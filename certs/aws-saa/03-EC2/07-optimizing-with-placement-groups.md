# EC2 07 - Optimizing with Placement Groups

- types of placement groups
  - cluster
    - group of instances in a single [[Availability Zone|AZ]]
    - applications that need 
      - low network latency
      - high network [[throughput]]
  - spread
    - group of instances in distinct underlying hardware
    - small number of critical instances that should be separate
  - partition
    - each partition has its own set of racks
    - each rack has its own network and power
    - no two partitions in the same group share the same racks
    - isolate the impact of hardware failure within the application

Review
- cluster = low network latency high [[throughput]]
  - can't span multiple [[Availability Zone|AZ]]
- spread = individual critical instances
- partition = multiple instances: [[HDFS]], [[Apache HBase|HBase]], [[Apache Cassandra|Cassandra]]
- homogenous instances
- can't merge placement groups
- move instance into group after stopping
  - [[Command Line Interface|CLI]] or SDK not console