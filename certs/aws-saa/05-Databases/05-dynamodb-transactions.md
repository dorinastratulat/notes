- [[ACID]]
	- atomic
		- all changes to data must be performed successfuly or not at all
	- consistent
		- data must be in a consistent state before and after transaction
	- isolated
		- no other process can change the data while the transaction is running
	- durable
		- changes made by a transaction must persist
- [[ACID]] with [[DynamoDB]]
	- [[DynamoDB]] transactions provide [[ACID]] across 1 or more tables within a single AWS account and [[region]]
	- applications that require coordinated inserts, deletes, updates to multiple items as part of a single logical business operation
- all or nothing
	- transaction succeeds across one or more tables or transaction fails
- use cases
	- processing financial transactions
	- fulfilling and managing orders
	- multiplayer game engines
	- coordinating actions across distributed components and services
- transactions
	- multiple all-or-nothing operations
	- 3 options for reads
		- eventual consistency
		- strong consistency
		- transactional
	- 2 options for writes
		- standard
		- transactional
	- up to 25 items or 4MB of data per transaction

Review
- any scenario that mentions [[ACID]] = [[DynamoDB]] transaction
- transactions provide [[ACID]] across 1+ dables in a single AWS account and [[region]]
- all-or-nothing transactions