# Deploying a Multi-Tier Website Using AWS EC2

## Project Overview
This project demonstrates how to deploy a multi-tier website using Amazon EC2. Amazon EC2 provides scalable computing capacity in the AWS cloud, eliminating the need to invest in hardware up front and enabling faster development and deployment of applications.

## Problem Statement
Company ABC wants to move their product to AWS. They have the following setup:
- MySQL Database
- PHP Website

The company seeks high availability for this product and requires auto-scaling enabled on this website.

## Architecture Diagram
![Architecture Diagram](Project/Diagrams/architecture.png)

## Project Components
1. **MySQL Database**: Hosted on an Amazon RDS instance.
2. **PHP Website**: Deployed on an EC2 instance with auto-scaling and load balancing.

## Steps to Deploy
1. **Set Up MySQL Database**:
    - Create an RDS instance.
    - Configure security groups and VPC.
2. **Deploy PHP Website**:
    - Launch an EC2 instance and install LAMP stack.
    - Deploy the PHP application.
    - Configure auto-scaling and load balancing using Amazon EC2 Auto Scaling and Elastic Load Balancing (ELB).

## Prerequisites
- AWS Account
- Basic knowledge of AWS services
- MySQL and PHP knowledge

## Detailed Documentation
Please refer to the [Documentation](Project/Documentation/Deploying-Multi-Tier-Website-Using-AWS-EC2.md) for detailed steps and configurations.

## Source Code
Find the source code in the [SourceCode](Project/SourceCode) folder.

## Conclusion
By following the steps outlined in this project, Company ABC can successfully migrate their product to AWS, ensuring high availability and scalability.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
