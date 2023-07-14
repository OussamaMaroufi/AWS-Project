 # Deploy a highly available (HA) web application on AWS

## Objective

The objective of this project is to deploy a highly available (HA) web application on AWS. 
## Deployment

The application is deployed on an EC2 instance within the AWS environment. The following components are required for the environment:

- **Virtual Private Cloud (VPC):** Create a new VPC (not the default one).
- **Public Subnets:** Create 2 public subnets on 2 different availability zones (AZs) and configure the necessary routing tables.
- **Private Subnets:** Create 2 private subnets on 2 different AZs and configure the necessary routing tables.
- **Internet Gateway:** Set up an Internet Gateway.
- **Load Balancer:** Create a Load Balancer that resides within the 2 public subnets.
- **Autoscaling Group:** Configure an Autoscaling group for the EC2 instances hosting the web application. The instances should be placed in the private subnets.
- **NAT Gateways:** Add 2 NAT Gateways in the public subnets to allow EC2 instances to perform updates.
- **MySQL Database:** Create a multi-AZ RDS instance for the MySQL database.
- **Security Groups:** Establish 3 security groups: one for the load balancer, one for the EC2 instances, and one for the bastion host.
- **Bastion Host:** Set up a bastion host machine to allow SSH access to the EC2 instances.

## Setup

Follow the steps below to set up the environment and deploy the application:

1. Create a new VPC using the AWS Management Console or CLI.
2. Configure 2 public subnets and 2 private subnets, each on a different AZ. Set up the necessary routing tables.
3. Create an Internet Gateway and attach it to the VPC.
4. Set up a Load Balancer within the public subnets.
5. Configure an Autoscaling group for the EC2 instances and place them in the private subnets.
6. Add 2 NAT Gateways in the public subnets.
7. Create a multi-AZ RDS instance for the MySQL database.
8. Configure the required security groups for the load balancer, EC2 instances, and bastion host.
9. Set up a bastion host machine to enable SSH access to the EC2 instances.
10. Update the security groups of the EC2 instances to allow SSH access only via the bastion host.
## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to submit a pull request.

The following diagram illustrates the architecture of the project
![Screenshot from 2023-07-14 11-13-39](https://github.com/OussamaMaroufi/AWS-Project/assets/93825558/cc8ef1f1-74ad-4383-ba07-9e4bf8889f5b)
