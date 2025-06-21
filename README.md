# AWS-VPC-Project
This repository provides the approach to build the project on AWS Virtual Private Cloud (VPC).

#FIRST STEP - CREATING THE VPC
1. Go to the AWS VPC service and click Create VPC .
2. Select 'VPC and more' and provide the name for your VPC.
3. Provide the IP Address Range (for 65,536 IPs, enter 10.0.0.0/16).
4. Enter the number of availability Zones - In this project we have made 2 availability zones.
5. Then enter the number of subnets - we have 2 public subnets in this project.
6. Then enter the number of private subnets - we have made 2 private subnets in this project(1 in each public subnet).
7. Enter the number of NAT gateways - we have not used NAT gatewasy in our project as it is a paid service and does not provide a free-tier.
8. Then choose the end point (S3 Gateway) - But we used none in this project, we have only the internet gateway(igw) only which is necessary and default.
9. Enable both DNS options.
10. Then create Create VPC .
