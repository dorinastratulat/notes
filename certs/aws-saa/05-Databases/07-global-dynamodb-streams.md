- steams
	- time ordered sequence of item level changes in table
		- [[FIFO]] streams of data
	- stored for 24 hours
	- sequence broken up into shard
	- inserts, updates, deletes
	- combine with [[lambda]] for functionality like stored procedures
- global tables
	- managed multi-master multi-[[region]] replication
	- globally distributed applications
	- based on [[DynamoDB]] streams
	- multi-[[region]] redundancy for disaster recover or [[high availability]]
	- no application rewrites
	- replication latency < 1 second

Review
- 