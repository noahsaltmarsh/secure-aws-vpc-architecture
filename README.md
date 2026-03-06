# secure-aws-vpc-architecture

# Secure AWS VPC Architecture

## Project Overview

This project demonstrates how to design and deploy a secure AWS network architecture using industry security best practices.

The environment includes:

- Custom Virtual Private Cloud (VPC)
- Public and private subnets
- Internet Gateway
- NAT Gateway for outbound private traffic
- Bastion host for secure administrative access
- Private EC2 instance isolated from the internet
- Security Groups and Network ACLs for layered network security
- IAM roles implementing least-privilege access
- AWS CloudTrail for API activity auditing
- Amazon GuardDuty for threat detection

This project simulates a real-world cloud security environment where sensitive systems are isolated in private networks and accessed securely through controlled entry points.

---

## Architecture Overview

The architecture separates resources into public and private network segments.

Public Subnet
- Bastion Host (SSH entry point)
- NAT Gateway for outbound traffic

Private Subnet
- Internal EC2 instance
- No direct internet access

Traffic Flow

User → Bastion Host → Private EC2  
Private EC2 → NAT Gateway → Internet

---

## Security Features

This architecture implements multiple layers of security:

- Network segmentation using VPC and subnets
- Bastion host controlled SSH access
- Security Groups restricting inbound traffic
- Network ACLs enforcing subnet-level rules
- IAM roles preventing credential exposure
- CloudTrail logging all API actions
- GuardDuty detecting suspicious behavior

---

## Skills Demonstrated

AWS Cloud Networking  
VPC Architecture Design  
Network Security (Security Groups & NACLs)  
Identity and Access Management (IAM)  
Security Monitoring (CloudTrail & GuardDuty)

---

## Project Documentation

Architecture Diagram  
docs/00-architecture.md

Build Process  
docs/01-build-steps.md

Security Configuration  
docs/02-security-controls.md

Validation Testing  
docs/03-validation-tests.md

Cleanup and Cost Control  
docs/04-cleanup.md
