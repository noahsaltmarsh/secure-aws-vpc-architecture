# Architecture Overview

This project implements a secure AWS Virtual Private Cloud (VPC) architecture designed to isolate internal resources while allowing controlled administrative access and outbound internet connectivity.

The environment includes:

- A dedicated VPC network
- Public and private subnets
- A bastion host for secure administrative access
- A NAT gateway to allow outbound internet traffic from private resources
- Security groups controlling network access
- AWS CloudTrail for infrastructure logging and auditing

## Network Layout

The VPC contains two primary subnet types:

### Public Subnet
The public subnet contains the bastion host. This instance has a public IP address and can be accessed from the internet using SSH.

### Private Subnet
The private subnet contains internal EC2 instances that do not have public IP addresses and cannot be accessed directly from the internet.

## Access Path

Administrative access follows this path:

User Laptop → Bastion Host → Private EC2

This architecture ensures that private systems are never directly exposed to the public internet.

## Internet Connectivity

Private instances require internet access for tasks such as installing software updates. This is provided through a NAT Gateway.

Private EC2 → NAT Gateway → Internet

The NAT gateway allows outbound traffic but blocks inbound connections.
