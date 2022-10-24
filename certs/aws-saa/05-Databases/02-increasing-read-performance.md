# Databases 02 - Increasing Read Performance with Read Replicas

- read replica
	- read-only copy of the primary database
	- great for read-heavy workloads
	- takes load off primary database
	- scenario 
		- multi-[[Availability Zone|AZ]]     = disaster recovery
		- read-replica = performance
	- can be separate or same [[Availability Zone|AZ]]
	- can be cross-[[region]]
	- each read-replica has its own DNS endpoint
	- replicas can be promoted to their own database
		- this breaks replication
- key facts
	- replicas all about scaling performance, not disaster recovery
	- must have auto backups enabled to deploy read replica
	- multiple read replicas are supported
		- up to 5 replicas per database instance

Review
- when to use multi-[[Availability Zone|AZ]]
	- **exact copy** of prod db in different [[Availability Zone|AZ]]
	- used for disaster recovery
	- in event of failure, [[RDS]] will automatically failover to the standby
- when to use read-replica
	- **read-only copy** of primary db
	- same [[Availability Zone|AZ]], cross [[region]], [[Availability Zone|AZ]]
	- scale read performance
	- good for read-heavy workloads to take load off primary database for read-only workloads 