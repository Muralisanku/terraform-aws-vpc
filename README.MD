##### AWS VPC Module

This module creates following resources. We are using HA, we are getting first 2 AZ's automatically.
* Create VPC
* Internet Gateway with VPC associations
* 2 public subnets in 1a and 1b
* 2 private subnets in 1a and 1b
* 2 database subnets in 1a and 1b
* Create Elastic IP
* NAT Gateway in 1a public subnet
* Public route table
* private route table
* database route table
* Subnets and Route table associations
* VPC Perring if user requests
* Adding the peering route in default VPC, if user dont provide acceptor VPC explicitly
* Adding the peering routes in public, prvate and database route tables

### Inputs
* Project_name (Required) - Your project name
* environment (Required) - Which environment you are working in
* vpc_cidr (Optional) - Default value is 10.0.0.0/16, user can override
* enable_dns_hostnames (Optional) - Default value is true
* common_tags (Optional) - Better to provide
* vpc_tags (Optional)
* igw_tags (Optional)
* public_subnets_cide (Required) - User must provide 2 valid public subnets CIDR
* public_subnets_tags (Optional)
* private_subnets_cide (Required) - User must provide 2 valid private subnets CIDR
* private_subnets_tags (Optional)
* database_subnets_cide (Required) - User must provide 2 valid database subnets CIDR
* database_subnets_tags (Optional)
* nat_gateway_tags (Optional)
* public_route_table_tags (Optional)
* public_route_table_tags (Optional)
* database_route_table_tags (Optional)
* is_peering_required (Optional) - default value is false
* acceptor_vpc_id (Optional) - default value is default VPC ID
* vpc_peering_tags (Optional) - default value is empty, type is map

#### Output

* vpc_id - VPC ID created