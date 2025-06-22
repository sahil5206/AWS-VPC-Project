# AWS-VPC-Project
This repository provides the approach to build the project on AWS Virtual Private Cloud (VPC).

We will follow the following diagram for making our VPC Project.
![Diagram of the VPC Project](https://github.com/user-attachments/assets/2f81739c-2742-4a60-857e-2d0389112c5e)


# FIRST STEP - CREATE THE VPC
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

# SECOND STEP - CREATE EC2 INSTANCES IN THE PRIVATE SUBNET
1. Go to the EC2 service dashboard and create two EC2 instances(private) one in each availability zones.
2. you will see that you there is no public IP Address of those private subnet instances.
3. bu you cannot access those private instances directly, you have to create a public instances named - 'Bastion Host' or 'Jump Server'.![EC2 Instances](https://github.com/user-attachments/assets/2c9fba92-6c4d-468e-ac6b-88f6a4bf9343)

4. Use the same 'Key-Pair' for every instance in this VPC project.
5. Deploy your application in the private Instance - We have the deployed the basic html page(code provided in this repository).
 But you cannot access the private instance directly
6. Copy the Key-Pair's .pem file to the Batsion Host Instance manually. 

![.pem file in Bastion Host](https://github.com/user-attachments/assets/33817fff-4323-4690-ad5b-31979f73db20)

7. use the following command for connecting your PC with the Bastion Host

   `chmod 400 your-key.pem`
   
   `ssh -i your-key.pem ubuntu@<Bastion-Public-IP> `
