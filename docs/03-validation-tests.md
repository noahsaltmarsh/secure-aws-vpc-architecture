# Validation Tests

Several tests were performed to verify that the architecture was functioning correctly.

## Bastion SSH Access

Successfully connected from the local machine to the bastion host using SSH.

## Private Instance Access

From the bastion host, SSH access to the private EC2 instance was verified.

This confirmed that internal network communication was functioning.

## Internet Access from Private Instance

The following command was executed from the private instance:

curl https://google.com

The successful response confirmed that the NAT gateway allowed outbound internet connectivity.

## CloudTrail Logging

CloudTrail was verified to be active and logging AWS infrastructure events such as EC2 instance creation and security group modifications.
