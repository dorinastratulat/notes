
### Create the VPC
1. go to AWS console
2. go to VPC
	1. notice 1 default VPC for every [[region]]
3. Click "Your VPCs" on left sidebar
4. Click orange "Create VPC" button
5. Select "VPC Only"
6. Give VPC a name
7. Select [[IPv4]] [[CIDR]] block
	1. Input `10.0.0.0/16` netmask `/16`
8. Select "Default" tenancy
9. Click "Create VPC"
10. This will create the VPC, and a default route table and security group

### Create the Subnets
1. Click "Subnets" on left sidebar
2. Click orange "Create Subnet"
3. Select VPC you just created
4. Give the subnet a name
5. Select an [[Availability Zone]]
6. Give it [[IPv4]] [[CIDR]] address range with netmask greater than VPC
	1. `10.0.1.0/24` netmask `/24`
7. Click "Create Subnet"

Create second subnet with above instructions with [[CIDR]] range `10.0.2.0/24`

Note: AWS reserves the first 4 and last [[IP]] addresses in each [[CIDR]] `/24` block

### Set up Public Subnet
1. Click "Subnets" on left sidebar
2. Select VPC you want to be public
3. Click "Actions"
	1. Click "Edit Subnet Settings"
	2. Check "Enable auto-assign public IPv4 address"

1. Click "Internet Gateways" on left sidebar
2. Click orange "Create internet gateway"
3. Give gateway a name
4. Go back to "Internet Gateway" on left sidebar
5. Select newly created gateway
6. Click "Actions"
	1. Click "Attach to VPC"
	2. Select our new VPC
	3. Click "Attach"

1. Click "Route Tables" on left sidebar
2. Click "Create route table"
3. Give route table a name
4. Select our new VPC
5. Click "Create route table"
6. Click "Edit routes"
	1. Add route
		1. Destination - `0.0.0.0/0`
		2. Target - our new internet gateway
	2. Click save
7. Click "Subnet associations" tab
8. Click "Edit subnet associations"
	1. Select the subnet we want to be public
	2. Click save