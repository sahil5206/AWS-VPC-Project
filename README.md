# AWS-VPC-Project
This repository provides the approach to build the project on AWS Virtual Private Cloud (VPC).

We will follow the following diagram for making our VPC Project.
![Diagram of the VPC Project](https://github.com/user-attachments/assets/2f81739c-2742-4a60-857e-2d0389112c5e)


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

You will get your Resource Map, you can go through it for understanding the flows and connection in your VPC.
![Resource Map](https://github.com/user-attachments/assets/c98db7d9-afb4-4ad2-a5e4-16e1996a35cd)

