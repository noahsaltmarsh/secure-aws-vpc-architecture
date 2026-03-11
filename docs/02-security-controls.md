# Security Controls

Several security controls were implemented to protect the environment.

## Network Isolation

Public and private subnets were used to separate internet-facing resources from internal resources.

Private EC2 instances do not have public IP addresses.

## Bastion Host Access

Administrative access to private systems is restricted through a bastion host.

Users must connect:

Laptop → Bastion → Private EC2

This prevents direct internet access to internal servers.

## Security Groups

Security groups act as virtual firewalls controlling inbound and outbound traffic.

Rules implemented include:

- SSH access allowed to bastion host
- SSH access from bastion to private instance
- All other inbound traffic blocked

## CloudTrail Logging

AWS CloudTrail was enabled to record all API activity.

This provides:

- audit trails
- infrastructure monitoring
- incident investigation capability
