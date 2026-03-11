# Build Steps

The following steps were used to deploy the secure VPC environment.

## 1. Create VPC

A new VPC was created with the CIDR block:

172.31.0.0/16

This provides the internal IP range for all resources in the network.

## 2. Create Subnets

Two subnets were created:

Public Subnet – used for the bastion host  
Private Subnet – used for internal servers

## 3. Internet Gateway

An Internet Gateway was attached to the VPC to allow public resources to communicate with the internet.

## 4. NAT Gateway

A NAT Gateway was deployed inside the public subnet to allow outbound internet traffic from private resources.

## 5. Route Tables

Two route tables were configured.

Public Route Table
- Routes traffic to the Internet Gateway

Private Route Table
- Routes internet traffic through the NAT Gateway

## 6. Bastion Host

An EC2 instance was deployed in the public subnet and configured as a bastion host.

SSH access is allowed only through the bastion.

## 7. Private EC2 Instance

An internal EC2 instance was deployed in the private subnet with no public IP address.

## 8. Security Groups

Security groups were configured to allow:

- SSH access to the bastion host
- SSH access from the bastion to the private instance
