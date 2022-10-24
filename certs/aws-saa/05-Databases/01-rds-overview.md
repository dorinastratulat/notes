---
date created: 2022-10-19 15:15
date updated: 2022-10-19 15:16
---

# Databases 01 - [[RDS]] Overview

- Relational Database Service
	- [[RDBMS]] support
		- [[Microsoft SQL Server|SQL Server]]
		- [[Oracle Database]]
		- [[MySQL]]
		- [[PostgreSQL]]
		- [[MariaDB]]
		- [[Amazon Aurora]] ([[PostgreSQL]] & [[MySQL]] compatible)
	- up and running in minutes
	- multi-[[Availability Zone|AZ]]
	- failover capability
	- automated backups
	- used for [[OLTP]]
- [[OLTP]] vs [[OLAP]]
	- [[OLTP]]
		- process data from transactions in real time
			- orders, banking, payments, booking
		- large number of small transactions in real time
	  - [[OLAP]]
		- complex queries to analyze historical data
		- large amounts of data
		- queries that take time to complete
		- [[Big Data]]
- Multi-[[Availability Zone|AZ]]
	- [[RDS]] creates exact copy of prod DB in another [[Availability Zone|AZ]]
	- handles replication for you
	- writing to prod writes to the standby/replica
	- available
		- [[Microsoft SQL Server|SQL Server]]
		- [[MySQL]]
		- [[MariaDB]]
		- [[Oracle Database]]
		- [[PostgreSQL]]
	- [[RDS]] will automatically fail over to the standby during a failure
	- database operations can resume quickly without intervention
	- secondary is promoted to primary
	- not for performance improvements, can't connect to secondary when primary is active
