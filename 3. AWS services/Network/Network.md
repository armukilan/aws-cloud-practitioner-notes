# Network

[Network](1.png)

## Enterprise/ Hybrid Networking

[Network](2.png)

## VPC

Virtual Private cloud is a logically isolated section of AWS network where you launch your AWS resources. You choose a range of IPs using CIDR range

CIDR range of 10.0.0.0/16 = 65536 address

Subnets - A logical part of IP network into multiple smaller network segments. You are breaking up your IP range for VPC into smaller network.

Subnets need to have a smaller CIDR range than to the VPC represent their portion
eg. Subnet CIDR range 10.0.0.24/24 = 256 IP Address

[Network](3.png)

Public subnet is one that can reach internet and private subnet is ne that cannot reach internet. 

## Security Group vs NACL

[Network](4.png)

Visit cidr.xyz