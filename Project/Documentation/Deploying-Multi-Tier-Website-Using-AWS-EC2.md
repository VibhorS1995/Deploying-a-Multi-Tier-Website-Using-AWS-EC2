
Project 1 - Deploying a Multi-Tier Website Using AWS EC2

Topic: Deploy a Multi-tier website using EC2 
Description: Amazon Elastic Compute Cloud (Amazon EC2) provides scalable computing capacity in the Amazon Web Services (AWS) cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic. 

Problem Statement: 
Company ABC wants to move their product to AWS. They have the following things setup right now: 
1. MySQL DB 
2. Website (PHP) 

The company wants high availability on this product, therefore wants autoscaling to be enabled on this website. 

Solution:
Created an Ubuntu EC2 instance, installed php and mysql client on it.  

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture1.png)

#!/bin/bash
sudo apt-get update -y
sudo apt-get install apache2 -y
sudo add-apt-repository -y ppa:ondrej/php
sudo apt install php5.6 mysql-client php5.6-mysqli -y

Created a RDS database.

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture2.png)
 
Using filezilla copy the code to Ec2 instance.

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture3.png)


Created a table data.

CREATE TABLE data (
    firstname varchar(255),
    email varchar(255)
);

Tested the website:

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture4.png)
 

Checked the table and data has been added in data table. 

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture5.png)  

Created an AMI for the EC2 machine that we have configured.

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture6.png)  

Created a Launch configuration:

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture7.png)  

 Created an Application Load balancer:

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture8.png)  


Created Auto scaling group to make the website highly available:

![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/tree/main/Project/Diagrams/Picture9.png) 


Tested the website using the DNS name of Load balancer:
  
 ![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/raw/main/Project/Diagrams/Picture10.png)   

Value is added to the table.

 ![image](https://github.com/VibhorS1995/Deploying-a-Multi-Tier-Website-Using-AWS-EC2/main/Project/Diagrams/Picture11.png) 

 
