### AWS VPC Module

This module creates following resources. We are using HA, we are getting first 2 AZ automatically.

* Create VPC
* Internet Gateway with VPC association
* 2 Public subents in 1a and 1b
* 2 private subents in 1a and 1b
* 2 Database subents in 1a and 1b
* Elastic IP
* NAT Gateway in 1a public subnet
* Public Route Table
* Private Route Table
* Database Route Table
* Subnets and Route table associations
* VPC peering if user requests
* Adding the peering route in default VPC, if user dont provide acceptor VPC explicitly.
* Adding the peering routes in public, provate and database rote tables

### Inputs

* Project_name (Required) - your project name
* environment (Required) - which environment you are working
* vpc_cide (Optional) - Default value is 10.0.0.0/16, user can override
* enable_dns_hostnames (Optional) - Default Value is true
* common_tags (Optional) - Better to Provide
* vpc_tags (Optional) - default value is empty, type is map
* igw_tags (Optional) - default value is empty, type is map
* public_subnets_cidr (Required) - user must provide 2 valid public CIDR
* public_subnets_tags (Optional)  - default value is empty, type is map
* private_subnets_cidr (Required) - user must provide 2 valid private CIDR
* private_subnets_tags (Optional) - default value is empty, type is map
* database_subnets_cidr (Required) - user must provide 2 valid database CIDR
* database_subnets_tags (Optional) - default value is empty, type is map
* nat_gateway_tags (Optional) - default value is empty, type is map
* public_route_table_tags (Optional) - default value is empty, type is map
* private_route_table_tags (Optional) - default value is empty, type is map
* database_route_table_tags (Optional) - default value is empty, type is map
* is_peering_required (Optional) - default value is false
* acceptor_vpc_id (Optional)  - default value is default VPC ID
* vpc_peering_tags (Optional) - default value is empty, type is map

### Outputs

* vpc_id - VPC ID created