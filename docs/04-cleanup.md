# Cleanup Steps

To avoid unnecessary AWS costs, the following resources should be deleted after testing.

## EC2 Instances

Terminate the bastion host and private EC2 instances.

## NAT Gateway

Delete the NAT Gateway and release the associated Elastic IP address.

## Internet Gateway

Detach and delete the Internet Gateway.

## Subnets

Delete both the public and private subnets.

## VPC

Delete the VPC once all resources inside it have been removed.

## CloudTrail

Delete the CloudTrail trail and the associated S3 log bucket if it is no longer needed.
